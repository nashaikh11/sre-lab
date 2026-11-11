   # Learning journal

   ## Week 0 – 11 Nov 2026
   - Created Azure free account and set a monthly budget alert
   - Created this repo
   - install tools, read SRE book chapter 1
   - 1. SRE vs DevOps: the order is the other way round
SRE didn’t evolve from DevOps. Google started SRE around 2003, when Ben Treynor Sloss put software engineers in charge of operations. The term “DevOps” only appeared around 2009. The two grew up in parallel with very similar ideas: break down the wall between developers and operations, automate, share ownership.

The common interview line is: “SRE is a concrete implementation of DevOps.” DevOps is the philosophy, and SRE is a specific way of doing it, with clear practices like SLOs, error budgets and the toil cap.

2. The 50% cap is about operational work, not just monitoring
The cap covers all ops work: tickets, on-call, manual fixes, repetitive tasks (toil). Monitoring itself is a core SRE function, not something to minimize. You’re right about the purpose: at least 50% of the time stays for engineering, meaning automating away toil and improving the system. If ops work goes over 50%, the extra is pushed back to the development team, which gives developers a reason to build more reliable software.

3. Core responsibilities: you’re on the right track
The book’s full list is:

Durable focus on engineering (the 50% rule)
Maximum change velocity without breaking the SLO (error budgets)
Monitoring
Emergency response (fast recovery, measured as MTTR)
Change management (progressive rollouts, fast detection, safe rollback)
Demand forecasting and capacity planning
Provisioning
Efficiency and performance

One useful detail on alerting from the chapter: monitoring output should be one of three kinds. Alerts need a human to act now, tickets need action but not right now, and logs are only for later investigation. Nobody should be paged for something they can’t act on.
