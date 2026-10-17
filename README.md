# Kevin Blake Lopez

I work on the IT Audit Machine. People collect evidence against controls, examiners assess it, and the application holds the findings, files, and reports for one entity and one audit year. The code is CodeIgniter 4, Vue, and TypeScript, on MySQL. Tests run with Pest, Codeception, Vitest, and Playwright.

The bugs I spend time on are the ones where the framework's account and the database disagree. `updateBatch` drops a `where()` that was only chained on the builder, so a batch can write outside the scope the caller set. `getPost()` never sees the JSON body the browser sent. A queue worker that fails with a transaction still open can leave that transaction for the next job. The database is shared, so I count statements instead of trusting local wall time, and a test has to put a real request or a real query on one side of that boundary.

The public project is the [PostgreSQL Persistence Conformance Suite](https://github.com/KevinBlakeLopez/PostgreSQL-Persistence-Conformance-Suite). It drives Lucid, MikroORM, and TypeORM through their own APIs, injects controlled failures, and asks PostgreSQL whether the framework's report of the transaction matches what the server did.

## Contact

[kevinblakelopez@gmail.com](mailto:kevinblakelopez@gmail.com)
