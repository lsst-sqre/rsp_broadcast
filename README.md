# Broadcast messages for the Rubin Science Platform

This repository contains the content source for broadcast messages of all RSP environments managed by [Phalanx](https://github.com/lsst-sqre/phalanx).
A *broadcast* is a message that appears to all RSP users, and may be visible to anonymous users on the RSP's homepage ([Squareone](https://github.com/lsst-sqre/squareone)) as well.
These broadcasts are the content seen in the red ribbon at the top of the home page, for instance.

Broadcasts are individual Markdown files in the [`broadcasts/`](./broadcasts) directory.
Once you commit or merge to the default branch (`main`), broadcasts are refreshed automatically in each RSP environment through the [Semaphore](https://github.com/lsst-sqre/semaphore) service.

## Writing broadcast messages, if you're in a hurry

The canonical resource for learning how to write and schedule broadcast messages is the [Semaphore documentation](https://semaphore.lsst.io).
This section provides a primer for writing messages and controlling their visibility in RSP environments.

### Each broadcast is a `.md` file in the broadcasts directory

A basic broadcast markdown file looks like this:

```markdown
---
summary: The summary line, **markdown formatted**, should ideally be a sentence or two.
---

The markdown body is for additional content and can include multiple
paragraphs, links, lists, code blocks, images (externally-sourced), you name
it. Any [GitHub-flavoured markdown content](https://github.github.com/gfm/) is
allowed.

This content is only shown when a user interacts with a message by tapping on
"Show more" or the equivalent button.
```

The **summary** is **required** for every message
The **body** (content outside the `---` fences) is **optional**.

Both are formatted as [GitHub-flavoured Markdown](https://github.github.com/gfm/).

### Target RSP environments with the `env` front-matter field

Without an `env` field, the message may be sourced by **all RSP environments!**

To target a single environment, set its Phalanx environment name in the `env` field:

```markdown
---
summary: The markdown-formatted broadcast message.
env: idfprod
---
```

To target multiple environments, make `env` an array instead:

```markdown
---
summary: The markdown-formatted broadcast message.
env:
  - idfprod
  - stable
---
```

The [Phalanx README](https://github.com/lsst-sqre/phalanx#environments) includes a list of environment names.

### Turn a message off, regardless of other scheduling

To "hide" a broadcast that is currently visible, or is scheduled to become visible, you have two options:

1. Delete the message's file (`git rm` and commit).
   This is useful if you're confident you won't need that message in the future.

2. Toggle the message off by adding `enabled: false` to the message's front-matter.
   This is useful for temporarily disabling a message.

This is a disabled message:

```markdown
---
summary: This message is disabled.
enabled: false
---
```

To re-enable the message (which is also the default):

```markdown
---
summary: This message is disabled.
enabled: true
---
```

### Information messages (category)

By default, messages are in the ``maintenance`` category to tell users about system stability issues.
For informational messages, such as announcements or calls-to-action, you can instead, create an "info" message by setting ``category: info`` in the front-matter:

```markdown
---
summary: This is an informational message.
category: info
---
```

In Squareone, informational message are displayed in Rubin teal; maintenance messages in red.
