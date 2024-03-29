# Experiment design and preparation



![Template trello card for a single experiment](<../../.gitbook/assets/Chaos trello template card.png>)

We often use [Trello](https://trello.com/) as a collaboration tool for Chaos Days, with each card representing a single experiment. Our template card uses the format:

| Heading                                                      | Example                                                                                                                                                                                                                                       |
| ------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Experiment title: \<Component> \<Failure> \<Expected result> | Third-party service Y being unavailable leads to our service X queuing and retrying requests                                                                                                                                                  |
| What failure are you invoking?                               | Response time for requests from service X to Y starts exceeding 10 seconds. Simulate by stopping service Y.                                                                                                                                   |
| Expected impact                                              | This should have no visible client impact for N minutes, during which service X will queue and retry requests, whilst giving clients an OK response. After N minutes the response will change to _Service not available_.                     |
| Expected response                                            | Queue and retry kicks in, then alerts fire if 10 Service not available responses occur within 60 seconds. The team’s support person will respond to the alert within 15 minutes and use the runbook to investigate connectivity to service Y. |
| Rollback steps                                               | Restart service Y.                                                                                                                                                                                                                            |
| Other experiments to run in parallel                         | Intermittent failures in the Queuing platform.                                                                                                                                                                                                |

Having designed the experiment, the next step is to determine its execution. This requires consideration of:

1. How will the system be modified to simulate or cause the failure condition? Will the engineer need to create a script or program to cause the condition? Can this be programmed so the failure can be repeatedly run? Consider if any [third party](https://www.gremlin.com/) or [cloud-provided](https://aws.amazon.com/fis/) chaos engineering tools might help.
2. [Which environment](../where-to-run-a-chaos-day.md) will the experiment be run in?
3. What load does the system need to be under to trigger the failure and make it observable?
4. For the host environment, how will the load occur? For example, if the experiment is running in production, will steady-state production load be sufficient, or does additional synthetic load need injecting? If a pre-production environment is used, how would a production load be simulated?
5. When the failure occurs in the given environment, will configured alerts automatically fire at the error level generated by the induced load, or will the alert threshold need temporarily adjusting?

**When designing experiments, be mindful of the** [**probe effect**](https://en.wikipedia.org/wiki/Probe\_effect) **(see also** [**Chaos Engineering**](https://www.oreilly.com/library/view/chaos-engineering/9781492043850/) **p224); the means of injecting the failure condition might alter the system in such a way to cause alternative or unrealistic chaos, thus distorting the experiment.**
