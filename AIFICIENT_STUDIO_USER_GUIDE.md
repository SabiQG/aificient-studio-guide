# Aificient Studio User Guide

Last reviewed: September 18, 2026 (app version 1.6.0).

This guide explains how to use Aificient Studio from the application interface. It focuses on visible screens, menus, controls, generation workflows, editing tools, GPU management, settings, and common troubleshooting.

## 1. What Aificient Studio Does

Aificient Studio helps you create AI-generated video from a written idea. You can:

- Brainstorm video ideas.
- Turn an idea into a structured story script.
- Create reusable characters, and add new ones to a story at any point.
- Build a project **asset base** — products, wardrobe, locations, props — that the script weaves into scenes and that characters can wear, so a real brand, outfit, or place stays consistent across the whole video.
- Generate scene images, narration, sound effects, video clips, and a final stitched video.
- Animate a poster — one you already have, or one the app designs for you.
- Review and edit individual scenes, recast them, and change which assets they show.
- Regenerate only the parts that need changes.
- Render video with a local GPU runtime, rented GPU instances, or Aificient Cloud when that option is available.
- Claim free daily credits on a plan or trial, and try the app on a free trial before subscribing.

### Two Kinds of Project

The app makes two kinds of project, and you choose which one you are making when you start the creation chat:

- **History** — the original multi-scene flow. A concept becomes a script, characters, scene images, narration, sound effects, scene clips, and a final stitched video. Everything in this guide applies to it unless a section says otherwise.
- **Poster** — a single poster brought to life as a short animated clip (5–15 seconds) with model-generated sound. There are no scenes, no narration, no captions, and no stitching. See "Poster Projects".

Both kinds appear in the same project list, grouped by type, and both can render on your own GPU or on Aificient Cloud.

Most History projects follow this path:

1. Create or select a concept, optionally attaching the products, wardrobe, or locations the video must feature.
2. Review the generated scenes, characters, and planned assets.
3. Choose render settings.
4. Generate assets and video.
5. Inspect the result in the canvas and scene sidebar.
6. Edit or regenerate parts if needed — rewrite text, recast a scene, add a character, dress a character or a scene with assets.
7. Download the final video.

### Desktop, Web, and Phone

The same app runs as a desktop application (Windows) and in the browser. Everything in this guide applies to both unless a note says otherwise; the differences that matter are:

- **Web** has no local or rented GPUs: scene videos render on Aificient Cloud, GPU rentals are offered from the desktop app, and the `Publish` dialog is desktop-only.
- **Phone** (a viewport narrower than 768 px) keeps every feature but rearranges it: the left sidebar becomes a drawer behind a menu button at the top-left, most composer pills fold into an `Options` sheet, dropdowns become bottom sheets you can swipe away, and the right project sidebar is reached through a floating `Details` pill. Tablets and larger screens behave like the desktop.

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

### Introduction Tour

The first time a new account reaches the home screen, a short guided tour walks through the workspace. It starts on its own when all of these are true: you are signed in, your plan and credits have loaded, no project is open, and the account is less than 14 days old. It dims the screen, spotlights the real control for each step, and shows a card with a `Step N of 7` counter and a progress bar.

The seven steps, in order:

1. `Welcome to Aificient Studio` — a centered welcome card; its button reads `Show me around`.
2. `Three ways to create` — spotlights the `Story` / `Poster` / `Character` picker above the composer.
3. `Start with a sentence` — spotlights the prompt box.
4. `Shape it before you render` — spotlights the row of pills under the prompt (style, duration, language, pinned characters, and the `Brainstorm` switch). On a phone the text points you to the `Options` sheet instead.
5. `From script to video` — spotlights the send button and explains the stages (script, images, narration, scene videos, final cut) and the render choice (your GPU or Aificient Cloud; `Lite` fast and affordable, `Pro` for maximum quality).
6. `Everything is saved` — spotlights the sidebar navigation (projects, character library, render queue). On a phone it spotlights the menu button that opens the sidebar drawer.
7. A closing card that depends on your account:
   - **Welcome credits available** — `You have N free credits`, with `Start creating` and `Compare plans`.
   - **Free trial on offer** — `Try <Plan> free for N days`, with a `Start free trial` button (marked with a flag icon) that opens the trial checkout directly, and `See all plans`.
   - **No plan, no credits, no trial** — `Choose a plan to start creating`, with `See plans` and `Not now`.
   - **Subscribed** — `You're all set`, showing the plan's credits for the period, with `Start creating`.
   - **Billing unavailable** — `You're ready`, pointing you to `Settings > Usage` for plan and credits.

Navigation: `Next` (or `Show me around` on the first step), `Back` from step 2 onward, `Skip tour` at the bottom-left, and the close button at the top-right. Keyboard: `→` next, `←` back, `Esc` closes. `Enter` also advances, because the primary button has focus. `Skip tour` is not always an exit: if the account has welcome credits or a trial on offer, it jumps to the closing card so you still see that information. The spotlighted control cannot be clicked while the tour is open.

The tour is remembered **per account, per device or browser** — the same new account on a second computer or in another browser sees it again while it is still within its first 14 days. Replay it at any time from `Settings > General > Introduction tour > Replay`; replay ignores the account-age rule, closes Settings, and returns you to the home screen.

## 3. Main Workspace

After signing in, the left sidebar stays visible while the main area changes with what you are doing:

- Left sidebar: primary navigation, recent projects, project search, generation assets, and the user/settings area.
- Home/new-project screen: appears in the main area when no project is open. It contains the Story, Poster, and Character creation chats; brainstorming is a `Brainstorm` switch inside Story.
- Center canvas: appears when a project is open and shows its visual flow and generated assets.
- Right project sidebar: appears with an open project and contains the project outline, asset browser, project-specific settings, and resume actions. Its tabs and outline follow the project type — `Schema` / `Assets` / `Settings` for a History project, `Plan` / `Assets` / `Settings` for a poster.

The top-right window controls let you minimize, maximize/restore, or close the app (desktop only). The same top-right area also has an `Ask AI` button that opens the Support Assistant, an in-app help chat (see "Support Assistant (Ask AI)"). On a phone `Ask AI` is an icon-only pill, and a menu button at the top-left opens the sidebar drawer.

If no project is selected, the main area shows the home/new-project screen instead of an empty canvas. The left sidebar remains available so you can open an existing project, search, manage characters, or inspect generation assets without closing the creation screen.

## 4. Left Sidebar

### Primary Navigation

The top of the sidebar contains:

- `New project`: leaves the currently open project, shows the home/new-project screen in the main area, and starts a fresh creation chat when needed.
- `Character list`: opens the reusable-character library over the current screen.
- `Generation assets` (desktop): opens a flyout beside the sidebar with Aificient Cloud jobs, the local GPU, rented GPU instances, and the create-instance action. On the **web** this row is `Aificient Cloud` instead: there are no GPUs to manage, so it opens the cloud render queue directly and shows a rendering / queued / history count badge; the flyout's footer on the web offers `Download desktop app` for GPU rentals.

The magnifying-glass button in the sidebar header opens project search. With an empty search it lists recent projects; type to filter by name. Results are grouped by project type, and filter chips (`All`, `History`, `Posters`) let you narrow the search to one type — those chips exist only inside the search dialog and never filter the sidebar list. You can click a result or use the up/down arrow keys and `Enter` (the footer shows the key hints). Press `Esc` or click outside the dialog to close it.

### Promo Slot, Profile Row, and Sign Out

Just above the profile row the sidebar has one slot that shows, in this priority:

- `Daily credits ready` — the daily-credit claim card, when today's free credits are still unclaimed (see "Daily Credits").
- `Try <Plan> free` — the free-trial card, when the account has no subscription and a trial is on offer (see "Free Trial").
- `Download the desktop app` / `For the full experience` — on the web only, when neither of the above applies.

The bottom row shows your avatar initial, your name, and your plan line (for example `Pro · Free trial`, or `Gift Trial` while you are on welcome credits). **Clicking anywhere on that row opens Settings.** The separate `Sign out` button sits beside it.

### Recent Projects

The `Recent projects` list shows projects stored in your workspace, grouped by type under a `History` and a `Posters` heading. Click a row to leave the home screen and open that project's canvas.

Each group:

- Collapses and expands from its heading.
- Shows the 25 most recent projects first, with `Show more` to reveal the next 25.
- Is hidden entirely when it has no projects, so a workspace with no posters shows no `Posters` heading.

A project row can show:

- Active selection.
- Running/generation indicator.
- Final video completed indicator.

When you open a project, a progress overlay can move through `Loading project`, `Checking for active renders`, `Building canvas`, and `Preparing scenes` before the canvas becomes ready. Media previews are loaded in a controlled queue during this process so large projects do not try to decode every image and video at once.

### Project Menu

Right-click a project, or click the `…` (`Project options`) control on its row, to open its menu. The `…` control appears on hover on the desktop and is always visible on touch screens.

Available actions:

- `Rename`: opens a rename dialog for the selected project. Enter a new project name and select `Rename`, or press `Enter`, to save it.
- `Delete`: removes the project.

There is no duplicate action. Deleting a project is permanent from the app's point of view, so use it carefully.

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

The Aificient Cloud option shows the project's `Lite` or `Pro` tier, resolution, and estimated credit cost before submission. It requires an active subscription, enough credits, and each scene's image; scenes whose script has spoken text also need their narration generated first, because the narration decides the clip's length. A submission can contain up to 32 missing scenes, and a scene's narration can be at most 13 seconds long. If your credits do not cover the whole submission, the app sends the scenes one at a time, in order, until the next one is refused for credits; the scenes it could pay for render, and the rest are listed in the generation report so you can render them from the scene panel once you have more credits.

How a cloud clip is made: the video model animates the scene image and composes the clip's own soundtrack — quiet ambience and sound effects implied by the visible action only, never speech or music. Your narration is **not** baked into the clip; it is mixed over it later, in the preview and in the final stitch. Each clip's length is derived automatically from its narration (voice delay + narration + a short tail, whole seconds between 4 and 15); a scene with no spoken text renders as a 5-second clip. Renders made on gift credits carry a small visible Aificient watermark; paid renders do not.

Aificient Cloud is selected by itself; it cannot be combined with local or rented GPUs in the same submission. Once submitted, each scene appears as a separate cloud job. The app refreshes completed clips into the project automatically.

Poster projects can also render on Aificient Cloud. A poster is a single clip, so the scene-count and scene-length limits above do not apply to it; it submits one job that carries the project's saved mode, resolution, and duration, and the delivered clip already includes its generated audio.

When cloud jobs exist, open `Generation assets > Aificient Cloud` to view the current session's queue and history. The window shows queued, running, completed, failed, and cancelled jobs with progress and status messages. You can remove an individual queued job or use `Cancel queued` for all queued jobs in a project. Reserved credits are refunded when a cloud job fails or is cancelled.

While cloud clips are queued or rendering, the center canvas keeps showing the project's overall generation progress and the bottom of the right scene sidebar shows the Aificient Cloud queue/rendering status. Cancel queued cloud clips from `Generation assets > Aificient Cloud`; the canvas progress bar does not include a cloud-cancel button.

For account-wide cloud render history, including settled prices, use `Settings > Usage > Load latest generation jobs`.

New projects render at `720p` by default: it is much cheaper than `1080p` with very similar quality. `1080p` stays available as an explicit choice and costs more per clip.

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

- `Story`: write one video story from a clear brief and refine it in chat. Produces a History project. Its composer has a `Brainstorm` switch for exploring five directions before the story is written (see "Brainstorm" under "Story Mode").
- `Poster`: animate a poster you already have, or design one from zero and animate it. Produces a poster project.
- `Character`: generate a reusable character (image + voice) for your library.

Each mode has its own hero text, its own composer controls, and its own accent colour, so it is always clear which one is active. Story turns amber while `Brainstorm` is on and sky blue while it is off.

The top-right `History` control (`Chat history`) opens your previous creation chats — this is chat history, not the project list, which lives in the left sidebar. The dropdown is headed `Recent chats` with a count and a refresh button, and has filter chips `All` / `Story` / `Poster` / `Character`; it opens pre-filtered to the composer's current mode, and the `Story` filter also lists brainstorm chats, which keep their own icon. Each row shows the chat's icon, title, a preview, and a relative time; hover a row for `Delete chat`. Empty states read `No saved chats yet` or `No chats in this mode` (switch the filter to `All`). On a phone the control is icon-only and the list opens as a bottom sheet. The active conversation title appears in the top bar after the conversation has started.

### Story Mode

Use Story mode when you already have a video idea. (Earlier versions called this mode `Concept` and had a separate `Brainstorm` mode; brainstorming is now a switch inside Story.)

Typical workflow:

1. Enter your idea.
2. Choose style, duration, language, and optional characters.
3. Optionally attach the products, wardrobe, or locations the video must feature (see "Attaching Assets to a Story").
4. Send the prompt.
5. Review the generated story script.
6. Ask for corrections, or edit the script directly with `Edit` (see "Reviewing and Editing the Generated Concept").
7. Continue to render settings.

The generated story can include:

- Title.
- Artistic style.
- Narrator.
- Characters.
- Assets — the reference images you attached, plus any the script planned on its own.
- Scene list.
- Scene descriptions.
- Scene scripts.
- Sound effect cues.

#### Attaching Assets to a Story

A story can be built around real things: a product you sell, an outfit a character must wear, a location that has to look a certain way, a prop. Attach their images before you send the prompt and the script weaves them into the scenes; later, on the canvas, they form the project's **asset base** (see "Project Assets Node (Asset Base)").

The Story composer has an `Assets` pill (image-plus icon) with an `n/8` badge — its tooltip reads `Attach products, wardrobe or locations the video must feature. The script weaves them into the scenes.` It opens an `Assets (n/8)` panel with:

- An `Add` button and a dashed drop target: `Drop PNG / JPG anywhere, or click to browse`, with `N more · up to 20MB each` underneath. When the panel is full it reads `No room left — remove one to add another`, and `Uploading…` while a file is in flight.
- A list of the staged files with a thumbnail (click for a full-screen preview), a humanized name (`lata-cocacola_final.jpg` becomes `lata cocacola final`), and a remove `×`.

You can also drag images anywhere onto the home screen: an overlay reads `Attach to the story` with `Products, wardrobe or locations the video must feature · N more fit.` A refused drop shakes and says `Only PNG or JPG images`. There is no clipboard paste.

Rules and messages:

- PNG or JPG only, up to 20 MB each; at most **8 assets per story request** (`At most 8 assets can be attached to one story.`, `Only N more asset(s) fit — the extras were skipped.`).
- Assets attach on the first prompt **and** on corrections — files you stage while refining ride the correction turn and join the plan's catalogue.
- The sent message keeps thumbnails of what you attached; reopening a saved chat rebuilds them from the plan. A file that is no longer in your storage keeps its slot as a placeholder with the tooltip `<name> — no longer in your assets`.

The plan card the assistant replies with has an `Assets` block listing every asset: thumbnail, name, kind tag, a violet `AI planned` tag for ones the script invented on its own, and an amber `generated later` tag for ones that have no image yet (the app renders those at the start of the first generation run). Each scene row in the plan also shows the asset chips it uses next to its character chips, so you can see where a product or outfit lands before rendering anything.

#### Find Inspiration

Below the empty Story composer (with `Brainstorm` off) there is a `Find inspiration` button. It expands a small showcase of four real generated videos — `Countryside promo` and `Samurai at dawn` (Cinematic), `Golden retriever` and `Weird science` (3D Disney). Each card shows a poster still, plays a short muted loop, and names its artistic style. Hover a card to see `Use this idea`; click it to drop a matching brief into the composer **and** select the artistic style that clip was rendered with. You can then edit the text before sending it. Click the button again to collapse the showcase. With `Brainstorm` on, the showcase is replaced by four topic chips you can click to seed a brainstorm.

#### Brainstorm

Turn on the `Brainstorm` switch in the Story composer when you want help exploring ideas before committing to one. It is a small on/off switch below the prompt, after the language control, not a separate mode: the segmented control stays on `Story`, and the hero reads `Story · Brainstorm` while it is on.

Typical workflow:

1. Turn on `Brainstorm` and enter a topic or rough direction.
2. Review the five generated directions.
3. Ask for more options or corrections.
4. Click `Write story` on the idea you like. The app opens a Story chat seeded with that idea and writes the full script; `Brainstorm` is off in that chat.

Turning the switch off returns you to a Story chat without brainstorming; turning it back on reopens your brainstorm chat.

### Poster Mode

Use Poster mode to turn a still poster into a few seconds of motion. It is described in full under "Poster Projects"; in short:

1. Choose `I have a poster` (import finished artwork) or `From zero` (the app designs the poster first).
2. Attach the poster image, or describe the poster you want plus any reference images and pinned characters.
3. Set the clip duration, and — for `From zero` — the aspect ratio.
4. Send the prompt and review the generated poster plan.
5. Refine the plan in chat if needed, then `Create project`.

### Character Mode

Use Character mode to create reusable characters for your library. Its hero reads `Design a character once. Reuse it across every video.`, and under it the home screen shows `Your cast · N` — up to six of your library characters as tiles, with a `See all` tile that opens the library.

The composer placeholder is `Describe a character: 'A brave young woman detective with a red jacket'...`. Its controls are:

- The visual-style pill.
- A `Female` / `Male` segmented toggle.
- An `Image` pill for a reference image (`Add reference image`); once set it reads `Reference` with a thumbnail and a clear `×`. You can also drop an image anywhere on the screen — the overlay reads `Use as the reference image` / `The character keeps this face, hair and build.` — or paste an image URL in the pill's popover.
- A `Voice` pill that opens the voice picker (see "Voice").

The first message creates the character; every later message in the same chat is a correction that rewrites it, so you refine conversationally ("older", "add a scar", "different jacket"). Each character gets **one reference image** (there is no turnaround or model sheet). When it is done the assistant replies `Created <name>. Available in your library.`, and from then on the character can be pinned in a Story or Poster composer or added to an existing story from the `Add character` modal's `Library` tab.

### Stopping an In-Progress Chat Request

While a brainstorm, story, or character request is being generated, the chat's send button turns into a stop button (a filled square). Click it to cancel the request you just started.

When you cancel:

- The request stops and the chat shows a neutral `Generation canceled.` note instead of an error.
- A late or stale result is not applied after you cancel.
- If the request had already finished on the server, its real result is shown instead of being discarded.
- If the request is no longer available, the chat shows that it is no longer available.

Canceling affects only the single in-progress chat request. It does not remove previous messages, ideas, stories, or characters you already created. This stop button is separate from `Stop Generation` for video and asset rendering (see "Stop Generation").

### Reviewing and Editing the Generated Concept

Yes — you can change the script before you start generating. There are two ways to do it, on two different screens of the creation flow. You can use either one, or both.

**1. Ask the AI in the chat (Story chat, with or without Brainstorm).** While you are still in the chat conversation, keep typing to request changes in natural language — for example, "make scene 2 funnier", "rename the main character to Mia", or "shorten the narration". The assistant rewrites the concept for you and the conversation updates with the result. This is best when you want the AI to rework wording, tone, or whole sections.

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

The creation controls sit in and directly below the chat composer at the bottom of the home screen. Switch modes along the composer's top edge; use the pills and segmented controls below the prompt for style, duration, language, pinned characters, attachments, and Character-mode options.

Only the controls that mean something for the active mode are shown. Poster mode, for example, has no visual-style preset (the look comes from your prompt or the imported artwork) and no language control, but it adds a pipeline toggle, an image-attachment pill, and an aspect-ratio pill. The full pill row, left to right, is: `Options` (phone only), style, `Assets` (Story), the poster pipeline toggle and `Poster image` / `Reference assets` (Poster), aspect ratio (Poster from zero), duration, language, the `Brainstorm` switch (Story), `Characters`, the `Female` / `Male` toggle, `Image`, and `Voice` (Character), then a credit chip and the send button.

Once a plan exists in the conversation, the aspect-ratio, duration, and language controls lock for that chat.

### Credit Chip

When the price of the current mode is known, a small `N cr` chip sits next to the send button. Its tooltip reads `N credits per generation, corrections included. Creating the project is free.` — the chat turns that write or rewrite a script are what is metered, not the `Create project` step.

### Options Sheet (Phone)

On a phone the style, poster pipeline, aspect ratio, language, gender, and duration controls fold into an `Options` pill that opens a bottom sheet with a row per control (`Visual style` opens the style picker). The `Assets`, `Characters`, and `Brainstorm` controls stay in the pill row, and their popovers open as bottom sheets.

### Assets (Story)

The `Assets` pill attaches up to 8 PNG/JPG reference images — products, wardrobe, locations, props — that the script must feature. It is described under "Attaching Assets to a Story".

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

The style affects concept writing and visual generation. The style pill opens a `Visual style` picker of nine tiles, each with a one-line tagline, with `Cinematic` and `3D Disney` first.

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

In Poster mode the duration pill offers whole seconds from 5 to 15 instead (8 by default), because a poster is a single clip rather than a set of scenes.

### Language

The app supports English and Spanish concept generation.

Language affects:

- Script text.
- Narration.
- Scene wording.

### Pinned Characters

In Story mode (with or without `Brainstorm`), you can pin existing library characters. The `Characters` pill (its badge counts the pinned ones) opens a `Pin characters` popover listing your library, with a `Create` shortcut that jumps to Character mode; the empty state reads `No characters yet.` Pinned characters are included in the concept so the generated story uses them. Story mode has no limit on how many you pin.

Poster mode can pin characters too, but only in the `From zero` pipeline — a character has to be placed into a poster while it is being designed, and an imported poster is already finished. There you can pin up to 3 characters, and each one spends a slot from the poster's shared reference budget (see "Reference Images and Characters").

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

The all-characters view (headed `Characters` with a count) lets you:

- Create a new character with `New character` (this closes the library and opens Character mode on the home screen).
- Search characters (`Search characters…`).
- Filter by type.
- Filter by gender.
- Filter by voice.
- Open details.
- Rename characters from their detail view.
- Preview images (`View image` on a card).
- Delete characters (`Delete character` on a card). The confirmation reads `Delete character?` — `This permanently removes the character and its generated reference image from your library. This cannot be undone.`

When Character mode is open on an empty creation chat, the home screen also shows up to six characters from your cast; use `See all` when more are available.

There are three ways to get a character into the library:

- Create it in Character mode on the home screen.
- Save a project character from its canvas card with the `Library` button — it copies the character **including its reference image** into the library under a new id, and the project copy is untouched. The button reads `Saved` for a moment afterwards and is disabled until the character has an image (`Generate the character image first`).
- (Indirectly) a character created in a story stays a project character until you save it this way.

And three ways to use a library character:

- Pin it in the Story or Poster composer before the script is written.
- Add it to an existing story from the `Add character` modal's `Library` tab (see "Add a Character to a Project").
- It arrives in the project as a **global** character.

Characters from the library are treated as global references. On the canvas they show a `global` badge and cannot be edited, deleted, or dressed with project assets from the project; their card offers `Project variant` instead, which gives the project its own editable copy (see "Project Variant of a Library Character").

## 10. Render Settings

Before starting generation, the app shows render settings.

This section describes the History render-settings screen. A poster has its own, shorter version of the same screen — see "Creating a Poster Project".

### Format

Choose:

- Aspect ratio: `Portrait (9:16)` (default) — "TikTok, Reels and Shorts" — or `Landscape (16:9)` — "YouTube and desktop".
- Resolution: `720p` (default) or `1080p`. `720p` is much cheaper to render with very similar quality; `1080p` costs more per clip.

Use `9:16` for vertical/social video. Use `16:9` for widescreen video.

The action button at the bottom reads `Start generation`, `Start images and audio` when `Images and audio only` is on, or `Queue on N GPUs` when several GPUs are selected, with a summary line of the chosen aspect, resolution, tier, and target. If no runtime is ready the screen says so (`No GPU is ready right now. Start your local runtime or spin up a rented instance before generating.` or `Aificient Cloud is unavailable right now. Try again in a moment.`).

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

The default depends on your account: trial accounts (welcome credits, no plan) start on `Lite`, and accounts on a paid plan start on `Pro`. You can switch either way before starting the generation.

Suggested use:

- Use `Lite` for previews, quick feedback, or when your GPU has less than 31 GB of VRAM (the app shows a `Recommended` badge on `Lite` in that case).
- Use `Pro` for finished videos when the selected GPU has enough memory.
- A100 runtimes require `Pro`; the app blocks the `Lite`/FP8 path on an A100 and asks you to switch.

On Aificient Cloud the tier is a quality/price knob: `Lite` renders with fewer refinement steps, `Pro` with more (about a third more compute), and `Pro` is priced accordingly.

### Images and Audio Only

Enable this option when you want to generate:

- Character references.
- Scene images.
- Narration.
- Sound effects.

Video rendering and final stitching are skipped. This is useful for reviewing assets before spending GPU time.

## 11. Center Canvas

The canvas shows the project as a connected visual flow.

Common node groups, left to right:

- Project info.
- Project assets (the asset base card, right after the project card).
- Character references (the cast column, with `Add character` under the last card).
- Script.
- Scenes.
- Scene text/details.
- Images.
- Audio.
- Video clips.
- Stitch.
- Final output.

You can pan, zoom, and use the mini-map to navigate larger projects.

Those node groups are the History flow. A poster project uses the same canvas with its own, much shorter chain — see "The Poster Canvas".

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
- Three step chips (image, audio, video) whose tooltips read `ready`, `generating`, `failed`, `skipped`, or `pending`.
- A `Cast` strip — one chip per character in the scene (narrator chips are marked `· narrator`), ending in an `Add cast` / `Edit cast` button that opens the cast picker (see "Change a Scene's Cast").
- An `Assets` strip — one chip per project asset assigned to the scene, ending in an `Add assets` / `Edit assets` button that opens the asset picker (see "Dress a Scene or a Character with Assets"). This strip appears once the project has an asset base. Assets that have no image yet show as muted chips with the tooltip `<name> · pending generation`.

### Description, Character Reference, and Script Nodes

These nodes show editable scene text.

Click them to open rewrite tools when generation is not active.

### Project Assets Node (Asset Base)

The `Assets` card sits in its own column right after the project card and holds the project's **asset base**: reusable reference images — a branded product, a wardrobe item, a location, a prop — that scenes and characters reference by id. When a scene image or a character image is rendered, the assigned assets are attached to the image model as visual references, so the same bottle, jacket, or storefront appears the same way in every shot. The asset base exists in History (story) projects only.

The header shows the asset count and two buttons:

- `Upload an image` — a file picker for PNG/JPG images (several at a time; they upload one after another). Uploaded assets are ground truth: they are never regenerated.
- `Create from a prompt` (atom icon) — opens `New asset from a prompt` (`The image model renders it in the project's artistic style`), with `Name`, a `Kind` chip row (`Product`, `Wardrobe`, `Location`, `Prop`), and `What it looks like` (`A complete visual brief: shape, colors, materials, branding…`). `Create & generate` creates the entry and renders its image right away.

The empty state reads `Products, wardrobe, locations…` / `Upload an image or create one with AI.`

Each asset is a tile with a thumbnail and its name (hover for the description):

- A dashed tile with an atom glyph is an asset that has no image yet (`pending`) — typically one the script planned. It is rendered at the start of the next generation run, before characters and scenes.
- A small `AI` corner badge marks assets the script planned on its own.
- A spinner covers a tile while that asset is being generated or updated.

Click a tile to open its detail modal, titled with the asset's name and subtitled `Planned by the script` or `Your asset`:

- The image (click, or `View full screen`, to open the viewer) and tags: `AI planned` / `User`, the kind, and `pending` or `uploaded`.
- `Used in` — for example `Scenes 2, 4 · worn by Maya`, or `Nowhere yet — pick it from a scene card, or place it with AI below.`
- `Generate image` / `Regenerate image` — for generated assets only; uploaded assets have no regenerate button.
- `Details` — name, kind, and description (`What the models read about this asset. Editing these regenerates nothing.`); a `Save` button appears once something changed.
- `Place with AI` — describe where the asset belongs (`e.g. "show it wherever the chemist is drinking"`); the model picks the scenes (and the character, for wardrobe) and those scenes regenerate. The result line reads `Now in scenes 2, 3.` or `Not placed in any scene.`, and when something changed the generation run starts automatically.
- `Delete from project` — asks first. If the asset is assigned anywhere, the confirmation spells out what goes with it: the generated image and video of every scene that uses it, and everything featuring any character that wears it (including that character's image); narration and caption timings are kept. An unassigned asset is simply removed. `Keep it` / `Delete asset`.

Notes:

- There is no fixed cap on the asset base itself. The caps are 8 attachments per story request in the composer, 5 assets per scene, and 3 per character. Those two limits are fixed by the service and are not project settings.
- Asset changes are blocked while a task runs (`Cannot update assets while a task is in progress`).
- Finished project assets also appear in the right sidebar's `Assets` tab under `Project asset`.

**Creative uses:** product placement for a brand video (upload the packshot, let the script place it, then keep it in every scene where it matters); a character's signature wardrobe (a jacket or uniform assigned as their outfit so it survives every regeneration); a real location or set (a shop front, a kitchen, a stage) that several scenes share; a prop that must look identical each time it appears. Because uploads are never regenerated, what you upload is exactly what the image model is shown.

### Character Node

Each cast card shows the character's reference image (click it to open the full-screen viewer, subtitled `Character reference`), its name, badges — `narrator`, `global` for a library character, and the type (`person` / `animal` / `object`) — and its description. A card whose reference image is being generated shows an active state; a new character with no image yet shows the card without artwork until its first generation run.

For project characters, under the description there is an `Outfit` strip: one chip per project asset the character wears, ending in an `Add outfit` / `Edit outfit` button (see "Dress a Scene or a Character with Assets"). It appears once the project has an asset base.

The action row (hidden while the project is generating) has three buttons for a project character:

- `Edit` — opens the character editor (see "Edit Character").
- `Library` — saves a copy, image included, to your character library; reads `Saved` briefly afterwards. Disabled until the character has an image (`Generate the character image first`).
- Delete — `Deletes character reference visuals and affected scene videos. Use Resume Generation when you want to rebuild them.`

A **global** (library) character shows a single `Project variant` button instead: `Give this project its own editable copy of the character. The library entry stays as it is.` (see "Project Variant of a Library Character").

Under the last card of the cast column hangs a dashed `Add character` button (`Add a character to the script`); when the script has no characters yet it is a card of its own. It is disabled while a task runs (`Wait for the running task to finish`). See "Add a Character to a Project".

### Image Node

Shows the generated scene image.

Actions can include:

- Preview fullscreen.
- Retry loading.
- `Delete image` — `Deletes the scene image, raw clip, and final video. Use Resume Generation when you want to rebuild them.`

Deleting a scene image means dependent video assets must be regenerated.

### Audio Node

Shows available audio tracks.

Actions can include:

- Play/pause.
- Seek.
- Retry loading.
- `Delete narration` / `Delete audio` — `Deletes narration, generated audio, raw clip, and final video. The scene image is kept. Use Resume Generation when you want to rebuild them.`

Regenerating audio can affect later video stages because video timing depends on audio. For cloud-rendered scenes the rule is forgiving: if the new narration (plus the voice delay and tail) still fits inside the rendered clip, the clip is **kept** — the scene simply plays longer or shorter at the next stitch, with no re-render. Only when the new narration outgrows the clip is the clip deleted, with a warning, so the scene can be re-rendered at the right length. Captions' word timings and the final video are always refreshed after an audio change.

### Video Node

Shows a generated scene video clip.

While a clip is waiting in a local, rented, or Aificient Cloud render queue, the node shows a colored `Queued` badge with a small queue icon instead of its normal status icon. Once rendering starts, it switches to the normal active/progress state.

Actions can include:

- Play/pause.
- Seek.
- Fullscreen preview.
- A narration mute toggle (`Narration on — click to mute` / `Narration off — click to unmute`) so you can hear the clip's own soundtrack alone.
- `Delete video` (raw clips only) — `Deletes scene video clips and final video.`
- `Cancel` on a captioned clip while its caption burn is running.
- Rate the clip with thumbs up or thumbs down. A dislike can include an optional preset reason or custom comment; select the active rating again to clear it.

Each scene has two video boxes when captions are on: `raw clip` and `captioned clip`.

Deleting a scene video means the final video must be regenerated.

For cloud-rendered scenes, pressing play previews the clip and its narration **together**: the voice enters after the configured voice delay, the clip's own soundtrack plays underneath at the project's `SFX volume`, and playback stops where the final video will cut the scene — so what you hear and where it ends is what the stitched video will keep.

### Stitch Node

Shows final video stitching status. The stitch runs locally in the desktop app (no GPU needed) as soon as every scene clip is ready: the app downloads the clips and, for cloud-rendered scenes, their narration tracks; mixes each narration over its clip's own soundtrack (the model's ambience dips under the voice, scaled by the project's `SFX volume`); trims each narrated scene to end a beat after its voice finishes (the rendered clip is an oversized canvas — the narration decides the scene's real length); combines the scenes with the configured transition; writes the provenance watermark; and uploads the final video to your project.

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

For a History project it has three tabs:

- `Schema`.
- `Assets`.
- `Settings`.

A poster project uses the same column with a `Plan` tab in place of `Schema` and a much smaller `Settings` form — see "The Poster Sidebar".

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
- Project assets (each labelled `Project asset`).
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

- Aspect ratio (`Vertical 9:16` / `Widescreen 16:9`).
- Resolution (`720p` / `1080p`).
- Quality (Lite or Pro).
- Guidance values (Video/Audio CFG).
- Speech pace.
- Voice delay and scene tail.
- SFX volume — how loud the video model's own soundtrack (ambience and effects) plays under your narration, in the preview and in the final stitch. Default 20%.
- Transition duration.
- Whether captions are burned into this project's videos (`Burn-in captions`).
- Caption position, font (`Bangers`, `Luckiest Guy`, `Anton`, `Poppins`, `Inter`), size, and colors, with a live `Preview` and a `Reset` that returns the style to your preset.

The sticky footer has a `Discard changes` button and a primary button that reads `No changes to apply`, `Apply changes`, `Applying`, then `Applied`. If settings are changed, apply them before rendering video: while there are unsaved changes the `Resume Generation` menu shows `Generation changes pending to be saved!` and its render action is blocked.

## 15. Resume Generation

`Resume Generation` is the button at the bottom of the right sidebar. It lights up amber when a project has missing or invalidated assets, and is disabled (`Project generation is complete`) when there is nothing left to do.

Use it after:

- Stopping generation.
- Deleting an image, audio, or video.
- Rewriting scene text.
- Editing character visuals, changing a scene's cast, or changing an outfit or a scene's assets.
- Adding a character or an asset — including a new character that is **not in any scene yet**: its reference image counts as missing, so the button stays active even on a project whose final video is already finished, and `Images + Audio only` renders it for preview without touching the video.
- A generation failure.
- Running images/audio first and rendering video later.

Clicking the button opens the `Generate video on` menu:

- A warning `Generation changes pending to be saved!` when the `Settings` tab has unapplied changes; the render action stays blocked until you apply or discard them.
- A runtime list — `Aificient Cloud` (with tier, resolution, and estimated credits) and each ready local or rented GPU (with its queue depth). Tick one or more GPUs to split the missing videos across them, or Aificient Cloud by itself. When nothing is available the list reads `No GPU available — start a runtime to render video.`
- `Add to render queue` (or `Queue on N GPUs`) — renders the missing scene videos on the selected runtime(s). Missing images and audio are generated first automatically.
- `Images + Audio only` / `Skip video rendering` — generates missing images, character references, project assets, and audio without rendering video. Its tooltip reads `Generate missing images, character references, and audio without rendering video`, or `Images, character references, and audio are already ready` when there is nothing of that kind to do.

The app reuses existing completed assets where possible and only regenerates missing or affected parts.

When every raw clip is ready and only caption burns or the final stitch remain, the button acts directly instead of opening the menu (no GPU is needed for that local work), and it is labelled `Stitch Final Video` when only the stitch is left. Its tooltip tells you why it is lit: `All scene clips are ready — stitch the final video`, `N captioned clips are missing — resume local generation`, or `Some generated assets are missing`.

On a phone the button is a floating `Resume` / `Stitch` pill beside the `Details` pill, and the menu opens as a bottom sheet.

On a poster project the same menu offers a single runtime choice plus `Images only` — see "Rendering and Resuming a Poster".

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

This stop action is for video and asset generation. To cancel a brainstorm, story, or character request on the creation home screen, use the stop button that replaces the chat's send button (see "Stopping an In-Progress Chat Request").

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

- For `API task` failures (images, audio, characters), review or rewrite the affected scene or character, then use `Resume Generation`.
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

### Add a Character to a Project

You can add a character to a story at any point after it exists — a rival who appears halfway through, a mascot, a narrator's sidekick. Click `Add character` under the last cast card (or the `Add character` card when the script has no cast yet). The modal, titled `Add character` with the project name, has three tabs:

- **`Manual`** — `Name`, `Gender` (None / Female / Male), `Type` (Person / Animal / Object), a `Humanized` checkbox, and a `Description` (`A stable visual identity the image model can repeat: age, build, face, hair, wardrobe and colors, distinguishing marks`). Below it, `Reference images (optional, up to 3)` — PNG or JPEG photos of the character or of what they wear; `They join the project's assets and the character is drawn from them.` Button: `Add character`.
- **`AI`** — a single `Prompt` (`Who should join the story? e.g. a rival chemist in her fifties: sharp grey suit, silver bob, rimless glasses`) plus the same reference-image strip; the model reads the whole script for context and writes the character. With references attached: `The AI writes the character from these images; the prompt adds what they cannot show.` Button: `Write & add`.
- **`Library`** — `Your library`: pick one of your library characters (ones already in the script are hidden). It arrives as a **global** character with its library image. Empty states: `Every library character is already in this script.` or `Your library is empty. Create characters from the home screen in Character mode.`

There is no voice field here: voice is only editable later, and only for the narrator.

The modal states the rule plainly: `Nothing regenerates now. The new character is in no scene until you cast them from a scene card; their reference image renders on the next generation run.` After saving it confirms `<Name> joined the script` / `Not in any scene yet: cast them from a scene card. Their reference image renders on the next generation run, or right away with Regenerate.`, with a summary card and two buttons: `Close` and `Regenerate images + audio`.

To see the new character before deciding where they go, render their reference image first: use `Regenerate images + audio` in that confirmation, or later `Resume Generation > Images + Audio only` — the sidebar button stays active for an uncast character with no image even when the project's final video is already done, and the card shows the generation progress. Then cast them from the `Cast` strip of the scenes they belong in; each recast scene regenerates its image and video on the next run.

Reference photos you attach are uploaded to the project asset base first and become the character's outfit references.

### Change a Scene's Cast

Every scene card has a `Cast` strip. `Add cast` / `Edit cast` opens the `Scene N cast` picker — a checklist of `Characters in this project (N in scene)` with avatar, name, and `narrator` / `library character` labels. There is no per-scene limit. As soon as the selection changes the picker warns `This scene regenerates with the new cast` — `Saving deletes this scene's image and videos so the next generation draws exactly these characters. Narration and caption timings are kept.` — and `Save cast` applies it. The scene's `Character Reference` text is kept in step with the new cast. Empty catalogue: `This script has no characters yet — add one from the board first.`

### Dress a Scene or a Character with Assets

Both scene cards and character cards can carry project assets (see "Project Assets Node (Asset Base)"), through the same picker: a checklist headed `Assets in this project (n/max selected)` with thumbnails, each asset's description or kind, or `Pending generation` for one with no image yet. Entries are disabled once the cap is reached. Buttons: `Cancel` / `Save assets`. If the project has no asset base: `This project has no assets yet — add one from the Assets card first.`

- **Scene assets** — `Add assets` / `Edit assets` on the scene card opens `Scene N assets`. Up to 5 are attached to the image model when the scene image is rendered. Warning: `This scene regenerates with the new set` — `Saving deletes this scene's image and videos so the next generation uses the new references. Narration and caption timings are kept.`
- **Character outfit** — `Add outfit` / `Edit outfit` on the character card opens `<Name> · wardrobe` (`Assets applied to this character's appearance`). Up to 3 are attached when the character's reference image is rendered, and travel with the character into every scene they appear in. Warning: `The character regenerates with the new wardrobe` — `Saving deletes this character's image and the media of every scene they appear in, so the next generation applies the new wardrobe everywhere. Narration is kept.` Library (global) characters cannot wear project assets — make a `Project variant` first.

After saving, use `Resume Generation` (or `Images + Audio only`) to rebuild the affected images.

Alternatively, open an asset's detail modal from the `Assets` card and use `Place with AI` to let the model decide which scenes (and which character, for wardrobe) should carry it.

### Project Variant of a Library Character

A library character on the canvas is **global**: it cannot be edited, deleted, or dressed inside the project, so that every project using it stays consistent. Its card offers `Project variant` instead. The modal explains: `This project gets its own copy of <name>: same look, same scenes, but editable here and able to wear project assets.` and `Your library character stays untouched, and so does every other project using it. Nothing regenerates now — the scenes keep their images until you change something about the variant.` `Create variant` swaps the library reference for a project character that starts from the library image; if the library entry had no image, the next run renders one.

### Edit Character

For editable project characters, `Edit` on the card opens the `Edit character` editor with two tabs, `Manual` and `AI`:

- **`Manual`** — the portrait beside `Name`, `Gender`, `Type`, and `Humanized` (`A non-person that behaves like a person`). A `Look` section (`What the image model draws: a stable visual identity, plus the project assets the character wears.`) holds the `Description` and the `Outfit` chips; changing the outfit is saved on its own and regenerates the character and the scenes they appear in. A `Voice` section appears **only if this character is the narrator** (`This character narrates. A new voice re-records the narration and re-renders the videos; artwork stays.`), using the voice picker with previews described under "Voice". Only the fields you actually change are applied, so a voice-only change leaves the rest untouched.
- **`AI`** — an `Instruction` (`The model rewrites this character from your note, keeping the identity details image generation relies on.`, e.g. `make her older, silver hair, add a leather jacket`) and a `Keep the current look as reference` toggle: `The current image is saved as a project asset and shown to the image model, so the rewritten character stays recognizable.` That reference uses one outfit slot; when the outfit is full the toggle explains `Outfit is full (n/max): remove an asset to keep the current look as a reference.`, and with no image yet `No reference image yet: the new look is drawn from the description alone.`

What gets invalidated depends on what you change, and the editor's warning box says so before you confirm:

- A visual change (name, gender, type, humanized, description, outfit) or an AI rewrite — `Visuals will be regenerated`: the character's reference image and the visuals of every scene it appears in are deleted; narration and generated audio are kept.
- A voice-only change — `Audio and video will be regenerated`: narration audio and rendered video for the affected scenes are deleted; scene images and the reference image are kept.

Saving is a two-step commit: `Rewrite character`, then `Confirm rewrite` on the `Confirm the rewrite` panel (`The affected visuals are deleted now and rebuilt on the next generation run.`). On success the editor reads `Character updated` and offers `Regenerate images + audio`.

Manual character editing is best for exact name/type/description/voice changes. AI character editing is best when you want to preserve the character idea but change the style, personality, appearance, or level of detail. Library (global) characters cannot be edited from the canvas (`Global characters cannot be edited from the jamboard`) — change them in the character library, or make a `Project variant`.

### Delete Assets

Some nodes let you delete specific assets.

After deletion, use `Resume Generation` to regenerate what is missing.

Typical effects:

- Delete image: the scene image is removed, and video for that scene may need to be regenerated.
- Regenerate audio: the narration is recreated; a cloud-rendered clip survives if the new narration still fits inside it, and is deleted with a warning when it does not.
- Delete video: the scene clip is removed, and the final video must be regenerated.
- Delete character: the character's reference image and the videos of the scenes it appears in are removed.
- Delete a project asset: the asset is removed together with the generated image and video of every scene that uses it and everything featuring any character that wears it (including that character's image); narration and caption timings are kept. An unassigned asset is simply removed.
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
- Voice delays and scene tail.
- SFX volume (the level of the video model's own soundtrack under the narration; default 20%).
- Transition duration.
- Burn-in captions on or off.
- Caption position, font, size, and colors.

**Guidance (CFG)** controls how strictly the AI follows your prompts. **Video guidance (Video CFG)** determines how closely the video matches the scene description. **Audio guidance (Audio CFG)** determines how closely the generated audio matches the sound description. Higher values force stricter adherence to the prompt, while lower values allow more creative freedom.

Project settings can override global defaults for that project.

## 20. Poster Projects

A poster project turns a single poster into a short animated clip. It is a different kind of project from the multi-scene History flow: there are no scenes, no narration track, no captions, and no final stitch. The animation the app produces **is** the final video, and its soundtrack is generated by the video model itself.

Everything else you already know still applies: posters live in the same project list, render on the same GPUs or on Aificient Cloud, use the same credits, and use the same canvas and right-sidebar layout.

### The Two Poster Pipelines

Poster mode has a segmented toggle in the composer:

- **`I have a poster`** — you attach finished artwork and describe how it should move. The app derives an opening frame from your poster and animates towards it. The aspect ratio comes from the image itself, and reference images and characters are not used.
- **`From zero`** — you describe the poster you want. The app designs the poster first, then derives the opening frame from it, then animates it. Here you can attach reference images, pin library characters, and choose the aspect ratio.

Once a plan exists in the conversation, the toggle locks for that chat: switching pipelines means starting a new poster chat.

### Writing the Poster Prompt

The composer controls for Poster mode are:

- **Pipeline toggle** — `I have a poster` / `From zero`.
- **`Poster image`** (`I have a poster` only) — pick the JPG or PNG to animate. The file is uploaded to your assets folder before the prompt is sent.
- **`Reference assets`** (`From zero` only) — attach JPG/PNG images that guide the design. The pill shows a `used/5` badge.
- **`Characters`** (`From zero` only) — pin up to 3 library characters to be placed into the poster.
- **Aspect ratio** (`From zero` only) — `9:16`, `3:4` (default), `1:1`, `4:3`, or `16:9`.
- **Duration** — whole seconds from 5 to 15, 8 by default.

The prompt itself is required for `From zero`; for `I have a poster` the image is what is required, and the text describes the motion.

#### Reference Images and Characters

Reference images and pinned characters share **one budget of 5**. Each character counts exactly as much as an image, and characters have their own extra limit of 3:

- 3 characters leave room for 2 reference images.
- 5 reference images leave room for no characters.

The composer shows one combined counter on the `Reference assets` pill and disables whichever side has run out of room. If a plan created before this shared limit holds more than 5 references, the app blocks `Create project` and tells you so — send any correction in chat and the plan comes back trimmed and ready to create.

### The Poster Plan

The reply in the chat is a **poster plan** card showing:

- Its title and a badge for the pipeline used.
- The imported poster, or thumbnails of the reference images and pinned characters.
- Three collapsible prompts — `Poster prompt` (only when designing from zero), `First frame prompt`, and `Video prompt`.
- Duration and aspect-ratio chips.
- The `Create project` action.

Keep typing in the chat to refine it — "snappier reveal", "different typography", "add light jazz music" — and the plan is rewritten. You can attach new images with a correction; they are merged into the plan, and if that pushes past the 5-reference budget the oldest ones are dropped. The plan that comes back is always the accurate record of what survived, so read the card rather than what you attached. The composer clears its attachments after every turn for exactly this reason.

Writing a poster plan is a metered charge: reference images are read by the prompt-writing model, so more of them makes the plan cost more (and take longer to produce).

### Creating a Poster Project

`Create project` opens the poster render-settings screen, with the plan preview attached beside it. It contains:

- **Aspect ratio** — read-only. It is stamped from the poster itself.
- **Resolution** — `720p` (default, much cheaper) or `1080p`.
- **Mode** — `Lite` (faster, smaller GPUs) or `Pro` (best quality). Trial accounts start on `Lite`; accounts on a paid plan start on `Pro`.
- **Video duration** — the length of the animation.
- **Images only** — stop after the poster images and skip the animation. You can render it later from the project.
- **Runtime** — where the animation renders. A poster is a single clip, so this is a **single choice**: one GPU (local or rented) *or* Aificient Cloud. The Aificient Cloud row shows the tier, resolution, duration, and estimated credit cost of the current settings.

Creating the project also **starts its generation immediately** — the button reads `Start generation`, or `Start images` when `Images only` is on. If no runtime is available you can still create the project with images only and render the animation later.

### The Poster Canvas

The canvas shows the poster's own chain, left to right:

```
project → assets → poster prompt → poster image → first frame prompt → first frame → video prompt → final video
```

Notes on the layout:

- The references design the **poster**; the **first frame** is derived from the finished poster alone, not from the references or character faces. The animation then runs between the frame and the poster.
- An imported poster has no `poster prompt` step, so that column is closed up and the artwork sits one step after the assets box.
- The three prompt nodes are clickable and open the rewrite modal (see below).
- The media nodes show the designed poster, the first frame, and the final animation, each with a progress state while it is being generated and a delete button.

Poster previews are shown at their real proportions, so a `3:4` or `9:16` poster is not cropped to fit the node.

### The Poster Sidebar

The right sidebar of a poster project has three tabs: `Plan`, `Assets`, and `Settings`.

**Plan** is the outline. Click any row to centre the canvas on that node:

- `Project` and `Assets` (with a count of references).
- The three prompts — `Poster prompt` (from zero only), `First frame prompt`, `Video prompt`.
- The three generated items — `Poster image`, `First frame`, `Final video` — each showing `Not generated`, `Queued`, `Generating N%`, `Generated`, or `Failed`. For an imported poster, `Poster image` simply reads `Imported`.

**Assets** lists the poster's reference images together with whatever the generation has produced, with download and focus actions.

**Settings** is a poster's whole video configuration, and it is deliberately small:

- `Aspect ratio` — read-only, set by the poster.
- `Resolution` — `720p` (default) / `1080p`.
- `Mode` — `Lite` / `Pro`.
- `Video duration`.

Changes are staged until you select `Apply changes` (or discard them with the circular-arrow button). While there are unsaved changes the footer warns `Unsaved video settings` and the render action is blocked, because a render always uses the **saved** settings. None of the History settings — captions, guidance scales, speech pace, voice delays, transitions — exist for a poster.

The sidebar footer holds the same actions as a History project: `Stop Generation` while a run is active, an `Aificient Cloud` status chip while the clip is in the cloud queue, and otherwise the `Resume Generation` menu.

### Rendering and Resuming a Poster

`Resume Generation` on a poster offers:

- A **single** runtime choice — one GPU (local or rented) or Aificient Cloud, with its estimated credit cost — and `Add to render queue` to render the animation. Missing poster images are regenerated first automatically, so this is the "finish the poster" action.
- `Images only`, which fills in the missing poster and first frame without rendering the animation. Those are cloud tasks and need no GPU.

The action is disabled once everything has been generated.

GPU renders join the same per-GPU queue as History scene videos, so a busy GPU is still a valid choice. Cloud renders appear in `Generation assets > Aificient Cloud` alongside History jobs. Either way the finished clip lands as the project's final video — there is nothing to burn or stitch afterwards, so the project simply completes when the clip is delivered.

If you close the app while a poster render is in progress, reopening the project reattaches to it and the sidebar and canvas pick the progress back up.

### Editing a Poster

Click any of the three prompt nodes on the canvas to rewrite it, either by typing the replacement yourself or by describing the change and letting the AI rewrite it. This is the same modal used for scene text in a History project.

Editing a prompt invalidates everything downstream of it, and the modal spells out exactly what will be deleted **for this project as it stands today**:

- Rewriting the poster prompt deletes the poster image, the first frame, and the animation.
- Rewriting the first-frame prompt deletes the first frame and the animation; the poster is kept.
- Rewriting the video prompt deletes the animation; both images are kept.

If nothing has been generated from that prompt yet, the modal says so and the edit only updates the plan. After a rewrite that removed images, `Regenerate images` in the modal refills them straight away; the animation is rendered from the sidebar's `Resume Generation` menu, where the runtime choice lives.

The delete buttons on the media nodes cascade the same way — deleting the poster also removes the first frame and the animation, deleting the first frame also removes the animation, and deleting the animation leaves both images. Each button's tooltip states what it takes with it.

### What Posters Do Not Have

- **Captions.** There is no narration track to transcribe, so there is no caption step and no captioned-clip column.
- **Stitching.** A poster is one clip; the render is the final video.
- **Publishing.** The `Publish` dialog is available for History projects only.
- **Scene tools.** No scene list, no character node editing inside the project — a poster's characters come from your library at plan time.

### A Note on Poster Reference Images

Poster reference images stay in your **assets folder**; they are not copied into the project. That means the same image can back several posters, and deleting it from your assets breaks every poster that references it. If that happens, the app tells you the reference is no longer in your assets folder — attach it again in a chat correction to continue.

## 21. Global Settings

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

- App version (a `v1.6.0`-style chip on the app card).
- `Updates` — the status line (`You are on the latest version`, `Latest N available`, or `Manual update check`) and a `Check` button that becomes `Update to latest` when a newer version exists.
- `Introduction tour` / `A short walk through the workspace.` — a `Replay` button that closes Settings and restarts the guided tour on the home screen (see "Introduction Tour").
- Current subscription and an upgrade action; a violet `Free trial · bills <date>` badge while you are on a free trial.
- User account information (name and email).
- Help/contact link.

### Usage

This section shows the credits included with your plan, credits used and remaining, renewal or cancellation information, and usage over time. Depending on the subscription source, it can also provide plan-management, upgrade, or pending-change actions. While you are on welcome credits it shows a `Gift Trial` plan card with `Complimentary access`, its expiry, and `Client since`. Free daily credits and the free trial are described under "Credits, Plans, Free Trial, and Daily Credits".

At the bottom, click **Load latest generation jobs** to open your account-wide Aificient Cloud video render history. This history includes jobs from all projects and lists the newest jobs first.

Each job can show:

- Content and scene name.
- Status: `Queued`, `Running`, `Completed`, `Failed`, `Cancelled`, or `Unknown`.
- Quality tier and resolution.
- Requested and finished times.
- Progress percentage plus the current stage or message while the job is queued or running.
- The settled credit price for a completed job, shown with the credit icon (for example, `3.4 credits`).

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
- Social media caption instructions.
- Local runtime download folder.
- Video guidance (Video CFG).
- Audio guidance (Audio CFG).
- Prefetch count.

**Social Media Caption Instructions** is optional free-form guidance the AI follows when it drafts a publish caption (with the **Generate** button in the Publish dialog). Use it to set a tone, style, call-to-action, emoji use, or other constraints — for example, "casual and punchy, end with a question, no more than two emojis." It applies to every project, and you can leave it blank.

The runtime download folder can only be changed while the local runtime is stopped and is not downloading, setting up, or booting. Use `Default` to return to the app's standard data folder.

### Audio Config

Controls:

- Speech pace.
- SFX volume — the default level of the video model's own soundtrack under the narration (a 0–100% slider; default 20%). New projects start from this value; each project can override it in its own `Settings` tab.
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
transcribes the scene's **narration audio** to get word-by-word timings aligned
to where the voice sits in the final video (a small paid step, billed like
other generations), then your own machine burns those captions into a copy of
the clip. The app also self-checks stored timings before every burn — timings
that do not match the narration, or that predate a timing change, are corrected
or re-transcribed automatically. That local render shares the same queue as the
final stitch, so it never competes with video generation on the GPU.

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
  captioned cuts, the saved word timings, and the final video. The plain clips
  are kept. Select `Stitch Final Video` to rebuild the final video from those
  plain clips. Because the word timings are deleted, turning captions back on
  later re-transcribes each scene (the same small per-scene charge) — which
  also makes an off-and-on round trip a clean reset if captions ever look
  wrong.

In some restored or older projects, the Stitch node can instead show a
`Re-stitch with captions` or `Re-stitch without captions` shortcut when the
existing final video's recorded caption mode does not match the current
setting.

> Note: re-rendering a scene's video replaces its plain cut, and its captioned
> cut is removed at the same time — the old captions were burned onto the take
> you just replaced. The scene's captioned box goes back to empty, ready to be
> generated again through `Resume Generation`.

## 22. Credits, Plans, Free Trial, and Daily Credits

Generation and cloud rendering run on **credits**. Your balance, plan, and renewal date live in `Settings > Usage`; the plan line under your name in the left sidebar shows the plan at a glance (for example `Pro · Free trial`, or `Gift Trial` while you are on welcome credits). Credit amounts are shown with up to one decimal (for example `2.5 credits`).

### Welcome Credits

A new account starts with a small welcome gift of credits (`Gift Trial`). It is sized for one or two Lite 720p cloud clips, not a whole video — enough to try the pipeline. While you are on welcome credits with no plan, new stories and posters default to the `Lite` tier, and renders made on gift credits carry a small visible Aificient watermark.

### Free Trial

When a free trial is on offer for your account, it applies to **one plan** (normally the cheapest): you save a card, receive the trial's credits immediately, nothing is charged for the trial's days, and the plan starts billing when the trial ends unless you cancel. Everywhere in the app a `Start free trial` action is marked with a **flag icon**.

Where you meet it:

- The **closing step of the introduction tour** — `Try <Plan> free for N days`, with `Start free trial` and `See all plans`.
- The **sidebar card** above your profile row — `Try <Plan> free` / `N days free · N credits`; one click opens the checkout. It shows only while the account has no subscription and disappears the moment a plan or trial starts.
- The **chat**, when a story/poster/character turn is refused for lack of credits (see "Running Out of Credits").
- The **out-of-credits card** inside a project — `Keep creating — N days on us`.
- The **plans modal** (`Compare plans` / `See plans` anywhere, or `Settings > Usage`) — the trial plan's card shows `0 / N days`, `then <price> / <interval>`, the trial credits, and a gold `Start free trial` button. Clicking it shows `Opening secure checkout in your browser. Your trial credits are granted as soon as your card is saved — nothing is charged today.`

Checkout always opens **outside the app**: your default browser on the desktop, a new tab on the web. When you return, a result card reads `Your free trial has started` with `N credits are ready to use.` and the date the plan bills, or `That card can't start a trial` with the reason (prepaid and disposable cards cannot start a trial; a card that already started a free trial on another account cannot start a second one) and a `Try another card` button.

During the trial the plans modal shows `You're on a free trial of <Plan> until <date>, when it becomes a paid plan. You can switch plans after that, or start the plan now to get its full credits today.` Other plans read `Available after trial`. `Start plan now` opens a confirmation (`Ends your <Plan> trial today. Your card is billed right away and the plan's full credits unlock immediately.`) with `Due now`, `Credits unlocked`, and `Then` rows. If you use up the trial's credits early, the out-of-credits card says `You've used your trial credits` and offers `Start my plan now`.

Once a subscription is active — including a free trial — new stories and posters default to the `Pro` tier.

### Daily Credits

Accounts on an active plan or free trial can claim a free top-up of credits **once per calendar day**. The amount comes with your plan (plan cards in the plans modal show `+N credits every day`, and the trial offer says `Plus N credits to claim free every day of the trial.`). The day resets at **midnight in Europe/Madrid** (`00:00 CET` or `00:00 CEST`), the same moment for everyone — not 24 hours after your last claim. Accounts with no subscription have nothing to claim.

Claiming always takes a click; nothing is credited automatically. Three places offer it:

- **A popup, once per day** — `Your daily credits are ready` / `A fresh top-up lands on <Plan> every single day — today's is waiting.` with a `Claim N credits` button. It opens the first time the app sees an open claim that day on that device, and stays out of the way while the plans modal, an out-of-credits card, a billing result, or the tour is open. After claiming it reads `+N credits added` / `They're in your balance now — N credits to spend.` with `Back to creating`, plus a small confetti payoff. Closing it with `×`, `Esc`, or the backdrop leaves the claim on the sidebar card.
- **The sidebar card** above your profile row — `Daily credits ready` / `Claim N credits`; its tooltip reads `Claim today's N credits — free with your plan, every day at 00:00 CET.` One tap claims. It then reads `+N credits added` / `Back tomorrow at 00:00 CET`, fades out, and reappears on its own after the next reset even in a session left open overnight. This card takes priority over the free-trial card and the desktop-app link.
- **The out-of-credits card** inside a project, when you hit zero on a plan or trial: `Today's free credits are still unclaimed.` and the primary button becomes `Claim N credits free`. After claiming, the gauge climbs back and the card closes by itself so you can retry the generation.

From the second consecutive day the card and popup show a streak (`3-day streak · keep it going`). Once today's credits are claimed the controls disappear; the out-of-credits card instead shows a countdown chip such as `Free credits in 6 hours` (tooltip `Resets at 00:00 CEST (Europe/Madrid)`). If a claim is refused because it was already made on another device, the app simply re-syncs your balance; any other failure shows `Unable to claim your daily credits.` There is no separate toast — the card or popup state is the confirmation.

### Running Out of Credits

- **In the creation chat**, a refused turn gets a plain reply instead of an error bar — `You've used up all the credits on your current plan. Upgrade to keep generating — you'll get more credits instantly.`, `You've used up your welcome credits. Start your free trial to keep generating — you'll get N credits right away.`, or `This account doesn't have any credits yet. …` — followed by a card: `Try <Plan> free for N days` with `Start free trial` and `See all plans` when a trial is on offer, otherwise `Out of credits` / `Upgrade plan` or `No credits yet` / `See plans`.
- **Inside a project** (a generation run or a cloud render submission), an out-of-credits card takes over with an animated gauge counting down to `0 credits left` and one of: `Keep creating — N days on us` (`Start free trial`), `You've used your trial credits` (`Start my plan now`), `You're out of credits` on a paid plan (`Upgrade plan` — `Move up a tier and the extra credits land instantly — you only pay the difference for the days left.`), or `You're out of credits` with `Choose a plan`. On a plan or trial the daily-claim lifeline described above appears here too. `Not now` closes it.
- **Cloud renders** that cannot be fully paid for are sent scene by scene until the balance runs out; the rest are listed in the generation report (`Not enough credits to render this scene. Render it from the scene panel once you have more credits.`).

## 23. Publishing the Final Video

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

## 24. Updates

The app can check whether a newer desktop version is available.

If an update is available:

1. A modal shows the current and latest version.
2. Click `Update` to start.
3. A dedicated update window shows download progress.
4. The installer opens when ready.
5. The app closes so the installer can continue.

If the update fails, the update window shows an error.

## 25. Downloads and Sharing

You can download final videos and many generated assets.

When downloading:

- Choose where to save the file.
- The app writes only to the selected location.
- Downloads may take time for large videos.

The fullscreen viewer also includes a share action when supported by your system.

## 26. Where To Find UI Options

Use this section when a user asks questions like "Where is X?", "How do I open X?", "Where can I change X?", "I cannot find X", or "Where is the button for X?".

When answering, give the shortest path from a stable area of the app, such as `left sidebar > Settings > GPU Config`. If an option only appears after selecting a project, opening a modal, generating an asset, or entering render settings, say that first.

### Main Navigation Locations

| User asks for | Where to find it |
| --- | --- |
| `Ask AI`, help chat, or Support Assistant | Top-right window-actions area, next to the minimize/maximize/close controls. |
| Window minimize, maximize, restore, or close | Top-right window controls. |
| Projects | Left sidebar, in the `Recent projects` list below the primary navigation. |
| Search projects | Magnifying-glass button in the left-sidebar header; it opens a search dialog with recent projects and filtered results. |
| Filter projects by type (History / Posters) | The `All` / `History` / `Posters` chips inside the project search dialog. The sidebar list itself is grouped by type instead of filtered. |
| Older projects that are not in the list | Expand the project's group heading in the left sidebar, then use `Show more` (groups page 25 at a time). |
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
| Introduction tour / guided tour / replay the tour | It runs by itself for a new account on the home screen. To replay: `Settings > General > Introduction tour > Replay`. |
| Claim daily credits / free daily credits | The `Daily credits ready` card above the profile row in the left sidebar, the once-a-day popup, or the `Claim N credits free` button on the out-of-credits card inside a project. Requires an active plan or trial; resets at 00:00 Europe/Madrid. |
| Start the free trial | The `Try <Plan> free` card above the profile row in the left sidebar, the tour's closing step, the out-of-credits card, the chat card after a refused turn, or the plans modal — all marked with a flag icon. |
| Plans / compare plans / upgrade | `Settings > Usage`, the profile row in the left sidebar (opens Settings), or any `See plans` / `Compare plans` / `Upgrade plan` link. |
| Credit balance | `Settings > Usage`; the plan line under your name in the left sidebar shows the plan. |
| Menu on a phone / where did the sidebar go | The menu button at the top-left opens the sidebar as a drawer (phones only). |
| Aificient Cloud queue on the web | `Aificient Cloud` in the left sidebar (the web replaces `Generation assets` with it). |

### Creation Home Screen Locations

| User asks for | Where to find it |
| --- | --- |
| Story mode (formerly Concept) | Left sidebar > `New project`, then choose `Story` in the segmented control above the home-screen composer. |
| Brainstorm | Left sidebar > `New project`, choose `Story`, then turn on the `Brainstorm` switch below the prompt, after the language control. |
| Character mode | Left sidebar > `New project`, then choose `Character` above the composer. |
| Poster mode | Left sidebar > `New project`, then choose `Poster` above the composer. |
| Animate a poster I already have | Poster mode, then the `I have a poster` toggle below the prompt, then the `Poster image` pill. |
| Design a poster from a description | Poster mode, then the `From zero` toggle below the prompt. |
| Poster reference images | Poster mode > `From zero`, then the `Reference assets` pill below the prompt. |
| Poster aspect ratio | Poster mode > `From zero`, aspect-ratio pill below the prompt. For an imported poster the ratio comes from the image and cannot be set. |
| Poster clip length | Poster mode, duration pill below the prompt (5–15 seconds), or later in the project's right sidebar > `Settings` > `Video duration`. |
| Find inspiration / example videos | Creation home screen in `Story` mode with `Brainstorm` off, the `Find inspiration` button below the composer. |
| Idea prompt or chat prompt | Creation home screen, `Story` mode (with or without `Brainstorm`), in the bottom composer. |
| Character prompt | Creation home screen, `Character` mode, in the bottom composer. |
| Visual style | Creation home screen, style pill below the prompt. |
| Duration | Creation home screen, duration pill below the prompt in Story mode. |
| Language | Creation home screen, language control below the prompt in Story mode. |
| Pinned characters | Creation home screen, `Characters` pill below the prompt in Story mode. |
| Character library | `Character list` in the left sidebar, or the `Characters` picker in a Story composer. |
| Character search, filters, previews, rename, create, and delete | Left sidebar > `Character list`. |
| Reference image for a character | Creation home screen, `Character` mode, `Image`/`Reference` control below the prompt. |
| Character voice | Creation home screen, `Character` mode, `Voice` pill below the prompt. |
| Generate button for a story | Creation home-screen chat, on the generated story script. |
| Stop or cancel a brainstorm, story, or character chat request | Creation home-screen chat — while a request is generating, the send button becomes a stop (filled square) button; click it to cancel. |
| Edit the generated concept (title, characters, scenes, scripts) | Two ways: ask the AI in the `Story` chat, or click `Edit` in the `Script` preview panel on the render-settings screen. |
| Edit the script by asking the AI / with a prompt | Creation home-screen `Story` chat — type the change you want and the assistant rewrites the script. |
| `Edit` button for the script | Right-side `Script` preview panel on the render-settings screen (after continuing from the concept), not on the chat screen. |
| Edit a scene title, description, or script before generating | Render-settings `Script` preview panel in `Edit` mode, in the scene's card. |
| Change which characters appear in a scene | Render-settings `Script` preview panel in `Edit` mode, under `Characters in scene`. |
| Edit the narrator voice profile | Render-settings `Script` preview panel in `Edit` mode, in the `Narrator` section. |
| Render settings before first generation | Continue from a generated concept on the creation home screen; render settings slide into the main workspace. |
| Attach a product, outfit, location, or prop image to a story | Creation home screen, `Story` mode, the `Assets` pill below the prompt (up to 8 PNG/JPG, 20 MB each), or drag the images anywhere onto the home screen. |
| Assets attached to a story / what the script planned | The `Assets` block on the plan card in the chat (`AI planned` and `generated later` tags), and the asset chips on each scene row of the plan. |
| Composer options on a phone (style, aspect, language, duration) | The `Options` pill below the prompt opens a bottom sheet with those controls. |
| Price of a chat generation | The `N cr` chip next to the send button; corrections are included and creating the project is free. |
| Chat history / reopen a brainstorm, story, poster, or character chat | `History` at the top-right of the creation home screen (`Recent chats`, filter `All` / `Story` / `Poster` / `Character`). |

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
| Video guidance (Video CFG) | Selected project > right sidebar > `Settings`, or global `Settings > Model Config`. |
| Audio guidance (Audio CFG) | Selected project > right sidebar > `Settings`, or global `Settings > Model Config`. |
| Prefetch count | Global `Settings > Model Config`. |
| Speech pace | Selected project > right sidebar > `Settings`, or global `Settings > Audio Config`. |
| SFX volume (video-model soundtrack level under the narration) | Selected project > right sidebar > `Settings`, or global `Settings > Audio Config`. |
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
| Stop or cancel video/asset generation | During active generation, in the visible generation/progress controls or right sidebar stop action. To cancel a brainstorm/story/character chat request instead, use the stop button in the creation home-screen chat. Cloud queue cancellation is under `Generation assets > Aificient Cloud`. |
| Generation error summary, error box, or list of failed tasks | Top-right corner of the center canvas, shown after a generation finishes with one or more errors. |
| Publish | Bottom area of the right scene sidebar for the selected project. Opens the Publish dialog to post the final video to TikTok, Instagram Reels, or YouTube Shorts. Enabled once the project has a final video. |
| Generate an AI caption | Publish dialog, compose step, the `Generate` (atom) button next to the caption section. |
| Add or change a TikTok sound | Publish dialog, compose step, the `Sound` section picker. |
| Choose the cover / thumbnail frame | Publish dialog, review step (after `Prepare publish`), the `Thumbnail` section. |
| Schedule a post for later | Publish dialog, review step, `When to publish` > `Schedule`. |
| Cancel an in-progress upload | Publish dialog upload progress screen, the `Cancel` button. |
| Publish history (past/queued posts) | Publish dialog, `History` button at the top-right. |
| Poster render settings (mode, resolution, duration, runtime) | The settings screen after `Create project` on a poster plan, or later in the project's right sidebar > `Settings` tab. |
| Where a poster animation renders | Poster render-settings screen > `Runtime` (one GPU or Aificient Cloud), or the project's right sidebar > `Resume Generation`. |
| Render a poster animation later | Poster project > right sidebar > `Resume Generation` > pick a runtime > `Add to render queue`. |
| Generate the poster images without the animation | Poster render-settings screen > `Images only`, or right sidebar > `Resume Generation` > `Images only`. |
| Poster mode (Lite/Pro), resolution, or clip duration for an existing poster | Poster project > right sidebar > `Settings` tab, then `Apply changes`. |
| Render the reference image of a new character that is not in any scene | Right sidebar > `Resume Generation` > `Images + Audio only` (the button stays active for an uncast character with no image, even when the final video exists), or `Regenerate images + audio` right after adding the character. |
| Generate the images of pending project assets | They render automatically at the start of the next run; use `Resume Generation` > `Images + Audio only`, or `Generate image` in the asset's detail modal. |
| Assets per scene / assets per character limits | Fixed by the service (5 per scene, 3 per character); there is no setting for them. The scene and outfit pickers stop at those numbers. |
| Resume Generation on a phone | The floating `Resume` / `Stitch` pill beside `Details` at the bottom of the screen. |

### Project Review And Editing Locations

| User asks for | Where to find it |
| --- | --- |
| Project outline | Select a project, then open the right scene sidebar > `Schema` tab (`Plan` tab for a poster). |
| Poster plan outline and generation status | Select the poster, then right sidebar > `Plan` tab. |
| Poster prompt, first-frame prompt, or video prompt | Center canvas of the poster project; click the prompt node to open its rewrite modal. |
| Delete a poster image, first frame, or animation | The matching media node on the poster canvas; the button states what the delete takes with it. |
| Scene list | Select a project, then right scene sidebar > `Schema` tab. |
| Asset browser | Select a project, then right scene sidebar > `Assets` tab. |
| Project-specific settings | Select a project, then right scene sidebar > `Settings` tab. |
| Focus a scene or node | Click an item in right scene sidebar > `Schema`, or use a focus action in `Assets`. |
| Scene description, character reference, or script text | Center canvas, in the scene's text/detail nodes. |
| Rewrite scene text | Click the scene text node on the center canvas, then choose manual edit or AI rewrite. |
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
| Add a character to an existing story | `Add character` under the last cast card on the center canvas (or the `Add character` card when there is no cast); tabs `Manual`, `AI`, `Library`. |
| Put a character into a scene / change a scene's cast | The `Cast` strip on the scene card (`Add cast` / `Edit cast`), then `Save cast`. |
| Project assets / asset base | The `Assets` card right after the project card on the center canvas; also listed as `Project asset` in right sidebar > `Assets`. |
| Upload an image as a project asset | `Upload an image` on the `Assets` card (PNG/JPG). |
| Create a project asset with AI | `Create from a prompt` (atom icon) on the `Assets` card. |
| Edit, regenerate, place, or delete a project asset | Click its tile on the `Assets` card: `Details`, `Generate` / `Regenerate image`, `Place with AI`, `Delete from project`. |
| Give a character an outfit / wardrobe | The `Outfit` strip on the character card (`Add outfit` / `Edit outfit`), or the `Look` section of the character editor. |
| Assign assets to a scene | The `Assets` strip on the scene card (`Add assets` / `Edit assets`). |
| Save a project character to the library | The `Library` button on the character card (needs a generated image). |
| Edit a library (global) character inside a project | Not possible directly: click `Project variant` on its card to get an editable project copy, or edit it in `Character list`. |
| Keep a character recognizable while rewriting it with AI | Character editor > `AI` tab > `Keep the current look as reference`. |
| Delete a character from a project | The trash button on the character card (project characters only). |
| Mute the narration while previewing a clip | The narration toggle on the video node. |

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
| Social media caption instructions / guidance for AI publish captions | `Settings > Model Config`. |
| Vast.ai key or API key | `Settings > API Keys`. |
| Vast.ai balance | `Settings > API Keys`. |
| GPU rental disk space, max price, or reliability filters | `Settings > GPU Config`. |
| GPU family for a rental | Left sidebar > `Generation assets` > `Create instance`, then choose a GPU profile. |
| Default model quality, guidance, or prefetch | `Settings > Model Config`. |
| Local runtime download folder | `Settings > Model Config`; stop the local runtime before changing it. |
| Default speech pace, SFX volume, or default narrator voices | `Settings > Audio Config`. |
| Default voice timing, transition duration, or captions | `Settings > Video Config`. |
| Replay the introduction tour | `Settings > General`, the `Introduction tour` row, `Replay`. |
| Free-trial status or billing date | `Settings > General` (the `Free trial · bills <date>` badge) or `Settings > Usage`. |
| Daily credits amount for a plan | The `+N credits every day` row on each plan card in the plans modal. |

## 27. Support Assistant (Ask AI)

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

## 28. Troubleshooting

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
- Your subscription is active and has enough credits for the displayed estimate. With fewer credits than the estimate, only the first scenes the balance covers are sent; the rest wait for more credits.
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

### I cannot add another poster reference image

Reference images and pinned characters share one budget of 5, and characters have their own limit of 3. The `Reference assets` pill shows the combined count and its tooltip explains what is blocking you — unpin a character to free a slot, or remove an image.

### A poster plan will not create

- **"This poster has N references and the limit is now 5."** The plan was written before images and characters shared a budget. Send any correction in the chat; the oldest extras are dropped and the plan comes back ready to create.
- **"One of the reference images is no longer in your assets folder."** Poster references live in your assets folder rather than inside the project. If one was deleted, attach it again in a chat correction.
- **"A selected character is no longer in your library."** Unpin it and send the prompt again.
- **Reference images must be JPG or PNG.** Convert the file and attach it again.
- **The poster took too long to generate.** Reference images make plan generation slower — try again, or with fewer of them.

### The poster render button is disabled

Check, in order:

- The `Settings` tab has no unsaved changes. A render always uses the saved video config, so the footer warns `Unsaved video settings` and blocks the submit until you `Apply changes`.
- A runtime is selected in the `Resume Generation` menu (one GPU, or Aificient Cloud when it is available).
- The animation is not already rendered — the button is disabled when there is nothing left to do.

### My poster has no captions or Publish button

Posters do not have either. There is no narration track to transcribe, so there is no caption step, and the `Publish` dialog is available for History projects only.

### I added a character but cannot generate its image

A new character is in no scene until you cast them, and nothing regenerates when you add them. To render the reference image for preview, use `Regenerate images + audio` in the confirmation right after adding, or right sidebar > `Resume Generation` > `Images + Audio only`. The button stays active for an uncast character with no image even when the project's final video already exists; the character card shows the progress and the image lands when the run finishes. To put the character in the video, use the `Cast` strip on the scenes they belong in.

### I cannot edit, delete, or dress a character

A card with a `global` badge is a library character: it cannot be changed from inside a project (`Global characters cannot be edited from the jamboard`). Click `Project variant` on its card to get an editable copy for this project, or edit the original in `Character list`. Every card's actions are also hidden while the project is generating; wait for the run to finish or stop it.

### I cannot attach more assets to a story

The composer accepts at most 8 assets per story request, PNG or JPG, up to 20 MB each (`At most 8 assets can be attached to one story.`, `Only N more asset(s) fit — the extras were skipped.`, `Only PNG or JPG images are accepted.`, `Image exceeds the 20MB limit.`). Remove one from the `Assets` panel to add another. Inside a project the asset base itself has no cap, but a scene can carry at most 5 assets and a character at most 3. Those limits are fixed by the service and cannot be changed; unselect one asset in the picker to make room for another.

### "Cannot update assets while a task is in progress"

Asset, outfit, and cast changes are blocked while a generation task runs. Wait for it to finish, or stop the generation, then try again.

### An asset tile is dashed / a chip says "pending generation"

That asset has no image yet — usually one the script planned. It renders automatically at the start of the next generation run (before characters and scenes). To render it now, open its tile and click `Generate image`, or use `Resume Generation` > `Images + Audio only`. A failed asset never fails the run; the scene simply generates without that reference.

### I cannot claim my daily credits

- Daily credits need an active plan or free trial; an account with no subscription has nothing to claim.
- They can be claimed once per calendar day and reset at 00:00 Europe/Madrid (`CET` / `CEST`), not 24 hours after the last claim. Once claimed, the card and popup disappear and the out-of-credits card shows `Free credits in N hours` instead.
- If you claimed on another device, the app re-syncs silently. Any other failure shows `Unable to claim your daily credits.` — check your connection and try again from the sidebar card.

### The free trial checkout refused my card

Prepaid and disposable cards cannot start a trial, and a card that already started a free trial on another account cannot start a second one. The result card offers `Try another card`; the trial stays available.

### The introduction tour did not appear

It starts on its own only for an account less than 14 days old, on the home screen, once billing has loaded, and only once per device or browser. Replay it any time from `Settings > General > Introduction tour > Replay`.

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

## 29. Recommended Workflows

### Fast Preview Workflow

Use this when you want to inspect assets before video rendering.

1. Create a concept.
2. Choose `Generate images and audio only`.
3. Review images and narration.
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

1. Create a character in Character mode (it lands in the library), or save a project character from its card with `Library`.
2. Pin it when creating a new concept, or add it to an existing story from `Add character > Library`.
3. Generate the project.
4. Review scenes where the character appears.
5. If the character needs a project-only change (a different outfit, a scar, an older look), click `Project variant` on its card and edit the copy.

### Add a Character Mid-Project Workflow

Use this when a story needs someone who was not in the original script.

1. Click `Add character` under the cast column and describe them (`Manual`), let the AI write them from a prompt or reference photos (`AI`), or pick one from `Library`.
2. Click `Regenerate images + audio` in the confirmation (or `Resume Generation > Images + Audio only`) to render the reference image and check the look. Nothing else regenerates yet.
3. Adjust with `Edit` if needed — `Keep the current look as reference` keeps the face while you change details.
4. Open the `Cast` strip on each scene the character belongs in and `Save cast`; those scenes regenerate their image and video on the next run.
5. `Resume Generation` to rebuild the affected scenes and the final video.

### Brand or Product Placement Workflow

Use this when a real product, logo, or location must appear consistently.

1. In the Story composer, attach the packshots and location photos with the `Assets` pill (up to 8), then describe the video.
2. Read the plan card's `Assets` block and the asset chips on each scene row; ask for corrections in chat if the product should appear elsewhere.
3. Generate. Uploaded assets are never regenerated — what you uploaded is what the image model is shown.
4. On the canvas, fine-tune: `Edit assets` on a scene to add or remove the product, or open the asset's tile and use `Place with AI` (`show it wherever the chemist is drinking`).
5. Missing something? `Upload an image` or `Create from a prompt` on the `Assets` card adds new assets at any time.
6. `Resume Generation` to rebuild only the scenes you changed.

### Consistent Wardrobe Workflow

Use this when a character must wear the same outfit in every scene.

1. Add the outfit to the asset base (upload a photo of the garment, or `Create from a prompt` with kind `Wardrobe`), or attach a reference photo when adding the character.
2. On the character card, `Add outfit` and select the asset (up to 3 per character). Saving regenerates the character's image and the scenes they appear in.
3. `Resume Generation > Images + Audio only` to review the new look before spending render time.
4. `Resume Generation` with a runtime to re-render the affected clips and the final video.

### Animate an Existing Poster

Use this when you already have finished artwork.

1. Open `Poster` mode and select `I have a poster`.
2. Attach the poster image and describe how it should move.
3. Pick a clip length, then send the prompt.
4. Refine the plan in chat until the motion reads right.
5. `Create project`, choose `Lite`/`Pro`, resolution, and one runtime, then `Start generation`.
6. Download the animation from the final-video node.

### Design and Animate a Poster From Zero

Use this when there is no artwork yet.

1. Open `Poster` mode and select `From zero`.
2. Describe the poster, attach up to 5 references (each pinned character counts as one), and pick the aspect ratio and duration.
3. Review the plan's three prompts and refine them in chat.
4. `Create project` with `Images only` if you want to inspect the poster before spending render time.
5. Check the designed poster and first frame on the canvas; rewrite a prompt and regenerate the images if needed.
6. Use `Resume Generation` > pick a runtime > `Add to render queue` to render the animation.

## 30. Glossary

### Asset

A generated file such as an image, audio clip, scene video, or final video. Not to be confused with a project asset (below).

### Project Asset / Asset Base

A reusable reference image in a story project — a product, a wardrobe item, a location, a prop — that scenes and characters reference by id. The asset base is the `Assets` card on the canvas that holds them. Assets come from the composer's `Assets` pill, from the script planner (`AI planned`), from `Upload an image`, or from `Create from a prompt`. Uploaded assets are ground truth and are never regenerated; generated ones can be re-rolled. A `pending` asset has no image yet and renders at the start of the next run.

### Outfit (Wardrobe)

The project assets a character wears, shown as chips on the character card. They are attached to the image model when the character's reference image is rendered, so the look follows the character into every scene. Capped at 3 per character by the service.

### Cast

The characters that appear in a scene, shown as chips on the scene card and edited with `Edit cast`. Changing a scene's cast regenerates its image and video; narration is kept.

### Global (Library) Character

A character that lives in your library and is referenced by a project rather than owned by it. It shows a `global` badge on the canvas and cannot be edited, deleted, or dressed from inside a project.

### Project Variant

An editable project-only copy of a library character, created with the `Project variant` button. The library entry and every other project using it stay untouched.

### Welcome Credits (Gift Trial)

The small credit gift a new account starts with — enough for one or two Lite 720p cloud clips. Renders made on gift credits carry a small Aificient watermark, and new projects default to `Lite`.

### Free Trial

A time-limited trial of one plan: save a card, receive the trial's credits at once, pay nothing until the trial ends. Marked everywhere with a flag icon.

### Daily Credits

A free top-up that accounts on a plan or trial can claim once per calendar day (reset at 00:00 Europe/Madrid) from the sidebar card, the daily popup, or the out-of-credits card. It always takes a click.

### Introduction Tour

The seven-step guided walk through the home screen that starts for new accounts and can be replayed from `Settings > General`.

### Runtime

A local or rented GPU environment used for video rendering.

### Render Queue

The per-GPU line of pending work. Each scene video is a job that waits its turn on the GPU it was assigned to, so multiple projects can share a GPU and a single project's videos can be split across several GPUs. The final stitch is not a GPU job — it runs locally in the app.

### Aificient Cloud

The subscription-backed render service available on initial render settings and from `Resume Generation` for eligible scene videos. It uses credits and has its own queue, separate from local and rented GPU queues.

### History Project

The multi-scene kind of project: a concept becomes a script, scenes, images, narration, clips, and a stitched final video. It is what the `Story` chat produces (with or without `Brainstorm`).

### Poster Project

A project that animates one poster into a short clip (5–15 seconds) with model-generated sound. It has no scenes, captions, or stitch step — the rendered animation is the final video.

### Poster Plan

The output of a poster chat: a title, up to three prompts (poster, first frame, video), the attached references, and the clip's duration and aspect ratio. Creating a project from it is what starts generation.

### First Frame

The opening image of a poster animation, derived from the finished poster. The animation runs from the first frame back to the poster.

### Reference Budget

The five slots a poster's reference images and pinned characters share. Each character counts as one slot, and characters have their own limit of three.

### Scene Image

The still image used as the visual basis for a scene.

### Narration

The spoken audio generated from the scene script.

### SFX

The sound effects and ambience the video model composes into each clip's own
soundtrack. There are no separate SFX tracks or cues to edit; the `SFX volume`
setting controls how loud this soundtrack plays under the narration.

### Raw Clip

A generated scene video before final stitching.

### Stitch

The process of combining scene clips into the final video: each cloud scene's narration is mixed over its clip's soundtrack, each narrated scene is trimmed to end just after its voice, and the scenes are joined with the configured transition. It runs locally in the desktop app once every scene clip is ready. Only one stitch runs at a time; additional stitches wait in a local queue.

### Final Output

The completed video shown in the Output node.

### Guidance (CFG)

Classifier-Free Guidance. A setting that controls how strictly the AI follows your prompt. Video guidance (Video CFG) applies to visual generation, and Audio guidance (Audio CFG) applies to sound generation. Higher values mean stricter adherence, while lower values allow more creative freedom.

### Support Assistant

The in-app help chat, opened with the `Ask AI` button, that answers questions about using the app based on this guide.
