<template>
  <div dir="rtl" class="h-full body" id="body">
    <div
      class="w-6xl absolute left-1/2 transform -translate-x-1/2 origin-top pb-8">
      <header
        class="flex items-center justify-between my-1 bg-opacity-80 dark:bg-opacity-80 rounded-xl">
        <a
          href="https://dastyar.io/"
          target="_self"
          class="flex items-center my-2"
          ><img
            src="icons/icon.png"
            alt="dastyaaaar logo"
            class="w-10 h-auto" />
          <h1 class="mr-2 font-black text-2xl text-sky-600 dark:text-sky-500">
            دستیار
          </h1></a
        >

        <!-- start: Setting -->
        <setting />
        <!-- end: Setting -->
        
      </header>
      <main class="flex gap-x-4">
        <!-- start: TODO -->
        <todo />
        <!-- end: TODO -->

        <div class="flex-2 flex flex-col gap-y-3.5">
          <!-- start: GoogleSearch -->
          <google-search />
          <!-- end: GoogleSearch -->

          <section>
            <div class="grid grid-cols-6 grid-rows-2 gap-y-3 gap-x-2.5">
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill pt-1"
                  style="width: 2.2rem; height: 2.2rem">
                  <path
                    pid="0"
                    d="M12 16c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2m0-6c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2m0-6c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2M6 16c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2m0-6c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2m0-6c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2m12 12c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2m0-6c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2m0-6c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2z"></path></svg
                ><span class="mt-3 leading-none">دم دستی</span>
              </div>
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill pt-1"
                  style="width: 2.2rem; height: 2.2rem">
                  <path
                    pid="0"
                    d="M2 12h2v5h16v-5h2v5c0 1.11-.89 2-2 2H4a2 2 0 01-2-2v-5m10 3l5.55-5.46-1.42-1.41L13 11.25V2h-2v9.25L7.88 8.13 6.46 9.55 12 15z"></path></svg
                ><span class="mt-3 leading-none">دانلود‌ها</span>
              </div>
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill pt-1"
                  style="width: 2.2rem; height: 2.2rem">
                  <path
                    pid="0"
                    d="M13.5 8H12v5l4.28 2.54.72-1.21-3.5-2.08V8M13 3a9 9 0 00-9 9H1l3.96 4.03L9 12H6a7 7 0 017-7 7 7 0 017 7 7 7 0 01-7 7c-1.93 0-3.68-.79-4.94-2.06l-1.42 1.42A8.896 8.896 0 0013 21a9 9 0 009-9 9 9 0 00-9-9"></path></svg
                ><span class="mt-3 leading-none">تاریخچه</span>
              </div>
              <a
                href="https://www.google.com/"
                target="_self"
                class="favorite relative text-center"
                ><button
                  class="btn-icon absolute top-1 left-1 hover:bg-gray-200">
                  <svg
                    viewBox="0 0 24 24"
                    class="svg-icon svg-fill"
                    style="width: 0.8rem; height: 0.8rem">
                    <path
                      fill="#c6c3c3"
                      stroke="none"
                      pid="0"
                      d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12 19 6.41z"></path>
                  </svg></button
                ><img
                  src="https://www.google.com/s2/favicons?sz=64&amp;domain=https://www.google.com/"
                  class="pt-1 w-7" /><span class="mt-3 leading-none"
                  >گوگل</span
                ></a
              ><a
                href="https://reg.mazust.ac.ir"
                target="_self"
                class="favorite relative text-center"
                ><button
                  class="btn-icon absolute top-1 left-1 hover:bg-gray-200">
                  <svg
                    viewBox="0 0 24 24"
                    class="svg-icon svg-fill"
                    style="width: 0.8rem; height: 0.8rem">
                    <path
                      fill="#c6c3c3"
                      stroke="none"
                      pid="0"
                      d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12 19 6.41z"></path>
                  </svg></button
                ><img
                  src="https://www.google.com/s2/favicons?sz=64&amp;domain=https://reg.mazust.ac.ir"
                  class="pt-1 w-7" /><span class="mt-3 leading-none"
                  >آموزش دانشگاه</span
                ></a
              ><a
                href="https://web.whatsapp.com/"
                target="_self"
                class="favorite relative text-center"
                ><button
                  class="btn-icon absolute top-1 left-1 hover:bg-gray-200">
                  <svg
                    viewBox="0 0 24 24"
                    class="svg-icon svg-fill"
                    style="width: 0.8rem; height: 0.8rem">
                    <path
                      fill="#c6c3c3"
                      stroke="none"
                      pid="0"
                      d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12 19 6.41z"></path>
                  </svg></button
                ><img
                  src="https://www.google.com/s2/favicons?sz=64&amp;domain=https://web.whatsapp.com/"
                  class="pt-1 w-7" /><span class="mt-3 leading-none"
                  >whats app</span
                ></a
              >
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 3rem; height: 2.5rem">
                  <path
                    fill="#c6c3c3"
                    stroke="none"
                    pid="0"
                    d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"></path>
                </svg>
              </div>
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 3rem; height: 2.5rem">
                  <path
                    fill="#c6c3c3"
                    stroke="none"
                    pid="0"
                    d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"></path>
                </svg>
              </div>
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 3rem; height: 2.5rem">
                  <path
                    fill="#c6c3c3"
                    stroke="none"
                    pid="0"
                    d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"></path>
                </svg>
              </div>
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 3rem; height: 2.5rem">
                  <path
                    fill="#c6c3c3"
                    stroke="none"
                    pid="0"
                    d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"></path>
                </svg>
              </div>
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 3rem; height: 2.5rem">
                  <path
                    fill="#c6c3c3"
                    stroke="none"
                    pid="0"
                    d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"></path>
                </svg>
              </div>
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 3rem; height: 2.5rem">
                  <path
                    fill="#c6c3c3"
                    stroke="none"
                    pid="0"
                    d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"></path>
                </svg>
              </div>
              <!---->
            </div>
          </section>
        </div>
        <div class="flex-1 flex flex-col gap-y-3.5">
          <div class="flex gap-x-4">
            <section
              class="bg-white bg-opacity-95 dark:bg-opacity-95 rounded-xl shadow-card relative dark:bg-gray-600 dark:shadow-favorite p-2 pb-1 h-32 flex justify-center items-end w-1/2">
              <button class="btn-icon absolute right-1 top-1">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 0.7rem; height: 0.7rem">
                  <path
                    fill="#c6c3c3"
                    stroke="none"
                    pid="0"
                    d="M12 8a4 4 0 014 4 4 4 0 01-4 4 4 4 0 01-4-4 4 4 0 014-4m0 2a2 2 0 00-2 2 2 2 0 002 2 2 2 0 002-2 2 2 0 00-2-2m-2 12c-.25 0-.46-.18-.5-.42l-.37-2.65c-.63-.25-1.17-.59-1.69-.99l-2.49 1.01c-.22.08-.49 0-.61-.22l-2-3.46a.493.493 0 01.12-.64l2.11-1.66L4.5 12l.07-1-2.11-1.63a.493.493 0 01-.12-.64l2-3.46c.12-.22.39-.31.61-.22l2.49 1c.52-.39 1.06-.73 1.69-.98l.37-2.65c.04-.24.25-.42.5-.42h4c.25 0 .46.18.5.42l.37 2.65c.63.25 1.17.59 1.69.98l2.49-1c.22-.09.49 0 .61.22l2 3.46c.13.22.07.49-.12.64L19.43 11l.07 1-.07 1 2.11 1.63c.19.15.25.42.12.64l-2 3.46c-.12.22-.39.31-.61.22l-2.49-1c-.52.39-1.06.73-1.69.98l-.37 2.65c-.04.24-.25.42-.5.42h-4m1.25-18l-.37 2.61c-1.2.25-2.26.89-3.03 1.78L5.44 7.35l-.75 1.3L6.8 10.2a5.55 5.55 0 000 3.6l-2.12 1.56.75 1.3 2.43-1.04c.77.88 1.82 1.52 3.01 1.76l.37 2.62h1.52l.37-2.61c1.19-.25 2.24-.89 3.01-1.77l2.43 1.04.75-1.3-2.12-1.55c.4-1.17.4-2.44 0-3.61l2.11-1.55-.75-1.3-2.41 1.04a5.42 5.42 0 00-3.03-1.77L12.75 4h-1.5z"></path>
                </svg></button
              ><span
                class="text-xs font-light absolute top-1 right-5 p-1 text-gray-500 dark:text-gray-300"
                >Tehran</span
              >
              <div class="flex flex-col items-center">
                <div
                  class="flex items-end font-black text-3.5xl leading-loose h-17">
                  {{ time }}
                </div>
                <a
                  href="https://www.bahesab.ir/time/timer/?utm_source=dastyar&amp;utm_medium=taghvim&amp;utm_campaign=partner"
                  target="_self"
                  class="btn-anchor font-regular flex"
                  ><svg
                    viewBox="0 0 24 24"
                    class="svg-icon svg-fill ml-1"
                    style="width: 1.1rem">
                    <path
                      pid="0"
                      d="M12 20a7 7 0 01-7-7 7 7 0 017-7 7 7 0 017 7 7 7 0 01-7 7m7.03-12.61l1.42-1.42c-.45-.51-.9-.97-1.41-1.41L17.62 6c-1.55-1.26-3.5-2-5.62-2a9 9 0 00-9 9 9 9 0 009 9c5 0 9-4.03 9-9 0-2.12-.74-4.07-1.97-5.61M11 14h2V8h-2m4-7H9v2h6V1z"></path></svg
                  >زمان‌سنج</a
                >
              </div>
            </section>
            <section
              class="bg-white bg-opacity-95 dark:bg-opacity-95 rounded-xl shadow-card relative dark:bg-gray-600 dark:shadow-favorite p-2 pb-1 px-3 flex items-end h-32 w-1/2">
              <button class="btn-icon absolute right-1 top-1">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 0.7rem; height: 0.7rem">
                  <path
                    fill="#c6c3c3"
                    stroke="none"
                    pid="0"
                    d="M12 8a4 4 0 014 4 4 4 0 01-4 4 4 4 0 01-4-4 4 4 0 014-4m0 2a2 2 0 00-2 2 2 2 0 002 2 2 2 0 002-2 2 2 0 00-2-2m-2 12c-.25 0-.46-.18-.5-.42l-.37-2.65c-.63-.25-1.17-.59-1.69-.99l-2.49 1.01c-.22.08-.49 0-.61-.22l-2-3.46a.493.493 0 01.12-.64l2.11-1.66L4.5 12l.07-1-2.11-1.63a.493.493 0 01-.12-.64l2-3.46c.12-.22.39-.31.61-.22l2.49 1c.52-.39 1.06-.73 1.69-.98l.37-2.65c.04-.24.25-.42.5-.42h4c.25 0 .46.18.5.42l.37 2.65c.63.25 1.17.59 1.69.98l2.49-1c.22-.09.49 0 .61.22l2 3.46c.13.22.07.49-.12.64L19.43 11l.07 1-.07 1 2.11 1.63c.19.15.25.42.12.64l-2 3.46c-.12.22-.39.31-.61.22l-2.49-1c-.52.39-1.06.73-1.69.98l-.37 2.65c-.04.24-.25.42-.5.42h-4m1.25-18l-.37 2.61c-1.2.25-2.26.89-3.03 1.78L5.44 7.35l-.75 1.3L6.8 10.2a5.55 5.55 0 000 3.6l-2.12 1.56.75 1.3 2.43-1.04c.77.88 1.82 1.52 3.01 1.76l.37 2.62h1.52l.37-2.61c1.19-.25 2.24-.89 3.01-1.77l2.43 1.04.75-1.3-2.12-1.55c.4-1.17.4-2.44 0-3.61l2.11-1.55-.75-1.3-2.41 1.04a5.42 5.42 0 00-3.03-1.77L12.75 4h-1.5z"></path>
                </svg></button
              ><span
                class="text-xs font-light absolute top-1 right-5 p-1 text-gray-500 dark:text-gray-300"
                >تهران</span
              >
              <div class="flex flex-col items-center w-full">
                <div class="w-full mb-1 text-center">
                  <div class="flex items-center justify-around">
                    <div class="flex flex-col items-center justify-center">
                      <span dir="ltr" class="font-medium text-2xl leading-none"
                        >7°C</span
                      >
                    </div>
                    <!-- <img
                      src="/img/50d.d9abd872.svg"
                      alt="weather icon"
                      class="mb-2 w-10"
                    /> -->
                  </div>
                  <span class="text-xs font-medium">خیلی سرده 👀</span>
                </div>
                <a
                  href="https://openweathermap.org/city/112931"
                  target="_self"
                  class="btn-anchor mt-auto font-medium flex"
                  ><svg
                    viewBox="0 0 24 24"
                    class="svg-icon svg-fill ml-1"
                    style="width: 1.1rem; height: 1.1rem">
                    <path
                      pid="0"
                      d="M6 19a5 5 0 01-5-5 5 5 0 015-5c1-2.35 3.3-4 6-4 3.43 0 6.24 2.66 6.5 6.03L19 11a4 4 0 014 4 4 4 0 01-4 4H6m13-6h-2v-1a5 5 0 00-5-5c-2.5 0-4.55 1.82-4.94 4.19C6.73 11.07 6.37 11 6 11a3 3 0 00-3 3 3 3 0 003 3h13a2 2 0 002-2 2 2 0 00-2-2z"></path></svg
                  >پیش بینی کامل</a
                >
              </div>
            </section>
          </div>
          <section
            class="bg-white bg-opacity-95 dark:bg-opacity-95 rounded-xl shadow-card relative dark:bg-gray-600 dark:shadow-favorite py-3 px-2">
            <!---->
            <div class="flex items-center justify-evenly gap-4">
              <div class="flex flex-col justify-center items-center">
                <span class="text-base font-medium">۱۴۰۰</span
                ><span class="text-4xl font-black h-8 mt-1">۸</span
                ><span class="text-2xl font-medium">دی</span>
              </div>
              <div
                class="flex flex-col justify-between items-start text-xs font-medium">
                <ul
                  class="list-disc list-inside text-warning-700 dark:text-warning-400 pb-1">
                  <li class="mb-1">بیست و چهارم جمادی الاول ۱۴۴۳</li>
                  <li class="mb-1">بیست و نهم دسامبر ۲۰۲۱</li>
                  <li class="mb-1 text-sm font-normal">29 / 12 / 2021</li>
                </ul>
                <!---->
              </div>
            </div>
          </section>

          <date-picker
            class="font-regular inline-datepicker shadow-card relative dark:bg-gray-600 dark:shadow-favorite px-7 pt-5 pb-3"
            :auto-submit="true"
            :show="show"
            @close="show = false"
            popover="false"
            v-model="date"
            format="YYYY-MM-DD"
            display-format="jYYYY/jMM/jDD" />
        </div>
      </main>
    </div>
  </div>
</template>

<script>
import '../assets/styles/index.css'
import VuePersianDatetimePicker from 'vue-persian-datetime-picker'
import Todo from '@/components/Todo.vue'
import GoogleSearch from '@/components/GoogleSearch.vue'
import Setting from '../components/Setting.vue'

export default {
  name: 'App',
  data() {
    return {
      time: `${new Date().getHours()}:${new Date().getMinutes()} `,
      date: new Date().toISOString(),
      show: false,
    }
  },
  components: {
    datePicker: VuePersianDatetimePicker,
    Todo: Todo,
    GoogleSearch: GoogleSearch,
    Setting: Setting,
  },
}
</script>
