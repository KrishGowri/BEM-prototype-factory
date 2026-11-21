# BEM Prototype Factory

A small Streamlit application that creates downloadable EnergyPlus IDF starter models from user-selected building and operating assumptions.

## Run locally

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
streamlit run app.py
```

## What it generates

- One rectangular thermal zone with a configurable footprint, story height, and window-to-wall ratio.
- Basic envelope layers and simple glazing.
- Occupancy, lighting, equipment, infiltration, heating/cooling setpoints, and ideal-loads HVAC.
- A representative California Energy Commission climate-zone location and an editable EnergyPlus IDF download.

The `CalBEM` and `DEER` options are prototype-family labels only. This repository does not include official CalBEM or DEER prototype inputs. Defaults are transparent, generic starter assumptions and should not be interpreted as canonical, calibrated, or code-compliant standards data. Construction vintage is also currently a label, not a vintage-specific envelope library.

The output is a minimal, single-zone starter model—not a full-building prototype. It does not bundle an EPW weather file; provide a suitable weather file in the EnergyPlus workflow. Validate the IDF with the EnergyPlus version you will use and inspect its warnings before relying on simulation results.
