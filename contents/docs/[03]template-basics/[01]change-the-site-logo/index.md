---
type: guide
title: 'Change the Site Logo'
description: 'This guide will walk you through how to change the site logo'
category: template-basics
order: 1
---

# Change the Site Logo


The **site logo** is one of the key elements of your site's branding. In **T-Doc Template**, the logo is located in the `assets` folder.


You can change the logo quickly and easily — we will start by the most simple way to do so. 
If you want to use inline SVG or a custom image tag, see the [Modify the template guide](/docs/template-basics/change-the-site-logo/#option-2-modify-the-template-instead)

---

## Replace the Default Logo Files

1. Navigate to the **assets/images/logos/** directory in your project folder.
   - By default, this folder contains two logo files:
     - **logo.png**: The primary logo used across the site.
     - **logo~dark.png**: A variation of the logo used in dark mode (if your site supports it).

2. Create and name your custom logos
   -  **Recommended File Format**: Use PNG with a transparent background for best results.
   If you prefer other formats (e.g., SVG or JPG), ensure that your site supports them. 
   - **Rename your custom logos** to match the default logo file names:
   - `logo.png` (for the primary logo)
   - `logo~dark.png` (for the dark mode logo)

3. Copy your custom logo files into the **assets/images/logos/** directory.
   - Overwrite the existing `logo.png` and `logo~dark.png` files.


4. Regenerate the Site

After replacing the logo files, you need to regenerate your site for the changes to take effect:

Open your terminal and navigate to your project directory.

Run the following command:

   ```sh
   toucan generate
   ```

This command will process the updated assets and regenerate the site.


5. Preview Your Changes

Start the local development server to preview the updated site:

   ```sh
   toucan serve
   ```

Open your browser and navigate to [http://localhost:3000](http://localhost:3000).

Check that the new logo is displayed on the site and dark mode logo is displayed correctly (if you have one).

---












## Option 2: Modify the Template Instead

Instead of replacing the default `logo.png` files, you can directly modify the navigation template to use your own inline SVG or a custom image tag.

### Use a Custom Inline SVG

1. Open the navigation template file:

   ```sh
   templates/default/views/partials/navigation.mustache
   ```

2. Locate the following block there:

   ```html
   <a href="{{baseUrl}}/" class="logo">
     <svg ...>...</svg>
     <span>{{site.name}}</span>
   </a>
   ```

3. Replace the `&lt;svg&gt;` tag with your own custom inline SVG content.

### Use a Custom <img> Tag

If you prefer using an image file instead of inline SVG:

1. Replace the `&lt;svg&gt;` element with an image tag, like so:

   ```html
   <picture>
     <source
       srcset="{{baseUrl}}/images/logos/logo~dark.png"
       media="(prefers-color-scheme: dark)"
     />
     <img
       src="{{baseUrl}}/images/logos/logo.png"
       alt="Logo of {{site.name}}"
       title="{{site.name}}"
     />
   </picture>
   ```

2. Make sure the path matches your custom logo file and that it's placed in the correct location.

3. You can add logic for dark mode by switching the image source via JavaScript or CSS.

Regenerate the site and check if your changes appear correctly.

> Tip: Keep the `alt` attribute meaningful for better accessibility.

---

## Troubleshooting

If the updated logo does not appear, check the following:

1. **File Naming**: Ensure that your custom files are named exactly `logo.png` and `logo~dark.png`.
2. **File Path**: Confirm the files are located in **assets/images/logos/**.
3. **Cache**: Clear your browser cache or use an incognito window to view the changes.

---
