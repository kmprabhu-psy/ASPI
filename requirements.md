# Requirements Document: Anonymous Support Platform

## Context & Background

### The Indian Mental Health Landscape

India faces a significant mental health crisis with limited infrastructure to address it. According to the National Mental Health Survey (2015-16), nearly 150 million Indians need mental health care, but fewer than 30 million seek help. The country has a severe shortage of mental health professionals, with only 0.75 psychiatrists per 100,000 people (compared to the WHO recommendation of 3 per 100,000). This gap is even more pronounced in rural areas and tier-2/tier-3 cities.

### Cultural Barriers to Seeking Help

In Indian society, mental health challenges carry significant stigma. Discussing psychological struggles is often seen as a sign of weakness or a family matter to be kept private. Key cultural barriers include:

- **Family Honor (Izzat)**: Mental health issues are perceived as bringing shame to the family, particularly affecting marriage prospects
- **Collectivist Culture**: Individual struggles are often suppressed to maintain family harmony and avoid burdening others
- **Generational Expectations**: Pressure to fulfill parental expectations in education, career, and marriage creates immense stress but little room for open discussion
- **Gender-Specific Pressures**: Women face additional barriers due to patriarchal norms, while men are expected to be stoic and not show vulnerability
- **Lack of Awareness**: Mental health literacy is low, with many unable to recognize symptoms or understand that help is available
- **Economic Constraints**: Professional mental health services are expensive and often not covered by insurance, making them inaccessible to most

### Why Anonymity is Crucial in the Indian Context

Anonymity addresses several India-specific barriers:

1. **Stigma Reduction**: Users can discuss struggles without fear of social judgment or family discovery
2. **Safe Exploration**: People can explore whether they need help without committing to formal therapy
3. **Peer Connection**: Realizing others face similar challenges (exam pressure, arranged marriage stress, workplace discrimination) reduces isolation
4. **Language Comfort**: Supporting Hinglish allows natural expression without formal English barriers
5. **Accessibility**: Free, anonymous support reaches those who cannot afford or access professional services
6. **Bridge to Care**: Gentle guidance toward professional resources when needed, without forcing immediate commitment

### Platform Mission in Indian Context

This platform serves as a critical bridge between India's mental healthcare infrastructure and the millions who are uncertain if they need professional help. By providing anonymous peer support combined with AI-powered guidance, the platform:

- Reduces the barrier to seeking initial support
- Helps users realize they are not alone in their struggles
- Provides culturally-sensitive facilitation that respects Indian communication norms
- Guides users toward appropriate professional resources when patterns indicate need
- Enables the limited pool of mental health professionals to reach and support masses through AI assistance
- Creates a safe space for exploring mental health concerns without family or social discovery

## Stakeholders & Personas

### Primary Stakeholders

1. **Users**: Individuals seeking peer support for mental health and life challenges
2. **Human Supervisors**: Trained mental health professionals monitoring risk cases
3. **Platform Administrators**: Teams managing feedback, moderation, and platform operations
4. **Mental Health Organizations**: Partners providing crisis resources and professional referrals

### User Personas

#### Persona 1: Priya - Engineering Student (19, Bangalore)

**Background**: Second-year engineering student at a tier-1 college, living in a hostel away from family in a small town in Uttar Pradesh.

**Challenges**:
- Intense academic pressure and fear of failure
- Parental expectations to secure high-paying job to support family
- Imposter syndrome among high-achieving peers
- Anxiety about placements and future
- Difficulty sleeping before exams

**Barriers to Seeking Help**:
- Parents would be "disappointed" if they knew she was struggling
- Worried friends would judge her as weak
- Cannot afford private therapy on student budget
- Doesn't know if her stress is "serious enough" for professional help

**Platform Needs**: Anonymous space to discuss exam stress, connect with others facing similar pressure, learn coping strategies, and understand when professional help might be needed.

#### Persona 2: Rahul - Software Engineer (28, Pune)

**Background**: Works at a startup with long hours, recently moved to Pune for job, living alone for the first time.

**Challenges**:
- Burnout from 60-hour work weeks and "hustle culture"
- Pressure to switch jobs for higher salary to support parents
- Loneliness and isolation in new city
- Parents pressuring him to agree to arranged marriage
- Feeling stuck between personal desires and family expectations

**Barriers to Seeking Help**:
- "Men don't talk about feelings" cultural norm
- Worried colleagues would see him as unable to handle pressure
- Therapy is expensive and he's sending money home
- Doesn't want to worry his parents

**Platform Needs**: Anonymous outlet to discuss work stress and family pressure, connect with others navigating similar life transitions, explore feelings without judgment.

#### Persona 3: Anjali - Homemaker (32, Jaipur)

**Background**: Married for 5 years, living in joint family with in-laws, has a 3-year-old daughter.

**Challenges**:
- Feeling isolated and undervalued as homemaker
- Constant criticism from mother-in-law
- Husband works long hours, limited emotional support
- Lost sense of identity after leaving career
- Postpartum depression that was never addressed

**Barriers to Seeking Help**:
- Cannot discuss family issues outside home (family honor)
- No financial independence to pay for therapy
- Limited privacy to make calls or attend sessions
- Worried about being labeled "difficult" or "unstable"
- Doesn't have language to articulate what she's feeling

**Platform Needs**: Safe space to express feelings anonymously, connect with other women facing similar family dynamics, validate that her feelings are real, access resources discreetly.

#### Persona 4: Arjun - College Dropout (22, Lucknow)

**Background**: Dropped out of college after failing exams, working in family business, feels like a disappointment.

**Challenges**:
- Shame about dropping out when peers are graduating
- Constant comparison to successful cousins
- Parents' disappointment and "we sacrificed everything" guilt
- Anxiety about future and feeling trapped
- Occasional thoughts of self-harm when overwhelmed

**Barriers to Seeking Help**:
- Extreme stigma around mental health in his community
- Cannot tell parents he's struggling (would add to their disappointment)
- No awareness of mental health resources
- Limited English proficiency, uncomfortable with formal settings

**Platform Needs**: Hinglish support, anonymous crisis detection and resource guidance, connection with others who feel like "failures," gentle path toward professional help if needed.

#### Persona 5: Meera - Working Mother (35, Mumbai)

**Background**: Marketing manager, married with two school-age children, managing career and household responsibilities.

**Challenges**:
- Guilt about being working mother vs. societal expectations
- Juggling demanding job with childcare and household management
- Lack of support from spouse who sees household as "her responsibility"
- Exhaustion and feeling like she's failing at everything
- Anxiety about children's education and future

**Barriers to Seeking Help**:
- No time for therapy appointments during work hours
- Worried about being seen as unable to "handle it all"
- Concerned therapy would be seen as self-indulgent
- Fear that admitting struggle would impact career

**Platform Needs**: Flexible access during odd hours, quick support sessions that fit her schedule, connection with other working mothers, validation that her struggles are real.

## Introduction

This document specifies the requirements for an AI-facilitated anonymous support platform that serves as a bridge between mental healthcare infrastructure and people who are uncertain if they need professional help. The platform enables users to connect around shared experiences through moderated discussion groups on topics such as stress, anxiety, family issues, and other personal challenges.

The platform's core mission is to:
- Provide peer support to users who may be hesitant to seek professional help
- Help users realize they are not alone in their struggles
- Guide users toward appropriate professional resources when needed
- Create a safe, supportive environment for exploring mental health concerns
- Enable human mental health professionals to reach and support masses through AI assistance

Anonymity is central to the platform's design, as it helps users feel comfortable opening up about their struggles and significantly reduces the barrier to entry for seeking support. The platform maintains human oversight wherever possible, ensuring that trained professionals remain in the loop for critical decisions while AI handles scale. Through AI-powered moderation, facilitation, and screening combined with human supervision, the platform maintains healthy, productive conversations while identifying users who may benefit from professional mental healthcare services.

## Glossary

- **Platform**: The anonymous support and discussion system
- **User**: An individual participating in support groups
- **Group**: A discussion space of 6-8 people focused on a specific topic
- **Topic**: A predefined life situation category (exam stress, work burnout, family problems, anxiety, etc.)
- **Lobby**: A waiting area for users who have selected a topic but are waiting for enough members to form a group
- **AI_Moderator**: The AI system responsible for real-time content moderation (doxing, anonymity breaches, hate speech, rude behavior, arguments)
- **AI_Facilitator**: The AI system responsible for keeping conversation flow and preventing echo chambers
- **AI_Screener**: The AI system that analyzes language patterns and uses specialized trained models to identify users at risk of mental health breakdown or crisis, and guides them to support resources
- **Risk_Dashboard**: The administrative interface for human supervisors to monitor users identified as at-risk
- **Feedback_Dashboard**: The administrative interface for dedicated teams to monitor user feedback and complaints
- **Human_Supervisor**: A trained professional who monitors the risk dashboard and oversees crisis interventions
- **Hinglish**: A hybrid language mixing Hindi and English commonly used in India
- **Code-switching**: The practice of alternating between languages within a conversation
- **Message**: User-generated content posted to a group
- **Session**: A time-bounded period of group discussion
- **Flag**: A marker indicating content that requires review or has been identified as problematic
- **Anonymity_Manager**: The system component that protects user identity

## Requirements

### Requirement 1: User Registration and Anonymous Identity

**User Story:** As a user, I want to create an anonymous profile, so that I can participate in support groups without revealing my real identity.

#### Acceptance Criteria

1. WHEN a user registers, THE Platform SHALL create an anonymous identifier for that user
2. WHEN a user registers, THE Platform SHALL verify the user is 18 years or older through self-declaration
3. WHEN a user participates in a group, THE Platform SHALL display only the anonymous identifier
4. THE Anonymity_Manager SHALL prevent exposure of personally identifiable information in user profiles
5. WHEN a user creates a profile, THE Platform SHALL allow optional demographic information without requiring identifying details
6. THE Platform SHALL generate unique anonymous identifiers that cannot be traced back to user accounts by other users
7. THE Platform SHALL provide an account deletion option accessible from user settings
8. WHEN a user requests account deletion, THE Platform SHALL follow the data removal process specified in Requirement 13

### Requirement 2: Language Support

**User Story:** As a user, I want to communicate in Hinglish naturally, so that I can express myself without language barriers.

#### Acceptance Criteria

1. THE Platform SHALL support Hinglish as the primary language (code-switching between Hindi and English)
2. THE Platform SHALL handle Devanagari script for Hindi text input and display
3. THE AI_Moderator SHALL analyze content in Hinglish for moderation purposes
4. THE AI_Facilitator SHALL generate prompts and responses in Hinglish matching the group's communication style
5. THE AI_Screener SHALL detect crisis patterns in Hinglish messages
6. THE Platform SHALL handle mixed-script conversations (Latin and Devanagari) seamlessly

### Requirement 3: User Onboarding

**User Story:** As a new user, I want to understand how the platform works, so that I can participate effectively and safely.

#### Acceptance Criteria

1. WHEN a user first accesses the platform, THE Platform SHALL display an onboarding flow explaining anonymity principles
2. THE Platform SHALL explain the roles of AI_Moderator, AI_Facilitator, and AI_Screener during onboarding
3. THE Platform SHALL present community norms including respectful communication, anonymity protection, and supportive behavior
4. THE Platform SHALL clearly communicate that the platform provides peer support, not professional therapy or medical advice
5. THE Platform SHALL explain what the platform can do (peer support, crisis resource guidance) and cannot do (therapy, diagnosis, emergency intervention)
6. THE Platform SHALL require users to acknowledge understanding of anonymity guidelines before proceeding
7. THE Platform SHALL provide examples of appropriate and inappropriate content during onboarding
8. WHEN onboarding is complete, THE Platform SHALL allow users to access topic selection
9. WHEN a returning user logs in, THE Platform SHALL skip the onboarding flow and proceed directly to topic selection
10. THE Platform SHALL provide access to onboarding materials for returning users who wish to review them

### Requirement 4: Topic Selection and Group Assignment

**User Story:** As a user, I want to select a topic relevant to my situation and be placed in a small group, so that I can connect with others facing similar challenges.

#### Acceptance Criteria

1. WHEN a user accesses the platform, THE Platform SHALL display available topics including exam stress, work burnout, family problems, anxiety, and other life situations
2. THE Platform SHALL provide a persistent "Seek Help" button on the topic selection screen for immediate access to crisis resources
3. WHEN a user selects a topic, THE Platform SHALL place the user in a lobby for that topic
4. WHEN enough users (6-8) in the lobby opt in to join a group, THE Platform SHALL create a new 40-minute session
5. WHEN more than 8 users opt in simultaneously, THE Platform SHALL form multiple groups randomly from those who opted in
6. THE Platform SHALL distribute opted-in users across multiple groups to maintain group sizes between 6 and 8 members
7. IF only 5 users opt in after 15 minutes of waiting, THE Platform SHALL allow group formation with 5 members as minimum threshold
8. THE Platform SHALL not allow users to join groups mid-session
9. WHEN a 40-minute session ends, THE Platform SHALL dissolve the group and return all members to the lobby
10. THE Platform SHALL form groups randomly for each session
11. THE Platform SHALL not persist group membership across sessions

### Requirement 5: Lobby Experience

**User Story:** As a user waiting in a lobby, I want to know my status, prepare for the session, and have control over when I join a group, so that I can participate when ready.

#### Acceptance Criteria

1. WHEN a user is placed in a lobby, THE Platform SHALL display the current number of users waiting for that topic
2. THE Platform SHALL show the number of users who have opted in to join the next group
3. WHEN new users join the lobby, THE Platform SHALL update the waiting count in real-time
4. THE Platform SHALL provide estimated wait times based on historical topic popularity and opt-in rates
5. THE Platform SHALL display maximum wait time of 30 minutes before suggesting alternative topics
6. THE Platform SHALL provide an opt-in button or mechanism for users to indicate readiness to join a group
7. THE Platform SHALL display a clear status indicator showing whether the user has opted in or is still waiting
8. WHEN enough users (6-8) opt in, THE Platform SHALL notify them that a group is forming and start the session
9. WHILE a user is in a lobby, THE Platform SHALL display topic-specific tips and conversation starters related to their selected topic
10. THE Platform SHALL provide a mood check-in feature allowing users to express their current emotional state before joining
11. THE Platform SHALL use mood check-in data to help users reflect on their state before the session begins
12. WHILE a user is in a lobby, THE Platform SHALL allow them to browse other topics or exit the queue
13. WHEN a user chooses to drop out of a lobby, THE Platform SHALL return them to the topic selection screen

### Requirement 6: Real-Time AI Moderation

**User Story:** As a user, I want AI to moderate conversations in real-time, so that the group remains safe and respectful.

#### Acceptance Criteria

1. WHEN a user sends a message, THE AI_Moderator SHALL analyze the content in real-time
2. IF a message contains doxing attempts, THEN THE AI_Moderator SHALL block the message and warn the user
3. IF a message breaches anonymity, THEN THE AI_Moderator SHALL block the message and remind the user of anonymity guidelines
4. IF a message contains hate speech, THEN THE AI_Moderator SHALL block the message and issue a violation warning
5. IF a message exhibits rude behavior or argumentative language, THEN THE AI_Moderator SHALL flag the message for post-facto review
6. WHEN the AI_Moderator flags a message, THE Platform SHALL allow it to post but mark it for asynchronous moderation
7. WHEN asynchronous moderation determines a message violates guidelines, THE Platform SHALL remove the message retroactively
8. WHEN the AI_Moderator blocks a message, THE Platform SHALL provide specific feedback about the violation
9. THE AI_Moderator SHALL process and respond to messages within 1 second to maintain conversation flow

### Requirement 7: Abuse Prevention and User Banning

**User Story:** As a platform administrator, I want to ban users who abuse the platform, so that the community remains safe and supportive.

#### Acceptance Criteria

1. WHEN a user accumulates multiple severe violations, THE Platform SHALL ban the user from accessing the platform
2. THE Platform SHALL maintain a record of banned users to prevent re-registration
3. WHEN a user is banned, THE Platform SHALL notify them of the ban and the reason
4. THE Platform SHALL allow Human_Supervisors to review and appeal ban decisions
5. THE Platform SHALL implement progressive enforcement including warnings, temporary suspensions, and permanent bans based on violation severity

### Requirement 8: AI Conversation Facilitation

**User Story:** As a user, I want AI to facilitate productive conversations, so that discussions flow naturally and avoid becoming echo chambers.

#### Acceptance Criteria

1. WHEN a conversation stalls (no messages for 3 minutes), THE AI_Facilitator SHALL introduce relevant discussion prompts or questions
2. WHEN users are only agreeing with each other for 5+ consecutive messages, THE AI_Facilitator SHALL introduce alternative perspectives to prevent echo chambers
3. WHEN a user shares an experience, THE AI_Facilitator SHALL encourage other group members to respond
4. WHEN multiple users speak simultaneously, THE AI_Facilitator SHALL help organize the conversation flow
5. THE AI_Facilitator SHALL limit interventions to maximum 1 per 5 minutes to avoid dominating the discussion
6. THE AI_Facilitator SHALL intervene only when necessary (stalled conversation, echo chamber, or to encourage participation)
7. WHEN a topic is exhausted, THE AI_Facilitator SHALL suggest related discussion angles
8. THE AI_Facilitator SHALL adapt intervention style based on group engagement level (more active groups need less facilitation)

### Requirement 9: Real-Time Messaging and Notifications

**User Story:** As a user, I want to send and receive messages in real-time, so that I can have meaningful conversations with my support group.

#### Acceptance Criteria

1. WHEN a user sends a message, THE Platform SHALL deliver it to all group members within 2 seconds
2. WHEN a new message arrives, THE Platform SHALL notify active users immediately
3. THE Platform SHALL display messages in chronological order with timestamps
4. WHEN a user is offline, THE Platform SHALL store notifications for retrieval upon return
5. THE Platform SHALL support text messages up to 2000 characters in length
6. THE Platform SHALL not support rich text formatting in messages
7. THE Platform SHALL not provide message edit functionality
8. THE Platform SHALL not provide message delete functionality
9. THE Platform SHALL display a persistent "Seek Help" button in all messaging interfaces for immediate access to crisis resources
10. THE Platform SHALL display a clearly visible exit button in all messaging interfaces

### Requirement 10: Content Moderation and Reporting

**User Story:** As a user, I want to report concerning content, so that the community remains safe and supportive.

#### Acceptance Criteria

1. WHEN a user reports a message, THE Platform SHALL flag the content for AI and human review
2. WHEN content is flagged, THE AI_Moderator SHALL assess the severity and take appropriate action
3. IF content violates community guidelines, THEN THE Platform SHALL remove the content and notify relevant parties
4. THE Platform SHALL maintain a record of moderation actions for audit purposes
5. WHEN a user accumulates multiple violations, THE Platform SHALL restrict or suspend their access

### Requirement 11: User Feedback and Complaints Dashboard

**User Story:** As a platform administrator, I want to monitor user feedback and complaints, so that I can improve the platform and address user concerns.

#### Acceptance Criteria

1. THE Platform SHALL provide a feedback dashboard separate from the Risk_Dashboard
2. WHEN a user submits feedback or a complaint, THE Platform SHALL route it to the feedback dashboard
3. THE feedback dashboard SHALL be monitored by dedicated teams responsible for platform improvement
4. THE Platform SHALL categorize feedback by type including technical issues, feature requests, and community concerns
5. THE Platform SHALL allow administrators to respond to feedback and track resolution status

### Requirement 12: Session Management and Group Lifecycle

**User Story:** As a user, I want to participate in structured discussion sessions, so that conversations have clear beginnings and endings.

#### Acceptance Criteria

1. THE Platform SHALL create 40-minute time-bounded discussion sessions for each group (based on research showing optimal engagement duration for peer support)
2. WHEN a session starts, THE Platform SHALL notify group members
3. WHEN a session starts, THE AI_Facilitator SHALL send a welcome message explaining the session structure and time for introductions
4. THE Platform SHALL allocate time at the beginning of each session for group members to introduce themselves
5. WHEN a session ends, THE Platform SHALL archive the conversation and dissolve the group
6. WHEN a session is active, THE Platform SHALL display the remaining time to participants
7. WHEN a user attempts to drop out during a session, THE Platform SHALL display a confirmation warning to prevent accidental exits
8. WHEN a user confirms they want to drop out during a session, THE Platform SHALL return them to the lobby
9. THE Platform SHALL provide a clearly visible exit button during sessions
10. THE Platform SHALL form new groups randomly for each session
11. THE Platform SHALL not maintain persistent group membership across sessions
12. WHEN a user loses network connection during a session, THE Platform SHALL allow reconnection within 5 minutes without losing session access
13. WHEN a user reconnects after network interruption, THE Platform SHALL display missed messages and allow continued participation

### Requirement 12.1: Post-Session Experience

**User Story:** As a user who just completed a session, I want to reflect on my experience and provide feedback, so that I can process what I learned and help improve the platform.

#### Acceptance Criteria

1. WHEN a session ends, THE Platform SHALL provide a reflection space for users to capture their thoughts
2. THE Platform SHALL offer optional feedback prompts about the session experience
3. THE Platform SHALL allow users to submit feedback about the session quality, AI facilitation, and overall experience
4. WHEN post-session reflection is complete, THE Platform SHALL offer options to return to the same topic lobby or switch to a different topic
5. THE Platform SHALL route session feedback to the appropriate dashboard for review
6. THE Platform SHALL not require users to complete reflection or feedback before proceeding

### Requirement 13: Privacy, Data Protection, and AI Training

**User Story:** As a user, I want my data to be protected and used responsibly, so that my participation remains confidential while the platform improves.

#### Acceptance Criteria

1. THE Platform SHALL encrypt all messages in transit using TLS 1.3 and at rest using AWS KMS
2. THE Platform SHALL rotate encryption keys automatically every 30-90 days based on data sensitivity
3. THE Platform SHALL not share user data with third parties without explicit consent
4. WHEN a user deletes their account, THE Platform SHALL remove all personally identifiable information within 7 days
5. THE Platform SHALL use crypto-shredding to destroy encryption keys and make deleted data unrecoverable
6. THE Platform SHALL retain active messages for only 24-48 hours for enhanced privacy
7. THE Platform SHALL retain anonymized session metadata (timestamps, topic, group size, engagement metrics) for 90 days for platform improvement and validation
8. THE Platform SHALL retain flagged content and moderation decisions for 30 days for human review and AI training
9. THE Platform SHALL comply with Indian IT Act 2000, DPDP Act 2023, and international regulations (GDPR, CCPA)
10. THE Platform SHALL store Indian user data within India per data localization requirements
11. THE Platform SHALL anonymize all training data to prevent identification of individual users
12. THE Platform SHALL allow users to opt out of having their data used for AI training while maintaining platform access
13. THE Platform SHALL pre-process messages to remove PII before sending to Amazon Bedrock for AI analysis
14. THE Platform SHALL use Amazon Bedrock with "no data retention" policy and India region deployment
15. THE Platform SHALL establish Data Processing Agreements (DPA) with AWS for Bedrock usage
16. THE Platform SHALL implement comprehensive immutable audit logging with 7-year retention for compliance
17. THE Platform SHALL log all security-relevant events including authentication, authorization, data access, and configuration changes

### Requirement 14: AI Pattern Screening and Crisis Detection

**User Story:** As a user, I want the system to recognize when I'm struggling and guide me to appropriate resources, so that I can get the help I need.

#### Acceptance Criteria

1. WHEN the AI_Screener analyzes a user's messages, THE Platform SHALL use specialized trained models to detect language patterns
2. THE AI_Screener SHALL identify users at risk of mental health breakdown or crisis through pattern analysis
3. IF the AI_Screener identifies a user struggling with a specific issue, THEN THE Platform SHALL display targeted support resources through popups
4. WHEN support resources are suggested, THE Platform SHALL provide actionable prompts including hotlines, professional resources, and emergency contacts
5. THE AI_Screener SHALL analyze message patterns including sentiment, topic focus, language intensity, frequency, and crisis indicators
6. THE Platform SHALL present support resources in a non-intrusive manner that respects user autonomy
7. IF crisis indicators are detected, THEN THE Platform SHALL provide immediate access to emergency resources and crisis hotlines
8. WHEN a user is identified as at-risk, THE Platform SHALL add them to the risk tracking system for human supervisor review
9. THE Platform SHALL provide persistent access to crisis resources and support connections through a "Seek Help" button available on all screens

### Requirement 15: Risk Dashboard and Human Supervision

**User Story:** As a human supervisor, I want to monitor users identified as at-risk, so that I can ensure appropriate interventions are provided.

#### Acceptance Criteria

1. THE Platform SHALL provide a Risk_Dashboard interface for Human_Supervisors to monitor at-risk users
2. WHEN a user is flagged as at-risk by the AI_Screener, THE Risk_Dashboard SHALL display the user's anonymous identifier and risk level
3. THE Risk_Dashboard SHALL show relevant context including message patterns, detected crisis indicators, and recommended interventions
4. THE Platform SHALL maintain user anonymity in the Risk_Dashboard while providing sufficient context for intervention decisions
5. WHEN a Human_Supervisor reviews a case, THE Platform SHALL record the review and any actions taken
6. THE Risk_Dashboard SHALL prioritize cases by severity and urgency
7. THE Platform SHALL alert Human_Supervisors in real-time when high-severity cases are detected
8. THE Platform SHALL allow Human_Supervisors to escalate cases to emergency services when necessary while maintaining appropriate protocols

### Requirement 16: User Insights and Progress Tracking

**User Story:** As a user, I want to track my progress and gain insights from my participation, so that I can understand my journey and growth.

#### Acceptance Criteria

1. THE Platform SHALL track user participation metrics including session attendance and engagement levels
2. THE Platform SHALL provide users with insights about their participation patterns
3. THE Platform SHALL identify positive trends in user engagement and well-being indicators
4. THE Platform SHALL present insights in a supportive and non-judgmental manner
5. THE Platform SHALL protect user privacy when generating insights by using only the user's own data
6. THE Platform SHALL allow users to opt out of progress tracking while maintaining platform access

### Requirement 17: Accessibility and Future Audio Features

**User Story:** As a user with accessibility needs, I want to understand the platform's accessibility approach, so that I know what features are available now and planned for the future.

#### Acceptance Criteria

1. THE Platform SHALL provide basic accessibility features including keyboard navigation and screen reader compatibility
2. THE Platform SHALL document current accessibility limitations in user-facing documentation
3. THE Platform SHALL plan for future audio features that narrate chat messages for accessibility
4. WHEN audio features are implemented, THE Platform SHALL provide real-time narration of chat messages
5. THE Platform SHALL prioritize text-based accessibility in the current version while planning audio enhancements

### Requirement 18: Cultural Context and Sensitivity

**User Story:** As an Indian user, I want the platform to understand my cultural context, so that I feel respected and understood.

#### Acceptance Criteria

1. THE AI_Moderator SHALL recognize and respect Indian cultural communication styles and family dynamics
2. THE AI_Facilitator SHALL adapt conversation prompts to Indian cultural contexts (family expectations, arranged marriage, joint families, career pressure)
3. THE Platform SHALL avoid imposing Western-centric mental health frameworks
4. THE AI_Screener SHALL account for Indian cultural variations in expressing distress and seeking help
5. THE Platform SHALL provide India-specific support resources including local hotlines, NGOs, and mental health services
6. THE Platform SHALL train AI models on Indian cultural datasets and Hinglish conversations
7. THE Platform SHALL recognize cultural concepts like izzat (honor), sanskar (values), and family duty in conversations

### Requirement 19: Three-Component AI System Architecture

**User Story:** As a platform administrator, I want the AI system to have distinct components for moderation, facilitation, and screening, so that each function operates effectively and can be optimized for different topics.

#### Acceptance Criteria

1. THE Platform SHALL implement three separate AI components: AI_Moderator, AI_Facilitator, and AI_Screener
2. THE AI_Moderator SHALL focus exclusively on real-time content moderation and safety enforcement
3. THE AI_Facilitator SHALL focus exclusively on conversation flow and preventing echo chambers
4. THE AI_Screener SHALL focus exclusively on pattern analysis and support resource guidance
5. THE Platform SHALL coordinate between the three AI components to provide comprehensive support without conflicts
6. THE Platform SHALL maintain clear separation of concerns between the three AI components to enable independent updates and improvements
7. THE Platform SHALL support topic-specific fine-tuning of AI_Facilitator models to optimize conversation guidance for different topics
8. THE Platform SHALL support topic-specific fine-tuning of AI_Screener models to optimize crisis detection patterns for different topics
9. THE Platform SHALL allow AI_Moderator to operate consistently across all topics while AI_Facilitator and AI_Screener adapt to topic-specific needs
10. THE Platform SHALL track performance metrics separately for each AI component and each topic to identify optimization opportunities

### Requirement 20: AI Explainability and Transparency

**User Story:** As a user, I want to understand why AI makes decisions in simple language, so that I can trust the system and learn from its guidance.

#### Acceptance Criteria

1. WHEN the AI_Moderator blocks a message, THE Platform SHALL provide a specific explanation in Hinglish of which guideline was violated and why
2. WHEN the AI_Screener suggests support resources, THE Platform SHALL explain in simple language why those resources are relevant
3. WHEN the AI_Facilitator intervenes, THE Platform SHALL explain the reason (e.g., "conversation has stalled" or "introducing different perspective")
4. THE Platform SHALL explain AI roles during onboarding in simple, non-technical Hinglish
5. THE Platform SHALL use plain language that avoids technical jargon and is accessible to users with limited technical literacy
6. THE Platform SHALL ensure all AI explanations are culturally appropriate and supportive in tone

### Requirement 21: Proactive Human Audit Sampling

**User Story:** As a human supervisor, I want to proactively audit AI quality across normal conversations, so that I can identify blind spots and improve AI performance beyond just reviewing flagged content.

#### Acceptance Criteria

1. THE Platform SHALL implement random sampling of conversations that were not flagged by AI systems to detect false negatives and blind spots
2. THE Platform SHALL sample at least 5% of all sessions randomly for human quality review regardless of AI flags
3. THE Platform SHALL provide human supervisors with tools to review AI_Facilitator quality and helpfulness in sampled conversations
4. THE Platform SHALL enable human supervisors to identify AI_Moderator false negatives where harmful content was not detected
5. THE Platform SHALL ensure random sampling covers different topics, languages (English and Hinglish), and user demographics
6. THE Platform SHALL distribute audit samples across different times of day and days of week to capture diverse usage patterns
7. WHEN human supervisors identify AI errors or blind spots during audits, THE Platform SHALL record the findings with specific context
8. THE Platform SHALL implement a feedback loop that uses audit findings to improve AI model training and detection capabilities
9. THE Platform SHALL track audit metrics including false negative rates, false positive rates, and quality scores for each AI component
10. THE Platform SHALL generate monthly audit reports summarizing AI performance issues and improvement recommendations
11. THE Platform SHALL prioritize model updates based on the severity and frequency of issues identified in human audits

### Requirement 22: AI Bias Monitoring and Fairness

**User Story:** As a platform administrator, I want to measure and prevent AI bias, so that all users receive fair and equitable treatment regardless of their demographics.

#### Acceptance Criteria

1. THE Platform SHALL track AI decision metrics broken down by user demographics including gender, region, language preference, and age group
2. THE Platform SHALL monitor AI_Moderator blocking rates across demographic groups to detect disparate impact
3. THE Platform SHALL monitor AI_Screener risk detection rates across demographic groups to identify potential bias
4. THE Platform SHALL monitor AI_Facilitator intervention patterns across demographic groups to ensure equitable facilitation
5. THE Platform SHALL calculate and track disparate impact ratios for AI decisions across protected demographic categories
6. WHEN disparate impact exceeds a threshold ratio of 1.25 for any demographic group, THE Platform SHALL flag the issue for review
7. THE Platform SHALL conduct quarterly bias audits by independent experts with expertise in AI fairness and cultural sensitivity
8. WHEN bias is detected in AI systems, THE Platform SHALL implement corrective action including model retraining, threshold adjustments, or rule modifications
9. THE Platform SHALL publish transparency reports on bias metrics at least twice per year including detection rates, disparate impact ratios, and corrective actions taken
10. THE Platform SHALL maintain a bias incident log documenting all detected bias issues, investigations, and remediation steps
11. THE Platform SHALL ensure bias monitoring covers both explicit demographic factors and proxy variables that may correlate with protected characteristics
12. THE Platform SHALL test AI models for bias before deployment using diverse test datasets representing the full user population

### Requirement 23: AI Ethics Advisory Board and Governance

**User Story:** As a stakeholder, I want an AI Ethics Advisory Board with Indian representation to provide oversight, so that AI systems are developed responsibly with diverse perspectives.

#### Acceptance Criteria

1. THE Platform SHALL establish an AI Ethics Advisory Board including users, mental health experts, privacy experts, ethicists, and cultural representatives
2. THE Platform SHALL ensure the Board includes representation from diverse Indian regions, languages, socioeconomic backgrounds, and cultural contexts
3. THE Platform SHALL grant the Board authority to review AI policies, major system changes, and ethical concerns
4. THE Platform SHALL require Board approval for major changes to AI moderation policies, screening algorithms, or data usage practices
5. THE Platform SHALL convene Board meetings at least quarterly
6. THE Platform SHALL provide the Board with access to anonymized data, metrics, and audit reports
7. THE Platform SHALL publish public reports summarizing Board meetings and recommendations at least twice per year
8. THE Platform SHALL implement a process for users to submit ethical concerns to the Board
9. THE Platform SHALL provide compensation to Board members to ensure diverse participation is not limited by economic barriers

### Requirement 24: User Appeal Mechanisms

**User Story:** As a user, I want to challenge AI decisions that I believe are incorrect, so that I have recourse when AI makes mistakes.

#### Acceptance Criteria

1. WHEN the AI_Moderator blocks a message, THE Platform SHALL provide an appeal button for human review
2. WHEN a user appeals, THE Platform SHALL route it to human supervisors for review within 24 hours
3. WHEN the AI_Screener flags a user as at-risk, THE Platform SHALL allow the user to request human review
4. THE Platform SHALL allow users to report AI_Facilitator issues (unhelpful interventions, inappropriate suggestions, culturally insensitive content)
5. WHEN an appeal is resolved, THE Platform SHALL notify the user with a clear explanation
6. WHEN an appeal overturns an AI decision, THE Platform SHALL restore the message or adjust risk status
7. THE Platform SHALL use appeal data to improve AI systems by identifying patterns in false positives
8. THE Platform SHALL track appeal metrics including volume, overturn rates, and resolution time
9. THE Platform SHALL ensure the appeal process is accessible in Hinglish with simple, clear instructions
10. THE Platform SHALL protect users from retaliation for filing appeals in good faith


## Non-Functional Requirements

### Performance Requirements

**NFR-1: Response Time**
- Message delivery latency SHALL be under 2 seconds for 95% of messages
- AI moderation decisions SHALL complete within 1 second for 99% of messages
- Topic selection and lobby updates SHALL respond within 500ms
- Risk dashboard SHALL load within 3 seconds for human supervisors

**NFR-2: Throughput**
- Platform SHALL support at least 10,000 concurrent users
- Platform SHALL handle at least 1,000 messages per second across all active groups
- Platform SHALL support at least 500 simultaneous active group sessions

**NFR-3: Scalability**
- Platform SHALL scale horizontally to accommodate user growth
- Platform SHALL automatically scale AI processing capacity based on load
- Platform SHALL support geographic distribution for Indian users across regions

### Reliability Requirements

**NFR-4: Availability**
- Platform SHALL maintain 99.5% uptime (allowing ~3.6 hours downtime per month)
- Platform SHALL implement graceful degradation if AI components fail
- Platform SHALL provide fallback mechanisms for critical safety features

**NFR-5: Data Durability**
- Platform SHALL ensure zero data loss for messages during active sessions
- Platform SHALL maintain backup systems with 99.999% durability for audit logs
- Platform SHALL implement automated backup and recovery procedures

**NFR-6: Fault Tolerance**
- Platform SHALL continue operating if individual AI components experience issues
- Platform SHALL implement circuit breakers for external service dependencies
- Platform SHALL provide clear error messages to users during service disruptions

### Security Requirements

**NFR-7: Authentication & Authorization**
- Platform SHALL implement secure authentication mechanisms
- Platform SHALL enforce role-based access control for administrative functions
- Platform SHALL implement multi-factor authentication for human supervisors

**NFR-8: Data Protection**
- Platform SHALL encrypt all data in transit using TLS 1.3
- Platform SHALL encrypt all data at rest using AWS KMS
- Platform SHALL implement message-level encryption with HMAC signatures
- Platform SHALL rotate encryption keys every 30-90 days based on sensitivity

**NFR-9: Anonymity Protection**
- Platform SHALL prevent correlation of user identities across sessions
- Platform SHALL implement technical measures to prevent doxing
- Platform SHALL audit all access to user data with immutable logs

**NFR-10: Compliance**
- Platform SHALL comply with Indian IT Act 2000 and amendments
- Platform SHALL comply with GDPR for international users
- Platform SHALL implement data residency controls for Indian user data
- Platform SHALL maintain audit logs for 7 years for compliance

### Usability Requirements

**NFR-11: Accessibility**
- Platform SHALL support keyboard navigation for all core functions
- Platform SHALL be compatible with common screen readers
- Platform SHALL maintain WCAG 2.1 Level AA compliance for text-based features
- Platform SHALL support users with slow internet connections (2G/3G)

**NFR-12: Language Support**
- Platform SHALL support Hinglish as primary language with seamless code-switching
- Platform SHALL handle Devanagari script for Hindi text
- Platform SHALL plan for future expansion to regional Indian languages (Tamil, Telugu, Bengali, Marathi)

**NFR-13: User Experience**
- Platform SHALL provide intuitive navigation requiring minimal training
- Platform SHALL complete onboarding flow in under 5 minutes
- Platform SHALL provide clear feedback for all user actions within 1 second
- Platform SHALL be mobile-responsive (works on phone, tablet, desktop browsers)

**NFR-14: Device Compatibility**
- Platform SHALL support modern web browsers (Chrome, Firefox, Safari, Edge) on desktop and mobile
- Platform SHALL be mobile-responsive and work on phone screens (320px width minimum)
- Platform SHALL function on devices with limited RAM (2GB minimum)
- Phase 3: Native mobile apps for Android 8.0+ and iOS 12+

### Maintainability Requirements

**NFR-15: Code Quality**
- Platform SHALL maintain modular architecture with clear separation of concerns
- Platform SHALL implement comprehensive logging for debugging
- Platform SHALL maintain automated test coverage above 80%

**NFR-16: Monitoring & Observability**
- Platform SHALL implement real-time monitoring of system health
- Platform SHALL track key performance indicators (KPIs) for AI components
- Platform SHALL provide dashboards for operational metrics
- Platform SHALL alert administrators of critical issues within 1 minute

**NFR-17: Deployment**
- Platform SHALL support zero-downtime deployments
- Platform SHALL implement automated rollback capabilities
- Platform SHALL maintain separate environments for development, staging, and production

### AI-Specific Requirements

**NFR-18: AI Performance**
- AI_Moderator SHALL achieve 95% accuracy in detecting policy violations
- AI_Facilitator SHALL maintain conversation engagement above 70% of session time
- AI_Screener SHALL achieve 90% sensitivity in detecting high-risk patterns
- Platform SHALL minimize false positives to avoid over-intervention

**NFR-19: AI Fairness & Bias**
- AI components SHALL be tested for bias across Indian demographic groups (region, language, caste, gender, socioeconomic status)
- Platform SHALL monitor AI decisions for disparate impact across Indian communities
- Platform SHALL implement bias mitigation strategies trained on Indian cultural contexts
- Platform SHALL provide transparency in AI decision-making

**NFR-20: AI Training & Improvement**
- Platform SHALL implement continuous learning from moderation feedback
- Platform SHALL update AI models monthly based on new patterns
- Platform SHALL maintain versioning for AI models with rollback capability
- Platform SHALL test new AI models in staging before production deployment

## Constraints & Assumptions

### Technical Constraints

**TC-1: Infrastructure**
- Platform MUST be built on AWS infrastructure for scalability and reliability
- Platform MUST use Amazon Bedrock for AI capabilities with no-data-retention policy
- Platform MUST implement serverless architecture where feasible to manage costs

**TC-2: Internet Connectivity**
- Platform MUST function on 2G/3G connections common in tier-2/tier-3 Indian cities
- Platform MUST optimize for high-latency, low-bandwidth scenarios
- Platform MUST implement progressive loading and offline-first capabilities where possible

**TC-3: Device Limitations**
- Platform MUST work on entry-level smartphones via mobile web browsers
- Platform MUST minimize battery consumption on mobile browsers
- Platform MUST keep web app bundle size under 5MB for fast loading on 2G/3G
- Phase 3: Native mobile apps MUST be under 50MB

**TC-4: Language Processing**
- Platform MUST handle code-switching between English and Hindi within single messages
- Platform MUST support Devanagari script rendering and input
- Platform MUST process informal Hinglish without requiring formal grammar
- Platform MUST recognize Indian English variations and idioms

### Regulatory & Legal Constraints

**RC-1: Data Localization**
- Platform MUST store Indian user data within India per data localization requirements
- Platform MUST implement data residency controls for sensitive information
- Platform MUST comply with evolving Indian data protection regulations

**RC-2: Mental Health Regulations**
- Platform MUST NOT provide medical advice or diagnosis
- Platform MUST clearly communicate that it is peer support, not professional therapy
- Platform MUST maintain appropriate disclaimers about limitations of AI-based support

**RC-3: Liability & Duty of Care**
- Platform MUST implement reasonable measures to detect and respond to crisis situations
- Platform MUST provide clear pathways to emergency services when needed
- Platform MUST maintain records for legal compliance and audit purposes

### Cultural & Social Constraints

**CC-1: Stigma & Privacy**
- Platform MUST maintain absolute anonymity to address mental health stigma
- Platform MUST prevent any possibility of identity disclosure to other users
- Platform MUST be accessible without requiring family knowledge or permission

**CC-2: Cultural Sensitivity**
- Platform MUST respect Indian cultural norms around family, relationships, and mental health
- Platform MUST avoid imposing Western mental health frameworks
- Platform MUST recognize diverse cultural contexts across Indian regions and communities

**CC-3: Language Barriers**
- Platform MUST accommodate users with limited English proficiency through Hinglish support
- Platform MUST support natural code-switching behavior common in Indian communication
- Platform MUST plan for expansion to major regional Indian languages (Hindi, Tamil, Telugu, Bengali, Marathi, Gujarati, Kannada, Malayalam)

### Economic Constraints

**EC-1: Affordability**
- Platform MUST be free for end users to address economic barriers
- Platform MUST minimize operational costs through efficient architecture
- Platform MUST plan sustainable funding model (grants, partnerships, freemium features)

**EC-3: Sustainability and Funding Model**
- Platform MUST establish a sustainable business model through diversified funding sources including government grants, mental health organization partnerships, corporate social responsibility programs, and optional freemium features
- Platform MUST secure funding for human supervisors, infrastructure costs, crisis resource partnerships, and ongoing AI model improvements
- Platform MUST develop contingency plans for reduced funding scenarios including prioritization of core safety features and graceful degradation of optional features
- Platform MUST maintain commitment to free access for all core features including group sessions, AI moderation, crisis detection, and support resources regardless of funding levels
- Platform MUST provide transparency about funding sources through public disclosure of major funders and partnerships
- Platform MUST ensure funding sources do not compromise user privacy, data protection, or platform independence
- Platform MUST avoid funding sources that create conflicts of interest with user welfare or platform mission
- Platform MUST plan for financial sustainability within 3 years of launch through a combination of grants, partnerships, and optional premium features
- Platform MUST maintain reserve funding equivalent to 6 months of core operational costs to ensure continuity during funding transitions

**EC-2: Resource Limitations**
- Platform MUST operate with limited human supervisor capacity initially
- Platform MUST maximize AI automation to scale with limited professional resources
- Platform MUST prioritize high-impact features given development resource constraints

### Assumptions

**A-1: User Behavior**
- Users seeking support will be willing to wait in lobbies for group formation
- Users will engage authentically when provided anonymous, safe environment
- Users will respond to AI facilitation and guidance

**A-2: Technology Access**
- Target users have access to smartphones with internet (even 2G/3G)
- Target users have basic digital literacy to navigate mobile apps
- Target users can read and write in Hinglish (mix of Hindi and English)

**A-3: AI Capabilities**
- Amazon Bedrock deployed in India region can handle Hinglish and Indian cultural context
- AI can be trained to understand Indian communication styles, family dynamics, and cultural nuances
- AI can achieve acceptable accuracy in moderation, facilitation, and screening for Indian users

**A-4: Mental Health Ecosystem**
- Indian mental health resources exist for referrals (NIMHANS, Vandrevala Foundation, iCall, Snehi, state helplines)
- Human supervisors with mental health training and Indian cultural understanding will be available
- Partnerships with Indian mental health NGOs and organizations can be established

**A-5: Regulatory Environment**
- Indian data protection regulations will allow anonymous peer support platforms
- Platform can operate within existing legal frameworks with appropriate disclaimers
- Regulations will not require medical licensing for peer support platforms

**A-6: Market & Adoption**
- There is significant unmet demand for anonymous mental health support in India
- Indian users will trust AI-moderated platform with appropriate human oversight
- Platform can achieve critical mass of users across Indian cities and towns for effective group formation

## Use Cases & Metrics

### Primary Use Cases

**UC-1: Student Seeking Exam Stress Support**

**Actor**: Priya (Engineering Student)

**Scenario**: Priya is experiencing severe anxiety before her semester exams. She's having trouble sleeping and feels overwhelmed but doesn't want to worry her parents.

**Flow**:
1. Priya discovers the platform through college peer or social media
2. She completes quick onboarding explaining anonymity and platform norms
3. She selects "Exam Stress" topic from available options
4. She waits in lobby, sees 4 others waiting, opts in when ready
5. Group forms with 7 students, 40-minute session begins
6. AI facilitator welcomes group and prompts introductions
7. Priya shares her anxiety about failing and disappointing parents
8. Other students share similar experiences, AI facilitator encourages responses
9. Group discusses coping strategies, AI prevents echo chamber by introducing alternative perspectives
10. AI screener detects Priya's sleep issues and anxiety patterns
11. Platform shows Priya popup with sleep hygiene tips and campus counseling resources
12. Session ends, Priya completes reflection and feels less alone
13. Priya returns to lobby for another session the next day

**Success Metrics**:
- Priya reports feeling less isolated (post-session survey)
- Priya learns at least one new coping strategy
- Priya is aware of professional resources if needed
- No anonymity breaches occur during session

**UC-2: Professional Experiencing Burnout**

**Actor**: Rahul (Software Engineer)

**Scenario**: Rahul is working 60-hour weeks and feeling exhausted. He's considering quitting but feels pressure to keep earning. He's never talked about this with anyone.

**Flow**:
1. Rahul finds platform through mental health awareness post on LinkedIn
2. He completes onboarding during late evening when alone
3. He selects "Work Burnout" topic
4. He waits in lobby, opts in when 6 others are ready
5. Group forms with mix of professionals from different industries
6. AI facilitator prompts discussion about work-life balance
7. Rahul shares feeling trapped between career and personal well-being
8. Others share similar struggles, AI facilitator asks about coping mechanisms
9. Group discusses boundary-setting, AI introduces perspective about sustainable careers
10. AI screener detects burnout patterns and exhaustion indicators
11. Platform shows Rahul resources about burnout, workplace mental health, and therapist directories
12. Rahul participates in 3 more sessions over 2 weeks
13. AI screener notices persistent negative patterns, adds Rahul to risk dashboard
14. Human supervisor reviews case, determines moderate risk, monitors for escalation
15. Rahul eventually books appointment with therapist from resource list

**Success Metrics**:
- Rahul engages in multiple sessions (retention)
- Rahul is identified for risk monitoring when appropriate
- Rahul takes action toward professional help
- Platform serves as bridge to formal care

**UC-3: Homemaker Feeling Isolated**

**Actor**: Anjali (Homemaker)

**Scenario**: Anjali feels undervalued and isolated in her joint family. She has limited privacy and no one to talk to about her feelings.

**Flow**:
1. Anjali discovers platform through women's WhatsApp group
2. She accesses platform on phone during afternoon when alone
3. She completes onboarding in Hinglish
4. She selects "Family Issues" topic
5. She waits in lobby, opts in when ready
6. Group forms with 8 women, various backgrounds
7. AI facilitator prompts discussion in Hinglish about family dynamics
8. Anjali shares feeling invisible and criticized by in-laws
9. Others share similar experiences with joint families and expectations
10. AI facilitator encourages sharing of coping strategies
11. Group discusses self-care, boundaries, finding support
12. Anjali feels validated that her feelings are real and shared by others
13. She returns for sessions multiple times per week
14. Platform becomes safe outlet for processing emotions

**Success Metrics**:
- Anjali successfully uses Hinglish without language barriers
- Anjali reports feeling validated and less alone
- Anjali maintains regular engagement with platform
- Privacy is maintained (no family discovery)

**UC-4: Crisis Detection and Intervention**

**Actor**: Arjun (College Dropout)

**Scenario**: Arjun is experiencing severe depression and has occasional thoughts of self-harm. He joins platform feeling hopeless.

**Flow**:
1. Arjun finds platform through online search for "feeling hopeless"
2. He completes onboarding, sees "Seek Help" button prominently displayed
3. He selects "Anxiety" topic (doesn't recognize depression)
4. He joins group session
5. During session, Arjun shares feeling like a failure and burden to family
6. AI screener detects crisis language patterns and self-harm indicators
7. Platform immediately shows Arjun popup with crisis hotlines and emergency resources
8. AI screener adds Arjun to risk dashboard with high priority
9. Human supervisor receives real-time alert
10. Supervisor reviews Arjun's message patterns and context
11. Supervisor determines high risk, prepares intervention protocol
12. Platform continues showing "Seek Help" button prominently to Arjun
13. Arjun clicks "Seek Help" and sees crisis resources with phone numbers
14. Supervisor monitors Arjun's continued participation
15. If crisis escalates, supervisor follows emergency protocol

**Success Metrics**:
- Crisis indicators are detected within 1 session
- Human supervisor is alerted within 5 minutes
- Arjun sees crisis resources immediately
- Appropriate intervention protocol is followed
- Platform maintains anonymity while enabling intervention

### Success Metrics

**User Engagement Metrics**
- Daily Active Users (DAU) and Monthly Active Users (MAU)
- Average sessions per user per week
- Session completion rate (users who stay for full 40 minutes)
- Return user rate (users who come back after first session)
- Average time from registration to first session

**Platform Health Metrics**
- Group formation time (average wait in lobby)
- Group size distribution (maintaining 6-8 members)
- Message volume per session
- User satisfaction scores (post-session surveys)

**AI Performance Metrics**
- AI_Moderator: False positive rate, false negative rate, response time
- AI_Facilitator: Conversation engagement rate, echo chamber prevention rate
- AI_Screener: Detection accuracy, false positive rate, time to detection

**Safety & Support Metrics**
- Number of users flagged for risk monitoring
- Response time for human supervisor review
- Number of users who access crisis resources
- Number of users who report seeking professional help after platform use

**Impact Metrics**
- User-reported reduction in feelings of isolation (surveys)
- User-reported increase in mental health awareness
- Number of successful referrals to professional services
- User testimonials about platform value

**Operational Metrics**
- System uptime and availability
- Average response time for messages
- Cost per user per session
- Human supervisor workload and capacity

## Scope Boundaries

### In Scope

**Core Platform Features**
- Anonymous user registration and identity management
- Topic-based group formation with 6-8 members
- 40-minute time-bounded discussion sessions
- Real-time messaging with English and Hinglish support
- AI-powered moderation for safety and community guidelines
- AI-powered facilitation for conversation flow
- AI-powered screening for crisis detection
- Risk dashboard for human supervisor monitoring
- Feedback dashboard for user complaints and suggestions
- Crisis resource guidance and "Seek Help" functionality
- User progress tracking and insights
- Post-session reflection and feedback

**AI Capabilities**
- Real-time content moderation (doxing, hate speech, anonymity breaches)
- Conversation facilitation and echo chamber prevention
- Pattern analysis for mental health risk detection
- Topic-specific model fine-tuning
- Continuous learning from feedback

**Safety & Privacy**
- End-to-end encryption for messages
- Data protection and privacy controls
- Account deletion and data removal
- Anonymity protection mechanisms
- Audit logging for compliance

### Out of Scope

**Professional Services**
- Direct therapy or counseling sessions
- Medical diagnosis or treatment recommendations
- Prescription or medication advice
- Emergency response or crisis intervention (platform guides to external services)
- Licensed mental health professional consultations through platform

**Advanced Features (Future Consideration)**
- Video or voice-based group sessions (Phase 4)
- One-on-one peer matching
- Long-term group persistence across sessions
- Scheduled sessions or recurring groups
- Direct messaging between users
- User profiles with history or reputation systems
- Gamification or rewards systems
- Integration with electronic health records
- Payment processing for premium features
- Native mobile apps (Phase 3)

**Content & Community**
- User-generated content moderation by community members
- Peer moderator or facilitator roles
- User-created topics or groups
- Public forums or open discussion boards
- Content sharing (images, videos, links)
- External integrations (social media, calendars)

**Geographic & Language Expansion (Future Consideration)**
- Additional regional Indian languages beyond Hinglish (Tamil, Telugu, Bengali, Marathi, Gujarati, Kannada, Malayalam)
- International expansion beyond India
- International crisis resources and hotlines
- Localization for countries beyond India

**Administrative Features**
- Detailed analytics and reporting dashboards
- A/B testing infrastructure for features
- User segmentation and targeting
- Marketing automation and campaigns
- Revenue management and billing systems

**Technical Infrastructure**
- Multi-cloud deployment (AWS only initially)
- On-premise deployment options
- White-label or multi-tenant architecture
- Public APIs for third-party integrations
- Native mobile apps (Phase 3)
- Mobile native apps (web-based initially)

### Explicitly Not Supported

**The platform will NOT**:
- Replace professional mental health services
- Provide emergency crisis intervention (guides to external services)
- Store or share user identifiable information with third parties
- Allow users to contact each other outside group sessions
- Maintain permanent group memberships or friendships
- Guarantee specific outcomes or therapeutic benefits
- Operate as a medical device or health service
- Provide legal, financial, or relationship counseling
- Support users under 18 years of age (initial release)
- Allow anonymous reporting to authorities without user consent
