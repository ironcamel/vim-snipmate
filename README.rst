============
snipmate.vim
============

:Author: `Michael Sanders`_
:Maintainer: `Rok Garbas`_
:Homepage: http://www.vim.org/scripts/script.php?script_id=2540 
:Contributors: `MarcWeber`_, `lilydjwg`_, `henrik`_, `steveno`_, `asymmetric`_, `jherdman`_, `ironcamel`_, `honza`_, `jb55`_, `robhudson`_, `kozo2`_, `MicahElliott`_, `darkwise`_, `redpill`_, `thisgeek`_, `sickill`_, `pose`_, `marutanm`_, `r00k`_, `jbernard`_, `holizz`_, `muffinresearch`_, `statik`_, Eustaquio Rangel, `alderz`_


.. contents::


Why forking snipMate?
=====================

::

    After several unsuccessful attempts of contacting Michael Sanders, no
    commits in last half year and long pull request line on github (none of
    pull requests were commented/replied/rejected) I decided to take action,
    step up and bring some love to this widely used plugin.

    But nothing to worry about. We all get busy, accupied with our daily work
    or just lose interest in doing boring maintainance.

    While reviewing pull requests on github.com/msanders I found lots of great
    improvements and I decided to **friendly** fork it, review and apply patches
    that were sent, notify all the patch submitters and decided to maintain
    snipmate.vim from now on. Of course if somebody wants to
    help, please do not hesitate to write me, I am open to any suggestions.

    Maybe I will only maintain it for a while until Michael Sanders takes things
    back into his hand or until some other super-hero shows up.

    Tnx and happy snipmating, Rok Garbas, 2011-02-02


Changelog
=========


1.0 [Unreleased]
----------------

    * Adding ``css.snippets`` from `tisho`_
      (https://github.com/tisho/css-snippets-snipmate)
      [2011-04-17, `garbas`_]

    * Lots of updates to snippets.

    * Made the trigger key configurable, https://github.com/garbas/vim-snipmate/pull/4.
      [2011-04-13, `thenoseman`_]

    * Handle single-line or multiline snippets.
      [2011-03-22, `johnbintz`_]

    * If there is only one snippet choose it directly.
      [2011-03-16, `blueyed`_]

    * Add snippets file for "diff" filetype and add bang to function
      definitons, allowing for reload.
      [2011-03-06, `blueyed`_]

    * Update snipmate to handle latest supertab version.
      [2011-02-09, `ervandew`_]

    * Updated README: added contributors, instructions how to install snipMate,
      some spellchecking of my wonderfull english, added this Changelog
      [2011-02-07, `garbas`_]

    * From below mentioned merges I must specially mention `MarcWeber`_'s patch
      which brought quite a few functionalities/improvements:
        - snippets are loaded lazily.
        - snippets are no longer cached. Thus you always get the snippets you 
          just wrote to a file without reloading anything.
        - When visually selecting a snippet in a .snippets file you can press
          <cr> to replace spaces by tabs automatically in a smart way.
      Big +1 to `MarcWeber`_ for this. Important to note is that we now depend
      on `vim-addon-mw-utils`_ and `tlib`_.
      [2011-02-02, `garbas`_]

    * Merged pull requests of `MarcWeber`_, `lilydjwg`_, `henrik`_, `steveno`_,
      `asymmetric`_, `jherdman`_, `ironcamel`_, `honza`_, `jb55`_,
      `robhudson`_, `kozo2`_, `MicahElliott`_, `darkwise`_, `redpill`_,
      `thisgeek`_, `sickill`_, `pose`_,
      [2011-02-02, `garbas`_]


0.83 [2009-07-13]
-----------------

    * last release done by `Michael Sanders`_, you can find it here:
        http://www.vim.org/scripts/download_script.php?src_id=11006


How to install
==============

Unfortunatly there are many ways to how to install vim plugins. If you don't
see you prefered way of installation plugins please consider adding updating
this section.

snipate dependencies
==============
Important to note is that since version 1.0 we depend on this 2 vim plugins:
    * `vim-addon-mw-utils`_ providing the implementation for caching parsed
      .snippets files.

    * `tlib`_ for tlib#input#List which provides the excellent filterable
      list selection view (and more).


Using `VAM`_
------------

::

    Add snipmate to the names to be installed. Or use "github:name/repo" if you
    want to use a non standard upstream.

    VAM will also fetch the dependencies listed above for you automatically.

Using `pathogen`_
--------------------------------------

::

    % cd ~/.vim
    % mkdir bundle
    % cd bundle
    % git clone https://github.com/tomtom/tlib_vim.git
    % git clone https://github.com/MarcWeber/vim-addon-mw-utils.git
    % git clone git://github.com/garbas/vim-snipmate.git

Then install any dependencies (see above).

Using `Vundle`_
---------------

::

    Install dependencies:
    Bundle "git://github.com/MarcWeber/vim-addon-mw-utils.git"
    Bundle "git://github.com/tomtom/tlib_vim.git"

    Install:
    Bundle "git://github.com/garbas/snipmate.vim.git"

    And :BundleInstall



Manually
--------

::

    % git clone git://github.com/garbas/vim-snipmate.git
    % cd snipmate.vim
    % cp -R * ~/.vim

Then in vim::

    :helptags ~/.vim/doc/

Then install any dependencies (see above).

TODO / Future
=============

    * Notify all "forkers" about new home and ask them nicely to review already
      merged changes and possibly send their changes.
      [2011-02-07, `garbas`_]

    * I'd like to investigate whether xptemplate or snipmate has the better
      engine. So maybe my vision of the future could be making xptemplate read
      snippet files. It is not important enough for me to work on it right now as
      snipmate works reasonable well for me.
      [2011-02-02, `MarcWeber`_]


    * Split core from snippets. Then reviewing patches and updates will be easier?
      Snippets should be distributed in additional repositories. Eg
      snipmate-snippets-ruby
      snipmate-snippets-vim
      snipmate-snippets-....
      One repo containing snippets is:
      git://github.com/scrooloose/snipmate-snippets.git

      comment without verifying it:
      < Silex> MarcWeber: btw, check out ultisnips. Much better than snipmate imho

      And before this discussion xptemplate vs snipmate vs ultisnips .. continues
      we should create a wiki page comparing them and keep that up to date.
      If you volunteer tell me so that I can reference the link.
      [2011-02-02, `MarcWeber`_]

.. _`Michael Sanders`: http://www.vim.org/account/profile.php?user_id=16544
.. _`Rok Garbas`: rok@garbas.si
.. _`VAM`: https://github.com/MarcWeber/vim-addon-manager
.. _`pathogen`: http://www.vim.org/scripts/script.php?script_id=2332
.. _`vim-addon-mw-utils`: https://github.com/MarcWeber/vim-addon-mw-utils
.. _`tlib`: https://github.com/tomtom/tlib_vim

.. _`garbas`: https://github.com/garbas
.. _`MarcWeber`: https://github.com/MarcWeber
.. _`lilydjwg`: https://github.com/lilydjwg
.. _`henrik`: https://github.com/henrik
.. _`steveno`: https://github.com/steveno
.. _`asymmetric`: https://github.com/asymmetric
.. _`jherdman`: https://github.com/jherdman
.. _`ironcamel`: https://github.com/ironcamel
.. _`honza`: https://github.com/honza
.. _`jb55`: https://github.com/jb55
.. _`robhudson`: https://github.com/robhudson
.. _`kozo2`: https://github.com/kozo2
.. _`MicahElliott`: https://github.com/MicahElliott
.. _`darkwise`: https://github.com/darkwise
.. _`redpill`: https://github.com/redpill
.. _`thisgeek`: https://github.com/thisgeek
.. _`sickill`: https://github.com/sickill
.. _`pose`: https://github.com/pose
.. _`marutanm`: https://github.com/marutanm
.. _`r00k`: https://github.com/r00k
.. _`jbernard`: https://github.com/jbernard
.. _`holizz`: https://github.com/holizz
.. _`muffinresearch`: https://github.com/muffinresearch
.. _`statik`: https://github.com/statik
.. _`Vundle`: https://github.com/gmarik/vundle
.. _`alderz`: https://github.com/alderz
.. _`johnbintz`: https://github.com/johnbintz
.. _`thenoseman`: https://github.com/thenoseman
.. _`ervandew`: https://github.com/ervandew
.. _`blueyed`: https://github.com/blueyed
.. _`tisho`: https://github.com/tisho
