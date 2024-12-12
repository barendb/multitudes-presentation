---
transition: fade-out
---

# Current Architecture

- NoSQL DB - AWS DynamoDB
- Ver Radar implemented a repository pattern
  - Data queried via an entity ex `Patient.getSingle(org_id, patient_id)`
- Every `entity` was a separate table. _Did not implement single|one table NoSQL pattern_
- Implementation mimicked more traditional RDS data storage

<div grid="~ cols-2 gap-2" m="t-2">
<img border="rounded" src="../assets/erd.png" />
<img border="rounded" src="../assets/sheet.png" />
</div>


<style>
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