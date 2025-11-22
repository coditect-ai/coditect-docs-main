# coditect-docs-main - Claude Code Configuration

## Project Overview

**coditect-docs-main** is the primary documentation site for the CODITECT platform, built with Docusaurus to provide comprehensive developer documentation, API references, tutorials, and guides.

### Purpose

**Problems Solved:**
- Centralized documentation hub for all CODITECT platform components
- Searchable, navigable technical documentation for developers
- Version-controlled documentation that stays in sync with platform releases
- Professional presentation of CODITECT capabilities and integrations

**Target Users:**
- Developers learning to use CODITECT
- Operators deploying and configuring CODITECT
- Technical writers maintaining documentation
- Product teams referencing specifications

**Ecosystem Role:**
- **Primary Documentation Hub** - Single source of truth for CODITECT documentation
- Aggregates content from all CODITECT submodules
- Provides unified search and navigation across all documentation
- Supports versioned documentation aligned with platform releases

### Current Status

**Development Stage:** Stub (Early Development)

This repository is currently in early development with placeholder content. Core documentation infrastructure is being established.

---

## Technology Stack

### Core Framework
- **Docusaurus 3.x** - React-based static site generator optimized for documentation
- **React 18** - UI component framework
- **MDX** - Markdown with JSX support for interactive documentation
- **TypeScript** - Type-safe development

### Search & Navigation
- **Algolia DocSearch** - Full-text search across documentation
- **Custom Sidebar** - Hierarchical navigation structure
- **Versioned Docs** - Documentation versioning per release

### Build & Deployment
- **Node.js 18+** - Runtime environment
- **Yarn/npm** - Package management
- **GitHub Actions** - CI/CD pipeline
- **GitHub Pages / Vercel** - Static site hosting

### Content Management
- **Git** - Version control for documentation
- **Markdown/MDX** - Documentation authoring format
- **Mermaid** - Diagram generation
- **Prism** - Code syntax highlighting

---

## Key Features

- **Unified Documentation Portal** - All CODITECT documentation in one searchable location
- **Interactive Code Examples** - Live code blocks with copy-to-clipboard functionality
- **Versioned Documentation** - Documentation versions aligned with platform releases
- **API Reference Generation** - Automated API documentation from OpenAPI specs
- **Multi-language Support** - Internationalization infrastructure for global reach

---

## Quick Start

### Prerequisites

- Node.js 18+ installed
- Yarn or npm package manager
- Git for version control

### Installation

```bash
# Clone the repository
git clone https://github.com/coditect-ai/coditect-docs-main.git
cd coditect-docs-main

# Install dependencies
yarn install
# or
npm install
```

### Development

```bash
# Start development server
yarn start
# or
npm run start

# Build for production
yarn build
# or
npm run build

# Serve production build locally
yarn serve
# or
npm run serve
```

### Local Development Server

The development server runs at `http://localhost:3000` with hot reload enabled. Changes to documentation files are reflected immediately.

---

## Directory Structure

```
coditect-docs-main/
├── .coditect -> ../../../.coditect           # Distributed intelligence symlink
├── .claude -> .coditect                       # Claude Code compatibility
├── docs/                                       # Documentation content
│   ├── intro.md                               # Getting started
│   ├── getting-started/                       # Quick start guides
│   │   ├── installation.md
│   │   ├── configuration.md
│   │   └── first-project.md
│   ├── guides/                                # In-depth guides
│   │   ├── agents/
│   │   ├── commands/
│   │   └── skills/
│   ├── api/                                   # API reference
│   │   ├── cloud-backend/
│   │   └── cli/
│   ├── architecture/                          # Architecture documentation
│   │   ├── distributed-intelligence.md
│   │   ├── submodule-system.md
│   │   └── memory-context.md
│   └── reference/                             # Reference materials
│       ├── glossary.md
│       ├── faq.md
│       └── troubleshooting.md
├── blog/                                      # Release notes and announcements
├── src/                                       # Custom React components
│   ├── components/
│   ├── pages/
│   └── css/
├── static/                                    # Static assets
│   ├── img/
│   └── files/
├── docusaurus.config.js                       # Docusaurus configuration
├── sidebars.js                                # Sidebar navigation structure
├── package.json                               # Dependencies
├── CLAUDE.md                                  # This file
└── README.md                                  # User-facing documentation
```

---

## Distributed Intelligence Architecture

### Symlink Structure

This repository uses the CODITECT distributed intelligence pattern:

```bash
.coditect -> ../../../.coditect    # Links to coditect-core
.claude -> .coditect               # Claude Code compatibility
```

### Benefits

- **Consistent AI Capabilities** - Same 50 agents, 72 commands, 24 skills as all CODITECT projects
- **Unified Context** - Shared understanding across documentation and codebase
- **Automated Documentation** - AI agents can generate and validate documentation
- **Quality Assurance** - Documentation specialist agents ensure consistency

### Available for Documentation

When working in this repository, you have access to:
- **codi-documentation-writer** - Comprehensive technical documentation specialist
- **codi-technical-reviewer** - Documentation quality and accuracy validation
- **codi-api-documentation** - API reference generation and validation
- All 72 slash commands for workflow automation

---

## Development Guidelines

### Documentation Authoring

**Content Standards:**
- Write for developers first, then operators
- Include working code examples for all features
- Use consistent terminology (see SUBMODULE-ANALYSIS-FRAMEWORK.md)
- Link to related documentation sections

**File Organization:**
- One concept per documentation file
- Group related docs in subdirectories
- Use descriptive file names (e.g., `distributed-intelligence.md`)
- Maintain sidebar organization in `sidebars.js`

**Formatting:**
- Use MDX for interactive components
- Include frontmatter with title, description, keywords
- Add navigation links (prev/next)
- Use Mermaid for diagrams

### Code Examples

```javascript
// Good: Working, complete example
const coditect = require('@coditect/sdk');

const agent = coditect.createAgent({
  name: 'custom-agent',
  capabilities: ['code-review', 'documentation']
});

agent.execute('Review this code for best practices');
```

### Versioning

- Documentation versions track platform releases (v1.0, v2.0, etc.)
- Breaking changes require new version
- Each version maintains its own docs snapshot

---

## Testing Approach

### Content Validation

```bash
# Check for broken links
yarn check-links

# Validate MDX syntax
yarn check-mdx

# Test build
yarn build
```

### Documentation Quality

- **Spell check** - Automated via CI
- **Link validation** - Broken link detection
- **Code example testing** - Validate code blocks execute correctly
- **Accessibility** - WCAG compliance checking

### CI/CD Pipeline

```yaml
# .github/workflows/docs.yml
- Build documentation
- Validate links and syntax
- Run code examples
- Deploy to staging
- Lighthouse performance testing
```

---

## AI Agent Guidelines

### When Working in This Repository

**Primary Tasks:**
1. **Content Creation** - Write and update documentation
2. **Code Examples** - Create working, tested examples
3. **Navigation** - Organize content hierarchy
4. **Quality Review** - Validate accuracy and consistency

**Best Practices:**

1. **Read Related Docs First**
   - Check existing content in relevant sections
   - Understand documentation style and conventions
   - Review sidebar organization

2. **Use Documentation Agents**
   - `codi-documentation-writer` for content creation
   - `codi-technical-reviewer` for quality validation
   - Follow documentation quality standards

3. **Maintain Consistency**
   - Use terminology from SUBMODULE-ANALYSIS-FRAMEWORK.md
   - Follow established formatting patterns
   - Cross-link related documentation

4. **Test All Examples**
   - Verify code examples execute correctly
   - Include expected output
   - Test across supported environments

5. **Update Navigation**
   - Add new pages to sidebars.js
   - Maintain logical groupings
   - Update cross-references

---

## Dependencies and Dependents

### Dependencies (Upstream)

| Repository | Relationship |
|------------|--------------|
| coditect-core | AI capabilities via symlink |
| All CODITECT repos | Content source for documentation |
| Algolia | Search infrastructure |

### Dependents (Downstream)

| Repository | Relationship |
|------------|--------------|
| coditect-cloud-ide | Embedded help/documentation links |
| coditect-cli | CLI documentation and help |
| coditect-cloud-frontend | Help center integration |

---

## Common Tasks

### Add New Documentation Page

```bash
# Create new doc file
touch docs/guides/new-feature.md

# Add frontmatter
cat > docs/guides/new-feature.md << 'EOF'
---
title: New Feature Guide
description: How to use the new feature
sidebar_position: 5
---

# New Feature Guide

Content here...
EOF

# Update sidebars.js to include new page
```

### Generate API Documentation

```bash
# From OpenAPI spec
yarn generate-api-docs --spec ../coditect-cloud-backend/openapi.yaml

# Update API reference section
```

### Deploy Documentation

```bash
# Deploy to GitHub Pages
yarn deploy

# Deploy to Vercel (preview)
vercel --prod
```

### Update Search Index

```bash
# Trigger Algolia crawl
yarn algolia-index
```

---

## Content Organization

### Documentation Hierarchy

1. **Getting Started** - Installation, configuration, first steps
2. **Guides** - Task-oriented how-to documentation
3. **API Reference** - Complete API documentation
4. **Architecture** - System design and concepts
5. **Reference** - Glossary, FAQ, troubleshooting

### Cross-Repository Content

This documentation aggregates content from:
- `coditect-core-architecture` - Architecture decisions and patterns
- `coditect-cloud-backend` - API reference and integration
- `coditect-cli` - CLI command reference
- `coditect-docs-training` - Training and certification materials

---

## Configuration Files

### docusaurus.config.js

Key configuration:
- Site metadata (title, tagline, URL)
- Theme customization
- Plugin configuration (Algolia, analytics)
- Navigation (navbar, footer)

### sidebars.js

Documentation navigation structure:
- Hierarchical categories
- Auto-generated sections
- Custom ordering

---

## Performance Optimization

### Build Optimization

- Static generation for fast loading
- Code splitting for large documentation sets
- Image optimization
- Lazy loading for non-critical content

### Search Optimization

- Algolia facets for filtered search
- Keyboard navigation
- Search suggestions
- Result highlighting

---

## Future Enhancements

### Short-term (Next Sprint)
- [ ] Complete initial documentation structure
- [ ] Configure Algolia DocSearch
- [ ] Set up CI/CD pipeline
- [ ] Create Getting Started guide

### Medium-term (Next Quarter)
- [ ] API reference auto-generation
- [ ] Version documentation for v1.0 release
- [ ] Add interactive tutorials
- [ ] Implement feedback collection

### Long-term (Next Year)
- [ ] Multi-language support
- [ ] Video tutorials integration
- [ ] Community contributions workflow
- [ ] Documentation analytics dashboard

---

## License

**Proprietary - AZ1.AI INC**

This repository and all contents are proprietary to AZ1.AI INC. Unauthorized copying, distribution, or modification is strictly prohibited.

Copyright (c) 2025 AZ1.AI INC. All rights reserved.

---

**Last Updated:** November 2025
**Repository:** https://github.com/coditect-ai/coditect-docs-main
**Owner:** AZ1.AI INC
**Lead:** Hal Casteel, Founder/CEO/CTO
