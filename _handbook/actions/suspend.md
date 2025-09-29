---
title: Suspend
description: Ban an account.
category: [actions, severe]
layout: handbook
weight: 35
---

## What it does

`{{ page.title }}` bans the account from our instance.

If the account is **local**, the account owner will be notified.

[See the Mastodon documentation for {{ page.title }}.](https://docs.joinmastodon.org/admin/moderation/#{{ page.title | downcase}}-user)

## Is it reversible?

Partially.

When using this action, you must be comfortable with potentially breaking
that individual's follower relationships. Relationships may not be restored if
the suspension is undone.

## When to `{{ page.title }}`

Because `{{ page.title }}` can cause data loss and silences the user, it is a
`{{ page.category[1] | capitalize }}` action.

{% include handbook/scenarios.md %}


