Full Regression Coverage
========================

 

Purpose
-------

 

The Full Regression Suite is the complete validation catalog used to achieve
broad confidence in the product.

It includes:

\- happy paths

\- edge cases

\- negative scenarios

\- interruption paths

\- environment and device variation

 

Coverage Domains from the Spreadsheet
-------------------------------------

 

### 1. Install / Uninstall / Upgrade / Storage

 

Coverage includes:

\- initial install

\- first run

\- launch after restart

\- uninstall / reinstall

\- model removal expectations

\- project/document cleanup expectations

\- upgrade behavior

\- updates during download

\- low-storage handling

 

### 2. First Start Flow / Device Synchronization

 

Coverage includes:

\- base UI validation

\- exact text and option validation

\- radio button state transitions

\- navigation based on selected path

\- yes/no device sync onboarding choices

 

### 3. Main Chat

 

Coverage includes:

\- prompt entry and send behavior

\- message ordering

\- generation state handling

\- response relevance sanity checks

\- stop/cancel behavior

\- repeated sends and future recoverability

 

### 4. Settings / Models / Tools

 

Coverage includes:

\- settings entry

\- model picker dialogs

\- persistence of selected models

\- applying and discarding changes

\- inference and tool-related settings

\- category-level settings behavior

 

### 5. Threads / Projects

 

Coverage includes:

\- create, rename, switch, and delete flows

\- chat isolation between threads

\- persistence after restart

\- project-level behavior and state protection

 

### 6. Repository / RAG / Documents

 

Coverage includes:

\- indexing flows

\- repository visibility

\- document-level validation

\- retrieval sanity

\- negative and partial states around repository content

 

### 7. Integrations

 

Coverage includes:

\- connect / disconnect

\- token validation

\- error handling

\- persistence after restart

\- multi-service behavior expectations

 

### 8. Audio / Voice

 

Coverage includes:

\- whisper model selection

\- dictation start

\- transcription insertion into input

\- sending transcribed text

\- permission dependencies and failure handling

 

### 9. Attachments / Images

 

Coverage includes:

\- selecting image/file inputs

\- sending attachments

\- response handling

\- unsupported states and interruptions

 

### 10. Offline / Lifecycle / Stability

 

Coverage includes:

\- airplane mode

\- background / foreground

\- force close

\- app relaunch

\- restart persistence

\- local-model-only expectations

 

Why This Matters
----------------

 

A regression suite should be comprehensive, but still structured. The
spreadsheet demonstrates breadth across product capability areas while
preserving release-focused priority markers (`P0`, `P1`, `P2`) that can be used
for risk-based execution planning.
