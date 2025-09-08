name: Event Name Detector

# Define events that trigger this workflow
on:
workflow_dispatch:     # Manual trigger
push:                  # Trigger on push to any branch
pull_request:          # Trigger on pull request events

jobs:
echo:
name: Display Trigger Event
runs-on: ubuntu-latest

    steps:    
      - name: Checkout Repository
        uses: actions/checkout@v3

      - name: Show Trigger Event
        run: echo "I've been triggered by ${{ github.event_name }} event"
