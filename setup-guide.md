# Tool Setup Guide for Energy Vampire Blasters

Step-by-step setup for David's tech stack. Total monthly cost: ~$5-10/mo to start.

---

## 1. Kit (ConvertKit) -- Email List + Nurture Sequences

**What it does:** Captures emails, sends automated sequences, delivers free downloads, tags buyers vs free subscribers.

**Cost:** Free up to 10,000 subscribers.

### Setup Steps

1. Go to kit.com and create a free account
2. Create a **Landing Page** for the Detection Kit:
   - Template: "Newsletter" or "Ebook" template
   - Headline: "Get the Free Energy Vampire Detection Kit"
   - Form fields: Email only (reduce friction)
   - After signup: redirect to the Detection Kit PDF or deliver via email
3. Create **Tags** to segment your audience:
   - `detection-kit` -- downloaded free guide
   - `quiz-taker` -- took the quiz
   - `book-buyer-guide` -- bought the $2.99 guide
   - `book-buyer-full` -- bought the $9.99 book
   - `challenge-ga` -- bought GA challenge
   - `challenge-vip` -- bought VIP challenge
   - `skool-member` -- joined Skool
4. Create **Email Sequence** "7-Day Challenge":
   - Import the 10 emails from `email-sequence.md`
   - Set timing: Welcome (immediate), then Days 1-7 (one per day), Day 8 (3 days after Day 7), Day 10 (5 days after Day 7)
   - Trigger: when someone gets tagged `challenge-ga` or `challenge-vip`
5. Create **Email Sequence** "Detection Kit Welcome":
   - Email 1 (immediate): "Here's your Detection Kit" + PDF link
   - Email 2 (Day 2): "The 5 vampires -- which one is yours?" + quiz link
   - Email 3 (Day 4): "Ready to go deeper?" + book CTA
   - Email 4 (Day 6): "The 7-Day Challenge is open" + challenge CTA
   - Email 5 (Day 8): "What people are saying" + Skool CTA

### Key Settings
- Sender name: "David Strauss | Energy Vampire Coach"
- Sender email: Use a professional email (david@energyvampireblasters.com or similar)
- Double opt-in: OFF (reduces friction for lead magnets)

---

## 2. Payhip -- Paid Downloads + Challenge Payments

**What it does:** Hosts paid digital products, handles payment, delivers files, no monthly fee.

**Cost:** Free plan. 5% transaction fee per sale. (On a $9.99 book = $0.50 fee. On a $47 VIP = $2.35 fee.)

### Setup Steps

1. Go to payhip.com and create an account
2. Create **4 products**:

| Product | Price | Type | Delivery |
|---------|-------|------|----------|
| Toxic Love Quick Guide | $2.99 | Digital download | PDF (print toxic-love-guide.html to PDF) |
| Breaking The Habit of Toxic Love | $9.99 | Digital download | PDF (print toxic-love-book.html to PDF) |
| 7-Day Challenge -- GA | $27 | Digital download | Redirect to Kit sequence (or deliver welcome PDF) |
| 7-Day Challenge -- VIP | $47 | Digital download | Redirect to Kit sequence + bonus materials |

3. For each product:
   - Upload the PDF file
   - Set the price
   - Write a short description
   - Add the book cover image as the product image
4. **Connect Payhip to Kit:**
   - Payhip has a native Kit/ConvertKit integration
   - Go to Payhip > Settings > Integrations > ConvertKit
   - Add your Kit API key
   - For each product, set it to add the appropriate Kit tag on purchase
   - This way, when someone buys the challenge, Kit automatically starts the email sequence

### Key Settings
- Currency: USD
- Checkout: Enable "Pay what you want" OFF (fixed prices)
- After purchase redirect: Set to a thank you page or the Kit landing page

---

## 3. ManyChat -- Instagram DM Automation

**What it does:** When someone comments a keyword on your Instagram post (like "VAMPIRE"), ManyChat automatically DMs them with a link.

**Cost:** Free up to 1,000 contacts. Pro is $15/mo for unlimited.

### Setup Steps

1. Go to manychat.com and connect David's @energyvampireblasters Instagram account
2. Create **Automation Flows** for each keyword:

| Keyword | DM Message | Link |
|---------|-----------|------|
| VAMPIRE | "Here's your free Energy Vampire Detection Kit! Download it here and find out which vampire is draining your life." | Kit landing page (email capture -> PDF) |
| ESCAPE | "Ready to break free? Here's your copy of Breaking The Habit of Toxic Love." | Payhip book page ($9.99) |
| QUIZ | "Let's find out which Energy Vampire is draining you! Take the 2-minute quiz:" | Quiz page URL |
| CHALLENGE | "The 7-Day Energy Vampire Blaster Challenge is here! Choose your level:" | Website challenge section or Payhip |

3. For each flow:
   - Trigger: "Comment contains keyword" (set to the Instagram post or all posts)
   - Action: Send DM with the message + link
   - Optional: Ask for email in the DM flow before sending the link (captures email in ManyChat too)
4. **Connect ManyChat to Kit:**
   - ManyChat has a native Kit integration
   - When someone gives their email in the DM flow, it adds them to Kit with the appropriate tag

### Key Settings
- Enable "Comment Automation" in ManyChat settings
- Set keyword matching to "contains" (not exact match) so "vampire" and "VAMPIRE" both work
- Test each flow by commenting the keyword on a test post

---

## 4. Buffer -- Social Media Scheduling

**What it does:** Schedule Instagram posts in advance so David can batch content.

**Cost:** $5/mo (Essentials plan). Covers 1 account.

### Setup Steps

1. Go to buffer.com and create an account
2. Connect @energyvampireblasters Instagram account
3. Set posting schedule (recommended):
   - Monday, Wednesday, Friday: 9am + 6pm (2 posts/day, 3 days)
   - Tuesday, Thursday: 12pm (1 post/day)
   - Saturday: 10am (1 post)
   - = 9 posts per week
4. Use the 30-day content calendar from `instagram-strategy.md` to pre-schedule posts

---

## 5. Skool -- Community ($97/mo)

**David already has this set up.** Key actions to prepare for launch:

1. Set price to $97/mo
2. Create a welcome post pinned to the top
3. Set up the gamified levels David already designed
4. Create a "Start Here" module in the classroom
5. Upload first week of drip content from the book
6. Schedule first weekly Zoom call

---

## Connection Map (How Everything Talks to Each Other)

```
Instagram post ("Reply VAMPIRE")
    |
    v
ManyChat (DMs them the link + captures email)
    |
    v
Kit (adds email with tag, starts nurture sequence)
    |
    +---> Free path: Detection Kit PDF delivered via Kit email
    +---> Paid path: Payhip purchase -> Kit tag -> challenge sequence
    |
    v
7-Day Challenge email sequence (Kit, automated)
    |
    v
Day 7: Skool invitation ($97/mo, VIP gets 50% off)
```

---

## Estimated Costs

| Tool | Monthly Cost |
|------|-------------|
| Kit (ConvertKit) | $0 (free up to 10K subs) |
| Payhip | $0 (5% per transaction) |
| ManyChat | $0 (free up to 1K contacts) |
| Buffer | $5/mo |
| Skool | $99/mo (David pays this to host the community) |
| **Total** | **$104/mo + 5% per Payhip sale** |

At 200 Skool members ($97/mo each), revenue = $19,400/mo. Cost = $104/mo. Margin: 99.5%.
