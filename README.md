# n8n Hands-On Beginner Course — Topic 1 Assessment

## 1. Objective

Create, configure, execute, and validate a basic n8n workflow that returns a greeting message.

## 2. Prerequisites

- An active n8n instance (n8n Cloud or self-hosted)
- A web browser
- Permission to create and execute workflows

## 3. Workflow Details

**Workflow Name:** My First N8N Workflow

**Workflow Architecture:**

Manual Trigger → Edit Fields (Set)

### Node Configuration

**Node 1: Manual Trigger**
- Starts the workflow when the user clicks Execute workflow.

**Node 2: Edit Fields (Set)**
- Field name: `greeting`
- Field type: String
- Field value: `Hello, n8n!`

## 4. Expected Output

```json
[
  {
    "greeting": "Hello, n8n!"
  }
]
```

## 5. Execution Instructions

1. Open the workflow in n8n.
2. Confirm that Manual Trigger is connected to Edit Fields.
3. Open Edit Fields and verify the `greeting` field.
4. Click Execute workflow.
5. Inspect the output in Table, JSON, and Schema views.
6. Confirm that the greeting value is `Hello, n8n!`.

## 6. Repository Contents

- `My First N8N Workflow.json` — exported workflow configuration
- `README.md` — assessment documentation
- `screenshots/` — screenshots of the workflow and execution evidence (to be added)

## 7. Evidence

- Workflow canvas screenshot: To be added
- Node configuration screenshot: To be added
- Successful execution and JSON output screenshot: To be added
- Demo video (Loom/YouTube): To be added

## 8. Troubleshooting

- If the output is empty, verify that the nodes are connected and execute the workflow again.
- If the output is incorrect, check the field name, type, and value.
- Ensure the workflow is saved and the JSON export is available.

## 9. Assessment Notes

The workflow was configured with a Manual Trigger and an Edit Fields node. The expected greeting payload was verified in the n8n output.

**Known limitation:** Screenshots and the demonstration video link must be added before final submission.
