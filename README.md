<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div class="hero">
        <div  class="card">
            <h1>Isaiah</h1>
            <p>@isaiah</p>
            <img src="images.png" alt="not the person image" id="profile-pic">
            <label for="input-file">Upload image</label>
            <input type="file" accept="image/jpeg, image/png, image/jpg" id="input-file">
        </div>
    </div>
</body>
</html>

<style>
    *{
        margin: 0;
        padding: 0;
    }
    .hero{
        width: 100%;
        height: 100vh;
        background-color: #d1d1d1;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .card{
        width: 400px;
        background-color: #fff;
        padding: 40px;
        border-radius: 15px;
        text-align: center;

    }
    .card h1{
        font-weight:500%;
        font-size: 70px;
        color: #000;
    }
    .card img{
        width: 180px;
        height: 180px;
        border-radius: 50%;
        margin-top: 40px;
        margin-bottom: 40px;
    }
    label{
        display: block;
        width: 200px;
        background:#e3362c ;
        color: #fff;
        padding: 12px;
        margin: 10px auto;
        border-radius: 10px;
    }
    input{
        display: none;
    }
</style>


<script>
    var profilepic = document.getElementById("profile-pic");
    var inputfile = document.getElementById("input-file");
    inputfile.onchange = function(){
        profilepic.src = URL.createObjectURL(inputfile.files[0]);
    }

</script>
