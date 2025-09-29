---
title: Freeze
description: Issue a warning to a local user.
category: [actions, moderate]
layout: handbook
weight: 20
---

## What it does

`{{ page.title }}` locks the user's account.

It is found as an option on the user's account page.

This is useful for giving a **local** user a time-out without severing their
follower connections. The account owner will be notified.

This option is only available for **local** users.

[See the Mastodon documentation for {{ page.title }}.](https://docs.joinmastodon.org/admin/moderation/#{{ page.title | downcase}}-user)

## Is it reversible?

Yes.

## When to use `{{ page.title }}`

Because `{{ page.title }}` silences a user, it is a
`{{ page.category[1] | capitalize }}` action.

{% include handbook/scenarios.md %}
