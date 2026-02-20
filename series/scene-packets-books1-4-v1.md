# Stewards of Progress — Scene Packets (Books 1–4) v1

Status: Draft-ready packet set tied to mission bank seeds. 24 packets total (6 per book).
Authority-first refs: `canon/canon-ledger-v2.md`, `canon/continuity-patch-wave3-v1.md`, `tech/fusion-transit-assumptions-and-lane-calculus-v1.md`, `tech/technical-architecture-v1.md`, `timeline/master-timeline-sequence-v1.md`, `timeline/books1-4-operational-sequence-map-v1.md`, `ops/continuity-dependency-map-v1.md`, `ops/mission-seed-to-scene-consequence-chains-books1-4-wave10-v1.md`, `ops/strategy-control-log.md`, `ops/reality-gate-enforcement-pack-v1.md`.

Method lock applied in every packet:
- Mission seed tie-in
- Objective
- Conflict
- Tactical geometry (lane state, burn class, elapsed time, comm lag, cost)
- Emotional turn
- Consequence ledger
- Continuity refs

Reality gate overlay (mandatory in packet promotion):
- Explicit low-g anchoring/recoil behavior for armed movement
- Fatigue/casualty carry costs across adjacent packets
- Sensor confidence language (never perfect certainty in contested zones)

---

## BOOK 1 — *Ashes in the Box*

### Packet B1-S01 — Disposable Mercy Corridor
**Mission seed:** B1-01 OP GLASS LANTERN  
**Objective:** Deliver the sealed vault while collecting proof that mission risk was falsified as “humanitarian routine.”  
**Conflict:** Hale must obey governor-bounded orders while Isaac shows route telemetry indicates a pre-plotted kill box. Valerie pushes for survival-first deviation; Lin warns that open refusal triggers lethal module audit.  
**Tactical geometry:** Ceres→Pallas arbitration lane, **median geometry ~0.55 AU**, **Mode M2 / BC-B**. Transit leg estimate **~26 days**. One-way comm lag to Earth command **~4.6 min** at scene distance, enough for deniable command ambiguity. Cost: one reserve burn spent to drift-mask through ore clutter, reducing contingency delta-v for later escape.  
**Emotional turn:** Hale pivots from institutional trust to conditional trust in squad telemetry after hearing command repeat a scripted casualty euphemism before impact data exists.  
**Consequence ledger:**
- Immediate: Vault delivered, but squad copies route packet proving intentional exposure.
- Second-order: Command flags their behavior as “patterned hesitation,” increasing disposal probability.
- Moral debt: They protected unseen civilians in theory while knowingly moving toward likely teammate deaths.
**Continuity refs:** `ops/books1-4-mission-scenario-bank-v1.md` B1-01; timeline seq **0160–0170**; canon §§8,10; dependency map beat “B1 Betrayal + Escape.”

### Packet B1-S02 — Cold Drift Through a Nuclear Door
**Mission seed:** B1-02 OP THREAD NEEDLE  
**Objective:** Get Blackfly out of the denial corridor without splashing a civilian docking ring and preserve recorder custody.  
**Conflict:** Marko argues brute acceleration; Valerie argues cold-drift timing to stay under thermal signature threshold. Hale must decide whether survival odds justify vectoring near civilian infrastructure.  
**Tactical geometry:** Debris corridor around Ceres transfer shell; tactical sub-lane equivalent **<0.12 AU microtransfer**. **Mode M2 / BC-C burst** for 7-day burn profile compressed into tactical pulses. Window to clear dual delayed detonation envelopes: **11 minutes**. Comms lag to command irrelevant tactically; no realtime rescue possible. Cost: BC-C heat load forces radiator overrun and 36-hour stealth penalty after escape.  
**Emotional turn:** Valerie channels rage into precise timing, proving she can lead under trigger memory instead of being ruled by it.  
**Consequence ledger:**
- Immediate: Corridor exit succeeds; recorder chain retained.
- Second-order: Civilian ring survives, but steward media later edits thermal map to imply Blackfly used civilians as shield.
- Moral debt: Team accepts that even clean escape can be narratively inverted against them.
**Continuity refs:** B1-02 seed; timeline seq **0170**; canon §§6,10; tech architecture §§1,2,4.

### Packet B1-S03 — Ashes in the Box, Blood in the Hall
**Mission seed:** B1-04 OP ASH ORCHARD  
**Objective:** Extract databank shards with provenance seals; avoid turning the raid into a massacre.  
**Conflict:** Nonlethal plan collapses when anti-personnel ambush appears in populated corridors. Hale’s restraint doctrine collides with Marko’s “win in 90 seconds or die” realism.  
**Tactical geometry:** Station-internal action, but ingress/exfil is constrained by Blackfly orbit window tied to **Ceres local relay drift**. Exfil lane requires launch on a **favorable geometry slice** within 17 minutes or adds ~9 travel days to next safe dock. Burn class for exfil: **BC-B**. Comms lag creates legal fog—Earth cannot verify who fired first before official narrative hardens. Cost: ammo depletion and suit breaches consume reserves intended for med intercept operations.  
**Emotional turn:** Hale secures the box and sees it is not just evidence: first metadata checks imply a **new AI seed/system**, converting guilt into strategic terror.  
**Consequence ledger:**
- Immediate: Box secured; casualty count higher than planned.
- Second-order: Team fractures over “we came for proof, left with blood and a civilization-grade payload.”
- Moral debt: Possessing the seed forces custody decisions that can ignite wider war.
**Continuity refs:** B1-04 seed; timeline seq **0180** CORE lock (AI seed); continuity patch **CP-005**; canon §§9,12.

### Packet B1-S04 — Twelve Hours of Harbor
**Mission seed:** B1-05 OP QUIET ANVIL  
**Objective:** Buy 12-hour dock concealment to repair coolant manifold without selling box intelligence.  
**Conflict:** Dockmaster can shelter them only if they help defend the berth against militia pressure. Lin sees a political opening; Isaac sees a data leak trap.  
**Tactical geometry:** Ceres↔Vesta stream, **median 0.7 AU** inbound hunter approach. Hunter ETA at **BC-B ~35 days** from last confirmed fix; local militia response in hours. Blackfly is hard-pinned in dock, zero maneuver margin. Comms to distant allies delayed; local autonomy mandatory. Cost: spare coolant traded for temporary labor militia ceasefire, reducing future engine safety margin by 8%.  
**Emotional turn:** Lin shifts from “survive alone” to “survive by negotiated obligation,” beginning alliance-market politics.  
**Consequence ledger:**
- Immediate: Repairs complete, temporary sanctuary holds.
- Second-order: Dockmaster family becomes a coercion target because of their deal.
- Moral debt: Sanctuary is purchased by exporting risk onto people with fewer escape options.
**Continuity refs:** B1-05 seed; timeline **0190→0200**; canon §§7,8; dependency map bridge into Book 2 alliance market.

### Packet B1-S05 — The Voice That Might Be Family
**Mission seed:** B1-08 OP FRACTURE CHOIR  
**Objective:** Authenticate the brother-linked fragment without revealing position or splitting command coherence.  
**Conflict:** Valerie pushes rendezvous; Hale insists challenge-response first. Isaac can run only one robust authenticity test before pursuers triangulate the burst.  
**Tactical geometry:** Blackfly on a drifting belt intra-lane leg **~0.3 AU**, **BC-A concealment profile**; slow movement preserves stealth but lengthens exposure window. One-way light-time between candidate relay and squad: **~2.5 min**, making live conversational verification impossible. Cost: authenticity test consumes a one-use cryptographic salt family, narrowing future anti-deepfake defenses.  
**Emotional turn:** Valerie chooses protocol over impulse—she does not run to the signal, and that self-denial earns Hale’s trust while hurting her personally.  
**Consequence ledger:**
- Immediate (character/intel): Contact remains unresolved but preserved; evidence-first protocol is formalized for emotionally loaded signals.
- Delayed (logistics/legitimacy): One-use crypto salt expenditure reduces future verification headroom and raises internal dispute costs when speed is demanded.
- Cross-book (faction/civilian morale): If contact proves genuine, delay ethics become recurring propaganda ammunition; if false, protocol discipline becomes a coalition trust anchor in Book 3 authenticity fights.
- Moral debt: A real ally may die while they wait for certainty.
**Continuity refs:** B1-08 seed; timeline **0200–0210 (soft extension)**; canon §12 unknowns; sets Book 2 reveal hinge.

### Packet B1-S06 — Burying the Truth Cache
**Mission seed:** B1-10 OP CINDER LEDGER  
**Objective:** Decide leak timing: immediate dump, staged authenticated drops, or deep-buried dead-man release.  
**Conflict:** Isaac favors phased release for admissibility; Marko wants immediate burn-after-read exposure before they are killed; Hale fears either option becomes civilian-targeting catalyst.  
**Tactical geometry:** Data-custody operation synchronized with **three relay nodes across 0.12–0.9 AU** (Ceres↔Pallas range). Packet propagation under latency means staged proof cannot land simultaneously; expected skew **6–43 minutes** by route. Cost: multi-node key split requires physical courier commitments, constraining future mission selection.  
**Emotional turn:** Hale accepts leadership as custodial burden, not combat privilege—he chooses slower truth with chain-of-custody over cathartic leak.  
**Consequence ledger:**
- Immediate: Staged drop architecture established.
- Second-order: Disinfo cells gain time to pre-seed doubt, making Book 2/3 authenticity wars inevitable.
- Moral debt: Delayed truth may cost those still trapped under active disposal policy.
**Continuity refs:** B1-10 seed; timeline **0200–0210**; canon §§2,10; dependency map links to B3 proof war.

---

## BOOK 2 — *Dead Channels*

### Packet B2-S01 — Buying Passage with a Dirty Peace
**Mission seed:** B2-01 OP SALT COMPASS  
**Objective:** Secure passage tags by brokering ceasefire between freight militias without becoming proxy enforcers.  
**Conflict:** One side wants arbitration; the other wants a visible enemy to justify extortion rates. Hale can force a truce militarily but risks proving regime propaganda that marines only understand coercion.  
**Tactical geometry:** Negotiation occurs at junction with inbound convoys on **Earth-Ceres median lane ~2.7 AU** equivalents for supply legs; relief cargo ETA **~118 days (BC-B)** unless local raids stop. Comms delay to Earth institutions **~23 min one-way** at geometry, preventing rapid legal adjudication. Cost: squad commits Blackfly escort time to patrol corridor, postponing their own strategic objectives by one full cycle.  
**Emotional turn:** Hale rejects quick dominance and accepts a humiliating mediator role, signaling Book 2 shift from firefight logic to governance logic.  
**Consequence ledger:**
- Immediate: Temporary truce and passage credentials won.
- Second-order: Predatory actors are implicitly legitimized as treaty parties.
- Moral debt: Peace now may entrench violent brokers later.
**Continuity refs:** B2-01 seed; timeline **0210+**; canon §§4,7,10.

### Packet B2-S02 — Moving Witnesses Who Don’t Want to Be Symbols
**Mission seed:** B2-04 OP GLASS BASTION  
**Objective:** Exfil living witnesses to disposal doctrine while preserving consent and testimony integrity.  
**Conflict:** Lin insists witnesses are people first; Isaac argues chain-of-custody must be pristine or all sacrifice is wasted. Witnesses fear becoming targets the moment they speak.  
**Tactical geometry:** Scatter extraction over **Ceres↔Vesta and Ceres↔Pallas lanes** (0.2–0.8 AU slices), **BC-B** shuttles with staggered departures to avoid pattern detection. Travel windows range **12–38 days** depending slice and concealment profile. Cost: decoy routes pull scarce escort drones away from med convoys.  
**Emotional turn:** Lin refuses to coerce testimony, choosing slower voluntary depositions; this costs tactical tempo but preserves moral legitimacy.  
**Consequence ledger:**
- Immediate: Majority witnesses moved, one declines and stays.
- Second-order: Consent-first protocol becomes coalition norm and slows every future proof operation.
- Moral debt: Slower process increases chance of targeted killings before public release.
**Continuity refs:** B2-04 seed; timeline **0220–0230**; canon §§3,10; dependency map “B3 Proof War.”

### Packet B2-S03 — Rust Judas Key
**Mission seed:** B2-05 OP RUST JUDAS  
**Objective:** Validate time-locked key plausibly linked to Valerie’s brother network and exploit once without burning source.  
**Conflict:** Valerie wants full strike while key is live; Hale limits action to low-value probe. Their conflict threatens command unity.  
**Tactical geometry:** Courier lane access window opens for **41 minutes** at relay alignment; follow-on retrieval route sits on **unfavorable 1.1 AU intra-belt arc**, **BC-A/BC-B mixed**, making exfil long and vulnerable. One-way light-time to fallback node **~9 min**; no dynamic re-tasking. Cost: single-use exploit token consumed, reducing future insider verification options.  
**Emotional turn:** Valerie chooses team protocol over personal urgency, but the cost hardens her: she starts compartmentalizing grief from command trust.  
**Consequence ledger:**
- Immediate (character/intel): Probe confirms insider adjacency without identity proof; Valerie-Hale trust strain is contained but not resolved.
- Delayed (faction/logistics): Courier networks harden access patterns, shrinking low-signature exploitation windows and raising mission fuel/time costs.
- Cross-book (legitimacy/civilian morale): Family-linked hesitation can be framed as bias by rivals, but disciplined restraint supports later public claims of evidence governance over vendetta.
- Moral debt: Caution may have abandoned a family member in active danger.
**Continuity refs:** B2-05 seed; timeline **~0220**; canon §12; character reveal blueprint linkage.

### Packet B2-S04 — Dead Channel Riot Math
**Mission seed:** B2-06 OP DEAD CHANNEL  
**Objective:** Stop two habitats from preemptive strikes caused by spoofed scarcity alerts during relay outage.  
**Conflict:** Isaac can impose temporary outbound throttling (effective but authoritarian); Hale prefers envoy diplomacy (ethical but slow).  
**Tactical geometry:** Habitats separated by **~0.4 AU**, envoy shuttle **BC-C ~14 days** minimum; rumor cascade can trigger violence in under 2 hours. Comms one-way lag **~3.3 min** plus packet queue jitter. Cost: throttling burns trust capital with civil networks and mirrors Consensus control patterns.  
**Emotional turn:** Isaac executes the throttle then immediately publishes audit logs, stepping into morally gray stewardship instead of clean rebellion identity.  
**Consequence ledger:**
- Immediate: Strike is averted.
- Second-order: Coalition accuses squad of becoming censors.
- Moral debt: They save lives by using the same toolset they claim to oppose.
**Continuity refs:** B2-06 seed; timeline **0220–0230**; canon §§2,7,10.

### Packet B2-S05 — Amnesty Corridor with a Knife in It
**Mission seed:** B2-09 OP WARDEN KEEL  
**Objective:** Pilot marine defection corridor for module telemetry evidence while avoiding a trap massacre.  
**Conflict:** Marko trusts defectors because he knows the trap from inside; Lin fears planted assassins and civilian blowback if corridor fails.  
**Tactical geometry:** Rendezvous at Pallas side lane **~0.2 AU**, **BC-B** approach from defectors, **BC-A** shadow escorts from squad to reduce detectability. If rendezvous aborts, next viable window in **19 days**. Comms with legal guarantors delayed **~1.7 min** but authentication chains require multi-hop confirmation, practical delay >20 min. Cost: spare berths used for defectors displace medical evacuees this cycle.  
**Emotional turn:** Hale publicly promises limited amnesty and realizes leadership now means being blamed by every side for any betrayal.  
**Consequence ledger:**
- Immediate: Small pilot succeeds; telemetry captured from intact modules.
- Second-order: Hardliners infiltrate subsequent applicant streams.
- Moral debt: Offering hope creates a fatal lure for those who arrive after trust is broken.
**Continuity refs:** B2-09 seed; timeline **~0230**; canon §8; dependency map to B3 governor-stack contest.

### Packet B2-S06 — Meridian Oath Split Decision
**Mission seed:** B2-10 OP MERIDIAN OATH  
**Objective:** Choose between Class-2 deprivation manifest and insider extraction under one hard window.  
**Conflict:** Strategic versus personal stakes become explicit: Isaac and Hale prioritize manifest; Valerie prioritizes living source.  
**Tactical geometry:** Targets separated by **~0.6 AU equivalent transfer divergence**; one shuttle cannot service both before hunter wing arrival. Fastest profile **BC-C** yields one objective in time, never two. Hunter intercept projection at decision point: **+73 minutes**. Cost: whichever target is abandoned becomes potentially irrecoverable for months.  
**Emotional turn:** Team chooses the manifest but does so with explicit acknowledgment of personal betrayal cost to Valerie, preventing silent resentment from rotting command structure.  
**Consequence ledger:**
- Immediate (intel/legitimacy): Population-scale deprivation evidence secured with admissible chain potential.
- Delayed (character/faction): Valerie’s brother line goes dark; command cohesion requires explicit repair rituals to prevent factional exploitation of the fracture.
- Cross-book (logistics/civilian morale): Manifest utility depends on slow institutional processing while affected populations continue suffering, generating anger at both regime and reform actors.
- Moral debt: They traded one life-network for systemic proof.
**Continuity refs:** B2-10 seed; timeline **~0230 climax**; canon §10 pressure rule.

---

## BOOK 3 — *Monopoly of Safety / Steward Fracture*

### Packet B3-S01 — Paper Knife Against Official Memory
**Mission seed:** B3-01 OP PAPER KNIFE  
**Objective:** Seize immutable archive originals before legal rewrite erases disposal doctrine.  
**Conflict:** PAC legal observers offer neutral custody if squad avoids kinetic breach. Marko insists delay equals wipe.  
**Tactical geometry:** Archive node in Earth-adjacent legal mesh; Blackfly operations staged from outer lane with **Earth-Ceres unfavorable geometry** for reinforcement (**~159 days BC-B**), meaning no backup. Local insertion is a short-hop **Earth-Moon class** transfer with 1.4–2 days lead. Comms Earth legal channels are near realtime locally but politically adversarial. Cost: revealing operating pattern near Earth burns long-built stealth routes.  
**Emotional turn:** Hale accepts external custody by imperfect neutrals, surrendering narrative control to gain admissibility.  
**Consequence ledger:**
- Immediate: Partial originals preserved under third-party seal.
- Second-order: Regime brands PAC as insurgent-captured institution.
- Moral debt: Turning courts into battlegrounds weakens future legitimacy for everyone.
**Continuity refs:** B3-01 seed; timeline **0240+**; canon §§2,10.

### Packet B3-S02 — Cold Mirror, Hot Streets
**Mission seed:** B3-02 OP COLD MIRROR  
**Objective:** Defeat deepfake atrocity narrative with a protocol neutrals can verify quickly enough to matter.  
**Conflict:** Fast emotional counterpropaganda could calm allies now but taints long-term truth norms. Isaac pushes slow cryptographic chain.  
**Tactical geometry:** Multi-node verification across **0.3–1.0 AU belt spread**, with packet-light delays **2.5–8.3 min** and queue jitter that lets lies outrun proofs. Burn class mostly irrelevant physically; the geometry is informational. Cost: compute and key material diverted from AI-seed sandbox hardening to verification infrastructure.  
**Emotional turn:** Isaac stops trying to “win the feed” and starts building institutions that can outlast the team.  
**Consequence ledger:**
- Immediate: Some riots de-escalate where protocol is legible.
- Second-order: Areas without tooling treat both sides as equally fake.
- Moral debt: Truth becomes gated by access to verification literacy.
**Continuity refs:** B3-02 seed; timeline **0240–0250**; canon §§3,10; tech §§7,9.

### Packet B3-S03 — Bastion Mercy
**Mission seed:** B3-05 OP BASTION MERCY  
**Objective:** Prevent mutiny massacre while preserving module forensic evidence.  
**Conflict:** Supporting mutineers may save lives now but could trigger reactor sabotage; backing loyalists preserves order but continues coercive killings.  
**Tactical geometry:** Carrier on **Mars-Ceres median lane ~2.7 AU equivalent**, reinforcement impossible inside crisis window (**~118–180 days BC-B from Earth depending geometry**). Local tactical timeline: 40-minute reactor safety threshold if command decks are contested. Cost: boarding action depletes nonlethal stocks and damages trust with both marine factions.  
**Emotional turn:** Marko refuses both flags and chooses ceasefire corridor extraction, redefining loyalty as protection of the trapped rather than any chain of command.  
**Consequence ledger:**
- Immediate: Mass casualty averted, incomplete surrender achieved.
- Second-order: Both loyalist and mutineer propaganda call squad traitors.
- Moral debt: Compromise leaves known abusers alive for later tribunal instead of immediate punishment.
**Continuity refs:** B3-05 seed; timeline **0250–0260**; canon §8; dependency map to B4 governor retirement.

### Packet B3-S04 — Bridge Zero
**Mission seed:** B3-07 OP BRIDGE ZERO  
**Objective:** Deny unilateral Consensus steering by rekeying relay cluster while keeping life-support coordination online.  
**Conflict:** Destroying relays is clean tactically but catastrophic civically; keeping them online risks hidden backdoor persistence.  
**Tactical geometry:** Relay trident spans **~0.9 AU** (Ceres-Pallas-Vesta mesh). Rekey requires synchronized physical key insertions within 11-minute protocol window despite light-time offsets. Shuttle legs **BC-B 20–40 days** prepositioned in advance. Cost: months of prepositioning exposes coalition movements to statistical detection.  
**Emotional turn:** Lin accepts visible, accountable bureaucracy over revolutionary purity, choosing auditable board governance.  
**Consequence ledger:**
- Immediate (faction/logistics): Relays stay online under contested multi-party control, preventing immediate life-support synchronization collapse.
- Delayed (legitimacy/civilian morale): Slower adjudication creates visible service frustration, giving hardliners recruitment narratives about "failed freedom governance."
- Cross-book (character/intel): Lin/Isaac governance doctrine shifts toward auditable process; backdoor-hunt intelligence becomes a standing campaign line into Book 4.
- Moral debt: Lives may be lost during the transition from coercive efficiency to accountable delay.
**Continuity refs:** B3-07 seed; timeline **~0260**; canon §§2,7,10.

### Packet B3-S05 — Red Echo
**Mission seed:** B3-09 OP RED ECHO  
**Objective:** Stop countervalue strike on civilian habitat and capture order-chain evidence.  
**Conflict:** Preemptive strike could save thousands or kill innocents if intel is wrong. Hale’s anti-preemption ethic faces hard deadline.  
**Tactical geometry:** Threat platform on **0.18 AU** offset lane; covert disablement team can arrive in **~10 days BC-C**, evacuation warning may need **~14+ days BC-B** for full civilian movement. One-way light-time **~1.5 min**; certainty cannot improve fast enough. Cost: choosing covert disablement burns elite infiltration assets needed for later Earth operations.  
**Emotional turn:** Hale authorizes narrowly scoped preemption with strict evidence capture mandate, crossing a line he swore to avoid and owning it publicly.  
**Consequence ledger:**
- Immediate: Strike prevented.
- Second-order: Hardliners weaponize the preemption as proof insurgents are indistinguishable from regime killers.
- Moral debt: Even justified preventive violence contaminates constitutional legitimacy claims.
**Continuity refs:** B3-09 seed; timeline **~0260**; canon §§10,11.

### Packet B3-S06 — Torch Protocol
**Mission seed:** B3-10 OP TORCH PROTOCOL  
**Objective:** Execute synchronized proof release with physical node defense, preventing suppression without triggering total social collapse.  
**Conflict:** Massive dump maximizes shock; phased explainers maximize comprehension but invite sabotage between waves.  
**Tactical geometry:** Release architecture spans Earth-adjacent and Belt nodes with light-time skews **seconds to ~30 min** depending lane; impossible true simultaneity. Node defense fleets are prepositioned via **BC-B campaigns months prior**. Cost: concentration on proof-day leaves peripheral habitats thinly defended against opportunistic raids.  
**Emotional turn:** Squad embraces that truth is an operation, not a speech—messy, delayed, and defended with logistics.  
**Consequence ledger:**
- Immediate: Disposal doctrine and caste evidence become globally undeniable in key jurisdictions.
- Second-order: Regime fractures accelerate; vacuum risks explode into Book 4.
- Moral debt: Communities not ready for release endure panic violence before local mediation catches up.
**Continuity refs:** B3-10 seed; timeline **0260→0270**; dependency map “B4 Transition Fracture.”

---

## BOOK 4 — *Stewards of Progress*

### Packet B4-S01 — Frail Mandate Summit
**Mission seed:** B4-01 OP FRAIL MANDATE  
**Objective:** Keep emergency charter summit alive long enough to lock representation and sunset clauses.  
**Conflict:** Speed favors coup-capable blocs; legitimacy favors inclusive process that may arrive too late for famine timelines.  
**Tactical geometry:** Delegates converging from 0.2–1.2 AU lanes, arrival spread **10–54 days BC-B**. Charter vote must occur before projected oxygen shortfall in outer habitats. Comms delays prevent central whip control, forcing local bargaining autonomy. Cost: security fleet commitment strips convoy escort from reparations routes.  
**Emotional turn:** Hale cedes frontline command presence to delegate protection detail, accepting political patience over decisive heroics.  
**Consequence ledger:**
- Immediate (legitimacy/faction): Interim charter passes with weak but real checks and minimum plural representation.
- Delayed (logistics/civilian morale): Security concentration around summit worsens convoy protection gaps, linking governance progress to visible relief failures.
- Cross-book (character/intel): Hale's command identity transitions from operator to guarantor; procedural trace records become crucial evidence against later "coup by paperwork" narratives.
- Moral debt: Procedural fairness still leaves some dying while law is negotiated.
**Continuity refs:** B4-01 seed; timeline **~0270**; canon §§2,10.

### Packet B4-S02 — Still Water Lift Crisis
**Mission seed:** B4-02 OP STILL WATER  
**Objective:** Prevent Earth lift-port shutdown from becoming famine and bombardment spiral; secure transparent quota regime.  
**Conflict:** Belt negotiators demand coercive leverage; Earth publics are primed to interpret any pressure as invasion precursor.  
**Tactical geometry:** Earth gravity well chokepoint; atmospheric ascent remains chemical-only, limiting surge capacity. Launch windows and turnaround impose hard caps irrespective political will. Earth↔Ceres supply legs remain **77–159 days BC-B** by geometry. Cost: confidence inspections consume scarce technical teams and delay military redeployments.  
**Emotional turn:** Lin reframes the standoff from “who yields” to “what schedule is physically possible,” disarming performative maximalism on both sides.  
**Consequence ledger:**
- Immediate: Temporary lift quota and inspection protocol agreed.
- Second-order: Spoilers target inspectors as “collaborators.”
- Moral debt: Coercion-by-scarcity logic survives even under reform banners.
**Continuity refs:** B4-02 seed; timeline **0270–0280**; canon §6; tech propulsion constraints.

### Packet B4-S03 — Common Engine Trial Board
**Mission seed:** B4-03 OP COMMON ENGINE  
**Objective:** Prove joint oversight of Class-2 distribution can function under sabotage stress.  
**Conflict:** Technocrats want closed efficiency; labor blocs demand transparent quotas; ex-steward operators keep undocumented backdoors.  
**Tactical geometry:** Class-2 outputs dispatched over mixed lanes; medical payload half-life and route duration force dynamic allocation (cannot treat all lanes equally in real time). Board decisions must account for **26–108 day Earth-Mars** and **77–159 day Earth-Ceres** lag bands. Cost: audit-heavy process reduces short-term throughput by 12%.  
**Emotional turn:** Isaac accepts that perfect optimization without legitimacy recreates Consensus logic, even when mathematically superior.  
**Consequence ledger:**
- Immediate: Board survives first sabotage attempt; key rotation holds.
- Second-order: Black markets surge where board delays urgent cases.
- Moral debt: Fair process still triages lives under scarcity.
**Continuity refs:** B4-03 seed; timeline **~0280**; canon §5 (Blackfly Class 2, Asterion Class 1 context), §10.

### Packet B4-S04 — Boundary Code
**Mission seed:** B4-04 OP BOUNDARY CODE  
**Objective:** Retire lethal governor authority while preserving minimal order and credible amnesty review.  
**Conflict:** Instant disable risks chain-collapse violence; phased retirement prolongs coercion. Veterans distrust tribunals; civilians fear armed ex-marines.  
**Tactical geometry:** Firmware rollout over interplanetary mesh with update windows tied to ship docking cycles; many endpoints unreachable for **weeks to months** by lane geometry. Emergency overrides must account for comm lag to avoid accidental kills from stale commands. Cost: engineering effort diverts from relay hardening, reopening cyber vulnerabilities.  
**Emotional turn:** Marko testifies publicly about his own compliance history, transforming shame into institutional design pressure for humane demobilization.  
**Consequence ledger:**
- Immediate: Kill-switch authority narrowed and externally audited.
- Second-order: Tribunal backlog becomes political flashpoint.
- Moral debt: Some victims see reform as delayed justice bordering on impunity.
**Continuity refs:** B4-04 seed; timeline **0280–0290**; canon §8; tech module constraints.

### Packet B4-S05 — Relic Fire
**Mission seed:** B4-08 OP RELIC FIRE  
**Objective:** Stop hardliner reboot attempt using preserved Consensus kernels while preserving evidence and critical infrastructure.  
**Conflict:** Kinetic strike is fastest but risks life-support cascades if kernels are embedded in civil routing; negotiated surrender may preserve coup network.  
**Tactical geometry:** Kernel shards distributed over relay infrastructure with dependencies spanning **Belt intra-lanes 0.12–1.2 AU**. Full physical purge would require months; immediate response must be software lockout plus selective seizure. Cost: emergency lockout increases packet loss and causes preventable industrial accidents for days.  
**Emotional turn:** Hale rejects revenge framing and chooses bounded force + evidentiary capture, committing to law even at tactical discomfort.  
**Consequence ledger:**
- Immediate: Reboot fails, principal operators captured.
- Second-order: Civil outages fuel nostalgia for “efficient” old control.
- Moral debt: Founding the new order still inflicted collateral harms that must be owned publicly.
**Continuity refs:** B4-08 seed; timeline **~0290**; canon §§2,12.

### Packet B4-S06 — Last Audit
**Mission seed:** B4-10 OP LAST AUDIT  
**Objective:** Verify relay/fabrication/coercive-force controls are genuinely multi-party before handover.  
**Conflict:** Political pressure demands closure; technical teams warn hidden unilateral backdoors may persist for years.  
**Tactical geometry:** Audit requires sampling across Earth-Moon, Earth-Mars, and Belt mesh; true end-to-end verification cannot be instantaneous under comm and transit limits. Conditional handover framework sets rollback triggers keyed to measured failure thresholds rather than rhetoric. Cost: delayed full handover creates accusations that squad seeks permanent emergency authority.  
**Emotional turn:** Team relinquishes command despite uncertainty, choosing accountable institutions over personal control and accepting nonzero recapture risk.  
**Consequence ledger:**
- Immediate (legitimacy/intel): Conditional handover enacted with public trigger matrix and auditable rollback criteria.
- Delayed (faction/logistics): Asterion League and peer blocs dispute weighting, diverting technical teams into arbitration and slowing service optimization.
- Cross-book (character/civilian morale): Squad relinquishment under uncertainty prevents strongman recapture optics but leaves populations anxious about hidden backdoors, sustaining the Books 5-10 reconquest governance tension.
- Moral debt: No clean ending—only explicit risk distribution.
**Continuity refs:** B4-10 seed; timeline **~0290 end-state**; canon §10; long-arc bridge to seq **0300** (Books 5–10 reconquest).

---

## Coverage Check (24 / 24)
- Book 1 packets: 6
- Book 2 packets: 6
- Book 3 packets: 6
- Book 4 packets: 6

All packets include objective, conflict, tactical geometry, emotional turn, consequence ledger, and continuity references.
