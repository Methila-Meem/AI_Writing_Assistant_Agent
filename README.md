Basic AI Writing Assistant Agent

Designed and implemented an AI-powered agent that assists users with writing tasks.
The agent helps to improve the quality of text by performing tasks such as grammar correction, vocabulary enhancement, and sentence rewriting.

The assistant uses four tools:

grammar_corrector – fixes grammar and punctuation.
Always runs first.

sentence_rewriter – improves clarity and flow.
Always runs after grammar correction.

vocab_enhancer – enriches word choice.
Runs only if the user requests vocabulary enhancement.

tone_adjuster – changes style (e.g., formal, casual).
Runs only if the user provides a tone.

Flow:
grammar → rewrite → (vocab if requested) → (tone if specified)

The LangGraph StateGraph enforces this order.
Grammar and rewriting are mandatory for every input; vocabulary and tone steps depend solely on the user’s optional choices.
