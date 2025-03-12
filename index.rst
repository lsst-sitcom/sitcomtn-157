#############################
Science Verification workflow
#############################

.. contents:: Table of Contents
   :depth: 2
   :local:

**********
Abstract
**********
This document outlines the workflow for Science Verification (SV) Units in the Rubin Observatory commissioning phase. It details the steps involved, tools used, and integration with existing systems. A key focus of this document is on the **JIRA and Zephyr Scale workflows** used for tracking SV tasks, test execution, and validation. It is based on the procedures defined in the `System-level Science Performance Verification Sprint <https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/372867091/System-level+Science+Performance+Verification+Sprint>`_ (February 2025) and focuses on tracking verification tickets, managing test cases, and generating verification artifacts.

************
Introduction
************
Science Verification is critical for assessing the performance and accuracy of Rubin's scientific workflows. This document provides a structured approach to defining, executing, and validating SV requirements.

**Scope:** This workflow is intended for commissioning team members, data scientists, and software engineers working on SV-related tasks.  

**Relation to other documentation:** This document complements other SITCOMTNs and DMTNs on commissioning workflows.

**************************************
Science Verification Workflow Overview
**************************************

SV ensure that the Rubin Observatory meets its scientific performance goals. The workflow includes defining goals, acquiring data, processing it, and validating results.


Workflow Steps
==============

1. **Defining Science Verification Goals**  

   - Identify key performance metrics \  
   - Align with science requirements \
   - This step is done by the SE team

2. **Selecting and Preparing SV**  

   - Choose/Make relevant test cases, test cycles, and test plans \ 
   -  This step will be done by Keith Bechtol and Marina Pavlovic

3. **Data Acquisition & Observing Strategy**  

   - Execute planned observations  \
   - SV tickets will be chosen by the previously acquired data 

4. **Data Processing & Reduction**  

   - Use LSST Science Pipelines for processing  \
   - Make the artifacts for SV (notebooks etc) \
   - This is the main task of the SV units 

5. **Performance Metrics & Validation**  

   - Compare results with expectations  \
   - Report anomalies and iterate on improvements  \
   - This is the task of the SV units

6. **Reporting & Documentation**  

   - Summarize findings in SITCOMTNs and JIRA tickets  \
   - Communicate results with relevant teams  \
   - This is the final task of the SV units \
   - Tickets are forwarded to the SE team after this step

Verification JIRA Workflow
==========================

.. _select_verification_ticket:

Selecting a Verification Ticket
-------------------------------

- Go to the `Kanban board <https://rubinobs.atlassian.net/jira/software/c/projects/LVV/boards/904>`_ or the `SV JIRA dashboard <https://rubinobs.atlassian.net/jira/dashboards/10183>`_ and select a verification ticket in the "To Do" column or "covered" ticket respectively.
- Use the "Quick filter" feature to view only the tickets for a specific Science Unit.
- For verification tickets that might need a change request:
  - Add the "ChangeRequested" label.
  - Add comments directly to the ticket.

.. _start_work:

Starting Work on the Ticket
---------------------------

- Set yourself as the assignee using the Assignee field.
- Update the Status from "Covered" to "In Verification."
- The ticket will move to the "In Progress" column on the Kanban board.

.. _create_jupyter_notebook:

Creating the Jupyter Notebook
-----------------------------

- Navigate to the `notebooks` directory in the Git repository (see `Git repo mapping <https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/372867091/System-level+Science+Performance+Verification+Sprint>`_).
- Name the notebook as `test_LVV-T***.ipynb`, replacing `***` with the Test Case number associated with the verification ticket under "Linked issues."
- Create a new branch in the Git repository:
  - Use the branch name `tickets/lvv-****`, replacing `****` with the verification ticket number.
  - Push the notebook and create a Pull Request to commit the notebook.

.. _notebook_requirements:

Notebook Requirements
----------------------

At minimum, the notebook should include:

- Name of related requirement(s) and their specification.
- Provenance information (e.g., Butler repo, collection, dataIds).
- Results.
- Conclusion remarks with PASS/FAIL assessment for each requirement.
- Refer to the template notebook for guidance.

.. _update_ticket_status:

Updating Ticket Status
----------------------

- Update the ticket Status from "In Verification" to "SE Review."
- The ticket will move to the "In Review" column on the Kanban board.
- Systems Engineering will review and manage administrative aspects of closing out the verification.

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


