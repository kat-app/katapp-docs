+++
title = "Getting Started"
weight = 1
+++

<div class="text-center">
  <img src="/katapp-logo-name.png" alt="KatApp Logo" class="mb-4" style="max-width: 300px;">
</div>

# Welcome to the KatApp Setup Guide

This guide walks you through setting up your local KatApp development environment. Use the sidebar navigation to follow the setup steps that match your needs.

> **Note:** If you're a regular user, your environment is already configured. Head to the [User Documentation](/user-documentation) for usage instructions.

## Prerequisites

### Docker Desktop (Recommended)

[Docker Desktop](https://www.docker.com/products/docker-desktop/) is our recommended tool for containerization. It streamlines the setup process significantly.

### Alternative: Rancher Desktop

If you're working in an organization:
- Docker Desktop may require a paid license
- Contact your IT help desk for license information
- Alternatively, use [Rancher Desktop](https://rancherdesktop.io/) - a free, open-source alternative with full Docker CLI support

## Local Development Setup

There are 3 ways to set up KatApp for local development:

1. **Quickstart** - Everything runs locally in Docker containers
2. **Local App Development** - The app runs locally but uses the cloud-based backend
3. **Full Local Development** - Everything runs locally with hot reloads for all components

## Quick Access

{{% children depth="1" style="h4" %}}