---
editor_options: 
  markdown: 
    wrap: 72
---

# `codeblitz001`: Get to know your new labmate, `Github`

## Background

In the Landscape Ecology Lab, we study disturbance, forest dynamics,
integrating field work and remote sensing. Much of this work involves
coding, analyzing large datasets, developing reproducible workflows, and
building methods that can be shared across projects. Coding is often
learned and practiced in isolation. Our **Code Blitzes** create a space
to code together, so we can sharpen skills, solve problems as a team,
and strengthen the collaborative spirit of our lab.

-   Provide training in collaborative coding skills in `R` and GitHub
    that improve reproducibility and teamwork across lab projects.

-   Strengthen our lab network by creating shared experiences for junior
    and senior members.

-   Advance research capacity in disturbance ecology, LiDAR, and remote
    sensing through shared tools, workflows, and problem-solving.

In this first Code Blitz, we’ll focus on getting everyone set up and
making their first contributions in GitHub. By the end of the session,
each lab member will have contributed to a shared project that forms the
foundation of a collaborative website.

<img src="img/codeblitz-photo.png" width="300"/></img>

**AI generated image depecting what our group is up to today. Aren't we
a handsome group?**

## Learning objectives:

For this code blitz, we'll each contribute portions of a lab website
that features our favorite field sites. But you can also do you favorite
vacation, hiking spot, etc. By the end of the blitz, you will

-   get to know new folks in the lab
-   get comfortable with collaborative contributions using Github and R
-   get comfortable learning syntax for a new coding language

Specifically we will

1.  Create GitHub accounts and install the necessary tools.
2.  Practice the basic workflow: branch, clone, edit, commit, and push.
3.  Contribute text using Markdown to build a shared lab website.

## Pre-Work

Prior to our first meeting, please complete the following tasks:

1.  [Setup a Github account](https://github.com/signup). Note that you
    may have to verify your account and possibly setup a
    dual-authentication. You can actually do this in your DUO app that
    you use for Jones Center authentication

2.  Make sure you have `RGUI` and `Rstudio` installed on your computer.
    You can find some instructions
    [here](https://rpubs.com/premisa/714217).

3.  install `gitbash` on your computer. In Windows open the Command
    Prompt by clicking start and typing `cmd`. When the command prompt
    is open type `winget install --id Git.Git -e --source winget`

## Assigned teams

We'll all complete the work, but let's still work in groups so that you
have a go-to team to ask questions. We will create Teams Rooms for you
to meet privately, share code, and answer questions. Go to your team
first to ask questions. If the issue persists, bring it to the larger
group.

| Team name | Room Name | Person 1 | Person 2 | Person 3    | Person 4  |
|:----------|:----------|:---------|:---------|:------------|:----------|
| Ferns     | Room 1    | Jeff     | Leah     | Latonya     | Jingting? |
| Saplings  | Room 2    | Khanh    | Tanner   | Carly       | Nathan    |
| Rhizomes  | Room 3    | Nicole   | Morne    | Ramp Fellow | Lain      |

## Instructions Part 1:

For this code blitz, we'll each contribute portions of a lab website
that features our favorite field sites. But you can also do you favorite
vacation, hiking spot, etc. By the end of the blitz, you will

The instructions are intentionally vague as this is the first time
trying this! We'll try to answer specific questions in person but you
should

1.  Create a new **branch** with your name (e.g., `jeff-profile`)
2.  **Clone** the code blitz repository and Open the template assigned
    for you
3.  Edit the assigned markdown (`.md`) document to make a profile.
4.  Make a profile of your **favorite field site**, vacation spot, or
    hiking trail. The important part is that its a real place that you
    know well and possibly have photos of. But this is all just
    practice, so whatever you want is fine. Could be imaginary I
    suppose.
5.  **Using the Markdown language**, fill in the fill in the requested
    information about your selected site. You'll need to insert photos,
    captions, format text, links, bullets etc. See here for a [Markdown
    Syntax Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)
6.  You will see a template website where you'll fill out the following
    sections. Each section denotes header levels for your profile. Fill
    out each section, using markdown syntax to add complexity
    complexity.
7.  [**You will include some some false information and errors in your
    profile.**]{style="color:red"} This is so that we can
    collaboratively edit later!
8.  When you are finished, be sure to **Commit the changes to your
    branch**
9.  Open a pull request from your branch to `main` which we will merge
10. Once merged, your profile will appear here:
    <https://landeco-jonesctr.github.io/codeblitz1/>

```         
# Name
## Biography
## Favorite field site
## Photo gallery
## Resources
## Map of field site
```

### `# Name`

Your name, duh, note the **Header level 1**, indicated by a single `#`

### `## Biography`

-   Note the **Header level 2** indicated by the double `##`.
-   Write a short 100 word biography about yourself, background, and
    hobbies.
-   Insert a photo you may have to upload it to the `img/` directory or
    link directly from a webpage. Specify a caption and adjust the size
    of the image
-   [Insert one *obviously false* statement about you in the
    biography]{style="color:red"}.

## `## Favorite field site`

-   Write a brief description of your site including location, features,
    and other information.
-   Include a **bulleted list** pertaining to your site. It could be a
    list of things to do there, features that you like, or a list of
    your favorite plants located there.
-   [Insert typo in your list for a partner to fix]{style="color:red"}.

## `## Photo gallery`

-   Insert 2-3 photos representative of your field site. They could be a
    representative plant or a photo from your visit.
-   Be sure to include a descriptive caption in each one
-   [Add a typo in one image path so that the link is
    broken.]{style="color:red"} Bonus: Make one of the photos a
    thumbnail with a hyperlink!

## `## Resources`

-   Add three references or links to a resource related to your selected
    field site. It may be a field guide, map, article, or data source.
-   Make sure they contain a hyperlink to an outside webpage

## `## Code`

-   Embed a chunk of `R` code that creates a map of your field site.

```{{r warning=FALSE}}
library(leaflet)
leaflet() %>% 
  addTiles() %>%     
  addMarkers(lng = -71.297210, lat = 44.055972, popup = "Barlett Experimental Forest")
```

-   Include a function in R that calculates tree basal area from a
    vector of tree dbh's from your site. The function should be able to
    -   Deal with missing dbh values
    -   work for multiple plot sizes

```         
dbh = c(35, 23, 12, NA, 8) # in cm
plot_area = 0.1 #in ha
```

-   To display a chunk of `R` code, you can use the following format,
    offset by three backticks ```` ``` ````

```{{r}}
myFunction = function(dbh, plot_area) {
 #my code
 return(basal_area)
}
```

## Instructions -- Homework Part 2:

**Within one week of today's exercise** complete the followign tasks
with an assigned partner.

Now that you’ve practiced committing to your own branch, we will try a
common workflow: **pull requests** (PRs). A pull request is how you
propose changes to a shared repository so others can review and approve
them before merging back into the main branch.

-   Fork the repository, and clone your fork, make a new branch
-   Correct the false information in your partners `Biography`
-   Correct the typo in your partners bulleted list in
    `Favorite field site`
-   Correct the broken link in the `Photo gallery`.
-   Commit your changes and push the repo back to Github
-   Test their `R` code for basal area in a separate window. Does it
    work for you? If not, suggest an edit
-   Open a pull request. Go to your fork on GitHub. You’ll see a banner
    prompting you to “Compare & pull request.” Click it. Write a short
    description of your change and submit the PR back to the main lab
    repo.
-   Review someone elses PR. Go to the lab repo \> Pull Requests tab.
    Review your partners PR to your profile, read it, and leave a short
    comment.
