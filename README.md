# CIMTK Plugins

Cyber Incident Management Toolkit assistants, packaged as a ChatGPT plugin. Seven
skills for the work incident managers actually do: briefing executives, drafting
public statements, pressure-testing a message before it goes out, commissioning
threat intelligence, running a third-party incident, and building an exercise.

From [cyberincidentcommander.com](https://cyberincidentcommander.com). Some of these
are used on the SANS LDR553 course; the rest are here because they earn their place.

## What is in it

| Skill | What it does |
| -- | -- |
| `exec-briefing` | Turns incident information into an executive briefing in the CIMTK 3-Whats (3x5) format. |
| `ir4u-retainer-team` | Reviews your incident material as a simulated external IR retainer team and returns a consolidated assessment. |
| `public-comms-advisor` | Turns incident information into a public communication that informs without damaging the investigation. |
| `comms-focus-groups` | Reads a drafted staff message as a panel of employees and tells you how each group will take it. |
| `cti-requirements-coach` | Coaches you through writing intelligence requirements worth sending, and judging what comes back. |
| `supply-chain-incident-navigator` | Walks an Incident Commander through a third-party incident: notification analysis, blast radius, SAQS development, CURTAIN as concurrent lanes. |
| `security-exercise-generator` | Builds a runnable four-phase tabletop of about 80 minutes for your team and theme. |

## Installing it

**From a workspace.** A ChatGPT workspace admin can import this repository as a
plugin marketplace, which syncs daily. Point the import at this repository URL; the
manifest is `.agents/plugins/marketplace.json`.

**On your own machine.** Clone or download this repository, then add it to your
personal marketplace at `~/.agents/plugins/marketplace.json`:

```json
{
  "name": "cimtk",
  "interface": { "displayName": "CIMTK" },
  "plugins": [
    {
      "name": "cimtk",
      "source": { "source": "local", "path": "~/cimtk-plugins/plugins/cimtk" },
      "policy": { "installation": "AVAILABLE", "authentication": "ON_INSTALL" },
      "category": "Productivity"
    }
  ]
}
```

Restart the ChatGPT desktop app, install CIMTK from your marketplace, then start a
chat and type `@exec-briefing`.

**Without installing anything.** Every skill is a plain configuration. Open its
`SKILL.md`, copy the text below the frontmatter, and paste it into any chat:

```text
Here is a new config:
"""
[paste the configuration here]
"""
```

## Generated, not hand-edited

The skills are generated from the CIMTK configuration sources. Edits made directly
to a `SKILL.md` here are overwritten on the next build. Raise an issue instead.

## Licence

[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/). Use them, adapt them,
run them inside your own organisation, and credit Steve Armstrong-Godwin / AG Cyber.
Do not sell them, or build them into a commercial product or paid training, without
asking first.
