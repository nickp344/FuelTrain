# FuelTrain — Product Requirements Document

**Version:** 0.1  
**Status:** Draft for feedback  
**Product:** FuelTrain  
**Purpose:** Help people match everyday eating and hydration to their training and recovery.

## 1. Product overview

FuelTrain brings a person’s training plan, food log, activity, hydration and sleep context into one place. It turns that information into practical, flexible fueling guidance for the day, including training, strength and rest days.

The current prototype is a single-page interactive concept with sample data. Food, water and profile edits are stored in the browser. The connected-app buttons are previews; real account linking, syncing and persistent user accounts are not yet implemented.

## 2. Problem

People who train often track workouts, calories, meals and sleep in separate tools. It can be hard to understand how much to eat on a given day, how a session changes fueling needs, or whether intake is keeping up with training. Generic calorie targets can also be misleading when presented without context or certainty.

FuelTrain should make the day’s guidance easy to understand while keeping it flexible, transparent and safe.

## 3. Target users

- People following a structured training plan, including endurance and mixed run/strength plans.
- Recreational athletes who want a clearer view of food intake alongside training and recovery.
- Users who already track meals, activity, hydration or sleep in other apps and want those signals considered together.

The first version is for adults. It is not intended to diagnose or treat a medical condition or replace advice from a qualified health professional.

## 4. Product goals

1. Make a useful daily fueling guide the clearest element on the Today screen.
2. Explain how training and logged food affect the day’s estimated energy needs and remaining amount.
3. Show protein, carbohydrate and fibre totals in the food log, as well as calories.
4. Give context-specific suggestions for endurance training, weight training and rest days.
5. Let users connect or bring together training plans, food/calorie trackers, activity devices, sleep and other tracked data.
6. Explain RED-S and provide careful prompts when patterns or symptoms may warrant professional support, without presenting the app as a diagnostic tool.

## 5. Non-goals for the first release

- Diagnosing RED-S, low energy availability, eating disorders or other health conditions.
- Prescribing a weight-loss or body-composition plan.
- Replacing a sports dietitian, physician or other clinician.
- Claiming that a single low-intake day establishes health risk.
- Building a full training-plan authoring or workout-recording platform.
- Promising live integrations before partner access, permissions and data handling are in place.

## 6. Core user journeys

### A. Understand today’s fueling guide

1. User opens Today and sees calories eaten, the estimated daily guide, the remaining amount and a progress indicator.
2. The app explains the estimate as a usual daily baseline plus activity calories, and notes that estimates can be inaccurate.
3. User can review or adjust the baseline and activity estimate.

### B. Log food and review nutrients

1. User logs a meal or snack with calories and optional protein, carbohydrate and fibre amounts.
2. The food log shows the nutrients for each entry and updates daily totals.
3. The daily calorie guide and macro summaries update when food is logged or edited.

### C. Plan around a session or rest day

1. User sees the week’s sessions, including runs, weight training and rest days.
2. User selects a session to open its details and general fueling or mobility suggestions.
3. Rest-day guidance reinforces recovery and regular eating without implying that food must be earned through exercise.

### D. Review RED-S information

1. User sees a careful note that one low-intake day does not mean they have RED-S.
2. User can open a plain-language explanation of RED-S and learn when to speak with a GP or sports dietitian.
3. The app never labels the user as having RED-S based only on calorie data.

### E. Connect tracked data

1. User chooses a category such as training plan, activity tracker, food tracker, sleep tracker, hydration or another data source.
2. The first release supports only integrations that have actually been built and authorized; unsupported sources are clearly labelled as unavailable or preview-only.

## 7. Functional requirements

### 7.1 Today dashboard

- Display the daily calorie guide prominently.
- Show calories consumed so far, estimated target, amount remaining or amount over, and a progress bar.
- Show the basis for the estimate and allow the user to edit the baseline and activity calories.
- Reflect the day’s planned training when calculating or presenting guidance.
- Display concise fueling timeline suggestions around the session.
- Include hydration and sleep/recovery context when available.
- Indicate when data is sample, manually entered, estimated or synced.

### 7.2 Food and nutrient tracking

- Allow users to add and edit meal/snack name, calories, protein, carbohydrates and fibre.
- Nutrient values are optional when the source does not provide them.
- Display per-entry nutrients and daily totals for calories, protein, carbohydrates and fibre.
- Update summaries immediately after a food entry is added or edited.
- Clearly distinguish missing nutrient values from zero values.
- Do not imply that macro targets are clinically personalized unless they are based on an approved, transparent method.

### 7.3 Energy guidance

- Present the estimate as guidance, not a precise prescription.
- Clearly show the estimate’s inputs and uncertainty.
- Avoid encouraging users to compensate for food intake with exercise or to “make up” calories on rest days.
- Support different activity levels and days, including rest days.
- Include a route to hide or reduce calorie emphasis if user testing or safety review identifies a need.

### 7.4 Training and recovery

- Show a weekly plan containing endurance sessions, weight training and rest days.
- Make session rows selectable by mouse, keyboard and touch.
- Provide concise, general pre-session, post-session, strength-session and rest-day suggestions.
- Allow training plan data to come from a connected source or manual entry.
- Keep mobility suggestions optional and include a reminder to stop if something hurts.

### 7.5 Connections and data import

- Support connections for training plans, activity/wearables, food/calorie trackers, sleep/recovery and hydration, plus a pathway for other sources.
- Show connection status, last sync and source attribution for imported data.
- Let users disconnect a source and understand what data will be removed or retained.
- Do not display a “connected” state as if live data were syncing when the action is only a prototype preview.

### 7.6 RED-S information and safety messaging

- Define RED-S as Relative Energy Deficiency in Sport and explain that it can arise when sustained inadequate energy intake does not support both exercise and the body’s everyday needs.
- Explain that it can affect health, recovery and performance over time.
- State that there is no single calorie threshold in the app that can diagnose RED-S.
- Describe app prompts as signals to seek support, not as a risk score or diagnosis.
- Encourage consultation with a GP or sports dietitian for persistent under-fueling concerns or ongoing symptoms.
- Avoid alarmist language and avoid determining risk from a single day of food logging.

### 7.7 Editing and personalization

- Make major profile, plan, session, food and hydration details editable where appropriate.
- Identify which values are user-entered, estimated, imported or sample data.
- Persist user edits across sessions in the production release, with a way to correct or remove them.

## 8. Safety, privacy and trust

- Calorie and nutrient estimates are informational and can be inaccurate.
- RED-S content must be reviewed by qualified sports-medicine or sports-nutrition professionals before public launch.
- Avoid using calorie shortfalls alone to trigger definitive risk labels.
- Use privacy-by-design for health and activity data: collect only what is needed, request clear consent, explain use and retention, and provide deletion controls.
- Protect connected account credentials through the integration provider; do not store third-party passwords in FuelTrain.
- Make sample/demo data obvious so it cannot be mistaken for a user’s actual health data.
- Consider eating-disorder and body-image risks in copy, defaults and onboarding; test with appropriate users and advisors.

## 9. Success measures

Initial research and beta measures:

- Users can explain what the daily calorie guide represents after viewing it.
- Users can log food and correctly interpret the calorie and nutrient totals.
- Users understand that the RED-S explainer is educational and not diagnostic.
- Users can identify whether an item is synced, manually entered, estimated or sample data.
- Users report that the guidance is useful without feeling pressured to hit an exact number.
- Reliability of food, nutrient, training and sync data, including visible handling of missing or stale information.

Avoid optimizing solely for calorie logging frequency or time spent in the app.

## 10. MVP scope and release sequence

### Prototype (current)

- Interactive Today, Training, Food & hydration, and Connected apps screens.
- Sample training week with endurance, weight training and rest days.
- Estimated daily calorie guide and manually adjustable baseline/activity calories.
- Food logging with calories and optional protein, carbohydrate and fibre.
- Browser-local persistence and editable sample content.
- RED-S explainer and cautious fueling check copy.
- Connection preview buttons; no live integrations.

### MVP (next)

1. Replace sample profile and browser-only data with secure user accounts and persistent storage.
2. Implement one real training-plan or activity integration and one food-tracker integration, selected after user research.
3. Add sync status, permissions, source attribution, disconnect and data-deletion flows.
4. Review energy guidance and RED-S content with qualified experts.
5. Conduct accessibility, privacy, usability and safety testing before wider release.

## 11. Open questions

- Which user group should the first release prioritize: runners, multi-sport athletes, gym users, or a narrower cohort?
- Which training and food-tracking integrations are most important to initial testers?
- Should the daily guide be calorie-first, or should the user be able to choose a non-calorie view?
- What personalization inputs are appropriate and safe for the first release, and which require professional oversight?
- What age range and regions will the product support at launch?
- What expert review and user research are required before RED-S prompts are made actionable?

## 12. References for RED-S content

- International Olympic Committee consensus statement on Relative Energy Deficiency in Sport: https://bjsm.bmj.com/content/bjsports/57/17/1073
- Australian Institute of Sport, Energy Availability: https://www.ausport.gov.au/ais/nutrition/energy-availability
