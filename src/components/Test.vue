<template>
  <div class="grid grid-cols-1 md:grid-cols-3 h-screen">
    <!-- Left Panel -->
    <div
      class="hidden md:flex flex-col w-full md:w-1/3 bg-blue-800 p-6 md:justify-start md:items-start md:h-full">
      <img src="../assets/Logo.png" alt="Logo" class="w-32 h-24 mb-4" />
      <h1 class="text-xl md:text-2xl font-bold text-white text-center">Login to XXX</h1>
    </div>
    
    <!-- Right Panel -->
    <div class="flex flex-col justify-center items-center w-full md:w-100 p-6 md:pl-16">
      <div class="bg-white p-6 md:p-8 rounded shadow-md w-full max-w-md md:ml-auto">
        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="email">
            Registered email or phone
          </label>
          <input
            class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
            id="email"
            type="text"
            placeholder="Enter your email or phone" />
        </div>
        <div class="mb-6">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
            Password
          </label>
          <input
            class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 mb-3 leading-tight focus:outline-none focus:shadow-outline"
            id="password"
            type="password"
            placeholder="Enter your password" />
        </div>
        <div class="flex flex-col md:flex-row items-center justify-between mb-4">
          <a class="text-sm text-blue-500 hover:text-blue-800 mb-2 md:mb-0" href="#">Forgot Password?</a>
          <a class="text-sm text-blue-500 hover:text-blue-800" href="#">Trouble logging in? Get help</a>
        </div>
        <button
          class="bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline w-full"
          type="button">
          Login
        </button>
        <div class="text-center mt-4">
          <p class="text-sm text-gray-600">
            Don't have an account yet?
            <a href="#" class="text-green-500">Register</a>
          </p>
        </div>
      </div>
      <button
        class="mt-4 bg-white border border-gray-300 text-gray-700 font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline flex items-center w-full max-w-md md:ml-auto justify-center"
        type="button">
        <span class="mr-2">Login with passkey</span>
        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4"></path>
        </svg>
      </button>
    </div>
  </div>
</template>