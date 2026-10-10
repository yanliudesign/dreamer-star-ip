<div align="center">

[English](README.md) · [中文](README_CN.md)

# ⭐ dreamer-star-ip

**A honey-yellow star character meets minimalist conceptual illustration inspired by editorial cartooning.**

One image = one idea + generous negative space + three structural hatching areas + a visual contrast hook.

[![License: MIT](https://img.shields.io/badge/LICENSE-MIT-2ea44f?style=flat-square)](LICENSE)
![Version](https://img.shields.io/badge/VERSION-6.2-2ea44f?style=flat-square)
![Examples](https://img.shields.io/badge/EXAMPLES-9-2ea44f?style=flat-square)
[![GitHub Stars](https://img.shields.io/github/stars/yanliudesign/dreamer-star-ip?style=flat-square&label=STARS&color=f97316)](https://github.com/yanliudesign/dreamer-star-ip/stargazers)

![Claude Code Skill](https://img.shields.io/badge/Claude_Code-Skill-d97757?style=flat-square&logo=anthropic&logoColor=white)
![Codex Skill](https://img.shields.io/badge/Codex-Skill-22c55e?style=flat-square&logo=openai&logoColor=white)
![OpenCode Skill](https://img.shields.io/badge/OpenCode-Skill-3b82f6?style=flat-square)
![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-8b5cf6?style=flat-square)
![Hermes Skill](https://img.shields.io/badge/Hermes-Skill-ec6f9e?style=flat-square)

</div>

## What It Is

The dreamer-star-ip character, 小星妍, is a slightly tilted, honey-yellow five-pointed star. She has a small curved "Dreamer" wordmark close above her head, hand-drawn hatching on one lower side, and a contextual status glyph such as a light bulb, `?`, crown, cloud, lightning bolt, spark, or speech bubble. She must take part in the image's central action and never appear as decoration.

**Best for:** editorial illustrations for Chinese articles, Xiaohongshu posts, presentations, Notion documents, and social media covers. The primary format is 3:4 portrait, with 4:3 and 1:1 also supported.

**Not intended for:** portrait-led covers, polished 3D commercial illustration, or presentation-style infographics and architecture diagrams.

## What It Produces

- A shot list of 4-8 illustration opportunities for an article, each tied to a specific passage and cognitive anchor.
- A complete 12-block English prompt for every selected scene, including composition, character action, labels, color rules, and anti-slop constraints.
- A final image when the host agent has access to an image-generation tool; otherwise, a copy-ready prompt for GPT Image, Nano Banana, Midjourney, or another image model.
- A short placement note explaining where each illustration belongs and why the visual metaphor supports the argument.

## References and Acknowledgements

This project draws on Ian's open-source work in [Ian Xiaohei Illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations), particularly its approach to extracting cognitive anchors from Chinese writing, building shot lists, and structuring editorial illustration workflows. Thank you to Ian for sharing the methodology.

See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for attribution and license details.

## What This Adds

Ian Xiaohei Illustrations provides a general workflow for turning Chinese writing into conceptual editorial illustrations. dreamer-star-ip extends that foundation into a reusable character-IP system focused on consistency across a series:

- A complete character specification covering geometry, personality, poses, signatures, companion roles, and failure modes.
- A 16-glyph state vocabulary across five intent families for expressing what the character is thinking or feeling.
- A library of 48 reusable actions across five categories, from star-specific visual metaphors to workplace scenarios, each ready to drop into the main prompt structure.
- Quantified composition rules for 3:4, 4:3, and 1:1 formats, including negative-space ratios, contrast axes, label limits, and hatching placement.
- A 12-block prompt structure designed to preserve the same visual identity across topics and image models.
- Tiered P0/P1/P2 quality control for deciding when to regenerate, edit locally, or accept a minor variation.

The goal is not to replace Ian's broader illustration toolkit. It is to make one original character system more repeatable, inspectable, and extensible.

## Project Structure

```text
dreamer-star-ip/
├── SKILL.md                        Main entry: positioning and five-step workflow
├── references/
│   ├── style-dna.md                Visual DNA, color, negative space, and hatching
│   ├── xiaoxingyan-ip.md           Complete character specification and pose library
│   ├── status-glyphs.md            16 status glyphs across five families
│   ├── action-library.md           48 reusable actions across five categories
│   ├── composition-patterns.md     Composition principles, contrast hooks, and formats
│   ├── prompt-template.md          12-block English prompt template
│   └── qa-checklist.md             Post-generation QA and anti-slop checklist
├── example/                        Nine finished images shown in the gallery below
├── action-library-preview.html     Visual index for browsing the action library
├── THIRD_PARTY_NOTICES.md          Upstream attribution and license notice
└── examples/
    ├── ai-era-product-interview-v6.2.md   Seven v6.2 prompt examples
    ├── six-vertical-illustrations.md      Six earlier portrait examples
    ├── four-poses/                        Pose studies
    └── ip-manual/                         Character manual
```

## Usage

### 1. Clone the repository

```bash
git clone https://github.com/yanliudesign/dreamer-star-ip.git
cd dreamer-star-ip
```

### 2. Install for your agent

The repository root is already a complete skill directory. Choose the command for your agent:

| Agent | Personal skill directory | Invoke with |
|---|---|---|
| [Claude Code](https://code.claude.com/docs/en/agent-sdk/skills) | `~/.claude/skills/` | `/dreamer-star-ip` |
| [Codex](https://developers.openai.com/codex/skills/) | `$CODEX_HOME/skills/` (default: `~/.codex/skills/`) | `$dreamer-star-ip` |
| [OpenCode](https://opencode.ai/v2/docs/skills) | `~/.config/opencode/skills/` | Ask it to use `dreamer-star-ip` |
| [OpenClaw](https://docs.openclaw.ai/tools/skills) | `$OPENCLAW_STATE_DIR/skills/` (default: `~/.openclaw/skills/`) | `/dreamer-star-ip` |
| [Hermes Agent](https://hermes-agent.nousresearch.com/docs/user-guide/features/skills/) | `~/.hermes/skills/` | `/dreamer-star-ip` |

<details>
<summary><strong>Claude Code</strong></summary>

```bash
mkdir -p "$HOME/.claude/skills"
ln -s "$(pwd)" "$HOME/.claude/skills/dreamer-star-ip"
```

</details>

<details>
<summary><strong>Codex</strong></summary>

```bash
CODEX_HOME="${CODEX_HOME:-$HOME/.codex}"
mkdir -p "$CODEX_HOME/skills"
ln -s "$(pwd)" "$CODEX_HOME/skills/dreamer-star-ip"
```

</details>

<details>
<summary><strong>OpenCode</strong></summary>

```bash
mkdir -p "$HOME/.config/opencode/skills"
ln -s "$(pwd)" "$HOME/.config/opencode/skills/dreamer-star-ip"
```

</details>

<details>
<summary><strong>OpenClaw</strong></summary>

```bash
OPENCLAW_STATE_DIR="${OPENCLAW_STATE_DIR:-$HOME/.openclaw}"
mkdir -p "$OPENCLAW_STATE_DIR/skills"
ln -s "$(pwd)" "$OPENCLAW_STATE_DIR/skills/dreamer-star-ip"
```

</details>

<details>
<summary><strong>Hermes Agent</strong></summary>

```bash
mkdir -p "$HOME/.hermes/skills"
ln -s "$(pwd)" "$HOME/.hermes/skills/dreamer-star-ip"
```

</details>

These macOS/Linux commands create a symbolic link, so `git pull` in the cloned repository updates the installed skill. Restart the agent or begin a new session after installation. For project-only use, place the skill under `.claude/skills/` (Claude Code), `.opencode/skills/` (OpenCode), or `skills/` (OpenClaw) inside that project.

### 3. Choose a workflow

The examples below use Codex's `$dreamer-star-ip` syntax. With Claude Code, OpenClaw, or Hermes, use `/dreamer-star-ip` instead. In OpenCode, ask the agent to use `dreamer-star-ip`.

**Plan illustrations without generating images**

```text
Use $dreamer-star-ip to analyze the article below. Do not generate images yet.
Create a shot list of about five illustrations, including placement, cognitive
anchor, visual metaphor, contrast hook, character action, status glyph, and labels.

<paste article>
```

**Generate a complete illustration series**

```text
Use $dreamer-star-ip to create four 3:4 editorial illustrations for the article
below. Give every image a distinct metaphor, generate each image separately, run
the QA checklist, and include a placement note and reproducible prompt.

<paste article>
```

**Illustrate one concept**

```text
Use $dreamer-star-ip to illustrate this idea:
"Trust is built one piece of evidence at a time."
Choose a fitting action from the action library and avoid reusing example compositions.
```

### Use as a prompt library

You can also copy a prompt from [`examples/ai-era-product-interview-v6.2.md`](examples/ai-era-product-interview-v6.2.md) into an image model such as GPT Image, Nano Banana, or Midjourney.

### Build a scene from the action library

Open [`action-library-preview.html`](action-library-preview.html) to browse the action library visually, or read [`references/action-library.md`](references/action-library.md) for the complete specifications.

1. Choose one of the 48 actions based on your topic.
2. Copy its action description into the `Single visual concept` and `Composition` sections of the main prompt template.
3. Add one or two short Chinese labels, then generate and review the result against the QA checklist.

The five categories cover star-specific actions, general poses, narrative scenario sets, reaction-image foundations, and job-search or workplace situations.

> Image generation depends on the tools available to your agent. If no image tool is available, the skill returns the complete prompt instead of pretending an image was generated.

## Examples

<table>
    <tr>
        <td><img src="example/71ceb6fd-f2c3-42c4-b419-3e87dc9a2bce.jpeg" width="240" height="320" alt="dreamer-star-ip example 1"></td>
        <td><img src="example/Gemini_Generated_Image_7yx70x7yx70x7yx7.png" width="240" height="320" alt="dreamer-star-ip example 2"></td>
        <td><img src="example/Gemini_Generated_Image_c2j3vhc2j3vhc2j3.png" width="240" height="320" alt="dreamer-star-ip example 3"></td>
    </tr>
    <tr>
        <td><img src="example/Gemini_Generated_Image_r5nht8r5nht8r5nh.png" width="240" height="320" alt="dreamer-star-ip example 4"></td>
        <td><img src="example/Screenshot%202026-07-18%20at%204.07.25%E2%80%AFPM.png" width="240" height="320" alt="dreamer-star-ip example 5"></td>
        <td><img src="example/Gemini_Generated_Image_w368oyw368oyw368.png" width="240" height="320" alt="dreamer-star-ip example 6"></td>
    </tr>
    <tr>
        <td><img src="example/be47bbf4-6d72-4e60-91fb-be46e41d7380.jpeg" width="240" height="320" alt="dreamer-star-ip example 7"></td>
        <td><img src="example/c29d3e5a-ec58-48a1-a1b1-9c5dad9d6762.jpeg" width="240" height="320" alt="dreamer-star-ip example 8"></td>
        <td><img src="example/e66317aa-5aff-4fed-a55a-6fa4eab4938e.jpeg" width="240" height="320" alt="dreamer-star-ip example 9"></td>
    </tr>
</table>

## Core Principles

- **One image, one idea.** Do not turn an illustration into an infographic or architecture diagram.
- **55-65% negative space.** Empty space gives the concept room to breathe.
- **Three structural hatching areas** at a consistent angle. Hatching elsewhere becomes visual noise.
- **A clear contrast hook.** Top versus bottom, before versus after, definition versus optimization, or individual versus group should read in a second.
- **The status glyph is the second-read clue.** Choose the symbol that best answers: "What is she primarily thinking or feeling right now?"
- **She is always doing something.** Never pose her at attention or use her as decoration. A small jump is better than a static stance.

## License

MIT. See [LICENSE](LICENSE).

The dreamer-star-ip character, status-glyph system, and composition language are open for learning and remixing. Please provide attribution when using them commercially.
