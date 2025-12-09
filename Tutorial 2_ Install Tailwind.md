# TUTORIAL 2: INSTALL TAILWIND

## STEP 1
- Install Tailwind
```
npm install tailwindcss @tailwindcss/vite --save
```

## STEP 2
- Create **app/assets/css/main.css**
- Copy and paste the following code
```
@import "tailwindcss";
```

## STEP 3
- Copy and paste the following code in file **_nuxt.config.ts_**
```
import tailwindcss from "@tailwindcss/vite";

export default defineNuxtConfig({
  compatibilityDate: "2025-11-13",
  devtools: { enabled: true },
  css: ['~/assets/css/main.css'],
  vite: {
    plugins: [
      tailwindcss(),
    ],
  },
});
```

## STEP 4
- Save and run
```
npm run dev
```

#
[<< Prev](https://code.cloud-connect.asia/ajmalnorshawali/setup-nuxt3-tailwind/-/blob/main/Tutorial%201:%20Install%20Nuxt.md)
|
[Next >>](https://code.cloud-connect.asia/ajmalnorshawali/setup-nuxt3-tailwind/-/blob/main/Tutorial%203:%20Install%20Flowbite.md)
