# DocuGenAI: Automated Code Documentation Generator

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/iKrish/DocuGenAI/main?labpath=docugenai-demo-a4.ipynb)

**LLM-Powered Repository Analysis and Documentation** using Google Gemini 2.5 Flash

This project demonstrates an AI-powered system that automatically generates comprehensive documentation for GitHub repositories. It analyzes repository structure, understands code functionality, and produces professional README files, architecture diagrams, and interactive Q&A.

---

## Quick Start Options

### Option 1: Run on MyBinder (Recommended for Demo)

**Click the badge above** or visit: [Launch on MyBinder](https://mybinder.org/v2/gh/iKrish/DocuGenAI/main?labpath=docugenai-demo-a4.ipynb)

**First-time setup on MyBinder:**
1. Wait 2-3 minutes for environment to build
2. When prompted, enter your **free** Gemini API key from [Google AI Studio](https://aistudio.google.com/app/apikey)
3. Run all cells to see examples on 3 different repositories

**Note:** MyBinder sessions are temporary. Your API key is only stored for the current session and not saved.

### Option 2: Run Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/iKrish/DocuGenAI.git
   cd DocuGenAI
   ```

2. **Get a free Gemini API key:**
   - Visit [Google AI Studio](https://aistudio.google.com/app/apikey)
   - Create or select a project
   - Generate an API key

3. **Set up environment:**
   ```bash
   # Create .env file
   echo "GEMINI_API_KEY=your-api-key-here" > .env
   
   # Install dependencies
   pip install -r requirements.txt
   ```

4. **Run the notebook:**
   ```bash
   jupyter notebook docugenai-demo-a4.ipynb
   ```

---

## Repository Structure

```
DocuGenAI/
├── docugenai-demo-a4.ipynb    # Main demo notebook (all-in-one)
├── requirements.txt            # Python dependencies
├── apt.txt                     # System dependencies (git for MyBinder)
├── .env.example               # API key template
├── .gitignore                 # Git ignore configuration
├── Examples/                   # Generated documentation outputs
│   ├── Example1.md            # Fraud Detection project docs
│   ├── Example2.md            # Recommender System project docs
│   └── Example3.md            # Azure Demo project docs
└── repos/                      # Cloned repositories (auto-created)
```

---

## What This Demonstrates

**AI Task Type:** Natural Language Understanding & Generation

1. **NLU as Interface** - Translates technical code into human-readable documentation
2. **Multiple NL Tasks** - Comprehension, extraction, summarization, structured generation
3. **Knowledge Retrieval** - Leverages LLM's training on programming patterns
4. **Conversation Memory** - Maintains context across multiple prompts

**Key Features:**
- Intelligent repository analysis (20+ programming languages)
- Multi-stage prompt engineering with conversation memory
- Automatic README generation
- Mermaid diagram creation for architecture visualization
- Interactive Q&A about codebase

**Example Repositories Analyzed:**
1. **SupervisedLearning** - Fraud detection ML project (scikit-learn, XGBoost)
2. **RecommenderSystem** - Movie recommendations (LightFM, collaborative filtering)
3. **AzureDemo** - Cloud deployment project (ASP.NET, Azure services)

---

## Technical Details

**LLM:** Google Gemini 2.5 Flash
- **Cost:** Free tier (15 req/min, 1500 req/day)
- **Context:** 1M tokens (can analyze large repositories)
- **Why:** Best free option for code understanding

**Configuration:**
- Temperature: 0.3 (focused, deterministic)
- Max tokens: 8192 per response
- Max files analyzed: 20 files per repo
- Max file size: 400KB per file

---

## Expected Outputs

For each repository, the system generates:

1. **Project Analysis** - Type, purpose, technologies, architecture
2. **Professional README** - Overview, features, installation, usage
3. **Mind Map** - Mermaid flowchart showing data flow and components
4. **Q&A Responses** - Answers to technical questions using conversation context

All outputs are saved to `Examples/` folder as markdown files.

---

## Files

- `docugenai-demo-a4.ipynb` - Main demo notebook with all code and examples
- `requirements.txt` - Python package dependencies
- `apt.txt` - System packages for MyBinder (git)
- `.env.example` - API key configuration template



