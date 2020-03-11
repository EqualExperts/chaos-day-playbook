# Ready for chaos?

## **When are you ready for chaos?**

Running a Chaos Day requires people’s time and system usage, so its scheduling needs to be considered just like any other piece of work.  Its benefit may not be as appealing or tangible as new features, however, which may cause investment in a Chaos Day to always be put off. This can be addressed by first making the smaller investment in a time-boxed risk assessment of your system \(we’ve found the [FAIR approach](https://www.fairinstitute.org/what-is-fair) useful\) to explore what failures could happen, their frequency and the magnitude of their impact.  This gives meaningful \(monetary\) data that can help stakeholders re-evaluate prioritising features over resilience.

Chaos Days provide particular benefits if run weeks/months before major changes are deployed to production or ahead of traffic peaks \(such as Black Friday for e-commerce sites\).  Allow a sufficient gap between consecutive events to allow for learning to be distilled and improvements to be applied. For one client with a very large platform \(1000 microservices, processing 1 billion requests on a peak day\), we found that 2–3 Chaos Days yearly was a suitable frequency for their context.  
Despite Chaos Days’ many benefits, if your production system is regularly “on fire”, you probably have enough ready-made chaos to contend with!  In this situation, your focus should be on running and [improving post-incident reviews](https://extfiles.etsy.com/DebriefingFacilitationGuide.pdf) to bring about system stability.  Once you’ve had a few months free of repeated production issues, try and run a small Chaos Day \(in pre-production\) to further explore system stability.

