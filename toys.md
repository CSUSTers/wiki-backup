---
title: 别老惦记你那
description: 
published: true
date: 2022-02-22T02:06:04.448Z
tags: 
editor: markdown
dateCreated: 2022-02-22T02:06:04.448Z
---

```scheme
(((λ (f)
     ((λ (x)
        (f (x x)))
      (λ (x)
        (f (x x))))
   (λ (f)
     (string-append
      "别老惦记着你那破"
      (f)
      "了")
     ))))
```

```scheme
(((λ (f)
     ((λ (x)
        (f (x x)))
      (λ (x)
        (f (x x)))))
   (λ (f)
     (λ (n)
       (if (> n 0)
         (string-append
          "别老惦记着你那破"
          (f
           (- n 1))
          "了")
         ""))))
  10)
```