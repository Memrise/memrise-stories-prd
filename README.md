# **Product Requirements Document: Memrise Stories**

---

## **1\. Overview**

* **Product Name:** Memrise Stories  
* **Purpose / Goal:** Teach languages through culturally authentic short stories, replacing flashcards and grammar drills with immersive narratives rooted in real-world settings — a Mexican market, a Parisian boulangerie, a British chip shop. The product follows a structured Pre-Reading / Reading / Post-Reading methodology designed to build comprehension, vocabulary, and cultural awareness in a single sitting, as well as re-reads and extra activities to keep building comprehension over time across vocabulary, syntax, and cultural understanding.  
* **Target Users:** Language learners (beginner to advanced) who want to add reading and cultural comprehension to their language learning stack. They are motivated by cultural curiosity more than exam prep, and prefer short, satisfying 5-15 minute sessions without streak pressure.  
* **Key Value Proposition:** The same cultural world told at three difficulty levels (Beginner, Intermediate, Advanced), combined with a structured reading-and-reinforcement loop that no competitor offers. Stories feel like stories, not exercises.  
* **Primary Deployment:** Standalone web application.

---

## **2\. Features**

### Landing Page
Hero section with value proposition, cultural framing, and a "Get started" call to action.

![Landing Page](screenshots/01-landing-page.png)

### Onboarding
Guided 3-step personalisation: name, preferred reading level, and interest areas. Target language is passed from the parent app.

| Step 1: Name | Step 2: Level | Step 3: Interests |
|---|---|---|
| ![Name](screenshots/02-onboarding-step-1-name.png) | ![Level](screenshots/04-onboarding-step-3-level.png) | ![Interests](screenshots/05-onboarding-step-4-interests.png) |

### Home Screen
Main screen showing a "snapshot" of the user's reading: number of stories in progress, stories read, and total re-reads. The screen has two states: on the user's first visit it surfaces a "Start here" story; on subsequent visits it shows the story they are currently working on. Both states include a "more stories" section.

![Home Screen](screenshots/06-dashboard.png)

### Story Library
Browsable catalogue of stories grouped by cultural topic (Food & Markets, Community & Local Life, Outdoors & Encounters, Traditions & Celebrations), filtered by the user's selected language and skill level.

![Story Library](screenshots/07-story-library.png)

### Pre-Reading
Story cover image, cultural teaser, and the types of vocabulary and cultural nuggets they'll learn.

| Cover & Teaser | Theme Selection |
|---|---|
| ![Pre-Reading](screenshots/08-pre-reading.png) | ![Themes](screenshots/08b-pre-reading-themes.png) |

### First Read
Full story text presented as a clean read. On the very first read, only a small selection of words and phrases are tap-to-gloss enabled to encourage immersion. Audio playback is available at normal speed and at a slower speed (0.75x).

| Read Introduction | Story Text with Audio |
|---|---|
| ![First Read](screenshots/09-first-read.png) | ![Story Text](screenshots/09b-first-read-text.png) |

### Rate & Review / Feedback
Users rate their own comprehension on a 5-point emoji scale (Lost, Foggy, Getting there, Solid, Crystal clear) and (optionally) provide feedback via a two-question survey anchored in the top navigation bar.

| Comprehension Rating | Feedback Form |
|---|---|
| ![Rate and Review](screenshots/10-rate-and-review.png) | ![Feedback](screenshots/10b-feedback-form.png) |

### Scaffolding / Unpacking
After the first read: cultural nuggets, vocabulary highlights, phrase breakdowns, a "What Stuck" summary of memorable words, and a "What Opened Up" summary of cultural insights.

![Scaffolding](screenshots/11-scaffolding.png)

### Bilingual Re-Read
User reads the story again with side-by-side translations and tap-to-gloss fully enabled.

![Bilingual Re-Read](screenshots/12-bilingual-reread.png)

### Story Order Activity
Reorder scrambled story sentences to demonstrate narrative comprehension. Can be skipped during the first-read flow; if skipped, it is added to the Activities hub.

![Story Order](screenshots/13-story-order.png)

### Re-Rate (Self-Assessment)
User re-scores their comprehension after scaffolding (before/after comparison shown). The self-assessment also persists at the top of the Story Unit Hub, where users can re-rate themselves at any time. After completing a few activities from the hub, users are nudged to re-rate; this nudge can be muted/unmuted from Settings.

![Rate Again](screenshots/14-rate-again.png)

### Great First Read (Celebration)
Celebration screen showing growth summary, with options to pick a recommended next story, go to activities, or re-read.

![Great First Read](screenshots/15-great-first-read.png)

### Personal Notebook
A persistent reference with five tabs: Words, Phrases, Cultural insights, free-form Notes, and a guided Journal with rotating reflection prompts.

![Notebook](screenshots/16-notebook.png)

### Settings
Users can update their name, skill level, and interests at any time. Also allows users to enable/disable the self-assessment re-rate nudge, and shows their purchases (if any) and Memrise account connection status when linked.

![Settings](screenshots/17-settings.png)

### Additional Features (no screenshot captured)

| Feature | Description |
|---|---|
| **Story Unit Hub** | After completing the first-time read flow, users land on a hub for each story instead of repeating the full linear flow — they can re-read, review scaffolding, or jump into activities. |
| **Post-Reading Activities** | Sentence Building (word tiles), Vocabulary Review, and Culture Quiz activities available after the core flow. |
| **Spaced Review** | A review interface that surfaces words the learner rated "tricky" or "no idea" through Phrase Recall, Vocabulary, and Cultural Insight multiple-choice activities. Scoring at least 50% advances the story's progress state. |
| **Tap-to-Gloss Translation** | Tap any word during reading to see its translation. On the very first read, only a small selection of words and phrases are tap-to-gloss enabled to encourage immersion; tap-to-gloss is then fully enabled on all subsequent reads. |
| **Audio Narration** | Full story audio playback with a slower-speed option (0.75x). Audio is pre-recorded and hardcoded for the launch stories so it loads instantly. |
| **Story Images** | Each story ships with a hardcoded cover image (in its native ratio) and a blur placeholder that shows while the full image loads. |
| **Vocabulary Confidence Rating** | Word-level mastery tracking where learners rate each word as "got it", "tricky", or "no idea" — these ratings feed into the spaced review system. |
| **Premium / Paywall Infrastructure** | Content gating system that distinguishes free and premium stories. Currently one default story per language is free; the rest require premium status. A one-time purchase checkout flow exists. *Note: this is currently an experiment toward a longer-term monetisation system.* |
| **Logout & Data Reset** | Users can log out of their session and/or reset their personal data (progress, notebook, preferences). |

---

## **3\. User Stories**

* As a **new visitor**, I want to see a compelling landing page that explains what Memrise Stories is, so that I understand the value before signing up.  
* As a **new user**, I want to go through a quick onboarding that asks my name, level, and interests, so that the app personalises my experience from the start.  
* As a **learner**, I want to browse a library of stories grouped by topic and filtered by my language and level, so that I can choose what interests me.  
* As a **learner**, I want to read a story with a clean, distraction-free first read (no translations), so that I can test my raw comprehension.  
* As a **learner**, I want to listen to audio narration of the story, so that I can hear correct pronunciation and improve listening skills.  
* As a **learner**, I want a slow-speed audio option, so that I can follow along at a comfortable pace.  
* As a **learner**, I want to rate my own comprehension before and after scaffolding, so that I can see how much the explanations helped me understand.  
* As a **learner**, I want to explore cultural nuggets, vocabulary, and phrases after reading, so that I understand the deeper meaning of the story.  
* As a **learner**, I want to tap any word to see its translation on re-reads, so that I can build vocabulary in context.  
* As a **learner**, I want to save words, phrases, and cultural insights to my personal notebook, so that I can review them later.  
* As a **learner**, I want to practice with sentence-building, vocabulary review, and culture quiz activities, so that I reinforce what I learned.  
* As a **learner**, I want a spaced review system that surfaces my weakest words, so that I retain vocabulary over time.  
* As a **returning learner**, I want to land on a story hub (not repeat the full guided flow), so that I can choose what to revisit efficiently.  
* As a **learner**, I want to write journal reflections prompted by questions, so that I can deepen my connection to the learning.  
* As a **learner**, I want to change my level or interests in settings, so that my experience stays relevant as I grow.  
* As a **learner**, I want to log out or reset my data, so that I can start fresh or disassociate my session.

---

## **4\. Functional Requirements**

| ID | Requirement |
| ----- | ----- |
| FR-1 | The system shall require new users to complete a 3-step onboarding (name, preferred reading level, interests) before accessing stories. The target language is passed from the parent app. |
| FR-2 | The system shall support three languages: Spanish, French, and English. |
| FR-3 | The system shall offer three skill levels per story: Beginner, Intermediate, and Advanced. Each level is a different version of the same cultural setting. |
| FR-4 | The system shall present stories in a linear guided flow on first read: Pre-Reading → First Read → Rate & Review → Scaffolding → Bilingual Re-Read → Story Order → Re-Rate → Celebration. |
| FR-5 | On the first read of a story, tap-to-gloss word translation shall be limited to a small, intentionally selected set of words and phrases. It shall be fully enabled on all subsequent reads. |
| FR-6 | The system shall play full audio narration of each story at normal speed and at a slower speed (0.75x) for learners who want a gentler pace. |
| FR-7 | The system shall allow users to rate their comprehension on a 5-point emoji scale (Lost, Foggy, Getting there, Solid, Crystal clear) after reading, and again after scaffolding, producing a before/after pair. |
| FR-8 | The system shall collect feedback per story via a two-question survey anchored in the top navigation bar. |
| FR-9 | The system shall allow users to save words, phrases, cultural insights, notes, and journal entries to a persistent personal notebook. |
| FR-10 | The system shall allow users to delete individual notebook entries. |
| FR-11 | The system shall track vocabulary confidence per word with three ratings: "got it", "tricky", "no idea". |
| FR-12 | The system shall provide a spaced review mode that prioritises words rated "tricky" or "no idea" through multiple-choice activities. |
| FR-13 | Scoring at least 50% in a spaced review session shall advance the story's progress state. |
| FR-14 | The Story Unit Hub shall become active for a story once its first-read flow has been completed, replacing the linear first-read flow on all subsequent visits. |
| FR-15 | The Story Unit Hub shall allow direct navigation to: re-read, scaffolding, activities, and re-rate comprehension. If the Story Order activity was skipped during the first-read flow, it is added to the Activities hub. |
| FR-16 | The Story Library shall group stories by cultural topic and display each story's title, locale flag, content type label, and cultural hint. |
| FR-17 | The Story Library shall show a locked overlay on stories that require premium access when the user is not premium. |
| FR-18 | The system shall track per-story progress through a state machine: not\_started → started → understood → reinforced → mastered. |
| FR-19 | The system shall provide a "Story Order" activity where users reorder scrambled sentences. Users may also skip this activity. |
| FR-20 | The system shall provide four post-reading activities: Story Order, Sentence Building, Vocabulary Review, and Culture Quiz. Story Order is embedded in the first-read flow; if skipped there, it is added to the Activities hub alongside the other three. |
| FR-21 | The Home Screen shall show a snapshot of the user's reading (stories in progress, stories read, total re-reads), a "Start here" story on first visit (or the user's currently in-progress story on return visits), and a "more stories" section. |
| FR-22 | The Settings page shall allow users to update name, skill level, and interests, enable/disable the self-assessment re-rate nudge, and view their Premium status. Changes shall be saved and reflected immediately. |
| FR-23 | The Settings page shall display the user's Memrise account connection status (username, email, user ID) when a Memrise session is active. |
| FR-24 | The system shall support a one-time premium unlock purchase that grants access to all gated stories. This is currently an experiment toward a longer-term monetisation system. |
| FR-25 | After a successful premium purchase, the unlock shall take effect immediately across all open tabs without requiring a page reload. |
| FR-26 | The 10 launch stories shall ship with hardcoded images (in their respective ratios) and audio for fast loading. AI image generation is not used at launch. |
| FR-27 | Audio narration is pre-recorded and hardcoded for each story, with separate files for normal-speed and slow-speed variants. |
| FR-28 | The journal feature shall present a rotating set of 8 guided reflection prompts. Users can skip to a different prompt. |
| FR-29 | The system shall assign each user a Memrise User ID. (The previous anonymous local identity was a Replit-era artifact and no longer applies.) |
| FR-30 | The system shall provide a logout function that clears the user's session, tokens, and local state. |
| FR-31 | The system shall provide a "reset my data" function that permanently deletes a user's progress, notebook entries, vocabulary confidence ratings, and preferences, effectively returning them to a fresh state. This action shall require explicit confirmation. |

---

## **5\. Business Rules**

* **Onboarding required:** Users cannot access the Story Library or Home Screen until onboarding is complete (name and level must both be set).  
* **Name validation:** Name must be non-empty after trimming whitespace. Defaults to "Explorer" if somehow blank at onboarding completion.  
* **Language options:** Exactly three languages are supported: Spanish, French, English. Each has regional cultural variants within stories.  
* **Skill levels:** Exactly three: Beginner, Intermediate, Advanced. Every story unit must have content at all three levels.  
* **First-read restriction:** During the first read of a story, tap-to-gloss is limited to a small, intentionally selected set of words and phrases. It is fully enabled on every read thereafter.  
* **Progress state machine:** Each story has per-learner progress tracked as: not\_started → started → understood → reinforced → mastered. The transitions are triggered by specific events (story opened, post-reading core completed, spaced review success, etc.).  
* **Spaced review threshold:** A score of at least 50% in a spaced review session is required to advance the progress state.  
* **Story gating:** A set of default stories (one per language) are free. All other stories require premium status to access.  
* **Premium detection:** Premium status is determined by a flag stored locally and is set by a successful checkout purchase. (Note: Memrise Pro status from a linked Memrise account does NOT grant premium access in Stories.)  
* **Checkout return handling:** The checkout return page verifies the payment session, sets the premium flag, syncs the learner profile, and redirects the user back to the previous screen, where a "Premium celebration" popup is triggered. The tab is not closed.  
* **Currency detection:** The checkout system detects the buyer's country from request headers and maps it to a currency (currently GB → GBP, all others → USD).  
* **Feedback access:** Story feedback is collected via a short two-question survey anchored in the top navigation bar, accessible to users at any point in the app experience.  
* **Story Order idempotency:** Once Story Order is completed for a story, it is recorded permanently. Skipping is also recorded. Neither can be overwritten.  
* **First-read completion idempotency:** The "first read completed" event is recorded at most once per story per learner. A check is made before emission to prevent duplicates.  
* **Navigation guard:** During certain phases (reading, story order, bilingual re-read), a confirmation prompt warns the user before navigating away to prevent accidental loss of progress.  
* **Settings preservation:** Changing settings does not reset progress. The settings page explicitly states "Your progress is preserved."  
* **Anonymous identity:** Every user receives an anonymous UUID stored in local storage. This identity persists across sessions and is the primary key for progress, notebook, and analytics data.  
* **Interests are optional:** The interests selection step during onboarding can be skipped entirely.

---

## **6\. Domain Concepts**

* A **Learner** is anyone who uses the app. Every Learner has a Memrise account ID associated with their profile.  
* A **Learner** has **Preferences**: a display name, a selected language, a skill level, and a list of interests.  
* A **Language** is one of the three supported options: Spanish, French, English. Each Language contains stories with different regional cultural **Locales** (e.g., Mexican Spanish, Castilian Spanish, British English, American English).  
* A **Story** is a piece of narrative content set in a specific cultural context. Each Story exists at three **Skill Levels** (Beginner, Intermediate, Advanced), meaning there are three written versions of the same cultural setting with varying complexity.  
* Stories are organised into **Topics** (Food & Markets, Community & Local Life, Outdoors & Encounters, Traditions & Celebrations).  
* A **Story** contains:  
  * a title  
  * cultural hint  
  * teaser  
  * full text  
  * full translations  
  * key phrases  
  * vocabulary callouts  
  * word details  
  * comprehension anchors  
  * cultural insights  
  * theme options  
  * matching phrases  
* A **Story** has **Audio** (normal speed and slow speed) and a **Cover Image** (with a blur placeholder).  
* A Learner's relationship with a Story is tracked through **Unit Progress**, which follows a defined state sequence: not started → started → understood → reinforced → mastered.  
* A Learner works through a Story via a **Reading Session**, which is a multi-phase guided flow (Pre-Reading → Reading → Rating → Scaffolding → Activities → Completion).  
* During a Reading Session, a Learner produces **Self-Assessment Scores** — a before/after pair measuring their perceived comprehension.  
* A Learner can provide **Story Feedback** via a short two-question survey accessible from the top navigation bar.  
* A Learner has a **Notebook** that holds five types of entries: Words, Phrases, Cultural insights, Notes, and Journal reflections. Notebook entries can be linked to a specific Story.  
* A Learner rates individual words with a **Vocabulary Confidence** rating: "got it", "tricky", or "no idea". These ratings feed into the Spaced Review system.  
* A **Spaced Review** session draws on a Learner's weakest vocabulary (words rated "tricky" or "no idea") and presents them in multiple-choice activities.  
* A Learner can have **Premium** status, which unlocks access to all gated Stories. Premium is granted only by a purchase.

---

## **7\. User Flows**

### **7.1 First-Time User Flow**

1. User arrives at the landing page, sees the hero section and value cards
   ![Landing Page](screenshots/01-landing-page.png)

2. User clicks "Get started"

3. Onboarding Step 1: User enters their name
   ![Onboarding - Name](screenshots/02-onboarding-step-1-name.png)

4. Onboarding Step 2: User selects their preferred reading level
   ![Onboarding - Level](screenshots/04-onboarding-step-3-level.png)

5. Onboarding Step 3: User picks interests (or skips)
   ![Onboarding - Interests](screenshots/05-onboarding-step-4-interests.png)

6. User is redirected to the Home Screen
   ![Home Screen](screenshots/06-dashboard.png)

### **7.2 First-Time Story Reading Flow**

1. User is pointed to the free story they can start with from the Home Screen or Library

2. **Pre-Reading:** User sees the story cover image, cultural teaser, and the types of vocabulary and cultural nuggets they'll learn
   ![Pre-Reading](screenshots/08-pre-reading.png)

3. **First Read:** User reads the full story text (only selected tap-to-gloss). Audio playback is available at normal speed and at a slower speed.
   ![First Read](screenshots/09b-first-read-text.png)

4. **Rate & Review:** User rates their comprehension and (optionally) provides feedback via the two-question survey
   ![Rate & Review](screenshots/10-rate-and-review.png)

5. **Scaffolding:** User explores vocabulary, slang, and cultural nuggets, plus "What Stuck" and "What Opened Up" summaries.
   ![Scaffolding](screenshots/11-scaffolding.png)

6. **Bilingual Re-Read:** User reads the story again with side-by-side translations and tap-to-gloss enabled
   ![Bilingual Re-Read](screenshots/12-bilingual-reread.png)

7. **Story Order:** User reorders scrambled sentences (or skips)
   ![Story Order](screenshots/13-story-order.png)

8. **Re-Rate:** User re-scores their comprehension (before/after comparison shown)
   ![Rate Again](screenshots/14-rate-again.png)

9. **Great First Read:** Celebration screen showing growth summary, with options to pick a recommended next story, go to activities, or re-read
   ![Great First Read](screenshots/15-great-first-read.png)

### **7.3 Return-Visit Story Flow**

1. User selects a previously-read story  
2. User lands on the Story Unit Hub  
3. User chooses from: Re-read the story, Review scaffolding, Jump into activities, or Update their comprehension rating  
4. User completes their chosen activity and returns to the hub

### **7.4 Post-Reading Activities Flow**

1. User enters the Activities tab (from the Great First Read screen or the Story Unit Hub)  
2. User sees available activities: Sentence Building, Vocabulary Review, Culture Quiz  
3. User completes activities (progress tracked per activity)  
4. After completing activities, user reaches the Completion screen with a growth summary and recommendation to re-read the story or pick another one

### **7.5 Spaced Review Flow**

1. Vocab review activity card on Story Unit Hub signals words due for review  
2. User selects vocab review activity  
3. System presents flashcards quiz focused on the user's weakest words  
4. If user scores at least 50%, the story's progress state advances

### **7.6 Notebook Usage Flow**

1. While reading or exploring scaffolding, user saves words, phrases, or cultural insights
2. User navigates to the Notebook page
   ![Notebook](screenshots/16-notebook.png)
3. User browses saved items across tabs (Words, Phrases, Cultural, Notes, Journal)
4. User can add saved items to activities (words to vocab review, cultural notes to culture quiz)
5. User can write free-form notes or journal reflections using guided prompts
6. User can delete individual entries

### **7.7 Premium Unlock Flow**

1. User taps on a locked story  
2. Pre-reading screen loads, then a paywall overlay appears  
3. User proceeds to checkout  
4. User completes payment  
5. Return page verifies the session and sets premium status  
6. Premium unlocks across all open tabs immediately  
7. User is redirected back to the Library

### **7.8 Settings Update Flow**

1. User navigates to Settings
   ![Settings](screenshots/17-settings.png)
2. User modifies name, level, or interests via collapsible sections
3. User clicks "Save changes" (disabled until there are actual changes)
4. Preferences are saved, learner profile is synced, and user is redirected to the Stories page

---

## **8\. Edge Cases**

* **No saved preferences:** If a user navigates directly to the Library, Dashboard, Notebook, Settings, or Stories pages without completing onboarding, they are redirected to the home page.  
* **Missing anonymous ID:** If the anonymous analytics ID is missing from local storage, all progress, notebook, and review operations degrade gracefully (return empty data, skip writes) without crashing.  
* **Missing Memrise token:** If the user is not linked to a Memrise account, the Settings page shows "Not connected" and all Memrise-specific data is simply hidden.  
* **Memrise API failure:** If the Memrise profile fetch fails, the Settings page shows an "Error" status badge. The rest of the app continues to function normally.  
* **Story data not found:** If a user tries to load a story that does not exist for their language/level combination, the story selection is silently ignored and the user stays on the current screen.  
* **Legacy language codes:** If a user's saved preferences contain old language codes, the system automatically migrates them to current codes on load.  
* **Progress state unknown on error:** If the system cannot determine a story's progress state (API failure), it defaults to treating the story as already read (read count \= 1, first read completed \= true) so the user gets the return-visit experience with full features enabled.  
* **Checkout cancellation:** If the user cancels checkout, the return page tracks the cancellation event, shows a message, and either closes the popup tab or redirects back to the Library.  
* **Payment verification failure:** If the checkout verification API fails, the return page tracks the failure, shows a message, and redirects the user back without granting premium.  
* **Duplicate first-read completion:** The system checks whether "first read completed" has already been recorded before emitting the event, preventing double-counting.  
* **Navigation during active phases:** During reading, story order, and bilingual re-read phases, a navigation guard prompts the user to confirm before leaving, preventing accidental progress loss.  
* **Empty notebook tabs:** Each tab shows a contextual empty state with guidance on how to populate it (e.g., "Save vocabulary while reading stories\!").  
* **Empty story library for a language:** If no stories exist for a selected language variant, the library shows a "Stories coming soon" placeholder.  
* **Concurrent tab premium unlock:** When premium is granted in a checkout popup tab, a storage event fires so other open tabs of the app detect the change and re-render unlocked content without a page reload.  
* **Handshake timeout:** If the Memrise iframe/popup handshake does not receive a response after 10 retries (30 seconds), the system stops retrying and continues in anonymous mode, emitting a diagnostic event.  
* **Stripe not configured:** If the Stripe secret key is missing or malformed, the system raises a clear configuration error rather than failing silently. The paywall UI should handle this gracefully.  
* **Logout with unsaved changes:** If a user triggers logout while in the middle of a reading session or activity, the navigation guard should prompt for confirmation before clearing the session.  
* **Data reset confirmation:** Resetting all user data is destructive and irreversible. The system must require explicit confirmation (e.g., a confirmation dialog with a warning) before proceeding.

---

## **9\. Non-Functional Requirements**

### **Performance**

* Audio and images for the launch stories are hardcoded and pre-loaded so they are available instantly.  
* Story images use blur placeholders for perceived instant loading.

### **Security**

* Memrise access tokens are stored in sessionStorage (not localStorage), limiting their lifetime to the browser tab.  
* The API proxy requires a Bearer token for all Memrise API calls.  
* Anonymous user IDs are non-reversible UUIDs with no personally identifiable information.  
* Checkout sessions are verified server-side before granting premium access.  
* Country override headers for currency testing are only honoured in non-production environments.

### **Scalability**

* The content architecture supports unlimited story additions without structural changes.  
* The language system can be extended to new languages by adding content files — no architecture changes needed.  
* All user data is keyed by anonymous UUID, supporting horizontal user growth.

### **Reliability**

* All progress, notebook, and review operations fail gracefully with fallback behaviour rather than crashing.  
* The Memrise postMessage handshake retries up to 10 times over 30 seconds before giving up.  
* The premium unlock propagates across all open tabs via storage events, ensuring consistency.  
* The checkout return page handles all failure modes (verification failure, network error, missing session ID) with clear user messaging and automatic redirect.

### **Accessibility**

* Focus management with custom focus-visible styles.  
* ARIA attributes on collapsible sections (aria-expanded, aria-controls, role="region").  
* Typography enforces 70-character line length limits for readability.  
* RTL (right-to-left) language support is built into the styling system for Arabic, Hebrew, and Farsi markets.

---

## **10\. Assumptions and Unknowns**

### **Assumptions**

* Users must have a Memrise account and be logged in to use the app.  
* Three languages (Spanish, French, English) are sufficient for the initial launch.  
* The deployment model is a standalone web application.  
* The current $0.99 one-time premium unlock is a placeholder. The long-term monetisation model is not yet decided and may change.  
* All story content is hand-authored at three skill levels. The content creation pipeline is outside the scope of this PRD.  
* Eight journal prompts provide sufficient variety for the reflection feature.  
* Language selection/switching is part of the existing prototype but is out of scope for the core product — users will have their language pre-determined.  
* The analytics dashboard is internal tooling and out of scope for product requirements.  
* There is no streak, daily goal, or guilt-driven re-engagement system by design. However, lighter re-engagement mechanisms (nudges, recommendations) are expected to be layered in over time.

### **Unknowns**

* **Spaced repetition algorithm:** The current spaced review system prioritises weak words but has no forgetting-curve algorithm. A full SRS iteration is planned for a future version but the timeline and design are undefined.  
* **Story generation feature:** A "Generate a new story" card appears in the Library as "Coming Soon." The scope and feasibility of AI-generated or user-generated stories are unknown.  
* **Re-engagement mechanisms:** While the app deliberately avoids streaks and pressure, lighter re-engagement features (email summaries, return nudges, recommended stories) are expected to be added. Their design is undefined.  
* **Multi-device sync:** Progress is stored server-side (by anonymous UUID), but it is unclear how a user would access their progress from a different device without explicit account creation.  
* **Long-term monetisation:** The current one-time purchase is a prototype placeholder. Whether the product will use its own subscription, integrate with Memrise Pro, or adopt another model is undecided.  
* **Story recommendation logic:** The recommendation engine exists but its algorithm and criteria are not documented from a product perspective.  
* **Logout and data reset implementation:** The PRD now requires these features (FR-30, FR-31), but they do not exist in the current prototype and will need to be built.

