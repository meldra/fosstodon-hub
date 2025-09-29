---
title: Sensitive
description: Forces media to be opt-in
category: [actions, moderate]
layout: handbook
weight: 15
---

## What it does

`{{ page.title }}` forces all of the account's media to be hidden behind a
content warning.

This is useful for media that is not serious enough for deletion but which
people commonly want to opt-in to seeing.

If the account is **local**, The account owner will be notified.

[See the Mastodon documentation for {{ page.title }}.](https://docs.joinmastodon.org/admin/moderation/#{{ page.title | downcase}}-user)

## Is it reversible?

Yes.

## When to use `{{ page.title }}`

Because `{{ page.title }}` affects visibility, it is a
`{{ page.category[1] | capitalize }}` action.

{% include handbook/scenarios.md %}
