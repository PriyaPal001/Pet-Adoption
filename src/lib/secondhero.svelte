<script>
  import { fade, fly, scale, slide } from "svelte/transition";
  let crData = [
    {
      id: 1,
      img: "https://i.pinimg.com/564x/26/c7/35/26c7355fe46f62d84579857c6f8c4ea5.jpg",
      title: "Cute Softy Cat",
      gender: "Female",
      status: false,
      tags: ["Healty", "House Trained", "Adult", "Smart"],
      location: "Navi Mumbai, India",
      price: "900",
    },
    {
      id: 2,
      img: "https://i.pinimg.com/564x/56/ce/5c/56ce5cf1623e3ee5d53ca85d156fcc98.jpg",
      title: "Swag hai Hamara",
      gender: "Female",
      status: true,
      tags: ["Healty", "Stylish", "Funny", "Smart"],
      location: "Pune , India",
      price: "1600",
    },
    {
      id: 3,
      img: "https://i.pinimg.com/564x/ca/9a/c8/ca9ac8953f9cdbeaf4b3c3737e24520d.jpg",
      title: "Orange Fufi",
      gender: "Male",
      status: false,
      tags: ["Healty", "Loving", "Energetic", "Always Hungry"],
      location: "Mumbai, India",
      price: "1200",
    },
  ];
  let i = 0;
  let changeI = () => {
    setInterval(() => {
      if (i == crData.length - 1) {
        i = 0;
      } else {
        i++;
      }
    }, 1600);
  };
  changeI();
</script>

<div class="bg-white py-6 sm:py-8 lg:py-12">
  <div class="mx-auto max-w-screen-2xl px-4 md:px-8">
    <div class="rounded-lg bg-gray-100 px-4 py-6 md:py-8 lg:py-12">
      <p
        class="mb-2 text-center font-semibold text-indigo-500 md:mb-3 lg:text-lg"
      >
        Introducing
      </p>

      <h2
        class="mb-4 text-center text-2xl font-bold text-gray-800 md:mb-6 lg:text-3xl"
      >
        Revolutionary way to build the web
      </h2>

      <p class="mx-auto max-w-screen-md text-center text-gray-500 md:text-lg">
        This is a section of some simple filler text, also known as placeholder
        text. It shares some characteristics of a real written text but is
        random or otherwise generated.
      </p>
    </div>
  </div>
</div>
<!-- <div class="carousel w-full h-96 p-10 m-10 ">
  <div id="slide1" class="carousel-item relative w-full">
    <img
      src="https://d1hjkbq40fs2x4.cloudfront.net/2016-07-16/files/cat-sample_1313-5.jpg"
      class="w-full"
    />
    <div
      class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2"
    >
      <a href="#slide4" class="btn btn-circle">❮</a>
      <a href="#slide2" class="btn btn-circle">❯</a>
    </div>
  </div>
  <div id="slide2" class="carousel-item relative w-full">
    <img src="https://wallpaperaccess.com/full/266770.jpg" class="w-full" />
    <div
      class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2"
    >
      <a href="#slide1" class="btn btn-circle">❮</a>
      <a href="#slide3" class="btn btn-circle">❯</a>
    </div>
  </div>
  <div id="slide3" class="carousel-item relative w-full">
    <img
      src="https://media.istockphoto.com/id/155096695/photo/homeless-kitten.jpg?s=612x612&w=0&k=20&c=bwfOxHPADtSpt0LGrEp0J8zCqBsWfLLalQsSB1pVom8="
      class="w-full"
    />
    <div
      class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2"
    >
      <a href="#slide2" class="btn btn-circle">❮</a>
      <a href="#slide4" class="btn btn-circle">❯</a>
    </div>
  </div>
  <div id="slide4" class="carousel-item relative w-full">
    <img
      src="https://st2.depositphotos.com/1265959/7648/i/950/depositphotos_76484803-stock-photo-a-poor-dog-behind-the.jpg"
      class="w-full"
    />
    <div
      class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2"
    >
      <a href="#slide3" class="btn btn-circle">❮</a>
      <a href="#slide1" class="btn btn-circle">❯</a>
    </div>
  </div>
</div> -->
<div class="flex  justify-evenly align-middle items-center">
  <div class="flex justify-start  mx-10 bg-white">
    <div class="h-80 md:w-[400px] md:h-[500px] carousel rounded-box ">
      <div class="carousel-item w-full ">
        {#key i}
          <img
            in:fade
            src={crData[i].img}
            class="w-full rounded-2xl "
            alt="Tailwind CSS Carousel component"
          />
        {/key}
      </div>
    </div>
  </div>
  <div>
    <div
      class="c_title relative text-left flex flex-col md:w-[450px] md:h-[350px]  rounded-xl  px-8 py-10 border-2 border-purple-700 shadow-xl shadow-purple-500 bg-fuchsia-50"
    >
      {#key i}
        <h2 class="text-2xl md:text-4xl font-bold text-gray-800" in:fade>
          {crData[i].title}
        </h2>
      {/key}

      <div class="mt-3 ">
        <div>Location : {crData[i].location}</div>
        <div>Gender : {crData[i].gender}</div>
      </div>
      <div class="mt-4 ">
        {#key i}
          <div in:slide>
            {#each crData[i].tags as tag}
              <span
                in:fade
                class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2"
              >
                {tag}
              </span>
            {/each}
          </div>
        {/key}
      </div>

      <div class="flex absolute bottom-3 justify-around mt-3  items-center">
        <div class="mx-5">
          <h2 class="text-slate-700 text-xl">
            Price : Rs.{crData[i].price} /-
          </h2>
        </div>
        <div class="card-actions justify-end">
          <button class="btn btn-primary">Buy Now</button>
        </div>
      </div>
    </div>
  </div>
</div>
