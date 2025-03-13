<template>
  <div
    class="grid grid-cols-1 md:grid-cols-3 h-screen transition-all duration-300 dark:bg-white-900">
    <!-- Kolom Kiri -->
    <div
      class="hidden md:flex flex-col w-full md:w-2/4 bg-sky-900 p-6 md:justify-start md:items-start md:h-full">
      <img
        src="../assets/Logo.png"
        alt="Company Logo"
        class="w-50 h-35 mb-4 animate-fade-in" />
      <h1
        class="text-xl md:text-2xl font-bold text-white text-left text-center w-50">
        Login to XXX Epayment
      </h1>
    </div>
    <!-- Kolom Kanan-->
    <div
      class="flex flex-col justify-center items-center w-full max-w-md md:ml-auto">
      <div
        class="bg-gray-100 dark:bg-gray-800 p-6 md:p-8 rounded shadow-md w-full max-w-md md:ml-auto">
        <div class="mb-4">
          <label
            class="block text-black dark:text-gray-300 text-sm font-bold mb-2"
            for="email">
            Registered email or phone
          </label>
          <input
            class="shadow appearance-none border-b-2 border-gray-400 w-full py-2 px-3 text-gray-700 dark:text-white leading-tight focus:outline-none focus:border-transparent hover:border-green-500 transition-all duration-700 focus:ring-0"
            id="email"
            type="email"
            autocomplete="email"
            placeholder="Enter your Email"
            aria-label="Enter your registered email or phone" />
        </div>
        <div class="mb-6">
          <label
            class="block text-black dark:text-gray-300 text-sm font-bold mb-2"
            for="password">
            Password
          </label>
          <input
            class="shadow appearance-none border-b-2 border-gray-400 w-full py-2 px-3 text-gray-700 dark:text-white leading-tight focus:outline-none focus:border-transparent hover:border-green-500 transition-all duration-700 focus:ring-0"
            id="password"
            type="password"
            autocomplete="off"
            placeholder="Enter your Password"
            aria-label="Enter your password" />
        </div>
        <div
          class="flex flex-col md:flex-row items-center justify-between mb-4">
          <a
            class="text-sm text-blue-500 hover:text-blue-800 transition-all duration-300 mb-2 md:mb-0"
            href="#"
            >Forgot Password?</a
          >
          <a
            class="text-sm text-blue-500 hover:text-blue-800 transition-all duration-300"
            href="#"
            >Trouble logging in? Get help</a
          >
        </div>
        <button
          class="bg-green-500 hover:bg-green-700 transition-all duration-300 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline w-full flex justify-center items-center"
          type="button"
          aria-label="Login to your account">
          <span>Login</span>
          <svg
            class="w-5 h-5 ml-2 animate-spin hidden"
            id="loading-spinner"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg">
            <circle
              class="opacity-25"
              cx="12"
              cy="12"
              r="10"
              stroke="currentColor"
              stroke-width="4"></circle>
            <path
              class="opacity-75"
              fill="currentColor"
              d="M4 12a8 8 0 018-8v8H4z"></path>
          </svg>
        </button>
        <div class="text-center mt-4">
          <p class="text-sm text-gray-600 dark:text-gray-300">
            Don't have an account yet?
            <a href="#" class="text-green-500 hover:underline">Register</a>
          </p>
        </div>
      </div>
      <button
        class="mt-10 bg-gray-100 dark:bg-gray-700 border border-gray-300 dark:border-gray-600 text-white-700 dark:text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline flex items-center w-full max-w-md md:ml-auto justify-center hover:bg-green-100 dark:hover:bg-gray-600 transition-all duration-300"
        type="button"
        aria-label="Login with passkey">
        <span class="mr-2">Login with passkey</span>
        <svg
          class="w-4 h-4"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg">
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M12 4v16m8-8H4"></path>
        </svg>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    handleLogin() {
      const spinner = document.getElementById("loading-spinner");
      spinner.classList.remove("hidden");
      setTimeout(() => {
        spinner.classList.add("hidden");
        alert("Login successful");
      }, 2000);
    },
  },
};
</script>
