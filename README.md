# Mobile-Charging-Animation
Mobile Charging Animation in html/css/js
<!DOCTYPE html>
<html lang="en">
<head>
    
    <title>electronic_Code</title>
</head>
<style>
    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    body{
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
        color: white;
        background-color: black;
    }
    .box{
        display: flex;
        justify-content: center;
        align-items: center;
        position: relative;
        width: 311px;
        height: 400px;
        flex-direction: column;
        border-radius: 23px;
        overflow: hidden;
        background: #0e0e1a;
    }
    .all-compunt{
        display: flex;
        position: relative;
        justify-content: center;
        align-items: center;
        height: 400px;
        width: 300px;
        flex-direction: column;
        background: #00001c;
        border-radius: 23px;
        overflow: hidden;
    }
    .rotat-color{
        width: 30rem;
        height: 10rem;
        background: linear-gradient(45deg,#ff006e,#6d00ff);
        position: absolute;
        animation: rotat 4s infinite ease-in-out;
    }
    @keyframes rotat{
        0%{
            transform: rotate(0deg);
        }
        100%{
            transform: rotate(359deg);
        }
    }
    .all-compunt .percent{
        position: relative;
        width: 183px;
        height: 183px;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .circle{
        width: 12rem;
        border-radius: 50%;
        z-index: 2;
    }
    #number{
        position: absolute;
        font-size: 28px;
        font-family: cursive;
        font-weight: 600;
        z-index: 2;
    }
    .bubble{
        width: 3rem;
        position: absolute;
        bottom: 5rem;
        animation: bubbleani 1s infinite ease-in-out;
    }
    @keyframes bubbleani{
        0%,100%{
            opacity: 0;
        }
        50%{
            opacity: 1;
        }
    }
    .img-charg img{
        width: 6rem;
        position: relative;
        bottom: -4rem;
    }
</style>
<body>
    <div class="box">
        <div class="rotat-color"></div>
        <div class="all-compunt">
            <div class="percent">
                <img src="./circle.gif" alt="" class="circle">
                <div id="number">
                    0%
                </div>
            </div>
            <img src="./bubble.png" alt="" class="bubble">
            <div class="img-charg">
                <img src="./charger.png" alt="">
            </div>
        </div>
    </div>
    <script>
        const numb=document.querySelector("#number");
        let conter=0;
        setInterval(()=>{
            if(conter==100){
                clearInterval();

            }
            else{
                conter+=1;
                numb.textContent=conter+"%";
            }
        },200);
    </script>
</body>
</html>
