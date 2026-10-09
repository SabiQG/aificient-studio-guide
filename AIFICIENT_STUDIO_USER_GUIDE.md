# Aificient Studio User Guide

Last reviewed: October 9, 2026 (app version 1.6.5).

This guide explains how to use Aificient Studio from the application interface. It focuses on visible screens, menus, controls, generation workflows, editing tools, GPU management, settings, and common troubleshooting.

## 1. What Aificient Studio Does

Aificient Studio helps you create AI-generated video from a written idea. You start in a creation chat, review the script and scenes the AI proposes, and render on your own GPU or on Aificient Cloud. You can:

- Brainstorm video ideas.
- Turn an idea into a structured story script.
- Create reusable characters, and add new ones to a story at any point.
- Build a project **asset base** (products, wardrobe, locations, props) that the script weaves into scenes and that characters can wear, so a real brand, outfit, or place stays consistent across the whole video.
- Generate scene images, narration, sound effects, video clips, and a final stitched video.
- Narrate in any of fifteen languages, picked by hand or read from what you wrote, with a narrator voice from the app's library, one of thousands more in the `Voice library`, or your own clone. You can change the narrator's voice from the canvas at any time.
- Clone your own voice from a few recordings and narrate with it.
- Animate a poster, one you already have or one the app designs for you.
- Make a short creator-style ad (a **UGC ad**) for a product, a course, or an event from your photos or a product page, a creator, and a voice. Or open it on something impossible with `Crazy hook`.
- Review and edit individual scenes, recast them, change which assets they show, and have the AI write a newly cast character or asset into the scene's text, or take a deleted one out of it.
- Ask the in-project assistant (`Edit with AI`) to make changes for you: rewrite a scene, add one, change the voice, turn captions on, render what is missing.
- Teach the AI your own standing instructions once (your tone, your structure, what to avoid) as **Skills**, and switch them on in any chat.
- Choose how each scene comes in after the one before: a hard cut, a crossfade, a wipe, a zoom, and more.
- Regenerate only the parts that need changes.
- Render video with a local GPU runtime, rented GPU instances, or Aificient Cloud when that option is available.
- Claim free daily credits on a plan or trial, and try the app on a free trial before subscribing.

### Three Kinds of Project

You choose which kind of project you are making when you start the creation chat:

- **History** — the original multi-scene flow. A concept becomes a script, characters, scene images, narration, sound effects, scene clips, and a final stitched video. Everything in this guide applies to it unless a section says otherwise.
- **Poster** — a single poster brought to life as a short animated clip (5–15 seconds) with model-generated sound. There are no scenes, no narration, no captions, and no stitching. See "Poster Projects".
- **UGC ad** — a creator-style ad of one to ten short scenes, planned from what you sell. A creator speaks on camera (or a voice speaks off screen), every clip is rendered on Aificient Cloud from your photos and the voice's reading of each line, and the clips are stitched like a story. See "UGC Ads".

All three appear in the same project list, grouped by type. History and Poster projects render on your own GPU or on Aificient Cloud; UGC ads render on Aificient Cloud only.

### Your First Video, Step by Step

This is the shortest path through a History project. Each step has its own section later in the guide.

1. Sign in with the method offered to you: Google, Apple, or an email code (see "Signing In").
2. Click `New project` in the left sidebar. The home screen opens with the creation chat.
3. Pick **Story** above the composer and type what the video is about in the prompt box. If you have them, attach the products, wardrobe, or locations the video must feature. If you are not sure yet, ask for ideas and the assistant brainstorms before writing the script (see "Creating a New Project").
4. Review the plan card: the scenes, characters, and planned assets the AI proposes.
5. Continue to the render settings: aspect, resolution, `Lite` (fast and affordable) or `Pro` (maximum quality), and where to render, your GPU or Aificient Cloud (see "Render Settings").
6. Click `Start generation`. The app works through the stages in order: script, images, narration, scene videos, final cut.
7. Watch the result come together in the canvas and the scene sidebar (see "Center Canvas").
8. Fix what you want to change: rewrite a scene's text, recast it, add a character, or dress a character or a scene with assets (see "Editing and Regeneration").
9. Click `Resume Generation` to render only the parts you changed (see "Resume Generation").
10. Download the final video from the Output node (see "Downloads and Sharing").

### Desktop, Web, and Phone

The same app runs as a desktop application (Windows) and in the browser. A native **iPhone app** shares the same account, projects, characters, voices, credits, and plan (see "The iPhone App"). Everything in this guide applies to the desktop and the web unless a note says otherwise. The differences that matter:

- **Web** has no local or rented GPUs. Scene videos render on Aificient Cloud, and so does the final stitch (the desktop stitches locally). GPU rentals are offered from the desktop app, and the `Publish` dialog is desktop-only.
- **Phone** (a viewport narrower than 768 px) keeps every feature but rearranges it. The left sidebar becomes a drawer behind a menu button at the top-left, most composer pills fold into an `Options` sheet, dropdowns become bottom sheets you can swipe away, and the right project sidebar is reached through a floating `Details` pill. Tablets and larger screens behave like the desktop.

## 2. Signing In

When you open the app, you may see a sign-in window. The sign-in methods available can include Google, Apple, and an email code.

### Email Code

If email sign-in is available:

1. Enter your email address.
2. Click `Send code`.
3. Enter the 6-digit code you receive. The app verifies it automatically once all digits are entered.

The code screen also lets you resend the code after the cooldown, use a different email, and see when the code expires.

### Staying Signed In and Sign-in Messages

On the desktop app a sign-in is always remembered. The app renews its session in the background while it is open and when it starts, so a window left open overnight is still signed in the next morning. An app update does not sign you out either: the stored session is reissued for the new version. The web app does the same.

`Sign out` ends the session at the server as well, so it stops working everywhere.

Only two things end a session: the server rejecting it as no longer valid, or a closed account. A lost connection, a server error, a proxy or firewall answer, or an "update required" answer never signs you out; the app keeps the session and tries again.

While the sign-in screen is showing, the app keeps looking for the stored session by itself:

- Every few seconds at first, then less often (up to every two minutes).
- Whenever the window comes to the front.
- The moment the connection returns, so an app that starts offline signs you in once it is back.

> **Note:** On the web a sign-in has to finish in the browser tab that started it.

#### Messages You May See

| Message | What it means |
| --- | --- |
| `Your session expired. Sign in again.` | The server rejected the stored session as no longer valid, so the app signed out. Sign in again. |
| `Sign-in took too long or was already used. Sign in again.` | The sign-in failed. Start it again. |
| `That sign-in was not started from this app. Sign in again from here.` | The sign-in failed. Start it again from this app. |
| `Sign-in did not complete. Sign in again.` | The sign-in failed. Start it again. |
| `Couldn't reach the server to finish signing in. Check your connection and try again.` | The sign-in failed because the server could not be reached. Check your connection, then try again. |
| `Sign-in isn't available right now. Try again in a moment.` | Sign-in is not available at the moment. Try again shortly. |
| `An update is required to keep using Aificient Studio. Update to continue — you'll stay signed in.` | You signed in, but this build is too old. The required-update prompt opens over the sign-in screen (see "App Updates"); install it and the app comes back signed in, without signing in again. |
| `You're signed in, but your account couldn't be loaded yet. Aificient Studio keeps trying — no need to sign in again.` | You signed in, but the account details did not load yet. The app retries on its own. |
| `This version of Aificient Studio can no longer sign in. Update the app to continue.` | This old build can no longer sign in at all. Update the app. |
| `This account is closed and set to be deleted on <date>. To keep it, sign in to the Aificient iPhone app if that is where you asked for it, or write to info@aificient.io.` | The account was closed. It shows on the sign-in screens and, if it happens mid-session, as a toast before the app signs out. |

### Introduction Tour

The first time a new account reaches the home screen, a short guided tour walks through the workspace. It dims the screen, spotlights the real control for each step, and shows a card with a `Step N of 7` counter and a progress bar.

The tour starts on its own when all of these are true:

- You are signed in.
- Your plan and credits have loaded.
- No project is open.
- The account is less than 14 days old.

#### The Seven Steps

| Step | Title | What it points at |
| --- | --- | --- |
| 1 | `Welcome to Aificient Studio` | A centered welcome card; its button reads `Show me around`. |
| 2 | `Three ways to create` | The `Story` / `Poster` / `Character` picker above the composer. |
| 3 | `Start with a sentence` | The prompt box. The card ends with `Not sure yet? Ask for ideas and it brainstorms five directions first.` |
| 4 | `Shape it before you render` | The row of pills under the prompt: `Visual style, duration, language and your pinned characters live in this row.` On a phone it reads `Visual style, duration and language sit behind Options; your pinned characters have their own pill.` |
| 5 | `From script to video` | The send button. The card explains the stages (script, images, narration, scene videos, final cut) and the render choice: your GPU or Aificient Cloud, with `Lite` fast and affordable and `Pro` for maximum quality. |
| 6 | `Everything is saved` | The sidebar navigation (projects, character library, render queue). On a phone it spotlights the menu button that opens the sidebar drawer. |
| 7 | Closing card | Depends on your account; see the next table. |

#### The Closing Card

| Your account | Card | What it offers |
| --- | --- | --- |
| Welcome credits available | `You have N free credits` | `Start creating` and `Compare plans`. |
| Free trial on offer | `Try <Plan> free for N days` | `Start free trial` (marked with a gift-box glyph), which opens the trial checkout directly, and `See all plans`. |
| No plan, no credits, no trial | `Choose a plan to start creating` | `See plans` and `Not now`. |
| Subscribed | `You're all set` | Shows the plan's credits for the period, with `Start creating`. |
| Billing unavailable | `You're ready` | Points you to `Settings > Usage` for plan and credits. |

#### Moving Through the Tour

| Control | What it does |
| --- | --- |
| `Next` | Advances one step. On the first step the button reads `Show me around`; both are drawn as the app's steel button. |
| `Back` | Goes back one step, from step 2 onward. |
| `Skip tour` (bottom-left) | Leaves the tour. If the account has welcome credits or a trial on offer, it jumps to the closing card instead, so you still see that information. |
| Close button (top-right) | Closes the tour. |
| `→` | Next. |
| `←` | Back. |
| `Esc` | Closes the tour. |
| `Enter` | Advances, because the primary button has focus. |

The spotlighted control cannot be clicked while the tour is open.

The tour is remembered **per account, per device or browser**. The same new account on a second computer or in another browser sees it again while it is still within its first 14 days.

> **Tip:** Replay the tour at any time from `Settings > General > Introduction tour > Replay`. Replay ignores the account-age rule, closes Settings, and returns you to the home screen.

## 3. Main Workspace

After you sign in, the left sidebar stays visible while the main area changes with what you are doing.

| Area | What it holds |
| --- | --- |
| Left sidebar | Primary navigation, recent projects, project search, generation assets, and the user/settings area. |
| Home/new-project screen | Shown in the main area when no project is open. It contains the Story, Poster, UGC, and Character creation chats. Brainstorming happens inside Story: ask for ideas and the assistant brainstorms before writing the script. |
| Center canvas | Shown when a project is open. It displays the project's visual flow and generated assets. Its bottom-right corner holds the `Edit with AI` bar, the in-project assistant that changes the project for you (see "Edit with AI"). |
| Right project sidebar | Shown with an open project. It contains the project outline, asset browser, project-specific settings, and resume actions. |
| Top-right area | Window controls to minimize, maximize/restore, or close the app (desktop only), and the `Ask AI` button that opens the Support Assistant, an in-app help chat (see "Support Assistant (Ask AI)"). |

The right sidebar's tabs and outline follow the project type:

- History project: `Schema` / `Assets` / `Settings`.
- Poster: `Plan` / `Assets` / `Settings`.
- UGC ad: `Scenes` / `Assets` / `Settings`.

When no project is selected, the main area shows the home/new-project screen instead of an empty canvas. The left sidebar stays available, so you can open an existing project, search, manage characters, or inspect generation assets without closing the creation screen.

> **Note:** On a phone `Ask AI` is an icon-only pill, and a menu button at the top-left opens the sidebar drawer.

## 4. Left Sidebar

The left sidebar is how you move around the app: primary navigation at the top, your recent projects in the middle, and your profile row and `Sign out` at the bottom. It stays visible whatever the main area shows.

### Primary Navigation

The top of the sidebar contains:

- `New project` — leaves the currently open project, shows the home/new-project screen in the main area, and starts a fresh creation chat when needed.
- `Character list` — opens the reusable-character library over the current screen.
- `Generation assets` (desktop) — opens a flyout beside the sidebar with Aificient Cloud jobs, the local GPU, rented GPU instances, and the create-instance action.
- `Aificient Cloud` (web) — takes the place of `Generation assets`. There are no GPUs to manage, so it opens the cloud render queue directly and shows a rendering / queued / history count badge. The flyout's footer on the web offers `Download desktop app` for GPU rentals.

#### Project Search

The magnifying-glass button in the sidebar header opens project search.

- With an empty search it lists recent projects; type to filter by name.
- Results are grouped by project type. The filter chips (`All`, `History`, `Posters`, `UGC`) narrow the search to one type; they exist only inside the search dialog and never filter the sidebar list.
- Click a result, or use the up/down arrow keys and `Enter`. The footer shows the key hints.
- Press `Esc` or click outside the dialog to close it.

### Promo Slot, Profile Row, and Sign Out

Just above the profile row, the sidebar has one slot that shows, in this priority:

- `Daily credits ready` — the daily-credit claim card, when today's free credits are still unclaimed (see "Daily Credits").
- `Try <Plan> free` — the free-trial card, when the account has no subscription and a trial is on offer (see "Free Trial").
- `Download the desktop app` / `For the full experience` — on the web only, when neither of the above applies.

The bottom row shows your avatar initial, your name, and your plan line (for example `Pro · Free trial`, or `Gift Trial` while you are on welcome credits). **Clicking anywhere on that row opens Settings.** The separate `Sign out` button sits beside it.

### Recent Projects

The `Recent projects` list shows the projects stored in your workspace, grouped by type under a `History`, a `Posters`, and a `UGC ads` heading (crazy hooks are UGC ads too). Click a row to leave the home screen and open that project's canvas.

Each group:

- Collapses and expands from its heading.
- Shows the 25 most recent projects first, with `Show more` to reveal the next 25.
- Is hidden entirely when it has no projects, so a workspace with no posters shows no `Posters` heading.

A project row can show:

- The active selection.
- A running/generation indicator (a blinking dot) while the project renders here, on Aificient Cloud, or on another device (another computer, the web, or the iPhone app).
- A final-video-completed indicator.

When you open a project, an overlay shows its name (or `Opening project`) and moves through `Loading project`, `Checking for active renders`, `Building canvas`, and `Preparing scenes`, ending on `Ready`. Media previews load in a controlled queue during this process, so large projects do not try to decode every image and video at once.

There is no progress bar. Instead, the canvas's dot grid flies together into the Aificient logo as the project loads (the share of dots in place is the progress), ripples while the scenes decode, snaps into place when the project is ready, and scatters back into the grid as the overlay fades.

### Project Menu

Right-click a project, or click the `…` (`Project options`) control on its row, to open its menu. The `…` control appears on hover on the desktop and is always visible on touch screens.

- `Rename` — opens the `Rename project` dialog (subtitled with the current name) with a `New name` field (`Project name`, hint `Enter to save`). Select `Rename`, or press `Enter`, to save it; `Cancel` closes it.
- `Delete` — opens `Delete project?` with the text `The project and everything generated for it — images, narration, clips and final videos — are removed from your library.`, a red `This cannot be undone.` line, and `Cancel` / `Delete project` buttons.

There is no duplicate action.

> **Warning:** Deleting a project is permanent from the app's point of view. Use it carefully.
## 5. GPU and Runtime Manager

A runtime is the GPU that renders your scene videos: your own machine's GPU (local) or a remote GPU instance you rent (rented). Rendering a video for the first time on a GPU you manage needs a ready runtime.

**Where:** `Generation assets` in the primary sidebar navigation.

A project whose images and audio are already ready can also use subscription-backed Aificient Cloud rendering through `Resume Generation`, without a ready runtime of your own (see "Aificient Cloud Rendering").

The `Generation assets` flyout appears beside the sidebar and closes when you select an item, click elsewhere, or press `Esc`. Inside it:

- The `Generation assets` row can show compact counts for resources that are actively working and resources that are ready.
- Select the local GPU or a rented instance to open its detail view.
- If cloud jobs exist, the flyout also includes `Aificient Cloud`.

The manager groups resources by status:

- Running/ready.
- Starting or installing.
- Stopped/inactive.
- Error.

### Local Runtime

The local runtime renders videos with your own GPU. It runs the same MiniMax-H3 engine that Aificient Cloud uses, so the picture you get for a given seed is the same; what changes is the time per clip (minutes rather than seconds) and the hardware it asks for.

| Requirement | Minimum | What the app says if it is not met |
| --- | --- | --- |
| Platform | The Windows desktop app | The web app and macOS show `Download the desktop app to generate locally` or `Generation not available on macOS` instead. |
| GPU VRAM | **24 GB** (the check accepts 23 GB, because a 24 GB card reports about 23.6) | The sidebar row reads `Needs 24 GB VRAM`; the detail view shows `insufficient VRAM` with `The local runtime needs at least 24 GB of VRAM to render MiniMax-H3. This GPU has N GB.`, and `Install Drivers` and `Start` are disabled. |
| System RAM | **24 GB** (not for the GPU, but because the model's weights stream through it) | Checked when you click `Install Drivers` or `Start`; see the messages table below. |
| Disk space | 40 GB free for the installer; the first start downloads the MiniMax-H3 model files (around 76 GB), so leave generous room | — |

The model download folder is set in `Settings > Model Config`.

On a 24 GB card the model does not fit entirely on the GPU, so the engine streams parts of it over PCIe every step. A 5-second clip takes about 4.5 minutes on an RTX 4090 at 720p, and 1080p roughly doubles that (see "The 1080p Warning"). From about 40 GB of VRAM upward the whole model sits on the card.

From the local runtime detail view, you can:

- `Install Drivers` — install or prepare the runtime.
- `Start` — start it.
- Stop it.
- Watch setup progress and the live log.
- View logs if something fails (`Error — last 12 lines`, with `Copy logs`).

> **Note:** Local and rented renders make clips the same way Aificient Cloud does. Each scene clip is animated from its image with a length derived from the narration (whole seconds between 4 and 15), and the narration is not baked into the clip — it is mixed over it at stitch time.

#### Messages You May See

| Message | What it means |
| --- | --- |
| `This machine has N GB of system RAM. The local runtime needs at least 24 GB — not for the GPU (<GPU> is fine), but because the model's weights stream through it. Use Cloud Render, or rent a GPU from the Vast.ai tab.` | The system RAM check failed when you clicked `Install Drivers` or `Start`. "The Vast.ai tab" means the rented-GPU tools: `Create instance` in `Generation assets`, and the `Vast.ai` key under `Settings > API Keys`. |
| `<GPU> has N GB VRAM. The local runtime needs at least 24 GB to render MiniMax-H3 — use Cloud Render, or rent a 24 GB+ GPU from the Vast.ai tab.` | The VRAM check failed at the same point. |
| `Setup failed. View details` | The sidebar row after either check fails. The message itself lands in the detail view's red `Error` block, with a `Copy logs` button. |

### Rented GPU Instances

Rented GPU instances are managed from the sidebar and the create-instance modal (see "Renting a GPU"). Only ready instances can be selected for video rendering.

From an instance detail view, depending on state, you may be able to:

- View setup progress.
- View logs in the `Instance logs` panel.
- Start.
- Stop.
- Reboot.
- Destroy.

The `Instance logs` panel shows each line's final state (a download progress bar is one line, not every redraw) with colour codes stripped. `Copy logs` copies that same text and reads `Copied` once it worked.

When an instance is running, its detail view also shows a render queue for that GPU (see "Render Queue").

### Render Queue

Each GPU has its own render queue, and every scene video becomes a job that waits its turn on the GPU you chose for it.

GPUs are not locked to a single project: several projects can line up on the same GPU at once, and a busy GPU is still a valid choice — your videos render after the ones already ahead of them.

The final stitch does not use a GPU: it runs locally in the app once all of a project's scene clips are ready.

Local stitches and caption burns share one local queue that runs one job at a time. If several projects finish rendering around the same time, their stitches run one after another (see "Stitch Node").

The render queue appears in the local runtime and rented instance detail views while the GPU is ready/running. For each GPU it shows:

- Jobs grouped by project, in the order they will run.
- The job currently rendering, with a live progress bar and percentage.
- Queued jobs marked as waiting, with their position in line.

From the render queue you can:

- `X` on a job's row — remove a single queued video, or cancel the one that is currently rendering.
- `Cancel all` next to the project name — cancel all of that project's videos across every GPU at once.

> **Tip:** The `Generation assets` flyout shows a small `N queued` count next to each local or rented GPU, so you can see at a glance how loaded it is without opening the detail view.

### Aificient Cloud Rendering

Eligible projects can render scene videos on `Aificient Cloud` instead of a GPU you manage. It can appear as a runtime on the initial render-settings screen, and later in the selected project's `Resume Generation` menu once source images and audio are ready.

Before submission, the Aificient Cloud option shows the project's `Lite` or `Pro` tier, resolution, and estimated credit cost. It requires:

- An active subscription and enough credits.
- Each scene's image.
- For scenes whose script has spoken text, the narration generated first, because the narration decides the clip's length.

| Limit | Value |
| --- | --- |
| Scenes per submission | Up to 32 missing scenes |
| Narration length per scene | At most 13 seconds |
| Clip length | Whole seconds between 4 and 15, derived automatically from the narration (voice delay + narration + a short tail); a scene with no spoken text renders as a 5-second clip |
| Default resolution for new projects | `720p`, which is much cheaper than `1080p` with very similar quality; `1080p` stays available as an explicit choice and costs more per clip |

Aificient Cloud is selected by itself; it cannot be combined with local or rented GPUs in the same submission.

> **Cost:** If your credits do not cover the whole submission, the app sends the scenes one at a time, in order, until the next one is refused for credits. The scenes it could pay for render; the rest are listed in the generation report so you can render them from the scene panel once you have more credits.

How a cloud clip is made:

- The video model animates the scene image and composes the clip's own soundtrack — quiet ambience and sound effects implied by the visible action only, never speech or music.
- Your narration is **not** baked into the clip; it is mixed over it later, in the preview and in the final stitch.
- Renders made on gift credits carry a small visible Aificient watermark; paid renders do not.

Once submitted, each scene appears as a separate cloud job, and the app refreshes completed clips into the project automatically. If the service answers that some of the scenes are already rendering elsewhere (on your own GPU, or on another device), the submission is retried once without them and nothing is charged for those scenes.

A single queued scene can be taken out of the queue from its video node with `Remove from queue`, which refunds it, and rendered again later with `Resume Generation`, even while the rest of the queue is still running.

> **Note:** Poster projects can also render on Aificient Cloud. A poster is a single clip, so the scene-count and scene-length limits above do not apply; it submits one job that carries the project's saved mode, resolution, and duration, and the delivered clip already includes its generated audio.

#### Cloud Queue and History

When cloud jobs exist, open `Generation assets > Aificient Cloud` to view the current session's queue and history. The window shows queued, running, completed, failed, and cancelled jobs with progress and status messages.

- Remove an individual queued job from its row.
- `Cancel queued` — cancels all queued jobs in a project.
- Reserved credits are refunded when a cloud job fails or is cancelled.

While cloud clips are queued or rendering, the center canvas keeps showing the project's overall generation progress, and the bottom of the right scene sidebar shows the Aificient Cloud queue/rendering status. Cancel queued cloud clips from `Generation assets > Aificient Cloud`; the canvas progress bar does not include a cloud-cancel button.

For account-wide cloud render history, including settled prices, use `Settings > Usage > Load latest generation jobs`.

## 6. Renting a GPU

Rent a remote GPU instance when you want to render without using your own card. Every tier renders the same picture; they differ in time and price.

**Where:** `Generation assets`, then `Create instance` (desktop only)

Clicking `Create instance` opens the `Available Instances` modal. The web offers `Download desktop app` instead, with `GPU rentals run from the desktop app`. If no Vast.ai key is configured, the flyout shows `Add Vast.ai key` instead.

### GPU Tier Cards

The modal header shows the selected tier, its disk, and your price ceiling (for example `RTX 5090 · 140 GB disk · up to $3/hr`) with a `Refresh` button. Above the offers table sit the GPU tier cards:

- Four are shown at first — `RTX 4090`, `RTX 5090`, `RTX PRO 6000`, and `H100 series`. `RTX 5090` is the default tier.
- A bare chevron on the rule beneath them (`Show 4 more GPUs` / `Show fewer GPUs`) reveals the other four. The list opens expanded when your saved tier is one of the hidden ones.
- Hover a card for a note on what that card does with the MiniMax-H3 model.

Each card shows:

- The tier name and its memory.
- The best live price (`$X.XX /hr`), or a price hint while offers load.
- `Price` bar — `Higher means lower expected rental cost.`
- `Speed` bar — `Higher means faster expected generation throughput.`
- `Headroom` bar — `Higher means more of the model stays on the card instead of streaming.`

| Tier | Memory | Price hint | What to expect |
| --- | --- | --- | --- |
| `RTX 3090` | 24 GB GDDR6X | Cheapest | Clears the floor, but the model streams and the card has no hardware fp8, so every step is slower. Best for overnight batches. |
| `RTX 4090` | 24 GB GDDR6X | Budget | The value pick, measured at about 4.5 min for a 5-second clip (about 13 min at 15 s). The model still streams; VRAM peaks near 23.3 GB, so nothing else can use the card. |
| `RTX 5090` | 32 GB GDDR7 | Balanced | Bigger blocks and fewer round trips per step; comfortable 1080p headroom. |
| `L40S / A6000` | 45–48 GB | Value | The first tier where the whole model sits on the card and stops streaming — usually the cheapest row per GB. |
| `A100 series` | 40–80 GB HBM2e | Pro | Fully resident with room for long clips; no hardware fp8, so not automatically faster than an L40S. Pick it for 15-second clips and large batches. |
| `RTX PRO 6000` | 96 GB GDDR7 | Pro | Holds everything at once, nothing streams or is re-read between clips; 15-second clips and the 1080p pass are routine. |
| `H100 series` | 80–94 GB HBM3 | Premium | What Aificient Cloud runs on: a 5 s 720p clip measured 37 s. Rent it when the wait matters more than the bill. |
| `H200` | 141 GB HBM3e | Premium | An H100 with more memory bandwidth; worth it for 15-second clips and back-to-back batches. |

### Offers

The search only returns offers that meet all of these:

- At least 23 GB of GPU memory.
- An Ampere or newer card.
- At least 100 GB of disk.
- At least 32 GB of host RAM.
- Your `Settings > GPU Config` price and reliability limits.

The offers table can include:

- GPU model.
- VRAM.
- Number of GPUs.
- Price.
- Upload and download bandwidth (speed in Mbps and transfer cost per TB).
- Reliability.
- Rent action.

### Download Quality Indicator

The `Download` column shows a small colored status dot next to the speed and cost. It is a quick visual hint for how well an offer can pull large model and asset files, balancing download speed against transfer cost.

| Dot | Meaning | Threshold |
| --- | --- | --- |
| Green | Fast and cheap | At least 1500 Mbps and under $3/TB |
| Yellow | Acceptable | At least 900 Mbps and under $6/TB |
| Red | Slower or more expensive downloads | Everything else |

Hover the dot to see a short text label. Greener dots generally mean faster instance setup and cheaper data transfer; red dots can mean slower setup or higher costs.

#### If No Offers Match

The list reads `No <tier> offers under $X/hr right now` with `Try again` and `Change settings`. `Change settings` opens `Settings > GPU Config` on top of the modal; the offers refresh when you close Settings.

## 10. Render Settings

Before starting generation, the app shows render settings. This section describes the History render-settings screen. A poster has its own, shorter version of the same screen — see "Creating a Poster Project" — and a UGC ad has `Video settings` — see "Video Settings for a UGC Ad".

### Format

- Aspect ratio — `Portrait (9:16)` (default), "TikTok, Reels and Shorts", or `Landscape (16:9)`, "YouTube and desktop". Use `9:16` for vertical/social video and `16:9` for widescreen video.
- Resolution — `720p` (default) or `1080p`.

> **Cost:** `720p` is much cheaper to render with very similar quality; `1080p` costs more per clip.

### Runtime

For the first generation, choose one or more ready GPUs, or select `Aificient Cloud` if it is available for your account.

- Each ready local or rented runtime is listed with a checkbox; tick every GPU you want this project to use. Each option shows how many jobs are already `in queue` on it.
- By default the app pre-selects the lightest-loaded GPU.
- Aificient Cloud is a separate, mutually exclusive target: selecting it clears the local/rented GPU selection. Its row shows the selected `Lite` or `Pro` tier, resolution, and estimated credit cost.

What each choice does:

- **One GPU selected:** all scene videos render on that GPU, in queue order.
- **Several GPUs selected:** the scene videos are split across the chosen GPUs so the project finishes faster.
- **Aificient Cloud selected:** scene videos are submitted to the cloud after their source images and audio are prepared; the app continues through captions and final stitching as the clips arrive.

| Situation | What you can do |
| --- | --- |
| No local/rented GPU and no Aificient Cloud option | Generate images and audio only, review assets, edit scenes, and prepare the project for later video rendering. |
| Local GPU ready | Render video, if the app shows the local runtime as supported and ready. |
| Rented GPU ready | Render video on any selected rented instance. |
| Aificient Cloud available | Render scene videos without starting your own GPU runtime. |
| Busy GPU | Select it anyway: GPUs are queued rather than blocked, so your videos go into its queue behind the work already running. Select additional GPUs to spread the work and finish sooner. |

#### The Action Button

The button at the bottom of the screen reads:

- `Start generation` — the default.
- `Start images and audio` — when `Images and audio only` is on.
- `Queue on N GPUs` — when several GPUs are selected.

It comes with a summary line of the chosen aspect, resolution, tier, and target.

#### Messages You May See

| Message | What it means |
| --- | --- |
| `No GPU is ready right now. Start your local runtime or spin up a rented instance before generating.` | No local or rented runtime is ready. |
| `Aificient Cloud is unavailable right now. Try again in a moment.` | Aificient Cloud cannot be used at the moment. |

### Quality

Two tiers are shown as labelled buttons, each with an icon and a short blurb:

- `Lite` — "Faster, lower VRAM": renders faster and runs on smaller GPUs.
- `Pro` — "Best quality": takes longer but gives the best quality.

The default depends on your account: trial accounts (welcome credits, no plan) start on `Lite`, and accounts on a paid plan start on `Pro`. You can switch either way before starting the generation.

Suggested use:

- `Lite` for previews and quick feedback, and on a 24 GB card when time matters.
- `Pro` for finished videos.

On every runtime the tier is a step-count knob, not a precision setting: `Lite` renders each clip with a few fast steps, `Pro` with many more. Any tier can run `Lite`, including an A100.

The engine decides how much of the model to keep on the card from its VRAM, so the picture for a given seed is the same on every GPU — only the time changes.

> **Cost:** On Aificient Cloud, `Pro` uses about a third more compute than `Lite` and is priced accordingly.

#### Messages You May See

| Message | What it means |
| --- | --- |
| `<GPU> has less than 23 GB of VRAM, which MiniMax-H3 cannot render on even with every block streamed. Use Cloud Render, or pick a 24 GB+ GPU (RTX 3090 / 4090 or better).` | You queued onto a card under 24 GB (a 3080, a 4070, a T4, a V100, …). The app refuses a GPU that is plainly too small. |

### Images and Audio Only

Enable this option when you want to generate only:

- Character references.
- Scene images.
- Narration.
- Sound effects.

Video rendering and final stitching are skipped.

> **Tip:** Use it to review assets before spending GPU time.

## 15. Resume Generation

`Resume Generation` is the button at the bottom of the right sidebar. It lights up amber when a project has missing or invalidated assets, and is disabled (`Project generation is complete`) when there is nothing left to do. The app reuses existing completed assets where possible and only regenerates missing or affected parts.

### When to Use It

Use `Resume Generation` after:

- Stopping generation.
- Deleting an image, audio, or video.
- Rewriting scene text.
- Editing character visuals, changing a scene's cast, or changing an outfit or a scene's assets.
- Adding a character or an asset.
- A generation failure.
- Running images/audio first and rendering video later.
- Removing a queued clip from a GPU or cloud queue, or cancelling one cloud scene while the others render.

> **Note:** A new character that is **not in any scene yet** also counts: its reference image is missing, so the button stays active even on a project whose final video is already finished, and `Images + Audio only` renders it for preview without touching the video.

### The `Generate video on` Menu

Clicking the button opens the `Generate video on` menu, which contains:

- `Generation changes pending to be saved!` — a warning shown when the `Settings` tab has unapplied changes. The render action stays blocked until you apply or discard them.
- The runtime list — `Aificient Cloud` (with tier, resolution, and estimated credits) and each ready local or rented GPU (with its queue depth). Tick one or more GPUs to split the missing videos across them, or Aificient Cloud by itself. When nothing is available the list reads `No GPU available — start a runtime to render video.`
- `Add to render queue` (or `Queue on N GPUs`) — renders the missing scene videos on the selected runtime(s). Missing images and audio are generated first automatically.
- `Images + Audio only` / `Skip video rendering` — generates missing images, character references, project assets, and audio without rendering video. It stays available while the cloud queue is busy, so a failed narration can be regenerated while clips render.

While images or narration are still missing, the `Aificient Cloud` row reads `Lite · 720p · generates the missing images/audio first` (or `Pro · …`) instead of a price. Picking it generates those assets first and queues the clips only if every one of them succeeds.

> **Note:** Like a GPU run, a failed asset stops before any clip is paid for, and the failure is in the generation report.

When every raw clip is ready and only caption burns or the final stitch remain, the button acts directly instead of opening the menu: it runs the remaining caption burns and final stitch locally, and no GPU is needed for that work. If only the final stitch is left, it is labelled `Stitch Final Video`.

On a phone the button is a floating `Resume` / `Stitch` pill beside the `Details` pill, and the menu opens as a bottom sheet. While clips render on Aificient Cloud, the floating `Cloud` pill (it opens the render queue) shrinks to its icon and count and moves left so the `Resume` pill fits beside it.

On a poster project the same menu offers a single runtime choice plus `Images only` — see "Rendering and Resuming a Poster".

#### Messages You May See

| Message | Where it appears |
| --- | --- |
| `All scene clips are ready — stitch the final video` | Tooltip of the button when only the stitch is left. |
| `N captioned clips are missing — resume local generation` | Tooltip of the button when captioned clips are missing. |
| `Some generated assets are missing` | Tooltip of the button when other assets are missing. |
| `Generate missing images, character references, and audio without rendering video` | Tooltip of `Images + Audio only`. |
| `Images, character references, and audio are already ready` | Tooltip of `Images + Audio only` when there is nothing of that kind to do. |

### Resume Beside a Live Cloud Queue

A busy Aificient Cloud queue does not hide `Resume Generation`. When at least one scene has no clip and is not in the queue — because you removed it, cancelled it, or deleted its clip — the button stays available. Its tooltip reads `N scene videos are missing and not in the cloud queue — render them while the queue runs`.

The opened menu notes `Renders only the N missing scene videos. The scenes already in the cloud queue keep rendering there; the final video is stitched once every clip is in.`

The resumed run renders only those scenes, on the cloud or the GPUs you tick. It never pays twice for a scene already queued, waits for the cloud clips, and then runs the captions and the stitch itself.

> **Note:** If a cloud job you were waiting on ends without a clip, that scene's video phase reports `The Aificient Cloud render ended without a clip`.

### Generating on Another Device

Every client — this app, the web, the iPhone app — registers the generation runs it starts, so the others can show them. Each reports its progress within each step every few seconds, so the percentage moves smoothly; the iPhone app also follows the run scene by scene on the lock screen.

If a device crashes mid-run, the scenes it held are freed within about two minutes.

While another device is generating the open project, the sidebar footer shows a sky-blue chip instead of the generate controls: `Generating on <place> N%`. The place is `<GPU name> · <device>`, `a rented <GPU> · <device>`, or `Aificient Cloud · <device>`, with a phone, cloud, or chip icon.

The project row in the left sidebar blinks like any other running project.

The chip's tooltip adds the current stage and `a new generation of this project waits until it is done.` The stages are:

- `Drawing the images`
- `Recording the voices`
- `Rendering your clips`
- `Putting your video together`

> **Note:** There is nothing to stop here: the device running it is the one that stops it. `Resume Generation` is hidden meanwhile, and starting a run anyway is refused with `This project is being generated on <place>.`

Nothing about other devices' runs is stored on this one; the list is rebuilt from the server every time the app starts.

### The 1080p Warning

When you queue scene videos at `1080p` onto a GPU that has to stream the model — any card under 40 GB of VRAM, which covers every 24–32 GB card, local or rented — the app asks first. The dialog is titled `1080p will be slow on <card>` (several cards are joined as `A, B and C`).

It explains: `It cannot hold the whole model, so every step pulls it back over PCIe — and 1080p renders twice the pixels. Expect clips to take up to twice as long, and anything past ~6 seconds not to fit at all.`

Your choices:

- `Switch to 720p` (`Switching…`) — saves the project's resolution as `720p` and then queues the same GPU selection. If the save fails nothing is queued.
- `Keep 1080p` — queues the render as selected.
- Clicking outside the dialog — cancels and queues nothing.
- `Don't ask again` — stops the dialog for good on this computer.

> **Warning:** `Don't ask again` applies to every account on this computer, and there is no setting to turn the dialog back on.

> **Note:** The dialog never appears for Aificient Cloud, for `Images + Audio only`, or for cards from 40 GB upward (L40S, A100, RTX PRO 6000, H100, H200).

### What Resume Can Run

| Work | Needs |
| --- | --- |
| Images and audio only | No ready video GPU. |
| Scene video rendering | At least one ready local or rented runtime. You can select several GPUs to split the remaining scene videos across them. |
| Aificient Cloud scene rendering | Eligible source assets, a subscription, enough credits, no more than 32 missing scenes, and supported scene lengths. It does not require your own ready GPU. |
| Missing captioned clips | No GPU. Uses saved word timings when available and burns captions locally. |
| Final stitching | The scene videos ready. It then runs locally in the desktop app without using a GPU. |
| Recovery after failure | Reruns only the missing or failed stages where possible. |

If the project already has images and audio, Resume moves directly toward video rendering once you pick Aificient Cloud or one or more of your own GPUs; if only video is missing, the app does not need to recreate the whole concept. Work sent to your GPUs is added to their render queues, so it starts even if a GPU is currently busy.

## 16. Stop Generation

When generation is active, the sidebar shows a stop/cancel action. You can usually continue later with `Resume Generation`.

Stopping generation:

- Stops the current app-side generation flow.
- Attempts to cancel active video work.
- Marks unfinished phases as cancelled.

> **Note:** This stop action is for video and asset generation. To cancel a brainstorm, story, or character request on the creation home screen, use the stop button that replaces the chat's send button (see "Stopping an In-Progress Chat Request").

## 17. Generation Error Summary

When a generation finishes and one or more parts of it failed, the canvas shows an error summary box in the top-right corner. If everything succeeds, no box is shown.

- The box starts collapsed, showing only a header such as `Generation finished with 3 errors`.
- Click the header (or its chevron) to expand the full list, and click it again to collapse it.
- Click the trash/`Clear` button next to the header to dismiss the summary for the current project.
- The box stays on screen until you clear it, or until you start a new generation or resume the project.
- The box reports results for the currently selected project. Switching projects hides it; it reappears for the project it belongs to until you dismiss it or start a new run.

### What It Shows

When expanded, the box lists every failure from the most recent finished generation, grouped into two categories:

- `Runtime tasks` — work that runs on the GPU runtime (video generation and audio alignment) plus the final stitch, which runs locally in the app.
- `API tasks` — work that runs on the cloud service, such as character images, scene images, narration, and sound effects.

Each entry shows:

- The type of generation that failed (for example, `Video generation` or `Audio`).
- The scene it belongs to, when the failure is scene-specific.
- The reason reported for the failure.

If a reason is long, it is shortened with a `Show more` link. Click `Show more` to read the full text and `Show less` to collapse it again.

> **Note:** Cancelled steps are not listed as errors. If you stop a generation, the box still reports any real failures that happened before you stopped, but not the steps that were simply cancelled.

### What To Do With It

Use the summary to decide what to fix or rerun:

- `API task` failures (images, audio, characters) — review or rewrite the affected scene or character, then use `Resume Generation`.
- `Runtime task` failures (video, alignment) — check that a GPU runtime is ready and review its logs, then use `Resume Generation`.
- Stitch failures — these happen locally. Check your internet connection and disk space, then use `Resume Generation` to retry the stitch.
- A **409 error** — the runtime is busy with a task, possibly due to a state mismatch between the runtime and the UI. Wait a few minutes and try again; if the issue persists, restart the runtime.
## 7. Creating a New Project

Click `New project` in the left sidebar to open the creation home screen in the main workspace. The sidebar stays visible, and the creation screen replaces the project canvas until you open or create a project. Clicking `New project` while a project is open deselects that project and begins a fresh creation chat when needed.

The segmented control at the top of the chat composer offers four modes, in this order:

| Mode | What it makes | Project kind |
| --- | --- | --- |
| `Story` | One video story from a clear brief, refined in chat (or five brainstormed directions first, see "Brainstorm") | History project |
| `Poster` | A few seconds of motion from a poster you already have, or from one the app designs from zero | Poster project |
| `UGC` (megaphone icon) | A creator-style ad for a product, a course or an event, from your photos, a creator and a voice | UGC ad |
| `Character` | A reusable character (image and voice) for your library | Library character |

Each mode has its own hero text, composer controls and accent colour, so it is always clear which one is active. Story is sky blue, and a Story chat that turned into a brainstorm shows `Story · Brainstorm` in its eyebrow and turns amber. UGC is rose.

Two things are shared by every mode:

- A `Skills` pill (puzzle icon) in the composer switches your saved standing instructions on for the chat (see "Skills").
- The prompt box grows with its text up to ten lines (six on a phone), then scrolls.

### Chat History

The top-right `History` control (`Chat history`) opens your previous creation chats. This is chat history, not the project list, which lives in the left sidebar.

- The dropdown is headed `Recent chats` with a count and a refresh button.
- Filter chips `All` / `Story` / `Poster` / `UGC` / `Character` narrow the list. It opens pre-filtered to the composer's current mode. The `Story` filter also lists brainstorm chats, which keep their own icon.
- Each row shows the chat's icon, title, a preview and a relative time. Hover a row for `Delete chat`.
- Empty states read `No saved chats yet` or `No chats in this mode` (switch the filter to `All`).
- On a phone the control is icon-only and the list opens as a bottom sheet.

The active conversation title appears in the top bar once the conversation has started.

### Story Mode

Use Story mode (formerly `Concept`) when you have a video idea, or only a topic. The mode's description reads `Write one video story from a clear brief and refine it in chat. Not sure yet? Ask for ideas and it brainstorms five directions first.`

Its hero reads `Describe your video and I'll draft the full script — scenes, narration and characters — ready to refine in chat and generate. Not sure yet? Ask for ideas and I'll brainstorm first.`, and the composer placeholder is `Describe your video — or ask for ideas and I'll brainstorm first.`

Typical workflow:

1. Enter your idea.
2. Choose style, duration, language and optional characters.
3. Optionally attach the products, wardrobe or locations the video must feature (see "Attaching Assets to a Story").
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

A story can be built around real things: a product you sell, an outfit a character must wear, a location that has to look a certain way, a prop. Attach their images before you send the prompt and the script weaves them into the scenes.

Later, on the canvas, they form the project's **asset base** (see "Project Assets Node (Asset Base)").

The Story composer has an `Assets` pill (image-plus icon) with an `n/8` badge. Its tooltip reads `Attach products, wardrobe or locations the video must feature. The script weaves them into the scenes.` It opens an `Assets (n/8)` panel with:

- An `Add` button and a dashed drop target: `Drop PNG / JPG anywhere, or click to browse`, with `N more · up to 20MB each` underneath.
- A list of the staged files, each with a thumbnail (click for a full-screen preview), a humanized name (`lata-cocacola_final.jpg` becomes `lata cocacola final`) and a remove `×`.

You can also drag images anywhere onto the home screen. An overlay reads `Attach to the story` with `Products, wardrobe or locations the video must feature · N more fit.` A refused drop shakes (see the messages below). There is no clipboard paste.

Rules:

- PNG or JPG only, up to 20 MB each.
- At most **8 assets per story request**.
- Assets attach on the first prompt **and** on corrections. Files you stage while refining ride the correction turn and join the plan's catalogue.
- The sent message keeps a compact row of what went with it: stacked avatars of the pinned characters, thumbnails of the attached images, and a puzzle glyph with a count when skills were on (hover it for their names; one deleted since shows as `Deleted skill`).
- Reopening a saved chat rebuilds that row from the plan. A file that is no longer in your storage keeps its slot as a placeholder with the tooltip `<name> · no longer in your assets`.
- When the service refuses an attachment, the assistant answers with a plain sentence instead of an error code (see the table below). The same sentences appear if `Create project` fails for one of those reasons.

The plan card the assistant replies with has an `Assets` block listing every asset: thumbnail, name, kind tag, a violet `AI planned` tag for ones the script invented on its own, and an amber `generated later` tag for ones that have no image yet (the app renders those at the start of the first generation run).

Each scene row in the plan also shows the asset chips it uses next to its character chips, so you can see where a product or outfit lands before rendering anything.

#### Messages You May See

These appear while you attach assets, or when `Create project` fails for the same reason.

| Message | What it means |
| --- | --- |
| `Uploading…` | A file is in flight. |
| `No room left — remove one to add another` | The panel is full. |
| `At most 8 assets can be attached to one story.` | The 8-asset limit is reached. |
| `Only N more asset(s) fit — the extras were skipped.` | You dropped more files than the free slots. |
| `Only PNG or JPG images` | The drop held another file type. |
| `The AI couldn't make out that image. Try a clearer picture, or try again in a moment.` | The service could not read the image. |
| `A project can hold at most 20 assets. Delete one to add another.` | The project's asset cap is reached. |
| `Only JPG and PNG images can be added.` | The service refused the file type. |
| `That image is over 20 MB.` | The file is over the size limit. |
| `That file is empty.` | The file has no content. |
| `That took too long. Try again in a moment.` | The request timed out. |

#### Find Inspiration

Below the empty Story composer there is a `Find inspiration` button. It expands a small showcase of four real generated videos: `Countryside promo` and `Samurai at dawn` (Cinematic), `Golden retriever` and `Weird science` (3D Disney). Each card shows a poster still, plays a short muted loop and names its artistic style.

1. Hover a card to see `Use this idea`, then click it. A matching brief lands in the composer **and** the artistic style that clip was rendered with is selected.
2. Edit the text if you like, then send it.
3. Click `Find inspiration` again to collapse the showcase.

The button fades away once your prompt runs past two lines.

> **Note:** A blank brainstorm thread (reached only from a `What's new` link) shows four topic chips you can click to seed a brainstorm instead.

#### Brainstorm

There is no `Brainstorm` switch. The **first brief of a new Story chat** decides by itself: describe a video and the assistant writes the script; ask for ideas, or send a topic or a rough direction, and it brainstorms five directions first.

Only that first message is routed this way. Corrections never are, and a chat seeded from a picked idea always writes the story.

When the assistant answers with ideas, the Story chat becomes a brainstorm chat: the eyebrow reads `Story · Brainstorm`, the accent turns amber, and the reply says `Here are five directions. Pick Write story to develop one into a script, or reply with a correction to rewrite the batch.`

Typical workflow:

1. Enter a topic or rough direction (for example "ideas for a coffee brand launch").
2. Review the five generated directions.
3. Ask for more options or corrections. The reply reads `Updated. These are the revised directions based on your latest correction.`
4. Click `Write story` on the idea you like. The app opens a Story chat seeded with that idea and writes the full script.

Starting a `New chat` from a brainstorm chat opens a fresh Story chat whose first brief decides again. Brainstorm chats are saved in the chat `History` under the `Story` filter with their own icon.

### Poster Mode

Use Poster mode to turn a still poster into a few seconds of motion. It is described in full under "Poster Projects".

Typical workflow:

1. Choose `I have a poster` (import finished artwork) or `From zero` (the app designs the poster first).
2. Attach the poster image, or describe the poster you want plus any reference images and pinned characters.
3. Set the clip duration and, for `From zero`, the aspect ratio.
4. Send the prompt and review the generated poster plan.
5. Refine the plan in chat if needed, then click `Create project`.

### UGC Mode

Use UGC mode to turn what you sell — a product, a course, an event — into a short creator-style ad. The mode's description reads `Creator-style ads for a product, a course or an event, from your photos, a creator and a voice.` It is described in full under "UGC Ads".

Typical workflow:

1. Describe what you sell, who it is for, and the offer.
2. Attach up to 6 photos of the product and of the places to film in (no people), or paste the product's page into `Product URL` and `Import` it.
3. Optionally pin up to 2 creators from your character library. The first one leads and speaks on camera.
4. Pick a `Voice`, an `Angle`, and the format, length, language and camera feel in the settings pill. Or switch on `Crazy hook` to open the ad on something impossible, and pick a `Hook idea`.
5. Send the brief and review the scene-by-scene ad plan. Refine it in chat.
6. Click `Generate`, choose `Lite`, `Pro`, or `Max`, the resolution, captions, and whether to `Generate storyboard only`, then `Start generation`.

### Character Mode

Use Character mode to create reusable characters for your library. Its hero reads `Design a character once. Reuse it across every video.` Under it the home screen shows `Your cast · N`: up to six of your library characters as tiles, with a `See all` tile that opens the library.

The composer placeholder is `Describe a character: 'A brave young woman detective with a red jacket'...`. Its controls are:

- The visual-style pill (see "Visual Style").
- A gender control offering `Auto`, `Female` and `Male`. `Auto` (the default) lets the app read the gender from your description and the reference image. Selecting a voice fixes the gender to that voice's, and the control is disabled while one is selected (`Set by the selected voice — clear the voice to choose.`).
- An `Image` pill for a reference image (`Add reference image`). Once set it reads `Reference` with a thumbnail and a clear `×`. You can also drop an image anywhere on the screen (the overlay reads `Use as the reference image` / `The character keeps this face, hair and build.`) or paste an image URL in the pill's popover.
- A `Voice` pill that opens the voice picker (see "Voice"). Once a voice is chosen the pill shows its name.

Typical workflow:

1. Describe the character.
2. Optionally set the style, gender, reference image and voice.
3. Send the message. This creates the character; when it is done the assistant replies `Created <name>. Available in your library.`
4. Refine conversationally ("older", "add a scar", "different jacket"). Every later message in the same chat is a correction that rewrites the character.

Each character gets **one reference image** (there is no turnaround or model sheet). Once created, the character can be pinned in a Story or Poster composer, or added to an existing story from the `Add character` modal's `Library` tab.

### Stopping an In-Progress Chat Request

While a brainstorm, story, poster, UGC ad or character request is being generated, the chat's send button turns into a stop button (a filled square, `Cancel generation`). Click it to cancel the request you just started.

When you cancel:

- The request stops and the chat shows a neutral `Generation canceled.` note instead of an error.
- A late or stale result is not applied after you cancel.
- If the request had already finished on the server, its real result is shown instead of being discarded.
- If the request is no longer available, the chat shows that it is no longer available.

Canceling affects only the single in-progress chat request. It does not remove previous messages, ideas, stories or characters you already created.

> **Note:** This stop button is separate from `Stop Generation` for video and asset rendering (see "Stop Generation").

### Reviewing and Editing the Generated Concept

You can change the script before you start generating. There are two ways, on two different screens of the creation flow; use either one, or both.

#### Ask the AI in the Chat

1. Stay in the Story chat conversation.
2. Type the change in natural language, for example "make scene 2 funnier", "rename the main character to Mia" or "shorten the narration".
3. Send it. The assistant rewrites the concept and the conversation updates with the result.

This is best when you want the AI to rework wording, tone or whole sections.

#### Edit by Hand on the Render-Settings Screen

1. Continue from the concept. The render-settings screen slides into the main workspace and a `Script` preview panel appears on the right.
2. Click `Edit` at the top-right of that panel. The panel switches into edit mode and the button changes to `Done`.
3. Make your changes.
4. Click `Done` to apply them and leave edit mode.

This is best for small, exact fixes, and it sits next to the render settings and the `Generate` button. Use the back arrow in the render-settings header to return to the chat.

In the hand editor you can change:

- Video title.
- Narrator voice profile (the short description of how the narrator should sound).
- Character names and descriptions.
- Which characters appear in each scene (toggle the character chips under `Characters in scene`).
- Each scene's title, description, and spoken line or script.

Notes:

- Library (global) characters and the narrator are locked in the hand editor. The panel labels them and points you to the character library to change a global character.
- Your edits, whether from the chat or made by hand, are applied to the concept that gets generated, so they directly affect the resulting video.
- This editing happens on the concept before generation. To change scenes or assets after generation, use the canvas nodes and rewrite tools (see "Editing and Regeneration").

## 8. Creation Controls

The creation controls sit in and directly below the chat composer at the bottom of the home screen. Switch modes along the composer's top edge; use the pills and segmented controls below the prompt for style, the technical settings (format, length, language), pinned characters, attachments, skills and mode-specific options.

Only the controls that mean something for the active mode are shown. Poster mode, for example, has no visual-style preset (the look comes from your prompt or the imported artwork) and no language control, but it adds a pipeline toggle and an image-attachment pill.

### The Pill Row at a Glance

The full pill row, left to right:

| Pill | Where it appears (modes) | What it does |
| --- | --- | --- |
| `Options` | Phone only | Folds several controls into a bottom sheet (see "Options Sheet (Phone)") |
| Style pill (`Style`, or the current style's short name) | Story, Character | Opens the `Visual style` picker (see "Visual Style") |
| `Assets` | Story, UGC | Attaches reference images the script must feature (see "Assets (Story and UGC)") |
| `Hook idea` or `Angle` | UGC | Picks the ad's angle, or a hook idea when `Crazy hook` is on (see "UGC Ads") |
| Poster pipeline toggle | Poster | Chooses `I have a poster` or `From zero` (see "Poster Projects") |
| `Poster image` / `Reference assets` | Poster | Image-attachment pill: the poster to import, or reference images (see "Poster Projects") |
| Settings pill | Story, Poster, UGC | Aspect ratio, target duration, narration language and camera feel in one panel (see "Settings Pill") |
| `Characters` | Story, Poster (`From zero`), UGC | Pins library characters (see "Pinned Characters") |
| `Voice` | UGC | Opens the voice picker for the ad (see "Voice") |
| Gender control (`Auto` / `Female` / `Male`) | Character | Sets the character's gender (see "Character Mode") |
| `Image` | Character | Attaches the character's reference image (see "Character Mode") |
| `Voice` | Character | Opens the voice picker for the character (see "Voice") |
| `Skills` | Every mode | Switches your standing instructions on (see "Skills Pill") |
| `Crazy hook` switch | UGC | Opens the ad on something impossible (see "UGC Ads") |
| Credit chip | Modes with a known price | Shows the price per generation (see "Credit Chip") |
| Send button | Every mode | Sends the prompt; it becomes a stop button while a request runs (see "Stopping an In-Progress Chat Request") |

### Settings Pill

The technical knobs share **one settings pill**. Its label sums them up: `30s · Auto` for a story, `3:4 · 8s` for a poster designed from zero, `9:16 · 30s · Auto` for a UGC ad. A picked language shows as its flag, and a UGC camera feel as a small glyph.

Its tooltip spells every one out (`Aspect ratio 9:16 · Length 30s · Language Spanish · Camera Auto`). The pill opens a panel with the sections the mode uses:

- `Aspect ratio` — Poster `From zero` and UGC (a story picks its ratio later, on the render-settings screen).
- `Target duration` — a slider over the mode's lengths, with the range shown above it (see "Duration").
- `Narration language` — a row that opens the language list (see "Language").
- `Camera feel` — UGC ads only (see "UGC Ads").

> **Note:** Once a plan exists in the conversation, the whole panel locks for that chat and shows the plan's values.

### Credit Chip

When the price of the current mode is known, a small `N cr` chip sits next to the send button. Its tooltip reads `N credits per generation, corrections included. Creating the project is free.`

> **Cost:** The chat turns that write or rewrite a script are what is metered, not the `Create project` step.

UGC mode shows no chip: its plan turns are metered by how much the planner writes, so there is no fixed price to show. Creating a UGC project is free as well.

### Options Sheet (Phone)

On a phone the style, poster pipeline, aspect ratio, language, gender and duration controls fold into an `Options` pill. It opens a bottom sheet titled `Options` with a row per control (`Visual style` opens the style picker), plus a `Skills` section.

In UGC mode the sheet opens with the `Crazy hook` switch, then `Angle` or `Hook idea`, `Aspect ratio`, `Camera`, `Language`, the duration slider and `Skills`.

The `Assets` and `Characters` controls (and `Voice` and `Skills` in UGC) stay in the pill row, and their popovers open as bottom sheets.

### Assets (Story and UGC)

- In Story mode the `Assets` pill attaches up to 8 PNG/JPG reference images — products, wardrobe, locations, props — that the script must feature. See "Attaching Assets to a Story".
- In UGC mode the same pill holds up to 6 photos of the product and of the places to film in, plus the `Product URL` import. See "Creating a UGC Ad".

### Visual Style

The style pill shows the short name of the current style, or `Style`. It opens a `Visual style` picker of twelve tiles, each with a one-line tagline, in this order:

| Pill name | Full name | Tagline |
| --- | --- | --- |
| `Cinematic` | Cinematic Realistic | Photoreal, filmic lighting |
| `3D Disney` | 3D Disney-style Animation | Glossy, expressive 3D animation |
| `Collage` | Editorial Collage (Vox-style) | Cut-paper news explainer collage |
| `Stickman` | Stickman Animation | Simple stick figures, flat worlds |
| `Rubber Hose` | Rubber Hose Cartoon (Cuphead-style) | Bendy 1930s toons, inked & grainy |
| `Cartoon` | Classic Cartoon (Tom & Jerry) | Bold, bouncy hand-drawn toons |
| `Anime` | Japanese Anime (Studio Ghibli) | Painterly anime warmth |
| `Pixel` | Retro Pixel Art | Crunchy retro pixel art |
| `Comic` | Comic Book / Manga | Inked panels & halftones |
| `Watercolor` | Artistic Watercolor | Soft, flowing watercolor |
| `Low Poly` | Low Poly / Geometric | Faceted geometric shapes |
| `Isometric` | Isometric Animation | Clean isometric dioramas |

`Collage`, `Stickman` and `Rubber Hose` are the newest. `Rubber Hose` draws the 1930s golden-age cartoon look that Cuphead revived: noodle limbs, pie-cut eyes, white gloves, painted backgrounds and film grain. The style affects concept writing and visual generation.

> **Tip:** You can change the style while refining a concept in the chat: pick a different style and send a correction, and the new style is applied to the refined concept. If you change it more than once, the most recent selection wins.

### Duration

The `Target duration` slider in the settings pill steps through the mode's lengths:

| Mode | Lengths |
| --- | --- |
| Story | 15, 30, 45, 60, 120 or 180 seconds |
| Poster | Whole seconds from 5 to 15 (8 by default), because a poster is a single clip rather than a set of scenes |
| UGC ad | 15 seconds to 1 minute in 5-second steps (30 by default) |
| UGC crazy hook | 10, 15, 20 or 30 seconds (15 by default) |

> **Note:** Longer videos usually mean more scenes, more assets and more render time.

### Language

The `Narration language` row of the settings pill sets the narration language. It opens a `Narration language` list with `Auto` at the top, kept apart from the rest because it is a different kind of answer, followed by the catalogue, each row with its flag and its native name:

English, Spanish, Arabic, Dutch, French, German, Hindi, Indonesian, Italian, Japanese, Korean, Polish, Portuguese, Russian and Turkish.

`Auto` is the default: the app reads the language from your brief, in this order:

1. An explicit request in the brief ("write it in Japanese").
2. The language you wrote the prompt in.
3. English, when neither says anything.

The settings pill wears the chosen flag, or the word `Auto` while it is set to detect. In a UGC ad the same setting is the language the lines are spoken in.

Language affects:

- Script text.
- Narration.
- Scene wording.
- Captions and their word timings.

> **Note:** The setting locks once a plan exists in that chat. From then on the plan card in the chat shows the script's language as a code chip (`EN`, `ES`, `JA`, …).

### Pinned Characters

The `Characters` pill (its badge counts the pinned ones) opens the `Pin characters` panel:

- A header with the pinned count (`2/3` where a limit applies) and a `Create` shortcut that jumps to Character mode.
- A `Search characters` box.
- Your library as a list of rows: thumbnail, name, and either the character's description or its type and gender.
- Pinned rows carry a check and always stay in view. The rest load ten at a time behind a `Load more · N left` button at the foot of the list.
- The empty state reads `No characters yet` / `Design one once and pin it into any story.` with a `Create a character` button. A search with no hits reads `No characters match`.

Pinned characters are included in the concept so the generated story uses them. Limits per mode:

| Mode | Limit | Notes |
| --- | --- | --- |
| Story | No limit | |
| UGC | Up to 2 creators | `Pin up to 2 creators from your library. The first one leads and speaks on camera.` The first chip carries a `Lead` tag (see "Creating a UGC Ad"). |
| Poster (`From zero` only) | Up to 3 | Each one spends a slot from the poster's shared reference budget (see "Reference Images and Characters"). |

Poster mode pins only in the `From zero` pipeline: a character has to be placed into a poster while it is being designed, and an imported poster is already finished.

In Poster mode the panel spells the budget out above the list — `Each character uses one reference-image slot · N left.`, or `Characters share the reference-image budget, and it is full — remove a reference image to pin one.` — and greys out the rows you cannot pin.

A library character remembers the visual style it was drawn in. If you pin one made in a different style from the one selected in the composer, its chip gets an amber outline and a warning icon (`Made in <style> — this project uses <style>`).

A line under the composer explains it: `<Name> was made in a different style than this project (<Style>), so it may look out of place in the scenes.`

> **Tip:** If the style mismatch matters, pick the character's own style, or make a `Project variant` later.

### Voice

When you assign a voice, the app opens the voice picker. It is reached from `Character` mode, the `Voice` pill of a UGC chat, the character editor, the `Narrator` card on the canvas, a UGC ad's character modal, or Settings. The app never names the voice provider: the voices are just "the library" and "my voices".

#### Tabs

The header has two text tabs, `Library` and `My voices` (with a count), when you can keep voices of your own; otherwise it is a plain `Voices` list.

- `Library` — the app's curated narration voices. While the server narrates on the voice library, this tab shows the multilingual narrators, or, when the picker is opened from the `Narrator` card, the voices native to the script's language. Voices you saved from the `Voice library` are listed under `My voices` instead, so each one appears once. On a server without the voice library this tab is the fixed list of thirty built-in voices.
- `My voices` — your own voices, in two sections when both exist: `Cloned` (the voices you cloned in `Settings > Voices`) and `Saved` (library voices you bookmarked in the `Voice library`). Clones native to the narration language are listed first. A clone whose model is being rebuilt carries a `Rebuilding` tag (`Rebuilt automatically the next time it narrates`) and stays selectable.

A `Clear` link at the top-right removes the selection where a voice is optional. Where a voice is required (the `Narrator` card, the default voices in Settings) there is no `Clear`.

#### Search and Filters

Above the list sits a search box (`Search voices`, or `Search your voices`) with two gender toggles folded into it. Their titles read `Female voices only`, `Male voices only` and `Show every voice`. Where the gender is fixed by the field, a static `Female voices` / `Male voices` mark is shown instead.

With no gender chosen, the list is grouped under sticky `Female`, `Male` and `Other` headers with counts. The arrow keys move between rows and `Enter` picks; the current pick is scrolled into view when the picker opens.

#### Each Row

Each row shows:

- A play button (`Play preview` / `Stop preview`, or `No preview`). Click it to hear a short preview and click it again to stop.
- The voice name.
- Trait pills: `Female` or `Male`, then the accent with its country flag, `Global` with a globe for a multilingual narrator, or the language with its flag for a clone.
- A one-line description.

The `Library` tab can also offer `Automatic` rows. In the default-voice fields of Settings there is a single `Automatic` (`The best library voice for the script's language and accent`); on the `Narrator` card there is one per gender (`The default female narrator for the language` / `The default male narrator for the language`).

A voice id the library no longer holds is also displayed as `Automatic`.

#### Footer

The footer carries `Browse thousands more voices` (compass icon), which opens the `Voice library` explorer (see "Voice Library (Explorer)"). On `My voices` it also has a `Clone` link to `Settings > Voices`.

#### Messages You May See

| Message | What it means |
| --- | --- |
| `No voices of your own yet` with `Clone your voice, or save voices from the library.` | `My voices` is empty. The `Clone a voice` button opens `Settings > Voices`. |
| `No voices match` with `Try another name or clear the gender.` | The search or gender toggle has no hits. |
| `No <Language> voices on the shelf yet.` | A language-scoped library has nothing native. The `Browse <language> voices` button opens the `Voice library` on that language. |

### Voice Library (Explorer)

The `Voice library` dialog is where you browse the full voice catalogue. It is offered while narration runs on the voice library, and it is full screen on a phone. Its subtitle reads `Every voice can narrate in any language.`

**Where:** `Browse thousands more voices` at the foot of any picker, `Browse <language> voices`, or `Explore` in `Settings > Voices`.

#### Tabs and Search

- Two tabs: `Explore` and `Saved` (with a count).
- A search box: `Search by name or style — warm, deep, calm…` on `Explore`, or `Filter saved voices` on `Saved`.

#### Filters

`Explore` has five filters. A `Clear` link appears once a filter is active, and results load thirty at a time as you scroll.

| Filter | Options | Notes |
| --- | --- | --- |
| `Language` | Every narration language, with its flag | Opens on the language of the field you came from |
| `Accent` | `Any accent` plus the accents the service offers for that language | Hidden when there are none |
| `Gender` | `Any voice` / `Female` / `Male` | Locked when the field fixes it |
| `Best for` | `Any use`, `Storytelling`, `Explainer`, `Conversational`, `Social media`, `Characters`, `Entertainment`, `Advertising` | |
| `Sort` | `Trending` (default), `Most used`, `Most added`, `Newest` | |

#### Each Row

Each row has a preview button, the name, trait pills and a `<use case> · <tagline>` line.

- Hover a row for `Use`. Click it (or press `Enter`) to pick that voice for the field you came from. The dialog closes and the voice is saved to your shelf at the same time.
- The bookmark button (`Save voice` / `Remove from saved voices`) saves a voice without picking it.

Saved voices appear under `My voices` in every picker and speak every language. Removing one from the shelf does not affect scripts that already use it. The shelf has a cap set by the service.

#### Messages You May See

| Message | What to do |
| --- | --- |
| `The voice library could not be reached.` with `Check your connection and try again.` | Click `Retry`. |
| `No voices match` with `Try another search or clear the filters.` | Change the search or clear the filters. |
| `Nothing saved yet` with `Bookmark voices while you explore; they show up under My voices in every picker.` (on `Saved`) | Your shelf is empty. Use the `Explore voices` button to find voices to bookmark. |
| `You already keep N voices. Remove one to save another.` | The shelf cap is reached. Remove a saved voice before saving another. |
| `That voice could not be saved. Try again.` | Any other save failure. Try again. |

### Skills Pill

The `Skills` pill (puzzle icon, with a count badge once any are on) sits in every mode's pill row. Its tooltip reads `Your skills: standing instructions the AI follows`, or `N skills on`.

It opens a searchable checklist of your skills, grouped by your sections. Tick up to 10 to have the AI follow them in this chat and in the ones after it. The selection is remembered on this device until you switch it off, and it is shared by every mode.

Skills are created and edited in `Settings > Skills` (see "Skills").

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

### Library Actions

The all-characters view (headed `Characters` with a count) lets you:

- Create a new character with `New character`. This closes the library and opens Character mode on the home screen.
- Search characters (`Search characters…`).
- Filter by type, by gender and by voice.
- Open details (tall portraits are framed whole, not cropped).
- Rename characters from their detail view.
- Preview images (`View image` on a card).
- Delete characters (`Delete character` on a card).

> **Warning:** The delete confirmation is headed `Delete character?` with the character's name, reads `The character and its generated reference image are removed from your library.` with a red `This cannot be undone.` line, and offers `Cancel` / `Delete character` (`Deleting…` while it runs).

When Character mode is open on an empty creation chat, the home screen also shows up to six characters from your cast; use `See all` when more are available.

### Getting a Character into the Library

- Create it in Character mode on the home screen (see "Character Mode").
- Save a project character from its canvas card with the `Library` button. It copies the character **including its reference image** into the library under a new id, and the project copy is untouched. The button reads `Saved` for a moment afterwards, and it is disabled until the character has an image (`Generate the character image first`).
- A character created in a story stays a project character until you save it this way.

### Using a Library Character

- Pin it in the Story, Poster or UGC composer before the script is written (in a UGC ad it becomes one of the creators on camera).
- Add it to an existing story from the `Add character` modal's `Library` tab (see "Add a Character to a Project"), or to a UGC ad from `Add character` > `Gallery`.
- It arrives in the project as a **global** character.

> **Note:** Library characters are treated as global references. On the canvas they show a `global` badge and cannot be edited, deleted or dressed with project assets from the project; their card offers `Project variant` instead, which gives the project its own editable copy (see "Project Variant of a Library Character").
## 11. Center Canvas

The canvas shows the project as a connected visual flow. You can pan, zoom, and use the mini-map to navigate larger projects. The `Edit with AI` bar in the bottom-right corner opens the in-project assistant (see "Edit with AI").

The node groups, left to right:

| Column | What it holds |
| --- | --- |
| Project info | The `Project` card. |
| Project assets | The asset base card, right after the project card. |
| Character references | The cast column, with `Add character` under the last card. |
| Narrator | The narrator-voice card. The script text opens from the project card. |
| Scenes | One card per scene. |
| Scene text/details | The editable scene text. |
| Images | The generated scene images. |
| Audio | The scene audio tracks. |
| Video clips | The generated scene clips. |
| Transitions | One join node between each pair of scenes, when the project has two or more. |
| Stitch | The final-video stitching status. |
| Final output | The final video. |

These node groups are the History flow. A poster project uses the same canvas with its own, much shorter chain — see "The Poster Canvas". A UGC ad has its own board — see "The UGC Board".

## 12. Canvas Nodes

Each node on the canvas is a card for one part of the project. The entries below list what each card shows, the actions it offers, and what to watch for.

### Project Info

The `Project` card shows the project name, `Ns · N scenes` with the script status icon, and the `Style` (long style text is clamped to three lines; hover for the full text). While the script is being written the status icon reads `Writing the script…`; if it fails, `Script generation failed`.

**Actions**

- `View script` — appears once the script is complete. Opens the read-only `Script` modal: `Ns · N scenes`, the `Style`, and one block per scene with its number and title, its length, its visual description, and its narration in quotes.

### Narrator

The card between the cast column and the scenes is the project's narrator voice (formerly the `Script` card; the script text opens from the `Project` card's `View script` button). Its header shows how many scenes are narrated (`N scenes`) and the script status: `Waiting for the script…` while the script is being written, or `Script generation failed`.

Once the script is ready, the card shows:

- The current voice's name, with a preview button.
- The voice's description.
- Trait chips: `Female` / `Male`, and `Global` (a multilingual voice), the accent with its flag, or the language.
- A notice box when the service switched the voice while creating the project — for example because the voice you picked does not narrate in the script's language, so the automatic voice for that language is used instead.

When the narrator is on `Automatic`, the card asks the service which library voice the narration really uses for the script's language, the narrator's gender, and (for Spanish or English) the accent set in `Settings > Audio Config > Automatic voice accent`. It shows **that** voice, with a small `Auto` tag (`Picked automatically for the language, the gender and the accent`) and a working preview.

If the lookup fails (for example offline), the card falls back to `Automatic` with `The best library voice for the script's language and accent` and no preview.

**Actions**

- `Change voice` (`Change the voice`) — a full-width button that opens the voice picker. Disabled with `Wait for the generation to finish` while a run is active.

#### Changing the Voice

1. Click `Change voice`. The voice picker opens, scoped to the script's language, with an `Automatic` row per gender and no `Clear` (see "Voice").
2. Pick a different voice. The `Change narrator` confirmation opens, headed with the voice's name and gender. It reads `The narrator will speak with <name>` (` — the default <gender> voice for the language` for `Automatic`) and says what happens to existing narration (see the messages below).
3. Click `Change and re-record` (or `Change voice` when nothing was recorded yet) to confirm, or `Cancel`.

Confirming saves the narrator. When narration existed, an images-and-audio run starts right away to re-record it.

> **Cost:** Re-recording costs the audio price times the narrated scenes; the confirmation shows the total as `About N credits.`

#### Messages You May See

| Message | What it means |
| --- | --- |
| `The narration of N scenes is re-recorded` | Narration exists. The confirmation adds `About N credits.` and `Scene images and rendered clips are kept; a clip is only re-rendered if its new narration no longer fits in it. The final video is stitched again.` |
| `No narration was recorded yet: every scene is narrated with this voice when you generate.` | Nothing is recorded yet, so nothing is re-recorded. |
| `Cannot change the narrator while a generation is running` | The change is refused while a generation is running. |
| `The narrator could not be changed.` | The change failed; the card shows this text. |

### Scene

The scene card shows the scene number, title, and duration, plus three step chips (image, audio, video) whose tooltips read `ready`, `generating`, `failed`, `skipped`, or `pending`. Under them sit two strips:

- `Cast` — one chip per character in the scene (narrator chips are marked `· narrator`), ending in an `Add cast` / `Edit cast` button.
- `Assets` — one chip per project asset assigned to the scene, ending in an `Add assets` / `Edit assets` button. The strip appears once the project has an asset base. Assets that have no image yet show as muted chips with the tooltip `<name> · pending generation`.

**Actions**

- `Add cast` / `Edit cast` — opens the cast picker (see "Change a Scene's Cast").
- `Add assets` / `Edit assets` — opens the asset picker (see "Dress a Scene or a Character with Assets").

### Description, Character Reference, and Script Nodes

These nodes show editable scene text.

**Actions**

- Click the node — opens the rewrite tools, when generation is not active.

### Project Assets Node (Asset Base)

The `Assets` card sits in its own column right after the project card. It holds the project's **asset base**: reusable reference images — a branded product, a wardrobe item, a location, a prop — that scenes and characters reference by id. The asset base exists in History (story) projects only.

#### What It Holds

When a scene image or a character image is rendered, the assigned assets are attached to the image model as visual references, so the same bottle, jacket, or storefront appears the same way in every shot. Typical uses:

- Product placement for a brand video: upload the packshot, let the script place it, then keep it in every scene where it matters.
- A character's signature wardrobe: a jacket or uniform assigned as their outfit, so it survives every regeneration.
- A real location or set (a shop front, a kitchen, a stage) that several scenes share.
- A prop that must look identical each time it appears.

Each asset is a tile with a thumbnail and its name (hover for the description):

- A dashed tile with an atom glyph is an asset that has no image yet (`pending`) — typically one the script planned. It is rendered at the start of the next generation run, before characters and scenes.
- A small `AI` corner badge marks assets the script planned on its own.
- A spinner covers a tile while that asset is being generated or updated.

The empty state reads `Products, wardrobe, locations…` / `Upload an image or create one with AI.` Finished project assets also appear in the right sidebar's `Assets` tab under `Project asset`.

#### Adding Assets

The header shows the asset count and two buttons:

- `Upload an image` (tooltip `Upload an image — it's named and described from the picture`) — a file picker for PNG/JPG images, several at a time (they upload one after another). The service looks at each picture and writes the asset's name, kind, and description itself, so the file name never names an asset.
- `Create from a prompt` (atom icon) — opens `New asset from a prompt` (`The image model renders it in the project's artistic style`), with `Name`, a `Kind` chip row (`Product`, `Wardrobe`, `Location`, `Prop`), and `What it looks like` (`A complete visual brief: shape, colors, materials, branding…`). `Create & generate` creates the entry and renders its image right away.

Uploaded assets are ground truth: they are never regenerated, so what you upload is exactly what the image model is shown. Asset changes are blocked while a task runs.

> **Cost:** Describing an uploaded picture is one small, charged AI call per image.

#### The Asset Detail Modal

Click a tile to open its detail modal, titled with the asset's name and subtitled `Planned by the script` or `Your asset`. It holds:

- The image (click it, or `View full screen`, to open the viewer) and tags: `AI planned` / `User`, the kind, and `pending` or `uploaded`.
- `Used in` — for example `Scenes 2, 4 · worn by Maya`, or `Nowhere yet — pick it from a scene card, or place it with AI below.`
- `Generate image` / `Regenerate image` — for generated assets only; uploaded assets have no regenerate button.
- `Details` — name, kind, and description (`What the models read about this asset. Editing these regenerates nothing.`). A `Save` button appears once something changed.
- `Place with AI` — describe where the asset belongs (`e.g. "show it wherever the chemist is drinking"`); the model picks the scenes (and the character, for wardrobe) and those scenes regenerate. When something changed, the generation run starts automatically.
- `Delete from project` — asks first, with `Keep it` / `Delete asset`. An unassigned asset is simply removed.

If the name or description were filled in while the modal was open, the `Details` fields update unless you had already edited them.

> **Warning:** Deleting an assigned asset also deletes the generated image and video of every scene that uses it, and everything featuring any character that wears it (including that character's image). Narration and caption timings are kept; the confirmation spells out what goes.

If scenes had the asset assigned to them directly, the app then offers to rewrite their text without it (see "Rewrite Scenes After a Delete").

#### Limits

All caps are fixed by the service and are not project settings.

| Limit | Value |
| --- | --- |
| Assets per project | 20 |
| Attachments per story request in the composer | 8 |
| Assets per scene | 5 |
| Assets per character | 3 |
| Upload formats | PNG or JPG |
| Upload size | Up to 20 MB per image |

#### Messages You May See

Upload and creation errors are plain sentences in the app's error toast. Running out of credits opens the out-of-credits card.

| Message | What it means |
| --- | --- |
| `A project can hold at most 20 assets. Delete one to add another.` | The project is at the 20-asset cap. |
| `Cannot update assets while a task is in progress` | Asset changes are blocked while a task runs. |
| `The AI couldn't make out that image. Try a clearer picture, or try again in a moment.` | The service could not describe the uploaded picture. |
| `Only JPG and PNG images can be added.` | The file is not a JPG or PNG. |
| `That image is over 20 MB.` | The file is too large. |
| `That file is empty.` | The file has no content. |
| `That took too long. Try again in a moment.` | The call took too long. |
| `The AI isn't available right now. Try again in a moment.` | The service is unavailable. |
| `Give the asset a name.` | A prompt-made asset needs a `Name`. |
| `Describe what the asset looks like.` | A prompt-made asset needs `What it looks like`. |
| `That name is too long — shorten it and try again.` | The prompt-made asset's name is too long. |
| `The image could not be added.` | Any other upload failure. |
| `The asset could not be created.` | Any other creation failure. |
| `Now in scenes 2, 3.` | `Place with AI` result: the asset was placed in those scenes. |
| `Not placed in any scene.` | `Place with AI` result: the model placed it nowhere. |
| `Its details were filled in from its image.` | Added to the `Place with AI` result when the service described the asset on the way. |

### Character Node

Each cast card shows the character's reference image, its name, badges — `narrator`, `global` for a library character, and the type (`person` / `animal` / `object`) — and its description. Click the image to open the full-screen viewer, subtitled `Character reference`.

A card whose reference image is being generated shows an active state; a new character with no image yet shows the card without artwork until its first generation run.

For project characters, an `Outfit` strip sits under the description: one chip per project asset the character wears, ending in an `Add outfit` / `Edit outfit` button. It appears once the project has an asset base.

**Actions**

- `Add outfit` / `Edit outfit` — changes which project assets the character wears (see "Dress a Scene or a Character with Assets").
- `Edit` — opens the character editor (see "Edit Character").
- `Library` — saves a copy, image included, to your character library, and reads `Saved` briefly afterwards. Disabled until the character has an image (`Generate the character image first`).
- Delete — removes the character from the project after a confirmation (`Remove character`). The confirmation names the affected scenes.
- `Project variant` — shown on a **global** (library) character instead of `Edit`, `Library`, and Delete: `Give this project its own editable copy of the character. The library entry stays as it is.` (see "Project Variant of a Library Character").

The action row is hidden while the project is generating.

A removed character leaves the script and the cast of every scene it was in. The narrator cannot be removed this way, and a library character leaves only this project. When the character was cast in any scene, the app then offers to rewrite those scenes' text without them (see "Rewrite Scenes After a Delete").

> **Warning:** Removing a character deletes its reference image and the generated image and video of every scene it was in, because they were drawn with it. Narration and caption timings are kept.

Under the last card of the cast column hangs a dashed `Add character` button (`Add a character to the script`); when the script has no characters yet it is a card of its own. It is disabled while a task runs (`Wait for the running task to finish`). See "Add a Character to a Project".

### Image Node

Shows the generated scene image.

**Actions**

- Preview fullscreen — opens the image in the fullscreen viewer.
- Retry loading — loads the image again.
- `Delete image` — `Deletes the scene image, raw clip, and final video. Use Resume Generation when you want to rebuild them.`

> **Warning:** Deleting a scene image means the dependent video assets must be regenerated.

### Audio Node

Shows the scene's available audio tracks.

**Actions**

- Play/pause — plays or pauses the track.
- Seek — jumps to a point in the track.
- Retry loading — loads the audio again.
- `Delete narration` / `Delete audio` — `Deletes narration, generated audio, raw clip, and final video. The scene image is kept. Use Resume Generation when you want to rebuild them.`

Regenerating audio can affect later video stages, because video timing depends on audio. For cloud-rendered scenes the rule is forgiving:

- If the new narration (plus the voice delay and tail) still fits inside the rendered clip, the clip is **kept**. The scene plays longer or shorter at the next stitch, with no re-render.
- Only when the new narration outgrows the clip is the clip deleted, with a warning, so the scene can be re-rendered at the right length.
- Captions' word timings and the final video are always refreshed after an audio change.

### Video Node

Shows a generated scene video clip. When captions are on, each scene has two video boxes: `raw clip` and `captioned clip`.

**Actions**

- Play/pause — plays or pauses the clip.
- Seek — jumps to a point in the clip.
- Fullscreen preview — opens the clip in the fullscreen viewer.
- Narration mute toggle (`Narration on — click to mute` / `Narration off — click to unmute`) — lets you hear the clip's own soundtrack alone.
- `Delete video` (raw clips only) — `Deletes scene video clips and final video.` Asks first (see below).
- `Cancel` — shown on a captioned clip while its caption burn is running.
- `Remove from queue` — shown while the clip is queued (see below).
- Thumbs up / thumbs down — rates the clip. A dislike can include an optional preset reason or custom comment; select the active rating again to clear it.

#### Queued Clips

While a clip is waiting in a local, rented, or Aificient Cloud render queue, the node shows a colored `Queued` badge with a small queue icon instead of its normal status icon. Once rendering starts, it switches to the normal active/progress state.

A queued clip carries a `Remove from queue` button (`Removing...` while it works). Its tooltip depends on the queue:

- GPU queue: `Takes this scene's clip out of the GPU's render queue. The other scenes keep rendering.`
- Aificient Cloud: `Takes this scene's clip out of the Aificient Cloud render queue, refunding it. The other scenes keep rendering.`

The button is not offered once the clip is rendering. A removed scene is rendered again by `Resume Generation`, which can run beside the live queue (see "Resume Generation").

#### Deleting a Clip

`Delete video` asks first: `Delete this video?` (subtitle `Scene N`) — `The video is deleted. The next Resume Generation renders it again, and the old one can't be brought back.` and `Rendering it again costs credits again.` — with `Cancel` / `Delete video`.

> **Warning:** Deleting a scene video means the final video must be regenerated.

#### Previewing a Cloud-Rendered Scene

For cloud-rendered scenes, pressing play previews the clip and its narration **together**: the voice enters after the configured voice delay, the clip's own soundtrack plays underneath at the project's `SFX volume`, and playback stops where the final video will cut the scene. What you hear, and where it ends, is what the stitched video keeps.

### Stitch Node

Shows the final video stitching status. The stitch runs locally in the desktop app (no GPU needed) as soon as every scene clip is ready; on the **web** it runs on Aificient Cloud instead.

**Actions**

- `Stitch Final Video` — the action at the bottom of the right sidebar when every required scene clip is ready but the final video is missing. Starts the local stitch without choosing a GPU.

#### What the Stitch Does

- Downloads the clips and, for cloud-rendered scenes, their narration tracks.
- Mixes each narration over its clip's own soundtrack; the model's ambience dips under the voice, scaled by the project's `SFX volume`.
- Trims each narrated scene to end a beat after its voice finishes. The rendered clip is an oversized canvas; the narration decides the scene's real length.
- Joins the scenes with the transition you set for each cut, or the project's crossfade where you set none (see "Scene Transitions").
- Writes the provenance watermark and uploads the final video to your project.

#### Steps Shown While It Runs

1. Downloading scene videos (`Downloading scene video N/M`) and, for cloud-rendered scenes, their narration (`Downloading narration N/M`).
2. Analyzing scene videos.
3. Stitching scene videos, with live progress.
4. Joining scene videos.
5. Writing the provenance watermark.
6. Uploading the final video, with real upload progress.

Scenes are normalised two at a time into segments and the crossfades are encoded separately, so a long project needs about 2.8 GB of memory at the peak for thirty 1080p scenes. The final file goes straight to storage; the upload cap is 1 GB.

#### States

| State | Meaning |
| --- | --- |
| Queued | Waiting for another local stitch to finish, or preparing to start. The node shows `Queued` with `Waiting for another render to finish` until it is its turn. |
| Waiting | Waiting to start. |
| Running | The stitch is in progress. |
| Completed | The final video is stitched and uploaded. |
| Error | The stitch failed. |
| Skipped | The stitch did not run. |

#### The Local Queue

Only one local job runs at a time; stitches and caption burns share the queue. If several projects finish rendering around the same time, their stitches queue up and run one after another. Cancelling a generation also removes its stitch from the queue.

Local stitching needs a working internet connection to download the clips and upload the result, plus temporary free disk space. Temporary files are cleaned up after the stitch finishes.

> **Cost:** On the web the stitch runs on Aificient Cloud (`Stitching on Aificient Cloud · <elapsed>`) at 0.1 credits per stitch. The server applies its own limit on scenes per stitch and shows its own message if a project exceeds it.

### Transition Node

With two or more scenes, a column of join nodes sits between the last video column and the Stitch node, one per cut. Each shows `Transition` with `N-1 → N`, the transition's icon and name, and `Hard cut` or `<Name> · <length>s` (for example `Crossfade · 0.4s`).

**Actions**

- `Change transition` (`How scene N comes in after scene N-1`) — opens the transition picker. Locked while a generation is running (`Wait for the generation to finish to change the transition`).

> **Note:** Changing a transition deletes only the final video — see "Scene Transitions".

### Output Node

Shows the final video when available. When the project has no poster image (the first scene image was deleted, or a UGC ad, which has none), the node previews the video's first frame instead.

**Actions**

- Play — plays the final video.
- Seek — jumps to a point in the video.
- Fullscreen — opens the video in the fullscreen viewer.
- Download — saves the final video.
- Thumbs up / thumbs down — rates the final video, optionally adding a reason when you dislike it.

## 13. Fullscreen Media Viewer

Images and videos can open in fullscreen, from the canvas nodes, from a character card's reference image, and from the asset detail modal.

One bar at the top-left holds the icon, the title and subtitle, and the actions; it stays on screen while the viewer is open:

- `Download`.
- `Share`.
- `Close`.

> **Note:** If sharing is not available on your system, the app falls back to copying or opening the media link.

## 14. Right Scene Sidebar

The right sidebar appears when a project is selected. For a History project it has three tabs: `Schema`, `Assets`, and `Settings`.

A poster project uses the same column with a `Plan` tab in place of `Schema` and a much smaller `Settings` form — see "The Poster Sidebar". A UGC ad has `Scenes`, `Assets`, and `Settings` tabs of its own — see "The UGC Sidebar".

### Schema Tab

The `Schema` tab is a project outline. It shows:

- Project, characters, scenes, and the final video. Clicking an item focuses the related node on the canvas.
- Scene rows: duration, asset readiness, generation status, and missing or completed stages.
- A scene whose clip is queued on Aificient Cloud is drawn as waiting, with a dashed, pulsing border.
- A scene whose clip is rendering on Aificient Cloud gets the same sky-blue glow as a scene this computer is generating.

### Assets Tab

The `Assets` tab groups generated files. Common groups:

- Scene images.
- Character images.
- Narration.
- Sound effects.
- Generated audio.
- Raw clips.
- Final video.
- Project assets (each labelled `Project asset`).
- Metadata.

From each entry you can focus the related node or download the asset.

### Settings Tab

The `Settings` tab controls project-specific video settings, in four sections: Format, Model, Audio, and Captions.

| Setting | What it does |
| --- | --- |
| Aspect ratio | `Vertical 9:16` or `Widescreen 16:9`. |
| Resolution | `720p` or `1080p`. |
| Quality | Lite or Pro. |
| Guidance values | Video/Audio CFG. |
| Speech pace | How fast the narration is spoken. |
| Voice delay and scene tail | How long the voice waits before it enters a scene, and how long the scene runs on after it ends. |
| SFX volume | How loud the video model's own soundtrack (ambience and effects) plays under your narration, in the preview and in the final stitch. Default 20%. |
| Transition duration | The length of the project's default crossfade, used at every cut that has no transition of its own (see "Scene Transitions"). |
| `Burn-in captions` | Whether captions are burned into this project's videos. |
| Caption position, font, size, and colors | The caption style, with a live `Preview` (its sample words are in the script's own language and script) and a `Reset` that returns the style to your preset. |
| `Font` | Offers only the fonts that can write the project's language — the ones made for its script first, then the Latin display fonts that also cover it — each drawn in its own face. |

If the stored font cannot write the language, the picker shows the font that will really be used and notes `<Font> has no <Language> characters, so captions use <Font>.` (see "Caption Fonts" under "Global Settings").

The sticky footer has `Discard changes` and a primary button that reads `No changes to apply`, `Apply changes`, `Applying`, then `Applied`.

> **Note:** Apply settings before rendering video. While there are unsaved changes the `Resume Generation` menu shows `Generation changes pending to be saved!` and its render action is blocked.
## 18. Editing and Regeneration

Aificient Studio lets you change individual parts of a project without starting from scratch. Some edits are manual, some are AI-assisted, and some trigger regeneration because later assets depend on the edited part. This section covers editing from the canvas after generation.

To edit the concept before generation (title, characters, scenes, scripts), continue from the creation chat to render settings and use the `Edit` button in the right-side `Script` panel (see "Reviewing and Editing the Generated Concept").

Three words come up throughout:

- **Manual edit** — you type the replacement yourself.
- **AI edit** — you describe the change you want and the app rewrites that component.
- **Regeneration** — the app recreates missing or invalidated assets and keeps completed assets that are still valid.

### Rewrite Scene Text

**Use it when:** a scene's text needs different wording. Editable fields are Description, Character reference, and Script; each can be rewritten manually or with AI.

**Steps**

1. Click the scene text node on the canvas.
2. Choose manual edit or AI rewrite.
3. Enter the replacement text or the rewrite instruction.
4. Confirm the change.
5. Regenerate the affected assets when prompted.

**What regenerates:** rewriting a field removes the generated assets that depend on it, so the project stays consistent.

- Description — usually a new image and video.
- Script — usually new narration and video.
- Character reference — usually new visuals.

### Add a Character to a Project

**Use it when:** the story needs someone who was not there at the start — a rival who appears halfway through, a mascot, a narrator's sidekick. You can add a character at any point after the project exists.

**Steps**

1. Click `Add character` under the last cast card (or the `Add character` card when the script has no cast yet). A modal titled `Add character` with the project name opens.
2. Pick one of the three tabs and fill it in (see the table below).
3. Click the tab's button. A summary card confirms the addition, with `Close` and `Regenerate images + audio`.
4. To see the character before placing them, click `Regenerate images + audio` there, or later use `Resume Generation > Images + Audio only`. The sidebar button stays active for an uncast character with no image even when the project's final video is already done, and the card shows the generation progress.
5. Cast them from the `Cast` strip of the scenes they belong in (see "Change a Scene's Cast").

| Tab | What you fill in | Button |
| --- | --- | --- |
| `Manual` | `Name`, `Gender` (None, Female or Male), `Type` (Person, Animal or Object), a `Humanized` checkbox, and a `Description` (`A stable visual identity the image model can repeat: age, build, face, hair, wardrobe and colors, distinguishing marks`). Below it, `Reference images (optional, up to 3)` — PNG or JPEG photos of the character or of what they wear | `Add character` |
| `AI` | A single `Prompt` (`Who should join the story? e.g. a rival chemist in her fifties: sharp grey suit, silver bob, rimless glasses`) plus the same reference-image strip. The model reads the whole script for context and writes the character | `Write & add` |
| `Library` | `Your library`: pick one of your library characters (ones already in the script are hidden). It arrives as a **global** character with its library image | Pick the character |

**What regenerates:** nothing now. The character is in no scene until you cast them; their reference image renders on the next run, and each recast scene regenerates its image and video on the next run.

> **Note:** There is no voice field here. Voice is only editable later, and only for the narrator.

> **Note:** Reference photos you attach are uploaded to the project asset base first and become the character's outfit references (`They join the project's assets and the character is drawn from them.`).

#### Messages You May See

| Message | What it means |
| --- | --- |
| `Nothing regenerates now. The new character is in no scene until you cast them from a scene card; their reference image renders on the next generation run.` | The modal's rule. |
| `<Name> joined the script` / `Not in any scene yet: cast them from a scene card. Their reference image renders on the next generation run, or right away with Regenerate.` | Confirmation after saving. |
| `The AI writes the character from these images; the prompt adds what they cannot show.` | `AI` tab, once reference images are attached. |
| `Every library character is already in this script.` | `Library` tab: nothing left to add. |
| `Your library is empty. Create characters from the home screen in Character mode.` | `Library` tab: no library characters yet. |

### Change a Scene's Cast

**Use it when:** a scene should show a different set of characters.

**Steps**

1. On the scene card, click `Add cast` or `Edit cast` in the `Cast` strip. The `Scene N cast` picker opens: a checklist of `Characters in this project (N in scene)` with avatar, name, and `narrator` / `library character` labels. There is no per-scene limit.
2. Tick or untick characters. As soon as the selection changes, the picker warns `This scene regenerates with the new cast`.
3. If your pick adds someone the scene did not have, or takes out someone it had, decide whether the AI should also rewrite the scene's text (see "Write Changes into the Scene"). The button then reads `Save and write in` or `Save and rewrite`.
4. Click `Save cast` (or the write-in button).

**What regenerates:** the scene's image and videos; narration and caption timings are kept. The scene's `Character Reference` text is kept in step with the new cast.

#### Messages You May See

| Message | What it means |
| --- | --- |
| `This scene regenerates with the new cast` — `Saving deletes this scene's image and videos so the next generation draws exactly these characters. Narration and caption timings are kept.` | Warning shown as soon as the selection changes. |
| `This script has no characters yet — add one from the board first.` | The project has no characters; add one before casting. |

### Dress a Scene or a Character with Assets

**Use it when:** a scene image should include specific project assets, or a character should wear them (see "Project Assets Node (Asset Base)").

Both use the same picker: a checklist headed `Assets in this project (n/max selected)` with thumbnails and each asset's description or kind, or `Pending generation` for one with no image yet. Entries are disabled once the cap is reached. Buttons: `Cancel` / `Save assets`.

| Target | Card buttons | Picker title | Limit | How the assets are used |
| --- | --- | --- | --- | --- |
| Scene | `Add assets` / `Edit assets` | `Scene N assets` | Up to 5 | Attached to the image model when the scene image is rendered. |
| Character | `Add outfit` / `Edit outfit` | `<Name> · wardrobe` (`Assets applied to this character's appearance`) | Up to 3 | Attached when the character's reference image is rendered; they travel with the character into every scene they appear in. |

**Steps**

1. Open the picker from the scene card or the character card.
2. Tick the assets you want.
3. On a scene, decide whether newly added assets should be written into the scene's text and removed ones written out of it (`Save and write in` / `Save and rewrite`, see "Write Changes into the Scene"). A character's outfit picker does not offer this.
4. Click `Save assets`.
5. Rebuild the affected images with `Resume Generation` (or `Images + Audio only`).

**What regenerates:** for a scene, its image and videos (narration and caption timings are kept); for a character, their image and the media of every scene they appear in (narration is kept).

> **Note:** Library (global) characters cannot wear project assets. Make a `Project variant` first (see "Project Variant of a Library Character").

> **Tip:** Open an asset's detail modal from the `Assets` card and use `Place with AI` to let the model decide which scenes (and which character, for wardrobe) should carry it.

#### Messages You May See

| Message | What it means |
| --- | --- |
| `This scene regenerates with the new set` — `Saving deletes this scene's image and videos so the next generation uses the new references. Narration and caption timings are kept.` | Warning in the scene picker. |
| `The character regenerates with the new wardrobe` — `Saving deletes this character's image and the media of every scene they appear in, so the next generation applies the new wardrobe everywhere. Narration is kept.` | Warning in the wardrobe picker. |
| `This project has no assets yet — add one from the Assets card first.` | The project has no asset base yet. |
| `Pending generation` | The asset has no image yet. |

### Write Changes into the Scene

**Use it when:** attaching or detaching a character or asset should also change what the scene's text says. Attaching only hands the image model a reference, and detaching only takes it away: the text may still describe it, so the next image would draw it from the words.

When your draft changes who or what the scene holds, the cast and scene-asset pickers show a card: a `New in this scene` row with a chip per addition, a `Leaving this scene` row with a struck-through chip per removal, and a switch, on by default, whose wording follows the change:

| Your draft | Switch | When on | When off |
| --- | --- | --- | --- |
| Adds only | `Write them into the scene` (`Write it into the scene` for a single asset) | `The AI rewrites the scene description and the character reference so the shot shows where they are and what happens.` | `Attached as a reference only — the scene's text stays as it is.` |
| Removes only | `Take them out of the scene` (`Take it out of the scene` for a single asset) | `The AI rewrites the scene description and the character reference without them, so the image stops drawing them from the words.` | `Detached as a reference only — the scene's text may still describe them.` |
| Adds and removes | `Rewrite the scene` | `The AI rewrites the scene description and the character reference: the new ones in, the others out.` | `The references are swapped only — the scene's text stays as it is.` |

**Steps**

1. Change the cast or the assets in the picker. The card appears as soon as your draft adds or removes something.
2. Leave the switch on. Optionally add a two-line note under `How the scene changes` (up to 600 characters). Its placeholder reads `Optional — e.g. she walks in from the left and waves`, `Optional — e.g. it sits on the table and she picks it up`, or, for a swap, `Optional — e.g. he walks in where the other one stood`.
3. Click `Save and write in` (additions only) or `Save and rewrite` (anything removed), both with the atom icon. With the switch off the button stays `Save cast` / `Save assets`.
4. Wait for the rewrite. The cast or asset list is saved first (`Cast saved` / `Assets saved`), then the modal shows `Writing into the scene` — `Rewriting the scene description and the character reference…` — and cannot be closed until it finishes. The pick is already saved at that point, so a failure never loses it.
5. Read the result. On success the new `Scene description` and `Character reference` are shown read-only, with `<name> · described from its image` for any asset the service named from its picture. Footer: `Close` / `Regenerate images + audio`.

**What regenerates:** only the scene's description and character reference are rewritten; its image and clips regenerate on the next run. No scene is added and numbering does not change.

> **Cost:** The rewrite is a charged scene rewrite (no price is shown in the picker). Nothing is charged twice if you save again while an earlier rewrite is still running.

#### Messages You May See

| Message | What it means |
| --- | --- |
| `Written into the scene` (or `Taken out of the scene` when you only removed things) | Success, for example `Ana is part of the shot now. Leo is out of it. The scene's image and videos regenerate from the new text; narration is kept.` |
| `Not written in yet` | Failure, with the reason and `The scene keeps its text, with the new references attached.` (or, when you only removed things, a note that the scene keeps its text and may still draw them from it). The note box reopens with `Leave as it is` / `Try again`. |
| `Wait for the generation to finish, then try again.` | A generation is running; wait for it to end. |
| `The AI could not rewrite the scene this time. Try again, or say how it should change.` | Retry, or add a note under `How the scene changes`. |
| `The scene still holds what you took out. Reload the project and try again.` | Reload the project and retry. |
| `The scene changed since this was opened. Reload the project and try again.` | Reload the project and retry. |
| `You're out of credits for this rewrite.` | You have no credits left for the rewrite. |
| `Scene rewriting isn't available right now.` | The service is unavailable; try later. |
| `The scene could not be rewritten. Try again.` | A general failure; retry. |
| `This scene is still being rewritten from your earlier save. Its new text shows here when it is done — there is no need to try again.` | You saved again while an earlier rewrite of the same scene was still running (typically after a network error). The card keeps the `Writing into the scene` spinner, offers only `Close`, re-reads the project for about two minutes, and switches to the success view as soon as the new text arrives. |

A full sentence sent by the service is shown as it comes.

### Rewrite Scenes After a Delete

**Use it when:** you have just deleted a project character (`Remove character`) or a project asset (`Delete asset`). The delete removes its images, but the text of the scenes it was in may still describe it, and the next scene image would draw it again from the words.

The offer appears right after the delete when the character was cast in at least one scene, or the asset was assigned directly to at least one scene (scenes that only had it through a character's outfit do not count).

**Steps**

1. Delete the character or asset. The modal `Rewrite without <name>` opens, subtitled `Scene 2` or `Scenes 2, 4`, with a `Deleted` caption over the item's struck-through chip.
2. Optionally add a note under `How the scenes change` (up to 600 characters). The placeholder is `Optional — e.g. she finishes the call alone at the counter` for a character, `Optional — e.g. her hands are empty now; she just waves` for an asset.
3. Click `Rewrite N scenes` (atom icon), or `Leave as it is` to skip. While it works the button reads `Rewriting…` with `Rewriting N scenes…`, and the modal cannot be closed.
4. Review the result. On success the title becomes `Taken out of the scenes` and each scene's new description is shown read-only. Footer: `Close` / `Regenerate images + audio` (an images-and-audio-only run).

**What regenerates:** descriptions and character references are rewritten; narration is kept. The scenes' images and videos regenerate from the new text.

> **Cost:** Each scene is a small AI edit, charged on its own.

> **Note:** If you choose `Leave as it is`, you can still clean a scene up later from its cast or asset picker, or by rewriting its text.

#### Messages You May See

| Message | What it means |
| --- | --- |
| `Their images are gone, but the text of scenes 2, 4 may still describe them, and the next image would draw them from the words. The AI rewrites each one without them.` | The modal's explanation, worded for one scene or for an asset as needed. |
| `Each scene is a small AI edit, charged on its own. Descriptions and character references are rewritten; narration is kept.` | The modal's cost and scope line. |
| `Rewritten` — `N scenes no longer describe them. Their images and videos regenerate from the new text; narration is kept.` | Success (green block). |
| `Scenes 3, 5 kept their text` — `They may still be drawn there. Try again for those scenes.` | Only some scenes failed; `Try again` retries just those. |

The failure reasons are the same as for a write-in (see "Write Changes into the Scene").

### Project Variant of a Library Character

**Use it when:** you need to edit, delete, or dress a library character inside one project. A library character on the canvas is **global**: it cannot be edited, deleted, or dressed inside the project, so every project using it stays consistent. Its card offers `Project variant` instead.

**Steps**

1. Click `Project variant` on the character card. The modal explains: `This project gets its own copy of <name>: same look, same scenes, but editable here and able to wear project assets.` and `Your library character stays untouched, and so does every other project using it. Nothing regenerates now — the scenes keep their images until you change something about the variant.`
2. Click `Create variant`. The library reference is swapped for a project character that starts from the library image.

**What regenerates:** nothing now; the scenes keep their images until you change something about the variant. If the library entry had no image, the next run renders one.

### Edit Character

**Use it when:** an editable project character should change — their identity, their look, or (for the narrator) their voice. `Edit` on the card opens the `Edit character` editor with two tabs:

| Tab | What you fill in |
| --- | --- |
| `Manual` | The portrait beside `Name`, `Gender`, `Type`, and `Humanized` (`A non-person that behaves like a person`). A `Look` section (`What the image model draws: a stable visual identity, plus the project assets the character wears.`) holds the `Description` and the `Outfit` chips. A `Voice` section appears only if this character is the narrator. Only the fields you actually change are applied. |
| `AI` | An `Instruction` (`The model rewrites this character from your note, keeping the identity details image generation relies on.`, e.g. `make her older, silver hair, add a leather jacket`) and a `Keep the current look as reference` toggle (`The current image is saved as a project asset and shown to the image model, so the rewritten character stays recognizable.`). That reference uses one outfit slot. |

On the `Manual` tab, changing the outfit is saved on its own and regenerates the character and the scenes they appear in.

The `Voice` section (`This character narrates. A new voice re-records the narration and re-renders the videos; artwork stays.`) uses the voice picker described under "Voice"; its button shows the voice's name, or `Select a voice`. A voice change is saved through the narrator, exactly like `Change voice` on the `Narrator` card.

**Steps**

1. Click `Edit` on the character card.
2. On `Manual`, change the fields you want; on `AI`, write the `Instruction` and decide whether to keep `Keep the current look as reference` on.
3. Read the editor's warning box: it says what will be invalidated before you confirm (see the table below).
4. Click `Rewrite character`, then `Confirm rewrite` on the `Confirm the rewrite` panel (`The affected visuals are deleted now and rebuilt on the next generation run.`).
5. On success the editor reads `Character updated` and offers `Regenerate images + audio`.

**What regenerates:** it depends on what you change.

| You change | What is deleted | What is kept |
| --- | --- | --- |
| A visual field (name, gender, type, humanized, description, outfit) or an AI rewrite | The character's reference image and the visuals of every scene it appears in | Narration and generated audio |
| The voice only | The narration of every narrated scene, recorded again with the new voice | Scene images, the reference image and rendered clips |
| A visual field and the voice | Both of the above | Only what both rows above keep |

> **Note:** After a voice change a clip is re-rendered later only if its new narration no longer fits inside it; the final video is stitched again.

> **Tip:** Use `Manual` for exact name, type, description, or voice changes. Use `AI` to keep the character idea but change the style, personality, appearance, or level of detail.

The footer also has a `Regenerate image` button for when the character is right but the picture is not. It changes nothing about the character: it deletes the reference image and the visuals of the scenes the character appears in, starts an images-and-audio-only run, and closes the editor.

The card shows the progress and the new image lands when the run finishes.

#### Messages You May See

| Message | What it means |
| --- | --- |
| `Visuals will be regenerated` | Warning before confirming a visual change or an AI rewrite. |
| `The narration will be re-recorded` — `The narration of every narrated scene is deleted and recorded again with the new voice; scene images, the reference image and rendered clips are kept.` | Warning before confirming a voice-only change. |
| `…and the narration of every narrated scene is re-recorded with the new voice.` | The warning's ending when a visual change is combined with a voice change. |
| `Outfit is full (n/max): remove an asset to keep the current look as a reference.` | The outfit slots are full; free one to use `Keep the current look as reference`. |
| `No reference image yet: the new look is drawn from the description alone.` | The character has no image yet, so there is nothing to keep as a reference. |
| `Global characters cannot be edited from the jamboard` | A library (global) character. Change it in the character library, or make a `Project variant`. |

### Delete Assets

**Use it when:** one generated piece is wrong and you want only that piece rebuilt. Some nodes let you delete specific assets; after deletion, use `Resume Generation` to regenerate what is missing.

| Action | Effect |
| --- | --- |
| Delete image | The scene image is removed; the video for that scene may need to be regenerated. |
| Regenerate audio | The narration is recreated. A cloud-rendered clip survives if the new narration still fits inside it, and is deleted with a warning when it does not. |
| Delete video | Asks first (`Delete this video?`), then removes the scene clip and the final video. The final video must be regenerated. |
| Delete character | The character leaves the project and every scene's cast; its reference image and the images and videos of the scenes it was in are removed. Narration is kept. The app then offers to rewrite those scenes' text without them (see "Rewrite Scenes After a Delete"). |
| Regenerate a character's image (`Edit` > `Regenerate image`) | The reference image and the visuals of the scenes it appears in are removed and rendered again immediately, images and audio only. |
| Delete a project asset | The asset is removed together with the generated image and video of every scene that uses it and everything featuring any character that wears it (including that character's image); narration and caption timings are kept. An unassigned asset is removed and nothing else changes. When scenes had it assigned directly, the app offers to rewrite them without it. |
| Regenerate character visuals | Character reference imagery and affected scene visuals may need to be regenerated. |

### Regenerate vs Resume Generation

**Use it when:** you want the app to rebuild what an edit or a delete invalidated. The app does not intentionally regenerate everything: it keeps valid completed assets and focuses on the missing or affected stages.

| Button | Use it when | What it does |
| --- | --- | --- |
| `Regenerate` | A modal or node offers it right after an edit. The write-in and rewrite results, `Rewrite without <name>`, `Add character`, and the character editor all end with `Regenerate images + audio`. | Continues from the change you just made. |
| `Resume Generation` | You have stopped generation, fixed errors, deleted assets, or generated images and audio first. | Scans the project and continues whatever is missing. |

You can also ask for any of these in plain words with `Edit with AI` (see "Edit with AI").

## 19. Project Settings

Project settings affect the selected project and can override the global defaults for that project.

| Setting | What it controls |
| --- | --- |
| Aspect ratio | The shape of the frame. |
| Resolution | The output resolution. |
| Quality | Lite or Pro. |
| Video guidance (Video CFG) | How closely the video matches the scene description. |
| Audio guidance (Audio CFG) | How closely the generated audio matches the sound description. |
| Speech pace | The pace of the narration. |
| Voice delays and scene tail | The delays around the voice and the tail of each scene. |
| SFX volume | The level of the video model's own soundtrack under the narration; default 20%. |
| Transition duration | The default crossfade at cuts that have no transition of their own. Per-cut transitions are set on the canvas (see "Scene Transitions"). |
| Burn-in captions | Whether captions are burned into the video, on or off. |
| Caption position, font, size, and colors | Where burned-in captions sit and how they look. |

**Guidance (CFG)** controls how strictly the AI follows your prompts. **Video guidance (Video CFG)** sets how closely the video matches the scene description, and **Audio guidance (Audio CFG)** sets how closely the generated audio matches the sound description. Higher values force stricter adherence to the prompt; lower values allow more creative freedom.

## 24. Scene Transitions

Every cut between two scenes can have its own transition — how the next scene comes in. Transitions exist in stories and UGC ads (a poster has only one clip), on the desktop, the web, and the iPhone app.

### Setting a Transition

- **On the canvas** — the `Transition` join node between two scenes (`N-1 → N`) shows the current one (`Hard cut`, or for example `Crossfade · 0.4s`). Click `Change transition` (`How scene N comes in after scene N-1`).
- **In a UGC scene's editor** — the `Comes in with` box in the `Scene` tab, from scene 2 on. This changes the draft and is saved with the scene (`Saved. No clip needed to change; finish the video to see the new transition.`).
- **With `Edit with AI`** — "suggest a transition into scene 4", or "use a dip to black before the last scene".

The picker (`Transition`, `Scene N-1 → Scene N`) is a grid of fourteen tiles; each plays a sample when you hover it.

| Transition | What it does | Default length |
| --- | --- | --- |
| `Cut` | A hard cut, straight to the next shot | instant |
| `Crossfade` | A soft blend from one shot into the next | 0.4 s |
| `Dip to black` | A short fade through black, for a time skip | 0.6 s |
| `Flash` | A quick white flash, for a reveal | 0.3 s |
| `Slide` | The next shot slides in | 0.4 s |
| `Wipe` | A clean edge sweeps the next shot in | 0.5 s |
| `Zoom` | Punches in to the next shot | 0.5 s |
| `Circle` | Opens from the centre like an iris | 0.6 s |
| `Dissolve` | A grainy, film-like blend | 0.6 s |
| `Pixelate` | Breaks into pixels and back | 0.6 s |
| `Blur` | A soft motion-blur swap | 0.5 s |
| `Radial` | A clock-hand sweep | 0.6 s |
| `Mono fade` | Drains to black and white, then blends | 0.7 s |
| `Squeeze` | Squeezes one shot into the next | 0.5 s |

Below the grid:

- `Length` slider — 0.2–1.5 seconds, from `Snappy` to `Smooth`, with a link back to the default.
- `Comes in` direction — for `Slide` and `Wipe` only: `From right` (default), `From left`, `From below`, or `From above`.
- With `Cut` selected the picker reads `Straight to the next shot, no overlap. Hover a transition to see it.`
- Footer: `Only the final video is rebuilt — no scene renders again.` — `Cancel` / `Apply`.

### What Changes

Applying a transition saves it at once and deletes **only the final video**: no clip, captioned cut, or storyboard is touched, and nothing is charged beyond the stitch. Rebuild the final video with `Stitch Final Video` at the bottom of the sidebar, or ask `Edit with AI` to stitch. A transition has to be shorter than both scenes it joins.

> **Note:** Transitions cannot be changed while a generation is running (`Wait for the generation to finish to change the transition`).

### Defaults

| Project kind | Default at a cut |
| --- | --- |
| Any project, first scene | Never has a transition. |
| UGC ad | A hard cut until you choose otherwise. |
| Story | The project's crossfade, whose length is the `Transition duration` setting (shown on the node as `Crossfade · <length>s`). |

Once you apply a transition to a cut, that cut keeps its own and stops following the setting.
## 20. Poster Projects

A poster project turns a single poster into a short animated clip. It has no scenes, no narration track, no captions, and no final stitch: the animation the app produces **is** the final video, and the video model generates its soundtrack.

Everything else works as in a History project. Posters live in the same project list, render on the same GPUs or on Aificient Cloud, use the same credits, and use the same canvas and right-sidebar layout.

### The Two Poster Pipelines

Poster mode has a segmented toggle in the composer with two pipelines.

| Pipeline | How it works |
| --- | --- |
| `I have a poster` | You attach finished artwork and describe how it should move. The app derives an opening frame from your poster and animates towards it. The aspect ratio comes from the image itself; reference images and characters are not used. |
| `From zero` | You describe the poster you want. The app designs the poster first, derives the opening frame from it, then animates it. You can attach reference images, pin library characters, and choose the aspect ratio. |

> **Note:** Once a plan exists in the conversation, the toggle locks for that chat. To switch pipelines, start a new poster chat.

### Writing the Poster Prompt

| Control | Pipeline | What it does |
| --- | --- | --- |
| Pipeline toggle | Both | Switches between `I have a poster` and `From zero`. |
| `Poster image` | `I have a poster` | Picks the JPG or PNG to animate. The file is uploaded to your assets folder before the prompt is sent. |
| `Reference assets` | `From zero` | Attaches JPG or PNG images that guide the design. The pill shows a `used/5` badge. |
| `Characters` | `From zero` | Pins up to 3 library characters to be placed into the poster. |
| Aspect ratio | `From zero` | `9:16`, `3:4` (default), `1:1`, `4:3`, or `16:9`. |
| Duration | Both | Whole seconds from 5 to 15, 8 by default. |

For `From zero` the prompt is required. For `I have a poster` the image is required, and the text describes the motion.

#### Reference Images and Characters

Reference images and pinned characters share **one budget of 5**. Each character counts exactly as much as an image, and characters have their own extra limit of 3.

| Example | Characters | Reference images |
| --- | --- | --- |
| Three characters pinned | 3 | 2 |
| Five images attached | 0 | 5 |

The composer shows one combined counter on the `Reference assets` pill and disables whichever side has run out of room.

> **Note:** If a plan created before this shared limit existed holds more than 5 references, the app blocks `Create project` and tells you so. Send any correction in chat and the plan comes back trimmed and ready to create.

### The Poster Plan

The reply in the chat is a **poster plan** card. It shows:

- Its title and a badge for the pipeline used.
- The imported poster, or thumbnails of the reference images and pinned characters.
- Three collapsible prompts: `Poster prompt` (only when designing from zero), `First frame prompt`, and `Video prompt`.
- Duration and aspect-ratio chips.
- The `Create project` action.

Keep typing in the chat to refine the plan ("snappier reveal", "different typography", "add light jazz music") and it is rewritten. You can attach new images with a correction; they are merged into the plan. If that pushes past the 5-reference budget, the oldest ones are dropped.

The plan that comes back is always the accurate record of what survived, so read the card rather than what you attached. The composer clears its attachments after every turn for exactly this reason.

> **Cost:** Writing a poster plan is a metered charge. The prompt-writing model reads your reference images, so more of them makes the plan cost more and take longer to produce.

### Creating a Poster Project

`Create project` opens the poster render-settings screen, with the plan preview attached beside it.

| Setting | Options |
| --- | --- |
| Aspect ratio | Read-only. It is stamped from the poster itself. |
| Resolution | `720p` (default, much cheaper) or `1080p`. |
| Mode | `Lite` (faster, smaller GPUs) or `Pro` (best quality). Trial accounts start on `Lite`; accounts on a paid plan start on `Pro`. |
| Video duration | The length of the animation. |
| Images only | Stops after the poster images and skips the animation. You can render it later from the project. |
| Runtime | Where the animation renders. A poster is a single clip, so this is a **single choice**: one GPU (local or rented) or Aificient Cloud. The Aificient Cloud row shows the tier, resolution, duration, and estimated credit cost of the current settings. |

Creating the project also **starts its generation immediately**: the button reads `Start generation`, or `Start images` when `Images only` is on. If no runtime is available, you can still create the project with images only and render the animation later.

### The Poster Canvas

The canvas shows the poster's own chain, left to right: project, assets, poster prompt, poster image, first frame prompt, first frame, video prompt, and final video.

- The references design the **poster**. The **first frame** is derived from the finished poster alone, not from the references or character faces. The animation then runs between the frame and the poster.
- An imported poster has no `poster prompt` step, so that column is closed up and the artwork sits one step after the assets box.
- The three prompt nodes are clickable and open the rewrite modal (see "Editing a Poster").
- The media nodes show the designed poster, the first frame, and the final animation, each with a progress state while it is being generated and a delete button.
- Poster previews are shown at their real proportions, so a `3:4` or `9:16` poster is not cropped to fit the node.

### The Poster Sidebar

The right sidebar of a poster project has three tabs: `Plan`, `Assets`, and `Settings`.

#### Plan

`Plan` is the outline. Click any row to centre the canvas on that node.

- `Project` and `Assets` (with a count of references).
- The three prompts: `Poster prompt` (from zero only), `First frame prompt`, `Video prompt`.
- The three generated items: `Poster image`, `First frame`, `Final video`.

Each generated item shows its state: `Not generated`, `Queued`, `Generating N%`, `Generated`, or `Failed`. For an imported poster, `Poster image` reads `Imported`.

#### Assets

`Assets` lists the poster's reference images together with whatever the generation has produced, with download and focus actions.

#### Settings

`Settings` is a poster's whole video configuration, and it is deliberately small.

- `Aspect ratio` — read-only, set by the poster.
- `Resolution` — `720p` (default) or `1080p`.
- `Mode` — `Lite` or `Pro`.
- `Video duration`.

Changes are staged until you select `Apply changes`, or discard them with the circular-arrow button. While there are unsaved changes the footer warns `Unsaved video settings` and the render action is blocked, because a render always uses the **saved** settings.

> **Note:** None of the History settings (captions, guidance scales, speech pace, voice delays, transitions) exist for a poster.

#### Sidebar Footer

The footer holds the same actions as a History project:

- `Stop Generation` while a run is active.
- An `Aificient Cloud` status chip while the clip is in the cloud queue.
- A `Generating on <place> N%` chip while another device is generating the poster. Starting a generation here then fails with `This project is being generated on <place>.`
- Otherwise, the `Resume Generation` menu.

### Rendering and Resuming a Poster

`Resume Generation` on a poster offers two actions:

- A **single** runtime choice (one GPU, local or rented, or Aificient Cloud, with its estimated credit cost) and `Add to render queue` to render the animation. Missing poster images are regenerated first automatically, so this is the "finish the poster" action.
- `Images only`, which fills in the missing poster and first frame without rendering the animation. These are cloud tasks and need no GPU.

The action is disabled once everything has been generated.

GPU renders join the same per-GPU queue as History scene videos, so a busy GPU is still a valid choice. Cloud renders appear in `Generation assets > Aificient Cloud` alongside History jobs. Either way the finished clip lands as the project's final video; there is nothing to burn or stitch afterwards, so the project completes when the clip is delivered.

> **Note:** If you close the app while a poster render is in progress, reopening the project reattaches to it and the sidebar and canvas pick the progress back up.

### Editing a Poster

Click any of the three prompt nodes on the canvas to rewrite it. Type the replacement yourself, or describe the change and let the AI rewrite it. This is the same modal used for scene text in a History project.

Editing a prompt invalidates everything downstream of it. The modal spells out exactly what will be deleted **for this project as it stands today**.

| Prompt you rewrite | What is deleted | What is kept |
| --- | --- | --- |
| Poster prompt | The poster image, the first frame, and the animation | — |
| First-frame prompt | The first frame and the animation | The poster |
| Video prompt | The animation | Both images |

If nothing has been generated from that prompt yet, the modal says so and the edit only updates the plan. After a rewrite that removed images, `Regenerate images` in the modal refills them straight away. The animation is rendered from the sidebar's `Resume Generation` menu, where the runtime choice lives.

#### Deleting Generated Media

The delete buttons on the media nodes cascade the same way. Each button's tooltip states what it takes with it.

- Deleting the poster also removes the first frame and the animation.
- Deleting the first frame also removes the animation.
- Deleting the animation leaves both images.

> **Warning:** Deleting the animation asks first (`Delete this video?`, subtitled `The animation`, with `Cancel` and `Delete video`). Deleting the poster or the first frame does not ask.

`Edit with AI` works on a poster too. Ask it to rewrite a prompt, regenerate the poster or the first frame, change the tier, resolution, or length, estimate the animation's cost, or render it (see "Edit with AI").

### What Posters Do Not Have

- **Captions.** There is no narration track to transcribe, so there is no caption step and no captioned-clip column.
- **Stitching.** A poster is one clip; the render is the final video.
- **Publishing.** The `Publish` dialog is available for History projects only.
- **Scene tools.** No scene list and no character node editing inside the project. A poster's characters come from your library at plan time.
- **Transitions.** There is only one clip, so there is nothing to join.

### A Note on Poster Reference Images

Poster reference images stay in your **assets folder**; they are not copied into the project. The same image can therefore back several posters.

> **Warning:** Deleting an image from your assets breaks every poster that references it. The app tells you the reference is no longer in your assets folder; attach it again in a chat correction to continue.

## 22. Edit with AI

`Edit with AI` is an assistant that edits the open project for you. Tell it what to change in plain words ("regenerate the image of scene 2", "make scene 3's narration more dramatic", "add a proof scene after scene 3", "turn captions on with a bold font").

It runs the same actions the canvas buttons run, then tells you what it did. It also answers questions about the project. It works in story, poster, and UGC projects, on the desktop, the web, and in the iPhone app.

> **Note:** It is not the Support Assistant. `Ask AI` (top-right) answers questions about the app from this guide and never changes anything. `Edit with AI` works only on the open project, changes it, and can spend credits.

### Opening It

**Where:** the `Edit with AI` bar in the bottom-right corner of the canvas, once a project is open. On a phone the bar sits just above the `Details` pill.

1. Click the bar, or press `Ctrl+K` (`⌘K` on a Mac; the bar shows the shortcut). Focused, it reads `Ask AI to change anything…`.
2. Type a request and press `Enter` to send it and open the window. `Enter` on an empty bar just opens the window; `Esc` clears the bar.
3. The window grows from the corner, titled `Edit with AI` with `Story · <name>`, `Poster · <name>`, or `UGC ad · <name>` under it. On a phone it opens as a bottom sheet.

Window controls:

- Drag its top or left edge (or the corner) to resize it; the size is remembered.
- `New chat` clears the conversation.
- The close button or `Esc` hides the window and keeps the conversation.

An empty window suggests a few requests for the project type, for example `Regenerate the image of scene 2`, `Make the motion slower and more elegant`, or `Draw the storyboards of every scene`.

### Talking to It

Type in `Tell me what to change…` and press `Enter`. A message can be up to 4000 characters and can ask for several things at once ("the image of 2 and the narration of 3 and 5").

While it thinks it shows `Thinking…`; while it works, `Working on the project — you can keep using the board.` `Stop` cancels the current turn; anything already produced is kept.

Under each answer a timeline lists every action it ran in plain words, with a failed step in red and its reason. Examples: `Reading scene 3`, `Rewriting the narration of scene 3`, `Adding a scene at position 4`, `Changing the narrator voice`, `Turning captions off`, `Estimating the render cost`, `Rendering the missing clips`, `Setting the transition into scene 4`.

The conversation is kept per project for as long as the app is open: switching projects keeps it, quitting clears it.

### What It Can Do

#### Stories

- Read a scene or the whole story.
- Rewrite a scene's narration, description, or character action.
- Regenerate the images or narration of several scenes.
- Add a scene written from a brief at any position, delete scenes, or reorder them.
- Change a scene's cast or assets.
- Create an asset, dress a character, or place an asset ("Ana buys the watch instead of the stone in scene 3").
- Add, edit, or remove a character (never the narrator, never a library character).
- Change the narrator's voice.
- Set the speech pace.
- Change video settings, captions, and caption style.
- Generate captions.
- Estimate the cost and render the missing clips.
- Stitch the final video.
- Suggest and set transitions.
- Suggest voices.
- Stop a generation.
- Rename the project.

#### UGC Ads

- Read and rewrite scenes.
- Set exact scene fields and on-screen texts.
- Add (up to 10), delete, or move scenes.
- Edit the product facts.
- Draw storyboards.
- Read the lines again or change the ad's voice.
- Regenerate a generated reference image (never your own photos).
- Change the render settings.
- Estimate and render.
- Delete one scene's clip.
- Suggest or set transitions.
- Suggest voices.
- Stop a generation.
- Rename the project.

#### Posters

- Read the plan.
- Rewrite the poster, first-frame, or video prompt.
- Regenerate the poster, the first frame, or the animation.
- Set the tier, resolution, and length.
- Estimate and render the animation.
- Stop a generation.
- Rename the project.

#### Suggestions, Confirmations, and Refusals

Suggested voices come as cards with a play button and `Use`; suggested transitions come as cards with a hover preview and `Apply`. Clicking either sends that choice as your next message.

Before anything costly or destructive, it tells you the estimate and waits for you to agree in the chat:

- Rendering video.
- Changing the narrator's or the ad's voice (which re-records every line).
- Deleting a scene that has a finished clip.
- Removing a character.
- Deleting a UGC clip.

> **Cost:** Media it triggers costs exactly what the same action costs from the board. Video it renders always goes to **Aificient Cloud**, never to your own GPUs.

Anything that changes media is refused in three situations, and the assistant says which one applies:

- A run is active in this app.
- Another device is generating the project.
- A task is running on the project.

#### Messages You May See

| Message | What it means |
| --- | --- |
| `The assistant declined this request.` | The assistant refused to carry out the request. |
| `The assistant is not available right now.` | The assistant cannot be reached at the moment. |
| `No connection. Check your network and try again.` | Your network connection is down. |
| `The assistant could not answer.` | The turn ended without an answer. |

Where it helps, the error offers `Try again`. Running out of credits shows the usual out-of-credits message.

### Skills in the Assistant

The assistant follows your skills too. Its own `Skills` control in the composer's hint row starts with the skills the project was planned with (or, if none were recorded, the composer's selection). Toggling skills here never changes the composer's selection. See "Skills".

## 23. Skills

A **skill** is a standing instruction the AI follows in every chat where you switch it on: your tone, your structure, what to avoid. For example: "always open with a bold question, speak like a friend, keep sentences short, end with a call to action to my site".

Write it once and switch it on from the `Skills` pill in any composer (Story, brainstorms, Poster, UGC, Character) and in a project's `Edit with AI`. Skills belong to your account, so they follow you to every device, the iPhone app included.

**Where:** `Settings > Skills` (puzzle icon).

### Managing Skills

The page lists your skills under a `Skills` heading with an `n/50` count, a `New section` button, and a `New skill` button.

Its explanation reads `Standing instructions the AI follows in every chat — your tone, your structure, what to avoid. Switch them on from the Skills pill in the composer and in a project's assistant; they apply to stories, posters, UGC ads and characters alike.`

With no skills yet, two tiles offer `Create your first skill` and `New section`.

#### Creating a Skill

The form reads `Describe it in your own words; the AI writes the instructions and a name.`

1. Click `New skill`.
2. Optionally type a `Name` (the field reads `Name — optional, the AI suggests one`) and pick a section.
3. Describe the skill in your own words.
4. Click `Create skill` or press `Ctrl+Enter`. The page shows `Writing your skill…` while the AI writes it, and the skill is saved at once.

> **Cost:** Writing a skill costs a small amount of credits. Without enough, you see `Not enough credits to write the skill.`

#### Editing and Deleting a Skill

1. Open the skill with **Edit**. It shows the skill's `Name` and its instructions (`The instructions the AI follows.`) for you to edit by hand.
2. Click `Save` or press `Ctrl+Enter`. It saves exactly what you typed.

`Delete` asks once more (`Delete?`) before removing the skill.

#### Sections

Sections group skills under a name and an icon (`UGC`, `Brand`, `Kids`…). They only organise the list; the AI never sees them. Skills without a section are listed under `No section`.

1. Click `New section`.
2. Type a name and pick one of 48 icons.

Hover a section heading for its actions:

- `New skill in this section`
- `Rename or change the icon`
- `Delete the section (its skills stay)`

#### Limits

| Limit | Value |
| --- | --- |
| Skills per account | 50. At the limit: `You have reached the number of skills your account can keep.` |
| Sections per account | 20 |
| Skill name | Up to 60 characters |
| Instructions | Up to 4000 characters |

### Switching Skills On

1. Open the `Skills` pill in a composer or in a project's `Edit with AI`. A checklist opens.
2. Find a skill with `Search skills` (it searches names, instructions, and section names) or with the section filter.
3. Tick up to 10 skills.

The picker's strings:

| Element | What it shows |
| --- | --- |
| Tick limit | `Up to 10 skills at once` |
| Footer | `None on`, `N on`, or `N on · up to 10` |
| Link to Settings | `Manage skills ↗` |
| Empty state | `A skill is a short note the AI follows in every generation: your tone, your structure, what to avoid. Write one once, switch it on here.` and a `Create a skill` button |

#### How the Selection Behaves

- The selection is one per device, shared by every mode, and remembered until you switch it off.
- You can change it mid-chat; corrections carry the current selection.
- A sent message shows a puzzle glyph with the number of skills it used (hover for their names).
- A project remembers the skills its chat used, and its `Edit with AI` starts with those switched on.
## 21. UGC Ads

A UGC ad is a short, creator-style ad for something you sell: a product, a course, an event. The planner writes it as one to ten short scenes, each with a beat (`Hook`, `Problem`, `Reveal`, `Demo`, `Benefit`, `Proof`, `Twist`, `Call to action`) and each showing product b-roll, a creator talking to camera, or the creator with the product. You refine the plan in chat, then render it on Aificient Cloud.

**Where:** the `UGC` mode on the creation home screen.

Each scene is rendered by a reference-to-video model (Seedance) from your photos, the creator's portrait, and the voice's own reading of the scene's line, so the creator lip-syncs to exactly those words. The clips are then captioned (if you want), given any on-screen texts you add, and stitched into the final ad.

| Compared with… | Difference |
| --- | --- |
| A story (History) | No visual-style preset, no scene images, and no narrator or narration mix: each spoken line is read first and the clip is rendered to it. Rendering happens on Aificient Cloud only. The planner never writes on-screen text; you add texts per scene in the project. |
| A poster | A poster is one 5–15 second clip. A UGC ad has several scenes, dialogue, a creator, and a voice, and is stitched like a story. |

**Crazy hook** is a switch inside UGC mode, not a separate mode: the ad opens on something impossible, an absurd event filmed like real footage, that reveals what you sell. A crazy hook is still a UGC ad, with the same project list (`UGC ads`), the same board, and the same sidebar. Only its name (`Crazy Hook`), its planning controls, and its lengths change.

UGC mode is available on the desktop, on the web, and on a phone, where the composer's knobs move into the `Options` sheet. If the server does not offer it yet, the chat says `UGC ads aren't available on this server yet.` If rendering is not available, it says `UGC rendering isn't available right now. Try again later.`

### Creating a UGC Ad

1. Pick `UGC` in the mode picker on the creation home screen.
2. Describe what you sell, who it is for, and the offer. Or paste the product's page in the `Assets` panel and let the app read it.
3. Attach up to 6 photos with the `Assets` pill, and mark the real places to film in as locations.
4. Pick an `Angle`, or switch on `Crazy hook` and pick a `Hook idea`.
5. Set the format, length, language, and camera feel in the settings pill.
6. Pin up to 2 `Characters` and pick a `Voice`.
7. Send the brief. The plan card appears in the chat (see "The Ad Plan").

#### The Home Screen

The hero reads `Turn what you sell into a creator-style ad.`, with the subtitle `Describe your product or service and the offer, attach a few photos, and pick a creator and a voice. I'll write a short scene-by-scene ad you can refine in chat before rendering — or switch on Crazy hook to open it on something impossible.` The placeholder is `Describe what you sell — a product, a course, an event — who it's for, and the offer…`.

With `Crazy hook` on, the eyebrow reads `UGC · Crazy hook`, the title `Open your ad on something impossible.`, and the placeholder `What you sell and who it's for — we'll invent the chaos…`.

The pill row, left to right: `Assets`, `Angle` (or `Hook idea` with Crazy hook on), the settings pill, `Characters`, `Voice`, `Skills`, and the `Crazy hook` switch. There is no `Find inspiration` showcase and no credit chip in this mode.

#### Photos and Locations

The `Assets` pill (`n/6` badge) holds the photos the ad is built from. Its tooltip spells out the rule: `Up to 6 photos, no people: clear shots of what you sell (a product keeps its label, colours and packaging) and of the real places to film in — mark those as locations. Creators come from your characters.`

- Up to **6 photos**: of what you sell and of the real places to film in.
- **No people.** Everyone on camera comes from your characters.
- PNG or JPG only, up to 20 MB each.
- Product photos and locations share the 6 slots; marking one as a location costs nothing extra.
- When the plan turns out to sell a service, the hint changes to `Optional — up to 6 photos, no people: the venue or the classroom (mark those as locations) and the materials, like a workbook or the course on a laptop. The teacher or host comes from your characters.`

The panel (`Assets (2/6 · 1 location)`) has an `Add` button, a drop target (`Drop PNG / JPG anywhere, or click to browse`, `N more · up to 20MB each`), and the staged photos. Each photo shows a thumbnail, its name, a `Location` toggle (map-pin icon), and a remove `×`.

The `Location` toggle marks a photo as a place:

- `Use as a location: a place the ad is filmed in, not a product.` marks it.
- `A location: a place the ad is filmed in. Click to use it as a product photo again.` undoes it.
- In the tray above the prompt a marked photo carries a `Location` strip, and the sent message labels it `<name> · location`.

You can also drop photos anywhere on the home screen (`Add photos` / `Up to 6 photos of the product and its places, no people · N more fit.`).

#### Photo Messages

| Message | What it means |
| --- | --- |
| `Only PNG or JPG images are accepted.` | The file is another format. |
| `Image exceeds the 20MB limit.` | The file is larger than 20 MB. |
| `At most 6 photos can be attached.` | The 6 slots are full. |
| `Only N more photos fit — the extras were skipped.` | N of the dropped photos were added; the rest were skipped. |

#### Importing a Product Page

1. Under the photo list, paste the product's own page into `Product URL` (for example `https://shop.com/product`). The hint reads `Paste the product's page: its name, details and photos are read for the ad.`
2. Click `Import`. It reads `Reading…` while it works.
3. The page's name, brand, price, description, key points, offer, and photos are read. The AI picks the photos that clearly show the product, and they fill whatever room is left of the 6.

After an import the product shows twice: as a card in the `Assets` panel, and as a chip above the prompt with a fanned photo deck. The card shows the main photo, the name, `brand · price · site`, the description, the key points, the offer, and the other photos, with a `×` (`Remove the product and its photos`). Click either to open the product.

- While a product is staged, photos cannot be marked as locations.
- With a product staged and no plan yet, you can send without typing anything; the chat shows `An ad for <product name>`.

#### Import Notices

| Message | What to do |
| --- | --- |
| `No usable photos on the page — upload some, or the ad generates them.` | Upload photos, or let the ad generate them. |
| `None of the page's photos clearly shows the product — open the product to pick the ones to use.` | Open the product and pick the photos to use. |
| `The page's photos didn't fit — remove a staged photo to make room.` | Remove a staged photo to make room. |
| `Only N of the page's M photos fit.` | The rest were left out. Open the product to change which photos are used. |
| `The page contained hidden text aimed at AI; it was ignored.` | Nothing; the hidden text was not used. |

#### Import Errors

Imports are limited to 20 per hour per account; past that, wait a little and try again.

| Message | What to do |
| --- | --- |
| `That doesn't look like a web address. Paste the product page's link (https://…).` | Paste the full link, starting with https://. |
| `That address can't be read: only public web pages on standard ports are allowed.` | Use a public page on a standard port. |
| `The shop didn't answer. Some large shops don't let apps read their pages — try the same product on the brand's site or another shop, or upload the photos instead.` | Try the brand's site or another shop, or upload the photos. |
| `The page wasn't found (404). Check the link.` | Check the link. |
| `This shop blocks apps from reading its pages. Try the same product on the brand's site or another shop, or upload the photos and describe it instead.` | Try the brand's site or another shop, or upload the photos and describe the product. |
| `That link isn't a web page.` | Paste a link to a web page. |
| `The page is too large to read.` | Upload the photos and describe the product instead. |
| `The page has no readable content.` | Upload the photos and describe the product instead. |
| `This looks like a list of products, not one product. Open the product you want and paste its own page.` | Open the product and paste its own page. |
| `The page could not be read.` | Try again, or upload the photos and describe the product. |

#### The Product Modal

Clicking the imported product opens `Product`, with the site as subtitle.

| Section | Fields | Limits |
| --- | --- | --- |
| `Photos · X of Y` | Every photo found on the page; click one to add it or take it out. The first selected photo carries a `Main` badge. | A photo that cannot fit says `No room left for photos — take one out first` |
| `Product` | `Name`, `Brand`, `Price`, and `Offer` (for example `-20% this week, free shipping…`) | `Name` is required, up to 80 characters (`Give the product a name.`); `Offer` up to 160 characters |
| `Description` | One text field | Up to 400 characters |
| `Key points · n/5` | One line per point, with `+ Add` and a remove `×` per point | Up to 5, 120 characters each |

Each section carries a hint:

- `Photos · X of Y` — `Every photo found on the page. The AI picked the ones marked; click a photo to add it to the ad or take it out. The first one is the main shot.`
- `Product` — `What the ad calls it, and what it costs.`
- `Description` — `One or two plain sentences: what it is, who it's for, the problem it solves.`
- `Key points · n/5` — `The facts the ad leans on. Short phrases sell best.`

A footnote reads `Read from <site>. The ad is written from these facts only: no price or offer that isn't here, and no links.` The footer has `Remove product`, `Cancel`, and `Save`.

#### Angle

The `Angle` pill (ads only) chooses the approach. Once a plan has an angle the pill shows it (`… From the plan.`), and you can change it with any correction.

| Choice | Hint |
| --- | --- |
| `Auto` | The planner picks (`Angle: the planner picks the approach.`) |
| `Problem → solution` | Name the pain, then the product fixes it |
| `Testimonial` | An honest review after real use |
| `Unboxing` | First look: open it, react, show the details |
| `Before / after` | — |
| `3 reasons` | One per beat |
| `Day in the life` | — |
| `POV` | A first-person moment the viewer steps into |
| `Demo` | Show exactly how it works, step by step |

#### Crazy Hook and Hook Idea

The `Crazy hook` switch (comic-burst glyph) reads `Open on something impossible: an absurd event, filmed like real footage, that reveals what you sell`. It hides `Angle` and `Camera feel`, shows `Hook idea`, and switches the lengths to 10, 15, 20, or 30 seconds. Flipping the switch on a correction switches the existing plan's format.

`Hook idea` offers:

- `Surprise me` — the default; the planner invents the event.
- `Delivery chaos`, `Falls from the sky`, `Giant product`, `Force of nature`, `Animal heist`, `Explosive reveal`, `Impossible physics`, `Trick shot`, `Chain reaction`, `Hidden-camera prank`, and `Time warp` — each with a one-line hint.

#### Format, Length, Language, and Camera Feel

The settings pill (`9:16 · 30s · Auto`) holds four settings. All four lock once the first plan exists.

- `Aspect ratio` — `9:16` (default), `1:1`, or `16:9`.
- `Target duration` — 15 seconds to 1 minute in 5-second steps (30 by default). A crazy hook offers 10, 15, 20, or 30 (15 by default).
- `Narration language` — the language the lines are spoken in; `Auto` reads it from your brief.
- `Camera feel` (ads only) — see the table.

| Choice | Hint |
| --- | --- |
| `Auto` | Picks the camera for each scene (default) |
| `Handheld` | Selfie and handheld shots |
| `Mixed` | Handheld people, steady product |
| `Static` | Tripod and top-down, no shake |

#### Creators and Voice

- `Characters` — `Pin up to 2 creators from your library. The first one leads and speaks on camera.` The first chip carries a `Lead` tag. Pinning is optional: with nobody pinned, the planner invents a creator (shown on the plan as `New creator`). More than two: `At most 2 characters can appear in one ad — the first one leads.`
- `Voice` — the voice every line is spoken in, picked from the usual voice picker. By default it is the lead character's voice, then the plan's. Its tooltip says where the current one comes from: `Voice: <name>, from <lead name>.`, `Voice: <name>, from the plan.`, or `Voice: none picked — the lead's voice, or your default voice.`

#### Sending the Brief

Send is enabled once you describe what you sell, or a product page is staged. While the planner works, the chat shows `Writing the ad` (`Inventing the hook` for a crazy hook), and the send button becomes a stop button.

If something blocks sending, the button's tooltip says what:

| Message | What to do |
| --- | --- |
| `Describe what you sell, who it's for, and the offer.` | Type the brief. |
| `At most 6 photos can be attached — remove N.` | Remove N photos. |
| `At most 2 characters can appear in one ad — the first one leads.` | Unpin a character. |
| `At most 10 references can be attached and each character counts as one — remove a photo or a character.` | Remove a photo or a character. |

### The Ad Plan

The reply reads `Here's the ad plan. Refine it in chat, or generate the video when it looks right.` (`Here's the crazy hook. …`), followed by the plan card. The card is read-only and shows:

- An `Ad` or `Crazy Hook` eyebrow and the title, with chips for the angle, the total length, the format, and the dialogue language (flag and code).
- For a crazy hook, a `Hook` block: the hook idea, the event, `Reveal …`, and `Twist …`.
- The product: up to four photos (a sparkle marks one that will be generated), the name (`Untitled product` / `Untitled service` if none), the offer and call to action, and a `Details` toggle for the description and key points.
- Who and where: the creators (or `No one on camera`), the voice with a preview button (or `No dialogue`), and the locations with thumbnails.
- `Scenes · N` with the total length. Each row shows its number, beat, location, the spoken line in quotes (or what happens), a sound cue on crazy hooks, and its seconds. `N images are generated when the project is prepared.` notes images that do not exist yet.
- A footer with `Video ≈ X cr` (`Estimated from the scene lengths at the default quality. You choose quality, resolution and captions next.`) and the `Generate` button (clapperboard). Older cards in the chat have `Generate` disabled.

Keep typing to refine the plan; the placeholder reads `Refine the ad: punchier hook, add a demo shot, shorter lines, a different offer…` (`Refine the hook: a bigger event, a faster reveal, a different twist, a louder reaction…`). A correction can bring new photos or locations, a new cast or voice, a new angle or hook idea, the Crazy hook switch, or a newly imported product page, always with some typed text. The reply reads `Updated. The ad plan reflects your latest direction.`

> **Warning:** If new photos would push past 6, the composer warns first: `The ad keeps at most 6 photos — sending these drops one from the plan (location photos first, the oldest first).`

`Generate` checks the plan first and refuses when something is off:

| Message | What to do |
| --- | --- |
| `This plan has no product yet. Send a correction naming it.` (for a service, `This plan doesn't name the service yet. …`) | Send a correction that names the product or service. |
| `This plan has no scenes yet.` | Send a correction. |
| `This plan has N scenes and the limit is 10. Send a correction to shorten it.` | Send a correction to shorten it. |
| `This plan has N references and the limit is 10. Send any correction to trim it.` | Send any correction. |
| `This plan has N photos and the limit is 6. Send any correction to trim it.` | Send any correction. |
| `This plan happens in N places and the limit is 6. Send a correction to merge some of them.` | Send a correction to merge some places. |

### Video Settings for a UGC Ad

`Generate` slides in `Video settings`, with the plan beside it on large screens under `The plan`. The back arrow, `Back to chat`, returns to the chat.

| Setting | Options | Notes |
| --- | --- | --- |
| `Format` | For example `9:16 · 30s` | `Set by the plan.` Read-only. |
| `Quality` | `Lite`, `Pro` or `Max` | A UGC ad **always starts on Lite**, on every plan. `Lite renders fastest, at 720p.`, `Pro moves more naturally, up to 1080p.` and `Max gives the best motion and detail.`, each followed by the video estimate. |
| `Resolution` | `720p` or `1080p` | `1080p` is for Pro and Max (`Pro or Max. Lite renders at 720p.`) and is delivered as HEVC, with larger files. |
| `Captions` | On or off | `Burned in with your usual caption style.` Starts from your global captions setting. |
| `Generate storyboard only` | Off by default | `Every scene is sketched in four panels (≈ X cr). Stop there to check them before any video, then render from the project.` |

The button reads `Start generation` (or `Create storyboards` with `Generate storyboard only` on), with a summary such as `9:16 · 30s · Lite · 720p · Captions · ≈ X cr`. There is no runtime choice: UGC ads render on Aificient Cloud.

> **Cost:** The estimate covers the video plus one storyboard per scene (or only the storyboards). Generated reference images and the reading of the lines are charged separately.

Starting creates the project (it appears under `UGC ads` in the sidebar and opens on its board) and starts its first run at once. See "Generating and Resuming a UGC Ad".

### The UGC Board

The board runs left to right: the project card, the characters, the `Assets` card, the scene cards, their storyboards, their clips, the finished cuts (only when captions are on or some scene has texts), the transitions (with two or more scenes), the `Stitch` node, and the `Output`. The canvas selects; a modal edits. Click a scene card to open the scene editor, or a character or asset tile to open the asset modal. The `Edit with AI` bar sits in the bottom-right corner.

#### Project Card

`Project`, the ad's title, `<N>s · <N> scenes`, and under a `Style` heading the kind and product (`UGC ad · <product>` or `Crazy Hook · <product>`).

#### Character Cards

One per person on camera, the lead first (at most 2). Each shows the portrait (click for full screen), the name with a source chip, the scenes they are in (and `N photos` beside them when the person has two pictures), and a description. The lead's card also shows the ad's voice: a preview button, the voice's name, and its gender and accent. The voice is changed from the lead's `Edit` modal (see "Voice and Spoken Lines").

| Element | States |
| --- | --- |
| Portrait | `Not generated yet` with an atom icon until it is drawn; `Generating…` while it is |
| Source chip | `Library`, `Invented`, or `Your photo` |
| Scenes | `Scenes 1, 3`, or `In no scene yet` |

**Actions**

- `Edit` — opens the asset modal on that person.
- `Add character` — a dashed button under the last card (`Add a character: from your gallery, from a photo, or invented`).

With nobody on camera, a `Narrator` card takes their place: `Anonymous narrator` / `Nobody is on camera; the lines are spoken off screen.`, with the voice, an `Edit voice` button that opens the voice modal, and the same `Add character` button.

#### Assets Card

`Assets` with a count of the images that are not people (click the word to open the sidebar's Assets tab). The tiles run product photos, then other assets, then locations. Empty, the card reads `Product photos, assets, places…` / `Upload a photo or create one with AI.`; while the run draws images it glows and reads `Generating references · <done> of <total>`.

| Tile | Meaning |
| --- | --- |
| `AI` corner badge | A generated image |
| Pin | A place |
| Dashed tile, `<name> — not generated yet; click to generate it` | An image not generated yet |
| Dashed tile, `<name> — a place described in words; click to add a photo` | A place described only in words |

**Actions**

- Upload button — `Upload a product photo`, or `Upload a photo of the service`.
- Atom button — `Create an asset with AI`.
- Click a tile to open the asset modal (see "Assets, Characters, and Locations").

#### Scene Cards

The cover is the scene's location photo (or the place in words, `No specific place`, or `The place's photo is not generated yet`). On top: the scene number, the beat, and the length. Along the bottom edge: round avatars of the images the scene sends (`@Image2 · <name>`).

Below the cover:

- The title and the place.
- For a speaking scene: the speech label (`On camera`, `Voice-over`, `Filmer reacts`), the line in quotes, and its voice-line row (see "Voice and Spoken Lines").
- What happens on screen, or `Ambient shot`.

The footer shows the camera and the sound cue, plus:

| Footer item | Meaning |
| --- | --- |
| `No dialogue` | A silent scene |
| The transition | Shown when it is not a cut |
| `Custom` | The prompt was hand-edited (`The scene renders from a hand-written prompt`) |
| `1 text` / `N texts` | On-screen texts (`Burned into the scene's finished cut`) |

A scene that needs review has a red border and a `Needs review · <reason>` strip (see "Needs Review").

**Actions**

- Click the card (or press `Enter`) to edit it (see "Editing a Scene").

#### Storyboard Nodes

`Scene N · storyboard`: four quick sketches of the shot (opening frame, two key moments, final frame) so you can check it before paying for its video. Click the sheet to see it full screen.

| State | Meaning |
| --- | --- |
| `Four quick sketches of the shot, to check it before its video` | Empty; nothing drawn yet |
| `Sketching the storyboard…` | Drawing |
| `Redrawing…` | Drawing over an old sheet |
| `The storyboard could not be drawn` | Failed |

**Actions**

- `Storyboard` / `Redraw` — shows its price (`· 0.6 cr`, for example) and draws only that scene: references first if needed, no voice, no video. Hidden while a run is active.

#### Clip Nodes

`Scene N · clip` shows the rendered take at its own proportions, with play and seek, full screen (`Download`, `Share`, `Close`), and thumbs up/down once ready.

| State | Meaning |
| --- | --- |
| `Preparing the render` | The scene is being prepared |
| `Submitting to Aificient Cloud` | The scene is being sent to the cloud |
| `Queued on Aificient Cloud` | Waiting in the cloud queue (with a `Queued` chip) |
| `Rendering on Aificient Cloud` | Rendering |
| `Rendering a new take` | A new take is rendering; the old take stays dimmed underneath |
| `Rendering failed`, `Cloud rendering failed`, or `Cancelled` | The render did not finish |

Under the preview, two things can appear once a take exists:

- A `Trimmed` chip with the saved trim (`−0.4s start · −0.6s end`). Its tooltip reads `Trimmed in the final video; the clip stays whole. Click to change or remove it.`, and clicking it reopens the trim modal.
- A grey strip, `The read slipped: montaña → montañaña · +la · −siempre`, when the delivered clip did not say the line word for word (see "The Read Check").

**Actions** (all hidden during a run)

- `Render` / `Regenerate` — see "Rendering a Scene".
- Scissors — `Trim the start or the end for the final video; the clip stays whole` (see "Trimming a Clip").
- Bin — `Deletes this clip, its finished cut and the final video. Resume Generation renders it again.` It asks first.

#### Trimming a Clip

A trim cuts the start or the end of a scene's clip **in the final video only**. The clip itself stays whole, nothing renders, and you can undo it at any time.

1. On the clip node, click the scissors (`Trim the clip of scene N`). The `Trim clip` modal opens, subtitled `Scene N`.
2. Drag the handle at either end of the filmstrip (`Trim the start`, `Trim the end`); the cut parts dim. The preview loops only the kept part (`Play the kept part` / `Pause`, with a `1.2 / 4.2 s` counter), and a click on the strip moves the playhead.
3. Read `Keeps 4.20 s of 5.00 s` and the chips `−0.40 s start` / `−0.60 s end`; `Reset` clears both.
4. Click `Save trim` (`Only the final video is cut again; nothing renders`). Once a trim is saved, resetting it and saving reads `Remove trim`.

| Rule | Value |
| --- | --- |
| Trim per side | Up to 10 seconds |
| Kept | At least 1 second of every scene (both sides shrink if needed) |
| What it changes | The final video is deleted; clips, finished cuts, and storyboards stay |
| What runs next | `Resume Generation` becomes `Stitch Final Video` |

The note in the modal sums it up: `The clip stays whole — only the final video is cut, and you can undo it any time.` Transitions, edge fades, and captions apply to the trimmed span, and a trim survives later edits by the planner or `Edit with AI`. During a run the button is locked (`Wait for the generation to finish`); a failed save reads `The trim could not be saved.`

#### The Read Check

When a clip lands, the service transcribes it and compares it with the line. If a word differs, the clip node shows a grey strip under the preview: `The read slipped: <heard as> → <line> · +<extra word> · −<missing word>` (the first three mismatches, then `(+N)`). Its tooltip reads `The clip was transcribed and compared with the line. <all mismatches>. Regenerate to get another read.`

It is a warning only: nothing re-renders and nothing is charged. `Regenerate` the scene for another take, or keep it if the slip does not matter. The transcriber can raise a false alarm, so listen before you spend. `Edit with AI` sees the slip too (`READ SLIPPED in the clip`) and can offer to render the scene again. The strip is hidden while a new render runs.

#### Finished Cuts

`Scene N · finished` is the clip with its captions and texts burned in.

| State | Meaning |
| --- | --- |
| `With captions and texts`, `With captions`, or `With texts` | What was burned in |
| `No captions or texts to burn in` | The scene needs neither |
| `Captions failed` or `The texts could not be burned in` | The burn failed |

#### Transitions, Stitch, and Output

As in a story (see "Scene Transitions"): a join node between each pair of scenes with `Change transition`, then `Stitch` (`Waiting…`, `Stitching…`, `Stitched`, `Failed`) and `Output` with the final video and `Download` (full screen `Final Video`).

### Voice and Spoken Lines

Every spoken line is **read first** by the ad's voice, as its own take. The take is sent with the scene's render, so the clip lip-syncs to it word for word, and the scene lasts as long as its line: the take's length plus a short tail, rounded up to whole seconds, between 4 and 15. A take is dropped when its line, the voice, or the language changes.

> **Note:** A take can be at most about 14.5 seconds (`A spoken line runs longer than one clip can carry. Shorten it.`).

#### The Voice Row

The voice row on the lead's card (or on the `Narrator` card) is read-only: a preview button, the voice's name (or `No voice yet`), and its gender and accent. An `Auto` tag marks a voice the app picked for the language, gender, and accent.

#### Changing the Ad's Voice

1. Click `Edit` on the lead's card (or `Edit voice` on the `Narrator` card). The modal's `Voice` section reads `Every line this character says is read in this voice.` (the voice modal: `The voice every spoken line is read in`).
2. Click `Change voice` (or `Pick a voice`; tooltip `Changing the voice reads every line again and re-renders every speaking scene`) and pick a voice.
3. Read the amber confirmation: `<new> replaces <old> for every spoken line.`, what it removes (every speaking scene's clip and the final video, or `No clip uses the voice yet.`), and `Every spoken line is read again in the new voice; each scene shows its line while it is read.`
4. Click `Change and read the lines` (or `Cancel`). The lines of every speaking scene that has no clip yet are read again.

The voice modal also has a `Spoken lines` section with `Read` / `Read again` (`Read the lines again. Clips already rendered keep the read they were rendered from.`), and a `Done` button. A voice change keeps the speech pace.

#### Speech Pace

How fast every line is read is set in the sidebar's `Settings` tab, under `Voice`: `Speech pace` with `Slow`, `Med−`, `Med`, `Med+` (the default), and `Fast` (`How fast every line is read. Changing it reads them again.`). It is not staged with `Apply changes`: picking a pace opens `Change speech pace` (for example `Read at a slow pace`) right away.

- The dialog says what happens: `Every spoken line is read again at a slow pace. This deletes the clips of scenes 1, 3 and the final video. …` — or `… No clip uses the voice yet.`
- Confirm with `Change and read the lines` (`Change pace` when nothing speaks), or `Cancel`.
- The control is disabled with `The ad has no voice yet` or `Wait for the generation to finish`; a failure reads `The pace could not be changed.`

#### The Line Row

The line row on each speaking scene card plays the take (play/pause, seek, time), or reads `Not read yet`, `Reading the line…` (the card is outlined in blue), or the error in red. Its ↻ button (`Read the line` / `Read the line again`) always reads the line again.

> **Warning:** If the scene already has a clip, reading again warns `The clip was rendered from the old read, so it is removed and has to be rendered again.`

#### Messages You May See

Only a missing voice blocks the video; lines that are not read yet are read by the run itself.

| Message | What to do |
| --- | --- |
| `This ad has spoken lines but no voice. Pick a voice before rendering.` | Pick a voice. |
| `A spoken line runs longer than one clip can carry. Shorten it.` | Shorten the line. |
| `Could not read the line.` | Read the line again. |
| `The voice could not read the lines. Try again.` | Try again. |
| `A spoken line came back unreadable. Read the lines again.` | Read the lines again. |
| `A scene's read line is missing. Read the lines again.` | Read the lines again. |
| `The pace could not be changed.` | Try the speech pace again. |

### Editing a Scene

Clicking a scene card on the board opens the scene editor: `Scene N`, subtitled with the scene's length, speech, and beat (`5 s · On camera · Hook`), with `Previous scene` / `Next scene` arrows and an `N / total` counter. (A row in the sidebar's `Scenes` tab only centres the board on the card.)

> **Warning:** There is no unsaved-changes guard. Closing the editor or stepping to another scene drops the draft; switching tabs keeps it.

| Tab | What you edit |
| --- | --- |
| `Scene` | The brief, the spoken line, the shot, and the action |
| `Location` | Which of the ad's places the scene happens in, and where in it |
| `References` | Which images the scene sends |
| `Prompt` | The prompt the clip renders from |
| `Texts` | Up to 3 on-screen texts |

#### The Scene tab

- The title is edited in place at the top (placeholder `Scene N`); on a crazy hook there is also a `Beat`.
- `What they say` — a `Who speaks` control (`On camera`, `Voice-over`, `Off camera`, or `None`) and the line box, with the take's player and a hint such as `4.2 s read · needs 5 s`, `12 words · needs ~6 s`, or `Not read yet`. A silent scene reads `Nobody speaks: the scene plays with its own sound.`
- `Shows` (`Creator` / `Product` / `Both`; `Experience` for a service) and `Camera` (see the table), side by side.
- `What happens` — the action, with a sound strip: `Add a sound cue` opens a field (`A sound, in English — e.g. ice clinking in a glass`; `Replaces the room tone`), and an `×` removes it (`Remove the sound cue`).
- The bottom bar — `Duration`, a −/+ stepper (`Between N and 15 seconds`; the minimum is what the line needs, at least 4 seconds); `Before the line`, 0–3 seconds of action before the line starts (`Seconds of action before the line starts`), for example a sip before the words; and, from scene 2 on, `Comes in`, a thumbnail of the transition that previews on hover and opens the transition picker.

> **Note:** `Before the line` is part of the prompt and the duration, so changing it re-renders the clip, and the minimum duration grows by it.

| Camera group | Choices |
| --- | --- |
| `Footage` | `Bystander phone`, `Security camera`, `Dashcam`, `Doorbell camera`, `Drone` |
| `Everyday` | `Selfie handheld` (default), `Handheld follow`, `Static tripod`, `Slow push-in`, `Orbit`, `Top-down`, `Pan`, `Tracking`, `Crash zoom` |

#### The Location tab

Pick one of the ad's places, `No specific place`, or `New location…` (a name and a description; `Its photo is generated from this description when you save.`). `New location…` is disabled with `No room for its photo` when the photo room is full. Below it sits `Where in the place, and how (stance first)` (for example `Sitting on the chair at the table, legs under it; close to the lens`).

#### The References tab

The images the scene sends (`n of 5`), as chips with their `@1`, `@2` tags; click one to send it or leave it out.

An image you add that the scene's text does not mention yet shows a `New in this scene` card: `Not in the prompt yet — say where it appears, or let the AI decide. Needed before saving.` (required for an asset), with `Write in` (the AI places it) and `Write it myself`. Until then, saving is blocked with `Say how <name> appears in the scene first (References)`.

#### The Prompt tab

The prompt the clip renders from, with an `Automatic` / `Edited` pill (the tab badge reads `custom`), `Edit` / `Done`, and `Rewrite with AI`. `@Image` tags show as picture chips and `@Audio1` as the voice; tags for images the scene no longer sends are red (`Removed image`).

- `Rewrite with AI` asks `What should change?` (`Every @Image and the voice are kept`); the sentences you did not ask to change are kept as they are. On success: `Rewritten. Save the scene to render from it.`
- An edited prompt says `Edited, so changes in the other tabs won't update it.`, with `Undo edits`.

#### The Texts tab

Up to 3 on-screen texts per scene, each up to 120 characters and 3 lines, with a live preview in the ad's format. Empty, the tab reads `No text on this scene. Texts are burned into the finished video by the app, so changing them never re-renders the clip.`

| Control | Options |
| --- | --- |
| `Position` | `Top` / `Center` / `Bottom` |
| `Style` | `Outline` / `Dark box` / `Light box` |
| `Size` | `S` / `M` / `L` |
| `Font` | `Poppins`, `Anton`, `Bangers`, `Luckiest Guy` |
| `Timing` | `Whole scene`, or a `Time window` with `From` / `To` |

Emoji are left out (`Emoji can't be burned into the video, so they're left out.`). The editor also warns about characters the font cannot draw and words wider than the frame.

#### Footer Buttons

- `Render clip` / `Regenerate clip` — with its price; reads `Rendering n%` or `Queued` while it renders (see "Rendering a Scene").
- `Edit with AI` — `Describe a change and the AI rewrites the whole scene`. It docks a one-line composer (`Tell the AI what to change — the whole scene follows`; `Enter` sends, `Esc` closes) that changes the draft only, keeping line, shot, place, and length in sync, and reports what changed (`Changed line, location, length`, with `Undo`).
- `Discard` — `Back to the saved scene`; shown only once there are unsaved changes.
- `Save scene` — saves and says what it did (see the table below).

#### Save Notices

| Message | What it means |
| --- | --- |
| `Saved. No clip needed to change.` | The change does not touch the clip. |
| `Saved. Scene N's clip was removed, with the final video.` | The clip and the final video are removed; render the scene again. |
| `Text saved. It is burned in when you finish the video.` | Texts never re-render the clip; the finish burns them in. |
| `Saved. No clip needed to change; finish the video to see the new transition.` | Only the finish is owed. |

A notice is sometimes followed by ` The lines will be read again in the new voice.` or ` Its storyboard no longer matched and was removed — redraw it to check the new shot.`, and by an action: `Render it now` or `Finish the video`.

> **Warning:** Saving a scene that is rendering asks first: `Scene N is rendering. If this change affects its clip, that take is discarded when it lands — its credits are still spent.` Choose `Keep editing` or `Save anyway`.

### Assets, Characters, and Locations

Clicking a tile, a character's `Edit`, or a row of the sidebar's `Assets` tab opens the asset modal. Its top shows the picture (`View full screen`), tags, `Used in`, and the actions; its footer has `Delete …` and `Done`.

Edits that do not touch a rendered clip save at once (`Saved.`). Edits that would remove rendered clips, or waste a take still rendering, ask first in an amber box with `Keep it` and the confirm button, spelling out the cost, for example:

- `This deletes the clips of scenes 1, 3 and the final video. Those clips render again on the next generation.`
- `The take rendering now for scene 2 is discarded when it lands — its credits are still spent.`

#### A Picture

A person, a product photo, an asset, or a loose place photo. The subtitle says what it is (`A character from your library`, `A person invented for this ad`, `A photo of the product`, `An asset the ad shows — not the product`, `A location photo`). The tags give its kind (`Person`, `Product` / `Service photo`, `Asset`, `Location photo`) and origin (`Your photo`, `Library`, `Generated`, `Edited photo`, `Not generated`).

**Actions**

- `Generate image` / `Regenerate image` — generated images only (`Draw this image (one image generation)`). Regenerating one that clips use asks `Generate a new image?`. **Your own photos are never regenerated.**
- `Replace photo` — your uploads (`Use another photo of yours (PNG or JPG); every scene that sends this one renders again`); confirm with `Replace the photo?`.
- `Change person` — a library character (`Pick another character from your library; every scene with this person renders again`). Opens `Replace <name>` with your gallery.
- `Details` — the `Name`; for an asset, `What it is — the video reads this`, written by AI from the picture and written again whenever the picture changes (a new image or a replaced photo; a name you set is kept); for a generated image, its `Prompt`. Saving details redraws nothing (`The image still shows the previous prompt — regenerate it to match.`).
- Scenes — a card per scene: click to send the image with that scene or leave it out (`A scene sends at most 5 images; changing what a rendered scene sends renders it again.`). Adding an **asset** to a scene opens that scene's editor so you can say how it appears.
- `Delete asset` — `Delete this asset?`. The image leaves the assets and every scene that sent it; those scenes turn red until you check their prompt (see "Needs Review"). A person whose last picture this was leaves the cast.

#### A Location

`A place the ad happens in`, tagged `Location` and `No photo`, `Your photo`, `Generated photo`, or `Edited photo`. A location needs a description or a photo. A place always keeps one photo; there is no "remove photo".

**Actions**

- `Generate photo` / `Regenerate photo` (or `Generate instead` over your photo) — draws it from its description.
- `Use my photo` — uses yours.
- `Details` — the `Name` and `Description` (`What every scene here says about the place. Re-describing re-renders their clips.`).
- `Photos the ad already holds` — use a loose place photo for this place (`Use for <place>`).
- `Scenes here` — move scenes in or out (`Move scene N here?`).
- `Delete location` — `Delete this place; its scenes wait for review`.

#### Adding

`Add to the assets` (`Something the ad shows, or a place it happens in`) has `Assets` and `Locations` tabs; under them, the ways are cards: `Generate` (`Drawn from your words` for an asset, `Drawn from a description` for a place) or `Upload` (`Your photo, as is or edited` / `Your photo of the place`). Assets open on `Generate`; the way you pick is kept when you switch tabs. An asset is named and described by the AI. An upload can carry an optional `Change it with AI (optional)` instruction, which produces an `Edited photo`.

- Buttons: `Add & generate`, `Add & edit`, or `Add photo`.
- While a generated asset is being made, its modal reads `Drawing the image — AI names and describes it next.`, then `AI is naming and describing it from the picture…`; its `Name` and description fields wait with `Named by AI once the image is ready…` / `Written by AI once the image is ready…`.
- `Add a character` (`A person on camera — from your gallery, from a photo, or invented`) offers `Gallery` (`One of your characters`, the default), `Upload` (`Your photo as their portrait`, optionally changed by AI), or `Generate` (`Invented from a description`, with `Who they are`), plus `Name (optional)` and `Gender` (`Any` / `Female` / `Male`).
- A generated creator is drawn full-body on a plain white background. A creator made from your own photo keeps that face: if the video provider refuses it as a real person, the service registers the portrait with the provider and submits the scene again by itself; only when that fails do you see a message (see "Render Messages").
- The lead's modal also has the `Voice` section where the ad's voice is changed (see "Changing the Ad's Voice").
- From the gallery, confirm `Add this person?` — `<name> joins the cast. Add them to a scene from the Scenes tab — no clip changes until then.`

> **Note:** Nothing you add joins a scene by itself.

### Needs Review

When you delete an asset or a location that scenes use, those scenes are flagged instead of silently changed. A scene is also flagged when its hand-edited prompt still names an image it no longer sends.

- The scene card gets a red border and `Needs review · <reason>`.
- The sidebar row gets a red number and `Needs review`.
- The editor shows a red box with the reason and `Fix the prompt and save the scene — no video renders until then.`

The reasons read like `<Name> was deleted from the assets — make sure the prompt no longer counts on it`, `The location "<place>" was deleted — pick another place and check the prompt`, or `The prompt still names an image this scene no longer sends — remove it or reword that part`.

To clear the flag, do one of these:

- Click `Open prompt`, fix the prompt, and save the scene. Saving clears the flag.
- Click `Looks right` (`The scene is right as it is — clears the flag, keeps its clip`).

> **Warning:** While any scene needs review, no video renders: `Scene 3 needs review (an asset it used was deleted).`

### Rendering a Scene

The clip node's `Render` (`Render this scene on Aificient Cloud`) and `Regenerate` (`Render a new take of this scene on Aificient Cloud; the final video is rebuilt when it lands`), and the editor's `Render clip` / `Regenerate clip`, render that one scene.

1. Click `Render` or `Regenerate`.
2. On an ad saved on `Lite` or `Pro`, even a first render asks (`Render this video?` — `Choose the quality for this scene.`). Pick a quality for **just this scene**: the ad's own (`Like the rest of the ad`) or a higher one — `Pro` (`Smoother motion` — `Steadier, more natural movement than Lite. Just this scene, a bit pricier.`) or `Max` (`For a complex scene` — `More natural movement when there's a lot going on. Just this scene, the priciest.`), each with its estimate. With a higher tier the button becomes `Render with Pro` / `Regenerate with Max`, and so on. On an ad saved on `Max`, a first render starts without asking.
3. Confirm. A `Pro` or `Max` take renders at the ad's own resolution (720p on a Lite ad) and leaves the ad's saved settings alone.

> **Warning:** Regenerating always asks `Regenerate this video?` — `The current video is replaced by a new render. The old take can't be brought back.`

> **Cost:** The dialog shows the cost before you confirm (`The new render costs ≈ X credits.`).

A render is blocked while something it needs is missing; the button's tooltip says what, ending in `No video until then.`

When the clip lands, the read check compares it with the line and warns if a word slipped (see "The Read Check"); trimming the start or the end for the final video lives on the clip node too (see "Trimming a Clip").

### The UGC Sidebar

The header shows the title, a line such as `UGC ad · 5 scenes · 32s · 9:16`, and a reload button (`Clear app media caches and reload previews`). Its tabs are `Scenes`, `Assets`, and `Settings`.

#### Scenes

The outline of the ad:

- `Project` (with the product); on a crazy hook, the hook concept with `Twist · …`.
- `Assets` (`6 images · 2 locations · voice`).
- One row per scene: its number, title, status, and place. Click it to centre the board on the scene card; the number badge's border carries the status (green when done, a blue glow while rendering, dashed and pulsing while queued, red when failed).
- `Final video` — `Stitching…`, `Ready`, `<done> of <n> clips`, or `Not stitched`.

| Scene status | Meaning |
| --- | --- |
| `7s` | Done |
| `Rendering 45%` | Rendering |
| `Queued` | Waiting in the cloud queue |
| `Failed` | The render failed |
| `Not rendered · 7s` | No clip yet |

#### Assets

Four categories; every row has a download button.

- `Visual` — `Characters` (`+` opens `Add a character`), `Product` / `Service` (`+` uploads a photo right away), `Assets` (`+` opens `Add an asset`), `Locations` (`+` opens `Add a location`), and `Storyboards` once there are any. A footer line reads `<n> of 6 photos — the product, the assets and the locations share them.`
- Rows carry origin chips (`Your photo`, `Library character`, `Generated`, `Not generated yet`) and scene chips (`S1`, `S2`, `+N`, or `No scene`). Empty groups explain themselves, for example `No product photo — the model invents the product. Upload one to show yours.`
- `Audio` — `Spoken lines`: one row per speaking scene with its length, `Reading…`, or `Not read yet`, an inline player, and a download (`scene_01_line.wav`).
- `Video` — `Scene clips`, `Finished cuts`, and `Final video`.
- `Data` — the plan file, `Ad plan`.

#### Settings

The ad's render settings. Defaults: Lite, 720p, captions off.

- `Render` — `Quality` `Lite` (`Seedance 2.0 fast · 720p`), `Pro` (`Seedance 2.0 · 720p or 1080p`) or `Max` (`Seedance 2.5 · 720p or 1080p`), each with its price per 10 seconds. On a crazy hook: `Max renders the chaos with more believable physics`.
- `Format` — `Aspect ratio` (read-only, `Set by the plan`) and `Resolution` `720p` / `1080p` (not on Lite: `1080p is available on Pro and Max`; HEVC, larger files). Switching to Lite drops back to 720p.
- `Captions` — the same caption controls as a story, with the note `Captions follow each spoken line. Texts you add to a scene are burned in whether captions are on or off.` Turning captions on or off, or changing their style, deletes the finished cuts and the final video; the finish rebuilds them without re-rendering any clip.
- `Voice` — `Speech pace` (`Slow` to `Fast`). Unlike the rest of the tab it applies at once, after a confirmation, and re-reads every line (see "Speech Pace").

The render and caption changes are staged until `Apply changes`. While they are unsaved the footer reads `Unsaved render settings` and rendering is blocked (`Save the render settings first`). Apply is disabled during a run (`The video is being generated. Apply these changes once it finishes.`).

#### Footer

- During a run: `Stop Generation`.
- While clips are in the cloud: a sky chip, `Aificient Cloud: rendering 2/4` or `Aificient Cloud: 3 in queue`, opens the render queue (`Captions, texts and the final cut run automatically once every clip is delivered.`).
- Otherwise: `Resume Generation`, amber when something is missing. It becomes `Stitch Final Video` when every clip exists and only the finish is owed (after a text, transition, or caption change, or a deleted final video) and then runs directly.

The `Resume Generation` menu, `Generate video on`, has a single runtime, `Aificient Cloud (Seedance)`, with the tier, resolution, and estimate, and two actions:

| Action | What it does |
| --- | --- |
| `Generate video · ≈ X cr` | `Sketches the storyboards still missing, then renders N scenes on Seedance, then captions, texts and the final cut`. It reads `Finish the video` when every clip is rendered and only captions, texts, or the stitch remain. |
| `Generate storyboard only` | `Assets, voice and a sketch of each scene · ≈ X cr`: generates the missing images, reads the lines, and draws a storyboard of every scene, without rendering video. Check them, then render. |

When something is missing the primary action explains it: `… Generate the assets first (Generate storyboard only).` or `… Open the scene, check its prompt and save it.` While scenes are already in the cloud queue, the button can still render the others: `Renders the N scenes nothing renders yet; the ones in the cloud queue keep rendering there`.

### Generating and Resuming a UGC Ad

A run goes through these steps and **keeps everything that already exists**; only the gaps are filled.

1. **Place photos** — every place with a description but no photo gets one (`Adding the missing place photos`).
2. **References** — every image not generated yet (portraits, product shots, assets, places), three at a time (`Generating references · x of y`).
3. **Lines** — the voice reads the lines of the scenes this run renders that have no take yet (`Reading the lines`).
4. **Storyboards** — a full run (`Start generation`, `Generate video`) sketches every scene that has neither a sheet nor a clip, three at a time; a failed sheet is reported and the run goes on. `Generate storyboard only` stops here.
5. **Check** — nothing renders while an image is missing, a scene needs review, or a prompt names an image it does not send: `No video until every asset is ready. <what is missing>`.
6. **Render** — each scene is submitted to Aificient Cloud and charged when it is accepted; its old clip, finished cut, and the final video are removed at that moment. The run ends at submission; the clips keep rendering in the cloud, even if you close the app.
7. **Finish** — once every clip is delivered, automatically: the finished cuts (captions are timed from the clip itself; texts are burned in, locally and free on the desktop, on the server on the web), then the stitch (local and free on the desktop; on the web on Aificient Cloud for 0.1 credits). Hard cuts are the default, with each scene's own transition where you set one, and any trims you saved cut the clips at this point. At a hard cut the sound of both clips is faded over a few hundredths of a second, so there are no clicks; across a transition the two soundtracks crossfade for its length. A failed burn falls back to the plain clip (`Scene N: <error> — its texts are not in the final video`).

Reopening a project whose clips all arrived while the app was closed runs the owed finish once by itself; it never renders a scene on its own. `Stop Generation` stops the local steps; scenes already in the cloud keep rendering and are paid. A queued one can still be cancelled (and refunded) from the render queue.

Desktop notifications: `UGC ad prepared` (`<name>: the storyboards are ready to review.`) and `UGC ad ready` (`<name>: the final video is ready.`), or `Crazy Hook …`.

> **Cost:** The plan card, the settings screen, the menu, and every render button show the estimate before you spend anything. Running out of credits opens the out-of-credits card.

- Clips — per second at the saved tier: Lite is the cheapest, then Pro, then Max; 1080p costs more.
- Storyboards — per sheet.
- Generated images and line readings — each charged separately.
- The stitch — free on the desktop; 0.1 credits on Aificient Cloud on the web.

#### Render Messages

| Message | What it means |
| --- | --- |
| `Too many scenes are rendering at once: …` | The cloud is rendering too many scenes at once; the message says more. |
| `Seedance could not render this scene: …` | The model failed on this scene; the reason follows. |
| `Seedance is busy right now` | The model is busy. |
| `Some of these scenes are already rendering. Wait for them to finish, then try again.` | Wait, then try again. |
| `The scene changed while it was being drawn — draw it again.` | The storyboard no longer matches the scene; draw it again. |
| `The plan changed while the render was being prepared. Try again.` | Try again. |
| `Wait for the current generation to finish before editing the ad.` | The ad is locked while a run is active. |
| `The video provider refused a reference image: real human faces and sensitive content are not accepted. Use a generated or illustrated creator, or a product-only photo, and render the scene again.` | A photo other than a creator's portrait shows a real face or sensitive content. Replace it. |
| `The video provider would not approve this creator's portrait. Use another creator image and render the scene again.` | The provider refused the creator's face even after registration. Use another image for that creator. |
| `The video provider refused this creator's face, and creator registration is not set up. Use a generated or illustrated creator.` | Registration is not available on this server; use a generated creator. |
| `Couldn't register this creator with the video provider. Try again in a minute.` or `Too many creators were registered with the video provider in the last few minutes. Try again shortly.` | Wait a minute, then render again. |
| `The ad's creators changed while it was being submitted. Render it again.` | Render the scene again. |

### What UGC Ads Do Not Have

- **Your own GPUs.** Clips render on Aificient Cloud only; there is no local or rented runtime choice.
- **A visual-style preset, scene images, or a narrator mix.** The look comes from your photos and the creators; the voice is read per line and lip-synced.
- **Publishing.** There is no `Publish` button; download the final video from the `Output` node, the full-screen viewer, or the `Assets` tab.
- **The `Generating on <place>` chip.** A UGC ad's sidebar does not show another device's run.

### UGC Limits

| What | Limit |
| --- | --- |
| Scenes | 1–10, each 4–15 seconds (a silent scene defaults to 5) |
| Photos (product, assets, and places together) | 6 |
| People on camera | 2 (the first one leads) |
| Reference images in total, people included | 10 |
| Places | 6 |
| Images sent per scene | 5 |
| On-screen texts per scene | 3, up to 120 characters each |
| Action before the line (`Before the line`) | 0–3 seconds |
| Trim per side (final video only) | Up to 10 seconds; at least 1 second of every scene is kept |
| Upload | PNG or JPG, up to 20 MB |
| Formats | `9:16`, `1:1`, `16:9` |
| Ad length | 15–60 seconds; crazy hook 10, 15, 20, or 30 |
| Spoken line | about 25 words (30 at most); one take at most about 14.5 seconds |
## 25. Global Settings

Settings holds your account and billing, the defaults new projects start from, and the services the desktop app connects to. Open it from the user/profile area in the left sidebar.

The Settings navigation lists these tabs, in this order:

| Tab | What it holds |
| --- | --- |
| General | Version, updates, the tour, your subscription, account and help. |
| Usage | Credits, billing, plan actions and the cloud render history. |
| Storage | Cloud storage used against your plan limit. |
| Notifications | Desktop alerts for finished videos, empty queues and ready GPUs. |
| Social Accounts | The accounts the Publish dialog posts to. |
| Video Config | Voice delays, transition and caption defaults for new projects. |
| Model Config | Video-model defaults, caption instructions, runtime download folder. |
| Audio Config | Speech pace, SFX volume, default narrator voices, automatic accents. |
| Voices | Your cloned voices and saved library voices. |
| Skills | The standing instructions the AI follows in chats. |
| API Keys | Keys for external services such as Vast.ai. |
| GPU Config | Limits for the rented GPU search. |

When the list is taller than the window it scrolls, with a fade and a chevron (`More settings`) at the bottom.

### General

| Control | What it does |
| --- | --- |
| Version chip | A `v1.6.5`-style chip on the app card shows the installed version. |
| `Updates` | A status line — `You are on the latest version`, `Latest N available`, or `Manual update check` — and a `Check` button that becomes `Update to latest` when a newer version exists. |
| `Introduction tour` | Described as `A short walk through the workspace.`; its `Replay` button closes Settings and restarts the guided tour on the home screen (see "Introduction Tour"). |
| Subscription | Your current subscription and an upgrade action. A violet `Free trial · bills <date>` badge shows while you are on a free trial. |
| Account | Your name and email. |
| Help | A help or contact link. |

### Usage

Usage shows the credits included with your plan, credits used and remaining, renewal or cancellation information, and usage over time. Depending on where the subscription is billed, it also offers plan-management, upgrade, or pending-change actions.

Under the plan name a line says where the plan is billed:

| Billing line | Meaning | Action |
| --- | --- | --- |
| `Billed through Stripe` | A Stripe plan | `Manage billing` |
| `Billed through the App Store` | A plan bought in the iPhone app | `Manage in App Store`, which opens your Apple subscriptions page (see "Plan Cards and App Store Billing") |
| `Complimentary access` | Welcome credits: a `Gift Trial` plan card with its expiry and `Client since` | None |

Free daily credits and the free trial are described under "Credits, Plans, Free Trial, and Daily Credits".

#### Generation Job History

At the bottom, click `Load latest generation jobs` to open your account-wide Aificient Cloud video render history. It includes jobs from all projects and lists the newest first. Each job can show:

- Content and scene name.
- Status: `Queued`, `Running`, `Completed`, `Failed`, `Cancelled`, or `Unknown`.
- Quality tier and resolution.
- Requested and finished times.
- Progress percentage plus the current stage or message while the job is queued or running.
- The settled credit price of a completed job, shown with the credit icon (for example `3.4 credits`).

> **Note:** A price appears only once billing has successfully settled a completed render. Queued, running, failed, cancelled and unknown jobs do not show one, and a completed job may omit it while billing is not settled.

Use `Previous` and `Next` to move through longer histories. The page refreshes automatically while it contains queued or running jobs and stops when no active jobs remain. Use the refresh control to check manually, or `Hide` to collapse the history.

### Storage

Storage shows how much cloud storage your projects and assets use, your plan limit, the percentage consumed, and the remaining space. Warning and critical states explain when storage is close to or over the allowance.

If you need more room, remove unneeded project data or use `Upgrade your plan`. Storage-limit errors also appear in a banner at the top of the app, with shortcuts to manage storage or view plans.

### Notifications

Desktop alerts can be switched on independently for:

- A scene video finishing.
- A final stitched project becoming ready.
- A GPU render queue becoming empty.
- A local or Vast.ai GPU finishing setup and becoming ready.

### Social Accounts

This tab connects the social accounts you publish to — the accounts the Publish dialog uses (see "Publishing the Final Video"). Each platform (TikTok, Instagram, YouTube) has its own row. **TikTok is supported today**; Instagram and YouTube show a `Coming soon` tag.

Everything here is **local to this computer**. Connecting an account opens a secure sign-in window, and your session stays on this device — nothing about your accounts is sent to a server.

| Control | What it does |
| --- | --- |
| `Connect` or `Add` | Signs in to an account (`Add` once you already have one). You can connect **multiple TikTok accounts**. |
| Status dot | Next to each account's avatar and display name. Green for `Connected`; amber for `Session expired` when the login needs to be refreshed. |
| Amber refresh/reconnect icon | On an account marked `Session expired`: sign in again. |
| Trash icon (on hover) | Removes the account and forgets its local login. |
| `Refresh metadata` (bottom-right) | Re-fetches the name, avatar and follower count of your connected accounts without reconnecting them. |

> **Note:** `Refresh metadata` checks account details and session state, but it does not replace an expired login — use the amber icon for that.

### Video Config

Video Config holds the defaults used when creating new projects:

- Start voice delay.
- End voice delay.
- Transition duration — the default crossfade between scenes of new stories.
- Captions — the switch, a live preview, `Position`, `Font` (all 51 fonts, see "Caption Fonts"), `Font Size`, and the text, highlight, outline and background colors. Turning captions on with no font set selects `Bangers`.

> **Note:** Changing these global defaults does not alter an existing project. To change captions, timing or other video settings for the selected project, use the right scene sidebar's `Settings` tab and apply the changes there (see "Captions").

### Model Config

Model Config sets the default video-model settings used by new projects:

- Quality (Lite or Pro).
- Social media caption instructions.
- Local runtime download folder.
- Video guidance (Video CFG).
- Audio guidance (Audio CFG).
- Prefetch count.

**Social Media Caption Instructions** is optional free-form guidance the AI follows when it drafts a publish caption (the **Generate** button in the Publish dialog). Use it to set a tone, style, call-to-action, emoji use, or other constraints — for example, "casual and punchy, end with a question, no more than two emojis." It applies to every project, and you can leave it blank.

The runtime download folder can only be changed while the local runtime is stopped and is not downloading, setting up, or booting. Use `Default` to return to the app's standard data folder.

### Audio Config

- Speech pace.
- SFX volume — the default level of the video model's own soundtrack under the narration, a 0–100% slider (default 20%). New projects start from this value; each project can override it in its own `Settings` tab.
- Default narrator voices.
- Automatic voice accent — the Spanish and the English accent an `Automatic` narrator speaks with.

#### Default Narrator Voices

The `Default narrator voices` box (`For narrators with no voice of their own, by gender. Automatic picks the library voice for the script's language and accent.`) has a `Female` and a `Male` row.

| Control | What it does |
| --- | --- |
| `Female` and `Male` rows | Each shows a preview button, the voice's name, trait pills, and description. |
| `Change` | Opens the voice picker locked to that gender (there is no `Clear`). |
| `Automatic` (a row in the picker) | Leave a default on it and the service chooses the library narrator for the script's language and accent. |

How the defaults apply:

- A narrator with no voice of its own is sent with the default for its gender.
- If that voice does not speak the script's language, the service uses its automatic voice instead and says so in a notice on the `Narrator` card.
- A voice assigned to the narrator itself (on the `Narrator` card, or in the character editor) always wins over these defaults.

#### Automatic Voice Accent

The `Automatic voice accent` box (`A narrator on Automatic speaks with a voice of this accent. A voice you choose keeps its own.`) has a `Spanish` and an `English` row, each with its flag and a dropdown:

| Language | Accents |
| --- | --- |
| `Spanish` | `Castellano (España)`, `Andaluz`, `Canario`, `Latino neutro`, `Mexicano`, `Colombiano`, `Argentino (rioplatense)`, `Chileno`, `Caribeño`, `Peruano`. |
| `English` | `No preference` (default), `American`, `British`, `Australian`, `Canadian`, `Irish`, `Scottish`, `Indian`, `South African`, `New Zealand`, `US Southern`. |

### Voices

`Settings > Voices` holds the narrator voices you cloned yourself: `Your own narrator voices, cloned from your recordings. Pick them from any voice field; every scene that names one is narrated with it.` The heading carries an `N/M` badge — how many you keep against the number your plan allows.

| Plan | Cloned voices allowed |
| --- | --- |
| Standard | 5 |
| Pro | 10 |
| Max | 20 |

Each voice is a row with a preview button, its name, trait pills (the gender, and the language with its flag), and a detail line: `Cloned from your recordings`, plus `No preview` or `Rebuilt on next use` when they apply. `Rebuilt on next use` means the service has to rebuild the voice; nothing is required from you.

| Control | What it does |
| --- | --- |
| Pencil | Renames the voice. |
| Bin | Deletes the voice. It asks once first: the button becomes `Delete?` and gives up after a few seconds. |
| Create tile | `Clone your first voice` while you have none, `New voice` afterwards. At the cap it turns into `Upgrade to keep more voices` and opens the plans modal instead; on the top plan it tells you to delete one to add another. |

> **Note:** While the server narrates with a different service, the section notes that your voices are not available on it right now.

#### Saved Library Voices

While narration runs on the voice library, a second block, `Saved library voices` (with its own `N/M` badge), lists the narrators you bookmarked in the `Voice library`: `Narrators you picked from the voice library. They show up in every voice picker and speak every language.`

- `Explore` opens the `Voice library`.
- Each row has a preview button, the name, trait pills, a `<use case> · <tagline>` line, and a remove button (`Remove from saved voices (scripts that use it keep it)`).
- While the list is empty it reads `Nothing saved yet — bookmark voices while exploring.`

#### Cloning a Voice

1. Click `New voice`. The modal opens with `Clone your own voice from a few recordings. It joins your voice library with a preview.`
2. Enter a `Name`.
3. Set `Language` and `Gender`. A clone always has a gender, because that is what the voice picker filters on.
4. Add `Recordings (1–2 minutes of clean speech)` — up to 5 audio files, 20 MB in total, in mp3, wav, m4a, aac, ogg, webm, or flac.
5. Click `Create voice · N credits`. When it finishes, the modal says `"<name>" is ready` and the voice can be picked from any voice field.

The modal's guidance for the recordings:

- One speaker, no music or echo.
- A natural narrating pace.
- Read in the language you will narrate in — the clone keeps your accent.
- Only clone a voice you have the right to use.

> **Cost:** Cloning is a one-off charge. The confirm button shows the price, so you see it before you commit your recordings.

### Skills

`Settings > Skills` is where you create, edit, organise into sections, and delete your skills — the standing instructions the AI follows in every chat where you switch them on. It is described in full under "Skills".

### API Keys

API Keys holds the keys for external services such as Vast.ai GPU rental. For a key you can:

- Add or change it.
- Show or hide it.
- Check the balance.
- Open the service page.

### GPU Config

GPU Config controls the rented GPU search. The GPU family itself is chosen in the `Available Instances` modal (`Create instance`); `GPU Config` lists the selectable families — `3090 / 4090 / 5090 / L40S / A100 / RTX 6000 / H100 / H200`, with `RTX 5090` as the default — and sets the shared Vast.ai search limits:

| Control | Range | Default |
| --- | --- | --- |
| `Disk Space` | 32–500 GB | 140 |
| `Max Price` | $0.5–10 per hour | $3 |
| `Min Reliability` | 50–100% | 76% |

The search also applies floors you cannot lower: 23 GB of GPU memory, an Ampere or newer card, 100 GB of disk, and 32 GB of host RAM.

> **Tip:** If offers are too expensive or none appear, adjust these settings. The `Change settings` button on the modal's empty state opens this section directly.

### Captions

Global `Settings > Video Config` supplies the caption defaults for newly created projects only. To change captions for an existing project:

1. Open the right scene sidebar's `Settings` tab.
2. Find `Captions` and set `Burn-in captions` to `On` or `Off`.
3. Apply the changes before continuing generation.

When captions are enabled, you can adjust:

- Position.
- Font.
- Size.
- Text color.
- Highlight color.
- Outline color.
- Optional background color.

#### Caption Fonts

The font catalogue has 51 faces, grouped by the script they are made for:

- `Latin & Cyrillic` (30): Bangers, Montserrat, Bebas Neue, Anton, Luckiest Guy, Poppins, Archivo Black, Lilita One, Titan One, Bungee, Paytone One, Alfa Slab One, Passion One, Kanit, Sigmar One, Bowlby One, Righteous, Carter One, Londrina Solid, Russo One, Rubik Mono One, Seymour One, Play, Black Ops One, Permanent Marker, Chewy, Amatic SC, Lobster, Creepster, Press Start 2P. (Russian is covered by Montserrat, Russo One, Rubik Mono One, Seymour One, Play, Amatic SC, Lobster, Press Start 2P, and the Japanese fonts.)
- `Japanese` (6): Dela Gothic One, M PLUS Rounded 1c, Zen Maru Gothic, RocknRoll One, Reggae One, DotGothic16.
- `Korean` (5): Black Han Sans, Do Hyeon, Jua, Bagel Fat One, Gasoek One.
- `Arabic` (4): Tajawal, Lalezar, Almarai, Rakkas.
- `Hindi` (6): Mukta, Hind, Khand, Rozha One, Yatra One, Kalam.

The default is `Bangers`. `Inter` is not in the catalogue. When the chosen font cannot write a project's language, that language's own default is used instead — both in the project picker (which says so under the field) and at burn time, instead of drawing empty boxes:

| Language | Fallback font |
| --- | --- |
| Japanese | `Dela Gothic One` |
| Korean | `Black Han Sans` |
| Arabic | `Tajawal` |
| Hindi | `Mukta` |
| Russian | `Montserrat` |

The two font pickers differ:

- The `Font` picker in `Settings > Video Config` lists all 51, each option drawn in its own typeface, with a small grey hint (`Japanese`, `Korean`, `Arabic`, `Hindi`) on the fonts made for a non-Latin script. Under it: `A project in a language this font cannot write uses that language's own default instead.`
- The per-project picker in the right sidebar's `Settings` tab lists only the fonts that can write that project's language.

Previews load the faces from the internet on first use; offline, previews fall back to the app's own font and nothing else changes.

Other caption rules:

- Caption size is independent of the resolution: the same font size takes the same share of the frame at 720p and 1080p.
- Japanese speech is split into one-line cues at phrase ends rather than by word count.
- Right-to-left languages highlight the current word on the correct side.
- Sentence ends recognise CJK, Arabic, and Devanagari punctuation.

#### How Captions Are Made

Captions are added after a scene's video is rendered, not during it. Each scene gets a second box on the board — **raw clip → captioned clip** — and the captioned one is produced like this:

1. Aificient transcribes the scene's **narration audio** to get word-by-word timings aligned to where the voice sits in the final video. This is a small paid step, billed like other generations.
2. Before every burn, the app self-checks the stored timings. Timings that do not match the narration, or that predate a timing change, are corrected or re-transcribed automatically.
3. Your own machine burns the captions into a copy of the clip. This local render shares the same queue as the final stitch, so it never competes with video generation on the GPU.
4. Both versions of the scene are saved to your project — the plain clip and the captioned one — so you can open the project on another computer and still see and use the captioned cuts.
5. When captions are on, the final video is stitched from the captioned clips, so the captions are baked into the video you publish.

> **Cost:** The word timings are saved too, so re-burning a scene's captions later — to try a different font or color, say — is free. You are charged again only when something changes the narration itself (a new script, new audio, or a different voice), because that makes the old timings wrong.

### Turning Captions On or Off Later

Captions can be switched at any time from the selected project's right-sidebar `Settings` tab. The raw scene videos do not have to be regenerated.

| Change | What is removed | What to do next |
| --- | --- | --- |
| Turning captions on | The old final video, because it does not match the project's caption setting. The captioned-clip column is added to the board. | Select `Resume Generation` to create all missing captioned clips locally and stitch a new captioned final video. |
| Changing caption style while captions remain on | The old captioned clips, because their burned style is stale. The saved word timings are retained. | Select `Resume Generation` to re-burn the clips locally at no additional transcription charge and rebuild the final video. Until that finishes, an older final video may still be available. |
| Turning captions off | The old captioned cuts, the saved word timings, and the final video. The captioned-clip column is hidden. The plain clips are kept. | Select `Stitch Final Video` to rebuild the final video from the plain clips. |

Because turning captions off deletes the word timings, turning them back on later re-transcribes each scene (the same small per-scene charge). That also makes an off-and-on round trip a clean reset if captions ever look wrong.

In some restored or older projects, the Stitch node can instead show a `Re-stitch with captions` or `Re-stitch without captions` shortcut when the existing final video's recorded caption mode does not match the current setting.

> **Note:** Re-rendering a scene's video replaces its plain cut, and its captioned cut is removed at the same time — the old captions were burned onto the take you just replaced. The scene's captioned box goes back to empty, ready to be generated again through `Resume Generation`.

## 26. Credits, Plans, Free Trial, and Daily Credits

Generation and cloud rendering run on **credits**. Your balance, plan, and renewal date live in `Settings > Usage`; the plan line under your name in the left sidebar shows the plan at a glance (for example `Pro · Free trial`, or `Gift Trial` while you are on welcome credits). Credit amounts are shown with up to one decimal (for example `2.5 credits`).

### Plan Cards and App Store Billing

Each card in the plans modal shows the plan's credits, `+N credits every day` where the plan has daily credits, its storage, and a feature list.

The first feature is `Up to N videos` — the plan's credits divided by the price of one 4-second Lite 720p clip, computed from the live price table (the line is omitted while prices have not loaded). The rest of the list:

| Plan | Includes |
| --- | --- |
| `Standard` (`What's included`) | `AI script, image & audio generation`, `Cloud video rendering`, `5 cloned voices of your own`, `Reusable character & style library`, `Publish straight to TikTok, Reels & Shorts`. |
| `Pro` (`Everything in Standard, plus`, tagged `Most popular`) | `More monthly credits for bigger projects`, `Priority GPU rendering queue`, `10 cloned voices of your own`, `Priority support`. |
| `Max` (`Everything in Pro, plus`) | `Our highest monthly credit allotment`, `Top-priority rendering at peak times`, `20 cloned voices of your own`, `Early access to new features`, `Dedicated priority support`. |

#### App Store Billing

A plan bought in the Aificient iPhone app is **billed through the App Store**, and the web and desktop apps say so wherever billing is managed. The plan cards then show the credits the App Store plan grants, which can differ from the web plan; a pending change is managed in the App Store too.

| Message | Where you see it |
| --- | --- |
| `Your plan is billed through the App Store. To change or cancel it, open your subscriptions in your Apple Account — from the Aificient app on your iPhone, or on the web.` | A banner at the top of the plans modal, with a `Manage in App Store` button. |
| `Manage in App Store` | The current plan's card, and `Settings > Usage` next to `Billed through the App Store`. |
| `Change in App Store` | The other plan cards, with `Your plan is billed through the App Store, so it changes there.` |
| `Not in the App Store` | A plan Apple does not sell, with `This plan isn't sold in the App Store, where your subscription is billed.` |
| `Your subscription is set to cancel <when>. You'll keep full access until then. To keep it, turn renewal back on in the App Store.` | `Settings > Usage` after a cancellation. |
| `Your plan is billed through the App Store. Manage it in your Apple Account's subscriptions.` | Any Stripe-side action on such an account is refused with this message. |

### Welcome Credits

A new account starts with a small welcome gift of credits (`Gift Trial`). It is sized for one or two Lite 720p cloud clips, not a whole video — enough to try the pipeline.

> **Note:** While you are on welcome credits with no plan, new stories and posters default to the `Lite` tier, and renders made on gift credits carry a small visible Aificient watermark.

### Free Trial

When a free trial is on offer for your account, it applies to **one plan** (normally the cheapest). You save a card and receive the trial's credits immediately; nothing is charged for the trial's days, and the plan starts billing when the trial ends unless you cancel.

`Start free trial` buttons carry a **gift-box glyph**; the sidebar trial card and the trial badges keep a small flag.

Where you meet it:

1. The **closing step of the introduction tour** — `Try <Plan> free for N days`, with `Start free trial` and `See all plans`.
2. The **sidebar card** above your profile row — `Try <Plan> free` / `N days free · N credits`; one click opens the checkout. It shows only while the account has no subscription and disappears the moment a plan or trial starts.
3. The **chat**, when a story, poster, or character turn is refused for lack of credits (see "Running Out of Credits").
4. The **out-of-credits card** inside a project — `Keep creating — N days on us`.
5. The **plans modal** (`Compare plans` / `See plans` anywhere, or `Settings > Usage`) — the trial plan's card shows `0 / N days`, `then <price> / <interval>`, the trial credits, and a gold `Start free trial` button. Clicking it shows `Opening secure checkout in your browser. Your trial credits are granted as soon as your card is saved — nothing is charged today.`

Checkout always opens **outside the app**: your default browser on the desktop, a new tab on the web. When you return, a result card tells you how it went:

| Result card | What it means |
| --- | --- |
| `Your free trial has started` | The card adds `N credits are ready to use.` and the date the plan bills. |
| `That card can't start a trial` | The card gives the reason and a `Try another card` button. Prepaid and disposable cards cannot start a trial; a card that already started a free trial on another account cannot start a second one. |

#### During the Trial

The plans modal shows `You're on a free trial of <Plan> until <date>, when it becomes a paid plan. You can switch plans after that, or start the plan now to get its full credits today.` Other plans read `Available after trial`.

`Start plan now` opens a confirmation — `Ends your <Plan> trial today. Your card is billed right away and the plan's full credits unlock immediately.` — with `Due now`, `Credits unlocked`, and `Then` rows. If you use up the trial's credits early, the out-of-credits card says `You've used your trial credits` and offers `Start my plan now`.

> **Note:** Once a subscription is active — including a free trial — new stories and posters default to the `Pro` tier. UGC ads always start on `Lite`, on every plan.

### Daily Credits

Accounts on an active plan or free trial can claim a free top-up of credits **once per calendar day**. The amount comes with your plan: plan cards in the plans modal show `+N credits every day`, and the trial offer says `Plus N credits to claim free every day of the trial.` Accounts with no subscription have nothing to claim.

> **Note:** The day resets at **midnight in Europe/Madrid** (`00:00 CET` or `00:00 CEST`), the same moment for everyone — not 24 hours after your last claim.

Claiming always takes a click; nothing is credited automatically. Three places offer it:

1. **A popup, once per day.** It opens the first time the app sees an open claim that day on that device, and stays out of the way while the plans modal, an out-of-credits card, a billing result, or the tour is open. Closing it with `×`, `Esc`, or the backdrop leaves the claim on the sidebar card.
2. **The sidebar card** above your profile row. One tap claims. This card takes priority over the free-trial card and the desktop-app link, and it reappears on its own after the next reset, even in a session left open overnight.
3. **The out-of-credits card** inside a project, when you hit zero on a plan or trial.

| Where | Before you claim | After you claim |
| --- | --- | --- |
| Popup | `Your daily credits are ready` / `A fresh top-up lands on <Plan> every single day — today's is waiting.` with a `Claim N credits` button. | `+N credits added` / `They're in your balance now — N credits to spend.` with a `Claimed` check pill in place of the button and a small confetti payoff; it closes by itself after about two seconds. |
| Sidebar card | `Daily credits ready` / `Claim N credits`; its tooltip reads `Claim today's N credits — free with your plan, every day at 00:00 CET.` | `+N credits added` / `Back tomorrow at 00:00 CET`, then it fades out. |
| Out-of-credits card | `Today's free credits are still unclaimed.`, and the primary button becomes `Claim N credits free`. | The gauge climbs back and the card closes by itself so you can retry the generation. |

From the second consecutive day the card and popup show a streak (`3-day streak · keep it going`). Once today's credits are claimed the controls disappear; the out-of-credits card instead shows a countdown chip such as `Free credits in 6 hours` (tooltip `Resets at 00:00 CEST (Europe/Madrid)`).

There is no separate toast — the card or popup state is the confirmation. If a claim is refused because it was already made on another device, the app re-syncs your balance; any other failure shows `Unable to claim your daily credits.`

### Running Out of Credits

**In the creation chat**, a refused turn gets a plain reply instead of an error bar, followed by a card. The reply is one of:

- `You've used up all the credits on your current plan. Upgrade to keep generating — you'll get more credits instantly.`
- `You've used up your welcome credits. Start your free trial to keep generating — you'll get N credits right away.`
- `This account doesn't have any credits yet. …`

The card is `Try <Plan> free for N days` with `Start free trial` and `See all plans` when a trial is on offer; otherwise `Out of credits` / `Upgrade plan` or `No credits yet` / `See plans`.

**Inside a project** (a generation run or a cloud render submission), an out-of-credits card takes over with an animated gauge counting down to `0 credits left` and one of:

| Card title | Button |
| --- | --- |
| `Keep creating — N days on us` | `Start free trial` |
| `You've used your trial credits` | `Start my plan now` |
| `You're out of credits` (on a paid plan) | `Upgrade plan` |
| `You're out of credits` | `Choose a plan` |

With `Upgrade plan` the card explains `Move up a tier and the extra credits land instantly — you only pay the difference for the days left.`, or for an App Store plan `Your plan is billed through the App Store: move up a tier there and the extra credits land as soon as Apple confirms it.`

On a plan or trial the daily-claim lifeline described under "Daily Credits" appears here too. `Not now` closes the card.

**Cloud renders** that cannot be fully paid for are sent scene by scene until the balance runs out. The rest are listed in the generation report: `Not enough credits to render this scene. Render it from the scene panel once you have more credits.`

## 27. Publishing the Final Video

Once a project has a final video, you can post it straight to social media from inside the app. Open the **Publish** dialog with the `Publish` button at the bottom of the right scene sidebar; it becomes active only after the final video exists. Publishing is offered for History projects; posters and UGC ads are downloaded and posted by hand.

Publishing runs **entirely on your own machine**. The app drives a private background browser session that is signed in as your account; nothing about your accounts or your post is sent to an Aificient server. **TikTok is supported today** — Instagram Reels and YouTube Shorts appear as tabs but show a "coming soon" panel.

Before you can post, connect at least one account in `Settings > Social Accounts` (see "Social Accounts"). If you have none connected, the dialog links you straight there; you can also reach it any time with the **Manage** link.

### Choosing a Platform

The top of the dialog has a tab per platform (TikTok, Instagram, YouTube). Each platform has its **own composer**, because every platform posts under different rules. Pick a platform, then fill in that platform's post. Only TikTok's composer is active right now.

### Step 1 — Compose

1. Under **Accounts**, pick the connected account(s) to post to. Only the selected platform's accounts are listed; each shows its avatar and follower count, and selected ones get a check badge.
2. Under **Caption**, write your caption in the single text box and put your `#hashtags` right inside it (hashtags are highlighted as you type). YouTube also shows a separate Title field.
3. Or click **Generate** — the atom button next to the section title — to have the AI draft a caption from your project. It follows the optional **Caption Instructions** you set in `Settings > Model Config`.
4. Under **Sound**, attach a TikTok sound, or leave it unset to keep your video's original audio.
5. Check the live **Preview** on the right. It mirrors how the post will look in the feed — the cover, caption, account handle, and the chosen sound spinning on the cover disc.
6. Click **Prepare publish** to slide to the review step.

The sound picker lets you **search** TikTok's public sound catalog, spot **Trending** sounds, and **preview** any track with the ▶ button before choosing. Once a track is selected it collapses into a row with a **volume** slider, and it plays over your video in the live preview so you can hear the mix. Browsing sounds needs no login.

### Step 2 — Review

The review step is a read-only recap plus the last two choices:

1. Check **Posting to**, **Caption**, and **Sound** — a summary of what you set in compose.
2. Choose the **Thumbnail (cover)**, the exact frame used as the cover. Drag the film-strip timeline to scrub anywhere in the video, or use the left/right peeks to nudge frame by frame. The chosen frame shows as a "Cover" preview.
3. Choose **When to publish**: **Publish now** or **Schedule**. Scheduling reveals a date/time picker; the time must be at least ~20 minutes in the future.
4. Click **Publish now** / **Schedule** to start the hand-off, or **Back** to return to compose.

### Upload Progress

As soon as you confirm, a progress screen takes over the dialog and **locks the form** so nothing changes mid-post. It shows the platform badge in a spinning ring, the **current step**, the account, and elapsed time, plus a row of step icons that fill in (and turn green) as the upload advances:

1. Preparing the video.
2. Opening TikTok Studio.
3. Uploading.
4. Caption.
5. Cover.
6. Sound.
7. Publishing or scheduling.

A **Cancel** button stops the background browser hand-off.

The progress is **saved app-wide**, not just in the dialog. You can close the Publish window and keep working — the post keeps going, and reopening Publish resumes the same live progress until it finishes.

| Result | What you see | What to do |
| --- | --- | --- |
| **Success** | "Published to TikTok", or "Scheduled on …" with the time. | **Post another** clears the form for a fresh post; **Done** closes the dialog. |
| **Couldn't finish** | A short reason and the step it stopped at. | Your caption, sound, and cover are kept, so **Back to editor** lets you try again. |

### Publish History

The **History** button (top-right of the dialog) lists past and prepared posts, with links to live posts and the option to cancel a queued one. It is hidden while an upload is in progress.

> **Note:** TikTok publishing automates the real TikTok Studio composer in the background, so your video is uploaded with the caption, cover, and sound attached, and the post is grouped under the chosen sound. TikTok changes its site often; if a step cannot be completed automatically, the upload stops and shows an error — try again.

## 28. Updates

### App Updates

The desktop app checks for a newer version at startup, every 15 minutes, and immediately whenever the server says the build is too old. The check runs in the sign-in window too, signed in or not. An update is either optional or required:

| Kind | What you see | What you can do |
| --- | --- | --- |
| Optional | Offered only once you are signed in. A modal titled `Aificient Studio <version> is ready` — `You are running <x>. A newer desktop build is available for your system.` — with a `Current v…` → `Latest v…` row. | `Update` or `Cancel`; the `×` is `Dismiss update`. |
| Required | An amber `Required update` pill and `You are running <x>. This update is required to keep using Aificient Studio — install it to continue.` It also appears over the sign-in screen (the window can still be moved and closed). | `Update now` only — there is no `×`, no `Cancel`, and clicking outside does nothing. It disappears by itself if the server lowers the required version. |

A dedicated update window then goes through these states:

- `Preparing update`, then `Downloading version <x>` with progress.
- `Opening installer` — `The installer is ready. This client will close now.`
- The app closes so the installer can continue.
- If it fails: `Update failed` / `Unable to install the update.` in the update window, or `Unable to start update` in the modal.

On the **web** a banner does the same job, on the sign-in page too:

- Optional: `Aificient Studio <x> is available` / `Refresh the page whenever you are ready to pick up the latest version.` with `Refresh` and a dismiss `×`.
- Required: `An update is required to keep using Aificient Studio` / `Version <x> has been released. Refresh the page to continue — finish anything in progress first.` with `Refresh` and no way to dismiss it.

Updating does not sign you out: the stored session is reissued for the new version on the desktop and on the web.

### What's New Cards

New features announce themselves with a **What's new** card. It opens by itself shortly after sign-in, last of the startup surfaces — after the introduction tour has decided whether it runs and after the daily-credit popup has had its turn — and never on top of another dialog. If something else is open, it waits for a quiet moment.

The card shows a picture, the `What's new` label, a title, a short description, and a few highlights.

One button closes it: `Got it`, or, when the announcement points somewhere, a button that takes you there — a Settings section, a composer mode on the home screen, or a link opened in your browser. The corner `×`, `Esc`, and a click outside close it too.

> **Note:** Each card is shown once per account. It is marked as seen the moment it appears, so it does not come back — on this device or any other — and there is no way to reopen one you have dismissed.

## 29. Downloads and Sharing

You can download final videos and many generated assets. When downloading:

- Choose where to save the file.
- The app writes only to the selected location.
- Downloads may take time for large videos.

The fullscreen viewer also includes a share action when your system supports it.

## 30. The iPhone App

**Aificient for iPhone** is a native version of the app for iOS 17 or later. It uses the **same account** as the desktop and web apps — the same projects, character library, voices, skills, credits, and plan — so you can start a story on your computer and check on it from your phone, or make a whole UGC ad on the phone and polish it on the desktop. Updates arrive through the App Store.

The phone does almost everything the desktop does: Story, Poster, UGC, and Character modes, the project screens, `Edit with AI`, skills, per-cut transitions, and your plan. What it leaves to the desktop is listed under "What Stays on the Desktop and the Web".

### Signing In on iPhone

The sign-in screen (`Turn an idea into` / `a finished video.`) offers `Continue with Apple`, `Continue with Google`, and `Continue with email`.

1. For email, type your address (`you@example.com`) and send it. The `Check your email` step asks you to `Enter the 6-digit code we sent to <email>`; the app checks the code as soon as the six boxes are filled (`Checking code…`).
2. `Resend code` becomes available after a countdown (`Resend code in Ns`); `Change email` goes back.

The session is remembered on the phone. Three other screens can replace sign-in:

| Screen | When | What to do |
| --- | --- | --- |
| `Time to update` | The app version is too old for the server | `Open the App Store` and update. |
| `This account is set to be deleted` | You asked to delete the account and are still inside the grace period | `Keep my account` cancels the deletion; `Sign out` leaves it. If support closed the account, the button reads `Write to support`. |
| `Test build` / `No devnet access` | A test build whose account is not approved yet | `Request access`, `Check again`, or `Sign out`. See "Test Builds". |

> **Note:** Google sign-in may fall back to the email code on the phone: `That sign-in isn't set up for the iPhone app yet. Use your email below — it works everywhere.`

### Getting Around

There is no tab bar. The app opens on **Create**, and the side menu is the navigation: tap the three-bar button at the top-left, or swipe in from the left edge of a root screen. Tap or drag the strip of screen that stays visible to close it.

| Menu item | What it opens |
| --- | --- |
| `Create` | The creation chat, exactly where you left it. |
| `Characters` | Your character library (see "Characters on iPhone"). |
| `Generations` | Every render you have sent to Aificient Cloud, grouped by project, with live progress; the `×` on a queued row removes it. |
| `Support bot` | The Support Assistant (`Ask AI`) as a sheet over whatever you are doing. The atom button at the top-right of Generations, a project, and Settings opens it too. |
| `Stories`, `Posters`, `UGC ads` | Your projects, ten at a time with `Load more`. Tap a section title to fold it. A filled dot marks a project whose final video exists. Long-press a project for `Rename` or `Delete`. |
| Round search button | The `Projects` search sheet, with `All` / `Stories` / `Posters` / `UGC` filters and `Load more · N left`. |
| Your initials | Settings (see "Settings, Plans, and Your Account on iPhone"). |
| The white button | `New creation` — or `Claim N free credits` when today's daily credits are waiting (it reads `+N added` afterwards), or `Try N days free` when a free trial is on offer. |

With no projects yet the lists read `No projects yet` / `Your video projects will appear here`.

The top-right corner of Create holds three small controls: a bulb that opens the mode's guide on aificient.io inside the app, `New chat`, and `History` (your previous chats, with `All` / `Story` / `Poster` / `UGC` / `Character` pills, grouped under `Today`, `Yesterday`, `This week`, and `Earlier`; long-press one to `Delete` it).

### Creating on iPhone

The mode picker above the text box offers `Story`, `Poster`, `UGC`, and `Character`. Each mode has the same hero, examples, and plan conversation as on the desktop; the controls sit **inside the text box** as small buttons, and the format pill (for example `9:16 · 30s`) opens an `Options` sheet with the rest.

| Mode | Hero | What you set |
| --- | --- | --- |
| `Story` | `Turn an idea into a video story.` | `+` (up to 8 images from `Photo Library` or `Files`), length (15 seconds to 3 minutes), characters, language (`Auto` or one of the fifteen), skills; the `Style` bubble above the box opens the twelve visual styles. Ask for ideas and it brainstorms five directions, each with `Write this story`. |
| `Poster` | `Bring a poster to life.` | `My poster` (animate a finished poster) or `From zero` (design it first, with up to 5 references and up to 3 characters); shape; length 5–15 seconds. |
| `UGC` | `Turn what you sell into a creator ad.` | See "UGC Ads on iPhone". |
| `Character` | `Design a character once. Use it everywhere.` | `Sex` (`Auto` / `Female` / `Male`, fixed by the voice while one is chosen), a style, a voice, skills. Designing costs credits from the first message; the result card offers `Open in the library`. |

The plan card ends in a white pill (`Create story`, `Create poster`, or `Generate` for an ad) that opens the settings sheet:

- **Story** — `Render settings`: `Aspect ratio` (`Portrait` / `Landscape`), `Resolution` (`1080p` / `720p`), `Quality` (`Lite` / `Pro`), `Images and audio only`; then `Start generation` (or `Start images and audio`) with its estimate.
- **Poster** — `Video settings`: the ratio is set by the poster, `Resolution`, `Mode` (`Lite` / `Pro`), `Video duration` (4–15 seconds), `Images only`; then `Start generation` (or `Start images`).

> **Note:** On the phone every video renders on Aificient Cloud, so there is no runtime choice. Starting a run asks for notification permission the first time.

If a chat turn is refused for lack of credits, a card takes the reply's place (`Out of credits`, `Free credits available`, `Try <Plan> free`, or `No credits yet`) with `Claim …`, `Start free trial`, `See plans` / `Upgrade plan`, and then `Send again`.

### UGC Ads on iPhone

You can make a UGC ad from start to finish on the phone, or open one made on the desktop. The controls are the desktop's (see "UGC Ads" for what each one does); this is where they sit on the phone.

#### The UGC Composer

- Hero: `Turn what you sell into a creator ad.` / `Tell me what you sell and add a few photos. I'll write the ad, and you can tweak it before rendering.` The placeholder reads `What you sell, who it's for, and the offer…`.
- The `Crazy hook` switch sits level with the mode picker (where a story has its style bubble). On, the eyebrow reads `UGC · CRAZY HOOK`, the hero `Open your ad with something impossible.` / `Tell me what you sell. I'll dream up a wild opening that lands on your product.`, and the placeholder `What you sell and who it's for — we'll invent the chaos…`.
- The `+` menu (`Up to 6 photos, no people`; then `N of 6 photos · N locations`, or `No room left — remove one to add another`) offers `Photo Library`, `Files`, and `Product URL…` (`Replace the product…` once one is staged). Long-press a photo chip for `Use as a location` / `Use as a product photo` / `Remove`; a place wears a `Location` strip.
- Characters (up to 2; the first carries a `Lead` tag — `The first one leads, on camera.`), `Voice` (`Ad voice`; `Clear` appears only after you picked one by hand, otherwise the lead's own voice is used), and `Skills`.
- The format pill opens `Options` (`Ad · 9:16 · 30s · Auto`): the `Crazy hook` toggle, `Angle` chips (or `Hook idea` chips for a hook), `Aspect ratio` (`9:16` / `1:1` / `16:9`), `Camera` (`Auto` / `Handheld` / `Mixed` / `Static`), `Language`, and the `Target duration` dial (ads 15–60 seconds in 5-second steps, hooks 10, 15, 20, or 30). Shape, camera, language, and length lock once a plan exists (`Set by the plan`).
- `Product URL…` opens `Import a product`: paste the page, tap `Import` (`Reading…`), and the product is staged with the photos the AI picked. Tap the product chip to open the `Product` editor (`Photos · n of m` with the first as `Main`, `Name`, `Brand`, `Price`, `Offer`, `Description`, `Key points · n/5`, `Remove product` / `Save`). A page alone can be the brief: the chat shows `An ad for <product>`.

While the planner works the chat reads `Writing the ad…` (`Inventing the hook…`) with a `Stop` button. The plan card is the desktop's: `Ad` or `Crazy Hook`, chips, the `Hook` box on a hook, the product row with `Details`, who and where, `Scenes · N`, and `Generate` with `Video ≈ N cr at Lite 720p. You choose quality, resolution and captions next.`

`Generate` opens `Video settings`: `Format` (`Set by the plan.`), `Quality` (`Lite` / `Pro` / `Max`, always starting on Lite), `Resolution` (`720p` / `1080p` — `Lite renders at 720p. 1080p is Pro or Max.`), `Captions`, `Storyboards first`, a recap under `The plan`, and `Start generation` (or `Create storyboards`) with the estimate.

#### The UGC Project Screen

The heading shows `UGC ad` or `Crazy Hook`, the title, and chips (the product, `N scenes`, the length, the format, `720p · Lite`, `Captions` or `No captions`, the language). Under it: the final video (share it from the toolbar) or a strip of the scenes' frames with `Final video not joined yet · N of M clips ready`, the run card with `Stop` / `Done`, and the ad's cloud queue (tap it for `Render queue` — `N rendering · N queued`, `Remove queued`, `Remove`, and rows such as `Discarded — the scene changed while it rendered`).

One white button always offers the next step with its price — `Generate video`, `Finish the video`, or `Stitch final video` — and a line that says what it does (`Renders N scenes on Seedance Lite · 720p, then captions, texts and the final cut`). When it is blocked it says why: what is missing (`The portrait of Leo and a photo of Kitchen are missing.`), a scene to review, unsaved render settings (`Render settings changes pending to be saved! Save the render settings first.`), or a reference still being generated. `Storyboards first` (`Assets, voice and a sketch of each scene · ≈ N cr`) sits under it.

The screen has four tabs: `Scenes`, `Cast`, `Assets`, and `Settings`.

**Scenes.** On a crazy hook, `The hook` card comes first. Each scene card shows its title, `Hook · 6s · Kitchen`, the line (or the action, or `Ambient shot`), the read take as a mini player (`Not read yet`, `Reading the line…`), step marks (`Voice` / `Silent`, `Storyboard`, `Clip` with its percentage, `Captions` / `Texts`), the avatars of the images it sends, an `Unsaved` tag when a draft exists, and a red `Needs review · …` banner when flagged. Between cards sits the transition row (`Transition 1 → 2`, `Hard cut` or `Crossfade · 0.4s`). Long-press a card for `Move up`, `Move down`, `Add a scene after`, or `Delete scene` (`Delete scene N?` — `The scenes after it move up and keep their clips. This can't be undone.`); a dashed `Add scene` button closes the list (an ad holds at most 10). The `New scene` sheet asks `What happens`, offers `Adapt the scenes around it` (`For continuity, the AI may also rewrite the scene before and after it — a neighbour that changes loses its clip and renders again.`), and `Write the scene`.

**The scene editor** (`Scene N`, with chevrons to step between scenes) shows the stage at the top — `Clip`, `Finished`, or `Storyboard` (a numbered 2×2 grid; `No storyboard yet` — `Four quick sketches of the shot, to check before paying for the video.`) — with a corner action (`Render the clip`, `Regenerate the clip`, `Draw the storyboard`, `Redraw the storyboard`; long-press for `Delete the clip`). A `Summary` lists the build steps with their buttons and states:

| Step | Buttons | States |
| --- | --- | --- |
| `Voice` | `Read` / `Redo` (`Read the line again?`) | `Read · 3.4s`, `Silent scene — nothing to say` |
| `Storyboard` | `Draw` / `Redo` | `Optional · ≈ N cr`, `Four sketches` |
| `Clip` | `Render` / `Redo` | `Queued in the cloud`, `Rendering in the cloud`, `Ready · 6s`, `Render failed · refunded`, `Needs the pictures first` |
| `Captions` / `Texts` | — | `Burned in when the video is finished`, `Burned into the clip` |

A flagged scene shows `Needs review` with `Open prompt` and `Looks right`. Below, the scene's settings are folds you open one at a time:

- `Title` — and, on a hook, `Beat` chips (`Hook`, `Problem`, `Reveal`, `Demo`, `Benefit`, `Proof`, `Twist`, `Call to action`, `No beat`).
- `Line` — `Speech` (`On camera`, `Voice-over`, `Off camera (filmer)` on a hook, `None`) and the `Line` (`read in 3.4s · needs 5s`; up to 30 words).
- `Shot` — `Shows`, the `Camera` menu (`Footage` and `Everyday` groups, as on the desktop), and `Comes in with` (`Hold to preview · tap to change`).
- `Action` — `What happens on screen`, `Sound` (in English), and `Duration` (4–15 seconds; `At least Ns, for its line`).
- `Location` — a place, `No specific place`, or `New location…` (`Its photo is generated from this description when you save.`), plus `Where in the place (optional)`.
- `Images` — the `@N` chips (`N of 4`) and the `Write in` card for a new asset (`Write it myself` / `Write in`).
- `Texts` — see "Texts on iPhone" below.
- `Prompt` — the `Automatic` / `Edited` badge, `Edit` / `Done`, `Rewrite with AI` (`What should change?` → `Rewrite`), `Undo edits`, and red chips for `Removed image` tags.

The footer appears only once something changed: `Discard` / `Save scene` (`Saving`), with a note such as `Saving replaces this scene's clip when the change affects it` or `Texts are burned in when the video is finished — the clip is kept`, and `Save while it renders?` when the scene is rendering. After a save: `Saved. No clip needed to change.`, or `Scene 2's clip was removed, with the final video.` with `Render it now` / `Finish the video`.

Rendering a scene opens the same dialog as on the desktop — `Render this video?`, `Regenerate this video?`, or `Delete this video?` — offering the tiers above the ad's (`Lite — Like the rest of the ad`, `Pro — Smoother motion`, `Max — For a complex scene`) and a button such as `Render with Max` or `Regenerate with Pro`, with `The render costs ≈ N credits.`

#### Texts on iPhone

`Add text` (up to 3) over a preview frame with a `Captions` band and a scrubber; each text has `Text N` (`n/120`), `Position`, `Style`, `Size`, `Font`, and `Timing` (`Whole scene` or a `Time window` with `From` / `To`), with the same emoji and missing-glyph warnings as the desktop. Texts are burned in with the captions on the server; changing them never re-renders the clip.

**Cast.** The `Voice` card (`Spoken by <lead>` or `Off screen`) with `Pick a voice` / `Change voice` (confirm with `Change and read the lines`) and a `Read the lines` row (`N lines not read yet · hear every line before paying for video`); then the people (`Lead`, `Library`, `Your photo` tags; `Scenes 1, 3`) and `Add character`.

**Assets.** `Product` / `Service` (`Upload a photo of the product`), `Assets` (`Add an asset`), and `Locations` (`Add a location`), each with its count, and `N of 6 photos — the product, the assets and the locations share them.` A row opens the asset sheet with the same faces as the desktop: a picture (`Generate image` / `Regenerate image`, `Replace photo`, `Change person`, `Details`, a `Scenes` grid, `Delete asset`), a place (`Generate photo`, `Use my photo`, `Details`, `Photos the ad already holds`, `Scenes here`, `Delete location`), or the add face (`Add a character` with `Generate` / `Upload` / `Gallery`; `Add to the assets` with `Assets` / `Locations` and `Generate` / `Upload`). Confirmations spell out the cascade (`This deletes the clips of scenes 1, 3 and the final video. …`).

**Settings.** `Render` (`Quality` `Lite` / `Pro` / `Max` with the engine line and `≈ N cr / 10 s`; on a hook, `Max renders the chaos with more believable physics`), `Format` (`Aspect ratio` `Set by the plan`; `Resolution` `720p` / `1080p` — `1080p is available on Pro and Max`), `Captions` (`Burn-in captions`, the preview, position, font, `Size`, colours, `Background`, and a `My style` reset), then `Discard` / `Apply changes` (`Clips rendered already keep their quality; the next renders use the new one.`), and `Project` (`Rename`, `Delete project` — `It permanently removes the ad and everything generated for it. Queued renders are refunded.`). An unapplied draft puts an amber dot on the tab and holds `Generate video` back.

> **Note:** While a run owns the ad every edit is refused: `Wait for the current generation to finish before editing the ad.` Older `hook` projects open as UGC ads.

### Story and Poster Projects on iPhone

A story opens on its heading (`Story`, the title, and chips), then its final video (share it from the toolbar) or a strip of its scenes with `Final video not joined yet · N of M clips ready`. The run card (`Stop` / `Done`) keeps going if you leave the app (`Keeps going if you leave the app`, `Aificient Cloud is finishing it · you can close the app`). The white button offers the next step with its price — `Generate images & voices` (with `Or everything, up to the final video`), `Render N clips & finish`, or `Join the final video`. Four tabs:

- `Scenes` — cards with `Image`, `Voice` / `Silent`, `Clip`, and `Captions` marks and the narration player; a transition row between cards (a story cut with no transition of its own is tagged `Default` and uses the project's crossfade; long-press a row for `Use the project's crossfade`). Long-press a card for `Add a scene after this one` (or `Add a scene before this one` on scene 1), `Move up`, `Move down`, or `Delete scene…`; a dashed `Add scene` closes the list (`Say what happens — the AI writes it into the story.`; up to 32 scenes). The `Add a scene` sheet takes `What happens` (up to 2000 characters), `Let AI smooth the narration around it`, and `Add scene`; afterwards a `Scene N is in` banner offers `Generate image & narration`. Moving a scene asks first when a final video exists (`Move scene N up?`).
- `Cast` — the narrator (`Change voice`, confirmed with `Change and re-record`; an `Auto` tag names the voice the service picked), the characters (`Narrator` / `Library` tags; `Remove from story`), `Add character` (`Manual`, `With AI`, `Library`), and the character editor (`Draw portrait` / `Redraw portrait`, `Save to library`, `Make a project variant`, `Who they are`, `Voice`, `Outfit`).
- `Assets` — `Upload` or `Create with AI`; the asset editor (`Draw it` / `Redraw it`, `Used in`, `Details`, `Place with AI`, `Delete asset`).
- `Settings` — `Format`, `Model`, `Audio` (`Speech pace`, `Voice delay`, `Clip sound`, `Scene tail`, `Transition`), `Captions`, then `Apply changes` / `Discard`, and `Project` (`Rename`, `Delete project`).

**A scene** (`Scene N`; its menu has `Move up`, `Move down`, `Delete scene…`) shows the stage (`Image`, `Clip`, `Captions`) with a corner action (`Draw the image`, `Render the clip`, or their `again` variants), thumbs for the clip (`Why the dislike?`), a `Summary` of the steps — `Image` (`Generate` / `Redo`), `Voice` (`Record` / `Redo`), `Clip` (`Render` / `Redo` / `Remove`; `Queued in the cloud`, `Rendering in the cloud`, `Rendering on another device`, `Render failed · refunded`, `Needs the image first`, `Needs the voice first`), `Captions` (`Burned in when the video is joined`) — and folds: `Script`, `What happens`, `How the cast looks` (each with `Edit`, by hand or `Rewrite with AI`, and a warning about what is deleted), `Cast` (`Save cast`), `Assets` (up to 5, `Save assets`), and `Transition` (`Comes in with`, `Change`). Changing a cast or assets offers the write-in (`Place with AI` / `Rewrite with AI` / `Take out of the scene` / `Leave as it is`), then `Regenerate images + audio`.

**A poster** opens on its animation (`How is this animation?` rating, `Delete the animation`), `Generate the stills and the animation` (or `Or only the stills`), and `Animate on Aificient Cloud` with its price; then `Stills` (`Poster` or `Imported poster`, `First frame`; `Draw it` / `Draw it again` / `Delete`), `Prompts` (`Edit`), `Video settings` (`Set by the poster`, `Resolution`, `Mode` `Lite` / `Pro`, `Video duration` 4–15 seconds, `Save settings`, `Render the animation again`), and `References`.

**Transitions** are picked the same way everywhere: the picker (`Transition`, `Scene 1 → Scene 2`) has the fourteen tiles, the `Length` slider (0.2–1.5 seconds), `Comes in` for slides and wipes, and `Apply`; applying deletes only the final video (`Transition saved. The final video was deleted, to be joined again with it.`). See "Scene Transitions".

### Edit with AI and Skills on iPhone

The `Edit with AI` capsule sits at the bottom-right of every project screen (`Working on your project…` while busy). It opens a sheet headed `Edit with AI` with `Story · <name>`, `Poster · <name>`, or `UGC ad · <name>` and a `New chat` button. Empty, it suggests three requests for the project kind — for an ad `Make scene 1's hook punchier`, `Add a proof scene after scene 3`, `Draw the storyboards of every scene`; for a story `Regenerate the image of scene 2`, `Make scene 3's narration more dramatic`, `Turn captions on with a bold font`; for a poster `Make the motion slower and more elegant`, `Regenerate the poster image`, `Set the animation to 8 seconds`.

Type in `Tell me what to change…` (up to 4000 characters). While it works it shows `Thinking…`, then `Working — closing this won't stop it.`, and lists each action as a dotted timeline (`Reading the whole ad`, `Rendering scene 2`, `Changing the ad's voice`, `Saving the render settings`, `Drawing storyboards for scene 1, 2`, `Deleting scene 3`, `Changing the narrator voice`, `Stitching the final video`). Suggested voices come as cards with `Use`, transitions as cards with `Apply`. A message may run up to 12 steps, paid actions are quoted before they run, `Stop` cancels the turn, and failures offer `Try again`. It is the desktop assistant (see "Edit with AI"); the capsule hides while a scene or sheet is pushed over the project.

**Skills** work as on the desktop (see "Skills"): the puzzle-piece button in every composer and in the assistant's sheet opens the `Skills` picker (`None on` or the names; `Search skills`, a section filter, `Manage skills`, `N on · up to 10`). `Settings > Skills` manages them — `Create your first skill` / `New section` tiles, sections with `New skill in <section>` and `Rename or change the icon` / `Delete section`, long-press a skill for `Move to` or `Delete`. `New skill` takes a `Name` (optional, the AI suggests one), a `Section`, and `What it should do` (up to 2000 characters) → `Create skill`; an existing skill shows its `Instructions` (up to 4000) with `Save`. A section has a `Name` and an `Icon`.

### Following a Render

- **Live Activities** — while a project generates, the lock screen and the Dynamic Island show a card with the scene still, the cast, and the route of steps: `Images`, `Voices`, `Video`, `Stitch` for a story; `Poster`, `Frame`, `Animation` for a poster; `Assets`, `Lines`, `Sketches`, `Clips`, `Final` for an ad. It ends on `Your video is ready`, `Your poster is animated`, `Your ad is ready` (or `Your clips are ready`, `The storyboards are ready`, `The assets and the voice are ready`), `Finished with problems`, or `Stopped`. Tap it to open the project. Story and poster runs started on the desktop or the web can show one too (iOS 17.2 or later).
- **Notifications** — `Video ready` and `Project finished`, switched on in `Settings > Notifications` (with `Send test notification`; if the system has them off, `Open iOS Settings`).
- **Another device** — if the desktop or the web is generating a story or poster, the phone shows `Generating from <device>` or `Rendering on <device>` with the GPU and the scene progress, and refuses a second run (`Generating on another device`).

> **Note:** A UGC run started on the phone is not visible to other devices. Clips that land while the app is away are finished the next time you open the project.

### Characters on iPhone

`Characters` lists your library with `Search characters` and the `Type` (`All types`), `Gender` (`Any gender`), and `Voice` (`Any voice` / `No voice`) filters; `+` opens Character mode (`Design a character`); empty, it reads `No characters yet` with `Design one`. A character's screen shows its chips and `Description`, offers `Refine character` (it reopens the composer), and long-press gives `Rename` / `Delete` (`Projects that already cast them keep their own copy.`).

### Settings, Plans, and Your Account on iPhone

Tap your initials for Settings. The top shows who you are, your plan badge (`No plan`, `Gift trial`, `<Plan> · Trial`), a `Credits` card (`N of M used`, `Renews <date>`, `Need more credits?` with `Start free trial` / `See plans` / `Upgrade plan`), and `Today's free credits` with `Claim` when there are any.

| Group | Sections |
| --- | --- |
| `Account` | `General`, `Usage`, `Storage` |
| `Creating` | `Audio`, `Voices`, `Skills`, `Video` |
| `Alerts` | `Notifications` |
| `Desktop app` | `Social accounts`, `API keys`, `GPU config` — each badged `Desktop`, each a page that explains why it lives on the computer |

Under them: `Contact support`, `Terms of service`, `Privacy policy`, and `Sign out` (`Your projects stay on your account.`).

- `General` — the app card (`Version`; `Updates arrive through the App Store.`), the plan card (`Billed through the App Store`, `Billed on the web`, or `Complimentary access`; `Renews` / `Expires`; `Client since`; `Manage in the App Store` or `See plans`; `Restore purchases`), `Account` (`Name`, `Email`, `Delete account`), and `Help` (`Need help?`, `Ask the support assistant`, `Replay the introduction`).
- `Usage` — the credits meter (`This billing period` / `Welcome gift`; `Don't run out — Upgrade` past 80 %; `Total`, `Used`, `Remaining`), `Plan change scheduled` / `Your plan is ending` notices, `Usage over time` (`Day`, `Week`, `All plan`) with a `Breakdown`, and `Render history`.
- `Storage` — `Used`, `Plan limit`, `Available`, and `Need more space? Upgrade your plan`, with warnings when you are over.
- `Audio` — `Speech pace`, `SFX volume`, `Default narrator voices` (`Change` per gender), `Automatic voice accent` (Spanish, English).
- `Voices` — your clones (`Clone · ES`, `No preview`, `Rebuilt on next use`; `Rename` / `Delete`), the create tile (`Clone your first voice`, `New voice`, or `Upgrade to keep more voices` — `Pro keeps 10 and Max 20`), and `Saved library voices` with `Explore`. `New voice` takes a `Name`, `Language`, `Gender`, and `Recordings` (`Record` / `Stop` with a level meter, or `Import`; up to 5 files and 20 MB in all — `Only clone a voice you have the right to use.`), then `Create voice · N credits`; it ends on `“<name>” is ready`.
- `Video` — the quality default (`Pro` / `Lite`), `Timing` (`Start voice delay`, `End voice delay`, `Transition duration`; `Transition longer than the end delay` warns), and the caption defaults (`Captions`, `Position`, `Font`, `Font size`, `Colours`, `Background box`, `Box colour`).
- `Notifications` — `Video ready`, `Project finished`, the desktop-only rows greyed out, and `Send test notification`.

#### Plans on iPhone

Plans on the phone are bought through the **App Store** (Apple In-App Purchase): the same `Standard`, `Pro`, and `Max` plans as on the web, at App Store prices, with the free trial and daily credits. A plan bought on the phone belongs to your account, so it works in the web and desktop apps too, where it shows as `Billed through the App Store`.

- The paywall (`Choose your plan`, or the reason that opened it) shows each plan with `Current`, `N days free`, `Most popular`, or `+N% value` badges and, opened, its credits per month, free daily credits, storage, and perks. The button reads `Start N-day free trial` (`Free for 7 days, then <price> / month. Cancel anytime.`), `Continue with <Plan>`, `Upgrade to <Plan>`, `Switch to <Plan>`, `Manage subscription`, or `Change it on the web` for a plan bought on the web. `Restore` recovers a purchase; `Web & desktop too` reminds you it is one plan everywhere.
- Change or cancel an App Store plan with `Manage in the App Store`. A plan bought on the web is changed on the web.
- The out-of-credits sheet (`You're out of credits`, `Keep creating, free for N days`, `You've used your trial credits`, `No credits yet`) offers `Start free trial`, `Upgrade plan`, `Choose a plan`, `See plans`, `Claim N credits free`, or `Not now`. The daily sheet (`Your daily credits are ready`, `Claim N credits`) and the welcome sheet (`You have N free credits`, `Try <Plan> free for N days`) work as on the desktop.

> **Note:** A subscription shared through Family Sharing cannot be used: `Purchases shared through Family Sharing can't be used here — subscribe on your own Apple ID.`

#### Deleting Your Account

`Settings > General > Delete account` is for an account made in the iPhone app and never used on a computer or the web; any other account sees `Not from the iPhone` and is asked to `Write to <support>`.

1. Read `What happens`: you are signed out everywhere, you have N days to change your mind, then projects, videos, characters, voices, conversations, and sign-in details are deleted for good.
2. If an App Store subscription is active, cancel it first (`Cancel your subscription first`, `Manage in the App Store`).
3. Type the word shown (`To go ahead, type <WORD>`) and tap `Delete my account`, then confirm `Delete your account?` (`You can still keep the account by signing in within N days.`).

Signing in again before the date opens `This account is set to be deleted` with `Keep my account`.

### The Introduction Tour on iPhone

The seven-step tour runs once per account on each phone: `Welcome to Aificient Studio`, `Four ways to create`, `Start with a sentence`, `Shape it before you render`, `From script to video`, `Everything is saved`, and a closing card that depends on your account (credits, trial, plan, or subscribed). Replay it from `Settings > General > Replay the introduction`.

### Test Builds

A TestFlight or other test build connects to a separate test environment with its own accounts, projects, and credits. `Settings > General` says so (`Test build` — `Purchases here are not charged. This build has its own accounts and projects, apart from the App Store version's.`), and an account that is not approved there yet sees `Test build` / `No devnet access` at sign-in, with `Request access`, `Check again`, and `Sign out`.

### What Stays on the Desktop and the Web

- **Your own GPUs.** Everything renders on Aificient Cloud; `GPU config` and `API keys` are desktop-only pages.
- **Publishing.** No `Publish` dialog or `Social accounts`; share the MP4 from the project.
- **`Max` for stories and posters.** On the phone `Max` exists for UGC ads only; stories and posters offer `Lite` and `Pro`.
- **UGC runs on other devices.** An ad generating on the phone is not shown on the desktop or the web, and the other way round.
- **Trimming UGC clips, `Before the line`, and the speech pace of an ad.** These are desktop-only for now.

## 31. Where To Find UI Options

Use this section to answer questions such as "Where is X?", "How do I open X?", "Where can I change X?" or "I cannot find X": give the shortest path from a stable area of the app, such as `left sidebar > Settings > GPU Config`. If an option only appears after selecting a project, opening a modal, generating an asset, or entering render settings, say that first.

### Main Navigation Locations

| User asks for | Where to find it |
| --- | --- |
| `Ask AI`, help chat, or Support Assistant | Top-right window-actions area, next to the minimize/maximize/close controls. |
| Window minimize, maximize, restore, or close | Top-right window controls. |
| Menu on a phone / where did the sidebar go | The menu button at the top-left opens the sidebar as a drawer (phones only). |
| Projects | Left sidebar, in the `Recent projects` list below the primary navigation. |
| Older projects that are not in the list | Expand the project's group heading in the left sidebar, then use `Show more` (groups page 25 at a time). |
| Search projects | Magnifying-glass button in the left-sidebar header; it opens a search dialog with recent projects and filtered results. |
| Filter projects by type (History / Posters / UGC) | The `All` / `History` / `Posters` / `UGC` chips inside the project search dialog. The sidebar list itself is grouped by type (`History`, `Posters`, `UGC ads`) instead of filtered. |
| Rename or delete a project | Right-click the project in the left sidebar project list, then choose `Rename` or `Delete`. |
| Create a project or start a new idea | `New project` in the left sidebar; the creation home screen replaces the canvas while the sidebar stays visible. |
| Reopen or delete a creation chat | Creation home screen, `History` at the top-right. |
| Open the reusable-character library | `Character list` in the left sidebar. |
| `Edit with AI` / the in-project assistant | The bar in the bottom-right corner of an open project's canvas, or `Ctrl+K` (`⌘K` on a Mac). On a phone it sits above the `Details` pill. |
| Skills (standing instructions for the AI) | Create and edit them in `Settings > Skills`; switch them on with the `Skills` pill in any composer, or the `Skills` control in `Edit with AI`. |
| Sign out | User/profile area at the bottom of the left sidebar. |
| Global Settings | The same user/profile area, then `Settings`. |
| GPU/runtime manager or Generation Assets | `Generation assets` in the left sidebar; it opens a flyout beside the sidebar. |
| Local runtime or rented GPU instance controls | Left sidebar > `Generation assets`, then the local GPU or the rented instance. |
| Runtime logs, or copy them | The local GPU or rented-instance detail view opened from the `Generation assets` flyout; `Copy logs` sits on the `Instance logs` panel or the `Error` block. |
| Rent GPU or add cloud GPU | Left sidebar > `Generation assets` > `Create instance` (desktop only). If a Vast.ai key is missing, use `Add Vast.ai key` first. |
| The other GPU tiers (3090, L40S, A100, H200) | `Create instance`, then the chevron under the four featured cards (`Show 4 more GPUs`). |
| Download quality indicator / colored status dot on offers | GPU rental modal offers table, in the `Download` column next to each offer's speed and cost. |
| Aificient Cloud queue on the web | `Aificient Cloud` in the left sidebar (the web replaces `Generation assets` with it). |
| Introduction tour / guided tour / replay the tour | It runs by itself for a new account on the home screen. To replay: `Settings > General > Introduction tour > Replay`. |
| The `What's new` card | It opens by itself after sign-in when there is an unseen announcement, once per account. It cannot be reopened afterwards. |
| Claim daily credits / free daily credits | The `Daily credits ready` card above the profile row in the left sidebar, the once-a-day popup, or the `Claim N credits free` button on the out-of-credits card inside a project. Requires an active plan or trial; resets at 00:00 Europe/Madrid. |
| Start the free trial | The `Try <Plan> free` card above the profile row in the left sidebar, the tour's closing step, the out-of-credits card, the chat card after a refused turn, or the plans modal — the buttons carry a gift-box glyph. |
| Plans / compare plans / upgrade | `Settings > Usage`, the profile row in the left sidebar (opens Settings), or any `See plans` / `Compare plans` / `Upgrade plan` link. |
| How many videos a plan covers | The `Up to N videos` line at the top of each plan card's feature list (4-second Lite 720p clips). |
| Manage or cancel a plan bought in the iPhone app | `Manage in App Store` in `Settings > Usage` or the plans modal; it opens your Apple subscriptions page. |
| Credit balance | `Settings > Usage`; the plan line under your name in the left sidebar shows the plan. |
| The iPhone app's menu, cloud queue, or settings | The three-bar button at the top-left (or a swipe from the left edge): `Create`, `Characters`, `Generations`, `Support bot`, your projects, and your initials for Settings. See "The iPhone App". |
| Follow a render on the iPhone lock screen | The Live Activity the iPhone app shows while a project generates (also for runs started on the desktop or the web, iOS 17.2+). |

### Creation Home Screen Locations

| User asks for | Where to find it |
| --- | --- |
| Story mode (formerly Concept), Character mode, or Poster mode | Left sidebar > `New project`, then choose `Story`, `Character`, or `Poster` in the segmented control above the home-screen composer. |
| Brainstorm | Left sidebar > `New project`, choose `Story`, and ask for ideas (or send a topic) as the first message of a new chat; the assistant brainstorms five directions before writing. There is no switch. |
| Find inspiration / example videos | Creation home screen in `Story` mode, the `Find inspiration` button below the empty composer. |
| Idea prompt or chat prompt | `Story` mode, in the bottom composer. |
| Visual style | Creation home screen, the style pill below the prompt (twelve tiles, including `Collage`, `Stickman` and `Rubber Hose`). |
| Duration | The settings pill below the prompt (`Target duration`). |
| Language | The same settings pill (`Narration language`). `Auto` by default — the app reads the language from your prompt — or pick one of the fifteen in the list. |
| Composer options on a phone (style, aspect, language, duration) | The `Options` pill below the prompt opens a bottom sheet with those controls. |
| Skills pill / switch my skills on | The `Skills` (puzzle) pill in the pill row, in every mode; on a phone, the `Skills` section of the `Options` sheet. |
| Price of a chat generation | The `N cr` chip next to the send button; corrections are included and creating the project is free. |
| Stop or cancel a brainstorm, story, or character chat request | Creation home-screen chat — while a request is generating, the send button becomes a stop (filled square) button; click it to cancel. |
| Chat history / reopen a brainstorm, story, poster, UGC, or character chat | `History` at the top-right of the creation home screen (`Recent chats`, filter `All` / `Story` / `Poster` / `UGC` / `Character`). |
| Pinned characters | The `Characters` pill below the prompt in Story mode; the panel has its own search and pages the library ten rows at a time. |
| Warning that a pinned character "was made in a different style" | The amber outline on its chip and the line under the composer: the character was drawn in another visual style than the one selected. |
| Character library | `Character list` in the left sidebar, or the `Characters` picker in a Story composer. |
| Character search, filters, previews, rename, create, and delete | Left sidebar > `Character list`. |
| Attach a product, outfit, location, or prop image to a story | `Story` mode, the `Assets` pill below the prompt (up to 8 PNG/JPG, 20 MB each), or drag the images anywhere onto the home screen. |
| Assets attached to a story / what the script planned | The `Assets` block on the plan card in the chat (`AI planned` and `generated later` tags), and the asset chips on each scene row of the plan. |
| Generate button for a story | Creation home-screen chat, on the generated story script. |
| Render settings before first generation | Continue from a generated concept on the creation home screen; render settings slide into the main workspace. |
| Edit the generated concept (title, characters, scenes, scripts) or the script | Two ways: ask the AI in the creation home-screen `Story` chat (type the change you want and the assistant rewrites the script), or click `Edit` in the right-side `Script` preview panel on the render-settings screen (after continuing from the concept). The `Edit` button is not on the chat screen. |
| Edit a scene title, description, or script before generating | Render-settings `Script` preview panel in `Edit` mode, in the scene's card. |
| Change which characters appear in a scene | The same panel in `Edit` mode, under `Characters in scene`. |
| Edit the narrator voice profile | The same panel in `Edit` mode, in the `Narrator` section. |
| Character prompt | Creation home screen, `Character` mode, in the bottom composer. |
| Character gender | `Character` mode, the gender pill below the prompt (`Auto` / `Female` / `Male`). It is fixed by the voice while one is selected. |
| Reference image for a character | `Character` mode, the `Image`/`Reference` control below the prompt. |
| Character voice | `Character` mode, the `Voice` pill below the prompt (it shows the chosen voice's name; `Library` and `My voices` tabs, and `Browse thousands more voices` for the `Voice library`). |
| Animate a poster I already have | Poster mode, then the `I have a poster` toggle below the prompt, then the `Poster image` pill. |
| Design a poster from a description | Poster mode, then the `From zero` toggle below the prompt. |
| Poster reference images | Poster mode > `From zero`, then the `Reference assets` pill below the prompt. |
| Poster aspect ratio | Poster mode > `From zero`, the settings pill below the prompt. For an imported poster the ratio comes from the image and cannot be set. |
| Poster clip length | Poster mode, the settings pill below the prompt (5–15 seconds), or later in the project's right sidebar > `Settings` > `Video duration`. |
| UGC mode / make an ad for a product, course, or event | Left sidebar > `New project`, then choose `UGC` (megaphone) above the composer. |
| Crazy hook | UGC mode, the `Crazy hook` switch at the end of the pill row (first row of the `Options` sheet on a phone); then the `Hook idea` pill. |
| Import a product page into an ad | UGC mode > `Assets` pill > `Product URL` > `Import`. Click the product chip or card afterwards to edit it. |
| Mark an ad photo as a location | UGC mode > `Assets` pill, the `Location` (map-pin) toggle on the photo's row, or the pin on its thumbnail above the prompt. |
| Ad angle (testimonial, unboxing, before/after…) | UGC mode, the `Angle` pill below the prompt. |
| Ad format, length, language, or camera feel | UGC mode, the settings pill (`9:16 · 30s · Auto`) below the prompt. |
| Creators of an ad / the lead | UGC mode, the `Characters` pill (up to 2; the first one is the `Lead`). |
| The voice of an ad | UGC mode, the `Voice` pill; later, `Edit` on the lead's card (or `Edit voice` on the `Narrator` card) > `Voice` > `Change voice`. |
| The speech pace of an ad | UGC ad > right sidebar > `Settings` > `Voice` > `Speech pace` (re-reads every line). |
| Generate a UGC ad / its video settings | The `Generate` button on the ad plan card in the chat, which opens `Video settings` (quality, resolution, captions, `Generate storyboard only`). |

### Render And Generation Locations

| User asks for | Where to find it |
| --- | --- |
| Aspect ratio or resolution | Initial render-settings screen, or selected project > right sidebar > `Settings` tab. |
| Quality (Lite or Pro) | Initial render-settings screen, selected project > right sidebar > `Settings`, or global `Settings > Model Config`. |
| Video guidance (Video CFG) or audio guidance (Audio CFG) | Selected project > right sidebar > `Settings`, or global `Settings > Model Config`. |
| Prefetch count | Global `Settings > Model Config`. |
| Speech pace, or SFX volume (video-model soundtrack level under the narration) | Selected project > right sidebar > `Settings`, or global `Settings > Audio Config`. |
| Default narrator voices (male/female fallback) | Global `Settings > Audio Config`, the `Default narrator voices` box — `Change` per gender, or leave it on `Automatic`. |
| Narration accent for an automatic voice (Spanish / English) | Global `Settings > Audio Config`, the `Automatic voice accent` box. |
| Start voice delay, end voice delay, or transition duration (the default crossfade) | Selected project > right sidebar > `Settings`, or global `Settings > Video Config`. |
| Transition between two scenes (crossfade, wipe, zoom, dip to black…) | The `Transition` join node between those scenes on the canvas > `Change transition`; in a UGC ad also the scene editor's `Comes in with` box. Then `Stitch Final Video`. |
| Resume Generation | Right scene sidebar for the selected project, shown when assets are missing or invalidated. |
| Resume Generation on a phone | The floating `Resume` / `Stitch` pill beside `Details` at the bottom of the screen. |
| GPU choice for rendering | Initial render-settings screen, or `Resume Generation` menu on the right sidebar. |
| Aificient Cloud rendering | Choose `Aificient Cloud` on the initial render-settings screen when available, or select a project with ready images/audio and use right sidebar > `Resume Generation` > `Aificient Cloud`. |
| Aificient Cloud queue and current-session history | Left sidebar > `Generation assets` > `Aificient Cloud`; the row appears after cloud jobs have been submitted. |
| Aificient Cloud queue/render progress | Center-canvas generation progress bar and the status at the bottom of the right scene sidebar. Cancel queued clips from `Generation assets > Aificient Cloud`. |
| Render the scenes that are missing while the cloud queue is still running | Right sidebar > `Resume Generation` — it stays available when a scene has no clip and is not in the queue (`render them while the queue runs`). |
| Remove one scene from a GPU or cloud render queue | The `Remove from queue` button on that scene's video node while it is still queued. |
| Generate images and audio only | Initial render-settings screen, or `Resume Generation` menu when available. |
| Render the reference image of a new character that is not in any scene | Right sidebar > `Resume Generation` > `Images + Audio only` (the button stays active for an uncast character with no image, even when the final video exists), or `Regenerate images + audio` right after adding the character. |
| Generate the images of pending project assets | They render automatically at the start of the next run; use `Resume Generation` > `Images + Audio only`, or `Generate image` in the asset's detail modal. |
| Assets per scene / assets per character limits | Fixed by the service (5 per scene, 3 per character); there is no setting for them. The scene and outfit pickers stop at those numbers. |
| Build a missing final video when all required clips are ready | Bottom of the right sidebar > `Stitch Final Video`. Some restored projects may instead offer `Re-stitch with captions` / `Re-stitch without captions` on the Stitch node. |
| Stop or cancel video/asset generation | During active generation, in the visible generation/progress controls or right sidebar stop action. To cancel a brainstorm/story/character chat request instead, use the stop button in the creation home-screen chat. Cloud queue cancellation is under `Generation assets > Aificient Cloud`. |
| Why the project says `Generating on …` / generation on another device | The sky-blue chip at the bottom of the right sidebar; stop it from the device that is running it. |
| The 1080p slow-card warning / `Don't ask again` | It opens by itself when you queue 1080p onto a GPU under 40 GB; `Don't ask again` silences it for this computer and cannot be undone from Settings. |
| Generation error summary, error box, or list of failed tasks | Top-right corner of the center canvas, shown after a generation finishes with one or more errors. |
| Enable or disable captions for an existing project | Select the project > right sidebar > `Settings` > `Captions` > `Burn-in captions`, then apply the changes. |
| Change caption position, font, size, colors, outline, or background for an existing project | The same `Captions` section in the project's right-sidebar `Settings`, then apply the changes. The `Font` list shows only fonts that can write the project's language. |
| Caption fonts for Japanese, Korean, Arabic, Hindi, or Russian | Any caption `Font` picker — the catalogue has 51 fonts grouped by script; a font that cannot write the language is replaced by that language's default automatically. |
| Set caption defaults for new projects | Global `Settings > Video Config`; caption styling appears after captions are enabled. |
| Generate all missing captioned clips, or re-burn captions after changing their style | Right sidebar > `Resume Generation` (after applying the project caption-style change). When the raw clips are ready, the caption work runs locally without a GPU picker, and saved word timings are reused. |
| Render a UGC ad / its storyboards | UGC ad > right sidebar > `Resume Generation` > `Generate video · ≈ X cr` or `Generate storyboard only`; or `Render` on one scene's clip node. |
| Trim the start or end of a UGC clip | The scissors on the scene's clip node > `Trim clip` > `Save trim`; then `Stitch Final Video`. |
| Add action before the line starts | Scene editor > `Scene` tab > `Before the line` (0–3 s); the clip re-renders. |
| "The read slipped" on a clip | The grey strip under the clip; hover it for every mismatch, then `Regenerate` if it matters. |
| Render one UGC scene on a higher tier | The scene's clip node > `Render` / `Regenerate` on an ad saved on Lite or Pro: the dialog offers `Pro` and/or `Max` for just that scene. |
| A UGC ad's quality, resolution, or captions | UGC ad > right sidebar > `Settings` tab, then `Apply changes`. |
| Poster render settings (mode Lite/Pro, resolution, clip duration, runtime) | The settings screen after `Create project` on a poster plan, or later in the poster project's right sidebar > `Settings` tab, then `Apply changes`. |
| Where a poster animation renders, or render it later | Poster render-settings screen > `Runtime` (one GPU or Aificient Cloud); later, the poster project's right sidebar > `Resume Generation` > pick a runtime > `Add to render queue`. |
| Generate the poster images without the animation | Poster render-settings screen > `Images only`, or right sidebar > `Resume Generation` > `Images only`. |
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
| Project outline or scene list (for a poster, the plan outline and generation status) | Select a project, then open the right scene sidebar > `Schema` tab (`Plan` tab for a poster, `Scenes` tab for a UGC ad). |
| Asset browser | The same right scene sidebar > `Assets` tab. |
| Project-specific settings | The same right scene sidebar > `Settings` tab. |
| Focus a scene or node | Click an item in right scene sidebar > `Schema`, or use a focus action in `Assets`. |
| The script text / script details | `View script` on the `Project` card on the center canvas (read-only). |
| Scene description, character reference, or script text | Center canvas, in the scene's text/detail nodes. |
| Rewrite scene text | Click the scene text node on the center canvas, then choose manual edit or AI rewrite. |
| Delete a scene image or a scene video | The scene image node or the video node on the center canvas. |
| Regenerate audio | Audio node on the center canvas. |
| Mute the narration while previewing a clip | The narration toggle on the video node. |
| Like, dislike, or clear feedback on a video | Scene Video node or final Output node on the center canvas; use the thumbs controls on the video. |
| Fullscreen media viewer | Click an image or video preview in the canvas or asset views. |
| Download an asset | Right scene sidebar > `Assets`, a canvas media node, the Output node, or the fullscreen media viewer. |
| Download final video | Output node on the center canvas, right scene sidebar > `Assets` > final video, or fullscreen media viewer. |
| Share media | Fullscreen media viewer, when sharing is supported by the system. |
| Which voice the narrator uses, or why it changed | The `Narrator` card on the center canvas — name, description, trait chips, and a notice when the service switched to the automatic voice. |
| Change the narrator's voice | The `Narrator` card on the center canvas > `Change voice`, then `Change and re-record` (or the narrator's character card > `Edit` > `Voice`; locked for library characters — change those in the library). |
| Edit a project character | Click the character node on the center canvas when the character is editable. |
| Regenerate character visuals or a character's reference image | Character node (card) on the center canvas — `Edit` > `Regenerate image`; or right after adding the character, `Regenerate images + audio`. |
| Keep a character recognizable while rewriting it with AI | Character editor > `AI` tab > `Keep the current look as reference`. |
| Give a character an outfit / wardrobe | The `Outfit` strip on the character card (`Add outfit` / `Edit outfit`), or the `Look` section of the character editor. |
| Add a character to an existing story | `Add character` under the last cast card on the center canvas (or the `Add character` card when there is no cast); tabs `Manual`, `AI`, `Library`. |
| Save a project character to the library | The `Library` button on the character card (needs a generated image). |
| Edit a library (global) character inside a project | Not possible directly: click `Project variant` on its card to get an editable project copy, or edit it in `Character list`. |
| Delete or remove a character from a project | `Delete` on the character card (project characters only), then `Remove character` in the confirmation. The character leaves the script and its scenes; those scenes' visuals are deleted, and the app offers to rewrite their text without them. The narrator cannot be removed. |
| Put a character into a scene / change a scene's cast | The `Cast` strip on the scene card (`Add cast` / `Edit cast`), then `Save cast` — or `Save and write in` to have the AI write the newcomer into the scene text. |
| Assign assets to a scene | The `Assets` strip on the scene card (`Add assets` / `Edit assets`). |
| Write a new character or asset into the scene text | The `New in this scene` card inside the scene's cast or asset picker: keep `Write them into the scene` on, optionally say how they appear, then `Save and write in`. |
| Take a character or asset out of the scene text | Untick it in the scene's cast or asset picker, keep `Take them out of the scene` on, then `Save and rewrite`. After deleting a character or asset, use `Rewrite N scenes` in the `Rewrite without <name>` offer. |
| Project assets / asset base | The `Assets` card right after the project card on the center canvas; also listed as `Project asset` in right sidebar > `Assets`. |
| Upload an image as a project asset | `Upload an image` on the `Assets` card (PNG/JPG, up to 20 MB, 20 assets per project); the service names and describes it from the picture. |
| Create a project asset with AI | `Create from a prompt` (atom icon) on the `Assets` card. |
| Edit, regenerate, place, or delete a project asset | Click its tile on the `Assets` card: `Details`, `Generate` / `Regenerate image`, `Place with AI`, `Delete from project`. |
| Poster prompt, first-frame prompt, or video prompt | Center canvas of the poster project; click the prompt node to open its rewrite modal. |
| Delete a poster image, first frame, or animation | The matching media node on the poster canvas; the button states what the delete takes with it. |
| Edit a UGC scene (line, shot, camera, place, prompt, texts) | Click the scene card on the board (a row in the sidebar's `Scenes` tab only centres the board on it). |
| On-screen texts on a UGC scene | Scene editor > `Texts` tab (up to 3). They are burned in when the video is finished. |
| Hear or re-read a UGC scene's spoken line | The line row on the scene card: play it, or ↻ to read it again. |
| A UGC scene marked `Needs review` | Open the scene, check the `Prompt` tab and save, or click `Looks right`. |
| Add a person, asset, or place to a UGC ad | `Add character` under the characters on the board; the upload or atom button on the `Assets` card; or the `+` on a group in the sidebar's `Assets` tab. |

### Global Settings Locations

| User asks for | Where to find it |
| --- | --- |
| App version, check for updates, or the help/contact link | `Settings > General`. |
| Account information | `Settings > General`, or the user/profile area in the left sidebar. |
| Replay the introduction tour | `Settings > General`, the `Introduction tour` row, `Replay`. |
| Free-trial status or billing date | `Settings > General` (the `Free trial · bills <date>` badge) or `Settings > Usage`. |
| Credit usage and usage timeline | `Settings > Usage`. |
| Cloud video generation history across all projects, or the settled price for a completed cloud render | `Settings > Usage`, then `Load latest generation jobs`; the price appears on the completed job when billing has settled. |
| Daily credits amount for a plan | The `+N credits every day` row on each plan card in the plans modal. |
| Storage used, limit, or available space | `Settings > Storage`. |
| Desktop notification preferences | `Settings > Notifications`. |
| Connect or remove a social account (TikTok, etc.) | `Settings > Social Accounts`. |
| Reconnect an account marked `Session expired` | `Settings > Social Accounts`, then select the amber refresh/reconnect icon on that account. |
| Refresh account name, avatar, or follower count | `Settings > Social Accounts`, `Refresh metadata`. |
| Vast.ai key, API key, or Vast.ai balance | `Settings > API Keys`. |
| GPU rental disk space, max price, or reliability filters | `Settings > GPU Config`. |
| GPU family for a rental | Left sidebar > `Generation assets` > `Create instance`, then choose a GPU profile. |
| Default model quality, guidance, or prefetch | `Settings > Model Config`. |
| Social media caption instructions / guidance for AI publish captions | `Settings > Model Config`. |
| Local runtime download folder | `Settings > Model Config`; stop the local runtime before changing it. |
| Default speech pace, SFX volume, automatic voice accent (Spanish / English), or default narrator voices | `Settings > Audio Config`. |
| Default voice timing, transition duration, or captions | `Settings > Video Config`. |
| Clone my own voice / rename or delete my voices | `Settings > Voices`, or the `Clone` link on the `My voices` tab of any voice picker. |
| Browse the voice library / save (bookmark) a library voice | `Browse thousands more voices` at the foot of any voice picker, or `Settings > Voices > Saved library voices > Explore`; bookmark a row with `Save voice`. |
| Remove a saved library voice | `Settings > Voices > Saved library voices`, the remove button on its row, or `Remove from saved voices` in the `Voice library`. |
| How many voices my plan keeps | `Settings > Voices` — the `N/M` badge beside the heading (Standard 5, Pro 10, Max 20). |
| Create, edit, group, or delete skills | `Settings > Skills` (`New skill`, `New section`). |
## 32. Support Assistant (Ask AI)

The Support Assistant is an in-app help chat that answers questions about using Aificient Studio. Its answers are based on this user guide.

**Where:** the `Ask AI` button in the top-right window-actions area, next to the window controls.

### Opening and Closing

- Open it with `Ask AI`. The chat is closed by default.
- Close it with the close button in the chat header, by pressing `Esc`, or by clicking `Ask AI` again.
- Reopening during the same session keeps your conversation. Closing the app clears it.

### Asking a Question

1. Type your question in the message box.
2. Press `Enter` to send, or `Shift+Enter` to add a new line.
3. Wait a few seconds while the assistant prepares an answer.
4. Read the answer, then ask follow-up questions if needed.

Limits and behaviour:

- A message can be up to 4000 characters. A counter appears as you get close to the limit.
- The send button is disabled while an answer is being generated.
- When the chat is empty, suggested questions are shown. Click one to ask it right away.

### What It Can Help With

- How features work, such as creating projects, characters, scenes, and videos.
- Where to find settings and controls.
- Steps for common workflows.
- Render settings, GPU options, and asset editing.

> **Note:** The assistant explains how to use the app. It does not change your project, start generation, or perform actions for you. To have the AI change the open project, use `Edit with AI` in the bottom-right corner of the canvas (see "Edit with AI").

### If the Assistant Cannot Answer

- If a request fails, the chat shows an inline message with a `Try again` option. Your question is kept so you can resend it.
- If help chat is temporarily unavailable, wait a little while and try again.
- If your session has expired, sign in again and reopen the chat.

## 33. Troubleshooting

Each entry names a symptom, why it happens, and what to do. Entries run by theme: sign-in, GPUs and runtimes, cloud and credits, generation and canvas, characters and assets, voices, captions, posters, UGC ads, Edit with AI and skills, publishing, and other.

### I cannot sign in

**Why:** A connection problem, a sign-in interrupted or finished somewhere else, or an app version that needs updating.

**Fix:**

1. Try a different sign-in method. If you use email, request a new code.
2. Match the message to the table.

| Message | What to do |
| --- | --- |
| `Couldn't reach the server to finish signing in. Check your connection and try again.` | Check your internet connection, then retry. |
| `Sign-in took too long or was already used.` or `That sign-in was not started from this app.` | Start again from the app. On the web, finish the sign-in in the same tab you started it in. |
| An update is required, or this version can no longer sign in | Click `Update now` in the update prompt that opens over the sign-in screen (on the web, `Refresh`). You stay signed in through the update. |
| `You're signed in, but your account couldn't be loaded yet.` | Wait. The app keeps retrying on its own; you do not need to sign in again. |
| The account is closed and set to be deleted | Sign in to the iPhone app if the deletion was requested there, or write to info@aificient.io. |

### "No devnet access"

**Why:** Only the Aificient test environment (devnet), used by test builds, shows this: an account there stays locked until it is approved. The released apps never show it.

**Fix:** The `No devnet access` window, with your email as subtitle, reads `This account doesn't have access to the Aificient devnet. To request access, write to info@aificient.io from the address you signed in with.` It cannot be dismissed; click `Copy email` to copy the address, or `Sign out`.

### No GPU is available

**Why:** No runtime is ready, or no rented offer matches your filters.

**Fix:**

1. Check the local runtime is installed and ready, with at least 24 GB of VRAM on the GPU and 24 GB of RAM on the machine. The sidebar says `Needs 24 GB VRAM`, the detail view `insufficient VRAM`, or the RAM message appears in the `Error` block when you start it.
2. For rented GPUs, check the Vast.ai key is configured, an instance is running and ready, and the search filters are not too strict.
3. Or pick `Aificient Cloud` on the initial render-settings screen, or under `Resume Generation` for an existing project whose images and audio are ready. Both need an active plan, enough credits, and eligible scene inputs.

### Local runtime will not install

**Why:** A system, hardware, or disk requirement is not met.

**Fix:**

1. Check your system is supported (Windows desktop app).
2. Check the minimums in the table. A smaller card or less RAM means Aificient Cloud or a rented GPU.
3. Check free disk space: 40 GB for the install, plus the model download of around 76 GB.
4. Open runtime details and review the visible error/logs (`Copy logs` copies them).

| Minimum | Message when it is not met |
| --- | --- |
| GPU with at least 24 GB of VRAM | `The local runtime needs at least 24 GB of VRAM to render MiniMax-H3. This GPU has N GB.` |
| At least 24 GB of system RAM | `This machine has N GB of system RAM. The local runtime needs at least 24 GB — not for the GPU (<GPU> is fine), but because the model's weights stream through it.` |

### A render is refused because the GPU is too small

**Why:** The selected runtime's card is plainly under 24 GB: `<GPU> has less than 23 GB of VRAM, which MiniMax-H3 cannot render on even with every block streamed. Use Cloud Render, or pick a 24 GB+ GPU (RTX 3090 / 4090 or better).`

**Fix:** Pick Aificient Cloud or a 24 GB+ GPU.

### The app warns that 1080p will be slow

**Why:** You queued 1080p onto a GPU under 40 GB, which has to stream the model. Clips past about 6 seconds may not fit at 1080p on such a card.

**Fix:** choose in the `1080p will be slow on <card>` dialog:

- `Switch to 720p` — saves the project at 720p (much cheaper, very similar quality) and queues it.
- `Keep 1080p` — goes ahead.
- `Don't ask again` — silences it on this computer.

### Rented GPU offers do not appear

**Why:** The Vast.ai key or balance is missing, or the filters exclude every offer.

**Fix:**

1. Check the Vast.ai key and the account balance.
2. Increase max price, lower minimum reliability, or reduce the disk requirement (the search never goes below 100 GB).
3. Pick a different GPU family (the chevron under the featured cards shows four more).
4. `Change settings` on the empty-offers state opens `Settings > GPU Config` without closing the modal.

### Aificient Cloud is unavailable

**Why:** Cloud needs an active subscription with credits, eligible scenes, and storage under its allowance.

**Fix:**

1. Initial project: check `Aificient Cloud` appears in the render-settings `Runtime` list. Existing project: confirm it has missing scene videos and its scene images and audio are ready, then check `Resume Generation`.
2. Check the subscription is active with enough credits for the displayed estimate. With fewer, only the first scenes the balance covers are sent; the rest wait for more credits.
3. Check the submission has no more than 32 missing scenes, and that each scene's audio plus voice delays is no longer than 13 seconds.
4. Check `Settings > Storage` is not over its allowance.

> **Note:** If a queued or running cloud render fails, open `Generation assets > Aificient Cloud` for its status. Failed and cancelled cloud jobs refund their reserved credits.

### Storage limit reached

**Why:** The account is over its plan's storage allowance. Generation actions that would add assets can stay blocked until it is under the allowance or the plan is upgraded.

**Fix:** Open `Settings > Storage` to see usage, the plan limit, and available space. Remove unneeded project data, or view the available plans for more storage.

### I cannot claim my daily credits

**Why:** Daily credits need an active plan or free trial and can be claimed once per calendar day; an account with no subscription has nothing to claim.

**Fix:**

- Wait for the reset at 00:00 Europe/Madrid (`CET` / `CEST`), not 24 hours after the last claim. Once claimed, the card and popup disappear and the out-of-credits card shows `Free credits in N hours` instead.
- If you claimed on another device, the app re-syncs silently.
- Any other failure shows `Unable to claim your daily credits.` Check your connection and try again from the sidebar card.

### The free trial checkout refused my card

**Why:** Prepaid and disposable cards cannot start a trial, and a card that already started a free trial on another account cannot start a second one.

**Fix:** Click `Try another card` on the result card. The trial stays available.

### My plan is billed through the App Store

**Why:** A plan bought in the iPhone app can only be changed or cancelled in your Apple subscriptions, so web checkout and Stripe actions are refused with `Your plan is billed through the App Store. Manage it in your Apple Account's subscriptions.`

**Fix:** Click `Manage in App Store` (`Settings > Usage` or the plans modal).

### Generation is incomplete

**Why:** One or more scenes failed.

**Fix:**

1. Check the generation error summary box in the top-right of the canvas for the specific failures and their reasons.
2. Open the Schema tab and find the scene with an error.
3. Open the Assets tab to see what is missing, and the runtime detail view to check logs.
4. Use `Resume Generation`.

### Editing is disabled

**Why:** Editing is blocked while generation is active.

**Fix:** Stop generation or wait for it to finish, then edit.

### The sidebar says the project is generating on another device

**Why:** Another computer, the web, or the iPhone app is generating this project (`Generating on <place> N%`). A run started here meanwhile is refused with `This project is being generated on <place>.`

**Fix:** Wait for it, or stop it from that device.

### The final video disappeared after I changed a transition

**Why:** Expected: a transition lives in the final cut, so changing one deletes only the final video. Every clip is kept.

**Fix:** Click `Stitch Final Video` at the bottom of the sidebar to rebuild it. No scene renders again.

### I added a character but cannot generate its image

**Why:** A new character is in no scene until you cast them, and nothing regenerates when you add them.

**Fix:**

1. To render the reference image for preview, use `Regenerate images + audio` in the confirmation right after adding, `Edit` > `Regenerate image` on the card, or right sidebar > `Resume Generation` > `Images + Audio only`.
2. The button stays active for an uncast character with no image even when the project's final video already exists. The card shows the progress, and the image lands when the run finishes.
3. To put the character in the video, use the `Cast` strip on the scenes they belong in.

### I cannot edit, delete, or dress a character

**Why:** A card with a `global` badge is a library character and cannot be changed from inside a project (`Global characters cannot be edited from the jamboard`). Every card's actions are also hidden while the project is generating.

**Fix:**

1. Click `Project variant` on its card for an editable copy for this project, or edit the original in `Character list`.
2. If the project is generating, wait for the run to finish or stop it.

### A deleted character or asset still shows up in a new scene image

**Why:** The scene's text still describes it, so the image model draws it from the words.

**Fix:**

1. Use `Rewrite N scenes` in the `Rewrite without <name>` offer that appears right after the delete.
2. If you chose `Leave as it is`, rewrite the scene's text yourself, or open its cast or asset picker, untick what should leave, and `Save and rewrite`.

### "This scene is still being rewritten from your earlier save"

**Why:** An earlier rewrite of that scene is still running (usually after a network error). Nothing is charged twice.

**Fix:** Close the card or wait. It switches to the result as soon as the new text arrives.

### I cannot attach more assets to a story

**Why:** Asset limits are fixed by the service and cannot be changed.

**Fix:**

1. In a story request, remove one from the `Assets` panel to add another.
2. In a project (at most 5 assets per scene and 3 per character), unselect one in the picker to make room.

| Limit | Message you may see |
| --- | --- |
| A story request holds at most 8 assets | `At most 8 assets can be attached to one story.` or `Only N more asset(s) fit — the extras were skipped.` |
| PNG or JPG only, up to 20 MB each | `Only PNG or JPG images are accepted.` or `Image exceeds the 20MB limit.` |
| A project's asset base holds at most 20 assets | `A project can hold at most 20 assets. Delete one to add another.` |

### The uploaded asset got a different name, or the upload says the AI couldn't read it

**Why:** Uploads are named and described by the service from the picture (a small charged call); the file name is never used.

**Fix:**

1. Edit the name or description in the asset's `Details` and `Save`.
2. `The AI couldn't make out that image. Try a clearer picture, or try again in a moment.` means the picture could not be described and nothing was stored. Try a clearer image.

### "Cannot update assets while a task is in progress"

**Why:** Asset, outfit, and cast changes are blocked while a generation task runs.

**Fix:** Wait for it to finish, or stop the generation, then try again.

### An asset tile is dashed / a chip says "pending generation"

**Why:** That asset has no image yet, usually one the script planned. It renders automatically at the start of the next generation run (before characters and scenes); a failed asset never fails the run, the scene generates without that reference.

**Fix:** To render it now, open its tile and click `Generate image`, or use `Resume Generation` > `Images + Audio only`.

### The narrator does not use the voice I picked

**Why:** The service switched the voice while creating the project, typically because the voice does not narrate in the script's language. The `Narrator` card on the canvas shows a notice saying so, and the narrator is on the automatic voice for that language.

**Fix:**

1. Open the `Narrator` card and click `Change voice`.
2. Pick a voice native to that language (the picker opens on them), or one of the multilingual `Global` voices.
3. The `Automatic voice accent` rows in `Settings > Audio Config` decide which Spanish or English accent an automatic narrator speaks with. A voice name with a small `Auto` tag is the one the service picked automatically; play its preview to hear it.

### The voice picker says `No <Language> voices on the shelf yet`

**Why:** The `Narrator` card's picker lists the library voices native to the script's language, and none is on your shelf.

**Fix:** Click `Browse <language> voices` to open the `Voice library` on that language and pick (or save) one. Picking a voice there also saves it under `My voices`.

### I cannot create another voice

**Why:** Your plan caps the voices you keep (Standard 5, Pro 10, Max 20). `Settings > Voices` shows `N/M` beside the heading, where M is that cap.

**Fix:**

1. At the cap, the create tile becomes `Upgrade to keep more voices` and opens the plans modal. On the top plan, delete a voice to make room for another.
2. A tile disabled with `Voice creation is not available on this server` means cloning is not configured there.

### My cloned voice says "Rebuilding" or "Rebuilt on next use"

**Why:** The voice service dropped the model; nothing of yours is lost.

**Fix:** Nothing to do. It is rebuilt automatically the next time the voice narrates, and the voice stays selectable meanwhile.

### I cannot save another library voice

**Why:** The shelf of saved library voices has a cap set by the service (`You already keep N voices. Remove one to save another.`).

**Fix:** Remove one from `Settings > Voices > Saved library voices`, or with `Remove from saved voices` in the `Voice library`. Scripts that already use a removed voice keep it.

### Captions use a different font than the one I chose

**Why:** The chosen font has no characters for the project's language, so the language's default is burned instead. The project's `Font` field says `<Font> has no <Language> characters, so captions use <Font>.` underneath.

**Fix:** Pick a font from that language's group. The project picker lists only fonts that can write it.

### I cannot add another poster reference image

**Why:** Reference images and pinned characters share one budget of 5, and characters have their own limit of 3. The `Reference assets` pill shows the combined count, and its tooltip explains what is blocking you.

**Fix:** Unpin a character to free a slot, or remove an image.

### A poster plan will not create

**Why:** Something the plan relies on changed, or it took too long to generate.

**Fix:** match the message:

| Message | What to do |
| --- | --- |
| "This poster has N references and the limit is now 5." | The plan predates the shared image-and-character budget. Send any correction in the chat; the oldest extras are dropped and the plan comes back ready to create. |
| "One of the reference images is no longer in your assets folder." | Poster references live in your assets folder, not inside the project. If one was deleted, attach it again in a chat correction. |
| "A selected character is no longer in your library." | Unpin it and send the prompt again. |
| Reference images must be JPG or PNG. | Convert the file and attach it again. |
| The poster took too long to generate. | Reference images make plan generation slower. Try again, or with fewer of them. |

### The poster render button is disabled

**Why:** A render needs saved settings, a runtime, and work left to do.

**Fix:** check, in order:

1. The `Settings` tab has no unsaved changes. A render always uses the saved video config, so the footer warns `Unsaved video settings` and blocks the submit until you `Apply changes`.
2. A runtime is selected in the `Resume Generation` menu (one GPU, or Aificient Cloud when it is available).
3. The animation is not already rendered; the button is disabled when there is nothing left to do.

### My poster has no captions or Publish button

**Why:** Posters have neither. There is no narration track to transcribe, so there is no caption step, and the `Publish` dialog is available for History projects only.

**Fix:** Nothing to do; this is by design.

### A UGC ad will not render

**Why:** Something is missing or unsaved; the sidebar's `Resume Generation` tooltip or the clip's `Render` tooltip names it.

**Fix:** match the tooltip:

| Tooltip or state | What to do |
| --- | --- |
| An image is not generated yet (`The photo of <place> … is missing.`) | Use `Generate storyboard only`, or open the tile and `Generate image`. |
| `This ad has spoken lines but no voice. Pick a voice before rendering.` | Click `Edit` on the lead's card (or `Edit voice` on the `Narrator` card) and pick a voice. |
| A scene needs review (red border) | Open it, check the `Prompt` tab and save, or click `Looks right`. |
| Unsaved render settings | Click `Apply changes` in the `Settings` tab. |
| A reference image is still being generated | Wait for it to finish. |
| `A spoken line runs longer than one clip can carry. Shorten it.` | Shorten that scene's line. |
| `Too many scenes are rendering at once` or `Seedance is busy right now` | Wait for some clips to finish, then try again. |

### I cannot add another photo, person, or place to a UGC ad

**Why:** The ad is at one of its limits:

- 6 photos of the product, its assets, and its places together.
- 2 people and 6 places.
- 10 reference images in all; a scene sends at most 5.

**Fix:** Delete a photo or a place you no longer need (`Delete asset` / `Delete location` in its modal), or take an image out of a scene. Photos with people in them are not used as assets; add people with `Add character`.

### A UGC clip says "The read slipped"

**Why:** When a clip lands, the service transcribes it and compares it with the line. The strip under the clip lists the words that differ (`montaña → montañaña`, `+la` for an extra word, `−siempre` for a missing one). It is a warning only; nothing re-renders and nothing is charged.

**Fix:**

1. Hover the strip to read every mismatch, then play the clip; the transcriber can raise a false alarm.
2. If the slip matters, click `Regenerate` on the clip for another take (a new render is charged).
3. If only the start or the end is wrong, the scissors on the clip node can trim it out of the final video for free.

### My UGC ad's texts or captions are not in the final video

**Why:** Texts and captions are burned into the scenes' finished cuts, which are made when the ad is finished. Emoji are always left out.

**Fix:**

1. After changing them, use `Stitch Final Video` (or `Finish the video`).
2. If a burn fails, that scene falls back to its plain clip and the report says `Scene N: <error> — its texts are not in the final video`.

### Edit with AI did not do what I asked

**Why:** A step failed, or the assistant refused or is waiting for your answer.

**Fix:**

1. Read the timeline under its answer: each step it ran is listed, and a failed one is red with its reason.
2. It refuses media changes while a generation runs on this project (here or on another device): wait for it, or ask it to stop the generation.
3. It always asks before rendering video or anything destructive, and waits for your answer in the chat.

### My skill is not being followed

**Why:** It is switched off, or the project's assistant uses its own selection.

**Fix:**

1. Check the `Skills` pill, which shows how many are on (a sent message shows a puzzle glyph with the count). At most 10 can be on at once.
2. In a project's `Edit with AI`, the assistant has its own selection, which starts from the skills the project was planned with.

### Publishing to social accounts

For the full walkthrough of the Publish dialog (compose, review, scheduling, and live upload progress), see "Publishing the Final Video".

**Why:** A missing final video, an account that is not connected or has expired, or a TikTok page change mid-upload.

**Fix:** match your case:

| Problem | What to do |
| --- | --- |
| The `Publish` button is greyed out | It only activates once the project has a final video. Finish video generation first. |
| No accounts to post to | Connect one in `Settings > Social Accounts` (TikTok is the only platform you can connect today). The dialog links you there, and the **Manage** link opens it any time. |
| An account shows "Session expired" | Open `Settings > Social Accounts`, select the amber refresh/reconnect icon on that account, and sign in again. `Refresh metadata` can re-check the account, but an expired login still requires reconnection. |
| The upload stopped with an error | TikTok changes its site often, so a step may occasionally fail to complete automatically. Your caption, sound, and cover are kept: choose **Back to editor** and try again. If it keeps failing, confirm the account still shows `Connected`. |
| I closed the Publish window mid-upload | The post keeps running and its progress is saved app-wide. Reopen `Publish` to watch it resume until it finishes. |
| I want to stop a post | Use **Cancel** on the upload progress screen (it stops the background hand-off), or cancel a queued or scheduled post from the **History** view. |
| Scheduling won't accept my time | Scheduled posts must be at least ~20 minutes in the future; pick a later time. |

> **Note:** Publishing runs entirely on your own machine through a private background browser session. Nothing about your accounts or posts is sent to an Aificient server.

### Rename project fails

**Why:** The runtime or cloud API that owns the project is unreachable.

**Fix:** Rename from the project list context menu. If it fails, check that the owning runtime or cloud API is reachable, then try again.

### The what's new card did not come back

**Why:** Each card is shown once per account and is marked as seen the moment it appears.

**Fix:** Nothing to do. It cannot be reopened, on this device or any other.

### The introduction tour did not appear

**Why:** It starts on its own only for an account less than 14 days old, on the home screen, once billing has loaded, and only once per device or browser.

**Fix:** Replay it any time from `Settings > General > Introduction tour > Replay`.

## 34. Recommended Workflows

Step-by-step paths through common jobs; each feature's own section has the details.

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
4. Choose `Lite` for speed and lower VRAM, or `Pro` for best quality.
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

1. Click `Add character` under the cast column. Describe them (`Manual`), let the AI write them from a prompt or reference photos (`AI`), or pick one from `Library`.
2. Click `Regenerate images + audio` in the confirmation (or `Resume Generation > Images + Audio only`) to render the reference image and check the look. Nothing else regenerates yet.
3. Adjust with `Edit` if needed. `Keep the current look as reference` keeps the face while you change details.
4. Open the `Cast` strip on each scene the character belongs in and `Save cast`. Those scenes regenerate their image and video on the next run.
5. `Resume Generation` to rebuild the affected scenes and the final video.

### Brand or Product Placement Workflow

Use this when a real product, logo, or location must appear consistently.

1. In the Story composer, attach the packshots and location photos with the `Assets` pill (up to 8), then describe the video.
2. Read the plan card's `Assets` block and the asset chips on each scene row. Ask for corrections in chat if the product should appear elsewhere.
3. Generate. Uploaded assets are never regenerated: what you uploaded is what the image model is shown.
4. On the canvas, fine-tune: `Edit assets` on a scene to add or remove the product, or open the asset's tile and use `Place with AI` (`show it wherever the chemist is drinking`).
5. Missing something? `Upload an image` or `Create from a prompt` on the `Assets` card adds new assets at any time.
6. `Resume Generation` to rebuild only the scenes you changed.

### Consistent Wardrobe Workflow

Use this when a character must wear the same outfit in every scene.

1. Add the outfit to the asset base (upload a photo of the garment, or `Create from a prompt` with kind `Wardrobe`), or attach a reference photo when adding the character.
2. On the character card, `Add outfit` and select the asset (up to 3 per character). Saving regenerates the character's image and the scenes they appear in.
3. `Resume Generation > Images + Audio only` to review the new look before spending render time.
4. `Resume Generation` with a runtime to re-render the affected clips and the final video.

### Swap the Narrator Voice Workflow

Use this when the script is right but the narrator is not.

1. On the canvas, open the `Narrator` card and click `Change voice`.
2. Pick a voice native to the script's language, a `Global` voice, one of `My voices`, or `Automatic`. Or `Browse thousands more voices` and pick one from the `Voice library` (it is saved to your shelf at the same time).
3. Read the `Change narrator` confirmation: it tells you how many scenes are re-recorded and the approximate credits. Images and rendered clips are kept.
4. Click `Change and re-record`. The narration is re-recorded straight away.
5. `Resume Generation` to re-render only the clips whose new narration no longer fits, and to stitch the final video again.

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
5. Check the designed poster and first frame on the canvas. Rewrite a prompt and regenerate the images if needed.
6. Use `Resume Generation` > pick a runtime > `Add to render queue` to render the animation.

### Product Ad From a Shop Page

Use this when you sell something online and want a creator-style ad for it.

1. Open `UGC` mode. In the `Assets` pill, paste the product's page into `Product URL` and `Import` it. Open the product card to check the photos, the name, the price, and the key points.
2. Optionally add photos of the places to film in and mark them `Location`, pin a creator with `Characters` (the first one leads), and pick a `Voice` and an `Angle`.
3. Describe who it is for and the offer, and send. Refine the ad plan in chat ("punchier hook", "add a demo shot", "shorter lines").
4. `Generate`, then turn on `Generate storyboard only` and `Create storyboards` to check every shot as four sketches before paying for video.
5. On the board, fix what needs fixing: open a scene to change its line, camera, or place, play its read line, or `Redraw` a storyboard.
6. `Resume Generation` > `Generate video`. Render a complex scene on `Pro` from its clip node if Lite is not enough.
7. Add on-screen texts in the scenes' `Texts` tab and pick the transitions, then `Stitch Final Video` and download the ad from the `Output` node.

### Crazy Hook Ad

Use this when you want an ad that stops the scroll.

1. Open `UGC` mode and switch on `Crazy hook`. Pick a `Hook idea` (or leave `Surprise me`) and a length.
2. Attach clear photos of the product (no people) and describe what you sell and who it is for.
3. Read the `Hook` block of the plan (the event, the reveal, and the twist) and refine it in chat ("a bigger event", "a faster reveal").
4. Generate with `Max` if the chaos needs more believable physics, or render the key scene alone on `Max`.

### Edit a Project by Asking

Use this when you know what you want changed but not where the button is.

1. Open the project and press `Ctrl+K` (`⌘K` on a Mac), or click `Edit with AI` in the bottom-right corner.
2. Ask for the change in plain words, several at once if you like ("regenerate the image of scene 2, make scene 3's narration more dramatic, and turn captions on").
3. Read the timeline under the answer to see what it did. Before rendering video or anything destructive it quotes the cost and waits for your yes.
4. Keep working on the board while it works; `Stop` cancels the current turn.

### Keep Your House Style With Skills

Use this when every video should sound and be structured the same way.

1. Open `Settings > Skills` > `New skill` and describe the rule in your own words ("open with a bold question, short sentences, end with a call to action to my site"). The AI writes the skill and names it.
2. Group skills into sections (`Brand`, `Kids`, `UGC`…) if you keep several.
3. Switch them on from the `Skills` pill before you send a brief. They stay on for the next chats on this device until you switch them off.
4. In a project's `Edit with AI`, the skills the project was planned with are already on.

### Polish the Cuts With Transitions

Use this when the scenes are right but the joins feel abrupt.

1. On the canvas, find the `Transition` node between the two scenes and click `Change transition`.
2. Hover the tiles to preview them, pick one, set its `Length` (and direction for `Slide` or `Wipe`), and `Apply`.
3. Repeat for the other cuts, or ask `Edit with AI` to suggest transitions.
4. `Stitch Final Video`: only the final cut is rebuilt; no scene renders again.

## 35. Glossary

Terms used across this guide, in alphabetical order.

### Aificient Cloud

The subscription-backed render service, available on initial render settings and from `Resume Generation` for eligible scene videos. It uses credits and has its own queue, separate from local and rented GPU queues.

### Asset

A generated file such as an image, audio clip, scene video, or final video. Not to be confused with a project asset (see "Project Asset / Asset Base").

### Automatic Voice

The narrator setting that lets the service choose the library voice for the script's language and accent, honouring the `Automatic voice accent` rows in `Settings > Audio Config`. Shown as `Automatic` on the `Narrator` card and in the pickers.

### Cast

The characters that appear in a scene, shown as chips on the scene card and edited with `Edit cast`. Changing a scene's cast regenerates its image and video; narration is kept.

### Cloned Voice

A narrator voice created from your own recordings in `Settings > Voices`; how many you can keep depends on your plan. It appears under `Cloned` in the `My voices` tab of every voice picker, and any scene whose narrator names it is narrated with it.

### Crazy Hook

A UGC ad that opens on something impossible, an absurd event filmed like real footage, that reveals what you sell. A switch in UGC mode, with its own `Hook idea` and lengths of 10–30 seconds.

### Daily Credits

A free top-up that accounts on a plan or trial can claim once per calendar day (reset at 00:00 Europe/Madrid) from the sidebar card, the daily popup, or the out-of-credits card. It always takes a click.

### Edit with AI

The in-project assistant in the bottom-right corner of the canvas (`Ctrl+K` / `⌘K`). It changes the open project when you ask, runs the same actions as the buttons, asks before anything costly, and can spend credits; not to be confused with the Support Assistant.

### Final Output

The completed video shown in the Output node.

### Finished Cut

A UGC scene's clip with its captions and on-screen texts burned in. The final ad is stitched from the finished cuts (or the plain clips where none is needed).

### First Frame

The opening image of a poster animation, derived from the finished poster. The animation runs from the first frame back to the poster.

### Free Trial

A time-limited trial of one plan: save a card, receive the trial's credits at once, pay nothing until the trial ends. Its buttons carry a gift-box glyph.

### Generation Run

A record, kept by the service, of one project being generated on one device (this app, the web, or the iPhone app). Other devices show it as a `Generating on <place> N%` chip and wait for it; only the device running it can stop it.

### Global (Library) Character

A character that lives in your library and is referenced by a project rather than owned by it. It shows a `global` badge on the canvas and cannot be edited, deleted, or dressed from inside a project.

### Guidance (CFG)

Classifier-Free Guidance: a setting that controls how strictly the AI follows your prompt, where higher values mean stricter adherence and lower values allow more creative freedom. Video guidance (Video CFG) applies to visual generation, and Audio guidance (Audio CFG) applies to sound generation.

### Headroom

The third bar on a GPU rental tier card: how much of the model stays on the card instead of streaming over PCIe each step. Cards under about 40 GB stream and are slower, especially at 1080p.

### History Project

The multi-scene kind of project: a concept becomes a script, scenes, images, narration, clips, and a stitched final video. It is what the `Story` chat produces (including when it brainstorms first).

### Introduction Tour

The seven-step guided walk through the home screen that starts for new accounts and can be replayed from `Settings > General`.

### iPhone App

The native iPhone version of Aificient: the same account, projects, characters, voices, skills, credits, and plan, with Story, Poster, UGC, and Character modes, `Edit with AI`, per-cut transitions, cloud rendering only, Live Activities on the lock screen, and plans bought through the App Store. GPUs and publishing stay on the desktop and the web.

### Lead

The first creator pinned to a UGC ad. The lead speaks on camera, and the ad's voice is shown on the lead's card and changed from its `Edit` modal.

### Lead-in (`Before the line`)

Up to 3 seconds of action a UGC scene plays before its spoken line starts, set in the scene editor. It is part of the prompt and the duration, so changing it re-renders the clip.

### Live Activity

The iPhone lock-screen and Dynamic Island card that follows a project's generation step by step and opens the project when tapped.

### Narration

The spoken audio generated from the scene script.

### Narrator Card

The canvas card between the cast and the scenes that shows the project's narrator voice and offers `Change voice`. Changing the voice re-records the narration; scene images and rendered clips are kept.

### Needs Review

The red state of a UGC scene whose prompt may still count on an image or place that was deleted, or that names an image it no longer sends. No video renders until it is fixed or marked `Looks right`.

### Outfit (Wardrobe)

The project assets a character wears, shown as chips on the character card and capped at 3 per character by the service. They are attached to the image model when the character's reference image is rendered, so the look follows the character into every scene.

### Poster Plan

The output of a poster chat: a title, up to three prompts (poster, first frame, video), the attached references, and the clip's duration and aspect ratio. Creating a project from it is what starts generation.

### Poster Project

A project that animates one poster into a short clip (5–15 seconds) with model-generated sound. It has no scenes, captions, or stitch step; the rendered animation is the final video.

### Project Asset / Asset Base

A reusable reference image in a story project (a product, a wardrobe item, a location, a prop) that scenes and characters reference by id; the asset base is the `Assets` card on the canvas that holds them. Assets come from the composer's `Assets` pill, the script planner (`AI planned`), `Upload an image`, or `Create from a prompt`; uploaded assets are ground truth and are never regenerated, generated ones can be re-rolled, and a `pending` asset has no image yet and renders at the start of the next run.

### Project Variant

An editable project-only copy of a library character, created with the `Project variant` button. The library entry and every other project using it stay untouched.

### Raw Clip

A generated scene video before final stitching.

### Reference Budget

The five slots a poster's reference images and pinned characters share. Each character counts as one slot, and characters have their own limit of three.

### Render Queue

The per-GPU line of pending work: each scene video is a job that waits its turn on the GPU it was assigned to, so multiple projects can share a GPU and a single project's videos can be split across several GPUs. The final stitch is not a GPU job; it runs locally in the app.

### Runtime

A local or rented GPU environment used for video rendering. It runs the MiniMax-H3 engine, the same one Aificient Cloud uses, and needs a 24 GB GPU (plus 24 GB of system RAM for the local runtime).

### Saved Voice

A voice from the `Voice library` that you bookmarked (`Save voice`) or picked for a field. Saved voices appear under `Saved` in the `My voices` tab of every picker, speak every language, and are listed in `Settings > Voices > Saved library voices`, a shelf with a cap set by the service.

### Scene Image

The still image used as the visual basis for a scene.

### SFX

The sound effects and ambience the video model composes into each clip's own soundtrack. There are no separate SFX tracks or cues to edit; the `SFX volume` setting controls how loud this soundtrack plays under the narration.

### Skill

A standing instruction the AI follows in every chat where it is switched on: your tone, structure, or rules. Written by the AI from your description in `Settings > Skills`, switched on from the `Skills` pill (up to 10 at once), and kept with your account.

### Read Check

The comparison the service runs between a delivered UGC clip and its line. A word that differs shows as `The read slipped: …` under the clip; it is a warning only, and `Regenerate` gets another take.

### Spoken Line (Read Take)

The voice's reading of one UGC scene's line, made before the clip. The clip lip-syncs to it word for word, the scene lasts as long as the line, and you can play or re-read it on the scene card.

### Stitch

The process of combining scene clips into the final video: each cloud scene's narration is mixed over its clip's soundtrack, each narrated scene is trimmed to end just after its voice, and the scenes are joined with each cut's transition (or the project's crossfade). It runs locally in the desktop app once every scene clip is ready; only one stitch or caption burn runs at a time, and the others wait in a local queue.

### Storyboard

Four quick sketches of one UGC scene's shot (opening frame, two key moments, final frame), drawn for a small charge so you can check the shot before paying for its video.

### Support Assistant

The in-app help chat, opened with the `Ask AI` button, that answers questions about using the app based on this guide.

### Transition

How a scene comes in after the one before in the final video: a hard cut, a crossfade, a dip to black, a wipe, a zoom, and nine more. Set per cut on the canvas's `Transition` nodes; changing one rebuilds only the final video.

### Trim (UGC)

A cut of up to 10 seconds from the start or the end of a UGC scene's clip, applied in the final video only. The clip stays whole, nothing renders, and `Stitch Final Video` rebuilds the cut; at least 1 second of every scene is kept.

### UGC Ad

A short creator-style ad for a product, a course, or an event: one to ten scenes with beats, a creator on camera (or a voice off screen), rendered on Aificient Cloud from your photos and the voice's reading of each line, then captioned, given on-screen texts, and stitched. Made in `UGC` mode; listed under `UGC ads`.

### Voice Library

The explorer of thousands of narration voices, opened with `Browse thousands more voices` from any voice picker or `Explore` in `Settings > Voices`. It filters by language, accent, gender, use case, and sort order, previews each voice, and lets you pick or save it.

### Welcome Credits (Gift Trial)

The small credit gift a new account starts with, enough for one or two Lite 720p cloud clips. Renders made on gift credits carry a small Aificient watermark, and new projects default to `Lite`.

### What's New Card

The once-per-account announcement shown at startup when a feature ships. See "Updates".

### Write-in

The option in a scene's cast or asset picker (`Write them into the scene`, `Save and write in`) that has the AI rewrite the scene's description and character reference so a newly added character or asset is actually in the shot, not only attached as a reference. It works the other way too (`Take them out of the scene` / `Save and rewrite` writes a removed one out of the text, and `Rewrite without <name>` does the same for every scene after a delete); it is a charged scene rewrite, and no scene is added.
