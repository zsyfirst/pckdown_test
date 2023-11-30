# Newpckdown

install.packages(c("usethis", "pkgdown"))

# Run once to configure package to use pkgdown
```r
usethis::use_pkgdown() 
```

# Run to build the website 
```r
pkgdown::build_site()
```

If you're using GitHub, we also recommend setting up GitHub actions to automatically build and publish your site:

``` r
usethis::use_github()

usethis::use_pkgdown_github_pages()
```

pkgdown can automatically generate a website of an R package, containing references to the enclosed function, different vignettes if exists, within two lines of code (slight exaggeration). It also helps to deploy the website to GitHub server. Amazingly, pkgdown facilitates automatic updates of the website following any changes made to the package that are pushed to GitHub.
```r
pkgdown::deploy_to_branch()
```
```r
usethis::use_github_action("pkgdown")
```

# walkthrough
While the pkgdown website provides a comprehensive walkthrough for those who set up their GitHub access 

If you run into problem when running usethis::use_pkgdown_github_pages() and get stuck, you should try to understand what the function does by reading its manual ?usethis::use_pkgdown_github_pages().

Is it possible to create the necessary gh_pages using pkgdown::deploy_to_branch()? Don’t forget to set up the GitHub Action by calling usethis::use_github_action("pkgdown"). Now you should be able to find access your website via github_account_name.github.io/pkg_name



