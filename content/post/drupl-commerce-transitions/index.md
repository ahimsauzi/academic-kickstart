---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Drupl Commerce Transitions"
subtitle: "Changing order state in Drupal Commerce 2.x"
summary: "How to use State Machine methods of the Drupal Commerce Order class to transition order
from one state to the next."
authors: []
tags: ["Drupal Commerce", "Drupal 8", "Commerce order"]
categories: ["Drupal", "Commerce"]
date: 2019-07-10T17:37:18-07:00
lastmod: 2019-07-10T17:37:18-07:00
featured: false
draft: false
math: true
highlight: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
Using the State Machine methods of the Drupal Commerce Order class we can transition order
from one state to the next.

```php
$order_state = $orderObj->getState();
$order_state_transitions = $order_state->getTransitions();
$order_state->applyTransition($order_state_transitions['complete']);

$orderObj->save();
```