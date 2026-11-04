# JoSAA Matching Mechanism Lab

**One List. One Seat. Better Matching.**

An interactive educational companion to a case presentation on *Centralized Admissions for Engineering Colleges in India* (Baswana et al., 2019), prepared by **Sayak Pranab Ghosh**, MBA, IIT Roorkee.

**Live application:** https://josaa-matching-lab.vercel.app/

## What is included?

- **Live Matching:** a working, four-round candidate-proposing Deferred Acceptance demonstration with three students and two programs using distinct JEE merit lists.
- **Quota Innovation Lab:** research-grounded explanations of institute-wide Defense Services quotas, phantom allocations, rejection chains, iterative OBC dereservation, and female-first reservation precedence.
- **Research Impact:** like-for-like historical IIT vacancy results and the authors' 2017 counterfactual findings.

The DA teaching example is computational and interactive. The DS quota and gender sections **illustrate** the publication's methods and data; they do not claim to recreate the production JoSAA engine. The dereservation slider illustrates capacity arithmetic, not a full recalculation of stable matchings.

## Getting started

This is a standalone static web application requiring no build tools or backend.

1. Clone or download this repository.
2. Open `index.html` in a modern browser.
3. Use the three tabs and step through the algorithm.

The project can be hosted on GitHub Pages, Vercel, or any static web server.

## Repository structure

```text
JoSAA-Matching-Lab/
├── index.html
├── README.md
├── LICENSE
└── docs/
    ├── algorithm.md
    └── research-notes.md
```

## Verification scenarios

For the demonstration's three candidates, preferences, and priorities, the terminal assignment is **Ravi → IIT EE**, **Asha → NIT CSE**, and **Meera unmatched**. Vacancy counts are **587, 286, 159, and 163** for 2014–2017 on the paper's like-for-like IIT sample.

## Research citation

Baswana, S., Chakrabarti, P. P., Chandran, S., Kanoria, Y., & Patange, U. (2019). Centralized Admissions for Engineering Colleges in India. *INFORMS Journal of Applied Analytics*, 49(5), 338–354. https://ssrn.com/abstract=3298917

## Disclaimer

Independent educational case companion. Not affiliated with JoSAA, IIT Roorkee, or the IIT admissions authorities. No live applicant data, operational admissions service, or current JoSAA data are used.
