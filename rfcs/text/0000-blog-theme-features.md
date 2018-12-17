# Blog Theme Features

- Start Date: 2018-12-17
- RFC PR: n/a
- Yarn Issue: https://github.com/vuejs/vuepress/issues/36

## Summary

To design and develop the VuePress default Blog Theme, we need to have a definition of blogging-related features that should be supported. This RFC suggests an initial feature set: pages, pagination, chronological archive, tags, RSS feed and an overridable sidebar.

## Motivation

Blogging-focused static site builders generally support all the imaginable features: tags, categories, social links, multiple authors and more. Designing a nice and easy to use theme leaves too many options. The motivation of this RFC is to propose, discuss and decide on the initial feature set that would actually be useful for most blogs, and so should be part of the default blog theme.

## Detailed design

### Proposed blog theme structure

- `posts` folder for posts
  - Posts are named as `2018-12-17-post-slug.md`
  - There can also be a folder named `2018-12-17-post-slug` to store post-related media, like images or downloads.
- `pages` folder for static pages, like "About" or "Contact".

### Post metadata

- Title
- Tags (list)
- Date (datetime for RSS feed)

### Theme-generated pages

- Paginated pages (/, /page/2/, ...)
- Archive listing all posts by date (/archive/)
- Tags page listing all tags (/tags/)
- Tag page (/tag/NAME/), possibly with pagination (/tag/NAME/page/2/)
- RSS feed (/feed.xml)

### Personalization

There should be three areas of customization:

- Behaviour variables, like how many posts per page, perhaps what should be the URL of feed, etc.
- Theme variables, like primary color, font, etc. Depends on design.
- Overridable files, like Sidebar content (to show profile and social links)

## Unresolved questions


