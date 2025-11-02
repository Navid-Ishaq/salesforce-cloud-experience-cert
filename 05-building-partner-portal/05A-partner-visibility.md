# 🌉 Understanding Partner Role Hierarchy and Opportunity Visibility in Salesforce Experience Cloud  
*A compassionate, structured study guide written as mentorship in motion.*  

---

## 1. Warm Welcome  
Hey there, Trailblazers 🌟 — welcome back to another step in mastering Salesforce Experience Cloud!  
In this session, we’re not just clicking buttons — we’re understanding **how trust, hierarchy, and access** come together to make your **partner ecosystem transparent and collaborative**.  

Today, you’ll learn how **role hierarchy** affects what your partners can see — and how managers and users interact with opportunities in real-time.  

---

## 2. Real-World Context  
Imagine a company like **United Oil & Gas Corp** working with multiple vendors and partner users.  
Each partner has its own internal structure — managers, users, and teams.  
Salesforce Experience Cloud allows you to **mirror that hierarchy digitally**, ensuring every partner sees what’s relevant to them, and nothing more.  

It’s like giving every team their own window into your ecosystem — tailored to their responsibilities.  

---

## 3. What We’re Achieving  
By the end of this guide, you’ll be able to:  
✅ Enable new accounts as **Partner Accounts**.  
✅ Create multiple **Partner Users** with different roles.  
✅ Assign opportunities to partners.  
✅ Test opportunity visibility across the **role hierarchy**.  

---

## 4. Core Concept — Partner Role Hierarchy  
In a Partner Community, users are tied to their **Account**, and Salesforce automatically builds a **three-level role hierarchy** (based on your setup):  

| Role | Description |
|------|--------------|
| **Partner Manager** | Supervises partner users; sees their records. |
| **Partner User** | Works on assigned opportunities and leads. |
| **Partner Executive (optional)** | Oversees multiple manager accounts. |  

This structure ensures managers can view what their users create — but users cannot see their manager’s records unless shared explicitly.  

---

## 5. Step 1: Enabling the Account as Partner  
Let’s begin by choosing a new account to work with — for example, **United Oil and Gas Corp**.  

1. Go to the **Account Record**.  
2. Click **Enable as Partner** (make sure this button exists on your page layout).  
3. If the button is missing, the account may already be enabled as a partner.  

Once enabled, this account becomes a **Partner Account** — meaning you can now create **Partner Users** under it.  

---

## 6. Step 2: Creating Partner Users  
Now let’s create two contacts:  
- **Stella Pavlova** → Partner User  
- **Jason Smith** → Partner Manager  

**For Stella:**  
1. Open her Contact record.  
2. Click **Enable Partner User**.  
3. Assign profile: *Partner Community User*.  
4. Assign role: *Partner User*.  
5. Save and verify her email invitation to set the password.  

**For Jason:**  
1. Open his Contact record under the same account.  
2. Click **Enable Partner User**.  
3. Assign profile: *Partner Community User*.  
4. Assign role: *Partner Manager*.  
5. Save and verify login.  

Both now belong to the same Partner Account, but with different hierarchy roles.  

---

## 7. Step 3: Logging in as Partner Users  
After setting up credentials, Stella and Jason can log in via the site URL (e.g., *Apple Vendors Portal*).  
- When **Stella** logs in → she sees the portal layout but **no opportunities yet**, since none are assigned.  
- When **Jason** logs in → same thing, no opportunities yet, until we assign ownership.  

It’s time to assign opportunities to test visibility!  

---

## 8. Step 4: Assigning Opportunities  
Go back to your internal Salesforce org and open **United Oil and Gas Corp**.  
You’ll now reassign some opportunities to Stella:  

1. Open any opportunity record.  
2. Click **Change Owner**.  
3. Choose “Partner User” and select *Stella Pavlova*.  
4. Repeat for 2–3 opportunities.  

Now Stella owns three opportunities.  

---

## 9. Step 5: Verifying Access  
Let’s test visibility:  
- **Stella** logs in and sees three opportunities — the ones she owns.  
- **Jason**, her manager, also sees these same three opportunities because of **role hierarchy inheritance**.  

💡 *Manager roles automatically roll up the visibility of their direct users’ records.*  

---

## 10. Step 6: Cross-Account Visibility (Important!)  
Now let’s bring in another partner: **Pat Stumbler**, who belongs to a *different Partner Account* — *Pyramid Construction*.  

When you assign opportunities under *United Oil and Gas Corp*, **Pat will not see them**.  
Partner Users can only see records tied to their **own Account** or records shared through explicit sharing rules.  

This ensures **data isolation and security** between partner organizations.  

---

## 11. Role-Based Access in Action  
To summarize access rules:  

| Role | Can View Their Own Opportunities? | Can View Subordinate’s Opportunities? | Cross-Account Access? |
|------|-----------------------------------|---------------------------------------|------------------------|
| Partner User | ✅ Yes | ❌ No | ❌ No |
| Partner Manager | ✅ Yes | ✅ Yes (from users below) | ❌ No |

This simple hierarchy makes collaboration easy while keeping boundaries clear.  

---

## 12. Step 7: Quick Login Using “Login to Experience as User”  
You can test access easily from the **Contact layout**.  
Add the button **Login to Experience as User** under *Mobile & Lightning Actions*.  
Now, from any contact record, click it to open their view of the portal instantly — no incognito windows required.  

It’s perfect for admin testing and troubleshooting.  

---

## 13. Ethical and Security Reflections  
Salesforce’s partner access model is built around **trust and transparency**.  
Always ensure:  
- Each partner account is legitimate and verified.  
- Data is segregated using account-level sharing.  
- Partner managers have only the access they need — no more, no less.  

Ethical CRM means **collaboration without compromise**.  

---

## 14. Common Pitfalls and Fixes  
⚠️ **Missing Buttons?** Check your Lightning Layouts.  
⚠️ **Duplicate Username?** Every Salesforce username must be globally unique.  
⚠️ **Partner Can’t See Opportunities?** Verify ownership and role hierarchy.  
⚠️ **Cross-Account Leakage?** Review your sharing rules.  

---

## 15. Best Practices  
✔ Keep partner naming conventions clean and consistent.  
✔ Assign opportunities thoughtfully — use Account Ownership alignment.  
✔ Test both partner user and manager logins before going live.  
✔ Document your hierarchy for audit clarity.  

---

## 16. Visual Summary 🧭  
```
Account → Enable as Partner
    ↓
Create Contacts → Enable as Partner Users
    ↓
Assign Roles → User / Manager
    ↓
Assign Opportunities → to Partner User
    ↓
Manager Automatically Sees Subordinate’s Opportunities
    ↓
Cross-Account Isolation Maintained
```

---

## 17. Reflection Moment 💭  
Pause and reflect: this isn’t just a demo — it’s a mirror of real business relationships.  
Each opportunity represents a shared goal, each hierarchy level represents trust.  
When you design portals this way, you’re not just managing data — you’re nurturing partnerships.  

---

## 18. Certification-Style Practice Questions  

**Q1:** What happens when you enable an Account as a Partner?  
→ The account becomes a Partner Account, allowing contacts to be converted into Partner Users.  

**Q2:** Can Partner Users from different accounts see each other’s opportunities?  
→ No, each Partner Account’s data is isolated unless shared manually.  

**Q3:** How does role hierarchy affect visibility?  
→ Managers can see all records owned by their users, but not vice versa.  

**Q4:** What is the purpose of the “Login to Experience as User” button?  
→ It allows admins to view the portal as a specific user for testing access.  

**Q5:** What defines ethical sharing in Partner Communities?  
→ Ensuring that users see only what’s relevant, maintaining privacy across accounts.  

---

## 🌱 Final Thought  
Every record shared, every login granted, is a sign of partnership and trust.  
Salesforce Experience Cloud is not just about visibility — it’s about *empowerment through responsible access.*  
Keep building with heart ❤️ and precision.  
