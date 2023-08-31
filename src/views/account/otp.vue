<script>
export default {
  page: {
    title: "OTP",
  }
};
</script>


<template>
  <div class="auth-page-wrapper pt-5">
    <div class="auth-one-bg-position auth-one-bg" id="auth-particles">
      <div class="bg-overlay"></div>

      <div class="shape">

        <svg xmlns="http://www.w3.org/2000/svg" version="1.1" xmlns:xlink="http://www.w3.org/1999/xlink"
          viewBox="0 0 1440 120">
          <path d="M 0,36 C 144,53.6 432,123.2 720,124 C 1008,124.8 1296,56.8 1440,40L1440 140L0 140z"></path>
        </svg>
      </div>
      <Particles id="tsparticles" :options="{
        particles: {
          number: {
            value: 90,
            density: {
              enable: true,
              value_area: 800,
            },
          },
          color: {
            value: '#ffffff',
          },
          shape: {
            type: 'circle',
            stroke: {
              width: 0,
              color: '#000000',
            },
            polygon: {
              nb_sides: 5,
            },
            image: {
              src: 'img/github.svg',
              width: 100,
              height: 100,
            },
          },
          opacity: {
            value: 0.8,
            random: true,
            anim: {
              enable: true,
              speed: 1,
              opacity_min: 0,
              sync: false,
            },
          },
          size: {
            value: 4,
            random: true,
            anim: {
              enable: false,
              speed: 4,
              size_min: 0.2,
              sync: false,
            },
          },
          line_linked: {
            enable: false,
            distance: 150,
            color: '#ffffff',
            opacity: 0.4,
            width: 1,
          },
          move: {
            enable: true,
            speed: 2,
            direction: 'none',
            random: false,
            straight: false,
            out_mode: 'out',
            attract: {
              enable: false,
              rotateX: 600,
              rotateY: 1200,
            },
          },
        },
        interactivity: {
          detect_on: 'canvas',
          events: {
            onhover: {
              enable: true,
              mode: 'bubble',
            },
            onclick: {
              enable: true,
              mode: 'repulse',
            },
            resize: true,
          },
          modes: {
            grab: {
              distance: 400,
              line_linked: {
                opacity: 1,
              },
            },
            bubble: {
              distance: 400,
              size: 4,
              duration: 2,
              opacity: 0.8,
              speed: 3,
            },
            repulse: {
              distance: 200,
            },
            push: {
              particles_nb: 4,
            },
            remove: {
              particles_nb: 2,
            },
          },
        },
        retina_detect: true,
        config_demo: {
          hide_card: false,
          background_color: '#b61924',
          background_image: '',
          background_position: '50% 50%',
          background_repeat: 'no-repeat',
          background_size: 'cover',
        },
      }" />
    </div>

    <div class="auth-page-content">
      <b-container>
        <b-row>
          <b-col lg="12">
            <div class="text-center mt-sm-5 mb-4 text-white-50">
              <div>
                <router-link to="/" class="d-inline-block auth-logo">
                  <img src="data:image/jpeg;base64,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" alt="" height="50" style="border-radius:25px;" />
                </router-link>
              </div>
              <p class="mt-3 fs-15 fw-medium">
                KEBHIPS
              </p>
            </div>
          </b-col>
        </b-row>

        <b-row class="justify-content-center">
          <b-col md="8" lg="6" xl="5">
            <b-card no-body class="mt-4">
              <b-card-body class="p-4">
                <div class="text-center mt-2">
                  <h5 class="text-success">OTP Verification</h5>
                </div>
                <div class="p-2 mt-4">
                  <b-alert v-model="authError" variant="danger" class="mt-3" dismissible>{{ authError }}</b-alert>

                  <div>

                  </div>

                  <form>
                    <div class="mb-3">
                      <label class="form-label" for="Enter verification pin"> Enter Pin sent to your Email</label>
                      <div class="position-relative auth-pass-inputgroup mb-3">
                        <input type="password" v-model="password" class="form-control pe-5" placeholder="Enter verification pin"
                          id="password-input" />
                        <b-button variant="link" class="position-absolute end-0 top-0 text-decoration-none text-muted"
                          type="button" id="password-addon">
                          <i class="ri-eye-fill align-middle"></i>
                        </b-button>
                        <div class="invalid-feedback">
                          <span></span>
                        </div>
                      </div>
                    </div>                

                    <div class="mt-4">
                      <b-button variant="primary" class="w-100" type="submit">
                        Verify
                      </b-button>
                    </div>
                  </form>
                </div>
              </b-card-body>
            </b-card>            
          </b-col>
        </b-row>
      </b-container>
    </div>

    <footer class="footer">
      <span class="container">
      &copy;right 2023
          <div class="float-end">
            <router-link to="/forgot-password" class="text-muted">developed by: <span class="text-primary fw-bold">Nex<span class="text-danger">inch</span></span></router-link>
          </div></span>
    </footer>
  </div>
</template>