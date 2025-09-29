---
title: Warn
description: Issue a warning to a local user.
category: [actions, minor]
layout: handbook
weight: 10
---

## What it does

`{{ page.title }}` sends a written warning to the user. Templates are
available.

This is useful for recommending that a user change their conduct or amend
their content to abide by the rules.

This option is only available for **local**, users.

It is found as an option in the `Custom` action.

[See the Mastodon documentation for {{ page.title }}.](https://docs.joinmastodon.org/admin/moderation/#{{ page.title | downcase}}-user)

## Is it reversible?

Yes.

## When to use `{{ page.title }}`

Because `{{ page.title }}` is just a special type of message, it is a
`{{ page.category[1] | capitalize }}` action.

{% include handbook/scenarios.md %}

