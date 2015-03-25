Snowdrift.coop
==============

[Snowdrift.coop](https://snowdrift.coop) is a non-profit, cooperative platform
for funding Free/Libre/Open (FLO) works. Using a many-to-many matching pledge,
we aim to empower the global community to better promote freedom-respecting
projects of all sorts.

For the basic idea, see our
[illustrated intro](https://snowdrift.coop/p/snowdrift/w/en/intro).

Other pages on the site explain our
[mission](https://snowdrift.coop/p/snowdrift/w/en/mission)
and include discussion and research on issues like
the
[economics of FLO projects](https://snowdrift.coop/p/snowdrift/w/en/economics),
the
[incentives behind donations](https://snowdrift.coop/p/snowdrift/w/en/psychology),
how our model departs from that of
[other funding sites](https://snowdrift.coop/p/snowdrift/w/en/othercrowdfunding),
and more.


Contributing
===========

Our [how-to-help page](https://snowdrift.coop/p/snowdrift/w/how-to-help)
includes further notes about the site and info about volunteering (including
in non-programming ways). We also have an in-progress, self-hosted
[ticket system](http://snowdrift.coop/p/snowdrift/t).

Snowdrift.coop is built with **Haskell** and the
**[Yesod web framework](http://www.yesodweb.com/)**,
but even if you don't yet know Haskell,
you may still put your HTML/CSS/Javascript skills to work!
We welcome contributions from developers of all skill levels.

Whatever your background, we're happy to answer questions or get any comments.
Hop on #snowdrift at
[freenode.net](http://webchat.freenode.net/?channels=#snowdrift), and say hello!


Essential build instructions
----------------------------

Note: our code is mirrored at
[Gitorious](https://gitorious.org/snowdrift/snowdrift)
(which is FLO, licensed AGPL, but is shutting down soon and we haven't finalized
our move to another FLO service yet) and
[GitHub](https://github.com/snowdriftcoop/snowdrift)
(which is popular but proprietary).

**You really should read our full [guide to our code](GUIDE.md)
which has step-by-step instructions that even a true beginner can follow.**
It also contains links for learning Haskell, comments about development methods,
and more.

But for those experienced with Git, Haskell, PostgreSQL, and perhaps even Yesod,
here's quick and dirty minimal instructions to get started:

```
// Install any dependencies you don't have:
// GHC **7.8.x**, cabal, PostgreSQL, zlib1g-dev, libpq-dev, happy, alex
// update cabal, set PATH, etc. — see GUIDE.md for more detailed instructions

// Fork, clone and install
git clone [your remote address]
// your remote looks like git@gitorious.org:snowdrift/yourusername-snowdrift.git]
cd snowdrift
cabal sandbox init
cabal install --enable-tests -fdev

// Set up the database with our quick script.
// To understand what the script does or to run the commands manually, see GUIDE.md
sdm init

// Launch the development site
Snowdrift Development

// To see the live site, point your browser to localhost:3000

// To rebuild after making changes run
cabal install -fdev

Read through GUIDE.md for thorough details about development, testing, and so on.
```
