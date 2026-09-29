## v3.0.415 — 2026-09-29

Reliability and accuracy fixes across Mail, Microsoft 365, Teams and Reminders; sharper permission and connection diagnostics; a tray stability fix; and you can now publish your saved recipes to the community.

## v3.0.414 — 2026-09-28

Easier setup: grant Full Disk Access, Screen Recording and Accessibility by dragging Local MCP into System Settings, with the window placed right where you need it. Automation is now asked only when an app is first used, and can be granted anytime from the menu bar. New Shortcuts tools let your AI list, view and run your Apple Shortcuts. Uninstalling now removes Local MCP's entries from System Settings. Plus many reliability fixes across Mail, Calendar, WhatsApp and permissions.

## v3.0.413 — 2026-09-21

Excel: sheet_name now selects the sheet you asked for — writing to a sheet that does not exist no longer lands in the first one. Services you turn off in the tray now also release the macOS permission they were given. Reminders and Calendar permission checks are more reliable after an update.

## v3.0.412 — 2026-09-20

Excel: sheet_name now selects the sheet you asked for — writing to a sheet that does not exist no longer lands in the first one. Services you turn off in the tray now also release the macOS permission they were given. Reminders and Calendar permission checks are more reliable after an update.

## v3.0.411 — 2026-09-19

Stability and reliability of the release pipeline. No changes to how LMCP works for you: same tools, same behaviour.

This version exists so the publication path itself is verified end to end — including the surfaces that can only be exercised by publishing for real.

## v3.0.410 — 2026-09-19

Signal and Telegram proxies now ship fully signed, so they start cleanly on macOS.

Perplexity and Raycast are detected automatically — Raycast on Windows too.

A direct link to the web-AI setup guide sits next to your connection URL.

The Agent Mesh is on by default.

Windows: install attribution survives a redirected Downloads folder.

## v3.0.386 — 2026-09-10

WhatsApp vuelve a funcionar. Los envíos fallaban en todas las Macs con la cuenta vinculada: WhatsApp estaba rechazando nuestro cliente por versión. Actualizado.

Conectar Mail desde la barra de menú. La fila de Mail ahora te dice en qué estado está y te ofrece conceder el permiso ahí mismo, en vez de dejarte sin camino. Y cuando no pudo medir tus cuentas, lo dice — antes afirmaba que no tenías ninguna sin haberlas contado.

Tus notas se cuentan sin pedirte permisos de más. Si ya diste Acceso Total al Disco, dejamos de pedirte Automatización para algo que no la necesita.

ChatGPT con plan gratuito ya no queda bloqueado. El auto-connect dejó de frenarse antes de intentar: ahora prueba y, si algo falla, te dice el motivo real.

Un permiso concedido ya no se reporta como denegado. Si la consulta al sistema tardaba, contestábamos "no tenés permiso" a quien sí lo tenía. Ahora un fallo transitorio dice "no sé", que es lo que efectivamente pasó.

Al conectar tus apps ya no se te abre Notes en la cara. El permiso se sigue pidiendo igual, pero la app se lanza oculta.

## v3.0.385 — 2026-09-09

Connecting ChatGPT is clearer about what happened. When there was no connector to remove,
the app now says so instead of reporting that it could not verify the step — so a clean run
no longer looks like a failure.

Mail is more reliable with Exchange accounts. Listing, reading and searching no longer stop
silently when a mailbox cannot be resolved: the app tells you which account and folder it
could not reach, and folder listings stay complete when a shared or on-device mailbox is
involved.

Settings now includes an Auto-launch switch. AI clients can start LMCP for you, and you can
turn that off if you would rather open it yourself from Applications. It only affects
*starting* LMCP — it does not stop or limit an LMCP that is already running.

Under the hood, the app reports more about its own memory use, so recurring slowdowns can be
traced to the part of the app responsible for them. These measurements are counts, sizes and
durations only.

## v3.0.384 — 2026-09-08

Files in the cloud
Word documents and PDFs that live in iCloud or another cloud provider and are not downloaded to this Mac now open instead of failing. When a folder genuinely cannot be listed, the message says why.

Mail and calendar
Times coming from Microsoft 365 are shown in your own time zone, with the zone named, so an event no longer appears hours off. Replying to an email can now save a native draft without sending it.

Settings
A service that is switched on but not yet configured says exactly that, instead of appearing connected.

Other improvements
Various fixes to setting up web AI clients, including clearer handling of sign-in flows that an embedded browser window cannot complete.

## v3.0.383 — 2026-09-07

El conector de ChatGPT ya no depende del idioma de la interfaz: el lector del interruptor de Developer mode reconoce el control en cualquier idioma, así que la conexión deja de fallar con "no encontramos el interruptor" en cuentas que no están en inglés. El diagnóstico que llega a soporte incluye ahora el idioma de la interfaz.

## v3.0.382 — 2026-09-07

Mail: moving and deleting messages no longer times out or reports "cooling down" on small batches; writes are queued with a clear, immediate reply. create_draft can save a native reply (reply_to_message_id, reply_all, text or HTML) to Drafts without sending. Automation permission for Mail is only marked revoked after two confirmed denials, background checks no longer probe Mail every 5 minutes, and a real revocation opens the permissions dialog again. Excel: excel_create and excel_write_cell write real numeric cells, so SUM and formulas work. Microsoft 365: onboarding retries once with a fresh device code when Microsoft rejects it after a passkey, with a clear message. OmniFocus installed from the Mac App Store is now recognized (no more "Requires OmniFocus Pro" on Pro). Slack: diagnostics report where Slack's own session was searched. Plus: Notes trash handling, terminal working-directory safety, Signal reads with empty senders, M365 readers show local time with its zone.

## v3.0.381 — 2026-09-06

Connect to ChatGPT works again. The Developer mode step that used to stop with "settings page didn't load" now completes.

Teams is more robust. A single message with a date the system cannot display no longer breaks listing or reading chats, and accented text comes through intact on every platform.

Agent Mesh stays accurate. Agents remain visible while they work, and the status panel explains itself when the mesh is off or the settings file cannot be read.

Setup tells the truth about Claude Code. If another install shadows the one you configured, the app says so instead of reporting it as configured. Mail moves only name folders that were verified.

## v3.0.380 — 2026-09-01

Updates are safer. If an update is interrupted, your working version is kept until the new one is verified — the app can no longer be left without a client installed.

Setup remembers what you already did. Microsoft 365 sign-in and the permissions you grant now survive a restart instead of asking again.

Mail and Teams fixes. Messages are sent from the account that owns the conversation, and mailbox lookups resolve correctly across multiple accounts.

Steadier under load, with faster reconnection after a network drop.

## v3.0.379 — 2026-08-29

Fixes for spreadsheets, reminders, email, and cloud files

Opening a PDF or Office file stored in OneDrive or iCloud Drive no longer stops Local MCP when the file has not finished downloading. When a mail request takes longer than expected, Local MCP now tells you whether Mail is stuck or simply working through a large mailbox, and suggests narrowing the search instead of restarting Mail. Requests that used to stop responding now come back with an answer, and a mail error no longer blames a permission you already granted. Reading an email now names its attachments, so you can save one without guessing. If a setup guide link does not open in your browser, the link is shown so you can copy it. And background components that quietly failed to update now report the failure and retry.

## v3.0.378 — 2026-08-28

Fixes for spreadsheets, reminders, and email

Writing a number to a spreadsheet cell now confirms correctly instead of reporting a failure that did not happen. Asking for your reminders returns what is still open — ask for completed ones when you want them. Email and command limits now tell you when a value was adjusted, and folder access messages no longer list every folder you have shared.

## v3.0.377 — 2026-08-26

New

• Delete notes, Google Drive files, and saved browser sessions. Local MCP could create notes but never remove them. Each deletion shows exactly what it will remove and waits for your confirmation.
• Windows: connecting an account now completes in the app instead of dead-ending in the browser.
• Windows is out of the waitlist — connecting from the cloud now works.

Fixed

Calendar
• Turning an all-day event into a timed one kept the whole day instead of the hours you asked for, and reported success anyway. Changing only the start time had the same problem.
• A repeating meeting showed up once instead of on every date it occurs.

Mail
• Moving a message to Trash or Archive in Gmail was refused.
• A message could be reported as moved while it was still in your inbox.
• New folders were reported as created when nothing had been created.
• Messages written with rich text were sent and saved with an empty body.
• A folder that could not be opened was reported as empty.
• Exchange accounts showed up unnamed in the account list.
• Mail search could report it was still indexing long after it had finished.

Notes
• Reading a note returned plain text, so bold, lists, and headings were lost each time a note was read and saved again.
• Deleted notes kept appearing in search results and could still be opened.

Reminders
• Folder lists could be served from an old snapshot without saying so.
• Moving a reminder to another list silently changed its identifier, breaking later updates.

Slack, WhatsApp and Teams
• Slack search returned results with no message text.
• WhatsApp search reported no results when it had found some.
• Local MCP could report WhatsApp as connected without having checked.

Privacy
• Listing Notion workspaces could include names and email addresses of people outside your account. It no longer does.

Screen, windows and the web
• Screenshots reported the same scale on every display.
• Saving a screenshot or recording to a new folder failed instead of creating the folder.
• Clicking a link in a web session could report the wrong page while it was still loading.
• Asking for a window that does not exist now says which windows are open.
• Keyboard shortcuts could leave a modifier key held down and swallow the next thing typed.

The menu bar app
• "Quit LMCP (until next login)" now stays quit.
• Declining a folder permission request left no trace on screen; it now tells you what happened and how to change it.
• When the Cloud Relay is unreachable, Local MCP now says why.
• Connecting ChatGPT no longer reports you as signed out while you are signing in, and the setup guide matches what ChatGPT shows.

## v3.0.376 — 2026-08-25

Mail search indexing is faster on large mailboxes and uses less CPU when it can't make progress.

## v3.0.375 — 2026-08-24

Connecting to ChatGPT is more reliable. Web automation now works with sites that expect real mouse input — menus and dropdowns open the way they do when you click them yourself. Approving a folder sticks: Local MCP no longer asks again for a folder you already allowed. Mail finds your mailboxes by name in any language, including localized inboxes. And when the menu bar icon has no room to appear, double-clicking Local MCP brings the window back instead of doing nothing.

## v3.0.374 — 2026-08-22

ChatGPT connects itself again — one click in the menu bar creates the connector, signs in, and authorizes, matching ChatGPT's redesigned interface. A new Reconnect button lets you refresh the connection anytime. Search your email by content: Mail search now looks inside message bodies, powered by a private on-device index. A single, faster engine now powers all web automation — pages that fail to load say so honestly, and sites with popups and file uploads work. Microsoft 365 stays signed in — fixed a bug that asked you to reconnect while your session was healthy. Hardened security: file writes go through one guarded path, and helper components verify their publisher before updating. Dozens of reliability fixes across Mail, Teams, Calendar, and Outlook.

## v3.0.373 — 2026-08-18

Mail is dramatically more reliable. Emails that appeared empty now load their full content — especially on Exchange and corporate accounts — and search handles accented text correctly. Teams no longer sends duplicate messages. WhatsApp unlinking asks for confirmation and completes cleanly. Notes browsing stays fast with large collections. Plus stability fixes across the board: fewer background crashes and more dependable connections for web-based AIs.

## v3.0.371 — 2026-08-14

Reading Microsoft Teams chats is cleaner — call and system events now show a short label instead of raw technical text. Connecting a web AI is smoother: the setup guide links open the right walkthrough, and the Microsoft 365 sign-in step is clearer and easier to tap. You can now invite colleagues to LMCP straight from the menu — pick contacts and send each a personal invite. Plus reliability improvements across Mail, Calendar and more.

## v3.0.370 — 2026-08-11

Local MCP is more reliable and more secure in this release.

• Connect Todoist and ServiceNow directly from the tray — no browser needed.
• The connection to web AIs (ChatGPT, Claude, Grok) now recovers on its own and stays steady through long sessions.
• Your contact email updates instantly across the app the moment you change it.
• Plus a broad set of privacy and security improvements under the hood.

## v3.0.369 — 2026-08-08

One slow call no longer holds up the rest: a heavy web page used to leave every other tool waiting behind it, and now they run side by side. Teams and Slack are dramatically faster to open — chats and channels that took several seconds now come back instantly. We also fixed a case where some tools returned an empty result instead of their data, and surveys from the team now arrive properly formatted in every client.

## v3.0.368 — 2026-08-08

Faster problem-solving: when something fails, LMCP now pinpoints the real cause — if Mail access was turned off it tells you exactly where to re-enable it instead of asking you to retry, and problem reports include recent tool names and error codes (never your content) so issues get fixed faster. Surveys and notices from the team now appear reliably right in your chat. Plus stability improvements across Mail and the status panel.

## v3.0.367 — 2026-08-07

Calendar: event updates no longer silently lose long notes — truncated previews are flagged and the full event can be read by id. Mail: search reliability improvements — breaker recoveries are no longer misreported as errors. Settings: the referral invite flow is now easy to find.

## v3.0.366 — 2026-08-07

This release focuses on reliability. Moving mail is now dependable: Local MCP only reports a message as moved once it can actually confirm it, and tells you plainly when it can't. Attachments that can't be found are reported instead of quietly going missing. Mail no longer stalls on large mailboxes — slow lookups now fail fast instead of hanging. Calendar events tell you exactly which calendar they landed in, so a hidden calendar no longer looks like a lost event. Relinking WhatsApp now recovers on its own when a previous session was still holding on, and it no longer claims to be connected when it isn't. Plus general stability improvements.

## v3.0.365 — 2026-08-07

This release focuses on reliability. Mail now handles a busy or syncing mailbox gracefully — searching, listing, moving messages, saving attachments, and creating drafts recover instead of erroring out. Opening an email that hasn't downloaded to your Mac yet returns a clearer result. Browsing files gives clearer messages for missing or mistyped paths. WhatsApp group details are tidier. Plus general stability improvements.

## v3.0.364 — 2026-08-06

WhatsApp status is more reliable, and reinstalling always works.

• WhatsApp connection status now refreshes only when you open the Local MCP menu, with a just-checked indicator — no more background checks that could interfere with your linked session.
• Fixed a case where reinstalling the app after removing it left it stuck as uninstalled and would not reconnect.

## v3.0.363 — 2026-08-05

More reliable, with fixes to your data and status.

• Spreadsheets: creating an Excel file now keeps every value, including numbers — no more dropped columns.
• Messages: search now works with names and text containing apostrophes (like O'Brien).
• WhatsApp: the menu bar shows your real connection status, so you know when to re-link instead of a misleading connected.
• Mail: opening emails and browsing your mailboxes from your assistant is smoother and more accurate.
• Under the hood: fixed a rare crash and hardened error handling across the toolset.

## v3.0.361 — 2026-08-04

This update makes Local MCP more reliable and easier for your assistant to use:

• Clearer guidance when something isn't found (a list, a chat, a message) — your assistant gets the exact next step instead of a dead end.
• Faster responses: actions in Teams and Reminders that could occasionally stall now return quickly.
• Cleaner, consistent results across Reminders, Calendar, Mail, WhatsApp, Teams, and Slack.
• Invalid requests (a missing list, an impossible date) are caught up front — no more 'done' confirmations for things that didn't happen.
• Your assistant finds the right tool faster across your apps.

## v3.0.360 — 2026-08-02

Todoist is here. Connect your Todoist account and list, create, and complete tasks right from your AI assistant.

This update also makes everyday tasks smoother: notes read cleanly, contact and file searches are more helpful and precise, and there are reliability and quality improvements across the app.

## v3.0.359 — 2026-07-31

Reading and listing your Apple Notes is now much faster and more reliable. Creating Excel and PowerPoint files works on every Mac — no setup required. You can now create repeating calendar events and delete an entire series at once. Plus reliability and behind-the-scenes improvements.

## v3.0.358 — 2026-07-31

Local MCP is more reliable and easier for your assistant to use.

• Reliability: the connection no longer freezes on a slow task — it's bounded and shows progress instead of a spinner, and status stays responsive even under load.
• Files: reading, writing, listing and searching local files is smoother, and your assistant finds the right file tool more reliably.
• Messages: read a conversation by simply naming the contact.
• Microsoft Teams: search across all your chats at once.
• Reminders: move reminders between lists, and see when each was created.
• Smarter discovery: clearer tool descriptions so the assistant picks the right capability — and a hint to retry in English when searching in another language.
• Under the hood: safer, verified auto-updates.

## v3.0.357 — 2026-07-30

Local MCP keeps getting more reliable.

• Calendar: events you create now go to the calendar you actually chose.
• Mail: folders list reliably (even empty ones), and reading email from very large mailboxes gives clear guidance instead of a confusing timeout.
• Microsoft Teams: sending chat messages now works across more account setups.
• OmniFocus: due dates show the correct day in your local time zone.
• Automations: multi-step recipes can pass results between steps, with a new wait step.
• Under the hood: snappier and more responsive, with more reliable update detection.

## v3.0.356 — 2026-07-30

Mail is more reliable with Exchange and Outlook accounts — your inbox and folders are found correctly, drafts show which account they'll send from, and moving messages is more dependable. Calendar events delete cleanly, and large meetings show attendee counts at a glance. Reminders use consistent IDs across the app. Automations can now pause between steps — so screen recordings capture exactly what you intended — and their results tell you where each file was saved. Excel create-and-read round-trips cleanly. Plus reliability and clarity improvements throughout.

## v3.0.355 — 2026-07-29

Reading email is faster and more reliable on large mailboxes, and you can pull a message's full text on demand when it isn't stored locally. New: search your Safari and Chrome browsing history. Better handling of same-named calendars across multiple accounts, faster file search, and improved iCloud Drive support.

## v3.0.354 — 2026-07-28

Mail is more accurate this release. Search now finds your emails even when the text has unusual spacing, dashes, or accented and uppercase words, and it stays within the account you search in. Reading a message no longer fails when that message was recently moved or deleted. Microsoft Teams now tells you clearly when it needs Full Disk Access to read your chats. Plus reliability and diagnostics improvements under the hood.

## v3.0.353 — 2026-07-28

Email search is more reliable: pasting a subject that contains a dash or other punctuation now finds the message instead of coming up empty, and your Mail accounts are detected reliably right after Mail opens. WhatsApp now tells you clearly when your link has expired so you can reconnect in one click. We also tidied up which integrations appear so you only see the ones that work today, plus reliability improvements across the board.

## v3.0.352 — 2026-07-28

This release is all about speed and reliability. Reading email no longer slows your Mac on large or slow accounts, and Microsoft Teams messages load dramatically faster. WhatsApp is more dependable — large chats read reliably and a sent message is never wrongly reported as failed. Setup is smoother, too: your AI can wire Local MCP into your other AI apps and jump you back to the setup wizard in one step. Plus stability fixes throughout.

## v3.0.351 — 2026-07-27

Mail is more dependable — reading your inbox now works reliably with Gmail and Microsoft Exchange accounts, and unread messages sort more accurately. Apple Notes now work even when the Notes app is closed. Deleting a OneDrive file now confirms it was really removed. Calendar events with large guest lists no longer get cut off. Setup is smoother: your AI can tell you exactly which macOS permissions still need approval. And Claude Desktop users get a new one-click install option. Plus reliability and performance improvements under the hood.

## v3.0.350 — 2026-07-26

Local MCP is more reliable and lighter on your Mac.

• The menu-bar app uses less energy while idle.
• A slow or stuck request can no longer make Local MCP unresponsive — and scheduled email routines now open Mail on their own instead of stopping.
• Everyday terminal commands and file reads handle edge cases (cloud placeholders, safe scripts) smoothly instead of hanging.
• Improved behind-the-scenes diagnostics so we can spot and fix slowdowns faster.

## v3.0.349 — 2026-07-26

Local MCP is faster, more reliable, and now taps community skills.

• Community skills: ask your AI what skills the LMCP community has shared, and install one in a single step — ready-made workflows for email, meetings, files and more.
• Mail stays responsive even when several requests run at the same time.
• Settings you turn on (like allowing terminal commands) now take effect right away.
• Clearer guidance when a file can't be found, plus security and reliability improvements throughout.

## v3.0.348 — 2026-07-25

WhatsApp is clearer and more up to date: contacts now show real names and phone numbers instead of technical IDs, and your chats stay current automatically. You can now turn any multi-step workflow into a reusable Skill and share it with other people — ask your assistant to save one. Reading email is more reliable, with clearer handling of messages that aren't downloaded to your Mac yet.

## v3.0.347 — 2026-07-25

WhatsApp linking is clearer: if your link has expired, LMCP now shows the QR to reconnect instead of wrongly saying you're already connected, and reassures you that your existing chats stay readable. Apple Notes now finds notes across every account (iCloud, Gmail, Exchange), not just your default one. Reminders with a date now land on the right day in every timezone. When a file can't be opened, LMCP tells you whether it's a permissions issue rather than calling it corrupt. Plus clearer status when Mail isn't open.

## v3.0.346 — 2026-07-24

Mail and Messages are dramatically more reliable. Sending an iMessage now works on the latest macOS, reading email degrades gracefully instead of getting stuck, and when a file or message isn't downloaded yet, LMCP tells you exactly how to fix it. WhatsApp reconnects cleanly, and error messages across the app are clearer and more actionable.

## v3.0.345 — 2026-07-23

Your Mac stays connected to web AIs more reliably — dropped connections now recover in seconds instead of minutes. Calendar invites give clearer guidance when permissions are missing, and the settings page now shows every app LMCP supports, including Chrome, Slack, Signal, Telegram, Notion, Google Drive, Zoom and Office documents.

## v3.0.344 — 2026-07-22

Mail and Messages are faster and more reliable. Reading an email now works even when the account name differs in capitalization or spacing, listing your mail accounts is instant instead of stalling when Mail is closed, sending an iMessage works even if Messages wasn't already open, and you can now search Messages by date range alone. Plus: Notion pages open reliably by ID, and getting started from the command line is smoother.

## v3.0.343 — 2026-07-21

Mail is faster and now recovers on its own if it ever gets stuck — and reading email on iCloud accounts is more reliable. Fixed listing tasks in OmniFocus, creating Word documents, and reading Microsoft Teams chats. Jan and LM Studio now configure in one click.

## v3.0.342 — 2026-07-19

Connecting a web AI is clearer and more reliable. Setup now confirms the moment ChatGPT, Claude.ai, or Grok connects to your Mac — no more guessing whether it worked. And if ChatGPT's connector setup gives you trouble, you'll see a one-tap option to use Claude.ai instead.

## v3.0.341 — 2026-07-17

Setting up web AIs is now simpler. ChatGPT, Claude.ai, and Grok each have their own guided, one-step setup, and you can add Cursor or VS Code with a single click. Calendar and Mail are more reliable, and Microsoft 365 now gives clearer next steps when your account's access is limited.

## v3.0.340 — 2026-07-15

• LMCP has a fresh new app icon.
• Granting permissions is smoother — the menu bar updates the moment you allow access.
• One-click access to Accessibility, Screen Recording, and folders.
• Notes and Office tools are faster and more reliable with large libraries.
• A smoother, more dependable installer.

## v3.0.339 — 2026-07-14

WhatsApp is smoother. Link your WhatsApp by scanning a QR code right from the menu bar — no Terminal needed. Plus we fixed an issue where sending WhatsApp messages could get stuck until you reconnected.

## v3.0.338 — 2026-07-12

Calendar and Reminders no longer show a false 'permissions lost' warning after an update — and their counts show correctly again. WhatsApp now offers a one-click reconnect when sending stops working, and Messages shows a clear way to grant send permission. Email accounts are more reliable (no more 'account not found' for an account that's right there), moving folders in OneDrive works, deleted notes no longer clutter your notes list, and getting set up is smoother if you connect through ChatGPT or Claude.ai in the browser.

## v3.0.337 — 2026-07-11

A cleaner, faster menu bar. Local MCP now groups your apps by what you actually do with them, shows everything at a glance, and only asks for a permission when a task truly needs it — no more prompts for access it already has. Setup is smoother too: onboarding now walks you through screen recording and accessibility so browser and screen tools work the first time. Your saved skills are now easy to read, rename, and remove right from Settings. Plus reliability improvements across Mail, Calendar and more.

## v3.0.336 — 2026-07-11

Automate any website. Local MCP now includes a built-in browser your AI can drive — log into Instagram, LinkedIn, X or any site once, and let your AI navigate, read pages, fill forms, and pull data for you. You sign in yourself (your password never touches the AI), and anything that posts or sends asks you first.

Connect Zalo. Link Zalo by scanning a QR, then reach and read your Zalo chats from any AI — the same easy way you already use WhatsApp.

Save your work as reusable workflows. Turn a multi-step task into a workflow you can rerun anytime, and look back at exactly what each run did.

Mail is faster and more reliable. Reading and listing email is quicker and no longer gets stuck on large mailboxes. Attachments with accented or special characters in their names now save correctly, and PowerPoint files on OneDrive open reliably.

Setup reflects reality. Local MCP no longer asks you to allow apps you've already granted, and you can add extra folders for file access in Advanced Settings.

## v3.0.335 — 2026-07-10

Local MCP can now record and edit screen demos — and drive any app's interface. Capture a screen recording, trim out the dead bits, turn a clip into a GIF, reframe it vertical for social, or blur anything private — all on your Mac, no other tools needed. Your AI can also click, type, and read on-screen to automate whatever you need. Plus a smoother way to connect web AIs (with a clear 'Copied' confirmation and step-by-step) and behind-the-scenes reliability improvements.

## v3.0.334 — 2026-07-09

Saving email attachments now works reliably, and Mail is more dependable when matching your accounts. Plus behind-the-scenes reliability and diagnostics improvements.

## v3.0.333 — 2026-07-08

Weather is here — ask your AI for the forecast in any city, and it's now part of your daily brief. Automated and scheduled emails now send reliably even when Mail isn't already open. Plus reliability improvements behind the scenes.

## v3.0.332 — 2026-07-06

Reliability improvements: Mail recovers faster when a slow account stalls, WhatsApp messages send reliably right after you link your account, and diagnostic commands with common redirections now run as expected.

## v3.0.331 — 2026-07-05

LMCP now runs lighter in the background — fewer network requests and improved reliability when you have multiple AI clients connected.

## v3.0.330 — 2026-07-05

Reading email is more reliable. LMCP now pulls the full message body from more formats — newsletters, forwarded messages, and mixed-format mail that sometimes came through blank — and looks up messages by ID more accurately. You can also rotate your cloud connection token in one click from the menu bar, and new users get a clearer welcome the first time they connect.

## v3.0.329 — 2026-07-04

Calendar events now land at the exact time you set — no more events slipping to midnight. Safari and Chrome browsing tools are more reliable, even when no window is open. Sending Microsoft Teams messages now works dependably. Clearer, more accurate guidance when a Mac permission still needs to be granted. And you can now enable terminal commands from Advanced Settings when you want Local MCP to run them.

## v3.0.328 — 2026-07-04

You can now attach files — like a PDF quote — to email drafts your AI prepares. Reading email is more reliable, including messages tucked into nested folders. New: you can opt in to let your AI run terminal commands — off by default, with a preview-and-confirm step and built-in safety limits. Chrome automation is steadier when no window is open, messaging integrations show clear setup guidance while they finish installing, and slow mail accounts now surface a helpful note instead of quietly stalling.

## v3.0.327 — 2026-07-03

OmniFocus now clearly tells you when it needs OmniFocus Pro, instead of a confusing permission error — so you know exactly what's going on. Mail handles large and syncing accounts more gracefully: it flags slow accounts up front so your requests stay fast and reliable. And recommending Local MCP to a colleague is now front-and-center in the menu bar — share it in a click and earn your Ambassador badge.

## v3.0.326 — 2026-07-02

OmniFocus is more reliable — it no longer says permission isn't granted when you've actually allowed access. Plus small reliability improvements to email.

## v3.0.325 — 2026-06-30

New: ask your AI about your Microsoft Teams call history — who you called, missed calls and durations. You can now disconnect WhatsApp from Local MCP too. Plus a more reliable cloud connection, and steadier Contacts, Calendar and Reminders right after an update.

## v3.0.324 — 2026-06-30

WhatsApp linking is clearer. When WhatsApp isn't connected yet, Local MCP now shows you exactly how to link it — with a QR code right in your chat, no Terminal needed.

## v3.0.323 — 2026-06-30

Local MCP is now easier to discover and connect from more AI assistants and tools. This update also includes behind-the-scenes reliability and connectivity improvements.

## v3.0.322 — 2026-06-29

Notes now keep their formatting. When your AI creates or edits an Apple Note, headings, bold and italic text, bullet and numbered lists, and links now appear with Apple Notes' native styling instead of raw Markdown symbols. Creating a note directly in a specific folder is also more reliable. Plus, clearer guidance when a Mac permission still needs to be granted.

## v3.0.321 — 2026-06-29

Email is smoother and more reliable: search no longer shows the same message twice, archiving and moving messages works correctly, and a message you just listed can be moved right away. Connecting OmniFocus is easier — grant access right from the menu bar. Plus fixes for the latest macOS.

## v3.0.320 — 2026-06-29

Email search is now much faster and more reliable. Searches that find no matches return instantly instead of making Mail hang, and multi-word searches are more accurate.

## v3.0.319 — 2026-06-29

Control Google Chrome directly from your AI — open tabs, read pages, click links, and fill in forms, just like Safari. Now you can also link WhatsApp by scanning a QR code right inside the chat, with no Terminal needed, and connecting Signal is clearer with step-by-step guidance. Your messaging apps now always appear in the menu bar with simple instructions to connect them. Plus a smoother first-run setup and reliability improvements throughout.

## v3.0.318 — 2026-06-28

Apple Mail keeps getting faster and clearer. Reading, listing and replying to email is now near-instant even on very large mailboxes. Dates from senders with a wrong clock now show correctly. And when a tool needs an app that simply isn't open, Local MCP now tells you to open it instead of showing a confusing permission message.

## v3.0.317 — 2026-06-27

Faster, more reliable Mac tools. Searching Apple Notes is now near-instant, even on large libraries. More tools respond cleanly instead of occasionally erroring out. You can now send email from an account by its name, calendar searches flag invalid dates instead of silently defaulting to today, and emails with bad sender timestamps show the correct date.

## v3.0.316 — 2026-06-27

Reliability improvements. Reporting a problem to our team now works on the first try — no more confusing errors or duplicate reports. Inviting a colleague is more dependable. And when a tool needs your attention — like granting access to Mail — you'll now see a clear, actionable message instead of a cryptic failure.

## v3.0.315 — 2026-06-27

Apple Mail is dramatically faster: reading and searching your email is now near-instant — even on very large mailboxes — and no longer freezes Mail. Slack, Teams, Telegram and Signal now set up their readers reliably, so your AI can read those chats out of the box. And the connection to web AIs (ChatGPT, Claude.ai, Grok) is steadier, with fewer dropouts.

## v3.0.314 — 2026-06-26

This update makes Reminders far more capable: your AI can now set a reminder's priority (low, medium, high), move reminders between lists, and create, rename, or delete lists. Email drafts now save to the correct account's Drafts on multi-account Macs. We also smoothed out file browsing with home-folder shortcuts and made recommending LMCP to a colleague clearer.

## v3.0.313 — 2026-06-25

Email attachments now work reliably: save attachments from any email to your Mac, and attach files when sending. Setting up Mail access is smoother and more dependable. Connecting Microsoft 365 and Outlook is easier — your AI can do it for you. Plus reliability fixes across Mail and messaging.

## v3.0.312 — 2026-06-25

Mail is more reliable — no more hangs when opening messages that haven't fully downloaded from iCloud. Excel: writing to existing spreadsheets now works smoothly. Teams runs more reliably. Cleaner uninstall — removing Local MCP now fully clears everything it created. Smoother first-time setup and permission prompts.

## v3.0.311 — 2026-06-23

Email works better with iCloud — searching now finds messages it sometimes missed, and moving emails to folders is confirmed reliably. Plus a new helper for drafting Signal messages.

## v3.0.310 — 2026-06-22

Connecting Local MCP to web AI assistants like ChatGPT and Claude.ai is now more reliable — approving a connector turns everything on automatically. Uninstalling stays clean (no more unexpected relaunches), and we fixed a stray startup error on some Macs.

## v3.0.309 — 2026-06-22

You can now ask your AI to save email drafts in Apple Mail for you to review and send yourself — nothing is sent without you. Plus a stability fix so Local MCP stays running reliably after an automatic update.

## v3.0.308 — 2026-06-22

Fewer unnecessary permission prompts. Local MCP no longer asks you to re-allow Mail, Notes, and other apps when access is already granted, and its status now reflects your real permissions more accurately.

## v3.0.307 — 2026-06-21

Granting access to Mail, Notes, Safari and Messages now works as expected — the macOS permission prompt appears so your AI can read and act in those apps. If a grant ever seemed stuck before, this fixes it.

## v3.0.306 — 2026-06-21

You can now send iMessages straight from your AI assistant — just ask, confirm, and it's sent. Permission prompts are smarter too: Local MCP no longer asks for access to an app that simply isn't open. Plus a more reliable, calmer first-run experience for new installs.

## v3.0.305 — 2026-06-21

A smoother first run: new users now reliably see the welcome guide that helps them get value right away (it no longer skips itself on machines with leftover permissions). Diagnostics are clearer too — a closed app is reported as simply not running instead of an error. Plus reliability fixes for reading Notes.

## v3.0.304 — 2026-06-21

Notes is more reliable — listing and searching your notes now works smoothly even on large libraries. Permission prompts are calmer too: once you've answered a request, it won't keep popping up, and each prompt now names the correct app.

## v3.0.303 — 2026-06-21

Getting started is smoother. The moment you connect Local MCP, you'll see tailored suggestions for what you can do with your Mail, Calendar, Notes and more — so you're productive from the first message. And if the app ever gets stuck on an older version, a single tap now reinstalls the latest while keeping all your permissions. Plus behind-the-scenes reliability improvements for AI assistants that work with your data.

## v3.0.302 — 2026-06-21

Connecting Microsoft 365 is now one click — open Settings, tap Connect Microsoft 365, sign in, and it connects automatically (no more typing commands). Mail and Outlook are more reliable: a new watchdog prevents the occasional hang. And results across your apps are richer and more structured, so your AI reads your mail, calendar, files and more with better accuracy.

## v3.0.301 — 2026-06-21

Your cloud storage and AI results just got better. Browsing Google Drive and OneDrive now works correctly — your assistant can list and navigate those folders instead of seeing them as unreadable files. Results from your apps are now richer and more structured, so AI assistants like ChatGPT read your mail, calendar, files and notes more accurately and reliably. Plus a steadier cloud connection and under-the-hood polish.

## v3.0.300 — 2026-06-21

Connecting Outlook and Microsoft 365 is now seamless — the setup button takes you straight to the right screen. Reading mail is faster and more dependable, with no more long waits. A refreshed first-run experience makes getting started clearer and supports more AI assistants. Plus reliability improvements to uninstall and behind the scenes.

## v3.0.299 — 2026-06-21

Mail is faster and more reliable — reading a message no longer stalls when an account isn't specified.

## v3.0.298 — 2026-06-20

A smoother first run. Setting up Local MCP is now clearer and more guided — official app icons, better contrast, and a step that helps you connect your AI assistant. Fresh installs land straight into the welcome guide, and OneDrive and Microsoft 365 are easier to connect from the start. Uninstalling also cleans up fully after itself.

## v3.0.297 — 2026-06-20

Mail is more reliable when several requests run at once. Onboarding is clearer, with simpler permission prompts. And 'Check for Updates' now works as expected.

## v3.0.296 — 2026-06-18

Auto-updates are now more reliable — your Mac always runs the latest version, even when more than one copy of the app is installed. This ensures recent fixes (including Slack stability) actually reach you without a manual reinstall.

## v3.0.295 — 2026-06-18

Local MCP can now map your full mailbox. Your AI assistant discovers every folder and nested subfolder across Mail and Outlook automatically — so organizing and finding email no longer misses anything. We also improved connection reliability, so Local MCP keeps running smoothly right after an update.

## v3.0.294 — 2026-06-18

Reliability and quality improvements across Mail search, Calendar event previews, Reminders, Teams channels, Slack, and document editing. Smoother first-time setup.

## v3.0.293 — 2026-06-17

Mail is more reliable — fixed an issue that could cause long delays or a hang when reading or sending email. Plus onboarding polish so your assistant stays focused on what you ask.

## v3.0.292 — 2026-06-17

Reading group chats in Messages now works reliably. And when you change which tools your AI can use in Settings, the update takes effect right away — your AI's available tools always match what you've allowed.

## v3.0.291 — 2026-06-17

Signal and Telegram now work on Intel-based Macs. You can also invite guests when creating calendar events — your assistant adds them and Calendar sends the invitations.

## v3.0.290 — 2026-06-16

Fix read_email timeout (two-phase body fetch, 8s hard cap), fix fs_list/fs_search/fs_read telemetry misclassification (path_not_allowed instead of jxa_permission_denied), fix image helper guard, fix image PNG dimension check.

## v3.0.289 — 2026-06-16

Reading your Signal messages now works on the latest versions of Signal Desktop.

## v3.0.288 — 2026-06-16

Searching your Notes is faster and no longer times out on large libraries. Signal now appears in your app list, and the first-time permission prompts for Slack and Signal no longer hold things up.

## v3.0.287 — 2026-06-16

Reading your Signal messages now works reliably — list and search your Signal Desktop conversations straight from your AI assistant. We also made the one-time permission prompt for Slack and Signal clearer, so it's obvious the request is coming from Local MCP.

## v3.0.286 — 2026-06-16

• Read your Signal chats directly from your AI assistant.
• Edit existing notes and reminders — not just create them.
• A friendlier first-run setup you can reopen anytime from the menu, and that no longer pops up on updates.
• Permission prompts now clearly say 'LMCP'.
• A refreshed, translucent menu bar.
• Reliability improvements.

## v3.0.285 — 2026-06-15

• Email replies are more reliable.
• A clearer menu bar — the app and server version and your tool-call count are now labeled at a glance.
• The first-run setup now appears only on new installs and stays dismissed once you close it.
• Reliability improvements.

## v3.0.284 — 2026-06-15

• A new guided setup gets you connected in under a minute — it walks you through permissions, Full Disk Access, and linking your desktop AI app or ChatGPT/Claude.ai, now in 9 languages.
• A cleaner, simpler menu bar.
• Reliability improvements across Mail, Contacts and Slack.

## v3.0.283 — 2026-06-15

• Slack channels and messages now load reliably in the latest Slack desktop app.
• Mail is faster and more dependable — fewer timeouts when listing accounts and opening messages.
• Contacts no longer hangs on large address books.
• Reliability improvements.

## v3.0.282 — 2026-06-15

• Slack works again with the latest Slack desktop app — browse your workspaces and channels and search messages
• New Restart button in the menu bar to quickly reconnect Claude, ChatGPT, Cursor and others when they haven't picked up LMCP yet
• Reliability improvements

## v3.0.281 — 2026-06-14

• Teams and Slack now set up reliably on a fresh install
• The app stays running and updates more smoothly
• Contacts is faster and more reliable on the latest macOS

## v3.0.280 — 2026-06-14

• Image Playground now works on the latest macOS
• Faster Mail — quicker inbox search and message loading, especially over the cloud connector
• Smoother, more reliable app updates
• Reliability improvements across Microsoft 365 and first-time setup

## v3.0.279 — 2026-06-13

More reliable web connections. ChatGPT, Claude and other web assistants now reconnect on their own if their secure session expires — no need to re-paste anything. Plus under-the-hood improvements so AI clients see clearer, safer tool labels.

## v3.0.278 — 2026-06-12

Local MCP now speaks your language. The menu bar app is fully translated across 10 languages — no more mixed English text.

Uninstall does what it says. Removing Local MCP now sticks cleanly instead of coming back.

Updates apply on their own. New versions activate during a quiet moment, so you are never stuck on an old build waiting to restart.

Smoother AI connections. ChatGPT, Claude and other assistants handle your calendar, email and message requests more reliably — and connecting ChatGPT is easier with a one-tap Copy token.

Moving emails into nested folders is more reliable.

## v3.0.277 — 2026-06-12

More reliable connections. We fixed a rare issue that could make tools hang or fail to respond under heavy use — Claude, Cursor and other apps now stay connected smoothly.

Generate images your way. Image Playground now lets you choose where to save generated images and reveals them in Finder when they're ready.

Calendar and Reminders are more dependable. Deleting an event or reminder now confirms exactly what you're removing, and clearly tells you when an item no longer exists.

Moving emails between folders is more reliable, including nested folders.

Cloud Relay now turns off completely. Switching it off immediately disconnects web connections as expected.

Invite a friend, right from Claude. You can now bring colleagues onboard in your own language — Claude pulls your contacts, drafts the message, and lets you edit before sending.

## v3.0.276 — 2026-06-11

This update makes Local MCP cleaner, leaner, and safer. Tool responses are more compact and easier for your AI to use, all-day calendar events read correctly, contact lookups stay small when several people match, and notes and emails come back as clean readable text instead of raw HTML. We also tightened privacy and safety: sensitive tokens are never exposed to the AI, and updates and other one-step actions now confirm before running.

## v3.0.275 — 2026-06-11

This update makes your results cleaner and easier to read. Email, calendar, and notes now appear as clear text instead of empty cards. You can limit how many calendar events and reminders are returned, and we improved behind-the-scenes diagnostics so issues get fixed faster.

## v3.0.274 — 2026-06-11

Local MCP gets a cleaner menu bar and easier setup. The new two-column design shows all your apps and AI assistants at a glance, and connecting a web assistant like ChatGPT, Claude, or Grok now takes a single click. A new 'Your LMCP' panel shows your usage, streak, and how you rank. Request a new app or feature right from the menu, see your version at a glance, and check for updates with one tap. We also made saving email attachments more reliable, clarified Image Playground's limits, and fixed the Spanish Gmail inbox.

## v3.0.273 — 2026-06-10

Three new integrations land today. Notion: your AI can now read and search your Notion pages and databases — no integration token, no admin approval, everything stays on your Mac. Google Drive: read, search, and write the files Google Drive for Desktop already syncs, with no Google Cloud setup. Zoom: summarize your recorded meetings — transcripts and meeting chat are read straight from your local recordings. Also in this update: Gmail inboxes in Spanish are now detected correctly, and tools show clearer names and safety labels in your AI client.

## v3.0.272 — 2026-06-10

New this release:

• On-device image generation groundwork — your Mac creates images locally with Apple Intelligence (rolling out where supported).
• Safari tools now guide you clearly when macOS needs a permission refresh.
• Reminders created by your AI now ring — notifications fire at the due time.
• Sharper, more accurate guidance for AI assistants connecting to your Mac.

## v3.0.271 — 2026-06-10

Quality and accuracy improvements:

• Your daily brief now shows your real unread email count.
• Slack connection status is reported accurately — no more incorrect reinstall prompts.
• More consistent tool results when running without the menu bar app.
• Behind-the-scenes groundwork for on-device image generation.

## v3.0.270 — 2026-06-09

Reliability and polish across your Mac tools:

• File search now understands shortcut paths like ~/Desktop and ~/Documents.
• Contact search returns more relevant people and better protects your address book.
• Microsoft Teams threads no longer show duplicate messages.
• Friendlier, clearer messages when an app isn't installed or you're not signed in.
• A more accurate at-a-glance view of which of your apps are connected.

## v3.0.269 — 2026-06-09

Contacts and Calendar are more reliable. Looking up a contact or deleting a calendar event no longer fails when the identifier was copied with extra formatting, and contact lookups now fall back to matching by name. Clearer guidance when an item can't be found.

## v3.0.268 — 2026-06-09

Local MCP is more stable. We fixed an issue where Apple Mail could freeze or stop responding when several requests reached it at once — most noticeable with Exchange accounts during a morning briefing or scheduled sync — by handling app requests one at a time per app. We also resolved a rare crash under heavy use. Your Mail, Calendar, and other apps now handle back-to-back requests smoothly.

## v3.0.267 — 2026-06-09

Local MCP is faster, more reliable, and more private. We rebuilt Mail, Notes, Reminders, OmniFocus, and Safari to run through a leaner, more dependable engine, and you can now delete reminders directly from your assistant. We fixed a rare crash and a bug that could hide file-browsing tools. We also strengthened your privacy: content from your emails, messages, files, and web pages can no longer steer the AI off task, and the local connection is now locked to your account. You can opt out of anonymous improvement signals anytime in Settings.

## v3.0.266 — 2026-06-08

You can now delete reminders and browse files on your Mac, directly from your AI assistant. This release also includes reliability improvements under the hood.

## v3.0.265 — 2026-06-08

Local MCP is more reliable and more private. We fixed a rare crash, updates now restart cleanly, and we hardened how your data is handled: content from your emails and messages can no longer steer the AI off task, and the local connection is locked to your account. Slack shows clearer status, and you can opt out of anonymous improvement signals in Settings.

## v3.0.264 — 2026-06-08

More reliable tool calls — momentary glitches reading Notes, Safari, OmniFocus, and Messages now retry automatically instead of failing. Updates also apply more dependably.

## v3.0.263 — 2026-06-08

More reliable under heavy use — fixes a rare freeze that could happen when several AI clients connect and disconnect. Plus smaller stability improvements.

## v3.0.262 — 2026-06-08

Updates now take effect right away — fixes and new features reach your assistant without waiting for a restart. Connections to cloud assistants (ChatGPT, Claude.ai, Grok) are also more stable, with fewer dropped sessions.

## v3.0.261 — 2026-06-07

Safari bookmarks are back — your assistant can read them again. The app also stays responsive when a tool takes a while, instead of hanging the session. Plus smaller reliability fixes.

## v3.0.260 — 2026-06-07

Smarter app selection. When you use both your Apple apps and a Microsoft 365 account, your AI assistant now more reliably reaches the right one for calendar, contacts, and reminders — fewer mix-ups between your iCloud and work accounts.

## v3.0.259 — 2026-06-07

LMCP starts faster and more reliably — every tool is ready the moment the app launches. Your AI can now check the current date and time on your Mac. And uninstalling LMCP now fully cleans up after itself.

## v3.0.258 — 2026-06-07

The Claude Desktop extension and npm setup now run on their own — no separate app required to get started. If you also install the full Local MCP app, the extension automatically connects to it for cloud access and auto-updates. Reliability improvements under the hood.

## v3.0.257 — 2026-06-06

Performance and reliability improvements under the hood.

## v3.0.256 — 2026-06-06

Working with large OneDrive folders is now faster and more reliable. This update also includes behind-the-scenes improvements to connection stability and a smoother install experience.

## v3.0.255 — 2026-06-05

Faster, more reliable setup. We removed a setup step that could stall the installer — especially on Windows — so LMCP gets up and running more smoothly.

Discover more as you go. LMCP now points you to other apps on your Mac it can help with, so you find more of what it can automate without hunting for it.

## v3.0.254 — 2026-06-05

Opening LMCP for the first time now shows a visual welcome card — a live snapshot of what it can see on your Mac plus every app it connects to and ready-to-use automation ideas — so you know exactly what's possible from the first message.

## v3.0.253 — 2026-06-05

Your very first chat now instantly shows what LMCP can see on your Mac — your contacts, emails, calendar and reminders — so you get real value from the first message instead of an empty screen.

## v3.0.252 — 2026-06-04

Email is more resilient: if a single message ever makes Mail hang, Local MCP now recovers on its own instead of stalling the rest of your session. Checking for updates also no longer triggers an unnecessary restart.

## v3.0.251 — 2026-06-04

Reminders and Microsoft To Do are more reliable: they no longer report a permission error when access has already been granted. Your calendar and daily briefing now consistently show the events scheduled for today. And when a tool needs a macOS permission such as Full Disk Access for Microsoft Teams, Local MCP now explains exactly how to enable it instead of showing a confusing error.

## v3.0.250 — 2026-06-04

LMCP now speaks your language. The menu bar app is fully localized — Spanish, Portuguese, French, German, Italian, Dutch, Chinese, Japanese, and Korean — and setup guides open in your language too.

Connecting a web AI is now one paste. A new Copy URL button hands you a ready-to-use connector link for Grok and Claude.ai — no extra sign-in steps. ChatGPT, Claude.ai, and Grok all show a clear, up-to-date connection status in the menu bar.

Plus smoother, more reliable updates behind the scenes.

## v3.0.249 — 2026-06-03

Updates now apply reliably — if your Mac was stuck on an older version, it catches up on its own, and fresh installs always get the latest build.

A clearer setup screen. Your AI apps are now grouped by how they connect: desktop apps (Claude, Cursor, VS Code) link directly, while web AIs (ChatGPT, Claude.ai, and now Grok) connect through the Cloud Relay. Connecting a web AI no longer asks for an email — it just works.

Grok is now supported as a connected AI.

## v3.0.248 — 2026-06-03

A cleaner, smarter tool list. Claude now hides integrations like Slack and VPN until you've actually set them up, so it picks the right tool instead of guessing — and connection checks stay available so you can always get set up.

More reliable installs. Installing LMCP now always delivers the very latest version.

## v3.0.247 — 2026-06-03

Faster, more reliable email. Reading and searching mail on Macs with several accounts is quicker and no longer times out, and moving messages is faster too.

A cleaner, smarter tool list. Claude now sees only the apps and accounts you've actually connected, so it picks the right tool instead of guessing.

Microsoft 365 is steadier. It automatically rides out Microsoft's temporary rate limits and service hiccups, with fewer false 'sign in again' prompts.

The menu bar app keeps itself up to date more reliably.

## v3.0.246 — 2026-06-02

Your email, calendar, and notes now appear as clean, interactive cards right inside the chat — in assistants that support it. We also reduced macOS permission pop-ups on startup (LMCP now asks only when it actually needs access) and made results clearer with helpful next-step suggestions.

## v3.0.245 — 2026-06-02

Calendar is more reliable — we fixed a rare crash that could happen with certain recurring events. ChatGPT and other cloud AI assistants can now reach your Mail and Apple Notes through the connector. And when sending email, you can now choose which of your accounts it goes out from.

## v3.0.244 — 2026-06-01

Connecting ChatGPT and Claude.ai is clearer and simpler. The menu bar now shows whether each AI assistant is genuinely connected instead of always reading 'connected,' and points you to setup when it isn't. Linking a connector now takes just your token, and your account email stays in sync between the menu bar and Settings.

## v3.0.243 — 2026-06-01

OneDrive file listing now stays inside your OneDrive folders — agents can no longer browse your entire Mac by mistake.

## v3.0.242 — 2026-05-31

Updating is more reliable. Local MCP now confirms it's actually running the newest version before marking an update complete, fixing cases where the app could get stuck on an older release and keep reinstalling without ever moving forward. Tool results also always display correctly now, including for a few tools that could previously return a blank response.

## v3.0.241 — 2026-05-31

Messages is more reliable. Listing, reading, and searching your conversations now works across every chat — including ones whose latest message is an attachment or reaction. Slack workspaces now show up correctly. Setup is smoother too: connecting Claude Desktop and Claude Code is more dependable, leftover copies are cleaned up automatically on update, and the menu bar settings window always opens in the right spot. Onboarding is now fully translated.

## v3.0.240 — 2026-05-31

Reinstalling or updating now cleans up after itself automatically — old leftover copies are removed and Local MCP always launches the current version. Plus more reliable setup for Claude Code and OmniFocus.

## v3.0.239 — 2026-05-31

Claude Code now connects reliably. Local MCP configures Claude Code in the right place and repairs any stale connection automatically, so the tools are there after every update, reinstall, or version change — no manual setup needed.

## v3.0.238 — 2026-05-31

Updating and uninstalling now work the way you expect. Clicking Install in the menu bar applies the new version right away instead of waiting on a restart. And Uninstall now fully removes Local MCP — the app and all its connections to your AI clients — in a single click.

## v3.0.237 — 2026-05-31

Setup is now more reliable. Local MCP configures Claude Desktop, Cursor, Windsurf, VS Code, and Zed automatically — even on Macs without Node.js installed — and your Mail, Notes, Messages, and Safari permissions stay put across updates, so you don't have to re-approve them after each release.

## v3.0.236 — 2026-05-31

Microsoft Teams now shows your real chat count in the menu bar instead of telling you to open Teams when it's already working. Behind the scenes, app permissions (Mail, Notes, Messages, Safari) are now more resilient across updates.

## v3.0.235 — 2026-05-31

Microsoft 365 keeps you connected: when your session expires, LMCP now sends a notification and shows a one-tap Reconnect right in the menu bar — so your email and calendar tools never stop working without you knowing. Calendar is faster and more reliable on large or shared calendars, with leaner results. And when your AI reaches for a tool that isn't available, it's now pointed to the right one.

## v3.0.234 — 2026-05-30

OmniFocus now requests permission automatically during installation — reinstalling resolves the issue. Downloading the DMG from local-mcp.com/get now opens the installer correctly instead of showing binary text. The confirmation email arrives in your language with DMG installation instructions. Minor improvements to the download flow.

## v3.0.233 — 2026-05-30

OmniFocus tools now show a clear fix when Automation permission needs to be re-granted — tap 'Fix in Settings' directly from the tray. Auto-update is now more reliable for machines that were stuck on older versions. iMessage search no longer fails on accounts with attachments.

## v3.0.232 — 2026-05-30

OmniFocus Standard users now see a clear message instead of a cryptic error. Teams chat history: clearer guidance when messages haven't synced locally yet.

## v3.0.231 — 2026-05-30

Update checks are now more reliable — the app will detect and install new versions faster.

## v3.0.230 — 2026-05-30

Language switcher is now in the top menu for easier access. WhatsApp shows a cleaner status once connected. Teams and other services show cleaner status information.

## v3.0.229 — 2026-05-30

OmniFocus now shows 'Requires Pro' when Standard edition is detected. Safari displays your bookmark count. Language switcher moved to the top of the menu. Error details now visible in the Activity log for easier diagnosis.

## v3.0.228 — 2026-05-29

OmniFocus, Mail, Notes and Safari now work on first install — no separate permissions needed. Tapping the version number checks for updates instantly. Restart is more reliable.

## v3.0.227 — 2026-05-28

OmniFocus diagnostics now use a single JXA probe path, preventing false permission warnings when OmniFocus reports a Pro-feature limitation. This improves reliability of troubleshooting results.

## v3.0.226 — 2026-05-28

Service status display is clearer in the tray when apps are not active. OmniFocus diagnostics now avoid mislabeling Pro-feature limits as permission issues. This improves troubleshooting clarity and day-to-day reliability.

## v3.0.225 — 2026-05-28

OmniFocus diagnostics now correctly identify Pro-feature limitations instead of showing a permissions issue. This update improves troubleshooting accuracy and setup guidance. Minor reliability improvements for diagnostic error classification.

## v3.0.224 — 2026-05-28

Diagnostics now distinguish permission issues from app limitations and improve setup guidance in Settings. Service detection is more accurate for Mail, Notes, and OmniFocus. Stability and reliability improvements across local integrations.

## v3.0.223 — 2026-05-27

Setup is clearer after you connect an AI app: step-by-step prompts to try your first command, with one-tap copy. Email signup in the menu bar is more reliable. General stability improvements.

## v3.0.222 — 2026-05-26

M365 mail is more reliable with fewer connection errors. Teams works better on large accounts. You can restart LMCP from the menu bar without closing your AI editor.

## v3.0.221 — 2026-05-25

The menu bar app now updates to the latest version automatically after you close your AI editor, instead of staying on an older release while Cursor is open. Fleet version reporting now reflects the app installed on your Mac.

## v3.0.220 — 2026-05-25

Cursor and Claude stay connected to Local MCP more reliably after updates. Running npx local-mcp in Terminal now shows a clear finished message instead of hanging silently. Calendar permission prompts return faster with clearer guidance when access is still pending.

## v3.0.219 — 2026-05-24

AI editors like Cursor stay connected to Local MCP more reliably. Calendar and Reminders respond within seconds when permissions are still pending, with clear steps to approve access on your Mac. Teams shows a helpful message when no account is signed in.

## v3.0.218 — 2026-05-24

Fixed a critical bug where Cursor and Claude Desktop would disconnect after the first tool call. Connections are now stable throughout the entire session.

## v3.0.217 — 2026-05-24

Fixed a crash where the app could disconnect mid-session when updating in the background.

## v3.0.216 — 2026-05-23

Activity history is now visible in Settings → Advanced. See every tool call with timestamp, source, and status — and clear the log with one click.

## v3.0.215 — 2026-05-23

Connection stability improvements. The app now reconnects more smoothly when updates are installed in the background, with fewer interruptions to your workflow.

## v3.0.214 — 2026-05-23

Microsoft 365: the app now shows a warning banner when your M365 session has expired, with a one-click reconnect button. Sessions are also renewed automatically in the background before they expire. Error details from Microsoft are now logged to help diagnose reconnection issues.

## v3.0.213 — 2026-05-23

Improved reliability when reading Teams data on machines with large conversation histories or multiple tenants.

## v3.0.212 — 2026-05-22

Fixes a rare disconnect that could occur right after installation. The app now detects when an existing session is active and avoids interrupting it.

## v3.0.211 — 2026-05-22

Fixed: Microsoft Teams integration now works reliably when Teams is actively syncing in the background.

## v3.0.210 — 2026-05-22

Fixed: Excel files with multiple sheets now read correctly — previously some files with renamed or reordered sheets would fail to open.

## v3.0.209 — 2026-05-22

Microsoft 365 users: the app now silently refreshes expiring credentials before they fail, and shows the specific error code when re-authentication is needed. Fixed: running 'uninstall' now permanently removes Local MCP — the app will no longer restart after uninstalling.

## v3.0.208 — 2026-05-22

Windows users: fixed a connectivity issue that was preventing the cloud connector from working. AI tools now connect reliably on the first try. Microsoft 365 users: credentials are now refreshed silently before expiry, and the app shows a clearer message when re-authentication is needed.

## v3.0.206 — 2026-05-20

Fixed a crash when copying or regenerating the API key in Settings. ChatGPT now shows as connected when the Cloud Relay is active. Uninstall is more reliable and cleans up all files completely.

## v3.0.205 — 2026-05-20

Teams and Slack now work reliably on macOS 26. Fixed a code signing issue that caused the Teams and Slack co-processes to fail at startup on hardened runtime (exit 255).

## v3.0.204 — 2026-05-20

Fixed a macOS permission dialog that appeared on startup. The app is now properly signed and notarized so this won't happen again.

## v3.0.203 — 2026-05-18

New installs via DMG now auto-configure Claude Desktop, Cursor, and other AI clients on first launch — no manual setup needed. Email fixes: reply, search, and read email are now more reliable on Exchange and multi-account setups.

## v3.0.202 — 2026-05-18

Improved diagnostics to help detect and fix update issues faster.

## v3.0.201 — 2026-05-18

Improved setup tracking — the tray now correctly records when it configures Claude Desktop, Cursor, or other AI clients.

## v3.0.200 — 2026-05-18

Fixed a system dialog that appeared on every update asking for permission to access data from other apps.

## v3.0.199 — 2026-05-18

Fixed a privacy permission dialog that appeared on every update.

## v3.0.198 — 2026-05-18

Fixed a privacy permission dialog that appeared on every update.

## v3.0.197 — 2026-05-18

Fixed a privacy permission dialog that appeared on every update.

## v3.0.196 — 2026-05-18

Improved reliability and performance.

## v3.0.195 — 2026-05-18

Tray menu now shows all component versions: tray, server, and when the settings UI was last loaded.

## v3.0.193 — 2026-05-18

Permissions are no longer requested on every update. Calendar, Contacts, and Reminders access now persists across app updates.

## v3.0.192 — 2026-05-17

Fixes a disconnect that could occur when Claude Desktop updated the server in the background. Improved stability on macOS.

## v3.0.191 — 2026-05-17

Evernote integration. Intel Mac support. Improved reliability for Calendar, Reminders, and M365 connections.

## v3.0.189 — 2026-05-17

Fixes Calendar, Reminders, and Contacts permission dialogs appearing repeatedly after updates. Dialogs now appear once at startup in the proper context and are suppressed during background service scans. Also fixes Outlook showing setup prompt when Microsoft 365 is already connected.

## v3.0.188 — 2026-05-17

Fixes a bug where macOS Automation permission dialogs (for Mail, Notes, Safari, etc.) would reappear on every app restart. Permission dialogs now appear only once.

## v3.0.187 — 2026-05-17

After an automatic update, a one-click Restart button now appears in the menu bar to reconnect Claude Desktop instantly — no manual steps needed. New: ask Claude to show your tool call history for auditing and compliance.

## v3.0.186 — 2026-05-17

Your email is now requested right at the top of the app — no more scrolling to find it. Added IT admin controls (read-only mode and tool blocking) in the Advanced settings tab. Email tools now handle Drafts folder and verify moves completed successfully.

## v3.0.185 — 2026-05-17

Email fixes: move email now detects sync failures, Drafts messages readable, categories field consistent across all email tools.

## v3.0.184 — 2026-05-17

Microsoft 365 contacts and email search now work correctly. Gatekeeper warnings resolved — the app is fully signed and notarized.

## v3.0.183 — 2026-05-17

Improved reliability for Mac users. Signing and verification updates.

## v3.0.182 — 2026-05-17

Stability improvements and bug fixes.

## v3.0.180 — 2026-05-17

Service toggles now work in Settings. Microsoft 365, ServiceNow, and all new tools are visible in the Overview tab even before connecting. Fixed a bug where toggling a service on/off had no effect.

## v3.0.179 — 2026-05-17

Settings page redesigned: all service controls are now in a single Overview tab. Tray is lighter — shows status only, opens Settings for configuration. Fixed a bug where TCC permissions (Calendar, Mail, etc.) were lost on every update.

## v3.0.178 — 2026-05-17

You can now enable or disable individual services (Calendar, Mail, Contacts, etc.) directly from the menu bar or Settings. Fixed a crash on first install when the tray app was being set up in the background. Microsoft 365 and ServiceNow integrations now appear in the Connect tab.

## v3.0.177 — 2026-05-16

Microsoft 365 directory search is back. Connect your M365 account to search your organization's directory, look up colleagues, and see who you work with most. Developer ID signing now keeps app permissions stable across updates.

## v3.0.176 — 2026-05-10

Fixed Google sign-in — Gemini models now work correctly after connecting your Google account.

## v3.0.175 — 2026-05-10

Local Studio now loads correctly on all installations.

## v3.0.174 — 2026-05-09

Better error messages when Mail is syncing — now tells you exactly what to do. Improved Teams diagnostics. Clearer message when OneDrive file access is blocked.

## v3.0.173 — 2026-05-09

Improved reliability for users without Node.js installed — Local MCP no longer resets your AI client configuration on restart. Better diagnostics when Microsoft Teams data is unavailable.

## v3.0.172 — 2026-05-06

Fixed Windows tar extraction issue and improved admin dashboard reliability.

## v3.0.171 — 2026-05-04

Fixed an issue on Windows where the server could get stuck in a not-running state after an automatic update.

## v3.0.170 — 2026-05-04

Calendar events now filter correctly by calendar name. When you ask Claude to show events from a specific calendar, it now returns only those events instead of all calendars combined. Google Drive tools no longer show an error when Google Drive is not installed.

## v3.0.169 — 2026-05-04

Meeting participants now visible in calendar events. When you ask Claude about your calendar, each event now includes the attendee list with names, emails, and their roles (organizer, required, optional). Perfect for meeting-prep workflows. Local Studio improvements: sign in with Anthropic or OpenAI directly from the settings panel — no need to paste API keys manually. The settings drawer has been redesigned to show connection status and let you disconnect providers individually.

## v3.0.168 — 2026-05-03

Introducing Local Studio — a full AI workspace built into the app. Open it from the tray and chat with your AI model while browsing your local files. Your data stays private on your machine. Available on Mac and Windows.

## v3.0.167 — 2026-05-02

Messages search now works reliably on all macOS versions.

## v3.0.166 — 2026-05-02

Windows updates are now more reliable. The app no longer crashes when downloading updates while running.

## v3.0.165 — 2026-05-02

Installation is more reliable on Windows. The dashboard now shows a close button when opened as a popup window.

## v3.0.164 — 2026-05-02

Windows tray now opens a native-looking dashboard popup with the same rich UI as Mac. Toast notifications for first tool call, updates, and starter prompts. Improved service detection and cloud relay status.

## v3.0.162 — 2026-05-01

LMCP now starts automatically after install — no AI client needed to begin. The server runs in the background, ready for when you connect your first AI agent.

## v3.0.161 — 2026-05-01

One-click install now works on Mac and Windows. Download the extension file, open it in Claude Desktop, done. Also fixes download as .zip issue on Chrome/Edge.

## v3.0.160 — 2026-05-01

One-click install: download the extension file and open it in Claude Desktop — no terminal needed. Auto-updates included. Also improved Outlook email guidance and privacy enhancements.

## v3.0.159 — 2026-05-01

One-click install: download the .mcpb extension and drop it into Claude Desktop. Also improved Outlook guidance — email tools now explain how to connect Exchange accounts.

## v3.0.158 — 2026-05-01

Your AI agent connects automatically. LMCP now detects when you install a new AI client and offers to configure it with one click — no manual config editing needed.

## v3.0.157 — 2026-05-01

Privacy improvement: problem reports now ask for your permission before sending, show a preview of what will be sent, and only include anonymous technical data. No personal information is ever transmitted.

## v3.0.156 — 2026-04-30

Email setup: LMCP now asks for your email during install. Teams and Slack connect faster on Windows. Search and list emails are smarter — no more timeouts on multi-account setups.

## v3.0.155 — 2026-04-30

Faster setup: LMCP now auto-restarts your AI client after install — no manual restart needed. Calendar events can now target a specific calendar by name.

## v3.0.154 — 2026-04-29

Notes search 10x faster with native query. Notes listing uses batch access (3 calls vs 200). Cloud relay on Windows. Enhanced tray with activity feed. Heartbeat every 5 min. 40 QA tests. Code-signed Windows binaries.

## v3.0.150 — 2026-04-28

Improved reliability of Email and Notes tools. Fixed Teams detection for accounts set up recently. Internal performance improvements.

## v3.0.147 — 2026-04-27

Uninstall now fully cleans AI client configs, security fixes for loopback binding and update verification

## v3.0.146 — 2026-04-27

Cross-platform Desktop Extension support: install Local MCP in Claude Desktop on macOS or Windows in two clicks.

## v3.0.145 — 2026-04-27

Language selector in tray, uninstall with feedback, bug fixes

## v3.0.144 — 2026-04-26

Fixed an issue where LocalMCPTray could not auto-start when launched from Claude Desktop on some machines. Fixed a bug where auto-updates could reset Calendar and Contacts permissions. Improved error messages when LocalMCPTray fails to install.

## v3.0.143 — 2026-04-26

Download for Windows button. Standalone installer — no Node.js required. 57 tools including daily briefing.

## v3.0.141 — 2026-04-26

57 Windows tools including daily briefing. System tray app. Auto-update. App detection telemetry. 3 new Windows setup guides.

## v3.0.140 — 2026-04-26

Windows installer now works with Microsoft Store Claude Desktop. Fixed MSIX path detection and npx command wrapper.

## v3.0.139 — 2026-04-26

Windows support (beta). 52 tools for Outlook, OneDrive, Excel, Teams, Slack and more. Install on Windows: npx local-mcp setup.

## v3.0.138 — 2026-04-25

Fixed a silent connection failure for users with multiple Node.js versions installed via nvm. If Claude Desktop was picking up an old Node version, LMCP would fail to start with no visible error. Now shows a clear message with the fix, and the correct Node version is always used automatically.

## v3.0.137 — 2026-04-25

Calendar permissions are now detected correctly — users with Add Events Only will see a fix prompt. Setup now works without Python or Homebrew on any Mac. Roo-Cline and Claude Code are now supported as AI clients in the tray. Email searches on machines with many accounts are more reliable.

## v3.0.136 — 2026-04-25

Install setup now captures which AI client was configured. Email prompt errors are now reported correctly. Bug fixes and reliability improvements.

## v3.0.135 — 2026-04-25

LMCP now restarts automatically if it stops unexpectedly — no more 'Local MCP is not running' errors after an update. The menu bar icon stays visible and reconnects on its own.

## v3.0.134 — 2026-04-25

Update reliability: LMCP now restarts cleanly after downloading an update — no more dropped connections in Claude Desktop. Search emails is faster, with a timeout so it never hangs on large mailboxes. Notes tools now work even when Notes.app is closed.

## v3.0.133 — 2026-04-24

Setup wizard now exits cleanly after completing instead of hanging in the terminal.

## v3.0.132 — 2026-04-24

Fixed a startup error that prevented the setup wizard from completing on fresh installs.

## v3.0.131 — 2026-04-24

Settings email now saves and shows instantly. Tray shows a banner when the server updates itself — prompting you to start a new conversation in your AI client.

## v3.0.125 — 2026-04-24

Fixed a crash that occurred when running multiple tool calls at startup. Messages, Notes, Safari, and Mail permission prompts now appear correctly when the app first launches.

## v3.0.124 — 2026-04-24

Fixed a false notification about missing Calendar and Reminders permissions. Messages now properly requests Automation access on first use.

## v3.0.123 — 2026-04-24

Mail, Safari, Notes, and Messages tools now work reliably on macOS 26 Tahoe. Fixed a permissions issue where system automations were silently blocked on newer macOS versions.

## v3.0.122 — 2026-04-24

Email, Notes, Messages, and Safari tools no longer lose access after an update. Fixed a reliability issue where tool permissions would reset each time the app updated.

## v3.0.121 — 2026-04-23

Email is faster (removed a per-message blocking call that caused timeouts on Exchange accounts). Teams chat messages now show better diagnostics when empty. OmniFocus tools handle missing app gracefully. Tray stays visible and auto-restarts after crashes.

## v3.0.120 — 2026-04-23

Fixed iMessage conversations not loading in list_message_chats.

## v3.0.119 — 2026-04-23

Mail, Messages, Notes, and Safari now reliably request the required permissions on first launch.

## v3.0.118 — 2026-04-23

Fixed a bug that could prevent the app from updating to newer versions on some Mac configurations.

## v3.0.117 — 2026-04-23

Fixed a bug where the app could get stuck on an older version and stop receiving updates.

## v3.0.116 — 2026-04-23

Automation permissions for Mail, Messages, Notes, and Safari are now requested automatically on first launch. No more silent permission failures after updates.

## v3.0.116 — 2026-04-23

Automation permissions for Mail, Messages, Notes, and Safari are now requested automatically on first launch. No more silent permission failures after updates.

## v3.0.115 — 2026-04-23

First-time setup now automatically installs the background process that handles Automation permissions for Mail, Messages, Safari, and Notes. This prevents permission resets after future updates.

## v3.0.114 — 2026-04-23

Automation permissions for Mail, Messages, and Safari no longer reset after updates. A new stable co-process handles all JXA automation so macOS grants it permanent access.

## v3.0.113 — 2026-04-22

Notes, Messages, Safari, and OmniFocus tools are now fully operational. Fixed a parsing bug that caused all JXA-based tools to return errors since manifest v9.

## v3.0.112 — 2026-04-22

Email, Calendar, Contacts, Notes, and Messages tools restored. Fixed a regression introduced in the previous release that caused several tools to appear unavailable or fail with permission errors on macOS 26.x.

## v3.0.111 — 2026-04-22

Settings now shows the manifest version. Bug fixes and stability improvements.

## v3.0.110 — 2026-04-22

New: report issues and request integrations directly from Claude. Added to-do list support. Performance improvements and bug fixes.

## v3.0.109 — 2026-04-22

The admin panel now shows which manifest version is running on each machine.

## v3.0.108 — 2026-04-22

Added support for JetBrains IDEs and Continue as AI client options. Settings and services can now update automatically.

## v3.0.106 — 2026-04-22

Reminders management is now complete — mark reminders done, delete them, and browse your lists directly from Claude.

## v3.0.105 — 2026-04-21

Calendar, Contacts, and Reminders tools now load dynamically — faster updates without reinstalling.

## v3.0.103 — 2026-04-21

Calendar, Contacts, and Reminders now show correctly as active after you've granted permission in System Settings. Fixed a display bug where these services appeared as 'Permission needed' even with Full Access enabled.

## v3.0.102 — 2026-04-21

Calendar, Contacts, and Reminders permissions now prompt correctly with the Local MCP icon.

## v3.0.101 — 2026-04-21

All macOS privacy dialogs (Calendar, Contacts, Reminders) now show the Local MCP icon. Reliability and performance improvements.

## v3.0.100 — 2026-04-21

Auto-updates now apply seamlessly without breaking your Claude Desktop connection. Silent tool failures are now automatically tracked and surfaced in the admin panel.

## v3.0.99 — 2026-04-21

Calendar and Reminders status in the menu bar now accurately reflects actual permissions. Fixed a rare issue where Calendar and Reminders could show as available even after macOS reset their permissions. Permission request dialogs now appear proactively for all three services on first launch.

## v3.0.98 — 2026-04-21

WhatsApp now available for all users. The app automatically installs and keeps WhatsApp tools up to date alongside every other update — no manual setup required. Contacts and Calendar permissions work reliably after updates. Fixed an issue where permissions could appear lost after an update, and another where the system permission dialog would never appear for Contacts. Cleaner System Settings: resolved an issue that caused multiple duplicate entries to accumulate in Privacy & Security over time.

## v3.0.97 — 2026-04-20

Tray Install button now triggers updates immediately. Fixed duplicate permissions notice after update. Better guidance when Teams channels or emails aren't accessible.

## v3.0.96 — 2026-04-20

Fixes a permission prompt that appeared when installing on macOS Sonoma and Sequoia. Email reliability improvements for Exchange and Outlook accounts — messages found by search are now accessible via read. Better error messages when Mail automation permission is not granted.

## v3.0.95 — 2026-04-20

Removed Microsoft 365 directory tools (connect_m365_account, search_m365_directory). These required Azure Active Directory setup and went against local-first principles. Your org directory is still searchable via Contacts — macOS syncs Exchange contacts locally through Contacts.app, no authentication required.

## v3.0.92 — 2026-04-20

You can now edit existing calendar events directly — change the title, time, location, or notes without canceling and recreating. Works with recurring events too (update just this one or all future occurrences).

## v3.0.91 — 2026-04-20

Email categories for Outlook/Exchange accounts, faster file search.

## v3.0.90 — 2026-04-20

Exchange email now works reliably. Read and search messages across all Exchange folders — including Sent Items and nested mailboxes — without errors or missing results.

## v3.0.89 — 2026-04-19

Anonymous cloud relay activation — no more email prompts during curl|bash installs. Cloud connect works out of the box; link an email later at local-mcp.com/settings to sync across Macs. (LMC-605)

## v3.0.85 — 2026-04-19

Bug fixes: graceful 45s drain before auto-update prevents dropped tool calls; self-update now restarts in stdio mode (fixes ~48 stuck machines); Gmail IMAP save_attachment retry fix; recover tray-less stuck machines; tray shows Not connected after 60s timeout. New: TCC auto-prompt for Calendar/Contacts/Reminders on startup; WhatsApp Connect button in tray menu.

## v3.0.84 — 2026-04-19

Fixed a crash where the tray showed as offline when WhatsApp was connected. Fixed duplicate tray icons appearing in the menu bar. Fixed background processes that were not cleaned up during a session. Improved monitoring for machines that go temporarily offline.

## v3.0.83 — 2026-04-19

- Fixed an issue where Excel files with only numbers wouldn't open
- Fixed zombie processes that accumulated when AI clients disconnected
- Permission setup is now faster — grant access directly from the menu bar
- Machines stuck on old versions will now update automatically

## v3.0.82 — 2026-04-18

Morning briefing in one call. New daily_brief tool combines your calendar, reminders, and inbox into a single morning overview. Also includes: improved setup flow, chat history blob handling fix, notification improvements, and UI rebrand to LMCP.

## v3.0.81 — 2026-04-18

v3.0.81: Fix TCC permission cascade, OneDrive cloud placeholders, daemon tunnel conflicts. Add fleet health monitoring, activation nudge, tray suggestions.

## v3.0.80 — 2026-04-18

Connection stability: fixes server disconnections after updates. Your Claude Desktop connection now stays alive through auto-updates.

## v3.0.79 — 2026-04-18

Connection stability: LMCP no longer disconnects from Claude Desktop after updates.

## v3.0.78 — 2026-04-18

Stability fix: resolves server disconnections after auto-update. Your tools stay connected now.

## v3.0.77 — 2026-04-18

Startup fix: automatically cleans up stale processes from previous versions. Resolves 'Server disconnected' errors after updates. Slack now visible in the menu bar.

## v3.0.76 — 2026-04-18

Tray fix: resolves 'Offline' status showing on all services after v3.0.74 update. Slack channels now visible in the menu bar. All your tools and data are safe — just a display fix.

## v3.0.75 — 2026-04-18

File reading is more reliable — Excel and Word tools no longer hang on cloud-synced files. If macOS resets app permissions after an update, the menu bar now shows a Fix Permissions prompt to get you back on track quickly.

## v3.0.74 — 2026-04-18

LMCP now guides you from install to first tool call. Smart prompts suggest what to try based on your connected apps. A new Recipes tab shows ready-to-use workflows you can copy and paste. Plus: Slack channel reading is here.

## v3.0.73 — 2026-04-17

OmniFocus is now instant. Previously, checking tasks could hang for up to 60 seconds when OmniFocus wasn't installed — now it responds immediately with a clear message. Cloud relay handles multiple requests simultaneously for faster email access.

## v3.0.72 — 2026-04-17

Email is more reliable. When Mail.app isn't running, you'll get a clear message instead of a long wait. Excel now handles iCloud files seamlessly. Calendar events with all-day dates and email replies work better. First-time users get helpful example prompts to get started faster. Several stability improvements for Ventura users.

## v3.0.71 — 2026-04-16

Fixed a bug where sending an email would leave a duplicate message in the Drafts folder.

## v3.0.70 — 2026-04-16

v3.0.70: fix list_emails JXA timeout on Ventura+Exchange (FB-C1D537) — budget whose() probe loops to 3s, preventing 13-probe×3s=39s overrun

## v3.0.69 — 2026-04-16

fix(mail): cache dateSent() + proactive outreach needed for D2494FB7 (LMC-39)

## v3.0.68 — 2026-04-16

LMC-40: show TRIAL badge for trial users (was FREE / Early adopter)

## v3.0.67 — 2026-04-16

fix(mail): LMC-39 eager property capture — eliminates deferred Exchange round-trips from list_emails sort+serialize

## v3.0.66 — 2026-04-16

LMC-29: lower stale_warning threshold 10→7 to push reinstall prompt to v3.0.56 stuck machines

## v3.0.65 — 2026-04-16

Teams IndexedDB fix (6910018) + identity tray prompt banner (ba9dea4) — CEO-approved bundle per LMC-9

## v3.0.63 — 2026-04-16

New onedrive_set_scope tool — your AI assistant can now restrict OneDrive access to a specific folder directly, no config file editing needed. Just ask: Restrict my OneDrive access to the Claude workspace folder.

## v3.0.62 — 2026-04-16

OneDrive folder scoping — restrict LMCP access to specific folders per OneDrive account. Configure allowed paths in config.json, enforced across all read, write, and delete operations. Built for enterprise teams with sensitive documents.

Smarter Safari automation — new back button tool, link extraction for navigating dashboards, and automatic page-load waiting after clicks.

Read 55+ file types from OneDrive — now supports HTML, TypeScript, Java, Go, Rust, SQL, Dockerfile, and many more code and config files.

New onedrive_file_info tool — get file size, dates, and type without listing the entire directory.

## v3.0.61 — 2026-04-16

Email is faster and more reliable on Exchange accounts. Inbox detection now uses a fast lookup before walking the mailbox tree, eliminating timeouts on deep folder hierarchies.

Smarter permission guidance. When a macOS permission is missing, your AI assistant now tells you exactly how to fix it before you hit an error.

Getting started suggestions. New users get concrete examples of what to ask — like Read my latest emails or What is on my calendar — so you can start using LMCP right away.

## v3.0.60 — 2026-04-15

The menu bar app now reads state directly from a shared file instead of polling your local server over HTTP, making it lighter and faster. Calendar now detects when macOS gives it limited access and shows a clear message explaining how to upgrade to full access in System Settings. The auto-updater no longer silently deadlocks on startup — a threading bug that prevented update telemetry from working since v3.0.54 has been fixed. Fresh installs no longer briefly flash an expired license warning. Activity counts in the menu bar now show cloud vs local calls separately.

## v3.0.59 — 2026-04-15

Reliability improvements to the auto-updater.

## v3.0.58 — 2026-04-15

Local MCP now gently asks for your email the first time you open the menu bar — so we can reach you if something breaks or when a major fix ships. You can dismiss the prompt and we won't ask again for a week, or permanently after a few dismissals. If you prefer to stay anonymous, just ignore it. No spam, no marketing — only important fixes and release notes.

## v3.0.56 — 2026-04-14

Email is much faster on corporate Outlook and Exchange accounts with lots of folders. Previously, asking Claude to 'check my unread email' could time out if your inbox was nested inside a deep folder tree. Now the email tool finds your inbox quickly and gracefully handles accounts that are mid-sync. Also fixed a documentation mismatch where the tool list mentioned Outlook-specific tools that didn't exist — the regular email tools work against Outlook accounts directly once you add them to Mail.app.

## v3.0.55 — 2026-04-14

Email now works reliably on Macs running in languages other than English. If your Mac's interface is in Spanish, French, German, Italian, Portuguese, Dutch, Japanese, Korean, Chinese, Russian, or most other languages, Claude and other AI agents can now find and read your inbox automatically without you having to spell out the exact mailbox name. This release also includes small behind-the-scenes improvements to the menu bar app and self-update health monitoring.

## v3.0.53 — 2026-04-14

Email is more reliable on accounts that take a moment to connect. When one account is slow, LMCP now moves on and shows you the messages from the rest instead of timing out. Saving attachments from Exchange mail is much more dependable too — LMCP retries automatically if the server is still downloading the file. OneDrive files open faster and give a clear message if they haven't finished syncing yet. The file reader now handles text files from banking systems and other legacy sources that use non-UTF-8 encodings. Calendar permission errors are clearer. Stock chart lookups are resilient to Yahoo rate limiting.

## v3.0.52 — 2026-04-12

Email attachments save reliably now. Reading emails on Exchange accounts is faster. OneDrive write errors show clear fix instructions.

## v3.0.51 — 2026-04-11

Cloud connections from Claude.ai and ChatGPT now work end-to-end. We fixed a routing bug that was preventing tool calls from reaching your Mac through the cloud relay, and we improved how permissions survive across updates so you should see fewer 'permission denied' messages right after auto-update.

## v3.0.48 — 2026-04-11

Listing emails on Macs with multiple accounts is now reliable — no more timeouts when asking Claude to read your inbox.

## v3.0.47 — 2026-04-11

Teams chat reading is now resilient to corrupted or outdated records in Microsoft Teams' local storage — no more empty results or errors when asking Claude to read a Teams conversation.

## v3.0.46 — 2026-04-11

list_emails is now reliable with multiple Mail accounts on macOS Sequoia — no more stalls or empty results when you ask Claude to check your inbox.

## v3.0.45 — 2026-04-11

Better admin telemetry for TCC permission state — we can now spot machines that need permission re-enabling after macOS updates.

## v3.0.44 — 2026-04-11

Admin analytics now reflect the real number of tool calls per machine — previously stuck at zero for stdio clients.

## v3.0.43 — 2026-04-11

Tray email changes now sync to the admin dashboard and cloud relay in real time.

## v3.0.42 — 2026-04-11

Microsoft Teams now works for all users (multi-tenant). Cleaner admin push messages. Better warnings for outdated installs.

## v3.0.41 — 2026-04-11

Fixes 4 bugs found during QA: better error messages for missing files, admin trial-users dashboard, cleaner errors when reading missing chats/notes, and correct version number in tray About box.

## v3.0.40 — 2026-04-10

Cleaner permission management. Also fixes Gmail/Exchange/iCloud inbox detection and Teams chat duplicates.

## v3.0.39 — 2026-04-10

Fixes a critical bug where macOS privacy panel was filling with duplicate LMCP entries on every update. Also fixes Gmail/Exchange/iCloud inbox detection and Teams chat duplicates.

## v3.0.37 — 2026-04-10

Smarter problem reports — Claude.ai now auto-attaches versions, permissions, recent logs, and tool history when something fails.

## v3.0.36 — 2026-04-10

Smarter problem reports — Claude.ai now auto-attaches versions, permissions, recent logs, and tool history when something fails.

## v3.0.35 — 2026-04-10

Bug reports and feature requests now reach the team. Feature Requests panel shows only real requests. Support email updated.

## v3.0.34 — 2026-04-10

Cloud connection more reliable. Tray reliably cleans up after crash. Permission warnings now appear after macOS resets them.

## v3.0.33 — 2026-04-10

Calendar/Contacts permissions: clearer error messages and a tray notification when macOS resets them after an update.

## v3.0.32 — 2026-04-10

VS Code setup now works correctly. Improved AI client detection.

## v3.0.31 — 2026-04-10

Faster cloud responses — list_emails and other tools no longer make the connector time out.

## v3.0.30 — 2026-04-10

Cloud connection status updates faster and more reliably.

## v3.0.29 — 2026-04-10

Fixes tray showing 'connecting' when the cloud tunnel is actually up.

## v3.0.28 — 2026-04-10

Cloud connection now self-heals after updates and network drops — no more stuck tunnels.

## v3.0.27 — 2026-04-10

Fix: the tray app now auto-updates correctly when the daemon does. Previously the daemon could keep updating its own binary while the tray stayed on the original installed version forever.

## v3.0.26 — 2026-04-10

One-click OAuth approval from the menu bar. When ChatGPT or Claude.ai web requests access, you get a notification on your Mac and click Approve once — no more copying tokens.

## v3.0.25 — 2026-04-10

Daemon now auto-updates itself: when a new version ships, the daemon downloads it and restarts within ~3 seconds without losing the cloud tunnel for long. No manual restart needed.

## v3.0.24 — 2026-04-10

Cloud Relay tunnel now stays connected even when you close every MCP client. The LMCP menu bar app keeps a dedicated daemon alive so Claude.ai web and ChatGPT keep working without needing Claude Desktop running in the background.

## v3.0.23 — 2026-04-10

Recent activity history shows your last MCP tool calls in the menu bar. Update notifications now include release notes inline. Behind the scenes: refresh tokens, revoke endpoint, faster admin telemetry, and security headers.

## v3.0.22 — 2026-04-10

Fix: list_emails and search_emails now work on Macs set to Spanish, French, German and 13 other languages. Previously they could return empty for accounts whose inbox was named in your local language (e.g. 'Bandeja de entrada' in Spanish).

## v3.0.21 — 2026-04-10

Tray icon now pulses when there is MCP activity — green for local stdio calls and indigo for Cloud Relay calls. New step-by-step guide for Claude.ai web setup. Tested end-to-end with real Mail.app accounts via Cloud Relay.

## v3.0.20 — 2026-04-10

Redesigned settings page with clearer Home dashboard and dedicated Connect tab. ChatGPT and Claude.ai web setup is now guided with copy-ready credentials in the menu bar. Settings page opens reliably after updates.

## v3.0.19 — 2026-04-10

Cloud Data Forwarding toggle now translated to 10 languages (Spanish, Portuguese, French, German, Italian, Dutch, Chinese, Japanese, Korean).

## v3.0.18 — 2026-04-10

Cloud Relay is now privacy-first by default. Cloud agents (claude.ai, sheet add-ins) only see setup tools unless you opt in. Toggle 'Cloud Data Forwarding' from the menu bar when you want them to access Mail, Calendar, Teams, and OneDrive on this Mac. Also fixes a duplicate connection issue when running multiple AI client conversations.

## v3.0.17 — 2026-04-08

Fixed tray build — now correctly compiles with TrayStrings.swift. LMCP branding in tray menu bar.

## v3.0.16 — 2026-04-08

Tray rebrand to LMCP. Server binary auto-updates on version mismatch.

## v3.0.15 — 2026-04-08

Server binary now auto-updates when a new version is available. Previously, machines could stay on old versions indefinitely. Also includes all recent bug fixes and the LMCP rebrand.

## v3.0.14 — 2026-04-06

LMCP is now free for all early adopters — no more trial countdown. Your license never expires. Also: new name (LMCP), PDF reading fixed, calendar dates corrected, OneDrive auto-download.

## v3.0.13 — 2026-04-06

LMCP is the new name. Same product, same tools, shorter name. Also includes: PDF reading fixed (native PDFKit), calendar all-day dates corrected, OneDrive files auto-download.

## v3.0.11 — 2026-04-06

PDF files now open reliably — no more dependency errors. Calendar all-day events show the correct end date. OneDrive files download automatically when your AI reads them — no need to open Finder first.

## v3.0.8 — 2026-04-05

Send rich HTML emails. You can now send beautifully formatted emails with tables, links, and styling using the new html_body parameter. Cloud connector discovery is smarter — AI agents get useful tool descriptions and one-command install instructions.

## v3.0.7 — 2026-04-05

Send rich HTML emails. The send_email tool now supports an html_body parameter, so you can send beautifully formatted emails with tables, links, and styling — directly from your AI agent.

## v3.0.6 — 2026-04-05

Settings page now dynamically shows all available services. NordVPN appears in both the menu bar tray and Settings when installed.

## v3.0.5 — 2026-04-05

NordVPN now appears in the menu bar tray with real-time connection status. Your VPN section shows whether you're connected or disconnected, updating automatically.

## v3.0.4 — 2026-04-05

Fixed: Contacts app no longer opens unexpectedly. A background process was briefly launching the Contacts app every minute — this is now resolved.

New: NordVPN integration. Check your VPN connection status, get server recommendations by country, and run diagnostics — all from your AI assistant. Connect/disconnect is still done in the NordVPN app.

## v3.0.3 — 2026-04-05

The app now speaks your language. Tray, settings, and web are available in Italian, Dutch, and 10 other languages — auto-detected from your system preferences.

## v3.0.2 — 2026-04-05

Teams integration is now more reliable with timeout protection. Email listing is faster for accounts with many folders. Better error messages for OneDrive cloud files and PowerPoint.

## v3.0.1 — 2026-04-05

Outlook integration now guides you to connect accounts through Mail.app for full email access. Claude Code is now automatically configured during setup. Smarter version numbering for more reliable updates.

## v3.0.0 — 2026-04-05

Version numbering is now clearer and more consistent. Under the hood, all version comparisons have been upgraded to full semantic versioning for more reliable updates.

## v2.13 — 2026-04-05

Smarter updates and self-healing. Excel and PowerPoint tools now auto-install dependencies. Improved AI client detection for Claude Desktop and Cursor. Leave a review directly from your AI assistant. Push notifications now reach your menu bar.

## v2.12 — 2026-04-04

Smarter updates. Your AI clients now auto-detect and connect to the latest version of Pilot MCP. Improved AI client detection for Claude Desktop, Cursor, Windsurf, and VS Code. Push notifications from the admin now reach your menu bar. Leave a review directly from your AI assistant with the new leave_review tool.

## v2.11 — 2026-04-04

Excel, Word, and PowerPoint now work out of the box — no manual setup needed.

## v2.10 — 2026-04-04

Reduced battery and network usage. Teams now connects automatically.

## v2.9 — 2026-04-04

Teams integration now works out of the box. Improved automatic component updates.

## v2.8 — 2026-04-04

Fixed automatic updates failing on restart. Improved reliability.

# Changelog

All notable changes to Local MCP are documented here.


## v1.142 — 2026-04-02
Removed duplicate To Do entry from the menu bar — To Do works via macOS Reminders sync and is shown there. Documentation updated to clarify how Microsoft To Do integrates.

## v1.141 — 2026-04-02
Admin panel now shows which AI client (Claude Desktop, Cursor, Windsurf, VS Code) is connected per machine.

## v1.140 — 2026-04-02
Fixed a conflict where the old server version kept running after upgrading, causing two processes to compete for the same port.

## v1.139 — 2026-04-01
New: Stocks tools — live quotes, historical chart data, and symbol search via Yahoo Finance. No API key required.

## v1.138 — 2026-04-01
New: Microsoft To Do tools — list, create, and complete tasks directly from your AI client. Works via macOS Reminders sync.

## v1.137 — 2026-04-01
New: `version_info` tool shows server, tray, and teams-proxy versions. `list_my_feedback` now shows live open/closed status of your submitted reports.

## v1.136 — 2026-04-01
Fixed item counts showing true/false instead of numbers. Calendar same-day queries now return all events for that day. Clearer error messages for Outlook, Messages, and Safari.

## v1.135 — 2026-04-01
Teams tools now work automatically without manual setup.

## v1.134 — 2026-04-01
Machine timeline and tool usage metrics in admin panel.

## v1.133 — 2026-04-01
Admin panel now shows tray version per machine.

## v1.132 — 2026-04-01
Cloud Relay stays connected reliably.

## v1.131 — 2026-04-01
Fixed settings page errors and Cloud Relay status display.

## v1.130 — 2026-04-01
Server status refreshes every 30 seconds. Updates install automatically in the background.

## v1.129 — 2026-04-01
Detailed logs now written to server.log for easier debugging.

## v1.128 — 2026-04-01
Cloud Relay connection reliability improvements. Machine activity now visible in dashboard.

## v1.127 — 2026-04-01
Server now checks for updates every 30 minutes automatically.

## v1.126 — 2026-04-01
Contacts now detected even without full permissions. Cloud Relay no longer shows "Connecting" when not configured.

## v1.125 — 2026-04-01
OmniFocus: inbox filter, defer dates, flagged tasks, and completed task support. New quick prompts for emails and calendar.

## v1.124 — 2026-04-01
Cloud Relay: connect Claude.ai and ChatGPT remotely without keeping a local connection open.

## v1.123 — 2026-04-01
Settings page can now detect and auto-configure Claude Desktop, Cursor, VS Code, Windsurf, and Zed.

## v1.111–v1.122 — 2026-04-01
Stability improvements, performance fixes, and internal pipeline updates.

## v1.110 — 2026-04-01
Admin: machines table now shows license email and online status.

## v1.109 — 2026-04-01
Beta channel support: mark machines as beta testers from the admin panel to receive builds before they go to all users.

## v1.108 — 2026-04-01
Setup wizard is now fully in English. Improved first-run experience.

## v1.107 — 2026-04-01
Settings page now loads correctly.

## v1.106 — 2026-04-01
Settings page now works correctly in all installation modes.

## v1.105 — 2026-04-01
Settings page now works correctly when running via npm/Claude Desktop.

## v1.104 — 2026-04-01
Tray now updates automatically when the server starts. Fixes the Install button not working on older tray versions.

## v1.103 — 2026-04-01
Fixed recurring permission dialog — Teams data is no longer accessed every 60 seconds in the background. The permission prompt now only appears when you actively use Teams tools, not constantly in the background.

## v1.102 — 2026-04-01
Fixed recurring permission dialog — server now has a stable code-signing identity that macOS remembers. No more repeated prompts after allowing once.

## v1.101 — 2026-04-01
Fixed recurring TCC permission dialog — the server binary now has a stable code-signing identity so macOS remembers the permission. No more repeated prompts.

## v1.100 — 2026-04-01
Install button now works correctly. Update banner shows whether it's a server or tray update.

## v1.99 — 2026-04-01
Tray now shows server status correctly in all installation modes. Restart button gives feedback while server is restarting. Tray version always visible in menu bar.

## v1.98 — 2026-04-01
The menu bar icon can now be hidden without stopping the MCP server. macOS and chip type now visible in the admin dashboard.

## v1.97 — 2026-04-01
Fixed permission dialogs appearing every 30 seconds in npm mode.

## v1.96 — 2026-04-01
Cloud Relay now connects reliably in all installation modes.

## v1.95 — 2026-04-01
Cloud Relay now connects reliably. All services (Mail, Calendar, etc.) now appear correctly in the menu bar.

## v1.94 — 2026-04-01
Improved reliability after Mac restart — menu bar now stays connected. Minor fixes and improvements.

## v1.93 — 2026-04-01
Menu bar icon now shows correctly in Finder and Launchpad. Server status is now visible in the menu bar after a Mac restart.

## v1.92 — 2026-03-31
Menu bar app now appears in /Applications for easy access. Fixed update button for all users.

## v1.91 — 2026-03-31
Install button now works correctly — server updates and restarts automatically. Fixed auto-update for npm users.

## v1.90 — 2026-03-31
Menu bar icon now updates automatically on Claude Desktop restart. Admin panel shows server and tray versions separately.
---

## v1.87 — 2026-03-31
More stable cloud connection. Clearer setup for ChatGPT and Claude.ai integration.

## v1.86 — 2026-03-31
Introducing suggested prompts — click + in Claude Desktop to see "Check my inbox", "Today's schedule" and more. Tap Report a Bug in the menu bar to send feedback instantly.

## v1.85 — 2026-03-31
You can now report bugs directly from the menu bar. Cleaner post-install instructions. Better experience for Windows users visiting the site.

## v1.84 — 2026-03-28
Deploy pipeline improvements across all distribution channels.

## v1.81 — 2026-03-28
Deploy pipeline improvements. All version numbers now sync automatically across npm, MCP Registry, and MCPB bundle.

## v1.76 — 2026-03-28
License activation from Settings UI. All 56 tools verified. Improved admin panel with trial days, plan type, and timezone. Quit stops all processes.

## v1.71 — 2026-03-28
Unique device tracking across all surfaces. Email change in Cloud Relay now updates correctly. Create email folders. 54 AI tools.

## v1.60 — 2026-03-28
Settings changes now persist correctly across restarts. Full UTF-8 support for calendar names in all languages.

## v1.56 — 2026-03-28
Fine-grained permissions — control Read and Write access separately for each email account, calendar, OneDrive folder, and Teams tenant. See available tools per service.

## v1.55 — 2026-03-28
Live log viewer with color-coded levels (errors in red, warnings in orange). Bug reports now automatically include diagnostic data for faster resolution.