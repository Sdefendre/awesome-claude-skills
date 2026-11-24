---
name: apple-app-intents
description: Build and review iOS apps with App Intents, App Entities, App Shortcuts, and App Schemas for Siri and Apple Intelligence. Use when adding Siri actions, entity search, onscreen awareness, or migrating existing Shortcuts integrations.
---

# Apple App Intents

Teach a coding agent to add App Intents, App Schemas, App Shortcuts, and related Siri and Apple Intelligence integrations to an iOS app. The maintained skill, installer, Swift example, and research notes live in [Sdefendre/apple-app-intents-skill](https://github.com/Sdefendre/apple-app-intents-skill). MIT licensed.

## When to Use This Skill

- Adding Siri actions, App Shortcuts, or App Schema support to an iOS app
- Auditing an existing Shortcuts or App Intents integration
- Mapping app entities and queries to Apple's current supported schemas
- Validating what can actually be tested on a given SDK and device

## What This Skill Does

1. **Capability mapping**: Map real app actions and data to custom intents or schema-conforming entities.
2. **Implementation guidance**: Persistent entities, queries, App Shortcuts, shared services, background execution, and navigation.
3. **Validation**: Separate business-logic tests, metadata extraction, system execution, and on-device checks. A green unit test is not a complete Siri experience.

## How to Use

Install the skill from the source repository (Git and Python 3.10+ for the optional installer):

```
git clone https://github.com/Sdefendre/apple-app-intents-skill.git
cd apple-app-intents-skill
python3 scripts/install.py --agent claude
```

Site: https://sdefendre.github.io/apple-app-intents-skill/

### Basic Usage

```
Use the apple-app-intents skill to audit this app's Siri integration. Preserve existing shortcuts. Implement the missing entity queries, schema requirements, indexing lifecycle, and cold-launch navigation, then show the build and device-test evidence.
```

### Advanced Usage

```
Use the apple-app-intents skill to build a SwiftUI reading-list app. Let me save articles, find them, mark them read, and open a specific article. Map each capability to the current supported App Schema or a custom intent. Include entity queries, persistence, App Shortcuts, and tests. Explain which Siri capabilities can actually be verified on my SDK and device.
```

## Example

**User**: "Use apple-app-intents to add a searchable Notes-style entity and an open-item intent that works after a cold launch."

**Output**: A capability map (action, service, entity/query, exact schema or custom intent, evidence needed), then an implementation plan that preserves the app's architecture and records what still has to be verified on a device.

**Credit:** Created by Steve Defendre. Source: https://github.com/Sdefendre/apple-app-intents-skill

## Tips

- Building iOS apps requires macOS and full Xcode. Testing Siri needs an eligible device, OS, enabled services, and a supported language and region.
- The research baseline is 10 September 2026, including WWDC26. Recheck Apple's current docs when choosing APIs.
- Not every custom intent is discoverable through Siri AI.

## Common Use Cases

- New App Intents integration in a SwiftUI app
- Migration of an older Shortcuts or App Intents setup
- Review of schema fit, required groups, and test evidence
