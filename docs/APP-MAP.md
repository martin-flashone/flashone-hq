# FlashOne.AI — App Map (v1.2.104)

## Architecture
- Flutter web app (also iOS, Android beta)
- Firebase backend
- Multi-AI: Gemini (default), OpenAI, Grok, Mistral, Groq, Llama, Qwen, Deepseek
- Freemium model with Pro tier

## Navigation (5 bottom tabs with beta features ON)

### 1. Home
- **Beta Features Toggle** — On/Off for: Transcripts, AI Tutor, Goals, Calendar, Study Reminders
- **AI Top-Up** — Purchase more tokens or images
- **Beta Feature Buttons:**
  - AI Coach PRO — Pronunciation practice
  - Transcribe PRO — Record & transcribe audio
  - Translate PRO — Speak & translate
- **Timed Learning / Pomodoro:**
  - 8 sessions/day target
  - Streak tracking (days)
  - Total session count
  - Settings (gear icon)
  - Start Session button
- **Mastery Progress:**
  - Crown icon to mark cards as mastered
  - Shows mastered card count
- **Study Mode Selector:** Mastery | SRS | CBR Mode
- **Reminders:**
  - Create Reminder
  - Calendar link
  - Notification Settings
  - Mark All Read / Clear All
  - Individual notifications with timestamps
- **Tutorial Progress:**
  - 4 pages of tutorials
  - 2000 tokens reward per tutorial
  - Page 1: Add a Deck, Download a shared deck, Add Flashcards!, Deck & Flashcard Inputs
  - Pages 2-4: (need to explore)

### 2. Calendar / Plan (Beta)
**Roadmap sub-tab:**
- Goals — Set learning goals and track progress
- Events — Classes, training sessions, meetings
- Habits — Build and track learning habits
- Study Reminders — Set reminders to review and study
- Learning Blocks — Review cards scheduled by learning algorithms

**Calendar sub-tab:**
- View modes: Auto, Day, 5-Day, Week, Schedule List
- Print weekly calendar
- Filters: Learning Blocks, Reminders, Events, Goals, Habits
- Navigate forward/back, Today button, date picker
- FAB (+) to add new items

### 3. Notes+
**Data tab:**
- Content pipeline — upload/add data to generate flashcards
- Filter chips: All, Text, Documents, Images w/ Text, Websites, YouTube, Transcripts, By Class
- Search bar
- "Select for Notes" button
- FAB (+) to add data:
  - Generate AI Image
  - Upload from Gallery
  - Take Photo
  - Upload Images w/ Text (AI OCR)
  - Upload File (PDF, DOCX)
  - Add Website/Video (PRO)
  - Transcribe (PRO)

**Notes tab:**
- Generated from Data items
- Empty state → "Go to Data Tab" CTA

**Images tab:**
- (Need to explore further)

### 4. Flashcards
**Deck View:**
- Hierarchical decks (parent → child)
- Each deck card shows: title, description, card count (mastered/total)
- Custom backgrounds: color gradients or AI-generated images
- Expand arrow to show child decks
- Deck context menu (tap or three-dots):
  - Edit Deck Details
  - Add Decks (generate AI child decks)
  - Add Video/Website URL
  - Practice with AI Coach
  - Publish/Share Deck
  - Delete

**Edit Deck:**
- Deck Name, Description
- Color tab (25+ gradient options) or Image tab
- Parent Deck selector (hierarchical)
- Save button

**Mind Map View:**
- Visual node-based view of decks
- Fullscreen expand per deck
- "+" to add child nodes
- Interactive canvas

### 5. New / Shared Decks
- Search bar
- Tabs: All Public Decks, Premium, My Decks, Shared With Me
- Filters: My Labels, Categories, Top Creators
- Deck cards show: rating, download count, creator name, category label
- Community marketplace feel

## Menu (three-dots, top right)
- **Account & Profile** — Avatar, Username, Full Name, Email (locked), Country, Privacy (Allow Deck Discovery), Sign-in Methods
- **Give Feedback**
- **Settings:**
  - Subscription (Pro)
  - Languages — Change app language
  - App Defaults:
    - Navigation Labels
    - AI Provider Settings (provider + model selection, advanced LLM toggle, auto-focus, personal API keys)
    - Audio & Text-to-Speech
    - Learning Modes & SRS
    - Learning Timer
    - Flashcard Defaults
    - Default Deck Visibility (Unlisted/Link Only)
    - Mastery Animations (Random/Surprise me!)
  - Notification Settings
  - Recently Deleted — View and restore deleted decks
  - Permission Settings — Camera, photos, etc.
  - Contact Support — Submit ticket with attachments
  - Privacy Policy
  - Terms of Use
  - Version 1.2.104 + Check for Updates

## Test Data (existing in account)
- 3 decks: Understanding Pro Accounts (7 cards, 4 child decks), The Art of Apple Pie (9 cards), The World of Cheese Its (0 cards)
- 5 data items: 1 transcript, 1 YouTube video, 1 website, 2 image OCR extractions

## Test Accounts
- **Pro:** proflashone@gmail.com
- **Premium:** premiumflashone@gmail.com
- **Free:** freeflashone@gmail.com
- All same password, Google Sign-In

## Deck Creation Methods (Generate Decks)
- **Manual** — Name, description, color, parent deck, Create Deck
- **Topic** — Enter topic, set # of decks, AI generates structure
- **Saved Content** — Generate from data items in Notes+
- **Copy/Paste** — Paste content, then process with:
  - Parse Structure — Preserve exact hierarchy
  - Summarize Content — Extract and organize main topics
  - Generate Outline — Create comprehensive curriculum from scratch
- **Add Image** — Generate from image content
- **Add Document** — Generate from PDF/DOCX

## Deck Page Options (top-right three-dots on Flashcards page)
- Reorder Decks
- Delete Multiple (batch)
- Copy Entire Outline
- Settings

## Deck Card Interactions
- **Tap deck card** — Opens the Deck Player (study view)
- **Long-press deck card** — Opens context menu (Edit, Add Decks, Add URL, AI Coach, Share, Delete)
- **Three-dots (⋮) on card** — Also opens context menu
- **Expand arrow (left)** — Show/hide child decks
- Cards with "7/0" = 7 total cards / 0 mastered

## Deck Player
- **Header:** Back arrow, "Flashcards" title, Speaker icon (TTS), Three-dots menu
- **Deck card display:** Shows mastery badge (e.g., "10/10 mastered" or "10/10 graduated"), ◀ ▶ arrows to navigate between decks
- **▶ Review Cards** — Start study session
- **Study modes:** Normal, Mastery, SRS, CBR, Reset
  - Normal: "Showing all cards" / "10/10 graduated" (green)
  - Mastery: "Hiding X mastered cards" / "10/10 mastered" (yellow/gold)
  - SRS / CBR: (need to explore)
- **Sort flashcards** button + "Default" label
- **X subdecks** dropdown
- **Cards list:** Scrollable list of flashcard fronts, each with three-dots menu
- **+ Add Flashcard** button
- **FAB (+)** button (bottom right)

## Still Need to Explore
- [ ] Actually study flashcards (flip, grade, study session flow)
- [ ] Create a new deck from scratch (manual + AI)
- [ ] Generate flashcards from data items
- [ ] Generate notes from data items
- [ ] AI Coach conversation
- [ ] Transcribe feature
- [ ] Translate feature
- [ ] Images tab in Notes+
- [ ] Print to PDF
- [ ] Share/publish a deck
- [ ] Download a shared deck
- [ ] Subscription/billing flow
- [ ] Languages switching
- [ ] Tutorial walkthroughs (pages 2-4)
- [ ] Pomodoro timer session
- [ ] Goals, Events, Habits, Study Reminders, Learning Blocks (Roadmap items)
- [ ] Deck Options button on Flashcards page header
- [ ] Free tier vs Premium vs Pro differences
- [ ] AI Top-Up purchase flow
- [ ] Contact Support form
