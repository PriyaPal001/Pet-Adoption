<script>
    let petdetails = {
        name: "",
        age: "",
        breed: "",
        gender: "",
        color: "",
        weight: "",
        description: "",
        image_url: "",
        pet_type: "",
        location: "",
        owner_number: "",
    };

    let handledata=()=>{

    }
</script>

<h1 class="">Pet Details</h1>

<section class="relative flex flex-wrap lg:h-screen lg:items-center">
    <div class="w-full px-4 py-12 sm:px-6 sm:py-16 lg:w-1/2 lg:px-8 lg:py-24">
        <form
        on:submit|preventDefault={handledata}
        class="mt-0 grid grid-cols-6 gap-6 border-2 border-blue-900 py-14 px-5 md:px-20 rounded-2xl"
        >
          <div class="col-span-8 sm:col-span-3">
            <label
              for="Name"
              class="block text-sm font-medium text-gray-700"
            >
             Name
            </label>

            <input
            bind:value={petdetails.name}
              type="text"
              id="FirstName"
              name="first_name"
              class="mt-1 w-full rounded-md border-gray-200 bg-white text-sm text-gray-700 shadow-sm"
            />
          </div>

          <div class="col-span-8 sm:col-span-3">
            <label
              for="Age"
              class="block text-sm font-medium text-gray-700"
            >
              Age
            </label>

            <input
            bind:value={petdetails.age}
              type="text"
              id="LastName"
              name="last_name"
              class="mt-1 w-full rounded-md border-gray-200 bg-white text-sm text-gray-700 shadow-sm"
            />
          </div>

          <div class="col-span-8 sm:col-span-3">
            <label
              for="Breed"
              class="block text-sm font-medium text-gray-700"
            >
              Breed
            </label>

            <input
            bind:value={petdetails.breed}
              type="text"
              id="Breed"
              name="breed"
              class="mt-1 w-full rounded-md border-gray-200 bg-white text-sm text-gray-700 shadow-sm"
            />
          </div>

          <div class="col-span-8 sm:col-span-3">
            <label
              for="Gender"
              class="block text-sm font-medium text-gray-700"
            >
              Gender
            </label>

            <input
            bind:value={petdetails.gender}
              type="text"
              id="Gender"
              name="gender"
              class="mt-1 w-full rounded-md border-gray-200 bg-white text-sm text-gray-700 shadow-sm"
            />
          </div>

          <div class="col-span-8 sm:col-span-3">
            <label
              for="Color"
              class="block text-sm font-medium text-gray-700"
            >
              Color
            </label>

            <input
            bind:value={petdetails.color}
              type="text"
              id="Color"
              name="color"
              class="mt-1 w-full rounded-md border-gray-200 bg-white text-sm text-gray-700 shadow-sm"
            />
          </div>

          <div class="col-span-8 sm:col-span-3">
            <label
              for="Weight"
              class="block text-sm font-medium text-gray-700"
            >
              Weight
            </label>

            <input
            bind:value={petdetails.weight}
              type="text"
              id="Weight"
              name="weight"
              class="mt-1 w-full rounded-md border-gray-200 bg-white text-sm text-gray-700 shadow-sm"
            />

          </div>

          <div class="col-span-8 sm:col-span-3">
            <label
              for="Description"
              class="block text-sm font-medium text-gray-700"
            >
              Description
            </label>

            <input
            bind:value={petdetails.description}
              type="text"
              id="Description"
              name="description"
              class="mt-1 w-full rounded-md border-gray-200 bg-white text-sm text-gray-700 shadow-sm"
            />

          </div>  

          <div class="col-span-8 sm:col-span-3">
            <label
              for="Image"
              class="block text-sm font-medium text-gray-700"
            >
              Image Url
            </label>

            <input
            bind:value={petdetails.image_url}
              type="url"
              id="Image"
              name="image"
              class="mt-1 w-full rounded-md border-gray-200 bg-white text-sm text-gray-700 shadow-sm"
            />
          </div>

          <div class="col-span-8 sm:col-span-3">
            <label
              for="PetType"
              class="block text-sm font-medium text-gray-700"
            >
              Pet Type
            </label>

            <input
            bind:value={petdetails.pet_type}
              type="text"
              id="PetType"
              name="pet_type"
              class="mt-1 w-full rounded-md border-gray-200 bg-white text-sm text-gray-700 shadow-sm"
            />
          </div>

          <div class="col-span-8 sm:col-span-3">
            <label
              for="OwnerNumber"
              class="block text-sm font-medium text-gray-700"
            >
              Owner Number
            </label>

            <input
            bind:value={petdetails.owner_number}
              type="text"
              id="OwnerNumber"
              name="owner_number"
              class="mt-1 w-full rounded-md border-gray-200 bg-white text-sm text-gray-700 shadow-sm"
            />
          </div>

          <div class="col-span-8 sm:col-span-3">
            <label
              for="Location"
              class="block text-sm font-medium text-gray-700"
            >
              Location
            </label>

            <input
            bind:value={petdetails.location}
              type="text"
              id="Location"
              name="location"
              class="mt-1 w-full rounded-md border-gray-200 bg-white text-sm text-gray-700 shadow-sm"
            />
          <div class="col-span-8 sm:flex sm:items-center sm:gap-4 ">
            <button
            type="submit"
              class="inline-block shrink-0 rounded-md border border-purple-700 bg-purple-700 px-12 py-3 text-sm font-medium text-white transition hover:bg-purple-400 hover:text-white-600 focus:outline-none focus:ring active:text-blue-500"
            >
              Post
            </button>
          </div>

        </div>


        </form>
    </div>
  
    <div class="relative h-64 w-full sm:h-96 lg:h- lg:w-1/3 m-20 ">
      <img
        alt="Welcome"
        src="https://images.unsplash.com/photo-1630450202872-e0829c9d6172?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=774&q=80"
        class="absolute inset-0 h-full w-full object-cover rounded-2xl"
      />
    </div>
  </section>

  <style>
    label{
      font-size: 1.2rem;
      color: #f3f4f6;

    }

    input{
      font-size: 1.2rem;
      padding: 5px;

    }
  </style>
  