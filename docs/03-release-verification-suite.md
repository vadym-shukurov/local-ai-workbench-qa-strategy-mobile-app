Release Verification Suite
==========================

 

Purpose
-------

 

The Release Verification Suite (RVS) is the curated set of scenarios executed on
every release candidate to determine if the build is safe to ship.

It is intentionally smaller than the full regression suite. Its value comes from
high signal, not high volume.

 

Release Gate Principles
-----------------------

 

A scenario belongs in RVS when failure would:

\- block the user from entering the product

\- break the app’s core value proposition

\- create data loss or trust concerns

\- affect a critical permission or local-device workflow

\- make the release visibly unstable to end users

 

Major Areas Covered in This RVS
-------------------------------

 

### 1. Installation and First Run

 

Examples included:

\- install succeeds

\- app opens correctly on first launch

\- first-start synchronization choice is visible and actionable

\- “Get Started” path leads to the correct next screen

 

### 2. LLM Model Download and Readiness

 

Examples included:

\- model download starts automatically

\- progress, percentage, speed, and size are shown

\- network drop during download behaves safely

\- low-storage conditions are handled properly

 

### 3. Main Chat Certification Flow

 

Examples included:

\- user can send a prompt

\- sent message appears correctly

\- assistant begins generation

\- assistant response completes and is non-empty

\- sanity prompt such as `2+2?` returns a valid result

\- stop generation works and future prompts still work

 

### 4. Settings and Model Selection

 

Examples included:

\- settings panel opens

\- model picker opens

\- selected model can be changed and saved

\- selected model persists after restart

\- newly selected model responds correctly after save

 

### 5. Save Settings Validation

 

Examples included:

\- save applies changes

\- saved values persist

\- closing without save discards pending changes

 

### 6. Thread and Project Persistence

 

Examples included:

\- chat history persists after restart

\- switching threads changes visible conversation correctly

\- messages do not bleed between threads

\- renaming does not lose history

\- deleting thread removes its history

 

### 7. Permissions

 

Examples included:

\- microphone permission prompt behavior

\- allow / deny flows

\- camera permission prompt for QR scanning

\- persistence of permission behavior after restart

 

### 8. Integrations

 

Examples included:

\- integrations screen opens

\- token field validation works

\- invalid token flow is handled

\- valid connection succeeds

\- disconnect flow succeeds and persists after restart

 

### 9. Audio Transcription

 

Examples included:

\- audio transcription settings open

\- whisper model can be selected

\- whisper model persists

\- microphone dictation inserts text

\- transcribed text can be sent as a message

 

### 10. Offline and Stability

 

Examples included:

\- local chat works in airplane mode when expected

\- offline behavior when model is unavailable is controlled

\- app survives backgrounding during generation

\- app survives kill / reopen flow

 

Why These Scenarios Matter
--------------------------

 

This suite is not meant to prove every corner case. It is meant to answer one
question with confidence:

**Can a typical user install the app, get a local model ready, chat
successfully, manage settings, keep state, and trust the app under common mobile
conditions?**

If the answer is no, the release should not ship.
