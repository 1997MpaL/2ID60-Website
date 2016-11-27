# Uitprobeersel

var url = "http://api.openweathermap.org/data/2.5/weather";
var APIKEY = "84e66356e47e2053e60763a13e0b2d0b";

function showWeather(city) {
  var query = url + "?q=" + city + "&appid=" + APIKEY;
  $.getJSON(query, function(data) {
    $("#weather").append("Weather in " + city + ": " + data.weather[0].description);
  });
}

$(function() {
  showWeather("London");
  });
