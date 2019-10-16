<template>
  <div class="flex justify-center">
    <form class="shadow-2xl p-16 w-2/4 border-gray-100">
      <div class="flex flex-col">
        <label for="title">Title</label>
        <input type="text" class="border border-gray-400 mb-4 p-1" id="title" placeholder="Enter title" />
      </div>
      <div class="flex flex-col">
        <label for="firstName">First name</label>
        <input type="text" class="border border-gray-400 mb-4 p-1" id="firstName" placeholder="Author first name" />
      </div>
      <div class="flex flex-col">
        <label for="lastName">Last name</label>
        <input type="text" class="border border-gray-400 mb-4 p-1" id="lastName" placeholder="Author last name" />
      </div>
      <div class="flex flex-col">
        <label for="publisher">Publisher</label>
        <input type="text" class="border border-gray-400 mb-4 p-1" id="publisher" placeholder="Publisher" />
      </div>
      <div class="flex flex-col">
        <label for="year">Year</label>
        <input type="number" class="border border-gray-400 mb-4 p-1" id="year" placeholder="Publication year" />
      </div>
      <div class="flex flex-col">
        <label for="price">Price</label>
        <input type="text" class="border border-gray-400 mb-4 p-1" id="price" placeholder="Price" />
      </div>
      <div class="flex flex-col">
        <label for="image">Image</label>
        <input type="text" class="border border-gray-400 mb-4 p-1" id="image" placeholder="Image" />
      </div>
      <button type="submit" class="border rounded bg-blue-500 py-2 px-4 text-white font-medium tracking-wide">Submit</button>
    </form>
  </div>
</template>

<script>
export default {};
</script>
