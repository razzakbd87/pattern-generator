# Dependencies

The following software packages or tools are required, in addition to
those installed by the Haskell `stack` tool from hackage:

1. pandoc-filters (from https://github.com/jnoll/pandoc-filters).
   This is a set of tools for manipulating the Pandoc AST before
   generating the output.  The pattern generator uses the `makeTable` function to
   generate the "Implementation details" table.
2. pml-bnfc (from https://bitbucket.org/jhnoll/pml-bnfc). This is a
   fork of Andrew Butterfield's pml-bnfc parser suite for PML; it
   fixes a small incompatibility with current versions of GHC.
3. pml-graphit (from https://github.com/jnoll/pml-graphit).  This
   program generates UML "activity" diagrams from PML programs.
4. plantuml (from http://plantuml.com).  This does the actual
   rendering of process diagrams into png format.

Of these, only _plantuml_ needs to be installed manually; the others
will be automatically installed by `stack`.

# Installing

1. Download _plantuml.jar_ from http://plantuml.com/download

2. Install the Haskell `stack` tool.  On Ubuntu, this can be done with
   `apt-get`:

        sudo apt-get install haskell-stack

3. If you installed `stack` using `apt-get`, upgrade to the latest
   version.  
   
        stack install stack
    
    This will take some time, so be sure you have a reliable internet
connection and about 10 minutes.


5. Build the pattern generator tools using `stack`:

        stack build
        stack install
    
    This will also take some time as all of the above packages need to
be built, along with Pandoc which has a lot of dependencies.  Again,
ensure your internet connection is reliable and plan on about half an
hour to finish the whole process.

