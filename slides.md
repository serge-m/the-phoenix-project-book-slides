---
theme: default
title: The Phoenix Project
info: A visual short narrative based on the summary in short_version1.md
mdc: true
fonts:
  sans: Inter
  mono: IBM Plex Mono
---

<div class="cover">
  <div class="art-frame cover-art">
    <div class="frame-id">COVER</div>
    <div class="frame-copy">Automotive-parts factory at dusk · assembly lines becoming streams of data · a subtle phoenix-shaped arc of light</div>
  </div>
  <h1>The Phoenix Project</h1>
</div>

---

<NarrativeSlide number="01" title="A company bets on Phoenix" image="Parts Unlimited factory and retail network under pressure; a troubled digital program glowing at its center">

<!-- Prologue and Chapter 1 -->

**1.** *The Phoenix Project* takes place at **Parts Unlimited**, an automotive-parts manufacturer and retailer struggling to compete with faster rivals. The company has invested heavily in **Project Phoenix**, a large IT initiative intended to modernize its retail and online business. Phoenix is already late and over budget, but senior management believes that the company’s future depends on launching it.

**2.** **Bill Palmer**, formerly the Director of Midrange Technology Operations, is unexpectedly promoted to Vice President of IT Operations after the CIO and Bill’s previous boss are fired. The CEO, **Steve Masters**, gives him ninety days to stabilize IT and help rescue Phoenix, warning that IT Operations may otherwise be outsourced. Bill accepts reluctantly, knowing that senior IT positions at Parts Unlimited have a habit of ending badly.

</NarrativeSlide>

---

<NarrativeSlide number="02" title="The first fire" image="A tense operations room; corrupted payroll records on screens; storage hardware failing in parallel">

<!-- Chapters 2–3 -->

**3.** Bill’s first crisis is not Phoenix but payroll. Records for thousands of hourly employees have been corrupted, putting their salaries at risk. A simultaneous storage-system failure initially obscures the cause, but the payroll corruption is eventually traced to an unauthorized tokenization change deployed to protect personal data and satisfy an audit finding. The change was introduced without adequate testing because no suitable test environment was available.

**4.** The incident shows Bill that the company does not know what is happening inside its own IT systems. Engineers make changes without telling one another, urgent work bypasses normal procedures, and teams discover dependencies only after something breaks. Almost every difficult problem eventually reaches **Brent**, an experienced engineer who understands many systems that nobody else fully understands.

</NarrativeSlide>

---

<NarrativeSlide number="03" title="Two systems at war" image="Development and Operations teams pulling in opposite directions, divided by a fragile release pipeline">

<!-- Chapter 4 -->

**5.** Before Bill can bring the situation under control, management accelerates Phoenix. Development says that the software must be released, while Operations warns that requirements are incomplete and testing is inadequate. Development is judged by its ability to deliver features, whereas Operations is judged by production stability. Each side therefore sees the other as an obstacle.

<!-- Chapter 5 -->

**6.** Bill meets **Erik Reid**, a prospective board member who takes him through one of the company’s manufacturing plants. Erik asks Bill to think about IT as a production system. Work must flow through a sequence of work centers, and the output of the entire system is limited by its most constrained resource. Starting more work cannot improve output when the constraint is already overloaded.

</NarrativeSlide>

---

<NarrativeSlide number="04" title="Make the invisible visible" image="A wall-sized change board overflowing with cards while teams reveal colliding production changes">

<!-- Chapters 6–8 -->

**7.** Back at work, Bill discovers that IT has committed to approximately 105 projects, in addition to maintenance, security requirements and support work. He also asks **Patty McKee** to revive the change-management process. The first meetings are confused and unpopular, but writing changes on cards and placing them on a shared board begins to reveal how many teams are modifying production at the same time.

<!-- Chapter 9 -->

**8.** When the company’s credit-card processing systems fail, the incident call descends into guesswork and blame. Brent restores service almost accidentally while trying possible fixes, but the team cannot explain exactly what happened. Bill insists on better incident procedures and documentation. Meanwhile, the change board reveals that more than a hundred changes are planned for the same day as the Phoenix launch.

</NarrativeSlide>

---

<NarrativeSlide number="05" title="The constraint has a name" image="Brent at the center of a storm of calls, messages, tickets, and waiting coworkers; Bill observes the bottleneck">

<!-- Chapters 10–11 -->

**9.** Bill watches Brent and finally sees the scale of the problem. Brent is supposedly working on Phoenix, but calls, messages and visitors interrupt him continuously. Bill tries to protect him by routing requests through senior engineers, requiring them to document what Brent does and ensuring that he does not solve the same problem twice.

**10.** The new change process reveals that many planned changes cannot be completed because they conflict with other work, require unavailable people or depend on Brent. Bill recognizes Brent as a constraint shared by many different work centers. The more work everyone sends to him, the longer every project must wait.

</NarrativeSlide>

---

<NarrativeSlide number="06" title="Past the point of no return" image="A nighttime deployment war room; database migration barely moving; rollback path disappearing behind the team">

<!-- Chapters 12–13 -->

**11.** The Phoenix deployment nevertheless goes ahead. It is a huge, fragile operation involving Development, Quality Assurance, Operations, database administrators and business representatives. The software is not functioning properly in the test environment, new releases continue arriving from Development, and the production infrastructure differs from what developers and testers expected.

**12.** Bill warns that the launch should be delayed, but Marketing campaigns and executive commitments have already been made. The database conversion begins and runs far more slowly than planned. By the time the team understands the problem, it has passed the point at which the old systems can easily be restored.

</NarrativeSlide>

---

<NarrativeSlide number="07" title="Phoenix burns" image="Automotive-parts store in chaos; failed point-of-sale terminals, manual receipts, and exhausted response teams">

<!-- Chapters 14–15 -->

**13.** Phoenix eventually starts, but point-of-sale systems fail and stores must process transactions manually. Orders are lost or duplicated, customers are charged more than once, and credit-card information is exposed. The teams spend days fighting fires, and emergency repairs introduce still more uncertainty into the environment.

**14.** The failure deepens the conflict between departments. Operations believes Development handed over incomplete software, while Development believes Operations failed to provide the required environments and infrastructure. Yet Bill and Development leader **Chris Allers** begin to recognize that both groups are trapped in the same failing system. They agree that they must work together if the company is to survive.

</NarrativeSlide>

---

<NarrativeSlide number="08" title="The fourth type of work" image="Planned work buried under waves of incidents; Bill walking away from a late-night executive confrontation">

**15.** Bill then realizes what Erik calls the fourth type of work: **unplanned work**. Official schedules show projects, internal IT work and planned changes, but they do not show the incidents and emergency repairs consuming much of the organization’s capacity. Phoenix has displaced nearly all planned work, while the failures caused by Phoenix generate even more unplanned work.

<!-- Chapters 16–17 -->

**16.** A failure in the customer-invoicing system threatens a cash shortfall of about $50 million. When Steve demands immediate action without giving the team time to understand the situation, Bill refuses to allow uncontrolled changes and resigns. After speaking with Erik, Steve recognizes that his own leadership is perpetuating the problem. He apologizes and asks Bill to return for ninety days, admitting that the company’s leadership must change as well as IT.

</NarrativeSlide>

---

<NarrativeSlide number="09" title="Stop starting. Start finishing." image="Leadership gathered around one table; most project streams frozen while one critical path remains illuminated">

<!-- Chapters 18–19 -->

**17.** Steve brings the leaders of Development, Operations, Security and the business together and asks them to rebuild trust. Bill explains that IT has accepted more work than it can process. The resulting shortcuts create technical debt, which produces failures and still more unplanned work.

**18.** With Steve’s support, the company freezes most new project work. Development, QA, Operations and Security concentrate on Phoenix and on reducing the backlog created by years of overloaded systems. Business managers are no longer allowed to bypass priorities by sending private requests directly to individual engineers.

</NarrativeSlide>

---

<NarrativeSlide number="10" title="Protect flow, reduce risk" image="Senior engineers learning from Brent beside a factory safety line; useful controls replace towering paperwork">

<!-- Chapter 20 -->

**19.** Erik explains that Brent is not simply a work center; he is supporting too many work centers throughout the company. The team should accept work that does not require him, prioritize improvements that increase his capacity and prevent unauthorized changes that create emergencies. Senior engineers continue learning and documenting his methods so that Brent is not the only person capable of performing critical tasks.

<!-- Chapter 21 -->

**20.** An audit confrontation exposes another problem. Chief Information Security Officer **John Pesche** has generated large amounts of compliance work without clearly connecting it to actual business risk. Erik challenges him to learn from the safety organization in the manufacturing plant: effective controls should protect the flow of work and reduce risk, not merely produce paperwork at the end.

</NarrativeSlide>

---

<NarrativeSlide number="11" title="Work begins to flow" image="A clean Kanban system replacing tangled queues; small batches move steadily across a shared team workspace">

<!-- Chapters 22–23 -->

**21.** Patty begins using Kanban boards to make service requests and other operational work visible. She separates work according to whether it avoids Brent, increases Brent’s capacity or depends on him. The team also studies why supposedly simple Phoenix tasks take so long and discovers that most of the delay occurs while work waits between overloaded teams.

**22.** They respond by limiting work in progress, standardizing recurring tasks and improving handoffs. Instead of measuring how busy every individual appears, they begin measuring whether work is moving through the whole system. Preventive work, documentation and automation are treated as necessary investments rather than distractions from project delivery.

</NarrativeSlide>

---

<NarrativeSlide number="12" title="Begin with business value" image="IT, business, and security leaders mapping goals and risks together around one illuminated value stream">

<!-- Chapters 24–27 -->

**23.** John changes his approach and begins asking business leaders what they are trying to achieve and which risks actually threaten those objectives. Bill and Patty conduct similar interviews with Sales, Marketing and Finance. They discover that many business goals depend on IT, although IT was rarely involved when those goals and projects were selected.

**24.** The teams begin evaluating projects and security controls according to business value and risk. Security specialists work with Development and Operations during ordinary work instead of delivering requirements immediately before release. This reduces separate compliance projects and allows controls and audit evidence to be built into the systems themselves.

</NarrativeSlide>

---

<NarrativeSlide number="13" title="Feedback moves upstream" image="A hidden production configuration exposed, then a bright feedback loop connecting Operations back to Development">

<!-- Chapter 28 -->

**25.** A later Phoenix deployment is smaller and proceeds more smoothly, but it still encounters a serious database problem. The team discovers that Brent had previously made a special change at **Sarah Moulton’s** request, creating a difference between the production environment and the assumptions used by Development and QA. The release succeeds, but the incident shows that undocumented expert intervention remains dangerous.

<!-- Chapter 29 -->

**26.** Erik introduces the **Second Way**: feedback must travel quickly from Operations back toward Development. Quality cannot be inspected into the product only at the end. Brent and Operations knowledge must be involved earlier, when applications and environments are being designed. The company forms a small cross-functional team to develop business features outside the main Phoenix release cycle.

</NarrativeSlide>

---

<NarrativeSlide number="14" title="Toward continuous delivery" image="Factory changeovers transform into a software delivery pipeline; many manual gates collapse into an automated path">

<!-- Chapter 30 -->

**27.** At the manufacturing plant, Erik explains how smaller batches and shorter changeover times allow a factory to respond more quickly. He challenges Bill to imagine deploying software ten times a day. The goal is not speed for its own sake, but a deployment pipeline in which code, environments and configuration can move safely and repeatedly from Development to production.

<!-- Chapter 31 -->

**28.** Bill’s cross-functional team maps every step required to deploy a change. The map contains more than a hundred manual steps, delays and failure points. They identify environment creation and code packaging as major problems. Development, QA, Operations and Security agree to standardize environments, keep application and infrastructure definitions under version control, and automate the path from code commit to testing and production.

</NarrativeSlide>

---

<NarrativeSlide number="15" title="Unicorn learns at speed" image="A small cross-functional team shipping analytics through a clean pipeline into elastic cloud capacity">

<!-- Chapter 32 -->

**29.** The team becomes **Project Unicorn**. Using common environments, automated tests and a system largely separated from Phoenix’s fragile components, it begins delivering customer-analysis and marketing capabilities far faster than before. Phoenix adopts some of the same practices after the rest of the organization sees that they work.

<!-- Chapter 33 -->

**30.** When Unicorn’s reports are too slow, the team experiments with cloud computing and rapidly tests a solution. Marketing uses the new data for a small customer campaign, measures the response and expands what works. Security testing is integrated into the same automated process as QA testing, and defects can be corrected and redeployed within hours rather than waiting for another enormous release.

</NarrativeSlide>

---

<NarrativeSlide number="16" title="The business rises" image="A packed Thanksgiving retail store supported by calm technology teams scaling systems and releasing fixes safely">

<!-- Chapter 34 -->

**31.** The new approach is tested during the Thanksgiving shopping period. Heavy traffic creates problems, but the team can disable expensive features through configuration, add capacity and deploy new tools for stores and customers quickly. Sales reach record levels, helping put Parts Unlimited back on a path to profitability. IT has become capable of responding to business conditions instead of merely reacting to failures.

<!-- Chapter 35 -->

**32.** By January, severe incidents have become rare. Through initiatives such as **Project Narwhal** and the **Chaos Monkey**, teams deliberately inject failures to find weaknesses, improve monitoring and make systems more resilient. Development, QA, Operations and Security now work as one system, continuously learning instead of waiting for a crisis to force them together.

</NarrativeSlide>

---

<NarrativeSlide number="17" title="The Three Ways" image="Bill overlooking an integrated factory and technology organization; three luminous paths form flow, feedback, and learning loops">

**33.** Steve offers Bill a development path toward becoming Chief Operating Officer, explaining that technology is now inseparable from business operations. Parts Unlimited has not merely rescued Phoenix; it has changed how it selects, builds, deploys and improves technology.

<!-- Epilogue and overall message -->

**34.** The central message is expressed through the **Three Ways**. The First Way improves the flow of work from Development through Operations to the customer. The Second Way creates fast feedback from Operations to Development. The Third Way fosters continual experimentation, learning and resilience. Organizations put these ideas into practice by making work visible, limiting unfinished work, managing constraints, reducing batch sizes and automating repetitive processes. Reliable delivery is not the result of one perfect tool; it emerges when the entire organization learns to work as one system.

</NarrativeSlide>
