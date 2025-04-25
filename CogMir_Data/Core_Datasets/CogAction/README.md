# Action Description Dataset

-   **Purpose:** Contains a list of simple, discrete actions or short descriptive phrases. These can be used to populate simulation events, agent behaviors, or placeholders in simpler prompt templates.
-   **Source:** Generated based on user-provided examples and expanded list.
-   **Format:** `actions.jsonl` - Each line is a JSON object representing one action description.

## JSON Object Structure (per line):

```json
{
"index": "string",     // Sequential identifier for the action description (as a string)
"description": "string" // Text describing the action
}
```

-   **`index`**: A unique, sequential string identifier for easy reference.
-   **`description`**: The concise text describing the action or observation.
-   **Usage:** Entries from this file can be selected (e.g., by index or randomly) to define what an agent does or observes in a given context, or to fill simple `[ACTION]` placeholders in prompts that don't require complex typing or valence information.


