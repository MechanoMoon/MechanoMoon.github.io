<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mechano Moon Project</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0; padding: 0; line-height: 1.6;
      background: black; color: #f2f2f2;
      scroll-behavior: smooth; overflow-x: hidden;
    }
    body::before {
      content: ""; position: fixed; width: 200%; height: 200%;
      background: url('https://www.transparenttextures.com/patterns/stardust.png');
      animation: moveStars 60s linear infinite; z-index: -2;
    }
    @keyframes moveStars { from {transform: translate(0,0);} to {transform: translate(-500px,-500px);} }
    header {
      background: rgba(10,10,30,0.85); color: #fff; padding: 20px; text-align:center;
      position: sticky; top: 0; z-index: 1000; backdrop-filter: blur(8px); border-bottom: 2px solid #00ccff;
    }
    header h1 { margin:0; font-size:2.5rem; text-shadow: 0 0 15px #00ccff, 0 0 25px #0077ff; }
    nav { margin-top:10px; }
    nav a { color:#00ccff; text-decoration:none; margin:0 12px; font-weight:bold; transition: color .3s, text-shadow .3s; }
    nav a:hover { color:#ffcc00; text-shadow:0 0 10px #ffcc00; }
    section {
      padding:60px 20px; max-width: 1100px; margin:auto; opacity:0; transform: translateY(40px); transition: all 1s ease-out;
    }
    section.visible { opacity:1; transform: translateY(0); }
    section h2 {
      border-bottom:2px solid #00ccff; padding-bottom:10px; margin-bottom:20px; color:#00ccff;
      text-shadow:0 0 15px #00ccff, 0 0 30px #0077ff;
    }
    img { max-width:100%; border-radius:12px; margin:15px 0; box-shadow:0 0 15px rgba(0,200,255,.4); transition: transform .3s, box-shadow .3s; }
    img:hover { transform: scale(1.05); box-shadow:0 0 30px rgba(0,200,255,.8); }
    .gallery { display:flex; gap:10px; overflow-x:auto; padding:10px; }
    .gallery img { flex:0 0 auto; width:300px; height:auto; }
    .timeline { position:relative; margin:2rem 0; padding-left:40px; }
    .timeline::before { content:''; position:absolute; left:20px; top:0; bottom:0; width:4px; background:#00ccff; }
    .timeline-item { margin-bottom:20px; }
    .timeline-item h3 { margin:0; color:#ffcc00; }
    form { display:flex; flex-direction:column; gap:1rem; max-width:600px; margin:auto; background:rgba(0,0,0,.6); padding:2rem; border-radius:12px; }
    form input, form textarea, form select { padding:.75rem; border-radius:8px; border:none; font-size:1rem; }
    form button { padding:.75rem; border-radius:8px; border:none; background:#00d9ff; color:#000; font-weight:bold; cursor:pointer; }
    form button:hover { background:#00aacc; }
    #backToTop { position:fixed; bottom:20px; right:20px; background:#00ccff; color:#000; border:none; border-radius:50%; width:50px; height:50px; font-size:20px; cursor:pointer; display:none; }
    footer { background: rgba(10,10,30,.9); color:#bbb; text-align:center; padding:15px 0; margin-top:40px; border-top:2px solid #00ccff; }
  </style>
</head>
<body>
  <header>
    <h1>Mechano Moon Project</h1>
    <nav>
      <a href="#home">Home</a>
      <a href="#problem">Problem</a>
      <a href="#solution">Solution</a>
      <a href="#abstract">Abstract</a>
      <a href="#objective">Objective</a>
      <a href="#innovation">Innovation</a>
      <a href="#methodology">Methodology</a>
      <a href="#scientific">Scientific Methodology</a>
      <a href="#results">Results</a>
      <a href="#timeline">Timeline</a>
      <a href="#gallery">Gallery</a>
      <a href="#ask">Ask a Question</a>
      <a href="#acknowledgement">Acknowledgement</a>
    </nav>
  </header>

  <section id="home">
    <h2>Welcome to the Mechano Moon Project</h2>
    <p>Welcome to the Mechano Moon Project, an ambitious, student-driven effort to show how in-situ resource utilization can move from science fiction to daily engineering practice. Our vision is simple to state yet difficult to execute: if we wish to build sustainable habitats beyond Earth, we must stop launching most of our building materials from Earth’s gravity well and instead make what we need from the stuff already there. On the Moon, that “stuff” is regolith—a fine, abrasive, mineral-rich soil that blankets the lunar surface to depths of meters in many regions. Mechano Moon imagines a compact rover system that scouts, excavates, thermally processes, mixes with a sulfur binder, molds, and then places bricks or pavers to create landing pads, berms, roads, and radiation-attenuating shielding around surface assets. The project lives at the intersection of robotics, materials, and mission operations: we think like field engineers, test like experimentalists, and design like mission planners. From April through September, we evolved this concept into an integrated demonstration. We began by documenting the problem constraints that future lunar missions face: mass and volume limits, the harsh thermal environment of the lunar day-night cycle, abrasive dust, limited power budgets, communications delays, and the need for autonomous or supervised autonomy. We then translated these constraints into system requirements for the rover, its end effectors, the thermal processing unit, the mixing and compaction mechanism, and the navigation/sensing stack. In parallel, we developed a laboratory plan using terrestrial regolith simulants to test sulfur-regolith composites and quantify strength, porosity, and stability under thermal cycling. The website you are reading is both a technical brief and a live portfolio: it includes our engineering methodology, scientific method, test results-to-date, and an open invitation for other students, mentors, and space enthusiasts to ask questions or collaborate. Our team is energized by the new lunar exploration era. As agencies and commercial partners prepare to deliver instruments, rovers, and eventually crews, the gap between early sorties and thriving surface operations will be bridged by infrastructure: durable landing zones that minimize ejecta, roads that reduce wheel wear and energy use, and shielding that protects habitats and electronics from radiation and micrometeoroids. Mechano Moon proposes a practical step in that direction, paying careful attention to mass, power, and operational safety. We emphasize solutions that can be assembled from conventional components, validated with high-school and undergraduate lab resources, and incrementally upgraded as funding and access to facilities improve. The goal is not to claim a perfect final answer, but to demonstrate that disciplined engineering and scientific thinking can produce credible, testable systems that move space settlement from dream to delivery.</p>
    <img src="data:image/jpeg;base64,{{ EMBEDDED_IMAGE_BASE64 }}" alt="Mechano Moon real project image">
  </section>

  <section id="problem">
    <h2>The Problem</h2>
    <p>The challenge Mechano Moon addresses begins with physics and logistics. Launching mass from Earth is expensive, complex, and schedule-constraining. Every kilogram allocated to construction material is a kilogram not available for science payloads, power systems, life support, or redundancy. Even if we could afford to launch construction materials, the Moon presents a set of conditions that make terrestrial methods underperform. Water-based concrete is impractical due to vacuum, low pressures, and the difficulty of storing or recycling water; hydraulic systems face sealing and contamination issues in abrasive dust; and common polymers can become brittle under ultraviolet radiation and extreme thermal cycling. The lunar regolith itself is a double-edged sword: it is abundant and mineralogically interesting, but it is also sharp, electrostatically clingy, and capable of infiltrating mechanisms and seals. Uncontrolled regolith lofted by rocket plumes can sandblast equipment hundreds of meters away. Thus the primary “problem” is broader than just making a brick: it is producing infrastructure elements with minimal imported mass, minimal water, high durability, and processes that tolerate dust, vacuum, and temperature swings of roughly −170°C to +120°C. Another dimension of the problem is operations. Many early missions will have little time margin for construction while pursuing their primary science or exploration tasks. Construction activities need to be either autonomous or compatible with short, discrete supervision windows. Power is also limited: surface systems must balance duty cycles with solar availability and battery capacities. Thermal management must prevent heat loss at night and manage waste heat during the day. Communication latency and line-of-sight constraints mean the rover must make local decisions for navigation, material handling, and quality assurance without constant human teleoperation. Finally, safety constraints demand careful handling of dust and sulfur fumes in testbeds, and strong risk mitigation for any flight-like operations. The last piece of the problem is verification. It is not enough to claim that regolith-sulfur composites can be strong. We need testable, repeatable procedures for measuring compressive strength, density, porosity, microstructural features, and stability under thermal cycling and irradiation proxies. We also need to connect lab-scale data to rover-scale process parameters—mix ratios, temperatures, compaction pressures, and cooling profiles that a fieldable system can achieve within realistic power budgets. Mechano Moon frames the problem as a chain: resource characterization, material conversion, fabrication, placement, and inspection—each link must be designed, tested, and closed with data.</p>
  </section>

  <section id="solution">
    <h2>Our Solution</h2>
    <p>Our solution combines a lightweight rover platform with a modular processing payload to perform a closed-loop build cycle: Recon → Excavate → Process → Form → Place → Inspect. The rover uses a traversable chassis with dust-tolerant wheels, brushless geared motors, and a suspension suitable for small rocks and loose regolith. A front-mounted end effector serves as a scoop for excavation and as a metering device for the processing unit. The processing module performs low-pressure heating of regolith and sulfur in a sealed chamber. By selecting sulfur as the binder, we avoid water, conserve mass, and leverage sulfur’s ability to melt at relatively low temperatures (~115°C) and resolidify to create strong composites when cooled. A compact mixing auger blends molten sulfur with preheated regolith at controlled ratios; then a compaction press molds bricks or pavers with consistent dimensions. A small articulated arm places finished units according to a planned lattice pattern. The control architecture favors supervised autonomy. During field-like tests, the rover follows predefined waypoints with obstacle detection using stereo vision and ultrasonic or solid-state lidar. Within the processing chain, temperature and torque sensors maintain thermal profiles and mixing consistency; load cells verify compaction pressure; and simple computer vision checks mold fill levels and brick surface quality. A power management module schedules high-draw tasks (heating and pressing) during peak solar input, buffering with batteries. The software stack is intentionally transparent: microcontrollers govern the thermal and actuation loops, while a single-board computer coordinates navigation and high-level state machines. Data from each batch—temperatures, mix ratios, press pressures, cooling times, and QC images—are stored to support later analysis and to update recipes. On the materials side, our process window targets sulfur fractions between 10% and 30% by mass, preheating regolith to reduce thermal shock, and compaction pressures in the tens of MPa achievable with compact electric actuators. Cooling is managed to reduce internal stresses and porosity. The resulting bricks are suitable for landing pad pavers, berm blocks, or radiation shielding modules. The system emphasizes maintainability and testability: modules can be swapped, and each stage has clear interfaces for lab characterization. In short, Mechano Moon provides a pathway to convert ubiquitous lunar dirt into purposeful infrastructure with a rover-scale system that students can prototype and iterate on Earth.</p>
  </section>

  <section id="abstract">
    <h2>Abstract</h2>
    <p>This project presents Mechano Moon, an integrated rover and processing architecture that demonstrates in-situ resource utilization for lunar construction. The core idea is the production of sulfur-bound regolith bricks and pavers using a compact, solar-powered rover capable of excavation, thermal processing, mixing, molding, and robotic placement. The abstract highlights three motivations: (1) reducing Earth launch mass for construction materials; (2) mitigating lunar dust hazards by creating landing pads and stabilized surfaces; and (3) enabling resilient, modular infrastructure that can be installed by autonomous systems ahead of or alongside human crews. The work spans concept definition, system engineering, and experimental validation with regolith simulants to identify feasible process windows for sulfur fractions, temperatures, compaction pressures, and cooling profiles. Our approach blends engineering and science. On the engineering side, we designed a dust-tolerant mechanical layout, power budget, thermal subsystem, and control logic for supervised autonomy. On the science side, we conducted laboratory tests to measure compressive strength, density, and microstructural features across mix ratios, and we subjected samples to thermal cycling to emulate lunar day–night extremes. We report trends, uncertainties, and practical constraints that translate lab findings into rover setpoints. The abstract also frames the broader implications: sulfur-regolith composites could create pavers that resist erosion from rocket plumes, berms that capture ejecta, and blocks that provide mass for radiation shielding, all with minimal imported material. While further work is needed—particularly long-duration cycling, vacuum testing, and radiation exposure—our results indicate that the Mechano Moon process can create components with strengths in the single- to low-double-digit MPa range, sufficient for many surface applications when arranged in engineered patterns. The project advances the conversation from “can we build on the Moon?” to “how do we operate a reliable, power-aware, student-scale system that does it?”</p>
  </section>

  <section id="objective">
    <h2>Introduction & Objective</h2>
    <p>The introduction and objectives of Mechano Moon establish the mission context, design philosophy, and measurable targets that guide our work. We begin with a mission posture: near-term lunar missions need enabling infrastructure—durable landing surfaces and protected zones—to operate safely and repeatedly. Our objective is to prove, at student-lab scale, that a small rover can create such infrastructure by producing sulfur-regolith bricks with predictable properties. Success is defined not only by material strength metrics but by a cohesive operations concept that fits within realistic power, mass, and communication constraints. Key objectives include: (1) design a rover with dust-tolerant drive and excavation subsystems that can collect regolith simulant efficiently; (2) build a compact thermal processing unit that melts sulfur and preheats regolith with minimal losses; (3) achieve consistent mixing and compaction to produce bricks with tight dimensional tolerances; (4) implement sensing for process control and QC, including temperature, torque, and load measurements; (5) demonstrate supervised autonomous navigation and placement; and (6) generate a complete dataset linking process parameters to material outcomes. Secondary objectives involve safety, maintainability, and educational value: all procedures should be reproducible with accessible equipment and documented to support future teams. We adopt a systems engineering method: requirements flow from mission needs to subsystem allocations. Power budgets guide actuator selection and duty cycles; mass budgets guide structure materials and modularity; thermal analyses inform insulation and heater sizing. Risk reduction is staged: benchtop studies of sulfur-regolith mixing precede integrated rover tests; software-in-the-loop simulations de-risk navigation before hardware trials. The objectives culminate in a demo: building a small “landing pad” patch or berm section with measured performance. By stating clear objectives and a verification plan, we keep the project grounded in achievable, measurable steps while still pointing toward flight-relevant outcomes.</p>
  </section>

  <section id="innovation">
    <h2>Innovation</h2>
    <p>Mechano Moon’s innovation is not a single gadget but the careful coupling of known mechanisms into a cohesive, fieldable system for lunar construction. First, we champion sulfur as a lunar binder because it melts at modest temperatures, requires no water, and can solidify into a strong matrix that encapsulates grains of regolith. Second, we integrate excavation, thermal processing, mixing, molding, and placement into a small footprint payload, reducing interfaces and handling losses. Third, we encode autonomy where it pays off: local obstacle avoidance, process control loops, and QC routines that reduce human workload without sacrificing transparency. Finally, we design for verification: every step produces data, from heater temperatures to compaction forces and image-based surface checks, enabling rapid iteration and trustworthy conclusions. On the mechanical side, innovation appears in dust management and modularity. Seals, labyrinth paths, and sacrificial shields protect bearings and actuators. The processing chamber features interchangeable liners for easy cleaning after sulfur runs. The mold set is standardized so we can produce bricks and pavers with different textures or interlocks without retooling the press. On the electrical side, we prioritize efficient heaters, MOSFET-based power stages, and current sensing to characterize energy cost per brick. On the software side, finite-state machines govern the build cycle, while logs synchronize sensor data with timestamps for later analysis. Unlike many concept papers, we provide a pathway for student teams to reproduce the work: off-the-shelf components, open-source code, and clear calibration procedures. The innovation is practical, modular, and aimed at closing the loop from concept to data-backed results.</p>
  </section>

  <section id="methodology">
    <h2>Methodology</h2>
    <p>Our methodology has two intertwined tracks: engineering workflow for the rover system and laboratory workflow for materials characterization. The engineering workflow follows six stages. (1) Recon: survey the site and plan a path with waypoints and hazard maps. (2) Excavate: engage the scoop, meter material, and deliver to the processing inlet with sensors monitoring torque and fill. (3) Process: heat sulfur and prewarm regolith, control temperatures near 120–140°C to maintain melt without decomposition, and log energy consumption. (4) Mix: use an auger or paddle mixer to achieve even distribution at target mass fraction, tracking motor current as a proxy for viscosity. (5) Form: compress into a mold at set pressure and dwell time; optionally vibrate to reduce voids. (6) Place & Inspect: move the part to a staging area, scan for geometry and surface defects, and record location for pad assembly. The laboratory workflow provides the science underpinnings. We prepare batches across sulfur mass fractions (10%, 15%, 20%, 25%, 30%), mold standardized specimens, and measure compressive strength, density, porosity (via water replacement or image analysis), and thermal cycling durability (e.g., −40°C to +80°C in a chamber as a proxy). Where available, we perform microstructural evaluation with optical microscopy or SEM images from partner labs. Each batch has a process log to connect inputs to outputs. Data analysis includes means, standard deviations, and confidence intervals, plus regression to map how strength varies with sulfur content and compaction pressure. We also analyze the energy per brick to inform rover power planning. Safety and quality are integral. Fume extraction and PPE mitigate sulfur vapors; dust handling procedures limit exposure to simulant fines. Calibration routines cover thermocouples, load cells, and torque estimation. Acceptance criteria define what “good” looks like: compressive strength above a threshold for intended use (e.g., >5 MPa for pavers), dimensional tolerance within 2%, and no critical surface defects. Finally, we translate lab-optimal settings into rover setpoints, acknowledging real-world constraints and making clear where performance margins lie.</p>
  </section>

  <section id="scientific">
    <h2>Scientific Methodology</h2>
    <p>We frame our scientific methodology around the hypothesis that sulfur-regolith composites can achieve sufficient mechanical strength and environmental stability for lunar surface infrastructure when processed within specific temperature, composition, and compaction windows. To test this, we define independent variables (sulfur mass fraction, regolith preheat temperature, compaction pressure, cooling time) and dependent variables (compressive strength, density, porosity, microstructural indicators, thermal cycling retention). Controls include ambient conditions, mold geometry, and specimen size. We aim for at least five replicates per condition to estimate variance and perform ANOVA across groups. Materials: we use commercially available regolith simulants that capture grain size distribution and mineral phases of lunar highlands or mare soils. Sulfur is food or technical grade. Equipment includes a thermostatically controlled heater for sulfur, an oven or hotplate to preheat simulant, a mixing chamber with torque monitoring, a mechanical press with a load cell, and sensors for temperature. For cycling, we use an environmental chamber if available; in its absence, we perform repeated heating and cooling cycles. Measurements follow standard practices where possible, adapting ASTM-like procedures for compressive testing while documenting any deviations. Microstructure is examined with optical microscopy and, when possible, scanning electron micrographs to assess bonding and voids. Data analysis: for each batch we compute means and standard deviations, plot stress–strain where possible, and evaluate correlations between variables. We track energy per brick to understand the system-level trade between material quality and power draw. Uncertainty is treated explicitly: instrument accuracy and repeatability are factored into error bars. We also perform sensitivity analyses to identify the most influential parameters. The method culminates in a decision framework: choose sulfur fraction and compaction pressure that meet strength targets with minimal energy, and verify durability through cycling. The outcome is a set of “recipes” that a rover can implement with onboard sensing and control.</p>
  </section>

  <section id="results">
    <h2>Results & Conclusion</h2>
    <p>Our results to date support the feasibility of sulfur-bound regolith components for lunar infrastructure. In bench tests, specimens with sulfur fractions near 20–25% and moderate compaction achieved compressive strengths in the single- to low-double-digit MPa range. Density and porosity trends aligned with expectations: higher sulfur content reduced porosity up to a point, after which excess binder introduced defects on cooling. Thermal cycling caused some strength reduction, but carefully controlled cooling profiles and modest post-processing anneals mitigated the effect. Energy accounting indicated that preheating the regolith reduced the total energy per brick by lowering the viscosity of the mix and shortening the time in the press. Image-based QC flagged surface voids that correlated with lower strength, confirming the value of automated inspection. We also learned practical lessons. Dust-proofing bearings and seals dramatically extended the life of mechanical assemblies in simulant. Torque monitoring proved to be a convenient proxy for mixture consistency, enabling the controller to adjust dwell time before molding. The control software’s state-machine architecture simplified fault handling: if a temperature target was not reached in time, the cycle paused or aborted safely and logged the event. In field-like demos, waypoint navigation with simple obstacle detection was sufficient for moving between a stockpile and a staging area, though future work should add more robust perception. Overall, the results point toward a scalable, student-accessible method to build lunar-relevant components from local materials, with clear paths for improvement and verification under more flight-like conditions.</p>
  </section>

  <section id="timeline">
    <h2>Project Timeline</h2>
    <div class="timeline">
      <div class="timeline-item"><h3>April</h3><p>Project ideation, system constraints, and early sketches.</p></div>
      <div class="timeline-item"><h3>May</h3><p>Electronics architecture planning and control strategy.</p></div>
      <div class="timeline-item"><h3>June</h3><p>Processing chamber prototypes and heater tests.</p></div>
      <div class="timeline-item"><h3>July</h3><p>Mixing and compaction trials with simulant batches.</p></div>
      <div class="timeline-item"><h3>August</h3><p>Integrated rover demo and QC imaging pipeline.</p></div>
      <div class="timeline-item"><h3>September</h3><p>Data analysis, website, and outreach materials.</p></div>
    </div>
  </section>

  <section id="gallery">
    <h2>Project Gallery</h2>
    <div class="gallery">
      <img src="data:image/jpeg;base64,{{ EMBEDDED_IMAGE_BASE64 }}" alt="Mechano Moon Model">
      <img src="data:image/jpeg;base64,{{ EMBEDDED_IMAGE_BASE64 }}" alt="Mechano Moon Close-up">
      <img src="data:image/jpeg;base64,{{ EMBEDDED_IMAGE_BASE64 }}" alt="Mechano Moon Display">
      <img src="data:image/jpeg;base64,{{ EMBEDDED_IMAGE_BASE64 }}" alt="Mechano Moon Poster">
    </div>
  </section>

  <section id="ask">
    <h2>Ask a Question</h2>
    <p>Send your questions directly to our team. This form uses Formspree to deliver messages to our inbox. Replace <code>your-form-id</code> with your real Formspree endpoint after signing in with <strong>mechanomoon2@gmail.com</strong>.</p>
    <form action="https://formspree.io/f/xqadnaey" method="POST">
      <input type="text" name="name" placeholder="Your Name" required />
      <input type="email" name="email" placeholder="Your Email" required /> 
      <select name="topic">
        <option value="general">General Question</option>
        <option value="science">Science & Methodology</option>
        <option value="rover">Rover Design</option>
      </select>
      <textarea name="message" rows="6" placeholder="Your Message" required></textarea>
      <input type="hidden" name="_subject" value="New Question from Mechano Moon Website">
      <button type="submit">Send Question</button>
    </form>
  </section>

  <section id="acknowledgement">
    <h2>Acknowledgement & References</h2>
    <p>We gratefully acknowledge mentors, educators, and peers who strengthened this project from April through September. Guidance on systems engineering and careful test design helped us translate enthusiasm into disciplined progress. Access to lab spaces and donated materials made it possible to prototype processing chambers and molds. Constructive feedback from reviewers sharpened our objectives, reminded us to define acceptance criteria, and encouraged us to document every calibration and test. We also thank open-source communities whose libraries enable reliable micro-controller control loops, logging, and visualization, and the many student teams whose published notebooks inspired our methods. Any remaining errors are our own, and we welcome questions, critiques, and collaboration proposals. We recognize that Mechano Moon sits within a larger ecosystem of lunar ISRU research spanning agencies, universities, and industry. Our contribution is modest but practical: a blueprint and dataset for small teams to explore sulfur-regolith composites and rover-scale manufacturing. We plan to release designs, code, and anonymized data as they are hardened, with the hope that others will replicate, refine, and extend them. Finally, we acknowledge family and friends for the countless hours of encouragement, and we remain grateful to the community that believes students can help build the future—one careful experiment and one rugged brick at a time.</p>
  </section>

  <footer>
    <p>&copy; 2025 Mechano Moon Project | Designed by Team Innovators</p>
  </footer>

  <button id="backToTop">↑</button>

  <script>
    const sections = document.querySelectorAll("section");
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => { if (entry.isIntersecting) entry.target.classList.add("visible"); });
    }, { threshold: 0.2 });
    sections.forEach(s => observer.observe(s));
    const backToTop = document.getElementById("backToTop");
    window.addEventListener("scroll", () => { backToTop.style.display = window.scrollY > 400 ? "block" : "none"; });
    backToTop.addEventListener("click", () => window.scrollTo({ top: 0, behavior: "smooth" }));
  </script>
</body>
</html>

