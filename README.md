# spaceship-titanic-final

หลักการทำงานในแต่ละโมเดลทั้ง7
-RandomForestClassifier n_estimatorsint, default=100
  Random Forest คือการนำเอา Decision Tree มารวมกันหลายๆต้น แต่ละต้นทำนายผลลัพธ์ออกมา แล้วเปิดโหวตว่าควรจะเป็นคลาสไหน (เอาการตัดสินใจของโมเดลเหล่านั้นมาโหวตกันว่า Class ไหนถูกเลือกมากที่สุด)
  ![image](https://user-images.githubusercontent.com/78127819/198812660-80e2f2f8-b0ae-4b8b-81fd-1bcfddefaade.png)
  ![image](https://user-images.githubusercontent.com/78127819/198812666-169834f7-2741-4449-b04d-7d80e973f163.png)

-AdaBoostClassifier n_estimatorsint, default=50

  Boosting นำ Classifier หลายตัวมาทำงานเป็นโซ่ต่อกัน โดยแต่ละตัวจะแก้ไขจุดด้อยของ Classifier ตัวก่อนหน้า พอเทรนเสร็จแล้ว Classifier ทุกตัวจะพยากรณ์ร่วมกัน\
  หลักการทำงานของ AdaBoost คือการใช้ Classifier ที่ไม่ซับซ้อน เช่น Decision tree ที่มีชั้นเดียว (เรียกว่า Decision stump) หลายๆ Instance มาเทรนต่อกันเป็นลูกโซ่ โดยในการเทรนแต่ละรอบจะมีการกำหนดค่าน้ำหนักของข้อมูลแต่ละรายการ Classifier instance จะเรียนรู้จากค่าน้ำหนักเหล่านั้น โดยถ้าพยากรณ์ผิด ค่าน้ำหนักของรายการนั้นจะมีค่ามากขึ้น ส่งผลให้ Classifier instance นั้นได้รับ "คะแนน" ต่ำ แต่ในทางกลับกัน ถ้า Instance ไหนพยากรณ์ถูกเป็นสัดส่วนที่มาก ก็จะได้คะแนนมาก
การพยากรณ์ของ AdaBoost คือการถ่วงคะแนนเข้ากับคำตอบของแต่ละ Instance แล้วเลือกคำตอบจาก Class ที่ได้รวมแล้วได้ค่าน้ำหนักมากที่สุด
  ![image](https://user-images.githubusercontent.com/78127819/198813303-700582e9-a29b-431d-8568-560a6766519c.png)
 
-LGBMClassifier  
 ![image](https://user-images.githubusercontent.com/78127819/198814383-f432771d-a685-42a8-8caa-d626c9d61bf7.png)

-XGBClassifier
กลับมาที่ XGB ของเราต่อดีกว่า สำหรับเจ้าตัวโมเดลนี้ก็ถูกแต่งเสริมเติมแต่งจาก Gradient boosting ดังนี้

Regularization: สามารถลดการเกิด overfit ได้
Sparse Aware: สามารถจัดการกับ missing value อัตโนมัติ
Parallelization: สามารถทำงานแบบขนานกับจำนวน core ของ cpu ได้
Cache Optimization: ใช้ hardware อย่างมีประสิทธิภาพ

-CatBoostClassifier
![image](https://user-images.githubusercontent.com/78127819/198815074-6a7fd167-1132-4855-827e-36a44fa29865.png)

-KNeighborsClassifier
![image](https://user-images.githubusercontent.com/78127819/198814506-55b29a5a-44bb-421b-975c-42e60eeac4d4.png)
![image](https://user-images.githubusercontent.com/78127819/198814514-c5c05f8f-53df-4d13-a80c-69a8839b2014.png)
![image](https://user-images.githubusercontent.com/78127819/198814525-9134a20f-ff2b-49b2-ba44-ed0fc447fc01.png)

-DecisionTreeClassifier
 
 อธิบายแบบกระชับของ medium
 ![image](https://user-images.githubusercontent.com/78127819/198814642-d5c832ed-f548-4fae-aec6-eee156ef123b.png)

