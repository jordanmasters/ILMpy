argument_parser.py
========================================


Quickstart 
-----------------------

* Python 2 & 3 compatibility
* **Execute python code** in the chunks and **capture** input and output to a report.


Init ILM object::

    >>> p = ILM_Parser(debug=1)

small lattices::

    >>> args = '[a-z]^2 (4)^2'                              
    >>> (signal_space,meaning_space) = p.parse(args)

unordered (set-like) meaning-spaces::

    >>> args = '[a-g]^3 {3}.(4).(2)'                        
    >>> (signal_space,meaning_space) = p.parse(args)

noiserates::

    >>> args = '([b-d]:0.01).[aeiou] (3).(4)'               
    >>> (signal_space,meaning_space) = p.parse(args)

noiserates can go any sound-space::

    >>> args = '(([a-z]\[aeiou]):0.05).[aeiou] (4).(2)^2'   
    >>> (signal_space,meaning_space) = p.parse(args)

generalizable transformation sound-space::

    >>> args = '(a|A).[bc] (2)^2'                           
    >>> (signal_space,meaning_space) = p.parse(args)

transformation sound-space with noise::

    >>> args = '((aeiou|AEIOU):0.01)^2 {2}^2'               
    >>> (signal_space,meaning_space) = p.parse(args)
     
set-complements::

    >>> args = '([a-g]\[aeiou])^2.(aeiou|AEIOU).(bd|pt) (8).(5)' 
    >>> (signal_space,meaning_space) = p.parse(args)

with noise and powered::

    >>> args = '(([a-g]\[aeiou]):0.1)^2 {256}.(2)'            
    >>> (signal_space,meaning_space) = p.parse(args)



  Pweave markdown document in Atom together with output. Atom support using ``language-weave``-package.

.. note::

   Report bugs on `Github <https://github.com/mpastell/Pweave>`_.
   Post your questions and comments to `Pweave <https://groups.google.com/forum/?fromgroups=#!forum/pweave>`_
   google group.


Training Models
-----------------------

Rhymetrix can be installed through the github::

  git clone https://bitbucket.org/verbaleyes/rhymetrix  


Run this and init::

  run.py < thing.txt 


Making Predictions
-----------------------

Browse `documentation <index.html>`_ or go straight to an `examples <examples/index.html>`_

