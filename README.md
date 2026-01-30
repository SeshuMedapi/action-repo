# action-repo

This repository is used to generate GitHub events that are consumed by an external webhook service.

It is intentionally kept simple and is only responsible for triggering events such as:
- Push
- Pull Request
- Merge

These events are sent to the webhook server (via GitHub Webhooks) for further processing and storage.

---

## Purpose

This repository exists to:
- Trigger GitHub events
- Send those events to a webhook endpoint
- Help test the complete webhook → backend → database → UI flow

---

## Events Used

The following GitHub events are enabled:
- `push`
- `pull_request`
- `merge`

## How to Test

1. Clone the repository:
git clone <our-action-repo-url>

2. Make any code change:
git add .
git commit -m "Test push event"
git push

3. OR create a Pull Request:
Create a new branch
Push changes
Open a PR to main

4. These actions will automatically trigger webhook events.

5. Expected Result:
Events are successfully sent to the webhook server
Events are stored in MongoDB
Events appear in the UI of the webhook application

