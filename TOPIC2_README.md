# n8n Topic 2 — Understanding Workflow Execution & Debugging Basics

## 1. Objective

Create, execute, and debug an n8n workflow containing a Manual Trigger, Edit Fields node, and HTTP Request node. Demonstrate an intentional failure, inspect the error, correct the configuration, and verify successful execution.

## 2. Workflow Structure

Manual Trigger → Edit Fields → HTTP Request

### Edit Fields Configuration

- Field name: `greeting`
- Data type: String
- Value: `Hello, n8n!`

### HTTP Request Configuration

- Method: GET
- Failed test URL: `https://this-domain-does-not-exist-12345.com`
- Corrected URL: `https://httpbin.org/get`
- Authentication: None

## 3. Intentional Failure and Diagnosis

The HTTP Request node initially failed because the configured domain was invalid or unavailable.

Observed error:

"The connection cannot be established, this usually occurs due to an incorrect host (domain) value."

The Edit Fields node produced the expected greeting input:

```json
{
  "greeting": "Hello, n8n!"
}
```

The failure demonstrated how an incorrect HTTP Request URL prevents a node from establishing a connection.

## 4. Resolution and Successful Test

The invalid URL was replaced with:

`https://httpbin.org/get`

The HTTP Request node was tested again using **Execute step**. The successful response returned JSON containing request information, including the request URL and headers.

The workflow was subsequently displayed with successful indicators on the Edit Fields and HTTP Request nodes.

## 5. Test Step vs. Execute Workflow

- **Execute step:** Runs the selected node for isolated testing. It is useful for checking a node's configuration and output.
- **Execute workflow:** Runs the workflow from its trigger through the connected nodes, allowing the complete workflow execution to be validated.

## 6. Execution History and Evidence

The supporting screenshots document the workflow configuration, the failed HTTP Request, and the corrected successful HTTP Request.

Execution history should be reviewed to verify the failed and successful runs, their timestamps, durations, inputs, outputs, and error details where available.

## 7. Files in This Repository

- `My First N8N Workflow.json` — Topic 1 workflow source.
- Topic 2 debugging workflow JSON — exported workflow source.
- Topic 2 screenshots — supporting assessment evidence.
- `TOPIC2_README.md` — Topic 2 setup and debugging documentation.

## 8. Conclusion

This exercise demonstrates basic n8n workflow execution, input/output inspection, error identification, HTTP Request troubleshooting, and correction through isolated node testing.

## 9. Assumptions and Limitations

- The assessment uses a public HTTP test endpoint.
- The external endpoint must be reachable when testing the workflow.
- Screenshots provide visual evidence; the exported workflow JSON provides the workflow configuration.
- Confirm the saved execution history and complete the demonstration video before final submission.
