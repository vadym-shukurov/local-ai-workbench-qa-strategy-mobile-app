Risk and Priority Model
=======================

 

Priority Definitions
--------------------

The spreadsheet’s **Priority Matrix** distinguishes issues by release impact,
not by technical curiosity.

 

### P0 - Release Blocker<br>

Examples:

-   app cannot function

-   data loss

-   crash in a core flow

-   core feature unusable

A P0 means the release should not ship unless explicitly accepted by leadership
under exceptional conditions.  


### P1 - Major<br>

Examples:  
- important feature broken but workaround may exist  
- severe degradation in main flow  
- settings or persistence issues that reduce confidence  
- permission or integration issues affecting major usage

A P1 usually requires careful triage against release scope and user impact.  


### P2 - Minor<br>

Examples:  
- non-critical behavior issue  
- lower-impact edge-case failure  
- UI or recovery issue with limited blast radius

A P2 should still be tracked, but typically does not block release by itself.  


How the Priority Model Supports the Suite Structure<br>
-------------------------------------------------------

### Fast Smoke<br>

Uses a tiny slice of mostly P0/P1 user journeys to reject obviously bad builds
quickly.  


### Release Verification<br>

Focuses on the highest-value and highest-risk scenarios, mostly P0/P1, with
selected P2 checks only where they are disproportionately visible or likely.  


### Full Regression<br>

Retains broad coverage across all priorities, including low-frequency edge cases
and failure paths.  


Practical Release Framing<br>
-----------------------------

A QA lead should align bug priority with product promise:  
- local AI must still feel reliable  
- model setup must be understandable  
- user state must survive common interruptions  
- permissions must not create dead ends  
- offline behavior must be transparent and safe  


Example Release Blockers for This Product<br>
---------------------------------------------

Likely P0 outcomes include:  
- app does not reach general chat after install  
- local model never becomes usable  
- sending a prompt crashes the app  
- chat history disappears after restart  
- selecting or saving a model corrupts core functionality  
- core permission flow traps the user  
- deleting or switching threads causes state loss  


Why This Model Shows QA Leadership<br>
--------------------------------------

The value is not only in the labels. The value is in how labels drive:  
- execution order  
- release gate decisions  
- communication with product/engineering  
- tradeoff discussions under schedule pressure
