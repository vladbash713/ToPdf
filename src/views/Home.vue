<template>
  <main>
    <div class = "pdf-wrapper">
      <div ref="printMe" id="nodeToRenderAsPDF">
      <section  class="page">
        <div class="overlay">
          <div id="left_rect"></div>
          <div id="right_rect"></div>
        </div>
        <div class="left">
          <img src="https://res.cloudinary.com/flexi-images/image/upload/v1563038123/test/photo-1103597_1280_plezhe.png"> 
          <!-- <img src="https://upload.wikimedia.org/wikipedia/commons/f/f9/Phoenicopterus_ruber_in_S%C3%A3o_Paulo_Zoo.jpg"> -->
          <div class="section about">
            <h1>About Me</h1>
            <p>
              Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
            </p>
          </div>
          <div class="section contact">
            <h1>Contact</h1>
            <p>
              John Doe<br>
              Some Street 123<br>
              1234 City<br><br>
              <b>T:</b> 01234 5678910<br>
              <b>M:</b> john.doe@mail.com
            </p>
          </div>
        </div>
        <div class="right">
          <div class="top">
            <h1>John Doe</h1>
            <h2>01.01.1990</h2>
          </div>
          <div class="section">
            <h1>Lorem Ipsum</h1>
            <div class="sub half">
              <h2>School (2,0)</h2>
              <h3>Sep 2000 - Aug 2015</h3>
              <h4>Some School</h4>
            </div>
            <div class="sub half">
              <h2>B.Sc. Business</h2>
              <h3>Sep 2016 - Mar 2019</h3>
              <h4>Some University</h4>
            </div>
          </div>
          <div class="section">
            <h1>Lorem Ipsum</h1>
            <div class="sub">
              <h2>Softwaredeveloper at some company</h2>
              <h3>Aug 2015 - Mar 2016</h3>
              <ul>
                <li>Lorem ipsum dolor sit amet, consetetur sadipscing elitr</li>
                <li>Lorem ipsum dolor sit amet, consetetur sadipscing elitr</li>
                <li>Lorem ipsum dolor sit amet, consetetur sadipscing elitr</li>
              </ul>
            </div>
            <span class="dash"></span>
            <div class="sub">
              <h2>Softwaredeveloper at some company</h2>
              <h3>Apr 2016 - Feb 2017</h3>
              <ul>
                <li>Lorem ipsum dolor sit amet, consetetur sadipscing elitr</li>
                <li>Lorem ipsum dolor sit amet, consetetur sadipscing elitr</li>
                <li>Lorem ipsum dolor sit amet, consetetur sadipscing elitr</li>
                <li>Lorem ipsum dolor sit amet, consetetur sadipscing elitr</li>
                <li>Lorem ipsum dolor sit amet, consetetur sadipscing elitr</li>
                <li>Lorem ipsum dolor sit amet, consetetur sadipscing elitr</li>
              </ul>
            </div>
            <span class="dash"></span>
            <div class="sub">
              <h2>Softwaredeveloper at some company</h2>
              <h3>Mar 2017 - Mar 2018</h3>
              <ul>
                <li>Lorem ipsum dolor sit amet, consetetur sadipscing elitr</li>
                <li>Lorem ipsum dolor sit amet, consetetur sadipscing elitr</li>
                <li>Lorem ipsum dolor sit amet, consetetur sadipscing elitr</li>
                <li>Lorem ipsum dolor sit amet, consetetur sadipscing elitr</li>
                <li>Lorem ipsum dolor sit amet, consetetur sadipscing elitr</li>
              </ul>
            </div>
          </div>
          <div class="section">
            <h1>Lorem Ipsum</h1>
            <div class="sub half">
              <h2>IT-Knowledge</h2>
              <ul>
                <li>PHP, Java, JavaScript</li>
                <li>HTML, CSS, jQuery, MySQL</li>
                <li>Operating Systems: Windows, MacOS</li>
              </ul>
            </div>
            <div class="sub half">
              <h2>Languages</h2>
              <ul>
                <li>German</li>
                <li>English</li>
                <li>French</li>
                <li>Spanish</li>
              </ul>
            </div>
            <span class="dash"></span>
            <div class="sub">
              <h2>Interests</h2>
              <ul>
                <li>Lorem ipsum dolor sit amet, consetetur sadipscing elitr:</li>
                <ul>
                  <li>Sed diam nonumy eirmod tempor invidunt</li>
                  <li>Sed diam nonumy eirmod tempor invidunt</li>
                  <li>Sed diam nonumy eirmod tempor invidunt</li>
                </ul>
                <li>
                  Sed diam nonumy eirmod tempor invidunt
                </li>
              </ul>
            </div>
          </div>
        </div>
      </section>
      </div>
    </div>
    <v-btn @click="print" flat small class="primary caption">Print CV</v-btn>
  </main>
</template>

<style type="text/css" scoped>
* {
  margin: 0;
  padding: 0;
  font-family: 'Open Sans';
}

body {
  background: #aaa;
}

.dash {
  content: '';
  width: 100%;
  height: 1px;
  background: #676767;
  display: block;
  clear: both;
}

.page {
  width: 1000px;
  height: 1470px;
  background: white;
  position: relative;
  overflow: hidden;
}

.page .overlay #left_rect {
  width: 200%;
  height: 500px;
  background: #676767;
  position: absolute;
  z-index: 1;
  transform: rotate(-45deg);
  left: -100%;
  top: -50px;
}

.page .overlay #right_rect {
  width: 200%;
  height: 500px;
  background: #26556d;
  position: absolute;
  transform: rotate(16.18deg);
  z-index: 2;
  left: -100px;
  top: -249px;
}

.page .left,
.page .right {
  float: left;
}

.page .left {
  width: calc(38.1966% - 50px);
  height: 100%;
  background: #eee;
  padding: 565px 25px 0;
}

.page .left img {
  width: 250px;
  position: absolute;
  left: 60px;
  top: 190px;
  z-index: 2;
}

.page .left .section {
  margin-bottom: 25px;
}

.page .left .section.contact {
  position: absolute;
  left: 25px;
  bottom: 0;
}

.page .right {
  width: calc(61.8034% - 50px);
  height: 100%;
  margin-top: 200px;
  padding: 25px;
}

.page .right .top h1 {
  color: #255571;
  font-size: 35px;
  float: left;
}

.page .right .top h2 {
  color: #666;
  font-size: 20px;
  float: left;
  margin-top: 15px;
  margin-left: 10px;
  font-weight: 400;
}

.page .right .top:after {
  content: '';
  display: block;
  clear: both;
  height: 25px;
}

.page .right .section:after {
  content: '';
  display: block;
  clear: both;
  height: 25px;
}

.page .section h1 {
  color: #26556d;
  font-size: 25px;
  text-transform: uppercase;
}

.page .right .section .sub {
  padding: 5px 0 10px;
}

.page .right .section .sub.half {
  width: calc(50% - 10px);
  float: left;
}

.page .right .section .sub h2 {
  color: #676767;
  font-size: 18px;
}

.page .right .section .sub h3 {
  color: #676767;
  font-size: 18px;
  font-weight: 400;
  margin-bottom: 5px;
}

.page .right .section .sub h4,
.page .left .section p {
  color: #777;
  font-size: 17px;
  font-weight: 400;
}

.page .right .section .sub ul {
  margin-left: 30px;
  color: #777;
  font-size: 17px;
  font-weight: 400;
}
.pdf-wrapper{
  display: flex;
  justify-content: center;
  padding: 100px 0px;
}
</style>

<script>
const jsPDF = require('jspdf')
var domtoimage = require('dom-to-image');
export default {
  data: () => ({}),

  methods: {
    print() {
      const filename = 'Generated_CV.pdf';
      var node = document.querySelector('#nodeToRenderAsPDF')
      domtoimage.toPng(node)
      .then(function (dataUrl) {
        let imgWidth = 1000; 
        let imgHeight = 1470;
        const paperWidth = 595;
        const paperHeight = 842;
        // const pdf = new jsPDF({
        //   orientation: 'portrait',
        //   unit: 'pt',
        //   format: [paperWidth, imgHeight * paperWidth /imgWidth]
        // });
        // pdf.addImage(dataUrl, 'PNG', 0, 0, paperWidth, imgHeight * paperWidth /imgWidth);
        // pdf.save(filename);
          let img = new Image();
          img.src = dataUrl;
          
         img.onload = () => {
          let pdf = new jsPDF('p', 'pt', 'a4');
          var canvas = document.createElement("canvas");
          canvas.width = imgWidth;
          canvas.height = imgHeight;
          let ctx = canvas.getContext("2d");
          ctx.drawImage(img,0,0);
          var pxFullHeight = canvas.height;
          var pxPageHeight = Math.floor(canvas.width * paperHeight / paperWidth);
          var nPages = Math.ceil(pxFullHeight / pxPageHeight);
          var pageHeight = paperHeight;
          var pageCanvas = document.createElement('canvas');
          var pageCtx = pageCanvas.getContext('2d');
          pageCanvas.width = canvas.width;
          pageCanvas.height = pxPageHeight;
          for (var page=0; page<nPages; page++) {
            // Trim the final page to reduce file size.
            if (page === nPages-1 && pxFullHeight % pxPageHeight !== 0) {
              pageCanvas.height = pxFullHeight % pxPageHeight;
              pageHeight = pageCanvas.height * paperWidth / pageCanvas.width;
            }

            // Display the page.
            var w = pageCanvas.width;
            var h = pageCanvas.height;
            pageCtx.fillStyle = 'white';
            pageCtx.fillRect(0, 0, w, h);
            pageCtx.drawImage(canvas, 0, page*pxPageHeight, w, h, 0, 0, w, h);

            // Add the page to the PDF.
            if (page)  pdf.addPage();
            var imgData = pageCanvas.toDataURL('image/' + 'image/png', 0.95);
            pdf.addImage(imgData, 'image/png', 0, 0, paperWidth, pageHeight);
          }
          pdf.save(filename);
         }
        }
      );
    }
  }
}
</script>
