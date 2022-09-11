# Experimenting Figma Tokens with Tailwind CSS
I am exploring and evaluating Figma Tokens plugin (in Figma) as part of key workflow for dealing with Design Tokens while keeping tight integration with development. Part of the tech and tools involved:
- Figma Tokens (to handle, modify and extend Design Tokens)
- Tailwind CSS
- Style Dictionary

## First challenge (from Designing in Figma POV)
One of the first issue I noticed as a designer is that the default tailwind tokens are not easily accessible in Figma Tokens. This just naturally hinders productivity on the design side because the tailwind default essentially its already available in code. Right now it seems like we have to either manually port it and maintain it which is counter-productive. More in depth explanation:

### Visualization of the challenge
![help](https://user-images.githubusercontent.com/827167/189519221-525c919f-6acf-481c-93d0-61d58b242f10.jpg)

### Video explainer of the challenge and help needed
https://user-images.githubusercontent.com/827167/189519301-2691cd9d-ace5-4fd5-8a46-0f47fe54dc0e.mp4

## Second challenge (Integrate Figma Tokens with localhost repo)

_Coming soon, still drafting_

---

> ## figma-tokens-example-tailwindcss
>
> This example illustrates how you can transform your tokens stored on Figma Tokens (with GitHub sync enabled) to be automatically transformed with token-transformer and Style Dictionary to a TailwindCSS environment with multiple themes. The theme switcher itself just adds `light-theme` or `dark-theme` to the root class, so in theory you could have not only light or dark theme but many different themes.
>
> Change your tokens in `tokens.json` (either directly or with the Figma Tokens plugin in Figma). The GitHub action will automatically generate tokens to the `tokens/` directory that can then be read by Style Dictionary, which will output tokens to the format you defined in `build.js` - css variables will be generated in the `output` directory which Tailwind will pick up and generate utility classes.
>
> Note: Ideally generated css/dist files wouldn't be part of the repository but rather live in the build environment. I only included them here for showcase.
