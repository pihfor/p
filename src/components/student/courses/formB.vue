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
              <h5 class="card-title mb-3 mb-md-0 flex-grow-1">FORM B</h5>
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
          <header>
            <div class="header">
              <div class="left">
                <h6>Name :</h6>
                <h6>Matricule :</h6>
                <h6>Major :</h6>
                <h6>Minor :</h6>
              </div>
              <div class="center">
                  <img src="" alt="">
              </div>
              <div class="right">
                  <h6>Department :</h6>
                  <h6>Semester :</h6>
                  <h6>Academic Year :</h6>
                  <h6>Printed Date :</h6>
              </div>
            </div>
          </header>
          <div class="body">
              <div class="title"><h2>REGISTERED COURSES</h2></div>
              <hr>
              <table>
                  <thead>
                      <tr>
                          <th>S/N</th>
                          <th>Course code</th>
                          <th>Course Title</th>
                          <th>Credit Value</th>
                          <th>Course Type</th>
                          <th>Course Instructor(s)</th>
                      </tr>
                      <tr class="bg-primary">
                          <td colspan="6">
                          <div  class="title">Elective Courses</div>
                          </td>
                      </tr>
                  </thead>
                  <tr>
                      <td>1</td>
                      <td>CENP2101</td>
                      <td>FUNDAMENTALS OF COMPUTER ENGINEERING</td>
                      <td>3</td>
                      <td>E</td>
                      <td><li>
                          LIENOU JEAN-PIERRE
                      </li>
                      <li>
                          LIENOU JEAN
                      </li>
                  </td>
                  </tr>
                  <tr>
                      <td>2</td>
                      <td>CENP2101</td>
                      <td>FUNDAMENTALS OF COMPUTER ENGINEERING</td>
                      <td>3</td>
                  </tr>
                  <tr>
                      <td>3</td>
                      <td>CENP2101</td>
                      <td>FUNDAMENTALS OF COMPUTER ENGINEERING</td>
                      <td>3</td>
                      <td>E</td>
                      <td><li>
                          LIENOU JEAN-PIERRE
                      </li></td>
                  </tr>
                  <tr>
                      <td>4</td>
                      <td>CENP2101</td>
                      <td>FUNDAMENTALS OF COMPUTER ENGINEERING</td>
                      <td>3</td>
                      <td>E</td>
                      <td><li>
                          LIENOU JEAN-PIERRE
                      </li></td>
                  </tr>
                  <tr>
                      <td>5</td>
                      <td>CENP2101</td>
                      <td>FUNDAMENTALS OF COMPUTER ENGINEERING</td>
                      <td>3</td>
                      <td>E</td>
                      <td>
                          <li>
                              LIENOU JEAN-PIERRE
                          </li>
                          <li>
                              LIENOU JEAN-PIERRE
                          </li>
                      </td>
                  </tr>
                  <tr>
                      <td>6</td>
                      <td>CENP2101</td>
                      <td>FUNDAMENTALS OF COMPUTER ENGINEERING</td>
                      <td>3</td>
                      <td>E</td>
                      <td><li>
                          LIENOU JEAN-PIERRE
                      </li></td>
                  </tr>            
                  <tr class="bg-primary">
                      <td colspan="6">
                          <div  class="title">Required Courses</div>
                      </td>
                  </tr>
                  
                  <tr>
                      <td>7</td>
                      <td>CENP2101</td>
                      <td>FUNDAMENTALS OF COMPUTER ENGINEERING</td>
                      <td>3</td>
                      <td>E</td>
                      <td><li>
                          LIENOU JEAN-PIERRE
                      </li></td>
                  </tr>
                  <tr>
                      <td>8</td>
                      <td>CENP2101</td>
                      <td>FUNDAMENTALS OF COMPUTER ENGINEERING</td>
                      <td>3</td>
                      <td>E</td>
                      <td><li>
                          LIENOU JEAN-PIERRE
                      </li></td>
                  </tr>  
                  <tr>
                      <td colspan="3"><h3 class="title">Total Credit Value</h3></td>
                      <td>29</td>
                      <td colspan="2"></td>
                  </tr>
              </table>
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
