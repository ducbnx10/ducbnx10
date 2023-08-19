var duongVaVatThe = {
    "đường bộ": [
        { tocDoGioiHan: 20, vatThe: "Người đi bộ" },
        { tocDoGioiHan: 60, vatThe: "Xe đạp" },
        { tocDoGioiHan: 120, vatThe: "Ô tô" },
        { tocDoGioiHan: 150, vatThe: "Xe tải hoặc xe khách" }
    ],
    "đường thuỷ": [
        { tocDoGioiHan: 10, vatThe: "Thuyền buồm" },
        { tocDoGioiHan: 60, vatThe: "Thuyền chạy động cơ" },
        { tocDoGioiHan: 100, vatThe: "Tàu điện ngầm" },
        { tocDoGioiHan: 150, vatThe: "Tàu biển" }
    ],
    "đường không": [
        { tocDoGioiHan: 300, vatThe: "Máy bay trực thăng" },
        { tocDoGioiHan: 800, vatThe: "Máy bay phản lực" }
    ]
};

var loaiDuong = "đường bộ";
var tocDo = 500; // km/h

var vatThe = "Không xác định vật thể";

if (duongVaVatThe[loaiDuong]) {
    for (var i = 0; i < duongVaVatThe[loaiDuong].length; i++) {
        if (tocDo <= duongVaVatThe[loaiDuong][i].tocDoGioiHan) {
            vatThe = duongVaVatThe[loaiDuong][i].vatThe;
            break;
        }
    }
}

console.log("Vật thể trên " + loaiDuong + " với tốc độ " + tocDo + " km/h là: " + vatThe);
