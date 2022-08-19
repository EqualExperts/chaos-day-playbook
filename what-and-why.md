---
cover: .gitbook/assets/2b@4x.png
coverY: 37.839721945250176
---

# What & Why

## Why Chaos

Chaos Days are a practice within the field of Chaos engineering, which is [defined](https://principlesofchaos.org/) as:

> _<mark style="color:blue;">**The discipline of experimenting on a system in order to build confidence in the system's capability to withstand turbulent conditions in production.**</mark>_

Modern systems consist of a high number of complex components, with equally  complex connections between them. Defects are always present, and failures will occur.  For an IT system, turbulence comes in many forms, ranging from single-point to multiple, unrelated failures, often combined with sudden changes in external pressure (e.g., traffic spikes). &#x20;

The complexity of IT systems makes it impossible to predict how they will respond to this turbulence.  One such example was a [Google Cloud Outage](https://status.cloud.google.com/incident/cloud-networking/19009) that led to reports of people being [unable to operate their home air-conditioning](http://bit.ly/2ZavoyP).  The trigger was the combined impact of three separate, unrelated bugs, which severely impacted the Google Cloud US network for several hours. &#x20;

Chaos Days allow teams to safely explore these turbulent conditions by designing and running controlled experiments in pre-production or production environments.  Each experiment injects a failure into the system (e.g., terminate a compute instance, fill up a storage device) in order to analyse the impact and system response. &#x20;



![](.gitbook/assets/COMPLEXITY@4x.png)

## What benefits do Chaos Days provide?

An IT system includes the people who develop and operate it and the knowledge, experience, tools and processes they use to respond to incidents.  As John Allspaw puts it:&#x20;

> [_People are the adaptable element of complex systems._](https://vimeo.com/showcase/6542214/video/370008157)__

The analysis of a team’s response to incidents provides many lessons that can lead to improved system resilience. The [Oxford Dictionary defines resilience](http://english.oxforddictionaries.com/resilience) as:

1. the capacity to recover quickly from difficulties
2. the ability of a substance or object to spring back into shape; elasticity.

Some learning may be technical, such as implementing retry mechanisms and circuit breakers; other types of learning include the processes a team uses to detect, triage and resolve an incident (such as communication channels, escalation routes, runbooks, etc.).&#x20;

A key but often underestimated benefit is the sharing of internal knowledge that individual team members rely on when working through an incident.  By spreading this knowledge across the team, resilience is improved just through people’s greater cognisance of system behaviour and failure scenarios when tackling production incidents or developing system enhancements.\


Chaos Days improve system resilience by developing its:

| ![](<.gitbook/assets/people@4x (2).png>)    | <p></p><p>People, by giving them new: </p><ul><li>knowledge about system behaviour</li><li>expertise in diagnosing and resolving incidents</li><li>skills and behaviours in collaborating, communicating and thinking during high-stress periods</li><li>understanding of how ownership and operability impact system recovery </li></ul>                                                                                                                                                                                                                                           |
| ------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ![](<.gitbook/assets/processes@4x (1).png>) | <p></p><p>Processes, through guiding improvements in: </p><ul><li>incident management (such as communication channels, team roles, timeline documentation)</li><li>incident analysis (e.g., improving how post-incident reviews are conducted)</li><li>engineering approach (e.g., feature requirements including how faults should be handled and how resilience testing is performed during feature development)</li></ul>                                                                                                                                                        |
| ![](<.gitbook/assets/products@4x (1).png>)  | <p></p><p>Products/toolsets, by initiating changes that: </p><ul><li>Make services more resilient (e.g., <a href="https://aws.amazon.com/builders-library/timeouts-retries-and-backoff-with-jitter">implementing retries</a> when a downstream fails).</li><li>Make services and dependencies simpler and easier to reason about, which is important when under pressure.</li><li>Improve observability so that engineers can isolate failures and fix them faster.</li><li>Improve documentation, such as more informative exception messages and runbook documentation.</li></ul> |
