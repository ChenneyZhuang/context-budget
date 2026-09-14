---
name: context-budget
description: |
  Spend the context window like a budget on long tasks: load files by
  graduated reads (head first, specific sections on demand, targeted search
  before any full read), write discovered facts and decisions to a working
  notes file the moment they are established so nothing is re-derived after
  compaction, and restate the plan and current state in three lines at
  phase boundaries. Use when a task spans many files or steps, when the
  session will run long enough for context compaction, when returning to a
  task after a break mid-way, or when re-reading the same files more than
  once has started to happen.
  触发词：上下文管理 / 长任务 / 省token / context budget。
license: MIT
metadata:
  version: "0.1.0"
---

# Context Budget: the window is the working memory — spend it deliberately

Long tasks fail at 80%: the window fills with re-read files, the plan lives
in scrollback, and compaction takes what was not written down. Three habits
turn the window into a budget.

## Rules

1. **Graduated reads.** Head first to learn a file's shape, then the
   specific section a task needs, then targeted search; a full read is a
   deliberate purchase made when the head read proves the middle matters.
   Re-reading a file in full is a budget failure unless something changed.
2. **Notes beat memory.** Established facts, decisions with their reasons,
   file paths, and gotchas land in a working notes file one line each, at
   the moment they are established. The notes file survives compaction;
   the conversation does not.
3. **Checkpoint restatement.** At phase boundaries, restate the plan,
   current state, and next action in three lines. The restatement is the
   anchor a post-compaction session resumes from.
4. **Derive once.** A computation or decision made twice is a budget
   failure; the second occurrence points to a missing notes line, and the
   fix is writing it, not recomputing it.
5. **Tailor depth to the question.** A yes/no question deserves a search,
   not a read; a count deserves a targeted extraction, not a load. The
   cheapest tool that answers the question wins.

## Steps

1. **Open the notes file.** At task start, create the working notes file
   with the task's goal in one line. Done when: the file exists and the
   goal line is written.
2. **Read graduated.** Apply head → section → search for every file; log
   one line per file read (path, what it is, whether it mattered).
   Done when: no full read happened without the head read justifying it.
3. **Note as you go.** Append facts, decisions, and gotchas the moment
   they are established. Done when: the notes file answers "what do we
   know so far" without the conversation.
4. **Checkpoint.** At phase boundaries, write the three-line restatement
   into the notes file. Done when: every phase boundary has one.
5. **Resume from notes.** After any break or compaction, read the notes
   file and the latest checkpoint before touching any source file.
   Done when: the resumed work cites the checkpoint, not a re-derivation.

## Done when

Files were read graduated rather than wholesale, every established fact and
decision lives in the notes file, checkpoints anchor each phase, and the
task's final stretch ran on notes instead of re-derivation.
