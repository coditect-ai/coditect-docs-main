# coditect-docs-main

**Documentation Repository - AZ1.AI CODITECT Ecosystem**

---

## Overview

The primary documentation hub for the CODITECT platform, built with Docusaurus to provide comprehensive developer documentation, API references, tutorials, and user guides. This repository serves as the authoritative source for all CODITECT platform documentation, ensuring developers and operators have access to accurate, searchable, and well-organized technical content.

**Status:** Stub (Planning Phase)
**Category:** docs
**Priority:** P0

---

## Purpose

### What Problem This Solves

- **Centralized Documentation**: Single source of truth for all CODITECT platform documentation
- **Developer Onboarding**: Comprehensive guides to help new developers get started quickly
- **API Reference**: Complete API documentation with interactive examples
- **Searchable Content**: Algolia-powered search for instant access to documentation

### Who Uses It

- **Developers**: Learning to build with CODITECT
- **Operators**: Managing CODITECT deployments
- **Technical Writers**: Contributing to documentation
- **End Users**: Finding answers to common questions

### Ecosystem Role

This repository is the **primary public-facing documentation** for the CODITECT platform. It aggregates content from multiple sources across the ecosystem and presents it in a unified, accessible format. All other CODITECT repositories reference this documentation site for detailed technical information.

---

## Key Features

- **Docusaurus 3.x** - Modern documentation framework with MDX support
- **Algolia Search** - Fast, full-text search across all documentation
- **Interactive Examples** - Live code examples with syntax highlighting
- **Version Management** - Documentation versioning aligned with platform releases
- **Multi-language Support** - Internationalization-ready architecture
- **Dark Mode** - Automatic theme switching based on system preferences
- **Mobile Responsive** - Fully responsive design for all devices
- **API Documentation** - OpenAPI/Swagger integration for REST APIs

---

## Technology Stack

- **Framework:** Docusaurus 3.x
- **Language:** TypeScript, MDX
- **UI Framework:** React 18
- **Search:** Algolia DocSearch
- **Styling:** CSS Modules, TailwindCSS
- **Build Tool:** Webpack
- **Deployment:** Static site generation (SSG)
- **Hosting:** Vercel / Netlify / GCP Cloud Storage

---

## Quick Start

### Prerequisites

- Node.js >= 18.0.0
- npm >= 9.0.0 or yarn >= 1.22.0
- Git

### Installation

```bash
# Clone repository
git clone https://github.com/coditect-ai/coditect-docs-main.git
cd coditect-docs-main

# Install dependencies
npm install

# Start development server
npm run start
```

### Development

```bash
# Run development server (hot reload)
npm run start

# Build production site
npm run build

# Serve production build locally
npm run serve

# Clear cache and build
npm run clear && npm run build

# Type checking
npm run typecheck
```

---

## Directory Structure

```
coditect-docs-main/
├── .coditect -> ../../../.coditect    # Distributed intelligence symlink
├── .claude -> .coditect               # Claude Code compatibility
├── docs/                              # Documentation content (MDX)
│   ├── getting-started/               # Quick start guides
│   ├── concepts/                      # Core concepts
│   ├── guides/                        # Step-by-step guides
│   ├── api/                           # API reference
│   ├── cli/                           # CLI documentation
│   └── troubleshooting/               # Common issues
├── blog/                              # Release notes, announcements
├── src/                               # Custom React components
│   ├── components/                    # Reusable UI components
│   ├── pages/                         # Custom pages
│   └── css/                           # Global styles
├── static/                            # Static assets (images, files)
├── docusaurus.config.ts               # Docusaurus configuration
├── sidebars.ts                        # Sidebar navigation
├── package.json                       # Dependencies
├── PROJECT-PLAN.md                    # Detailed project plan
├── TASKLIST.md                        # Task tracking
└── README.md                          # This file
```

---

## Distributed Intelligence

This repository is part of the CODITECT distributed intelligence architecture:

```
.coditect -> ../../../.coditect  # Links to master brain
.claude -> .coditect             # Claude Code compatibility
```

**Benefits:**
- Access to 50 specialized AI agents
- 72 slash commands available
- 24 reusable skills
- Consistent development patterns across all projects

**Learn more:** [WHAT-IS-CODITECT.md](https://github.com/coditect-ai/coditect-core/blob/main/WHAT-IS-CODITECT.md)

---

## Content Structure

### Documentation Sections

1. **Getting Started**
   - Installation guide
   - First project tutorial
   - IDE setup
   - System requirements

2. **Core Concepts**
   - Distributed intelligence architecture
   - Agent framework
   - Skills and commands
   - Memory context system

3. **Guides**
   - Building with CODITECT
   - Custom agent development
   - Workflow automation
   - Best practices

4. **API Reference**
   - REST API endpoints
   - Authentication
   - Request/response schemas
   - Error handling

5. **CLI Documentation**
   - Installation
   - Command reference
   - Configuration

6. **Troubleshooting**
   - Common issues
   - FAQ
   - Support resources

---

## Integration with CODITECT Platform

### Dependencies

- [coditect-core](../core/coditect-core) - Core framework and agents
- [coditect-core-architecture](../core/coditect-core-architecture) - ADRs and design docs

### Dependents

- All CODITECT repositories reference this documentation
- [coditect-cloud-frontend](../cloud/coditect-cloud-frontend) - Links to docs
- [coditect-cloud-backend](../cloud/coditect-cloud-backend) - API documentation source

### Content Sources

This documentation aggregates content from:
- API specifications from backend repositories
- Agent documentation from coditect-core
- Architecture decisions from coditect-core-architecture
- Tutorial content from coditect-docs-training

---

## Development Guidelines

### Writing Documentation

- Use MDX format for enhanced components
- Follow the style guide in `/docs/contributing/style-guide.md`
- Include code examples with proper syntax highlighting
- Add frontmatter metadata to all documents
- Use admonitions for tips, warnings, and notes

### Code Examples

```mdx
---
title: Example Document
sidebar_position: 1
---

# Document Title

:::tip Quick Tip
Use the CODITECT router to find commands automatically.
:::

```python
from coditect import Agent

agent = Agent("my-agent")
result = agent.execute("task description")
```
```

### Commit Messages

Follow conventional commit format:
```
type(scope): description

feat(docs): add authentication guide
fix(api): correct endpoint documentation
docs(getting-started): improve installation steps
```

---

## Testing

```bash
# Build and check for broken links
npm run build

# Check for broken links only
npm run docusaurus check-broken-links

# Validate documentation structure
npm run validate
```

---

## Deployment

### Production Build

```bash
# Generate static site
npm run build

# Preview production build
npm run serve
```

### Deployment Options

**Vercel (Recommended):**
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel --prod
```

**Netlify:**
```bash
# Build command: npm run build
# Publish directory: build
```

**GCP Cloud Storage:**
```bash
gsutil -m rsync -r build gs://docs.coditect.ai
```

---

## Project Details

- **Type:** Documentation
- **Priority:** P0
- **Timeline:** 6 weeks
- **Budget:** $55K
- **Team Size:** 1 engineer

### Milestones

1. **Week 1-2**: Site setup and navigation structure
2. **Week 3-4**: Core documentation content
3. **Week 5**: Search integration and styling
4. **Week 6**: Testing, SEO, and deployment

---

## Related Resources

- **Master Repository:** [coditect-rollout-master](https://github.com/coditect-ai/coditect-rollout-master)
- **Core Framework:** [coditect-core](https://github.com/coditect-ai/coditect-core)
- **Architecture:** [coditect-core-architecture](https://github.com/coditect-ai/coditect-core-architecture)
- **Live Site:** [docs.coditect.ai](https://docs.coditect.ai) (when available)

---

## Contributing

### Adding Documentation

1. Create MDX file in appropriate directory under `/docs`
2. Add frontmatter with title and sidebar position
3. Update `sidebars.ts` if creating new section
4. Submit pull request with preview link

### Reporting Issues

- Use GitHub Issues for documentation errors
- Include page URL and description of issue
- Suggest corrections when possible

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed contribution guidelines.

---

## License

Copyright (C) 2025 AZ1.AI INC. All Rights Reserved.

**PROPRIETARY AND CONFIDENTIAL** - This repository contains AZ1.AI INC. trade secrets and confidential information. Unauthorized copying, transfer, or use is strictly prohibited.

---

*Built with Excellence by AZ1.AI CODITECT*
*Systematic Development. Continuous Context. Exceptional Results.*
