# gpt-talk-distiller

ChatGPT conversation distillation engine. Takes ChatGPT Exporter `.md` as input, auto-classifies into 4 patterns (progressive deepening / topic jump / repeated pressure / memory injection), re-threads topics, and extracts 8 types of items (decisions, numbers, open questions, ideas, actions, reversals, meta-events, pressure recurrence) into a clean `.md` output.

**Goal:** preserve scattered decisions, numbers, and reversals across the timeline by re-weaving them per topic, with no loss.

## Flow

`input → utterance pair indexing → pattern classification → 8-type extraction → topic re-threading → output`

## 4 Patterns

| Pattern | Trait | Output Variant |
|---|---|---|
| Progressive Deepening | single topic, stepwise development, 0~1 reversals | reversal timeline (if any) |
| Topic Jump | A→B→A recurrence, short messages, meta-instructions | topic recurrence marker |
| Repeated Pressure | same topic 3+ recurrences, short rebuke ("??", "really?") | recurrence count + depth tracking |
| Memory Injection | single round, user dump, response is compression | compression-loss verification table |

## 8 Extraction Types

decision · number/fact · open question · idea/hypothesis · action · reversal/discard · meta-event · pressure recurrence

## Validation

Validated against 4 real ChatGPT export samples covering all 4 patterns.

## Korean

[README.ko.md](./README.ko.md)
