<template>
  <div>
    <div class="px-4">
      <div
        class="v-popover event-popover w-7 h-7 flex items-center justify-center rounded-full :bg-gray-500 cursor-pointer hover:bg-gray-100 dark:hover:bg-gray-500 relative">
        <div class="trigger" style="display: inline-block">
          <input
            class="btn-icon"
            type="file"
            id="img"
            name="img"
            accept="image/*" />
          <button class="btn-icon" id="uploadButton">
            <svg
              viewBox="0 0 24 24"
              class="svg-icon svg-fill"
              style="width: 1.5rem; height: 1.5rem">
              <path
                fill="#1a77f3"
                stroke="none"
                pid="0"
                d="M12 8a4 4 0 014 4 4 4 0 01-4 4 4 4 0 01-4-4 4 4 0 014-4m0 2a2 2 0 00-2 2 2 2 0 002 2 2 2 0 002-2 2 2 0 00-2-2m-2 12c-.25 0-.46-.18-.5-.42l-.37-2.65c-.63-.25-1.17-.59-1.69-.99l-2.49 1.01c-.22.08-.49 0-.61-.22l-2-3.46a.493.493 0 01.12-.64l2.11-1.66L4.5 12l.07-1-2.11-1.63a.493.493 0 01-.12-.64l2-3.46c.12-.22.39-.31.61-.22l2.49 1c.52-.39 1.06-.73 1.69-.98l.37-2.65c.04-.24.25-.42.5-.42h4c.25 0 .46.18.5.42l.37 2.65c.63.25 1.17.59 1.69.98l2.49-1c.22-.09.49 0 .61.22l2 3.46c.13.22.07.49-.12.64L19.43 11l.07 1-.07 1 2.11 1.63c.19.15.25.42.12.64l-2 3.46c-.12.22-.39.31-.61.22l-2.49-1c-.52.39-1.06.73-1.69.98l-.37 2.65c-.04.24-.25.42-.5.42h-4m1.25-18l-.37 2.61c-1.2.25-2.26.89-3.03 1.78L5.44 7.35l-.75 1.3L6.8 10.2a5.55 5.55 0 000 3.6l-2.12 1.56.75 1.3 2.43-1.04c.77.88 1.82 1.52 3.01 1.76l.37 2.62h1.52l.37-2.61c1.19-.25 2.24-.89 3.01-1.77l2.43 1.04.75-1.3-2.12-1.55c.4-1.17.4-2.44 0-3.61l2.11-1.55-.75-1.3-2.41 1.04a5.42 5.42 0 00-3.03-1.77L12.75 4h-1.5z"></path>
            </svg>
          </button>
        </div>
      </div>
    </div>
    <!-- <div
      id="popover_5wqp06hcjk"
      aria-hidden="false"
      tabindex="0"
      class="tooltip popover vue-popover-theme open"
      x-placement="bottom"
      style="
        visibility: visible;
        position: absolute;
        will-change: transform;
        top: 0px;
        left: 0px;
        transform: translate3d(107px, 44px, 0px);
      ">
      <div class="wrapper">
        <div class="tooltip-inner popover-inner" style="position: relative">
          <div>
            <div class="flex flex-col p-2">
              <div class="flex items-center justify-between mb-4">
                <h4 class="text-xs font-bold text-sky-800">دارک مود</h4>
                <div class="flex flex-col justify-center items-center">
                  <div class="flex justify-center items-center">
                    <span>
                      <svg
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                        class="h-3 w-3 text-gray-600">
                        <path
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          stroke-width="2"
                          d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z"></path>
                      </svg>
                    </span>
                    <div
                      class="cursor-pointer w-8 h-4 flex items-center bg-gray-300 rounded-full mx-1 px-1">
                      <div
                        class="bg-white w-3 h-3 rounded-full transform transition-transform duration-200 -translate-x-3"></div>
                    </div>
                    <span>
                      <svg
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                        class="h-3 w-3 text-gray-600">
                        <path
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          stroke-width="2"
                          d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z"></path>
                      </svg>
                    </span>
                  </div>
                </div>
              </div>
              <div>
                <h4 class="text-xs font-bold text-sky-800 w-full mb-1">
                  انتخاب پس‌زمینه
                </h4>
                <div class="w-full grid grid-cols-5 gap-1">
                  <div
                    class="cursor-pointer w-9 h-9 rounded"
                    style="background-color: rgb(196, 222, 247)"></div>
                  <div
                    class="cursor-pointer w-9 h-9 rounded"
                    style="background-color: rgb(175, 235, 209)"></div>
                  <div
                    class="cursor-pointer w-9 h-9 rounded"
                    style="background-color: rgb(255, 234, 177)"></div>
                  <div
                    class="cursor-pointer w-9 h-9 rounded"
                    style="background-color: rgb(61, 81, 142)"></div>
                  <div
                    class="cursor-pointer w-9 h-9 rounded"
                    style="background-color: rgb(90, 96, 108)"></div>
                  <img
                    src="https://github.com/Mhdi1381/images/raw/main/bg1-tiny.jpg"
                    alt="پس زمینه 1"
                    class="cursor-pointer w-9 h-9 rounded" />
                  <img
                    src="https://github.com/Mhdi1381/images/raw/main/bg2-tiny.jpg"
                    alt="پس زمینه 2"
                    class="cursor-pointer w-9 h-9 rounded" />
                  <img
                    src="https://github.com/Mhdi1381/images/raw/main/bg3-tiny.jpg"
                    alt="پس زمینه 3"
                    class="cursor-pointer w-9 h-9 rounded" />
                  <img
                    src="https://github.com/Mhdi1381/images/raw/main/bg4-tiny.jpg"
                    alt="پس زمینه 4"
                    class="cursor-pointer w-9 h-9 rounded" />
                  <img
                    src="https://github.com/Mhdi1381/images/raw/main/bg5-tiny.jpg"
                    alt="پس زمینه 5"
                    class="cursor-pointer w-9 h-9 rounded" />
                  <img
                    src="https://github.com/Mhdi1381/images/raw/main/bg6-tiny.jpg"
                    alt="پس زمینه 6"
                    class="cursor-pointer w-9 h-9 rounded" />
                  <img
                    src="https://github.com/Mhdi1381/images/raw/main/bg7-tiny.jpg"
                    alt="پس زمینه 7"
                    class="cursor-pointer w-9 h-9 rounded" />
                  <img
                    src="https://github.com/Mhdi1381/images/raw/main/bg8-tiny.jpg"
                    alt="پس زمینه 8"
                    class="cursor-pointer w-9 h-9 rounded" />
                  <img
                    src="https://github.com/Mhdi1381/images/raw/main/bg9-tiny.jpg"
                    alt="پس زمینه 9"
                    class="cursor-pointer w-9 h-9 rounded" />
                  <img
                    src="https://github.com/Mhdi1381/images/raw/main/bg10-tiny.jpg"
                    alt="پس زمینه 10"
                    class="cursor-pointer w-9 h-9 rounded" />
                  <img
                    src="https://github.com/Mhdi1381/images/raw/main/bg11-tiny.jpg"
                    alt="پس زمینه 11"
                    class="cursor-pointer w-9 h-9 rounded" />
                  <img
                    src="https://github.com/Mhdi1381/images/raw/main/bg12-tiny.jpg"
                    alt="پس زمینه 12"
                    class="cursor-pointer w-9 h-9 rounded" />
                  <img
                    src="https://github.com/Mhdi1381/images/raw/main/bg13-tiny.jpg"
                    alt="پس زمینه 13"
                    class="cursor-pointer w-9 h-9 rounded" />
                  <img
                    src="https://github.com/Mhdi1381/images/raw/main/bg14-tiny.jpg"
                    alt="پس زمینه 14"
                    class="cursor-pointer w-9 h-9 rounded" />
                  <img
                    src="https://github.com/Mhdi1381/images/raw/main/bg15-tiny.jpg"
                    alt="پس زمینه 15"
                    class="cursor-pointer w-9 h-9 rounded" />
                </div>
              </div>
            </div>
          </div>
          <div tabindex="-1" class="resize-observer">
            <object
              aria-hidden="true"
              tabindex="-1"
              type="text/html"
              data="about:blank"></object>
          </div>
        </div>
        <div class="tooltip-arrow popover-arrow" style="left: 107px"></div>
      </div>
    </div> -->
  </div>
</template>

<script>
import $ from 'jquery'

export default {
  name: 'Setting',
  mounted() {
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
}
</script>
