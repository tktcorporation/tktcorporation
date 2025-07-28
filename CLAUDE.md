# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a GitHub profile repository for @tktcorporation that automatically generates and displays development metrics and profile summary cards using GitHub Actions.

## Key Components

### Profile Summary Cards
- Located in `profile-summary-card-output/` directory
- Contains 60+ theme variations, each with 5 SVG files showing different metrics
- Automatically generated via GitHub Actions workflow

### GitHub Actions Workflows

1. **Waka Readme** (`.github/workflows/waka-readme.yml`)
   - Updates README with WakaTime development metrics
   - Runs daily via cron schedule
   - Requires `WAKATIME_API_KEY` and `GH_PERSONAL_ACCESS_TOKEN` secrets

2. **Profile Summary Cards** (`.github/workflows/profile-summray-cards.yml`)
   - Generates GitHub profile summary cards in multiple themes
   - Runs daily via cron schedule
   - Uses GitHub token for authentication

## Common Commands

Since this is a profile repository with automated workflows, there are no build or test commands. The primary interactions are:

- **Trigger workflow manually**: Use GitHub Actions UI or `workflow_dispatch` event
- **View generated metrics**: Check the README.md file or browse the SVG files in `profile-summary-card-output/`

## Working with This Repository

When making changes:
- The README.md contains sections managed by GitHub Actions (between `<!--START_SECTION:waka-->` and `<!--END_SECTION:waka-->`)
- Profile summary cards are referenced via raw GitHub URLs in the README
- All workflows are scheduled to run daily but can be triggered manually