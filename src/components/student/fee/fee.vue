<script>
// import Layout from "../../../layouts/main.vue";
// import appConfig from "../../../../app.config";
export default {
  name:"fee",
  page: {
    title: "Course Registration",
    // meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "Fee",
      fees: [
        {
            id: 1,
            type: "Registration Fee",
            transaction_id :  '456577',
            amount: "20,0000",
            description: "Registration",

        },
        {
            id: 2,
            type: "Tuition Fee",
            transaction_id :  '2024455',
            amount: "520,0000",
            description: "part Fee",

        },
        {
            id: 3,
            type: "Registration Fee",
            transaction_id :  '45678994',
            amount: "20,0000",
            description: "Registration",

        },
        {
            id: 4,
            type: "Tuition Fee",
            transaction_id :  '2134455',
            amount: "450,0000",
            description: "Complete Fee",

        },
      ],
      items: [
        {
          text: "",
          href: "/",
        },
        {
          text: "Fee",
          active: true,
        },
      ],
      thumbsSwiper: null,
    };
  },
  components: {
    // Layout,
  },
  
  methods: {
    downloadRow() {
    // Get the selected row index.
    const rowIndex = document.querySelector("table").selectedRowIndex;

    // If no row is selected, return.
    if (rowIndex < 0) {
        return;
    }

    // Get the row data.
    const rowData = document.querySelector("table").rows[rowIndex].cells;

    // Create a CSV string from the row data.
    const csvString = rowData.map(cell => cell.textContent).join(",");

    // Download the CSV string as a file.
    const blob = new Blob([csvString], { type: "text/csv" });
    const url = window.URL.createObjectURL(blob);
    const link = document.createElement("a");
    link.href = url;
    link.download = `row-${rowIndex}.csv`;
    document.body.appendChild(link);
    link.click();
    }
    },
  
};
</script>

<template>
  <div>
    <b-card>
      <b-card-header>
        <div class="d-md-flex align-items-center">
        <h5 class="card-title mb-md-0 flex-grow-1">FEE</h5>
        </div>
      </b-card-header>
    </b-card>

    <b-row>
      <b-col lg="12" >
        <div>
          <b-card class="mt-3">
            <b-card-body>
                <div class="p-3 W-100 bg-danger text-light text-md-center">Incomplete Fee</div>
            </b-card-body>
            <b-card-body class="borderless">
              <ul class="nav nav-tabs nav-tabs-custom nav-success" role="tablist">
                <li class="nav-item">
                  <b-link class="nav-link fs-14 active" data-bs-toggle="tab" href="#transaction" role="tab">
                    <i class="ri-folder-4-line d-inline-block d-md-none"></i>
                    <span class="d-none d-md-inline-block">Transactions</span>
                  </b-link>
                </li>
                <li class="nav-item">
                  <b-link class="nav-link fs-14" data-bs-toggle="tab" href="#register" role="tab">
                    <i class="ri-list-unordered d-inline-block d-md-none"></i>
                    <span class="d-none d-md-inline-block">Pay Fee</span>
                  </b-link>
                </li>
              </ul>
            </b-card-body> 

            <div class="tab-content text-muted">
              <div class="tab-pane" id="register" role="tabpanel">
                <b-row>
                    <b-col xl="12">
                        <b-card no-body>
                            <b-card-body>
                            <form action="">
                                <div>
                                    <b-row class="g-3">

                                    <b-col lg="12">
                                        <div>                   
                                            <label for="">Select FEE Type</label>
                                            <select class="form-select" name="fee" id="fee">
                                                <option selected>Registration Fee</option>
                                                <option value="">Tuition</option>
                                            </select>
                                        </div>
                                    </b-col>
                                    <b-col lg="12">
                                    <div class="my-3 gy-3">
                                        <div class="form-check form-check-inline">
                                            <input id="credit" name="paymentMethod" type="radio"
                                                class="form-check-input" checked required>
                                            <label class="form-check-label" for="credit">Credit
                                                card</label>
                                        </div>
                                        <div class="form-check form-check-inline">
                                            <input id="debit" name="paymentMethod" type="radio"
                                                class="form-check-input" required>
                                            <label class="form-check-label" for="debit">MOMO</label>
                                        </div>
                                        <div class="form-check form-check-inline">
                                            <input id="Orange Money" name="paymentMethod" type="radio"
                                                class="form-check-input" required>
                                            <label class="form-check-label" for="Orange Money">Orange Money</label>
                                        </div>
                                    </div>
                                    </b-col>
                                    <b-col cols="12">
                                        <label for="username" class="form-label">Description</label>
                                        <div class="input-group">
                                            <!-- <span class="input-group-text">@</span> -->
                                            <Textarea class=" form-control"></Textarea>
                                        </div>
                                    </b-col>
                                    <b-col md="12">
                                        <label for="cc-name" class="form-label">Amount</label>
                                        <input type="text" class="form-control" id="cc-name"
                                            placeholder="" required>
                                        <div class="invalid-feedback">
                                            is required
                                        </div>
                                    </b-col>

                                    <b-col md="6">
                                        <label for="cc-number" class="form-label">
                                            Number</label>
                                        <input type="text" class="form-control" id="cc-number"
                                            placeholder="" required>
                                        <div class="invalid-feedback">
                                            Number is required
                                        </div>
                                    </b-col>
                                    </b-row>
                                    <div class="mt-3 md-text-end">
                                        <b-button variant="success" type="submit">Done</b-button>
                                    </div>
                                </div>

                            </form>
                            </b-card-body>
                        </b-card>
                    </b-col>
                </b-row>
              </div>
            </div>
            <div class="tab-content text-muted">
              <div class="tab-pane active" id="transaction" role="tabpanel">
                
                <b-card no-body>
                    <b-card-body>
                      <h5 class="card-title mb-3"></h5>
                      <div class="table-responsive">
                        <table class="table table-borderless mb-0 w-100">
                          <thead>
                            <tr class="bg-light text-muted">
                              <th scope="col">S/n</th>
                              <th scope="col">Type</th>
                              <th scope="col">Transaction ID</th>
                              <th scope="col">Amount</th>
                              <th scope="col">Description</th>
                              <th scope="col">Action</th>
                            </tr>
                          </thead>
                          <tbody>
                            <tr v-for="(fee, index) in this.fees" :key="index">
                              <td scope="col">{{ fee.id }}</td>
                              <td scope="col">{{ fee.type }}</td>
                              <td scope="col">{{ fee.transaction_id }}</td>
                              <td scope="col">{{ fee.amount }}</td>
                              <td scope="col">{{ fee. description }}</td>
                              <td>
                               <b-link @click="downloadRow()">
                                <i class="ri-download-fill align-bottom me-2 text-primary"></i>
                                </b-link>
                              </td>      
                            </tr>
                          </tbody>
                        </table>
                      </div>
                    </b-card-body>
                  </b-card>
              </div>
            </div>
          </b-card>
        </div>
      </b-col>
    </b-row>
  </div>
</template>
