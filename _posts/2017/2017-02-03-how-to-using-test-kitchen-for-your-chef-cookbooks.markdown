---
layout: "post"
title: "How To - Using Test Kitchen for your Chef Cookbooks"
date: "2017-02-03 07:11"
published: true
tags:
 - chef
 - howto
---

Setup the kitchen env (Provision machine & run cookbooks)
```
kitchen converge
```

Verifies an instance after it has been converged
```
kitchen verify
```

Run both at once (this destroys the end image if test are successful)
```
kitchen test
```
