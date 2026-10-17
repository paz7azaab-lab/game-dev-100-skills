# Game Development: 100 Skill Areas

These are workflow categories, not claims that 100 separate plugins or agents are installed. Pick the areas relevant to a task and record evidence in the execution log. Status values: `planned`, `in progress`, `passed`, `failed`, `blocked`.

## Product, goals, and design
1. Product Vision & Audience — define the intended players and the core promise.
2. Requirements & Acceptance Criteria — make desired behavior observable and testable.
3. Scope & Prioritization — rank work by player value, risk, and effort.
4. Game Design Fundamentals — align mechanics, feedback, goals, and constraints.
5. Core Gameplay Loop — specify the repeatable player action/reward loop.
6. Systems & Emergent Design — check how mechanics interact.
7. Progression & Difficulty — tune learning, challenge, pacing, and mastery.
8. Economy & Resource Balancing — model sources, sinks, scarcity, and inflation.
9. Reward Design — make rewards understandable, fair, and motivating.
10. Monetization & Ethical Pricing — keep offers transparent and avoid deceptive pressure.

## World, levels, narrative, and content
11. Worldbuilding & Lore — maintain consistent world rules and tone.
12. Narrative & Quest Design — make objectives readable and outcomes meaningful.
13. Level Design — shape routes, landmarks, pacing, and player decisions.
14. Open-World Structure — manage navigation, discovery, and content density.
15. Mission & Objective Design — ensure objectives are clear and verifiable.
16. Tutorial & Onboarding — teach through concise, timely feedback.
17. Player Guidance & Wayfinding — communicate where to go without needless friction.
18. Content Variety & Coherence — reduce repetition while preserving identity.
19. Procedural Content — validate generated content for quality and edge cases.
20. Localization & Culturalization — support language, layout, and cultural context.

## Art direction and presentation
21. Art Direction — establish a coherent visual identity.
22. Visual Readability — distinguish units, threats, resources, and actions at a glance.
23. UI/UX Design — make common actions understandable and efficient.
24. Iconography & Typography — keep symbols and text legible on target screens.
25. Color & Contrast — maintain hierarchy and accessible contrast.
26. 2D Art Pipeline — manage sprite consistency, atlases, and export settings.
27. 3D Modeling & Materials — maintain scale, silhouette, and material readability.
28. Animation & Timing — communicate state and impact with clear motion.
29. VFX & Combat Feedback — make events readable without obscuring gameplay.
30. Audio & Sound Design — use audio to communicate state and reinforce identity.

## Graphics and rendering
31. 3D Graphics & Rendering — choose suitable rendering techniques for target hardware.
32. Lighting & Composition — guide attention and support visual clarity.
33. Camera Design — keep action and context visible across device sizes.
34. Shader & Material Optimization — measure cost and visual benefit.
35. Asset Import & Compression — use appropriate formats and sizes.
36. LOD & Culling — avoid rendering unnecessary detail.
37. Particle Budgeting — cap overdraw and effect counts on mobile.
38. Resolution & Aspect-Ratio Handling — support the intended device range.
39. Loading & Streaming — manage assets without disruptive stalls.
40. Visual Regression Review — compare screenshots for unintended changes.

## Engineering foundations
41. Language & Runtime Fundamentals — follow the project’s actual language/runtime.
42. Code Organization — keep modules focused and dependencies clear.
43. Software Architecture — define boundaries and data ownership.
44. Data Modeling & Serialization — validate saved and networked data.
45. State Management — keep UI, gameplay, and persistence state consistent.
46. Input Handling — support touch, keyboard, controller, or other target inputs.
47. UI Implementation — wire controls to real actions and meaningful states.
48. Save/Load & Migration — preserve player progress across versions.
49. Error Handling & Logging — make failures diagnosable without leaking secrets.
50. Dependency & Build Management — make builds repeatable and dependencies explicit.

## Gameplay systems and simulation
51. Character & Unit Controllers — make movement and actions predictable.
52. Physics & Collision — verify boundaries, layers, and edge cases.
53. AI Behavior — test decision rules and recovery from unexpected states.
54. Pathfinding & Navigation — check reachability, costs, and blocked routes.
55. Combat Systems — validate damage, range, cooldowns, and feedback.
56. Abilities & Status Effects — define stacking, duration, and interaction rules.
57. Inventory & Equipment — prevent invalid items and inconsistent ownership.
58. Building & Crafting Systems — validate placement, costs, upgrades, and limits.
59. Economy Simulation — test resource flow over time and at extremes.
60. Time-Based Actions — handle timers, offline progress, and clock changes safely.

## Online and platform systems
61. Multiplayer Architecture — define authoritative state and failure behavior.
62. Networking & Synchronization — test latency, packet loss, and reconnection.
63. Server Authority — validate valuable state on trusted servers when applicable.
64. Matchmaking & Lobbies — handle empty queues, disconnects, and party rules.
65. Social Systems — design friends, alliances, chat, and permissions safely.
66. Anti-Cheat & Exploit Resistance — identify trust boundaries and abuse cases.
67. Account & Session Security — protect authentication and session lifecycle.
68. Cross-Platform Compatibility — validate platform-specific behavior and limits.
69. Mobile Lifecycle — handle pause, resume, interruptions, and low memory.
70. Offline & Poor-Network Behavior — fail gracefully and avoid losing progress.

## Performance and reliability
71. Performance Profiling — measure before optimizing.
72. CPU Optimization — identify hot paths and unnecessary work.
73. GPU & Overdraw Optimization — inspect rendering cost on target devices.
74. Memory & Leak Management — monitor allocations, asset lifetime, and leaks.
75. Battery & Thermal Awareness — avoid sustained unnecessary device load.
76. Startup & Loading Performance — measure launch and scene transition time.
77. Network Efficiency — limit payloads, requests, and synchronization churn.
78. Reliability & Crash Triage — classify failures and reproduce them.
79. Compatibility Matrix — test declared OS/device/runtime targets.
80. Accessibility & Reduced Motion — provide readable controls and suitable motion options.

## Testing and quality assurance
81. Unit Testing — test isolated rules and calculations.
82. Integration Testing — test connected systems and data flow.
83. Automated Testing — make repeatable checks executable where feasible.
84. Gameplay Testing — verify the player experience against acceptance criteria.
85. Regression Testing — ensure fixes do not break existing behavior.
86. Software Architecture Review — check boundaries, coupling, and maintainability.
87. Evidence-Based Debugging — reproduce, form a hypothesis, and verify the cause.
88. Code Review & Refactoring — improve clarity without changing behavior unintentionally.
89. Acceptance Testing — check each agreed criterion explicitly.
90. End-to-End Validation — test complete player flows on the target platform.

## Release, security, privacy, and business
91. Requirements Traceability — map each requirement to implementation and evidence.
92. Completion Audit — separate completed, partial, and unverified work.
93. Design-to-Code Verification — compare implementation to approved designs.
94. Release & Versioning — document versions, migrations, and rollback plans.
95. Build & Packaging Validation — inspect output artifact and platform configuration.
96. Store & Compliance Readiness — review store requirements and third-party licenses.
97. Analytics & Observability — collect only useful, privacy-conscious diagnostics.
98. Revenue Forge — assess pricing, productization, and realistic market paths; never guarantee income.
99. Security & Anti-Cheat Review — review exploits, purchase validation, abuse, and recovery paths.
100. User Privacy & Safety — minimize data, secure it, and provide age-appropriate reporting/blocking and abuse controls.

## How to record use
Use IDs (for example `22`, `46`, `69`, `85`) in each task record. The index itself does not mark any area as passed.
