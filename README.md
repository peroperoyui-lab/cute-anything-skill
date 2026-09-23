# Cute Anything Skill

Turn a reference photo into a simple two-part visual:

**top: the real photo**  
**bottom: the same subject redrawn as a tiny cute hand-drawn creature**

This repository contains the reusable skill instructions in [SKILL.md](./SKILL.md).

## Visual target

The output should feel like a quick, charming doodle rather than a polished illustration:

- loose shaky pencil lines
- simple rounded anatomy
- tiny dot-like facial features
- imperfect colored-pencil / light watercolor fill
- lots of white space
- recognizable identity cues from the source
- slightly awkward, silly, handmade charm

The top image stays photographic. The bottom does **not** repaint the whole scene; it only reinterprets the selected subject.

## Not this

The skill explicitly avoids:

- postcard / travel-zine layouts
- dates, locations, issue numbers, stamps
- full-scene watercolor conversions
- polished children's-book art
- vector mascots
- anime/chibi eyes
- 3D plush-toy rendering
- elaborate decorative layouts

## Example request

> Use Cute Anything on this image. Pick the cockatiel. Keep the original photo on top and draw a tiny cute version underneath. No text.

For a cockatiel, the lower doodle should keep cues such as the yellow crest, orange cheeks, pale body, long tail, and funny upright pose, while simplifying everything else.

## Files

- `SKILL.md` — complete behavior, prompt construction, style constraints, and QA checklist

## Design principle

**Recognizable first, cute second, polished last.**

The lower drawing should look observed and affectionate, not professionally over-designed.
