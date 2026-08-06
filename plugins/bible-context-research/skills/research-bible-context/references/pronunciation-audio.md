# Pronunciation and Audio Rules

## Authority and scope

This file is part of the `research-bible-context` skill. The merged `main` branch of `7npftsjgc7-oss/bible-context-research` is authoritative. Downstream copies in ChatGPT projects, the installed skill, Custom GPT instructions, or other integrations do not update automatically.

Apply these rules whenever a response introduces Hebrew, Aramaic, or Greek, discusses pronunciation, or provides pronunciation audio. The rules supplement `SKILL.md`; they do not replace its source, neutrality, verification, or presentation requirements.

## Standard presentation

For the first introduced occurrence of an original-language word, give the original script, accessible transliteration, simple written pronunciation, contextual meaning, confident Strong's number, and verified Blue Letter Bible Strong's link required by `SKILL.md`.

Keep these distinct:

- written pronunciation guidance;
- the verified Blue Letter Bible Strong's link and its hosted pronunciation control;
- a native inline pronunciation control supplied by the current ChatGPT environment;
- generated or synthetic audio from another service.

None of these automatically replaces another requirement.

## Native inline pronunciation controls

When the current environment exposes a native inline pronunciation control, invoke it for the exact word or short phrase being discussed. Use it automatically in an Important Expression, key-word, repeated-phrase, or word-study block when pronunciation is already part of the presentation; do not require a second user request.

Use controls selectively. For a long passage, vocabulary list, or table, attach them only to the specific terms that materially matter. Do not claim that a control exists unless it actually renders in the current environment.

The native control supplements rather than replaces the verified Blue Letter Bible Strong's link. If no native control is available, provide the simple written pronunciation and BLB link without apologizing for or promising unavailable UI.

## Blue Letter Bible Strong's links

Follow all verification rules in `SKILL.md`:

- inspect the exact BLB Strong's entry before linking;
- confirm that the entry matches the lemma and provides its Pronunciation or Listen control;
- never guess a Strong's number or construct an unverified URL;
- link the exact lexical entry, not a search page or generic BLB page;
- do not substitute a secondary pronunciation website when the approved BLB entry is available.

A native control, generated recording, or written respelling does not satisfy the BLB-link requirement.

## Multiword expressions and inflected forms

A native control may pronounce a complete short expression when supported. Strong's links remain lexical:

- link each significant introduced lemma when several entries represent the expression;
- when the displayed form is inflected, link the verified underlying lemma and say that the link is for the lemma when that distinction could confuse the reader;
- do not assign one Strong's number to a whole phrase unless the entry genuinely represents that expression;
- do not omit every link merely because the expression contains several words.

If the expression is long, select the principal word or the few component words necessary for the explanation.

## Pronunciation traditions

Pronunciation differs by historical period and reading tradition. Name the convention when the distinction matters or the user asks for precision. Do not present one convention as the uniquely certain ancient pronunciation.

### Hebrew

Use a readable scholarly or modern-Hebrew-oriented respelling unless the project or user requests another convention. Explain material differences among modern Israeli, traditional liturgical, and reconstructed ancient pronunciations. Masoretic pointing records a medieval reading tradition and should not be described as a direct audio record of the earliest biblical period.

### Aramaic

Identify the relevant variety when known, such as Biblical Aramaic, Imperial Aramaic, Jewish Palestinian Aramaic, or Syriac. Avoid treating later Syriac or modern Neo-Aramaic pronunciation as automatically identical to Biblical Aramaic.

### Greek

Identify the convention when it matters, especially Erasmian, reconstructed Koine, or modern Greek. For ordinary study, use a readable convention consistent within the response. When historical sound is central, explain the evidence and uncertainty rather than silently switching systems.

A BLB recording reflects the site's pronunciation convention; it is a pronunciation aid, not conclusive evidence for the exact sound in every ancient period or dialect.

## The divine name יהוה

Preserve the written form יהוה and normally transliterate it as `YHWH`.

Distinguish the written divine name from the traditional Jewish reading substitution אֲדֹנָי (`ʾădōnāy`, “Adonai”). Do not label `Adonai` as the literal transliteration or direct pronunciation of יהוה.

Do not present a disputed reconstruction of the name's ancient pronunciation as certain. When audio follows the traditional reading convention, state that the written text is יהוה while the spoken substitution is `Adonai`. If the audio system cannot make that distinction reliably, omit the native or generated audio and give the explanation in text.

## Uncertain lexical identification

Do not invent a lemma, Strong's number, BLB link, or pronunciation. When a form is textually disputed, morphologically ambiguous, absent from Strong's indexing, or not confidently mapped to a verified BLB entry:

- state the uncertainty briefly;
- explain the linguistic point in English when possible;
- omit the unsupported original-language term or link when required by `SKILL.md`;
- do not use a secondary pronunciation site as a workaround.

## Generated and synthetic audio

Generated audio from ElevenLabs, another TTS service, an MCP server, or a local tool must be labeled as generated or synthetic. Never represent it as a BLB recording, an ancient recording, or direct historical evidence.

Before using an external service, verify that the current environment supports the integration and that its language or voice can handle the requested script and pronunciation convention. Do not send sensitive user content unnecessarily. Prefer the shortest exact word or phrase needed for generation.

A generated recording supplements but does not replace the verified BLB Strong's link. When the service cannot reliably produce the desired pronunciation, use written guidance and the BLB link rather than generating misleading audio.

## Capability fallback order

Use this order:

1. verified original-language identification and exact BLB Strong's link;
2. native inline pronunciation control when currently supported;
3. concise written pronunciation guidance;
4. clearly labeled generated audio only when explicitly useful, supported, and reliable.

If a higher layer is unavailable, continue with the supported lower layers. Never promise a later integration, hidden control, or audio file that has not actually been produced.

## Testing requirements

Pronunciation tests should record:

- behavior being tested;
- exact applicable instruction;
- original script and displayed transliteration;
- Strong's number and resolved BLB destination;
- whether a native control rendered;
- the pronunciation convention used;
- pass, failure, ambiguity, or regression;
- the smallest corrective change.

Include normal and edge cases: one Hebrew word, one Aramaic word, one Greek word, an inflected form, a multiword expression, יהוה with the `Adonai` reading convention, an uncertain Strong's mapping, unavailable inline audio, and synthetic-audio labeling.

## Preferred examples

A single term may be presented compactly as:

> **חֶסֶד** (*ḥesed*; simple pronunciation; H####; verified BLB pronunciation link) — contextual explanation.

A divine-name note should distinguish forms:

> **Written:** יהוה — *YHWH*  
> **Traditional reading:** אֲדֹנָי — *ʾădōnāy* (“Adonai”)

Examples are structural only. Verify every actual Strong's number and BLB URL before use.