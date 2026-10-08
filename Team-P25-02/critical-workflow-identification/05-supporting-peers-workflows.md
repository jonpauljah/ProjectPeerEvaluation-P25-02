<a id="section-17"></a>

# 5. Supporting PEERS Workflows

The following supporting workflows contribute to one or more critical workflows. They are documented separately because they are enabling behaviors rather than independent primary user goals. Their required preservation is determined by the critical workflows they support.

| ID | Supporting Workflow | Supports | Why It Matters | Preservation Expectation |
| --- | --- | --- | --- | --- |
| SW-01 | CSV Parsing and Roster Validation | CW-03 | Processes supported roster input into usable student data and prevents malformed input from undermining the roster workflow. | Preserve the parsing/validation behavior required for supported roster uploads. |
| SW-02 | Application Data Persistence and Relationship Consistency | CW-02 through CW-09 | Stores course, roster, team, evaluation, and response data in MongoDB and maintains relationships required by later workflows. | Preserve correct persistence and the data relationships required by the critical workflow chain. |
| SW-03 | Rubric / Evaluation Configuration | CW-05 and CW-08 | Supports preparation of the evaluation activity and the fields students complete during peer evaluation. | Preserve the configuration behavior required by the currently supported evaluation workflow. |
| SW-04 | Evaluation Reminder Distribution | CW-07 and CW-08 | Provides follow-up messages to incomplete students using the configured email service. | Preserve supported reminder behavior where it is part of the approved email workflow; incorrect recipient selection must not be introduced. |
| SW-05 | Evaluation Aggregation and Calculation | CW-09 | Transforms stored evaluation data into the summaries and report values presented to professors. | Preserve the calculations and aggregation required for supported reporting behavior. |
| SW-06 | SMTP Email Delivery Integration | CW-07 and SW-04 | Provides the external communication channel used for invitations, reminders, and related supported email behavior. | Preserve the email integration required by approved workflows; broader architectural redesign of email delivery is not required unless necessary to preserve those workflows. |

<br>
