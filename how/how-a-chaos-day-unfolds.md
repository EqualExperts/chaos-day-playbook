# How a Chaos Day unfolds

As with any team activity, having a single person be the nominated facilitator/lead will make the Chaos Day or Week run more smoothly. Ideally, this should be someone who has been involved in the meetings leading up to this point, but not one of the Agents of Chaos as they’ll likely focus on individual experiments.

At the start of the Chaos Day / Week, the facilitator should remind all participants:

* Which environment is being targeted
* To treat failures observed in that environment as though Production was on fire (e.g. use standard incident response procedures)
* Which communication channel to use to report and collaborate on failures (we recommend using whichever channel you normally use for issues in a given environment).

Once the Agents of Chaos start running the experiments, the facilitator should help them:

1. Document what they’re doing, in a similar manner to documenting a production incident. Knowing who did what, when and why provides more data to harvest during the Chaos Day retrospectives.
2. Ensure not too many experiments are run in parallel and know when to stop, ramp down or ramp up experiments. Keep an eye on how service teams are responding to the experiments, in case they are being overwhelmed by incidents. We’ve found that using a simple kanban board (e.g. Trello) to show which experiments are in progress can be helpful to visualise what’s in progress, still to do, done, etc.
3. Draw the experiments to a close and return the environment to its normal state. Don’t leave this too late in the day/week, as some failures can be harder to rollback than first thought. Remember to restore any logging and/or alerting configuration changes. Let participants know when the chaos event is over, so they can respond appropriately should an incident occur in the target environment.
4. Kick off the retrospective process (covered in the next section).
