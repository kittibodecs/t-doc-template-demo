---
type: guide
title: 'Creating a new category'
description: 'This guide will walk you through how to add a new category'
category: template-basics
order: 2
---

# Creating a New Category

Categories are essential for organizing content in documentation websites. They help visitors find guides and enhance site navigation. Follow the steps below to add a new category in **T-Doc Template**.


## Step 1: Navigate to the Docs Directory

Open your project directory.
Go to the **contents/docs/** folder. This folder contains all documentation content.


## Step 2: Create a New Category Directory

Create a new directory for your category:

Name the folder based on the category name you want to add. For example:

   ```bash
   mkdir contents/docs/my-new-category
   ```

Use lowercase letters and hyphens for consistency in folder naming.


## Step 3: Add an `index.md` File

Inside the new directory (e.g., `contents/docs/my-new-category`), create a file named `index.md`.
This file contains the metadata for the category.

Add the following content to the `index.md` file:

```yaml
---
type: category
title: My New Category
description: "A description for this category."
order: 1
---
```


**Fields Explanation**:

- **type**: Always set to `category`.
- **title**: The display name of the category.
- **description**: A short description of the category. 
- **order**: Specifies the display order of categories, with lower numbers appearing first.


[Regenerate the site automatically](/docs/getting-started/03-how-to-use#regenerate-the-site) and refresh your browser. 
Check that the new category appears in the left-hand documentation menu.


## Troubleshooting

- Make sure there are no useless characters and typos inside your index.md file. 
- Ensure there are 3 hyphens(---) at the beginning and at the end of your markdown file. This is called the [front matter](https://toucansites.com/docs/content-management/front-matter/).








