## Tailwind 4 setup
```cmd
npm init
```
```cmd
npm install tailwindcss @tailwindcss/cli
```

+ mkdir src > input.css >  @import "tailwindcss";
+ src > index.html
```html
<link href="./output.css" rel="stylesheet">
```
```cmd
npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch
```

## Structure
```md
my-project/
│
├─ package.json          # Created by npm init
├─ tailwind.config.js    # (Optional, if you need custom config later)
│
├─ src/                  # All your development files
│  ├─ css/
│  │  └─ input.css       # Tailwind imports + your custom CSS
│  │
│  ├─ js/
│  │  └─ main.js         # Your JS files (optional)
│  │
│  ├─ index.html         # Main HTML page
│  └─ pages/             # (Optional) Extra HTML pages if your site grows
│
└─ dist/                 # Auto-generated output (production build)
   └─ output.css         # The compiled Tailwind CSS (DO NOT EDIT)

```

### Your src/css/input.css should look like:
```css
@import "tailwindcss";
```


## Running Tailwind (Development Mode)
### Use this command so Tailwind watches for changes:
```cmd
npx @tailwindcss/cli -i ./src/css/input.css -o ./dist/output.css --watch
```
```html
<link href="../dist/output.css" rel="stylesheet">
```

## Adding Scripts to package.json (So you don’t type that long command every time)
### Edit package.json and add:
```json
"scripts": {
  "dev": "npx @tailwindcss/cli -i ./src/css/input.css -o ./dist/output.css --watch",
  "build": "npx @tailwindcss/cli -i ./src/css/input.css -o ./dist/output.css --minify"
}
```
> For development (live watching)
```cmd
npm run dev    
```
>  For production (minified CSS)
```cmd
npm run build  
```
## deploying
> Install gh-pages
```cmd
npm install gh-pages --save-dev
```
```cmd
mkdir public
```
> Now build the CSS directly into public/:
```cmd
npx @tailwindcss/cli -i ./src/css/input.css -o ./public/output.css --minify
```
> Copy your site files into public/:
```bash
cp src/index.html public/
cp -r src/js public/
```
> Fix the CSS Link in public/index.html
```html
<link href="./output.css" rel="stylesheet">
```
> Update package.json Scripts

```json
"scripts": {
  "dev": "npx @tailwindcss/cli -i ./src/css/input.css -o ./public/output.css --watch",
  "build": "npx @tailwindcss/cli -i ./src/css/input.css -o ./public/output.css --minify",
  "deploy": "npm run build && cp src/index.html public/ && cp -r src/js public/ && gh-pages -d public"
}
```
> Deploy Your Site

```bash
npm run deploy
```


## tainwind 3 setup
```cmd
npm install -D tailwindcss@3
npx tailwindcss init
```
> Add the paths to all of your template files in your tailwind.config.js file.
```js
 /** @type {import('tailwindcss').Config} */
export default {
   content: ["./src/**/*.{html,js}"],
   theme: {
     extend: {},
   },
   plugins: [],
 }
```
> Add the @tailwind directives for each of Tailwind’s layers to your main CSS file.
+ src/input.css
```cmd
@tailwind base;
@tailwind components;
@tailwind utilities;
```
```cmd
npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
```
+ src/index.html
```html
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="./output.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```
