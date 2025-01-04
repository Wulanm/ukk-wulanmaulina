<template>
   <div class="welcome-page">
    <div
      id="carouselExampleSlidesOnly"
      class="carousel slide"
      data-bs-ride="carousel"
    >
      <div class="carousel-inner">
        <div class="carousel-item active">
          <div class="carousel-content">
            <img
              src="/assets/img/bacground.jpg"
              class="d-block w-100"
              alt="Background Image"
            />
  <div class="prestasi-siswa">
    <h1>Prestasi Siswa</h1>
    <div class="grid">
      <div v-for="(prestasi, index) in prestasiList" :key="index" class="card">
        <h3>{{ prestasi.nama }}</h3>
        <P><strong>Kelas:</strong> {{ prestasi.kelas }}</P>
        <p><strong>Bidang:</strong> {{ prestasi.bidang }}</p>
        <p><strong>Tahun:</strong> {{ prestasi.tahun }}</p>
        <p><strong>Deskripsi:</strong> {{ prestasi.deskripsi }}</p>
      </div>
    </div>
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
      prestasiList: [
        {
          nama: 'Zulpa Agustin',
          kelas: '12 PPLG 4',
          bidang: 'Matematika',
          tahun: 2024,
          deskripsi: 'Juara 1 Olimpiade Matematika Nasional.',
        },
        {
          nama: 'Wulan Maulina',
          kelas: '12 PPLG 4',
          bidang: 'Matematika',
          tahun: 2024,
          deskripsi: 'Juara 1 Olimpiade Matematika Nasional.',
        },
        {
          nama: 'Jian Kamil',
          kelas: '12 PPLG 4',
          bidang: 'Prisai Diri',
          tahun: 2024,
          deskripsi: 'Juara 1.',
        },
        {
          nama: 'Agistina',
          kelas: '12 PPLG 4',
          bidang: 'Matematika',
          tahun: 2024,
          deskripsi: 'Juara 1 Olimpiade Matematika Nasional.',
        },
         {
          nama: 'Melanie',
          kelas: '12 PPLG 4',
          bidang: 'Matematika',
          tahun: 2024,
          deskripsi: 'Juara 1 Olimpiade Matematika Nasional.',
        },
         {
          nama: 'Ziankha',
          kelas: '12 PPLG 4',
          bidang: 'Matematika',
          tahun: 2024,
          deskripsi: 'Juara 1 Olimpiade Matematika Nasional.',
        },
      ],
    };
  },
};
</script>

<style scoped>
.carousel-content img {
  max-height: 600px;
  width: 100%;
}

.prestasi-siswa {
  text-align: center;
  padding: 20px;
}

.prestasi-siswa h1 {
  margin-bottom: 20px;
  color: #2c3e50;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 20px;
  justify-items: center;
}

.card {
  background: #fff;
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 15px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  width: 100%;
  max-width: 300px;
  text-align: left;
}

.card h3 {
  margin: 0;
  color: #007bff;
}

.card p {
  margin: 5px 0;
  font-size: 14px;
  color: #555;
}
</style>
