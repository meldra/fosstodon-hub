---
title: Delete posts
description: Removes a user's messages.
category: [actions, severe]
layout: handbook
weight: 30
---

## What it does

`{{ page.title }}` removes the reported messages. Moderators are able to both
add and remove posts from the original report.

If the account is **local**, the account owner will be notified.

## Is it reversible?

No.

When using this action, you must be comfortable with silencing the message
that you are deleting. At the time of writing (current version is v4.4.5), it
is not possible to recover the deleted messages due to protocol limitations.

## When to `{{ page.title }}`

Because `{{ page.title }}` will cause data loss and silences the user, it is a
`{{ page.category[1] | capitalize }}` action.

{% include handbook/scenarios.md %}


