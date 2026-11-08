# From Running Models to Orchestrating Science: Environmental Modelling in the Age of Generative and Agentic AI

**Article type:** Position Paper (Perspective)  
**Target journal:** *Environmental Modelling & Software* (Elsevier)

---

**Alex Neumann**  
Department of Physical & Environmental Sciences, University of Toronto Scarborough, Toronto, Canada  
Email: alex.gudimov@utoronto.ca  
ORCID: *[to be inserted]*

---

## Highlights

- Generic-model default sits poorly with equifinality and uniqueness of place.
- BMI and FEWS-like shells already privilege orchestration over monoliths.
- Generative agents make problem-specific codes and workflows newly practical.
- Humans keep Architect, Verify, Own; AI accelerates the Execute layer.
- AEVO names the educational corollary of this professional role shift.

*(Elsevier: 3–5 bullets, ≤85 characters each including spaces.)*

---

## Abstract

Environmental modelling has long oscillated between reusable community codes and problem-specific representations that honour place, purpose, and decision stakes. Classical epistemology—equifinality, uniqueness of place, and good modelling practice—shows that “one model to rule them all” is philosophically fragile, yet practice often still defaults to configuring the same named models. Generative and agentic AI now change the production function of modelling: large language models and multi-agent systems can draft scientific code, synthesise mechanistic structures, assemble pipelines, and orchestrate research workflows at decision tempo. This position paper argues that the productive response is neither to replace the modeller with an agent nor to entrench unexamined generic application. It is to redefine practice as architecture and orchestration: humans specify purpose, assumptions, interfaces, and acceptability; agents draft and run code and data pipelines; humans invalidate, verify, and own decision stakes. Coupling infrastructure—BMI/CSDMS components, Delft-FEWS-style open shells, and digital-twin workflow publishers—already embodies this shift in software terms. Generative AI populates those shells faster while industrialising equifinality unless verification hardens. The paper proposes an Architect–Execute–Verify–Own (AEVO) practice contract, with a brief educational corollary, and a research agenda for behavioural benchmarks, assumption cards, acceptance tests, and institutional norms for AI-assisted model builds.

**Keywords:** environmental modelling; generative AI; agentic AI; model orchestration; equifinality; good modelling practice; digital twins; verification and validation; professional practice; AEVO

---

## 1. Introduction

Environmental models are no longer only research instruments. They sit inside flood forecasts, water-allocation negotiations, air-quality advisories, ecosystem-based fisheries advice, environmental impact assessments, and increasingly in “digital twin” programmes that promise continuous, place-aware situational awareness. In that sense, modelling is decision infrastructure: the quality of problem framing, assumptions, and verification travels into public and private stakes as surely as any numerical result (Jakeman et al., 2006; Voinov and Bousquet, 2010). The professional question is therefore not only “which model is best?” but “what modelling *practice* is fit for the decisions we claim to support?”

That question has become sharper as operational and policy timelines compress. Agencies and consortia increasingly expect auditable chains from data ingestion through simulation to published products, with versioned configurations and reproducible archives. Simultaneously, scientific culture continues to reward named community codes, familiar GUIs, and transferable “best practice” parameterisations. The collision of those incentives is the lived experience of many environmental modellers: pressure to move fast with a trusted generic tool, and pressure to justify structure, uncertainty, and place conditioning with a care that generic defaults rarely encode.

Two trajectories have shaped the field over the past three decades. The first is the consolidation of **generic, reusable community models**—process-rich codes that can be configured for many sites—and of **component frameworks** that couple such codes across domains and scales (Argent, 2004; Peckham et al., 2013; Werner et al., 2013). The second is a persistent philosophical and empirical critique: many structures and parameterisations can be “behavioural” against the same data (**equifinality**); places retain irreducible uniqueness; and good modelling practice (GMP) is still unevenly institutionalised (Beven, 2000, 2006; Beven and Lane, 2022; SESMO / EMS joint special issue on GMP, ~2024). The result is a familiar tension. Software culture rewards reuse and named codes; epistemology warns that unexamined reuse can be a form of scientific self-deception.

Generative and agentic artificial intelligence arrive into this unfinished project not merely as emulators or surrogate models, but as **code-and-workflow generators**. Recent systems draft analysis pipelines, recover mechanistic ecosystem equations, assemble food-web parameterisations, implement agent-based models from protocol text, and coordinate multi-agent “scientist” workflows over climate and Earth-system data (e.g. ClimateAgent; EarthLink; LEMMA; SPELL; TerraAgent; TianJi-Environ—citations in Sections 4–5). Capability claims should be read cautiously: many sources are preprints; executability does not equal behavioural fidelity; and reproducibility of AI-generated projects remains incomplete. Even with those hedges, the direction of travel is clear enough to force a field-level question: *If generating and running candidate models becomes cheap, what becomes scarce?*

**Central claim (normative).** The scarce skills are architecture, verification design, and ownership of decision stakes. Environmental modelling should therefore shift emphasis from repeatedly executing the same generic models toward **orchestrating workflows** and **generating problem-specific codes and structures**—with generative AI accelerating the Execute layer, and humans retaining Architect, Verify, and Own. Community models and coupling standards remain essential as libraries of process hypotheses and interoperable components; what should be disrupted is the culture of treating a named model as the answer without problem-specific structure, limits of acceptability, and place conditioning.

**What this paper is not.** It is not an empirical benchmark of a new agent system, not a software release note, not a curriculum paper, and not a claim that AI “solves” equifinality or validation. It is a position paper: design and normative claims are labelled as such; published vignettes are used illustratively; research agenda items are proposals, not results.

**Contribution.** Relative to existing clusters—GMP and equifinality literature; CSDMS/FEWS-style orchestration engineering; AI-scientist technical demos; and SciML verification perspectives—this paper joins classical environmental-modelling epistemology with generative/agentic practice and coupling infrastructure, and argues for an explicit Architect–Execute–Verify–Own contract as professional identity redesign rather than as classroom slogan alone. The distinctive move is not another survey of LLM capabilities, nor a restatement that equifinality exists. It is to argue that generative AI **changes the production function** of candidate environmental models, and therefore converts long-standing epistemological warnings into urgent engineering and governance problems for the EMS community.

Section 2 revisits the unfinished critique of generic modelling. Section 3 argues that software trajectories already point to orchestration. Section 4 assesses what generative and agentic AI change. Section 5 hardens the verification and ownership mandate. Section 6 sketches the professional role shift. Section 7 offers a short educational corollary (AEVO). Section 8 proposes a research and practice agenda. Section 9 closes the position.

---

## Box 1. What this paper is *not* claiming

- **Not** that an “AGI hydrologist” or autonomous Earth-system scientist is imminent or desirable as a substitute for human judgement.
- **Not** that community models (SWAT, MODFLOW, WRF, EwE-class codes, etc.) should be abandoned; they remain libraries of process hypotheses and BMI-wrappable components.
- **Not** that generative AI skips Jakeman’s first steps (purpose, data, conceptualisation) or dissolves equifinality.
- **Not** that educational branding (AEVO) is itself empirical evidence; it is a naming of a labour division already implied by orchestration and AI-scientist designs.
- **Not** fabricated case results: vignettes below summarise *published* reports and mark preprints explicitly.

---

## 2. The unfinished critique of generic modelling

### 2.1 Equifinality and uniqueness of place

Beven’s equifinality thesis remains the field’s sharpest internal critique of optimisation culture: many parameter sets—and, more deeply, many model structures—can be consistent with available observations within realistic error bounds (Beven, 2006). Coupled with **uniqueness of place**, the claim is stronger still: hydrological (and by extension environmental) landscapes are not interchangeable instances of a single transferable process machine; aggregation of small-scale laws does not erase place-conditioned behaviour (Beven, 2000, 2001). Distributed “general theory” modelling therefore faces structural as well as parametric ambiguity.

These arguments predate deep learning and generative AI, yet they gain urgency as candidate models multiply. Beven (2020) explicitly bridges uniqueness of place into the deep-learning era as a foil to fantasies of universal “models of everywhere.” If many structures already fit, then accelerating structure generation without corresponding invalidation discipline does not reduce uncertainty—it industrialises it.

A parallel move in the philosophy of evaluation replaces soft “validation” rhetoric with **invalidation** and **limits of acceptability**: models are tested for fitness to purpose against stated tolerances, not certified as true (Beven and Lane, 2022). That stance is not pessimism; it is professional hygiene. It also foreshadows the Verify mandate under AI: fluent code that runs is not yet a scientific claim that has survived attempted falsification.

It is important to state what uniqueness of place does *not* imply. It does not imply that every study must invent a private ontology, nor that transferable process understanding is worthless. It implies that transfer of a *named model configuration* is not the same as transfer of *understanding*, and that the burden of proof for transfer sits with the modeller who claims it. Generative AI can help explore alternative structures for a place; it cannot dissolve the obligation to show that a structure remains behavioural—and decision-adequate—under local constraints.

A further practical consequence follows for “models of everywhere” narratives, whether physics-based or learned. If places differ in dominant processes, data regimes, and decision questions, then a universal emulator or a universal process code is at best a prior library and at worst a seductive default. Beven’s (2020) caution about deep learning and uniqueness of place therefore generalises cleanly to generative model construction: scale of generation is not a substitute for place-conditioned evaluation.

### 2.2 Good modelling practice and the ten steps

Jakeman, Letcher and Norton’s (2006) ten iterative steps—still the spine of much EMS and iEMSs guidance—place purpose, data, conceptual structure, and evaluation before software cleverness. The ongoing GMP agenda, including joint special-issue efforts across SESMO / EMS / *Ecological Modelling* (~2024), shows that the field is still trying to *normalise* practice that textbooks have long recommended. Bridging work on the GMP–end-user gap emphasises organisational and communicative barriers, not only technical ones (Schuwirth et al., ~2021; see citation note in References).

**Implication for AI.** Generative systems can accelerate later steps (coding, calibration scaffolding, figure drafts, literature synthesis). They cannot honestly skip Step 1: purpose and problem framing remain human–stakeholder work (Jakeman et al., 2006; Voinov and Bousquet, 2010). Treating an agent’s first compilable SWAT/WRF/EwE configuration as “the model” is simply GMP failure at machine speed.

GMP also clarifies why “AI productivity” metrics mislead when applied naively to environmental modelling. Tokens generated, scripts compiled, or notebooks completed are not proxies for purpose clarity, conceptual adequacy, or decision-relevant uncertainty communication. A field that has spent years arguing for iterative learning with clients who may not initially know their needs (Jakeman et al., 2006) should recognise generative agents as powerful *participants in later loops*, not as replacements for the partnership that defines why a model exists. The GMP–practice gap is organisational as much as technical; AI can widen that gap if agencies reward speed of configuration over quality of framing and evaluation.

### 2.3 Reuse aspiration versus clone-and-own reality

Software engineering optimism has long promised reusable environmental components. Experience is more mixed. Holzworth et al. (2010) document how framework boundaries, interfaces, and intellectual-property friction can make recreation easier than adaptation. de Kok et al. (2015) show, in coastal ICZM settings, that supposedly reusable components often remain case-dependent. Argent (2004) already argued that integration is semantic and social, not only technical. Conference threads in iEMSs software practice similarly note that bespoke re-implementation can sometimes be *more transparent* than forced reuse of opaque legacy modules (see iEMSs conference literature; exact page metadata incomplete in this draft).

None of this is an argument against open science or community codes. It is an argument against conflating **named-model familiarity** with **problem-specific adequacy**. Generic models are valuable as hypothesis libraries; they become epistemically dangerous when their default application substitutes for structure choice under stated purpose and place constraints.

There is also a subtler software-sociology point. Clone-and-own behaviour often arises for rational reasons: opaque legacy modules, unclear licences, brittle build systems, missing tests, and semantic mismatches between components (Argent, 2004; Holzworth et al., 2010). In that light, AI-assisted re-implementation can sometimes *increase* transparency—if and only if the new code ships with tests, assumption records, and clear interfaces. The same AI assistance can also multiply opaque forks. The difference is governance of Verify, not the mere availability of code generation.

**Interim conclusion.** The field already knows that one-size-fits-all modelling fails on philosophical and practical grounds—yet institutional habits still often *run* the same model. That gap is the opening generative AI can either heal (by enabling tailored structures under verification) or widen (by flooding practice with unverified clones).

---

## 3. Orchestration was already the software destiny

If epistemology undermines the monolith, software history has been quietly building the alternative: **open shells and component contracts**. That history matters for the AI debate because it shows the field does not need to invent orchestration culture from scratch. It needs to recognise that generative tools should plug into an architectural settlement already underway—and to resist the regression to AI-authored monoliths that bypass coupling, provenance, and operational acceptance gates.

### 3.1 Component coupling: CSDMS and BMI

Peckham, Hutton and Norris (2013) articulated a component-based vision for Earth-surface dynamics in CSDMS. The Basic Model Interface (BMI), now at 2.0 (Hutton et al., 2020), standardises control and query functions so that models with different internal time and space discretisations can be wrapped and coupled. Practical tooling (bmi.csdms.io; pymt) treats interoperability as an engineering contract: initialise, update, exchange variables, finalise. The intellectual point for this paper is not the API detail; it is that **value migrates from owning a single codebase to designing coupled, auditable assemblies**.

Component thinking also disciplines generative AI in a useful way. An agent asked to “build a watershed model” without interface constraints may emit a brittle monolith. An agent asked to implement or wrap a component against BMI-like contracts is forced toward explicit variable exchange, units discipline, and time-stepping assumptions—artefacts that humans can inspect. **Normative design claim:** preferred targets for AI-generated environmental model code should be components and adapters that can enter existing coupling spines, not isolated notebooks that cannot be audited in operational workflows.

### 3.2 Delft-FEWS as open shell

Werner et al. (2013) describe Delft-FEWS as a flow forecasting *system* with **no inherent hydrological model**: models are plugged into a shell that manages data, workflows, and products. That architecture is an existence proof of the professional role this paper advocates. The scarce skill in operational forecasting environments has long been integration architecture—configuring which process representations, data streams, and publishing steps belong in a decision chain—not authorship of every numerical kernel. Recent cloud-native basin modelling work (e.g. FIRM for Murray–Darling contexts; Gijsbers et al., 2025) extends the same intuition: FEWS-like engines as scientific workflow and archive/traceability layers for policy-facing modelling.

The FEWS analogy also clarifies what should *not* be automated away. Shells encode institutional memory: which data quality checks are mandatory, which products are published to whom, which model versions are authorised for which warning levels. Generative agents can draft configurations and adapters for such shells; authorising a configuration for operational use remains a human Own act. In that sense, operational forecasting culture already rehearses the AEVO split—architecture of the chain, execution of runs, verification against observed events, ownership of published warnings—even when the vocabulary differs.

### 3.3 Digital twins and workflow publishers (high level)

Emerging digital-twin frameworks emphasise domain-agnostic infrastructure, plugins, and lineage (e.g. EDDIE open-source twin framing in the ISPRS Archives, 2026; Antflow workflow sharing/execution abstracts, EGU 2026). Operational programmes that combine NextGen-style hydrologic modelling with FEWS Generic BMI adapters likewise converge on **adapter + workflow** thinking. This paper deliberately keeps twin discussion high-level: twins matter here as demand signals for auditable, place-specific chains, not as a survey of twin ontologies. Twin rhetoric can also over-promise continuity and completeness; the orchestration thesis does not require believing every twin marketing claim. It requires noticing that when twins are built seriously, their scarce assets are workflow design, provenance, and acceptance criteria—exactly the Architect/Verify/Own layer.

**Point of the section.** Environmental modelling software culture already privileges orchestration over monoliths. Generative AI should be understood as a way to **populate components and adapters under human-designed workflows**, not as a replacement for the orchestrator role. The FEWS “shell with no inherent model” is the right metaphor for the AI era: agents may draft the plugs; humans still design the shell’s purpose, interfaces, and acceptance gates.

---

## 4. What generative and agentic AI change

### 4.1 From fixed-structure calibration to structure-and-pipeline generation

Classical modelling workflows often fix a structure early (choose Model X) and then spend effort on parameter estimation, scenario plumbing, and reporting. Generative systems compress—and sometimes invert—that sequence. They can propose equations, modules, scripts, and multi-step research plans before a human has committed to a community code. That is the practical meaning of “problem-specific generation”: not that every model must be written from a blank file, but that **structure choice and workflow assembly become cheap enough to revisit at decision tempo**.

This change is economic and cognitive as much as technical. When drafting a new structural hypothesis cost weeks of coding, rational modellers reused familiar structures even when conceptual doubts remained. When drafting costs hours or minutes—subject to verification—the opportunity cost of exploring alternatives falls. Equifinality then ceases to be only a philosophical warning and becomes an **engineering throughput problem**: many candidates can be produced; few can be seriously invalidated unless Verify capacity scales. That is why this paper refuses celebratory accounts of generation without parallel investment in acceptance testing and human review time.

### 4.2 Published vignettes (illustrative, not new empirics)

**Mechanistic discovery.** LEMMA (*Methods in Ecology and Evolution*) couples LLM equation synthesis with evolutionary structure search and estimation workflows, recovering NPZ- and COTS-like dynamics in reported experiments (LEMMA, 2025/26; DOI 10.1111/2041-210X.70244). The vignette supports feasibility of AI-assisted mechanistic construction; it does not license unsupervised deployment in management advice. For EMS readers, the important pattern is the *hybrid loop*: language models propose structure; classical estimation and search discipline the proposals. That pattern is closer to good modelling practice than “one-shot generate a model.”

**Ecological parameterisation.** SPELL (bioRxiv, 2025) automates functional-group and diet-matrix synthesis for EwE-class food-web models. Reported consistency and expert-agreement metrics are mixed (diet-matrix consistency on the order of roughly half to three-fifths in the preprint’s reported checks—exact figures should be re-checked against the version of record at citation time). The vignette’s value for this paper is precisely the partiality: automation helps; Verify remains non-optional. Food-web modelling also shows why problem-specific generation is not a rejection of community tools: EwE-class engines remain useful substrates; what changes is how diets and groups are proposed and checked before they enter management scenarios.

**ABMs from ODD.** LLM implementations of agent-based models from ODD protocol text show that executability is not behavioural fidelity (arXiv study, 2026; html 2602.10140). Strong models are possible; they are not guaranteed. Statistical behavioural tests remain the scarce layer. The ODD protocol itself becomes, in this light, an Architect artefact: a human-readable specification against which Execute output can be verified. Fields that lack equally explicit conceptual protocols may need to invent them before agent coding can be responsibly scaled.

**Multi-agent scientific workflows.** ClimateAgent (arXiv, 2025) explicitly decomposes ORCHESTRATE / PLAN / DATA / CODING roles—vocabulary that mirrors this paper’s thesis. EarthLink (arXiv, 2025) frames a self-evolving “copilot” so that scientists concentrate on value and result judgements. TerraAgent / TerraBench (arXiv, 2026) separates language-level planning from tool/simulator execution over heterogeneous Earth-system data. TianJi-Environ (arXiv/html, 2026) targets autonomous mechanism-testing loops around WRF-Chem-class numerical modelling. Collectively, these systems illustrate **Execute-layer automation under explicit orchestration**, not the disappearance of human judgement. Notably, several designs already encode a human-in-the-loop judgment role that this paper would classify as Own (value and result acceptance) and Verify (mechanism testing, benchmark scoring). The field’s task is to make those roles non-optional in environmental decision chains, not merely available as UI toggles in research demos.

**Macro reviews.** Domain and method reviews of LLMs in hydrology and in the scientific method more broadly situate these tools on a ladder from assistant to analyst to putative “scientist,” and call for evaluation metrics beyond task-completion scores (EarthArXiv hydrology review; *npj* / Springer Nature AI journal review, 2025—see References).

Taken together, the vignettes support a measured claim: **Execute is automating in identifiable layers**—code scaffolding, literature/data assembly, equation proposal, workflow planning—while **Architect and Verify remain the scarce skills**. They do not support a stronger claim that environmental modelling has been solved by agents. Several of the highest-profile systems remain preprints as of this draft; operational hydroecology and regulatory modelling face acceptance barriers that research demos do not. Honesty about that gap is part of the position, not a rhetorical hedge to be discarded later.

### 4.3 Limits that define the thesis

Three failure modes are already documented enough to shape a field position:

1. **Reproducibility gaps.** Studies of AI-generated scientific code report incomplete clean-environment executability and large declared-to-runtime dependency expansions (arXiv:2512.22387, 2025). “It ran on the author’s machine” is not a modelling deliverable.
2. **Methodological hallucinations.** Auditing frameworks such as ABE-Ralph (arXiv, 2026) highlight silent dataset shrinkage, oracle shortcuts, and other fidelity failures where code *runs* while the scientific claim is not what was advertised.
3. **Partial domain accuracy.** SPELL-like ecological automation and ODD→ABM behavioural gaps show that domain-specific correctness lags fluent scaffolding.

**Normative reading.** These limits do not argue against adoption; they argue against outsourcing Architect / Verify / Own. AI changes what is economically feasible (problem-specific generation at scale). It does not change who must answer for purpose, assumptions, and stakes. A field that celebrates agent task-completion scores without publishing verification designs is repeating, in a new key, the old mistake of celebrating calibration fit without structural scrutiny.

---

## 5. Uncertainty, verification, and ownership under AI-written models

### 5.1 Equifinality at industrial scale

Equifinality was manageable—if never solved—when candidate structures were scarce and human-authored. Generative modelling multiplies behavioural candidates. Without limits of acceptability, versioned assumptions, and independent verification, fluent agents can hide structural ambiguity behind confident code and polished figures. The risk narrative is straightforward: **AI without Verify industrialises equifinality and launders it as productivity**.

Industrialisation has institutional symptoms. Teams may ship more notebooks, more dashboards, and more scenario packs per month while the fraction of structures that have undergone independent invalidation falls. Reviewers may face fluent methods text that obscures silent dataset filters or oracle shortcuts (ABE-Ralph line of work). Managers may confuse “the agent finished the workflow” with “the model is fit for the warning product.” Each symptom is familiar from pre-AI modelling culture; AI mainly raises the clock speed.

A constructive response is to treat candidate multiplicity as something to be *managed*, not denied. Ensemble thinking, limits of acceptability, and multi-model comparison are classical tools. What changes is that ensembles may now include AI-proposed structures alongside community components. That only helps if humans design the comparison criteria in advance—an Architect task—and refuse to select winners by narrative fluency alone.

### 5.2 Transferable V&V lessons from SciML and hybrid Earth-system modelling

Trustworthy scientific machine learning literature offers transferable checklists: purpose definition, applicability domains, code verification, probabilistic calibration, uncertainty quantification, and documentation (SciML V&V recommendations in *Machine Learning: Science and Technology* / arXiv:2502.15496). Companion position work warns against “UQ theatre”—uncertainty displays that do not align with the decision-relevant intent (arXiv:2506.03037). Hybrid AI–physics Earth-system modelling faces additional opacity, access asymmetry, and numerical stability concerns; reproducibility guideline framings (e.g. *Nature Machine Intelligence* perspective, 2026, RHEM-style guidance) should be read as complementary institutional answers, not as competing tribes.

For environmental modelling culture specifically, these ML-facing checklists should be translated into **EMS-native artefacts**: assumption cards, limits-of-acceptability tables, BMI/FEWS workflow provenance, and peer review norms for AI-assisted builds (agenda in Section 8).

Translation matters because environmental models are often evaluated under sparse, noisy, and opportunistically observed data, with strong path dependence on conceptualisation. SciML guidance on applicability domains and documentation maps naturally onto Beven-style fitness-for-purpose thinking; guidance on probabilistic calibration maps onto the field’s long struggle with uncertainty communication; guidance against UQ theatre maps onto the temptation to decorate AI-built models with credible intervals that do not reflect structural doubt. Hybrid Earth-system reproducibility concerns—opacity, access asymmetry, numerical instability—likewise warn that AI–physics blends can create new classes of non-auditable behaviour precisely where decision stakes are highest.

### 5.3 Non-delegable ownership

Someone signs—professionally if not always legally—the forecast product, the EIA appendix, the twin dashboard, the allocation recommendation. Ownership here is stated as an **ethical and professional norm**, not as legal advice. Agents can propose uncertainty language; they cannot bear institutional trust, liability cultures, or democratic accountability. GMP’s modeller–manager partnership (Jakeman et al., 2006) and participatory modelling traditions (Voinov and Bousquet, 2010) already located the modeller as a facilitator of purpose and knowledge, not merely as a coder. Generative AI intensifies that identity: as coding cheapens, **assumption hygiene and stake communication become the centre of gravity**.

Ownership also has a documentation face. If an agent drafted the code, the human owner must still be able to explain which processes were included and excluded, which data contracts were assumed, which tests were run, and which residual risks remain. “The model was generated” is not an explanation. In regulatory and public-facing contexts, inability to narrate assumptions is already a credibility failure; AI makes that failure easier to stumble into and harder to excuse.

---

## 6. Professional identity: from model operator to system architect

### 6.1 Tasks that compress

Boilerplate coding, dependency scaffolding, first-pass literature synthesis, ensemble plumbing, figure drafts, and routine calibration loops are increasingly automatable. That compression is real and welcome where it frees attention. It is also uneven across domains and data regimes; operational hydroecology is not a coding contest leaderboard.

Compression also redistributes error modes. When humans wrote every line, certain mistakes were rare because they were tedious; agents may introduce dependency sprawl, silent API substitutions, or plausible-but-wrong process parameterisations at scale (reproducibility and fidelity studies cited in Section 4.3). The professional response is not nostalgia for manual coding; it is to treat compressed Execute work as *provisionally untrusted* until it passes Verify gates designed by humans who understand the environmental system and the decision context.

### 6.2 Tasks that intensify

Problem framing with stakeholders; choice of system boundaries and process hypotheses; interface and data contracts (including BMI-like thinking); design of acceptance tests and invalidation experiments; communication of uncertainty to decision owners; negotiation of resources for verification; and equity questions about who can afford agentic compute versus who bears environmental risk—these intensify. The modeller becomes less an operator of a familiar GUI and more a **knowledge orchestrator** and **decision partner**.

This intensification should reshape hiring, promotion, and project budgeting as much as individual skill. If institutions continue to staff projects as if the scarce resource were “someone who can drive Model X,” they will under-invest in verification design and over-invest in rapid configuration. **Normative claim:** project plans for AI-assisted environmental modelling should reserve explicit person-time for Architect and Verify stages, not only for agent subscriptions and GPU budgets. Without that reservation, Execute automation will simply move bottlenecks into silent quality failures.

### 6.3 Historical and emerging archetypes

The FEWS integrator archetype (Werner et al., 2013) already valued architecture over kernel authorship. Stakeholder modelling traditions valued facilitation of purpose (Voinov and Bousquet, 2010). Contemporary agent designs that separate orchestration/planning from tool execution (ClimateAgent; TerraAgent) rediscover the same split in AI-native form. Emerging tool-access contracts for environmental data (e.g. MCP-style interfaces—metadata incomplete; treat as emerging practice) further suggest that the modeller’s job includes designing the **contracts agents may use**, not only prompting chat interfaces.

**Careful claim.** Role change is redistribution of scarce attention, not disappearance of modelling expertise. Domain epistemology, process literacy, and decision ethics become *more* central as code generation cheapens. This is a normative professional claim, not an employment forecast. It is also not a claim that every modeller must become a software architect in the computer-science sense. It is a claim that environmental modelling competence increasingly includes the ability to design workflows, specify interfaces, and police verification—skills already latent in the best integrated-assessment and operational forecasting practice.

---

## Table 1. Illustrative task allocation before and after generative/agentic AI  
*(normative sketch, not an empirical time-use study)*

| Task cluster | Pre-generative default | Proposed AI-era allocation |
|--------------|------------------------|----------------------------|
| Purpose & decision stakes | Human | Human (Own) |
| Conceptual structure & boundaries | Human | Human Architect; AI may propose alternatives |
| Code / adapter drafting | Human-heavy | AI Execute; human review |
| Literature & data assembly | Human-heavy | AI-assisted Execute; human curation |
| Calibration / ensembles | Mixed | AI-accelerated Execute under human design |
| Limits of acceptability / invalidation | Often under-resourced | Human-led Verify; AI proposes tests |
| Uncertainty communication | Human | Human Own; AI drafts language |
| Coupling / workflow architecture | Specialist human | Human Architect over BMI/FEWS-like spine |
| Signing products / advice | Human | Human only |

---

## 7. Educational corollary: AEVO (brief)

If professional practice redistributes attention toward architecture, verification, and ownership, education should train that identity. **AEVO**—Architect–Execute–Verify–Own—is offered here as a compact naming of the labour division argued above, not as the empirical focus of this paper and not as a course syllabus.

| Phase | Field analogue | Primary responsibility |
|-------|----------------|------------------------|
| **Architect** | Purpose, boundaries, process hypotheses, interfaces, data contracts, acceptance criteria | Human modeller (+ stakeholders) |
| **Execute** | Code/scaffold generation, literature synthesis, calibration loops, ensemble runs, figure drafts | AI agents / assistants |
| **Verify** | Unit/process tests, limits of acceptability, behavioural replication, UQ, independent review | Human-led; AI may propose tests |
| **Own** | Assumptions, uncertainty communication, decision stakes, institutional trust | Humans (non-delegable) |

AEVO is best read as an educational corollary of Sections 3–6 and as one naming of a consensus already latent in orchestration shells and AI-scientist designs that keep humans as judges of value and results. Detailed pedagogy belongs elsewhere; the field claim stands without classroom evidence.

Two safeguards keep this bridge honest. First, AEVO is presented as a **naming**, not as proprietary theory: other communities may prefer “human-in-the-loop,” “orchestrator–worker,” or “analyst–scientist” ladders; the labour division matters more than the acronym. Second, teaching products associated with the author are disclosed under Competing interests; readers should evaluate the field argument on its citations and logic, not on course branding.

---

## 8. A research and practice agenda

The following items are **proposals**, not results.

1. **Behavioural fidelity benchmarks for AI-built environmental models.** Pass@k and clean-run rates are insufficient. Community benchmarks should score process constraints, conservation properties where relevant, behavioural replication against ODD-like specifications, and decision-relevant limits of acceptability—building on ODD→ABM lessons and SciML V&V checklists. Where possible, benchmarks should be stratified by decision class (exploratory research, operational forecast, regulatory assessment), because fitness-for-purpose is not a single scalar.

2. **Assumption cards co-generated with code.** Every AI-assisted build should emit a versioned, human-editable record of purpose, excluded processes, data contracts, random seeds, prompts/configs, and known failure modes. Treat prompts and tool traces as first-class provenance, analogous to FEWS workflow archives. Assumption cards should be diffable in version control so that reviewers can see what changed between candidate structures.

3. **Machine-readable acceptance tests as first-class artefacts.** Limits of acceptability should travel with the model as executable tests, not only as prose in a methods section. Agents can draft tests; humans must approve the tolerances. A minimum bar for AI-assisted EMS submissions—stated here as a **normative proposal**—would be that no generated model is published without the acceptance tests used to claim fitness for purpose.

4. **Prefer BMI/FEWS-like hooks as generation targets.** Encourage agent-generated adapters and components that plug into existing orchestration spines, rather than one-off monoliths that cannot be audited in operational shells (Peckham et al., 2013; Hutton et al., 2020; Werner et al., 2013).

5. **Institutional norms for peer review of AI-assisted model builds.** Journals, agencies, and consultancies need disclosure of AI assistance, archive requirements for configs/seeds/prompts, and review criteria that interrogate verification design—not only novelty of figures. Align with GMP normalisation efforts (Jakeman et al., 2006; SESMO/EMS GMP SI).

6. **Equity and access.** Agentic compute, proprietary model APIs, and twin programmes can widen capability gaps between institutions. A field position should ask who can generate and verify models versus who lives with environmental risk—an agenda item for ethics and science–policy venues as much as for EMS.

7. **Human–agent interaction patterns for environmental modelling.** Beyond single-prompt coding, study orchestration patterns that keep Architect/Own gates explicit (human approval of structure; mandatory Verify stages before product publication).

8. **Shared corpora of invalidated AI-built models.** Science advances by negative results as well as successes. A community archive of AI-generated structures that failed limits-of-acceptability tests would be more valuable than another leaderboard of demos that “ran.” This is a cultural as much as a technical proposal.

9. **Coupling semantics, not only coupling syntax.** Argent’s (2004) reminder that integration is semantic applies with force to agent-generated adapters: matching variable names is not matching meanings. Research should stress-test AI-produced BMI wrappers for unit errors, aggregation mismatches, and silent reinterpretation of fluxes—failure modes that are especially dangerous when code is fluent.

These agenda items are intentionally mixed: some are benchmark engineering, some are documentation standards, some are institutional norms, some are equity questions. That mixture matches the thesis. Generative AI is not only a methods novelty inside EMS; it is a stress test of the field’s willingness to fund verification and to redefine professional identity around orchestration.

---

## Figure captions (suggested artwork for submission)

**Figure 1.** Argument map: from generic-run culture, through equifinality/GMP critique and orchestration infrastructure, to generative/agentic Execute under an Architect–Verify–Own contract (AEVO as educational naming).

**Figure 2.** Stack diagram: human Architect/Own layers; agent Execute layer; shared Verify tooling; BMI / FEWS-like / twin workflow substrate.

*(Figures not drawn in this text draft; conceptual content specified for later illustration.)*

---

## 9. Closing position

Environmental modelling’s next maturity step is not a better universal model. It is a professional and technical practice of **orchestrating workflows** and **generating problem-specific models** under an Architect–Execute–Verify–Own contract. Generative and agentic AI make the Execute layer newly powerful—and newly dangerous—precisely because they multiply candidate structures at decision tempo. Coupling standards and open shells already showed where software value was migrating; AI accelerates population of those shells. Classical epistemology already showed why unexamined generics fail; AI raises the cost of ignoring that lesson.

The modeller’s future centre of gravity is not keystroke ownership of every script. It is architecture of purpose and interfaces, design of invalidation and acceptance, and ownership of assumptions and stakes. Community models remain indispensable libraries. Agents remain powerful drafters and runners. Humans remain answerable.

For *Environmental Modelling & Software* specifically, the invitation is practical. Continue publishing components, workflows, and evaluation methods—but judge AI-assisted contributions by the quality of their Architect artefacts and Verify designs as much as by novelty of generation. Reward assumption cards, acceptance tests, and coupling discipline. Treat fluent demonstrations without invalidation as incomplete. In doing so, the journal’s community can absorb generative capability without abandoning the hard-won lessons of equifinality, uniqueness of place, and good modelling practice.

That is the position this paper advances for the *Environmental Modelling & Software* community: treat generative AI as Execute-layer infrastructure inside an orchestration culture, harden Verify as GMP at machine speed, and refuse to delegate Own.

If the field succeeds, the visible change will not be that every paper boasts an agent co-author. It will be that problem-specific structures and auditable workflows become normal; that community models are used more honestly as component libraries; that acceptance tests travel with code; and that early-career modellers are trained as architects and verifiers rather than only as operators of a single named tool. That outcome is normative aspiration, not prediction—but it is an aspiration aligned with both classical environmental-modelling epistemology and the software trajectory the community has already built.

---

## Declarations

### Competing interests

The author develops and teaches educational products and may offer commercial courses related to environmental modelling practice and AI-assisted workflows (including AEVO-framed teaching). These activities constitute a potential competing interest relative to the educational corollary in Section 7. The field-level arguments in Sections 2–6 and 8–9 are presented as scholarly position claims independent of any specific course offering. No other competing financial interests are declared.

### Declaration of generative AI and AI-assisted technologies in the writing process

Generative AI tools were used to assist literature organisation, outlining, and drafting of prose for this manuscript. The author reviewed, edited, and takes full responsibility for the scientific content, normative claims, citation integrity, and final wording. No empirical results in this paper were generated by AI because the paper reports no new empirics.

### Funding

This research did not receive any specific grant from funding agencies in the public, commercial, or not-for-profit sectors.

### Data availability

No new datasets were generated or analysed for this position paper.

### Author contributions

Alex Neumann: conceptualisation; investigation (literature synthesis); writing — original draft; writing — review and editing.

---

## Acknowledgements

Colleagues in the environmental modelling and iEMSs communities whose GMP, coupling, and uncertainty work this position builds upon are gratefully acknowledged. Any errors of interpretation of cited works are the author’s alone.

---

## References

Argent, R.M., 2004. An overview of model integration for environmental applications—components, frameworks and semantics. *Environmental Modelling & Software* 19, 219–234. https://doi.org/10.1016/j.envsoft.2003.09.003 *(volume/pages confirmed against common citation; re-verify on Crossref before submission)*

Beven, K.J., 2000. Uniqueness of place and process representations in hydrological modelling. *Hydrology and Earth System Sciences* 4, 203–213. https://doi.org/10.5194/hess-4-203-2000

Beven, K.J., 2001. How far can we go in distributed hydrological modelling? *Hydrology and Earth System Sciences* 5, 1–12. https://doi.org/10.5194/hess-5-1-2001

Beven, K., 2002. Towards a coherent philosophy for environmental modelling. Related ePrint: https://eprints.lancs.ac.uk/id/eprint/459 *(full bibliographic details to be completed from the version of record / Royal Society proceedings line as applicable)*

Beven, K.J., 2006. A manifesto for the equifinality thesis. *Journal of Hydrology* 320, 18–36. https://doi.org/10.1016/j.jhydrol.2005.07.007

Beven, K., 2020. Deep learning, hydrological processes and the uniqueness of place. *Hydrological Processes* 34 (16). https://doi.org/10.1002/hyp.13805 *(complete page range to be confirmed)*

Beven, K.J., Lane, S., 2022. On (in)validating environmental models. 1. Principles of evaluation for environmental models. *Hydrological Processes*. https://doi.org/10.1002/hyp.14704 *(confirm exact title wording and year/volume on Crossref)*

de Kok, J.L., et al., 2015. Reusability of model components for environmental simulation — case studies in coastal ICZM. *Environmental Modelling & Software*. https://doi.org/10.1016/j.envsoft.2015.02.001 / ScienceDirect S1364815215000493 *(confirm full author list, volume, pages)*

Gijsbers, P., et al., 2025. FIRM: cloud-native integration for Murray–Darling basin modelling. *MODSIM2025*. https://doi.org/10.36334/modsim2025.j02.gijsbers *(confirm full author list and title wording)*

Holzworth, D.P., Huth, N.I., de Voil, P.G., 2010. Simplifying environmental model reuse. *Environmental Modelling & Software*. https://doi.org/10.1016/j.envsoft.2008.10.018 *(confirm volume/pages)*

Hutton, E.W.H., Piper, M.D., Tucker, G.E., 2020. The Basic Model Interface 2.0: A standard interface for coupling numerical models in the earth system sciences. *Journal of Open Source Software* 5 (51), 2317. https://doi.org/10.21105/joss.02317

Jakeman, A.J., Letcher, R.A., Norton, J.P., 2006. Ten iterative steps in development and evaluation of environmental models. *Environmental Modelling & Software* 21, 602–614. https://doi.org/10.1016/j.envsoft.2006.01.004

Peckham, S.D., Hutton, E.W.H., Norris, B., 2013. A component-based approach to integrated modeling in the geosciences: The design of CSDMS. *Computers & Geosciences* 53, 3–12. https://doi.org/10.1016/j.cageo.2012.04.002

Schuwirth, N., et al., ~2021. Bridging the gap between good modelling practice and end-user needs / related. *Environmental Science & Policy*. ScienceDirect S1462901120313496 *(full author list, exact title, year, volume, pages incomplete — verify before submission)*

SESMO / EMS / *Ecological Modelling* Joint Special Issue on Good Modelling Practice, introduction ~2024. https://sesmo.org/article/download/18755/18209 *(complete citation from published SI introduction)*

Voinov, A., Bousquet, F., 2010. Modelling with stakeholders. *Environmental Modelling & Software* 25, 1268–1281. https://doi.org/10.1016/j.envsoft.2010.03.007 *(pages commonly cited; confirm)*

Werner, M., Schellekens, J., Gijsbers, P., van Dijk, M., van den Akker, O., Heynert, K., 2013. The Delft-FEWS flow forecasting system. *Environmental Modelling & Software* 40, 65–77. https://doi.org/10.1016/j.envsoft.2012.07.010

### Generative / agentic AI and related (many preprints — update at revision)

ABE-Ralph fidelity auditing, 2026. Beyond Execution: Auditing experimental fidelity… arXiv html: https://arxiv.org/html/2608.26753 *(complete bibliographic metadata pending)*

AI-Generated Code Is Not Reproducible (Yet), 2025. https://doi.org/10.48550/arxiv.2512.22387

Align intent and implementation in UQ for ML, 2025. https://doi.org/10.48550/arxiv.2506.03037

Antflow, 2026. Workflow sharing/execution for digital twins. EGU abstract. https://doi.org/10.5194/egusphere-egu26-11128

ClimateAgent, 2025. Multi-agent orchestration for climate data science workflows. https://doi.org/10.48550/arxiv.2511.20109

EarthLink, 2025. Self-evolving AI agent copilot for Earth science. https://doi.org/10.48550/arxiv.2507.17311

EDDIE open-source analytical Digital Twin framework, 2026. *ISPRS Archives* L-4-W1-2026, 227. https://isprs-archives.copernicus.org/articles/L-4-W1-2026/227/2026/isprs-archives-L-4-W1-2026-227-2026.pdf

Embracing LLM technologies in hydrology. EarthArXiv / related. https://doi.org/10.31223/x58421 *(confirm final venue)*

Enhancing reproducibility in hybrid Earth system models, 2026. *Nature Machine Intelligence* Perspective (RHEM-style guideline framing). https://www.nature.com/articles/s42256-026-01299-5 *(confirm citation details on Nature site)*

LEMMA, 2025/26. Data-driven discovery of mechanistic ecosystem models with LLMs. *Methods in Ecology and Evolution*. https://doi.org/10.1111/2041-210X.70244

LLMs in the scientific method, 2025. Springer Nature AI / *npj*-family journal. https://doi.org/10.1038/s44387-025-00019-5

LLM implementation of ABMs from ODD, 2026. https://arxiv.org/html/2602.10140 *(DOI pending if assigned)*

SciML verification and validation for trustworthy scientific machine learning, 2025–26. *Machine Learning: Science and Technology*. https://doi.org/10.1088/2632-2153/ae59ec ; also https://doi.org/10.48550/arxiv.2502.15496

SPELL, 2025. AI-driven knowledge synthesis for food-web parameterisation. bioRxiv. https://doi.org/10.1101/2025.05.18.654761

TerraBench / TerraAgent, 2026. https://doi.org/10.48550/arxiv.2606.13148

TianJi-Environ, 2026. Autonomous AI scientist on WRF-Chem. https://arxiv.org/html/2606.07697 ; GitHub zwww-www/TianJi-Environ

### Software / standards (non-article)

CSDMS BMI documentation: https://bmi.csdms.io ; https://github.com/csdms/bmi ; https://github.com/csdms/pymt  
NOAA NextGen + Deltares FEWS Generic BMI Adapter documentation (wiki/docs — confirm stable URL at submission)  
iEMSs software best-practice conference materials, e.g. https://scholarsarchive.byu.edu/cgi/viewcontent.cgi?article=3899&context=iemssconference *(treat as grey literature; prefer peer-reviewed cite where overlapping)*

---

## Appendix A. Suggested cover-letter positioning sentence

*A field-level perspective that joins classical environmental-modelling epistemology (equifinality, uniqueness of place, GMP) with generative/agentic AI practice and coupling/orchestration infrastructure, arguing for an Architect–Execute–Verify–Own division of labour.*

---

*End of manuscript draft — 5 Sep 2026 (America/Toronto).*