<script>
// import Layout from "../../../layouts/main.vue";
// import appConfig from "../../../../app.config";

export default {
  page: {
    title: "Form B",
    // meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "Form B",
      items: [
        {
          text: "",
          href: "/",
        },
        {
          text: "Form B",
          active: true,
        },
      ],
      thumbsSwiper: null,
    };
  },
  components: {
    // Layout,
  },
};
</script>

<template>
  <div>
    <b-card no-body>
      <b-card-header class=" d-md-flex border-0">
          <div class="d-md-flex align-items-center">
              <h5 class="card-title mb-3 mb-md-0 flex-grow-1">Results</h5>
          </div>
      </b-card-header>
    </b-card>
    <b-card>
      <b-card-header>
        <b-row class="align-items-end">
          <div class="col-12 col-md-2 mb-3">
            <select name="year" id="year" class="form-select">
              <option value="2023/2024">Select year</option>
              <option value="2023/2024">2023/2024</option>
              <option value="2023/2024">2022/2023</option>
              <option value="2023/2024">2021/2022</option>
              <option value="2023/2024">2020/2021</option>
              <option value="2023/2024">2019/2020</option>
              <option value="2023/2024">2018/2019</option>
            </select>
          </div>
          <div class="col-12 col-md-2 mb-3">
            <select name="year" id="year" class="form-select">
              <option value="2023/2024">Select Semester</option>
              <option value="2023/2024">First</option>
              <option value="2023/2024">Second</option>
              <option value="2023/2024">Resit</option>
            </select>
          </div>
          <div class="col-12 col-md-2 mb-3">
            <b-button variant="success">Done</b-button>
          </div>
        </b-row>
      </b-card-header>
      <b-card-body class="">      
        <div>
         <div class="caption">Academic Year :</div>
            <div class="semester">
                <div class="col-12">
                    <div class="title">First Semester</div>
                    <table>
                        <thead>
                            <tr>
                                <th>Code</th>
                                <th>title</th>
                                <th>CV</th>
                                <th>CA</th>
                                <th>EXAM</th>
                                <th>Marks</th>
                                <th>GD</th>
                                <th>GP</th>
                                <th>WP</th>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>23</td>
                                <td>27</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>23</td>
                                <td>27</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>23</td>
                                <td>27</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>23</td>
                                <td>27</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>23</td>
                                <td>27</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td></td>
                                <td></td>
                                <td></td>
                                <td></td>
                                <td></td>
                                <td></td>
                                <td></td>
                                <td></td>
                                <td></td>
                            </tr>
                            <tr>
                                <td colspan="2"> total </td>
                                <td>29</td>
                                <td></td>
                                <td></td>
                                <td>21</td>
                                <td>51</td>
                            </tr>
                            <tr>
                                <td colspan="2"></td>
                                <td colspan="4" class="danger">GPA First Semester</td>
                                <td class="danger">2.40</td>
                            </tr>
                        </thead>
                    </table>
                </div>          
            </div> 
        </div>
      </b-card-body>
      <div class="col-12 mb-3 text-md-end">
        <b-button variant="success">Download</b-button>
      </div>
    </b-card>
  </div>
</template>
<style scoped>
 body{
     margin: 10px 100px;
 }
.header{
    display: flex;
}
.right{
    flex: 0.8;
}
.left{
    flex: 0.8 ;
}
.center{
    flex: 1.4;
}
 h4{
     border-bottom: 1px solid gray;
     padding-bottom: 10px;
     margin-bottom: 10px;
 }
 .title{
     text-align: center;
     margin-bottom: 5px;
 }
 hr{
    height: 5px;
    background: gray;

 }
 
table {   
    border-collapse: collapse;
    width: 100%;
  }
  table, td, th {
    border: 1px solid black;
    text-align: left;
  }
  
  th , td {
    padding: 5px;
  }
  .bg-primary{
      padding: 5px 0px;
      background: navy;
      color: #f1f1f1;
  }
</style>
