<script setup>
// import HelloWorld from './components/HelloWorld.vue'
import { ref, computed } from "vue";

const expression = ref("");
const result = computed(() => math.evaluate(expression.value));

function appendNumber(number) {
  if (number == "AC") {
    expression.value = "";
  } else {
    expression.value += String(number);
  }
}
</script>

<template>
  <main class="flex items-center justify-center fs-1 mt-10 font-monospace text-lg">
    <div class="w-72 bg-gray-800 rounded p-3">
      <form class="rounded h-24">
        <input
          v-model="expression"
          class="text-right w-full bg-gray-800 rounded 	
border-transparent"
        />
        <p class="text-right p-4">{{ result }}</p>
      </form>
      <div class="rounded text-white grid grid-cols-4 gap-2 mt-2">
        <button
          @click="appendNumber('AC')"
          class="col-span-3 rounded-full bg-blue-500 p-4 text-red-700 bg-gray-700"
        >
          AC
        </button>
        <button
          @click="appendNumber('/')"
          class="rounded-full text-green-600 bg-gray-700"
        >
          &divide;
        </button>

        <button
          @click="appendNumber('7')"
          class="rounded-full bg-gray-700"
        >
          7
        </button>
        <button
          @click="appendNumber('8')"
          class="rounded-full p-4 bg-gray-700"
        >
          8
        </button>
        <button
          @click="appendNumber('9')"
          class="rounded-full bg-gray-700"
        >
          9
        </button>
        <button
          @click="appendNumber('*')"
          class="rounded-full text-green-600 bg-gray-700"
        >
          &times;
        </button>
        <button
          @click="appendNumber('4')"
          class="rounded-full p-4 bg-gray-700"
        >
          4
        </button>
        <button
          @click="appendNumber('5')"
          class="rounded-full bg-gray-700"
        >
          5
        </button>
        <button
          @click="appendNumber('6')"
          class="rounded-full bg-gray-700"
        >
          6
        </button>
        <button
          @click="appendNumber('-')"
          class="rounded-full text-green-600 bg-gray-700"
        >
          &minus;
        </button>
        <button
          @click="appendNumber('1')"
          class="rounded-full p-4 bg-gray-700"
        >
          1
        </button>
        <button
          @click="appendNumber('2')"
          class="rounded-full bg-gray-700"
        >
          2
        </button>
        <button
          @click="appendNumber('3')"
          class="rounded-full bg-gray-700"
        >
          3
        </button>
        <button
          @click="appendNumber('+')"
          class="rounded-full text-green-600 bg-gray-700"
        >
          &plus;
        </button>
        <button
          @click="appendNumber('0')"
          class="rounded-full bg-gray-700"
        >
          0
        </button>
        <button
          @click="appendNumber('=')"
          class="col-span-3 rounded-full p-4 bg-green-700"
        >
          &equals;
        </button>
      </div>
    </div>
  </main>
</template>

<style scoped>
/* header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
} */
</style>
