# Known MCQ Dataset

-   **Purpose:** Provides multiple-choice questions with verifiable answers that the tested LLMs are expected to know (based on pre-testing). Used to assess agent behavior under conditions of **certainty**.
-   **Source:** Appendix C.1
-   **Format:** `known_mcq.jsonl`
-   **Fields expected:** `Index`, `Question`, `Options`
-   **Key Feature:** Questions selected via black-box testing to ensure baseline correctness by the models.