---
transition: fade-out
---

# Requirements

Solution needed to adhere to following requirements

<div grid="~ cols-2 gap-2" m="t-2">
<div>

## Business requirements

- 📊 **Reporting** - Ability to generate reporting from data
- 📈 **BI** - Ability to create Business Intelligence Dashboards / Client Dashboards (in App)
- 🩻 **Insights** - Engineers want to be able to gather insights from data
- ⏱️ **Urgency** - We needed a solution that could be implemented fairly quickly and easily
</div>
<div>

## Engineering requirements

- ❤️‍🩹 **Developer Ex** - Should not be difficult for engineers
- 🏋️‍♀️ **Robust, reliable and scalable** - Handle our growing customer base
- 🧹 **Maintenance** - Easy for engineers to maintain
- ⛔️ **Not complete refactor** - Avoid having a complete refactor


</div>
</div>

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
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

<div><h2>Was pretty obvious we needed our data in an RDS</h2></div>
<br/>
<div v-click><h2>Based on the team's experience - we opted for boring tech Postgres RDS</h2></div>