# Coding

Share thoughts, resources and tips on how best to code for research.

<img src="/images/Coding.png" width="600">

> Any researcher who wishes to become proficient at doing ... analysis must learn to code well and easily. The excellence of the research rests in large part on the excellence of the coding. (Anselm L. Strauss, Qualitative Analysis for Social Scientists, 1987, p. 27)

## Style guide
> Good style is important because while your code only has one author, it’ll usually have multiple readers. This is especially true when you’re writing code with others. In that case, it’s a good idea to agree on a common style up-front. Since no style is strictly better than another, working with others may mean that you’ll need to sacrifice some preferred aspects of your style. [*Advanced R*](http://adv-r.had.co.nz/Style.html) by Hadley Wickham

### R style guide
Use Hadley Wickham's [style guide](http://adv-r.had.co.nz/Style.html), the same guide that is used at RStudio and the Tidyverse packages. It almost the same at Google's [R style guide](https://google.github.io/styleguide/Rguide.xml).

[formatR](https://yihui.name/formatr/) and/or [styler](http://styler.r-lib.org) packages makes it easy to clean up poorly styled code. 

[lintR](https://github.com/jimhester/lintr) shows you where you code isn't following (Hadley's) style guide. 

These packages can all be modified, so speak up if there is particlar styling that doesn't make sense to you. We can make modifications for our team.

### SAS style guide
Is there a SAS style guide that is used at ICES? Let's use it -- if there is one.

## Documenation

**What nobody tells you about (code) documentation** from [Divo.com](https://www.divio.com/blog/documentation/)

> **The secret:**
> Documentation needs to include and be structured around its four different functions: tutorials, how-to guides, explanation and technical reference. Each of them requires a distinct mode of writing. People working with software need these four different kinds of documentation at different times, in different circumstances - so software usually needs them all.

# File name versioning
Semantic versioning. See http://semver.org/ One adaptation are tags for each algorithm. Use a suffix with the algorthim abbreviation. (e.g. v1.0.0-MPoRT). Really each algorithm is a descrete package or library that isn't dependant on others. At time of publication, we should have v1.0.0 or higher. However, other algorithms may be farther along that v1.0.0. Meaning is is fine to have MPoRT at v1.2.0 and then publish CVDPoRT v1.0.0. Just having v1.0.0 won't work well with a single GitHub repository. We need v1.0.0-MPoRT v1.0.0-CVDPoRT, etc. 

Use tags for major and minor version (either X or Y where versioning is x.y.z). See https://git-scm.com/book/en/v2/Git-Basics-Tagging

*Minor version (Y)* is used when changes need to be made for both PMML and LIME to correctly execute. 
*Patch version (Z)* can be used for PMML or LIME, but not necessarily both. Meaning it is OK to update PMML from v1.0.5 to v1.0.6, but not update LIME (e.g. leave LIME as v1.0.0).

# References

Wilson G, Aruliah DA, Brown CT, Chue Hong NP, Davis M, Guy RT, et al. Best practices for scientific computing. [PLoS Biol](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.1001745). 2014;12(1):e1001745.

How to document your code. [Divio Blog](https://www.divio.com/blog/documentation/)
