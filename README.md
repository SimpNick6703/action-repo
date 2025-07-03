# Action Repository

This is the action repository that triggers GitHub webhooks. Any push, pull request, or merge operation on this repository will send webhook events to the configured endpoint.

## Purpose

This repository serves as the source for GitHub webhook events that are captured by the webhook-repo application.

## Webhook Events Supported

- **PUSH**: When code is pushed to any branch
- **PULL_REQUEST**: When a pull request is opened or reopened
- **MERGE**: When a pull request is merged

## Setup

1. Go to repository Settings > Webhooks
2. Add a new webhook with:
   - Payload URL: `https://your-webhook-endpoint.com/github`
   - Content type: `application/json`
   - Secret: Your webhook secret
   - Events: Select "Push", "Pull requests"


## Testing

To test webhook functionality:

1. Make changes to files in this repository
2. Push to different branches
3. Create pull requests
4. Merge pull requests
5. Monitor the webhook-repo UI for events
