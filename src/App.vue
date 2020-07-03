<template>
  <div id="app">
    <div id="calender-week">
      <div class="container-fluid mt-5">
        <div class="row">
          <div class="col-12">
            <div class="card-group">
              
              <!-- Tage -->
              <div class="card">
                <div class="card-header text-center bg-vue">
                  <strong>Montag</strong>
                </div>
                <div class="card-body">
                  <div>1</div>
                  <div class="alert alert-success text-center">
                    <div>Müll rausbringen</div>
                    <div>
                      <i class="fas fa-edit mr-2"></i>
                      <i class="far fa-trash-alt"></i>
                    </div>
                  </div>
                </div>
              </div>
              <div class="card">
                <div class="card-header text-center bg-vue">
                  <strong>Dienstag</strong>
                </div>
                <div class="card-body">
                  <div>2</div>
                  <div class="alert alert-success text-center">
                    <div>Tischtennis</div>
                    <div>
                      <i class="fas fa-edit mr-2"></i>
                      <i class="far fa-trash-alt"></i>
                    </div>
                  </div>
                </div>
              </div>
              <div class="card">
                <div class="card-header text-center bg-vue">
                  <strong>Mittwoch</strong>
                </div>
                <div class="card-body">
                  <div>3</div>
                  <div class="alert alert-success text-center">
                    <div>Arbeit</div>
                    <div>
                      <i class="fas fa-edit mr-2"></i>
                      <i class="far fa-trash-alt"></i>
                    </div>
                  </div>
                </div>
              </div>
              <div class="card">
                <div class="card-header text-center bg-vue">
                  <strong>Donnerstag</strong>
                </div>
                <div class="card-body">
                  <div>4</div>
                </div>
              </div>
              <div class="card">
                <div class="card-header text-center bg-vue">
                  <strong>Freitag</strong>
                </div>
                <div class="card-body">
                  <div>5</div>
                  <div class="alert alert-primary text-center">
                    <div>Pizza Essen</div>
                    <div>
                      <i class="fas fa-edit mr-2"></i>
                      <i class="far fa-trash-alt"></i>
                    </div>
                  </div>
                </div>
              </div>
              <div class="card">
                <div class="card-header text-center bg-vue">
                  <strong>Samstag</strong>
                </div>
                <div class="card-body">
                  <div>6</div>
                </div>
              </div>
              <div class="card">
                <div class="card-header text-center bg-vue">
                  <strong>Sonntag</strong>
                </div>
                <div class="card-body">
                  <div>7</div>
                  <div class="alert alert-success text-center">
                    <div>Müll rausbringen</div>
                    <div>
                      <i class="fas fa-edit mr-2"></i>
                      <i class="far fa-trash-alt"></i>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div id="calendar-entry"></div>
  </div>
</template>

<script>
export default {
  name: "App"
};
</script>

<style scoped>
  .bg-vue {
    background-color: rgb(52, 73, 94);
    color: white;
  }

</style>