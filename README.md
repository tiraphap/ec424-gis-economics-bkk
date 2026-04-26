# EC424 — GIS สำหรับเศรษฐศาสตร์

**Workshop material** สำหรับวิชา EC424 — การใช้ภาพถ่ายดาวเทียม Landsat ตอบคำถามเชิงเศรษฐศาสตร์: การขยายตัวของเมือง การใช้ที่ดิน และการคาดคะเนอนาคต

**Case study:** กรุงเทพฯ + ปริมณฑล · เปรียบเทียบ LULC (Land Use / Land Cover) ปี 2015 vs 2025 + จำลองอนาคต 20 ปีด้วย CA-Markov

---

## 📂 ไฟล์ในโปรเจกต์

| ไฟล์ | คำอธิบาย |
|------|---------|
| [`ec424-gis-economics-bkk.ipynb`](ec424-gis-economics-bkk.ipynb) | Jupyter notebook หลัก — Random Forest classification + CA-Markov simulation |
| [`slides.html`](slides.html) | Reveal.js slides สำหรับการบรรยาย — มี interactive polls |

---

## 🚀 วิธีใช้

### Notebook (Google Colab)

1. เปิด [`ec424-gis-economics-bkk.ipynb`](ec424-gis-economics-bkk.ipynb) ใน Google Colab
2. รัน cells ทีละตัวจากบนลงล่าง
3. ใช้เวลา ~5-10 นาที (CPU เพียงพอ ไม่ต้องใช้ GPU)
4. ไม่ต้องสมัคร account อะไร — ใช้ **Microsoft Planetary Computer** (public API) สำหรับ Landsat data

### Slides

เปิด `slides.html` ใน browser (Chrome / Firefox / Edge) — กด `F` สำหรับ fullscreen

หรือเปิดผ่าน local server:
```bash
python -m http.server 8000
# แล้วเปิด http://localhost:8000/slides.html
```

**Keyboard shortcuts:**
- `→` / `←` เปลี่ยน slide
- `F` fullscreen · `S` speaker notes · `ESC` overview

---

## 📚 หัวข้อที่ครอบคลุม

1. **Spectral Signatures** — แต่ละวัตถุสะท้อนแสงต่างกันยังไง (lay foundation)
2. **NDVI / NDWI / NDBI** — ดัชนีสำหรับพืช / น้ำ / สิ่งก่อสร้าง
3. **Random Forest classification** — pseudo-label จาก spectral indices (ไม่ต้องเตรียม training data)
4. **LULC change analysis** — เปรียบเทียบพื้นที่ปี 2015 → 2025
5. **CA-Markov simulation** — จำลองอนาคต 20 ปีข้างหน้า
6. **Economic interpretation** — Urban sprawl, real estate, GDP proxy applications

---

## 🛠️ Stack

- **Microsoft Planetary Computer** (STAC API) — Landsat Collection 2 Level 2
- **rasterio / geopandas / shapely** — geospatial processing
- **scikit-learn** — Random Forest classifier
- **matplotlib** — visualization

ทั้งหมดเป็น open-source · รันได้บน Colab ฟรี

---

## 🎓 Capstone Ideas

นักศึกษาสามารถต่อยอดได้:
- เปลี่ยน AOI เป็นจังหวัดอื่นในไทย
- วิเคราะห์ความสัมพันธ์ระหว่าง urban growth กับ GDP จังหวัด
- ใช้ NDVI timeseries ทำนายผลผลิตการเกษตร
- รวม LULC + DEM + ฝน → flood risk mapping

---

## 📖 อ้างอิง

- Henderson, Storeygard & Weil (2012). *"Measuring Economic Growth from Outer Space"*. American Economic Review.
- Donaldson & Storeygard (2016). *"The View from Above: Applications of Satellite Data in Economics"*. Journal of Economic Perspectives.
- Jensen, J.R. (2007). *Remote Sensing of the Environment: An Earth Resource Perspective*.

---

## 📜 License

[MIT](LICENSE) — ใช้/ดัดแปลง/แจกจ่ายได้อย่างเสรี

---

ผศ.ดร.ถิรภาพ ฟักทอง · คณะเศรษฐศาสตร์ มหาวิทยาลัยธรรมศาสตร์
