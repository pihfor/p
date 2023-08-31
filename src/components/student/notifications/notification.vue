<script>

import { ref, watch } from "vue";
import useVuelidate from "@vuelidate/core";
// import PageHeader from "@/components/page-header";

export default {
  methods: {
    deleteRecord(ele) {
      ele.target.parentElement.parentElement.parentElement.remove();
    },
  },
  page: {
    title: "Notifications",
    // meta: [{ name: "description", content: appConfig.description }],
  },
   setup() {
    let files = ref([]);
    let dropzoneFile = ref("");
    const drop = (e) => {
      dropzoneFile.value = e.dataTransfer.files[0];
      files.value.push(dropzoneFile.value);
    };
    const selectedFile = () => {
      dropzoneFile.value = document.querySelector(".dropzoneFile").files[0];
      files.value.push(dropzoneFile.value);
    };
    watch(
      () => [...files.value],
      (currentValue) => {
        return currentValue;
      }
    );

    return { dropzoneFile, files, drop, selectedFile, v$: useVuelidate() };
  },
  data() {
    return {
      title: "Notifications",
      items: [
        {
          text: "Notifications",
          href: "/",
        },
        {
          text: "Notifications",
          active: true,
        },
      ],
    };
  },
 
  components: {
    // Layout,
    // PageHeader,
  },
};
</script>

<template>
    <b-card no-body>
        <b-card-header>
            <b-row>
                <b-col xxl="6" md="6">
                    <div class="card-title">Notifications</div>
                </b-col>
            </b-row>
        </b-card-header>
        <b-card-body>
            <div class="table-responsive mb-4">
                <div>
                    <div class="p-3">
                        <div class="toast fade show w-100" role="alert" aria-live="assertive"
                            data-bs-autohide="false" aria-atomic="true">
                            <div class="toast-header bg-soft-info">
                                <span class="fw-semibold me-auto">KEBHIPS</span>
                                <small>Just now</small>
                                <button type="button" class="btn-close" data-bs-dismiss="toast"
                                    aria-label="Close"></button>
                            </div>
                            <div class="toast-body">See? Just like this.</div>
                        </div>

                        <div class="toast fade show w-100" role="alert" aria-live="assertive"
                            data-bs-autohide="false" aria-atomic="true">
                            <div class="toast-header bg-soft-info">
                                <span class="fw-semibold me-auto">KEBHIPS</span>
                                <small>2 seconds ago</small>
                                <button type="button" class="btn-close" data-bs-dismiss="toast"
                                    aria-label="Close"></button>
                            </div>
                            <div class="toast-body">Heads up, toasts will stack automatically</div>
                        </div>

                        <div class="toast fade show w-100" role="alert" aria-live="assertive"
                            data-bs-autohide="false" aria-atomic="true">
                            <div class="toast-header bg-soft-info">
                                <span class="fw-semibold me-auto">KEBHIPS</span>
                                <small>Just now</small>
                                <button type="button" class="btn-close" data-bs-dismiss="toast"
                                    aria-label="Close"></button>
                            </div>
                            <div class="toast-body">See? Just like this.</div>
                        </div>
                    </div>
                </div>
            </div>
        </b-card-body>
    </b-card>
</template>