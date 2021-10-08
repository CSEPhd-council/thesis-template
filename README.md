# PhD/Lic Thesis Template at CSE

## Disclaimer
This is a short introduction to the PhD/Lic thesis template provided by the PhD council at CSE.
Please read this document carefully, as to avoid any annoying mistakes in your final, printed thesis!
As a PhD council, we provide this template as is.
While we try to keep it in sync with changes in the central layout instructions, there is no guarantee.


## Template Information
There are a number of layout decisions made in the template.
These can be adjusted, but again require your own LaTeX skills.
These decisions are:

- There is one single bibliography for the entire thesis.
- All appendices are located in the end of the thesis.


## Project Structure
The template contains of a number of files and folders.
Roughly, the structure is as follows:
- main.tex - the main file for your thesis is included in the root folder. In particular, it includes a number of important macros in the beginning (e.g., a flag defining whether it's a PhD or a Lic thesis, your thesis title, the year, division). From here, you can also easily see which other files are included and in which order.
- The inlet (inlaga.tex) and the errata (errata.tex) main files are also included in the root. You do need the inlet (as a loose paper in your thesis and as a PDF to announce the defence). Whether or not you need an errata is to some extent up to you, and also depends on how many and how critical errors you discover after printing.
- The single bibtex (bibliography) file is located in the root level folder as well. If you would like to change to multiple bibliographies in your thesis, you might have to modify this.
- TexFiles contains all other tex files. These are:
    - abstract.tex - the abstract of your thesis.
    - acknowledgment.tex - the acknowledgements.
    - appendedPapers.tex - the tex file that references all your papers included in the thesis. Each paper is structured into an abstract file (e.g., Chapter1_abstract.tex) and the remainder of the paper (e.g., Chapter1.tex).
    - contribution.tex - an explanation of your contributions to each included paper.
    - dedication.tex - dedication/smart quote at the beginning of your thesis.
    - firstpage.tex - the first two pages of your thesis. All the relevant information (e.g., author name, year, title) is set in the main.tex file. So it should not be necessary to touch this file unless it is out of sync with the layout instructions.
    - introduction.tex - the kappa (introduction chapter).
    - listPub.tex - the list of all publications, both included and others. It only contains a list, the actual links to the tex files of the included papers is in appendedPapers.tex.
    - settings.tex - includes, macros, etc. Modify if you need any additional packages, macros or other things that you don't want to clutter the main file with.
- All figures used in the front pages are located in Fig.
- All figures used in the kappa and the included papers are located in figures.

This structure can easily be adapted to personal preferences.

The reason to use subfolders for each paper and the figures included in those papers is that makes it quick and easy to replace individual papers (and new versions of those papers in case you want to include a new journal revision).


## Layout
The current layout is in sync with the Chalmers and GU layout instructions as of March 2018.

However, these tend to change and we cannot guarantee that we will always react on time (or even know about it).

Therefore, it is absolutely essential that you check those instructions!


## Authors
- Grischa Liebel
- Emil Alégroth
- Robert Feldt

### Acknowledgement note from the authors
While the current version of this template has been prepared by Grischa Liebel, the template has in a similar form been circulating in the CSE department for a while.

Grischa originally received the template from Emil Alégroth. At that point, it also included some work from Robert Feldt (either only the Rakefile, or the entire template - we don't know).

This is sadly where the trace ends.
However, we would like to acknowledge the original author(s) of this template, whoever they may be!


## Contributing

// TODO


## Version Notes
- 8th October 2021 (Linda) - updated mentions of the universities to use both on the same form (Chalmers universtity of technology | University of Gothenburg), changed use of one logo, commented out tech report number from lic template since it's not used anymore. 
- 18th April 2018 (Grischa) - Added the tech report number also for PhD theses.
- 16th April 2018 (Grischa) - Fixed the ISBN. Now the template follows the current layout instructions for both PhD and Lic.
- 13th March 2018 (Grischa) - Cleaned up the template and wrote these instructions. Both the inlet and the errata should be revisited. Also, the second page (part of firstpage.tex) does not yet include the ISBN needed for PhD theses. For Lic it's fine!
