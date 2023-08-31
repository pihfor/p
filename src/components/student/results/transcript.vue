<script >
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
              <h5 class="card-title mb-3 mb-md-0 flex-grow-1">Draft transcript</h5>
          </div>
      </b-card-header>
    </b-card>
    <b-card>
      <b-card-body class="">
         
        <div>    
            <header>
                <div>
                    <h5>Republic of Cameroon</h5>
                    <p>-------</p>
                    <h5>Ministry of Higher Education</h5>
                    <h3>KELDEN BILINGUAL HIGHER INSTITUTE OF PROFESSIONAL STUDIES</h3>
                    <h4>AFFILIATED TO THE UNIVERSITY OF BAMENDA</h4>
                    <h6>Authorization N<sup>o</sup> 18-10204/1/MINESUP/SG/DDES/SD-ESUP/SDA/LMN </h6>
                    <h6>N<sup>o</sup> 013MINEFOP/SG/DFOP/SDGSF/SACD</h6>
                    <h6>Yaounde derriere Lycee de Biyamassi</h6>
                    <h6>Contact 6773778901/651984308, Email:keldeninstitute21@gmail.com</h6>
                    <h6>Facebook: kelden bilingual Institute of Profeesional Studies</h6>
                    
                </div>
                <hr> 
            </header> 
            <div class="heading">
                <h4>Academic year :</h4>
                <h3>STUDENT TRANSCRIPT LEVEL</h3>
            </div>
            <table class="one">
                <thead>
                    <tr>
                        <th>Student's name :</th>
                        <th>Registration number :</th>
                    </tr>
                    <tr>
                        <th>Date of Birth :</th>
                        <th>Place of Birth :</th>
                    </tr>
                    <tr>
                        <th>School/Faculty</th>
                        <th>Department :</th>
                    </tr>
                    <tr>
                        <th>Degree in view :</th>
                        <th>Sex :</th>
                    </tr>
                </thead>
            </table>
            <div class="caption">Academic Year :</div>
            <div class="semester">
                <div class="col-3">
                    <div class="title">First Semester</div>
                    <table>
                        <thead>
                            <tr>
                                <th>Code</th>
                                <th>title</th>
                                <th>CV</th>
                                <th>Marks</th>
                                <th>GD</th>
                                <th>GP</th>
                                <th>WP</th>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
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
                <div class="col-3">
                    <div class="title">Resit Semester</div>
                    <table>
                        <thead>
                            <tr>
                                <th>Code</th>
                                <th>title</th>
                                <th>CV</th>
                                <th>Marks</th>
                                <th>GD</th>
                                <th>GP</th>
                                <th>WP</th>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
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
                <div class="col-3">
                    <div class="title">Second Semester</div>
                    <table>
                        <thead>
                            <tr>
                                <th>Code</th>
                                <th>title</th>
                                <th>CV</th>
                                <th>Marks</th>
                                <th>GD</th>
                                <th>GP</th>
                                <th>WP</th>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
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
                <div class="col-3">
                    <div class="title">Resit Semester</div>
                    <table>
                        <thead>
                            <tr>
                                <th>Code</th>
                                <th>title</th>
                                <th>CV</th>
                                <th>Marks</th>
                                <th>GD</th>
                                <th>GP</th>
                                <th>WP</th>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
                                <td>50</td>
                                <td>C</td>
                                <td>2</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>CENP2103</td>
                                <td>INTRODUCTION TO COMPUTER NETWORKS</td>
                                <td>2</td>
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
            <div class="col-12 mt-3">
                <div class="col-3">
                    <table>
                        <thead>
                            <caption>Grade System</caption>
                            <tr>
                                <th>Grade</th>
                                <th>Mark</th>
                                <th>GP</th> 
                            </tr>
                            <tr>
                                <td>A</td>
                                <td>(80-100)</td>
                                <td>4.0</td>
                            </tr>
                            <tr>
                                <td>B</td>
                                <td>(70-79)</td>
                                <td>3.5</td>
                            </tr>
                            <tr>
                                <td>C+</td>
                                <td>(60-69)</td>
                                <td>3.0</td>
                            </tr>
                            <tr>
                                <td>C</td>
                                <td>(50-59)</td>
                                <td>2.5</td>
                            </tr>
                            <tr>
                                <td>D+</td>
                                <td>(45-49)</td>
                                <td>1.5</td>
                            </tr>
                            <tr>
                                <td>D</td>
                                <td>(40-44)</td>
                                <td>1.0</td>
                            </tr>
                            <tr>
                                <td>F</td>
                                <td>(0-39)</td>
                                <td>0.0</td>
                            </tr>
                        </thead>
                    </table>
                </div>
                <div class="col-3">
                    <table>
                        <thead>
                            <caption>Degree Classification</caption>                          
                            <tr>
                                <th>
                                    GPA/class of Degree
                                </th>
                            </tr>
                            <tr>
                                <td>3.60-4.00 First Class </td>
                            </tr>
                            <tr>
                                <td>3.00-3.59 Second Class-UD</td>
                            </tr>
                            <tr>
                                <td>2.50-2.99 Second Class-LD</td>
                            </tr>
                            <tr>
                                <td>2.25-2.49 Third Class</td>
                            </tr>
                            <tr>
                                <td>2.00-2.24 Pass</td>
                            </tr>
                            <tr>
                                <td>UD(Upper Division)</td>
                            </tr>
                            <tr>
                                <td>LD(Lower Division)</td>
                            </tr>
                        </thead>
                    </table>
                </div>
                <div class="col-3">
                    <table>
                        <thead>
                            <caption>Legends</caption>                         
                            <tr>
                                <th>
                                    I = incomplete
                                </th>
                            </tr>
                            <tr>
                                <td>
                                    X = Absent
                                </td>
                            </tr>
                            <tr>
                                <td>* = Mark obtained After Resit</td>
                            </tr>
                            <tr>
                                <td>GP = Grade Point</td>
                            </tr>
                            <tr>
                                <td>GPA = Grade Point Average</td>
                            </tr>
                            <tr>
                                <td>CGPA = Cumulative Grade Point Average</td>
                            </tr>
                            <tr>
                                <td>WP= Weighted Point</td>
                            </tr>
                            <tr>
                                <td>.</td>
                            </tr>
                        </thead>
                    </table>
                </div>

                <div class="watermark">
                    <span class="text-primary">Draft</span>
                </div>  
                <div class="col-3">
                    <table>
                        <thead>
                            <caption>Legends</caption>                         
                            <tr>
                                <th>
                                Total Credits Attempted :
                                </th>
                            </tr>
                            <tr>
                                <td>
                                    Total Credits Earned :
                                </td>
                            </tr>
                            <tr>
                                <td>Cumulative GPA :</td>
                            </tr>
                            <tr>
                                <td>.</td>
                            </tr>
                            <tr>
                                <td>.</td>
                            </tr>
                            <tr>
                                <td>.</td>
                            </tr>
                            <tr>
                                <td>.</td>
                            </tr>
                            <tr>
                                <td>.</td>
                            </tr>
                        </thead>
                    </table>
                </div>
            </div>
        </div>
      </b-card-body>
    </b-card>
</div>
</template>
<style scoped>
 *{  
    box-sizing: border-box;
}
.watermark {
  position: absolute;
  top: 75%;
  left: 50%;
  font-size: 200px;
  transform: translate(-50%, -50%);
  rotate: 180;
  opacity: 0.1;
  z-index: 9999;
}

header{
    margin-top: 2%;
    text-align: center;
    margin-bottom: 10px;
}
hr{
    margin-top:5px;
    height: 3px;
    background: gray;
}
body{
    max-width:2100vw;
    margin: auto;
    margin: 20px;
}
th{
    font-size: 11px;
}
td{
    font-size: 7px;
}
.heading{
    display: flex;
    padding: 10px;
    background: navy;
}
.danger{
    background: rgb(253, 124, 124);
}
.heading h4{
    flex: 1.2;
    color: #f1f1f1;
}
.heading h3{
    flex: 1.8;
    color: #f1f1f1;
}
.one thead th{
    border: none;
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
.two th , td {
    text-align: center;
}
caption{
    font-size: 12px;
    padding: 2px;
}
.caption{
    text-align: center;    
    background: navy;
    color: #f1f1f1;
    padding: 5px; 
}
.title{    
    text-align: center;    
    background: rgb(162, 219, 241);
    padding: 5px; 
    border: 1px solid gray;
}

.row::after {
  content: "";
  clear: both;
  display: block;
}

[class*="col-"] {
  float: left;
}

html {
  font-family: "Lucida Sans", sans-serif;
}
.container{
    width: 100%;
}
.mt-3{
    margin-top: 3px;
}

/* For desktop: */
.col-1 {width: 8.33%;}
.col-2 {width: 16.66%;}
.col-3 {width: 25%;}
.col-4 {width: 33.33%;}
.col-5 {width: 41.66%;}
.col-6 {width: 50%;}
.col-7 {width: 58.33%;}
.col-8 {width: 66.66%;}
.col-9 {width: 75%;}
.col-10 {width: 83.33%;}
.col-11 {width: 91.66%;}
.col-12 {width: 100%;}

@media only screen and (max-width: 1115px) {
  /* For mobile phones: */
  [class*="col-"] {
    width: 100%;
  }
}
</style>
