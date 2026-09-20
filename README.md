# infinity-nexus
A self-contained, interactive 3D visualization of the geometric structure underlying the bidirectional-flow of cognition, self and consciousness.
Infinity Nexus: Interactive Visualization of the Bidirectional-Flow Framework
Companion file: `infinity\_nexus.html`
What this is
A self-contained, interactive 3D visualization of the geometric structure underlying the bidirectional-flow / predictive-processing architecture of cognition, self and consciousness developed in G. Wanjau, Bidirectional Flow Paper, The Self That Wasnt There and the accompanying thesis A Unified Sensing Framework.
The visualization depicts the topological structure of the framework (nested attractor layers, a shared boundary interface, and bidirectional trajectory cycles) in a form the reader can rotate, scale, and interrogate directly.
A note on terminology
The terms Soul, Ego, and Consciousness are used throughout as shorthand labels for the formal attractors A_S, A_E, and A_C in the framework's dynamical system. They are chosen for accessibility, not to import folk-psychological, religious, or psychoanalytic commitments. Readers familiar with any of those traditions should treat the labels as placeholders whose meaning is fixed by the paper's definitions (Def 3.2 and §10.5 to 10.8), not by prior associations with the words. Any structural claim made in this document about Soul, Ego, or Consciousness is a claim about the corresponding formal attractor, not about the referent those words carry elsewhere.
How to open
Open `infinity\_nexus.html` in any modern desktop or mobile browser. No server, install, or account is required; the file is fully self-contained (WebGL rendered client-side via Three.js loaded from public CDNs).
Interaction:
drag to orbit the scene
scroll or pinch to zoom
right-drag to pan (desktop)
the scene auto-rotates at a slow rate; drag anywhere to override
The animation runs continuously; there are no controls to pause it, by design (the point of the animation is that the model's invariants persist across the Body's varying placement).
How to view
This visualization rewards sustained attention. The animation is designed to run continuously and to be watched for at least a minute or two rather than glanced at. Its structure catalogues to non-verbal recognition over time; a brief look will register the geometry but not what the geometry does. Give it the same kind of attention you would give a piece of ambient music or a slow-moving natural scene, and it will unfold at the rate it is designed to unfold.
What the visualization depicts
Environment sphere (large, translucent blue). The field within which the organism is embedded. Extends beyond the visible frame to signal that it is not a bounded object but a portion of a field.
Body sphere (muted red, animated). The organism's Markov-blanketed system. The Body is rendered in two poses simultaneously, crossfading on a ~9 s cycle: internally tangent to the Environment (inside pose) and externally tangent (outside pose). The two configurations correspond to different metaphysical framings (embedded monism vs. structural interactionism / point-contact dualism); the crossfade encodes the framework's metaphysical neutrality (§15 of the paper). The Body's placement is a free variable; the Nexus and the phantom architecture are invariant.
Nexus (bright white core with a soft outer halo). The core marks the Body–Environment interface, compressed to a point for visual legibility. The surrounding halo is the Consciousness field radiating from that interface: consciousness suffuses the coupling point itself and is not confined to the outer torus. Formally the core corresponds to the Markov blanket variable Ξ separating internal from external states; the halo depicts A_C's basin extending down to and through Ξ.
Three tori anchored at the Nexus:
Soul (green, thin). Attractor A_S, the self-model as fixed point of the boundary dynamics.
Ego (gold, thin). Attractor A_E, touching Soul on a shared tangent circle.
Consciousness (pale violet, translucent, fatter). Attractor A_C, the meta-phantom, encapsulating Soul and Ego within its basin. Rendered as a subtle field presence rather than a bright surface: the attractor's basin is the substrate through which the trajectories move, and is meant to recede visually so the flow through it is what registers.
Soul and Ego pulse in opacity out of phase with each other, synchronized with the small-loop cycle: as the trajectory alternately visits each attractor's basin, the corresponding phantom's salience fluctuates.
Two figure-8 trajectories (integral curves of the vector field on state space):
Small loop (bright white, faster pulse). Trajectory whose closure passes through the Soul–Ego basin boundary at the tangent circle where the two lower attractors meet.
Large loop (bright white, slower pulse). Trajectory whose closure passes through the Nexus and reaches the geometric center of the Body in the "inside" pose (a distance of one Body radius from the Nexus, along the interface axis).
Bidirectionality. Along each loop, half the arrows travel in one direction and half in the other. This is intentional. The flow at each scale is bidirectional: the same source sustains both an ingoing and an outgoing trajectory simultaneously along the same integral curve. Input and output are two aspects of one motion, not two separate flows. There is no privileged forward direction.
Both loops render in bright white to signal that they belong to a single flow category (the vector field V) at two nested scales. Their opacities alternate out of phase, depicting the different characteristic timescales of the two nested cycles.
Formal correspondence
The visualization is a projection of the framework's dynamics onto a low-dimensional slice. It carries topological information faithfully; parameters and clinical variables are legitimately absent from a phase-portrait rendering.
Vector field on state space:
    V(Ψ) ≡ dΨ/dt

Loops in the visualization are integral curves of V. The word "flow" in the paper corresponds to this vector field, not to a diffuse process.
Layer dynamics (§11.2, active-inference message-passing):
    τ_i · dΨ_i/dt = γ_i · [ π↓_{i+1→i}(Ψ_{i+1}) − π↑_{i→i+1}(Ψ_i) ] + ξ_i(t)

with top-down predictions fixed by expected-free-energy minimization:
    π↓_{i+1→i} = argmin_π E_q[ φ_EFE(π, Ψ_{i+1}) ]

Ψ_i(t): state at layer i (Environment, Body, Soul, Ego, Consciousness)
π↑, π↓: upward and downward messages
γ_i: meta-precision at layer i (sets update rate; corresponds to different loop pulse rates)
τ_i: characteristic timescale at layer i
ξ_i(t): stochastic drive
φ_EFE: expected free energy functional
Attractors (fixed points of V):
    A_i = { Ψ_i : V(Ψ_i) = 0 }

The tori in the visualization mark these sets. They are static because attractors are, by definition, invariant under V.
Basins:
    𝓑(A) = { Ψ_0 : lim_{t→∞} Ψ(t | Ψ_0) = A }

Basin depth (§10.5b, Claim 10.5b):
    d(A_C) = inf_{Ψ ∈ ∂𝓑(A_C)} ‖Ψ − A_C‖

Basin nesting (Consciousness encapsulating Soul + Ego):
    𝓑(A_C) ⊇ 𝓑(A_S) ∪ 𝓑(A_E)

Nexus (Markov blanket variable Ξ):
    Ξ ⊥⊥ Ψ_int | Ψ_ext   and   Ξ ⊥⊥ Ψ_ext | Ψ_int

Ξ is high-dimensional in principle; the visualization projects it to a point. This is the only significant lossy compression in the mapping.
Mapping summary
Visual element	Formal object
Environment sphere (blue)	External state region
Body sphere (muted red, either pose)	Internal state region (Markov-blanketed system)
Nexus core (bright white point)	Markov blanket variable Ξ; saddle of V in the projected slice
Nexus halo (soft pale violet)	Consciousness field A_C radiating through the Ξ coupling
Consciousness torus (pale violet)	Attractor A_C and its basin 𝓑(A_C)
Soul torus (green)	Attractor A_S (Ψ(t)'s highest-weight constituent for A_C)
Ego torus (gold)	Attractor A_E, coupled to A_S at their shared basin boundary
Small figure-8, bright white	Trajectory γ_S(t) at characteristic timescale τ_S
Large figure-8, bright white	Trajectory γ_C(t) at characteristic timescale τ_C > τ_S
Alternating pulse (loops)	Different γ_i / τ_i at the two nested scales
Soul/Ego opacity fluctuation	Trajectory alternately visiting each basin; visited-attractor salience
Body crossfade (inside ↔ outside)	Metaphysical neutrality (§15): substance placement is unfixed
Notes and caveats
The visualization is schematic, not a numerical simulation. It does not display specific parameter values (α, γ_i, I_S) or run the equations. It communicates the topological structure the equations describe.
The 3D projection is lossy. The actual state space Ψ is high-dimensional; only qualitative geometric relations (nesting, tangency, shared crossing) are preserved.
Specific geometric quantities in the render (Nexus at (0, 0, −14), Consciousness radius 5, Soul–Ego tangent circle at r = 5) are visual composition, not empirical claims.
The Body's crossfading between poses is a claim about the framework's metaphysical neutrality, not a claim about physical dynamics. The Body does not literally teleport; the animation depicts the interpretive underdetermination of the substance-level question.
Version
This deposit corresponds to visualization version 16 (color-corrected),The Self That Wasn't There and Unified Sensing Framework.
Citation
Wanjau, G. (2026). Infinity Nexus:
The Self That Wasn't There:
A meditation on the phantom that runs from ego to cosmos 10.5281/zenodo.22804071
License
 CC BY 4.0
Dependencies
The HTML file loads two libraries from public CDNs at runtime:
Three.js r128 (cdnjs.cloudflare.com)
OrbitControls (cdn.jsdelivr.net)
No other assets or connections are required. The file will function offline if these libraries have been previously cached by the browser; for guaranteed offline use, inline the two scripts into the HTML.
