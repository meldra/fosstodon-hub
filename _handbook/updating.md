---
title: Reference material for this handbook
description: Understanding and maintaining this documentation.
category: intro
layout: handbook
weight: 1
---

Contents:

* TOC
{:toc}

## Severities

Severity levels are defined as:

- `severe`

  Actions which have permanent consequences.

- `moderate`

  Fully-reversible actions which involve silencing a user.

- `minor`

  Fully-reversible actions which do not affect the user's reach.

- `deferred`

  Closing the report and recording context for future reference.

## Adding actions

Moderation actions are stored in `/_handbook/actions`.

### Frontmatter

Their frontmatter takes the following format:
```
---
title: Warn
description: Issue a warning to a local user.
category: [actions, minor]
layout: handbook
weight: 10
---
```

`title` is the name of the action. Some actions have anchors in the Mastodon
documentation. The title in the frontmatter should be consistent with these
when they exist, as this allows using `{% raw %}{{ page.title }}`
or `{{ page.title | downcase }}{% endraw %}` throughout the page for
consistency.

`description` should briefly describe what the action does.

`category` must take the form of an array. `action` must be the first
category in the array. The array must contain a
[severities category](#severities).

`layout` must be `handbook`.

`weight` dictates the position of the action in lists in relation to other
actions. Actions must be weighted by the severity ranking.

### Page sections

Action pages should contain the following sections as second-level headings:

- What it does

  This section should:
  - Expand on the definition in the `description` frontmatter.
  - Identify if the account owner is notified.
  - Identify differences in behavior between local or external accounts.

- Is it reversible?

  This section should provide a simple clear response, such as "Yes", "No",
  or "Partially". Answers other than "Yes" must describe what is lost.

- When to use \`{% raw %}{{ page.title }}{% endraw %}\`

  This section must contain the following template code:
  
  `{% raw %}{% include handbook/scenarios.md %}{% endraw %}`
  
  This code will produce a list of appropriate situations for this action to
  be considered for use.

  You may provide other context around this.

## Adding Scenarios

Scenarios describe some common incident types that may show up in the reports
queue. They describe how to evaluate a situation with relevent context.

### Frontmatter

```
---
title: Emotional outbursts
description: Anger, protests, and other high emotions.
category: [scenarios, minor, deferred]
layout: handbook
weight: 2
---
```

`title` is a broad name for a general type of scenario. Unlike actions, there
is no need to keep consistency for external references.

`description` should briefly describe what the action does.

`category` must take the form of an array. `action` must be the first
category in the array. The array may contain multiple subsequent categories.
The options for these categories are the defined in the
[severities section](#severities) above.

`layout` must be `handbook`.

`weight` dictates the position of the action in lists in relation to other
actions. Actions must be weighted by the severity ranking.

### Page sections

- What does it look like?

  This section describes what a scenario might look like. It doesn't use
  actual specific examples, as those can give the illusion of simplicity
  for complex situations.

- What is the risk?

  This describes the visibility of this incident type to other users, and
  explains the social consequences of allowing the behavior to continue.

  The description may also explain the consequences of acting too harshly.

- Is user-level moderation sufficient?

  This section should explain if user-level moderation is a valid expectation,
  and what the consequences of expecting it may be.

- How to address

  Similar to the actions, this section must contain the following template
  code:
  
  `{% raw %}{% include handbook/scenarios.md %}{% endraw %}`

  This code will produce a list of appropriate actions for moderators to
  considered when dealing with this kind of incident.

  You may provide other context around this.

## Adding navigation guides

Navigation guides help moderators figure out how to find their way around the
Mastodon moderation UI.

### Frontmatter and include

Almost everything in the navigation guides pages is contained in the
page's frontmatter. Everything else is that itty bit of Liquid code down
there. This is the whole page.
{% raw %}
```
---
title: Report without posts
description: A report was submitted without any posts flagged.
category: navigation
layout: handbook
weight: 2
steps:
  - Click on the `View profile` button found in the report information grid at the top of the page.
  - Click on the box that contains the post count. The count is `18 posts` in this example. This is the number of posts that the user's server reports that they have made.
  - The known posts will be displayed on the next page. The page will only show posts your server has seen.
---

{% include handbook/navigation.md %}

```
{% endraw %}

### Images

Each of those `steps` in the frontmatter must correspond to an image. The
images are stored in `/assets/images/handbook/`.

Each page's images must be in a folder that named for the slugified title. In
this case it would be `/assets/images/handbook/report-without-posts`.
The files must be `.png` format, and must be named for the step number, starting
at `0`.

Images should have any identifying information about the affected account or
moderator redacted.
