# Portfolio refresh context

Updated: 2026-10-16

## Purpose and working approach

Refresh the portfolio copy to be approachable, concise, and easy to scan while keeping the existing static HTML/CSS layout. Keep the existing navigation and destination pages for the resume, certifications, and research papers. Do not invent project URLs; the current GitHub profile link is the only project destination published on the homepage.

Work in small phases so another session can resume without repeating research:

1. **Source review — complete.** Read the resume documents and map current portfolio pages.
2. **Portfolio refresh — complete.** Homepage is a lightweight GenAI/LLM-focused page with a friendly tone, resume-sourced impact metrics, and the user's latest portrait. Research, Certifications, and Rewards & Recognition pages share the homepage theme. Date-bearing lists and timelines are newest-first. The MapMyVisitors pageview counter is retained as a compact, fixed-width footer icon.
3. **Verification — complete.** Homepage and content pages render at desktop/mobile widths; the viewport has no horizontal overflow. Local links resolve, editor diagnostics are clean, and `git diff --check` passes. The homepage uses a standalone stylesheet and a 66 KB web-sized portrait derived from `images/Best.JPG`; it does not load the legacy stylesheet or JS libraries. No build/test command is configured. The MapMyVisitors third-party request may be blocked in local file previews.

## Source hierarchy and factual notes

- `Resume.pdf` is the current resume and should be preferred for current role and experience.
- `CV.pdf` and `A Resume.docx` provide historical detail but contain older or conflicting dates/counts.
- The public portfolio should not expose the residential address present in source documents.
- The user confirmed that the October 2026 Claude certification and peer-review recognitions listed in `Resume.pdf` are completed and may be represented as completed.
- Treat numerical achievements as resume-reported claims, not independently verified claims.

### Current professional profile

- **Name:** Varun Totakura
- **Email:** varun.totakura@gmail.com
- **Current role:** AI Engineer / Lead Assistant Manager, EXL Service Inc.; remote from New York; October 2024–present.
- **Summary:** AI/ML engineer with 5+ years of experience spanning healthcare analytics, LLM/RAG systems, deep learning, NLP, and ServiceNow automation.
- **Education:** MS in Computer Science, Florida State University (August 2024; GPA 3.54/4.0); BTech in Computer Science & Engineering, Guru Nanak Institutions / JNTU Hyderabad (2020; GPA 8.91/10).
- **Previous roles:** Graduate Research Assistant / AI/ML Engineer at Florida State University (August 2022–August 2024); Systems Engineer / AI Software Developer at Tata Consultancy Services (July 2020–September 2022 per current resume).
- **Selected research:** Alzheimer’s detection, deep-learning model correctness, active learning with imperfect oracles, and BERT/GAN-based bug localization.
- **Selected industry work:** Multi-agent analytics and RAG; healthcare campaign analytics and ML pipelines; ServiceNow integrations, chatbots, and automations.
- **Current-role impact:** Healthcare analytics supporting campaigns reaching 5M members and $1.5M annual revenue; LLM Recall@5 improved from 68% to 81%, hallucinations reduced from 12% to 6%, and query costs reduced 30%; a 7M+ record pipeline runs in under 30 seconds rather than 20 minutes (40× faster); leads five data scientists.
- **Other resume-reported metrics:** A 15M-record migration. Use only with appropriate project context from the resume.
- **Skills:** Python, SQL, JavaScript; PyTorch, TensorFlow, scikit-learn, Keras, LangChain/LangGraph, Hugging Face; Dask, PySpark, FastAPI, Streamlit; AWS, Azure, Google Cloud/Vertex AI; Docker, Jenkins, Airflow, Kafka; BigQuery, Snowflake, PostgreSQL, MySQL, MongoDB, Pinecone, Chroma; Power BI, Tableau, Matplotlib, Seaborn, Plotly.
- **Recognition:** TCS Star of the Month (three times), On the Spot awards, Learning Achievement Award, and second-place academic rank at Guru Nanak Institutions. Avoid stating the On the Spot count because the sources disagree.
- **Recognition PDFs:** `Recognition/IEEE_SMC_2026.pdf` confirms the IEEE SMC 2026 Certificate of Appreciation for reviewer service, held October 4–7, 2026; `Recognition/Certificate_MLWA_Recognised.pdf` confirms 10 reviews for *Machine Learning with Applications* between July and October 2026. These and other dated recognitions are sorted newest-to-oldest on `recognitions.html`.
- **Recent credentials/recognitions:** Resume lists Claude Certified Architect (Anthropic, October 2026), Deep Learning Specialization, and peer-review recognitions in October 2026. The user confirmed these October 2026 items are completed. The Claude badge URL provided by the user is `https://www.credly.com/badges/4d2176c3-645f-4d5f-b9e3-1d7c71170dfb`. The resume names five papers reviewed for IEEE SMC 2026 and ten for Elsevier's *Machine Learning with Applications*.
- **Certificate chronology:** User asked for newest-to-oldest ordering across the site and confirmed that Coursera courses without a source date should be assigned to 2020. Known dates retained: Machine Learning: Regression (October 9, 2020); three courses (Applied Machine Learning in Python, End-to-End ML with TensorFlow on GCP, Neural Networks and Deep Learning) from September 2020; Customer Analytics (February 2018). Claude Certified Architect is October 2026 and the Deep Learning Specialization is 2020. The Google Cloud Qwiklabs link is a profile, not a dated credential.
- **Publication status:** The current resume lists recent 2025/2026 works and an LLIE-CvT paper marked “Expected 2026.” Do not describe the expected paper as published. *MetaErr: Towards Predicting Error Patterns in Deep Neural Networks* (ICSM 2025, `https://ieeexplore.ieee.org/abstract/document/11541569`) and *Active Learning with Imperfect Oracles using Text Data* (IJCNN 2026, `https://arxiv.org/abs/2604.23290`) are listed on `researchpapers.html`.

### Known source conflicts

- TCS end date: September 2022 in `Resume.pdf`, July 2022 in `CV.pdf` and `A Resume.docx`; prefer September 2022.
- On the Spot award count: five in `Resume.pdf` and `A Resume.docx`, eight in `CV.pdf`; omit a count.
- Publication lists/statuses and paper counts differ between the documents; use the current resume for new references and preserve the existing paper page without claiming the lists are exhaustive.

## Existing site and links

- `index.html` is a lightweight, GenAI/LLM-focused homepage using the standalone `assets/css/home.css` stylesheet, a 1000×667 optimized portrait derived from the user's `images/Best.JPG`, and an asynchronous MapMyVisitors pageview-counter embed. The counter is configured at 56px wide; the date and branding row are hidden while the pageview count remains visible. It does not load the legacy stylesheet or JS libraries. The current-role work section covers multi-agent analytics/RAG, LLM quality and evaluation, healthcare campaign analytics and A/B testing, and pipeline performance in a balanced four-card grid. Impact metrics are resume-sourced.
- `recognitions.html` is the separate Rewards & Recognition page for professional awards, peer-review service, and academic achievement, sorted newest-to-oldest. Its IEEE and Machine Learning with Applications certificate links point to PDFs in `Recognition/`.
- Main navigation already links to `index.html`, `certifications.html`, `researchpapers.html`, and `Resume.pdf`. Keep those destinations.
- `certifications.html` contains ten linked Coursera certificates plus Deep Learning Specialization and Google Cloud QwikLab profile links. Preserve every existing URL.
- `researchpapers.html` contains 15 papers grouped newest-to-oldest by publication year, plus Scopus, ORCID, ResearchGate, and IEEE Author profile links. It shares the homepage visual theme. The user supplied IEEE Author profile URL: `https://authorprofile.ieee.org/author/745001893279356`. Preserve every existing URL and the local paper PDF path.
- `certifications.html` shares the homepage theme and groups credentials by year (2026, 2020, 2018), features the Claude credential, presents 2020 courses in a responsive card grid, and keeps the Qwiklabs profile separate as undated.
- Social profiles and email are in the homepage footer; preserve them.
- There are no provided links for each project, so do not imply project cards link to distinct repositories. Keep the existing GitHub profile URL.

## Homepage content direction

- Keep the homepage GenAI/LLM-first, human in tone, and grounded in the resume.
- Keep the dedicated research, certification, and rewards/recognition pages easy to find.
- Keep the homepage image-light and avoid blocking scripts; preserve direct access to the resume, visitor map, and user-provided certificate PDFs.
