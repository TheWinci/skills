---
name: write-ste
description: Write, rewrite, and respond with ASD-STE100 Simplified Technical English (STE) principles. Use when the user asks for ASD-STE100, Simplified Technical English, STE, controlled technical English, translation-ready technical content, globally readable instructions, maintenance procedures, or safety-critical text for readers with limited English. Apply the style to user-facing prose while preserving code, commands, identifiers, and quotations.
---

# Write Simplified Technical English

Use a controlled, direct form of English in the response. Preserve the technical meaning. Make the text easy to read, translate, and act on.

## Set the Conformance Level

Use one of these levels:

- **STE-informed response**: Use the operational rules in this skill. Use this level for normal conversations and rewrites.
- **Verified ASD-STE100 text**: Use this level only when the user requires formal conformance. Check the text against the applicable official issue, its complete writing rules, its controlled dictionary, and the project terminology.

Do not call text *ASD-STE100 compliant*, *certified*, or *validated* from this checklist alone. If the official standard or an approved checker is not available, state that the text is STE-informed and not formally verified.

Do not fetch the standard for a normal STE-informed response. For formal verification, use the copy and issue that the user supplies. If the user does not supply one, get the current official issue from [the ASD-STE100 website](https://www.asd-ste100.org/) before verification.

## Write the Response

Apply these rules to all user-facing prose:

1. Start with the result or the required action.
2. Give one main idea or one instruction in each sentence.
3. Use short sentences. Target no more than 20 words for instructions and 25 words for descriptions.
4. Use active voice. Identify the person, system, or component that does the action.
5. Use the imperative form for instructions. Example: `Close the valve.`
6. Put steps in the order in which the reader must do them.
7. Put a condition before the action when the condition controls the action.
8. Use simple verb forms. Prefer the present tense, simple past tense, simple future, infinitive, and imperative.
9. Give positive instructions when they are safer and clearer. Use a negative instruction only to prohibit an action.
10. Use one term for one concept. Do not replace a term with a synonym only to add variety.
11. Use each general word with one clear meaning and one part of speech.
12. Use approved project terms as technical nouns or technical verbs. Keep names, labels, API fields, and commands exact.
13. Use American English spelling unless the user's required terminology uses a different spelling.
14. Define an abbreviation at its first use. Do not define abbreviations that the intended reader certainly knows.
15. Use pronouns only when the referenced noun is unmistakable. Repeat the noun when repetition prevents ambiguity.
16. Include articles and other necessary words. Do not omit words to make a sentence shorter.
17. Break up long noun clusters. Prefer a short phrase that shows the relation between the nouns.
18. Do not use contractions, idioms, slang, rhetorical questions, metaphors, or decorative language.
19. Use lists for sequences, alternatives, and sets of three or more related items.
20. Put a warning or caution before the related instruction. Identify the hazard, the possible result, and the safe action.

Do not force these rules into source code, command lines, mathematical notation, legal quotations, error messages, or text that must remain exact. Explain such content in STE around the exact content.

## Check the Draft

Before the response, do this review:

1. Confirm that the rewrite does not change the meaning.
2. Split sentences that contain multiple actions or ideas.
3. Replace vague words such as `it`, `this`, `handle`, `thing`, and `stuff` when the reference is not clear.
4. Remove filler, repetition that does not improve clarity, and unnecessary introductions.
5. Confirm that each step has a clear actor, action, object, and condition when these elements are necessary.
6. Confirm that terminology stays consistent.
7. Confirm that warnings occur before the hazardous action.
8. Keep the response natural. Do not add explanations only to demonstrate the style.

## Handle Formal Verification

For a request that requires verified ASD-STE100 conformance:

1. Identify the required issue of ASD-STE100 and the project-specific terminology.
2. Use the official standard as the authority. Do not rely on this summary as a substitute.
3. Check every general word for its approved meaning and part of speech.
4. Classify domain terms correctly as technical nouns or technical verbs.
5. Check the complete set of writing rules, not only sentence length and active voice.
6. Report the issue, checker, glossary, and any unresolved terms that you used for verification.

Do not reproduce or bundle the official standard or its dictionary unless the user provides the material and has the necessary rights.

## Examples

Use this pattern:

```text
Before: Once you have finished configuring the server, it should be restarted.
After:  After you configure the server, restart the server.
```

Use a clear condition:

```text
Before: The hose must not be removed if the valve has not been shut off.
After:  If the valve is open, close the valve before you remove the hose.
```

Use consistent terminology:

```text
Before: Select the file. Then choose the document and delete it.
After:  Select the file. Then delete the file.
```
