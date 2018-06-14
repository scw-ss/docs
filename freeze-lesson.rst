#####################################
How to "freeze" an official SC lesson
#####################################

As the workshop gets closer we want to have a "frozen" reference to the lesson
so that we can be sure that no big changes happen between owr workshop
preparation and the workshop itself.

We should not fork the repository directly in the ``scw-ss`` github organization as
github only allows forking a repo once, thus this will only work the first time
we do it. Instead we create a completely independent repository from an existing one.

Let's do it with Software Carpentry git-novice lesson. We will clone the repo ``http://swcarpentry.github.io/git-novice`` to ``https://github.com/scw-ss/2018-06-27-cfmehu-git-novice`` in the github ``scw-ss`` organization account. For this::


1.- In github, create the desired target repo ``iamc/2018-06-27-cfmehu-git-novice``

2.- Clone the desired original repo locally, with the ``--bare`` option, and only the
``gh-pages`` branch (``-b gh-pages --single-brach``)::

    cd tmp
    git clone --bare -b gh-pages --single-branch git@github.com:swcarpentry/git-novice.git

3.- cd into the cloned repo and push ``--mirror``::

    cd git-novice.git
    git push --mirror git@github.com:scw-ss/2018-06-27-cfmehu-git-novice.git

4.- In case you cloned all branches, remove unwanted branches if needed in the github interface and set default branch to eg. ``gh-pages``.

5.- Remove the cloned bare original repo and clone your new one::

    cd ..
    rm -rf shell-novice.git
    git clone git@github.com:scw-ss/2018-06-27-cfmehu-git-novice.git



