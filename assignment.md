/assignment "Using Remote Repository"
type: link

---

- ในขั้นตอนด้านล่างต่อไปนี้ เราจะจำลองการทำงานเป็นทีมโดยสมมุติให้ Developer คนแรกแทนด้วย Dev 1 คนที่สองแทนด้วย Dev 2 และถ้ามีคนที่สามให้แทนด้วย Dev 3
- ให้เลือกกันในทีมได้เลยว่าใครจะเล่นบทบาทสมมุติเป็น **Dev 1, Dev 2 หรือ** ถ้ามี **Dev 3**
- เมื่อทำเสร็จทุก Exercise แล้วให้**ส่ง URL ของ Remote repository ใน Input ด้านล่าง**
  - URL ของ Remote repository คือ URL ที่เราใช้เข้า Github ของ Repo บน Web Browser

## Exercise #1 : Initializing Repository

- ให้นึกภาพสถานการณ์ตามว่าทีมเราได้รับมอบหมายให้พัฒนาเว็บไซต์ขึ้นมา 1 เว็บไซต์
- ซึ่งเป็นเว็บไซต์ที่เกี่ยวกับการหาบ้านให้กับสัตว์เลี้ยง โดยจะต้องมีการเก็บข้อมูลสัตว์เลี้ยงและผู้ใช้งานที่มาลงทะเบียน
- ขั้นตอนด้านล่างต่อไปนี้ **Dev 1 เป็นคนทำทั้งหมด**

  1. สร้างโฟลเดอร์ใหม่ชื่อว่า `pet-adoption-website` ลงไปใน PWD
  2. Initialize ตัว `pet-adoption-website` ให้เป็น Repository
  3. สร้างไฟล์ชื่อว่า `pet-profile-page.html` และ `user-profile-page.html` แล้วเขียนโค้ด HTML ตามด้านล่าง

     - โค้ดในไฟล์ `pet-profile-page.html` จะต้องมีดังนี้

       ***

         <h1>Pet profile page</h1>
         <h3>Pet_1</h3>
         <p>Petname: Bobo</p>
         <p>Type: Dog</p>
         <p>Age: 4</p>

     - โค้ดในไฟล์ `user-profile-page.html` จะต้องมีดังนี้

       ***

         <h1>User profile page</h1>
         <h3>User_1</h3>
         <p>Username: John</p>
         <p>Job: Developer</p>
         <p>Age: 28</p>

     - เมื่อทำเสร็จให้บันทึกไฟล์ให้เรียบร้อย แล้วสั่งให้ Git แสดงไฟล์ที่เปลี่ยนแปลงออกมาในหน้า Shell จากนั้นจะเห็นว่าไฟล์ `pet-profile-page.html` และ `user-profile-page.html` มีการแก้ไข

  4. เพิ่มไฟล์ `pet-profile-page.html` และ `user-profile-page.html` เข้าไปใน Staging area จากนั้นให้ลองตรวจสอบว่าทั้งสองไฟล์เข้าไปอยู่ใน Staging Area แล้วหรือไม่
  5. Commit ตัวไฟล์ที่อยู่ใน Staging Area เข้าไปใน Repository
  6. สร้าง Remote Repository บน Github
  7. เชื่อม Local Repository เข้ากับ Remote Repository ที่สร้างบน Github ในขั้นตอนที่ 6
  8. ให้ Push ตัว Branch `main` ของ Local Repository ไปยัง Remote repository ที่สร้างไว้ก่อนหน้านี้
  9. สุดท้าย ให้ไปเพิ่ม Dev 2 และ Dev 3 เป็น Collaborator ของ Repository บน Github

## Exercise #2 : Pushing Feature Branch to Remote Repository

- ขั้นตอนด้านล่างต่อไปนี้ **Dev 2 เป็นคนทำทั้งหมด**
  - สถานการณ์คือ **Dev 2** กำลังจะพัฒนา Feature ของตัวเองที่ได้รับมอบหมาย
  - Feature ที่ได้รับมอบหมายคือ การแก้ไขข้อมูลสัตว์เลี้ยงบนหน้าเว็บไซต์บน Repository เดียวกันกับ Dev 1

1. ให้ Clone ตัว Repository ที่ Dev 1 สร้างไว้ลงมาบนเครื่องของตัวเอง
2. จากนั้นสร้าง Branch ชื่อว่า `feature/pet-profile-page` จากนั้นให้เข้าไปแก้ไขข้อมูลสัตว์เลี้ยงในไฟล์ที่ชื่อว่า `pet-profile-page.html` เขียนโค้ด HTML เพิ่มเติม ==bในส่วนที่ Highlight สีฟ้า)== ดังนี้

   highlight: blue[6-9]

   ***

   <h1>Pet profile page</h1>
   <h3>Pet_1</h3>
   <p>Petname: Bobo</p>
   <p>Type: Dog</p>
   <p>Age: 4</p>
   <h3>Pet_2</h3>
   <p>Petname: Khaopad</p>
   <p>Type: Cat</p>
   <p>Age: 3</p>

3. จากนั้นให้ Commit แล้ว Push ตัว Branch `feature/pet-profile-page` ขึ้นไปบน Remote Repository ให้เรียบร้อย

## Exercise #3 : Pushing Feature Branch to Remote Repository

- ขั้นตอนด้านล่างต่อไปนี้ **Dev 3 เป็นคนทำทั้งหมด** (ถ้าไม่มี Dev 3 ให้ข้ามไปทำ Exercise #4 ได้เลย)

  - สถานการณ์คือ **Dev 3** กำลังจะพัฒนา Feature ของตัวเองที่ได้รับมอบหมาย
  - Feature ที่ได้รับมอบหมายคือ การแก้ไขข้อมูลผู้ใช้งานที่มาลงทะเบียนหาบ้านให้สัตว์เลี้ยงบนหน้าเว็บไซต์บน Repository เดียวกันกับ Dev 1 และ Dev 2

    1. ให้ Dev 3 Clone ตัว Repository ที่ Dev 1 สร้างไว้ลงมาบนเครื่องของตัวเอง
    2. ให้ Dev 3 สร้าง Branch ชื่อว่า `feature/user-profile-page` จากนั้นให้เข้าไปแก้ไขข้อมูลผู้ใช้งานในไฟล์ที่ชื่อว่า `user-profile-page.html` เขียนโค้ด HTML เพิ่มเติม ==b(ในส่วนที่ Highlight สีฟ้า)== ดังนี้

       highlight: blue[6-9]

       ***

       <h1>User profile page</h1>
       <h3>User_1</h3>
       <p>Username: John</p>
       <p>Job: Developer</p>
       <p>Age: 28</p>
       <h3>User_2</h3>
       <p>Username: Nadia</p>
       <p>Job: Teacher</p>
       <p>Age: 30</p>

    3. จากนั้นให้ Commit แล้ว Push ตัว Branch `feature/user-profile-page` ขึ้นไปบน Remote Repository ให้เรียบร้อย

## Exercise #4 : Fixing Code on Main Branch

- ขั้นตอนด้านล่างต่อไปนี้ **Dev 1 เป็นคนทำทั้งหมด**
  - สถานการณ์คือให้ Dev 1 เข้าไปแก้ไขข้อมูลผู้ใช้งานและข้อมูลสัตว์เลี้ยงบน Branch main

1. Dev 1 เข้าไปแก้ไขข้อมูลสัตว์เลี้ยงในไฟล์ที่ชื่อว่า `pet-profile-page.html` เขียนโค้ด HTML เพิ่มเติม ==b(ในส่วนที่ Highlight สีฟ้า)== ดังนี้

   highlight: blue[6-9]

   ***

   <h1>Pet profile page</h1>
   <h3>Pet_1</h3>
   <p>Petname: Bobo</p>
   <p>Type: Dog</p>
   <p>Age: 4</p>
   <h3>Pet_2</h3>
   <p>Petname: Khaotom</p>
   <p>Type: Cat</p>
   <p>Age: 4</p>

2. Dev 1 เข้าไปแก้ไขข้อมูลสัตว์เลี้ยงในไฟล์ที่ชื่อว่า `user-profile-page.html` เขียนโค้ด HTML เพิ่มเติม ==b(ในส่วนที่ Highlight สีฟ้า)== ดังนี้

   highlight: blue[6-9]

   ***

   <h1>User profile page</h1>
   <h3>User_1</h3>
   <p>Username: John</p>
   <p>Job: Developer</p>
   <p>Age: 28</p>
   <h3>User_2</h3>
   <p>Username: Robert</p>
   <p>Job: Doctor</p>
   <p>Age: 26</p>

3. ให้ Dev 1 ทำการ Commit และ Push การแก้ไขบน Branch main ขึ้นไปบน Remote Repository ให้เรียบร้อย

## Exercise #5 : Fetching and Pulling the Code from Remote Repo

- ขั้นตอนด้านล่างต่อไปนี้ให้ในทีมช่วยกันทำ
  /accordion "ถ้าทีมมี 3 คน ให้ดูตามขั้นตอนนี้ (Dev 1, Dev 2, Dev 3)"

  1. ให้ **Dev 1** ลอง Fetch เพื่อดูการแก้ไขที่เกิดขึ้นบน Remote Repository

  - Dev 1 จะสังเกตเห็นว่ามี Branch ถูกเพิ่มเข้ามาใน Git history ดังนี้
  - Branch `feature/pet-profile-page` ที่ถูกสร้างขึ้นโดย Dev 2
  - Branch `feature/user-profile-page` ที่ถูกสร้างขึ้นโดย Dev 3

  2. ต่อมาให้ **Dev 2** ลอง Fetch เพื่อดูการแก้ไขที่เกิดขึ้นบน Remote Repository

  - Dev 2 สามารถสังเกตเห็นการเปลี่ยนแปลงบน Git history ดังนี้
  - Branch `feature/user-profile-page` ที่ถูกสร้างขึ้นโดย Dev 3 ถูกเพิ่มเข้ามาใน Git history
  - Branch main จะมี Commit เพิ่มขึ้นมา 1 Commit จากการแก้ไขโค้ดของ Dev 1

  3. จากนั้นให้ **Dev 3** ลอง Fetch เพื่อดูการแก้ไขที่เกิดขึ้นบน Remote Repository

  - Dev 3 สามารถสังเกตเห็นการเปลี่ยนแปลงบน Git history ดังนี้
  - Branch `feature/pet-profile-page` ที่ถูกสร้างขึ้นโดย Dev 2 ถูกเพิ่มเข้ามาใน Git history
  - Branch main จะมี Commit เพิ่มขึ้นมา 1 Commit จากการแก้ไขโค้ดของ Dev 1

  4. จากนั้นให้ Dev 1, Dev 2 และ Dev 3 Pull โค้ดจาก Remote Repository ลงมาบน Local Repository ของตัวเอง

  - จากขั้นตอนทั้งหมดจะสังเกตได้ว่าหลังจากที่ทุกคน Fetch และ Pull โค้ดเรียบร้อยแล้ว **ไม่มี Conflict เกิดขึ้น** ทั้งๆที่เรามีการแก้ไขโค้ดที่เหมือนกันดังนี้
  - Dev 1 และ Dev 2 แก้ไขโค้ดในไฟล์ `pet-profile-page.html` ที่บรรทัดเดียวกัน
  - Dev 1 และ Dev 3 แก้ไขโค้ดในไฟล์ `user-profile-page.html` ที่บรรทัดเดียวกัน
  - ซึ่งสาเหตุที่ Conflict ไม่เกิดขึ้นเนื่องจาก
  - การเปลี่ยนแปลงของโค้ดที่เกิดจาก Dev 1, Dev 2 และ Dev 3 จะ**เกิดขึ้นคนละ Branch**
  - จึงทำให้การแก้ไขโค้ดของ Dev ทุกคนไม่ส่งผลกระทบต่อกัน ตัว Conflict จึงไม่เกิดขึ้นนั่นเอง
    /accordion

  /accordion "ถ้าทีมมี 2 คน ให้ดูตามขั้นตอนนี้ (Dev 1, Dev 2)"

  1. ให้ **Dev 1** ลอง Fetch เพื่อดูการแก้ไขที่เกิดขึ้นบน Remote Repository

  - Dev 1 จะสังเกตเห็นว่ามี Branch ถูกเพิ่มเข้ามาใน Git history ดังนี้
  - Branch `feature/pet-profile-page` ที่ถูกสร้างขึ้นโดย Dev 2

  2. ต่อมาให้ **Dev 2** ลอง Fetch เพื่อดูการแก้ไขที่เกิดขึ้นบน Remote Repository

  - Dev 2 สามารถสังเกตเห็นการเปลี่ยนแปลงบน Git history ดังนี้
  - Branch `main` จะมี Commit เพิ่มขึ้นมา 1 Commit จากการแก้ไขโค้ดของ Dev 1

  3. จากนั้นให้ Dev 1 และ Dev 2 Pull โค้ดจาก Remote Repository ลงมาบน Local Repository ของตัวเอง

  - จากขั้นตอนทั้งหมดจะสังเกตได้ว่าหลังจากที่ทุกคน Fetch และ Pull โค้ดเรียบร้อยแล้ว **ไม่มี Conflict เกิดขึ้น** ทั้งๆ ที่เรามีการแก้ไขโค้ดที่เหมือนกันคือ
  - Dev 1 และ Dev 2 แก้ไขโค้ดในไฟล์ `pet-profile-page.html` ที่บรรทัดเดียวกัน
  - ซึ่งสาเหตุที่ Conflict ไม่เกิดขึ้นเนื่องจาก
  - การเปลี่ยนแปลงของโค้ดที่เกิดจาก Dev 1 และ Dev 2 **เกิดขึ้นคนละ Branch**
  - จึงทำให้การแก้ไขโค้ดของ Dev ทุกคนไม่ส่งผลกระทบต่อกัน ตัว Conflict จึงไม่เกิดขึ้นนั่นเอง
    /accordion

## Exercise #6 : Merging to Main Branch

- ขั้นตอนด้านล่างต่อไปนี้ให้ **Dev 1 และ Dev 2 ช่วยกันทำ**
  - สถานการณ์คือ Dev 2 ต้องการที่จะรวมโค้ดใน Branch `feature/pet-profile-page` ของเราเอง กลับเข้าไปยัง Branch `main`

1. ให้ Dev 2 ทำการ Checkout ไปที่ Branch `main` และ Merge ตัว Branch `feature/pet-profile-page` เข้าไปยัง Branch `main`
2. จะสังเกตได้ว่าขั้นตอนการ Merge มี Conflict เกิดขึ้น เนื่องจากการแก้ไขโค้ดที่ไฟล์เดียวกัน จะถูกรวมเข้าด้วยกัน
   - ให้ Dev 1 และ Dev 2 ช่วยกันแก้ไข Conflict ให้ตกลงกันว่าอยากใช้โค้ดที่ใครเป็นคนเขียนขึ้นมา
   - ตัวอย่างการแก้ไข Merge Conflict สามารถดูได้[จากลิงก์นี้](https://youtu.be/fDziQGcL94A)
3. หลังจากที่ Dev 2 ได้ Merge โค้ดเสร็จเรียบร้อย ให้ Push Branch main ขึ้นไปบน Remote Repo
4. จากนั้นให้ Dev 1 และ Dev 3 (ถ้ามี) ลอง Fetch และ Pull โค้ดล่าสุดบน Remote Repo จะเห็นได้ว่า Branch `feature/pet-profile-page` ถูก Merge เข้าไปยัง Branch`main`เรียบร้อย

## Exercise #7 : Merging to Main Branch

- ถ้าทีมมีแค่ 2 คน ไม่ต้องทำ Exercise ข้อนี้
- ขั้นตอนด้านล่างต่อไปนี้ให้ **Dev 1 และ Dev 3 ช่วยกันทำ**
  - สถานการณ์คือ Dev 3 ต้องการที่จะรวมโค้ดใน Branch `feature/user-profile-page` ของเราเอง กลับเข้าไปยัง Branch `main`

1. ให้ Dev 3 ทำการ Checkout ไปที่ Branch `main` และ Merge ตัว Branch `feature/user-profile-page` เข้าไปยัง Branch `main`
2. จะสังเกตได้ว่าขั้นตอนการ Merge มี Conflict เกิดขึ้น เนื่องจากการแก้ไขโค้ดที่ไฟล์เดียวกัน จะถูกรวมเข้าด้วยกัน
   - ให้ Dev 1 และ Dev 3 ช่วยกันแก้ไข Conflict ให้ตกลงกันว่าอยากใช้โค้ดที่ใครเป็นคนเขียนขึ้นมา
   - ตัวอย่างการแก้ไข Merge Conflict สามารถดูได้[จากลิงก์นี้](https://youtu.be/fDziQGcL94A)
3. หลังจากที่ Dev 3 ได้ Merge เสร็จเรียบร้อย ให้ Push Branch `main` ขึ้นไปบน Remote Repo
4. จากนั้นให้ Dev 1 และ Dev 2 ลอง Fetch และ Pull โค้ดล่าสุดบน Remote Repo จะเห็นได้ว่า Branch `feature/user-profile-page` ถูก Merge เข้าไปยัง Branch main เรียบร้อย
   /assignment
