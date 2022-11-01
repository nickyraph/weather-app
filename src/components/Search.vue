<template>

    <div class="flex items-center justify-between">
        <input type="text" class="p-4 rounded-lg bg-[#24343D]" placeholder="Seach Here">

        <div class="flex bg-[#24343D] py-3 px-5 rounded-lg items-center justify-center space-x-4">
            <span class="text-gray-300">Filters:</span>
            <div class="border p-2 rounded-lg flex items-center space-x-3">
                <Span>Coldest</Span>
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" class="w-3 fill-current">
                    <path d="M233.4 406.6c12.5 12.5 32.8 12.5 45.3 0l192-192c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L256 338.7 86.6 169.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l192 192z"/>
                </svg>
            </div>
            <div class="border p-2 rounded-lg flex items-center space-x-3">
                <Span>10<sup>o</sup> - 20<sup>o</sup> C</Span>
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" class="w-3 fill-current">
                    <path d="M233.4 406.6c12.5 12.5 32.8 12.5 45.3 0l192-192c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L256 338.7 86.6 169.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l192 192z"/>
                </svg>
            </div>
            <div class="border p-2 rounded-lg flex items-center space-x-3">
                <Span>Rainy</Span>
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" class="w-3 fill-current">
                    <path d="M233.4 406.6c12.5 12.5 32.8 12.5 45.3 0l192-192c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L256 338.7 86.6 169.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l192 192z"/>
                </svg>
            </div>
        </div>
    </div>

</template>
