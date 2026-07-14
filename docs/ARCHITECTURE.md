# Infosys RAG Compliance Checker V1 Architecture

## Purpose

AI-assisted regulatory compliance checker assignment for contract review.

## Stack

Python, FastAPI, Streamlit, ChromaDB, PyPDF2

## System Context

```mermaid
flowchart LR
    User["Commercial contract PDF"] --> App["FastAPI document analysis and regulatory knowledge base"]
    App --> Data["Regulatory rules, parsed contract text, vector store"]
    App --> Output["Compliance report and risk observations"]
    Data --> Output
```
## Runtime Workflow

```mermaid
flowchart TD
    S1["Upload document"] --> S2["Extract contract text"]
    S2["Extract contract text"] --> S3["Search regulatory knowledge base"]
    S3["Search regulatory knowledge base"] --> S4["Evaluate clauses"]
    S4["Evaluate clauses"] --> S5["Return compliance report"]
```
## Production Readiness Notes

- Keep secrets in environment variables and commit only .env.example templates.
- Keep generated files, dependency folders, caches, and local databases out of version control.
- Run the GitHub Actions workflow before presenting or deploying changes.
- Update this document when the source layout, dependencies, or deployment model changes.

## Review Checklist

- Architecture diagram matches current source files.
- Workflow diagram matches the main user or data path.
- README links to this architecture document.
- CI workflow validates the project on every push and pull request.

