<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Netflix</title>
    <style>

        **HERE CSS**
        *{
            margin: 0;
            padding: 0;
            font-family:'Consolas';
            box-sizing: border-box;
        }
        body{
            background: #000;
            color: #fff;
        }
        .header{
            width: 100%;
            height: 100vh;
            background-image: linear-gradient(rgba(0,0,0,0.7),rgba(0,0,0,0.7)),url(header-image.png);
            background-size: cover;
            background-position: center ;
            padding: 10px 8%;
            position: relative;
        }
        nav{
            display:flex ;
            align-items: center;
            justify-content: space-between;
        
        }
        .logo{
            width: 150px;
            cursor: pointer;
        
        }
        nav button{
            border: 0;
            outline: 0;
            background: #db0001;
            color: #fff;
            padding: 7px 20px;
            font-size: 12px;
            border-radius: 4px;
            margin-left: 10px;
            cursor: pointer;
        }
        .language-btn{
            display: inline-flex;
            align-items: center;
            background: transparent;
            border: 1px solid #fff;
            padding: 7px 10px;
        
        
        }
        .language-btn img{
            width: 10px;
            margin-left: 10px;
        
        }
        .header-content{
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%,-50%);
            text-align: center;
            margin-top: 100px;
        
        }
        .header-content h1{
            font-size: 60px;
            line-height: 70px;
            font-weight: 600;
            max-width: 650px;
        }
        .header-content h3{
            font-weight: 400;
            margin-bottom: 20px;
        
        }
        .email-signup{
            background: #fff;
            border-radius: 4px;
            display: flex;
            align-items: center;
            margin-top: 30px;
            overflow: hidden;
        }
        .email-signup input{
            flex:1;
            border: 0;
            outline: 0;
            margin-left: 20px;
        
        }
        .email-signup button{
            background: #db0001;
            border: 0;
            outline: 0;
            color:#fff;
            font-size: 16px;
            cursor: pointer;
            padding: 15px 30px;
        
        }
        .feature{
            padding: 50px 12%;
            font-size: 22px;
        
        }
        .row{
            display: flex;
            width:100%;
            align-items: center;
            flex-wrap: wrap;
            padding: 50px 0;
        }
        .text-col{
            flex-basis: 50%;
            margin-bottom: 20px;
        
        }
        .img-col{
            flex-basis: 50%;
            margin-bottom: 20p;
        
        
        }
        .img-col img{
            display: block;
            width: 90%;
            margin:auto ;
        }
        .feature h2{
            font-size: 50px;
            font-weight: 600;
            margin-bottom: 20px;
        }
        /* ---------faq-------- */
        .faq{
            padding: 10px 12%;
            text-align: center;
            font-size: 18px;
        }
        .faq h2{
            font-weight: 500;
            font-size: 40px;
        
        }
        .accordion{
            margin: 60px auto;
            width: 100%;
            max-width: 750px;
        
        
        }
        .accordion li{
            list-style:none;
            width: 100%;
            padding: 5px;
        
        }
        .accordion li label{
            display: flex;
            align-items: center;
            padding: 20px;
            font-size: 18px;
            font-weight: 500;
            background: #303030;
            margin-bottom: 2px;
            cursor: pointer;
            position: relative;
        
        }
        label::after{
            content: "+";
            font-size: 34px;
            position: absolute;
            right: 20px;
            transition: transform 0.5s;
        
        }
        input[type="radio"]{
            display: none;
        
        }
        .accordion .content{
            background: #303030;
            text-align: left;
            padding: 0 20px;
            max-height: 0;
            overflow:hidden ;
            transition: max-height 0.5s,padding 0.5s;
        }
        .accordion input[type="radio"]:checked + label + .content{
            max-height: 600px;
            padding: 30px 20px;
        
        }
        .accordion input[type="radio"]:checked + label::after{
            transform: rotate(135deg);
        }
        
        .faq .email-signup{
            max-width: 600px;
            margin: 20px;
        
        }
        .faq small{
            font-size: 30px;
        }
        /* -----footer======= */
        .footer{
            padding: 50px 15% 10px;
            border-top: 6px solid #333;
            color:#777
        }
        .footer h2{
            font-size: 18px;
            font-weight: 400;
            margin-bottom:30px ;
        }
        .footer .col{
            flex-basis: 25%;
            flex-grow: 1;
            margin-bottom: 20px;
        }
        .footer .col a{
            display: block;
            text-decoration: none;
            color: #777;
            font-size: 14px;
            margin-bottom: 10px;
        
        }
        .footer .row{
            align-items: flex-start;
            padding: 10px 0;
        }
        .footer .language-btn{
            color: white;
            padding: 10px 20px;
            border-radius: 3px;
        }
        .copyright-text{
            font-size: 14px;
            margin-top:20px ;
            margin-bottom: 10px;
        
        }
        /* ------media queries for smsall screen---------- */
        @media only screen and (max-width:600px){
            .logo{
                width: 100px;
        
            }
            nav button{
                padding: 5px 10px;
            }
            nav .language-btn{
                padding: 4px 8px;
            }
            .header-content{
                position: unset;
                transform: none;
                padding-top: 150px;
        
            }
            .header-content h1{
                font-size: 30px;
            }
            .email-signup button{
                font-size: 12px;
                padding: 10px 15px;
            }
            .text-col,.img-col{
                flex-basis: 100%;
        
            }
            .feature h2{
                font-size: 30px;
            }
            .feature h3{
                font-size: 30px;
            }
            .feature p{
                font-size: 30px;
            }
            .row:nth-child(2),.row:nth-child(4){
                flex-direction: column-reverse;
            }
            .features .row{
                padding: 10px 0;
        
            }
            .faq h2{
                font-size: 20px;
            }
            .accordion .content{
                font-size: 14px;
        
            }
            .accordion li label{
                padding: 10px;
                font-size: 14px;
        
            }
            label::after{
                font-size: 22px;
            }
        
        }
        </style>
</head>
<body>
    <div class="header">
        <nav>
            <img src="https://www.edigitalagency.com.au/wp-content/uploads/Netflix-logo-red-black-png.png" class="logo">
            <div>
                <button class="language-btn">English <img src="down-icon.png" alt=""></button>
                <button>Sign In</button>
            </div>
        </nav>
        <div class="header-content">
            <h1>Unlimited movies,TV shows and more.</h1>
            <h3>Watch anywhere.Cancel anytime</h3>
            <p>Ready to watch Enter ypur email to creat or restart your memebership.</p>
            <form class="email-signup">
                <input type="emai
                " placeholder="Email address" required>
                <button type="submit">get started</button>
            </form>
        </div>

    </div>
    <div class="feature">
        <div class="row">
            <div class="img-col">
                <img src="https://assets.nflxext.com/ffe/siteui/acquisition/ourStory/fuji/desktop/tv.png" >
            </div>
            <div class="text-col">
                <h2>Enjoy on your TV.</h2>
                <p>
                    Watch on smart TVs, Playstation,xbox,Chromecast, Apple TV , Blu-ray players and more.
                </p>
            </div>

        </div>

    </div>
    <div class="row">
        <div class="img-col">
            <img src="https://assets.nflxext.com/ffe/siteui/acquisition/ourStory/fuji/desktop/mobile-0819.jpg" >
        </div>
        <div class="text-col">
            <h2>Download your shows to watch offline.</h2>
            <p>
                Save your favourites easily and always have something to watch.
            </p>
        </div>

    </div>
    <div class="row">
        <div class="img-col">
            <img src="https://assets.nflxext.com/ffe/siteui/acquisition/ourStory/fuji/desktop/device-pile-in.png" >
        </div>
        <div class="text-col">
            <h2>Watch everywhere.</h2>
            <p>
                Stream unlimited movies and TV shows on your phone, tablet, laptop, and TV.
            </p>
        </div>

    </div>
    <div class="row">
        <div class="img-col">
            <img src="https://occ-0-4606-3646.1.nflxso.net/dnm/api/v6/19OhWN2dO19C9txTON9tvTFtefw/AAAABYjXrxZKtrzxQRVQNn2aIByoomnlbXmJ-uBy7du8a5Si3xqIsgerTlwJZG1vMpqer2kvcILy0UJQnjfRUQ5cEr7gQlYqXfxUg7bz.png?r=420" >
        </div>
        <div class="text-col">
            <h2>Create profiles for children.</h2>
            <p>
                Send children on adventures with their favourite characters in a space made just for them—free with your membership.
            </p>
        </div>

    </div>
    <div class="faq">
        <h2>Frequent Asked Question</h2>
        <ul class="accordion">
            <li>
                <input type="radio" name="accordion" id="first">
                <label for="first">What is Netflix?</label>
                <div class="content">
                    <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate corrupti sed neque animi in earum placeat fuga ducimus. Explicabo, praesentium.
                    </p>
                </div>
            </li>
            <li>
                <input type="radio" name="accordion" id="second">
                <label for="first">How much does Netflix cost?</label>
                <div class="content">
                    <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate corrupti sed neque animi in earum placeat fuga ducimus. Explicabo, praesentium.
                    </p>
                </div>
            </li>
            <li>
                <input type="radio" name="accordion" id="third">
                <label for="first">Where can i watch?</label>
                <div class="content">
                    <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate corrupti sed neque animi in earum placeat fuga ducimus. Explicabo, praesentium.
                    </p>
                </div>
            </li><li>
                <input type="radio" name="accordion" id="fourth">
                <label for="first">Where can i wathc Netflix?</label>
                <div class="content">
                    <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate corrupti sed neque animi in earum placeat fuga ducimus. Explicabo, praesentium.
                    </p>
                </div>
            </li>
        </ul>
        <small>Ready to Watch? Enter your email to create or restart your membership.</small>
        <form class="email-signup">
            <input type="emai
            " placeholder="Email address" required>
            <button type="submit">get started</button>
        </form>
    </div>

    <div class="footer">
        <h2>Question? call 00-000-000-000</h2>

        <div class="row">
            <div class="col">
                <a href="#">FAQ</a>
                <a href="#">Invester Relation</a>
                <a href="#">Privacy </a>
                <a href="#">Speed Test</a>

            </div>
            <div class="col">
                <a href="#">Help</a>
                <a href="#">Jobs</a>
                <a href="#">Cookies Preference</a>
                <a href="#">Legal notices</a>

            </div>
            <div class="col">
                <a href="#">Account</a>
                <a href="#">Ways to watch</a>
                <a href="#">Corporate Information </a>
                <a href="#">only pn Netflix</a>

            </div>
            <div class="col">
                <a href="#">Media Center</a>
                <a href="#">Terms of Use</a>
                <a href="#">Contact Us </a>
                <a href="#">only pn Netflix</a>

            </div>
        </div>
        <button  class="language-btn">English <img src="down-icon.png" alt=""></button>
        <p class="copyright-text">Netflix India</p>
    </div>

</body>
</html> 
