# Hi, I'm Joshua Nancey 👋 — Mathematical Modeling, Trustworthy AI & Systems Engineer

🎓 **M.Eng. in Computer Science, Artificial Intelligence & Mathematical Modeling (`Label Mod'Math`)** — **Université de Technologie de Compiègne (UTC)** *(Graduated Sept. 2026)*  
📍 Paris, France · 🌐 Open to roles in **France, Switzerland, Germany, Netherlands, UK & Remote**  
🔗 **[Interactive Portfolio](https://joshdeutc.github.io)** · **[LinkedIn](https://www.linkedin.com/in/joshua-nancey-3218171a2)** · 📫 **joshua.nancey@etu.utc.fr**

---

### 🧭 About Me / Profil

> **EN:** Engineer bridging **rigorous mathematical modeling** (*stochastic processes, mathematical optimization, finite-sample statistical risk bounds, differential geometry*) and **production-grade AI & software systems** (*high-resolution medical vision, grounded clinical LLMs under strict GPU budgets, real-time collaborative servers, and OS-level Linux/Android security architectures*).
>
> **FR :** Ingénieur diplômé de l'**UTC Compiègne** (Génie Informatique — Filière **IAD** & Label **Mod'Math**), à l'interface entre la **modélisation mathématique rigoureuse** (*optimisation, processus stochastiques, garanties statistiques de risque en échantillon fini, géométrie différentielle 3D/4D*) et l'**ingénierie logicielle & IA de bout en bout** (*vision médicale haute résolution, LLMs cliniques sans hallucination sous contrainte GPU, architectures distribuées et sécurité système Linux/Android*).

---

### 🏆 Featured R&D & Engineering Projects

#### 1. 🏥 Medical AI, Statistical Risk Control & Grounded Clinical LLMs
- **[`tn10-medical-ai-showcase`](https://github.com/joshdeutc/tn10-medical-ai-showcase)** — *Epiconcept R&D Internship (6 months)*
  - **Part 1 (High-Resolution Mammography & Guaranteed Risk):** Fine-tuned the interpretable **GMIC** (`ResNet-22` global saliency + `ResNet-18` local patch attention) on **300+ GB** of 16-bit mammograms (RSNA, `2944×1920`), boosting AUC from `0.683` to **`0.889` (`95% CI: [0.858, 0.921]`)**. Implemented distribution-free **Selective Classification (SGR / Hoeffding bounds)** simultaneously bounding false-negative (`FNR ≤ 5%`) and false-positive (`FPR ≤ 5%`) clinical risks.
  - **Part 2 (`CATH-LLM` — European ECDC Infection Surveillance):** Benchmarked **20 local LLM configurations** (`MedGemma-27B`, `MedGemma-4B`, `Gemma-2-27B`, `Qwen-2.5-32B`, `Mistral-Small-24B`) on **MIMIC-IV** under a single **NVIDIA A100 40 GB** budget. Built a deterministic **verbatim grounding verifier** (`evidence_is_grounded`, `F1 = 0.91`) and demonstrated zero-shot cross-lingual transfer to **Croatian** clinical notes (**`F1 = 0.88`** via `NLLB-200` / `EuroLLM-9B`).
- **[`data-capsule-deep-piste`](https://github.com/Epiconcept-Paris/data-capsule-deep-piste)** — Co-authored an **8-chapter Dockerized interactive training capsule** transferring deep learning, uncertainty estimation (`MC Dropout`, `Deep Ensembles`), and selective risk control to public-health epidemiologists and data scientists.

#### 2. 📐 3D/4D Implicit Neural Surfaces & Biomechanical Modeling
- **[`surfaces-implicites`](https://github.com/joshdeutc/surfaces-implicites)** — *BMBI Lab Research Project (CNRS UMR 7338, UTC)*
  - Modeled 3D & 4D space-time deformable biological membranes (red blood cells & micro-capsules in shear flow) via continuous implicit level-sets $f_\theta(x,y,z,t) = 0$.
  - Compared polynomial regression (recovering the exact **Kuchel quartic in 10 coefficients** vs. `197,886` neural parameters), **3D Fourier features**, and **4D SIREN / Positional Encoding MLPs** with **Eikonal regularization** ($\|\nabla f\| = 1$), achieving **`IoU = 99.65%`** on non-affine capsule deformations.
  - Computed exact **Gaussian ($K$) and Mean ($H$) curvatures** via **2nd-order PyTorch `autograd`** without mesh discretization, verifying the **Gauss-Bonnet theorem** ($\oint K\,dA = 4\pi$) to **`0.025%` precision**.

#### 3. 📊 Tabular Deep Learning & Contextual Anomaly Detection
- **Contextual Anomaly Detection Platform** — *Aubay Innovation Lab Internship (6 months)*
  - Benchmarked **PyTorch Tabular** architectures (**GANDALF**, **FT-Transformer**, **TabTransformer**) coupled with **Isolation Forest** and **Deep Isolation Forest (DIF)** on mixed numerical/categorical datasets (`F1 = 0.903`, `ROC-AUC = 0.985`).
  - Engineered a full-stack **Flask REST API + React** web platform integrated with **AWS S3** and reproducible **Conda/Docker** environments.
- **[`Machine-learning-prediction`](https://github.com/joshdeutc/Machine-learning-prediction)** — *Statistical Learning & Clustering (`SY09`)*: Logistic regression with **Wald statistical tests**, Euclidean/Bayesian classifiers, and **Gower-distance / Adaptive Mahalanobis K-Means** on clinical cardiac data.
- **[`ETL-project`](https://github.com/joshdeutc/ETL-project)** — *Data Warehouse & Carbon Footprint Analytics (`NF26`)*: End-to-end Python ETL pipeline and dimensional modeling on the **ADEME Base Carbone** dataset.

#### 4. ⚙️ Distributed Systems, Security Architecture & AI Tooling
- **[`pdf-live-notes`](https://github.com/joshdeutc/pdf-live-notes)** — **Real-Time Human Stylus + AI Collaborative PDF Workspace**: **FastAPI + Server-Sent Events (SSE)** backend and **PDF.js + Perfect-Freehand** frontend enabling an AI agent to stream live vector annotations, spatial highlights, and sandboxed **interactive HTML5 simulation widgets (`<iframe>`)** directly onto a user's tablet canvas, paired with a native **Android Kiosk** client (`LockTask`).
- **[`monlycee-relay`](https://github.com/joshdeutc/monlycee-relay)** — **Zero-Trust Cloud Session Broker & Manifest V3 Browser Extension**: Offloads **Keycloak SSO** authentication to a remote Linux cloud microservice (**FastAPI + Playwright Headless Chromium** with `asyncio.Lock` concurrency and `< 50 ms` RAM session cache) and injects authenticated cookies into Microsoft Edge via a **Manifest V3 Service Worker** without ever storing credentials on the client machine.
- **[`custos`](https://github.com/joshdeutc/custos)** & **[`self-system`](https://github.com/joshdeutc/self-system)** — **Multi-Platform OS Hardening**: Native **Android Device Owner (`DevicePolicyManager`)** anti-circumvention suite in **Kotlin** (cryptographic time-locked policies, dual watchdog services) and **Linux** kernel/daemon enforcement (`systemd` watchdogs, `mitmproxy` TLS inspection, `dm-verity` read-only rootfs).
- **[`Seven-wonder-duel-in-C`](https://github.com/joshdeutc/Seven-wonder-duel-in-C)** — Complete object-oriented implementation of **7 Wonders Duel** in **C++17 & Qt 6** (MVC architecture, custom AI agents, UML design).

---

### 🛠️ Technical Stack

| Domain | Technologies & Methods |
| :--- | :--- |
| **Mathematical Modeling & OR** | Linear/Integer & Convex Optimization (Simplex, Lagrangian, KKT), Stochastic Processes (Markov Chains, Poisson, Queues), Hypothesis Testing, Finite-Sample Risk Bounds (Hoeffding, SGR), Differential Geometry (`autograd` 2nd-order curvatures) |
| **Deep Learning & AI** | PyTorch, Hugging Face (`Transformers`, `Accelerate`, `bitsandbytes`), Torchvision, PyTorch Tabular (`GANDALF`, `FT-Transformer`, `TabTransformer`), Scikit-Learn, OpenCV, SIREN / Implicit Neural Representations |
| **LLMs & Grounded RAG** | Local LLM Inference (`MedGemma`, `Gemma-2`, `Qwen-2.5`, `Mistral`, `NLLB-200`, `EuroLLM`), Constrained JSON Generation, Deterministic Verbatim Grounding, SQLite FTS5 BM25 + Knowledge Graph RAG, Multi-Judge LLM Evaluation |
| **Languages & Systems** | **Python**, **C / C++17 (Qt 6)**, **SQL**, **Kotlin (Android SDK)**, **R**, **Scilab / MATLAB**, **Bash / Linux (`systemd`)**, **JavaScript (ES6+ / React / Manifest V3)**, **Docker**, **Git / GitHub Actions**, **LaTeX / Quarto** |
