---
layout: post
title: Scalability
---

<p>So as I've been playing around with arrays, hashes, and such, I came across a fun and easy example of how a lack of scalability in your programs can really come back to bite you.</p>
<p>Here's an example problem for you to solve: </p>

<pre><code>[["a", "b", "p"], ["c", "d"], ["e", "f"], ["g", "h", "i", "j"]]</code></pre>

<p>And return the following: </p>
<ul>
  <li>abp</li>
  <li>cd</li>
  <li>ef</li>
  <li>ghij</li>
</ul>