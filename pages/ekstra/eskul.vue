<template>
  <div class="bg-gray-100 py-8 body">
    <div class="container mx-auto p-4">
      <h1 class="text-3xl font-bold mb-4 text-center text-gray-900">Ekskul</h1>
      <p class="text-gray-600 mb-8 text-center">Ekstrakurikuler Sekolah</p>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
        <div v-for="activity in activities" :key="activity.title" class="bg-white rounded-lg shadow-lg overflow-hidden">
          <div class="relative">
            <img :src="activity.image" :alt="activity.title" class="w-full h-36 object-cover" />
            <div class="absolute inset-0 bg-black opacity-50"></div>
            <div class="absolute inset-0 flex items-center justify-center text-dark text-center p-4">
              <div>
                <h2 class="text-2xl teks-center font-semibold">{{ activity.title }}</h2>
                <p class="mt-2 text-lg">{{ activity.description }}</p>
              </div>
            </div>
          </div>

          <div class="p-6">
            <div class="flex items-center mb-4">
              <i class="fas fa-user text-orange-500 mr-2"></i>
              <span class="text-gray-700 font-semibold">{{ activity.creator }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activities: [
        {
          title: "Perisai diri",
          image: "https://i.pinimg.com/736x/51/ab/47/51ab47c504edf68c8bd7c69f77220b04.jpg",
        },
        {
          title: "Seni Tari",
          image: "https://i.pinimg.com/736x/e5/03/e5/e503e58eb22102d10723a44218b3b587.jpg",
        },
        {
          title: "Osis",
          image: "https://i.pinimg.com/736x/f6/67/1f/f6671f74b2d7dc78f6017956d8b02695.jpg",
        },
        {
          title: "Pks",
          image: "https://i.pinimg.com/736x/ea/25/4b/ea254b6e53451f5744f98d1378a8d5a4.jpg",
        },
        {
          title: "Pramuka",
          image: "https://images.bisnis.com/posts/2023/11/14/1714300/pramuka_1_1699953189.jpeg",
        },
        {
          title: "Badminton",
          image: "https://i.pinimg.com/736x/54/3b/9e/543b9e592eecc7cc457642ec421a708f.jpg",
        },
         {
          title: "Futsal",
          image: "https://i.pinimg.com/736x/dc/d9/1a/dcd91ac50fb171ca3cbe8294b34d2d1c.jpg",
        },
          {
          title: "Sepak Bola",
          image: "https://i.pinimg.com/736x/dc/d9/1a/dcd91ac50fb171ca3cbe8294b34d2d1c.jpg",
        },
         {
          title: "Irma",
          image: "https://i.pinimg.com/736x/59/e5/03/59e503fadab5b450ec9a76fff650a8f2.jpg",
        },
         {
          title: "Volly",
          image: "https://i.pinimg.com/736x/8b/47/9b/8b479b145f5d43ce0f33a0da279863a7.jpg",
        },
         {
          title: "English Club",
          image: "https://i.pinimg.com/736x/36/f9/ca/36f9ca14076d3baf2921e5c944473da0.jpg",
        },
         {
          title: "Paskibra",
          image: "https://i.pinimg.com/736x/9c/56/28/9c56285c0289ef6e299884feeaa05ece.jpg",
        },
      ],
    };
  },
};
</script>

<style scoped>
.body {
  margin-top: 50px;
}

.bg-gray-100 {
  background-color: #4298cd99;
}

.container {
  max-width: 1280px;
}

.text-center {
  text-align: center;
}

.text-white {
  color: #0c0c0c;
}

.relative {
  position: relative;
}

.absolute {
  position: absolute;
}

.bg-black {
  background-color: #000;
}

.opacity-50 {

  opacity: 0.5;
}

.w-full {
  width: 100%;
}

.mt-4 {
  margin-top: 1rem;
}

button {
  font-weight: 600;
}

button:hover {
  background-color: #4b5563;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
}

button {
  transition: background-color 0.3s ease;
}

.py-8 {
  padding-top: 2rem;
  padding-bottom: 2rem;
}

.gap-8 {
  gap: 2rem;
}

.p-4 {
  padding: 1rem;
}

.p-6 {
  padding: 1.5rem;
}

.mb-8 {
  margin-bottom: 2rem;
}

.mb-4 {
  margin-bottom: 1rem;
}

.mt-2 {
  margin-top: 0.5rem;
}


.text-lg {
  font-size: 1.125rem; 
}

.relative .absolute {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>