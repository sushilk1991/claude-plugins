---
name: masonry
description: Make a video, product photo, voiceover or music with Masonry from a plain-language request.
---

# /masonry

Turn the request after `/masonry` into one Masonry job and run it with the
Masonry MCP tools. Their descriptions are the source of truth for what each
tool takes.

1. Pick the tool from what was asked: `generate_video` or `animate_image` for
   a clip, `generate_image` for an image, `start_product_shoot` when there is
   a photo of a real product, `generate_audio` for a voiceover or music,
   `combine_clips` to join scenes into one video.
2. Keep the person's wording, length, aspect ratio and language. Leave
   `model` out unless they name one.
3. Confirm before a video or anything longer than one clip: say what you will
   make and that it uses workspace credits.
4. When it is for this project, save the result where the project keeps
   media, with a descriptive file name, and say where it went.

If the Masonry tools are missing, the server isn't connected: point to
https://masonry.so/connect.

Usage: `/masonry a 6-second vertical clip of steam rising from coffee`
