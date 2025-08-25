# PhD/Lic Thesis Template at CSE

## Disclaimer
This is a short introduction to the PhD/Lic thesis template provided by the PhD council at CSE.
Please read this document carefully, as to avoid any annoying mistakes in your final, printed thesis!

As a PhD council, we provide this template as is.

While we try to keep it in sync with changes in the central layout instructions, there is no guarantee.

The current layout should be in sync with the Chalmers and GU layout instructions as of March 2022.

However, these tend to change and we cannot guarantee that we will always react on time (or even know about it).

**Therefore, it is absolutely essential that you check those instructions!**


## Building

The current version of this template has been verified to work with `pdflatex` and `bibtex`, but may work with other setups with minimal changes.

To build the thesis itself you can use the following commands

```
pdflatex -file-line-error -output-directory=build -aux-directory=build -synctex=1 main.tex
```

And for the bibliography

```
bibtex build/main -include-directory=build
```

As usual, to get latex to propagate the bibliography and page numbers everywhere you need to do the 4 calls:

```
pdflatex ...
bibtex ...
pdflatex ...
pdflatex ...
```

The same commands can be used for the `inlaga` and `errata` files, changing the `main` in the command for the corresponding one.

In the historic of the repository there is a rakefile that might help automate this. It's been removed from the current version because it was not kept up to date and had code specific to the original user.

## Project Structure
The template contains of a number of files and folders.
Roughly, the structure is as follows:

- `main.tex` - the main file for your thesis is included in the root folder. In particular, it includes a number of important macros in the beginning (e.g., a flag defining whether it's a PhD or a Lic thesis, your thesis title, the year, division). From here, you can also easily see which other files are included and in which order.
- The presentation page (`inlaga.tex`) and the errata (`errata.tex`) main files are also included in the root. You do need the inlet (as a loose paper in your thesis and as a PDF to announce the defence). Whether or not you need an errata is to some extent up to you, and also depends on how many and how critical errors you discover after printing.
- The single bibtex (bibliography) file is located in the root level folder as well. If you would like to change to multiple bibliographies in your thesis, you might have to modify this.
- `TexFiles/` contains all other tex files. These are:
    - `settings.tex` - General information about your thesis (title, author name, etc). Also includes, macros, etc. Modify if you need any additional packages, macros or other things that you don't want to clutter the main file with.
    - `firstpage.tex` - the first two pages of your thesis. All the relevant information (e.g., author name, year, title) is set in the settings.tex file. So it should not be necessary to touch this file unless it is out of sync with the layout instructions.
    - `dedication.tex` - dedication/smart quote at the beginning of your thesis.
    - `abstract.tex` - the abstract of your thesis.
    - `publicationsList.tex` - the list of all publications, both included and others. It only contains a list, the actual included papers are in appendedPapers.tex.
    - `acknowledgment.tex` - the acknowledgments.
    - `summary.tex` - the kappa (introduction chapter).
    - `appendedPapers.tex` - this includes the actual papers to be used
- `figures` contains the logos used in the presentation page.
- `papers` contains the tex files of the included papers and their figures. You should change this with your own files, and edit appendedPapers.tex to include those instead.

This structure can easily be adapted to personal preferences.


## Template Information
There are a number of layout decisions made in the template.
These can be adjusted, but again require your own LaTeX skills.

## Authors
- Emil Alégroth
- Robert Feldt
- Grischa Liebel
- Linda Erlenhov
- Roc R. Currius

### Acknowledgment note from the authors

This template has in a similar form been circulating in the CSE department for a while. Grischa originally received the template from Emil Alégroth. At that point, it also included some work from Robert Feldt. Now it's kept up-to-date by members of the PhD students council.

This is sadly where the trace ends.
However, we would like to acknowledge the original author(s) of this template, whoever they may be, so if you substantially contributed to it, let us know.


## Contributing

If you find errors with the layout of the template, please let us know so it can be updated. If you give us a list of the issues you found, it will make our lifes much easier.

You can either submit an issue here in the repo, or send us an email at the council mail `phdcouncil.cse at chalmers`.

If have some proposals for changes that might make things easier for new people to use the template, we will try to keep track of pull requests and make the proposed changes when we have time for it.

Thank you deeply for your contributions.


## Version Notes
- 21st March 2022 (Roc) - Fixed template to match the latest directives from Chalmers from April 2020. Also some design changes, and a *lot* of changes on the latex structure to try to simplify use.
- 8th October 2021 (Linda) - updated mentions of the universities to use both on the same form (Chalmers universtity of technology | University of Gothenburg), changed use of one logo, commented out tech report number from lic template since it's not used anymore.
- 18th April 2018 (Grischa) - Added the tech report number also for PhD theses.
- 16th April 2018 (Grischa) - Fixed the ISBN. Now the template follows the current layout instructions for both PhD and Lic.
- 13th March 2018 (Grischa) - Cleaned up the template and wrote these instructions. Both the inlet and the errata should be revisited. Also, the second page (part of firstpage.tex) does not yet include the ISBN needed for PhD theses. For Lic it's fine!
