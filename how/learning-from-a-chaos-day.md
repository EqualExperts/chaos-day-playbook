# Learning from a Chaos Day

Insights that help improve resilience are generated at every step of a Chaos Day, from sketching the system architecture at the beginning to responding to simulated failures on the day itself. As with real production incidents, further lessons can be extracted by holding post-mortem style retrospectives after the event, to analyse what happened. Some great resources on running incident reviews include:&#x20;

* [Etsy’s facilitation guide](https://extfiles.etsy.com/DebriefingFacilitationGuide.pdf)
* [Google’s SRE handbook](https://sre.google/sre-book/postmortem-culture/)&#x20;
* Jeli.io's [incident review guide](https://www.jeli.io/blog/what-is-incident-analysis-and-why-should-we-do-it/)

If several teams were involved in the Chaos Day, ask each team to run their own Chaos retrospective, then feed their top insights into a team-of-teams retrospective.

## Chaos retrospective format

Supporting a production service is a team sport, so ideally involve the whole team in the Chaos retrospective, not just the Agents of Chaos and responders. Split the time into sections, or _even separate meetings_, focusing on:

1. _What was learnt from the experiments?_ Use your standard incident review process, remembering to focus on surfacing new knowledge about system behaviour rather than  generating a long list of improvement tasks. If ideas for improvement do come up, note them and assign an owner to review them later (see item 3). Don’t get drawn into solutionising, because that needs a separate thinking space, and will take valuable time away from documenting what was learnt.
2. _What would improve the next Chaos Day?_ Spend the last 10 minutes of the meeting on this, noting down for future reference what changes would make the next Chaos Day even more successful.
3. What improvement considerations/ideas should progress onto a team’s backlog?

## Sharing the knowledge

Chaos Days surface a lot of knowledge that can help teams improve service resilience. To get further benefit, share this knowledge across the organisation, making it easy for other teams to find and consume. Consider writing publically about what you’ve done and learnt - chaos engineering is still in its infancy in the software engineering discipline and making experience reports public will help this important practice mature.
