---
type: guide
title: 'Creating a custom page'
description: 'This guide will walk you through how to create a custom page and add it to the navigation menu'
category: template-basics
order: 4
---

# Creating a Custom Page in Navigation

Adding a custom page is a great way to enhance your site’s functionality by including pages like ‘Contact Us,’ ‘FAQ,’ or other static content. Follow the steps below to create a custom page and add it to the navigation menu in **T-Doc Template**.

---

### Step 1: Edit the Navigation Menu

Open the **site.yaml** file in your project directory.

The `navigation` section of this file manages the navigation menu displayed on your site.

Add a new entry under the `navigation` section for your custom page. Example:

```yaml
navigation:
  - label: 'Docs'
    url: '/docs/'
  - label: 'About'
    url: '/about/'
  - label: 'Contact'
    url: '/contact/'
  - label: FAQ
    url: '/faq/'
```

**Fields Explanation**:

- **label**: The text displayed in the navigation menu.
- **url**: The relative URL of the custom page.

### Step 2: Create the Custom Page Directory

Navigate to the **contents/** folder.
Create a new directory for your custom page. For example:

```bash
mkdir contents/faq
```

### Step 3: Add an `index.md` File

Inside the new directory (e.g., `contents/faq`), create a file named `index.md`.
This file contains the metadata and content for the custom page.

Add the following content to the `index.md` file:

```text
---
title: "FAQ"
description: "Frequently asked questions"
views:
    html: pages.default_page
---
```

**Fields Explanation**:

- **title**: The title of the custom page.
- **description**: A short description or summary of the page's content.
- **template**: The Mustache template used to render the page.


### Step 4: Add Content to the Page

Below the metadata in `index.md`, write the content of your custom page using Markdown. Example:

```
## FAQ

### How do I reset my password?
If you forgot your password, you can reset it by clicking the "Forgot Password" link on the login page.

### How can I contact support?
You can reach our support team at [support@example.com](mailto:support@example.com).
```

### Step 5: Create a New Template (Optional)

If the default view `pages.default_page` does not fit your needs, create a custom Mustache file:
Navigate to **templates/default/views/pages/**.
Create a new Mustache file, e.g., `faq.mustache`.

Update the `views.html` field in the custom page's metadata to use your new view:

```text
views:
    html: pages.home
```

[Regenerate the site automatically](/docs/getting-started/03-how-to-use#regenerate-the-site) and refresh your browser
Ensure that the custom page is displayed correctly and can be accessed from the navigation menu.


