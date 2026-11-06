---
name: get-started
description: Set up Masonry, then make a first video or product photo, and a first Studio product shoot. Use right after Masonry is installed, or when someone asks how to start with Masonry, how to connect it, or what it can do.
---

# Get started with Masonry

Masonry makes videos, product photos, voiceovers and music in the person's
own Masonry workspace. This guide is a default path for a new user. When the person asks
for something specific, do that instead, and skip any step they don't want.

## 1. Check the connection

Call `get_credits`.

- It answers: Masonry is connected. Say which workspace is connected and its
  credit balance, in one line. Don't mention prices or plans.
- The host asks the person to sign in: wait for them. Sign-in happens on
  masonry.so, where they choose a workspace and select Allow. Nothing needs to
  be copied or pasted.
- It fails for another reason: say what failed and stop.

## 2. First video

If they want a video (most people do), ask what it is for in one short
question, unless they already said.

1. Offer one short clip built from the answer, for example: "a 6-second
   vertical clip of steam rising from your coffee on a sunlit counter".
2. After they agree, call `generate_video`. Leave `model` out unless they name
   one. To animate a photo they already have, use `animate_image` instead.
3. For a longer video (an ad, a story, a music video), agree on a few scenes
   first, generate each one, then join them with `combine_clips`, adding music
   from `generate_audio` if they want it.

## 3. First image

1. Ask what they sell, in one short question, unless they already said.
2. Offer one starter shot built from the answer, for example: "a product photo
   of your ceramic mug on a pale stone surface in soft daylight".
3. After they agree, call `generate_image` for one image. Leave `model` out
   unless they name one.
4. Tell them they can ask for changes in plain words ("warmer light", "add a
   eucalyptus sprig"); `remix_image` applies the change to that image.

## 4. First product shoot

Explain in one sentence: a Studio shoot turns one photo of their real product
into a matching set of finished photos. Ask for a photo of the product (an
attachment, an image link, or a product page link). Then follow the
`product-shoot` skill.

## 5. What to know

- Everything is saved in the Masonry workspace. `list_creations` shows recent
  work.
- Every generation uses the workspace's credits. When a tool reports that the
  workspace is out of credits, pass its message on as written, don't retry,
  and don't add your own suggestion to buy anything.
- Videos can take a few minutes; a video joined from several scenes takes
  longer.

## Don't

- Don't generate anything the person hasn't agreed to.
- Don't invent the person's product, brand name, or results.
- Don't promise features the tools don't have, such as deleting creations or
  opening another workspace.
