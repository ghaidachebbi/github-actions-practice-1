name: Event Name Detector

on:
workflow_dispatch:   # Exécution manuelle
push:                # À chaque push
pull_request:        # À chaque création/modification/fermeture de PR

jobs:
echo:
runs-on: ubuntu-latest

    steps:
      - name: Show trigger name
        run: echo "I've been triggered by ${{ github.event_name }} event"
