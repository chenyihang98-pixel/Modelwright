<h3 align="center">
  <a href="RELEASE-NOTES.md">简体中文</a> &nbsp;|&nbsp; English &nbsp;|&nbsp; <a href="RELEASE-NOTES.ja.md">日本語</a>
</h3>

# Changelog

The installer updates itself. For the portable build and the zip, download the new version from [Releases](https://github.com/chenyihang98-pixel/Modelwright/releases).

## 0.1.29 (2026-11-13)

**Improved**
- For a rigged character, “Rig & animate” now starts with the motions on your computer, which cost nothing; cloud motions say they cost credits
- In the simple view, what you changed in the advanced view (no rigging, no local optimisation, saving as a new version of an old asset, custom parameters) is listed in the generate panel, each with a way back
- The Motion studio says which motions a baked version already has in its file
- Shortcuts and the uninstall entry made by the English and Japanese installers describe the app in the language you installed

**Fixed**
- In Japanese, the messages of key tests, dropped pictures, link imports and parameter checks were in English
- Japanese wording that said the wrong thing: Tripo's sign-up note, the Hunyuan motion hint, Unity's “refresh” written as “update”
- The language picked in the installer was lost when the settings file happened to be in use during the first start

## 0.1.28 (2026-11-13)

The Unity plugin is now 0.1.34: press “Upgrade” on the Engine page.

**New**
- Colour fix in Texture: paint on the model to repair wrong colours, no credits needed
- Simple view: only the common modules and options by default; “Advanced” at the bottom left shows everything
- Japanese interface. Three installers — Chinese, English, Japanese — and the language you pick while installing is the app's language

**Improved**
- In the simple view, when the project has a glTF importer, a character sent to Unity in one click goes as GLB without stopping to ask about the format
- Steadier body when switching between walk and run, starting and stopping
- Tripo keeps cloud results for 7 days: tasks show the date, and expired ones fall back to the local file

**Fixed**
- A model's own motions looked different in the preview and after export
- In the range, the gun's stock came out of the character's back when aiming and walking backwards

## 0.1.27 (2026-11-10)

The Unity plugin is now 0.1.32 — click "Upgrade" on the Engine page.

**Added**
- Motion studio: "Jog" can be picked by hand. Still being tuned, not among the default motions yet

**Improved**
- Walk footfalls follow the real shoe sole, so feet no longer sink into the ground
- Switching between walk and run in the Unity play test keeps the feet in step

**Fixed**
- Sending a character again cleared skirt and face meshes that were still in use in Unity
- Baked and exported motions did not match what the Motion studio showed
- The character walked sideways in the Unity play test
- The body jerked when starting to run and when stopping

## 0.1.26 (2026-11-09)

The Unity plugin is now 0.1.29. Characters whose skinning it changed earlier are restored once you upgrade the plugin and send them again.

**Improved**
- The animation bar marks which motions came with the model file
- The quality panel and the task result card have a "Check seams" entry

**Fixed**
- The Unity plugin re-skinned characters with no skirt as if they wore one. It now leaves the model's own skinning alone by default
- Feet sank into the ground when switching between walk and run
- Sending with "Into the playground" ticked hung for ten minutes
- The first send marked the open scene as modified

## 0.1.25 (2026-11-08)

**Improved**
- The stride slider's upper limit now depends on how far each rig can step
- Walks outside that range cannot be saved or exported, and the app says why

**Fixed**
- With the stride set too large, the pelvis sagged and the legs could not reach the ground
- "Unify seam weights" stuck adjacent separate patches together. Seams along open edges are now left alone

## 0.1.24 (2026-11-08)

**Improved**
- The seam card says how many seams lie on open edges and were left unfixed
- Old walks do not change on their own; they upgrade only when you pick "New" under "Motion formulas" and save

**Fixed**
- Characters with shortish legs lifted the foot and then dropped it hard just before landing, worse at larger strides
- "Unify seam weights" stuck skirts, capes and clothes together

## 0.1.23 (2026-11-08)

Two versions' worth of changes; 0.1.22 was not released on its own. The Unity plugin is now 0.1.26 — click "Upgrade" on the Engine page, then send your existing characters once more.

**Added**
- Motion studio: "Complete base motions (local)" gives a rigged character idle, walk and wave
- "Weight fix" has "Unify seam weights", which fixes the black seams at the shoulders and crotch that split open as soon as the character moves
- The concept image dialog can have Tripo draw four views from a single front image
- If the network drops or the app closes during a paid image job, "Pick up the result" in the dialog gets it back without generating again

**Improved**
- Walk was redone: knees bend forward, the swinging leg is no longer stiff, feet plant firmly and arms hang naturally
- In the Playground and the Range, walk and run are paced to the stride speed, so feet slide much less

**Fixed**
- "Bake into a new version" pulled models with an adjusted size or origin back to the preset height
- On assembled characters, the legs tore the tail and skirt apart when walking or running

## 0.1.21 (2026-11-01)

Took one image all the way from generation into Unity and fixed what broke along the way.

**Fixed**
- Rigging a Tripo humanoid with quads returned only an FBX, which could not be baked. Triangles are now the default
- Tripo-rigged humanoids came into Unity facing sideways. They are now turned to face forward automatically
- On the first shot while aiming in the Range, the upper body jumped to the firing pose in a single frame
- Baked one-shot motions (fire, reload, jump) looped in Unity
- A character with no tail could still save a motion as a "Tail" sway
- After leaving version compare, the Motion studio stayed stuck on "Reading the skeleton…"
- Pressing E in the Playground did nothing for motions you named yourself

## 0.1.20 (2026-10-29)

The Unity plugin is now 0.1.22 — click "Upgrade" on the Engine page.

**Improved**
- In the Range, the support hand holds the gun while aiming and moves away to reload
- The Playground prefers the plain idle, walk and run instead of holding an aiming pose with empty hands

**Fixed**
- Turning the view right next to a crate in the Range made the camera lunge up behind the character, with the backpack covering the crosshair
- The pose jerked on the first hip-fire shot, on a quick tap of W and on a jump while running
- After landing, characters with no jump motion played idle for two seconds and then froze
- Pressing Tab while the mouse was locked left the character walking without stopping
- In the Range, nearby energy cells could not be hit and rifle bullets passed through walls
- In Unity, when two motions shared a name only one of them could be played

## 0.1.19 (2026-10-28)

The Unity plugin is now 0.1.20. For characters already sent into a project, upgrade and then click "Assets › Modelwright › 重新生成材质与预制体 (Rebuild Materials and Prefab)" in Unity.

**Added**
- Meshy can generate a motion from one sentence and apply it straight to the current rig
- Motion studio: "Update imported motions from their files" recalculates old motions that were imported crooked, in one click
- The Range has training settings: switches for AI sentries and for an invincible character

**Improved**
- Tripo humanoid rigging defaults to v3.0 and outputs GLB (its FBX has no textures)

**Fixed**
- Imported Mixamo motions leaned the upper body to one side
- Play-once motions such as a knockdown looped in the viewport and in Unity
- Left click did not fire while holding right click to aim
- Hunyuan models came into Unity pure white
- Meshy-rigged models were wrongly reported as "the skin stretches 100x"

## 0.1.18 (2026-10-28)

**Improved**
- Shift now toggles walk / run with one press instead of being held down
- You can fire and reload while walking; only the upper body plays the motion
- The default view sits a little higher, so the crosshair no longer lands on the ground in front of you
- Models that only have their own built-in animations can also be exported as an animated GLB

**Fixed**
- Left click did not fire in the Range
- Some models were scaled up nearly a hundred times on entering the Range
- A motion that was not saved was still reported as saved

## 0.1.17 (2026-10-27)

**Added**
- "Export an animated GLB file…" packs the model and all its motions into one file, and works for FBX characters too
- Motion studio: new "One part" template that moves just an arm, a leg, the head or the tail

**Improved**
- The Range now starts when you click the view and pauses on Esc or when you switch to another window
- Walk and run play at the actual movement speed, so feet slide much less

**Fixed**
- Characters walked sideways in the Range and the Playground
- While running or strafing, the character darted forward and then jumped back
- After dying and respawning, the body stayed tilted
- Imported motions held the head too low

## 0.1.16 (2026-10-27)

The Range has been redone.

**Added**
- The field is now a round neon arena with ring targets, pop-up targets, moving targets and energy cells that explode
- Four sentry bots chase you and slash at you; knock one down for points and it comes back a few seconds later
- The character has health: at zero it goes down, then respawns at the start a few seconds later
- The Range can now use backward walk, left / right strafe and knockdown motions

**Fixed**
- The HUD (score, ammo, crosshair) never showed, in the Playground as well
- A / D were swapped left and right in the Range and the Playground
- The muzzle pointed backwards and down. It now points at the crosshair when aiming and firing
- The camera sat too close, with the character filling half the screen

## 0.1.15 (2026-10-27)

New module: "Range" — bring your own character in for target practice.

**Added**
- The Range has ring targets, silhouette targets, moving targets and barrels, and seven weapons from a pistol to a katana
- Motion studio can import Mixamo FBX / GLB motions and fits them to your rig automatically
- Imported motions play in the viewport, the Playground and the Range, and GLB versions carry them into Unity too

**Improved**
- Assembly bench: ± scaling, Q / E to turn 90°, box select, align on an axis, magnet snapping and snap to the neighbouring part
- In "Parts", when outer clothing is not split off on its own, the body image is drawn with the clothes on

**Fixed**
- The "Parts" list was empty when the Assembly bench opened or switched to another assembly
- Characters generated in parts had a black line down the inside of both legs
- Uploads failed after switching the API key region

## 0.1.14 (2026-10-26)

**Added**
- The Asset library has folders (one level only): rename them, change the cover, and drag asset cards straight in
- Generated parts are filed into the character's folder automatically, and older assets are sorted once after upgrading
- The Asset library page in Settings has "Where files live": see the path and disk use, clear the cache, or delete all local data
- Assemble by hand and the Motion studio's joint corrections support Ctrl+Z to undo and Ctrl+Y to redo
- Unity folder naming accepts `{Folder}`, so everything for one character goes into the same subfolder

**Improved**
- The uninstaller asks whether to also delete app data and the asset library

**Fixed**
- Temporary files from part assembly piled up in the system temp folder and were never cleaned up

## 0.1.13 (2026-10-26)

**Added**
- Back button in the top-left corner; Esc, Alt+← and the mouse back button go back too
- With a dialog or menu open, or while typing, Esc closes that first
- Leaving with unsaved changes to an API key or a joint mapping asks first
- Going back only changes the page: generations already submitted and anything saved are not undone

## 0.1.12 (2026-10-26)

New module "Parts": generates a character as separate head, hair, body and clothes, then puts them together. A whole-body generation is an empty shell under the hair and clothes; building it in parts avoids that. This is a first version, and the assembly still needs adjusting by hand.

**Added**
- Workspace gets "Parts": tick a few options and it tells you whether to split, into which parts, and roughly how many credits it will cost
- Two images are drawn for each part automatically, one for the shape and one for the texture; a bad one is redrawn, at most twice
- Generated parts are checked automatically for holes, wrong proportions, a second face on the back of the head and the like
- Auto-assembly gives a starting point; then adjust each part's position, scale and rotation by hand, with the viewport following live
- Tripo API keys for the China and global regions can be stored side by side, each with its own test and balance

**Improved**
- Post-processing also trims stray flaps and closes small holes
- Result downloads resume a few more times when the stream drops, so they fail less often

## 0.1.11 (2026-10-25)

**Improved**
- "Showcase / cinematic" no longer shrinks images sent to Tripo to 1024; they go up at up to 2048
- "Showcase / cinematic" asks for the maximum face count by default, and uses 8K textures when the texture size is set to 8192

**Fixed**
- Tripo FBX characters with motions hunched over and had their face pulled out of shape as soon as they stood still
- A quick tap of Space in the Playground sometimes did not jump
- Designed motions did not line up after baking when bone names had a dot (e.g. UpperLeg.L)
- After submitting, the generate panel's input area was empty but still warned about too few views

## 0.1.10 (2026-10-25)

New module "Motion studio": pick a template, drag a few sliders, and a rigged character has a motion.

**Added**
- Six templates: idle, walk, run, jump, wave, bow
- Works out whether each bone is a hip, leg, arm or tail, so humanoids and quadrupeds both work; wrong guesses can be corrected by hand
- After "Save motion" the viewport and the Playground play it right away; GLB versions can "Bake into a new version", which goes into the Animator when sent to Unity
- The Playground plays your designed motions first; one with the same name overrides the clip in the file

## 0.1.9 (2026-10-25)

The app now has a built-in "Playground": the current model is the player, so you can run and jump around to try it out.

**Added**
- "Playground" is on the left of the Workspace: WASD to walk, Shift to run, Space to jump, E for an action, R to restart
- Idle, walk, run and jump are matched up by clip name; a model with no motions can still glide around
- Swap in another version of the asset, or any model in the asset library, at any time

**Fixed**
- Versions made by Neuron rig were labelled "Static" and were treated as static models when sent to Unity
- Neuron rig took a bump on a rock for an arm, a tuft of hair for the head, and split a chair into parts

## 0.1.8 (2026-10-25)

New feature "Neuron rig": characters that are not humanoid can be rigged too. The Unity plugin is now 0.1.8 — click "Upgrade" on the Engine page.

**Added**
- "③ Neuron rig": finds the movable parts from the model's shape and rigs them, e.g. a ball with four hands or a quadruped with a tail
- The rig comes with three clips (idle, walk, action); how each part swings, and how much, can be changed
- Tick "Into the playground" when sending to Unity and the import opens a scene where you drive the character with WASD
- "② Animate" takes external motion FBX files (on Mixamo pick FBX for Unity, Without Skin); they play even on a different skeleton

## 0.1.7 (2026-10-13)

The Unity plugin is now 0.1.7 — click "Upgrade" on the Engine page.

**Added**
- Face smoothing: eye-socket pits and bulging pupils on anime faces are smoothed out, in post-processing, the preview and Unity
- When an image is mistaken for a turnaround sheet, click "Not a sheet" and that image is not flagged again

**Improved**
- Hunyuan motion FBX files come out enlarged and torn in Unity, and the fault is in the files themselves. Import now warns about it and suggests Tripo / Meshy motions instead

**Fixed**
- Knees poked through the front of the skirt when a skirted character walked
- Hollow long dresses with no lower legs underneath were not detected

## 0.1.6 (2026-10-13)

**Added**
- Concept image dialog: new "Custom instruction" sends the text in the note box to the image model as written, with the selected image as reference

**Improved**
- Manual "Split a turnaround sheet" marks two pieces it is not sure about as a guess

**Fixed**
- A single character image was mistaken for a multi-view turnaround sheet, and the "Make a four-view sheet" button disappeared with it

## 0.1.5 (2026-10-12)

The Unity plugin is now 0.1.5 — click "Update plugin" on the Engine page. Send skirted characters that are already in Unity once more and the skirt behaves.

**Added**
- Target platform gets "Showcase / cinematic": top geometry detail and 4K textures, so fingers and strands of hair come through
- In Workspace "Image", pick a front image and click "Make a four-view sheet" to get four views in the same pose
- Concept image dialog: new "Resolution" option, 1K / 2K / 4K
- Pre-flight warns when a back or side view is drawn mirrored, and "Mirror this view" fixes it in one click

**Improved**
- Sheet splitting was rewritten: 2×3 six-view sheets and sheets with labels or close-up boxes can be split, and front, back, left and right are recognised and slotted automatically

**Fixed**
- Skirts flipped up like a board when a character ran; fixed in Unity and in the app's preview
- Sending to the same project again reported "asset name does not match the file name"

## 0.1.4 (2026-10-12)

Only the Unity plugin changed: it is now 0.1.4 — click "Update plugin" on the Engine page. Characters with motions that were already sent need sending once more. Hunyuan FBX files with motions still come into Unity at the wrong size; not fixed in this version.

**Fixed**
- Characters with motions vanished the moment Play mode started (in both 0.1.2 and 0.1.3)
- After "Update the existing one", a model whose skeleton had changed kept the rotations of the old bones

## 0.1.3 (2026-10-12)

Tencent Hunyuan's old API was shut down, so this version moves to TokenHub: Hunyuan now needs a TokenHub API key, and each model has to be enabled under "Enablement" in the console first. The Unity plugin is now 0.1.3.

**Added**
- Tencent Hunyuan now runs through TokenHub: text-to-3D, image-to-3D, multi-view, texturing, retopology, rigging and format conversion all work
- Hunyuan can add motions: 48 presets, or pick "Motion described in words" and write one sentence
- In Settings and the first-run guide, each provider has a "How to connect" section that shows how to get an API key
- When a Hunyuan model is not enabled or its quota has run out, the task stops and tells you which console page to open

**Fixed**
- The placeholder clip that comes with a Meshy rig became the default animation state in Unity
- Sending a Meshy version with motions to Unity wrongly reported "No GLB counterpart"
- Hunyuan prices are converted to CNY only for keys confirmed to be from the China site; others show credits only

## 0.1.2 (2026-10-09)

Characters with motions now move as soon as they arrive in Unity. The Unity plugin is now 0.1.2.

**Added**
- Characters with motions get an Animator set up automatically when sent to Unity, idle by default; a controller you swapped in yourself is not overwritten

**Improved**
- Rig and animation request parameters are written to the log (without the API key), which makes problems easier to trace
- A motion that does not match the rig is stopped before submitting, so no task runs for nothing

**Fixed**
- Motions could not be added to a biped after rigging. Humanoids and quadrupeds now each use the matching rig model, and a wrong choice is corrected automatically
- Skeletons with Mixamo naming could not take motions on Tripo. The default is now the provider's native naming, and picking Mixamo shows a warning
- Picking several motions at once kept only the last one. Output is now FBX, with all of them included

## 0.1.1 (2026-10-08)

Upgrading from 0.1.0 takes one manual install: download the installer and install it into the same folder; the asset library, settings and API keys are kept. After that, updates are automatic.

**Added**
- The installed version updates itself (turn it off under "Settings → Language & about"); the portable edition and the zip do not

**Improved**
- A cloud rigging error no longer fails the whole job: it carries on as a static character, and rigging can be retried later in the Workspace
- When a result download times out and retries, the progress card shows "retrying (n / 3)"

**Fixed**
- Models sent to Unity 6 came out white, with no textures
- Unity 6 showed .meta warnings in the Console
- "Update the existing one" placed a duplicate of the model in the scene

## 0.1.0 (2026-10-07)

First public release.

- Four kinds of input: text, image, multi-view and batch. Works with Tripo / Meshy / Tencent Hunyuan, using your own API keys
- Presets by asset type, target platform and art style, which work out face count, texture size, LODs and colliders
- Images, parameters, cost and balance are checked before any credits are spent; requests that charge credits are never resent automatically
- Local post-processing: decimation, LODs, colliders, pivot and size correction, texture packing
- Asset library: version history, Chinese search, recycle bin, export to GLB / OBJ / STL / PLY
- One-click send to Unity 2022.3 / Tuanjie 1.x / Unity 6, with materials and a prefab created and placed in the scene
