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
│   ├── action-library.md            48 reusable actions across five categories
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

### Install as a Codex skill

```bash
# Global Codex skill (defaults to ~/.codex/skills)
CODEX_HOME="${CODEX_HOME:-$HOME/.codex}"
mkdir -p "$CODEX_HOME/skills"
ln -s "$(pwd)" "$CODEX_HOME/skills/dreamer-star-ip"
```

Then start a new Codex conversation and say: `Use dreamer-star-ip to illustrate this article` or `Generate a thinking pose with dreamer-star-ip`.

### Use as a prompt library

You can also copy a prompt from [`examples/ai-era-product-interview-v6.2.md`](examples/ai-era-product-interview-v6.2.md) into an image model such as GPT Image, Nano Banana, or Midjourney.

### Build a scene from the action library

Open [`action-library-preview.html`](action-library-preview.html) to browse the action library visually, or read [`references/action-library.md`](references/action-library.md) for the complete specifications.

1. Choose one of the 48 actions based on your topic.
2. Copy its action description into the `Single visual concept` and `Composition` sections of the main prompt template.
3. Add one or two short Chinese labels, then generate and review the result against the QA checklist.

The five categories cover star-specific actions, general poses, narrative scenario sets, reaction-image foundations, and job-search or workplace situations.

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
