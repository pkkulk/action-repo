# Action Repository (Simulation)

This repository contains the simulation script used to test the **Webhook Receiver** application.

## Purpose
Since testing webhooks with a live GitHub repository can be slow or complex, this script (`simulate_events.py`) lets you instantly send fake "Push", "Pull Request", and "Merge" events to your local server.

## How to Use

### 1. Start your Webhook Server
Make sure your Flask app (from `webhook-repo`) is running on `http://localhost:5000`.

### 2. Run the Simulation
Run the following command in your terminal:
```bash
python3 simulate_events.py
```

### 3. Check the Result
- Look at your terminal: You should see "Status: 200" for each event sent.
- Look at your Webhook Receiver Dashboard: The new events ("Prathmesh pushed...", etc.) should appear in the list.

## Events Simulated
- **PUSH**: Simulates a commit push to the `staging` branch.
- **PULL_REQUEST**: Simulates opening a PR from `staging` to `master`.
- **MERGE**: Simulates merging a PR from `dev` to `master`.
