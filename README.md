# Jiny Build

## 설치 및 초기화

### 프로젝트 설치 및 업데이트

```
composer create-project jiny/build my-site
composer update
```

### Tailwind CSS 설치
Install tailwindcss and its peer dependencies via npm, and then run the init command to generate both tailwind.config.js and postcss.config.js.

```
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

Configure your template paths
Add the paths to all of your template files in your tailwind.config.js file.

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./resources/**/*.blade.php",
    "./resources/**/*.js",
    "./resources/**/*.vue",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

Add the Tailwind directives to your CSS
Add the @tailwind directives for each of Tailwind’s layers to your ./resources/css/app.css file.

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Start your build process
Run your build process with npm run dev.

```
npm run dev
```

Start using Tailwind in your project
Make sure your compiled CSS is included in the <head> then start using Tailwind’s utility classes to style your content.

```
<!doctype html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  @vite('resources/css/app.css')
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```

## 서버실행

### 라라벨로 로컬 서버 실행하기
새로운 터미널로 라라벨 서버를 실행합니다.
```
php artisan serve
```

### 접속하기
`localhost:8000`으로 접속합니다.