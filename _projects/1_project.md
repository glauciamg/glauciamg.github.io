---
layout: page
title: Device-independent cryptography
description: It leads to cryptographic protocols that are secure even
when the systems are not well characterized or manufactured by an untrusted provider.
img: assets/img/diqkd2.png
importance: 1
category: work
---

Quantum properties lead to levels of security for cryptographic tasks that are inconceivable
even with the most powerful classical technology. The notorious example is quantum key
distribution (QKD), in which two parties, Alice and Bob, establish a secret key unknown to an
eavesdropper, Eve, with unlimited resources. This allows them to communicate with unconditional
security, in contrast to current cryptosystems that rely on computational assumptions.
A successful implementation of QKD requires a precise characterization of the underlying
quantum system. Deviations from such assumptions led to the hacking of many commercially
available QKD schemes. Hence, without a full characterization of the systems, or if they are
manufactured by an untrustworthy provider, can we still achieve secure communication? Surprisingly,
quantum properties also offer a solution to this problem, and secure communication can
be established even when the users are ignorant about the internal working of their devices. This
is the device-independent (DI) paradigm, which models systems and measurement apparatuses as black boxes where the only relevant information is the statistics of inputs (measurement
settings) and outputs (measurement outcomes).




The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %}
