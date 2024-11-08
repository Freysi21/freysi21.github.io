---
layout: post
title:  "The most to-the-point guide about setting up a gitpage with a custom domain of the top of my head"
date:   2024-11-04 17:43:24 +0000
categories: development shotgun 
---
<link rel="stylesheet" type="text/css" href="{{ site.baseurl }}/assets/css/styles.css">


Create account and buy the domain. Get that done ASAP. DNS stuff usually takes some time to process. 

Create account and create a repo named [github-username].github.io.

Get ruby, vscode and jekyll.

Write vscode:https:://github.com/[github-username]/[github-username].github.io

run jekyll new . in the root of your repo.

push this out to your repo.

go to github and select settings in the avatar/profile img menu. The toothy wheel. 

Under Automation and (something else...) go to pages. Enter the name of you domain like so example.com

Don't include www. thats something else called apex or sum shit like dat.

press verify/save or whatever is next to the button.

Here you get TXT stuff 4 ur DNS stuff. Put that in the DNS Provider(The thing u bought the domain).  
At this point if you did the dns in the beginning it might be processed and available for tweaking.

Im not going into specifics about the dns since that varies between provider. So just get ur self into an edit menu for your dns rec you bought. Pencil icon or sum. There should be a dropdown with the TXT value among AAAA, MX, CNAME and maybe some other stuff. Dont stress the other stuff just select the TXT. Add _github-pages-challenge value to the host field, usually the first input field (other then the dropdown). Add the long string of gibberish to the other. 
Now you gotta take care of sending request to the dns to github nameservers. 

Add four A records with this IPs

185.199.108.153

185.199.109.153

185.199.110.153

185.199.111.153

Now ur done in ur dns provider

Go back to github and press verify. Now ya verified dns with github.

Now its ready for use. But nothing has been selected for it. So go to the [github-username].github.io repository setting. Not the profile/avatar settings. 

Under Automation and creamation select pages. 

write in ur domain into the only text input

press save. Some check is gonna start. If that fails you should probs find a better guide. If not congratz. Ya got a website that you can tweak and have fun with.

You can find more stuff on the code you are working with in the repo by looking into jekyll and minima. Also I recommend you add sass for styling. 