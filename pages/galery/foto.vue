<template>
  <div class="bg-gray-100 py-8 body">
    <div class="container mx-auto p-4">
      <h1 class="text-3xl font-bold mb-4 text-center text-gray-900">
        Galeri Sekolah
      </h1>
      <p class="text-gray-600 mb-8 text-center">Momen-Momen Sekolah Kami</p>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
        <div v-for="image in images" :key="image.id" class="relative group">
          <img
            :src="image.src"
            :alt="image.alt"
            class="w-full h-64 object-cover rounded-lg shadow-lg cursor-pointer transition-transform transform group-hover:scale-105"
            @click="openModal(image.src)"
          />
          <div
            class="absolute bottom-0 left-0 w-full bg-black bg-opacity-60 text-white text-center py-2"
          >
            <p>{{ image.title }}</p>
          </div>
        </div>
      </div>
    </div>
    <div
      v-if="isModalOpen"
      class="fixed inset-0 bg-black bg-opacity-70 flex justify-center items-center z-50"
      @click="closeModal"
    >
      <img :src="modalImage" class="max-w-full max-h-full" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isModalOpen: false,
      modalImage: "",
      images: [
        {
          id: 1,
          title: "Kegiatan Safety Reading",
          src: "https://asset.kompas.com/crops/HVv0q6xGbJDFT4SQXXEb3VWoWDg=/0x0:0x0/1200x800/data/photo/2024/07/24/66a07447032c2.jpg",
          alt: "Belajar Mengajar",
        },
        {
          id: 2,
          title: "Kegiatan Olahraga",
          src: "https://assets.pikiran-rakyat.com/crop/0x0:0x0/1200x675/photo/2024/07/14/1467207474.png",
          alt: "Olahraga",
        },
        {
          id: 3,
          title: "Kegiatan Pramuka",
          src: "https://images.bisnis.com/posts/2023/11/14/1714300/pramuka_1_1699953189.jpeg",
          alt: "Pramuka",
        },
        {
          id: 4,
          title: "Pentas Seni",
          src: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSYIrYvzqN8N274xcE-Tcn8k2RSWlHVLiaEeg&s",
          alt: "Pentas Seni",
        },
        {
          id: 5,
          title: "Kegiatan Hari Guru",
          src: "https://d.rapidcdn.app/snapinsta?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1cmwiOiJodHRwczovL3Njb250ZW50LWZyYTUtMS5jZG5pbnN0YWdyYW0uY29tL3YvdDUxLjI5MzUwLTE1LzQ2ODM4Mjg4Ml80NDE4MDA0NDg3MjUxMTRfNjU3NTM1NDkyNTI5MjY1NDk2M19uLndlYnA_c3RwPWRzdC1qcGdfZTM1X3M2NDB4NjQwX3NoMC4wOF90dDYmZWZnPWV5SjJaVzVqYjJSbFgzUmhaeUk2SW1sdFlXZGxYM1Z5YkdkbGJpNHhORE01ZURrMU9TNXpaSEl1WmpJNU16VXdMbVJsWm1GMWJIUmZhVzFoWjJVaWZRJl9uY19odD1zY29udGVudC1mcmE1LTEuY2RuaW5zdGFncmFtLmNvbSZfbmNfY2F0PTEwMiZfbmNfb2hjPXNJWFEtSjEwYVlFUTdrTnZnRzBEejNsJl9uY19naWQ9YzU0NTEyN2FmMGY3NDM3NThkMWJiNzA1YWI1ZjEzNzYmZWRtPUFQczE3Q1VCQUFBQSZjY2I9Ny01Jm9oPTAwX0FZQTlqMlFwcWV6SlJWUDZOak95MjFiblFtZWN5dWFqbEZ0ZDFFWE1tTXpoQXcmb2U9Njc3QkU4RkQmX25jX3NpZD0xMGQxM2IiLCJmaWxlbmFtZSI6IlNuYXBpbnN0YS5hcHBfdGh1bWJfNDY4MzgyODgyXzQ0MTgwMDQ0ODcyNTExNF82NTc1MzU0OTI1MjkyNjU0OTYzX24ud2VicCJ9.qdovQDc-Q2FKAmdH0E3dsQU_pjCwdXyn7Hu-Yq3ePR8",
          alt: "Paduan Suara",
        },
        {
          id: 6,
          title: "Kegiatan Upacara Bendera",
          src: "https://d.rapidcdn.app/snapinsta?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1cmwiOiJodHRwczovL3Njb250ZW50LXdhdzItMi5jZG5pbnN0YWdyYW0uY29tL3YvdDUxLjI5MzUwLTE1LzQ2OTAyMjUyM18xMjY2MjUwNzM0NjE4MTUxXzYzOTkyODA2Nzc1MjMzMTQ2NDJfbi53ZWJwP3N0cD1kc3QtanBnX2UzNV9zNjQweDY0MF9zaDAuMDhfdHQ2JmVmZz1leUoyWlc1amIyUmxYM1JoWnlJNkltbHRZV2RsWDNWeWJHZGxiaTR4TkRNNWVEazFPUzV6WkhJdVpqSTVNelV3TG1SbFptRjFiSFJmYVcxaFoyVWlmUSZfbmNfaHQ9c2NvbnRlbnQtd2F3Mi0yLmNkbmluc3RhZ3JhbS5jb20mX25jX2NhdD0xMDcmX25jX29oYz1LVkd5WjNydzNhQVE3a052Z0hBM3lSYyZfbmNfZ2lkPWU4NGQ5MjYxZWUzMzQwNWNhMmMxNDdlZmNkOGViY2E1JmVkbT1BUHMxN0NVQkFBQUEmY2NiPTctNSZvaD0wMF9BWURVVkJqdTZ6Vm1TM05BR2tzazROZWFsMm5ERkVJYTA1QUh6WEhuQTR3a3l3Jm9lPTY3N0JCREFDJl9uY19zaWQ9MTBkMTNiIiwiZmlsZW5hbWUiOiJTbmFwaW5zdGEuYXBwX3RodW1iXzQ2OTAyMjUyM18xMjY2MjUwNzM0NjE4MTUxXzYzOTkyODA2Nzc1MjMzMTQ2NDJfbi53ZWJwIn0.yI9ch_qfiUevcdJ1h8nsyL9rDKmhuO5N1s9G0iiZOeM",
          alt: "Hari Guru",
        },
        {
          id: 7,
          title: "Kegiatan Ujian Sekolah",
          src: "https://d.rapidcdn.app/snapinsta?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1cmwiOiJodHRwczovL3Njb250ZW50LWJydTItMS5jZG5pbnN0YWdyYW0uY29tL3YvdDUxLjI5MzUwLTE1LzQ2OTcyMjM2OF85ODY2NDIzNTM0OTI2NTRfODY4MDIwNjM2MjkwOTE5NzE1X24ud2VicD9zdHA9ZHN0LWpwZ19lMzVfczY0MHg2NDBfc2gwLjA4X3R0NiZlZmc9ZXlKMlpXNWpiMlJsWDNSaFp5STZJbWx0WVdkbFgzVnliR2RsYmk0eE5ETTVlRGsxT1M1elpISXVaakk1TXpVd0xtUmxabUYxYkhSZmFXMWhaMlVpZlEmX25jX2h0PXNjb250ZW50LWJydTItMS5jZG5pbnN0YWdyYW0uY29tJl9uY19jYXQ9MTEwJl9uY19vaGM9RzB6eURfQ09aSXdRN2tOdmdFRzNzemYmX25jX2dpZD04NmM3NjFjMzgxNWY0N2RiYTYzYjU0NDQyNWQ0YmJkZCZlZG09QVBzMTdDVUJBQUFBJmNjYj03LTUmb2g9MDBfQVlBeXRrLWJ6S0Q4Y05DcVJHRXRURGsxa3UxUjZUMVNoajRBVUJGNzhyLVh6USZvZT02NzdCQjhBMSZfbmNfc2lkPTEwZDEzYiIsImZpbGVuYW1lIjoiU25hcGluc3RhLmFwcF90aHVtYl80Njk3MjIzNjhfOTg2NjQyMzUzNDkyNjU0Xzg2ODAyMDYzNjI5MDkxOTcxNV9uLndlYnAifQ.GqkM4pKWQ4GVBN58u68s_PQWO46xJnamPa0iUzK009M",
          alt: "Kerohanian",
        },
        {
          id: 8,
          title: "Sosialisasi Polisi",
          src: "https://www.newstasikmalaya.com/storage/kapolsek-cibeureum-berikan-penyuluhan.jpg",
          alt: "Kerohanian",
        },
        {
          id: 9,
          title: "Jadwal Memakai Seragam",
          src: "https://d.rapidcdn.app/snapinsta?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1cmwiOiJodHRwczovL3Njb250ZW50LWxocjYtMi5jZG5pbnN0YWdyYW0uY29tL3YvdDM5LjMwODA4LTYvNDU0NjA2MjI5XzE3OTc1ODEyNjcwNzMzNjEyXzU0MDIyNzAyMjU3MjIwODc3OTRfbi5qcGc_c3RwPWRzdC1qcGdfZTM1X3M2NDB4NjQwX3NoMC4wOF90dDYmZWZnPWV5SjJaVzVqYjJSbFgzUmhaeUk2SW1sdFlXZGxYM1Z5YkdkbGJpNHhORFF3ZURFME5EQXVjMlJ5TG1Zek1EZ3dPQzVrWldaaGRXeDBYMmx0WVdkbEluMCZfbmNfaHQ9c2NvbnRlbnQtbGhyNi0yLmNkbmluc3RhZ3JhbS5jb20mX25jX2NhdD0xMDAmX25jX29oYz1sc1hXUHU5ZmIza1E3a052Z0hfWDZKSCZfbmNfZ2lkPTliNjNiOTRiMDdjYzRkNmJiYzcxYjljN2ZkNTA0ZTI3JmVkbT1BUHMxN0NVQUFBQUEmY2NiPTctNSZvaD0wMF9BWUNqYU1fYmVTQmI1eFV1VUtEZjd2aGZjcU5TdWpkc2VhSEpqRXgyeG1iVzZBJm9lPTY3N0JFNjk4Jl9uY19zaWQ9MTBkMTNiIiwiZmlsZW5hbWUiOiJTbmFwaW5zdGEuYXBwX3RodW1iXzQ1NDYwNjIyOV8xNzk3NTgxMjY3MDczMzYxMl81NDAyMjcwMjI1NzIyMDg3Nzk0X24uanBnIn0.d0p9ksZhjgwmLQLCguS2LQHtx1BMexIqQCKqLY0o1R4",
          alt: "Kerohanian",
        },
      ],
    };
  },
  methods: {
    openModal(imageSrc) {
      this.modalImage = imageSrc;
      this.isModalOpen = true;
    },
    closeModal() {
      this.isModalOpen = false;
      this.modalImage = "";
    },
  },
};
</script>

<style scoped>
.body {
  margin-top: 50px;
}

.bg-gray-100 {
  background-color: #ffffff;
}

.container {
  max-width: 1280px;
}

.text-center {
  text-align: center;
}

.text-white {
  color: #ffffff;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
}

.cursor-pointer {
  cursor: pointer;
}

.group:hover .group-hover\:scale-105 {
  transform: scale(1.05);
}

.group-hover\:scale-105 {
  transition: transform 0.3s ease;
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

.w-full {
  width: 100%;
}

.h-64 {
  height: 16rem;
}

.text-gray-600 {
  color: #6c6969;
}

.bg-black {
  background-color: #fffdfd;
}

.bg-opacity-60 {
  background-opacity: 0.6;
}

.fixed {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}

.z-50 {
  z-index: 50;
}

.max-w-full {
  max-width: 100%;
}

.max-h-full {
  max-height: 100%;
}
</style>
