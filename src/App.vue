<script setup lang="ts">
import SnippetListEntry from './components/SnippetListEntry.vue'
</script>

<template>
    <div class="min-h-screen flex flex-col px-36 gap-8">
        <header class="pt-4 pb-4">
            <div class="navbar bg-base-100 shadow-md rounded-md">
                <a class="text-orange-600 text-2xl font-bold h-12 pb-0.5 pt-2">Snippet Generator</a>
            </div>
        </header>

        <div class="flex-1 flex flex-col sm:flex-row gap-4">
            <main class="flex-1">
                <div class="grid grid-cols-1 auto-cols-max h-full py-4">
                    <div class=" shadow-sm mb-4">
                        <textarea style="outline: none;" class="textarea  textarea-primary w-full h-full"
                            placeholder="HTML"></textarea>
                    </div>
                    <div class="">
                        <textarea style="outline: none;" class="textarea textarea-accent w-full h-full"
                            placeholder="Snippet"></textarea>
                    </div>
                </div>
            </main>
            <nav class="order-first sm:w-96 h-12 gap-4">
                <p class="text-orange-500 font-bold">Snippets</p>
                <div class="items-strech pt-1 pb-4">
                    <div class="flex items-strech place-content-center gap-1">
                        <button class="flex-1 btn btn-xs">Export</button>
                        <button class="flex-1 btn btn-xs">Save</button>
                        <button class="flex-1 btn btn-xs">Import</button>
                    </div>
                </div>
                <div class="overflow-auto h-[calc(100vh-260px)]">
                    <SnippetListEntry v-for="x in 10" />
                </div>
            </nav>
        </div>

        <footer class="flex content-center gap-3 pt-3 pb-3">
            <p class="flex-1 text-end ">GitHub</p>
            <p class="flex-1 text-center ">Made with Tailwind & Daisy UI</p>
            <p class="flex-1 text-start">Block</p>
        </footer>
    </div>
</template>
<style scoped>

</style>
