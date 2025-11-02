# 🔐 Record Sharing and OWD in Salesforce Experience Cloud  
*A deeply human, structured study guide that makes complex Salesforce access models simple and intuitive.*  

---

## 1. Warm Welcome  
Hey there, Trailblazers 🌟 — welcome back to another chapter in your Salesforce Experience Cloud journey!  
You’ve already built a Partner Portal, enabled partner accounts, and created partner users and managers.  
Now, let’s talk about one of the most powerful — and often misunderstood — aspects of Experience Cloud: **Record Sharing and Organization-Wide Defaults (OWD)**.  

This is where collaboration meets control.  

---

## 2. Real-World Context  
Imagine you manage two partner companies:  
- 🏗 **Pyramid Consulting**  
- 🏨 **Grand Hotels**  

Each company has its own contacts, managers, and opportunities.  
You want every partner to see *only their own records* — unless they’re a manager, who should see their team’s work too.  

That’s the essence of **record visibility** in Salesforce Experience Cloud.  

---

## 3. What We’re Achieving  
By the end of this session, you’ll be able to:  
✅ Understand how **role hierarchy** affects visibility.  
✅ Identify differences between **internal and external OWDs**.  
✅ Grasp why **external users (partners)** see fewer records by default.  
✅ Recognize multiple ways to open access — ethically and securely.  

---

## 4. Foundation — Roles, Hierarchies, and Partner Access  
Let’s recap how we structured partners:  
- **Partner Manager** → Supervises partner users.  
- **Partner User** → Reports to the partner manager.  

Any records created by a *Partner User* automatically become visible to the *Partner Manager* due to **role hierarchy inheritance**.  

This is Salesforce’s way of mirroring real business reporting structures.  

---

## 5. Example: Two Partner Accounts  
Let’s visualize this setup.  

| Account | Partner Contacts | Roles | Owned Opportunities |
|----------|------------------|--------|---------------------|
| **Pyramid Consulting** | Avi, John, Stella | Avi – Partner User<br>John – Partner Manager<br>Stella – Partner User | Opp1 – Avi<br>Opp2 – John<br>Opp3 – Stella |
| **Grand Hotels** | Daisy, Mohit, Tracy | Mohit – Partner Manager<br>Daisy – Partner User<br>Tracy – Partner User | Opp4 – Daisy<br>Opp5 – Mohit<br>Opp6 – Tracy |  

Now let’s see who can view what.  

---

## 6. Record Visibility Breakdown  
| User | Account | What They Can See |
|------|----------|------------------|
| **Avi** | Pyramid Consulting | Only Opp1 (self-owned) |
| **Stella** | Pyramid Consulting | Only Opp3 (self-owned) |
| **John (Manager)** | Pyramid Consulting | Opp1, Opp2, Opp3 (team’s records) |
| **Daisy** | Grand Hotels | Only Opp4 |
| **Tracy** | Grand Hotels | Only Opp6 |
| **Mohit (Manager)** | Grand Hotels | Opp4, Opp5, Opp6 |  

This pattern reflects **role-based record sharing**.  

---

## 7. Why Role-Based Sharing Exists  
Salesforce assumes a world of responsibility — if you manage someone, you should see what they create.  
That’s exactly what **Role Hierarchy** enforces: *visibility flows upward.*  
But it only comes into play when **Organization-Wide Defaults (OWD)** are **Private**.  

So, let’s uncover what that means.  

---

## 8. Organization-Wide Defaults (OWD) Explained  
OWD defines the **base level of access** to each object across your org.  
There are two OWD columns for every object:  

| Access Type | Who It Applies To | Description |
|--------------|-------------------|--------------|
| **Internal Access** | Internal Salesforce users | For users like admins, standard users, sales reps |
| **External Access** | External users (portal, community, partner) | For Experience Cloud and portal users |  

To view OWD settings:  
**Setup → Sharing Settings → Default External Access.**  

---

## 9. Example: Opportunity Object OWD  
| Object | Internal Access | External Access |
|---------|-----------------|-----------------|
| **Opportunity** | Public Read/Write | Private |  

For **internal users**, everyone can see and edit opportunities.  
For **external users**, each partner can only see their own records.  

This ensures **data isolation** between different partner organizations.  

---

## 10. Key Concept: Internal vs External Users  
- **Internal Users:** System Admins, Standard Users (Salesforce Licenses).  
- **External Users:** Partner Users, Community Users (Experience Cloud Licenses).  

When an external user logs in, the **external OWD** column applies — meaning their access is typically much more limited.  

---

## 11. Role Hierarchy and OWD Together  
OWD is your *baseline fence*.  
Role hierarchy is the *gate* that lets certain people see over it.  

- If OWD = **Private**, users see *only what they own*.  
- Managers (higher in hierarchy) see their team’s records automatically.  
- Peers at the same level **cannot** see each other’s data unless sharing rules or sharing sets apply.  

---

## 12. Sharing Beyond Roles — Four Ways to Open Access  
When OWD is **Private**, Salesforce gives you four ethical ways to open visibility:  

| Method | Description | Applies To |
|---------|--------------|-------------|
| **Role Hierarchy** | Managers see records owned by subordinates. | Partners (Community Plus and above) |
| **Sharing Rules** | Share records between peers or teams. | Internal & External |
| **Sharing Sets** | Share records with external users based on Account or Contact link. | Experience Cloud users |
| **Account Relationships** | Define relationships between accounts to share across partner orgs. | Partner Communities |  

Each approach balances *visibility* with *privacy*.  

---

## 13. Ethical Access Design 🌱  
When designing sharing for partners, think ethically:  
✅ Give users **enough** access to do their job.  
🚫 Never overexpose records between unrelated partners.  
⚖️ Use hierarchy and rules intentionally — not as shortcuts.  

Data access is trust in digital form.  

---

## 14. Common Pitfalls and Fixes  
⚠️ **Confusing internal and external OWD columns** — always verify which applies.  
⚠️ **Partner Users seeing nothing?** Their external OWD is likely private.  
⚠️ **Managers can’t see subordinate records?** Role hierarchy may be disabled for external users.  
⚠️ **Peers can’t collaborate?** Add a sharing rule or sharing set.  

---

## 15. Best Practices  
✔ Keep OWD **as restrictive as possible** — open access only when needed.  
✔ Always document your **sharing model** before implementation.  
✔ Test user visibility using incognito logins.  
✔ Use **“View as Partner User”** to validate access paths.  
✔ Separate internal and external sharing logic clearly.  

---

## 16. Visual Summary 🧭  
```
OWD = Private (External)
        ↓
Partner User sees only their own records
        ↓
Role Hierarchy grants managers access to subordinates' records
        ↓
Sharing Rules / Sets / Account Relationships widen access responsibly
```

---

## 17. Reflection Moment 💭  
Think of sharing in Salesforce as the architecture of trust.  
OWD builds the walls.  
Role hierarchy opens the doors upward.  
Sharing rules and sets create carefully chosen windows.  

Every design choice you make tells your partners, *“We respect your data.”*  

---

## 18. Certification-Style Practice Questions  

**Q1:** What does OWD = Private mean for external users?  
→ They can only see the records they own.  

**Q2:** Which column in Sharing Settings affects Partner Users?  
→ *Default External Access.*  

**Q3:** How can you share records among partners within the same account?  
→ Use *Sharing Sets*.  

**Q4:** How can you share records across accounts?  
→ Use *Account Relationships.*  

**Q5:** When does role hierarchy apply to partners?  
→ For *Partner Community* or *Community Plus* users — not basic Community licenses.  

---

## 🌱 Final Thought  
Salesforce sharing is more than permissions — it’s **a digital reflection of organizational trust**.  
By mastering OWD, roles, and sharing rules, you create not just security, but *clarity and collaboration*.  
Keep your access models honest, minimal, and purposeful — that’s where good architecture meets good ethics. ❤️
