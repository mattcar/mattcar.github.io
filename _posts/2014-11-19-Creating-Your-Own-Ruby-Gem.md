---
layout: post
title: Creating Your Own Ruby Gem
---

<p>I'm sure an avid rubyist like yourself has relied heavily on gems created by the community. And I'm also sure, being the good person you are, you want to give back to that community! Well, good person or not (I don't judge), you can utilize this tutorial to get yourself going.</p>

<p>Before doing anything else, create a new account at http://rubygems.org (this assumes you don't already have one). Remember your password! Then, in your terminal, log in with the command: gem push</p>

<p>If you intend to make an executable gem, make sure you check out the final list</p>

<ol>
	<li>Choose a name for your gem and then do the following: bundle gem gem_name (not the underscores for spaces)</li>
	<li>cd into the gem name directory</li>
	<li>Edit spec.summary inside your gemspec file. (Make sure you get rid of the TODO!)</li>
	<li>Edit spec.description inside your gemspec file. (Again, make sure you get rid of the TODO!)</li>
	<li>Optional: If your gem is going to be dependent on another gem, add the dependency to your gemspec file (example: spec.add_dependency "weather_guy", "~> 0.0.5”).</li>
	<li>Prove that you're way ahead of other developers by editing your README file and making it readable AND useful.</li>
	<li>Write your code!</li>
		<ul><li> If your whole gem is just an executable, you can, technically, write all your gem code exclusively inside this executable file (more on this down further). However, it’s best practice (for organization and conventions’ sake) to put the main code somewhere in the lib/gem_name folder and refer to that code from your executable.</li></ul>
	<li>You don’t need git init, as it happens automatically when you create your gem:</li>
		<ul><li>git add —all</li></ul>
		<ul><li>git commit -m ‘initial commit’</li></ul>
	<li>To test out your gem locally, run: rake install</li>
	<li>Finally, run: rbenv rehash</li>
</ol>

<p>RELEASE INTO THE WILD</p>
<ol>
<li>Create github repo and push your code up there</li>
<li>run 'rake release' in terminal</li>
</ol>

<p>Note the following for building an executable gem</p>
<ol>
<li>Create a new folder at the root called bin.</li>
<li>Create a file inside of the bin folder and give it the same name as the command that will initiate the gem in the terminal</li>
<li>Add this to the top of the new file: #!/usr/bin/env ruby</li>
<li>From your terminal, run the chmod +x command on that file, for example: chmod +x bin/matt_rules
This changes the file from one that is read-and-write-only to one that is runnable (executable).</li>
<ul><li>Write your code in this file! You can, technically, write all your gem code exclusively inside this executable file. However, it’s best practice (from organization and conventions’ sake) to put the main code somewhere in the lib folder and refer to that code from your executable. If you want to get things to work on a basic level, you can try it out first in this file and always move code over later.</li></ul>
</ol>


<p><a href="https://github.com/mattcar/weather_guy">Check out this super great example</a></p>
