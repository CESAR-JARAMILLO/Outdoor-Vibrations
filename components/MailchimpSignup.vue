<template>
  <validation-observer
    v-slot="{ invalid }"
    ref="subscribe"
    tag="form"
    class="w-full max-w-lg"
    @submit.prevent="!invalid && subscribe()"
  >
    <div class="flex items-start">
      <div class="w-2/3">
        <validation-provider
          v-slot="{ errors }"
          rules="required|email"
          :bails="false"
          tag="div"
          name="Email"
        >
          <input
            id="grid-email"
            v-model="form.email"
            class="shadow bg-gray-300 appearance-none border-2 border-gray-300 w-full mb-2 py-2 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-primary-300"
            type="email"
            placeholder="Email"
          >
          <ul v-if="errors.length" class="list-disc list-inside text-red-500 m-2">
            <li :v-for="error in errors" class="leading-none">
              <small>{{ error }}</small>
            </li>
          </ul>
        </validation-provider>
        <p class="text-gray-600 text-xs px-2">
          Don't worry, we don't like spam either!
        </p>
      </div>
      <div class="w-1/3 pl-2">
        <button
          type="submit"
          class="btn-primary rounded"
          :class="{ disabled: invalid }"
          :disabled="invalid"
        >
          <span class="mr-2">Subscribe</span>
        </button>
      </div>
    </div>
  </validation-observer>
</template>
