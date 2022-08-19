# When to run a Chaos Day

To identify the best time to run your Chaos Day, you should first decide whether the experiments should occur on a single day or be spread over a few days:

* Opting for a single Chaos Day results in a more intensive but shorter event, for both Agents of Chaos and those responding to the chaos. While this approach adds stress, our experience is that the intensity also improves team dynamics and leads to a more memorable event that the team will talk about for years to come. On the downside, it can be harder to maintain the element of surprise, especially if experiments are being run in a pre-production environment. Teams need to be informed to treat failures in this environment as though production were on fire, and so it’s likely they’ll be paying close attention to that environment during that time. Plus, once the first experiment is over, the team is likely to realise Chaos Day is upon them!
* Spreading the chaos over a few days allows more of the team to be involved in brainstorming  experiments, but still maintains an element of surprise because they won’t know exactly when experiments will be run during the chosen period. It’s unlikely they will remain hypervigilant for the whole of the period, so when failures do occur there will be an element of surprise. Spreading the experiments out allows adjustments to be made to each experiment over the period, because lessons from earlier experiments can be used to improve the execution of later ones.
* If this is your first Chaos Day, we recommend starting small and learning the ropes by just running a few experiments on a single day.

The next step is to fix a date for the experiments.&#x20;

### This should be at least a couple of weeks after the planning session to allow engineering time to design, implement and test the experiments.&#x20;

Check if other teams have any key dependencies on the target environment and services over the Chaos Day, to avoid impacting them should the failures ripple out too far and for too long!

Once a date has been agreed, inform the participating teams and reiterate that:

1. Supporting teams should treat this as a regular day, and keep busy doing regular work, not watching and waiting for the chaos to unfold.
2. If an issue is observed in the target environment during that period, it should be treated as though it were a production issue. Agree on what communication channel should be used for incident response, though, as you may want to keep your production channel clear in case real production incidents occur at the same time!

Finally, book a physical or virtual space so that the Agents of Chaos can collaborate more effectively on the experiments. They should also have their own private communication channel (e.g. a Slack private channel), ideally set up as soon as the group’s members have been identified.
