# CPU Scheduling Simulator

A fully in-browser CPU Scheduling Simulator built with **PyScript** — no server required. Python runs entirely in the browser via WebAssembly.

🔗 **Live demo:** _your-vercel-url.vercel.app_

---

## Algorithms Supported

| Algorithm | Type |
|---|---|
| FCFS | Non-preemptive |
| SJF | Non-preemptive |
| SRTF | Preemptive (SJF) |
| Round Robin | Preemptive (configurable quantum) |

## Output

- Gantt charts for all 4 algorithms
- Per-process timing tables (WT & TAT)
- Performance comparison bar chart
- Edge-case detection & handling report
- Download chart as PNG

## Files

| File | Purpose |
|---|---|
| `index.html` | Main app (PyScript HTML — deployed to Vercel) |
| `cpu_scheduler_pyscript.html` | Same as index.html (local copy) |
| `cpu_scheduler (1).py` | Original standalone Python script |
| `cpu_scheduler_app.py` | Python HTTP server version (local use only) |

## Run Locally

**Option 1 — Static (PyScript):** Just open `index.html` in Chrome/Edge.
> If you see CORS errors, serve it:
> ```bash
> python -m http.server 8080
> # then open http://localhost:8080
> ```

**Option 2 — Python Server:**
```bash
pip install matplotlib numpy
python cpu_scheduler_app.py
# opens http://localhost:8765 automatically
```

## Deploy to Vercel

```bash
npm i -g vercel
vercel --prod
```

Or connect the GitHub repo in the [Vercel dashboard](https://vercel.com/new) for auto-deploy on every push.

## Tech Stack

- **Frontend:** Vanilla HTML + CSS + JavaScript
- **Python runtime:** [PyScript](https://pyscript.net/) (Pyodide / WASM)
- **Plotting:** matplotlib + numpy
- **Hosting:** Vercel (static)
