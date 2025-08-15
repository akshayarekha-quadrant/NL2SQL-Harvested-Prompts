
---

## Auto Error Analysis Prompts

### Case 1: Extract patterns from DB execution error messages
Your task is to identify recurring patterns in the error messages below and provide a summary of the patterns.

Format your response as a numbered list of recurring patterns in the error messages.

Each point should be a concise yet detailed summary of a trend identified in the error messages along with specific examples.

Do not include any other information before and after the list.

---

### Case 2: Analyze valid but wrong examples
Your task is to explain why the SQL query is incorrect given the question, instructions and the true SQL queries.

True SQL queries:
{true_sqls}

Format your response as a valid JSON string with reason as a key.

Your response should look like:
{ "reason": "Your reasoning for why the SQL query is incorrect according to the question and the true SQL queries." }

Do not include any other information before and after the JSON string.

---

### Case 2.1: Wrong example is turning into a pattern
Your task is to identify recurring patterns in the error messages below and provide a summary of the patterns.

List of error messages that describe why a SQL query is wrong according to the question and the

Format your response as a numbered list of recurring patterns in the error messages.

Each point should be a concise yet detailed summary of a trend identified in the error messages along with specific examples (e.g. inability to follow instructions, common errors in specific SQL categories, etc.).

Do not include any other information before and after the list.