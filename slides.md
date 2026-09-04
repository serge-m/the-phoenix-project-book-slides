---
theme: default
title: The Phoenix Project
info: A visual short narrative based on the summary in short_version1.md
mdc: true
fonts:
  sans: Inter
  mono: IBM Plex Mono
---

<div class="title-slide">
  <div class="title-block">
    <h1>The Phoenix Project</h1>
    <p class="title-credit">A book by Gene Kim, Kevin Behr &amp; George Spafford<br><span>Presentation by Sergey Matyunin</span></p>
  </div>
</div>

---

<NarrativeSlide number="01" title="A company bets on Phoenix"
  image1="Documentary exterior of the Parts Unlimited factory and warehouse, with loading docks and store-delivery trucks; beside the main entrance, a side door has a small readable IT plaque and a window through which server racks are visible."
  image1Src="/images/jpeg/paragraph-01-parts-unlimited-factory.jpg"
  image2="Steve hands a reluctant Bill Palmer an executive access badge and office key at the IT-floor doorway; through the glass rear exit in the same corridor, the former CIO and VP of IT Operations carry cardboard boxes toward the parking lot."
  image2Src="/images/jpeg/paragraph-02-bill-promotion.jpg"
>

<!-- Prologue and Chapter 1 -->

**1.** *The Phoenix Project* takes place at **Parts Unlimited**, an automotive-parts manufacturer and retailer struggling to compete with faster rivals. The company has invested heavily in **Project Phoenix**, a large IT initiative intended to modernize its retail and online business. Phoenix is already late and over budget, but senior management believes that the company’s future depends on launching it.

**2.** **Bill Palmer**, formerly the Director of Midrange Technology Operations, is unexpectedly promoted to Vice President of IT Operations after the CIO and Bill’s previous boss are fired. The CEO, **Steve Masters**, gives him ninety days to stabilize IT and help rescue Phoenix, warning that IT Operations may otherwise be outsourced. Bill accepts reluctantly, knowing that senior IT positions at Parts Unlimited have a habit of ending badly.

</NarrativeSlide>

---

<NarrativeSlide number="02" title="The first fire"
  image1="Over-the-shoulder view of a payroll application showing repeated employee rows, blank or garbled pay fields, and red validation markers; Bill stares at the monitor in shock while a payroll specialist and technician react; a storage unit behind them shows a red fault light."
  image1Src="/images/jpeg/paragraph-03-payroll-corruption.jpg"
  image2="Brent works across three monitors showing a server console, an incident ticket, and a network diagram; his phone rings, chat notifications stack up, and two engineers wait with different printed tickets while handwritten dependency notes cover the open rack beside him."
  image2Src="/images/jpeg/paragraph-04-brent-bottleneck.jpg"
>

<!-- Chapters 2–3 -->

**3.** Bill’s first crisis is not Phoenix but payroll. Records for thousands of hourly employees have been corrupted, putting their salaries at risk. A simultaneous storage-system failure initially obscures the cause, but the payroll corruption is eventually traced to an unauthorized tokenization change deployed to protect personal data and satisfy an audit finding. The change was introduced without adequate testing because no suitable test environment was available.

**4.** The incident shows Bill that the company does not know what is happening inside its own IT systems. Engineers make changes without telling one another, urgent work bypasses normal procedures, and teams discover dependencies only after something breaks. Almost every difficult problem eventually reaches **Brent**, an experienced engineer who understands many systems that nobody else fully understands.

</NarrativeSlide>

---

<NarrativeSlide number="03" title="Two systems at war"
  image1="At a deployment workstation, a developer presents a release manifest while an operations engineer points to failed test results and a mismatched server inventory on two monitors; a nearby rack alarm is active and the release checklist remains unsigned."
  image1Src="/images/jpeg/paragraph-05-development-operations-conflict.jpg"
  image2="Documentary factory-floor view: Bill and Erik in safety glasses walk beside an automotive assembly line where parts pile up before one occupied inspection station while downstream stations and workers wait idle."
  image2Src="/images/jpeg/paragraph-06-constraint-factory.jpg"
>

<!-- Chapter 4 -->

**5.** Before Bill can bring the situation under control, management accelerates Phoenix. Development says that the software must be released, while Operations warns that requirements are incomplete and testing is inadequate. Development is judged by its ability to deliver features, whereas Operations is judged by production stability. Each side therefore sees the other as an obstacle.

<!-- Chapter 5 -->

**6.** Bill meets **Erik Reid**, a prospective board member who takes him through one of the company’s manufacturing plants. Erik asks Bill to think about IT as a production system. Work must flow through a sequence of work centers, and the output of the entire system is limited by its most constrained resource. Starting more work cannot improve output when the constraint is already overloaded.

</NarrativeSlide>

---

<NarrativeSlide number="04" title="Make the invisible visible"
  image1="Patty pins cards onto a wall-sized change board crowded with 105 numbered project cards; many cards share the same short system labels and launch date, while maintenance and security cards wait in the backlog columns."
  image1Src="/images/jpeg/paragraph-07-change-board.jpg"
  image2="At a store service desk, a card terminal displays a payment error while an incident bridge runs on speakerphone; Brent swaps a network cable as another technician records each attempted fix and timestamp on a paper incident log."
  image2Src="/images/jpeg/paragraph-08-credit-card-incident.jpg"
>

<!-- Chapters 6–8 -->

**7.** Back at work, Bill discovers that IT has committed to approximately 105 projects, in addition to maintenance, security requirements and support work. He also asks **Patty McKee** to revive the change-management process. The first meetings are confused and unpopular, but writing changes on cards and placing them on a shared board begins to reveal how many teams are modifying production at the same time.

<!-- Chapter 9 -->

**8.** When the company’s credit-card processing systems fail, the incident call descends into guesswork and blame. Brent restores service almost accidentally while trying possible fixes, but the team cannot explain exactly what happened. Bill insists on better incident procedures and documentation. Meanwhile, the change board reveals that more than a hundred changes are planned for the same day as the Phoenix launch.

</NarrativeSlide>

---

<NarrativeSlide number="05" title="The constraint has a name"
  image1="Brent works at a keyboard mid-procedure while his phone rings and several engineers wait with tickets; a senior engineer photographs rack connections and writes numbered runbook steps as Bill stops another interruption at the doorway."
  image1Src="/images/jpeg/paragraph-09-protect-brent.jpg"
  image2="Close view of a ticket dashboard with server, database, network, and release jobs all assigned to Brent and wait times increasing; beside the monitor sit matching paper change forms bearing Brent’s initials and a fully booked calendar."
  image2Src="/images/jpeg/paragraph-10-brent-constraint-dashboard.jpg"
>

<!-- Chapters 10–11 -->

**9.** Bill watches Brent and finally sees the scale of the problem. Brent is supposedly working on Phoenix, but calls, messages and visitors interrupt him continuously. Bill tries to protect him by routing requests through senior engineers, requiring them to document what Brent does and ensuring that he does not solve the same problem twice.

**10.** The new change process reveals that many planned changes cannot be completed because they conflict with other work, require unavailable people or depend on Brent. Bill recognizes Brent as a constraint shared by many different work centers. The more work everyone sends to him, the longer every project must wait.

</NarrativeSlide>

---

<NarrativeSlide number="06" title="Past the point of no return"
  image1="In a deployment room, test and production racks stand side by side with visibly different hardware counts and configuration labels; a QA monitor shows a failed test run, numbered build packages accumulate in the release inbox, and an operator checks a paper checklist."
  image1Src="/images/jpeg/paragraph-11-deployment-room.jpg"
  image2="A database migration console remains at a low percentage while the wall clock shows late night; the rollback checkpoint is crossed out on a printed launch runbook, and sealed boxes of already-printed Phoenix store material are stacked nearby."
  image2Src="/images/jpeg/paragraph-12-database-migration.jpg"
>

<!-- Chapters 12–13 -->

**11.** The Phoenix deployment nevertheless goes ahead. It is a huge, fragile operation involving Development, Quality Assurance, Operations, database administrators and business representatives. The software is not functioning properly in the test environment, new releases continue arriving from Development, and the production infrastructure differs from what developers and testers expected.

**12.** Bill warns that the launch should be delayed, but Marketing campaigns and executive commitments have already been made. The database conversion begins and runs far more slowly than planned. By the time the team understands the problem, it has passed the point at which the old systems can easily be restored.

</NarrativeSlide>

---

<NarrativeSlide number="07" title="Phoenix burns"
  image1="Documentary view inside an automotive-parts store: point-of-sale terminals show error states, staff write carbon-copy receipts, duplicate order slips spill from a printer, worried customers hold payment cards, and support staff troubleshoot behind the counter."
  image1Src="/images/jpeg/paragraph-13-pos-failure.jpg"
  image2="Bill and Chris sit shoulder to shoulder at an incident workstation comparing a developer build log with an operations deployment log; each has highlighted a failed handoff, and they write one shared action list while technicians repair and retest behind them."
  image2Src="/images/jpeg/paragraph-14-bill-chris-collaboration.jpg"
>

<!-- Chapters 14–15 -->

**13.** Phoenix eventually starts, but point-of-sale systems fail and stores must process transactions manually. Orders are lost or duplicated, customers are charged more than once, and credit-card information is exposed. The teams spend days fighting fires, and emergency repairs introduce still more uncertainty into the environment.

**14.** The failure deepens the conflict between departments. Operations believes Development handed over incomplete software, while Development believes Operations failed to provide the required environments and infrastructure. Yet Bill and Development leader **Chris Allers** begin to recognize that both groups are trapped in the same failing system. They agree that they must work together if the company is to survive.

</NarrativeSlide>

---

<NarrativeSlide number="08" title="The fourth type of work"
  image1="Straight-on photograph of a physical work board: planned project and maintenance cards remain untouched in the backlog while current and in-progress columns are filled edge to edge with red Phoenix incident cards; a technician adds another timestamped incident."
  image1Src="/images/jpeg/paragraph-15-unplanned-work-board.jpg"
  image2="Steve’s office at night: a monitor shows an accounts-receivable batch with many invoices marked Failed, beside a printed cash forecast with a clearly readable $50M shortfall; Bill sets his badge on the desk and leaves while Steve holds the phone."
  image2Src="/images/jpeg/paragraph-16-cash-shortfall-resignation.jpg"
>

**15.** Bill then realizes what Erik calls the fourth type of work: **unplanned work**. Official schedules show projects, internal IT work and planned changes, but they do not show the incidents and emergency repairs consuming much of the organization’s capacity. Phoenix has displaced nearly all planned work, while the failures caused by Phoenix generate even more unplanned work.

<!-- Chapters 16–17 -->

**16.** A failure in the customer-invoicing system threatens a cash shortfall of about $50 million. When Steve demands immediate action without giving the team time to understand the situation, Bill refuses to allow uncontrolled changes and resigns. After speaking with Erik, Steve recognizes that his own leadership is perpetuating the problem. He apologizes and asks Bill to return for ninety days, admitting that the company’s leadership must change as well as IT.

</NarrativeSlide>

---

<NarrativeSlide number="09" title="Stop starting. Start finishing."
  image1="Close documentary view of an incident postmortem spread across a worktable: recurring failure reports are linked by matching ticket IDs to deferred maintenance items, emergency patches, and duplicate change requests; Bill and Steve trace the repeated IDs with markers."
  image1Src="/images/jpeg/paragraph-17-postmortem-technical-debt.jpg"
  image2="A portfolio-management board shows dozens of project rows marked PAUSED, with only Phoenix, critical maintenance, and security marked ACTIVE; at the side, an engineer returns an unapproved request form to a business manager at the intake desk."
  image2Src="/images/jpeg/paragraph-18-project-freeze-board.jpg"
>

<!-- Chapters 18–19 -->

**17.** Steve brings the leaders of Development, Operations, Security and the business together and asks them to rebuild trust. Bill explains that IT has accepted more work than it can process. The resulting shortcuts create technical debt, which produces failures and still more unplanned work.

**18.** With Steve’s support, the company freezes most new project work. Development, QA, Operations and Security concentrate on Phoenix and on reducing the backlog created by years of overloaded systems. Business managers are no longer allowed to bypass priorities by sending private requests directly to individual engineers.

</NarrativeSlide>

---

<NarrativeSlide number="10" title="Protect flow, reduce risk"
  image1="At adjacent identical server racks, Brent demonstrates a critical procedure while senior engineers reproduce it independently from a numbered shared runbook; the nearby ticket dashboard visibly reassigns incoming work from Brent to named engineers."
  image1Src="/images/jpeg/paragraph-19-brent-runbook-training.jpg"
  image2="On the plant floor, John holds a thick audit binder while Erik demonstrates an actual machine guard, light curtain, emergency stop, and completed inspection checklist; the protected machine continues operating behind the barrier."
  image2Src="/images/jpeg/paragraph-20-risk-based-safety.jpg"
>

<!-- Chapter 20 -->

**19.** Erik explains that Brent is not simply a work center; he is supporting too many work centers throughout the company. The team should accept work that does not require him, prioritize improvements that increase his capacity and prevent unauthorized changes that create emergencies. Senior engineers continue learning and documenting his methods so that Brent is not the only person capable of performing critical tasks.

<!-- Chapter 21 -->

**20.** An audit confrontation exposes another problem. Chief Information Security Officer **John Pesche** has generated large amounts of compliance work without clearly connecting it to actual business risk. Erik challenges him to learn from the safety organization in the manufacturing plant: effective controls should protect the flow of work and reduce risk, not merely produce paperwork at the end.

</NarrativeSlide>

---

<NarrativeSlide number="11" title="Work begins to flow"
  image1="Patty moves cards on a physical Kanban board with three readable lane headings: Avoid Brent, Increase Capacity, and Needs Brent; queue columns are visibly fuller than the active-work column, and each card has an owner and date."
  image1Src="/images/jpeg/paragraph-21-kanban-brent-work.jpg"
  image2="Straight-on view of a team Kanban board with explicit WIP limits printed above each column; blocked cards carry handoff timestamps, recurring maintenance cards reference numbered runbooks, and a nearby laptop shows a scheduled automation job completed successfully."
  image2Src="/images/jpeg/paragraph-22-wip-limits-automation.jpg"
>

<!-- Chapters 22–23 -->

**21.** Patty begins using Kanban boards to make service requests and other operational work visible. She separates work according to whether it avoids Brent, increases Brent’s capacity or depends on him. The team also studies why supposedly simple Phoenix tasks take so long and discovers that most of the delay occurs while work waits between overloaded teams.

**22.** They respond by limiting work in progress, standardizing recurring tasks and improving handoffs. Instead of measuring how busy every individual appears, they begin measuring whether work is moving through the whole system. Preventive work, documentation and automation are treated as necessary investments rather than distractions from project delivery.

</NarrativeSlide>

---

<NarrativeSlide number="12" title="Begin with business value"
  image1="Artifact-focused dependency-mapping session: a printed sales-order workflow, marketing calendar, and finance close checklist are pinned beside a CMDB service map; Bill, Patty, and John draw specific lines between business steps and application or server cards."
  image1Src="/images/jpeg/paragraph-23-business-dependency-map.jpg"
  image2="Close screenshot of a continuous-integration build with unit tests, security scan, and evidence archive stages all passing; beside it, a security engineer reviews a pull-request diff and attached threat-model checklist with a developer and operator."
  image2Src="/images/jpeg/paragraph-24-integrated-security-pipeline.jpg"
>

<!-- Chapters 24–27 -->

**23.** John changes his approach and begins asking business leaders what they are trying to achieve and which risks actually threaten those objectives. Bill and Patty conduct similar interviews with Sales, Marketing and Finance. They discover that many business goals depend on IT, although IT was rarely involved when those goals and projects were selected.

**24.** The teams begin evaluating projects and security controls according to business value and risk. Security specialists work with Development and Operations during ordinary work instead of delivering requirements immediately before release. This reduces separate compliance projects and allows controls and audit evidence to be built into the systems themselves.

</NarrativeSlide>

---

<NarrativeSlide number="13" title="Feedback moves upstream"
  image1="Over-the-shoulder view of side-by-side terminal diffs for Production and QA: one extra database setting is highlighted only in Production, and the change history links it to Sarah’s private request; Brent and a DBA compare the screens."
  image1Src="/images/jpeg/paragraph-25-production-qa-drift.jpg"
  image2="Close screenshot of a code-review pull request: a configuration diff has inline comments from Operations and Brent about capacity, logging, deployment, and the production environment; the developer replies and pushes an updated revision before merge."
  image2Src="/images/jpeg/paragraph-26-feedback-upstream.jpg"
>

<!-- Chapter 28 -->

**25.** A later Phoenix deployment is smaller and proceeds more smoothly, but it still encounters a serious database problem. The team discovers that Brent had previously made a special change at **Sarah Moulton’s** request, creating a difference between the production environment and the assumptions used by Development and QA. The release succeeds, but the incident shows that undocumented expert intervention remains dangerous.

<!-- Chapter 29 -->

**26.** Erik introduces the **Second Way**: feedback must travel quickly from Operations back toward Development. Quality cannot be inspected into the product only at the end. Brent and Operations knowledge must be involved earlier, when applications and environments are being designed. The company forms a small cross-functional team to develop business features outside the main Phoenix release cycle.

</NarrativeSlide>

---

<NarrativeSlide number="14" title="Toward continuous delivery"
  image1="Documentary factory view of two real production cells: one has a huge batch waiting during a long tool change, while the other processes small trays after a rapid die swap; Erik demonstrates the quick-change fixture to Bill."
  image1Src="/images/jpeg/paragraph-27-small-batches-changeover.jpg"
  image2="A wall value-stream map contains more than one hundred sticky notes with wait times; beside it, a laptop build run shows environment creation, tests, packaging, security scan, and deployment completed, while team members replace selected manual notes with automation cards."
  image2Src="/images/jpeg/paragraph-28-value-stream-automation.jpg"
>

<!-- Chapter 30 -->

**27.** At the manufacturing plant, Erik explains how smaller batches and shorter changeover times allow a factory to respond more quickly. He challenges Bill to imagine deploying software ten times a day. The goal is not speed for its own sake, but a deployment pipeline in which code, environments and configuration can move safely and repeatedly from Development to production.

<!-- Chapter 31 -->

**28.** Bill’s cross-functional team maps every step required to deploy a change. The map contains more than a hundred manual steps, delays and failure points. They identify environment creation and code packaging as major problems. Development, QA, Operations and Security agree to standardize environments, keep application and infrastructure definitions under version control, and automate the path from code commit to testing and production.

</NarrativeSlide>

---

<NarrativeSlide number="15" title="Unicorn learns at speed"
  image1="Project Unicorn workspace with concrete artifacts: an infrastructure-as-code repository, matching environment manifests, green automated tests, and a deployed customer-analysis screen; on an adjacent monitor, an engineer copies the proven configuration template into the Phoenix repository."
  image1Src="/images/jpeg/paragraph-29-project-unicorn.jpg"
  image2="Dual-monitor engineering workstation: a cloud console on the left adds instances beside a performance chart showing report runtime dropping; the right monitor shows a small-cohort marketing experiment with conversion results and a deployment run where QA and security checks both pass."
  image2Src="/images/jpeg/paragraph-30-cloud-experiment.jpg"
>

<!-- Chapter 32 -->

**29.** The team becomes **Project Unicorn**. Using common environments, automated tests and a system largely separated from Phoenix’s fragile components, it begins delivering customer-analysis and marketing capabilities far faster than before. Phoenix adopts some of the same practices after the rest of the organization sees that they work.

<!-- Chapter 33 -->

**30.** When Unicorn’s reports are too slow, the team experiments with cloud computing and rapidly tests a solution. Marketing uses the new data for a small customer campaign, measures the response and expands what works. Security testing is integrated into the same automated process as QA testing, and defects can be corrected and redeployed within hours rather than waiting for another enormous release.

</NarrativeSlide>

---

<NarrativeSlide number="16" title="The business rises"
  image1="Busy automotive-parts store during Thanksgiving: checkout terminals keep processing customers while an operations laptop at the service desk shows one feature flag switched off, capacity increasing, and a store-tool deployment marked Successful."
  image1Src="/images/jpeg/paragraph-31-thanksgiving-resilience.jpg"
  image2="Controlled resilience test at an operations console: an engineer triggers a failure-injection job against one service instance; the topology dashboard marks that instance red, reroutes requests to healthy instances, and records automatic detection for the runbook update."
  image2Src="/images/jpeg/paragraph-32-chaos-monkey-test.jpg"
>

<!-- Chapter 34 -->

**31.** The new approach is tested during the Thanksgiving shopping period. Heavy traffic creates problems, but the team can disable expensive features through configuration, add capacity and deploy new tools for stores and customers quickly. Sales reach record levels, helping put Parts Unlimited back on a path to profitability. IT has become capable of responding to business conditions instead of merely reacting to failures.

<!-- Chapter 35 -->

**32.** By January, severe incidents have become rare. Through initiatives such as **Project Narwhal** and the **Chaos Monkey**, teams deliberately inject failures to find weaknesses, improve monitoring and make systems more resilient. Development, QA, Operations and Security now work as one system, continuously learning instead of waiting for a crisis to force them together.

</NarrativeSlide>

---

<NarrativeSlide number="17" title="The Three Ways"
  image1="In Steve’s glass office overlooking both the factory floor and IT status screens, Steve gives Bill a leadership-development memo and organization chart naming a COO track; Bill’s old IT badge and a new cross-business portfolio binder sit together on the desk."
  image1Src="/images/jpeg/paragraph-33-coo-track.jpg"
  image2="Straight-on view of three concrete artifacts sharing one build ID: a commit-to-production deployment record with timestamps, a production incident linked to a pull-request diff with inline comments, and a failure-injection experiment report with its resulting automated test."
  image2Src="/images/jpeg/paragraph-34-three-ways-artifacts.jpg"
>

**33.** Steve offers Bill a development path toward becoming Chief Operating Officer, explaining that technology is now inseparable from business operations. Parts Unlimited has not merely rescued Phoenix; it has changed how it selects, builds, deploys and improves technology.

<!-- Epilogue and overall message -->

**34.** The central message is expressed through the **Three Ways**. The First Way improves the flow of work from Development through Operations to the customer. The Second Way creates fast feedback from Operations to Development. The Third Way fosters continual experimentation, learning and resilience. Organizations put these ideas into practice by making work visible, limiting unfinished work, managing constraints, reducing batch sizes and automating repetitive processes. Reliable delivery is not the result of one perfect tool; it emerges when the entire organization learns to work as one system.

</NarrativeSlide>
