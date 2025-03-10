#############################
Science Verification workflow
#############################

.. abstract::

   This TN is a guid trough the science verification (SV) Jira workflow.


.. contents:: Table of Contents
   :depth: 2
   :local:

**********
Abstract
**********
This document outlines the workflow for Science Verification (SV) Units in the Rubin Observatory commissioning phase. It details the steps involved, tools used, and integration with existing systems. A key focus of this document is on the **JIRA and Zephyr Scale workflows** used for tracking SV tasks, test execution, and validation.

**********
Introduction
**********
Science Verification (SV) Units are critical for assessing the performance and accuracy of Rubin's scientific workflows. This document provides a structured approach to defining, executing, and validating SV units.

**Scope:** This workflow is intended for commissioning team members, data scientists, and software engineers working on SV-related tasks.  

**Relation to other documentation:** This document complements other SITCOMTNs and DMTNs on commissioning workflows.

******************************************
Science Verification Workflow Overview
******************************************
SV units ensure that the Rubin Observatory meets its scientific performance goals. The workflow includes defining goals, acquiring data, processing it, and validating results.

***************
Workflow Steps
***************
1. **Defining Science Verification Goals**  
   - Identify key performance metrics  
   - Align with science requirements  

2. **Selecting and Preparing SV Units**  
   - Choose relevant test cases  
   - Configure necessary software and hardware  

3. **Data Acquisition & Observing Strategy**  
   - Execute planned observations  
   - Monitor real-time data collection  

4. **Data Processing & Reduction**  
   - Use LSST Science Pipelines for processing  
   - Generate quality control reports  

5. **Performance Metrics & Validation**  
   - Compare results with expectations  
   - Report anomalies and iterate on improvements  

6. **Reporting & Documentation**  
   - Summarize findings in SITCOMTNs and JIRA tickets  
   - Communicate results with relevant teams  

*************************
Tools and Software Used
*************************
- **Rubin Science Platform (RSP)** – Interactive data analysis  
- **Jupyter Notebooks** – Workflow execution  
- **EFD & Chronograf** – Engineering and telemetry monitoring  
- **JIRA** – Task tracking, issue management, and workflow coordination  
- **Zephyr Scale** – Test case management and execution tracking for SV workflows

**********
References
**********
- SITCOMTN-XXX (related documents)  
- DMTN-XXX (relevant Data Management notes)  

**********
Appendix
**********
(Optional: Include additional technical details, command-line examples, or extended discussions.)


