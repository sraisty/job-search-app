# @/components/ui

This directory contains standard ui components that were created by **`shadcn/ui`**. `shadcn/ui` provides "beautifully designed components  built using Radix.js and Tailwind CSS: accessible and customizable components that you can copy and paste into your apps. Free. Open Source.

## SHADCN impact on package.json dependencies & devDependencies

Note that the name `shadcn/ui` is not listed as a dependency in the package.json.  Instead, shadcn added dependencies on radix, tailwind and a few other packages.  Note that these are DEPENDENCIES, not devDependencies:
    *`@radix-ui/react-slot`
    * `class-variance-authority`
    *`clsx`
    * `lucide-react`
    *`tailwind-merge`
    * `tailwindcss-animate`

## To add specific `shadcn` components to your project

1. `cd <project-root-directory>`
2. `npx shadcn@latest add button`
3. Answer the questions about theme/color schemes, etc. I said "Slate" for this project.
4. You might get a warning: `It looks like you are using React 19.
Some packages may fail to install due to peer dependency issues in npm (see https://ui.shadcn.com/react-19  ).`  
    * Don't worry about it.  The issue with the react-19 + next.js15 + tailwind4 + shadcn has been fixed in the most recent `shadcn@2.4.0-canary.12` release, which we are using.
    * so if asked, just pick "Use `--force`" when asked how you want to proceed.
    * The process of installing the component ADDS files:
        * `src/lib/utils.ts`
        * `src/components/ui/button.tsx`
        * `components.json`  (at project root directory.)
    * The install process might UPDATE these files:
        * `src/styles/globals.css`


To add more UI components:
`npx shadcn@latest add <name of component>`

To get the exact name of the component you need, refer to <https://ui.shadcn.com/docs/components/>

