<template>
  <div dir="rtl" class="h-full body" id="body">
    <div
      class="w-6xl absolute left-1/2 transform -translate-x-1/2 origin-top pb-8"
    >
      <header
        class="flex items-center justify-between my-1 bg-opacity-80 dark:bg-opacity-80 rounded-xl"
      >
        <a
          href="https://dastyar.io/"
          target="_self"
          class="flex items-center my-2"
          ><img
            src="icons/icon.png"
            alt="dastyaaaar logo"
            class="w-10 h-auto"
          />
          <h1 class="mr-2 font-black text-2xl text-sky-600 dark:text-sky-500">
            دستیار
          </h1></a
        >
        <div class="px-4">
          <div
            class="v-popover event-popover w-7 h-7 flex items-center justify-center rounded-full :bg-gray-500 cursor-pointer hover:bg-gray-100 dark:hover:bg-gray-500 relative"
          >
            <div class="trigger" style="display: inline-block">
              <input
                class="btn-icon"
                type="file"
                id="img"
                name="img"
                accept="image/*"
              />
              <button class="btn-icon" id="uploadButton">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 1.5rem; height: 1.5rem"
                >
                  <path
                    fill="#1a77f3"
                    stroke="none"
                    pid="0"
                    d="M12 8a4 4 0 014 4 4 4 0 01-4 4 4 4 0 01-4-4 4 4 0 014-4m0 2a2 2 0 00-2 2 2 2 0 002 2 2 2 0 002-2 2 2 0 00-2-2m-2 12c-.25 0-.46-.18-.5-.42l-.37-2.65c-.63-.25-1.17-.59-1.69-.99l-2.49 1.01c-.22.08-.49 0-.61-.22l-2-3.46a.493.493 0 01.12-.64l2.11-1.66L4.5 12l.07-1-2.11-1.63a.493.493 0 01-.12-.64l2-3.46c.12-.22.39-.31.61-.22l2.49 1c.52-.39 1.06-.73 1.69-.98l.37-2.65c.04-.24.25-.42.5-.42h4c.25 0 .46.18.5.42l.37 2.65c.63.25 1.17.59 1.69.98l2.49-1c.22-.09.49 0 .61.22l2 3.46c.13.22.07.49-.12.64L19.43 11l.07 1-.07 1 2.11 1.63c.19.15.25.42.12.64l-2 3.46c-.12.22-.39.31-.61.22l-2.49-1c-.52.39-1.06.73-1.69.98l-.37 2.65c-.04.24-.25.42-.5.42h-4m1.25-18l-.37 2.61c-1.2.25-2.26.89-3.03 1.78L5.44 7.35l-.75 1.3L6.8 10.2a5.55 5.55 0 000 3.6l-2.12 1.56.75 1.3 2.43-1.04c.77.88 1.82 1.52 3.01 1.76l.37 2.62h1.52l.37-2.61c1.19-.25 2.24-.89 3.01-1.77l2.43 1.04.75-1.3-2.12-1.55c.4-1.17.4-2.44 0-3.61l2.11-1.55-.75-1.3-2.41 1.04a5.42 5.42 0 00-3.03-1.77L12.75 4h-1.5z"
                  ></path>
                </svg>
              </button>
            </div>
          </div>
        </div>
      </header>
      <main class="flex gap-x-4">
        <div class="flex-1 flex flex-col gap-y-3.5">
          <section
            class="bg-white bg-opacity-95 dark:bg-opacity-95 rounded-xl shadow-card relative dark:bg-gray-600 dark:shadow-favorite relative flex-1"
          >
            <!---->
            <div class="flex flex-col h-full gap-5 justify-between p-5 z-0">
              <div class="flex-between-center">
                <h1
                  class="heading-primary filter font-extraBold"
                  id="taskTitle"
                >
                  دست نویس
                </h1>
                <button class="text-xs w-20 z-20 px-2 py-1 filter">
                  <svg
                    viewBox="0 0 24 24"
                    class="svg-icon svg-fill"
                    style="width: 0.8rem; height: 0.8rem"
                  >
                    <path
                      fill="white"
                      stroke="none"
                      pid="0"
                      d="M12 9a3 3 0 013 3 3 3 0 01-3 3 3 3 0 01-3-3 3 3 0 013-3m0-4.5c5 0 9.27 3.11 11 7.5-1.73 4.39-6 7.5-11 7.5S2.73 16.39 1 12c1.73-4.39 6-7.5 11-7.5M3.18 12a9.821 9.821 0 0017.64 0 9.821 9.821 0 00-17.64 0z"
                    ></path></svg
                  ><span @click="blurTask" class="font-normal">{{
                    showTask == true ? 'نمایش بده' : 'مخفی کن'
                  }}</span>
                </button>
              </div>
              <div
                id="tasksBody"
                class="mb-auto max-h-110 overflow-y-auto filter"
              >
                <ul class="max-h-full">
                  <li
                    v-for="(task, index) in tasks"
                    :key="task.name"
                    draggable="true"
                    class="todo__item flex items-center pl-1 pt-2 pb-1 border-t border-gray-300 dark:border-gray-500 hover:bg-gray-100 dark:hover:bg-gray-500"
                  >
                    <svg
                      viewBox="0 0 24 24"
                      class="svg-icon svg-fill handle cursor-move"
                      style="width: 1.8rem; height: 1.8rem"
                    >
                      <path
                        fill="#c6c3c3"
                        stroke="none"
                        pid="0"
                        d="M7 19v-2h2v2H7m4 0v-2h2v2h-2m4 0v-2h2v2h-2m-8-4v-2h2v2H7m4 0v-2h2v2h-2m4 0v-2h2v2h-2m-8-4V9h2v2H7m4 0V9h2v2h-2m4 0V9h2v2h-2M7 7V5h2v2H7m4 0V5h2v2h-2m4 0V5h2v2h-2z"
                      ></path></svg
                    ><input
                      type="checkbox"
                      id="074efaf7-b747-4786-9534-99243a21fa5c"
                      class="form-checkbox bg-gray-100 border-gray-300 text-green-50"
                    />
                    <div class="w-full text-right mr-2 ml-4">
                      <label
                        for="074efaf7-b747-4786-9534-99243a21fa5c"
                        class="text-sm font-semibold w-full text-appGray-900 dark:text-gray-300"
                        style="word-break: break-word"
                      >
                        {{ task.name }}
                      </label>

                      <div
                        class="flex items-center justify-between w-full text-2xs"
                      >
                        <span class="todo__item__tag dark:text-sky-800">
                          {{ task.flag }}</span
                        ><!---->
                      </div>
                    </div>
                    <button
                      class="btn-icon hover:bg-white dark:hover:bg-gray-600"
                      @click="deleteTask(index)"
                    >
                      <svg
                        viewBox="0 0 24 24"
                        class="svg-icon svg-fill"
                        style="width: 1.2rem; height: 1.2rem"
                      >
                        <path
                          fill="#c6c3c3"
                          stroke="none"
                          pid="0"
                          d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12 19 6.41z"
                        ></path>
                      </svg>
                    </button>
                  </li>
                </ul>
              </div>
              <form id="taskForm" class="flex justify-between gap-x-1 filter">
                <div
                  class="flex flex-col w-full border-2 border-sky-800 rounded-lg bg-sky-200 relative"
                >
                  <input
                    type="text"
                    placeholder="عنوان کار جدید"
                    required="required"
                    v-model="taskName"
                    class="w-full border-0 rounded-b-none font-regular"
                  />
                  <div class="h-px w-full bg-gray-300 dark:bg-gray-400"></div>
                  <div class="relative">
                    <input
                      dir="rtl"
                      v-model="taskFlag"
                      autocomplete="off"
                      type="text"
                      placeholder="برچسب کار"
                      maxlength="15"
                      class="tag-input w-full font-regular text-xs pb-0 pt-1 pr-5 pl-14 border-0 rounded-t-none"
                    />
                  </div>
                  <svg
                    viewBox="0 0 24 24"
                    class="svg-icon svg-fill absolute bottom-1 right-1"
                    style="width: 0.8rem; height: 0.8rem"
                  >
                    <path
                      fill="#a0a0a0"
                      stroke="none"
                      pid="0"
                      d="M5.5 7A1.5 1.5 0 014 5.5 1.5 1.5 0 015.5 4 1.5 1.5 0 017 5.5 1.5 1.5 0 015.5 7m15.91 4.58l-9-9C12.05 2.22 11.55 2 11 2H4c-1.11 0-2 .89-2 2v7c0 .55.22 1.05.59 1.41l8.99 9c.37.36.87.59 1.42.59.55 0 1.05-.23 1.41-.59l7-7c.37-.36.59-.86.59-1.41 0-.56-.23-1.06-.59-1.42z"
                    ></path>
                  </svg>
                  <!-- flags -->
                  <div class="absolute bottom-0 left-1 flag-inputs flex">
                    <label
                      ><input
                        type="checkbox"
                        false-value=""
                        true-value="low"
                        class="hidden placeholder" /><svg
                        viewBox="0 0 24 24"
                        class="svg-icon svg-fill cursor-pointer opacity-30 transition-opacity duration-100"
                        style="width: 1rem; height: 1rem"
                      >
                        <path
                          fill="#10B981"
                          stroke="none"
                          pid="0"
                          d="M6 3a1 1 0 011 1v.88C8.06 4.44 9.5 4 11 4c3 0 3 2 5 2 3 0 4-2 4-2v8s-1 2-4 2-3-2-5-2c-3 0-4 2-4 2v7H5V4a1 1 0 011-1z"
                        ></path></svg></label
                    ><label
                      ><input
                        type="checkbox"
                        false-value=""
                        true-value="medium"
                        class="hidden" /><svg
                        viewBox="0 0 24 24"
                        class="svg-icon svg-fill cursor-pointer opacity-30 transition-opacity duration-100"
                        style="width: 1rem; height: 1rem"
                      >
                        <path
                          fill="#F59E0B"
                          stroke="none"
                          pid="0"
                          d="M6 3a1 1 0 011 1v.88C8.06 4.44 9.5 4 11 4c3 0 3 2 5 2 3 0 4-2 4-2v8s-1 2-4 2-3-2-5-2c-3 0-4 2-4 2v7H5V4a1 1 0 011-1z"
                        ></path></svg></label
                    ><label
                      ><input
                        type="checkbox"
                        false-value=""
                        true-value="high"
                        class="hidden" /><svg
                        viewBox="0 0 24 24"
                        class="svg-icon svg-fill cursor-pointer opacity-30 transition-opacity duration-100"
                        style="width: 1rem; height: 1rem"
                      >
                        <path
                          fill="#DC2626"
                          stroke="none"
                          pid="0"
                          d="M6 3a1 1 0 011 1v.88C8.06 4.44 9.5 4 11 4c3 0 3 2 5 2 3 0 4-2 4-2v8s-1 2-4 2-3-2-5-2c-3 0-4 2-4 2v7H5V4a1 1 0 011-1z"
                        ></path></svg
                    ></label>
                  </div>
                  <!-- flags end -->
                </div>
                <button
                  type="submit"
                  class="btn-secondary px-2"
                  @click.prevent="addTask(taskName, taskFlag)"
                >
                  <svg
                    viewBox="0 0 24 24"
                    class="svg-icon svg-fill"
                    style="width: 1.5rem; height: 1.5rem"
                  >
                    <path
                      fill="#c6c3c3"
                      stroke="none"
                      pid="0"
                      d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"
                    ></path>
                  </svg>
                </button>
              </form>
            </div>
          </section>
        </div>
        <div class="flex-2 flex flex-col gap-y-3.5">
          <section
            class="bg-white bg-opacity-95 dark:bg-opacity-95 rounded-xl shadow-card relative dark:bg-gray-600 dark:shadow-favorite py-6 px-6 h-32"
          >
            <!---->
            <div class="flex flex-col items-center gap-3">
              <!-- <img
                src="/img/Google_logo.e99543bb.svg"
                alt="لوگوی گوگل"
                class="w-24"
              /> -->
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
                <button
                  type="submit"
                  class="py-2 w-2/12 rounded-3xl font-extraBold"
                >
                  جستجو
                </button>
              </form>
            </div>
          </section>
          <section>
            <div class="grid grid-cols-6 grid-rows-2 gap-y-3 gap-x-2.5">
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill pt-1"
                  style="width: 2.2rem; height: 2.2rem"
                >
                  <path
                    pid="0"
                    d="M12 16c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2m0-6c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2m0-6c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2M6 16c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2m0-6c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2m0-6c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2m12 12c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2m0-6c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2m0-6c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2z"
                  ></path></svg
                ><span class="mt-3 leading-none">دم دستی</span>
              </div>
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill pt-1"
                  style="width: 2.2rem; height: 2.2rem"
                >
                  <path
                    pid="0"
                    d="M2 12h2v5h16v-5h2v5c0 1.11-.89 2-2 2H4a2 2 0 01-2-2v-5m10 3l5.55-5.46-1.42-1.41L13 11.25V2h-2v9.25L7.88 8.13 6.46 9.55 12 15z"
                  ></path></svg
                ><span class="mt-3 leading-none">دانلود‌ها</span>
              </div>
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill pt-1"
                  style="width: 2.2rem; height: 2.2rem"
                >
                  <path
                    pid="0"
                    d="M13.5 8H12v5l4.28 2.54.72-1.21-3.5-2.08V8M13 3a9 9 0 00-9 9H1l3.96 4.03L9 12H6a7 7 0 017-7 7 7 0 017 7 7 7 0 01-7 7c-1.93 0-3.68-.79-4.94-2.06l-1.42 1.42A8.896 8.896 0 0013 21a9 9 0 009-9 9 9 0 00-9-9"
                  ></path></svg
                ><span class="mt-3 leading-none">تاریخچه</span>
              </div>
              <a
                href="https://www.google.com/"
                target="_self"
                class="favorite relative text-center"
                ><button
                  class="btn-icon absolute top-1 left-1 hover:bg-gray-200"
                >
                  <svg
                    viewBox="0 0 24 24"
                    class="svg-icon svg-fill"
                    style="width: 0.8rem; height: 0.8rem"
                  >
                    <path
                      fill="#c6c3c3"
                      stroke="none"
                      pid="0"
                      d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12 19 6.41z"
                    ></path>
                  </svg></button
                ><img
                  src="https://www.google.com/s2/favicons?sz=64&amp;domain=https://www.google.com/"
                  class="pt-1 w-7"
                /><span class="mt-3 leading-none">گوگل</span></a
              ><a
                href="https://reg.mazust.ac.ir"
                target="_self"
                class="favorite relative text-center"
                ><button
                  class="btn-icon absolute top-1 left-1 hover:bg-gray-200"
                >
                  <svg
                    viewBox="0 0 24 24"
                    class="svg-icon svg-fill"
                    style="width: 0.8rem; height: 0.8rem"
                  >
                    <path
                      fill="#c6c3c3"
                      stroke="none"
                      pid="0"
                      d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12 19 6.41z"
                    ></path>
                  </svg></button
                ><img
                  src="https://www.google.com/s2/favicons?sz=64&amp;domain=https://reg.mazust.ac.ir"
                  class="pt-1 w-7"
                /><span class="mt-3 leading-none">آموزش دانشگاه</span></a
              ><a
                href="https://web.whatsapp.com/"
                target="_self"
                class="favorite relative text-center"
                ><button
                  class="btn-icon absolute top-1 left-1 hover:bg-gray-200"
                >
                  <svg
                    viewBox="0 0 24 24"
                    class="svg-icon svg-fill"
                    style="width: 0.8rem; height: 0.8rem"
                  >
                    <path
                      fill="#c6c3c3"
                      stroke="none"
                      pid="0"
                      d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12 19 6.41z"
                    ></path>
                  </svg></button
                ><img
                  src="https://www.google.com/s2/favicons?sz=64&amp;domain=https://web.whatsapp.com/"
                  class="pt-1 w-7"
                /><span class="mt-3 leading-none">whats app</span></a
              >
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 3rem; height: 2.5rem"
                >
                  <path
                    fill="#c6c3c3"
                    stroke="none"
                    pid="0"
                    d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"
                  ></path>
                </svg>
              </div>
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 3rem; height: 2.5rem"
                >
                  <path
                    fill="#c6c3c3"
                    stroke="none"
                    pid="0"
                    d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"
                  ></path>
                </svg>
              </div>
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 3rem; height: 2.5rem"
                >
                  <path
                    fill="#c6c3c3"
                    stroke="none"
                    pid="0"
                    d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"
                  ></path>
                </svg>
              </div>
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 3rem; height: 2.5rem"
                >
                  <path
                    fill="#c6c3c3"
                    stroke="none"
                    pid="0"
                    d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"
                  ></path>
                </svg>
              </div>
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 3rem; height: 2.5rem"
                >
                  <path
                    fill="#c6c3c3"
                    stroke="none"
                    pid="0"
                    d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"
                  ></path>
                </svg>
              </div>
              <div class="favorite">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 3rem; height: 2.5rem"
                >
                  <path
                    fill="#c6c3c3"
                    stroke="none"
                    pid="0"
                    d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"
                  ></path>
                </svg>
              </div>
              <!---->
            </div>
          </section>
        </div>
        <div class="flex-1 flex flex-col gap-y-3.5">
          <div class="flex gap-x-4">
            <section
              class="bg-white bg-opacity-95 dark:bg-opacity-95 rounded-xl shadow-card relative dark:bg-gray-600 dark:shadow-favorite p-2 pb-1 h-32 flex justify-center items-end w-1/2"
            >
              <button class="btn-icon absolute right-1 top-1">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 0.7rem; height: 0.7rem"
                >
                  <path
                    fill="#c6c3c3"
                    stroke="none"
                    pid="0"
                    d="M12 8a4 4 0 014 4 4 4 0 01-4 4 4 4 0 01-4-4 4 4 0 014-4m0 2a2 2 0 00-2 2 2 2 0 002 2 2 2 0 002-2 2 2 0 00-2-2m-2 12c-.25 0-.46-.18-.5-.42l-.37-2.65c-.63-.25-1.17-.59-1.69-.99l-2.49 1.01c-.22.08-.49 0-.61-.22l-2-3.46a.493.493 0 01.12-.64l2.11-1.66L4.5 12l.07-1-2.11-1.63a.493.493 0 01-.12-.64l2-3.46c.12-.22.39-.31.61-.22l2.49 1c.52-.39 1.06-.73 1.69-.98l.37-2.65c.04-.24.25-.42.5-.42h4c.25 0 .46.18.5.42l.37 2.65c.63.25 1.17.59 1.69.98l2.49-1c.22-.09.49 0 .61.22l2 3.46c.13.22.07.49-.12.64L19.43 11l.07 1-.07 1 2.11 1.63c.19.15.25.42.12.64l-2 3.46c-.12.22-.39.31-.61.22l-2.49-1c-.52.39-1.06.73-1.69.98l-.37 2.65c-.04.24-.25.42-.5.42h-4m1.25-18l-.37 2.61c-1.2.25-2.26.89-3.03 1.78L5.44 7.35l-.75 1.3L6.8 10.2a5.55 5.55 0 000 3.6l-2.12 1.56.75 1.3 2.43-1.04c.77.88 1.82 1.52 3.01 1.76l.37 2.62h1.52l.37-2.61c1.19-.25 2.24-.89 3.01-1.77l2.43 1.04.75-1.3-2.12-1.55c.4-1.17.4-2.44 0-3.61l2.11-1.55-.75-1.3-2.41 1.04a5.42 5.42 0 00-3.03-1.77L12.75 4h-1.5z"
                  ></path>
                </svg></button
              ><span
                class="text-xs font-light absolute top-1 right-5 p-1 text-gray-500 dark:text-gray-300"
                >Tehran</span
              >
              <div class="flex flex-col items-center">
                <div
                  class="flex items-end font-black text-3.5xl leading-loose h-17"
                >
                  {{ time }}
                </div>
                <a
                  href="https://www.bahesab.ir/time/timer/?utm_source=dastyar&amp;utm_medium=taghvim&amp;utm_campaign=partner"
                  target="_self"
                  class="btn-anchor font-regular flex"
                  ><svg
                    viewBox="0 0 24 24"
                    class="svg-icon svg-fill ml-1"
                    style="width: 1.1rem"
                  >
                    <path
                      pid="0"
                      d="M12 20a7 7 0 01-7-7 7 7 0 017-7 7 7 0 017 7 7 7 0 01-7 7m7.03-12.61l1.42-1.42c-.45-.51-.9-.97-1.41-1.41L17.62 6c-1.55-1.26-3.5-2-5.62-2a9 9 0 00-9 9 9 9 0 009 9c5 0 9-4.03 9-9 0-2.12-.74-4.07-1.97-5.61M11 14h2V8h-2m4-7H9v2h6V1z"
                    ></path></svg
                  >زمان‌سنج</a
                >
              </div>
            </section>
            <section
              class="bg-white bg-opacity-95 dark:bg-opacity-95 rounded-xl shadow-card relative dark:bg-gray-600 dark:shadow-favorite p-2 pb-1 px-3 flex items-end h-32 w-1/2"
            >
              <button class="btn-icon absolute right-1 top-1">
                <svg
                  viewBox="0 0 24 24"
                  class="svg-icon svg-fill"
                  style="width: 0.7rem; height: 0.7rem"
                >
                  <path
                    fill="#c6c3c3"
                    stroke="none"
                    pid="0"
                    d="M12 8a4 4 0 014 4 4 4 0 01-4 4 4 4 0 01-4-4 4 4 0 014-4m0 2a2 2 0 00-2 2 2 2 0 002 2 2 2 0 002-2 2 2 0 00-2-2m-2 12c-.25 0-.46-.18-.5-.42l-.37-2.65c-.63-.25-1.17-.59-1.69-.99l-2.49 1.01c-.22.08-.49 0-.61-.22l-2-3.46a.493.493 0 01.12-.64l2.11-1.66L4.5 12l.07-1-2.11-1.63a.493.493 0 01-.12-.64l2-3.46c.12-.22.39-.31.61-.22l2.49 1c.52-.39 1.06-.73 1.69-.98l.37-2.65c.04-.24.25-.42.5-.42h4c.25 0 .46.18.5.42l.37 2.65c.63.25 1.17.59 1.69.98l2.49-1c.22-.09.49 0 .61.22l2 3.46c.13.22.07.49-.12.64L19.43 11l.07 1-.07 1 2.11 1.63c.19.15.25.42.12.64l-2 3.46c-.12.22-.39.31-.61.22l-2.49-1c-.52.39-1.06.73-1.69.98l-.37 2.65c-.04.24-.25.42-.5.42h-4m1.25-18l-.37 2.61c-1.2.25-2.26.89-3.03 1.78L5.44 7.35l-.75 1.3L6.8 10.2a5.55 5.55 0 000 3.6l-2.12 1.56.75 1.3 2.43-1.04c.77.88 1.82 1.52 3.01 1.76l.37 2.62h1.52l.37-2.61c1.19-.25 2.24-.89 3.01-1.77l2.43 1.04.75-1.3-2.12-1.55c.4-1.17.4-2.44 0-3.61l2.11-1.55-.75-1.3-2.41 1.04a5.42 5.42 0 00-3.03-1.77L12.75 4h-1.5z"
                  ></path>
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
                    style="width: 1.1rem; height: 1.1rem"
                  >
                    <path
                      pid="0"
                      d="M6 19a5 5 0 01-5-5 5 5 0 015-5c1-2.35 3.3-4 6-4 3.43 0 6.24 2.66 6.5 6.03L19 11a4 4 0 014 4 4 4 0 01-4 4H6m13-6h-2v-1a5 5 0 00-5-5c-2.5 0-4.55 1.82-4.94 4.19C6.73 11.07 6.37 11 6 11a3 3 0 00-3 3 3 3 0 003 3h13a2 2 0 002-2 2 2 0 00-2-2z"
                    ></path></svg
                  >پیش بینی کامل</a
                >
              </div>
            </section>
          </div>
          <section
            class="bg-white bg-opacity-95 dark:bg-opacity-95 rounded-xl shadow-card relative dark:bg-gray-600 dark:shadow-favorite py-3 px-2"
          >
            <!---->
            <div class="flex items-center justify-evenly gap-4">
              <div class="flex flex-col justify-center items-center">
                <span class="text-base font-medium">۱۴۰۰</span
                ><span class="text-4xl font-black h-8 mt-1">۸</span
                ><span class="text-2xl font-medium">دی</span>
              </div>
              <div
                class="flex flex-col justify-between items-start text-xs font-medium"
              >
                <ul
                  class="list-disc list-inside text-warning-700 dark:text-warning-400 pb-1"
                >
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
            display-format="jYYYY/jMM/jDD"
          />
        </div>
      </main>
    </div>
  </div>
</template>

<script>
import '../assets/styles/index.css'
import VuePersianDatetimePicker from 'vue-persian-datetime-picker'
import $ from 'jquery'

export default {
  name: 'App',
  data() {
    return {
      time: `${new Date().getHours()}:${new Date().getMinutes()} `,
      date: new Date().toISOString(),
      show: false,
      tasks: [],
      taskName: '',
      taskFlag: '',
      showTask: false,
    }
  },
  components: {
    datePicker: VuePersianDatetimePicker,
  },
  mounted() {
    this.show = true
    if (localStorage.getItem('tasks'))
      this.tasks = JSON.parse(localStorage.getItem('tasks'))

    $('#img').hide()
    $('#uploadButton').on('click', function () {
      $('#img').click()
    })

    if (localStorage.getItem('background_img') !== null) {
      $('#body').css(
        'background-image',
        'url("' + localStorage.getItem('background_img') + '")'
      )
    }

    $('#img').change(function () {
      var file = this.files[0]
      var reader = new FileReader()
      reader.onloadend = function () {
        $('#body').css('background-image', 'url("' + reader.result + '")')
        localStorage.setItem('background_img', reader.result)
      }
      if (file) {
        reader.readAsDataURL(file)
      }
    })
  },
  methods: {
    addTask(name, flag) {
      this.tasks.push({ name, flag })
      this.saveTasks()
    },
    deleteTask(position) {
      this.tasks.splice(position, 1)
      this.saveTasks()
    },
    blurTask() {
      var taskTitle = document.getElementById('taskTitle')
      var tasksBody = document.getElementById('tasksBody')
      var taskForm = document.getElementById('taskForm')

      if (!this.showTask) {
        this.showTask = true
        taskTitle.classList.add('blur-sm')
        tasksBody.classList.add('blur-sm')
        taskForm.classList.add('blur-sm')
      } else {
        this.showTask = false
        taskTitle.classList.remove('blur-sm')
        tasksBody.classList.remove('blur-sm')
        taskForm.classList.remove('blur-sm')
      }
    },
    saveTasks() {
      console.log(JSON.stringify(this.tasks))
      localStorage.setItem('tasks', JSON.stringify(this.tasks))
    },
  },
}
</script>
