---
created: 2026-02-09T21:21
updated: 2026-02-10T15:22
---
# 🛰️ Weekly Tactical Dashboard: Week {{date:ww}}

> [!info]+ **Commander’s Intent**
> Data is grouped into narrow panels for mobile visibility. This report reconciles clinical hardware stats with identity-based "Sovereignty" metrics.


---

## 📈 1. Hardware Status (The Physical System)
> [!abstract]+ **Intelligence Brief: Somatic & Energy**
```dataview
TABLE WITHOUT ID
    link(file.link, dateformat(date, "ccc")) AS "Day",
    physical_battery AS "Batt", 
    sleep_quality AS "Sleep",
    somatic_status AS "Status"
FROM "Bunker Reports"
WHERE date >= date(today) - dur(7 days)
SORT date ASC
```

---

## 🦴 2. Hardware Error Codes (Somatic Load)
> [!danger]+ **Intelligence Brief: Specific Interference**
> *Tracking the frequency of specific CKD/RTA symptoms.*
```dataview
TABLE WITHOUT ID
    link(file.link, dateformat(date, "ccc")) AS "Day",
    symptom_battle_ax AS "Ax",
    symptom_ice_water AS "Ice",-
    symptom_acidosis_weight AS "Heavy",
    symptom_system_lag AS "Lag"
FROM "Bunker Reports"
WHERE date >= date(today) - dur(7 days)
SORT date ASC
```

---

## 🧠 3. Cognitive & Autonomic Defense
> [!brain]+ **Intelligence Brief: Neuro-Psych Load**
```dataview
TABLE WITHOUT ID
    link(file.link, dateformat(date, "ccc")) AS "Day",
    cognitive_fog AS "Fog", 
    snhl_strain AS "SNHL",
    masking_effort AS "Mask",
    window_zone AS "Window",
    autonomic_signature AS "State"
FROM "Bunker Reports"
WHERE date >= date(today) - dur(7 days)
SORT date ASC
```

---

## 🛡️ 4. Sovereignty & Identity (Integrity Audit)
> [!shield]+ **Intelligence Brief: Role & Armor Trace**
```dataview
TABLE WITHOUT ID
    link(file.link, dateformat(date, "ccc")) AS "Day",
    armor_status AS "Armor",
    role_played AS "Role",
    utility_guilt AS "Guilt",
    mirror_narrative AS "Mirror"
FROM "Bunker Reports"
WHERE date >= date(today) - dur(7 days)
SORT date ASC
```

---

## 🌪️ 5. Environmental Friction (Friction Check)
> [!warning]+ **Intelligence Brief: External Stressors**
```dataview
TABLE WITHOUT ID
    link(file.link, dateformat(date, "ccc")) AS "Day",
    acoustic_load AS "Sound",
    thermal_load AS "Temp",
    gravity_load AS "Surface",
    social_load AS "Social"
FROM "Bunker Reports"
WHERE date >= date(today) - dur(7 days)
SORT date ASC
```

---

## 🥤 6. Protocol Sync (Guava Logs)
> [!check]+ **Intelligence Brief: Guava Compliance**
```dataview
TABLE WITHOUT ID
    link(file.link, dateformat(date, "ccc")) AS "Day",
    choice(guava_morning_sync = true, "✔️", "❌") AS "AM",
    choice(quava_night_sync = true, "✔️", "❌") AS "PM"
FROM "Bunker Reports"
WHERE date >= date(today) - dur(7 days)
SORT date ASC
```

---

## ✨ 7. Safety & Agency (The Evidence)
> [!success]+ **Intelligence Brief: Reclaimed Victories**
```dataview
TABLE WITHOUT ID
    link(file.link, dateformat(date, "ccc")) AS "Day",
    (default(Glimmer, "") + " " + default(Provision, "") + " " + default(Legacy, "")) AS "Evidence"
FROM "Bunker Reports"
WHERE date >= date(today) - dur(7 days)
WHERE Glimmer != null OR Provision != null OR Legacy != null
SORT date ASC
```

---

## 🎯 8. Tactical Adjustments
**Commander's Pivot:**
> 

---

#links
[[Bunker Log Archive]] | [[Vagal Reset Protocols]]


### **1. Hardware Trend Analysis (The Big Picture)**

#### **Mobility Trend:**
- [ ] Improved
- [ ] Stable
- [ ] Declining

#### **Cognitive Clarity:**
- [ ] Clear / High Focus
- [ ] Average / Standard Fog
- [ ] High Fog / Processing Delays

#### **Sleep Quality:**
- [ ] Restorative
- [ ] Fragmented
- [ ] Non-Existent

#### **Medication Efficacy:**
- [ ] Meds holding the line
- [ ] Breakthrough symptoms occurring
- [ ] Flares out-pacing the protocol
### **2. System Load Recap (Primary Drains)**
*Identify which fronts cost the most energy this week:*

- [ ] Social Masking (High performance cost)
- [ ] Physical Labor (Exceeded hardware limits)
- [ ] Cognitive Load (Heavy mental lifting)
- [ ] Symptom Management (Fighting active flares)
- [ ] Emotional Resilience (Defending against PsyOps)
- [ ] Administrative Burden (Medical/Brand logistics)

### **3. Strategic Intelligence (Post-Mortem)**

#### **Flare-Up Analysis:**
*If there was a system crash this week, what was the likely trigger?*
> 

#### **Supply & Logistics Check:**
*Are meds/supplies stocked for next week? List upcoming specialist appointments or needs:*
> 

#### **The Sovereign Win:**
*What was the biggest victory where you prioritized "The Man" over "The Brand" or the illness?*
>

### **4. Operational Forecast (Next 7 Days)**
*Set the tactical stance for the upcoming week based on current battery levels:*

- [ ] **DEFCON 5 (Normal Readiness):** Battery is high. Focus on "Brand" growth, complex projects, and social expansion.
- [ ] **DEFCON 4 (Increased Watch):** Stable but cautious. Proceed with standard tasks but monitor "System Load" closely.
- [ ] **DEFCON 3 (Round-the-Clock Ops):** Holding the line. Maintain current routines only; no new "Heavy Lifting" or extra social commitments.
- [ ] **DEFCON 2 (High Readiness):** Strategic withdrawal. Symptoms are winning; cancel non-essential tasks and prioritize "Hardware" stability.
- [ ] **DEFCON 1 (Maximum Readiness):** Full Bunker Status. Total hardware failure or mental burnout. Focus is 100% on survival and recovery.