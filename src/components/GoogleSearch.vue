<template>
  <section
    class="bg-white bg-opacity-95 dark:bg-opacity-95 rounded-xl shadow-card relative dark:bg-gray-600 dark:shadow-favorite py-6 px-6 h-32"
  >
    <!---->
    <div class="flex flex-col items-center gap-3">
      <img src="/icons/Google_logo.svg" alt="لوگوی گوگل" class="w-24" />
      <form
        target="_self"
        action="https://www.google.com/search"
        class="w-full flex items-center gap-2"
      >
        <div class="w-10/12 relative">
          <input
            type="text"
            name="q"
            autocomplete="off"
            placeholder="جستجو در گوگل"
            tabindex="1"
            required="required"
            class="w-full rounded-3xl pr-10 py-1 h-9 bg-gray-50 font-medium"
          /><svg
            viewBox="0 0 24 24"
            class="svg-icon svg-fill absolute right-2 top-1"
            style="width: 1.8rem; height: 1.8rem"
          >
            <path
              fill="gray"
              stroke="none"
              pid="0"
              d="M9.5 3A6.5 6.5 0 0116 9.5c0 1.61-.59 3.09-1.56 4.23l.27.27h.79l5 5-1.5 1.5-5-5v-.79l-.27-.27A6.516 6.516 0 019.5 16 6.5 6.5 0 013 9.5 6.5 6.5 0 019.5 3m0 2C7 5 5 7 5 9.5S7 14 9.5 14 14 12 14 9.5 12 5 9.5 5z"
            ></path>
          </svg>
        </div>
        <button type="submit" class="py-2 w-2/12 rounded-3xl font-extraBold">
          جستجو
        </button>
      </form>
    </div>
  </section>
</template>

<script>
export default {
  name: 'GoogleSearch',
}
</script>
