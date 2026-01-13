# multimodal-document-ai-evaluation

## Überblick
Dieses Repo enthält eine schlanke, CPU-freundliche Evaluationsstrecke für **FUNSD** mit **LayoutLM** und **LayoutLMv3**. 
Die Notebooks sind so aufgebaut, dass sie auf **macOS CPU-only (8 GB RAM)** reproduzierbar ausführbar sind.

## Kurzbeschreibung des Projekts
Das Repository dokumentiert eine Forschungsprojektarbeit im Bereich Document AI mit dem Fokus auf vergleichende Modellanalysen. Im Zentrum steht ein kontrollierter Vergleich von LayoutLM und LayoutLMv3 auf dem FUNSD-Datensatz unter klar definierten Rahmenbedingungen.

Ziel ist ein methodisch nachvollziehbarer, ressourcenbeschränkter Benchmark auf CPU-only-Hardware. Die Ergebnisse sind für Analyse und Diskussion gedacht und dienen als belastbare Grundlage für wissenschaftliche Argumentation, nicht als State-of-the-Art-Optimierung.

## Methodischer Scope (stichpunktartig)
- Datensatz: FUNSD
- Modelle: LayoutLM, LayoutLMv3
- Trainingsmodus: Fine-Tuning, fixer Seed
- Ziel: Vergleich innerhalb einer Modellfamilie

## Reproduzierbarkeit & Limitationen
- CPU-only Setup
- begrenzte Epochen / Batch Sizes
- bewusste Fokussierung auf wenige Modelle
- Nutzung im Rahmen einer wissenschaftlichen Arbeit (Analyse und Diskussion)
- kein Anspruch auf State-of-the-Art-Optimierung

## Schnellstart (macOS CPU-only)
1. Stelle sicher, dass Python 3.10–3.11 installiert ist (für `torch` aktuell stabil). Prüfe die Version mit:
   ```bash
   python3 --version
   ```
   Falls die Version nicht passt, installiere eine passende Version und nutze sie explizit, z. B. auf macOS mit Homebrew:
   ```bash
   brew install python@3.11
   python3.11 --version
   ```
   Verwende dann die gewünschte Version beim Erstellen der venv:
   ```bash
   python3.11 -m venv .venv
   ```
2. Erstelle eine virtuelle Umgebung und aktiviere sie:
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```
3. Installiere die Abhängigkeiten:
   ```bash
   pip install -r requirements.txt
   ```

4. Starte die Notebooks in der angegebenen Reihenfolge (siehe unten). Nutze z. B. `jupyter notebook` oder `jupyter lab`.

## Notebook-Reihenfolge
1. `01_setup_and_sanity.ipynb` – Setup & Sanity-Checks
3. `02_layoutlm_dryrun.ipynb` – LayoutLM Dry-Run
4. `03_layoutlm_fullrun.ipynb` – LayoutLM Full-Run
5. `04_layoutlmv3_runs.ipynb` – LayoutLMv3 Runs

