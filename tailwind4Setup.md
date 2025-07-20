## Basics
```
npm init
```
```
npm install tailwindcss @tailwindcss/cli
```

+ mkdir src > input.css >  @import "tailwindcss";
+ src > index.html
```
<link href="./output.css" rel="stylesheet">
```
```
npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch
```

## Structure
```
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
```
@import "tailwindcss";
```


## Running Tailwind (Development Mode)
### Use this command so Tailwind watches for changes:
```
npx @tailwindcss/cli -i ./src/css/input.css -o ./dist/output.css --watch
```
```
<link href="../dist/output.css" rel="stylesheet">
```

## Adding Scripts to package.json (So you don’t type that long command every time)
### Edit package.json and add:
```
"scripts": {
  "dev": "npx @tailwindcss/cli -i ./src/css/input.css -o ./dist/output.css --watch",
  "build": "npx @tailwindcss/cli -i ./src/css/input.css -o ./dist/output.css --minify"
}
```
> For development (live watching)
```
npm run dev    
```
>  For production (minified CSS)
```
npm run build  
```
