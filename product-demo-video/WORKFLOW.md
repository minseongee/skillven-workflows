---
name: product-demo-video
description: Make a product demo video in code with Remotion - script, build the scenes, add captions and render.
when_to_use: A launch, a changelog or a landing page needs a short product video and the team prefers code to a video editor.
steps:
  - id: script
    title: Write the script and storyboard
    checkpoint: true
  - id: create
    title: Create the Remotion project
    skill: remotion-dev/skills/skills/remotion-create
  - id: scenes
    title: Build the scenes
    skill: remotion-dev/skills/skills/remotion-best-practices
  - id: captions
    title: Add captions
    skill: remotion-dev/skills/skills/remotion-captions
  - id: render
    title: Render the video
    output: an MP4 file
---
## script
Agree on the length (usually 30 to 90 seconds), the audience, the three things the video
must show, and the screens or assets to use. Write the script scene by scene with timings.

## render
Preview the video in Remotion Studio with the user first, then render it with the Remotion
CLI (`npx remotion render`) to an MP4 at 1080p unless the user wants another size. Report
the output path, the length and the file size.
