---
layout: two-cols
---

# Solution 1

Complete migration from<br/>
AWS DynamoDB ➡️ Aurora RDS

|             |                                             |
|-------------|---------------------------------------------|
| Reporting   | ✅                                           |
| BI          | ✅                                           |
| Insights    | ✅                                           |
| Urgency     | ⚠️ Time consuming                           |
| Dev Ex      | ✅                                           |
| Scalable    | ❌ `Tasks` table is very I/O heavy and large |
| Maintenance | ✅                                           |
| No refactor | ❌ Large impact on codebase, downtime        |

⚠️ Performance unknown ❓

::right::

<img border="rounded" src="../assets/sol_1.png" width="70%" />

<style>
.slidev-layout td {
  padding: 0.1rem;
}

h1 {
  background-color: #6dd8aa;
  background-image: linear-gradient(45deg, #45CD93 10%, #6dd8aa80 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
layout: two-cols
---

# Solution 2

Half-n-half
* Keep I/O heavy data in DDB `Tasks`
* Move all other data to RDS
* Small infrastructure footprint
* ⚠️ Any time `tasks` data is required would be a DDB Query

|             |                                      |
|-------------|--------------------------------------|
| Reporting   | ✅                                    |
| BI          | ✅                                    |
| Insights    | ✅                                    |
| Urgency     | ⚠️ Time consuming                    |
| Dev Ex      | ✅                                    |
| Scalable    | ❓Unsure / Unknown                    |
| Maintenance | ✅                                    |
| No refactor | ❌ Large impact on codebase, downtime |

::right::

<img border="rounded" src="../assets/sol_2.png" width="70%" />

<style>
.slidev-layout td {
  padding: 0.1rem;
}

h1 {
  background-color: #6dd8aa;
  background-image: linear-gradient(45deg, #45CD93 10%, #6dd8aa80 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
layout: two-cols
---

# Solution 3

Replicate

* Stream DDB changes to Aurora RDS
* Aurora RDS becomes a read-only data store
* Minor impact on codebase
* ⚠️ Larger infra footprint, more things that can break

|             |                                            |
|-------------|--------------------------------------------|
| Reporting   | ✅                                          |
| BI          | ✅                                          |
| Insights    | ✅                                          |
| Urgency     | ✅                                          |
| Dev Ex      | ✅                                          |
| Scalable    | ✅                                          |
| Maintenance | ✅                                          |
| No refactor | ✅                                          |

::right::

<img border="rounded" src="../assets/sol_3.png" width="90%" />

<style>
.slidev-layout td {
  padding: 0.1rem;
}

h1 {
  background-color: #6dd8aa;
  background-image: linear-gradient(45deg, #45CD93 10%, #6dd8aa80 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
layout: fact
---

## We ended up going with Solution 3