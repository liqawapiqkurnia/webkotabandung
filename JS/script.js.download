// Inisialisasi peta
const map = L.map('map').setView([-6.903, 107.6510], 13);

// Basemap
const basemapOSM = L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
    maxZoom: 19,
    attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>'
}).addTo(map);

const osmHOT = L.tileLayer('https://{s}.tile.openstreetmap.fr/hot/{z}/{x}/{y}.png', {
    maxZoom: 19,
    attribution: '© OpenStreetMap contributors, Tiles style by Humanitarian OpenStreetMap Team hosted by OpenStreetMap France'
});

const baseMapGoogle = L.tileLayer('https://{s}.google.com/vt/lyrs=m&x={x}&y={y}&z={z}', {
    maxZoom: 20,
    attribution: 'Map by <a href="https://maps.google.com/">Google</a>',
    subdomains: ['mt0', 'mt1', 'mt2', 'mt3']
});

// Tambahkan tombol fullscreen
map.addControl(new L.Control.Fullscreen());

// Simpan koordinat "Home"
const home = {
    lat: -6.903,
    lng: 107.6510,
    zoom: 13
};

// Tambahkan tombol "Home"
L.easyButton('fa-home', function(btn, map){
    map.setView([home.lat, home.lng], home.zoom);
}, 'Kembali ke Home').addTo(map);

// Tambahkan tombol "My Location"
L.control.locate({
    position: 'topleft',
    setView: 'once',
    flyTo: true,
    keepCurrentZoomLevel: false,
    showPopup: false,
    locateOptions: {
        enableHighAccuracy: true
    }
}).addTo(map);