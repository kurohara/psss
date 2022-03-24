# psss
post scriptable style sheet: EXPERIMENTAL/MEMO, not for use

```mermaid
graph LR
    stext1["psss_block = "] -->
    psss_block --- postprocsep["<"] --- postproc
    spacing1[" | "] --- sass
    spacing2[" | "] --- css

    linkStyle 0,3,4 stroke-width:0;
    classDef simpleText border:none,border-width:0,    background-color:white,margin-right:0px;
    classDef spacing margin-left:20px;
    class stext1,spacing1,spacing2 simpleText;
    class spacing1,spacing2 spacing;
```