# 📚✨ **Building a Knowledge-Powered Experience Cloud Site — Adding Articles and Featured Topics with Heart**

---

## 💬 1. Friendly Introduction  
Welcome back, Trailblazer! 🌟  
In this session, we’re taking your **Experience Cloud site** one step closer to becoming a **complete self-service hub** — by adding **Knowledge Articles** and **Featured Topics** that help your customers find answers instantly.  

💡 *Imagine your Experience Cloud site as a digital library — every article is a helping hand waiting to guide your users.*

---

## 🧠 2. Business Context & Real-World Need  
In modern customer service, **knowledge is empowerment**.  
Businesses use Salesforce **Knowledge** and **Topics** to organize articles into accessible, searchable, and user-friendly categories.  

Through this setup, your Experience Cloud site can:  
📖 Display trending and featured articles.  
🔍 Help customers self-serve instead of raising cases.  
🧭 Organize content by themes like *Support*, *Products*, or *Features*.  
💬 Enhance engagement through relevant and well-structured content.  

✨ *When knowledge is easy to find, customers feel empowered, and your agents save valuable time.*

---

## ⚙️ 3. Core Concept (Simplified Explanation)  
**Salesforce Knowledge** is your organization’s internal and external help center — a place to store and publish helpful content.  

- **Knowledge Articles**: Contain answers, guides, and FAQs.  
- **Topics**: Act as categories to organize those articles.  
- **Trending or Featured Sections**: Showcase popular or important content on your Experience Cloud site.  

💬 *Think of Topics like shelves in a bookstore — each shelf holds related books (articles) your readers can explore.*

---

## 🧩 4. Key Components & Configurations  

Let’s break the process step by step 🔽  

### 🧱 Step 1: Enable Knowledge Setup  
1️⃣ Go to **Service Setup → Knowledge Setup**.  
2️⃣ Click **Start** and follow prompts.  
3️⃣ Add yourself (or relevant users) as Knowledge authors.  
4️⃣ Finish setup — Knowledge is now enabled.  

### 🧩 Step 2: Add Custom Fields to Knowledge Object  
1️⃣ Go to **Setup → Object Manager → Knowledge**.  
2️⃣ Create a new **Text Area Field** (for your article content).  
3️⃣ Make it visible to all profiles.  
4️⃣ Add this field to the **Lightning Knowledge FQ Layout**.  
5️⃣ Save your layout — now every article has a proper content section.  

### 🧭 Step 3: Enable Topics for Knowledge  
1️⃣ Go to **Setup → Topics for Objects**.  
2️⃣ Choose **Knowledge** as the object.  
3️⃣ Select fields for topic suggestions:  
   - **Title**  
   - **Text**  
4️⃣ Save — now your articles can be categorized under different topics (like *Support*, *New Products*, *Features*).  

### 🧾 Step 4: Create and Publish Knowledge Articles  
Let’s add your first few articles 🧠  

| Example Title | Example Text | Visibility |
|----------------|---------------|-------------|
| “When will iPhone 14 cases be available?” | “Expected release in November next year.” | ✔️ Visible to customers |
| “Can I customize my phone case?” | “Yes! You can personalize cases with names or photos from next month.” | ✔️ Visible to customers |
| “How long does delivery take?” | “Usually 2–3 business days.” | ✔️ Visible to customers |
| “How to return a damaged case?” | “Return within 3–4 business days with your order number for a quick refund.” | ✔️ Visible to customers |

✅ Save and **Publish** each article.  
✅ Mark “Visible to Customers” so it appears on the portal.  

---

## 💣 5. Common Challenges or Misconfigurations  
🚫 Forgetting to make articles “Visible to Customer.”  
🚫 Not assigning Topics — resulting in articles not showing on the site.  
🚫 Forgetting to publish after editing.  
🚫 Adding the Knowledge component directly (it only works via Topics).  

💬 *Always group your Knowledge Articles under Topics before publishing to the site.*

---

## 🧰 6. Consultant Tips & Best Practices  
🔹 Use clear, friendly article titles that sound like real customer questions.  
🔹 Keep answers short, positive, and solution-focused.  
🔹 Tag every article under relevant topics — it improves search and engagement.  
🔹 Regularly review trending topics to update fresh content.  
🔹 Always test visibility using a **customer community user** login.  

💡 *Knowledge works best when it feels human, not robotic.*

---

## 🧭 7. Real Implementation Example  
💬 *Picture this:*  
An eCommerce company selling iPhone accessories builds a **Knowledge Library** in their Experience Cloud portal.  

They create three featured topics:  
1️⃣ **Customer Support** – returns, refunds, delivery issues.  
2️⃣ **New Products** – latest accessories and updates.  
3️⃣ **Upcoming Features** – product launches and customizations.  

Each topic has 3–4 related Knowledge Articles.  
On the homepage, users instantly see “Trending Articles” like:  
> “How to track my order?”  
> “When will new designs be available?”  

Result: Fewer support cases, faster answers, and happier customers. 🌟  

---

## 🧮 8. Metrics & Success Indicators  
📈 **Article Views:** Track engagement per topic.  
💬 **Case Deflection Rate:** How many customers find answers without raising tickets.  
🧾 **Publication Volume:** Number of active, customer-visible articles.  
🌍 **Search Efficiency:** How often users find what they’re looking for.  

---

## 🧑‍💼 9. Role Connections  
Different Salesforce roles contribute uniquely:  
- **Admin:** Enables Knowledge, creates custom fields, and manages access.  
- **Consultant:** Designs content taxonomy (topics and structure).  
- **Author:** Writes and maintains Knowledge Articles.  
- **Architect:** Ensures scalability and search optimization.  

---

## 🧾 10. Exam Questions & Quick Recap  
🧠 **Q1:** What connects Knowledge Articles to the Experience Site?  
💬 **A:** Topics (they categorize and display articles).  

🧠 **Q2:** Where do you enable Knowledge in Salesforce?  
💬 **A:** Service Setup → Knowledge Setup.  

🧠 **Q3:** Why must you mark “Visible to Customer”?  
💬 **A:** So the article is viewable on the Experience Cloud portal.  

🧠 **Q4:** Can Knowledge be added directly to a site?  
💬 **A:** No, it must be displayed through Topics components.  

---

## 📜 11. Governance & Ethical Practice  
🟢 Keep all Knowledge Articles up to date.  
🟢 Avoid sharing internal-only content publicly.  
🟢 Respect copyright — write original help content.  
🟢 Review tone — make answers empathetic and professional.  

---

## 🔍 12. Real-Life Story or Case Study  
A non-profit created a **Knowledge Base** for volunteers.  
They organized help articles under *Training*, *Events*, and *Tech Support* topics.  

💡 Volunteers stopped flooding email support — they found answers instantly on the site.  
❤️ *Knowledge empowered everyone to serve better.*  

---

## 📚 13. Key Takeaways (Warm Recap)  
✅ Knowledge = Power + Simplicity.  
✅ Topics connect articles to site components.  
✅ Clear, relatable answers improve customer experience.  
✅ Publishing visibility is key to accessibility.  

---

## 🧩 14. Visual Blueprint (Concept Mapping)  
💡 *Visualize this structure:*  

| Layer | Function | Example |
|-------|-----------|----------|
| 🧱 Knowledge Base | Stores all articles | “How to return a damaged case?” |
| 🏷️ Topics | Categorize content | “Customer Support” |
| 🌐 Experience Site | Displays Topics & Articles | “Trending Articles” section |
| 👩‍💻 Customer | Searches or clicks topic | Finds answers instantly |

---

## 🧾 15. Try This Today (Practical Action)  
💡 Create one **Knowledge Article** for your company FAQ.  
💡 Enable **Topics for Knowledge** and tag it under “Customer Support.”  
💡 Publish and test its visibility as a **guest user**.  

---

## 🧡 16. Closing Note (Heartfelt Wrap-Up)  
✨ Every Knowledge Article is a small act of service —  
a digital helping hand that says, *“You’re not alone; here’s your answer.”*  

Your Experience Cloud site becomes more than a portal — it becomes a **space of understanding and empowerment.** 💙  

---

## 📘 17. Key Salesforce Terms & Full Forms  

| Term | Full Form |
|------|------------|
| CRM | Customer Relationship Management |
| CMS | Content Management System |
| KB | Knowledge Base |
| CSP | Content Security Policy |
| FAQ | Frequently Asked Questions |
| Topic | Categorization tag for Knowledge Articles |

---

## 🌿 18. Ethical Writing & Attribution Note  
All content is **originally written** for Salesforce education.  
No external or copyrighted material is reused.  
Goal: To promote **digital literacy, professional integrity, and knowledge empowerment.** 🌱  

---

## 💫 Soul Summary (2 Lines)  
Knowledge Articles don’t just share information — they build **trust**.  
In every Experience Cloud site, empathy is the real engine of engagement. 💙  
