# Use MKDocs, MKDocs-Material, and MKDocs-Monorepo for documentation

- Status: accepted
- Deciders: Derek Murawsky
- Date: 2/17/2022

Technical Story: Documentation is key for many reasons cheif among them being that I will forget how I did this in a year.

## Context and Problem Statement

As a human who forgets things, including where I documented something, I need to have clear documentation available in the same repo as the code that it documents.

## Decision Drivers

- Markdown is easy, and used in most project by default
- I already know MKDocs
- I want to learn MKDocs Monorepo for much of the work I do professionally

## Considered Options

- MKDocs with Material & Monorepo
- Plain Old Readmes with Markdown

## Decision Outcome

Chosen option: MKDocs with Material

### Positive Consequences

- It's really quite good looking and fairly simple to implement.
- I can generate a separate website and host it with github pages easily.

### Negative Consequences

- It's more complicated than Plain Old Readmes

## Links <!-- optional -->

- [MKDocs](https://www.mkdocs.org/)
- [MKDocs Material](https://squidfunk.github.io/mkdocs-material/)
- [MKDocs Monorepo](https://github.com/backstage/mkdocs-monorepo-plugin) plugin.

<!-- markdownlint-disable-file MD013 -->