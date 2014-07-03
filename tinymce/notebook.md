####Notes on getting RDFaCe to work with patterns and bioontologies
===============


20140703

OK

Kick-off.
First to change the contents of the right-click "context" menu.
Find out how this is populated, and replace with say OBI.
This might be eaisiest if we have a local copy of OBI in JSON or whatever RDFaCE looks for/parses....

####NOTE: It would seem the current version of RDFaCE has schema.org hardcoded as the only declared namespace in the HTML...

OK plugin.min.js in RDFaCE, line 319 is where the right-click context menu is called.
It is preceeded by a jQuery function that loads the selection.json that populates the context menu.

SO the plan is to hijack the right click to do two things. Load in a local version of the pattern Ontology, or grab the text and submit to the NCBO annotator, return a selection, and then insert the selection.

