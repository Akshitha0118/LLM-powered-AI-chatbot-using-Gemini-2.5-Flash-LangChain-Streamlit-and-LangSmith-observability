# -LLM-powered-AI-chatbot-using-Gemini-2.5-Flash-LangChain-Streamlit-and-LangSmith-observability

This Project, I worked on the development of an LLM-powered AI chatbot using Gemini 2.5 Flash, LangChain, Streamlit, and LangSmith observability. While building the system, I analyzed the LLM run logs to better understand how prompts flow through the pipeline and how responses are generated


# EX: Real Time Usage 
---
## AI Customer Support Systems :
---------------------------------
Many companies use AI for customer service automation.
Tracking helps to:
 - See which queries fail
 - Monitor conversation quality
 - Track response accuracy
 - Identify escalation cases
Example companies use this for:
 - ticket automation
 - FAQ bots
 - support assistants


# LLM Run Logs :-
----------------

## ==>1. User Input (Prompt)
The process starts when a user sends a prompt to the model.
Example: “Give me a prompt about cricket.”
This becomes the primary input that the AI system processes.

## ==>2. System Message (AI Role Definition)
Before the user query reaches the model, a system prompt is often added to define the model's behavior.
Example: “You are Gemini 2.5 Flash — a fast, multimodal, and intelligent AI assistant.”
This helps guide how the model should respond.

## ==>3. Human Message
This is the actual user request passed to the model after combining it with the system prompt.

==>4. Model Execution
The request is sent to the AI model (in this case Gemini 2.5 Flash), which processes the prompt and generates a response.

## ==>5. Generated Output
The model returns a response.
In this case, the model began generating a set of cricket-related prompts but the output stopped mid-response.

==>6. Finish Reason
The run log showed the finish reason as MAX_TOKENS, meaning the response was truncated because it reached the token limit.

## ==>7. Token Usage
LLM systems track tokens for both inputs and outputs.
Example metrics:
• Input tokens: 34
• Output tokens: 1020
• Total tokens: 1054
This information is important for monitoring cost, efficiency, and performance.

## ==>8. Tool Calls
The log also indicates whether the model used external tools or functions.
In this run, no tools were called.

==>9. Safety Ratings
Safety checks ensure the response complies with content policies.
No safety issues were flagged in this execution.

## ==>10. Metadata & Tracing
The run was recorded using LangSmith, which stores information such as:
• Organization
• Workspace
• Project
• Execution depth
This helps developers debug, monitor, and optimize AI applications.

## ==>LLM Pipeline Flow
User Prompt → LangChain Processing → System Prompt Added → AI Model (Gemini) → Response Generated → LangSmith Logs & Tracing

Understanding these logs is extremely helpful when building production-grade AI applications, debugging prompt behavior, and optimizing token usage.
