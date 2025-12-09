# TUTORIAL 2: INSTALL FLOWBITE

## STEP 1
- Install Tailwind
```
npm install flowbite --save
```

## STEP 2
- Open **app/assets/css/main.css**
- Copy and paste the following code
```
@import "tailwindcss";
@import "flowbite/src/themes/default";
```

## STEP 3
- Create **composables/useFlowbite.js**
- Copy and paste the following code
```
export function useFlowbite(callback) {
    if (process.client) {
        import('flowbite').then((flowbite) => {
        callback(flowbite);
        });
    }
}
```

## STEP 4
- Save

#
[<< Prev](https://code.cloud-connect.asia/ajmalnorshawali/setup-nuxt3-tailwind/-/blob/main/Tutorial%202%3A%20Install%20Tailwind.md)
|
[Next >>](https://code.cloud-connect.asia/ajmalnorshawali/setup-nuxt3-tailwind/-/blob/main/Tutorial%204:%20Nuxt%20Views.md)
