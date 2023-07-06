# Links

A simple landing page for displaying profile information and social media links. It's like those LinkTree or "link in bio" pages you see around the internet.

The code is deliberately very simple. Just one HTML file, and one (optional) CSS file.

You can see it in action here: [https://links.chrism.cloud/](https://links.chrism.cloud/).

The profile is marked up using the [H-Card microformats](https://microformats.org/wiki/h-card), for some basic [IndieWeb](https://indieweb.org/) compatibility.

## Use + Customisation

If you want to use this as the basis of your own page, fork this repository. From there, edit the contents of the HTML to your needs. It's split into a couple of distinct sections:

- Header + profile picture.
- "About Me" text
- Social links

Obviously you'll want to change the name used throughout, add your own text, and update the links to your own profiles.

For the user picture, I sized mine to 250px by 250px. You can adjust for your own, if you need to.

Icons are from [Font Awesome](https://fontawesome.com/). I've used the SVG versions as I didn't want to include any extraneous scripts or CSS if I didn't need to. If you want to add an icon for a service I don't use, [here is where to get one to match](https://fontawesome.com/search?o=r&m=free&f=brands).

To change the colours or other styling, you will need to remove the optimised CSS from the `<head>` section of the HTML file, and uncomment the link to the stylesheet `/assets/css/style.css`. The code for the links are all near the bottom of this file. The gist of how the link hover effects works is:

- Each link has a set of selectors which looks for the start of the URL.
- These selectors define the colour used for the normal state and the hover state. `box-shadow` is used for the hover effect.
- There's also a selector to define the colour of the SVG icons in each state.

## Deployment

The project can be deployed pretty much anywhere - it's just HTML and CSS, after all. I've got mine hosted in [Azure Static Web Apps](https://azure.microsoft.com/en-gb/products/app-service/static/) for free, but other options like [Netlify](https://www.netlify.com/) should work just fine. Both of those options can deploy directly from GitHub whenever you make changes. There's some configuration for Azure SWA in the project, but you'll need to hook it up to your own account (or remove it if you don't need it).
