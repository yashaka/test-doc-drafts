# Test Plan Draft

(based on [first Iakiv Kramarenko's draft from 2021 in GDocs](https://docs.google.com/document/d/1VFc9yfFKHXQs28divxwIaJSuN0KpgIF_jedRG1yISAg/edit?usp=sharing))

- **AS A project team WE WANT to provide product features matching business goals, requirements and corresponding stakeholders expectations SO the company business gives profit and grows 🙂**

- ## Taking Into Account ↘️

  - ### Context

    - Very early stage of adopting QA/Testing/AQA on a project
    - *TBD*
    - Challenges/Obstacles
      - *TBD*

  - ### Thinking, Supposing, Assuming

    - *(TBD – clean & elaborate the examples below)*
    - Devs don't understand why and how do unit test (Supposition)
      - Starting from basic coverage on E2E level will give faster and more broad coverage in context of Smoke/Acceptance testing
    - Investing in early automation will result in better quality in context of DevOPS, and general faster time to market

  - ### Legend (Terms used)

    - *TBD*

- ## ⬇️ Thus, We Plan Testing... ⬇️

- ## Where to? ↘️

  (~ metrics)  
  - «Bugs found after Story Status == Done» SHOULD → 0

    - by Team during regression VS End Users (~ missed bugs on PROD)
  - «Bugs found by Automation Quality Gates (AQG)» VS «False Failures (% of Flaky Tests)» VS «Manually found after»
    - *Can be also compared taking into account that not everything can be possible to automate*
  - «Average Feature Time to Market» VS «Regression Time to Market (A vs M)»:% SHOULD → 0
  - *Other to consider:*
    - Bugs per Component/Developer
      - as instrument to plan autotests coverage and focus during regression

- ## What? ↘️

  - **now (thorough)**

    - Functional
      - Form validation, i.e. all mandatory fields
      - Navigation
      - Links
      - Search and display the correct results
      - Pop-up or confirmation messages
      - Sorting
      - Create, edit, delete, and update (CRUD) tasks
      - Negative
      - *TBD (elaborate if needed)*
    - Persistence
      - **TODO**: elaborate checklist
    - Visual
      - the right color, shape, position and size
      - no overlap
      - No broken images
      - *TBD: elaborate if needed*
    - Compatibility
      - Functional / Visual
        - Platform/Devices
          - *TBD (specify)*
  - **now (trivial/light)**

    (PASSED = "kind of OK/good-enough for the first release")  
    - Performance
      - *TBD (elaborate the "kind of OK/good-enough for the first release")*
  - **later** (*TBD - define starting criteria*)

    - Performance
      - *TBD*
    - Security
      - *TBD*

- ## When? ↘️

  - (Story | Bug) Status == Testing  
    - Exploratory
    - Including corresponding Regression, if relevant
  - Code Freeze before Release

    - Scheduled Regression
      - with selected test runs specifically per components of features to be released

- ## ⬇️ How? ⬇️

  - **TLDR**: «Automated Verification, Exploratory Validation»

- ## Documenting/Tracking

  - Product-related
    - Functional Map (mind-map/diagrams)  
      - general checklists per Test Type
      - high level business logic in context of user scenarios/workflows
      - with component/features dependencies
        - *TBD (elaborate to actual tooling/impl., e.g. features deps table (=> better end to end test))*
    - Story  
      - Acceptance Criteria
      - Test Ideas / Checklists in Functional Map
      - *(TBD - elaborate if needed, e.g. ⤵)*
        - add Demos/Videos/UserDocs
        - add specific kind of tagging (per story|AC|TC|...)
          - AQA-related: automated
          - ...
    - Code  
      - Auto-tests (including pending/manual)
        - available in human-readable format via html-like reports
        - eliminating duplication between code and stories/F.-Map/TMS
          - (TBD - consider «Test Cases as A Code» as a practice)
    - Bugs (= defects found or kept after Story Status => Done)
      - Tagging the ones found by automation
      - Linking to dependencies
  - Process-related (QÆ)  
    - There is one entry point to all QÆ process-related tasks
      - *(TBD – define impl., e.g. some kind of Epic, called QÆ,  is the only one parent for everything ... Or It could be a project, a label, etc.)*
    - Story describing process practice/property, e.g. :"Devs writes E2E tests on regular basis per feature"
      (*TBD: issue type can be specified*)  
      - Once DONE, the Test Plan should be updated  
        - (*TBD: can be implemented automatically in some way or another*)
    - Task describes more or less technical work/spikes/r&d items, like framework-ish features, etc.
    - Never-ending task for "other" time logging (like meetings) – prefixed/ended with ∞ and is always in progress
    - Process or tooling problems, revealed after corresponding issue was closed – considered a QÆ bug and created in Jira as Task with "Fix " prefix
      - (*TBD: or specifically defined issue type*).
  - General  
    - Test Data Preparation/Preconditions/Setup
      - Demos/Videos
      - ...
    - Onboarding
      - ...

- ## Utilizing

  - Jira as it is, Miro for *TBD*, Google Docs for *TBD*
  - TMS: *TBD*

- ## Automating

  - ### What?

    - Functional  
      - E2E/System level
        - basic most important scenarios/workflows (high priority)
        - atomic (very low priority)
    - ...

  - ### When?

    - Develop
      - leftovers – in free from manual testing time
      - related to "fresh" features – started during Testing stage on a feature life cycle
      - *TBD*
      - ...
    - Triggered
      - [NOW] locally
      - [LATER] CI
        - ...

  - ### How?

    - #### Utilizing tools

      - E2E/System (UI/API)
        - JavaScript + Playwright stack
        - Mailinator for mails testing
        - *TBD...*

    - #### Following Guidelines & Conventions

      - *[TBD: link to README in a codebase](...)*

- ## On environments

  - *TBD*

- ## Estimating

  - on early stage of planning (issue appeared in backlog and initially brainstormed/groomed by the team)
    - in story points (relative fibonacci based values compared to reference)
      (*TBD: find out/document reference*)  
    - for rough long-term prediction, also taking into account historical data (actual hours logged, task living time)
    - we don't estimate in hours

- ## Risking on

  - Finding perfect match between Automation vs Manual, Automated Unit vs E2E
    - **Mitigation**: Doing everything in small steps/iterations, with maximum visibility and regular review/retro based on metrics collected
  - Knowledge bottlenecks
    - **Mitigation:**
      - regular knowledge sharing
      - docs/demos/videos

- ## Heading to

  **(↘️ HOW Backlog ↘️)**  
  - Metrics kept on regular basis
  - Automation E2E available from CI/CD
  - Automation E2E integrated as QG into CD PipeLine
  - 3-amigos meeting (BA, Dev, Test)  
    - «Test Design - Key Cases» syncs between Dev, Test/SDET per Story
      - reflected in DoR
  - Automating new Features E2E finished BEFORE Story Status == Done
  - Automating new Features E2E started WHEN Story Status == Development
  - Automating new Features E2E is part of Story Status == Development
  - Unit testing vs E2E detailed plan/strategy defined
  - All new Features are unit tested before Status == Done
  - All new Features are unit tested before Status == Ready for Test
  - Devs responsible for unit tests
  - Left overs are unit tested
  - Devs use E2E (analyze failures, update existing during Status == Development)
    - BE
    - FE
  - Devs write > 0 of E2E during Status == Development)
  - Devs are responsible for E2E tests coverage (Testers might help, including in context of review)
  - Automated Tests traced to Stories
  - Not-automated tests traced to Stories
  - Check-lists traced to Stories
  - No duplication in context of checklists between Stories with AC and Functional Map
  - Fully Automated Regression (~ Left overs are e2e-auto-tested)
    - Functional
      - all e2e scenarios
      - all atomic
        - unit
        - e2e
    - Visual
    - Compatibility (Visual/Functional)
    - Persistence
      - ...
  - Performance Testing Strategy defined & followed
    - ...
  - Perfect balance between Automated Unit vs E2E
  - Public beta-testing is defined & regulary executed
    - like [velas/test-us](https://github.com/velas/test-us/)
  - Security Testing Strategy defined & followed
    - *Bounty program for Security Testing*
