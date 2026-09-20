# Like, Scroll, and Stress: The Screen Time vs Mental Health

## Introduction
ผลกระทบของโซเชียลมีเดียต่อสุขภาพจิตเป็นประเด็นที่ได้รับความสนใจเพิ่มขึ้นต่อเนื่องตั้งแต่ปี 2023 เมื่อสำนักงานศัลยแพทย์ใหญ่แห่งสหรัฐฯ ประกาศให้เป็นปัญหาสาธารณสุขเร่งด่วน (Office of the Surgeon General, 2023) ผลสำรวจในปี 2025 พบว่าผู้ใช้กว่า 37% รู้สึกว่าโซเชียลมีเดียส่งผลเชิงลบต่อสุขภาพจิตของตน (Statista, 2025) และงานวิจัยในต้นปี 2026 ยังคงยืนยันความสัมพันธ์ระหว่างการใช้งานมากเกินไปกับผลลัพธ์ด้านสุขภาพจิตที่แย่ลง (PubMed, 2026)

อย่างไรก็ตาม งานวิจัยกลางปี 2026 เริ่มชี้ว่าปัจจัยสำคัญไม่ใช่ระยะเวลาการใช้งานโดยรวม แต่เป็นพฤติกรรมการใช้งาน เช่น การเลื่อนดูเนื้อหาแบบไม่มีที่สิ้นสุด (Mental Momentum Research, 2026) โดยกลุ่มวัยหนุ่มสาว (18-34 ปี) มีคะแนนสุขภาพจิตต่ำกว่าผู้สูงวัยอย่างชัดเจน (Sapien Labs, 2025-2026) ขณะที่งานวิเคราะห์ล่าสุดในเดือนสิงหาคม 2026 ก็ยอมรับว่าโซเชียลมีเดียมีทั้งประโยชน์และโทษควบคู่กัน (Worldatnet, 2026)

จากบริบทนี้ การศึกษาความสัมพันธ์ระหว่างพฤติกรรมการใช้โซเชียลมีเดีย การนอนหลับ ความเครียด และสุขภาพจิตของนักเรียนนักศึกษา จึงมีความสำคัญในการหาปัจจัยที่แท้จริงที่ส่งผลต่อสุขภาวะ เพื่อนำไปสู่แนวทางแก้ไขที่ตรงจุด
## initial question
ในปัจจุบัน มีการใช้งานโซเชียลมีเดียจำนวนมากและหลายภาคส่วนเริ่มกังวลถึงผลกระทบจากการใช้งานที่มากเกินไป เช่นในกรณีของหลายประเทศ ที่เริ่มมีการแบนหรือจำกัดการใช้งานสมาร์ทโฟนในโรงเรียนดังเนื้อหาส่วนหนึ่งในข่าวที่ระบุไว้ว่า  ['social media environments can expose young people, particularly girls, to risks such as harassment, unrealistic social pressures and harmful content'](https://www.unesco.org/gem-report/en/articles/how-many-countries-have-phone-bans-school) พวกเราจึงมีการตั้งข้อสงสัยว่าจริงๆแล้วการใช้โซเชียลมีเดียเป็นปริมาณแค่ไหน ถึงจะเรียกว่ากำลังพอดี ซึ่งคำถามแรกๆที่เราสงสัยจากข้อมูลที่ได้ประกอบด้วย

- ระยะเวลาในการใช้โซเซียลต่อวันมีผลอย่างไรต่อสุขภาพจิต ความเครียด และผลการเรียน
- แต่ละช่วงวัยมีพฤติกรรมอย่างไรในการเล่นอินเตอร์เน็ต
- ระดับการศึกษามีผลต่อการชั่วโมงการเล่นโซเซียลไหม
- การเล่นโซเซียลที่มากอาจทำให้นอนดึกและมีช่วงการนอนน้อยและอาจส่งผลต่อสุขภาพจิต
- ผู้หญิงและผู้ชายอาจมีพฤติกรรมการใช้งานโซเชียลมีเดียที่ต่างกัน และอาจมี mental health ที่แตกต่างกัน

## Data Scope
โปรเจกต์นี้ใช้ชุดข้อมูล [Impact of Social Media on Life](https://www.kaggle.com/datasets/harishyadav0506/impact-of-social-media-on-life) จากเว็บไซต์ Kaggle ซึ่งเก็บข้อมูลจากกลุ่มนักเรียนและนักศึกษาในปีค.ศ. 2026 จำนวน 4,500 คน ในช่วงอายุตั้งแต่ 15-26 ปี โดยข้อมูลที่ใช้ในโปรเจกต์ จะมีหัวข้อดังนี้

Late_Night_Usage	Social_Comparison_Frequency	Perceived_Stress_Score	Mental_Health_Index	Academic_Performance_GPA	Overall_Impact

- **ข้อมูลประชากร (Demographics):**
  - อายุ (Age)
  - เพศ (Gender)
  - ระดับการศึกษา (Academic Level); อุดมศึกษา (High School), ปริญญาตรี (Undergraduate) และปริญญาโท (Postgraduate)
- **ตัวชี้วัดการใช้งาน (Usage Metrics):**
  - ประเภทแพลตฟอร์ม (Primary Platform)
  - จำนวนชั่วโมงที่ใช้โซเชียลต่อวัน (Daily Usage Hours)
- **ตัวชี้วัดสุขภาพจิต (Health & Psychometrics):**
  - จำนวนชั่วโมงการนอน (Sleep Duration Hours)
  - คะแนนคุณภาพการนอน 1-5 (Sleep Quality Score)๖Subjective sleep quality score (1–5), late-night scrolling indicators, Perceived Stress Scale (PSS: 0–40), and composite Mental Health Index (10–98).
Academic & Outcome: Cumulative GPA and multi-factor classification label (Overall_Impact: Beneficial, Neutral, Negative).
