---
title: Description of an Alembic
categories:
- General
- External sources
feature_image: "https://picsum.photos/2560/600?image=872"
---

The complete distilling apparatus consists of three parts: the "cucurbit" (Arabic ḳarʿa, Greek βίκος), the still pot containing the liquid to be distilled, which is heated by a flame; the "head" or "cap" (Arabic anbiḳ, Greek ἄμβιξ) which fits over the mouth of the cucurbit to receive the vapors, with an attached downward-sloping "tube" (Greek σωλήν), leading to the "receiver" (Arabic ḳābila, Greek ἄγγος or φιάλη) container.

<!-- more -->
---
title: "Edge Case: Nested and Mixed Lists"
categories:
  - Edge Case
tags:
  - content
  - css
  - edge case
  - lists
  - markup
---

Nested and mixed lists are an interesting beast. It's a corner case to make sure that

* Lists within lists do not break the ordered list numbering order
* Your list styles go deep enough.

### Ordered -- Unordered -- Ordered

1. ordered item
2. ordered item 
  * **unordered**
  * **unordered** 
    1. ordered item
    2. ordered item
3. ordered item
4. ordered item

### Ordered -- Unordered -- Unordered

1. ordered item
2. ordered item 
  * **unordered**
  * **unordered** 
    * unordered item
    * unordered item
3. ordered item
4. ordered item

### Unordered -- Ordered -- Unordered

* unordered item
* unordered item 
  1. ordered
  2. ordered 
    * unordered item
    * unordered item
* unordered item
* unordered item

### Unordered -- Unordered -- Ordered

* unordered item
* unordered item 
  * unordered
  * unordered 
    1. **ordered item**
    2. **ordered item**
* unordered item
* unordered item