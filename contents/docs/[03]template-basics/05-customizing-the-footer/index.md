---
type: guide
title: 'Customizing the footer'
description: 'This guide will walk you through customizing the footer.'
category: template-basics
order: 5
---

# Customizing the Footer

The footer is an important section of your website, often used to display additional navigation, social media links, or copyright information. Follow these steps to customize the footer in **T-Doc Template**.

---

## Edit the Footer Content

Open the **site.yaml** file in your project directory.

   - This file contains the global configuration for your site, including footer content.

Locate the `footer-socials` section. Example:

```yaml
footer-socials:
  - title: 'LinkedIn'
    url: 'https://linkedin.com/'
  - title: 'X'
    url: 'https://x.com/'
```

Add, update, or remove social media links as needed:
   - **title**: The name of the social platform or link.
   - **url**: The URL for the social link.
   - **icon** (optional): You can use a one-line SVG tag.


## Add Custom Links or Text

To include additional text (e.g., copyright notices or custom links), add a section like this in **site.yaml**:

   ```yaml
   footer-links:
     - label: 'Privacy Policy'
       url: '/privacy-policy/'
     - label: 'Terms of Service'
       url: '/terms-of-service/'
   ```

Modify the content to fit your requirements:

   - **label**: The text for the footer link.
   - **url**: The relative or absolute URL for the link.
   - **icon** (optional): The icon for the footer link.


## Update Footer Styles (Optional)

### Update Footer Structure 

Navigate to the **templates/default/views/partials/** directory. The footer layout is defined in the Mustache file: `footer.mustache`.

Edit the `footer.mustache` to adjust the structure or additional content. Example:

   ```html
   <footer>
     <div class="footer-links">
       {{#footer-links}}
       <a href="{{url}}">{{label}}</a>
       {{/footer-links}}
     </div>
     <div class="footer-socials">
       {{#footer-socials}}
       <a href="{{url}}" target="_blank">{{title}}</a>
       {{/footer-socials}}
     </div>
   </footer>
   ```

Adjust `footer.mustache` to change the structure, such as sections, rearrangement of elements, or adding new placeholders.


### Update Footer Style 

The visual appearance is handled in the CSS stylesheet.
Modify them in **templates/default/assets/css/footer.css** to match your design preferences.

Here you can define: 
- layout: flexbox, grid, or inline styles
- colors: background, text, hover states
- spacing: margins, paddings, alignment.


[Regenerate the site automatically](/docs/getting-started/03-how-to-use#regenerate-the-site) and refresh your browser.
Scroll to the footer section to check if the updates have been applied.




