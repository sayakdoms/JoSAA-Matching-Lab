# Matching model and implementation notes

## Candidate-proposing Deferred Acceptance

Programs have capacities `q[p]`, candidates submit ordered preferences, and each program ranks applicants by the applicable merit list.

1. Every currently rejected/unmatched candidate applies to their highest remaining acceptable program.
2. Each program tentatively retains the `q[p]` highest-priority candidates among incumbents and new applicants.
3. Rejected candidates continue to the next program.
4. When no more proposals occur, tentative holds become final.

Under standard responsive-priority assumptions, the matching is stable and candidate-optimal among stable matchings. Truthful preference reporting is a dominant strategy under the standard candidate-proposing model. Complicated reservation and intertemporal rules require additional care.

## Demonstration data

| Candidate | JEE Advanced rank | JEE Main rank | First choice |
|---|---:|---:|---|
| Asha | 2 | 1 | IIT EE |
| Ravi | 1 | 3 | NIT CSE |
| Meera | 3 | 2 | IIT EE |

Both programs have one seat. The interactive trace reproduces four successive proposal/rejection rounds and yields Ravi at IIT EE and Asha at NIT CSE.

## Three innovations in the case

**Defense Services quota (2015):** A small institute-wide nonnested quota complicates stability. The authors used temporary phantom DS allocations followed by rejection chains, with a supernumerary fallback in rare pathological cases. DS allocations were made supernumerary from 2016.

**OBC dereservation:** Convert unfilled OBC capacities to open-category capacities and rerun the existing algorithm until convergence. OBC assignments weakly decrease between runs; final stability need not imply candidate optimality. Approximately four iterations were sufficient in practice. The website's slider demonstrates one input-capacity change only.

**Female reservation (2018):** Female-reserved program capacity is attempted first, followed by gender-neutral seats. This preserves female eligibility for merit-based seats and keeps reserved-category admissions closer to the target. Female candidates using gender-neutral seats: IITs 10 vs 66 (reverse-order counterfactual); NITs 467 vs 847.

## Limitations

This website does not implement all virtual programs, nesting, DS rejection-chain recursion, iterative reruns of full DA, tie-handling, institute state quotas, or official eligibility/priority tables. Its impact data are historical, not current admission statistics.
