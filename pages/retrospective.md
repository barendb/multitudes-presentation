---
transition: fade-out
layout: fact
---

<div><h1>Did it work?</h1></div>
<div v-click><h1>Yes... 😎</h1></div>


---
transition: fade-out
---

# Retrospective

What went well

- Was able to turn solution around fairly quickly
- Side by side development without impact on other feature development
- sub 100ms sync time DDB ➡️ RDS
- \#justworked 🙏


---
transition: fade-out
---

# Retrospective - 2

What didn't go well

- Cutting teeth on code generation
  - Thought this would be easy but took time to find good solution
- RDS had performance issues
  - RDS DB needed to add additional indexes
  - Needed to add a caching layer for queries, we didn't anticipate that we would need this initially
  - Autoscaling on RDS took some time to find optimal configuration
- Domain knowledge footprint is quite large
  - More moving parts - means more things that can break

---
transition: fade-out
---

# Retrospective - 3

If I'd do it again 🤔❓

- Opt for solution 2 - `half-n-half`
  - Think having more of the light I/O data in RDS would have improved our ability to implement some features
  - Less infra to maintain
  - Domain / Code footprint would be smaller
- `Present Day` if I was required to use solution 3
  - use AWS out of the box DDB ➡️ RDS sync process 