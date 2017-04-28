---
layout: post
title: Internship in INRIA
date: '2017-4-28T00:00:00.000+02:00'
author: Nicola Pezzotti
tags:
- Research
- Visual Analytics
- Data Structures
- Progressive Visual Analytics
- INRIA

---

A couple of weeks ago I started by internship in the [INRIA][1]'s research team [AVIZ][2].
I'm working with the scientific leader of the team, [Jean-Daniele Fekete][3], on the development of efficient data structures that support the progressive analysis of large datasets.

Due to the efficiency requirements of our solution, I'm spending quite some time in optimizing my C++ code.
I'm using [Valgrind][4] and [kcachegrind][5] to, respectively, profile and analyze my code performance.
kcachegrind creates a [treemap visualization][6] of the call performed by my benchmark code, allowing for the identification of critical functions that requires an optimization.

<center>
<img src="{{ site.baseurl }}/images/kcachegrind.png">

</center>


[1]: https://www.inria.fr/centre/saclay
[2]: http://aviz.fr/
[3]: https://en.wikipedia.org/wiki/Jean-Daniel_Fekete
[4]: http://valgrind.org/
[5]: http://kcachegrind.sourceforge.net/html/Home.html
[6]: https://en.wikipedia.org/wiki/Treemapping
