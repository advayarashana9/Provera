# Provera

**Provera** is an AI-powered financial verification platform designed to automatically audit and reconcile financial statements against official SEC filings (10-K, 10-Q, 8-K, etc.). By extracting, mapping, and cross-referencing line items against regulatory disclosures, Provera detects discrepancies, anomalies, and potential reporting risks in real time.

---

## Key Features

* **SEC Data Integration:** Direct pipeline with the SEC EDGAR system to parse and pull structured XBRL and unstructured PDF/HTML filings.
* **Automated Line-Item Reconciliation:** Uses NLP and custom LLM parsers to cross-reference private or audited financial statements with official public disclosures.
* **Anomaly & Discrepancy Detection:** Flags variance, missing disclosures, inconsistent accounting methodologies, or recalculation errors.
* **Audit Trail & Sourcing:** Provides granular visual back-references linking extracted figures back to exact coordinates in source filings.
* **REST API & Web Dashboard:** Easily query verification results programmatically or explore interactive reports via the dashboard.

---

## Tech Stack

* **Core Engine:** Python (FastAPI / PyTorch / Transformers)
* **Document Processing:** Unstructured, Tesseract OCR, PDFPlumber, Sec-Edgar-Downloader
* **Vector & Relational Storage:** PostgreSQL (pgvector) / Qdrant
* **Frontend:** React / Next.js / Tailwind CSS

---

## Getting Started

### Prerequisites

* Python 3.10+
* Node.js 18+
* PostgreSQL instance with `pgvector` enabled
* SEC EDGAR API User-Agent header (required by SEC guidelines)

### Environment Setup

Clone the repository and set up environment variables:

```bash
git clone [https://github.com/your-org/provera.git](https://github.com/your-org/provera.git)
cd provera
cp .env.example .env
