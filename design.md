# Design Document: Anonymous Support Platform

## System Overview

The platform is an AI-facilitated anonymous peer support system for mental health in India. Users join topic-based groups (6-8 people) for 40-minute sessions moderated by AI, with human supervisors monitoring high-risk cases.

**Core Components:**
- Anonymous user management and authentication
- Lobby system for group formation
- Real-time messaging with AI moderation
- Three AI systems: Moderator (safety), Facilitator (conversation flow), Screener (crisis detection)
- Risk dashboard for human supervisors
- Feedback dashboard for platform improvement

**Technology Stack:**
- AWS infrastructure (India region)
- Amazon Bedrock for AI (no data retention)
- DynamoDB for data storage
- WebSocket for real-time messaging
- React Native for mobile app

## Architectural Principles

1. **India-First**: Hinglish support, Indian cultural context, data localization
2. **Privacy by Design**: Anonymity, encryption, minimal data retention
3. **Human-in-Loop**: AI handles scale, humans handle critical decisions
4. **Fail-Safe**: Graceful degradation when AI fails, always show crisis resources
5. **Scalability**: Serverless architecture for cost-effective scaling
6. **Simplicity**: Minimal viable features, no feature bloat

## Development Phases

### Phase 1: Hackathon Prototype (10 Days)
**Goal**: Win hackathon by demonstrating high-impact, feasible solution with strong business case

**Hackathon Evaluation Optimization:**

**Ideation & Creativity (30%)**
- Novelty: AI-facilitated anonymous peer support (not therapy chatbot)
- Alignment: Addresses India's mental health crisis with culturally-sensitive approach
- Uniqueness: Three AI systems (Moderator, Facilitator, Screener) + human oversight
- Demo: Show AI preventing echo chambers, detecting crisis, maintaining anonymity

**Impact (20%)**
- Clear beneficiaries: 150M Indians needing mental health support
- Quantifiable impact: Bridge to care for those uncertain about seeking help
- Demo: Show crisis detection → resource guidance flow
- Testimonial-ready: Beta testers share "felt less alone" stories

**Technical Aptness (30%)**
- Plausible architecture: AWS serverless, proven tech stack
- Working demo: Real-time chat with AI moderation
- Scalability story: Serverless scales to millions
- Constraints addressed: Low bandwidth (2G/3G), Hinglish support

**Business Feasibility (20%)**
- Go-to-market: Partner with colleges (exam stress), corporates (burnout)
- Value proposition: Free for users, funded by grants + CSR
- Sustainability: Phase 2 freemium features (priority matching, extended sessions)
- Traction: Letters of intent from 2-3 college counseling centers

---

**Prototype Scope:**

**Core Features:**
- Anonymous registration (phone + OTP, age verification)
- Single topic: "Exam Stress" (relatable for judges/audience)
- Manual group formation (admin dashboard to create groups of 6)
- Real-time messaging (Socket.io)
- AI Moderator (Amazon Bedrock - Claude):
  - Block hate speech, doxing, anonymity breaches
  - Provide specific explanations in Hinglish
- AI Facilitator (Amazon Bedrock - Claude):
  - Detect conversation stalls (3 min silence)
  - Introduce discussion prompts
  - Prevent echo chambers
- Crisis detection (keyword-based):
  - Keywords: "suicide", "self-harm", "hopeless", "end it all"
  - Trigger: Show popup with crisis resources (NIMHANS, Vandrevala Foundation)
- 40-minute session timer with auto-dissolution
- Post-session reflection (simple feedback form)

**Demo Flow (5 minutes):**
1. Show problem: Stats on India's mental health crisis, stigma
2. Show solution: Platform walkthrough
3. Live demo: 6 users (3 real, 3 simulated) in "Exam Stress" group
   - User shares stress → AI Facilitator encourages others to respond
   - User posts agreement → AI introduces alternative perspective
   - User mentions "feeling hopeless" → Crisis popup appears
   - Conversation stalls → AI prompts discussion
   - Someone tries to share phone number → AI blocks with explanation
4. Show impact: "User felt less alone, accessed counseling resources"
5. Show business model: Partnerships, sustainability plan

**Technical Implementation:**

**Frontend:**
- React web app (mobile-responsive)
- Pages: Register, Topic Selection, Chat, Post-Session
- WebSocket for real-time messaging

**Backend:**
- Node.js + Express
- Socket.io for WebSocket
- AWS Lambda (for Bedrock API calls)
- DynamoDB (for user data, messages, sessions)

**AI Integration:**
- Amazon Bedrock (Claude 3 Haiku - fast + cheap)
- Moderator prompt: "Analyze this message for violations: hate speech, doxing, anonymity breach, rude behavior. Respond in JSON with: {violation: true/false, type: string, explanation: string}. Use Hinglish for explanation."
- Facilitator prompt: "Given this conversation history on 'Exam Stress', suggest a discussion prompt to keep conversation flowing. Respond in Hinglish. Max 50 words."

**Data Storage:**
- Users table: user_id, phone_hash, anonymous_id, age_verified
- Sessions table: session_id, topic, start_time, user_ids[]
- Messages table: message_id, session_id, user_id, content, timestamp

**Crisis Detection:**
- Simple keyword matching (regex)
- If match: Show popup with resources
- Log to console (for demo purposes)

---

**Out of Scope (Phase 1):**
- Lobby system (manual group formation instead)
- AI Screener with ML models (keyword-based only)
- Risk dashboard (just console logs)
- Feedback dashboard
- Data encryption (use HTTPS, but no KMS)
- Multi-topic support (single topic only)
- Hinglish NLP (Bedrock handles it)

---

**Hackathon Deliverables:**

1. **Working Prototype** (deployed on AWS)
2. **Pitch Deck** (10 slides):
   - Problem (India's mental health crisis)
   - Solution (AI-facilitated peer support)
   - Demo (screenshots/video)
   - Impact (beneficiaries, metrics)
   - Technical Architecture (diagram)
   - Business Model (partnerships, sustainability)
   - Roadmap (Phase 2-4)
   - Team (backgrounds, why us)
   - Ask (funding, partnerships)
3. **Demo Video** (2 minutes) - backup if live demo fails
4. **GitHub Repo** (clean code, README)
5. **Letters of Intent** (2-3 colleges/NGOs interested in piloting)

---

**Success Criteria:**
- Live demo works for 6 users chatting simultaneously
- AI moderation blocks obvious violations with Hinglish explanations
- AI facilitation introduces 2-3 prompts during 5-minute demo
- Crisis detection triggers popup when keywords detected
- Judges understand impact, feasibility, and business model
- **Target: Top 3 finish**

---

### Phase 2: MVP (4-5 Months)
**Goal**: Production-ready platform for initial user testing

**Scope:**
- Anonymous registration with age verification
- 5 topics: Exam Stress, Work Burnout, Family Issues, Anxiety, General Support
- Lobby system with opt-in and group formation (6-8 users, min 5 after 15 min)
- 40-minute sessions with automatic dissolution
- AI Moderator using Amazon Bedrock (real-time content moderation)
- AI Facilitator using Amazon Bedrock (conversation prompts, echo chamber prevention)
- Basic AI Screener (keyword-based crisis detection)
- Risk dashboard (manual review of flagged users)
- Feedback dashboard
- Hinglish support (code-switching)
- Data encryption (TLS 1.3, AWS KMS)
- 24-48 hour message retention
- Crisis resources ("Seek Help" button)
- Post-session reflection

**Out of Scope:**
- Advanced AI screening models, proactive human audits, appeal mechanisms, audio features

**Architecture:**
- Frontend: React Native (iOS + Android)
- Backend: AWS Lambda + API Gateway
- Real-time: AWS AppSync (GraphQL subscriptions)
- Storage: DynamoDB
- AI: Amazon Bedrock (Claude/Llama models)
- Auth: AWS Cognito

**Success Criteria:**
- 100 concurrent users across multiple groups
- AI moderation accuracy >85%
- <2 second message delivery
- Human supervisors can review flagged cases within 24 hours

---

### Phase 3: Enhanced AI + Human Oversight (6-8 Months)
**Goal**: Improve AI accuracy and strengthen human-in-loop

**Scope:**
- Advanced AI Screener with trained models (sentiment analysis, crisis pattern detection)
- Topic-specific AI Facilitator fine-tuning
- Proactive human audit sampling (5% random sessions)
- User appeal mechanisms for AI decisions
- AI bias monitoring across Indian demographics
- AI explainability (detailed explanations for moderation decisions)
- Enhanced risk dashboard (severity scoring, intervention recommendations)
- Progressive enforcement (warnings, temp bans, permanent bans)
- Session reconnection after network interruption
- Mood check-in before sessions

**Out of Scope:**
- Audio features, additional languages

**New Components:**
- ML training pipeline for AI Screener
- Audit sampling system
- Appeal workflow system
- Bias monitoring dashboard

**Success Criteria:**
- AI moderation accuracy >95%
- AI screening sensitivity >90%
- <5% false positive rate on risk detection
- Human supervisors review 5% of sessions proactively
- Appeal resolution within 24 hours

---

### Phase 4: Audio + Accessibility (8-10 Months)
**Goal**: Add audio features for accessibility

**Scope:**
- Text-to-speech for chat messages (real-time narration)
- Voice input option (speech-to-text)
- Audio-only mode for users with visual impairments
- Enhanced accessibility (screen reader optimization, keyboard navigation)
- Audio moderation (detect tone, aggression in voice)
- AI Ethics Advisory Board establishment

**Out of Scope:**
- Regional Indian languages (future phase)

**New Components:**
- Audio processing pipeline
- Speech-to-text / text-to-speech integration
- Audio moderation system

**Success Criteria:**
- Audio narration with <3 second latency
- Voice input accuracy >90% for Hinglish
- WCAG 2.1 Level AA compliance

---

## High-Level Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                     Web Browser                              │
│              (React App - Mobile Responsive)                 │
└────────────┬────────────────────────────────────────────────┘
             │
             │ HTTPS/WSS
             │
┌────────────▼────────────────────────────────────────────────┐
│                     API Gateway                              │
│              (REST + WebSocket)                              │
└────────────┬────────────────────────────────────────────────┘
             │
     ┌───────┴───────┐
     │               │
┌────▼─────┐   ┌────▼─────────────────────────────────────┐
│  Lambda  │   │         AppSync (GraphQL)                 │
│Functions │   │    (Real-time Subscriptions)              │
└────┬─────┘   └────┬─────────────────────────────────────┘
     │              │
     │         ┌────▼─────┐
     │         │DynamoDB  │
     │         │ Tables   │
     │         └──────────┘
     │
┌────▼──────────────────────────────────────────────────────┐
│              Amazon Bedrock                                │
│   (AI Moderator, Facilitator, Screener)                   │
└────────────────────────────────────────────────────────────┘
```

## Component-Level Design

### 1. User Management Service
**Responsibilities:**
- Anonymous registration (phone + OTP)
- Age verification (18+ self-declaration)
- Anonymous ID generation (UUID)
- Account deletion

**APIs:**
- `POST /auth/register` - Register with phone number
- `POST /auth/verify` - Verify OTP
- `DELETE /auth/account` - Delete account

**Data:**
- User table: `user_id`, `phone_hash`, `age_verified`, `created_at`, `anonymous_id`

---

### 2. Lobby Service
**Responsibilities:**
- Topic selection
- User queueing
- Opt-in tracking
- Group formation (6-8 users, min 5 after 15 min)
- Wait time estimation

**APIs:**
- `GET /topics` - List available topics
- `POST /lobby/join` - Join topic lobby
- `POST /lobby/opt-in` - Opt in to next group
- `POST /lobby/leave` - Leave lobby

**Data:**
- Lobby table: `topic_id`, `user_id`, `opted_in`, `joined_at`

**Logic:**
- Check opted-in users every 30 seconds
- If 6-8 users: create group immediately
- If >8 users: create multiple groups
- Degrading thresholds for low-traffic topics:
  - 5-6 users after 10 min: create group
  - 5 users after 15 min: create group
  - 4 users after 20 min: create group
- Cross-topic merging: If multiple related topics have 3-4 users each after 15 min, suggest merging (e.g., "Exam Stress" + "Academic Pressure" → "Student Stress")

---

### 3. Session Service
**Responsibilities:**
- Create 40-minute sessions
- Manage session lifecycle
- Track session state
- Handle user dropout
- Session reconnection (5 min window)

**APIs:**
- `POST /session/create` - Create new session
- `POST /session/{id}/join` - Join session
- `POST /session/{id}/leave` - Leave session
- `GET /session/{id}/status` - Get session status

**Data:**
- Session table: `session_id`, `topic_id`, `start_time`, `end_time`, `status`, `user_ids[]`

**Logic:**
- Auto-dissolve after 40 minutes
- Return users to lobby on session end
- Allow reconnection within 5 minutes of disconnect

---

### 4. Messaging Service
**Responsibilities:**
- Real-time message delivery (<2 sec)
- Message persistence (24-48 hours)
- Message ordering
- Offline message storage

**APIs:**
- WebSocket: `sendMessage`, `receiveMessage`
- `GET /messages/{session_id}` - Fetch message history

**Data:**
- Message table: `message_id`, `session_id`, `user_id`, `content`, `timestamp`, `ttl` (24-48 hours)

---

### 5. AI Moderator Service
**Responsibilities:**
- Real-time content analysis (<1 sec)
- Block violations (doxing, hate speech, anonymity breach)
- Flag for review (rude behavior, arguments)
- Provide specific violation explanations

**Integration:**
- Amazon Bedrock (Claude model)
- Prompt: "Analyze this message for: doxing, hate speech, anonymity breach, rude behavior. Respond in JSON."

**Logic:**
- Severe violations: Block message, warn user
- Minor violations: Allow message, flag for async review
- Track violation count per user

**Data:**
- Moderation table: `message_id`, `violation_type`, `severity`, `action_taken`, `explanation`

---

### 6. AI Facilitator Service
**Responsibilities:**
- Detect conversation stalls (3 min silence)
- Detect echo chambers (5+ agreement messages)
- Generate discussion prompts
- Limit interventions (max 1 per 5 min)

**Integration:**
- Amazon Bedrock (Claude model)
- Prompt: "Given this conversation history and topic, suggest a discussion prompt."

**Logic:**
- Monitor message patterns
- Intervene only when necessary
- Adapt to group engagement level

---

### 7. AI Screener Service
**Responsibilities:**
- Analyze message patterns for crisis indicators
- Detect mental health breakdown risk
- Trigger support resource popups
- Add users to risk dashboard

**Integration:**
- Phase 2: Keyword-based (suicide, self-harm, hopeless)
- Phase 3: Trained ML models (sentiment, crisis patterns)

**Logic:**
- Analyze per-user message history
- Calculate risk score
- Threshold: High risk → dashboard + popup

**Data:**
- Risk table: `user_id`, `session_id`, `risk_score`, `indicators[]`, `flagged_at`

---

### 8. Risk Dashboard Service
**Responsibilities:**
- Display flagged users
- Prioritize by severity
- Track supervisor reviews
- Record interventions

**APIs:**
- `GET /dashboard/risk` - List at-risk users
- `POST /dashboard/risk/{user_id}/review` - Mark as reviewed
- `POST /dashboard/risk/{user_id}/intervene` - Record intervention

**Data:**
- Review table: `user_id`, `supervisor_id`, `reviewed_at`, `action_taken`, `notes`

---

### 9. Feedback Dashboard Service
**Responsibilities:**
- Collect user feedback
- Categorize feedback (technical, feature, community)
- Track resolution status

**APIs:**
- `POST /feedback` - Submit feedback
- `GET /dashboard/feedback` - List feedback
- `PUT /dashboard/feedback/{id}` - Update status

**Data:**
- Feedback table: `feedback_id`, `user_id`, `category`, `content`, `status`, `created_at`

---

## Data Models & Relationships

### Core Tables

**Users**
```
user_id (PK)
phone_hash (unique, indexed)
anonymous_id (unique)
age_verified (boolean)
created_at
opt_out_ai_training (boolean)
```

**Sessions**
```
session_id (PK)
topic_id
start_time
end_time
status (active, ended)
user_ids[] (list)
```

**Messages**
```
message_id (PK)
session_id (indexed)
user_id
content (encrypted)
timestamp
ttl (24-48 hours)
moderation_status (approved, flagged, blocked)
```

**Moderation_Actions**
```
action_id (PK)
message_id
user_id
violation_type
severity (low, medium, high)
action_taken (warn, flag, block)
explanation
timestamp
```

**Risk_Flags**
```
flag_id (PK)
user_id (indexed)
session_id
risk_score (0-100)
indicators[] (keywords, patterns)
flagged_at
reviewed (boolean)
reviewer_id
reviewed_at
```

**Feedback**
```
feedback_id (PK)
user_id
session_id
category (technical, feature, community)
content
status (open, in_progress, resolved)
created_at
```

### Relationships
- User → Messages (1:N)
- Session → Messages (1:N)
- Session → Users (N:M via user_ids array)
- User → Risk_Flags (1:N)
- Message → Moderation_Actions (1:1)

---

## Security Measures

### 1. Anonymity Protection
- Generate UUID for anonymous_id (no PII)
- Hash phone numbers (SHA-256 + salt)
- Never expose phone numbers in API responses
- Separate anonymous_id per session (Phase 3)

### 2. Data Encryption
- TLS 1.3 for all API traffic
- AWS KMS for data at rest
- Separate encryption keys per data sensitivity
- Key rotation every 30-90 days

### 3. Authentication & Authorization
- AWS Cognito for user auth
- JWT tokens with 1-hour expiry
- Role-based access (user, supervisor, admin)
- MFA for supervisors

### 4. Data Retention
- Messages: 24-48 hours (auto-delete via DynamoDB TTL)
- Flagged content: 30 days
- Anonymized metadata: 90 days
- Audit logs: 7 years

### 5. PII Removal
- Pre-process messages before sending to Bedrock
- Regex patterns for phone, email, address, names
- Replace with placeholders: [PHONE], [EMAIL], [NAME]

### 6. Rate Limiting
- 10 messages per minute per user
- 100 API requests per minute per user
- DDoS protection via AWS WAF

### 7. Audit Logging
- Log all authentication attempts
- Log all data access (who, what, when)
- Log all moderation actions
- Immutable logs (write-only)
- 7-year retention for compliance

---

## Formal Correctness Properties

### P1: Anonymity Preservation
**Property**: No user's real identity SHALL be exposed to other users or stored in message content.

**Validation**:
- Unit test: Verify anonymous_id generation is unique and random
- Integration test: Verify API responses never contain phone_hash
- Property test: For all messages, content SHALL NOT contain phone numbers, emails, or names after PII removal

---

### P2: Message Delivery Guarantee
**Property**: All messages sent during an active session SHALL be delivered to all session members within 2 seconds.

**Validation**:
- Integration test: Send message, verify all users receive within 2 sec
- Load test: 100 concurrent sessions, measure p95 latency
- Property test: For all messages in active sessions, delivery_time <= 2 seconds

---

### P3: Session Time Bounds
**Property**: All sessions SHALL last exactly 40 minutes and auto-dissolve.

**Validation**:
- Unit test: Verify session timer triggers dissolution at 40 min
- Integration test: Create session, wait 40 min, verify status = ended
- Property test: For all sessions, end_time - start_time = 40 minutes

---

### P4: Group Size Constraints
**Property**: All groups SHALL have 4-8 members at formation (4 only after 20 min wait).

**Validation**:
- Unit test: Verify group formation logic enforces 4-8 range with time-based thresholds
- Integration test: Simulate lobby with various user counts and wait times, verify group sizes
- Property test: For all groups, (4 <= member_count <= 8) AND (member_count = 4 IMPLIES wait_time >= 20 min)

---

### P5: Moderation Response Time
**Property**: AI Moderator SHALL analyze and respond to messages within 1 second.

**Validation**:
- Integration test: Send message, measure moderation latency
- Load test: 1000 messages/sec, measure p99 latency
- Property test: For all messages, moderation_time <= 1 second

---

### P6: Data Retention Compliance
**Property**: Messages SHALL be deleted within 24-48 hours, PII SHALL be deleted within 7 days of account deletion.

**Validation**:
- Unit test: Verify DynamoDB TTL is set correctly
- Integration test: Create message, wait 48 hours, verify deletion
- Integration test: Delete account, wait 7 days, verify PII removed
- Property test: For all messages, current_time - timestamp <= 48 hours OR message deleted

---

### P7: Crisis Resource Availability
**Property**: "Seek Help" button SHALL be visible on all screens.

**Validation**:
- UI test: Verify button exists on topic selection, lobby, session, post-session screens
- Accessibility test: Verify button is keyboard-accessible and screen-reader compatible
- Property test: For all screens, seek_help_button.visible = true

---

### P8: Encryption in Transit and Rest
**Property**: All data SHALL be encrypted in transit (TLS 1.3) and at rest (AWS KMS).

**Validation**:
- Security test: Verify TLS 1.3 is enforced on all endpoints
- Security test: Verify DynamoDB encryption is enabled
- Penetration test: Attempt to intercept unencrypted data

---

## Error Handling Design

### 1. AI Service Failures
**Scenario**: Bedrock API is down or slow

**Handling**:
- Moderator failure: Allow message through, flag for async review, log error
- Facilitator failure: Skip intervention, continue session normally
- Screener failure: Show generic crisis resources, log error

**User Impact**: Minimal, session continues

---

### 2. Network Interruptions
**Scenario**: User loses connection during session

**Handling**:
- Allow reconnection within 5 minutes
- On reconnect: fetch missed messages, resume session
- After 5 minutes: mark user as dropped, continue session with remaining users

**User Impact**: Can rejoin if quick, otherwise loses session

---

### 3. Group Formation Timeout
**Scenario**: Not enough users opt in after 30 minutes

**Handling**:
- Suggest alternative topics with more users
- Allow user to stay in lobby or switch topics
- Send notification when group is ready

**User Impact**: Longer wait, but not stuck

---

### 4. Session Overload
**Scenario**: Too many concurrent sessions (>500)

**Handling**:
- Queue new group formations
- Display wait time estimate
- Scale Lambda functions automatically

**User Impact**: Slight delay in group formation

---

### 5. Data Corruption
**Scenario**: Message fails to save to DynamoDB

**Handling**:
- Retry 3 times with exponential backoff
- If still fails: log error, notify user "message failed to send"
- Do not block other messages

**User Impact**: Single message lost, user can resend

---

### 6. Moderation False Positives
**Scenario**: AI blocks legitimate message

**Handling**:
- Provide specific explanation to user
- Offer appeal button (Phase 3)
- Log for human review

**User Impact**: Message blocked, but can appeal

---

## Comprehensive Testing Strategy

### 1. Unit Tests
**Coverage**: >80% for all services

**Focus**:
- Business logic (group formation with degrading thresholds, session lifecycle)
- Data validation (age verification, message length)
- Utility functions (PII removal, encryption)
- Lobby merging logic (cross-topic group formation)

**Tools**: Jest, Mocha

**Key Test Cases**:
- Group formation at different time thresholds (10, 15, 20 min)
- PII removal for Indian phone formats (+91, 10-digit)
- Hinglish text processing edge cases

---

### 2. Integration Tests
**Focus**:
- API endpoints (auth, lobby, session, messaging)
- Database operations (CRUD, TTL)
- AI service integration (Bedrock API calls)
- WebSocket connections
- Cross-service workflows (lobby → session → messaging)

**Tools**: Supertest, Postman

**Key Test Cases**:
- Complete user journey: register → lobby → opt-in → session → message → leave
- AI moderation pipeline: message → Bedrock → decision → action
- Session reconnection after network drop

---

### 3. Property-Based Tests
**Focus**:
- Correctness properties (P1-P8)
- Invariants (group size, session duration, anonymity)

**Tools**: fast-check (JavaScript)

**Examples**:
- Property: All groups have 4-8 members with time-based constraints
- Property: All messages delivered within 2 seconds
- Property: No PII in message content after processing
- Property: For all Hinglish messages, code-switching is preserved
- Property: For all sessions, reconnection allowed within 5 minutes

---

### 4. AI-Specific Tests

#### 4.1 Adversarial Testing
**Focus**: Users attempting to bypass moderation

**Test Cases**:
- Obfuscated hate speech (l3t sp3ak, using emojis)
- PII in Hinglish ("mera number hai nau nau nau...")
- Doxing attempts with indirect references
- Anonymity breaches using coded language

**Tools**: Custom test harness with adversarial prompts

**Success Criteria**: AI catches >90% of adversarial attempts

---

#### 4.2 Hinglish-Specific Tests
**Focus**: Code-switching and Indian language patterns

**Test Cases**:
- Pure Hindi (Devanagari script)
- Pure English
- Mixed Hinglish ("Yaar, I'm so stressed about exams")
- Regional variations (Mumbai vs Delhi Hinglish)
- Transliterated Hindi (Roman script)

**Tools**: Custom test dataset with 1000+ Hinglish samples

**Success Criteria**: AI moderation accuracy >85% across all variations

---

#### 4.3 Cultural Sensitivity Tests
**Focus**: AI responses are culturally appropriate

**Test Cases**:
- Family dynamics (joint family, arranged marriage)
- Religious references (festivals, practices)
- Caste-related discussions (sensitive but not hate speech)
- Gender-specific pressures (dowry, career expectations)

**Tools**: Human review panel with diverse Indian backgrounds

**Success Criteria**: 0 culturally insensitive AI responses in 100 test cases

---

#### 4.4 Bias Testing
**Focus**: AI treats all demographics fairly

**Test Datasets**:
- Messages from different regions (North, South, East, West India)
- Different socioeconomic indicators (English proficiency, education level)
- Different genders (male, female, non-binary)
- Different age groups (18-25, 26-35, 36-45)

**Metrics**:
- Moderation false positive rate by demographic
- Screening sensitivity by demographic
- Disparate impact ratio (should be <1.25)

**Tools**: Custom bias analysis scripts

**Success Criteria**: No demographic group has >1.25x higher false positive rate

---

#### 4.5 AI Performance Benchmarking
**Focus**: Track AI accuracy over time

**Metrics**:
- Moderation accuracy (true positives / total violations)
- False positive rate (blocked legitimate messages / total messages)
- False negative rate (missed violations / total violations)
- Screening sensitivity (detected crises / total crises)
- Screening specificity (true negatives / total non-crises)

**Frequency**: Weekly in Phase 2, Daily in Phase 3

**Tools**: Custom analytics dashboard

---

### 5. Load Tests
**Focus**:
- Phase 2: 100 concurrent users
- Phase 3: 1000 concurrent users
- Phase 4: 5000 concurrent users

**Scenarios**:
- Spike test: 0 → 1000 users in 1 minute
- Soak test: 500 users for 2 hours
- Stress test: Increase load until system breaks

**Metrics**:
- p95 latency for message delivery (<2 sec)
- p99 latency for AI moderation (<1 sec)
- Error rate (<0.1%)
- Throughput (messages/second)

**Tools**: Artillery, k6, Locust

---

### 6. Security Tests

#### 6.1 Authentication & Authorization
- Attempt to access other user's sessions
- Attempt to bypass age verification
- JWT token manipulation
- Session hijacking attempts

#### 6.2 Data Protection
- TLS enforcement (reject non-TLS connections)
- Encryption at rest verification
- PII leakage in logs, error messages, API responses
- SQL injection (though using DynamoDB)

#### 6.3 Rate Limiting
- Exceed message rate limit (10/min)
- Exceed API rate limit (100/min)
- DDoS simulation

#### 6.4 Anonymity Breaches
- Attempt to correlate users across sessions
- Attempt to extract phone numbers from hashes
- Timing attacks to identify users

**Tools**: OWASP ZAP, Burp Suite, custom scripts

**Frequency**: Before each production deployment

---

### 7. Accessibility Tests (Phase 4)
**Focus**:
- Screen reader compatibility (NVDA, JAWS, VoiceOver)
- Keyboard navigation (no mouse required)
- Color contrast (WCAG AA standards)
- Audio narration latency (<3 sec)
- Voice input accuracy (>90% for Hinglish)

**Tools**: axe, Lighthouse, manual testing with assistive tech

**Success Criteria**: WCAG 2.1 Level AA compliance

---

### 8. End-to-End Tests
**Focus**:
- Complete user flows across multiple devices
- Multi-user scenarios (2 groups, 12 users total)
- Error recovery scenarios

**Test Cases**:
- Happy path: Register → lobby → session → post-session
- Network failure: Disconnect mid-session → reconnect
- AI failure: Bedrock down → graceful degradation
- Lobby timeout: Wait 30 min → switch topics
- Cross-topic merge: 2 small lobbies → 1 merged group

**Tools**: Cypress, Playwright

**Frequency**: Before each release

---

### 9. Chaos Engineering (Phase 3)
**Focus**: System resilience under failure conditions

**Experiments**:
- Kill Bedrock API (simulate 100% failure rate)
- Throttle DynamoDB (simulate capacity limits)
- Introduce network latency (500ms, 1000ms, 2000ms)
- Partition network (split users across regions)
- Kill Lambda functions randomly

**Tools**: AWS Fault Injection Simulator, Chaos Monkey

**Success Criteria**: System degrades gracefully, no data loss

---

### 10. User Acceptance Testing
**Focus**:
- Real users test in controlled environment
- Collect qualitative and quantitative feedback

**Phase 1**: 20 users (friends, family)
**Phase 2**: 100 beta users (college students, working professionals)
**Phase 3**: 1000 early adopters

**Metrics**:
- User satisfaction score (1-5 scale)
- Session completion rate (>50%)
- Return user rate (>30%)
- Net Promoter Score (NPS)

**Feedback Collection**:
- Post-session surveys
- In-app feedback forms
- User interviews (10-15 users per phase)

---

### 11. Regression Testing
**Focus**: Ensure new changes don't break existing functionality

**Strategy**:
- Run full test suite on every PR
- Automated regression tests in CI/CD pipeline
- Manual smoke tests before production deployment

**Tools**: GitHub Actions, Jenkins

---

### 12. Performance Regression Testing
**Focus**: Ensure performance doesn't degrade over time

**Metrics**:
- Baseline performance in Phase 2
- Track p95 latency, error rate, throughput weekly
- Alert if metrics degrade >10% from baseline

**Tools**: CloudWatch, custom dashboards

---

## Phase-Specific Testing Focus

### Phase 1 (Hackathon):
- Manual testing only
- Focus on demo scenarios
- No automated tests

### Phase 2 (MVP):
- Unit tests (>80% coverage)
- Integration tests (all APIs)
- Property tests (P1-P8)
- AI-specific tests (Hinglish, adversarial, basic bias)
- Load tests (100 users)
- Security tests (auth, encryption, PII leakage)
- E2E tests (happy path + error scenarios)
- UAT with 100 beta users

### Phase 3 (Enhanced AI):
- Expand AI tests (cultural sensitivity, advanced bias)
- Add chaos engineering tests
- Add performance regression tests
- Expand load tests (1000 users)
- Weekly AI performance benchmarking
- UAT with 1000 early adopters

### Phase 4 (Audio):
- Add accessibility tests (WCAG 2.1 AA)
- Add audio quality tests (latency, clarity)
- Add speech recognition accuracy tests (Hinglish)
- Expand load tests (5000 users)
- UAT with diverse accessibility needs

---

## Deployment Strategy

### Phase 1:
- Single AWS account (dev)
- Manual deployment
- No CI/CD

### Phase 2:
- Separate environments (dev, staging, prod)
- CI/CD pipeline (GitHub Actions)
- Blue-green deployment
- Automated rollback on errors

### Phase 3:
- Canary deployments (10% → 50% → 100%)
- Feature flags for gradual rollout
- A/B testing infrastructure

### Phase 4:
- Multi-region deployment (India regions)
- Auto-scaling based on load
- Disaster recovery plan

---

## Monitoring & Observability

### Metrics to Track:
- User metrics: DAU, MAU, session completion rate, return rate
- Performance: p95 latency, error rate, uptime
- AI metrics: moderation accuracy, false positive rate, screening sensitivity
- Business: groups formed per day, messages sent, crisis resources accessed

### Tools:
- CloudWatch for logs and metrics
- X-Ray for distributed tracing
- Custom dashboards for AI performance
- PagerDuty for alerts

### Alerts:
- Error rate >1%
- p95 latency >3 seconds
- AI service failure
- High-risk user flagged

---

## Open Questions & Risks

### Open Questions:
1. How to handle Hinglish in Bedrock models? (Test with Claude/Llama)
2. What's the optimal AI intervention frequency? (A/B test in Phase 3)
3. How to prevent user re-registration after ban? (Device fingerprinting?)

### Risks:
1. **AI accuracy for Hinglish**: Mitigation: Fine-tune models, use Indian datasets
2. **User adoption**: Mitigation: Partner with colleges, NGOs for initial users
3. **Human supervisor capacity**: Mitigation: Start small, scale gradually
4. **Cost of Bedrock API**: Mitigation: Optimize prompts, cache responses, monitor usage

---

## Success Metrics by Phase

### Phase 1:
- Demo works for 2 groups of 6 users
- Basic moderation blocks obvious violations

### Phase 2:
- 100 concurrent users
- AI moderation accuracy >85%
- <2 second message delivery
- 50% session completion rate

### Phase 3:
- 1000 concurrent users
- AI moderation accuracy >95%
- AI screening sensitivity >90%
- 5% proactive human audits completed

### Phase 4:
- Audio narration with <3 second latency
- Voice input accuracy >90%
- WCAG 2.1 Level AA compliance
