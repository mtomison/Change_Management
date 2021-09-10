
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
