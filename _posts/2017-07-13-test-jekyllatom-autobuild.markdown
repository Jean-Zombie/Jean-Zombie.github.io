---
layout: post
title: "Jekyll's autobuild feature"
date: "2017-07-13 12:34:53 +0200"
---

I had one problem with my blog workflow: The manual building of the html with _Jekyll_. After I finished writing a post in _Atom_ I would have had to manually execute `jekyll serve` in my bash before I could push the changes to GitHub.

But it doesn't need to be like that. You can simply add this line to your __config.yml_:   
`Atom:`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Jekyll: Toggle Auto Build`

Now, whenever you save your article in _Atom_ the html will be build automatically. Given the path to your _Jekyll_ binary is set and recognized by _Atom_. I had to provide the full path in the _Jekyll-Atom_-plugin under "Settings", "Build command":    
`[path/to/your/jekyll/bin], build`
