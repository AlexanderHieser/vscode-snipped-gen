<template>
    <div class="min-h-screen flex flex-col">
        <header class="pl-8 pt-1">
            <p class="text-orange-600 text-2xl font-bold h-12 pb-1">Snippets</p>
        </header>

        <div class="flex-1 flex flex-col sm:flex-row">
            <main class="flex-1 pt-6">
                <div class="grid grid-cols-1 auto-cols-max h-full py-4">
                    <div class=" border border-gray-200 shadow-sm m-6">
                        <textarea class="textarea w-full h-full p-2" placeholder="Snippet HTML"></textarea>
                    </div>
                    <div class="border border-gray-200 shadow-sm m-6">
                        <textarea class="textarea w-full h-full" placeholder="Snippet HTML"></textarea>
                    </div>
                </div>
            </main>

            <nav class="order-first sm:w-96 h-12">
                <div class="items-strech pt-4 px-4">
                    <div class="flex items-strech place-content-center ">
                        <div class="btn-group">
                            <button class="flex-auto btn btn-sm">Export</button>
                            <button class="btn btn-sm">Save</button>
                            <button class="btn btn-sm">Import</button>
                        </div>
                    </div>
                </div>
                <div class="overflow-auto h-[calc(100vh-100px)]">
                    <SnippetListEntry v-for="x in 10" />
                </div>
            </nav>
        </div>

        <footer class="bg-gray-100 items-center"></footer>
    </div>
</template>