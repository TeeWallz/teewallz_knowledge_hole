---
id: Home
title: Home
slug: /
sidebar_position: -1
# sidebar_label: Easy
sidebar_class_name: pink
---
# My Knowledge Hole/Garden

This is the seed of my Digital garden.

I had my notes stored in Notion, but I found that informated started getting lost inside the databases.

This iteration currently uses [docusaurus](https://docusaurus.io/) and was inspired by [wiki.nikiv.dev](https://wiki.nikiv.dev/). Please send them some love.

I wanted to use the following solutions, but Docusaurus ticked more boxes for me:

Requirements:
- Auto generated sidebar with collapsing functionality
- Markdown support
- Embedded React/Vue if possible
- As little setup code as possible for this first iteration.


Other Solutions:
- [Vuepress](https://vuepress.vuejs.org/)
  - This solution looked awesome because I prefer Vue to React and would have liked to use embedded Vue
  - Sidebar auto generation is not supported by default and is [really difficult to enable, requiring custom js](https://bootcamp.uxdesign.cc/vuepress-vs-vitepress-an-ultimate-guide-for-all-ya-fence-sitters-4f25f4da025). After a day of faffing around I wasn't work it
- [11ty](https://www.11ty.dev/)
  - Next to [Vue 3's Composition API](https://vuejs.org/api/composition-api-setup.html#basic-usage), Eleventy is my next favourite web tool
  - This may have been preferable as it compiles the Markdown into files, as opposed to Docusaurus being an SPA
  - I couldn't find many tools that allowed for eact Auto sidebars that looked good from the get-go.
  - I got a few tools working, but nothing 'felt' stable