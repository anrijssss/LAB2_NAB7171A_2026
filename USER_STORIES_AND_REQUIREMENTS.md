# User Stories and Requirements - MK Studio Interview with Kev

**Interviewed:** Kev, Technical Director at MK Studio  
**Date:** Interview conducted at Mr TT drinks stall  
**Projects Involved:** MU (front & back end), Stig (front & back end), TC (frozen), and others  

---

## Executive Summary
Kev is the technical specialist/guru at MK Studio, managing four active projects while dealing with resource constraints, lack of formal processes, and challenges around code quality, porting, and team coordination. The organization has a strong technological foundation but lacks the processes and resources to scale effectively.

---

## SECTION A: CURRENT STATE & DAILY ACTIVITIES

### A1: Development Process Overview

**Current Daily Responsibilities:**
- Primary focus: Coding across multiple projects (MU frontend, MU backend, Stig frontend, Stig backend)
- Technical specialist role covering game engine and menu system development
- Playing a "devil's advocate" role during game design discussions to identify edge cases

**Key Insight:** Kev was previously doing R&D on phone messaging (since 2002, ~2 years). PhoneCompany's Java implementation on mobile phones in 2002 gave MK Studio a technological advantage.

---

### A2: Game Development Focus Areas

#### A2.1 Game Engine Development
**User Story:** As a technical specialist, I need to develop game engines that are efficient and handle complex gameplay mechanics, so that games run smoothly across different phone platforms.

**Requirements:**
- Game engine must support core gameplay functionality
- Must optimize for resource-constrained mobile devices
- Must handle physics/mechanics (e.g., terrain computation)

**Current Challenge:** Game engines like Racer have computational challenges; terrain rendering causes lag on mobile phones.

---

#### A2.2 Menu System Development

**User Story:** As a technical specialist, I need menu system solutions for games, so that players can navigate and interact with game interfaces effectively.

**Requirements - Two Approaches:**

1. **Using Phone API (Standard Approach)**
   - Use PhoneCompany APIs for menu generation
   - Pros: Looks standard, easier to port across platforms
   - Cons: Less visually interesting, limited customization
   - Less tedious to implement

2. **Custom In-Game Menu System**
   - Create proprietary menu systems specific to each game
   - Pros: Looks great, can be memory-saving
   - Cons: Hard to port, tedious to develop, each game is unique
   - Cannot be automated or componentized at current stage

**User Story:** As a developer, I want menu system development to be less tedious, so that I can focus on more complex technical challenges.

**Requirements:**
- Explore opportunities to automate menu creation workflows
- Investigate componentization of common menu patterns
- Create reusable menu templates where applicable
- Document menu best practices for team use

**Current Blockers:** 
- No two games are identical, making standardization difficult
- Menu development is seen as work that interns could handle, but is currently consuming senior developer time

---

## SECTION B: PROCESS & ORGANIZATIONAL CHALLENGES

### B1: Role & Resource Allocation

#### B1.1 Role Definition
**Current State:** Kev's official title is "Technical Director" but the role was never formally defined with clear expectations.

**User Story:** As a Technical Director, I need clear role definition and responsibilities, so that I can effectively manage technical decisions and team coordination.

**Requirements:**
- Define Technical Director role expectations and scope
- Clarify decision-making authority
- Establish reporting structure
- Create role documentation

**Current Challenge:** The role title "sounded nice" at founding but lacks substance. Kev "covers the holes" by switching between projects as needed.

---

#### B1.2 Resource Constraints & Staffing

**Current Staffing Issues:**
- Understaffed situation: Originally just Kev and Ryan
- Team now larger but still stretched thin
- Ryan was pulled away from MU coding to handle Deployments (Guy couldn't do it alone)
- Guy was shifted from MU to Stig backend
- Kev ended up covering both MU frontend and backend

**User Story:** As a Technical Director, I need adequate backend coding resources, so that projects don't fall behind and developers aren't overloaded.

**Requirements:**
- **Immediate Need:** 1 additional backend coder to handle project load
- Help new hire KC get productive quickly
- Redistribute workload so one person isn't covering multiple critical areas
- Resolve porting issues that currently block development

**Strategic Goal:** Apply the Pareto (80/20) principle to identify which 20% of efforts deliver 80% of output, allowing better resource allocation.

---

#### B1.3 Internationalization & Localization

**Current State:** All development currently in English only

**User Story:** As MK Studio, I need to expand into international markets, so that we can grow revenue and reach new player bases.

**Requirements:**
- Support French language for games
- Support German language for games
- Support other European languages as appropriate
- Implement localization framework for future language additions

**Market-Specific Challenges:**
- **China Market:** Have joint venture for kakaoke game release, but difficult market penetration due to:
  - Must work through partners rather than direct distribution
  - High diversity of mobile phone platforms
  - Local brands (e.g., Ningbird company) add platform complexity
  - Current resource constraints prevent full support

---

#### B1.4 Porting & Platform Support

**Critical Challenge:** Not enough resources to support all platforms

**User Story:** As a mobile games developer, I need efficient porting processes, so that I can deploy games across multiple phone platforms without excessive rework.

**Requirements:**
- Create porting strategy and procedures
- Document platform differences and compatibility requirements
- Develop tools to assist with cross-platform deployment
- Prioritize platform support based on market analysis
- Allocate resources for porting activities

**Current Blockers:**
- China market has numerous unique platforms including Ningbird
- Menu system porting complexity (custom menus hard to port)
- Computational challenges vary by platform (e.g., terrain rendering)
- Limited team capacity to test and optimize for each platform

---

### B2: Process & Procedures

#### B2.1 Current State of Processes

**Current Procedures:**
- Only formalized process: CVS for code check-in
- No other standard procedures in place

**Why?** When team was small (just Kev and Ryan), communication was easy and procedures weren't necessary.

**User Story:** As a growing team, I need standardized development processes, so that we can coordinate effectively across multiple projects and team members.

**Requirements:**
- Create process documentation for:
  - Requirements specification format
  - Design review procedures
  - Code review procedures
  - Testing and QA processes
  - Release procedures
  - Change management

**Justification from Interview:**
- Team is expanding rapidly
- Different people working on different parts of games
- Multiple people "wearing multiple hats"
- Need "out of bounds markers" and checklists for team members who need structure

---

#### B2.2 Requirements & Specification Process

**Current State:** 
- Rudimentary specs from Axel (Vision/Design lead)
- High-level requirements only, missing implementation details
- Examples of gaps: gun attributes, distance-to-damage calculations
- Kev must identify these issues himself during coding

**User Story:** As a developer, I need detailed specifications that cover game mechanics and edge cases, so that I don't discover missing requirements mid-implementation.

**Requirements:**
- Requirements must specify:
  - Game mechanics and physics
  - Weapon/item attributes and behaviors
  - Edge case handling (e.g., "what if you throw a bomb on yourself?")
  - State machine behaviors
  - AI scenarios and responses
- Establish specification review process before coding begins
- Create specification template for consistency
- Involve technical team in design reviews to catch missing scenarios

**Key Issue:** Scenarios aren't discovered during initial design discussions. Designers often say "only you would think of that" when Kev identifies missing edge cases. This wastes coding time fixing oversights.

---

#### B2.3 Collaboration & Communication

**Current Challenges:**
- Before Larry joined, Axel's frequent absence made it difficult to finalize specs
- Team would work on "other things" while waiting for Axel
- Filled time on other projects instead of staying focused

**Role of Larry:**
- Now serves as main point of contact
- Improvements since Larry joined, but still room for improvement

**User Story:** As a team member, I need clear points of contact and communication channels, so that I can get clarification and keep projects moving forward.

**Requirements:**
- Establish clear communication protocols
- Define escalation paths for blocked decisions
- Create backup/alternate contacts for critical roles
- Implement status tracking to prevent idle time
- Regular sync meetings for multi-project coordination

**For Larger Team Needs:**
- Some team members need clear checklists and structure
- "Out of bounds markers" needed to define acceptable decisions
- Different people respond to process differently (not everyone is "dynamic")

---

### B3: Version Control & Code Management

**Current State:** Only CVS check-in procedure is formalized

**User Story:** As a development team, I need robust version control and code management practices, so that we can track changes, manage branches, and prevent conflicts.

**Requirements:**
- Maintain CVS/version control discipline
- Define branching strategy (e.g., feature branches, release branches)
- Define commit message standards
- Create code review process linked to version control
- Document version control procedures for new team members

---

### B4: Quality Assurance & Testing

#### B4.1 Testing Challenges for Mobile Games

**Current State:** No rigorous testing framework

**Historical Attempts:**
- Previously used JUnit for testing
- No good equivalent exists for J2ME
- Junit tester on SourceForge was not very good

**Fundamental Challenges:**
- Testing is different for each phone platform
- Cannot use traditional unit testing approaches in J2ME
- Code is often embedded directly into main program (not modularized) to save memory
- This makes it difficult to segregate code for testing
- Random elements in AI add complexity
- Many scenarios to test with AI involvement

**User Story:** As a QA process, I need effective testing strategies for mobile games on constrained platforms, so that game quality meets standards without excessive time investment.

**Requirements:**
- Develop platform-specific testing strategies
- Define test scenarios for AI behaviors
- Create testing procedures for physics/engine calculations
- Document platform-specific limitations and workarounds
- Establish minimal testing requirements before release

**Constraint:** Even if tools existed, there wouldn't be time for rigorous testing given current resource levels.

---

#### B4.2 Work Accuracy Verification

**Current Process:** Play and test, localized testing

**Challenges:**
- Not as easy as unit testing for business software
- Business software: methods, functions, libraries organized and accessible
- Game code: functions embedded in main program for memory efficiency
  - Makes code segregation difficult
  - Can't test components in isolation
- **Biggest blocker:** No time for thorough testing

**User Story:** As a developer, I need practical testing approaches that work within memory and time constraints, so that I can verify game functionality effectively.

**Requirements:**
- Define "good enough" testing standards for mobile games
- Create testing checklist for common scenarios
- Establish playtesting procedures
- Document known limitations and platform-specific bugs
- Create quick regression testing suite for critical paths

---

### B5: Feature Completion & Sign-Off

#### B5.1 Definition of "Complete"

**Current State:** Varies significantly

**Formal Approach (in business software):** Sign off milestones as completed

**Gaming Approach:** "Complete" only when playable

**Who Determines Completion:**
- Internal testers or beta testers provide feedback
- Feedback determines if game is "playable"
- Typically game engine done first, then menu system

**Current Problem:** Skipping stages in development

**Example Issue:** MU project
- Playability was not signed off before interface work began
- Wasted 3 weeks on GUI and components
- Root cause: Not following established procedures

**User Story:** As a project lead, I need clear completion criteria and sign-off procedures, so that development stages proceed in logical order and resources aren't wasted.

**Requirements:**
- Define completion criteria for:
  - Core game engine/mechanics
  - AI behaviors
  - Menu system/UI
  - Platform-specific optimization
  - Overall playability
- Implement sign-off process before starting dependent work
- Document main features that must be sign-off approved
- Create stage-gate process for development phases
- Establish review criteria with stakeholders before work begins

**Specific Gap:** No clear measure of when something is "complete." Need explicit feature-level sign-off.

---

## SECTION C: MARKET & PRODUCT STRATEGY

### C1: Current Market Position

**Strengths:**
- Leading mobile games developer in Singapore (self-assessed by Kev)
- Strong technological foundation from early R&D (Java on mobile in 2002)
- Critical acclaim: Slingers game received 9.5/10 from Game Axxis magazine
- Location-based gaming expertise (Slingers was one of first ever location-based games)

**Concerns:**
- Small team; easily overtaken by well-funded competitors
- Uncertainty about how long market leadership will last
- Lucas and Koei coming to Singapore (though Kev optimistic this is good)

---

### C2: Realized & Unrealized Opportunities

**Regret 1: Missed Buddy Finder Opportunity**
- Created one of first SMS-based Buddy Finder applications
- Never launched
- Now several competitors have launched similar products
- Impact: Lost first-mover advantage and market opportunity

**Regret 2: Racer Performance Issues**
- Terrain computation is laggy on both phone series
- Computationally challenging
- Game playability impacted by technical limitations
- Opportunity cost: Time spent on optimization

---

### C3: Future Potential & Vision

**Kev's Vision for MK Studio:**
"The combined skills of the developers could achieve much more than they are now, because there are no processes in place to enable them to achieve their full potential."

**Full Potential Definition:**
- Receive industry respect and kudos
- Produce "solid games" - games that are "cool"
- "Cool" = great, about fashion, hype (not easily implemented)

**Unexploited Opportunity: Location-Based Marketing**
- Slingers demonstrated location-based gaming capability
- Potential: Over-The-Air (OTA) messaging from nearby retailers
- Example: If near Burger King, their offers could beam to player
- Blocker: Not many retailers want association with killing (in context of shooting games)

**User Story:** As MK Studio, I want to realize our potential to create cool, respected games and explore innovative marketing approaches, so that we become an industry leader and maximize game success.

**Requirements:**
- Implement processes to enable full potential realization
- Develop "coolness" criteria for game design
- Explore OTA messaging implementation for location-based games
- Research retailer partnership opportunities for games that match their brand
- Create innovation pipeline for next-generation game features

---

## SUMMARY OF KEY REQUIREMENTS & PRIORITIES

### High Priority (Immediate)

1. **Hire 1 Additional Backend Developer**
   - Address resource constraint
   - Enable Kev to focus on specialization rather than covering holes

2. **Formalize Development Processes**
   - Define standard procedures beyond just CVS
   - Create requirements specification format
   - Establish design review process
   - Define stage-gate completion criteria

3. **Improve Specifications & Requirements**
   - Require detailed mechanical specifications before coding starts
   - Include edge cases and AI scenarios
   - Implement design review with technical team

4. **Define Technical Director Role**
   - Clarify responsibilities and authority
   - Establish decision-making framework

### Medium Priority

5. **Implement Quality Assurance Framework**
   - Define testing strategies for mobile platforms
   - Create testing checklists and procedures
   - Establish regression testing suite

6. **Optimize Menu System Development**
   - Investigate automation opportunities
   - Create reusable components and templates
   - Document best practices to reduce tedious work

7. **Establish Porting & Platform Strategy**
   - Prioritize platform support based on market analysis
   - Create porting procedures and tools
   - Address China market expansion challenges

### Lower Priority (Strategic)

8. **Internationalization Support**
   - Implement localization framework for French, German, other languages
   - Plan for market expansion

9. **Innovation & Market Exploration**
   - Research location-based marketing opportunities (OTA messaging)
   - Develop brand partnerships strategy
   - Create innovation pipeline

10. **Process Improvements for Scale**
    - Develop procedures for larger teams
    - Create "out of bounds" guidelines for team members needing structure
    - Implement project management tracking

---

## DOCUMENT NOTES

**Interview Method:** Informal setting (drinks stall) without prepared questions, relying on interviewer memory
**Interviewee:** Kev, Technical Director, 5 years work experience at MK Studio
**Tone:** Kev engaged but somewhat frustrated with current constraints; optimistic about potential if processes and resources improved
**Key Phrases:**
- "I cover the holes" (regarding role flexibility)
- "Under staffed" (when asked how multi-project juggling feels)
- "Cool is not easy to implement" (regarding game design aspirations)
- "We are still quite small really" (regarding market position)
