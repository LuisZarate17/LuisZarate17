```bash
$ whoami
luis zarate · software engineer · seattle, wa

$ cat status.txt
open to full-time SWE roles · WSU CS '26 · President's Honor Roll
```

I like finding out where systems break. Race conditions, slow queries,
and the fixes that quietly make things worse before they make them better.

---

### 🔧 Start here

**[labqueue](https://github.com/LuisZarate17/labqueue)** · C# · .NET 10 · PostgreSQL 17 · k6 · Docker

A reservation API I built to break on purpose, then fix with measurements.

| | before | after |
|---|---|---|
| 50 simultaneous bookings for one slot | 50 confirmed | **1 confirmed** |
| Availability query throughput | 3,423 req/s | **7,282 req/s** (2.1×) |
| p95 latency | 21.78 ms | **9.91 ms** |

* **The bug:** a SELECT-then-INSERT race double-booked slots under concurrent load. Fixed with a PostgreSQL exclusion constraint (`btree_gist`).
* **The twist:** the fix caused deadlocks (40P01, about 1 in 20 runs), and EF Core's retry policy made it worse by turning them into a lock convoy. The writeup shows how I traced it.
* **The speedup:** a GiST index replaced a sequential scan on the overlap query, cutting query time 27×. I report the 2.1× end-to-end number because that's what a user would actually feel.

### Also built

**[MasteryPilot](https://github.com/LuisZarate17/MasteryPilot)** · Python · Django · FAISS · local LLM

Self-hosted AI tutor for school districts. Hybrid retrieval over each district's own curriculum, 492 tests, and a 4-bit open-weight model (Qwen3) running on local GPU so student data never leaves the building. I owned the Django backend on a 3-person team.

**[CougarConnect](https://github.com/LuisZarate17/CougarConnect)** · C# · Blazor Server · .NET 8 · PostgreSQL

Alumni networking platform with search, connection requests, and messaging. ASP.NET Core Identity auth with 2FA, live demo, tested with xUnit.

---

### 🧰 Stack

`C#` `Python` `TypeScript` `C/C++` `SQL`
`ASP.NET` `Blazor` `Django` `Flask` `React` `PostgreSQL`
`Docker` `GitHub Actions` `k6` `xUnit` `pytest` `FAISS` `Linux`

### 🖥️ Off the clock

* Built my own PC and run 14B local LLMs on it with an RTX 5070 Ti
* Coached middle school football in Pullman
* Hablo español

📫 [LinkedIn](https://www.linkedin.com/in/luiszarate1) · lz.zarate.1@gmail.com
