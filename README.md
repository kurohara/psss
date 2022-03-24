# psss
Post Scriptable Style Sheet: EXPERIMENTAL/MEMO -- just making clear of this idea for now.  
May SASS is enough, but even so, making such a weird tool is fun for me.  

* Stream-like creation of stylesheet.
* Want to reduce cursor movement.

```mermaid
graph LR
    stext1("psss_block: ") ---
    psss_block --- postprocsep["<"] --- postproc
    sass_block
    stext1 --- sass_block

    stext2("postproc:") --- map
    seladd
    seldel
    inner
    stext2 --- seladd
    stext2 --- seldel
    stext2 --- inner

    stext3("map:") --- maptok['map'] --- parL["("] --- regexp --- comma1[","] ---  region --- comma2[","] --- expr --- parR[")"]
    parL --- str --- comma1

    stext4("inner:") --- innertok['inner'] --- parL2["("] --- sass_block2["sass_block"] --- parR2[")"]

    linkStyle 0,3,4 stroke-width:1;
    classDef simpleText border:none,border-width:0,    background-color:white,margin-right:0px;
    classDef spacing margin-left:20px;
    class stext1 simpleText;
    class spacing1,spacing2 spacing;
```