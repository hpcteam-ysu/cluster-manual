# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a VitePress-based documentation site for the Yanshan University GPU Cluster user manual (燕山大学GPU集群用户手册). The project generates a static website providing comprehensive guidance for HPC cluster usage.

## Development Commands

Essential commands for development:

```bash
# Development server
npm run dev

# Build static site
npm run build

# Preview built site locally
npm run preview
```

## Project Structure

- `vitepress-docs/` - Main documentation source directory
  - `.vitepress/config.mts` - VitePress configuration file
  - `index.md` - Homepage with hero section and feature highlights
  - `manual/` - Main documentation content
    - `access/` - Cluster access instructions
    - `hardware/` - Hardware specifications
    - `scow/` - SCOW system usage
    - `slurm/` - SLURM job scheduler documentation
    - `software/` - Software overview
    - `terms.md` - Service terms
    - `qa.md` - Q&A section
  - `public/images/` - Static images for documentation
- `images/` - Legacy image directory (duplicated in public/)

## Content Architecture

The documentation follows a structured approach:
1. Service terms and hardware overview for new users
2. Access methods (campus network and external)
3. Job scheduling with SLURM system
4. Visual management through SCOW web interface
5. Q&A for troubleshooting

The site is fully in Chinese and targets academic HPC users. Navigation is configured with a comprehensive sidebar for the manual section.

## Key Dependencies

- VitePress 1.3.4+ for static site generation
- Mermaid support configured but not yet implemented
- TypeScript support included
- Local search provider enabled

## Content Guidelines

- All content is in Chinese (zh-CN)
- Images should be placed in `vitepress-docs/public/images/`
- Manual sections follow the navigation structure defined in config.mts
- The site uses a home layout with hero section and feature cards