---
layout: post
title: Scalability
---

<p>So as I've been playing around with arrays, hashes, and such, I came across a fun and easy example of how a lack of scalability in your programs can really come back to bite you.</p>
<p>Here's an example problem for you to solve; take the following array: </p>

<pre><code>[["a", "b", "p"], ["c", "d"], ["e", "f"], ["g", "h", "i", "j"]]</code></pre>

<p>And return the following: </p>
<ul>
  <p>abp</p>
  <p>cd</p>
  <p>ef</p>
  <p>ghij</p>
</ul>

<p>My first approach was to do the following: </p>
<pre><code>
x.each do |a, b, c, d|
	if a and b and c and d
		puts "#{a}#{b}#{c}#{d}"
	elsif a and b and c
		puts "#{a}#{b}#{c}"
	elsif a and b
		puts "#{a}#{b}"
	elsif 
		puts "#{a}"
	end
end
</code></pre>

<p>Easy enough, right? Well, what if that array wasn't static? What if one of those inner arrays held, say, 5 values? If you guessed that the 5th value of one of the inner rays wouldn't be returned, you would be correct! Check out the following code, which requires less lines AND can 'scale':</p>
<pre><code>
x.each do |outer|
	outer.each do |inner|
		print inner
	end
	puts
end
</code></pre>
<p> Loops within loops: difficult to grasp at first, but common AND useful!</p>
