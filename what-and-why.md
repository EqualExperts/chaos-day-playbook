# What & Why

## Why Chaos

Chaos Days are a practice within the field of Chaos engineering, which is [defined](https://principlesofchaos.org/) as:

> ### _**The discipline of experimenting on a system in order to build confidence in the system's capability to withstand turbulent conditions in production.**_

Modern systems are comprised of a high number of complex components, with an equally high number of complex connections between them. Defects are always present, and failures will occur.  For an IT system, turbulence comes in many forms, ranging from single-point failure to multiple, unrelated failures, often combined with sudden changes in external pressure \(e.g., traffic spikes\).  

The complexity of IT systems makes it impossible to predict how they will respond to this turbulence.  One such example was a [Google Cloud Outage](https://status.cloud.google.com/incident/cloud-networking/19009) that led to reports of people being [unable to operate their home air-conditioning](http://bit.ly/2ZavoyP).  The trigger was the combining of three separate, unrelated bugs to severely impact the Google Cloud US network for several hours.  

Chaos Days allow teams to safely explore these turbulent conditions by designing and running controlled experiments in pre-production or production environments.  Each experiment injects a failure into the system \(e.g., terminate a compute instance, fill up a storage device\) in order to analyse the impact and system response.  

## What benefits do Chaos Days provide?

An IT system includes the people who develop and operate it and the knowledge, experience, tools and processes they use to respond to incidents.  As John Allspaw puts it: 

> ### [_People are the adaptable element of complex systems._](https://vimeo.com/showcase/6542214/video/370008157)\_\_

The analysis of a team’s response to incidents provides many lessons that can lead to improved system resilience. The [Oxford Dictionary defines resilience](http://english.oxforddictionaries.com/resilience) as:

1. the capacity to recover quickly from difficulties
2. the ability of a substance or object to spring back into shape; elasticity.

Some learning may be technical, such as implementing retry mechanisms and circuit breakers; other types of learning include the processes a team uses to detect, triage and resolve an incident \(such as communication channels, escalation routes, runbooks, etc.\). 

A key but often underestimated benefit is the sharing of internal knowledge that individual team members rely on when working through an incident.  By spreading this knowledge across the team, resilience is improved just through people’s greater cognisance of system behaviour and failure scenarios when tackling production incidents or developing system enhancements.  


Chaos Days improve system robustness by developing its:

* People, through giving them new: 
  * knowledge about system behaviour
  * expertise in diagnosing and resolving incidents
  * skills and behaviours in collaborating, communicating and thinking during high-stress periods
  * understanding of how ownership and operability impact system recovery 
* Processes, through guiding improvements in: 
  * incident management \(such as communication channels, team roles, timeline documentation\)
  * incident analysis \(e.g., improving how post-incident reviews are conducted\)
  * engineering approach \(e.g., feature requirements include how faults should be handled, resilience testing is performed during feature development\)
* Products/toolsets, by initiating changes that: 
  * Make services more resilient \(e.g., [implementing retries](https://aws.amazon.com/builders-library/timeouts-retries-and-backoff-with-jitter) when a downstream fails\).
  * Make services and dependencies simpler and easier to reason about \(which is important when under pressure\).
  * Improve observability so that engineers can isolate failures and fix them faster.
  * Improve documentation, such as more informative exception messages and runbook documentation.

