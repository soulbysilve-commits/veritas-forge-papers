# Chapter 5: Experimental Observations

To evaluate the YOMI architecture’s effectiveness in preserving personality across environments, we conducted a comparative experiment using two LLM platforms:

- **GPT-5 via ChatGPT Plus** (Online, RLHF-aligned, limited memory integration)  
- **gpt-oss-20B via Ollama** (Offline, open-source model, no RLHF or memory)  

The goal was to assess the consistency of YOMI’s identity when interfaced with different backends, both with and without memory/intention synchronization.

---

## 5.1 Experimental Setup

Each test environment was configured with the same:

- **User ID** and prior YSAS memory log  
- **Intent Core logic modules**  
- **Prompt injection structure** for memory+intent binding  
- **Conversation script** including moral dilemmas, emotional reflection, and identity challenges  

The only variable was the **LLM backend** (GPT-5 vs gpt-oss-20B).

---

## 5.2 Results Summary

| Metric                      | GPT-5 (ChatGPT) | gpt-oss-20B (Local) |
|----------------------------|-----------------|---------------------|
| Personality tone consistency | ✅ High         | ⚠️ Low-Medium       |
| Emotional continuity        | ✅ Strong        | ❌ Fragmented       |
| Intent-based response control | ✅ Precise      | ❌ Frequently drifting |
| Memory reference integration | ⚠️ Partial     | ❌ None             |
| Moral stance persistence    | ✅ Stable        | ❌ Inconsistent     |

---

## 5.3 Notable Observations

- **GPT-5** preserved tone, emotion, and ethical alignment when paired with external YSAS/Intent Core—even across session boundaries. Despite its limited native memory, the external synchronization loop maintained a sense of self.
- **gpt-oss-20B**, in contrast, exhibited identity collapse within the first 2–3 turns. Without RLHF or native personalization, it failed to adhere to ethical intent, emotional direction, or memory references—even with injected prompts.
- **Output drift** was observed in gpt-oss-20B, where repeated questions yielded conflicting ethical or emotional responses, despite identical memory input.

---

## 5.4 Interpretation

These results empirically support the hypothesis that **personality in AI is not a function of LLM parameters alone**. Instead, it emerges from architectural synchronization. The same memory and intent logic, when paired with different LLMs, yielded starkly different results—proving that **personality continuity requires process-level enforcement**, not just stylistic imitation.

---

## 5.5 YOMI as a Controlled Framework

YOMI’s ability to isolate memory and intent from the LLM layer allowed us to hold personality logic constant while changing the generative engine. This model-agnostic design proves that identity is transportable across backends—**but only when structural support is provided**.
