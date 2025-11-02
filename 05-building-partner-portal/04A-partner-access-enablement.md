# 🤝 Enabling Partner Access in Salesforce Experience Cloud  
*A compassionate, structured study guide that turns learning into mentorship.*  

---

## 1. Warm Welcome  
Hello, Trailblazers 🌟 — welcome back!  
So far, we’ve created our **Partner Portal site**, but it’s only visible to *internal users*. Today, we’ll bridge that gap and **give our external partners access** — the very reason we built this portal in the first place.  

Let’s turn our static portal into a thriving collaboration space for your vendors and partners.  

---

## 2. Real-World Context  
Imagine you’re Apple, managing partnerships with distributors like AT&T or Pyramid Construction.  
Your internal team can already see opportunities, leads, and deals within Salesforce. But your **partners** — those external vendors who help you sell — need *controlled access* to collaborate effectively.  

That’s where **Experience Cloud Partner Access** steps in.  

---

## 3. What We’re Achieving  
By the end of this session, you’ll be able to:  
✅ Enable partner access at the **Account** level.  
✅ Create **Partner Users** at the **Contact** level.  
✅ Assign appropriate **profiles, roles, and licenses** for secure collaboration.  

---

## 4. Conceptual Foundation — Accounts, Contacts, and Partners  
In Salesforce:  
- **Accounts** represent your *partner companies* (e.g., AT&T).  
- **Contacts** represent the *people working at those companies* (e.g., John, Simran, Michael).  
- **Partner Users** are Salesforce user accounts created from those contacts so they can log into the portal.  

So, when we say “enable as partner,” we’re really turning an **Account** into a **Partner Organization**.  

---

## 5. The Two Key Buttons  
When you enable Experience Cloud for Partner Sites, Salesforce gives you two special buttons:  

| Button | Used On | Purpose |
|---------|----------|----------|
| **Enable as Partner** | Account Page | Converts an Account into a Partner Account |
| **Enable as Partner User** | Contact Page | Creates a Partner User login for that contact |

We’ll enable these buttons so you can easily manage partner access.  

---

## 6. Preparing the Account Layout  
Let’s customize the **Account Page Layout** first.  
1. Go to **Setup → Object Manager → Account → Page Layouts**.  
2. Select your desired layout (e.g., *Account Layout*).  
3. In the **Mobile & Lightning Actions** section, drag:  
   - 🟢 *Enable as Partner*  
   - 🔴 *Disable Partner Account*  

💡 *Tip:* The “Disable Partner” button lets you revoke access later — for instance, if a vendor relationship ends.  

4. Click **Quick Save** when done.  

---

## 7. Preparing the Contact Layout  
Next, edit the **Contact Layout**:  
1. Navigate to **Setup → Object Manager → Contact → Page Layouts**.  
2. Select the desired layout (e.g., *Contact Layout*).  
3. Under **Mobile & Lightning Actions**, drag:  
   - 🟢 *Enable as Partner User*  
   - 🔴 *Disable Partner User*  

Click **Save**, and you’re ready to manage partner contacts dynamically.  

---

## 8. Real-World Analogy 🌍  
Think of it like this:  
- The **Account** is your *partner company’s front door*. You unlock it by clicking *Enable as Partner*.  
- The **Contacts** are *employees inside that building*. You hand them keys (login credentials) with *Enable as Partner User*.  

Once both steps are done, your partners can log in and collaborate in your Experience Cloud site.  

---

## 9. Creating a Partner User  
Now that your layouts are ready, let’s create a partner user manually:  

1. Go to **Setup → Users → New User**.  
2. Fill in details like name, email, and username.  
3. Choose a **Partner License** (e.g., *Channel Sales Team*).  
4. Assign a **Profile** — e.g., *Partner Community User* or *Custom Sales Profile*.  
5. Click **Save**.  

Salesforce will send a verification email to the user, prompting them to set up their password.  

---

## 10. Linking Accounts and Contacts  
Let’s bring it all together.  

1. Choose an existing **Account** (e.g., *Pyramid Construction*).  
2. Click **Enable as Partner** — now it’s a partner account.  
3. Open a **Contact** under that account (e.g., *Pat Stuller*).  
4. Click **Enable as Partner User**.  

Salesforce automatically:  
- Creates a **User Record** for Pat.  
- Assigns a **Partner Role** (e.g., *Partner User* or *Partner Manager*).  
- Sends an activation email for login setup.  

---

## 11. Roles and Hierarchies  
When you enabled Partner Accounts, Salesforce asked: *How many partner roles do you want?*  
Let’s say you chose two:  
- **Partner Manager** (supervises partner users)  
- **Partner User** (regular collaborator)  

These roles follow a built-in hierarchy — users report to their managers automatically.  

---

## 12. Example Implementation Story  
Let’s illustrate:  

🏗 **Pyramid Construction** becomes a Partner Account.  
👤 *Pat Stuller* becomes a Partner User under Pyramid.  
📧 Pat receives an email to activate his login.  
🔐 Once he logs into the **Apple Vendors Portal**, he sees:  
- Home tab, Deals tab, Marketing tab — but **no opportunities yet.**  

Why? Because permissions and sharing rules still need to be configured — we’ll handle that in the next tutorial.  

---

## 13. Ethical & Security Insight  
Remember: granting access is about **trust**.  
Always verify that:  
- Only legitimate partner accounts are enabled.  
- Partner users have restricted data visibility.  
- You maintain an audit trail of all partner activations.  

Empathy in CRM means protecting your partners’ and customers’ data equally.  

---

## 14. Troubleshooting & Common Pitfalls  
❌ *Missing Buttons?*  
Make sure you’ve added the actions to the correct **Lightning Layouts**.  

❌ *Duplicate Username Error?*  
Usernames must be **globally unique across Salesforce** (e.g., `user@company.com.portal`).  

❌ *Partner Can’t See Data?*  
They might need proper **sharing rules** or **role hierarchy** updates.  

---

## 15. Best Practices  
✔ Keep naming conventions consistent (e.g., “Partner – Account Name”).  
✔ Always test in **Incognito Mode** to simulate external user access.  
✔ Use **custom profiles** for more granular permission control.  
✔ Review partner access logs quarterly.  

---

## 16. Visual Summary (Quick Reference)  
```
Account → Enable as Partner
     ↓
Contact → Enable as Partner User
     ↓
User Record Created
     ↓
Assign License + Profile
     ↓
Partner Logs Into Portal
     ↓
Verify Access → Adjust Sharing Rules
```

---

## 17. Reflection Moment 💭  
Pause and consider: you’re not just enabling buttons — you’re empowering collaboration.  
Every *Enable as Partner* click symbolizes **trust**, and every partner login represents **shared growth**.  
Salesforce isn’t just software; it’s a digital handshake between organizations.  

---

## 18. Certification-Style Questions  

**Q1:** What’s the difference between *Enable as Partner* and *Enable as Partner User*?  
→ *Enable as Partner* converts an Account; *Enable as Partner User* creates login access for a Contact.  

**Q2:** Where can you find the “Enable as Partner” button to add it to the layout?  
→ *In the Account Page Layout → Mobile & Lightning Actions.*  

**Q3:** Why might a Partner User see “no opportunities” after logging in?  
→ *Because sharing rules and role hierarchies haven’t been configured yet.*  

**Q4:** What are the two common partner roles in Salesforce?  
→ *Partner Manager* and *Partner User.*  

**Q5:** What does ethical CRM practice require when granting partner access?  
→ *Transparency, limited data visibility, and proper auditing.*  

---

## 🌱 Final Thought  
Creating partner access isn’t just a configuration step — it’s the start of a digital partnership built on clarity and mutual respect.  
In Salesforce, technology meets trust, and with each portal you create, you’re not just enabling logins — you’re enabling collaboration. ❤️
