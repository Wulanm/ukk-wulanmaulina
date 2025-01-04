<template>
   <div class="welcome-page">
    <div id="carouselExampleSlidesOnly" class="carousel slide" data-bs-ride="carousel">
      <div class="carousel-inner">
        <div class="carousel-item active">
          <div class="carousel-content">
            <img src="/assets/img/bacground.jpg" class="d-block w-100" alt="..." />
  <div class="container">
    <div class="image-section">
      <img src="~/assets/img/kurniawan.png" alt="Image" />
    </div>
    <div class="text-section">
      <h2>Sejarah SMK Negeri 4 Tasikmalaya</h2>
      <p>
        Sejalan dengan Program Pemerintah di bidang pendidikan Menengah Kejuruan pada saat itu, yaitu pemerataan akses, ditambah pula dengan banyaknya keinginan masyarakat yang mengharapkan adanya SMK Negeri di daerah Kecamatan Purbaratu
        Kota Tasikmalaya. Hal ini terutama untuk menampung tamatan dari SLTP yang ingin melanjutkan ke SMK. Beberapa tokoh masyarakat dan unsur pejabat pemerintah di Kecamatan Purbaratu Kota Tasikmalaya mengusulkan kepada Pemerintah Kota
        Tasikmalaya dan Pemerintah Provinsi Jawa Barat agar berdirinya SMK Negeri di Kecamatan Purbaratu Kota Tasikmalaya.
      </p>
      <p>
        Setelah melalui perjuangan yang sangat panjang dari berbagai pihak, khususnya Disdik Kota Tasikmalaya dan pihak-pihak terkait lainnya, sesuai prosedur dan ketentuan yang berlaku pada waktu itu, akhirnya pada tahun pelajaran
        2010/2011 SMK Negeri 4 Tasikmalaya mulai berdiri. Pada awalnya, sekolah ini membuka Kompetensi Keahlian Teknik Komputer dan Jaringan dengan pendaftar peserta didik baru yang berjumlah 44 orang.
      </p>
      <p>
        Tempat belajar pada awalnya menumpang di SMP Negeri 17 Kota Tasikmalaya, dan sekolah induknya adalah SMK Negeri 2 Kota Tasikmalaya. Untuk tenaga pendidik dan tenaga kependidikan masih dibantu sepenuhnya oleh kedua sekolah tersebut.
        Pada tahun 2012, keluarlah surat Izin Pendirian berdasarkan keputusan Kepala Badan Pelayanan Perizinan Terpadu Kota Tasikmalaya No. 420/9/SK-BPPT/2012 Tanggal 06 Februari 2012.
      </p>
    </div>
    <div class="vision-mission-goals">
      <div class="vision">
        <h2>Visi</h2>
        <p>“Menjadi sekolah unggul yang menghasilkan lulusan berkompeten, berkarakter, dan siap menghadapi tantangan global.”</p>
      </div>
      <div class="mission">
        <h2>Misi</h2>
        <ul>
          <li>Menyelenggarakan pendidikan berbasis teknologi dan informasi.</li>
          <li>Meningkatkan kualitas pembelajaran sesuai kebutuhan dunia kerja.</li>
          <li>Menanamkan nilai-nilai karakter pada seluruh peserta didik.</li>
          <li>Memperluas kerjasama dengan dunia usaha dan dunia industri.</li>
          <li>Menyiapkan lulusan yang memiliki jiwa kewirausahaan.</li>
        </ul>
      </div>
      <div class="goals">
        <h2>Tujuan</h2>
        <ul>
          <li>Menciptakan lingkungan belajar yang kondusif dan inovatif.</li>
          <li>Menghasilkan lulusan yang mampu bersaing di tingkat nasional dan internasional.</li>
          <li>Mendorong peserta didik untuk memiliki keterampilan praktis dan adaptif.</li>
          <li>Menjalin kemitraan strategis dengan dunia usaha dan dunia industri.</li>
          <li>Melahirkan generasi yang beretika dan memiliki wawasan global.</li>
        </ul>
      </div>
    </div>
  </div>
  <!-- Identitas Sekolah -->
<section class="identitas-sekolah">
  <div class="container">
    <h2 class="text-center ">Identitas Sekolah</h2>
    <table class="table table-striped mt-3">
      <tbody>
        <tr>
          <th>Nama Sekolah</th>
          <td>SMK Negeri 4 Tasikmalaya</td>
        </tr>
        <tr>
          <th>NPSN</th>
          <td>12345678</td>
        </tr>
        <tr>
          <th>Alamat</th>
          <td>Jl.Depok Kel.Sukamenak Kec.Purbaratu Kota Tasikmalaya 46196</td>
        </tr>
        <tr>
          <th>Email</th>
          <td>smkn4tasikmalaya@gmail.com</td>
        </tr>
        <tr>
          <th>Telepon</th>
          <td>(0265) 123456</td>
        </tr>
      </tbody>
    </table>
  </div>
</section>
  </div>
  </div>
  </div>
  </div>
  </div>
</template>

<style scoped>
.identitas-sekolah {
  background-color: #f9f9f9;
  padding: 1px 0;
}

.identitas-sekolah h2 {
  font-size: 2.5rem;
  font-weight: 700;
  color: #11419f;
  margin-bottom: 1.5rem;
}

.table {
  width: 100%;
  margin-top: 1.5rem;
}

.table th {
  text-align: left;
  font-weight: bold;
  color: #333;
}

.table td {
  color: #555;
}





.carousel-content img {
  max-height: 600px;
  object-fit: cover; 
  width: 100%; 
}

.container {
  display: flex;
  align-items: flex-start;
  gap: 20px;
  padding-top: 8%;
  flex-wrap: wrap;
}

.image-section {
  flex: 1;
  text-align: center;
}

.image-section img {
  max-width: 80%;
  height: auto;
}

.text-section {
  flex: 2;
  padding-left: 20px;
}

.text-section h2 {
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 10px;
}

.text-section p {
  font-size: 16px;
  line-height: 1.6;
  margin-bottom: 15px;
}

.vision-mission-goals {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  margin-top: 20px;
}

.vision,
.mission,
.goals {
  flex: 1;
  padding: 20px;
  background-color: #f9f9f9;
  border: 1px solid #ddd;
  border-radius: 8px;
  min-width: 300px;
}

.vision h2,
.mission h2,
.goals h2 {
  font-size: 20px;
  font-weight: bold;
  margin-bottom: 10px;
}

.vision p,
.mission ul,
.goals ul {
  font-size: 16px;
  line-height: 1.6;
}

.mission ul,
.goals ul {
  list-style-type: disc;
  margin-left: 20px;
}


.footer {
  background-color: #11419f79;
  padding: 40px 0;
  margin-top: 0px;
  width: 100%; 
  height: 10px;
}

.footer p {
  color: white;
  font-size: 14px;
  margin: 0;
  text-align: center;
}
</style>