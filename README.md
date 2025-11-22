# 💻 Personal Website

Welcome to my [personal website](https://rajdyp.github.io/)!

---

## Project Overview

A lightweight static resume website built with Python and Jinja2. Simple YAML-based content management with automated GitHub Pages deployment.

---

## Setup & Installation

### Prerequisites
- Python 3.x
- pip

### Installation

1. Clone the repository:
```bash
git clone https://github.com/rajdyp/rajdyp.github.io.git
cd rajdyp.github.io
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

---

## Usage & Development

### Updating Content

Edit your resume data in `data/resume.yaml`. This single file contains all the content for your website.

### Generating the Site

Run the generator to create the static HTML:
```bash
python generator.py
```

This will render the template with your YAML data and output the result to `docs/index.html`.

### Local Development

After generating the site, you can open `docs/index.html` directly in your browser to preview changes.

Alternatively, run a local development server:
```bash
python generator.py && python -m http.server 8000 -d docs
```

Then visit `http://localhost:8000` in your browser to view your site.

### Deployment

The site is automatically deployed to GitHub Pages via GitHub Actions when you push to the `main` branch. No manual deployment needed!

---

## Project Structure

```
rajdyp.github.io/
├── data/
│   └── resume.yaml          # Resume content (edit this to update the site)
├── templates/
│   └── index.html           # Jinja2 template for HTML output
├── docs/                    # Generated static site (served by GitHub Pages)
│   └── index.html           # Generated output
├── .github/
│   └── workflows/
│       └── deploy.yml       # CI/CD: builds and deploys on push to main
├── generator.py             # Renders template with YAML data
├── requirements.txt         # Python dependencies
└── README.md
```
