# Development Log

## July 22, 2026

- Created GitHub repository
- Published first GitHub Pages website
- Designed homepage layout
- Established color palette
- Added hero section
- Added reflection cards
- Added quote section
- Added footer

---

## July 27, 2026

- Created About page
- Reorganized About page content
- Added profile image section
- Added "The Story Behind the Name"
- Added "What You'll Find Here" cards
- Added favorite scripture section
- Added closing invitation
- Styled About page
- Added responsive About layout

## Current Development Progress

Tender Mercies has moved from an initial homepage concept into a functional personal blog with a working publishing structure.

### Completed

* Built the main homepage with the Tender Mercies visual identity.
* Created a responsive header and navigation system.
* Added the About page.
* Created a Reflections archive page (`blog.html`).
* Created the first full reflection page:

  * **What Am I Willing to Leave Behind?**
* Connected the homepage and archive page to the first published reflection.
* Added a custom reflection image and responsive card styling.
* Added a reusable long-form blog post layout.
* Created reflection-question styling for intentional pauses in articles.
* Added a reusable weekly invitation section at the end of reflections.
* Added a consistent full footer across the website.
* Updated navigation and internal links across all pages.
* Removed dead placeholder links.
* Tested the website on desktop and mobile.
* Enabled GitHub Pages for public viewing.

### Current Site Structure

```text
Israel-Lopez/
├── index.html
├── about.html
├── blog.html
├── posts/
│   └── what-am-i-willing-to-leave-behind.html
├── images/
└── styles/
    └── styles.css
```

### Next Development Priorities

The next phase will focus on improving the publishing workflow and adding new content rather than rebuilding the existing layout.

Possible next steps include:

* Publish additional reflections.
* Replace remaining placeholder reflection cards with real posts.
* Add functional category filtering to the Reflections page.
* Add a newsletter subscription system.
* Continue improving accessibility and responsive behavior.
* Consider adding Books and Contact pages later.

## Weekly Publishing Checklist

Use this process whenever a new Tender Mercies reflection is published.

### 1. Prepare the reflection

- Finalize the title.
- Finalize the reflection text.
- Choose the category:
  - Faith
  - Life
  - Family
- Estimate the reading time.
- Write a short card description.
- Write the SEO/social description.

### 2. Create the featured image

- Create or choose the post image.
- Save it inside:

```text
images/ faith-anchored.png (this is an example on how to file a img file)

add the following as part of the create a new post, in the post.js

{
    title: "POST TITLE",
    date: "Month Day, Year",
    dateValue: "YYYY-MM-DD",
    category: "Faith",
    readTime: "8 min read",
    image: "images/post-image.png",
    alt: "Image description",
    url: "posts/post-filename.html",
    description:
        "Short description for the homepage and reflections archive."
}

Use the real publication date in dateValue.
The site will then automatically:
sort reflections by date;
show the newest 3 on the homepage;
add the post to the full Reflections archive;
include it in the correct category filter;
update the homepage Read the latest reflection button.
5. Test locally
Open the site with Live Server and check:
Home shows the newest reflection first.
Home still shows only 3 reflections.
blog.html shows the new reflection.
The correct category filter includes it.
Read the latest reflection opens the new post.
Read reflection opens the correct page.
Back to all reflections works.
Featured image loads.
Footer and navigation work.
Take a Pause still works.
6. Validate
Upload the new post HTML to the W3C HTML Validator.
Target:
0 errors
0 warnings
7. Check mobile
Test the live page on a phone after publishing.
Check:
post text width and spacing;
featured/card image cropping;
homepage reflection cards;
navigation;
footer;
newsletter section.
8. Commit and publish
Example:
git add .
git commit -m "Publish POST TITLE reflection"
git push
Wait for GitHub Pages to deploy, then check the live site.
9. Newsletter
After the new post is live:
prepare the new-reflection email in Kit;
include the reflection title;
include a short introduction;
link to the new post;
send yourself a test first;
then send to subscribers.
10. Final live check
Open the public Tender Mercies site and verify:
homepage;
new post;
reflections archive;
latest-reflection button;
category filter;
newsletter;
social-sharing link preview when applicable.


That gives you one repeatable publishing routine instead of trying to remember every little thing each week.

One thing I’d add to `project.md` too, but much shorter:

```md
## Publishing System

Tender Mercies uses `scripts/posts.js` as the central source of post metadata.

The homepage automatically displays the three newest reflections, while the Reflections archive displays all published posts and filters them by category.

New reflection pages are created from `posts/post-template.html`.

