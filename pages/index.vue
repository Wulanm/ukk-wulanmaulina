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
            <div class="carousel-text">
              <h1>Selamat Datang di Website Resmi</h1>
              <h1>SMK Negeri 4 Tasikmalaya</h1>
            </div>
          </div>
        </div>
        <div class="carousel-item">
          <div class="carousel-content">
            <img src="..." class="d-block w-100" alt="..." />
            <div class="carousel-text">
              <h1>Judul Slide 2</h1>
              <p>Deskripsi slide 2</p>
            </div>
          </div>
        </div>
        <div class="carousel-item">
          <div class="carousel-content">
            <img src="..." class="d-block w-100" alt="..." />
            <div class="carousel-text">
              <h1>Judul Slide 3</h1>
              <p>Deskripsi slide 3</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <section class="sambutan">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-lg-6">
            <h2 class="sambutan-title">Sambutan Kepala Sekolah</h2>
            <p>
              Assalamu'alaikum warahmatullahi wabarakatuh,
              <br />
              Selamat datang di website resmi SMK Negeri 4 Tasikmalaya. Kami
              sangat bangga dapat memperkenalkan sekolah kami melalui platform
              ini. Semoga informasi yang ada dapat memberikan gambaran jelas
              mengenai kegiatan, prestasi, dan fasilitas yang kami miliki.
              <br />
              Terima kasih atas perhatian dan kerjasama yang telah terjalin,
              semoga kita semua senantiasa diberikan kemudahan dalam menjalani
              aktivitas belajar mengajar di SMK Negeri 4 Tasikmalaya.
              <br />
              Wassalamu'alaikum warahmatullahi wabarakatuh.
            </p>
          </div>
          <div class="col-lg-6">
            <img src="/assets/img/kurniawan.png" alt="Kepala Sekolah"  class="img-fluid rounded" />
          </div>
        </div>
      </div>
    </section>
    <div class="container mx-auto p-4">
      <div class="bg-white shadow-md rounded-lg p-6">
        <div class="text-center mb-6">
          <h1 class="text-2xl font-bold text-gray-800">Kompetensi Keahlian</h1>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
          <div
            v-for="(kompetensi, index) in kompetensiKeahlian"
            :key="index"
            class="bg-gray-100 p-4 rounded-lg shadow-md"
          >
            <div class="flex items-center mb-4">
              <i :class="kompetensi.icon" class="text-3xl text-gray-800"></i>
              <h2 class="ml-4 text-xl font-semibold text-gray-800">
                {{ kompetensi.name }}
              </h2>
            </div>
            <p class="font-semibold text-gray-800">
              Sarana pendukung pembelajaran:
            </p>
            <ul class="list-disc list-inside text-gray-700">
              <li v-for="(sarana, index) in kompetensi.sarana" :key="index">
                {{ sarana }}
              </li>
            </ul>
          </div>
        </div>
        <div class="container">
          <h4 class="mt-5">
            Berita <br />
            <span class="text-primary">Terbaru</span>
          </h4>
          <span class="text-artikel">
            <p class="mt-3">
              Berita terbaru, cerita inspiratif dan informasi terkini seputar
              kegiatan serta prestasi sekolah kami.
            </p>
          </span>
          <div class="row m-3 justify-content-center">
            <div class="col-md-5">
              <div class="card mt-3 bg-light rounded-4">
                <img
                  src="/assets/img/iduka.jpg"
                  class="card-img-top p-2 rounded-4"
                  alt="img-artikel"
                />
                <div class="card-body">
                  <p class="text-end">Kamis, 12 Okt 2023</p>
                  <h5 class="text-center mt-1">
                    SMKN 4 Tasikmalaya Koneksikan Iduka dengan Pencari Kerja
                  </h5>
                  <a
                    href="https://radartasik.id/2023/10/12/smkn-4-tasikmalaya-koneksikan-iduka-dengan-pencari-kerja/"
                    target="_blank"
                    ><p class="mt-4">
                      Baca Selengkapnya
                      <span
                        ><i class="bi bi-arrow-right-circle text-black"></i
                      ></span>
                    </p>
                  </a>
                </div>
              </div>
            </div>
            <div class="col-md-5">
              <div class="card mt-3 bg-light rounded-4">
                <img
                  src="/assets/img/honda.jpeg"
                  class="card-img-top p-2 rounded-4"
                  alt="img-artikel"
                />
                <div class="card-body">
                  <p class="text-end">Senin, 20 Mei 2024</p>
                  <h5 class="text-center mt-1">
                    Honda Resmikan Safety Riding Lab di SMKN 4 Tasikmalaya,
                    Ciptakan Bibit Keselamatan di Jawa Barat
                  </h5>
                  <a
                    href="https://www.pikiran-rakyat.com/otomotif/pr-018109177/honda-resmikan-safety-riding-lab-di-smkn-4-tasikmalaya-ciptakan-bibit-keselamatan-pada-gen-z?page=all"
                    target="_blank"
                    ><p class="mt-4">
                      Baca Selengkapnya<span
                        ><i class="bi bi-arrow-right-circle text-black"></i
                      ></span>
                    </p>
                  </a>
                </div>
              </div>
            </div>
            <div class="col-md-5">
              <div class="card mt-3 bg-light rounded-4">
                <img src="/assets/img/expocreannnova.jpg" class="card-img-top p-2 rounded-4"alt="img-artikel"/>
                <div class="card-body">
                  <p class="text-end">Senin 27 Feb 2023</p>
                  <h5 class="text-center mt-1">
                    Siswa SMKN 4 Tasikmalaya Adu Inovasi dan Kreativitas di Expo
                    Creanova
                  </h5>
                  <a href="https://radartasik.id/2023/03/02/siswa-smkn-4-tasikmalaya-adu-inovasi-dan-kreativitas-di-expo-creanova/"  target="_blank" ><p class="mt-4">Baca Selengkapnya <span><i class="bi bi-arrow-right-circle text-black"></i></span>
                    </p>
                  </a>
                </div>
              </div>
            </div>
            <div class="col-md-5">
              <div class="card mt-3 bg-light rounded-4">
                <img src="/assets/img/kerjasama.jpg" class="card-img-top p-2 rounded-4"alt="img-artikel"/>
                <div class="card-body">
                  <p class="text-end">Kamis, 2 Mar 2023</p>
                  <h5 class="text-center mt-1">
                    Sinergi Bagi Negeri, DAM Kerjasama dengan SMKN 4 Tasikmalaya
                    Terapkan KTBSM Sepeda Motor Astra Honda
                  </h5>
                  <a
                    href="https://jabar.tribunnews.com/2023/03/02/sinergi-bagi-negeri-dam-kerjasama-dengan-smkn-4-tasikmalaya-terapkan-ktbsm-sepeda-motor-astra-honda"
                    target="_blank"
                    ><p class="mt-4">
                      Baca Selengkapnya
                      <span
                        ><i class="bi bi-arrow-right-circle text-black"></i
                      ></span>
                    </p>
                  </a>
                </div>
              </div>
            </div>
            <div class="col-md-5">
              <div class="card mt-3 bg-light rounded-4">
                <img src="/assets/img/safety-reading.jpg" class="card-img-top p-2 rounded-4" alt="img-artikel"/>
                <div class="card-body">
                  <p class="text-end">Senin, 20 Mei 2024</p>
                  <h5 class="text-center mt-1">
                    SMKN 4 Tasikmalaya Terapkan Aturan Ketat Terhadap Kendaraan
                    Bermotor
                  </h5>
                  <a href="https://radartasik.id/2025/01/02/smkn-4-tasikmalaya-terapkan-aturan-ketat-terhadap-kendaraan-bermotor/2/"target="_blank"><p class="mt-4">Baca Selengkapnya
                    <span><i class="bi bi-arrow-right-circle text-black"></i ></span>
                    </p>
                  </a>
                </div>
              </div>
            </div>
            <div class="col-md-5">
              <div class="card mt-3 bg-light rounded-4">
                <img src="/assets/img/kurikulum.jpeg" class="card-img-top p-2 rounded-4" alt="img-artikel"/>
                <div class="card-body">
                  <p class="text-end">Rabu,9 Agustus 2023</p>
                  <h5 class="text-center mt-1">
                    Sinkronisasi Kurikulum SMKN 4 Tasikmalaya dengan Inovindo
                  </h5>
                  <a href="https://inovindoacademy.com/berita/sinkronisasi-kurikulum-smkn-4-tasikmalaya-dengan-inovindo"target="_blank" ><p class="mt-4">Baca Selengkapnya
                      <span><i class="bi bi-arrow-right-circle text-black"></i></span>
                    </p>
                  </a>
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
  name: "KompetensiKeahlian",
  data() {
    return {
      kompetensiKeahlian: [
        {
          name: "Teknik Komputer dan Jaringan",
          icon: "fas fa-network-wired",
          sarana: ["Bengkel TKJ", "Network Simulator", "Techno Park", "Dll"],
        },
        {
          name: "Rekayasa Perangkat Lunak",
          icon: "fas fa-code",
          sarana: [
            "Laboratorium Komputer",
            "Computer Server",
            "Techno Park",
            "Dll",
          ],
        },
        {
          name: "Teknik dan Bisnis Sepeda Motor",
          icon: "fas fa-tools",
          sarana: ["Bengkel TBSM", "Unit Produksi", "Techno Park", "Dll"],
        },
        {
          name: "Desain Komunikasi Visual",
          icon: "fas fa-camera",
          sarana: ["Bengkel DKV", "Unit Produksi", "Techno Park", "Dll"],
        },
        {
          name: "Teknik Otomasi Industri",
          icon: "fas fa-industry",
          sarana: ["Bengkel TOI", "Unit Produksi", "Techno Park", "Dll"],
        },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  padding: 2rem;
}

.bg-white {
  background-color: #ffffff;
}

.shadow-md {
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.rounded-lg {
  border-radius: 8px;
}

.text-center {
  text-align: center;
}

.text-gray-800 {
  color: #2d3748;
}

.text-xl {
  font-size: 1.25rem;
}

.font-bold {
  font-weight: bold;
}

.mb-6 {
  margin-bottom: 1.5rem;
}

.grid {
  display: grid;
}

.grid-cols-1 {
  grid-template-columns: repeat(1, 1fr);
}

.md\:grid-cols-2 {
  grid-template-columns: repeat(2, 1fr);
}

.lg\:grid-cols-3 {
  grid-template-columns: repeat(3, 1fr);
}

.gap-6 {
  gap: 1.5rem;
}

.bg-gray-100 {
  background-color: #f7fafc;
}

.p-4 {
  padding: 1rem;
}

.rounded-lg {
  border-radius: 8px;
}

.shadow-md {
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.flex {
  display: flex;
}

.items-center {
  align-items: center;
}

.mb-4 {
  margin-bottom: 1rem;
}

.ml-4 {
  margin-left: 1rem;
}

.font-semibold {
  font-weight: 600;
}

.list-disc {
  list-style-type: disc;
}

.list-inside {
  padding-left: 1.5rem;
}

.text-gray-700 {
  color: #4a5568;
}

.bg-green-600 {
  background-color: #338ba6e2;
}

.text-white {
  color: #ffffff;
}

.container {
  max-width: 1280px;
}

.text-center {
  text-align: center;
}

.font-bold {
  font-weight: 700;
}

.mb-2 {
  margin-bottom: 0.5rem;
}

.mb-6 {
  margin-bottom: 1.5rem;
}

.pt-4 {
  padding-top: 1rem;
}

.border-t {
  border-top-width: 1px;
}

.border-white {
  border-color: #ffffff;
}

.h1 {
  font-family: "Abhaya Libre ExtraBold";
}

.carousel-content img {
  max-height: 600px;
  width: 100%;
}

.carousel-text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  color: rgb(255, 255, 255);
  padding: 1rem;
  border-radius: 8px;
}

.carousel-text h1 {
  font-size: 2rem;
  margin: 0;
}

.carousel-text p {
  font-size: 1.2rem;
  margin: 0;
}

.sambutan {
  padding: 4rem 0;
  background-color: #f4f4f4;
}

.sambutan-title {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 1.5rem;
  color: #11419f;
}

.sambutan p {
  font-size: 1.2rem;
  line-height: 1.6;
  color: #333;
}

.sambutan img {
  max-width: 100%;
  height: auto;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

@media (max-width: 768px) {
  .sambutan .row {
    text-align: center;
  }

  .sambutan .col-lg-6 {
    margin-bottom: 2rem;
  }
}

.card-img-top {
  width: 100%;
  height: 250px;
}

.card {
  background-color: transparent;
  backdrop-filter: blur(20px);
  border: 2px solid #ffff;
}

h4,
h5,
p {
  font-family: "Poppins", serif;
}

h4 {
  margin-left: 95px;
}

.text-artikel p {
  margin-left: 95px;
  max-width: 30%;
}

a {
  color: #000 !important;
  text-decoration: none;
}

@media only screen and (min-width: 600px) and (max-width: 890px) {
  h4,
  .text-artikel p {
    margin-left: 30px;
  }

  .card-img-top {
    width: 100%;
    height: 170px;
  }

  p,
  a {
    font-size: small;
  }

  h5 {
    font-size: medium;
  }
}

@media only screen and (max-width: 600px) {
  h4 {
    margin-left: 35px;
  }

  .card-img img {
    width: 100%;
    margin-left: 5px;
    margin-top: 35px !important;
  }

  .text-artikel p {
    margin-left: 35px;
    max-width: 50%;
    font-size: small;
  }

  .card-img-top {
    width: 100%;
    height: 200px;
  }

  p,
  a {
    font-size: small;
  }

  h5 {
    font-size: medium;
  }

  .berita i {
    margin-left: 5px;
  }
}
</style>
