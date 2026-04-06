# Relationship Communication Assistant

## Browser Extension Technical Specification

---

## PRODUCT VISION

A browser extension that prevents relationship damage by helping users communicate their truth while validating what the other person is actually seeking - using their own authentic voice, not generic templates.

**Core Innovation:** Analyzes conversation history to learn YOUR communication patterns and suggests responses that sound like YOU, but tonally calibrated to what the other person needs in this moment.

---

## THE PROBLEM WE SOLVE

**Common Scenario:**

- Partner texts: "cool" or "ok" or "busy again?"
- User responds briefly/factually
- Partner was actually seeking connection/reassurance
- Small miscommunication compounds over time
- Relationship deteriorates from accumulated micro-rejections

**Root Cause:**

- People miss emotional subtext in mundane messages
- Direct communicators unintentionally come across as harsh
- Honest people struggle to be soft without feeling fake
- No tool exists that preserves authenticity while improving tone

---

## CORE FUNCTIONALITY

### 1. Conversation History Analysis

**What it reads:**

- Past messages between user and this specific contact
- Message frequency, length, timing patterns
- Emotional tone progression over time
- User's typical vocabulary and phrasing
- Contact's communication patterns and triggers

**What it learns:**

```javascript
const relationshipProfile = {
  // User's communication style
  userVoice: {
    typicalTone: "direct, factual, brief",
    commonPhrases: ["yeah", "sure", "heading home", "busy"],
    emotionalRange: "low - rarely uses emotive language",
    strengthPattern: "clear and honest",
    weaknessPattern: "misses when softness is needed"
  },
  
  // Contact's patterns
  contactNeeds: {
    primaryNeed: "connection and reassurance",
    triggerWords: ["ok", "cool", "fine"] // when distant
    seekingPattern: "asks logistics but wants engagement",
    respondsWellTo: "warmth + specificity",
    shutsDownFrom: "brief + dismissive"
  },
  
  // Relationship dynamics
  dynamic: {
    successfulExchanges: [/* examples of convos that went well */],
    conflictTriggers: [/* patterns that led to tension */],
    relationshipHealth: "declining - less engagement, more distance",
    riskLevel: "moderate - showing early warning signs"
  }
}
```

**Privacy:** All analysis happens locally. No messages sent to servers.

---

### 2. Real-Time Need Detection

**When new message arrives, extension analyzes:**

```javascript
function detectHiddenNeed(message, conversationContext) {
  // Surface content vs. emotional subtext
  const surfaceContent = message.text; // "cool"
  
  // Contextual signals
  const signals = {
    previousMessages: ["you eat yet?", "grabbed something"],
    timeOfDay: "9pm - typical connection time",
    recentPattern: "3 days of brief exchanges",
    messageLength: "single word - unusually short",
    tonalShift: "was warm earlier, now curt"
  };
  
  // Hidden need analysis
  return {
    surfaceRequest: "Acknowledging information",
    actualNeed: "CONNECTION",
    confidence: 0.85,
    evidence: [
      "Single word after asking personal question",
      "Pattern: she seeks engagement at night",
      "Recent distance in conversation tone"
    ],
    risk: "If you respond briefly, validates her fear you don't care"
  };
}
```

**Detection triggers:**

- Sudden message length change
- Emotionally loaded words ("always", "never", "fine", "whatever")
- Time gaps in conversation (long silence then reaching out)
- Question followed by minimal response from you
- Shift from warm to cold tone

---

### 3. Personalized Modular Response Builder

**Key Innovation:** Options are extracted from YOUR past messages, not generic templates.

**How it works:**

```javascript
function generatePersonalizedOptions(userVoice, contactNeeds, context) {
  // Segment 1: OPENING
  const openingOptions = {
    fromYourVocabulary: [
      "hey", // you use this with her often
      "sorry", // you said this when reconnecting before
      "yo" // casual - matches your usual tone
    ],
    tonalGuidance: {
      "hey": "engaging - signals you want to connect",
      "sorry": "apologetic - acknowledges distance", 
      "yo": "casual - might feel too dismissive here"
    },
    recommended: "hey" // based on her need for connection
  };
  
  // Segment 2: CORE CONTENT
  const coreOptions = {
    fromYourVocabulary: [
      "want to talk?", // you used this successfully before
      "miss you", // you said this 2 weeks ago
      "been busy", // your typical explanation
      "everything ok?" // your pattern when checking in
    ],
    tonalGuidance: {
      "want to talk?": "invites connection - addresses her need",
      "miss you": "vulnerable - high connection value",
      "been busy": "explanatory - might feel like excuse here",
      "everything ok?": "caring - shows concern"
    },
    recommended: "want to talk?" // validates without over-explaining
  };
  
  // Segment 3: ENDING
  const endingOptions = {
    fromYourVocabulary: [
      "what's up?", // you use this to open dialogue
      "call you?", // your pattern for escalating
      "♥️", // you sent this emoji 4 times this month
      "ttyl" // your typical sign-off
    ],
    tonalGuidance: {
      "what's up?": "opens conversation - invites sharing",
      "call you?": "escalates to voice - high engagement",
      "♥️": "affection - softens message",
      "ttyl": "closes conversation - risky here"
    },
    recommended: "what's up?" // keeps conversation open
  };
  
  return { openingOptions, coreOptions, endingOptions };
}
```

**Visual Interface (same as game):**

```
┌─────────────────────────────────────┐
│  Maya                         9:47pm│
├─────────────────────────────────────┤
│            Maya: cool          ◄──  │
│                                     │
│  💡 She's likely seeking:           │
│     CONNECTION                      │
│     (based on conversation pattern) │
│                                     │
├─────────────────────────────────────┤
│  Build your response:               │
│                                     │
│  ┌────────┐ ┌──────────┐ ┌───────┐│
│  │►hey   ◄│ │want to   │ │what's ││
│  │  [use ↑↓│ │talk?     │ │up?    ││
│  │   often]│ │[worked   │ │[opens ││
│  └────────┘ │ before]  │ │convo] ││
│             └──────────┘ └───────┘│
│                                     │
│  Preview: "hey want to talk? what's │
│            up?"                     │
│                                     │
│  ✓ Engages warmly (your style)     │
│  ✓ Validates her need              │
│  ✓ Authentic to how you talk       │
│                                     │
│      [Send]  [Use Default Reply]   │
│                                     │
└─────────────────────────────────────┘
```

---

### 4. Contextual Vocabulary Extraction

**How the extension learns your voice:**

```javascript
function buildUserVocabulary(messageHistory) {
  const vocabulary = {
    // Frequently used openings
    openings: extractPatterns(messages, /^(\w+,?\s)/),
    // "hey", "yo", "so", "look"
    
    // Common phrases for connection
    connectionPhrases: findEmotionalLanguage(messages),
    // "miss you", "thinking of you", "want to see you"
    
    // Typical explanations
    explanations: findJustifications(messages),
    // "been busy", "work is crazy", "exhausted"
    
    // Your checking-in patterns
    checkIns: findQuestions(messages),
    // "you ok?", "everything good?", "what's wrong?"
    
    // Sign-offs you actually use
    closings: extractPatterns(messages, /(\w+)$/),
    // "ttyl", "talk soon", "♥️", "night"
  };
  
  // Filter by success rate
  const effectiveVocabulary = vocabulary.filter(phrase => {
    const usageContext = findUsageContext(phrase);
    const recipientResponse = getSubsequentMessage(usageContext);
    return wasPositiveResponse(recipientResponse);
  });
  
  return effectiveVocabulary;
}
```

**Result:** Extension only suggests phrases YOU actually use that have WORKED before.

---

### 5. Relationship Pattern Dashboard (Premium Feature)

**Insights shown to user:**

```
┌─────────────────────────────────────┐
│  Relationship Insights - Maya       │
├─────────────────────────────────────┤
│                                     │
│  📊 Communication Health: 68/100    │
│  ⚠️  Declining (was 82 last month)  │
│                                     │
│  Your patterns with Maya:           │
│  • Response time: 2-3 hours avg     │
│  • Typical tone: Brief, factual     │
│  • Emotional language: 12% of msgs  │
│                                     │
│  What works:                        │
│  ✓ Specific plans ("dinner Friday?")│
│  ✓ Checking in ("you ok?")          │
│  ✓ Warmth before logistics          │
│                                     │
│  What creates distance:             │
│  ✗ One-word responses               │
│  ✗ Explaining busy without warmth   │
│  ✗ Closing conversations abruptly   │
│                                     │
│  Maya's patterns:                   │
│  • Seeks connection: Evenings       │
│  • Gets distant when: Feels ignored │
│  • Needs: Reassurance she matters   │
│                                     │
│  🎯 Suggestion:                     │
│  When she sends brief messages at   │
│  night, she's usually seeking       │
│  engagement. Try opening dialogue   │
│  before explaining your day.        │
│                                     │
└─────────────────────────────────────┘
```

---

### 6. Warning System (Conflict Prevention)

**Proactive alerts when risk detected:**

```
┌─────────────────────────────────────┐
│  ⚠️  Communication Pattern Alert    │
├─────────────────────────────────────┤
│                                     │
│  Maya has sent 3 brief messages     │
│  after you explained being busy.    │
│                                     │
│  This pattern preceded your last    │
│  argument (2 weeks ago).            │
│                                     │
│  Her likely state: Feeling          │
│  deprioritized                      │
│                                     │
│  Suggested action:                  │
│  Initiate connection before she     │
│  fully withdraws.                   │
│                                     │
│  [Compose message now]  [Remind me] │
│                                     │
└─────────────────────────────────────┘
```

---

## TECHNICAL ARCHITECTURE

### Platform Support

**Browser Extension (Primary):**

- Chrome/Edge/Brave: Manifest V3
- Firefox: WebExtensions API
- Safari: Safari Extensions

**Integration Points:**

- iMessage Web (messages.apple.com via browser)
- WhatsApp Web (web.whatsapp.com)
- Facebook Messenger Web
- Instagram DMs Web
- Any web-based messaging platform

**Future:** Native mobile apps (iMessage keyboard, WhatsApp plugin)

---

### Data Flow

```
┌─────────────────────────────────────┐
│  USER'S DEVICE (All processing local)│
├─────────────────────────────────────┤
│                                     │
│  1. Extension reads conversation    │
│     ↓                               │
│  2. Analyzes patterns locally       │
│     ↓                               │
│  3. Builds relationship profile     │
│     ↓                               │
│  4. New message arrives             │
│     ↓                               │
│  5. Detects hidden need             │
│     ↓                               │
│  6. Generates personalized options  │
│     ↓                               │
│  7. User builds response            │
│     ↓                               │
│  8. Sends via platform (not us)     │
│     ↓                               │
│  9. Learns from outcome             │
│                                     │
│  NO DATA SENT TO SERVERS            │
│  (Privacy-first architecture)       │
│                                     │
└─────────────────────────────────────┘
```

---

### Machine Learning Components

**Local ML Models (run in browser):**

```javascript
// 1. Need Detection Model
const needDetector = await tf.loadLayersModel('local://need-classifier');
// Trained on: conversational context → hidden emotional need
// Output: [connection, significance, autonomy, safety, understanding]

// 2. Tone Analysis Model  
const toneAnalyzer = await tf.loadLayersModel('local://tone-classifier');
// Analyzes: phrase combinations → perceived tone
// Output: [warm, neutral, cold, defensive, engaging, dismissive]

// 3. Pattern Recognition
const patternRecognizer = await tf.loadLayersModel('local://pattern-finder');
// Identifies: conversational sequences → relationship dynamics
// Output: health score, risk factors, successful patterns
```

**Training Data Sources:**

- Anonymized, consensual relationship conversation datasets
- Behavioral science research on communication
- Therapist-validated interaction patterns
- User feedback on what worked/didn't work

**Continuous Learning:**

```javascript
// As user interacts, model learns
function updatePersonalModel(userChoice, outcome) {
  const trainingData = {
    input: {
      context: conversationContext,
      needDetected: hiddenNeed,
      optionsPresented: phraseOptions
    },
    output: {
      userChoice: selectedPhrases,
      recipientResponse: nextMessage,
      userSatisfaction: feedbackScore // optional user rating
    }
  };
  
  // Retrain personal model locally
  personalModel.fit(trainingData);
  // This model becomes unique to user's relationships
}
```

---

### Privacy & Security

**Core Principles:**

1. **Local-first processing** - All analysis on device
2. **Zero message storage** - Process and discard
3. **Opt-in learning** - User controls what's tracked
4. **Encrypted backups** - If user enables cloud sync
5. **Transparent data use** - Clear what's analyzed and why

**Technical Implementation:**

```javascript
// Privacy settings
const privacyConfig = {
  dataStorage: {
    conversationHistory: "local-only", // IndexedDB, never server
    learnedPatterns: "encrypted-backup-optional",
    personalVocabulary: "device-only",
    relationshipProfiles: "local-only"
  },
  
  dataRetention: {
    rawMessages: "processed-then-deleted",
    patterns: "retained-for-learning",
    insights: "user-controlled-deletion"
  },
  
  permissions: {
    readMessages: "required",
    sendMessages: "never - user sends manually",
    shareData: "never - no telemetry",
    cloudSync: "opt-in-only"
  }
};
```

**Security:**

- End-to-end encryption for any cloud features
- No third-party analytics or tracking
- Open source core (users can audit)
- Regular security audits
- GDPR/CCPA compliant by design

---

## USER EXPERIENCE FLOW

### First Time Setup

**Step 1: Install Extension**

```
Welcome to Relationship Communication Assistant

This tool helps you communicate authentically while 
being mindful of what others are actually seeking.

How it works:
1. Analyzes your conversation patterns
2. Detects hidden emotional needs in messages
3. Suggests responses using YOUR voice
4. Helps prevent miscommunication

Your privacy: Everything happens on your device.
We never see your messages.

[Get Started]
```

**Step 2: Choose Contacts to Track**

```
Which relationships would you like help with?

Select up to 3 (Free) or unlimited (Premium):

☐ Maya Chen (Girlfriend)
☐ James Park (Best Friend)  
☐ Robert Chen (Dad)

Extension will learn your communication patterns
with each person individually.

[Continue]
```

**Step 3: Initial Learning Period**

```
Learning your communication style with Maya...

Reading conversation history: ████████░░ 80%

What we've learned so far:
✓ Your typical tone: Direct, honest, brief
✓ Your common phrases: "hey", "yeah", "busy"
✓ Maya's patterns: Seeks connection in evenings
✓ What works: Specific plans, warm check-ins

This will improve as you use the extension.

[Start Using]
```

---

### Daily Use Flow

**Scenario: New message arrives**

```
┌─────────────────────────────────────┐
│  💬 New message from Maya           │
│                                     │
│  Maya: "cool"                       │
│                                     │
│  [Analyze] ← Click to get help     │
└─────────────────────────────────────┘
```

**User clicks Analyze:**

```
┌─────────────────────────────────────┐
│  Message Analysis                   │
├─────────────────────────────────────┤
│                                     │
│  Surface: Acknowledging info        │
│  Hidden need: CONNECTION (85%)      │
│                                     │
│  Why: Single word after asking      │
│  personal question. Pattern shows   │
│  she seeks engagement at night.     │
│                                     │
│  Risk: Brief response may feel      │
│  dismissive                         │
│                                     │
│  [Build Better Response]            │
│                                     │
└─────────────────────────────────────┘
```

**User clicks Build Better Response:**

```
[Shows modular sentence builder with personalized options]
[User constructs: "hey want to talk? what's up?"]
[Preview shows tone analysis]
[User clicks Send - message goes via platform]
```

**After sending, optional feedback:**

```
┌─────────────────────────────────────┐
│  How did that go?                   │
│                                     │
│  Did Maya respond positively?       │
│                                     │
│  😊 Yes, felt good                  │
│  😐 Okay, but could be better       │
│  😟 No, still felt off              │
│                                     │
│  [This helps us learn]              │
│                                     │
└─────────────────────────────────────┘
```

---

## FEATURES BY TIER

### Free Version

**Included:**

- ✓ Track 3 relationships
- ✓ Basic need detection (5 core needs)
- ✓ Personalized response builder
- ✓ Your vocabulary extraction
- ✓ Simple tone guidance
- ✓ Privacy-first local processing

**Limitations:**

- Only 3 active relationships at a time
- Basic insights (no detailed analytics)
- No conflict prediction
- No relationship health scoring

---

### Premium ($12/month or $99/year)

**Everything in Free, plus:**

- ✓ Unlimited relationships
- ✓ Advanced need detection (15+ nuanced needs)
- ✓ Relationship health dashboard
- ✓ Pattern insights and trends
- ✓ Conflict prediction warnings
- ✓ "Explain why this works" feature
- ✓ Success pattern identification
- ✓ Encrypted cloud backup (optional)
- ✓ Priority support

**Advanced Features:**

**Conflict Prediction:**

```
⚠️ Warning: High risk of conflict
Pattern match: 87% similar to previous argument

Trigger identified: Extended busy period + brief responses
Expected reaction: Withdrawal → confrontation

Suggested intervention:
Proactively initiate connection in next 24 hours

[See details] [Remind me]
```

**Success Pattern Insights:**

```
💚 Communication win detected!

What worked:
You: "hey want to talk? what's up?"
Maya: [Long, engaged response]

Why it worked:
✓ Opened warmly (not defensively)
✓ Invited dialogue (not closed)
✓ Validated her connection need
✓ Used your authentic voice

Save this pattern? [Yes] [No]
```

**Relationship Trends:**

```
📈 30-Day Communication Report

Health Score: 68 → 74 (+6)
Response time: 3hrs → 1.5hrs (improving)
Emotional language: 12% → 24% (great!)
Conversation length: Increasing

What's working:
✓ More check-ins initiated by you
✓ Warmer openings before logistics
✓ Better response time in evenings

Keep improving:
⚠ Still brief when explaining busy
⚠ Sometimes close convos abruptly
```

---

### Enterprise/Therapy Edition ($50+/month)

**For therapists, coaches, couples counselors:**

**Additional Features:**

- ✓ Multi-client management
- ✓ Anonymized case studies
- ✓ Export communication reports
- ✓ Therapist dashboard for tracking
- ✓ Guided exercises and homework
- ✓ Before/after comparison tools
- ✓ HIPAA-compliant version available

**Use Case:**

```
Therapist assigns to couple:
"Use the extension for 2 weeks, then we'll 
review your communication patterns together."

Reports show:
- Each person's typical tone
- Mismatch points (where needs aren't met)
- Successful vs. unsuccessful exchanges
- Progress over time
```

---

## MONETIZATION STRATEGY

### Revenue Model

**Individual Subscriptions:**

- Free: 3 relationships (conversion funnel)
- Premium: $12/mo or $99/yr (primary revenue)
- Target: 10,000 paying users = $120K MRR

**Enterprise/Therapy:**

- $50-500/mo depending on client volume
- Target: 100 therapists = $15K MRR

**One-time purchases:**

- Lifetime Premium: $299 (for early adopters)
- Course bundle: "Master Communication" + Premium ($149)

**Projected ARR at Scale:**

- 50K free users (awareness + conversion)
- 10K premium users × $99/yr = $990K
- 100 enterprise users × $600/yr = $60K
- **Total: ~$1M ARR**

---

### Go-to-Market Strategy

**Phase 1: Game Launch (Validation)**

- Free game goes viral
- Proves people want to learn this skill
- Builds email list of interested users
- Social proof through testimonials

**Phase 2: Extension Beta (Early Adopters)**

- Invite game players to beta test extension
- Offer lifetime discount for early feedback
- Iterate based on real usage
- Generate case studies

**Phase 3: Public Launch**

- Press: "The app that prevents breakups"
- Target: Relationship subreddits, YouTube, TikTok
- Partnerships: Therapists, relationship coaches
- Content marketing: "Why 'cool' doesn't mean cool"

**Phase 4: B2B Expansion**

- Pitch to therapy practices
- Create training programs for counselors
- Academic partnerships for research
- Clinical validation studies

---

## TECHNICAL IMPLEMENTATION ROADMAP

### MVP (Months 1-3)

**Core functionality:**

- [x] Browser extension shell
- [x] iMessage Web integration
- [x] Read conversation history
- [x] Basic need detection (rule-based)
- [x] Modular response builder UI
- [x] Personalized vocabulary extraction
- [x] Local storage of patterns
- [ ] Chrome extension published

**Tech Stack:**

- Frontend: React + TypeScript
- Storage: IndexedDB (local-first)
- ML: TensorFlow.js (client-side)
- Build: Vite + Manifest V3

---

### V1.0 (Months 4-6)

**Enhanced features:**

- [ ] WhatsApp Web integration
- [ ] ML-based need detection
- [ ] Relationship health scoring
- [ ] Pattern insights dashboard
- [ ] Firefox + Safari extensions
- [ ] Premium tier launch

**Infrastructure:**

- [ ] Stripe payment integration
- [ ] Optional encrypted cloud backup
- [ ] User accounts (optional)
- [ ] Analytics (privacy-preserving)

---

### V2.0 (Months 7-12)

**Advanced capabilities:**

- [ ] Conflict prediction system
- [ ] Multi-contact support (unlimited)
- [ ] Messenger/Instagram integration
- [ ] Mobile app (iOS/Android)
- [ ] Therapist dashboard
- [ ] API for third-party integrations

---

## SUCCESS METRICS

### User Engagement

- Daily Active Users (DAU)
- Messages analyzed per user/day
- Response builder usage rate
- Free → Premium conversion %

### Product Effectiveness

- User-reported relationship improvement
- Conflict prevention success rate
- Response quality scores (user feedback)
- Retention: 30/60/90 day cohorts

### Business Metrics

- MRR/ARR growth
- Customer Acquisition Cost (CAC)
- Lifetime Value (LTV)
- LTV:CAC ratio (target: 3:1)
- Churn rate (target: <5%/month)

### Impact Metrics

- Relationships saved (user testimonials)
- Improved communication scores
- Reduced miscommunication incidents
- User-reported satisfaction increase

---

## COMPETITIVE DIFFERENTIATION

**Vs. Generic Communication Advice:**

- ❌ Generic: "Use I-statements"
- ✅ Us: "You typically say 'yeah' - try 'hey' here instead"

**Vs. AI Writing Assistants:**

- ❌ AI: Rewrites in formal/generic tone
- ✅ Us: Uses YOUR vocabulary, maintains YOUR voice

**Vs. Relationship Apps:**

- ❌ Apps: General tips and articles
- ✅ Us: Real-time, personalized, relationship-specific

**Vs. Therapy:**

- ❌ Therapy: Weekly sessions, expensive, reactive
- ✅ Us: Real-time prevention, affordable, proactive

**Our Moat:**

- Personalized to individual relationship dynamics
- Learns from YOUR actual conversation patterns
- Preserves authenticity (doesn't make you sound fake)
- Privacy-first (all processing local)
- Game-to-tool ecosystem (teaches then applies)

---

## PROMPT FOR AI CODING ASSISTANT

Use this when building the extension:

```
Build a browser extension for relationship communication assistance.

CORE FUNCTIONALITY:
1. Read messaging web app conversations (iMessage Web, WhatsApp Web)
2. Analyze conversation history to learn user's voice
3. Detect hidden emotional needs in new messages
4. Generate personalized response options using user's vocabulary
5. Modular sentence builder UI (3 segments: opening, core, ending)
6. All processing happens locally (privacy-first)

USER FLOW:
- User receives message
- Extension detects hidden need (CONNECTION, SIGNIFICANCE, etc.)
- Shows modular builder with options from user's vocabulary
- User builds response using arrow keys/clicks
- Preview updates in real-time
- User sends via platform (not through extension)

DATA SOURCES:
- Conversation history (read from DOM)
- Extract user's common phrases, patterns
- Identify contact's communication style
- Learn what phrases work vs. don't work

UI COMPONENTS:
- Floating widget on messaging apps
- Modular sentence builder (same as game design)
- Need detection indicator
- Tone guidance labels
- Send button (opens platform's send)

TECHNICAL REQUIREMENTS:
- Manifest V3 browser extension
- React + TypeScript
- IndexedDB for local storage
- TensorFlow.js for ML (need detection)
- No external API calls
- Privacy-first architecture

SECURITY:
- No message data leaves device
- Optional encrypted cloud backup
- Transparent permissions
- Open source core

Build this with clean architecture, strong privacy controls,
and smooth UX matching the game's modular builder design.
```

---

## CONCLUSION

This extension solves real relationship pain by:

1. **Teaching awareness** (via the game)
2. **Applying in real-time** (via the extension)
3. **Personalizing to YOU** (learns your voice)
4. **Preserving authenticity** (not generic templates)
5. **Preventing damage** (proactive warnings)

**The unfair advantage:** You built this from lived experience, deep persuasion knowledge, and genuine desire to help others avoid the pain you experienced.

**Next steps:**

1. Finish game MVP
2. Validate people learn the skill
3. Build extension with beta users
4. Launch to game's audience
5. Scale with testimonials

This could genuinely help millions of people communicate better while staying authentic to who they are.