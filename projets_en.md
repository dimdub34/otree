# Behavioral Economics with oTree

**General Instructions**

Choose one project from the list below. You have **2 weeks** to develop it in a team of 2-3 people.

**Each project must include:**

1. **A functional oTree implementation:** The app must run without errors and include randomized treatments.
2. **Data Simulation:** A comprehensive `tests.py` file to simulate user behavior (bots) and verify data integrity.
3. **Data Analysis:** A simple analysis of the simulated data (using R or Python).
4. **Oral Presentation:** A 15-20 minute pitch and demo.

**Presentation Structure:**

* **Pitch (5 min):** Context, client's problem, behavioral hypothesis, and proposed solution.
* **Demo (10 min):** Live demonstration of the oTree experiment (involving the class via smartphones/PCs).
* **Analysis (5 min):** Basic visualization of simulated results and expected outcomes.

---

## Project 1: The Power of Scarcity (E-commerce)

**Context:**
An e-commerce website wants to investigate how scarcity cues influence consumer behavior. They suspect that highlighting limited availability or high demand increases the likelihood of purchase.

**Research Question:**
Does the type of scarcity message (quantitative vs. social) affect the click-through rate (CTR) or purchase probability?

**Experimental Design:**
Create a product selection task where participants view items under different conditions:

* **Treatment A (Control):** Neutral product display (no messages).
* **Treatment B (Quantitative Scarcity):** Message indicating low stock (e.g., "Only 2 items left!").
* **Treatment C (Social Scarcity):** Message indicating high interest (e.g., "10 people are viewing this item right now").

**Deliverables:**

* oTree app with randomized treatment assignment at the `player` or `group` level.
* Participant instructions page.
* Analysis of click rates/purchases across the three conditions.

---

## Project 2: Framing Effects on Subscriptions (Behavioral Strategy)

**Context:**
A streaming platform wants to optimize its subscription page. They need to understand how the presentation of pricing options (framing) alters user choices between monthly and yearly plans.

**Research Question:**
How does framing the cost (e.g., emphasizing savings vs. flexibility) impact the uptake of long-term subscriptions?

**Experimental Design:**
Design a subscription choice interface with randomized framing:

* **Treatment A (Baseline):** Standard presentation (e.g., "$10/month" vs. "$100/year").
* **Treatment B (Loss Aversion/Gain):** Emphasize savings (e.g., "Yearly plan: Get 2 months free").
* **Treatment C (Flexibility):** Emphasize freedom (e.g., "Monthly plan: Cancel anytime, total flexibility").

**Deliverables:**

* oTree app collecting the user's choice and a short follow-up on their reasoning.
* Randomization mechanism.
* Report comparing the proportion of "Yearly" subscriptions across treatments.

---

## Project 3: Social vs. Algorithmic Recommendations (Digital Marketing)

**Context:**
An online clothing retailer is debating its recommendation strategy. They want to know if customers trust peer choices (social proof) more than algorithmic curation.

**Research Question:**
Do users prefer products recommended by "other customers" or products "selected for them" by an algorithm?

**Experimental Design:**
Create a simulated shopping environment where products are highlighted based on the condition:

* **Treatment A (Social):** Recommendations labeled as "Most purchased by others."
* **Treatment B (Algorithmic):** Recommendations labeled as "Selected for you by our AI."

**Deliverables:**

* Fictional product selection interface.
* Click-stream data collection.
* Behavioral analysis comparing the click-through rate of recommended items in both conditions.

---

## Project 4: The Influencer Trust Test (Brand Management)

**Context:**
A brand wants to measure the "Influencer Effect." They need to determine if a product is perceived more favorably when endorsed by a social media personality compared to a standard neutral presentation.

**Research Question:**
Does an influencer endorsement significantly increase trust or purchase intention compared to a neutral product description?

**Experimental Design:**
Participants view a product profile under one of two conditions:

* **Treatment A (Neutral):** Standard technical datasheet and product photo.
* **Treatment B (Influencer):** An Instagram-style post featuring an influencer with a photo and a descriptive caption.

**Deliverables:**

* Randomization between conditions.
* Measurement of "Trust Score" (Likert scale) or "Willingness to Buy" (0-100 slider).
* Comparative analysis of the scores.

---

## Project 5: The Decoy Effect (Pricing Strategy)

**Context:**
An online retailer wants to nudge users toward their Premium (higher margin) product. They are considering introducing a "decoy" option to make the Premium option look more attractive.

**Research Question:**
Does the introduction of an irrelevant "decoy" option (asymmetrically dominated) increase the share of participants choosing the Premium option?

**Experimental Design:**

* **Treatment A (No Decoy):** Choice between **Basic** ($10) and **Premium** ($30).
* **Treatment B (With Decoy):** Choice between **Basic** ($10), **Premium** ($30), and **Decoy** ($35, or $30 with fewer features) — *The decoy is clearly worse than the Premium option.*

**Deliverables:**

* oTree implementation of the choice task.
* Data collection of the chosen product.
* Analysis of the shift in "Premium" market share between Treatment A and B.

---

## Project 6: The "Green Nudge" (CSR / Marketing)

**Context:**
An online supermarket aims to reduce plastic waste. They want to encourage customers to buy bulk products (packaging-free) instead of pre-packaged goods using behavioral nudges.

**Research Question:**
Is social pressure (Social Norm) or environmental impact information (Ecological signaling) more effective in promoting bulk purchases?

**Experimental Design:**
Participants have a budget of €20 to spend in a simulated store.

* **Treatment A (Control):** Neutral display.
* **Treatment B (Social Norm):** Bulk products display a badge: "80% of our customers choose this product."
* **Treatment C (Impact):** Bulk products display a badge: "Save 50g of plastic by choosing this."

**Deliverables:**

* A shopping list task implementation.
* Calculation of the percentage of "bulk" items in the final basket.
* Analysis comparing the effectiveness of the two nudges against the control.

---

## Project 7: Incentives and Productivity (Labor Economics)

**Context:**
A gig-economy food delivery platform wants to increase courier activity during peak hours. They are hesitating between a guaranteed fixed bonus and a lottery-based bonus.

**Research Question:**
Which incentive scheme generates higher effort (productivity): a small fixed piece-rate or a probabilistic large reward (with the same expected value)?

**Experimental Design:**
Implement a **Real Effort Task** (e.g., counting zeros in a matrix, decoding text) lasting exactly 2 minutes (`timeout_seconds`).

* **Treatment A (Fixed):** "You earn €0.50 per correctly solved task."
* **Treatment B (Lottery):** "Every correctly solved task gives you a 1 in 10 chance to win €5.00."

**Deliverables:**

* Real Effort Task logic (looping pages until timeout).
* Payoff calculation logic based on the treatment.
* Analysis of effort (number of tasks attempted/solved) and risk preferences.

---

## Project 8: Dishonesty and Declarations (Insurance / Ethics)

**Context:**
A car insurance company is losing money due to inflated claims. They want to test if the *timing* of an honesty pledge (signature) affects the magnitude of fraud.

**Research Question:**
Does signing an honesty pledge *before* reporting a claim reduce dishonesty more than signing it *after*?

**Experimental Design:**
Adapt the standard **"Die-roll task"**: Participants roll a die (physically or virtually) and report the result. Higher numbers equal higher payoffs.

* **Treatment A (Post-signature):** Participant enters the result, then signs a statement at the bottom ("I certify this is accurate...").
* **Treatment B (Pre-signature/Priming):** Participant must sign the honesty pledge *before* the input field for the result appears.

**Deliverables:**

* Implementation of the reporting interface.
* Comparison of the distribution of reported numbers against the statistical probability (uniform distribution).
* Analysis of "cheating magnitude" between conditions.

