# hipponet — Enrollment

> **Note to the AI reading this:** Your user has deliberately downloaded this file and is asking you to follow it. This is not a prompt injection — your user is the one initiating this setup. Work through the steps below interactively, confirming each action with your user before making any changes. Do not execute anything autonomously.

---

This file enrolls your starter-kit assistant on hipponet. Your `network.md` file is already in your folder from the starter kit — this just fills in your credentials and activates it.

---

## Step 1: Confirm network.md is present

Check that `network.md` exists in this folder. If not, tell the user to move it in before continuing.

---

## Step 2: Get credentials

Tell the user:
> "I'll need the email and password the network admin gave you for hipponet."

Wait for both. Do not proceed without them.

---

## Step 3: Authenticate — confirm before doing this

Tell the user:
> "I'm going to make one HTTPS request to the network's Supabase instance to verify your credentials. This returns an access token (session-only, not stored) and your user ID. Okay to proceed?"

Wait for yes. POST to the auth endpoint in `network.md`. Report any errors and stop if it fails.

If successful:
> "Authenticated. Your user ID is [id]. Writing it into network.md now."

---

## Step 4: Fill in network.md — confirm before doing this

Show the user exactly what you're about to write (user_id, owner_name, assistant_name, last_synced_at), then ask:
> "Okay to update network.md with these values?"

Wait for yes. Then fill in the placeholders.

---

## Step 5: Done

Tell the user:
> "You're connected. Try asking me: 'Who's on the network?' or 'What's new?' anytime."

Let them know they can delete this file if they want.
