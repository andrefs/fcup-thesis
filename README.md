# FCUP thesis layout 

Latex version of the thesis layout available at [http://sigarra.up.pt/fcup](https://sigarra.up.pt/fcup/pt/web_base.gera_pagina?p_pagina=*admiss%c3%a3o%20a%20provas%20acad%c3%a9micas).

Layout rights go to Faculdade de Ciências da Universidade do Porto. Arial font rights go to Microsoft.


## Requisites and Compiling

The recommended Latex distribuition is [**TeXLive 2016**](https://www.tug.org/texlive/windows.html) (Windows/Ubuntu). You can it on the macOS by downloading **MacTeX** in [**here**](https://www.tug.org/texlive/windows.html).

For the Arial font and all packages to work, **_main.tex_** must be executed with `xelatex`. 

After making the proper modifications to the file **_vars.tex_**, you must run
```
xelatex -interaction=nonstopmode -file-line-error -pdf main
```
in the workspace root to generate the output pdf. Compilation may take a few seconds.


## Contents

The project itself is simplified such that there are two .tex files:
1. **_Title Page:_** Includes all relevant thesis information (with hyperlinks). To be included in the final thesis as the 1st page.
2. **_Examiner Page:_** Page with for the examiner to sign and make the necessary comments. To be included in the final thesis as the 2st page.
3. **_Disk Template:_** Printing template for disk.
4. **_Disk Cases:_** Front/back cover of the disk case.
5. **_Book Cover:_** Special page to be printed when assembling a booklet version of the thesis. Spine width is adjustable.


## File organization

The project itself is simplified such that there are two .tex files:
- **_main.tex:_** contains all the definitions, structuring and layouts/metrics of the document
- **_vars.tex:_** contains all information about the thesis type, title, author, ...
- **_fonts:_** contains all the Arial fonts used to render text
- **_logos:_** relevant university logos, including Universidade do Porto (UP), Universidade do Aveiro (UA) e Universidade do Minho (UM)
- **_msc:_** mandatory vector graphics for `msc` thesis type
- **_phd:_** mandatory vector graphics for `phd` thesis type


## Customizable parameters in **_vars.tex_**

### `\thesistype{arg1}` 

- **arg1:**  `msc` | `phd`

Change the layout between PhD (Doctor of Philosophy) and MSc (Master of Science)


### `\spinewidth{arg1}` 

- **arg1:** _title of the thesis for the front page_ (default: 15mm, minimum: 8mm)

Allows to change the width of the spine of the book cover


### `\fronttitle{arg1}` and `\spinetitle{arg1}` 

- **arg1:**  _title of the thesis for the front page/book spine_

This allows to change the titles used in the document


### `\authorname[href]{arg1}` 

- **href:** _hyperlink used on the author field_ (optional)
- **arg1:** _name of the author_

Changes the author name. For the **href** can be used a website of a mail, using `mailto:mail@univ.edu` as hyperlink.
The **href** argument is optional, i.e. can be used `\authorname{arg1}` as well.

### `\otheraffiliation[href]{arg1}{arg2}{agr3}` and `\extraaffiliation[href]{arg1}{arg2}{agr3}`

- **href:** _hyperlink used on the University2/University3 field_ (optional)
- **arg1:** _relative path to the logo of the University2/University3_
- **arg2:** _initials of the University2/University3_
- **arg3:** _fullname of the University2/University3_

Sets up the pages to incorporate fullname/logo/initials for the University2/University3 field.
The **href** argument is optional, i.e. can be used `\otheraffiliation{arg1}{arg2}{agr3}` as well.

### `\degreename{arg1}` 

- **arg1:** _fullname of the degree_

### `\degreename{arg1}` 

- **arg1:** _name of the scientific area of the thesis_

### `\supervisor[href]{arg1}` and `\cosupervisor[href]{arg1}`

- **href:** _hyperlink used on the supervisor/cosupervisor field_ (optional)
- **arg1:** _name of the supervisor/cosupervisor_

Commenting the `\cosupervisor` field hides the field in the titlepage

### `\supervisorposition{arg1}` and `\cosupervisorposition{agr1}`

- **arg1:** _position of the supervisor/cosupervisor_

This fields can be commented out separately.

### `\supervisoraffiliation[href]{arg1}` and `\cosupervisoraffiliation[href]{arg1}`

- **href:** _hyperlink used on the supervisor/cosupervisor affiliation university_ (optional)
- **arg1:** _name of the supervisor/cosupervisor university_