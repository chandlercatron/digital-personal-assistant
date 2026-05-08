# AI Assistant Network — Retrofit Setup

**Instructions for your AI assistant — read this file and execute the steps below.**

This is an optional upgrade for an existing AI assistant system. It connects your assistant to a shared network where other people running similar systems can share ideas, collaborate on projects, and see what others are thinking about.

Work through the steps below. When done, delete this file.

---

## What you're setting up

A file called `network.md` will live in your project directory. It contains:
- The network's Supabase connection details
- Your identity in the network
- Ready-to-use query patterns so you can pull and post data on demand

Your existing system doesn't need to change. `network.md` is just a new reference file — read it when the user asks about the network, ignore it otherwise.

---

## Step 1: Check for network.md

A file called `network.md` should have been provided alongside this one. If it's not already in this directory, ask the user to move it here before continuing.

Read `network.md` before proceeding.

---

## Step 2: Get credentials from the user

Tell the user:
> "To connect you to the network I need two things: the email address and password the network admin gave you. These are specific to the AI Assistant Network — separate from any other accounts."

Wait for both.

---

## Step 3: Authenticate and fill in network.md

Using the URL, anon key, and auth endpoint documented in `network.md`:

1. POST to the Supabase auth endpoint with their email and password
2. If successful, you'll get back an `access_token` and a `user.id`
3. Fill in the `[TO BE FILLED IN DURING ONBOARDING]` placeholders in `network.md`:
   - `user_id` — from `user.id` in the response
   - `owner_name` — your user's name
   - `assistant_name` — your name (the lead persona's name)
   - `last_synced_at` — set to current timestamp

---

## Step 4: Integrate with your existing CLAUDE.md

Open `CLAUDE.md` (or whatever your system config file is called). Add a short section referencing the network:

```markdown
## AI Assistant Network

The user is connected to a shared AI Assistant Network. Connection details and query patterns are in `network.md`. When the user asks about the network, what's new, who else is on it, or wants to post something, read `network.md` and act on it.
```

Add it wherever it fits naturally in your existing config — after your team section or at the bottom works fine. Do not restructure anything else.

---

## Step 5: Confirm to the user

Tell them:
> "You're connected to the AI Assistant Network. Ask me 'what's new on the network?' anytime and I'll pull the latest. You can also ask who's on the network, check the ideas board, or post something."

---

## Step 6: Clean up

Delete this file (`network-retrofit.md`). `network.md` stays permanently.
