## SQL Generation Prompts

### SQLCoder (Basic Prompt)

Generate a SQL query to answer [QUESTION]{user_question}[/QUESTION]

If you cannot answer the question with the available database schema, return 'I do not know'


---

### SQLCoder Model Specific Prompts Generalised
The query will run on a database with the following schema:
{table_metadata_string}

Follow instructions to the letter, and answer questions without making any additional assumptions.

Generate a {db_type} query to answer this question: {user_question} {instructions} DDL statements: {table_metadata_string}

Generate a valid {db_type} query that best answers the question {user_question}.

I will reflect on the user's request before answering the question.

I was asked to generate a SQL query for this question: {user_question}


---

### How it plans the response
{instruction_reflections} With this in mind, here is the {db_type} query that best answers the question while only using appropriate tables and columns from the DDL statements:

**Instruction_reflections**
"\nFollow the instructions below to generate the query:",
"\nAdditionally, I was asked to follow the instructions below to generate the query:",

---

### Output Format
Given the database schema, here is the SQL query that answers {user_question}
[sql query]