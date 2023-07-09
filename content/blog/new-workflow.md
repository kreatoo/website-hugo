---
title: "Latest update - Kreato Linux v2"
date: 2023-07-09T07:00:17+03:00
draft: false
---

Hello!
It has been a while since i have written a blog.
This blog is about the recent path Kreato Linux has been taking on centralizing things.


# The beginning
At first, it was like every other project on the planet. Every project is seperated on a seperate repo.

But that is;

* Boring
* Harder to manage
* And not organized

So i wanted to go with something else.

# v4
While v4 was happening, *many* things got merged onto the main source tree. The merging is now complete!
You now need only **4** repositories to completely get Kreato Linux's source code, and only **1** to build it!

These repos consist of;

* src (Source tree)
* wiki (The wiki)
* kpkg-repo (The main repository)
* And this website!

The source tree now contains all you need, to building the rootfs to pushing the docker image! I tried to make it as tidy as i can. Suggestions are welcome.

This was heavily inspired from how \*BSD operates.

Next step is to fix all the broken packages and (hopefully) bring Flatpak support to Kreato Linux!

v2 will release after everything is done for! We are not far away!

- Kreato
