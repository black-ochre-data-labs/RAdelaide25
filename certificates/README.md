# Certificates

- Participant names should be provided in the csv `certNames.csv`, with columns `Name`,`position`,`institution`,`nbrOfDays`
- The main `tex` document `certificates_RAdelaide25.tex` can then be run using `pdflatex` to generate the certificates.
- This file is then tidies up using ghostscript
- Final pdfs are formed using `pdfseparate` to split by page

The complete set of commands is

```bash
F="certificates_RAdelaide25"
pdflatex ${F}.tex
gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dNOPAUSE -dQUIET -dBATCH -sOutputFile=cert-compressed.pdf ${F}.pdf
pdfseparate cert-compressed.pdf cert-%d.pdf
rm cert-compressed.pdf
rm ${F}.aux ${F}.log ${F}.fls ${F}.fdb_latexmk
```

Files were then renamed in R using

```r
library(tidyverse)
certNames <- read_csv("certNames.csv") |>
	mutate(
		pdf = paste0("cert-", row_number(), ".pdf"),
		Name = Name |> str_replace_all("([:alnum:]+).*", "\\1.pdf")
	)
for (i in 1:20) file.rename(certNames$pdf[[i]], certNames$Name[[i]])
```