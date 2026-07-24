# Aificient Studio User Guide

Last reviewed: July 24, 2026.

This guide explains how to use Aificient Studio from the application interface. It focuses on visible screens, menus, controls, generation workflows, editing tools, GPU management, settings, and common troubleshooting.

## 1. What Aificient Studio Does

Aificient Studio helps you create AI-generated videos from a written idea. You can:

- Brainstorm video ideas.
- Turn an idea into a structured concept.
- Create reusable characters.
- Generate scene images, narration, sound effects, video clips, and a final stitched video.
- Review and edit individual scenes.
- Regenerate only the parts that need changes.
- Render scene videos with a local GPU runtime, rented GPU instances, or Aificient Cloud when that option is available.

Most projects follow this path:

1. Create or select a concept.
2. Review the generated scenes and characters.
3. Choose render settings.
4. Generate assets and video.
5. Inspect the result in the canvas and scene sidebar.
6. Edit or regenerate parts if needed.
7. Download the final video.

## 2. Signing In

When you open the app, you may see a sign-in window.

Available sign-in methods can include:

- Google.
- Apple.
- Email code.

### Email Code

If email sign-in is available:

1. Enter your email address.
2. Click `Send code`.
3. Enter the 6-digit code you receive.
4. The app verifies the code automatically once all digits are entered.

The code screen also lets you:

- Resend the code after the cooldown.
- Use a different email.
- See when the code expires.

## 3. Main Workspace

After signing in, the left sidebar stays visible while the main area changes with what you are doing:

- Left sidebar: primary navigation, recent projects, project search, generation assets, and the user/settings area.
- Home/new-project screen: appears in the main area when no project is open. It contains the Concept, Brainstorm, and Character creation chats.
- Center canvas: appears when a project is open and shows its visual flow and generated assets.
- Right scene sidebar: appears with an open project and contains the project outline, asset browser, project-specific settings, and resume actions.

The top-right window controls let you minimize, maximize/restore, or close the app. The same top-right area also has an `Ask AI` button that opens the Support Assistant, an in-app help chat (see "Support Assistant (Ask AI)").

If no project is selected, the main area shows the home/new-project screen instead of an empty canvas. The left sidebar remains available so you can open an existing project, search, manage characters, or inspect generation assets without closing the creation screen.

## 4. Left Sidebar

### Primary Navigation

The top of the sidebar contains:

- `New project`: leaves the currently open project, shows the home/new-project screen in the main area, and starts a fresh creation chat when needed.
- `Character list`: opens the reusable-character library over the current screen.
- `Generation assets`: opens a flyout beside the sidebar with Aificient Cloud jobs, the local GPU, rented GPU instances, and the create-instance action.

The magnifying-glass button in the sidebar header opens project search. With an empty search it lists recent projects; type to filter by name. You can click a result or use the up/down arrow keys and `Enter`. Press `Esc` or click outside the dialog to close it.

### Recent Projects

The `Recent projects` list shows projects stored in your workspace. Click a row to leave the home screen and open that project's canvas.

A project row can show:

- Active selection.
- Running/generation indicator.
- Final video completed indicator.

When you open a project, a progress overlay can move through `Loading project`, `Checking for active renders`, `Building canvas`, and `Preparing scenes` before the canvas becomes ready. Media previews are loaded in a controlled queue during this process so large projects do not try to decode every image and video at once.

### Project Menu

Right-click a project to open its menu.

Available actions:

- `Rename`: opens a rename dialog for the selected project. Enter a new project name and select `Rename`, or press `Enter`, to save it.
- `Delete`: removes the project.

Deleting a project is permanent from the app's point of view, so use it carefully.

## 5. GPU and Runtime Manager

Open `Generation assets` in the primary sidebar navigation to manage generation resources. Its flyout appears beside the sidebar and closes when you select an item, click elsewhere, or press `Esc`.

The `Generation assets` row can show compact counts for resources that are actively working and resources that are ready. Inside the flyout, select the local GPU or a rented instance to open its detail view. If cloud jobs exist, the flyout also includes `Aificient Cloud`.

Initial video rendering with a GPU you manage needs a ready runtime. A runtime can be:

- Local: uses your machine's GPU.
- Rented: uses a remote GPU instance.

For an existing project whose images and audio are ready, `Resume Generation` can also offer subscription-backed Aificient Cloud rendering without requiring your own ready runtime (see below).

The manager groups resources by status:

- Running/ready.
- Starting or installing.
- Stopped/inactive.
- Error.

### Local Runtime

The local runtime lets you render videos with your own GPU.

Useful notes:

- It is intended for Windows in the current app.
- It requires a GPU with enough VRAM.
- The UI shows if your GPU is unsupported or below the requirement.
- Setup may require significant disk space.

From the local runtime detail view, you can:

- Install or prepare the runtime.
- Start it.
- Stop it.
- Watch setup progress.
- View logs if something fails.

### Rented GPU Instances

Rented GPU instances are managed from the sidebar and the create-instance modal.

From an instance detail view, depending on state, you may be able to:

- View setup progress.
- View logs.
- Start.
- Stop.
- Reboot.
- Destroy.

Only ready instances can be selected for video rendering.

When an instance is running, its detail view also shows a **render queue** for that GPU (see below).

### Render Queue

GPUs are no longer locked to a single project. Each GPU has its own render queue, and every scene video becomes a job that waits its turn on the GPU you chose for it. This means several projects can line up on the same GPU at once, and a busy GPU is still a valid choice — your videos simply render after the ones already ahead of them.

The final stitch does not use a GPU: it runs locally in the app once all of a project's scene clips are ready. Local stitches have their own one-at-a-time queue — if several projects finish rendering around the same time, their stitches run one after another (see the Stitch Node section).

The render queue appears in the local runtime and rented instance detail views while the GPU is ready/running. For each GPU it shows:

- Jobs grouped by project, in the order they will run.
- The job currently rendering, with a live progress bar and percentage.
- Queued jobs marked as waiting, with their position in line.

From the render queue you can:

- Remove a single queued video, or cancel the one that is currently rendering, using the `X` on its row.
- Cancel all of a project's videos across every GPU at once with `Cancel all` next to the project name.

The `Generation assets` flyout shows a small `N queued` count next to each local or rented GPU so you can see at a glance how loaded it is without opening the detail view.

### Aificient Cloud Rendering

In addition to GPUs you manage yourself, eligible projects can use `Aificient Cloud` to render scene videos. It can appear as a runtime on the initial render-settings screen and later in the selected project's `Resume Generation` menu when source images and audio are ready.

The Aificient Cloud option shows the project's `Lite` or `Pro` tier, resolution, and estimated credit cost before submission. It requires an active subscription, enough credits, and valid image/audio inputs. A submission can contain up to 32 missing scenes, and each scene's audio plus configured voice delays must fit within the 13-second cloud-render limit.

Aificient Cloud is selected by itself; it cannot be combined with local or rented GPUs in the same submission. Once submitted, each scene appears as a separate cloud job. The app refreshes completed clips into the project automatically.

When cloud jobs exist, open `Generation assets > Aificient Cloud` to view the current session's queue and history. The window shows queued, running, completed, failed, and cancelled jobs with progress and status messages. You can remove an individual queued job or use `Cancel queued` for all queued jobs in a project. Reserved credits are refunded when a cloud job fails or is cancelled.

While cloud clips are queued or rendering, the center canvas keeps showing the project's overall generation progress and the bottom of the right scene sidebar shows the Aificient Cloud queue/rendering status. Cancel queued cloud clips from `Generation assets > Aificient Cloud`; the canvas progress bar does not include a cloud-cancel button.

For account-wide cloud render history, including settled prices, use `Settings > Usage > Load latest generation jobs`.

## 6. Renting a GPU

Open `Generation assets` and click `Create instance` to open the GPU rental modal. If no Vast.ai key is configured, the flyout shows `Add Vast.ai key` instead.

The modal lets you choose a GPU profile and shows available offers.

Common profiles:

- RTX 4090: budget option.
- RTX 5090: balanced option.
- A100: professional option.
- H100: premium option.

The offers table can include:

- GPU model.
- VRAM.
- Number of GPUs.
- Price.
- Upload and download bandwidth (speed in Mbps and transfer cost per TB).
- Reliability.
- Rent action.

### Download Quality Indicator

The `Download` column shows a small colored status dot next to the speed and cost. It is a quick visual hint for how well an offer can pull large model and asset files, balancing download speed against transfer cost:

- Green: fast and cheap — at least 1500 Mbps and under $3/TB.
- Yellow: acceptable — at least 900 Mbps and under $6/TB.
- Red: everything else (slower or more expensive downloads).

Hover the dot to see a short text label. Greener dots generally mean faster instance setup and cheaper data transfer; red dots can mean slower setup or higher costs.

If no offers appear, try adjusting GPU settings in `Settings > GPU Config`.

## 7. Creating a New Project

Click `New project` in the sidebar to show the creation home screen in the main workspace. It is no longer a centered modal: the left sidebar stays visible, and the creation screen replaces the project canvas until you open or create a project. Clicking `New project` while a project is open deselects that project and begins a fresh creation chat when needed.

The creation home screen has three modes in the segmented control at the top of the chat composer:

- `Concept`.
- `Brainstorm`.
- `Character`.

The top-right `History` control opens previous Concept, Brainstorm, and Character chats. You can reopen a chat, refresh the history, or delete a saved chat. The active conversation title appears in the top bar after the conversation has started.

### Concept Mode

Use Concept mode when you already have a video idea.

Typical workflow:

1. Enter your idea.
2. Choose style, duration, language, and optional characters.
3. Send the prompt.
4. Review the generated concept.
5. Ask for corrections, or edit the concept directly with `Edit` (see "Reviewing and Editing the Generated Concept").
6. Continue to render settings.

The generated concept can include:

- Title.
- Artistic style.
- Narrator.
- Characters.
- Scene list.
- Scene descriptions.
- Scene scripts.
- Sound effect cues.

### Brainstorm Mode

Use Brainstorm mode when you want help exploring ideas.

Typical workflow:

1. Enter a topic or rough direction.
2. Review the generated idea options.
3. Ask for more options or corrections.
4. Choose an idea to turn it into a full concept.

### Character Mode

Use Character mode to create reusable characters for your library.

You can set:

- Character prompt.
- Gender.
- Reference image.
- Voice.
- Visual style.

Generated characters can later be pinned into video concepts.

### Stopping an In-Progress Chat Request

While a brainstorm, concept, or character request is being generated, the chat's send button turns into a stop button (a filled square). Click it to cancel the request you just started.

When you cancel:

- The request stops and the chat shows a neutral `Generation canceled.` note instead of an error.
- A late or stale result is not applied after you cancel.
- If the request had already finished on the server, its real result is shown instead of being discarded.
- If the request is no longer available, the chat shows that it is no longer available.

Canceling affects only the single in-progress chat request. It does not remove previous messages, ideas, concepts, or characters you already created. This stop button is separate from `Stop Generation` for video and asset rendering (see "Stop Generation").

### Reviewing and Editing the Generated Concept

Yes — you can change the script before you start generating. There are two ways to do it, on two different screens of the creation flow. You can use either one, or both.

**1. Ask the AI in the chat (concept/brainstorm screen).** While you are still in the chat conversation, keep typing to request changes in natural language — for example, "make scene 2 funnier", "rename the main character to Mia", or "shorten the narration". The assistant rewrites the concept for you and the conversation updates with the result. This is best when you want the AI to rework wording, tone, or whole sections.

**2. Edit by hand on the render-settings screen.** When you continue from the concept, the render-settings screen slides into the main workspace and a `Script` preview panel appears on the right. Click `Edit` at the top-right of that panel to switch it into edit mode. The button changes to `Done`; click it again to apply your changes and leave edit mode. This is best for small, exact fixes, and it sits next to the render settings and the `Generate` button. Use the back arrow in the render-settings header to return to the chat.

While editing by hand on the render-settings screen, you can change:

- Video title.
- Narrator voice profile (the short description of how the narrator should sound).
- Character names and descriptions.
- Which characters appear in each scene (toggle the character chips under `Characters in scene`).
- Each scene's title, description, and spoken line/script.

Notes:

- The `Edit` button is on the render-settings screen, not on the chat screen. On the chat screen you edit by asking the AI with a prompt instead.
- Library (global) characters and the narrator are locked in the hand editor. The panel labels them and points you to the character library to change a global character.
- Your edits, whether from the chat or made by hand, are applied to the concept that gets generated, so they directly affect the resulting video.
- This editing happens on the concept before generation. To change scenes or assets after generation, use the canvas nodes and rewrite tools (see "Editing and Regeneration").

## 8. Creation Controls

The creation controls sit in and directly below the chat composer at the bottom of the home screen. Switch modes along the composer's top edge; use the pills and segmented controls below the prompt for style, duration, language, pinned characters, and Character-mode options.

### Visual Style

The style picker includes presets such as:

- 3D animation.
- Classic cartoon.
- Anime.
- Retro pixel art.
- Cinematic realistic.
- Comic/manga.
- Watercolor.
- Low poly.
- Isometric animation.

The style affects concept writing and visual generation.

You can also change the style while refining a concept in the chat. If you pick a different style and then send a correction, the new style is applied to the refined concept. If you change it more than once during refinement, the most recent selection wins.

### Duration

Available durations include:

- 15 seconds.
- 30 seconds.
- 45 seconds.
- 60 seconds.
- 120 seconds.
- 180 seconds.

Longer videos usually mean more scenes, more assets, and more render time.

### Language

The app supports English and Spanish concept generation.

Language affects:

- Script text.
- Narration.
- Scene wording.

### Pinned Characters

In Concept and Brainstorm modes, you can pin existing library characters. Pinned characters are included in the concept so the generated story uses them.

### Voice

When you assign a voice (in `Character` mode, the character editor, or Settings), the app opens a voice picker. It lists a set of named voices, each shown with:

- A `Male` or `Female` tag.
- The voice name.
- A short description of how it sounds (for example, "Warm, inviting voice" or "Firm, confident delivery").

Each row has a play button. Click it to hear a short preview of that voice, and click again (or the square) to stop. Voices that match the relevant gender are listed first. When a voice is required, the picker hides the `Clear` option; otherwise you can clear the selection to fall back to a default.

## 9. Character Library

The character library stores reusable characters. Open it from `Character list` in the left sidebar; it appears as an overlay without leaving the current home screen or project.

A character can include:

- Name.
- Description.
- Type.
- Gender.
- Voice.
- Visual image.
- Style information.

The all-characters view lets you:

- Create a new character with `New character` (this closes the library and opens Character mode on the home screen).
- Search characters.
- Filter by type.
- Filter by gender.
- Filter by voice.
- Open details.
- Rename characters from their detail view.
- Preview images.
- Delete characters.

When Character mode is open on an empty creation chat, the home screen also shows up to six characters from your cast; use `See all` when more are available.

Characters from the library are treated as global references. They cannot be edited directly from a project canvas node.

## 10. Render Settings

Before starting generation, the app shows render settings.

### Format

Choose:

- Aspect ratio: `16:9` or `9:16`.
- Resolution: `1080p` or `720p`.

Use `9:16` for vertical/social video. Use `16:9` for widescreen video.

### Runtime

For the first generation, choose one or more ready GPUs or select `Aificient Cloud` if it is available for your account. Each ready local or rented runtime is listed with a checkbox; tick every GPU you want this project to use. Aificient Cloud is a separate, mutually exclusive target, so selecting it clears the local/rented GPU selection. Its row shows the selected `Lite` or `Pro` tier, resolution, and estimated credit cost.

- **One GPU selected:** all scene videos render on that GPU, in queue order.
- **Several GPUs selected:** the scene videos are split across the chosen GPUs so the project finishes faster. Each option also shows how many jobs are already `in queue` on it.
- **Aificient Cloud selected:** scene videos are submitted to the cloud after their source images and audio are prepared; the app continues through captions and final stitching as the clips arrive.

GPUs are queued rather than blocked, so a busy GPU is still a fine choice — selecting it just adds this project's videos to its queue behind any work already running. By default the app pre-selects the lightest-loaded GPU.

If no local or rented GPU is ready, you can select Aificient Cloud when available or generate images and audio only.

What you can do depends on GPU availability:

- No local/rented GPU and no Aificient Cloud option: generate images and audio only, review assets, edit scenes, and prepare the project for later video rendering.
- Local GPU ready: render video if the app shows the local runtime as supported and ready.
- Rented GPU ready: render video on any selected rented instance.
- Aificient Cloud available: render scene videos without starting your own GPU runtime.
- Busy GPU: no need to wait — selecting it queues your videos behind the current job. Select additional GPUs to spread the work and finish sooner.

### Quality

Two tiers are shown as labelled buttons, each with an icon and a short blurb:

- `Lite`: "Faster, lower VRAM" — renders faster and runs on smaller GPUs.
- `Pro`: "Best quality" — takes longer but gives the best quality.

Suggested use:

- Use `Lite` for previews, quick feedback, or when your GPU has less than 31 GB of VRAM (the app shows a `Recommended` badge on `Lite` in that case).
- Use `Pro` for finished videos when the selected GPU has enough memory.
- A100 runtimes require `Pro`; the app blocks the `Lite`/FP8 path on an A100 and asks you to switch.

### Images and Audio Only

Enable this option when you want to generate:

- Character references.
- Scene images.
- Narration.
- Sound effects.

Video rendering and final stitching are skipped. This is useful for reviewing assets before spending GPU time.

## 11. Center Canvas

The canvas shows the project as a connected visual flow.

Common node groups:

- Project info.
- Character references.
- Script.
- Scenes.
- Scene text/details.
- Images.
- Audio.
- Video clips.
- Stitch.
- Final output.

You can pan, zoom, and use the mini-map to navigate larger projects.

## 12. Canvas Nodes

### Project Info

Shows:

- Project name.
- Style.
- Duration.
- Scene count.

### Script

Shows script status and can open script details once ready.

Script details can include:

- Style.
- Duration.
- Narrator.
- Scene list.

### Scene

Shows:

- Scene number.
- Scene title.
- Duration.

### Description, Character Reference, Script, and SFX Nodes

These nodes show editable scene text.

Click them to open rewrite tools when generation is not active.

### Character Node

Shows a character reference image and metadata.

For project-local characters, actions may include:

- Edit character.
- Regenerate visuals.

Global/library characters are protected from direct project editing.

### Image Node

Shows the generated scene image.

Actions can include:

- Preview fullscreen.
- Retry loading.
- Delete image.

Deleting a scene image means dependent video assets must be regenerated.

### Audio Node

Shows available audio tracks.

Actions can include:

- Play/pause.
- Seek.
- Retry loading.
- Regenerate audio.

Regenerating audio can affect later video stages because video timing depends on audio.

### Video Node

Shows a generated scene video clip.

While a clip is waiting in a local, rented, or Aificient Cloud render queue, the node shows a colored `Queued` badge with a small queue icon instead of its normal status icon. Once rendering starts, it switches to the normal active/progress state.

Actions can include:

- Play/pause.
- Seek.
- Fullscreen preview.
- Delete video.
- Rate the clip with thumbs up or thumbs down. A dislike can include an optional preset reason or custom comment; select the active rating again to clear it.

Deleting a scene video means the final video must be regenerated.

### Stitch Node

Shows final video stitching status. The stitch runs locally in the desktop app (no GPU needed) as soon as every scene clip is ready: the app downloads the clips, combines them with the configured transition, writes the provenance watermark, and uploads the final video to your project.

Only one stitch runs at a time. If several projects finish rendering around the same time, their stitches queue up and run one after another — a waiting stitch shows `Queued` with a `Waiting for another stitch to finish` message until it is its turn. Cancelling a generation also removes its stitch from this queue.

While a stitch is running, the node can report these steps:

- Downloading scene videos.
- Analyzing scene videos.
- Stitching scene videos (with live progress).
- Writing the provenance watermark.
- Uploading the final video.

Possible states:

- Queued (waiting for another local stitch to finish, or preparing to start).
- Waiting.
- Running.
- Completed.
- Error.
- Skipped.

Local stitching needs a working internet connection to download the clips and upload the result, plus temporary free disk space. Temporary files are cleaned up after the stitch finishes.

If every required scene clip is ready but the final video is missing, the action at the bottom of the right sidebar is labelled `Stitch Final Video`. Select it to start the local stitch without choosing a GPU.

### Output Node

Shows the final video when available.

Actions can include:

- Play.
- Seek.
- Fullscreen.
- Download.
- Rate the final video with thumbs up or thumbs down, optionally adding a reason when you dislike it.

## 13. Fullscreen Media Viewer

Images and videos can open in fullscreen.

Available actions:

- Download.
- Share.
- Close.

If sharing is not available on your system, the app falls back to copying or opening the media link.

## 14. Right Scene Sidebar

The right sidebar appears when a project is selected.

It has three tabs:

- `Schema`.
- `Assets`.
- `Settings`.

### Schema Tab

The Schema tab is a project outline.

It shows:

- Project.
- Characters.
- Scenes.
- Final video.

Clicking an item focuses the related node on the canvas.

Scene rows can show:

- Duration.
- Asset readiness.
- Generation status.
- Missing or completed stages.

### Assets Tab

The Assets tab groups generated files.

Common groups:

- Scene images.
- Character images.
- Narration.
- Sound effects.
- Generated audio.
- Raw clips.
- Final video.
- Metadata.

Actions can include:

- Focus related node.
- Download asset.

### Settings Tab

The Settings tab controls project-specific video settings.

Sections:

- Format.
- Model.
- Audio.
- Captions.

You can change:

- Aspect ratio.
- Resolution.
- Quality (Lite or Pro).
- Guidance values (Video/Audio CFG).
- Speech pace.
- Voice timing.
- Sound effect volume.
- Transition duration.
- Whether captions are burned into this project's videos.
- Caption position, font, size, and colors.

If settings are changed, apply them before rendering video. The app may block video generation while project settings have unsaved changes.

## 15. Resume Generation

`Resume Generation` appears when a project has missing or invalidated assets.

Use it after:

- Stopping generation.
- Deleting an image, audio, or video.
- Rewriting scene text.
- Editing character visuals.
- A generation failure.
- Running images/audio first and rendering video later.

The resume menu lets you:

- Choose one or more ready GPUs for video (selecting several splits the render across them).
- Choose `Aificient Cloud` by itself to render eligible missing scene videos for the displayed credit estimate.
- Generate images and audio only.

The app reuses existing completed assets where possible and only regenerates missing or affected parts.

When all raw scene clips are already ready, no GPU choice is needed. The same sidebar action runs the remaining caption burns and final stitch locally. If only the final stitch remains, its label changes to `Stitch Final Video`.

### What Resume Can Run

Depending on project state and available GPU resources, Resume can be used for:

- Images and audio only: does not require a ready video GPU.
- Scene video rendering: requires at least one ready local or rented runtime. You can select several GPUs to split the remaining scene videos across them.
- Aificient Cloud scene rendering: requires eligible source assets, a subscription, enough credits, no more than 32 missing scenes, and supported scene lengths. It does not require your own ready GPU.
- Missing captioned clips: uses saved word timings when available, burns captions locally, and does not require a GPU.
- Final stitching: requires the scene videos to be ready; it then runs locally in the desktop app without using a GPU.
- Recovery after failure: reruns only the missing or failed stages where possible.

If the project already has images and audio, Resume can move directly toward video rendering once you pick Aificient Cloud or one or more of your own GPUs. Work sent to your GPUs is added to their render queues, so it starts even if a GPU is currently busy. If only video is missing, the app does not need to recreate the whole concept.

## 16. Stop Generation

When generation is active, the sidebar shows a stop/cancel action.

Stopping generation:

- Stops the current app-side generation flow.
- Attempts to cancel active video work.
- Marks unfinished phases as cancelled.

You can usually continue later with `Resume Generation`.

This stop action is for video and asset generation. To cancel a brainstorm, concept, or character request on the creation home screen, use the stop button that replaces the chat's send button (see "Stopping an In-Progress Chat Request").

## 17. Generation Error Summary

When a generation finishes, the canvas can show an error summary box in the top-right corner. It only appears if one or more parts of the generation failed. If everything succeeds, no box is shown.

The box starts collapsed, showing only a header such as `Generation finished with 3 errors`. Click the header (or its chevron) to expand the full list, and click it again to collapse it. The box stays on screen until you clear it, or until you start a new generation or resume the project.

To clear the box, click the trash/`Clear` button next to the header. This dismisses the summary for the current project.

### What It Shows

When expanded, the box lists every failure from the most recent finished generation, grouped into two categories:

- `Runtime tasks`: work that runs on the GPU runtime (video generation and audio alignment) plus the final stitch, which runs locally in the app.
- `API tasks`: work that runs on the cloud service, such as character images, scene images, narration, and sound effects.

Each entry shows:

- The type of generation that failed (for example, `Video generation` or `Audio`).
- The scene it belongs to, when the failure is scene-specific.
- The reason reported for the failure.

If a reason is long, it is shortened with a `Show more` link; click `Show more` to read the full text and `Show less` to collapse it again.

Cancelled steps are not listed as errors. If you stop a generation, the box still reports any real failures that happened before you stopped, but it does not list the steps that were simply cancelled.

### What To Do With It

Use the summary to decide what to fix or rerun:

- For `API task` failures (images, audio, SFX, characters), review or rewrite the affected scene or character, then use `Resume Generation`.
- For `Runtime task` failures (video, alignment), check that a GPU runtime is ready and review its logs, then use `Resume Generation`. Stitch failures happen locally — check your internet connection and disk space, then use `Resume Generation` to retry the stitch.

If you encounter a **409 error**, this indicates the runtime is busy with a task, possibly due to a state mismatch between the runtime and the UI. Wait a few minutes and try again; if the issue persists, restart the runtime.

The box reports results for the currently selected project. Switching projects hides it; it reappears for the project it belongs to until you dismiss it or start a new run.

## 18. Editing and Regeneration

Aificient Studio lets you change individual parts of a project without starting from scratch. Some edits are manual, some can be AI-assisted, and some require regeneration because later assets depend on the edited part.

This section covers editing a project after generation, from the canvas. To edit the concept before generation (its title, characters, scenes, and scripts), continue from the creation chat to render settings and use the `Edit` button in the right-side `Script` panel instead (see "Reviewing and Editing the Generated Concept").

In general:

- Manual edit means you type the replacement yourself.
- AI edit means you describe the change you want and the app rewrites that component.
- Regeneration means the app recreates missing or invalidated assets while keeping completed assets that are still valid.

### Rewrite Scene Text

Scene text can be rewritten manually or with AI.

Editable scene fields:

- Description.
- Character reference.
- Script.

How to use it:

1. Click the scene text node on the canvas.
2. Choose manual edit or AI rewrite.
3. Enter the replacement text or rewrite instruction.
4. Confirm the change.
5. Regenerate the affected assets when prompted.

Rewriting these fields can remove dependent generated assets so the project stays consistent.

Examples:

- Changing the description usually requires a new image and video.
- Changing the script usually requires new narration and video.
- Changing character references usually requires new visuals.

### Rewrite SFX

The SFX editor lets you:

- Add cues.
- Remove cues.
- Change cue descriptions.
- Change cue start times.
- Change cue durations.
- Ask AI to rewrite the sound design.

Cue validation helps prevent invalid timings.

Changing SFX can require regenerating generated audio, video clips, and final output.

Manual SFX editing is best when you know the exact cue timing. AI SFX editing is best when you want to describe the overall sound direction, such as making the sound design softer, more cinematic, simpler, or more realistic.

### Edit Character

For editable project characters, the character editor can change:

- Name.
- Gender.
- Type.
- Humanized setting.
- Description.
- Voice (narrator characters only).

You can edit manually or ask AI to rewrite the character. In manual mode, only the fields you actually change are applied, so a voice-only change leaves the rest untouched.

The `Voice` control appears only for the narrator. It uses the same voice picker with previews described under "Voice", so you can listen before choosing. For library (global) characters the voice is locked and shown read-only — change it in the character library instead.

What gets invalidated depends on what you change:

- Changing a visual field (name, gender, type, humanized, description) or using AI rewrite deletes the character's reference image and the scene visuals where it appears. Narration, SFX, and other audio are preserved.
- Changing only the voice keeps the artwork (scene images and the reference image) but deletes the narration audio and rendered video for the affected scenes. Re-generate audio and video to apply the new voice.

The editor's warning box updates to tell you which of these will happen before you confirm.

Manual character editing is best for exact name/type/description/voice changes. AI character editing is best when you want to preserve the character idea but change the style, personality, appearance, or level of detail.

### Delete Assets

Some nodes let you delete specific assets.

After deletion, use `Resume Generation` to regenerate what is missing.

Typical effects:

- Delete image: the scene image is removed, and video for that scene may need to be regenerated.
- Regenerate audio: narration/SFX-related audio is recreated, and dependent video may need to be regenerated.
- Delete video: the scene clip is removed, and the final video must be regenerated.
- Regenerate character visuals: character reference imagery and affected scene visuals may need to be regenerated.

### Regenerate vs Resume Generation

Use `Regenerate` when a modal or node offers it immediately after an edit. It continues from the change you just made.

Use `Resume Generation` when you want the app to scan the project and continue whatever is missing. This is useful after stopping generation, fixing errors, deleting assets, or generating images/audio first.

The app does not intentionally regenerate everything. It keeps valid completed assets and focuses on the missing or affected stages.

## 19. Project Settings

Project settings affect the selected project.

Common settings:

- Aspect ratio.
- Resolution.
- Quality (Lite or Pro).
- Video guidance (Video CFG).
- Audio guidance (Audio CFG).
- Speech pace.
- Voice delays.
- SFX volume.
- Transition duration.
- Burn-in captions on or off.
- Caption position, font, size, and colors.

**Guidance (CFG)** controls how strictly the AI follows your prompts. **Video guidance (Video CFG)** determines how closely the video matches the scene description. **Audio guidance (Audio CFG)** determines how closely the generated audio matches the sound description. Higher values force stricter adherence to the prompt, while lower values allow more creative freedom.

Project settings can override global defaults for that project.

## 20. Global Settings

Open Settings from the user/profile area in the left sidebar.

Sections:

- General.
- Usage.
- Storage.
- Notifications.
- Social Accounts.
- API Keys.
- GPU Config.
- Model Config.
- Audio Config.
- Video Config.

### General

Shows:

- App version.
- User account information.
- Current subscription and an upgrade action.
- Update check.
- Help/contact link.

### Usage

This section shows the credits included with your plan, credits used and remaining, renewal or cancellation information, and usage over time. Depending on the subscription source, it can also provide plan-management, upgrade, or pending-change actions.

At the bottom, click **Load latest generation jobs** to open your account-wide Aificient Cloud video render history. This history includes jobs from all projects and lists the newest jobs first.

Each job can show:

- Content and scene name.
- Status: `Queued`, `Running`, `Completed`, `Failed`, `Cancelled`, or `Unknown`.
- Quality tier and resolution.
- Requested and finished times.
- Progress percentage plus the current stage or message while the job is queued or running.
- The settled credit price for a completed job, shown with the credit icon (for example, `1.2 credits`).

A price appears only when a completed render has been successfully settled by billing. Queued, running, failed, cancelled, and unknown jobs do not show a price. A completed job may also omit the price while billing is not settled.

Use **Previous** and **Next** to move through longer histories. The app refreshes the current page automatically while it contains queued or running jobs, and stops refreshing when no active jobs remain. Use the refresh control to check manually, or **Hide** to collapse the history.

### Storage

This section shows how much cloud storage your projects and assets use, your plan limit, the percentage consumed, and the remaining space. Warning and critical states explain when storage is close to or over the allowance.

If you need more room, remove unneeded project data or use **Upgrade your plan**. Storage-limit errors also appear in a banner at the top of the app with shortcuts to manage storage or view plans.

### Notifications

This section controls desktop alerts independently for:

- A scene video finishing.
- A final stitched project becoming ready.
- A GPU render queue becoming empty.
- A local or Vast.ai GPU finishing setup and becoming ready.

### Social Accounts

This section connects the social accounts you publish to. It is where you add or remove the accounts used by the Publish dialog (see "Publishing the Final Video").

Key points:

- Everything is **local to this computer**. Connecting an account opens a secure sign-in window, and your session stays on this device — nothing about your accounts is sent to a server.
- Each platform (TikTok, Instagram, YouTube) has its own row. **TikTok is supported today**; Instagram and YouTube show a `Coming soon` tag.
- Click `Connect` (or `Add` if you already have one) to sign in. You can connect **multiple TikTok accounts**.
- Each connected account shows its avatar, display name, and a status dot — green for `Connected`, amber for `Session expired` when its login needs to be refreshed.
- For an account marked `Session expired`, select its amber refresh/reconnect icon and sign in again. `Refresh metadata` checks account details and session state, but it does not replace an expired login.
- Hover an account and click the trash icon to remove it. Removing an account also forgets its local login.
- **Refresh metadata** (bottom-right of the panel) re-fetches the name, avatar, and follower count for your connected accounts without reconnecting them.

### API Keys

Used for external services such as Vast.ai GPU rental.

You can:

- Add/change the key.
- Show/hide the key.
- Check balance.
- Open the service page.

### GPU Config

Controls the rented GPU search.

Common options:

- Disk space.
- Max price.
- Minimum reliability.

Choose the GPU family in the `Create Instance` modal. `GPU Config` shows the selectable families and controls the shared Vast.ai search limits.

If offers are too expensive or no offers appear, adjust these settings.

### Model Config

Controls the default video-model settings used by new projects.

Common options:

- Quality (Lite or Pro).
- Negative prompt.
- Caption instructions.
- Local runtime download folder.
- Video guidance (Video CFG).
- Audio guidance (Audio CFG).
- Prefetch count.

**Caption Instructions** is optional free-form guidance the AI follows when it drafts a publish caption (with the **Generate** button in the Publish dialog). Use it to set a tone, style, call-to-action, emoji use, or other constraints — for example, "casual and punchy, end with a question, no more than two emojis." It applies to every project, and you can leave it blank.

The runtime download folder can only be changed while the local runtime is stopped and is not downloading, setting up, or booting. Use `Default` to return to the app's standard data folder.

### Audio Config

Controls:

- Speech pace.
- Sound effect volume.
- Whether generated concepts should include SFX cues.
- Default narrator voices.

#### Default Narrator Voices

This section sets a fallback `Male` and `Female` voice, each chosen with the voice picker (including previews). When a narrator has no voice assigned, the app picks one of these defaults based on the narrator's gender. Assigning a voice to a specific narrator in the character editor overrides the default for that narrator.

### Video Config

Controls the defaults used when creating new projects:

- Start voice delay.
- End voice delay.
- Transition duration.
- Captions.

Changing these global defaults does not alter an existing project. To change captions, timing, or other video settings for the selected project, use the right scene sidebar's `Settings` tab and apply the changes there.

### Captions

For an existing project, open the right scene sidebar's `Settings` tab, find `Captions`, and set `Burn-in captions` to `On` or `Off`. Apply the changes before continuing generation. Global `Settings > Video Config` supplies the caption defaults for newly created projects only.

When captions are enabled, you can adjust:

- Position.
- Font.
- Size.
- Text color.
- Highlight color.
- Outline color.
- Optional background color.

**How captions are made.** Captions are added *after* a scene's video is
rendered, not during it. Each scene gets a second box on the board — **raw clip
→ captioned clip** — and the captioned one is produced in two steps: Aificient
transcribes the finished clip to get word-by-word timings (a small paid step,
billed like other generations), then your own machine burns those captions into
a copy of the clip. That local render shares the same queue as the final
stitch, so it never competes with video generation on the GPU.

After caption generation, both versions of each scene are saved to your
project: the plain clip and the captioned one. You can therefore open the
project on another computer and still see and use the generated captioned cuts.

When captions are on, the final video is stitched from the captioned clips, so
the captions are baked into the video you publish.

Because the word timings are saved too, re-burning a scene's captions later —
to try a different font or color, say — is **free**. You are only charged again
if something changes the narration itself (a new script, new audio, or a
different voice), because that makes the old timings wrong.

### Turning Captions On or Off Later

Captions can be switched at any time from the selected project's right-sidebar
`Settings` tab. The raw scene videos do not have to be regenerated.

- **Turning captions on** adds the captioned-clip column to the board. Applying
  the change removes the old final video because it no longer matches the
  project's caption setting. Select `Resume Generation` to create all missing
  captioned clips locally and stitch a new captioned final video.
- **Changing caption style while captions remain on** removes the old
  captioned clips because their burned style is stale. The saved word timings
  are retained, so select `Resume Generation` to re-burn the clips locally at
  no additional transcription charge and rebuild the final video. Until that
  finishes, an older final video may still be available.
- **Turning captions off** hides the captioned-clip column and removes the old
  captioned cuts and final video. The plain clips are kept. Select
  `Stitch Final Video` to rebuild the final video from those plain clips.

In some restored or older projects, the Stitch node can instead show a
`Re-stitch with captions` or `Re-stitch without captions` shortcut when the
existing final video's recorded caption mode does not match the current
setting.

> Note: re-rendering a scene's video replaces its plain cut, and its captioned
> cut is removed at the same time — the old captions were burned onto the take
> you just replaced. The scene's captioned box goes back to empty, ready to be
> generated again through `Resume Generation`.

## 21. Publishing the Final Video

Once a project has a final video, you can post it straight to social media from inside the app. Open the **Publish** dialog with the `Publish` button at the bottom of the right scene sidebar (it becomes active only after the final video exists).

Publishing runs **entirely on your own machine**. The app drives a private background browser session that is signed in as your account; nothing about your accounts or your post is sent to an Aificient server. **TikTok is supported today** — Instagram Reels and YouTube Shorts appear as tabs but show a "coming soon" panel.

Before you can post, connect at least one account in `Settings > Social Accounts` (see "Social Accounts"). If you have none connected, the dialog links you straight there; you can also reach it any time with the **Manage** link.

### Choosing a Platform

The top of the dialog has a tab per platform (TikTok, Instagram, YouTube). Each platform has its **own composer**, because every platform posts under different rules. Pick a platform, then fill in that platform's post. Only TikTok's composer is active right now.

### Step 1 — Compose

In the composer you set up the post:

- **Accounts** — pick which connected account(s) to post to (only the selected platform's accounts are listed). Each shows its avatar and follower count, and selected ones get a check badge.
- **Caption** — write your caption in a single text box and put your `#hashtags` right inside it (hashtags are highlighted as you type). Click **Generate** — the atom button next to the section title — to have the AI draft a caption from your project; it follows the optional **Caption Instructions** you set in `Settings > Model Config`. (YouTube also shows a separate Title field.)
- **Sound** — attach a TikTok sound, or leave it unset to keep your video's original audio. Open the picker to **search** TikTok's public sound catalog, spot **Trending** sounds, and **preview** any track with the ▶ button before choosing. Once a track is selected it collapses into a row with a **volume** slider, and it plays over your video in the live preview so you can hear the mix. Browsing sounds needs no login.

The live **Preview** on the right mirrors how the post will look in the feed — the cover, caption, account handle, and the chosen sound spinning on the cover disc.

When the post is ready, click **Prepare publish** to slide to the review step.

### Step 2 — Review

The review step is a read-only recap plus the last two choices:

- **Posting to**, **Caption**, and **Sound** — a summary of what you set in compose.
- **Thumbnail (cover)** — choose the exact frame used as the cover. Drag the film-strip timeline to scrub anywhere in the video, or use the left/right peeks to nudge frame by frame. The chosen frame shows as a "Cover" preview.
- **When to publish** — choose **Publish now** or **Schedule**. Scheduling reveals a date/time picker; the time must be at least ~20 minutes in the future.

Use **Back** to return to compose, or **Publish now** / **Schedule** to start the hand-off.

### Upload Progress

As soon as you confirm, a **progress screen takes over the dialog and locks the form** so nothing changes mid-post. It shows:

- The platform badge in a spinning ring, the **current step**, the account, and elapsed time.
- A row of step icons that fill in as the upload advances: preparing the video → opening TikTok Studio → uploading → caption → cover → sound → publishing/scheduling. Completed steps turn green.
- A **Cancel** button that actually stops the background browser hand-off.

This progress is **saved app-wide**, not just in the dialog. You can close the Publish window and keep working — the post keeps going, and reopening Publish resumes the same live progress until it finishes.

When it completes you'll see either:

- **Success** — "Published to TikTok" (or "Scheduled on …" with the time). Choose **Post another** to clear the form for a fresh post, or **Done** to close.
- **Couldn't finish** — a short reason and the step it stopped at. Your caption, sound, and cover are kept, so **Back to editor** lets you try again.

### Publish History

The **History** button (top-right of the dialog) lists past and prepared posts, with links to live posts and the option to cancel a queued one. It is hidden while an upload is in progress.

> Note: TikTok publishing automates the real TikTok Studio composer in the background so your video is uploaded with the caption, cover, and sound attached, and the post is grouped under the chosen sound. TikTok changes its site often, so if a step can't be completed automatically the upload stops and shows an error — just try again.

## 22. Updates

The app can check whether a newer desktop version is available.

If an update is available:

1. A modal shows the current and latest version.
2. Click `Update` to start.
3. A dedicated update window shows download progress.
4. The installer opens when ready.
5. The app closes so the installer can continue.

If the update fails, the update window shows an error.

## 23. Downloads and Sharing

You can download final videos and many generated assets.

When downloading:

- Choose where to save the file.
- The app writes only to the selected location.
- Downloads may take time for large videos.

The fullscreen viewer also includes a share action when supported by your system.

## 24. Where To Find UI Options

Use this section when a user asks questions like "Where is X?", "How do I open X?", "Where can I change X?", "I cannot find X", or "Where is the button for X?".

When answering, give the shortest path from a stable area of the app, such as `left sidebar > Settings > GPU Config`. If an option only appears after selecting a project, opening a modal, generating an asset, or entering render settings, say that first.

### Main Navigation Locations

| User asks for | Where to find it |
| --- | --- |
| `Ask AI`, help chat, or Support Assistant | Top-right window-actions area, next to the minimize/maximize/close controls. |
| Window minimize, maximize, restore, or close | Top-right window controls. |
| Projects | Left sidebar, in the `Recent projects` list below the primary navigation. |
| Search projects | Magnifying-glass button in the left-sidebar header; it opens a search dialog with recent projects and filtered results. |
| Create a project or start a new idea | `New project` in the left sidebar; the creation home screen replaces the canvas while the sidebar stays visible. |
| Reopen or delete a creation chat | Creation home screen, `History` at the top-right. |
| Open the reusable-character library | `Character list` in the left sidebar. |
| Rename project | Right-click the project in the left sidebar project list, then choose `Rename`. |
| Delete project | Right-click the project in the left sidebar project list, then choose `Delete`. |
| Sign out | User/profile area at the bottom of the left sidebar. |
| Global Settings | User/profile area at the bottom of the left sidebar, then `Settings`. |
| GPU/runtime manager or Generation Assets | `Generation assets` in the left sidebar; it opens a flyout beside the sidebar. |
| Local runtime controls | Left sidebar > `Generation assets` > local GPU. |
| Rented GPU instance controls | Left sidebar > `Generation assets` > rented instance. |
| Runtime logs | Open the local GPU or rented-instance detail view from the `Generation assets` flyout. |
| Rent GPU or add cloud GPU | Left sidebar > `Generation assets` > `Create instance`. If a Vast.ai key is missing, use `Add Vast.ai key` first. |
| Download quality indicator / colored status dot on offers | GPU rental modal offers table, in the `Download` column next to each offer's speed and cost. |

### Creation Home Screen Locations

| User asks for | Where to find it |
| --- | --- |
| Concept mode | Left sidebar > `New project`, then choose `Concept` in the segmented control above the home-screen composer. |
| Brainstorm mode | Left sidebar > `New project`, then choose `Brainstorm` above the composer. |
| Character mode | Left sidebar > `New project`, then choose `Character` above the composer. |
| Idea prompt or chat prompt | Creation home screen, `Concept` or `Brainstorm` mode, in the bottom composer. |
| Character prompt | Creation home screen, `Character` mode, in the bottom composer. |
| Visual style | Creation home screen, style pill below the prompt. |
| Duration | Creation home screen, duration pill below the prompt in Concept or Brainstorm mode. |
| Language | Creation home screen, language control below the prompt in Concept or Brainstorm mode. |
| Pinned characters | Creation home screen, `Characters` pill below the prompt in Concept or Brainstorm mode. |
| Character library | `Character list` in the left sidebar, or the `Characters` picker in a Concept/Brainstorm composer. |
| Character search, filters, previews, rename, create, and delete | Left sidebar > `Character list`. |
| Reference image for a character | Creation home screen, `Character` mode, `Image`/`Reference` control below the prompt. |
| Character voice | Creation home screen, `Character` mode, `Voice` pill below the prompt. |
| Generate button for a concept | Creation home-screen chat, on the generated concept. |
| Stop or cancel a brainstorm, concept, or character chat request | Creation home-screen chat — while a request is generating, the send button becomes a stop (filled square) button; click it to cancel. |
| Edit the generated concept (title, characters, scenes, scripts) | Two ways: ask the AI in the `Concept`/`Brainstorm` chat, or click `Edit` in the `Script` preview panel on the render-settings screen. |
| Edit the script by asking the AI / with a prompt | Creation home-screen `Concept` or `Brainstorm` chat — type the change you want and the assistant rewrites the concept. |
| `Edit` button for the script | Right-side `Script` preview panel on the render-settings screen (after continuing from the concept), not on the chat screen. |
| Edit a scene title, description, or script before generating | Render-settings `Script` preview panel in `Edit` mode, in the scene's card. |
| Change which characters appear in a scene | Render-settings `Script` preview panel in `Edit` mode, under `Characters in scene`. |
| Edit the narrator voice profile | Render-settings `Script` preview panel in `Edit` mode, in the `Narrator` section. |
| Render settings before first generation | Continue from a generated concept on the creation home screen; render settings slide into the main workspace. |

### Render And Generation Locations

| User asks for | Where to find it |
| --- | --- |
| Aspect ratio | Initial render-settings screen, or selected project > right sidebar > `Settings` tab. |
| Resolution | Initial render-settings screen, or selected project > right sidebar > `Settings` tab. |
| GPU choice for rendering | Initial render-settings screen, or `Resume Generation` menu on the right sidebar. |
| Aificient Cloud rendering | Choose `Aificient Cloud` on the initial render-settings screen when available, or select a project with ready images/audio and use right sidebar > `Resume Generation` > `Aificient Cloud`. |
| Aificient Cloud queue and current-session history | Left sidebar > `Generation assets` > `Aificient Cloud`; the row appears after cloud jobs have been submitted. |
| Aificient Cloud queue/render progress | Center-canvas generation progress bar and the status at the bottom of the right scene sidebar. Cancel queued clips from `Generation assets > Aificient Cloud`. |
| Generate images and audio only | Initial render-settings screen, or `Resume Generation` menu when available. |
| Quality (Lite or Pro) | Initial render-settings screen, selected project > right sidebar > `Settings`, or global `Settings > Model Config`. |
| Negative prompt | Global `Settings > Model Config`. |
| Video guidance (Video CFG) | Selected project > right sidebar > `Settings`, or global `Settings > Model Config`. |
| Audio guidance (Audio CFG) | Selected project > right sidebar > `Settings`, or global `Settings > Model Config`. |
| Prefetch count | Global `Settings > Model Config`. |
| Speech pace | Selected project > right sidebar > `Settings`, or global `Settings > Audio Config`. |
| SFX volume | Selected project > right sidebar > `Settings`, or global `Settings > Audio Config`. |
| Generate SFX cues | Global `Settings > Audio Config`. |
| Default narrator voices (male/female fallback) | Global `Settings > Audio Config`, in the `Default Narrator Voices` section. |
| Start voice delay or end voice delay | Selected project > right sidebar > `Settings`, or global `Settings > Video Config`. |
| Transition duration | Selected project > right sidebar > `Settings`, or global `Settings > Video Config`. |
| Enable or disable captions for an existing project | Select the project > right sidebar > `Settings` > `Captions` > `Burn-in captions`, then apply the changes. |
| Set caption defaults for new projects | Global `Settings > Video Config`; caption styling appears after captions are enabled. |
| Change caption position, font, size, colors, outline, or background for an existing project | Select the project > right sidebar > `Settings` > `Captions`, then apply the changes. |
| Generate all missing captioned clips | Right sidebar > `Resume Generation`; when the raw clips are ready, the caption work runs locally without a GPU picker. |
| Re-burn captions after changing their style | Apply the project caption-style change, then select `Resume Generation`; saved word timings are reused. |
| Build a missing final video when all required clips are ready | Bottom of the right sidebar > `Stitch Final Video`. Some restored projects may instead offer `Re-stitch with captions` / `Re-stitch without captions` on the Stitch node. |
| Resume Generation | Right scene sidebar for the selected project, shown when assets are missing or invalidated. |
| Stop or cancel video/asset generation | During active generation, in the visible generation/progress controls or right sidebar stop action. To cancel a brainstorm/concept/character chat request instead, use the stop button in the creation home-screen chat. Cloud queue cancellation is under `Generation assets > Aificient Cloud`. |
| Generation error summary, error box, or list of failed tasks | Top-right corner of the center canvas, shown after a generation finishes with one or more errors. |
| Publish | Bottom area of the right scene sidebar for the selected project. Opens the Publish dialog to post the final video to TikTok, Instagram Reels, or YouTube Shorts. Enabled once the project has a final video. |
| Generate an AI caption | Publish dialog, compose step, the `Generate` (atom) button next to the caption section. |
| Add or change a TikTok sound | Publish dialog, compose step, the `Sound` section picker. |
| Choose the cover / thumbnail frame | Publish dialog, review step (after `Prepare publish`), the `Thumbnail` section. |
| Schedule a post for later | Publish dialog, review step, `When to publish` > `Schedule`. |
| Cancel an in-progress upload | Publish dialog upload progress screen, the `Cancel` button. |
| Publish history (past/queued posts) | Publish dialog, `History` button at the top-right. |

### Project Review And Editing Locations

| User asks for | Where to find it |
| --- | --- |
| Project outline | Select a project, then open the right scene sidebar > `Schema` tab. |
| Scene list | Select a project, then right scene sidebar > `Schema` tab. |
| Asset browser | Select a project, then right scene sidebar > `Assets` tab. |
| Project-specific settings | Select a project, then right scene sidebar > `Settings` tab. |
| Focus a scene or node | Click an item in right scene sidebar > `Schema`, or use a focus action in `Assets`. |
| Scene description, character reference, script, or SFX text | Center canvas, in the scene's text/detail nodes. |
| Rewrite scene text | Click the scene text node on the center canvas, then choose manual edit or AI rewrite. |
| Rewrite SFX | Click the SFX/text detail node for the scene on the center canvas. |
| Edit a project character | Click the character node on the center canvas when the character is editable. |
| Change a narrator's voice | Click the narrator's character node on the center canvas, then use the `Voice` picker in the character editor (locked for library characters — change those in the library). |
| Delete scene image | Scene image node on the center canvas. |
| Regenerate audio | Audio node on the center canvas. |
| Delete scene video | Video node on the center canvas. |
| Like, dislike, or clear feedback on a video | Scene Video node or final Output node on the center canvas; use the thumbs controls on the video. |
| Regenerate character visuals | Character node on the center canvas. |
| Fullscreen media viewer | Click an image or video preview in the canvas or asset views. |
| Download an asset | Right scene sidebar > `Assets`, a canvas media node, the Output node, or the fullscreen media viewer. |
| Download final video | Output node on the center canvas, right scene sidebar > `Assets` > final video, or fullscreen media viewer. |
| Share media | Fullscreen media viewer, when sharing is supported by the system. |

### Global Settings Locations

| User asks for | Where to find it |
| --- | --- |
| App version | `Settings > General`. |
| Account information | `Settings > General`, or the user/profile area in the left sidebar. |
| Check for updates | `Settings > General`. |
| Help/contact link | `Settings > General`. |
| Credit usage and usage timeline | `Settings > Usage`. |
| Cloud video generation history across all projects | `Settings > Usage`, then `Load latest generation jobs`. |
| Settled price for a completed cloud render | `Settings > Usage`, then `Load latest generation jobs`; the price appears on the completed job when billing has settled. |
| Storage used, limit, or available space | `Settings > Storage`. |
| Desktop notification preferences | `Settings > Notifications`. |
| Connect or remove a social account (TikTok, etc.) | `Settings > Social Accounts`. |
| Reconnect an account marked `Session expired` | `Settings > Social Accounts`, then select the amber refresh/reconnect icon on that account. |
| Refresh account name, avatar, or follower count | `Settings > Social Accounts`, `Refresh metadata`. |
| Caption instructions / guidance for AI captions | `Settings > Model Config`. |
| Vast.ai key or API key | `Settings > API Keys`. |
| Vast.ai balance | `Settings > API Keys`. |
| GPU rental disk space, max price, or reliability filters | `Settings > GPU Config`. |
| GPU family for a rental | Left sidebar > `Generation assets` > `Create instance`, then choose a GPU profile. |
| Default model quality, negative prompt, guidance, or prefetch | `Settings > Model Config`. |
| Local runtime download folder | `Settings > Model Config`; stop the local runtime before changing it. |
| Default speech pace, SFX volume, SFX cues, or default narrator voices | `Settings > Audio Config`. |
| Default voice timing, transition duration, or captions | `Settings > Video Config`. |

## 25. Support Assistant (Ask AI)

The Support Assistant is an in-app help chat that answers questions about using Aificient Studio. Its answers are based on this user guide.

### Opening and Closing

- Open it with the `Ask AI` button in the top-right window-actions area, next to the window controls.
- The chat is closed by default.
- Close it with the close button in the chat header, by pressing `Esc`, or by clicking `Ask AI` again.
- Reopening during the same session keeps your existing conversation. Closing the app clears it.

### Asking a Question

1. Type your question in the message box.
2. Press `Enter` to send, or `Shift+Enter` to add a new line.
3. Wait a moment while the assistant prepares an answer. Answers usually take a few seconds.
4. Read the answer, then ask follow-up questions if needed.

Notes:

- A message can be up to 4000 characters. A counter appears as you get close to the limit.
- The send button is disabled while an answer is being generated.
- When the chat is empty, suggested questions are shown. Click one to ask it right away.

### What It Can Help With

- How features work, such as creating projects, characters, scenes, and videos.
- Where to find settings and controls.
- Steps for common workflows.
- Understanding render settings, GPU options, and asset editing.

The assistant explains how to use the app. It does not change your project, start generation, or perform actions for you.

### If the Assistant Cannot Answer

- If a request fails, the chat shows an inline message with a `Try again` option, and your question is kept so you can resend it.
- If help chat is temporarily unavailable, wait a little while and try again.
- If your session has expired, sign in again and reopen the chat.

## 26. Troubleshooting

### I cannot sign in

Try:

- Check your internet connection.
- Try a different sign-in method.
- If using email, request a new code.
- If the app says your version cannot sign in, update or reinstall the app.

### No GPU is available

Check:

- Local runtime is installed and ready.
- Your local GPU meets the requirement shown by the app.
- Vast.ai key is configured if using rented GPUs.
- A rented instance is running and ready.
- GPU search filters are not too strict.

You may also be able to select `Aificient Cloud` on the initial render-settings screen. For an existing project whose images and audio are ready, look under `Resume Generation`. Both paths require an active plan, enough credits, and eligible scene inputs.

### Aificient Cloud is unavailable

Check:

- On an initial project, check whether `Aificient Cloud` appears in the render-settings `Runtime` list.
- On an existing project, confirm it has missing scene videos and its scene images and audio are ready, then check `Resume Generation`.
- Your subscription is active and has enough credits for the displayed estimate.
- The submission has no more than 32 missing scenes.
- Each scene's audio plus voice delays is no longer than 13 seconds.
- `Settings > Storage` is not over its allowance.

If a queued or running cloud render fails, open `Generation assets > Aificient Cloud` for its status. Failed and cancelled cloud jobs refund their reserved credits.

### Storage limit reached

Open `Settings > Storage` to see usage, the plan limit, and available space. Remove unneeded project data or view the available plans for more storage. Generation actions that would add assets can remain blocked until the account is under its allowance or the plan is upgraded.

### Local runtime will not install

Check:

- Your system is supported.
- Your GPU has enough VRAM.
- You have enough free disk space.
- Open runtime details and review the visible error/logs.

### Rented GPU offers do not appear

Try:

- Check the Vast.ai key.
- Check account balance.
- Increase max price.
- Lower minimum reliability.
- Pick a different GPU family.
- Reduce disk requirement.

### Generation is incomplete

Try:

- Check the generation error summary box in the top-right of the canvas for the specific failures and their reasons.
- Open the Schema tab and find the scene with an error.
- Open the Assets tab and check what is missing.
- Open the runtime detail view and check logs.
- Use `Resume Generation`.

### Editing is disabled

Editing is blocked while generation is active. Stop generation or wait for it to finish, then edit.

### Rename project fails

Project rename is supported from the project list context menu. If it fails, check that the runtime or cloud API that owns the project is reachable, then try again.

### Publishing to social accounts

For the full walkthrough of the Publish dialog (compose, review, scheduling, and live upload progress), see "Publishing the Final Video." This entry covers the common problems.

- **The `Publish` button is greyed out.** It only activates once the project has a final video. Finish video generation first.
- **No accounts to post to.** Connect one in `Settings > Social Accounts` (TikTok is the only platform you can connect today). The dialog also links you there, and you can reach it any time via the **Manage** link.
- **An account shows "Session expired".** Open `Settings > Social Accounts`, select the amber refresh/reconnect icon on that account, and sign in again. `Refresh metadata` can re-check the account, but an expired login still requires reconnection.
- **The upload stopped with an error.** TikTok changes its site often, so a step may occasionally fail to complete automatically. Your caption, sound, and cover are kept — choose **Back to editor** and try again. If it keeps failing, confirm the account still shows `Connected`.
- **I closed the Publish window mid-upload.** That's fine — the post keeps running and the progress is saved app-wide. Reopen `Publish` to see it resume until it finishes.
- **I want to stop a post.** Use **Cancel** on the upload progress screen (it stops the background hand-off), or cancel a queued/scheduled post from the **History** view.
- **Scheduling won't accept my time.** Scheduled posts must be at least ~20 minutes in the future; pick a later time.

Publishing runs entirely on your own machine through a private background browser session; nothing about your accounts or posts is sent to an Aificient server.

## 27. Recommended Workflows

### Fast Preview Workflow

Use this when you want to inspect assets before video rendering.

1. Create a concept.
2. Choose `Generate images and audio only`.
3. Review images, narration, and SFX.
4. Rewrite weak scenes or characters.
5. Resume generation later with a ready GPU.

### Full Video Workflow

Use this when you want a final video immediately.

1. Create or select a concept.
2. Choose aspect ratio and resolution.
3. Select one or more ready GPUs (pick several to split the render and finish faster), or choose Aificient Cloud by itself when available.
4. Choose `Lite` for speed/lower VRAM or `Pro` for best quality.
5. Start generation.
6. Monitor the canvas.
7. Download the final video from Output.

### Scene Fix Workflow

Use this when only one scene needs changes.

1. Select the scene.
2. Click the text, image, audio, or video node you want to change.
3. Rewrite or delete the asset.
4. Resume generation.
5. Review the updated scene and final output.

### Character Reuse Workflow

Use this when you want consistent characters across projects.

1. Create a character in Character mode.
2. Save it to the library.
3. Pin it when creating a new concept.
4. Generate the project.
5. Review scenes where the character appears.

## 28. Glossary

### Asset

A generated file such as an image, audio clip, scene video, or final video.

### Runtime

A local or rented GPU environment used for video rendering.

### Render Queue

The per-GPU line of pending work. Each scene video is a job that waits its turn on the GPU it was assigned to, so multiple projects can share a GPU and a single project's videos can be split across several GPUs. The final stitch is not a GPU job — it runs locally in the app.

### Aificient Cloud

The subscription-backed render service available on initial render settings and from `Resume Generation` for eligible scene videos. It uses credits and has its own queue, separate from local and rented GPU queues.

### Scene Image

The still image used as the visual basis for a scene.

### Narration

The spoken audio generated from the scene script.

### SFX

Sound effects generated or assigned to a scene.

### Raw Clip

A generated scene video before final stitching.

### Stitch

The process of combining scene clips into the final video. It runs locally in the desktop app once every scene clip is ready. Only one stitch runs at a time; additional stitches wait in a local queue.

### Final Output

The completed video shown in the Output node.

### Guidance (CFG)

Classifier-Free Guidance. A setting that controls how strictly the AI follows your prompt. Video guidance (Video CFG) applies to visual generation, and Audio guidance (Audio CFG) applies to sound generation. Higher values mean stricter adherence, while lower values allow more creative freedom.

### Support Assistant

The in-app help chat, opened with the `Ask AI` button, that answers questions about using the app based on this guide.
