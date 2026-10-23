### Hi, I'm Luis Zarate

Software engineer in Seattle. I build backend systems and measure where they break: race conditions, slow queries, and the fixes that make things worse before they make them better.

WSU Computer Science, May 2026 · President's Honor Roll · Bilingual (English / Spanish)
**Open to full-time software engineering roles.**

---

### Start here

**[labqueue](https://github.com/LuisZarate17/labqueue)** · C# / .NET 10 · PostgreSQL 17 · k6 · Docker
A lab reservation API built to find and fix real database failures under concurrent load.
* Found a SELECT-then-INSERT race that double-booked slots under load; closed it with a PostgreSQL exclusion constraint (`btree_gist`)
* The fix introduced deadlocks (40P01, roughly 1 in 20 runs), and EF Core's retry policy turned them into a lock convoy. The writeup covers how I traced and resolved it
* Replaced a sequential scan on overlap queries with a GiST index, measured by before/after P99 latency

### Other work

**[MasteryPilot](https://github.com/LuisZarate17/MasteryPilot)** · Python · Django · C# · React · local 8B LLM
AI curriculum tutor that runs an open-weight model on local hardware instead of calling a hosted API. Three-person team; I owned the Django backend and the C# model selector.

**[AlumniNetwork](https://github.com/LuisZarate17/AlumniNetwork)** · React · TypeScript · ASP.NET · SQL Server · NUnit
Full-stack alumni directory with profile management and search, built test-first with NUnit across Agile sprints.

---

### Stack

**Languages:** C#, Python, TypeScript, C/C++, SQL
**Backend:** ASP.NET, Entity Framework, Django, Flask, PostgreSQL, SQL Server
**Frontend:** React, TypeScript
**Infra & testing:** Docker, GitHub Actions, k6, NUnit, pytest, Linux

### Contact

[LinkedIn](https://www.linkedin.com/in/luiszarate1) · lz.zarate.1@gmail.com
