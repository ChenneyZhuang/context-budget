# context-budget 上下文预算

Long tasks do not fail at the start; they fail at 80%, when the window is full of re-read files and the plan is somewhere in the scrollback. Manage the window like a budget.

长任务不是败在开头，是败在 80%——窗口里塞满重读的文件，计划躺在回滚的聊天里。把上下文窗口当预算管。

## Why / 为什么

An agent's working memory is the context window, and the two ways it dies on long tasks are **re-reading** (loading the same 5,000-line file three times because nothing was noted) and **re-deriving** (recomputing decisions already made three turns ago). Both are budget failures: the token was spent once and bought nothing durable. The cure is mechanical — graduated reads, notes to disk, checkpoint restatement.

agent 的工作记忆就是上下文窗口，长任务死法有两种：**重读**（同一份 5000 行文件读了三遍，因为什么都没记）和**重推导**（三轮前定过的决策重新算一遍）。这都是预算失败：token 花了一次，没买到任何耐用的东西。解法是机械的——分层读取、落盘记笔记、检查点复述。

## The three habits / 三个习惯

1. **Graduated reads.** Head first (first ~100 lines to learn the shape), then the specific section, then targeted search. A full read is a deliberate purchase, made when the head read proves the middle matters.
2. **Notes beat memory.** Facts, decisions, file paths, and gotchas land in a working notes file the moment they are established — one line each. The notes file survives compaction; the conversation does not.
3. **Checkpoint restatement.** At phase boundaries (before a long build, after a big discovery), restate the plan and current state in three lines. This is the anchor that survives when the window is compacted mid-task.

## What it changes at 80% / 80% 处的差异

Without the budget: the agent re-reads, contradicts its earlier decisions, and the final third of the task runs on fumes. With it: the plan is three lines long, every established fact is in the notes file, and the last stretch reads two small files instead of recalling ten.

没有预算：重读、推翻自己三轮前的决定、最后三分之一靠残血硬撑。有预算：计划只有三行，每个已确立的事实都在笔记文件里，最后一程是读两个小文件，而不是回忆十个。

## Install / 安装

```bash
npx skills add ChenneyZhuang/context-budget
```

Per-agent paths: [COMPATIBILITY.md](COMPATIBILITY.md). MIT. v0.1.0.

各 agent 安装路径见 COMPATIBILITY.md。MIT 许可，v0.1.0。
