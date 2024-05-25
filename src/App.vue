<template>
  <div id="app">
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <a class="navbar-brand" href="#">Toko Online</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item">
            <a class="nav-link" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Products</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Contact</a>
          </li>
        </ul>
      </div>
    </nav>

    <!-- Carousel -->
    <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
      <ol class="carousel-indicators">
        <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
        <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
        <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
      </ol>
      <div class="carousel-inner">
        <div class="carousel-item active">
          <div class="carousel-caption d-none d-md-block">
            <h5>Promo Terbaik Minggu Ini</h5>
            <p>Dapatkan diskon hingga 50% untuk produk terpilih.</p>
          </div>
        </div>
        <div class="carousel-item">
          <div class="carousel-caption d-none d-md-block">
            <h5>Produk Terbaru</h5>
            <p>Lihat koleksi terbaru kami untuk musim ini.</p>
          </div>
        </div>
        <div class="carousel-item">
          <div class="carousel-caption d-none d-md-block">
            <h5>Belanja Mudah dan Cepat</h5>
            <p>Pengalaman belanja yang mudah dan menyenangkan.</p>
          </div>
        </div>
      </div>
      <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>

    <!-- Cards Section -->
    <div class="container mt-5">
      <div class="row">
        <div class="col-md-4" v-for="product in products" :key="product.id">
          <div class="card">
            <img class="card-img-top" :src="product.image" alt="Product image">
            <div class="card-body">
              <h5 class="card-title">{{ product.name }}</h5>
              <p class="card-text">{{ product.description }}</p>
              <a href="#" class="btn btn-primary">Beli Sekarang</a>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Footer -->
    <footer class="bg-dark text-center text-lg-start mt-5 text-white">
      <div class="container p-4">
        <div class="row">
          <div class="col-lg-6 col-md-12 mb-4 mb-md-0">
            <h5 class="text-uppercase">Toko Online</h5>
            <p>
              Toko online terbaik untuk segala kebutuhan Anda. Kami menyediakan berbagai macam produk berkualitas dengan harga yang kompetitif.
            </p>
          </div>
          <div class="col-lg-3 col-md-6 mb-4 mb-md-0">
            <h5 class="text-uppercase">Links</h5>
            <ul class="list-unstyled mb-0">
              <li>
                <a href="#!" class="text-white">Home</a>
              </li>
              <li>
                <a href="#!" class="text-white">Products</a>
              </li>
              <li>
                <a href="#!" class="text-white">About</a>
              </li>
              <li>
                <a href="#!" class="text-white">Contact</a>
              </li>
            </ul>
          </div>
          <div class="col-lg-3 col-md-6 mb-4 mb-md-0">
            <h5 class="text-uppercase">Kontak Kami</h5>
            <ul class="list-unstyled mb-0">
              <li>
                <a href="mailto:info@tokoonline.com" class="text-white">info@tokoonline.com</a>
              </li>
              <li>
                <a href="tel:+621234567890" class="text-white">+62 123 456 7890</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="text-center p-3 bg-secondary">
        © 2023 Toko Online. All rights reserved.
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        { 
          id: 1, 
          name: 'Produk 1', 
          description: 'Deskripsi singkat tentang produk 1.', 
          image: 'https://id-test-11.slatic.net/p/930acc2d34f7c62d2edf914ad9feba50.jpg'

        },
        { 
          id: 2, 
          name: 'Produk 2', 
          description: 'Deskripsi singkat tentang produk 2.', 
          image: 'https://cdn0-production-images-kly.akamaized.net/9YWKOweruT5L96SYlfZFBT_nN6Y=/0x0/smart/filters:quality(75):strip_icc():format(jpeg)/kly-media-production/medias/1647624/original/059640300_1499935439-20170713VYT_Sepatu_Specs_05.JPG' 
        },
        { 
          id: 3, 
          name: 'Produk 3', 
          description: 'Deskripsi singkat tentang produk 3.', 
          image: 'http://3.bp.blogspot.com/-RlXZAuEnVQE/UMnaut4EQ6I/AAAAAAAAAjI/HygNYSVDqz4/s1600/gambar-foto-sepatu-futsal.jpg' 
        }
      ]
    }
  }
}

</script>

<style>
body {
    font-family: Arial, sans-serif;
}

.navbar-brand {
    font-weight: bold;
    color: #ffffff !important;
}

.nav-link {
    color: #ffffff !important;
}

.carousel-caption h5 {
    background-color: rgba(0, 0, 0, 0.5);
    padding: 10px;
    border-radius: 5px;
    color: #ffffff;
}

.carousel-caption p {
    background-color: rgba(0, 0, 0, 0.5);
    padding: 5px;
    border-radius: 5px;
    color: #ffffff;
}

.card-title {
    color: #007BFF;
}

.card-text {
    color: #343a40;
}

.btn-primary {
    background-color: #007BFF;
    border-color: #007BFF;
}

.footer {
    background-color: #343a40;
    padding: 20px 0;
}

.footer .container p {
    margin-bottom: 0;
}

.footer .list-unstyled li {
    margin-bottom: 10px;
}

.footer .text-center {
    background-color: #212529;
    color: white;
    padding: 10px 0;
}

.footer a {
    color: #ffffff;
}

</style>
