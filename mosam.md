This is my weather App. This App fetch the data from the free weather site with the help of API key. And show the data according to city and my current location and also show the 5 day forecast and some basic information like polution and humity and according to weather the side bacground is also change.

index.html
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Weather App</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css" rel="stylesheet">
    <link href="style.css" rel="stylesheet">
</head>

<body>
    <div class="container">
        <div class="header">
            <div class = "mylogo">
            <img style="height: 60px;" src="https://cdn-icons-png.flaticon.com/512/3157/3157542.png" id="logo">
            <h1 class = "mylogotext"><b><span style="color:rgb(237, 207, 11)">STROM</span><span style="color:rgb(25, 217, 231)">METRICS</span></b></h1>
            </div>
            <div class="weather-input">
                <input type="text" name="city" id="city_input" placeholder="Enter City Name">
                <button type="button" id="searchBtn">
                    <i class="fa fa-search"></i> Search
                </button>
                <button type="button" id="locationBtn">
                    <i class="bx bx-target-lock"></i> Current Location
                </button>
            </div>
        </div>
    </div>

    <div class="city-name">
        <h2 id="cityNameDisplay">City Name</h2>
    </div>
    <div class="weather-data">
        <div class="weather-left">
           
            <div class="card">
                <div class="current-weather">
                    <div class="details">
                        <p>Now</p>
                        <h1>____&deg;C</h1>
                        <p>_______</p>
                    </div>
                    <div class="weather-icon">
                        <img src="https://openweathermap.org/img/wn/04d@2x.png" alt="cloud img">
                    </div>
                </div>
                <hr>
                <div class="card-footer">
                    <p><i class="fa fa-calendar"></i> _______</p>
                    <p><i class="fa fa-map-marker-alt"></i> _______</p>
                </div>
            </div>
            <div class="card">
                <h1 style="font-weight: bold;">5 Days Forecast</h1>
                <div class="day-forecast">
                    <div class="forecast-item">
                        <div class="icon-wrapper">
                            <img src="https://openweathermap.org/img/wn/02d.png" alt="cloud img">
                            <span>Day: _&deg;C</span>
                            <span>Night: _&deg;C</span>
                        </div>
                        <p>___</p>
                        <p>___</p>
                    </div>
                    <div class="forecast-item">
                        <div class="icon-wrapper">
                            <img src="https://openweathermap.org/img/wn/02d.png" alt="cloud img">
                            <span>Day: _&deg;C</span>
                            <span>Night: _&deg;C</span>
                        </div>
                        <p>___</p>
                        <p>___</p>
                    </div>
                    <div class="forecast-item">
                        <div class="icon-wrapper">
                            <img src="https://openweathermap.org/img/wn/02d.png" alt="cloud img">
                            <span>Day: _&deg;C</span>
                            <span>Night: _&deg;C</span>
                        </div>
                        <p>___</p>
                        <p>___</p>
                    </div>
                    <div class="forecast-item">
                        <div class="icon-wrapper">
                            <img src="https://openweathermap.org/img/wn/02d.png" alt="cloud img">
                            <span>Day: _&deg;C</span>
                            <span>Night: _&deg;C</span>
                        </div>
                        <p>___</p>
                        <p>___</p>
                    </div>
                    <div class="forecast-item">
                        <div class="icon-wrapper">
                            <img src="https://openweathermap.org/img/wn/02d.png" alt="cloud img">
                            <span>Day: _&deg;C</span>
                            <span>Night: _&deg;C</span>
                        </div>
                        <p>___</p>
                        <p>___</p>
                    </div>
                </div>
            </div>
            </div>
            <div class="weather-right">
                <h1 style="font-weight: bold; margin-left: 10px;">Today's Highlights</h1>
                <div class="highlights">
                    <div class="card">
                        <div class="card-head">
                            <p>Air Quality Index</p>
                            <p class="air-index aqi-1">Good</p>
                        </div>
                        <div class="air-quality-bar">
                            <div class="score-bar">
                                <div class="score-bar-fill" id="aqiScore" style="width: 0;"></div>
                            </div>
                        </div>
                        <div class="air-indices">
                            <i class="fa-solid fa-wind fa-3x"></i>
                            <div class="item">
                                <p>PM2.5</p>
                                <h2>_____</h2>
                            </div>
                            <div class="item">
                                <p>PM10</p>
                                <h2>_____</h2>
                            </div>
                            <div class="item">
                                <p>SO2</p>
                                <h2>_____</h2>
                            </div>
                            <div class="item">
                                <p>CO</p>
                                <h2>_____</h2>
                            </div>
                            <div class="item">
                                <p>NO</p>
                                <h2>_____</h2>
                            </div>
                            <div class="item">
                                <p>NO2</p>
                                <h2>_____</h2>
                            </div>
                            <div class="item">
                                <p>NH3</p>
                                <h2>_____</h2>
                            </div>
                            <div class="item">
                                <p>O3</p>
                                <h2>_____</h2>
                            </div>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-head">
                            <p >Sunrise & Sunset</p>
                        </div>
                        <div class="sunrise-sunset">
                            <div class="item">
                                <div class="icon">
                                   <i class="fas fa-sun fa-4x"></i>
                                </div>
                                <div>
                                    <p>Sunrise</p>
                                    <h2>______</h2>
                                </div>
                            </div>
                            <div class="item">
                                <div class="icon">
                                    <i class="fas fa-sun fa-4x"></i>
                                </div>
                                <div>
                                    <p>Sunset</p>
                                    <h2>______</h2>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-head">
                            <p style="font-size:1.5rem;color:white; font-weight:bold;">Humidity</p>
                        </div>
                        <div class="card-item">
                            <i class="fa-solid fa-droplet" style="font-size: 2rem;"></i>
                            <h2 id="HumidityVal">____%</h2>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-head">
                            <p style="font-size:1.5rem;color:white; font-weight:bold;">pressure</p>
                        </div>
                        <div class="card-item">
                            <i class="fa-regular fa-compass" style="font-size: 2rem;"></i>
                            <h2 id="pressureVal">____hPa</h2>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-head">
                            <p style="font-size:1.5rem;color:white; font-weight:bold;">Visibility</p>
                        </div>
                        <div class="card-item">
                            <i class="fa-regular fa-eye" style="font-size: 2rem;"></i>
                            <h2 id="visibilityVal">____Km</h2>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-head">
                            <p style="font-size:1.5rem;color:white; font-weight:bold;">Wind Speed</p>
                        </div>
                        <div class="card-item">
                            <i class="fa-solid fa-location-arrow" style="font-size: 2rem;"></i>
                            <h2 id="WindSpeedVal">____m/s</h2>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-head">
                            <p style="font-size:1.5rem;color:white; font-weight:bold;">Feels Like</p>
                        </div>
                        <div class="card-item">
                            <i class="fa-solid fa-temperature-three-quarters" style="font-size: 2rem;"></i>
                            <h3 id="FeelsVal">____&deg; C</h3>
                        </div>
                    </div>
                </div>
                <h2 style="margin-left: 10px;">Today At</h2>
                <div class="hourly-forecast">
                    <div class="card">
                        <p>9 AM</p>
                        <img src="https://openweathermap.org/img/wn/04d.png" alt="">
                        <p>___&deg;C</p>
                    </div>
                    <div class="card">
                        <p>9 AM</p>
                        <img src="https://openweathermap.org/img/wn/04d.png" alt="">
                        <p>___&deg;C</p>
                    </div>
                    <div class="card">
                        <p>9 AM</p>
                        <img src="https://openweathermap.org/img/wn/04d.png" alt="">
                        <p>___&deg;C</p>
                    </div>
                    <div class="card">
                        <p>9 AM</p>
                        <img src="https://openweathermap.org/img/wn/04d.png" alt="">
                        <p>___&deg;C</p>
                    </div>
                    <div class="card">
                        <p>9 AM</p>
                        <img src="https://openweathermap.org/img/wn/04d.png" alt="">
                        <p>___&deg;C</p>
                    </div>
                    <div class="card">
                        <p>9 AM</p>
                        <img src="https://openweathermap.org/img/wn/04d.png" alt="">
                        <p>___&deg;C</p>
                    </div>
                    <div class="card">
                        <p>9 AM</p>
                        <img src="https://openweathermap.org/img/wn/04d.png" alt="">
                        <p>___&deg;C</p>
                    </div>
                    <div class="card">
                        <p>9 AM</p>
                        <img src="https://openweathermap.org/img/wn/04d.png" alt="">
                        <p>___&deg;C</p>
                    </div>
                </div>
            </div>
    </div>

    
    <footer>
        <div class="footerContainer">
          <div class="socialIcons">
            <a href="https://www.facebook.com/TheWeatherChannel/"><img src="https://cdn3.iconfinder.com/data/icons/social-media-black-white-2/512/BW_Facebook_glyph_svg-256.png" alt="Facebook"></a>
            <a href="https://www.instagram.com/weatherindia/?hl=en"><img src="https://cdn3.iconfinder.com/data/icons/remixicon-logos/24/instagram-fill-256.png" alt="Instagram"></a>
            <a href="https://x.com/indiametdept?lang=en"><img src="https://cdn3.iconfinder.com/data/icons/social-media-black-white-2/512/BW_Twitter_glyph_svg-256.png" alt="Twitter"></a>
            <a href="https://openweathermap.org/"><img src="https://cdn3.iconfinder.com/data/icons/font-awesome-brands/512/google-plus-256.png" alt="Google Plus"></a>
            <a href="https://www.youtube.com/@TheWeatherChannel"><img src="https://cdn4.iconfinder.com/data/icons/ionicons/512/icon-social-youtube-256.png" alt="YouTube"></a>
          </div>
          
          <div class="footerNav">
            <ul>
              <li><a href="">Home</a></li>
              <li><a href="https://support.google.com/websearch/answer/13687874?hl=en">Help</a></li>
              <li><a href="https://www.weather.gov/cae/weatherterms.html#:~:text=Saturation%3A%20The%20condition%20in%20which,strong%20winds%20and%20large%20hail.">Term & Condition</a></li>
            </ul>
          </div>
        </div>
        <div class="footerBottom">
          <p>Copyright &copy;2024; Designed by <span class="designer">Faheem</span></p>
      </div>
      </footer>
    <script src="https://momentjs.com/downloads/moment.min.js"></script>
    <script src="script.js"></script>
</body>

</html>

style.css
```css
:root{
    --bg-color1:#95b8db;
    --bg-color2:#486ebb;
    --aqi-1:#d4e157;
    --aqi-2:#ffee58;
    --aqi-3:#ffca28;
    --aqi-4:#ff7043;
    --aqi-5:#ef5350;
}
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
body{
    min-height: 100vh;
    background-image: url('https://images.alphacoders.com/744/thumb-1920-744574.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    color: #fff;
    font-family: sans-serif;
}
hr{
    margin-bottom: 10px;
}

/***************************Navbar****************************/
input::placeholder {
    color: #999999;
}
.header{
    position: sticky;
    top: 0;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
    padding: 15px 0;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
    backdrop-filter: blur(10px);
    & .mylogo{
        display: flex;
        flex-direction: row;
        border-radius: 20px;
        & .mylogotext{
            padding-top: 10px;
        }
    }
    
    & #city_input{
        background-color: var(--bg-color2);
        border: none;
        padding: 12px;
        font-size: 16px;
        border-radius: 25px;
        color: #fff;
        &:focus{
            outline: none;
        }
    }
    & #searchBtn{
        background-color: var(--bg-color2);
        border: none;
        padding: 12px;
        font-size: 16px;
        border-radius: 25px;
        background-color: #fff;
        cursor: pointer;
    }
    & #locationBtn{
        background-color: var(--bg-color2);
        border: none;
        padding: 12px;
        font-size: 16px;
        border-radius: 25px;
        background-color:#ea6a4b;
        cursor: pointer;
    }
}

.city-name {
    text-align: left;
    margin-bottom: 20px;
}

.city-name h2 {
    font-size: 50px;
    font-weight: 600;
    color: #fff;
    margin-left: 10px;
}
#city_input::placeholder {
    color: black;
    text-align: center;
}
/******************************   CARD      *******************************************/
.card{
    border: 2px solid white;
    backdrop-filter: blur(10px); 
    padding: 15px;
    padding: 15px;
    border-radius: 15px;
    margin-bottom: 15px;
    margin-left: 10px;
    margin-right: 10px;
    & p{
        font-size: 14px;
        color: #0d0c0c;
    }
    & h1{
        font-size: 32px;
        font-weight: 500;
    }
}
.weather-data{
    
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 12px; 
    & .weather-left{
        grid-column: span 1; 
    
        & .current-weather{
            display: flex;
            justify-content: space-between;
            align-items: center;
            & h1{
                margin: 7px 0;
            }
            & p{
                color: black;
                font-size: 1.3rem;
            }
        }
        & .card-footer p{
            font-size: 14px;
            margin-bottom: 12px;
        }
        & .forecast-item{
            display: grid;
            grid-template-columns: repeat(3,1fr);
            place-items: center;
            margin-bottom: 15px;
            & .icon-wrapper{
                display: flex;
                align-items: center;
            }
        }
    }
    & .weather-right{
       
       grid-column: span 3;
        & h1{
           margin-bottom: 10px;
        }
        & .highlights{
            display: grid;
            grid-template-columns: repeat(4,1fr);
            column-gap: 15px;
            & .card:nth-of-type(1),
            & .card:nth-of-type(2){
                grid-column: span 2;
            }
            & .card-head{
                display: flex;
                justify-content: space-between;
                margin-bottom: 10px;
                p{
                    font-size: 1.2rem;
                    font-weight: bold;
                }
                & .air-index{
                    color: #000;
                    padding: 5px 10px;
                    border-radius: 15px;
                    &.aqi-1{
                        background-color: var(--aqi-1);
                    }
                    &.aqi-2{
                        background-color: var(--aqi-2);
                    }
                    &.aqi-3{
                        background-color: var(--aqi-3);
                    }
                    &.aqi-4{
                        background-color: var(--aqi-4);
                    }
                    &.aqi-5{
                        background-color: var(--aqi-5);
                    }
                    
                }
            }
            & .air-indices{
                display: grid;
                grid-template-columns: repeat(4, 1fr);
                place-items: center;
                & p{
                    text-align: center;
                }
            }
            & .sunrise-sunset{
                display: grid;
                grid-template-columns: repeat(2, 1fr);
                & .item{
                    display: flex;
                    align-items: center;
                    gap: 10px;
                    & h2{
                        margin-top: 15px;
                    }
                }
            }
            & .card-item{
                display: flex;
                justify-content: space-between;
            }
        }
        & .hourly-forecast{
            display: grid;
            grid-template-columns: repeat(8, 1fr);
            column-gap: 10px;
            & .card{
                text-align: center;
            }
        }
    }
}

.score-bar {
    width: 100%;
    background-color: #e0e0e0;
    border-radius: 10px;
    overflow: hidden;
    height: 10px;
    margin: 10px 0;
}

.score-bar-fill {
    height: 100%;
    background-color: #d7190b;
    transition: width 0.3s ease-in-out;
    border-radius: 10px;
}

/******************Media query *******************************/


@media (max-width: 1280px) {
  
    .weather-data {
        grid-template-columns: repeat(3, 1fr);
        & .weather-right{
            grid-column: span 2;
            & .highlights{
                grid-template-columns: repeat(3, 1fr);
                & .card:nth-of-type(1){
                    grid-column: span 3;
                }
            }
            & .hourly-forecast{
                grid-template-columns: repeat(6, 1fr);
            }
        }
    }
}

@media(max-width:1040px){
   
    .weather-data{
        grid-template-columns: repeat(2, 1fr);
        & .weather-right{
            grid-column: span 1;
            & .highlights{
                grid-template-columns: repeat(2,1fr);
                & .card:nth-of-type(1){
                    grid-column: span 2;
                }
            }
            & .hourly-forecast{
                grid-template-columns: repeat(4,1fr);
            }
        }
    }
}

@media(max-width:1040px){
    .weather-data .weather-right .highlights{
        & .card{
            grid-column: span 2;
        }
        & .air-index{
            grid-template-columns: repeat(3, 1fr);
        }
    }
}

@media(max-width:850px){
   
    #locationBtn{
        margin-top: 5px;
       
    }

    .weather-data{
        grid-template-columns: 1fr;
        & .weather-right .highlights{
            & .card:nth-of-type(3),
            & .card:nth-of-type(4),
            & .card:nth-of-type(5),
            & .card:nth-of-type(6),
            & .card:nth-of-type(7){
                grid-column: span 1;
            }
            & .air-indices{
                grid-template-columns: repeat(5, 1fr);
            }
        }
    }
}

@media(max-width:660px){
    
    .header{
        flex-direction: column;
        & h1{
            margin-bottom: 8px;
        }
        & #city_input, #searchBtn, #locationBtn{
            width: 100%;
            margin-bottom: 10px;
        }
    }
}

@media(max-width:580px){
   
    .weather-data .weather-right .highlights .air-indices{
        grid-template-columns: repeat(4,1fr);
    }
}

@media(max-width:520px){
  
    .weather-data .weather-right .highlights {
        & .card:nth-of-type(3),
        & .card:nth-of-type(4),
        & .card:nth-of-type(5),
        & .card:nth-of-type(6),
        & .card:nth-of-type(7){
            grid-column: span 2;
        }
        & .air-indices{
            grid-template-columns: repeat(3, 1fr);
        }  
    }
}

@media(max-width:480px){
    
    .weather-data .weather-right .highlights .sunrise-sunset {
        grid-template-columns: 1fr;
    }
}

@media(max-width:450px){
   
    .weather-data .weather-right .hourly-forecast {
        grid-template-columns: repeat(3, 1fr);
    }
}

@media(max-width:380px){
    
    .weather-data .weather-right .highlights .air-indices {
        grid-template-columns: repeat(2, 1fr);
    }
}


/* Footer  */
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }
  footer {
      background-color: hwb(245 4% 91% / 0.502); /* Adjust the rgba value to control the transparency */
    color: #fff;  /* Adjust the rgba value to control the transparency */
    
  }
  .footerContainer {
    width: 100%;
    height: 2%;
  }
  .socialIcons {
    display: flex;
    justify-content: center;
  }
  .socialIcons a {
  text-decoration: none;
  padding: 10px;
  background-color: white;
  margin: 10px;
  border-radius: 50%;
  display: inline-block;
  }
  
  .socialIcons a img {
  width: 30px; /* Adjust the size of your icons */
  height: 30px;
  display: block;
  }
  
  .socialIcons a:hover {
  background-color: #efe8e8;
  transition: 0.5s;
  }
  
  .socialIcons a img:hover {
  filter: invert(100%); /* This will invert the colors on hover, you can adjust as needed */
  transition: 0.5s;
  }
  
  .footerNav {
    margin: 30px 0;
  }
  .footerNav ul {
    display: flex;
    justify-content: center;
    list-style-type: none;
  }
  .footerNav ul li a {
    color: white;
    margin: 20px;
    text-decoration: none;
    font-size: 1.5em;
    opacity: 0.7;
    transition: 0.5s;
  }
  .footerNav ul li a:hover {
    opacity: 1;
  }
  .footerBottom {
    background-color: #010317;
    padding: 20px;
    text-align: center;
  }
  .footerBottom p{
    color: white;
    font-size: 1em;
  }
  .designer{
    opacity: 0.7;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: 400px;
    margin: 0px 5px;
  }
  @media (max-width: 700px) {
      .footerNav ul{
        flex-direction: column;
      }
      .footerNav ul li{
        width: 100%;
        text-align: center;
        margin: 10px;
      }
  }

  script.js
  ```js
  let cityInput = document.getElementById('city_input'),
    searchBtn = document.getElementById('searchBtn'),
    locationBtn = document.getElementById('locationBtn'),
    api_key = '3406e46404466438320be318dc0777d6',
    currentWeatherCard = document.querySelectorAll('.weather-left .card')[0],
    fiveDaysForecastCard = document.querySelector('.day-forecast'),
    aqiCard = document.querySelectorAll('.highlights .card')[0],
    sunriseCard = document.querySelectorAll('.highlights .card')[1],
    humidityVal = document.getElementById('HumidityVal'),
    pressureVal = document.getElementById('pressureVal'),
    visibilityVal = document.getElementById('visibilityVal'),
    WindSpeedVal = document.getElementById('WindSpeedVal'),
    FeelsVal = document.getElementById('FeelsVal'),
    hourlyForecastCard = document.querySelector('.hourly-forecast'),
    aqiList = ['Good', 'Fair', 'Moderate', 'Poor', 'Very Poor'];

// Define weather backgrounds
const weatherBackgrounds = {
    'fog': 'url(https://img1.picmix.com/output/pic/normal/9/4/2/8/5488249_c770d.gif)',
    'drizzle': 'url(https://www.icegif.com/wp-content/uploads/2021/11/icegif-695.gif)',
    'light rain': 'url(https://i.pinimg.com/originals/38/e3/11/38e3115f1d06ba0b443a75ff0c7cf2ee.gif)',
    'clear sky': 'url(https://img95.lovepik.com/photo/40106/1742.gif_wh860.gif)',
    'few clouds': 'url(https://i.makeagif.com/media/3-29-2016/_3nGic.gif)',
    'scattered clouds': 'url(https://i.makeagif.com/media/3-29-2016/_3nGic.gif)',
    'broken clouds': 'url(https://i.makeagif.com/media/3-29-2016/_3nGic.gif)',
    'shower rain': 'url(https://i.pinimg.com/originals/0d/65/87/0d65871fbae4469f4bd521e3497e04a6.gif)',
    'moderate rain': 'url(https://media0.giphy.com/media/JjrDsvilNKgw0/giphy.gif)',
    'rain': 'url(https://i.pinimg.com/originals/3a/b3/e3/3ab3e3bb80df0bfb1c9c312bac9b46e8.gif)',
    'thunderstorm': 'url(https://cdn.pixabay.com/animation/2024/04/03/23/48/23-48-16-122_512.gif)',
    'snow': 'url(https://i.pinimg.com/originals/d5/39/9d/d5399da17d9792aa3a066720b547a3f8.gif)',
    'mist': 'url(https://i.pinimg.com/originals/c1/41/3a/c1413a777f05d5639012dc8c947ad366.gif)',
    'overcast clouds': 'url(https://www.adventurebikerider.com/wp-content/uploads/2017/10/tumblr_o27c7fByaO1tchrkco1_500.gif)',
    'haze': 'url(https://64.media.tumblr.com/fd163b68f798321847925cfbf3793168/65ff7c05f97690ea-b4/s400x600/9ceddaa26f8c1c7166a6ea354613a31b0261e28e.gif)',
    // Default background
    'default': 'url(https://i.pinimg.com/originals/85/db/41/85db411e5bebff00b8a21f6d29d8c394.gif)'
};

// Function to update the page background based on weather description
function updateBackground(description) {
    let background = weatherBackgrounds[description] || weatherBackgrounds['default'];
    document.body.style.backgroundImage = background;
    document.body.style.backgroundSize = 'cover'; // Optional: Ensures the background covers the entire page
}



function getWeatherDetails(name, lat, lon, country, state) {
    let FORECAST_API_URL = `https://api.openweathermap.org/data/2.5/forecast?lat=${lat}&lon=${lon}&appid=${api_key}`,
        WEATHER_API_URL = `https://api.openweathermap.org/data/2.5/weather?lat=${lat}&lon=${lon}&appid=${api_key}`,
        AIR_POLLUTION_API_URL = `https://api.openweathermap.org/data/2.5/air_pollution?lat=${lat}&lon=${lon}&appid=${api_key}`,
        days = [
            'Sunday',
            'Monday',
            'Tuesday',
            'Wednesday',
            'Thursday',
            'Friday',
            'Saturday'
        ],
        months = [
            'Jan',
            'Feb',
            'Mar',
            'Apr',
            'May',
            'Jun',
            'Jul',
            'Aug',
            'Sep',
            'Oct',
            'Nov',
            'Dec'
        ];

    fetch(AIR_POLLUTION_API_URL).then(res => res.json()).then(data => {
        let { co, no, no2, o3, so2, pm2_5, pm10, nh3 } = data.list[0].components;
        aqiCard.innerHTML = `
                <div class="card-head">
                    <p style="color:white;">Air Quality Index</p>
                    <p class="air-index aqi-${data.list[0].main.aqi}">${aqiList[data.list[0].main.aqi - 1]}</p>
                </div>
                <div class="air-quality-bar">
                    <div class="score-bar">
                        <div class="score-bar-fill" id="aqiScore" style="width: 0;"></div>
                    </div>
                </div>
                <div class="air-indices">
                    <i class="fa-solid fa-wind fa-3x"></i>
                    <div class="item">
                        <p style="font-size:1.2rem;color:white;">PM2.5</p>
                        <h2>${pm2_5}</h2>
                    </div>
                    <div class="item">
                        <p style="font-size:1.2rem;color:white;">PM10</p>
                        <h2>${pm10}</h2>
                    </div>
                    <div class="item">
                        <p style="font-size:1.2rem;color:white;">SO2</p>
                        <h2>${so2}</h2>
                    </div>
                    <div class="item">
                        <p style="font-size:1.2rem;color:white;">CO</p>
                        <h2>${co}</h2>
                    </div>
                    <div class="item">
                        <p style="font-size:1.2rem;color:white;">NO</p>
                        <h2>${no}</h2>
                    </div>
                    <div class="item">
                        <p style="font-size:1.2rem;color:white;">NO2</p>
                        <h2>${no2}</h2>
                    </div>
                    <div class="item">
                        <p style="font-size:1.2rem;color:white;">NH3</p>
                        <h2>${nh3}</h2>
                    </div>
                    <div class="item">
                        <p style="font-size:1.2rem;color:white;">O3</p>
                        <h2>${o3}</h2>
                    </div>
                </div>
            `;

        // Update the AQI score bar based on the AQI value
        const aqiValue = data.list[0].main.aqi * 20; // Assuming the AQI value ranges from 1 to 5
        const aqiScore = document.getElementById('aqiScore');

        // Update the width of the score bar based on AQI value
        aqiScore.style.width = `${aqiValue}%`;

        // Optionally, change the color based on AQI range
        if (aqiValue <= 50) {
            aqiScore.style.backgroundColor = '#44f205'; // Good
        } else if (aqiValue <= 100) {
            aqiScore.style.backgroundColor = '#f4e04d'; // Moderate
        } else if (aqiValue <= 150) {
            aqiScore.style.backgroundColor = '#f2cf05'; // Unhealthy for Sensitive Groups
        } else if (aqiValue <= 200) {
            aqiScore.style.backgroundColor = '#f28b05'; // Unhealthy
        } else if (aqiValue <= 300) {
            aqiScore.style.backgroundColor = '#f26805'; // Very Unhealthy
        } else {
            aqiScore.style.backgroundColor = '#f20505'; // Hazardous
        }
    }).catch(() => {
        alert('Failed to fetch Air Quality Index');
    });


    fetch(WEATHER_API_URL).then(res => res.json()).then(data => {
        let date = new Date();
        currentWeatherCard.innerHTML = `
            <div class="current-weather">
                    <div class="details">
                        <p style="font-size:1rem;color:white; font-weight:bold;">Now</p>
                        <h1 style="font-size:2rem;color:white;font-weight:bold">${(data.main.temp - 273.15).toFixed(2)}&deg;C</h1>
                        <p style="font-size:1.2rem;color:white;">${data.weather[0].description}</p>
                    </div>
                    <div class="weather-icon">
                        <img style="width:120px" src="https://openweathermap.org/img/wn/${data.weather[0].icon}.png" alt="">
                    </div>
                </div>
                <hr>
                <div class="card-footer">
                    <p style="font-size:1rem;color:white; font-weight:bold;"><i class="fa fa-calendar"></i> ${days[date.getDay()]}, ${date.getDate()} ${months[date.getMonth()]}, ${date.getFullYear()}</p>
                    <p style="font-size:1rem;color:white; font-weight:bold;"><i class="fa fa-map-marker-alt" style="padding-right: 10px; "></i><a href="https://www.google.com/maps/search/?api=1&query=${lat},${lon}" target="_blank" style="color:white;">${name}, ${country}</a></p>
                </div>
        `;
    
        // Update background based on weather description
        updateBackground(data.weather[0].description);
        
        let { sunrise, sunset } = data.sys,
            { timezone, visibility } = data,
            { humidity, pressure, feels_like } = data.main,
            { speed } = data.wind,
            sRiseTime = moment.utc(sunrise * 1000).utcOffset(timezone / 60).format('hh:mm A'),
            sSetTime = moment.utc(sunset * 1000).utcOffset(timezone / 60).format('hh:mm A');
        sunriseCard.innerHTML = `
            <div class="card-head">
                <p style="color:white;">Sunrise & Sunset</p>
            </div>
            <div class="sunrise-sunset">
                <div class="item">
                    <div class="icon">
                        <i class="fas fa-sun fa-4x"></i>
                    </div>
                    <div>
                        <p style="font-size:1.2rem; color:white;">Sunrise</p>
                        <h2>${sRiseTime}</h2>
                    </div>
                </div>
                <div class="item">
                    <div class="icon">
                        <i class="fas fa-sun fa-4x"></i>
                    </div>
                    <div>
                        <p style="font-size:1.2rem; color:white;">Sunset</p>
                        <h2>${sSetTime}</h2>
                    </div>
                </div>
            </div>
        `;
        humidityVal.innerHTML = `${humidity}%`;
        pressureVal.innerHTML = `${pressure}hPa`;
        visibilityVal.innerHTML = `${visibility / 1000}km`;
        WindSpeedVal.innerHTML = `${speed}m/s`;
        FeelsVal.innerHTML = `${(feels_like - 273.15).toFixed(2)}&deg;C`;
    }).catch(error => {
        console.error('Error fetching weather data:', error);
    });

    fetch(FORECAST_API_URL).then(res => res.json()).then(data => {
        let hourlyForecast = data.list;
        hourlyForecastCard.innerHTML = '';
        for (i = 0; i <= 7; i++) {
            let hrForecastDate = new Date(hourlyForecast[i].dt_txt);
            let hr = hrForecastDate.getHours();
            let a = 'PM';
            if (hr < 12) a = 'AM';
            if (hr == 0) hr = 12;
            if (hr > 12) hr = hr - 12;
            hourlyForecastCard.innerHTML += `
                <div class="card">
                    <p style="color:white;">${hr} ${a}</p>
                    <img style="width:70%;" src="https://openweathermap.org/img/wn/${hourlyForecast[i].weather[0].icon}.png" alt="">
                    <p style="color:white;">${(hourlyForecast[i].main.temp - 273.15).toFixed(2)}&deg;C</p>
                </div>
            `;
        }
        let uniqueForecastDay = [];
        let fiveDaysForecast = data.list.filter(forecast => {
            let forecastDate = new Date(forecast.dt_txt).getDate();
            if (!uniqueForecastDay.includes(forecastDate)) {
                return uniqueForecastDay.push(forecastDate);
            }
        });

        fiveDaysForecastCard.innerHTML = '';

        for (let i = 0; i < fiveDaysForecast.length; i++) {
            let date = new Date(fiveDaysForecast[i].dt_txt);

            // Variables to store the closest day and night temperatures
            let dayTemp = null;
            let nightTemp = null;
            let closestDayDiff = Infinity;
            let closestNightDiff = Infinity;

            data.list.forEach(item => {
                let itemDate = new Date(item.dt_txt).getDate();
                if (itemDate === date.getDate()) {
                    let itemTime = new Date(item.dt_txt).getHours();
                    let timeDiff = Math.abs(itemTime - 12); // Difference from noon for daytime
                    if (timeDiff < closestDayDiff) {
                        closestDayDiff = timeDiff;
                        dayTemp = item.main.temp;
                    }
                    timeDiff = Math.abs(itemTime - 0); // Difference from midnight for nighttime
                    if (timeDiff < closestNightDiff) {
                        closestNightDiff = timeDiff;
                        nightTemp = item.main.temp;
                    }
                }
            });

            // Convert Kelvin to Celsius
            dayTemp = Math.round((dayTemp - 273.15).toFixed(2));
            nightTemp = Math.round((nightTemp - 273.15).toFixed(2));

            fiveDaysForecastCard.innerHTML += `
        <div class="forecast-item">
            <div class="icon-wrapper">
                <img src="https://openweathermap.org/img/wn/${fiveDaysForecast[i].weather[0].icon}.png" alt="cloud img">
                <span>Day: ${dayTemp}&deg;C</span>
                <span>Night: ${nightTemp}&deg;C</span>
            </div>
            <p  style="font-size:1.2rem;color:white;">${date.getDate()} ${months[date.getMonth()]}</p>
            <p  style="font-size:1.2rem;color:white;">${days[date.getDay()]}</p>
        </div>
    `;
        }
    }).catch(() => {
        alert('Failed to fetch weather forecast');
    })
}
// Update the displayed city name when the search button is clicked
searchBtn.addEventListener('click', function () {
    const cityName = cityInput.value.trim();
    if (cityName) {
        document.getElementById('cityNameDisplay').textContent = cityName; // Update with input value
        getCityCoordinates(); // Fetch coordinates and update weather data
    } else {
        alert('Please enter a city name.');
    }
});

// Update the displayed city name when the location button is clicked
locationBtn.addEventListener('click', function () {
    // Fetch and update city name display based on current location
    getUserCoordinates(); // Fetch current location and update weather data
});

function getCityCoordinates() {
    let cityName = cityInput.value.trim();
    cityInput.value = ''; // Clear input field
    if (!cityName) return;
    let GEOCODING_API_URL = `https://api.openweathermap.org/geo/1.0/direct?q=${cityName}&limit=1&appid=${api_key}`;
    fetch(GEOCODING_API_URL).then(res => res.json()).then(data => {
        if (data && data.length > 0) {
            let { name, lat, lon, country, state } = data[0];
            document.getElementById('cityNameDisplay').textContent = name; // Update with correct city name from API
            getWeatherDetails(name, lat, lon, country, state); // Fetch and display weather details
        } else {
            alert(`No results found for ${cityName}`);
        }
    }).catch(() => {
        alert(`Failed to fetch coordinates of ${cityName}`);
    });
}

function getUserCoordinates() {
    navigator.geolocation.getCurrentPosition(position => {
        let { latitude, longitude } = position.coords;
        let REVERSE_GEOCODING_URL = `https://api.openweathermap.org/geo/1.0/reverse?lat=${latitude}&lon=${longitude}&limit=1&appid=${api_key}`;

        fetch(REVERSE_GEOCODING_URL).then(res => res.json()).then(data => {
            let { name, country, state } = data[0];
            document.getElementById('cityNameDisplay').textContent = name; // Update with the city name from location
            getWeatherDetails(name, latitude, longitude, country, state); // Fetch and display weather details
        }).catch(() => {
            alert('Failed to fetch user coordinates');
        });
    }, error => {
        if (error.code === error.PERMISSION_DENIED) {
            alert('Geolocation permission denied. Please reset location permission to grant access again.');
        }
    });
}

searchBtn.addEventListener('click', getCityCoordinates);
locationBtn.addEventListener('click', getUserCoordinates);
cityInput.addEventListener('keyup', e => e.key === 'Enter' && getCityCoordinates());
window.addEventListener('load', getUserCoordinates);

