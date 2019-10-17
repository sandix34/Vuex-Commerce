<template>
  <div class="flex justify-center">
    <form @submit.prevent="create" class="shadow-2xl p-16 w-2/4 border-gray-100">
      <div class="flex flex-col">
        <label for="id">ID</label>
        <input
          type="text"
          class="border border-gray-400 mb-4 p-1"
          id="id"
          placeholder="Enter id (ISBN)"
          v-model="book.id"
        />
      </div>
      <div class="flex flex-col">
        <label for="title">Title</label>
        <input
          type="text"
          class="border border-gray-400 mb-4 p-1"
          id="title"
          placeholder="Enter title"
          v-model="book.title"
        />
      </div>
      <div class="flex flex-col">
        <label for="firstName">First name</label>
        <input
          type="text"
          class="border border-gray-400 mb-4 p-1"
          id="firstName"
          placeholder="Author first name"
          v-model="book.author.firstName"
        />
      </div>
      <div class="flex flex-col">
        <label for="lastName">Last name</label>
        <input
          type="text"
          class="border border-gray-400 mb-4 p-1"
          id="lastName"
          placeholder="Author last name"
          v-model="book.author.lastName"
        />
      </div>
      <div class="flex flex-col">
        <label for="publisher">Publisher</label>
        <input
          type="text"
          class="border border-gray-400 mb-4 p-1"
          id="publisher"
          placeholder="Publisher"
          v-model="book.publisher"
        />
      </div>
      <div class="flex flex-col">
        <label for="year">Year</label>
        <input
          type="number"
          class="border border-gray-400 mb-4 p-1"
          id="year"
          placeholder="Publication year"
          v-model="book.year"
        />
      </div>
      <div class="flex flex-col">
        <label for="price">Price</label>
        <input 
          type="text" 
          class="border border-gray-400 mb-4 p-1" 
          id="price" 
          placeholder="Price"
          v-model="book.price"
         />
      </div>
      <div class="flex flex-col">
        <label for="image">Image</label>
        <input 
          type="text" 
          class="border border-gray-400 mb-4 p-1" 
          id="image" 
          placeholder="Image"
          v-model="book.image" 
        />
      </div>
      <button
        type="submit"
        class="border rounded bg-blue-500 py-2 px-4 text-white font-medium tracking-wide"
      >Submit</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      book: {
        title: "",
        author: {
          firsName: "",
          lastName: ""
        },
        publisher: "",
        year: "",
        price: "",
        image: ""
      }
    }
  },
  methods: {
    create() {
      console.log(this.book);
      this.$store.dispatch("createProduct", this.book);
    }
  }
};
</script>
