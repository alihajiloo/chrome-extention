<template>
  <div class="flex-1 flex flex-col gap-y-3.5">
    <section
      class="bg-white bg-opacity-95 dark:bg-opacity-95 rounded-xl shadow-card relative dark:bg-gray-600 dark:shadow-favorite relative flex-1"
    >
      <!---->
      <div class="flex flex-col h-full gap-5 justify-between p-5 z-0">
        <div class="flex-between-center">
          <h1 class="heading-primary filter font-extraBold" id="taskTitle">
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
        <div id="tasksBody" class="mb-auto max-h-110 overflow-y-auto filter">
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

                <div class="flex items-center justify-between w-full text-2xs">
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
</template>

<script>
export default {
  name: 'Todo',
  data() {
    return {
      tasks: [],
      taskName: '',
      taskFlag: '',
      showTask: false,
    }
  },
  mounted() {
    if (localStorage.getItem('tasks'))
      this.tasks = JSON.parse(localStorage.getItem('tasks'))
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
      localStorage.setItem('tasks', JSON.stringify(this.tasks))
    },
  },
}
</script>
