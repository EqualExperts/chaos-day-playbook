# When to run a Chaos Day

The first decision to make when deciding when to run your Chaos Day is whether the experiments should occur on a single day or be spread over a few days:

* Opting for a single Chaos Day results in a more intensive but shorter event, for both the Agents of Chaos and those responding to the chaos. Although this adds stress, our experience is that the intensity improves team dynamics and leads to a more memorable event - something the team will talk about for years to come. On the downside, it can be harder to maintain the element of surprise, especially if experiments are being run in a pre-production environment. Teams need to be informed to treat failures in this environment as though production were on fire, and so it’s likely they’ll be paying close attention to that environment during that time. Plus, once the first experiment is over, the team are likely to realise Chaos Day is upon them!
* Spreading the chaos out over a few days allows more of the team to be involved in brainstorming the experiments, but still maintains an element of surprise as they won’t know which experiments will be run when over the chosen period. It’s also unlikely they’d be able to remain hypervigilant for the whole of the period, so when failures do occur there will be an element of surprise. Spreading the experiments out also enables more attention and tuning to be made to each experiment run over the period, as the lessons from earlier experiments can be used to improve the execution of later ones.
* If this is your first Chaos Day, we recommend starting small though and learning the ropes by just running a few experiments on a single day.

The next step is to fix a date for the experiments, at least a couple of weeks after the planning session to allow engineering time to design, implement and test the experiments. Check if other teams have any key dependencies on the target environment and services over the Chaos Day, to avoid impacting them should the failures ripple out too far and for too long!

Once a date has been agreed, inform the participating teams and reiterate that:

1. Supporting teams should treat this as a regular day, and be busy doing regular work, not watching and waiting for the chaos to unfold.
2. If an issue is observed in the target environment during that period, it should be treated as though it were a production issue. Agree on what communication channel should be used for incident response, though, as you may want to keep your production channel clear in case real production incidents occur at the same time!

Finally, book a physical or virtual space for the agents of chaos to work together in, so they can collaborate more effectively on the experiments. They should also have their own private communication channel (e.g. a Slack private channel), ideally set up as soon as the group’s members have been identified.
