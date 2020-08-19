# 5-minute guide

## 5-minute guide to running a Chaos Day

This section is a bare-bones version of the what and how of running a Chaos Day.  The rest of the playbook expands each step, covering the key outcomes, common problems and examples of application.

If you already know [what Chaos Days](what-and-why.md#what-benefits-do-chaos-days-provide) are, [why they are beneficial](what-and-why.md#why-chaos) and that you’re [ready to run one](ready-for-chaos.md), read on.  If you’d first like to get a firmer understanding, skip over this section and read [What and why](what-and-why.md). 

The steps for running a Chaos Day are

1. Plan who, what, when, where.
2. Execute the experiments.
3. Review execution, impact, response and chaos mechanics.
4. Share knowledge gained.

![](https://lh6.googleusercontent.com/niygH5itfxmuGxV_Kckfm4It0AFc6x4p3X38IUrYOXF2Kv6rrFNcBpXmcN5MCrzbNKtwVkod2yUcdtIaQZfAiLPljlCUAY6dJ5vIJNwG1Xyp-Qwap5ChCYO9qtepieFXePhZSHjxiug)

### Chaos planning

1. Start small: involve one or two teams, not the entire engineering group.
2. Identify a few of the most experienced engineers across those teams.  They will be the _agents of chaos_, who will design and execute the experiments.
3. At least two weeks ahead of Chaos Day, facilitate a planning session with the agents of chaos.  Draw the system architecture on a whiteboard \(or [remote equivalent](https://remote-working.playbook.ee/remote-working-runbooks/remote-workshops)\), then use post-its and/or a Trello board to brainstorm possible experiments that simulate a failure that your system should tolerate.  Don’t focus on failures that you have no control over, such as an outage within your cloud provider, as they have low learning value. For each experiment, consider:  
   1. Failure mode \(e.g., partial connectivity loss, an instance being terminated, network slowdown\).  
   2. Expected impact in both technical and business terms \(e.g., dependant services fail, or in-progress customer transactions are halted\).  
   3. Anticipated response \(e.g., the service auto-heals, an alert is fired, or nobody notices\).  
   4. If the failure remains unresolved, how would the injected fault be rolled back?
   5. Should the experiment be run in isolation \(e.g., would a degradation in monitoring limit learning from other experiments?\)  
   6. Which environment will it be run on?  Our experience suggests that using the same pre-production environment for all experiments makes execution easier, providing valuable learning, without production's costs and risks.  
4. Shortlist 4–8 experiments based on business risk and learning opportunity \(e.g., what failure mode would have the greatest risk to the business and a system response that you’re uncertain about?\).  
5. Prepare the experiments \(hence, the two-week gap between planning and the main event\), keeping them secret from the participating teams to maximise the realism of unexpected failures.  
6. Determine a date for Chaos Day, checking that it won’t impact key business events \(e.g., if the target environment is severely degraded, checking this won’t delay any production releases that need to pass through it around that date\).
7. Schedule post-chaos review meetings for participating teams \(as close to after Chaos Day as possible\).

### Experiment execution

1. Let participating teams know when Chaos Day is, and that they should treat failures in the target environment as if “production were on fire.”
2. Ensure that participating teams know which communication channel\(s\) to use \(e.g., a public \#pre-prod-incidents Slack channel\), to aid documenting response timelines.
3. Provide a physical/[remote space](https://remote-working.playbook.ee/remote-working-runbooks/remote-workshops) \(and plenty of snacks\) for the agents of chaos. Provide a facilitator to help the team keep pace through the experiments \(we’ve found using the Trello board from planning to be helpful here, with additional columns for experiments: In Progress, Resolved by Agents, Resolved by Owning Team\).
4. Monitor each experiment closely, analysing and documenting impact and team response.  A private Slack channel is useful \(e.g., \#agents-of-chaos\), as is the Trello board.
5. Ensure experiments are concluded and normal service restored before the end of the day.

### Chaos review

1. Run reviews for each experiment, with a wide group of people: the agents of chaos, those who responded, or helped with a diagnosis and resolution, plus their colleagues.
2. Structure each review as a [post-incident review/post-mortem](https://landing.google.com/sre/sre-book/chapters/postmortem-culture/): Walk through the timeline, discussing and documenting what people saw, thought, did \(and didn’t do\).  Focus on surfacing new knowledge about system behaviour, instead of improvement tasks. If ideas for improvement come up, note them and assign an owner to consider them later, to avoid knee-jerk resilience solutions.
3. Identify improvements you could make to the mechanics of running the Chaos Day itself.  Document them somewhere you and others can easily return to when you run the next one \([improvements](contributing/how-to-contribute.md) to this playbook are also most welcome!\).

### Sharing the knowledge gained

Disseminate the review write-ups as widely as possible, so other engineers, teams, and wider stakeholders can benefit from the new-found knowledge.  This might include any combination of posting them on a wiki, sharing them on Slack and presenting them at a show-and-tell.  
  


