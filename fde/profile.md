# My FDE project: Requirements to verification trace checker

Industry: MedTech and medical devices
Started from example: design-trace-gaps
Updated: 2026-10-21

## Problem
Design engineers build the trace matrix between design inputs and verification tests by hand for the design history file, and gaps are often found late in a design review.

## Users and approver
Design engineers use it; the design quality lead reviews and approves each proposed trace link before it goes into the design history file.

## Data
Write a synthetic list of 60 design inputs and 70 verification test protocol summaries for a simple device such as a home blood pressure monitor.

## Success measure
Precision and recall of proposed links against a hand-built trace matrix; number of true gaps found.

## How I will build it
- Retrieval: Put the documents straight into the prompt, with prompt caching
- Workflow or agent: A fixed workflow: plain code with one or two model calls, and a human approval step
- Model: A frontier model through its API; keep the model name in config so it can change

Why: Using Agentic workflow and my SME understanding - goign to use Rust and Postgres along with next.js track to build it and deploy in AWS

<!-- fde-data {"project":{"industry":"medtech-devices","example":"design-trace-gaps","title":"Requirements to verification trace checker","problem":"Design engineers build the trace matrix between design inputs and verification tests by hand for the design history file, and gaps are often found late in a design review.","users":"Design engineers use it; the design quality lead reviews and approves each proposed trace link before it goes into the design history file.","data":"Write a synthetic list of 60 design inputs and 70 verification test protocol summaries for a simple device such as a home blood pressure monitor.","measure":"Precision and recall of proposed links against a hand-built trace matrix; number of true gaps found."},"updated":"2026-10-21","setup":{"answers":{"facts":"yes","size":"small","steps":"fixed","leave":"yes","volume":"low"},"recommended":{"retrieval":"Put the documents straight into the prompt, with prompt caching","flow":"A fixed workflow: plain code with one or two model calls, and a human approval step","model":"A frontier model through its API; keep the model name in config so it can change"},"why":"Using Agentic workflow and my SME understanding - goign to use Rust and Postgres along with next.js track to build it and deploy in AWS"}} -->
