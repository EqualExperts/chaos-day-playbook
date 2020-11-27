# Who to involve in a Chaos Day

![](../.gitbook/assets/image%20%283%29.png)

Having decided which service\(s\) to experiment on, three groups of people need identifying:

1. _Stakeholders_ are anyone connected with the service who’d benefit from lessons drawn out by a Chaos Day. It’s not just the team’s engineers that can gain new insights: designers, product owners and delivery managers all contribute to a system’s design, implementation and operation and so also all have a stake in its resilience. For instance, a designer and a product owner both need to be cognisant of how failures ripple through a system and ultimately impact end-users.
2. _Responders_ are whoever normally responds to service incidents. If you’re practising the principle of [you build it, you run it](https://queue.acm.org/detail.cfm?id=1142065), then this will be the team that owns the service. In other cases, it may be a support or operations team removed from the engineering team. Either way, to maximise the realism and learning opportunities of a Chaos Day, include responders as much as possible throughout the process.
3. _Agents of chaos_ are the engineers who’ll be designing and running the actual experiments. For a team’s first Chaos Day, these people should be two or more of the most experienced engineers on the team\(s\). If several teams are involved, then take the most experienced engineer from each team. This has two benefits. Firstly, it uncovers knowledge gaps within the team, because these engineers are non-contactable during the Chaos Day itself. Secondly, the experiments they design tend to more realistically reflect real-world failures as well as explore system failure modes less known to other engineers.

Common problems in identifying these groups are:

1. Not all collaborators are identified \(e.g. teams that own downstream systems\) and/or involved in the Chaos Day process - Nora Jones describes this as [Trap 2 of the 8 traps of Chaos Engineering](https://medium.com/@njones_18523/chaos-engineering-traps-e3486c526059). Although it’s costly getting everyone involved in the various meetings, people learn new things throughout the process, as different mental models are discussed, experiments proposed, executed and reviewed.
2. The team struggles to cope without their most experienced engineer. In one Chaos Day we ran, the responding team had to drag their agent of chaos back in, to resolve the failure they had induced. If you think this might happen to your team, then consider making the experient design and execution process open to the team, as described in the [Experiment Design](what-experiments-to-run-on-a-chaos-day.md) and [Execution](how-a-chaos-day-unfolds.md) sections.

