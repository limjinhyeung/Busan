<template>
  <main>
    <div id="carouselExampleCaptions" class="carousel slide carousel-fade" data-bs-ride="carousel">
            <div class="carousel-inner">
                <div class="carousel-item active head">
                    <img src="https://cdn.pixabay.com/photo/2017/03/14/16/56/banner-2143727_1280.jpg" class="d-block w-100" >
                    <div class="d-none d-md-block carousel_subtext">
                        <div class="subject">
                            <p>관광지</p>
                            <p style="font-size: 30px;">tourist attraction</p>
                        </div>
                    </div>
                </div>
            </div>
    </div>
    <div class="box" style="height: 1700px;">
    <br>
    <h2 class="text-center">관광지</h2>
    <br>
    <div class="container">
        <div class="row row-cols-1 row-cols-md-3 g-4">
            <div class="col">
                <router-link to="/touristspotdetails">
                    <div class="card h-100">
                        <img src="https://www.visitbusan.net/uploadImgs/files/cntnts/20191229153530528_thumbL" class="card-img-top" alt="...">
                        <div class="card-body">
                            <h5 class="card-title">해운대해수욕장</h5>
                            <p class="card-text">부산광역시 해운대구 해운대해변로 264</p>
                            <span class="badge text-bg-dark me-1">자연</span>
                            <span class="badge text-bg-dark me-1">걷기</span>
                            <span class="badge text-bg-dark me-1">이색여행</span>
                        </div>
                    </div>
                </router-link>
            </div>
            <div class="col">
                <a href="">
                    <div class="card h-100">
                        <img src="https://www.visitbusan.net/uploadImgs/files/cntnts/20191229160529389_thumbL" class="card-img-top" alt="...">
                        <div class="card-body">
                            <h5 class="card-title">광안리 바다</h5>
                            <p class="card-text">부산광역시 수영구 광안해변로 219</p>
                            <span class="badge text-bg-dark">자연</span>
                            <span class="badge text-bg-dark">걷기</span>
                            <span class="badge text-bg-dark">이색여행</span>
                        </div>
                    </div>
                </a>
            </div>
            <div class="col">
                <a href="">
                    <div class="card h-100">
                        <img src="https://www.visitbusan.net/uploadImgs/files/cntnts/20191222164810529_thumbL" class="card-img-top" alt="...">
                        <div class="card-body">
                            <h5 class="card-title">흰여울문화마을</h5>
                            <p class="card-text">부산광역시 영도구 흰여울길</p>
                            <span class="badge text-bg-dark">자연</span>
                            <span class="badge text-bg-dark">걷기</span>
                            <span class="badge text-bg-dark">이색여행</span>
                        </div>
                    </div>
                </a>
            </div>
            <div class="col">
                <a href="">
                    <div class="card h-100">
                        <img src="https://www.visitbusan.net/uploadImgs/files/cntnts/20191222180829962_thumbL" class="card-img-top" alt="...">
                        <div class="card-body">
                            <h5 class="card-title">태종대</h5>
                            <p class="card-text">부산광역시 영도구 전망로 24</p>
                            <span class="badge text-bg-dark">자연</span>
                            <span class="badge text-bg-dark">걷기</span>
                            <span class="badge text-bg-dark">이색여행</span>
                        </div>
                    </div>
                </a>
            </div>
        </div>
    </div>
    <br>
    <nav>
        <ul class="pagination justify-content-center">
            <li class="page-item">
                <a class="page-link" href="">Prev</a>
            </li>
            <li class="page-item active">
                <a class="page-link" href="">1</a>
            </li>
            <li class="page-item">
                <a class="page-link" href="">Next</a>
            </li>
        </ul>
    </nav>
    </div>
  </main>
</template>

<script>
export default {

}
</script>

<style>

</style>