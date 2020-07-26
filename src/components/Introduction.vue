1<template>
  <div class="hello">
    <div class="container my-5 z-depth-1 amber accent-4">
      <section class="dark-grey-text">
        <div class="row pr-lg-5">
          <div class="col-md-7 mb-4">
            <div class="view">
              <img src="https://mdbootstrap.com/img/illustrations/graphics(4).png" class="img-fluid" alt="smaple image">
            </div>
          </div>
          <div class="col-md-5 d-flex align-items-center">
            <div>
              <h3 class="font-weight-bold mb-4">Ahh! What was that song?</h3>
              <p>Do you also get troubled with the same ? 
                <br>
                Here you can jot down it.
              </p>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Introduction',
  props: {
    msg: String
  }
}
</script>
