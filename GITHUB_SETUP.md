# Setting Up cerno-ai/cerno-docs Repository

## Step 1: Create the Repository on GitHub

1. Go to: https://github.com/organizations/cerno-ai/repositories/new
2. Fill in the details below:

### Repository Details

**Repository name:** `cerno-docs`

**Description:**
```
🔍 High-performance RAG system for intelligent document Q&A with hybrid retrieval, GPU acceleration, and citation-backed answers. Upload docs, ask questions, get precise responses.
```

**Visibility:** ✅ Public

**Initialize repository:**
- [ ] Do NOT add README (we already have one)
- [ ] Do NOT add .gitignore (we already have one)
- [ ] Do NOT add license (we already have one)

### Repository Topics/Tags

Add these topics (click "Add topics" on the repo page after creation):

```
rag
retrieval-augmented-generation
document-processing
question-answering
fastapi
nextjs
faiss
semantic-search
nlp
ai
gemini
llm
python
typescript
docker
gpu-acceleration
embeddings
reranking
bm25
document-intelligence
hybrid-search
citation-backed
knowledge-base
```

### Repository Settings (After Creation)

#### About Section
- **Website:** (Add if you have a demo site)
- **Topics:** (Add the tags above)
- **Description:** Use the description above

#### Features to Enable
- ✅ Issues
- ✅ Discussions (recommended for community)
- ✅ Projects (optional)
- ✅ Wiki (optional)

#### Social Preview
Upload a custom social preview image (1280x640 recommended) showing:
- Cerno Docs logo/name
- Key features
- Screenshot of the UI

---

## Step 2: Push Code to New Repository

Once the repository is created on GitHub, run these commands:

```bash
# Make sure you're in the googlerag directory
cd d:\googlerag

# Switch to main branch
git checkout main

# Push main branch to cerno-ai/cerno-docs
git push cerno main

# Push contract-guardian branch (to preserve original)
git push cerno contract-guardian

# Push rag-refactor branch (development)
git push cerno rag-refactor

# Set cerno as the default remote (optional)
git remote set-url origin https://github.com/cerno-ai/cerno-docs.git

# Verify remotes
git remote -v
```

---

## Step 3: Configure Branch Settings

On GitHub → Settings → Branches:

### Default Branch
- Set `main` as the default branch

### Branch Protection Rules (Recommended)
For `main` branch:
- ✅ Require a pull request before merging
- ✅ Require approvals (at least 1)
- ✅ Require status checks to pass before merging
- ✅ Require branches to be up to date before merging
- ✅ Include administrators

---

## Step 4: Set Up GitHub Pages (Optional)

Settings → Pages:
- Source: Deploy from a branch
- Branch: `main`
- Folder: `/docs` or `/`

---

## Step 5: Add Repository Description & Topics via GitHub CLI (Alternative)

If you have GitHub CLI installed:

```bash
# Set description
gh repo edit cerno-ai/cerno-docs --description "🔍 High-performance RAG system for intelligent document Q&A with hybrid retrieval, GPU acceleration, and citation-backed answers"

# Add topics
gh repo edit cerno-ai/cerno-docs --add-topic rag,retrieval-augmented-generation,document-processing,question-answering,fastapi,nextjs,faiss,semantic-search,nlp,ai,gemini,llm,python,typescript,docker,gpu-acceleration,embeddings,reranking,bm25
```

---

## Step 6: Create Initial Release (Optional)

GitHub → Releases → Create a new release:
- **Tag:** `v1.0.0`
- **Title:** `Cerno Docs v1.0.0 - Initial Release`
- **Description:**
  ```markdown
  # 🎉 Cerno Docs v1.0.0 - Initial Public Release

  High-performance Retrieval-Augmented Generation (RAG) system for intelligent document Q&A.

  ## ✨ Features
  - Multi-format document support (PDF, DOCX, PPTX, XLSX, TXT, images)
  - Hybrid search with BM25 + FAISS vector similarity
  - GPU-accelerated embeddings and reranking
  - Citation-backed answers with source attribution
  - Modern Next.js UI with real-time chat interface
  - Docker deployment with GPU/CPU support

  ## 🚀 Quick Start
  \`\`\`bash
  docker compose up --build -d
  \`\`\`
  Visit http://localhost:3000

  ## 📚 Documentation
  - [README](https://github.com/cerno-ai/cerno-docs#readme)
  - [Installation Guide](./INSTALLATION.md)
  - [Technical Deep Dive](./Explanation.md)
  - [Contributing](./CONTRIBUTING.md)

  **Full changelog:** Initial release
  ```

---

## Step 7: Announcement Template

### Social Media Post Template

```
🚀 Excited to announce Cerno Docs - an open-source RAG system for intelligent document Q&A!

✨ Features:
- Multi-format support (PDF, DOCX, images, etc.)
- Hybrid retrieval (BM25 + FAISS)
- GPU acceleration
- Citation-backed answers
- Modern React UI

🔗 Check it out: https://github.com/cerno-ai/cerno-docs

#OpenSource #AI #RAG #NLP #Python #FastAPI #MachineLearning
```

### Reddit Post Template (r/MachineLearning, r/LanguageTechnology)

```
Title: [P] Cerno Docs - Open-source RAG system for intelligent document Q&A

Body:
Hi everyone! I'm excited to share Cerno Docs, an open-source RAG system I've been working on.

**What it does:**
Upload documents (PDF, DOCX, images, etc.) and ask questions to get precise, citation-backed answers using hybrid retrieval and state-of-the-art LLMs.

**Key features:**
- Hybrid search combining BM25 (keyword) + FAISS (semantic)
- GPU-accelerated embeddings and reranking
- Smart document routing (small docs → direct LLM, large docs → full RAG)
- Multi-language support with automatic detection
- Modern Next.js UI with real-time streaming

**Tech stack:**
FastAPI, Next.js, Google Gemini, SentenceTransformers, FAISS, Docker

**GitHub:** https://github.com/cerno-ai/cerno-docs

Would love to hear your feedback and suggestions!
```

---

## Checklist

- [ ] Create `cerno-docs` repository on GitHub under `cerno-ai` organization
- [ ] Add repository description
- [ ] Add repository topics/tags
- [ ] Push `main` branch
- [ ] Push `contract-guardian` branch
- [ ] Push `rag-refactor` branch
- [ ] Set `main` as default branch
- [ ] Configure branch protection rules
- [ ] Enable GitHub Discussions
- [ ] Create v1.0.0 release
- [ ] Update GitHub About section
- [ ] Announce on social media
- [ ] Submit to relevant communities

---

**Next Command to Run (after creating repo on GitHub):**
```bash
git push cerno main
git push cerno contract-guardian
git push cerno rag-refactor
```
