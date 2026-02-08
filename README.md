# SwiftData Expert Skill

Expert guidance for AI coding tools using the Agent Skills format.  
Focus: safe persistence architecture, predictable concurrency, migration safety, and CloudKit sync for SwiftData-first projects.

## Installation

```bash
npx skills add https://github.com/vanab/SwiftData-agent-skill --skill swiftdata-expert-skill
```

## Scope

This skill targets:

- SwiftData schema design and lifecycle management
- query and fetch behavior in SwiftUI and service layers
- model context boundaries and mutation safety
- schema evolution and persistent history operations
- CloudKit-compatible storage design
- incremental adoption with Core Data coexistence

## Audience

- teams shipping SwiftData-backed applications
- developers debugging persistence and sync failures
- engineers planning schema changes on existing user data

## Capabilities

### Persistence decisions

- select container and configuration strategy
- separate UI-bound and background persistence flows
- apply deterministic context and save boundaries

### Concurrency safety

- enforce model isolation with `ModelContext` and `@ModelActor`
- avoid cross-context mutable model usage
- use identifier-based handoff patterns

### Query quality

- build stable predicates and sort strategies
- configure `FetchDescriptor` limits and offsets
- reduce unnecessary fetch work

### Migration and history

- apply lightweight and custom migration planning
- model versions with `VersionedSchema`
- process and clean persistent history with tokens

### CloudKit integration

- configure capabilities and container selection
- design within CloudKit schema constraints
- handle SwiftData sync opt-in and opt-out modes

## Skill Structure

```text
swiftdata-expert-skill/
├── SKILL.md
└── references/
    ├── cloudkit-sync.md
    ├── concurrency-and-actors.md
    ├── core-data-adoption.md
    ├── implementation-playbooks.md
    ├── migrations-and-history.md
    ├── model-context-and-lifecycle.md
    ├── modeling-and-schema.md
    ├── querying-and-fetching.md
    ├── relationships-and-inheritance.md
    └── troubleshooting-and-updates.md
```

## Coverage Notes

- Primary focus: SwiftData (`@Model`, `ModelContainer`, `ModelContext`, `Query`, migrations, history, CloudKit).
- Secondary focus: Core Data coexistence boundaries during migration.
