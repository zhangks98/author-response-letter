# Author Response Letters
Latex template to quickly write author response letters to review comments. 

Based on @mschroen's [review_response_letter](https://github.com/mschroen/review_response_letter). 

## Example
Use the example `Einstein1905.tex`. Please ensure the class file `ar2rc.cls` is in the same directory.

<img alt="Screenshot of the output PDF of a Author Response Letter to Review Comments" src="https://cloud.githubusercontent.com/assets/7942719/26349939/c9889c00-3fb1-11e7-91c6-908012e2797e.png" style="max-width: 100%" />

```  
\section{Reviewer 1}
\subsection{Page 4 Line 15}
\RC Paragraph on how I do not like the paper.
\AR Thank you, we changed the text as suggested.
begin{quote} The cat in the box is \DIFdelbegin \DIFdel{dead}\DIFdelend \DIFaddbegin \DIFadd{alive}\DIFaddend . \end{quote}
```

Then run `pdflatex myletter.tex` to make `myletter.pdf`, or typeset with any TeX front-end program.

## Changelog
- Created the document class `ar2rc` to allow additional preambles in the main document.
- Non-labeled paragraphs for author response does not require additional `\AR*`.
- Use [mdframed](https://ctan.org/pkg/mdframed) instead of [framed](https://ctan.org/pkg/framed), and support breakable text boxes for quotes.
- Easier syntax to make title.

## Additional features

- supports latexdiff commands
- supports text highlighting with `\hl{}`
- supports tables and figures,
- supports non-labeled paragraphs for reviewer comments, starting with `\RC*` instead of `\RC`.

