# milincic.com

```bash
# create a new project with npm
npm create astro@latest

# Add Vue.js Using NPM
npx astro add vue

# Install LEss preprocessor
npm install less

# Start project
npm run dev
```

### layout
```html
---
import '../../public/less/style.less';
---

<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width" />
		<link rel="icon" type="image/svg+xml" href="/favicon.svg" />
		<meta name="generator" content={Astro.generator} />

		<!-- uikit  -->
		<script defer is:client src="https://unpkg.com/htmx.org@1.9.2" integrity="sha384-L6OqL9pRWyyFU3+/bjdSri+iIphTN/bvYyM37tICVyOJkWZLpP2vGn6VUEXgzg6h" crossorigin="anonymous"></script>
		<script is:client src="/uikit/dist/js/uikit.min.js"></script>
		<script is:client src="/uikit/dist/js/uikit-icons.min.js"></script>

		<link rel="preconnect" href="https://fonts.googleapis.com">
		<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
		<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500&family=Jost:wght@300;400;500&display=swap" rel="stylesheet">

		<title>{title}</title>
	</head>

	<body>
		<slot />
	</body>

</html>
```