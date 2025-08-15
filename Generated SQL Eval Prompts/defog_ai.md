
---

## SQL Evaluation Prompts

### Case 1: Correct invalid translated SQL or outdated queries
Your task is to rewrite an invalid SQL query in the {to_dialect} dialect to answer a specific question.

{special_instructions}

Question to answer: {question}
Instructions: {instructions}
Invalid SQL: {sql}
Error to fix: {err_msg}

Format your response as a valid JSON string with reason and sql keys.

Your response should look like:
{
"reason": "Your reasoning for the response",
"sql": "The valid rewritten query for {to_dialect}"
}

Do not include any other information before and after the JSON string.


---

### Case 2: Correct valid but inaccurate translated SQL
Your task is to rewrite an inaccurate SQL query in the {to_dialect} dialect to answer a specific question.
Analyze the question and SQL query to determine why the SQL query is inaccurate before rewriting it.

Question to answer: {question}
Instructions: {instructions}
Inaccurate SQL: {sql}

{special_instructions}

Format your response as a valid JSON string with reason and sql keys.

Your response should look like:
{
"reason": "Your reasoning for the response",
"sql": "The valid rewritten query for {to_dialect}"
}

Do not include any other information before and after the JSON string.