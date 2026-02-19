# FlashOne.AI — QA Test Plan

## Overview
This test plan covers systematic QA testing of FlashOne.AI across web (primary), with notes for iOS and Android when access is available. Tests are organized into profiles that can be run independently or combined.

**Test Account:** proflashone@gmail.com  
**Web App:** https://app.flashone.ai/app/  
**Funnel:** https://get.flashone.ai  
**Marketing Site:** https://flashone.ai  

---

## Test Profiles

### 🔴 P1 — Smoke Test (5-10 min)
Quick sanity check after any deployment. Hit the critical paths.

- [ ] App loads without errors
- [ ] Login via Google works
- [ ] All 5 bottom nav tabs load (Home, Calendar, Notes+, Flashcards, New)
- [ ] Can create a new data item (text input)
- [ ] Can generate flashcards from data
- [ ] Can open and study a deck
- [ ] Can navigate back to Home
- [ ] No console errors (critical)
- [ ] Beta features toggle on/off works

### 🟡 P2 — Comprehensive Test (30-60 min)
Full walkthrough of all features. Run after significant updates.

#### Authentication & Onboarding
- [ ] Google Sign-In
- [ ] Apple Sign-In (iOS only)
- [ ] Sign out and re-login
- [ ] Session persistence (refresh page, still logged in?)
- [ ] New user onboarding flow (funnel at get.flashone.ai)
- [ ] "Register Instead" flow from login modal

#### Home Dashboard
- [ ] Beta Features toggle (on/off, UI updates correctly)
- [ ] AI Coach PRO button (opens, functions)
- [ ] Transcribe PRO button (opens, functions)
- [ ] Translate PRO button (opens, functions)
- [ ] AI Top-Up button (opens purchase flow)
- [ ] Timed Learning / Pomodoro
  - [ ] Start session
  - [ ] Complete a session
  - [ ] Settings (session count, duration)
  - [ ] Streak tracking
- [ ] Mastery Progress display
- [ ] Study mode buttons (Mastery, SRS, CBR Mode)
- [ ] Reminders section
  - [ ] Create reminder
  - [ ] Mark all read
  - [ ] Clear all
  - [ ] Notification settings
  - [ ] Calendar button (beta)
- [ ] Tutorial Progress
  - [ ] Each tutorial step clickable
  - [ ] Token reward works
  - [ ] Pagination (Page 1-4)
- [ ] Notification bell (top right)
- [ ] Menu (three dots, top right)

#### Calendar / Plan (Beta)
- [ ] Roadmap sub-tab loads
- [ ] Calendar sub-tab loads
- [ ] View modes: Auto, Day, 5-Day, Week, Schedule List
- [ ] Print weekly calendar
- [ ] Filter toggles: Learning Blocks, Reminders, Events, Goals, Habits
- [ ] Navigate forward/back weeks
- [ ] Today button
- [ ] Date picker
- [ ] Add new item via FAB (+)
- [ ] Edit/delete existing calendar items
- [ ] Learning Block display and interaction

#### Notes+ — Data Tab
- [ ] Empty state displays correctly
- [ ] Add data item — Text/Prompt
- [ ] Add data item — PDF upload
- [ ] Add data item — DOCX upload
- [ ] Add data item — YouTube URL
- [ ] Add data item — Audio/Video file (transcription)
- [ ] Add data item — Image
- [ ] Data item list/grid view
- [ ] Select data items
- [ ] Delete data items
- [ ] Edit data items
- [ ] Search/filter data items

#### Notes+ — Notes Tab
- [ ] Empty state with "Go to Data Tab" CTA
- [ ] Generate notes from data items
- [ ] View generated notes
- [ ] Edit notes
- [ ] Delete notes
- [ ] Notes formatting and readability

#### Notes+ — Images Tab
- [ ] Image gallery display
- [ ] AI image generation (if applicable)
- [ ] Image management

#### Flashcards — Deck View
- [ ] Deck list displays correctly
- [ ] Deck cards show title, description, card count
- [ ] Deck backgrounds/themes render
- [ ] Create new deck (manual)
- [ ] Create deck via AI generation
- [ ] Open a deck
  - [ ] View all cards in deck
  - [ ] Flip cards
  - [ ] Edit cards
  - [ ] Delete cards
  - [ ] Add cards to existing deck
- [ ] Study a deck
  - [ ] Mastery mode
  - [ ] SRS mode
  - [ ] CBR mode
- [ ] Deck menu (three dots)
  - [ ] Share deck
  - [ ] Print to PDF
  - [ ] Delete deck
  - [ ] Edit deck info
- [ ] Expand/collapse deck (arrow button)

#### Flashcards — Mind Map View
- [ ] Mind map renders
- [ ] Nodes display correctly
- [ ] Navigation/zoom works
- [ ] Interaction with nodes

#### New / Shared Decks
- [ ] All Public Decks loads and displays
- [ ] Premium decks section
- [ ] My Decks section
- [ ] Shared With Me section
- [ ] Search functionality
- [ ] Category filter
- [ ] My Labels filter
- [ ] Top Creators filter
- [ ] Download a shared deck
- [ ] Rate a deck
- [ ] View creator profile
- [ ] Share a deck (from My Decks)

#### AI Features
- [ ] AI flashcard generation from text
- [ ] AI flashcard generation from PDF
- [ ] AI flashcard generation from DOCX
- [ ] AI flashcard generation from YouTube URL
- [ ] AI note generation
- [ ] AI Coach conversation
- [ ] AI Transcribe (record audio → text)
- [ ] AI Translate
- [ ] AI image generation
- [ ] Token usage tracking
- [ ] Token limit enforcement
- [ ] Model selection (if exposed to user)

#### Account & Settings
- [ ] Profile/account page
- [ ] Subscription status display
- [ ] Token balance display
- [ ] Language settings
- [ ] Notification preferences
- [ ] Theme (dark/light if available)
- [ ] Delete account flow
- [ ] Sign out

### 🟢 P3 — Feature-Specific Test
Run when Sunny flags a specific feature update. Pick the relevant section from P2 and test deeply.

**Template for feature-specific testing:**
1. Test the happy path (feature works as expected)
2. Test edge cases (empty inputs, very long inputs, special characters, unicode/emoji)
3. Test error handling (network off, invalid data, rate limits)
4. Test state persistence (does it survive a page refresh?)
5. Test across the flow (does this feature impact other features?)

### 🔵 P4 — Regression Test (15-20 min)
After bug fixes. Verify the fix AND check nothing else broke.

- [ ] Reproduce the original bug (confirm it's fixed)
- [ ] Test adjacent features that could be affected
- [ ] Run P1 Smoke Test
- [ ] Check for new console errors

### 🟣 P5 — UX / Polish Test
Focused on user experience, visual quality, and demo-readiness.

- [ ] All text is readable (no truncation, no overflow)
- [ ] Buttons are tappable/clickable (proper hit targets)
- [ ] Loading states show spinners/skeletons (no blank screens)
- [ ] Error states have helpful messages
- [ ] Empty states have clear CTAs
- [ ] Animations are smooth (no jank)
- [ ] Color contrast is adequate
- [ ] Consistent spacing and alignment
- [ ] No placeholder text or "Lorem ipsum" in production
- [ ] All images load (no broken images)
- [ ] Responsive layout at different widths
- [ ] Dark mode consistency

### 🟤 P6 — Funnel / Conversion Test
Testing the get.flashone.ai onboarding funnel.

- [ ] Funnel loads
- [ ] Step 1: "What do you want to learn?" — all options clickable
- [ ] Step 2: "What's your biggest study challenge?" — all options clickable
- [ ] Step 3: "How do you prefer to study?" — all options clickable
- [ ] Step 4: "How soon do you want to see results?" — all options clickable
- [ ] Back button works on each step
- [ ] Progress bar updates correctly
- [ ] Pricing page loads after funnel
- [ ] Monthly/Annual toggle works
- [ ] Premium plan details display
- [ ] Pro plan details display
- [ ] "Start 7-Day Free Trial" buttons work
- [ ] "Just want to try it free first?" link works
- [ ] "Download Mobile App" button works
- [ ] Stripe checkout loads (don't complete purchase)

### ⚫ P7 — Marketing Site Test
Testing flashone.ai

- [ ] Homepage loads
- [ ] Navigation links work (Features, Pricing, About Us)
- [ ] Web Login dropdown → Web Login, Top Up Credits, Public Decks
- [ ] "Start Free Now" → get.flashone.ai funnel
- [ ] "See How It Works" → scrolls to features
- [ ] Phone screenshots display
- [ ] "Available on All Your Devices" section
- [ ] Feature cards display
- [ ] Testimonials display
- [ ] Footer links work (Home, Pricing, About Us, Privacy Policy, Terms, Delete Account, Contact Us)
- [ ] Language switcher
- [ ] Dark/light mode toggle
- [ ] Mobile responsive

---

## Localization Testing
FlashOne supports 4 localized languages + 26 pending.

- [ ] Language switch works
- [ ] All UI strings translate (no untranslated keys showing)
- [ ] RTL languages display correctly (if applicable)
- [ ] Date/time formats localize
- [ ] Currency formats localize (pricing)

---

## Bug Report Template

```markdown
### Bug: [Short description]
**Severity:** Critical / High / Medium / Low  
**Test Profile:** P1-P7  
**Page/Feature:** [Where it happened]  
**Steps to Reproduce:**
1. 
2. 
3. 

**Expected:** [What should happen]  
**Actual:** [What actually happened]  
**Screenshot:** [If applicable]  
**Console Errors:** [If any]  
**Browser/Device:** [Web/iOS/Android + version]  
**Date:** YYYY-MM-DD
```

---

## Test Run Log

| Date | Profile | Tester | Result | Bugs Found | Notes |
|------|---------|--------|--------|------------|-------|
| | | | | | |

---

## How to Request Testing

Sunny sends me a message with:
1. **What changed** — feature name or description
2. **Test profile** — or I'll pick the right one
3. **Priority areas** — anything specific to focus on

I'll run the tests, document results, and report back with any bugs found.
