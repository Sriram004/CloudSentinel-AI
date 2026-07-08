CloudSentinel AI
An AI-powered multi-cloud CSPM (Cloud Security Posture Management) working model — real misconfiguration scanning, IAM attack-path analysis, Terraform static analysis, remediation generation, compliance mapping, and a live AI security copilot.

Live structure:

index.html — landing/showcase page
dashboard.html — the working dashboard app (single self-contained file)
No backend, no build step, no dependencies to install — everything runs client-side in the browser (Chart.js and D3 load from CDN).

Deploy it (pick one)
Option A — GitHub Pages (recommended, free, matches your existing portfolio workflow)
Create a new repo, e.g. cloudsentinel-ai, on your GitHub (github.com/Sriram004).
Push these two files to the repo root:
git init
git add index.html dashboard.html
git commit -m "CloudSentinel AI — CSPM working model"
git branch -M main
git remote add origin https://github.com/Sriram004/cloudsentinel-ai.git
git push -u origin main
In the repo: Settings → Pages → Source → Deploy from a branch → main / root.
Your site goes live at https://sriram004.github.io/cloudsentinel-ai/ within a minute or two.
Link it from your portfolio's projects grid, same as Detectra and SecuNova.
Option B — Netlify Drop (fastest, no git required)
Go to https://app.netlify.com/drop
Drag the folder containing index.html and dashboard.html onto the page.
Netlify gives you a live URL immediately (you can rename the subdomain in site settings).
Option C — Vercel
npm i -g vercel (one-time)
From this folder: vercel --prod
remediate cloud security risks.  
🔍 Key Features  
✅ Multi-cloud asset discovery (AWS, Azure, GCP)  
✅ 300+ cloud security misconfiguration checks  
✅ IAM privilege escalation & attack path analysis  
✅ Public S3 bucket and exposed resource detection  
✅ Terraform & Infrastructure-as-Code security scanning  
✅ AI-powered risk scoring and breach impact prediction  
✅ One-click automated remediation scripts  
✅ CIS Benchmark & compliance reporting (NIST, PCI DSS, ISO 27001)  
✅ Executive security dashboards with real-time insights  
✅ AI Security Copilot for natural language cloud investigations  
🛠️ Tech Stack  
Python (FastAPI)  
React + TypeScript  
PostgreSQL  
Docker & Kubernetes  
Terraform  
Neo4j  
Open Policy Agent (OPA)  
Checkov  
Trivy  
LangChain + LLMs  
This project strengthened my understanding of:  
- Cloud Security  
- DevSecOps  
- Infrastructure as Code (IaC)  
- IAM Security  
- Risk Assessment  
- AI for Cybersecurity  
- Secure Cloud Architecture  
Building CloudSentinel AI gave me hands-on experience in solving real-world cloud security challenges and designing solutions inspired by enterprise CSPM platforms.  
I am continuously exploring innovative cybersecurity projects that bridge AI, cloud computing, and security engineering.  
I would love to hear your feedback and connect with professionals in Cloud Security, SOC, Detection Engineering, and DevSecOps.  
🔍 Misconfiguration Scanner — 22 rules evaluated against AWS/Azure/GCP resources (public S3 buckets, open security groups, disabled MFA, unencrypted storage, and more)  
📊 AI Risk Engine — deterministic scoring across exposure, IAM privilege, data sensitivity, and blast radius  
🔗 IAM Attack Path Analyzer — a real BFS graph traversal that finds actual privilege-escalation chains to admin-tier policies  
⚙️ Terraform Scanner — regex-based static analysis on IaC, with auto-generated secure fixes  
✅ Compliance Mapping — CIS AWS, NIST 800-53, PCI DSS 4.0, ISO 27001, and CSA CCM, scored live from findings  
🤖 AI Security Copilot — wired to a live Claude API call that reasons over the current scan state
