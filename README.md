# Vehicle Motion Analysis – ENEL 862 Project  

## 📌 Project Overview  
This project analyzes the motion of a **Honda CR-V (1998 model)** as it moves across a parking lot and over a speed bump. Using **video analysis techniques in MATLAB**, the study estimates the vehicle’s speed, wheel displacement, body movement, and the effect of passenger load on suspension response.  

Three sets of videos were analyzed:  
- **No bump**  
- **Small bump**  
- **Large bump**  
Each set includes five trials with increasing numbers of passengers (1–5).  

The goal was to extract as much quantitative information as possible about the CR-V’s motion from video data.  

---

## ⚙️ Methodology  
1. **Pixel-to-Centimeter Conversion**  
   - Vehicle length (front light → rear tire) was measured in pixels.  
   - Real-world length was obtained from manufacturer specifications.  
   - Conversion ratio: **~1.25 cm/pixel**.  

2. **Speed Estimation**  
   - Rear tire tracked across frames.  
   - Instantaneous speed calculated from displacement vs. time.  
   - Average speed ≈ **181.2 cm/s**.  

3. **Wheel & Body Displacement**  
   - Applied **Hough Transform** to detect circles (lights, wheels).  
   - Wheel vertical movement ≈ **7.67 cm**.  
   - Body vertical movement ≈ **1.25 cm**.  

4. **Speed Bump Height Estimation**  
   - Estimated from wheel displacement – body displacement.  
   - Speed bump height ≈ **6.41 cm**.  

5. **Passenger Load Effect**  
   - More riders → increased suspension compression.  
   - Wheel displacement changed slightly.  
   - Body displacement increased more significantly with passenger count.  

---

## 📊 Results Summary  
- **Pixel-to-cm ratio:** ~1.25 cm/pixel  
- **Average speed:** 181.2 cm/s  
- **Wheel displacement (vertical):** 7.67 cm  
- **Body displacement (vertical):** 1.25 cm  
- **Speed bump height:** 6.41 cm  
- **Passenger effect:** Higher load → more body displacement  

---

## 🛠️ Tools & Techniques  
- **MATLAB** (video processing, Hough Transform, motion analysis)  
- **Image cropping** to reduce background noise  
- **Circle detection** for feature localization (lights, wheels)  
- **Graphing** instantaneous velocity over time  

