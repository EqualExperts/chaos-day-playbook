# Where to run a Chaos Day

## It doesn’t have to be production

Chaos Engineering was made famous by [Netflix running their Chaos Monkey in production](https://www.gremlin.com/chaos-monkey/). However, as Norah Jones writes in her excellent [Chaos Engineering Traps post](https://medium.com/@njones\_18523/chaos-engineering-traps-e3486c526059), the Netflix team learned a lot about resilience just by automating their experiments, before they were even run in production!

Because Chaos Engineering is highly contextual, what is right for one organisation may not be appropriate for another. If your pre-production environment is a close enough replica of production (e.g. same architecture, characteristics and supporting structures, such as service configuration, deployment, telemetry, etc.) then running experiments in pre-production will provide valuable lessons, without the costs and risks of targeting production.

Your production environment will always be the most realistic environment to run experiments in, so always consider first how experiments could be run there without impacting users or the business. Various techniques make this possible, including:

1. _Shadow running production traffic in isolated production instances_ - production requests are replicated as early as possible and replicated traffic is directed down a set of production service instances that are reserved for experimentation.
2. [_Blue-green deployments_](https://martinfowler.com/bliki/BlueGreenDeployment.html) _or_ [_canary releases_](https://launchdarkly.com/blog/what-is-a-canary-release/) - experiments are deployed to a small percentage of your production estate, which receives a small amount of production traffic, thus controlling the proportion of sessions impacted if experiments get out of control.
3. _Flying below the error threshold radar_ - (in combination with blue-green deployments) most complex environments have a low-level, steady-state error rate. This allows experiments to be safely run providing they don’t elevate the error rate above an impactful threshold. This requires close monitoring of the steady-state error level and any delta introduced by an experiment, plus the ability to quickly disable an experiment before the threshold is exceeded.
4. _Friendly beta users_ - if production traffic can be segregated by user, and you have access to a set of users willing to participate in experiments, then beta user traffic could be directed to production instances that are reserved for experimentation.

## Environmental considerations

Some of the Chaos Days we have run have multiple pre-production environments to choose from, alongside the production environment. When choosing which pre-production environment to use, consider:

1. _Likeness to production_ - how different to production is the environment’s architecture and configuration (e.g. instance size/compute power), connectivity (e.g. which services are present and operational, which are stubbed or connected to external dependencies), supporting structures such as deployment mechanisms, telemetry and alerting configuration? Even if your pre-production is technically identical to production, there may still be differences in how teams interact or treat that environment. For example, alerts may not follow the same process as for Production, alerts may be ignored in pre-production environments due to existing high signal-to-noise.
2. _Load generation_ - failures are only observable when triggered by a stimulus, normally in the form of simulated user traffic. Environments that already have load tests running against them can often be easier to experiment on.
3. _Telemetry_ - because pre-production environments normally receive less traffic than production, and are often used for testing, their logging, monitoring and alerting services may require configuration changes (e.g. turn on alerts, set error threshold lower) before (and after)  Chaos Day in order for failures to show up during the event.&#x20;
4. _Business impact_ - what is the impact on other teams that use this environment? Do they need it to be fully functional in order to deliver a time-critical capability? If experiments get out of control and cause more chaos than intended, how quickly could normal service be resumed?
5. _Communication channels_ - how do teams normally collaborate when an issue occurs in production? Is there a similar setup for the pre-production environment? Aim to standardise as much as possible across environments, so that Chaos Day participants strengthen their muscle memory for how to respond during a real production incident.
