Automation Recommendations
==========================

 

<br>Automation Goal
-------------------

 

Automation should reduce release risk and execution time without pretending that
every AI behavior can be asserted perfectly.

For this product, the first automation targets should be deterministic
workflows, persistence checks, and release blockers.  


Automate First
--------------

 

High-value candidates:  
- install / launch / reach chat  
- first-run flow sanity  
- model download state visibility  
- send prompt / receive non-empty response  
- settings save / persistence after restart  
- thread create / switch / persistence  
- permission prompt invocation checks  
- force close / reopen persistence checks

These form the backbone of a reliable build-verification pipeline.  

 

Automate Next
-------------

 

Once the product and UI are stable:  
- integration token field validation  
- model switching flows  
- repository / indexing state transitions  
- offline mode sanity behavior  
- regression around background / foreground handling  

 

Keep Partly Manual
------------------

 

Some areas should remain manual or exploratory-heavy:  
- response quality judgment beyond simple sanity prompts  
- image analysis nuance  
- dictation quality in real acoustic conditions  
- UX confusion in onboarding  
- low-storage, interruption, and recovery nuance across OEM behavior  

 

Exploratory Focus Areas
-----------------------

 

Where I would spend manual exploratory time:  
- onboarding clarity  
- trust and privacy perception  
- permission dead ends  
- state corruption after interruptions  
- long-session stability  
- model switching under load  
- retrieval quality consistency  

 

CI / Release Pipeline View
--------------------------

 

A practical rollout would be:  
1. **PR / build stage:** smoke automation  
2. **release candidate stage:** RVS automation + targeted manual checks  
3. **milestone / pre-major-release stage:** deeper regression, exploratory, and
device-matrix expansion

