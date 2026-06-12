# Frontend Mentor - REST Countries API with color theme switcher

![Design preview for the REST Countries API with color theme switcher coding challenge](preview.jpg)

## Welcome! 👋

Thanks for checking out this front-end coding challenge.

[Frontend Mentor](https://www.frontendmentor.io) challenges help you improve your coding skills by building realistic projects.

**To do this challenge, you need a good understanding of HTML, CSS, and JavaScript.**

## ⚠️ Please note: this challenge no longer uses a live API

This challenge was originally built around the [REST Countries API](https://restcountries.com). That API has since moved to a paid, account-based service, so its old free endpoints no longer return data. To keep this challenge free and working out of the box, we've included all the country data in a `data.json` file for you to use instead.

You'll still practice the skills this challenge is all about: requesting data, waiting for the response, looping through it, searching, filtering, and rendering it to the page. Working with a local JSON file is very close to working with an API. You fetch the data, handle the response, and shape it into your UI. The main difference is that there's no third-party server in the mix, so you don't need an API key and you won't get blocked by the API going down mid-build.

If you'd like to practice calling a real endpoint, you can host `data.json` yourself (for example, on GitHub Pages) and fetch it over the network. That gives you the same request-and-response flow against a URL you control.

## The challenge

Your challenge is to use the country data in `data.json` to build out the application and get it looking as close to the design as possible.

You can use any JavaScript framework/library on the front-end such as [React](https://react.dev) or [Vue](https://vuejs.org). You also have complete control over which packages you use to do things like fetch the data or style your project.

Your users should be able to:

- See all countries from the data on the homepage
- Search for a country using an `input` field
- Filter countries by region
- Click on a country to see more detailed information on a separate page
- Click through to the border countries on the detail page
- Toggle the color scheme between light and dark mode *(optional)*

## The data

All 250 countries live in the `data.json` file as an array of country objects. Each object holds everything you need for both the homepage cards and the detail pages.

Here's a trimmed example of a single country object, showing the fields the design uses:

```json
{
  "name": "Germany",
  "nativeName": "Deutschland",
  "capital": "Berlin",
  "region": "Europe",
  "subregion": "Western Europe",
  "population": 83516593,
  "topLevelDomain": [".de"],
  "currencies": [{ "code": "EUR", "name": "Euro", "symbol": "€" }],
  "languages": [{ "iso639_1": "de", "iso639_2": "deu", "name": "German", "nativeName": "Deutsch" }],
  "borders": ["AUT", "BEL", "CZE", "DNK", "FRA", "LUX", "NLD", "POL", "CHE"],
  "alpha3Code": "DEU",
  "flags": {
    "svg": "https://flagcdn.com/de.svg",
    "png": "https://flagcdn.com/w320/de.png"
  }
}
```

Each object includes some extra fields too (such as `alpha2Code`, `callingCodes`, `area`, and `timezones`), so feel free to explore the file and use whatever you need.

### Fields used in the design

| Property | Type | Description |
| --- | --- | --- |
| `name` | string | The country's common name, shown on the cards and detail page |
| `nativeName` | string | The country's name in its native language, shown on the detail page |
| `flags` | object | Flag image URLs in `svg` and `png` formats (served by [flagcdn.com](https://flagcdn.com)) |
| `population` | number | Total population, used on the cards and detail page |
| `region` | string | The region the country belongs to, used by the region filter |
| `subregion` | string | The more specific subregion, shown on the detail page |
| `capital` | string | The capital city |
| `topLevelDomain` | array | The country's top-level domain(s), for example `[".de"]` |
| `currencies` | array | Currency objects, each with a `code`, `name`, and `symbol` |
| `languages` | array | Language objects, each with the language `name` and its codes |
| `borders` | array | The `alpha3Code`s of bordering countries, used to link between detail pages |
| `alpha3Code` | string | The country's three-letter code, used to match `borders` back to countries |

A few small territories have empty or zero values for fields like `capital` or `borders`, so it's worth handling those gracefully in your UI.

### A note about the data

The country data is a point-in-time snapshot rather than a live feed, with population figures reflecting 2024 estimates. That means the numbers won't always match other sources exactly, which is completely fine for this challenge. The flag images are served by [flagcdn.com](https://flagcdn.com), a free flag CDN, so they'll load over the network while everything else comes from your local `data.json`.

### Want some support on the challenge?

[Join our community](https://www.frontendmentor.io/community) and ask questions in the **#help** channel.

## Where to find everything

Your task is to build out the project to the designs inside the `/design` folder.

In this challenge, you will find mobile and desktop designs in light and dark mode color schemes for both pages.

The designs are in JPG static format. Using JPGs will mean that you'll need to use your best judgment for styles such as `font-size`, `padding` and `margin`.

If you would like the Figma design file to inspect the design in more detail, you can [subscribe as a PRO member](https://www.frontendmentor.io/pro).

The country data comes from the `data.json` file in the root of this starter code, and the flag images load from [flagcdn.com](https://flagcdn.com). You can use an icon font library for the icons.

There is also a `style-guide.md` file containing the information you'll need, such as color palette and fonts.

## Using AI coding assistants

We've included two files to help you if you're using AI coding assistants (like Claude, GitHub Copilot, Cursor, etc.) while working on this challenge:

- `AGENTS.md` - Contains detailed instructions for AI assistants on how to help you with this challenge. It's tailored to this challenge's difficulty level, so the AI will provide guidance appropriate to your learning stage—offering more support for beginner challenges and encouraging more independence on advanced ones.
- `CLAUDE.md` - A pointer file that directs Claude-based tools to the AGENTS.md instructions.

**How to use them:** You don't need to do anything! These files are automatically detected by most AI coding tools. The AI will read them and adjust its behavior to be a better learning partner—guiding you toward solutions rather than just giving you the answers.

**Note:** These files are designed to help you *learn*, not to do the work for you. The AI is instructed to ask questions, give hints, and explain concepts rather than writing complete solutions.

## Building your project

Feel free to use any workflow that you feel comfortable with. Below is a suggested process, but do not feel like you need to follow these steps:

1. Initialize your project as a public repository on [GitHub](https://github.com/). Creating a repo will make it easier to share your code with the community if you need help. If you're not sure how to do this, [have a read-through of this Try Git resource](https://try.github.io/).
2. Configure your repository to publish your code to a web address. This will also be useful if you need some help during a challenge as you can share the URL for your project with your repo URL. There are a number of ways to do this, and we provide some recommendations below.
3. Look through the designs to start planning out how you'll tackle the project. This step is crucial to help you think ahead for CSS classes to create reusable styles.
4. Before adding any styles, structure your content with HTML. Writing your HTML first can help focus your attention on creating well-structured content.
5. Write out the base styles for your project, including general content styles, such as `font-family` and `font-size`.
6. Start adding styles to the top of the page and work down. Only move on to the next section once you're happy you've completed the area you're working on.

## Deploying your project

As mentioned above, there are many ways to host your project for free. Our recommended hosts are:

- [GitHub Pages](https://pages.github.com/)
- [Vercel](https://vercel.com/)
- [Netlify](https://www.netlify.com/)

You can host your site using one of these solutions or any of our other trusted providers. [Read more about our recommended and trusted hosts](https://www.frontendmentor.io/guides/hosting-your-solution).

## Create a custom `README.md`

We strongly recommend overwriting this `README.md` with a custom one. We've provided a template inside the [`README-template.md`](./README-template.md) file in this starter code.

The template provides a guide for what to add. A custom `README` will help you explain your project and reflect on your learnings. Please feel free to edit our template as much as you like.

Once you've added your information to the template, delete this file and rename the `README-template.md` file to `README.md`. That will make it show up as your repository's README file.

## Submitting your solution

Submit your solution on the platform for the rest of the community to see. Follow our ["Complete guide to submitting solutions"](https://www.frontendmentor.io/guides/how-to-submit-solutions) for tips on how to do this.

Remember, if you're looking for feedback on your solution, be sure to ask questions when submitting it. The more specific and detailed you are with your questions, the higher the chance you'll get valuable feedback from the community.

## Sharing your solution

There are multiple places you can share your solution:

1. Share your solution page in the **#finished-projects** channel of the [community](https://www.frontendmentor.io/community).
2. Share on [X (formerly Twitter)](https://x.com/frontendmentor) and mention **@frontendmentor**, including the repo and live URLs in your post. We'd love to take a look at what you've built and help share it around.
3. Share your solution on [LinkedIn](https://www.linkedin.com/company/frontend-mentor/).
4. Blog about your experience building your project. Writing about your workflow, technical choices, and talking through your code is a brilliant way to reinforce what you've learned. Great platforms to write on are [dev.to](https://dev.to/), [Hashnode](https://hashnode.com/), and [CodeNewbie](https://community.codenewbie.org/).

We provide templates to help you share your solution once you've submitted it on the platform. Please do edit them and include specific questions when you're looking for feedback.

The more specific you are with your questions the more likely it is that another member of the community will give you feedback.

## Got feedback for us?

We love receiving feedback! We're always looking to improve our challenges and our platform. So if you have anything you'd like to mention, please email hi[at]frontendmentor[dot]io.

This challenge is completely free. Please share it with anyone who will find it useful for practice.

**Have fun building!** 🚀
