# TUTORIAL 4: NUXT VIEWS

# STEP 1
- Create **app/components/Navbar.vue**
- Copy and paste the following code
```
<template>
<nav class="fixed top-0 z-50 w-full bg-white border-b border-gray-200">
    <div class="px-3 py-3">
        <div class="flex items-center justify-between">
            <!-- logo -->
            <div class="flex items-center">
                <div class="flex items-center ms-2 md:me-24">
                    <img src="https://flowbite.com/docs/images/logo.svg" class="h-8 me-3" alt="FlowBite Logo" />
                    <span class="font-bold">Flowbite</span>
                </div>
            </div>
            <!-- menu -->
            <ul class="flex items-center">
                <li>
                    <NuxtLink class="text-gray-700 hover:text-gray-800 cursor-pointer">
                        Wishlist
                    </NuxtLink>
                </li>
            </ul>
        </div>
    </div>
</nav>
</template>
```

# STEP 2
- Create **app/components/Sidebar.vue**
- Copy and paste the following code
```
<template>
<aside class="fixed top-0 left-0 z-30 w-64 h-screen pt-20 bg-white border-r border-gray-200">
    <div class="h-full px-3 pb-4 overflow-y-auto bg-white">
        <ul class="font-medium">
            <li>
                <NuxtLink to="/" class="flex items-center p-2 rounded-lg text-gray-700 hover:bg-gray-100">
                    <span>Home</span>
                </NuxtLink>
            </li>
        </ul>
    </div>
</aside>
</template>

```

# STEP 3
- Create **app/layouts/default.vue**
- Copy and paste the following code
```
<template>
<Navbar />
<Sidebar />

<div class="pt-20 px-4 ml-64">
    <slot />
</div>
</template>
```

# STEP 4
- Create **app/pages/index.vue**
- Copy and paste the following code
```
<template>
<h1 class="text-2xl font-bold">HELLO TAILWIND</h1>
</template>
```

## STEP 5
- Open file **app.vue**
- Copy and paste the following code
```
<script setup>
import { onMounted } from 'vue'
import { useFlowbite } from '~~/composables/useFlowbite';

// initialize components based on data attribute selectors
onMounted(() => {
    useFlowbite(() => {
        initFlowbite();
    })
})
</script>

<template>
<NuxtLayout>
    <NuxtPage />
</NuxtLayout>
</template>
```

## STEP 5
- Save and run
```
npm run dev
```

#
[<< Prev](https://github.com/ajmalnorshawali/setup-nuxt3-tailwind/blob/main/Tutorial%203_%20Install%20Flowbite.md)
