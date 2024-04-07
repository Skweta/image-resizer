<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Image Resizer & Compressor</title>
<style>
  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f8f9fa;
    color: #333;
  }

  .container {
    max-width: 600px;
    margin: 50px auto;
    padding: 20px;
    border-radius: 8px;
    background-color: #fff;
    box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.1);
  }

  h1 {
    text-align: center;
    color: #007bff;
    margin-bottom: 30px;
    font-weight: bold;
    text-transform: uppercase;
    letter-spacing: 2px;
  }

  select, input[type="number"], input[type="range"], button {
    width: calc(100% - 20px);
    padding: 10px;
    margin: 5px 0;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-size: 16px;
    background-color: #f8f9fa;
  }

  select:focus, input[type="number"]:focus, input[type="range"]:focus, button:focus {
    outline: none;
    border-color: #007bff;
  }

  button {
    background-color: #007bff;
    color: #fff;
    font-weight: bold;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }

  button:hover {
    background-color: #0056b3;
  }

  #output {
    margin-top: 20px;
    text-align: center;
  }

  img {
    max-width: 100%;
    height: auto;
    display: block;
    margin-top: 20px;
    border-radius: 5px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
  }
</style>
</head>
<body>
<div class="container">
  <h1>Image Resizer & Compressor</h1>
  <div>
    <label for="exam">Select Exam:</label>
    <select id="exam">
      <option value="custom">Custom Requirements</option>
      <option value="SI_CPO_2024">SI/CPO/SELECTION POST PHASE XII 2024</option>
      <option value="SBI_PO_CLERK">SBI PO/SBI Clerk</option>
    </select>
  </div>
  <div id="documentType" style="display: none;">
    <label for="docType">Type of Document:</label>
    <select id="docType">
      <!-- Options will be dynamically added based on the selected exam -->
    </select>
  </div>
  <input type="file" accept="image/*" id="imageInput">
  <div>
    <label for="width">Width: </label>
    <input type="number" id="width" value="200">
    <select id="widthUnit">
      <option value="px">px</option>
      <option value="cm">cm</option>
    </select>
  </div>
  <div>
    <label for="height">Height: </label>
    <input type="number" id="height" value="200">
    <select id="heightUnit">
      <option value="px">px</option>
      <option value="cm">cm</option>
    </select>
  </div>
  <div>
    <label for="quality">Quality (1-100): </label>
    <input type="range" id="quality" min="1" max="100" value="80">
  </div>
  <div>
    <label for="maxSize">Maximum Size (KB): </label>
    <input type="number" id="maxSize" value="200">
  </div>
  <div>
    <label for="minSize">Minimum Size (KB): </label>
    <input type="number" id="minSize" value="20">
  </div>
  <div>
    <label for="format">Format:</label>
    <select id="format">
      <option value="jpeg">JPEG</option>
      <option value="png">PNG</option>
    </select>
  </div>
  <button id="resizeBtn">Resize & Compress</button>
  <button id="downloadBtn">Download & Save</button>
  <a id="downloadLink" style="display: none;"></a>
  <div id="output"></div
</div>
<script>
  document.getElementById('exam').addEventListener('change', function() {
    var exam = this.value;
    var docTypeSelect = document.getElementById('docType');
    var documentTypeDiv = document.getElementById('documentType');

    if (exam === 'SI_CPO_2024') {
      documentTypeDiv.style.display = 'block';
      docTypeSelect.innerHTML = '<option value="signature">Signature</option>';
      setExamDetails(4, 2, 10, 20, 'cm');
    } else if (exam === 'SBI_PO_CLERK') {
      documentTypeDiv.style.display = 'block';
      docTypeSelect.innerHTML = '<option value="profile_photo">Profile Photo</option><option value="signature">Signature</option>';
      // Initially, setting the exam details for profile photo
      setExamDetails(200, 230, 20, 50, 'px');
    } else {
      documentTypeDiv.style.display = 'none';
    }
  });

  document.getElementById('docType').addEventListener('change', function() {
    var exam = document.getElementById('exam').value;
    var docType = this.value;
    var width, height, maxSize;
    
    if (exam === 'SBI_PO_CLERK') {
      if (docType === 'profile_photo') {
        setExamDetails(200, 230, 20, 50, 'px')
      } else if (docType === 'signature') {
        setExamDetails(140, 60, 10, 20, 'px')
      }
    }
  });

  function setExamDetails(width, height, minSize, maxSize, units) {
    document.getElementById('width').value = width;
    document.getElementById('height').value = height;
    document.getElementById('maxSize').value = maxSize;
    document.getElementById('minSize').value = minSize; // Add this line
    document.getElementById('widthUnit').value = units;
    document.getElementById('heightUnit').value = units;
  }

  document.getElementById('resizeBtn').addEventListener('click', function() {
    var imageInput = document.getElementById('imageInput');
    var width = document.getElementById('width').value;
    var widthUnit = document.getElementById('widthUnit').value;
    var height = document.getElementById('height').value;
    var heightUnit = document.getElementById('heightUnit').value;
    var quality = document.getElementById('quality').value;
    var format = document.getElementById('format').value;
    var output = document.getElementById('output');
    var downloadLink = document.getElementById('downloadLink');
    var downloadBtn = document.getElementById('downloadBtn');
    var maxSizeKB = document.getElementById('maxSize').value;
    var minSizeKB = document.getElementById('minSize').value;

    // Convert width and height to pixels if units are in cm
    if (widthUnit === 'cm') {
      width = width * 37.7952755906; // 1 cm = 37.7952755906 pixels
    }
    if (heightUnit === 'cm') {
      height = height * 37.7952755906; // 1 cm = 37.7952755906 pixels
    }

    // Convert minSizeKB and maxSizeKB to bytes
    var minSizeBytes = minSizeKB * 1024;
    var maxSizeBytes = maxSizeKB * 1024;

    // Check if width and height meet the required dimensions
    var exam = document.getElementById('exam').value;
    var docType = document.getElementById('docType').value;
    var validWidth, validHeight;

    if (exam === 'SI_CPO_2024') {
      validWidth = 4 * 37.7952755906; // 4cm to px
      validHeight = 2 * 37.7952755906; // 2cm to px
    } else if (exam === 'SBI_PO_CLERK') {
      if (docType === 'profile_photo') {
        validWidth = 200;
        validHeight = 230;
      } else if (docType === 'signature') {
        validWidth = 140;
        validHeight = 60;
      }
    }

    if (width !== validWidth || height !== validHeight) {
      output.innerHTML = '<p style="color: red;">Please set the width and height according to the requirements.</p>';
      return;
    }

    // Check if the file size exceeds the maximum size
    if (maxSizeBytes < minSizeBytes || maxSizeBytes < 0) {
      output.innerHTML = '<p style="color: red;">Maximum size should be greater than minimum size and positive.</p>';
      return;
    }

    // Validation passed, continue with resizing and compressing
    var file = imageInput.files[0];
    var reader = new FileReader();

    reader.onload = function(e) {
      var img = new Image();
      img.src = e.target.result;

      img.onload = function() {
        var canvas = document.createElement('canvas');
        var ctx = canvas.getContext('2d');

        canvas.width = width;
        canvas.height = height;

        ctx.drawImage(img, 0, 0, width, height);

        var resizedImage = canvas.toDataURL('image/' + format, quality / 100);

        // Check if the file size exceeds the maximum size
        if (resizedImage.length > maxSizeBytes) {
          output.innerHTML = '<p style="color: red;">Output image exceeds maximum file size.</p>';
          return;
        }

        output.innerHTML = '<img src="' + resizedImage + '" alt="Resized Image">';
        downloadLink.href = resizedImage;
        downloadLink.download = 'resized_image.' + format;
        downloadBtn.style.display = 'inline';
      }
    }

    reader.readAsDataURL(file);
  });

  document.getElementById('downloadBtn').addEventListener('click', function() {
    var downloadLink = document.getElementById('downloadLink');
    downloadLink.click();
  });
</script>
</body>
</html>
