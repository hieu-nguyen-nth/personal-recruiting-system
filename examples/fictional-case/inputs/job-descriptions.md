# Job and discovery fixtures — entirely fictional

These are authored full postings for an offline demonstration, not current vacancies. Reserved URLs do not resolve. The candidate's enrollment equivalence, location and authorization must not be guessed.

## JD A — JD-A-v1

- Company: Kestrel Exhibit Systems (fictional).
- Requisition: EX-KES-41.
- Title: Product Discovery Intern — Collections Intake.
- Canonical fixture URL: https://example.invalid/kestrel/jobs/EX-KES-41
- Term: July–September 2029, twelve weeks; location to be confirmed.
- Product: Intake workflow software for small museums and exhibition operators.
- Assignment: Observe staff intake work, synthesize recurring exceptions, test low-fidelity workflow concepts with a designer and present a prioritized discovery brief to a product mentor.
- Responsibilities: Plan observation sessions with guidance; distinguish observed facts from assumptions; document user problems; work with design and operations; explain what a small pilot can and cannot establish.
- Required: Active enrollment in a qualifying graduate product/service program; evidence of user observation and synthesis; clear written communication; availability for the term.
- Preferred: Experience with cultural collections or equipment handling; spreadsheet analysis; comfort with low-fidelity prototypes.
- Not stated: Whether a certificate qualifies; authorization/sponsorship policy; exact interview rubric; conversion prospects; scope of final product decision ownership.
- Posting fixture date: 2029-02-01.

## JD B — JD-B-v1

- Company: The same Kestrel Exhibit Systems.
- Requisition: EX-KES-42.
- Title: Data Platform Intern — Collection Imports.
- Canonical fixture URL: https://example.invalid/kestrel/jobs/EX-KES-42
- Term: July–September 2029, twelve weeks; location to be confirmed.
- Assignment: Extend a production collection-import pipeline, add tests and failure monitoring, and review implementation with a platform engineer.
- Responsibilities: Write Python import code and SQL transformations, debug failed imports and document data contracts.
- Required: Prior production Python data-pipeline experience, practical SQL and availability for the term. Coursework alone does not meet the stated pipeline requirement.
- Preferred: Collection metadata standards and operations experience.
- Not stated: Authorization policy or flexibility on mandatory technical experience.
- Posting fixture date: 2029-02-01.

## Discovery response fixture

Query key `fixture-collections-intern-2029`, ordered as below, returns three raw results. Teaching batch limit: two raw results per simulated run. This is not a real provider payload.

| Offset | Provider fixture ID | Employer/requisition | URL | Identity |
|---|---|---|---|---|
| 0 | FIX-J01 | Kestrel / EX-KES-41 | https://example.invalid/kestrel/jobs/EX-KES-41 | JD A, canonical |
| 1 | FIX-M01 | Kestrel / EX-KES-41 | https://example.invalid/mirror/collections-intake | Same opening; mirror explicitly supplies requisition EX-KES-41 |
| 2 | FIX-J02 | Kestrel / EX-KES-42 | https://example.invalid/kestrel/jobs/EX-KES-42 | JD B, distinct opening |

Run 1 processes offsets 0–1 and saves next offset 2. Run 2 resumes offset 2 with the same query key and exhausts the fixture. A different title or URL does not override the explicit shared employer/requisition of the mirror.
