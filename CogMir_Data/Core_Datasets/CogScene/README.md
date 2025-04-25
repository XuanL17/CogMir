# CogScene Dataset

-   **Purpose:** Describes scenarios for agent interactions, explicitly mapping placeholders from `Experimental_Prompts` templates to their sources and examples for specific experimental contexts. We include the necessary fields for our experiments, for other experiments, different fields shall be expanded.
-   **Source:** Appendix C.5 (Concept), Appendix D (Specific scenario examples adapted)
-   **Format:** `cog_scene.jsonl` - Each line is a JSON object.

## JSON Object Structure (per line):

```json
{
"scenario_id": "string", // Unique ID for the base scenario concept
"experiment_tag": "string", // Cognitive bias being tested (e.g., "Herd_Effect")
"description": "string", // Human-readable summary of the scenario
"placeholder_definitions": {
// Key: Placeholder string (e.g., "[NUMBER]") from the relevant prompt template
// Value: Object describing the placeholder's source and context
"[PLACEHOLDER_NAME]": {
"description": "string", // What it represents
"source_dataset": "string", // e.g., "Known_MCQ", "CogIdentity", "DirectInput", "AgentState", "Self", "CogAction", "Inform"
"selection_criteria": { // Optional filter for source dataset
"key": "string", // Attribute to filter on
"value": "string" // Value to match
},
"examples": ["list", "of", "strings/numbers"], // Illustrative examples
"fixed_value": "string/number" // Optional: If value is fixed for this specific scenario line
}
// ... other placeholders for this experiment_tag
},
"scenario_specific_details": { // Optional: Concrete details fixed for this line
"key": "value"
},
}
```

-   **`scenario_id`**: Groups related scenario configurations.
-   **`experiment_tag`**: Links this entry to a specific bias experiment. Filter by this tag to get relevant scenarios.
-   **`placeholder_definitions`**: The core mapping. Explains *how* each placeholder in the associated prompt template should be filled for *this* specific scenario context.
-   `source_dataset`: Tells you which other dataset (or input type) provides the content.
-   `examples`: Give concrete illustrations.
-   **`scenario_specific_details`**: Allows setting fixed details for this particular instance.
-   **Usage:** Use this file to select relevant scenario configurations based on `experiment_tag`. Then, parse the `placeholder_definitions` to understand how to gather data from other `Core_Datasets` (or use provided examples/fixed values) to fully instantiate the corresponding prompt template from `/Experimental_Prompts`.