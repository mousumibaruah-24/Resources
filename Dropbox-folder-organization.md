* ``/admin`` - for project related expenses/receipts/invoices, progress reports, etc.

* ``/analysis`` - the most important folder. It that will be used for the data analysis
  - ``/analysis/input`` - there is no such folder. the final cleaned data used for analysis should be saved in ``build/output`` 
  - ``/analysis/code`` - has the stata code to build and analyse the data
  - ``/analysis/output`` - files generated during the analysis can be saved here 
  - ``/analysis/temp`` - consists of intermediate or transition datasets that are constructed in the process of data analysis

* ``/build`` - use to prepare the dataset for analysis
  - ``/build/input`` - all the raw data is saved here. note: do not overwrite the raw data
  - ``/build/code`` - the do files that clean the data and generate variables for analysis are saved here
  - ``/build/output`` - the final output .dta file that will be used for analysis is saved here
  - ``/build/temp`` - all intermediate files created in the process of going from "input" to "output" are saved here. 

* ``/maps`` - for shapefiles, ArcMap documents etc. 

* ``/lit`` - for literature review, primarily academic papers, but may also include government reports, legal orders etc. This folder will be made redundant once we switch to [Paperpile](https://paperpile.com/)

* ``/notes`` - document minutes of meetings, agenda for Skype calls and internal communication. Use [GitHub-flavored Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) to write these

* ``/paper`` - save working drafts of papers and presentations here
  - ``/paper/tables`` - .tex tables go here 
  - ``/paper/figures`` - figures go here 

* ``/proposal`` - use for saving proposal, grant applications etc. 

* ``/overleaf`` -- use for overleaf files