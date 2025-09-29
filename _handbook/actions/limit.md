---
title: Limit
description: Quarantine an account.
category: [actions, moderate]
layout: handbook
weight: 25
---

## What it does

`{{ page.title }}` reduces the visibility of the account on our instance.

If the account is **local**, the account owner will be notified.

[See the Mastodon documentation for {{ page.title }}.](https://docs.joinmastodon.org/admin/moderation/#{{ page.title | downcase}}-user)

## Is it reversible?

Yes.

## When to use `{{ page.title }}`

Because `{{ page.title }}` affects visibility, it is a
`{{ page.category[1] | capitalize }}` action.

{% include handbook/scenarios.md %}
