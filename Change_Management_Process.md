
## Objectives and Scope
### Definition
ITIL defines a change as, "The addition, modification or removal of anything that could have an effect on IT Services.”

### Purpose
The purpose of the Change Control process is to maximize the number of successful IT changes by assessing risks properly, authorizing changes to proceed, and then managing a change schedule.  You need to balance the need to make beneficial changes that will deliver additional value with the need to protect customer and users from the adverse effect of changes. (von Schlag & Perry, 2019)

### Objectives
The objectives of the Change Control process at UMB are:

- Establish and maintain a standard process and tool for managing changes
- Right-size the approval process based on the level of risk
- Improve communications regarding changes
- Provide greater visibility into the Change Calendar
- Capture metrics and lessons learned to continuously improve the Change Management process.

### Scope
The Change Control practice will begin when the associate is aware that a change to the Development, QA, Production, or Disaster Recovery environment may occur (as opposed to just before the change is about to be implemented). Advance awareness and creation of a change provides for:

- Better governance, prioritization and planning of work
- Early impact and conflict analysis avoid delays and rework
- Increases Change Calendar visibility
- Streamlined approval workflow

The following types of changes are in-scope of the Change Management process:

-  All hardware, operating system and software changes to data center and network infrastructure

*Note: All enterprise patches are in-scope*

All changes to enterprise applications
All Direct Data changes MUST follow the change management process
Desktop/Laptop security patching
The following types of changes are out-of-scope:

Individual Desktop/laptop changes
Service requests that aren’t considered a Change to the environment
Example: User access requests

**NOTE: Changes that must be documented are further defined in the Roles and Responsibilities section below.*

 

## Types of Changes
There are three types of changes. The definitions are:

| Type of Changes |Definition      |
|-----------------|----------------|
|Standard Change  |A low risk, pre-authorized, routine change, Well understood and fully documented, Implemented without needing additional authorization.        |
|Normal           |Using a standardized process, these changes are assessed, authorized, and scheduled. Initiation of a normal change is triggered by the creation of a change request.|
|Emergency        |Changes that must be implemented as soon as possible. Assessment and authorization is expedited. May be acceptable to defer some documentation and reduce the amount of testing. Requires a separate change authority.|

### Change Events
Please go to Change Event Creation Procedure for instructions on when and how to create a Change Event.

### Risk calculation
The risk assessment is automatic and is determined by three (3) factors.

 1. **Application Criticality**: These are CI’s with a BIA rating of 1
    through 3 or a Critical Application
 2. **Advanced Notice**: A normal change must be created at least 72 hours
    before the planned start date and time. If it is created less than
    72 hours before the planned start date and time, the change’s risk
    is elevated.
 3. **Complexity**: If there are more than 4 implementation CTASKs assigned
    to 3 or more distinct teams, AND/OR there are 10 or more teams
    assigned to validation tasks the risk is elevated.

If it is determined that the risk is too low once it has been fully populated, the risk can be elevated.  Go to Manual Elevation of Risk instructional article to learn how.
|Type of Change |Risk Calculation  |Approvals in system generated order & is it required?                         |
|----------------|-------------------------------|-----------------------------|
|Standard| Automatically low         |No Approval Required           |
|Normal - Low Risk|App BIA rating 0, 4-6, Not a critical application. Created 72+ hours before planned start date. Fewer than 3 distinct implementation teams and/or fewer than 10 validation teams. |Requester's Manager - always required. QA Management - if specific rules are triggered. Additional Approval - If added. Implementation Manager - If implementation CTASK. Change Management - always required. |
|Normal - Medium Risk |App BIA rating 1- 3, Critical application. OR Created <72 hours before planned start date. OR 5+ implementation tasks AND 3+ distinct implementation teams and/or 10+ validation teams.    |Requester's Manager - always required. QA Management - if specific rules are triggered. Additional Approval - If added. Implementation Manager - If implementation CTASK. Change Management - always required. Escalated Approvals - If rules dictate the need.
|Normal - High Risk |App BIA rating 1- 3, Critical application. AND/OR Created <72 hours before planned start date. AND/OR 5+ implementation tasks AND 3+ distinct implementation teams and/or 10+ validation teams     |Requester's Manager - always required. QA Management - if specific rules are triggered. Additional Approval - always required. Implementation Manager - If implementation CTASK. Change Management - always required. Escalated Approvals - If rules dictate the need. 
|Emergency |Not applicable.    |Requester's Manager - always required. Implementation Manager - If implementation CTASK.

### Escalated Approvals
If the change request does not meet all requirements below, **Escalated Approvals** will be required.  These approvals include  1 CIO Direct AND the Command Center / Production Support Management.

> #### Requirements
Applicable to Normal Medium and Normal High changes.

 - Change is reviewed in a minimum of 2 CAB meetings.
 - Change is planned in an approved maintenance window.
 - Change is fully approved in ONE of the 2 CAB meetings.

***Note:** For more information on CAB Meetings please see Change Advisory Board (CAB) Procedure.*

>#### Moratorium Approvals
If a change request must be implemented during a scheduled moratorium window, it will require 1 ETS Direct AND the Command Center Approver.

## Change State Model
|Change State |Definition | Applicable Change Types
|----------------|-------------------------------|-----------------------------|
|New| The change request is not yet submitted for review and authorization.         |All
|Assess |Requested by Manager review and technical approval of the change details are performed during this state. | Normal
|Authorize |Additional Approvers, QA Managers, Implementation Managers, Change Managers provide final authorization and scheduling of the change during this state. If there are escalated approvals, these will happen in this state. | Normal, Emergency
|Scheduled |The change is fully approved and authorized and is waiting for the planned start date. | All 
|Implement |The planned start date and time has approached and the actual work to implement the change is being conducted. | All |
|Review | Work is completed and validation to determine success is performed. | All |
|Closed | All review work is complete, and the change is closed. | All |
|Canceled | A change can be canceled at any point, except Closed state, when it is no longer required. | All

### Change Form Fields
#### Main Form Fields

> Number
> - The change number, which is automatically assigned by the system. *This information is added to the approval request emails.*   
> - Required, automatically populated.

> Requested by
> - Automatically populated with whomever was logged in and created the Change Request, but can be modified. _This information is added to the approval request emails._
> Required, automatically populated and editable.

> Category
> - A drop-down field with predefined options. Other fields may become required, depending on what is selected here.  _**Note**: Selecting Enterprise Applications and Mainframe will require additional fields to appear._
>  -- **Is a code change involved?**
>  -- **Is a direct data change involved?**
>  - Required

> Is a code change involved? 
> - A yes / no question. If yes, **Code Language, Has a code scan been completed and results attached?, Technical Peer Reviewer** must be answered.
> - Required if Category = Mainframe or Enterprise Applications

> Is a direct data change involved?
> - A yes / no question. If yes, Direct Data Change Reviewer must be populated.
> - Required if Category = Mainframe or Enterprise Applications

> Is CI record update required?
> - A drop-down field that, if yes is selected, creates a CTASK to update the CI record with the modifications from this change.
> - Answer ‘Yes’ if there is any change to the overall configuration of this CI including, but not limited to, version or the relationships. ***Note**: The resulting CTASK is a documentation task and is not required to be completed before closing your change.*
> - Required

> Elevate Risk Calculation
> - A checkbox that will allow the manual elevation of the risk of a change.  The risk can only be raised, not lowered.
> - Not required

> Approval Status
> - Indicates where the change is in the approval workflow.
> - Required, Automatic

> State
> - Change state that indicates where the change is in the overall change workflow.
> - Required, Automatic

> Assignment Group
> - The group responsible for coordinating change activities with this record. This team may or may not be the implementers as well. *This information is added to the approval request emails.*
> - Required

> Assigned to
> - The individual responsible for coordinating the change activities related to this record. This individual may or may not have implementation activities as well. Responsible for transitioning the change to the Implement and Review states by clicking on the Implement and Review buttons. 
> - Required before implementation

> Short Description
> - A brief description of the change. *This information is added to the approval request emails.*
> - Required

> Description
> - A more in-depth description of the change in layman’s terms. *This information is added to the approval request emails.*
> - Required

> Justification
> - A reason for this change, what is driving it. Also, if this record is requiring escalated approvals, answer why. *This information is added to the approval request emails.* 
> - Required

> Parent
> - This is where you add the Project number, RITM, Incident or Problem record that is driving this change. 
>- No

> Payment Card Industry (PCI) Questions
>- Questions that identify whether a change will require actions to secure the environment.
>-- Is this change expanding the existing CDE (CAT1/2) environment?
>-- Does this change apply to a CDE (CAT/2) edge security device or appliance?
>-- Does this change upgrade the first digit of a CDE app, OS, or device firmware?
>- Required

#### Schedule and Planning tabs
> Schedule – Planned start date (yyyy-MM-dd HH:mm:ss)
> - This is the planned start date and time you are requesting to perform this change. *This information is added to the approval request emails.*
> - Required

> Schedule – Planned end date (yyyy-MM-dd HH:mm:ss)
> - This is the planned end date and time you expect activities to end. *This information is added to the approval request emails.*
> - Required

>Schedule – Actual start date (yyyy-MM-dd HH:mm:ss)
>- This is the actual start date and time you performed the change. 
>- Required, Automated & Editable

> Schedule – Actual end date (yyyy-MM-dd HH:mm:ss)
>- This is the actual end date and time you performed the change.
>- Required, Automated & Editable

> Planning – Backout plan
>- Enter steps to revert the change to its state prior to implementation. Include information regarding when the change can be backed out during implementation and if the change window includes time to backout.
***NOTE**: This can reference an attachment, but you must add the attachment.* 
*Answers the question, **"What is the back-out plan and has it been tested?"***
>- Required

> Planning – Change plan
> - Detailed implementation steps. 
***NOTE**: This can reference an attachment, but you must add the attachment. Answers the question, "**What is the implementation plan and has it been tested?"***
>- Required

> Planning – Test plan
>- Required information:
--Requirement
--Process/Function/Component to test
--Testing steps
--Expected Result Description
--Name of Tester
--Actual Result Description
--Date and Time
--Pass or Fail
***NOTE**: This can reference an attachment, but you must add the attachment.*
*Answers the question, "**Was testing conducted**?"
>- Required

> Planning – Validation Plan Template
> - Link to the Validation Plan templates.
> - Not required, but must have something attached or in the **Validation plan** field below it. Selection creates validation tasks

> Planning – Validation Plan
> - Required information:
> --Requirement
--Process/Function/Component to test
--Testing steps
--Expected Result Description
--Name of Tester
***NOTE**: This can reference an attachment, but you must add the attachment.*
>- Required if no **Validation Plan Template** is selected.

#### Change Task, Approvers, et al Tabs at the Bottom
> Change Tasks
> - Tasks related to this change.
> --Planning – Actions taken to prepare for an upcoming change
--Testing – Testing activities done BEFORE the implementation of the change
--Review – Review activities done by code reviewers, direct data reviewers, and PCI reviewers
--Documentation – Any updates to documentation, including updates to Configuration Items
--Implementation – Actions taken DURING the planned implementation window necessary as part of the change. This task type MUST be added before requesting approval. 
>- Not required

> Approvers
> - All approvers and their decisions are recorded here.
> - Required, Automated & Editable

> Requested Items
> - RITM records related to this change must be added here.
> - Required if related to RITM

> Problems
>- Problem records related to this change must be added here.
>- Required if related to Problem

>Incidents
>- Incident records related to this change must be added here.
>- Required if related to Incident

> Incident Caused By
> - Incidents caused by this change must be added here. If a validation task is failed, the resulting incident is automatically added here.
>- Required if change caused an Incident

> Releases
>- Release records related to this change must be added here.  Typically, we do not use releases, so this won’t be populated.
>- Not required, we don't typically use this tab.

> Child Changes
>- Child Change records are changes done in lower environments as part of the development and testing prior to Production implementation.
>- May add QA or Dev changes related to this change

>Affected CIs
>- CIs that may be or will be affected by this change. If you mention in the description any CI, application, etc., you should add them here.
*Answers question, "**What infrastructure / applications COULD be impacted?**"
>- Required if multiple CI’s affected

>Impacted Services/CIs
>- These are business services that may be impacted by this change. These are typically the top critical applications.
*Answers question, "**What business partners or customers COULD be impacted?**"
>- Required if any services are impacted

>CAB Agenda Items
>- This records which CAB(s) a change is reviewed.
>- Automated

>Task SLAs
>- There is where you can find where the change record is in the closure process and whether the SLA for closing a change has been met or exceeded.
>- Automated

> Validation Tasks
>- Tasks for users to record their validations after a change has been completed.
>- Not required, Automated & Editable

### Roles and Responsibilities
> Change Requester
>- Open a new change record
>- Fill in initial required fields
>- Review change in CAB
>- Add additional affected CIs
>- Add Test results, validation plans, implementation plans, & back out plans
>- Add all implementation CTASKs
>- Enter the planned start and end dates
>- Add any non-implementation CTASKs
>- Adding stakeholders to the Watch List to communicate status of the change
>- Submit change for approval
>- Consulting with Lines of Business to identify potential customer impact

> Approvers
>- Change Requester’s Manager Approval
>- Assignment Group’s Manager Approval
>- Quality Assurance Approval
>- Additional Approval
>- Implementation Manager Approval
>- Change Manager Approval
>- CIO Direct
>- Command Center / Production Support Management

> Assigned To
>- Add additional affected CIs
>- Coordinating the resources that implement the change (within his or her team as well as resources that may be outside their team)
>- Add any non-implementation CTASKs
>- Adding stakeholders to the Watch List to communicate status of the change
>- Requesting CIO Direct approval, via the Change Requester Manager, for extending past the designated date/end time specified in the change and notifies stakeholders of extension after CIO Direct approval has been granted
>- Ensure change is fully approved
>- Complete the change
>- Close change within 72 hours of actual end date/time
>- Transition to Implement and Review states by clicking on the Implement and Review buttons.
>- Consulting with Lines of Business to identify potential customer impact

> Change Advisory Board (CAB) & Command Center
>- Approve change
>- Assess scheduling conflict

> Validators
>- Validate that a change worked
>- Provide validation results to Assigned To

> Assigned To’s Manager
>- Assign associate to the change record
>- If change is not successful, ensure the PIR is completed.
>- If change is an emergency, ensure the PIR is completed.
>- Discuss PIR in CAB
>- Ensuring consultation of Lines of Business for evaluation of customer impact

> Change Management team / Change Manager
>- Ensure adherence to the change process
>- Facilitate CAB meetings
>- Escalating to ETS Senior Management when an unauthorized change is discovered
>- Reporting on Change Management activities
>- Educating ETS staff on the Change Management process
>- Proposing and implementing improvements to the Change Management process

> Code and Direct Data Change Peer Reviewers
>- Review modifications to code or direct data changes to mitigate risk of malicious updates
>- If review fails, contact owner to discuss the outcome of the review

> CTASK Assigned To
>- Perform activity in Planning CTASK
>- Perform activity in Implementation CTASK
>- Perform activity in Testing CTASK
>- Perform activity in Review CTASK
>- Perform activity in Documentation CTASK

> Executive Leadership
>- Review change standard and processes
>- Review and approve requests for alternate change windows
>- Review and approve moratorium / blackout windows.

> Payment Card Industry (PCI) Significant Change Board
>- Review change identified changes for significance
>- Create PCI CTASKs
>- Manage the PCI Significant Change Process & procedures

## General Guidelines

 - All Changes that were defined as in-scope must follow the Change   
   Management process and MUST be recorded in an approved Change   
   Management tool.

- Implementation Windows are recorded in the Change Management tool as well as in the Knowledge Base article KB0013433
- Changes SHOULD NOT exceed 24 hours (from Planned start date to Planned end date) unless it is a parent to child changes.
- Changes SHOULD explain the work that is being done in significant detail to understand the potential impact to the environment and the value it will bring to the business.
- Moratoriums are scheduled annually and as needed.
- Incidents caused by a Change MUST be linked to the appropriate Change Record.
- If a Change Request requires multiple discrete deployments that span multiple timeframes, each deployment MUST be represented as its own Change Record that is linked to the Parent Record. Parent records can be Projects, Requested Items, Incidents, Problems, or other Changes.
- If a Change Request requires multiple Assignment groups to make changes within the same timeframe, each team’s deployment MUST be represented as its own Change Task Record that is linked to the overall Change Record.
- Standard changes are added to the standard change catalog by gaining appropriate approvals. The Standard Change Catalog is used as a central repository to retain approved Standard Changes. They have little to no impact to the production environment. Approved Standard changes can be implemented at a time when deemed best by all stakeholders involved.
- Any Standard Change may be re-evaluated at any time, and possibly, removed, if it results in an Incident.
- Annual review of Standard Changes MUST be performed by Management. Please see KB00014854 Standard Change Template Review Procedure
- A Change MUST be associated with at least one Configuration Item (CI). If a change affects multiple CIs, those CIs MUST be added to the Change Record in the Affected CIs tab.
- If the CI(s) in the Affected CIs tab are being modified due to your implementation, the CI record(s) should be modified within the CI record before closure.
- When a change deployment will go past the designated Planned End date/time specified in the change record, and/or outside the implementation window, ETS Direct approval is required.
- A few examples of reasons for this occurring may be:
-- Unexpected delays occurred prior to, or during implementation of the change
Or –
-- The change may be past the point where back out cannot occur and the change MUST proceed
- Process for requesting date/time extension:
-- The Manager must be notified, made aware of the projected end time, make sure that no other resources conflict with the extended end time, and then gain ETS Direct approval.
-- The Change Requester or Change Requester Manager MUST communicate the unanticipated issues with the Stakeholders.
- Upon closure of the change record, accurate Actual start, and Actual end dates/times should be specified, along with the reason for the time extension and the name of the person/persons that approved the extension.
- All changes, except for Emergency change type, should be tested prior to implementation and the results of your testing documented in the change record. There are times when testing cannot be performed (Examples: A testing platform is not available, the change that is being implemented is only accurate with Production data, or, a third-party Vendor is implementing the change(s) and they are responsible for testing). When pre-implementation testing is not possible, the reason why it is not possible must be stated in the Test plan section of the change record.
-- The testing information in changes must be clear, as directly accessible as possible, current, complete and understandable. 
-- The test information is critical enough that the sections in the Change Request form under Planning have sections specifically reserved for including it.  
-- Test result documentation from the change requesters, Assigned To associate, QA teams and business validators should be included in the Planning section of the form or attached to the change request whenever it is possible to do so.
-- If attached, the test information should be distinct from other documentation.
- The purpose of pre-implementation testing is:
-- To verify that the changes you are implementing function according to the expectations defined by the requirements and/or specifications
-- To uncover situations that could negatively impact the customer or usability
-- To ensure you don’t “break” anything that is currently in production
-- Ensure your change(s) are successful when you implement in production
- Change Requester selects additional approvers based on the person(s) that have knowledge of, might be required to participate in, and could potentially be impacted by the change.
- The Change Management policy MUST be approved by the CIO annually.
- Associates who fail to comply with the Change Management Process or other Company policies may be subject to disciplinary action, up to and including termination.
- For changes that require Code/Peer reviews, the individual listed as the reviewer shall contact the requested by individual listed in the change and discuss the outcome of the review in addition to adding work notes into the code review change task. At that time, they may determine that an additional review may be needed and/or determine the upcoming change should be delayed or even cancelled as a result.
- Post Implementation Reviews MUST be completed within five (5) days from when the change is closed.
- If a fully approved change needs to be rescheduled or it is determined that further information or additional tasks need to be added to the change, the Change Manager or their alternate must be contacted, and a restart may be requested. 
- End of Day Blackouts are scheduled from 2pm to 6pm Monday through Friday.  This blackout window affects normal and standard changes impacting the top applications and services and their supporting infrastructure as defined in the report Top Business Services and is only applicable to the Production environment. Development, QA/Test, and Disaster Recovery environments are exempt from this window. Emergency changes to restore a P1/P2/P3 are also exempt from this blackout window. 
