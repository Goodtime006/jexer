Jexer Work Log
==============

March 21, 2017

I am starting to gear up for making Jexer a serious project now.  I've
created its SourceForge project, linked it back to GitHub, have most
of its web page set up (looks like Qodem's), and released 0.0.4.  And
then this morning saw an out-of-bounds exception if you kill the main
demo window.  Glad I marked it Alpha on SourceForge...

Yesterday I was digging around the other Turbo Vision derived projects
while populating the about page, and made a sad/happy-ish realization:
Embarcadero could probably get all of them shut down if it really
wanted to, including Free Vision.  I uncovered some hidden history in
Free Vision, such that it appears that Graphics Vision had some
licensed Borland code in it, so there might be enough mud in the air
that Free Vision could be shut down the same way RHTVision was.  But
even worse is the SCOTUS ruling on Oracle vs Google: if APIs are
copyrighted (regardless of their thoughts on fair use), then any
software that matches the API of a proprietary project might find
itself subject to an infringement case.  So that too could shut down
the other API-compatible TV clones.

Fortunately, Jexer (and D-TUI) is completely new, and has no API
compatibility with Turbo Vision.  Jexer could be a new root to a whole
generation of TUI applications.

March 18, 2017

TStatusBar is working, as is "smart" window placement.  Overall this
is looking quite nice.  Found a lot of other small paper cut items and
fixed them.  It looks absolutely gorgeous on Mac now.

Tomorrow I will get to the public wifi and get this uploaded.

Time to call this 0.0.4 now though.  We are up to 32,123 lines of
code.

March 17, 2017

Jexer is coming back to active development status.  I had a lot of
other projects ahead of it in the queue, mostly Qodem but also Jermit
and of course lots of actual day job work keeping me too tired for
afterhours stuff.  But here we are now, and I want to get Jexer to its
1.0.0 release before the end of 2018.  After that it will be a
critical bit of function for IWP and NIB, if I ever get those going.
I need to re-organize the demo app a bit so that it fits within 80x25,
and then get to TStatusBar.

A status bar will be an optional part of TWindow.  If it exists, then
it will be drawn last by TApplication and get events routed to it from
TWindow's event handlers.  This will have the nice effect that the
status bar can change depending on which window is active, without any
real extra work on TApplication's part.

Putting together a proper TODO now, with release and regression
checklists.  I think I will see if jexer is available at SourceForge,
and if so grab it.  Perhaps I can put together some good Turbo Vision
resources too.  At the very least direct people to the Borland-derived
C++ releases and Free Vision.

