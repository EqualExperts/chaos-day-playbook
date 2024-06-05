---
cover: ../.gitbook/assets/4b.png
coverY: 13.833984375
---

# Complementary approaches

Chaos Days are one of many tools for improving system resilience.  Others include:

1. [AWS Game Days](https://aws.amazon.com/gameday/).  AWS runs these days to teach design and diagnosis techniques for improving resilience using an AWS-based fake production service.  They are intense and great fun but don’t teach you anything about your own system.
2. Per feature chaos testing.  When a team builds a new feature, they run manual or automated experiments to explore the feature’s impact on system resilience as part of its testing.  This can be a good way to introduce chaos-engineering principles, as well as help teams [shift-left](https://en.wikipedia.org/wiki/Shift-left\_testing) operability thinking (i.e., consider it earlier in the engineering process, instead of when the first product issue hits).
3. [Purple team security exercises](https://app.gitbook.com/s/-Lot\_zZroazuFRKM4vsv/practices/operate/security-testing-in-production#use-purple-team-exercises).  These exercises help to identify vulnerabilities and weaknesses in a product by simulating the behaviours and techniques of malicious attackers in the most realistic way possible.
4. Automated failure injection.  Tools such as [AWS's Fault Injection Simulator](https://aws.amazon.com/fis/),  [Gremlin](https://www.gremlin.com/) and [Netflix’s Chaos Monkey](https://github.com/netflix/chaosmonkey) can be used to inject regular but random failures to test the system response on an ongoing basis.
5. Production incidents.  Treat production incidents as learning opportunities, or in the [words of John Allspaw](https://twitter.com/allspaw/status/1233778870635155456), “Incidents are unplanned investments”.  If managed well (see [Google’s SRE book](https://sre.google/sre-book/postmortem-culture/) and [Etsy’s debriefing guide](https://extfiles.etsy.com/DebriefingFacilitationGuide.pdf)), then valuable, firsthand insights can be gained due to everything about the chaos being real!  Live issues can be costly to the business. Therefore, it is beneficial to extract as much business value from them as possible, which can be achieved through a better understanding of the system and possible resilience improvements.
6. Running a mini chaos event, as described next.
