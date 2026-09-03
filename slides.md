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
  <div class="visual-grid cover-art">
    <div class="art-frame">
      <div class="frame-id">COVER A</div>
      <div class="frame-copy">Wide exterior of the Parts Unlimited automotive-parts factory at dawn, loading bays and production halls visible, clean documentary composition, no people posing, no text or logos.</div>
    </div>
    <div class="art-frame">
      <div class="frame-id">COVER B</div>
      <div class="frame-copy">Close view through a factory doorway where a physical assembly line transitions into orderly streams of software data, restrained realistic editorial style, no words or logos.</div>
    </div>
  </div>
  <h1>The Phoenix Project</h1>
</div>

---

<NarrativeSlide number="01" title="A company bets on Phoenix"
  image1="Exterior of the Parts Unlimited automotive-parts factory, with a clearly visible door marked only by visual IT symbols leading into an older technology wing; retail stores and online orders implied in the distance; realistic editorial illustration, no written labels."
  image2="Bill Palmer receiving an unexpected executive promotion in the foreground while the former CIO and VP of IT Operations leave through a distant back exit carrying boxes; Bill looks reluctant, Steve gestures toward the troubled IT floor; no text or logos."
>

<!-- Prologue and Chapter 1 -->

**1.** *The Phoenix Project* takes place at **Parts Unlimited**, an automotive-parts manufacturer and retailer struggling to compete with faster rivals. The company has invested heavily in **Project Phoenix**, a large IT initiative intended to modernize its retail and online business. Phoenix is already late and over budget, but senior management believes that the company’s future depends on launching it.

**2.** **Bill Palmer**, formerly the Director of Midrange Technology Operations, is unexpectedly promoted to Vice President of IT Operations after the CIO and Bill’s previous boss are fired. The CEO, **Steve Masters**, gives him ninety days to stabilize IT and help rescue Phoenix, warning that IT Operations may otherwise be outsourced. Bill accepts reluctantly, knowing that senior IT positions at Parts Unlimited have a habit of ending badly.

</NarrativeSlide>

---

<NarrativeSlide number="02" title="The first fire"
  image1="Close view of a monitor filled with visibly corrupted payroll rows and broken data symbols; Bill Palmer stares at it in shock while two nearby technicians react with alarm; failed storage hardware glows red behind them; no legible interface text."
  image2="A chaotic IT workspace shown as tangled cables and undocumented changes converging on Brent at one workstation; engineers discover hidden system dependencies only when warning lights appear; concrete technical detail, not a posed meeting scene."
>

<!-- Chapters 2–3 -->

**3.** Bill’s first crisis is not Phoenix but payroll. Records for thousands of hourly employees have been corrupted, putting their salaries at risk. A simultaneous storage-system failure initially obscures the cause, but the payroll corruption is eventually traced to an unauthorized tokenization change deployed to protect personal data and satisfy an audit finding. The change was introduced without adequate testing because no suitable test environment was available.

**4.** The incident shows Bill that the company does not know what is happening inside its own IT systems. Engineers make changes without telling one another, urgent work bypasses normal procedures, and teams discover dependencies only after something breaks. Almost every difficult problem eventually reaches **Brent**, an experienced engineer who understands many systems that nobody else fully understands.

</NarrativeSlide>

---

<NarrativeSlide number="03" title="Two systems at war"
  image1="A fragile Phoenix software package on a conveyor between two work areas: developers push feature boxes toward release while operations engineers brace failing production servers on the other side; visual conflict between speed and stability, no text."
  image2="Bill and Erik walking beside an automotive assembly line where parts pile up dramatically at one narrow work center while every downstream station sits idle; the physical bottleneck is unmistakable, realistic factory detail."
>

<!-- Chapter 4 -->

**5.** Before Bill can bring the situation under control, management accelerates Phoenix. Development says that the software must be released, while Operations warns that requirements are incomplete and testing is inadequate. Development is judged by its ability to deliver features, whereas Operations is judged by production stability. Each side therefore sees the other as an obstacle.

<!-- Chapter 5 -->

**6.** Bill meets **Erik Reid**, a prospective board member who takes him through one of the company’s manufacturing plants. Erik asks Bill to think about IT as a production system. Work must flow through a sequence of work centers, and the output of the entire system is limited by its most constrained resource. Starting more work cannot improve output when the constraint is already overloaded.

</NarrativeSlide>

---

<NarrativeSlide number="04" title="Make the invisible visible"
  image1="Patty standing beside a wall-sized board as 105 project folders and change cards crowd every lane; cards visibly collide around the same production systems while maintenance and security work waits at the edges; no readable words."
  image2="A retail payment terminal failing beside a phone showing a chaotic incident call, while a nearby calendar date is buried beneath more than one hundred change cards scheduled for the Phoenix launch; Brent tests a cable without knowing why it works."
>

<!-- Chapters 6–8 -->

**7.** Back at work, Bill discovers that IT has committed to approximately 105 projects, in addition to maintenance, security requirements and support work. He also asks **Patty McKee** to revive the change-management process. The first meetings are confused and unpopular, but writing changes on cards and placing them on a shared board begins to reveal how many teams are modifying production at the same time.

<!-- Chapter 9 -->

**8.** When the company’s credit-card processing systems fail, the incident call descends into guesswork and blame. Brent restores service almost accidentally while trying possible fixes, but the team cannot explain exactly what happened. Bill insists on better incident procedures and documentation. Meanwhile, the change board reveals that more than a hundred changes are planned for the same day as the Phoenix launch.

</NarrativeSlide>

---

<NarrativeSlide number="05" title="The constraint has a name"
  image1="Brent trying to work on Phoenix while phones, chat alerts, paper tickets, and coworkers interrupt from every direction; Bill observes nearby as a senior engineer records Brent’s procedure in a notebook; focused narrative composition."
  image2="Multiple technical work streams—servers, databases, network gear, and application releases—narrow into a single workstation occupied by Brent, then emerge as a long queue; a clear human bottleneck rendered as a realistic workplace metaphor."
>

<!-- Chapters 10–11 -->

**9.** Bill watches Brent and finally sees the scale of the problem. Brent is supposedly working on Phoenix, but calls, messages and visitors interrupt him continuously. Bill tries to protect him by routing requests through senior engineers, requiring them to document what Brent does and ensuring that he does not solve the same problem twice.

**10.** The new change process reveals that many planned changes cannot be completed because they conflict with other work, require unavailable people or depend on Brent. Bill recognizes Brent as a constraint shared by many different work centers. The more work everyone sends to him, the longer every project must wait.

</NarrativeSlide>

---

<NarrativeSlide number="06" title="Past the point of no return"
  image1="Side-by-side test and production server racks that are visibly mismatched, surrounded by unfinished software packages arriving faster than QA can inspect them; deployment checklists spill across operations equipment; no generic boardroom."
  image2="A database migration progress display barely moving as the night clock advances; behind Bill, a rollback bridge to the old systems is physically retracting while Phoenix marketing material is already being delivered to stores; no legible text."
>

<!-- Chapters 12–13 -->

**11.** The Phoenix deployment nevertheless goes ahead. It is a huge, fragile operation involving Development, Quality Assurance, Operations, database administrators and business representatives. The software is not functioning properly in the test environment, new releases continue arriving from Development, and the production infrastructure differs from what developers and testers expected.

**12.** Bill warns that the launch should be delayed, but Marketing campaigns and executive commitments have already been made. The database conversion begins and runs far more slowly than planned. By the time the team understands the problem, it has passed the point at which the old systems can easily be restored.

</NarrativeSlide>

---

<NarrativeSlide number="07" title="Phoenix burns"
  image1="Inside an automotive-parts store, point-of-sale terminals show error states, staff write manual receipts, duplicate order slips spill from a printer, and worried customers hold payment cards; exhausted support staff work in the background."
  image2="Development and Operations stand on opposite sides of a cracked Phoenix release machine, initially pointing at each other, then beginning to repair the same broken mechanism together; Chris and Bill are clearly leading the joint effort."
>

<!-- Chapters 14–15 -->

**13.** Phoenix eventually starts, but point-of-sale systems fail and stores must process transactions manually. Orders are lost or duplicated, customers are charged more than once, and credit-card information is exposed. The teams spend days fighting fires, and emergency repairs introduce still more uncertainty into the environment.

**14.** The failure deepens the conflict between departments. Operations believes Development handed over incomplete software, while Development believes Operations failed to provide the required environments and infrastructure. Yet Bill and Development leader **Chris Allers** begin to recognize that both groups are trapped in the same failing system. They agree that they must work together if the company is to survive.

</NarrativeSlide>

---

<NarrativeSlide number="08" title="The fourth type of work"
  image1="A carefully planned work board is buried by a cascading wave of red incident tickets and emergency repairs; Phoenix consumes nearly every available lane while scheduled maintenance disappears underneath, concrete operational metaphor."
  image2="Fifty million dollars’ worth of customer invoices visibly trapped in a stalled digital queue; in the foreground Bill places his company badge on a desk and walks away while Steve remains on an angry late-night phone call."
>

**15.** Bill then realizes what Erik calls the fourth type of work: **unplanned work**. Official schedules show projects, internal IT work and planned changes, but they do not show the incidents and emergency repairs consuming much of the organization’s capacity. Phoenix has displaced nearly all planned work, while the failures caused by Phoenix generate even more unplanned work.

<!-- Chapters 16–17 -->

**16.** A failure in the customer-invoicing system threatens a cash shortfall of about $50 million. When Steve demands immediate action without giving the team time to understand the situation, Bill refuses to allow uncontrolled changes and resigns. After speaking with Erik, Steve recognizes that his own leadership is perpetuating the problem. He apologizes and asks Bill to return for ninety days, admitting that the company’s leadership must change as well as IT.

</NarrativeSlide>

---

<NarrativeSlide number="09" title="Stop starting. Start finishing."
  image1="An overloaded intake funnel crammed with projects feeds shortcuts into a growing heap of technical debt, which in turn produces broken servers and emergency tickets; Steve and Bill examine the self-reinforcing cycle, no labels."
  image2="A large project warehouse placed visibly in freeze: dozens of project crates are sealed behind barriers while only Phoenix, critical maintenance, and security work move along three clear lanes; side doors for private requests are locked."
>

<!-- Chapters 18–19 -->

**17.** Steve brings the leaders of Development, Operations, Security and the business together and asks them to rebuild trust. Bill explains that IT has accepted more work than it can process. The resulting shortcuts create technical debt, which produces failures and still more unplanned work.

**18.** With Steve’s support, the company freezes most new project work. Development, QA, Operations and Security concentrate on Phoenix and on reducing the backlog created by years of overloaded systems. Business managers are no longer allowed to bypass priorities by sending private requests directly to individual engineers.

</NarrativeSlide>

---

<NarrativeSlide number="10" title="Protect flow, reduce risk"
  image1="Brent demonstrates a critical server procedure while several senior engineers reproduce it independently from shared documentation; incoming work is redirected around him and the once-long queue begins to divide across capable people."
  image2="John stands between a towering stack of audit paperwork and a factory line protected by practical guards, sensors, and emergency stops; Erik points toward the working safety controls that protect flow instead of producing paper."
>

<!-- Chapter 20 -->

**19.** Erik explains that Brent is not simply a work center; he is supporting too many work centers throughout the company. The team should accept work that does not require him, prioritize improvements that increase his capacity and prevent unauthorized changes that create emergencies. Senior engineers continue learning and documenting his methods so that Brent is not the only person capable of performing critical tasks.

<!-- Chapter 21 -->

**20.** An audit confrontation exposes another problem. Chief Information Security Officer **John Pesche** has generated large amounts of compliance work without clearly connecting it to actual business risk. Erik challenges him to learn from the safety organization in the manufacturing plant: effective controls should protect the flow of work and reduce risk, not merely produce paperwork at the end.

</NarrativeSlide>

---

<NarrativeSlide number="11" title="Work begins to flow"
  image1="Patty arranges a physical Kanban board into three visually distinct lanes: work bypassing Brent, work increasing his capacity, and work requiring him; most task cards wait between overloaded stages rather than being worked."
  image2="Small standardized work packets move smoothly through connected Development, QA, Operations, and Security stations; documentation and automation tools keep each handoff moving while oversized batches remain stopped outside the system."
>

<!-- Chapters 22–23 -->

**21.** Patty begins using Kanban boards to make service requests and other operational work visible. She separates work according to whether it avoids Brent, increases Brent’s capacity or depends on him. The team also studies why supposedly simple Phoenix tasks take so long and discovers that most of the delay occurs while work waits between overloaded teams.

**22.** They respond by limiting work in progress, standardizing recurring tasks and improving handoffs. Instead of measuring how busy every individual appears, they begin measuring whether work is moving through the whole system. Preventive work, documentation and automation are treated as necessary investments rather than distractions from project delivery.

</NarrativeSlide>

---

<NarrativeSlide number="12" title="Begin with business value"
  image1="Sales orders, marketing campaigns, and finance reports appear as business outcomes resting on a previously hidden foundation of servers and software; John, Bill, and Patty trace each outcome down to its IT dependency."
  image2="Security controls are installed directly inside a moving software delivery pipeline—automated checks, evidence capture, and risk gates beside Development and Operations—while a separate late-stage compliance barrier is dismantled."
>

<!-- Chapters 24–27 -->

**23.** John changes his approach and begins asking business leaders what they are trying to achieve and which risks actually threaten those objectives. Bill and Patty conduct similar interviews with Sales, Marketing and Finance. They discover that many business goals depend on IT, although IT was rarely involved when those goals and projects were selected.

**24.** The teams begin evaluating projects and security controls according to business value and risk. Security specialists work with Development and Operations during ordinary work instead of delivering requirements immediately before release. This reduces separate compliance projects and allows controls and audit evidence to be built into the systems themselves.

</NarrativeSlide>

---

<NarrativeSlide number="13" title="Feedback moves upstream"
  image1="A production database cabinet opens to reveal one hidden custom configuration placed there after Sarah’s private request; beside it, the supposedly identical Development and QA environments lack that part, exposing configuration drift."
  image2="A bright feedback path runs from live production monitors backward to developers designing the next version; Brent and Operations join a small cross-functional team early, before application and environment plans harden."
>

<!-- Chapter 28 -->

**25.** A later Phoenix deployment is smaller and proceeds more smoothly, but it still encounters a serious database problem. The team discovers that Brent had previously made a special change at **Sarah Moulton’s** request, creating a difference between the production environment and the assumptions used by Development and QA. The release succeeds, but the incident shows that undocumented expert intervention remains dangerous.

<!-- Chapter 29 -->

**26.** Erik introduces the **Second Way**: feedback must travel quickly from Operations back toward Development. Quality cannot be inspected into the product only at the end. Brent and Operations knowledge must be involved earlier, when applications and environments are being designed. The company forms a small cross-functional team to develop business features outside the main Phoenix release cycle.

</NarrativeSlide>

---

<NarrativeSlide number="14" title="Toward continuous delivery"
  image1="An automotive factory contrasts one huge slow production batch with many small batches moving through rapid machine changeovers; the small-batch line visually transforms into frequent safe software deployments."
  image2="A value-stream map containing more than one hundred manual handoffs folds into a short automated route from code commit through matching environments, tests, packaging, security checks, and production deployment."
>

<!-- Chapter 30 -->

**27.** At the manufacturing plant, Erik explains how smaller batches and shorter changeover times allow a factory to respond more quickly. He challenges Bill to imagine deploying software ten times a day. The goal is not speed for its own sake, but a deployment pipeline in which code, environments and configuration can move safely and repeatedly from Development to production.

<!-- Chapter 31 -->

**28.** Bill’s cross-functional team maps every step required to deploy a change. The map contains more than a hundred manual steps, delays and failure points. They identify environment creation and code packaging as major problems. Development, QA, Operations and Security agree to standardize environments, keep application and infrastructure definitions under version control, and automate the path from code commit to testing and production.

</NarrativeSlide>

---

<NarrativeSlide number="15" title="Unicorn learns at speed"
  image1="Project Unicorn travels on a clean, separate delivery track built from matching environments and automated tests, rapidly delivering customer-analysis tools while the fragile Phoenix track runs beside it and begins adopting the same mechanisms."
  image2="A slow analytics report expands across elastic cloud servers and becomes fast; alongside it, a small marketing experiment grows only after measured customer response, while QA and security tests run together in the same pipeline."
>

<!-- Chapter 32 -->

**29.** The team becomes **Project Unicorn**. Using common environments, automated tests and a system largely separated from Phoenix’s fragile components, it begins delivering customer-analysis and marketing capabilities far faster than before. Phoenix adopts some of the same practices after the rest of the organization sees that they work.

<!-- Chapter 33 -->

**30.** When Unicorn’s reports are too slow, the team experiments with cloud computing and rapidly tests a solution. Marketing uses the new data for a small customer campaign, measures the response and expands what works. Security testing is integrated into the same automated process as QA testing, and defects can be corrected and redeployed within hours rather than waiting for another enormous release.

</NarrativeSlide>

---

<NarrativeSlide number="16" title="The business rises"
  image1="A busy automotive-parts store during Thanksgiving traffic remains operational as engineers toggle off one expensive feature, add server capacity, and safely deploy store tools; checkout lines move and sales indicators rise."
  image2="A mechanical chaos monkey deliberately disconnects one component inside a redundant system; traffic automatically reroutes, monitoring detects the fault, and Development, QA, Operations, and Security calmly strengthen the weak point."
>

<!-- Chapter 34 -->

**31.** The new approach is tested during the Thanksgiving shopping period. Heavy traffic creates problems, but the team can disable expensive features through configuration, add capacity and deploy new tools for stores and customers quickly. Sales reach record levels, helping put Parts Unlimited back on a path to profitability. IT has become capable of responding to business conditions instead of merely reacting to failures.

<!-- Chapter 35 -->

**32.** By January, severe incidents have become rare. Through initiatives such as **Project Narwhal** and the **Chaos Monkey**, teams deliberately inject failures to find weaknesses, improve monitoring and make systems more resilient. Development, QA, Operations and Security now work as one system, continuously learning instead of waiting for a crisis to force them together.

</NarrativeSlide>

---

<NarrativeSlide number="17" title="The Three Ways"
  image1="Bill moves from an IT operations doorway onto the main business operations floor; ahead, a simple staircase leads toward a COO office while factory, retail, and technology work visibly operate as one connected system."
  image2="One integrated value stream shown through three concrete paths: work flowing from Development to customer, operational feedback returning upstream, and a continuous loop of experiments, controlled failures, learning, and resilience; no written labels."
>

**33.** Steve offers Bill a development path toward becoming Chief Operating Officer, explaining that technology is now inseparable from business operations. Parts Unlimited has not merely rescued Phoenix; it has changed how it selects, builds, deploys and improves technology.

<!-- Epilogue and overall message -->

**34.** The central message is expressed through the **Three Ways**. The First Way improves the flow of work from Development through Operations to the customer. The Second Way creates fast feedback from Operations to Development. The Third Way fosters continual experimentation, learning and resilience. Organizations put these ideas into practice by making work visible, limiting unfinished work, managing constraints, reducing batch sizes and automating repetitive processes. Reliable delivery is not the result of one perfect tool; it emerges when the entire organization learns to work as one system.

</NarrativeSlide>
