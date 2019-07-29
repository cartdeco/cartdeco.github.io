<!DOCTYPE html>
<html>
<head>
    <meta charset='utf-8' />
    <title>Scotch whisky distilleries</title>
    <meta name='viewport' content='initial-scale=1,maximum-scale=1,user-scalable=no' />
    <script src='https://api.tiles.mapbox.com/mapbox-gl-js/v0.20.1/mapbox-gl.js'></script>
    <link href='https://api.tiles.mapbox.com/mapbox-gl-js/v0.20.1/mapbox-gl.css' rel='stylesheet' />
    <style>
        body { margin:0; padding:0; }
        #map { position:absolute; top:0; bottom:0; width:100%; height:800px;}
    </style>
</head>
<body>
    
<style>
    #campbeltown {
        display: block;
        position: absolute;
        right: 20px;
        top: 20px;
        margin: 0px auto;
        width: 135px;
        height: 40px;
        padding: 10px;
        border: none;
        border-radius: 3px;
        font-size: 13px;
        font-weight: bold;
        text-align: center;
        color: #333;
        background: #adc8bf;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    }
</style>
    
<style>
    #highland {
        display: block;
        position: absolute;
        right: 20px;
        top: 70px;
        margin: 0px auto;
        width: 135px;
        height: 40px;
        padding: 10px;
        border: none;
        border-radius: 3px;
        font-size: 13px;
        font-weight: bold;
        text-align: center;
        color: #333;
        background: #ffdcaa;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    }
</style>
    
<style>
    #islands {
        display: block;
        position: absolute;
        right: 20px;
        top: 120px;
        margin: 0px auto;
        width: 135px;
        height: 40px;
        padding: 10px;
        border: none;
        border-radius: 3px;
        font-size: 13px;
        font-weight: bold;
        text-align: center;
        color: #333;
        background: #e0ddb8;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    }
</style>

<style>
    #islay {
        display: block;
        position: absolute;
        right: 20px;
        top: 170px;
        margin: 0px auto;
        width: 135px;
        height: 40px;
        padding: 10px;
        border: none;
        border-radius: 3px;
        font-size: 13px;
        font-weight: bold;
        text-align: center;
        color: #333;
        background: #c4c5ff;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    }
</style>
    
<style>
    #lowland {
        display: block;
        position: absolute;
        right: 20px;
        top: 220px;
        margin: 0px auto;
        width: 135px;
        height: 40px;
        padding: 10px;
        border: none;
        border-radius: 3px;
        font-size: 13px;
        font-weight: bold;
        text-align: center;
        color: #333;
        background: #b0c6d6;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    }
</style>

<style>
    #speyside {
        display: block;
        position: absolute;
        right: 20px;
        top: 270px;
        margin: 0px auto;
        width: 135px;
        height: 40px;
        padding: 10px;
        border: none;
        border-radius: 3px;
        font-size: 13px;
        font-weight: bold;
        text-align: center;
        color: #333;
        background: #e0bbab;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    }
</style>
    
<style>
    .mapboxgl-popup-tip {
        max-width: 400px;
        font: 14px/20px 'Helvetica Neue', Arial, Helvetica, sans-serif;
    }
</style>

<style>
    .mapboxgl-popup {
        min-width: 160px;
        max-width: 400px;
        font: 12px/20px 'Roboto', Arial, Helvetica, sans-serif;
        color: #ccc; 
        padding: 0px;
        display: flex;
        margin: 0px 0px 0px 5px;
        position: absolute;
        line-height: 5px;
    }
    
    .mapboxgl-popup-content {
        position: relative;
        background: #333;
        border-radius: 3px;
        box-shadow: 0 1px 2px rgba(0,0,0,0.10);
        padding: 0px 0px 0px 0px;
        pointer-events: auto;
    }
    
    .mapboxgl-popup-anchor-bottom .mapboxgl-popup-tip  {
        border-top-color: #333;
    }
    
    .mapboxgl-popup-anchor-left .mapboxgl-popup-tip {
        border-right-color: #333;
    }
    
    .mapboxgl-popup-anchor-right .mapboxgl-popup-tip {
        border-left-color: #333;
    }
    
    .mapboxgl-popup-anchor-top .mapboxgl-popup-tip {
        border-bottom-color: #333;
    }
    
    .mapboxgl-popup-anchor-bottom-left .mapboxgl-popup-tip {
        border-bottom-color: #333;
    }
    
    .mapboxgl-popup-anchor-bottom-right .mapboxgl-popup-tip {
        border-bottom-color: #333;
    }
    
    .mapboxgl-popup-anchor-top-left .mapboxgl-popup-tip {
        border-bottom-color: #333;
    }
    
    .mapboxgl-popup-anchor-top-right .mapboxgl-popup-tip {
        border-bottom-color: #333;
    }
    
    .popup-product-link {
        color:inherit;
    }
    
    .mapboxgl-popup-close-button {
        color: #fff;
    }
    
</style>
    
<div id='map'></div>
<br/>
<button id='speyside'>SPEYSIDE</button>
<button id='campbeltown'>CAMPBELTOWN</button>
<button id='highland'>HIGHLAND</button>
<button id='islands'>ISLANDS</button>
<button id='islay'>ISLAY</button>
<button id='lowland'>LOWLAND</button>

<script>
    
// Navigation tools
var nav = new mapboxgl.Navigation({
    position: 'top-left'
}); // position is optional


// Set bounds to Scotland
var bounds = [
    [-13.75, 52.5], // Southwest coordinates
    [5, 62]  // Northeast coordinates
];

    
mapboxgl.accessToken = 'pk.eyJ1IjoiY2FydGRlY28iLCJhIjoiMkRSMXQzUSJ9.74YN7Lx-RgcpjBPWjtGcog'; // Mapbox access token
var map = new mapboxgl.Map({
    container: 'map', // container id
    style: 'mapbox://styles/cartdeco/cipryv0u9002cekm7qxmxnela', //stylesheet location
    center: [-4.31, 56.82], // starting position
    zoom: 6.5, // starting zoom
    maxBounds: bounds // Sets bounds as max
});
    
map.addControl(nav); // navigation controls + -

map.addControl(new mapboxgl.Geolocate({position: 'top-left'})); // Geolocation tool
    
// Data - geojson
    
map.on('load', function () {
    map.addSource("distilleries", {
        "type": "geojson",
        "data": {
            "type": "FeatureCollection",
            "features": [
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -4.070327,
               56.18888
            ]
         },
         "properties": {
            "cartodb_id": 25,
            "name": "Deanston",
            "wikipedia": "https://en.wikipedia.org/wiki/Deanston_distillery",
            "homepage": "http://deanstonmalt.com/",
            "image": "https://static.whiskybase.com/storage/companies/159/17307-big.jpg",
            "founded": 1965,
            "status": "Active",
            "number_of_stills": 2,
            "capacity_litres": 3000000,
            "type": "Single Malt",
            "age": "12 years old",
            "cask_types": "",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Distell, South Africa"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.58271,
               56.853218
            ]
         },
         "properties": {
            "cartodb_id": 69,
            "name": "Fettercairn",
            "wikipedia": "https://en.wikipedia.org/wiki/Fettercairn_distillery",
            "homepage": "http://www.whyteandmackay.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/3/3d/Fettercairn_Distillery_-_geograph.org.uk_-_870131.jpg",
            "founded": 1824,
            "status": "Operational",
            "number_of_stills": "",
            "capacity_litres": 1600000,
            "type": "Single Malt",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "owner": "Alliance Global Group",
            "icon": "alcohol-shop"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.700547,
               56.70182
            ]
         },
         "properties": {
            "cartodb_id": 49,
            "name": "Edradour",
            "wikipedia": "https://en.wikipedia.org/wiki/Edradour_distillery",
            "homepage": "http://www.edradour.com/",
            "image": "http://www.edradour.com/~edr99/files/cache/ad7bdc9002b31f8b882a2c2c56d505be_f179.JPG",
            "founded": 1825,
            "status": "Active",
            "number_of_stills": "",
            "capacity_litres": 95000,
            "type": "Single Malt",
            "age": "10, 12 years old",
            "cask_types": "",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Signatory Vintage Scotch Whisky Co."
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -6.195731,
               55.63436
            ]
         },
         "properties": {
            "cartodb_id": 5,
            "name": "Port Ellen",
            "wikipedia": "https://en.wikipedia.org/wiki/Port_Ellen_distillery",
            "homepage": "",
            "image": "https://upload.wikimedia.org/wikipedia/commons/c/c3/Port_Ellen_Distillery-Canthusus.jpg",
            "founded": 1825,
            "status": "Partly demolished",
            "number_of_stills": 2,
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Islay",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -4.463925,
               54.857937
            ]
         },
         "properties": {
            "cartodb_id": 20,
            "name": "Bladnoch",
            "wikipedia": "https://en.wikipedia.org/wiki/Bladnoch_distillery",
            "homepage": "http://bladnoch.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/e/eb/Bladnoch_Distillery_-_geograph.org.uk_-_244136.jpg",
            "founded": 1825,
            "status": "Operational",
            "number_of_stills": 1,
            "capacity_litres": 250000,
            "type": "Single Malt",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Lowland",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "David Prior"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -4.239049,
               56.94001
            ]
         },
         "properties": {
            "cartodb_id": 38,
            "name": "Dalwhinnie",
            "wikipedia": "https://en.wikipedia.org/wiki/Dalwhinnie_distillery",
            "homepage": "https://www.discovering-distilleries.com/dalwhinnie/",
            "image": "https://lh3.googleusercontent.com/-TRGVgzj3S2s/AAAAAAAAAAI/AAAAAAAAABg/17p3lkkBJpo/s0-c-k-no-ns/photo.jpg",
            "founded": 1898,
            "status": "Active",
            "number_of_stills": "",
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "15 years old",
            "cask_types": "",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.414259,
               57.311806
            ]
         },
         "properties": {
            "cartodb_id": 55,
            "name": "Tomintoul",
            "wikipedia": "https://en.wikipedia.org/wiki/Tomintoul_distillery",
            "homepage": "http://www.tomintoulwhisky.com/",
            "image": "http://www.tomintoulwhisky.com/templates/ad_tomintoul/assets/images/distillerylandscape.jpg",
            "founded": 1964,
            "status": "Open",
            "number_of_stills": "",
            "capacity_litres": 3300000,
            "type": "Single Malt",
            "age": "10, 12, 14, 16, 21 and 33 years old",
            "cask_types": "",
            "abv": "40%",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "By appointment",
            "icon": "alcohol-shop",
            "owner": "Angus Dundee"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.394711,
               57.41018
            ]
         },
         "properties": {
            "cartodb_id": 54,
            "name": "Cragganmore",
            "wikipedia": "https://en.wikipedia.org/wiki/Cragganmore_distillery",
            "homepage": "https://www.discovering-distilleries.com/cragganmore/",
            "image": "https://www.whisky.com/fileadmin/_processed_/csm_Cragganmore_Distille_3fc25fec713f3d8bf8ba6ca6024ff1ef_371a0fa2ef.jpg",
            "founded": 1869,
            "status": "Active",
            "number_of_stills": 4,
            "capacity_litres": 1520000,
            "type": "Single Malt",
            "age": "12 years old",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.36986,
               57.62367
            ]
         },
         "properties": {
            "cartodb_id": 56,
            "name": "Miltonduff",
            "wikipedia": "",
            "homepage": "http://www.pernod.fr/",
            "image": "https://s0.geograph.org.uk/geophotos/05/26/42/5264238_e2863bc5.jpg",
            "founded": 1824,
            "status": "Active",
            "number_of_stills": 6,
            "capacity_litres": 5900000,
            "type": "Single Malt",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "owner": "Pernod Ricard"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.368179,
               57.405308
            ]
         },
         "properties": {
            "cartodb_id": 148,
            "name": "Ballindalloch",
            "wikipedia": "",
            "homepage": "http://www.ballindallochdistillery.com/",
            "image": "http://www.ballindallochdistillery.com/wp-content/uploads/2015/06/how-to-find-us.jpg",
            "founded": 2011,
            "status": "Operational",
            "number_of_stills": "",
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Ballindalloch Distillery LLP"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.353298,
               57.459114
            ]
         },
         "properties": {
            "cartodb_id": 59,
            "name": "Tamdhu",
            "wikipedia": "https://en.wikipedia.org/wiki/Tamdhu_distillery",
            "homepage": "http://www.tamdhu.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/0/0b/Tamdhu_Entrance_-_geograph.org.uk_-_1070533.jpg",
            "founded": 1897,
            "status": "Operational",
            "number_of_stills": 3,
            "capacity_litres": 4500000,
            "type": "Single Malt",
            "age": "10 years old",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Ian MacLeod Distillers"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.278217,
               57.59903
            ]
         },
         "properties": {
            "cartodb_id": 97,
            "name": "Glen Elgin",
            "wikipedia": "https://en.wikipedia.org/wiki/Glen_Elgin_distillery",
            "homepage": "https://www.malts.com",
            "image": "http://www.scotchwhisky.net/images/dist/glen_elg_b.jpg",
            "founded": 1898,
            "status": "Active",
            "number_of_stills": 3,
            "capacity_litres": 1830000,
            "type": "",
            "age": "12 years old",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -4.260271,
               57.691517
            ]
         },
         "properties": {
            "cartodb_id": 39,
            "name": "Teaninich",
            "wikipedia": "https://en.wikipedia.org/wiki/Teaninich_distillery",
            "homepage": "http://www.diageo.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/3/35/Teaninich_Distillery_-_geograph.org.uk_-_1140657.jpg",
            "founded": 1817,
            "status": "Open",
            "number_of_stills": 10,
            "capacity_litres": "",
            "type": "Blended",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -6.126938,
               55.882893
            ]
         },
         "properties": {
            "cartodb_id": 7,
            "name": "Bunnahabhain",
            "wikipedia": "https://en.wikipedia.org/wiki/Bunnahabhain_Distillery",
            "homepage": "http://bunnahabhain.com/",
            "image": "https://www.islayinfo.com/images/distilleries/bunnahabhaindistillery.jpg",
            "founded": 1881,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "12, 18, 25, 40 years old",
            "cask_types": "",
            "abv": "",
            "region": "Islay",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Distell, South Africa"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.868271,
               58.02409
            ]
         },
         "properties": {
            "cartodb_id": 45,
            "name": "Clynelish",
            "wikipedia": "https://en.wikipedia.org/wiki/Clynelish_distillery",
            "homepage": "https://www.discovering-distilleries.com/clynelish/",
            "image": "https://media-cdn.tripadvisor.com/media/photo-s/09/d7/33/76/clynelish-distillery.jpg",
            "founded": 1872,
            "status": "Operational",
            "number_of_stills": "",
            "capacity_litres": 3400000,
            "type": "Single Malt",
            "age": "14 years old",
            "cask_types": "",
            "abv": "46%",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -4.238802,
               57.68835
            ]
         },
         "properties": {
            "cartodb_id": 40,
            "name": "Dalmore",
            "wikipedia": "https://en.wikipedia.org/wiki/Dalmore_distillery",
            "homepage": "http://www.thedalmore.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/8/86/Scotland_Alness_Dalmore_Distillery.jpg",
            "founded": 1839,
            "status": "Operational",
            "number_of_stills": 4,
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "12, 15, 18 and 25 years old",
            "cask_types": "",
            "abv": "40-43%",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Alliance Global Group"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -4.474794,
               57.522057
            ]
         },
         "properties": {
            "cartodb_id": 35,
            "name": "Glen Ord",
            "wikipedia": "https://en.wikipedia.org/wiki/Glen_Ord_Distillery",
            "homepage": "https://www.discovering-distilleries.com/glenord/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/a/a0/GlenOrd1.jpg",
            "founded": 1838,
            "status": "Operational",
            "number_of_stills": 7,
            "capacity_litres": 11500000,
            "type": "Single Malt",
            "age": "12, 15, 18, 32 and 36 years",
            "cask_types": "American white oak, ex-bourbon casks, Oloroso sherry casks",
            "abv": "40-46%",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -5.950851,
               55.832886
            ]
         },
         "properties": {
            "cartodb_id": 12,
            "name": "Isle of Jura",
            "wikipedia": "https://en.wikipedia.org/wiki/Jura_distillery",
            "homepage": "http://www.jurawhisky.com/en/",
            "image": "https://www.undiscoveredscotland.co.uk/jura/distillery/images/dsitillery-450.jpg",
            "founded": 1810,
            "status": "Operational",
            "number_of_stills": "",
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Island",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Emperador Inc."
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -5.604873,
               55.42945
            ]
         },
         "properties": {
            "cartodb_id": 13,
            "name": "Glen Scotia",
            "wikipedia": "https://en.wikipedia.org/wiki/Glen_Scotia_distillery",
            "homepage": "http://www.glenscotia.com/",
            "image": "http://www.glenscotia.com/web/images/distillery/image02.jpg",
            "founded": 1832,
            "status": "Operational",
            "number_of_stills": 1,
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "15 years old",
            "cask_types": "",
            "abv": "",
            "region": "Campbelltown",
            "country": "Scotland",
            "open_to_public": "By appointment",
            "icon": "alcohol-shop",
            "owner": "Loch Lomond Group"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.642386,
               56.287407
            ]
         },
         "properties": {
            "cartodb_id": 24,
            "name": "Kingsbarns",
            "wikipedia": "",
            "homepage": "http://www.kingsbarnsdistillery.com/",
            "image": "http://www.whiskyintelligence.com/wp-content/uploads/2014/12/Kingsbarns-Distillery-EM-01.jpg",
            "founded": 2014,
            "status": "Operational",
            "number_of_stills": "",
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Lowlands",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": ""
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.963991,
               57.661446
            ]
         },
         "properties": {
            "cartodb_id": 111,
            "name": "Inchgower",
            "wikipedia": "https://en.wikipedia.org/wiki/Inchgower_distillery",
            "homepage": "http://www.diageo.com/",
            "image": "http://www.whisky-emporium.com/T-Note-img/ZZ-distillery-Inchgower-1.jpg",
            "founded": 1871,
            "status": "Active",
            "number_of_stills": 2,
            "capacity_litres": 1990000,
            "type": "Single Malt",
            "age": "12, 13, 14, 21 and 30 years old",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -6.126273,
               55.63546
            ]
         },
         "properties": {
            "cartodb_id": 8,
            "name": "Lagavulin",
            "wikipedia": "https://en.wikipedia.org/wiki/Lagavulin_distillery",
            "homepage": "https://www.discovering-distilleries.com/lagavulin/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/6/63/Lagavulin_-_entrance.JPG",
            "founded": 1816,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "12, 16, 21, 25, 30 and 37 years old",
            "cask_types": "Bourbon, Sherry",
            "abv": "",
            "region": "Islay",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.511556,
               57.65766
            ]
         },
         "properties": {
            "cartodb_id": 135,
            "name": "Macduff",
            "wikipedia": "https://en.wikipedia.org/wiki/Macduff_distillery",
            "homepage": "",
            "image": "http://www.scotchwhisky.net/images/dist/macduff_dist2_b.jpg",
            "founded": 1960,
            "status": "Active",
            "number_of_stills": 3,
            "capacity_litres": 2400000,
            "type": "Single Malt",
            "age": "10, 11, 17, 32 and 36 years old",
            "cask_types": "",
            "abv": "40%",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Bacardi"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -4.833062,
               55.26063
            ]
         },
         "properties": {
            "cartodb_id": 123,
            "name": "Ailsa Bay",
            "wikipedia": "https://en.wikipedia.org/wiki/Girvan_distillery",
            "homepage": "http://www.williamgrant.com/ailsabay_distillery.php",
            "image": "https://pbs.twimg.com/media/C3CfDAGW8AEgcUA.jpg",
            "founded": "2007",
            "status": "Operational",
            "number_of_stills": 16,
            "capacity_litres": "12000000",
            "type": "Single Malt",
            "age": "8 years old",
            "cask_types": "",
            "abv": "",
            "region": "Lowland",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "William Grant & Sons"
         }
      },
                {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -0.824698,
               60.797971
            ]
         },
         "properties": {
            "cartodb_id": 200,
            "name": "Shetland Reel",
            "wikipedia": "",
            "homepage": "https://www.shetlandreel.com/",
            "image": "https://www.shetlandreel.com/site/assets/files/1083/distillery-sal-3-w1200-h120.jpg",
            "founded": "2010",
            "status": "Operational",
            "number_of_stills": 1,
            "capacity_litres": "",
            "type": "Blended Malt",
            "age": "5 years old",
            "cask_types": "",
            "abv": "",
            "region": "Islands",
            "country": "Scotland",
            "open_to_public": "By appointment",
            "icon": "alcohol-shop",
            "owner": "Private"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.114334,
               57.548145
            ]
         },
         "properties": {
            "cartodb_id": 110,
            "name": "Auchriosk",
            "wikipedia": "https://en.wikipedia.org/wiki/Auchroisk_distillery",
            "homepage": "http://www.diageo.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/d/da/Auchroisk_Distillery_-_geograph.org.uk_-_1134178.jpg",
            "founded": 1972,
            "status": "Active",
            "number_of_stills": 4,
            "capacity_litres": 3100000,
            "type": "Blended",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.259249,
               57.272686
            ]
         },
         "properties": {
            "cartodb_id": 71,
            "name": "Braeval",
            "wikipedia": "https://en.wikipedia.org/wiki/Braeval_distillery",
            "homepage": "http://www.pernod.fr/",
            "image": "http://potstill.org/jpeto_cache/braeval_fbx.jpg",
            "founded": 1973,
            "status": "Active",
            "number_of_stills": 2,
            "capacity_litres": 4200000,
            "type": "Single Malt",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Pernod Ricard"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.123819,
               57.44413
            ]
         },
         "properties": {
            "cartodb_id": 79,
            "name": "Dufftown",
            "wikipedia": "https://en.wikipedia.org/wiki/Dufftown_distillery",
            "homepage": "http://www.diageo.com/",
            "image": "http://www.dufftown.co.uk/images_cms/i244_l.jpg",
            "founded": 1895,
            "status": "Operational",
            "number_of_stills": 6,
            "capacity_litres": 4000000,
            "type": "Blended",
            "age": "15 years old",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.274956,
               57.45325
            ]
         },
         "properties": {
            "cartodb_id": 81,
            "name": "Dailuaine",
            "wikipedia": "https://en.wikipedia.org/wiki/Dailuaine_distillery",
            "homepage": "http://www.diageo.com/",
            "image": "http://www.scotchwhisky.net/images/dist/DAL-SIGN.jpg",
            "founded": 1852,
            "status": "Active",
            "number_of_stills": "",
            "capacity_litres": 3370000,
            "type": "Single Malt",
            "age": "7, 8, 9, 10, 11, 12, 13, 15, 16, 17, 18, 32, 34 years old",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.348899,
               57.471012
            ]
         },
         "properties": {
            "cartodb_id": 91,
            "name": "Cardhu",
            "wikipedia": "https://en.wikipedia.org/wiki/Cardhu_distillery",
            "homepage": "https://www.discovering-distilleries.com/cardhu/",
            "image": "http://www.undiscoveredscotland.co.uk/knockando/cardhu/images/cardhu-450.jpg",
            "founded": 1824,
            "status": "Active",
            "number_of_stills": "",
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "12 years old",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.961084,
               57.540104
            ]
         },
         "properties": {
            "cartodb_id": 113,
            "name": "Strathmill",
            "wikipedia": "https://en.wikipedia.org/wiki/Strathmill",
            "homepage": "http://www.diageo.com/",
            "image": "http://www.scotchwhisky.net/images/dist/smill_dist_b.jpg",
            "founded": 1891,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 1800000,
            "type": "Blended",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.231338,
               57.45578
            ]
         },
         "properties": {
            "cartodb_id": 134,
            "name": "Glenallachie",
            "wikipedia": "https://en.wikipedia.org/wiki/Glenallachie_distillery",
            "homepage": "http://www.pernod.fr/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/9/96/Glenallachie_Distillery_-_geograph.org.uk_-_741359.jpg",
            "founded": 1967,
            "status": "Open",
            "number_of_stills": 2,
            "capacity_litres": 3200000,
            "type": "Single Malt and Blended",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Pernod Ricard"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.049039,
               57.534286
            ]
         },
         "properties": {
            "cartodb_id": 116,
            "name": "Glentauchers",
            "wikipedia": "https://en.wikipedia.org/wiki/Glentauchers_distillery",
            "homepage": "http://www.pernod.fr/",
            "image": "https://thewhiskyphiles.files.wordpress.com/2018/11/glentauchers-distillery.jpg?w=584&h=374",
            "founded": 1897,
            "status": "Active",
            "number_of_stills": 3,
            "capacity_litres": 4500000,
            "type": "Single Malt",
            "age": "15 years old",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Pernod Ricard"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -7.044951,
               58.170555
            ]
         },
         "properties": {
            "cartodb_id": 122,
            "name": "Abhainn Dearg",
            "wikipedia": "https://en.wikipedia.org/wiki/Abhainn_Dearg_distillery",
            "homepage": "http://www.abhainndearg.co.uk/",
            "image": "http://www.abhainndearg.co.uk/images/field_bottle.jpg",
            "founded": 2007,
            "status": "Operational",
            "number_of_stills": "",
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "3 years",
            "cask_types": "American White Oak, Ex Bourbon Casks (main) Ex Sherry Casks",
            "abv": "46%, 56%, 58%",
            "region": "Island",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Independent"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.122703,
               57.442566
            ]
         },
         "properties": {
            "cartodb_id": 80,
            "name": "Mortlach",
            "wikipedia": "https://en.wikipedia.org/wiki/Mortlach_distillery",
            "homepage": "http://www.mortlach.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/a/a3/Dufftown_distillery.jpg",
            "founded": 1823,
            "status": "Active",
            "number_of_stills": 3,
            "capacity_litres": 3700000,
            "type": "Single Malt",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.119549,
               57.449142
            ]
         },
         "properties": {
            "cartodb_id": 82,
            "name": "Glendullan",
            "wikipedia": "https://en.wikipedia.org/wiki/Glendullan_distillery",
            "homepage": "http://www.diageo.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/f/f7/Glendullan.jpg",
            "founded": 1897,
            "status": "Operational",
            "number_of_stills": "",
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "12 and 23 years old",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.185102,
               57.48824
            ]
         },
         "properties": {
            "cartodb_id": 106,
            "name": "Craigellachie",
            "wikipedia": "https://en.wikipedia.org/wiki/Craigellachie_distillery",
            "homepage": "http://www.craigellachie.com/splash",
            "image": "https://cdn.diffords.com/contrib/stock-images/2017/4/43/2017f4711b63e6519ac1bd8da1492b7c0dd1.jpg",
            "founded": 1891,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 4000000,
            "type": "Single Malt",
            "age": "13, 17, 19 and 23 years",
            "cask_types": "",
            "abv": "40%",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Bacardi"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.210969,
               57.530087
            ]
         },
         "properties": {
            "cartodb_id": 101,
            "name": "Glen Grant",
            "wikipedia": "https://en.wikipedia.org/wiki/Glen_Grant_distillery",
            "homepage": "http://www.glengrant.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/1/1e/GlenGrant2.jpg",
            "founded": 1840,
            "status": "Active",
            "number_of_stills": 4,
            "capacity_litres": 5900000,
            "type": "Single Malt",
            "age": "10, 12 and 18 years",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Gruppo Campari"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.216655,
               57.536583
            ]
         },
         "properties": {
            "cartodb_id": 105,
            "name": "Speyburn",
            "wikipedia": "https://en.wikipedia.org/wiki/Speyburn-Glenlivet_distillery",
            "homepage": "http://www.speyburn.com/",
            "image": "https://forwhiskeylovers.com/sites/default/files/styles/article/public/distilleries/speyburn_0.jpg?itok=KsL7kDpR",
            "founded": 1897,
            "status": "Active",
            "number_of_stills": "",
            "capacity_litres": 1000000,
            "type": "Single Malt",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "InterBev"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.1608,
               57.3963
            ]
         },
         "properties": {
            "cartodb_id": 75,
            "name": "Allt-a-Bhainne",
            "wikipedia": "https://en.wikipedia.org/wiki/Allt-A-Bhainne",
            "homepage": "http://www.pernod.fr/",
            "image": "https://www.whisky.com/fileadmin/_processed_/csm_Allt-a-Bhaine_Distil_c2f028851362c96d6c293c7d23919ec9_0093cb01f3.jpg",
            "founded": 1975,
            "status": "Active",
            "number_of_stills": 2,
            "capacity_litres": 4000000,
            "type": "Scotch",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Pernod Ricard"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.312957,
               57.600773
            ]
         },
         "properties": {
            "cartodb_id": 94,
            "name": "Mannochmore",
            "wikipedia": "https://en.wikipedia.org/wiki/Mannochmore_distillery",
            "homepage": "http://www.diageo.com/",
            "image": "http://www.scotchwhisky.net/images/dist/mann_sign_b.jpg",
            "founded": 1971,
            "status": "Active",
            "number_of_stills": 3,
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "12 years old",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.9548,
               57.5714
            ]
         },
         "properties": {
            "cartodb_id": 115,
            "name": "Aultmore",
            "wikipedia": "https://en.wikipedia.org/wiki/Aultmore_distillery",
            "homepage": "http://www.aultmore.com/splash",
            "image": "http://maltandoak.com/wp-content/uploads/2015/01/Aultmore_b_fbx-e1422520520321.jpg",
            "founded": 1895,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 2100000,
            "type": "Single Malt",
            "age": "12 years",
            "cask_types": "",
            "abv": "43%",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Bacardi"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.7598,
               57.562077
            ]
         },
         "properties": {
            "cartodb_id": 118,
            "name": "Knockdhu",
            "wikipedia": "https://en.wikipedia.org/wiki/Knockdhu_distillery",
            "homepage": "http://ancnoc.com/",
            "image": "https://scontent.cdninstagram.com/vp/ccf4263d09d951d054ca7d0485125995/5DCE4B58/t51.2885-15/e35/s320x320/61989141_103441597579284_4325417707080399631_n.jpg?_nc_ht=scontent.cdninstagram.com",
            "founded": 1894,
            "status": "Operational",
            "number_of_stills": "",
            "capacity_litres": 1700000,
            "type": "Single Malt",
            "age": "12 and 16 years old",
            "cask_types": "American white oak ex-bourbon casks",
            "abv": "40-50%",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "By appointment",
            "icon": "alcohol-shop",
            "owner": "Inver House"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.283024,
               57.608845
            ]
         },
         "properties": {
            "cartodb_id": 95,
            "name": "Longmorn",
            "wikipedia": "https://en.wikipedia.org/wiki/Longmorn_distillery",
            "homepage": "http://www.longmornbrothers.com/html/distillery.htm",
            "image": "http://www.whiskymerchants.co.uk/communities/9/004/005/976/859//images/4535763752.jpg",
            "founded": 1893,
            "status": "Operational",
            "number_of_stills": 4,
            "capacity_litres": 3500000,
            "type": "Single Malt",
            "age": "15 and 16 years old",
            "cask_types": "American white oak, ex-bourbon casks",
            "abv": "40-43%",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Pernod Ricard"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -4.4375,
               55.922436
            ]
         },
         "properties": {
            "cartodb_id": 23,
            "name": "Auchentoshan",
            "wikipedia": "https://en.wikipedia.org/wiki/Auchentoshan_distillery",
            "homepage": "http://www.auchentoshan.com/",
            "image": "https://files.list.co.uk/images/a/auch-ext-lst107017-2.jpg",
            "founded": 1823,
            "status": "Operational",
            "number_of_stills": 1,
            "capacity_litres": 1800000,
            "type": "Single Malt",
            "age": "10 Years\n12 Years\n18 Years\n21 Years",
            "cask_types": "80% refill\n20% First fill sherry wood\n1st Fill Bourbon Cask\nBourbon with 1 year Oloroso finish and then 1 year Pedro Ximenez finish",
            "abv": "40%-43%",
            "region": "Lowland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Beam Suntory"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -6.289726,
               55.756844
            ]
         },
         "properties": {
            "cartodb_id": 4,
            "name": "Bowmore",
            "wikipedia": "https://en.wikipedia.org/wiki/Bowmore_distillery",
            "homepage": "http://www.bowmore.co.uk/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/3/3a/Morrison_Bowmore%2C_Islay.jpg",
            "founded": 1779,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 1700000,
            "type": "Single Malt",
            "age": "\tLegend\n12-year-old\n15-year-old\n18-year-old\n25-year-old",
            "cask_types": "American Oak (86%)\nSherry (14%)",
            "abv": "",
            "region": "Islay",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Beam Suntory"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.261641,
               55.002686
            ]
         },
         "properties": {
            "cartodb_id": 125,
            "name": "Annandale",
            "wikipedia": "https://en.wikipedia.org/wiki/Annandale_distillery",
            "homepage": "http://www.annandaledistillery.co.uk/",
            "image": "https://dimg.visitscotland.com/wsimgs/Annandale%20Distillery%20at%20night_823453710.jpg",
            "founded": 1836,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Lowland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Annandale Distillery Company"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.849721,
               56.62432
            ]
         },
         "properties": {
            "cartodb_id": 26,
            "name": "Aberfeldy",
            "wikipedia": "https://en.wikipedia.org/wiki/Aberfeldy_distillery",
            "homepage": "http://www.aberfeldy.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/4/4c/Aberfeldy-1.jpg",
            "founded": 1896,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 3500000,
            "type": "Single Malt",
            "age": "12 years",
            "cask_types": "American White Oak, Ex Bourbon Casks (main)",
            "abv": "40%-43%",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Bacardi"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.553248,
               56.648
            ]
         },
         "properties": {
            "cartodb_id": 126,
            "name": "Arbikie",
            "wikipedia": "",
            "homepage": "http://www.arbikie.com/",
            "image": "https://scotchwhisky.com/images/media/0f4fbb6e18b9b43ffa57f2926d8ddcc0.jpg",
            "founded": "",
            "status": "Operational",
            "number_of_stills": "",
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "",
            "cask_types": "Various",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Arbikie Distilling"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.722756,
               56.69829
            ]
         },
         "properties": {
            "cartodb_id": 48,
            "name": "Blair Atholl",
            "wikipedia": "https://en.wikipedia.org/wiki/Blair_Athol_distillery",
            "homepage": "http://www.blairatholl.org.uk/history-heritage/1604-Blair-Athol-Distillery-Visitor-Centre-and-Whisky-Shop",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/f/f2/Blair_Athol.JPG/800px-Blair_Athol.JPG",
            "founded": 1798,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 2500000,
            "type": "Single Malt",
            "age": "12 years",
            "cask_types": "",
            "abv": "43%",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -4.180834,
               57.840103
            ]
         },
         "properties": {
            "cartodb_id": 41,
            "name": "Balblair",
            "wikipedia": "https://en.wikipedia.org/wiki/Balblair_distillery",
            "homepage": "http://www.balblair.com/",
            "image": "https://pbs.twimg.com/media/CkmmSN2UgAEp3tl.jpg:large",
            "founded": 1790,
            "status": "Active",
            "number_of_stills": 1,
            "capacity_litres": 1800000,
            "type": "Single Malt",
            "age": "Various",
            "cask_types": "",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "ThaiBev"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.620768,
               57.613625
            ]
         },
         "properties": {
            "cartodb_id": 50,
            "name": "Benromach",
            "wikipedia": "https://en.wikipedia.org/wiki/Benromach_distillery",
            "homepage": "http://www.benromach.com/",
            "image": "https://upload.wikimedia.org/wikipedia/en/thumb/9/94/Benromach_Distillery.jpg/1280px-Benromach_Distillery.jpg",
            "founded": 1898,
            "status": "Operational",
            "number_of_stills": 1,
            "capacity_litres": 1500000,
            "type": "Single Malt",
            "age": "5, 10, 15, 21, 24, 50 years old.",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Gordon & MacPhail"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.757,
               57.3401
            ]
         },
         "properties": {
            "cartodb_id": 73,
            "name": "Ardmore",
            "wikipedia": "https://en.wikipedia.org/wiki/Ardmore_distillery",
            "homepage": "http://www.ardmorewhisky.com/",
            "image": "https://maltmileage.files.wordpress.com/2013/10/f5c22-picsart_1381646462593.jpg",
            "founded": 1898,
            "status": "Operational",
            "number_of_stills": 4,
            "capacity_litres": 5530000,
            "type": "Single Malt",
            "age": "Traditional, Triple Wood, Legacy (NAS), 12 years (Port Wood), 25 years, 30 years",
            "cask_types": "American White Oak, Ex Bourbon Casks (main)",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Beam Suntory"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -5.942348,
               56.690903
            ]
         },
         "properties": {
            "cartodb_id": 127,
            "name": "Ardnamurchan",
            "wikipedia": "",
            "homepage": "http://www.ardnamurchandistillery.com/",
            "image": "http://www.urbanrealm.com/images/news/news_4943.jpg",
            "founded": 2014,
            "status": "Operational",
            "number_of_stills": "",
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "",
            "cask_types": "American and European oak, ex-sherry casks and American oak ex-bourbon casks",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Adelphi Whisky"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.533124,
               57.325176
            ]
         },
         "properties": {
            "cartodb_id": 57,
            "name": "Balmenach",
            "wikipedia": "https://en.wikipedia.org/wiki/Balmenach_distillery",
            "homepage": "http://www.caorunngin.com/",
            "image": "http://www.scotchwhisky.net/images/dist/blm_sign.jpg",
            "founded": 1824,
            "status": "Active",
            "number_of_stills": 3,
            "capacity_litres": 2000000,
            "type": "Scottish Gin",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "ThaiBev"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.759167,
               57.56333
            ]
         },
         "properties": {
            "cartodb_id": 124,
            "name": "anCnoc",
            "wikipedia": "https://en.wikipedia.org/wiki/Knockdhu_distillery",
            "homepage": "http://ancnoc.com/",
            "image": "https://pbs.twimg.com/media/Cj8s18BWkAAe_AA.jpg:large",
            "founded": 1894,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 1700000,
            "type": "Single Malt",
            "age": "12, 16, 18, 22 and 35 years",
            "cask_types": "American White Oak, Ex Bourbon Casks (main)",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "By appointment",
            "icon": "alcohol-shop",
            "owner": "Inver House Distillers"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.236654,
               57.441612
            ]
         },
         "properties": {
            "cartodb_id": 129,
            "name": "Benrinnes",
            "wikipedia": "https://en.wikipedia.org/wiki/Benrinnes_distillery",
            "homepage": "http://www.diageo.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/7/79/The_beloved_Benrinnes_distillery%5E%5E_-_geograph.org.uk_-_186082.jpg",
            "founded": 1835,
            "status": "Active",
            "number_of_stills": 2,
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "15 years",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -5.074117,
               56.83469
            ]
         },
         "properties": {
            "cartodb_id": 34,
            "name": "Ben Nevis",
            "wikipedia": "https://en.wikipedia.org/wiki/Ben_Nevis_distillery",
            "homepage": "http://www.bennevisdistillery.com/",
            "image": "https://visitfortwilliam.s3.amazonaws.com/visitfortwilliam_uploads/production/photograph/image/6984/slider_distillery_page_4915.jpg",
            "founded": 1825,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 2000000,
            "type": "Single Malt",
            "age": "10-year-old\n16-year-old\n21-year-old",
            "cask_types": "",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Nikka Whisky Distilling"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.126919,
               57.457302
            ]
         },
         "properties": {
            "cartodb_id": 83,
            "name": "Balvenie",
            "wikipedia": "https://en.wikipedia.org/wiki/Balvenie_distillery",
            "homepage": "https://www.thebalvenie.com/",
            "image": "https://www.undiscoveredscotland.co.uk/dufftown/balvenie/images/balvenie-450.jpg",
            "founded": 1892,
            "status": "Operational",
            "number_of_stills": 5,
            "capacity_litres": 5600000,
            "type": "Single Malt",
            "age": "\t10-year-old\n12-year-old\n14-year-old\n15-year-old\n17-year-old\n18-year-old\n21-year-old\n25-year-old\n30-year-old\nvarious vintages",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "William Grant & Sons"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.905467,
               57.539692
            ]
         },
         "properties": {
            "cartodb_id": 130,
            "name": "Brackla",
            "wikipedia": "https://en.wikipedia.org/wiki/Royal_Brackla_distillery",
            "homepage": "https://www.lastgreatmalts.com",
            "image": "http://www.somersetwhisky.com/wp-content/uploads/2015/12/BracklaLogo.jpg",
            "founded": 1812,
            "status": "Active",
            "number_of_stills": 2,
            "capacity_litres": 3500000,
            "type": "Single Malt",
            "age": "12-year-old 16-year-old 21-year-old",
            "cask_types": "",
            "abv": "40%",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Bacardi"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -5.61095,
               55.427208
            ]
         },
         "properties": {
            "cartodb_id": 137,
            "name": "Glengyle",
            "wikipedia": "https://en.wikipedia.org/wiki/Glengyle_distillery",
            "homepage": "http://www.kilkerransinglemalt.com/",
            "image": "https://www.whiskys.co.uk/wp-content/uploads/2016/12/Glengyle-distillery..jpg",
            "founded": 1872,
            "status": "Operational",
            "number_of_stills": "",
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Campbelltown",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": ""
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.518213,
               57.62383
            ]
         },
         "properties": {
            "cartodb_id": 52,
            "name": "Glenburgie",
            "wikipedia": "https://en.wikipedia.org/wiki/Glenburgie_distillery",
            "homepage": "http://glenburgie.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/e/ed/Glenburgie.jpg",
            "founded": 1810,
            "status": "Open",
            "number_of_stills": 3,
            "capacity_litres": 4200000,
            "type": "",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Pernod Ricard"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.653499,
               56.736286
            ]
         },
         "properties": {
            "cartodb_id": 66,
            "name": "Glencadam",
            "wikipedia": "https://en.wikipedia.org/wiki/Glencadam_distillery",
            "homepage": "http://www.glencadamwhisky.com/",
            "image": "http://www.glencadamwhisky.com/images/news_images/heritage_large.jpg",
            "founded": 1825,
            "status": "Operational",
            "number_of_stills": "",
            "capacity_litres": 1500000,
            "type": "Single Malt",
            "age": "10, 12, 14, 15 and 21 years old",
            "cask_types": "Bourbon, port, oloroso sherry",
            "abv": "46%",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Angus Dundee plc"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -6.363026,
               55.76679
            ]
         },
         "properties": {
            "cartodb_id": 131,
            "name": "Bruichladdich",
            "wikipedia": "https://en.wikipedia.org/wiki/Bruichladdich_distillery",
            "homepage": "http://www.bruichladdich.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/0/02/Distillery-gates.jpg/1920px-Distillery-gates.jpg",
            "founded": 1881,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 1500000,
            "type": "Single Malt",
            "age": "2013 Core Range:\nBruichladdich Scottish Barley\nBruichladdich Islay Barley\nBruichladdich The Organic\nBruichladdich Bere Barley\nBruichladdich Black Art",
            "cask_types": "American Oak, European Oak, New Oak",
            "abv": "",
            "region": "Islay",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Remy Cointreau"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -6.109525,
               55.85414
            ]
         },
         "properties": {
            "cartodb_id": 9,
            "name": "Caol Ila",
            "wikipedia": "https://en.wikipedia.org/wiki/Caol_Ila_distillery",
            "homepage": "https://www.discovering-distilleries.com/caolila/",
            "image": "https://media-cdn.tripadvisor.com/media/photo-w/0d/ce/52/6d/caol-ila-distillery-landscape.jpg",
            "founded": 1846,
            "status": "Operational",
            "number_of_stills": "",
            "capacity_litres": 3500000,
            "type": "Single Malt",
            "age": "12, 18, 25 years old",
            "cask_types": "American Oak",
            "abv": "",
            "region": "Islay",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.738149,
               57.67935
            ]
         },
         "properties": {
            "cartodb_id": 119,
            "name": "Glenglassaugh",
            "wikipedia": "https://en.wikipedia.org/wiki/Glenglassaugh_distillery",
            "homepage": "http://www.glenglassaugh.com/",
            "image": "http://www.glenglassaugh.com/wp-content/themes/Glenglassaugh2014/images/homepage/news/random.php",
            "founded": 1875,
            "status": "Operational",
            "number_of_stills": "",
            "capacity_litres": 1000000,
            "type": "Single Malt",
            "age": "Various",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "BenRiach Distillery Company"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.288914,
               57.6099
            ]
         },
         "properties": {
            "cartodb_id": 96,
            "name": "BenRiach",
            "wikipedia": "https://en.wikipedia.org/wiki/BenRiach_distillery",
            "homepage": "http://www.benriachdistillery.co.uk/",
            "image": "http://www.benriachdistillery.co.uk/wp-content/uploads/2015/12/our-story-img1.jpg",
            "founded": 1898,
            "status": "Active",
            "number_of_stills": 2,
            "capacity_litres": 2800000,
            "type": "Single Malt",
            "age": "10-year-old\n16-year-old\n20-year-old",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "BenRiach Distillery Company"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.9571,
               57.535
            ]
         },
         "properties": {
            "cartodb_id": 112,
            "name": "Glen Keith",
            "wikipedia": "https://en.wikipedia.org/wiki/Glen_Keith",
            "homepage": "http://www.pernod.fr/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/8/8b/Glen_Keith_Distillery%2C_Moray%2C_Scotland_%E2%80%93_02-02-08.jpg/1280px-Glen_Keith_Distillery%2C_Moray%2C_Scotland_%E2%80%93_02-02-08.jpg",
            "founded": 1957,
            "status": "Under redevelopment",
            "number_of_stills": 3,
            "capacity_litres": 3500000,
            "type": "Blended",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Pernod Ricard"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.103983,
               56.29725
            ]
         },
         "properties": {
            "cartodb_id": 132,
            "name": "Daftmill",
            "wikipedia": "https://en.wikipedia.org/wiki/Daftmill_distillery",
            "homepage": "http://www.daftmill.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/e/e3/Daftmill_distillery_chimney.jpg/1280px-Daftmill_distillery_chimney.jpg",
            "founded": 2005,
            "status": "Active",
            "number_of_stills": 2,
            "capacity_litres": 2500,
            "type": "Single Malt",
            "age": "yet to be released",
            "cask_types": "",
            "abv": "",
            "region": "Lowland",
            "country": "Scotland",
            "open_to_public": "By appointment",
            "icon": "alcohol-shop",
            "owner": "Independent"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.625818,
               57.484188
            ]
         },
         "properties": {
            "cartodb_id": 85,
            "name": "GlenDronach",
            "wikipedia": "https://en.wikipedia.org/wiki/Glendronach_distillery",
            "homepage": "http://glendronachdistillery.co.uk/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/f/fd/Glendronach_Distillery_-_the_Garden_-_geograph.org.uk_-_990246.jpg",
            "founded": 1826,
            "status": "Active",
            "number_of_stills": 2,
            "capacity_litres": 1300000,
            "type": "Single Malt",
            "age": "8, 12, 15, 18, 20, 21, 31 and 33 years old",
            "cask_types": "Bourbon, oloroso sherry",
            "abv": "43-48%",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "BenRiach Distillery Company"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -6.107953,
               55.64067
            ]
         },
         "properties": {
            "cartodb_id": 10,
            "name": "Ardbeg",
            "wikipedia": "https://en.wikipedia.org/wiki/Ardbeg_distillery",
            "homepage": "http://www.ardbeg.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/2/2c/Ardbeg_across_bay_-_Canthusus.JPG",
            "founded": 1815,
            "status": "Active",
            "number_of_stills": 1,
            "capacity_litres": 1250000,
            "type": "Single Malt",
            "age": "\t10 Year Old\nAirigh Nam Beist\nBlasda\nCorryvreckan\nSupernova\nUigeadail\nRollercoaster\nAlligator\nArdbeg Day\nGalileo\nArdbog",
            "cask_types": "Bourbon, Sherry",
            "abv": "",
            "region": "Islay",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "LVMH"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.319489,
               57.337875
            ]
         },
         "properties": {
            "cartodb_id": 74,
            "name": "Glen Garioch",
            "wikipedia": "https://en.wikipedia.org/wiki/Glen_Garioch_distillery",
            "homepage": "http://www.glengarioch.com/",
            "image": "https://foodanddrink.scotsman.com/wp-content/uploads/2017/10/DSC0511-13-750x400.jpg",
            "founded": 1797,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "12 years old. Vintages",
            "cask_types": "",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Beam Suntory"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.128529,
               57.454464
            ]
         },
         "properties": {
            "cartodb_id": 84,
            "name": "Glenfiddich",
            "wikipedia": "https://en.wikipedia.org/wiki/Glenfiddich",
            "homepage": "http://www.glenfiddich.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/c/c8/Glenffidich_Distillery%28RLH%291979%2C_Dufftown%2C_Speyside%2C_Scotland.jpg",
            "founded": 1886,
            "status": "Operational",
            "number_of_stills": "",
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "12, 15, 18, 19, 21, 30, 40 and 50 years old",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "William Grant & Sons"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.31432,
               57.42651
            ]
         },
         "properties": {
            "cartodb_id": 68,
            "name": "Glenfarclas",
            "wikipedia": "https://en.wikipedia.org/wiki/Glenfarclas_distillery",
            "homepage": "http://www.glenfarclas.co.uk/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/9/91/Glenfarclas_Visitor_Centre.jpg",
            "founded": 1836,
            "status": "Active",
            "number_of_stills": 3,
            "capacity_litres": 3000000,
            "type": "Single Malt",
            "age": "10, 12, 15, 17, 18, 21, 25, 30 and 40 years old",
            "cask_types": "",
            "abv": "40, 43 and 46%",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "J & G Grant"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -4.36492,
               56.01386
            ]
         },
         "properties": {
            "cartodb_id": 22,
            "name": "Glengoyne",
            "wikipedia": "https://en.wikipedia.org/wiki/Glengoyne_distillery",
            "homepage": "http://www.glengoyne.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Glengoyne_Distillery.JPG/1280px-Glengoyne_Distillery.JPG",
            "founded": 1833,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 1100000,
            "type": "Single Malt",
            "age": "10, 12, 15, 18, 21 and 25 years old",
            "cask_types": "",
            "abv": "40-57.2%",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Dumgoyne"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.890606,
               55.891006
            ]
         },
         "properties": {
            "cartodb_id": 33,
            "name": "Glenkinchie",
            "wikipedia": "https://en.wikipedia.org/wiki/Glenkinchie_distillery",
            "homepage": "https://www.discovering-distilleries.com/glenkinchie/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/c/c7/Glenkinchie_Distillery1.jpg",
            "founded": 1837,
            "status": "Active",
            "number_of_stills": "",
            "capacity_litres": 2700000,
            "type": "Single Malt",
            "age": "12 and 14 years old",
            "cask_types": "",
            "abv": "",
            "region": "Lowland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.227963,
               57.466747
            ]
         },
         "properties": {
            "cartodb_id": 88,
            "name": "Aberlour",
            "wikipedia": "https://en.wikipedia.org/wiki/Aberlour_distillery",
            "homepage": "http://www.aberlour.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/4/4d/Aberlour_Distillery_2.JPG/1280px-Aberlour_Distillery_2.JPG",
            "founded": 1879,
            "status": "Active",
            "number_of_stills": 2,
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "10, 12, 15, 16, 18 and 30 years",
            "cask_types": "American White Oak, Ex Bourbon Casks (main)",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Pernod Ricard"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.20936,
               57.52564
            ]
         },
         "properties": {
            "cartodb_id": 103,
            "name": "Glen Spey",
            "wikipedia": "https://en.wikipedia.org/wiki/Glen_Spey_Distillery",
            "homepage": "http://www.diageo.com/",
            "image": "http://s0.geograph.org.uk/photos/88/58/885814_427a23ee.jpg",
            "founded": 1878,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 1400000,
            "type": "Single Malt",
            "age": "8 and 14 years old",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.338694,
               57.343056
            ]
         },
         "properties": {
            "cartodb_id": 37,
            "name": "Glenlivet",
            "wikipedia": "https://en.wikipedia.org/wiki/The_Glenlivet_distillery",
            "homepage": "https://www.theglenlivet.com",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/The_Glenlivet.jpg/1280px-The_Glenlivet.jpg",
            "founded": 1824,
            "status": "Operational",
            "number_of_stills": 7,
            "capacity_litres": 10500000,
            "type": "Single Malt",
            "age": "12, 15, 16, 18, 21 and 25 years old",
            "cask_types": "Bourbon, French oak",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Pernod Ricard"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -6.152172,
               55.62967
            ]
         },
         "properties": {
            "cartodb_id": 6,
            "name": "Laphroaig",
            "wikipedia": "https://en.wikipedia.org/wiki/Laphroaig_distillery",
            "homepage": "http://www.laphroaig.com/",
            "image": "https://2x1dks3q6aoj44bz1r1tr92f-wpengine.netdna-ssl.com/wp-content/uploads/2018/08/laphroaig-warehouse-from-malting-floor.jpg",
            "founded": 1815,
            "status": "Operational",
            "number_of_stills": 4,
            "capacity_litres": 2600000,
            "type": "Single Malt",
            "age": "10, 15, 18, 25, 27, 30 and 40 years old",
            "cask_types": "American oak bourbon, Oak quarter cask, European oak Oloroso sherry",
            "abv": "40-55.3%",
            "region": "Islay",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Beam Suntory"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -5.6106,
               55.4282
            ]
         },
         "properties": {
            "cartodb_id": 14,
            "name": "Springbank",
            "wikipedia": "https://en.wikipedia.org/wiki/Springbank_distillery",
            "homepage": "http://springbankwhisky.com/",
            "image": "http://whiskycyclist.weebly.com/uploads/7/6/7/4/7674573/218651_orig.jpg",
            "founded": 1828,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 750000,
            "type": "Single Malt",
            "age": "10, 12, 15, 18 and 21 years old",
            "cask_types": "Bourbon, Sherry, Wine, Rum, Calvados",
            "abv": "",
            "region": "Cambelltown",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Independent"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -5.276313,
               55.69754
            ]
         },
         "properties": {
            "cartodb_id": 128,
            "name": "Arran",
            "wikipedia": "https://en.wikipedia.org/wiki/Arran_distillery",
            "homepage": "http://www.arranwhisky.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/d/db/Arran_Distillery%2C_Lochranza_%2C_Isle_of_Arran.jpg/250px-Arran_Distillery%2C_Lochranza_%2C_Isle_of_Arran.jpg",
            "founded": 1995,
            "status": "Operational",
            "number_of_stills": 1,
            "capacity_litres": 750000,
            "type": "Single Malt",
            "age": "10 Years, 12 Years, 14 Years, 18 years",
            "cask_types": "American White Oak, Ex-Bourbon Casks (Main) Ex Sherry Casks",
            "abv": "46%",
            "region": "Island",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Isle of Arran Distillers Ltd"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.310597,
               57.318737
            ]
         },
         "properties": {
            "cartodb_id": 72,
            "name": "Tamnavulin",
            "wikipedia": "https://en.wikipedia.org/wiki/Tamnavulin_distillery",
            "homepage": "http://www.emperadorbrandy.com/",
            "image": "http://www.scotchwhisky.net/images/dist/tamn_dist.jpg",
            "founded": 1966,
            "status": "Operational",
            "number_of_stills": "",
            "capacity_litres": 4000000,
            "type": "Single Malt",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Emperador Distillers Inc."
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.216505,
               57.526493
            ]
         },
         "properties": {
            "cartodb_id": 100,
            "name": "Glenrothes",
            "wikipedia": "https://en.wikipedia.org/wiki/The_Glenrothes_distillery",
            "homepage": "http://www.bbr.com/producer-981-glenrothes-distillery-speyside",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/5/57/Rothes_Glenrothes_distillery_letters.jpg/1280px-Rothes_Glenrothes_distillery_letters.jpg",
            "founded": 1878,
            "status": "Operational",
            "number_of_stills": 5,
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "Select Reserve",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "The Edrington Group"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -6.069635,
               56.620674
            ]
         },
         "properties": {
            "cartodb_id": 11,
            "name": "Tobermory",
            "wikipedia": "https://en.wikipedia.org/wiki/Tobermory_distillery",
            "homepage": "http://tobermorydistillery.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Tobermory_Distillery%2C_Isle_of_Mull.jpg/220px-Tobermory_Distillery%2C_Isle_of_Mull.jpg",
            "founded": 1798,
            "status": "Active",
            "number_of_stills": 4,
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "10, 15, 20, 31 and 32 years old",
            "cask_types": "",
            "abv": "",
            "region": "Island",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Burn Stewart"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -5.472227,
               56.41498
            ]
         },
         "properties": {
            "cartodb_id": 15,
            "name": "Oban",
            "wikipedia": "https://en.wikipedia.org/wiki/Oban_distillery",
            "homepage": "https://www.discovering-distilleries.com/oban/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/4/4f/Oban_Distillery.jpg/1280px-Oban_Distillery.jpg",
            "founded": 1794,
            "status": "Operational",
            "number_of_stills": 1,
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "14, 18 and 32 years old",
            "cask_types": "",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.341088,
               57.644573
            ]
         },
         "properties": {
            "cartodb_id": 58,
            "name": "Glen Moray",
            "wikipedia": "https://en.wikipedia.org/wiki/Glen_Moray_distillery",
            "homepage": "http://www.glenmoray.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/e/e8/Glen_Moray_Distillery.JPG/1280px-Glen_Moray_Distillery.JPG",
            "founded": 1897,
            "status": "Operational",
            "number_of_stills": 3,
            "capacity_litres": 3300000,
            "type": "Single Malt",
            "age": "12 and 16 years old plus special bottlings",
            "cask_types": "Bourbon casks",
            "abv": "40%",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "La Martiniquaise"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.286972,
               57.635296
            ]
         },
         "properties": {
            "cartodb_id": 99,
            "name": "Linkwood",
            "wikipedia": "https://en.wikipedia.org/wiki/Linkwood_distillery",
            "homepage": "http://www.diageo.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/9/95/Linkwood_pagoda_-_geograph.org.uk_-_1134613.jpg",
            "founded": 1821,
            "status": "Operational",
            "number_of_stills": 3,
            "capacity_litres": 2500000,
            "type": "Single Malt",
            "age": "12, 26 and 30 years old",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.953928,
               57.546635
            ]
         },
         "properties": {
            "cartodb_id": 114,
            "name": "Strathisla",
            "wikipedia": "https://en.wikipedia.org/wiki/Strathisla_distillery",
            "homepage": "http://www.chivas.com/en/int/heritage/strathisla/",
            "image": "http://cdnfiles.hdrcreme.com/42333/original/strathisla-distillery-keith-scotland.jpg?1426749810",
            "founded": 1786,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 2400000,
            "type": "Single Malt",
            "age": "12, 14, 19 and 25 years old",
            "cask_types": "American white oak, ex-bourbon casks",
            "abv": "40-43%",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Chivas Brothers"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.551389,
               58.59528
            ]
         },
         "properties": {
            "cartodb_id": 147,
            "name": "Wolfburn",
            "wikipedia": "https://en.wikipedia.org/wiki/Wolfburn_distillery",
            "homepage": "http://www.wolfburn.com/",
            "image": "http://www.whiskyintelligence.com/wp-content/uploads/2013/01/aa24.jpg",
            "founded": 2013,
            "status": "Operational",
            "number_of_stills": 1,
            "capacity_litres": 115000,
            "type": "Single Malt",
            "age": "",
            "cask_types": "American oak bourbon",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "By appointment",
            "icon": "alcohol-shop",
            "owner": "Independent"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.786179,
               56.25736
            ]
         },
         "properties": {
            "cartodb_id": 28,
            "name": "Tullibardine",
            "wikipedia": "https://en.wikipedia.org/wiki/Tullibardine_distillery",
            "homepage": "http://www.tullibardine.com/",
            "image": "https://blosslynspage.files.wordpress.com/2017/03/dsc_0759.jpg",
            "founded": 1949,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 2700000,
            "type": "Single Malt",
            "age": "",
            "cask_types": "Bourbon, banyuls, sherry",
            "abv": "40%",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Picard Vins & Spiritueux"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.471851,
               57.668934
            ]
         },
         "properties": {
            "cartodb_id": 143,
            "name": "Roseisle",
            "wikipedia": "",
            "homepage": "http://www.diageo.com/en-row/ourbrands/infocus/Pages/InFocus-Roseisle.aspx",
            "image": "http://www.slowdrink.de/wp-content/uploads/2012/07/Roseisle-Distillery_1.jpg",
            "founded": 2010,
            "status": "Operational",
            "number_of_stills": 14,
            "capacity_litres": "",
            "type": "Blended",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -6.430833,
               55.786945
            ]
         },
         "properties": {
            "cartodb_id": 139,
            "name": "Kilchoman",
            "wikipedia": "https://en.wikipedia.org/wiki/Kilchoman_distillery",
            "homepage": "http://kilchomandistillery.com/",
            "image": "https://i1.wp.com/www.myhighlands.de/wp-content/uploads/2011/10/kilchoman-distillery.jpg",
            "founded": 2005,
            "status": "Operational",
            "number_of_stills": 1,
            "capacity_litres": 90000,
            "type": "Single Malt",
            "age": "3, 5, 8, 10 and 12 years old",
            "cask_types": "",
            "abv": "",
            "region": "Islay",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Independent"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.084722,
               58.434444
            ]
         },
         "properties": {
            "cartodb_id": 142,
            "name": "Old Pulteney",
            "wikipedia": "https://en.wikipedia.org/wiki/Old_Pulteney_distillery",
            "homepage": "http://www.oldpulteney.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/5/53/Pulteney_Distillery.jpeg",
            "founded": 1826,
            "status": "Active",
            "number_of_stills": 1,
            "capacity_litres": 1000000,
            "type": "Single Malt",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "InterBev"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.8528,
               56.389156
            ]
         },
         "properties": {
            "cartodb_id": 27,
            "name": "Glenturret",
            "wikipedia": "https://en.wikipedia.org/wiki/Glenturret_distillery",
            "homepage": "http://www.theglenturret.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/0/0e/Glenturret.jpg/1280px-Glenturret.jpg",
            "founded": 1775,
            "status": "Operational",
            "number_of_stills": 1,
            "capacity_litres": 340000,
            "type": "Single Malt",
            "age": "8, 10, 12, 15, 18, 21 and 25 years old",
            "cask_types": "Oak",
            "abv": "37.5-55.6%",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Highland Distillers"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -4.003873,
               57.343403
            ]
         },
         "properties": {
            "cartodb_id": 44,
            "name": "Tomatin",
            "wikipedia": "https://en.wikipedia.org/wiki/Tomatin_distillery",
            "homepage": "http://www.tomatin.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/7/73/Tomatin_entrance.jpg",
            "founded": 1897,
            "status": "Operational",
            "number_of_stills": 6,
            "capacity_litres": 5050000,
            "type": "Single Malt and Blended",
            "age": "12, 14, 18, 25 and 36 years old",
            "cask_types": "",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Takara Shuzo Corp."
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.955505,
               58.968185
            ]
         },
         "properties": {
            "cartodb_id": 117,
            "name": "Highland Park",
            "wikipedia": "https://en.wikipedia.org/wiki/Highland_Park_distillery",
            "homepage": "http://highlandpark.co.uk/",
            "image": "https://media-cdn.tripadvisor.com/media/photo-s/02/01/9a/bf/highland-park-distillery.jpg",
            "founded": 1798,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 2500000,
            "type": "Single Malt",
            "age": "12, 15, 16, 18, 21, 25, 30 and 40 years old",
            "cask_types": "Bourbon, Sherry",
            "abv": "",
            "region": "Island",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Edrington Group"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -4.077129,
               57.82597
            ]
         },
         "properties": {
            "cartodb_id": 43,
            "name": "Glenmorangie",
            "wikipedia": "https://en.wikipedia.org/wiki/Glenmorangie_distillery",
            "homepage": "http://www.glenmorangie.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/8/8e/Glenmorangie_Distillery.jpg/1280px-Glenmorangie_Distillery.jpg",
            "founded": 1843,
            "status": "Operational",
            "number_of_stills": 6,
            "capacity_litres": 6000000,
            "type": "Single Malt",
            "age": "10, 12, 18 and 25 years old",
            "cask_types": "American white oak, ex-bourbon  whisky casks",
            "abv": "40-46%",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Louis Vuitton Moët Hennessy"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -4.576879,
               55.992405
            ]
         },
         "properties": {
            "cartodb_id": 141,
            "name": "Loch Lomond",
            "wikipedia": "https://en.wikipedia.org/wiki/Loch_Lomond_distillery",
            "homepage": "http://www.lochlomondgroup.com/",
            "image": "https://www.rabbies.com/application/files/7515/3623/8584/WHIS_01_697_x_448.jpg",
            "founded": 1964,
            "status": "Active",
            "number_of_stills": 4,
            "capacity_litres": 4000000,
            "type": "Single Malt and Blended",
            "age": null,
            "cask_types": null,
            "abv": null,
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Loch Lomond Distillery Company"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.342934,
               57.456413
            ]
         },
         "properties": {
            "cartodb_id": 87,
            "name": "Knockando",
            "wikipedia": "https://en.wikipedia.org/wiki/Knockando_distillery",
            "homepage": "https://www.malts.com",
            "image": "http://www.scotchwhisky.net/images/dist/knockando_sign2.jpg",
            "founded": 1898,
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 1800000,
            "type": "Single Malt",
            "age": "18 years old",
            "cask_types": "American white oak, ex-bourbon casks/ European oak ex-sherry casks",
            "abv": "40%",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -4.002403,
               57.072727
            ]
         },
         "properties": {
            "cartodb_id": 144,
            "name": "Speyside",
            "wikipedia": "https://en.wikipedia.org/wiki/The_Speyside_distillery",
            "homepage": "http://www.speysidedistillery.co.uk/",
            "image": "http://1.bp.blogspot.com/-Q5_mKLzgTcM/UGg0_pkaejI/AAAAAAAABWw/m4iYiMOoeQg/s1600/Speyside+Distillery.JPG",
            "founded": 1962,
            "status": "Active",
            "number_of_stills": 2,
            "capacity_litres": 500000,
            "type": "Single Malt",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Harvey's of Edinburgh International"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.131361,
               57.460117
            ]
         },
         "properties": {
            "cartodb_id": 140,
            "name": "Kininvie",
            "wikipedia": "https://en.wikipedia.org/wiki/Kininvie_distillery",
            "homepage": "http://www.williamgrant.com/",
            "image": "https://www.whiskys.co.uk/wp-content/uploads/2017/03/Kininvie-Distillery.jpg",
            "founded": 1990,
            "status": "Mothballed",
            "number_of_stills": 3,
            "capacity_litres": "",
            "type": "Blended Malt",
            "age": "",
            "cask_types": "Bourbon",
            "abv": "40%",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "William Grant & Sons"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.209639,
               57.02973
            ]
         },
         "properties": {
            "cartodb_id": 70,
            "name": "Lochnagar",
            "wikipedia": "https://en.wikipedia.org/wiki/Royal_Lochnagar_distillery",
            "homepage": "https://www.discovering-distilleries.com/royallochnagar/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/9/96/Royal_Lochnagar_Distillery_Main_Building_2012.jpg/1920px-Royal_Lochnagar_Distillery_Main_Building_2012.jpg",
            "founded": 1826,
            "status": "Active",
            "number_of_stills": 1,
            "capacity_litres": 400000,
            "type": "Single Malt",
            "age": "",
            "cask_types": "",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.407822,
               57.397625
            ]
         },
         "properties": {
            "cartodb_id": 53,
            "name": "Tormore",
            "wikipedia": "https://en.wikipedia.org/wiki/Tormore_distillery",
            "homepage": "http://www.tormoredistillery.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/9/9f/GB_1990089.jpg/1920px-GB_1990089.jpg",
            "founded": 1958,
            "status": "Active",
            "number_of_stills": 4,
            "capacity_litres": 3700000,
            "type": "Single Malt",
            "age": "14 and 16 years old",
            "cask_types": "",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "No",
            "icon": "alcohol-shop",
            "owner": "Pernod Ricard"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.209939,
               57.483494
            ]
         },
         "properties": {
            "cartodb_id": 102,
            "name": "Macallan",
            "wikipedia": "https://en.wikipedia.org/wiki/The_Macallan_distillery",
            "homepage": "https://www.themacallan.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/8/8d/The_Macallan_Distillery.jpg",
            "founded": 1824,
            "status": "Operational",
            "number_of_stills": 10,
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "8, 10, 12, 15, 17, 18, 21, 25 and 30 years old",
            "cask_types": "Sherry",
            "abv": "",
            "region": "Speyside",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Edrington Group"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -3.62051,
               56.39595
            ]
         },
         "properties": {
            "cartodb_id": 145,
            "name": "Strathearn",
            "wikipedia": "",
            "homepage": "http://www.strathearndistillery.com/",
            "image": "http://www.whiskyintelligence.com/wp-content/uploads/2014/03/AA-strathearn2shot-1024x636.jpg",
            "founded": "2013",
            "status": "Operational",
            "number_of_stills": 2,
            "capacity_litres": 100000,
            "type": "Single Malt",
            "age": "",
            "cask_types": "Cherry, chestnut, mulberry",
            "abv": "",
            "region": "Highland",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Independent"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -2.985256,
               58.96345
            ]
         },
         "properties": {
            "cartodb_id": 109,
            "name": "Scapa",
            "wikipedia": "https://en.wikipedia.org/wiki/Scapa_distillery",
            "homepage": "http://www.scapamalt.com/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/f/f3/Scapa.jpg/250px-Scapa.jpg",
            "founded": 1885,
            "status": "Operational",
            "number_of_stills": 1,
            "capacity_litres": 1000000,
            "type": "Single Malt",
            "age": "14, 16 and 25 years old",
            "cask_types": null,
            "abv": null,
            "region": "Island",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Pernod Ricard"
         }
      },
      {
         "type": "Feature",
         "geometry": {
            "type": "Point",
            "coordinates": [
               -6.356556,
               57.30221
            ]
         },
         "properties": {
            "cartodb_id": 146,
            "name": "Talisker",
            "wikipedia": "https://en.wikipedia.org/wiki/Talisker_distillery",
            "homepage": "https://www.malts.com/en-row/home/",
            "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/8/89/Talisker_distillery_100212.jpg/300px-Talisker_distillery_100212.jpg",
            "founded": 1830,
            "status": "Active",
            "number_of_stills": 3,
            "capacity_litres": "",
            "type": "Single Malt",
            "age": "10, 12, 15, 18, 20, 25 and 30 years old",
            "cask_types": "",
            "abv": "",
            "region": "Island",
            "country": "Scotland",
            "open_to_public": "Yes",
            "icon": "alcohol-shop",
            "owner": "Diageo"
         }
      },
        {
            "type":"Feature",
            "geometry":{
                "type":"Point",
                "coordinates":[
                    -6.803976,
                    57.897603
            ]
        },
        "properties":{
            "cartodb_id":149,
            "name":"Isle of Harris Distillers",
            "wikipedia":null,
            "homepage":"http://www.harrisdistillery.com/",
            "image":"https://www.pressandjournal.co.uk/wp-content/uploads/sites/2/2019/06/RED_8052-558x372.jpg",
            "founded":2015,
            "status":"Operational",
            "number_of_stills":2,
            "capacity_litres":null,
            "type":null,
            "age":null,
            "cask_types":null,
            "abv":null,
            "region":"Island",
            "country":"Scotland",
            "open_to_public":"Yes",
            "owner":"Locally owned"
        }
    },
        {
            "type":"Feature",
            "geometry":{
                "type":"Point",
                "coordinates":[
                  -4.45586,
                  57.615144
             ]
        },
        "properties":{
            "cartodb_id":150,
            "name":"GlenWyvis",
            "wikipedia":null,
            "homepage":"https://glenwyvis.com/",
            "image":"http://www.crowdfunder.co.uk/uploads/projects/62232.jpg?v=1461575720",
            "founded":2016,
            "status":"Under construction",
            "number_of_stills":null,
            "capacity_litres":null,
            "type":null,
            "age":null,
            "cask_types":null,
            "abv":null,
            "region":"Highland",
            "country":"Scotland",
            "open_to_public":"No",
            "owner":null
        }
    }        
]
}
        }
                  
    );
    // Style map markers
    map.addLayer({
        "id": "distilleries",
        "type": "symbol",
        "source": "distilleries",
        "layout": {
            "icon-image": "circle-15"            
        }
    // This is the important part of this example: the addLayer
    // method takes 2 arguments: the layer as an object, and a string
    // representing another layer's name. if the other layer
    // exists in the stylesheet already, the new layer will be positioned
    // right before that layer in the stack, making it possible to put
    // 'overlays' anywhere in the layer stack.
    }, 'Country labels');
});
    
    // Hover event
    // Create a popup, but don't add it to the map yet.
var popup = new mapboxgl.Popup({
    closeButton: false,
    closeOnClick: false
});


    
    // Determine whisky region extents
document.getElementById('speyside').addEventListener('click', function() {
    map.fitBounds([[
        -3.8,
        57.75
    ], [
        -2.0,
        57.2
    ]]);
});
    
document.getElementById('campbeltown').addEventListener('click', function() {
    map.fitBounds([[
        -5.8,
        55.8
    ], [
        -5.4,
        55.23
    ]]);
});
    
document.getElementById('highland').addEventListener('click', function() {
    map.fitBounds([[
        -6.58,
        58.66
    ], [
        -1.65,
        55.73
    ]]);
});

document.getElementById('islands').addEventListener('click', function() {
    map.fitBounds([[
        0,
        59.5
    ], [
        -8.52,
        55.15
    ]]);
});

document.getElementById('islay').addEventListener('click', function() {
    map.fitBounds([[
        -6.55,
        55.97
    ], [
        -5.93,
        55.53
    ]]);
});
    
document.getElementById('lowland').addEventListener('click', function() {
    map.fitBounds([[
        -5.4,
        56.52
    ], [
        -1.8,
        54.60
    ]]);
});

// When a click event occurs near a place, open a popup at the location of
// the feature, with description HTML from its properties.
map.on('click', function (e) {
    var features = map.queryRenderedFeatures(e.point, { layers: ['distilleries'] });

    if (!features.length) {
        return;
    }

    var feature = features[0];

    var link = document.createElement('a');
    link.href = feature.properties.homepage;
    link.target = '_blank';
    link.textContent = feature.properties.name;

    
    // Use wrapped coordinates to ensure longitude is within (180, -180)
    var coords = feature.geometry.coordinates;
    var ll = new mapboxgl.LngLat(coords[0], coords[1]);
    var wrapped = ll.wrap();

    // info window style and data linkages
    
    var popup = new mapboxgl.Popup()
    popup.setLngLat(wrapped)
        .setHTML('<a href='+ feature.properties.homepage +' target=blank; class="popup-product-link"><img src="' + feature.properties.image +'" style="float:left;width:200px;height:128px;"><div class="popup-product-content" style="padding: 10px 5px 2px 10px;"></a><p class="popup-product-title" style="padding: 105px 0px 0px 0px;"><h2>' + feature.properties.name + '</h2></p><p class="popup-product-founded"><strong>Founded: </strong>' + feature.properties.founded + '</p><p class="popup-product-status"><strong>Status: </strong>' + feature.properties.status + '</p><p class="popup-product-type"><strong>Type: </strong>' + feature.properties.type + '</p><p class="popup-product-open"><strong>Open to the public: </strong>'+ feature.properties.open_to_public + '</p></div>')
        .addTo(map);
    
});

// Use the same approach as above to indicate that the symbols are clickable
// by changing the cursor style to 'pointer'.
map.on('mousemove', function (e) {
    var features = map.queryRenderedFeatures(e.point, { layers: ['distilleries'] });
    map.getCanvas().style.cursor = (features.length) ? 'pointer' : '';
});
    
</script>

</body>
</html>
