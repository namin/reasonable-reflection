# reasonable-reflection
A Rational Defense of Reasonable Reflection (LICS'26 Keynote)

## Artifacts

- [llm-meta-level](https://github.com/namin/llm-meta-level): the meta-level *is* an LLM proposing modifications to level 0; the 0↔1 boundary is checked by a verifier (sandbox / `tsc` / `dafny verify` across three instantiations), placing the LLM behind a kernel-style gate
- [lean-grey](https://github.com/namin/lean-grey): abstract reflective tower in Lean 4 with `execute-at-metalevel` and reflectively-modifiable governance policies; modifications restricted to guard+handler (no closures/heap)
- [lean-green](https://github.com/namin/lean-green): meta level realized as a mutable heap cell with closures and causal `set!`, plus the CakeML-style value-bisimulation infrastructure for conservative extension (CE) soundness theorem and an LLM proposer/gate cascade
- [**lean-sage**](https://github.com/namin/lean-sage): the synthesis — lean-grey's multi-level reflective tower over lean-green's heap/closure/`set!` substrate, with a kernel-checked proof-bearing admission gate on top: each `base-apply` modification carries its own CE proof, and admissions compose across the tower
- [lean-emerald](https://github.com/namin/lean-emerald): pedagogical rebuild of lean-sage's proof-bearing CE substrate, 5x smaller
- [climbing-calc](https://github.com/namin/climbing-calc): type-level proof-bearing admission for a total-functions calculator — Lean's type checker *is* the schema/operator gate
- [climber](https://github.com/namin/climber): gate governs the right to extend the proof system itself (sound axiom-schema extensions, Beklemishev-shaped)
- [defeater](https://github.com/namin/defeater): non-monotonic dual of climber — gate admits sound exception schemas, governing what gets withdrawn rather than added
- [reviser](https://github.com/namin/reviser): gate checks rationality of belief-revision operators, not the beliefs themselves
- [sc-mini/llm](https://github.com/namin/sc-mini): minimal positive supercompiler, forked with sound LLM-proposed rewrites
- verified discovery system: gate over discovery of theorems and heuristics
