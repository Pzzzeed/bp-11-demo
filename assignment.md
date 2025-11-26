นขั้นตอนด้านล่างต่อไปนี้ เราจะจำลองการทำงานเป็นทีมโดยสมมุติให้ Developer คนแรกแทนด้วย Dev 1 คนที่สองแทนด้วย Dev 2 และถ้ามีคนที่สามให้แทนด้วย Dev 3
ให้เลือกกันในทีมได้เลยว่าใครจะเล่นบทบาทสมมุติเป็น Dev 1, Dev 2 หรือ ถ้ามี Dev 3
เมื่อทำเสร็จทุก Exercise แล้วให้ส่ง URL ของ Remote repository ใน Input ด้านล่าง
URL ของ Remote repository คือ URL ที่เราใช้เข้า Github ของ Repo บน Web Browser
Exercise #1 : Initializing Repository
ให้นึกภาพสถานการณ์ตามว่าทีมเราได้รับมอบหมายให้พัฒนาเว็บไซต์ขึ้นมา 1 เว็บไซต์
ซึ่งเป็นเว็บไซต์ที่เกี่ยวกับการหาบ้านให้กับสัตว์เลี้ยง โดยจะต้องมีการเก็บข้อมูลสัตว์เลี้ยงและผู้ใช้งานที่มาลงทะเบียน
ขั้นตอนด้านล่างต่อไปนี้ Dev 1 เป็นคนทำทั้งหมด
สร้างโฟลเดอร์ใหม่ชื่อว่า pet-adoption-website ลงไปใน PWD
Initialize ตัว pet-adoption-website ให้เป็น Repository
สร้างไฟล์ชื่อว่า pet-profile-page.html และ user-profile-page.html แล้วเขียนโค้ด HTML ตามด้านล่าง
โค้ดในไฟล์ pet-profile-page.html จะต้องมีดังนี้

Copy
โค้ดในไฟล์ user-profile-page.html จะต้องมีดังนี้

Copy
เมื่อทำเสร็จให้บันทึกไฟล์ให้เรียบร้อย แล้วสั่งให้ Git แสดงไฟล์ที่เปลี่ยนแปลงออกมาในหน้า Shell จากนั้นจะเห็นว่าไฟล์ pet-profile-page.html และ user-profile-page.html มีการแก้ไข
เพิ่มไฟล์ pet-profile-page.html และ user-profile-page.html เข้าไปใน Staging area จากนั้นให้ลองตรวจสอบว่าทั้งสองไฟล์เข้าไปอยู่ใน Staging Area แล้วหรือไม่
Commit ตัวไฟล์ที่อยู่ใน Staging Area เข้าไปใน Repository
สร้าง Remote Repository บน Github
เชื่อม Local Repository เข้ากับ Remote Repository ที่สร้างบน Github ในขั้นตอนที่ 6
ให้ Push ตัว Branch main ของ Local Repository ไปยัง Remote repository ที่สร้างไว้ก่อนหน้านี้
สุดท้าย ให้ไปเพิ่ม Dev 2 และ Dev 3 เป็น Collaborator ของ Repository บน Github
Exercise #2 : Pushing Feature Branch to Remote Repository
ขั้นตอนด้านล่างต่อไปนี้ Dev 2 เป็นคนทำทั้งหมด
สถานการณ์คือ Dev 2 กำลังจะพัฒนา Feature ของตัวเองที่ได้รับมอบหมาย
Feature ที่ได้รับมอบหมายคือ การแก้ไขข้อมูลสัตว์เลี้ยงบนหน้าเว็บไซต์บน Repository เดียวกันกับ Dev 1
ให้ Clone ตัว Repository ที่ Dev 1 สร้างไว้ลงมาบนเครื่องของตัวเอง

จากนั้นสร้าง Branch ชื่อว่า feature/pet-profile-page จากนั้นให้เข้าไปแก้ไขข้อมูลสัตว์เลี้ยงในไฟล์ที่ชื่อว่า pet-profile-page.html เขียนโค้ด HTML เพิ่มเติม ในส่วนที่ Highlight สีฟ้า) ดังนี้

Copy
จากนั้นให้ Commit แล้ว Push ตัว Branch feature/pet-profile-page ขึ้นไปบน Remote Repository ให้เรียบร้อย

Exercise #3 : Pushing Feature Branch to Remote Repository
ขั้นตอนด้านล่างต่อไปนี้ Dev 3 เป็นคนทำทั้งหมด (ถ้าไม่มี Dev 3 ให้ข้ามไปทำ Exercise #4 ได้เลย)
สถานการณ์คือ Dev 3 กำลังจะพัฒนา Feature ของตัวเองที่ได้รับมอบหมาย
Feature ที่ได้รับมอบหมายคือ การแก้ไขข้อมูลผู้ใช้งานที่มาลงทะเบียนหาบ้านให้สัตว์เลี้ยงบนหน้าเว็บไซต์บน Repository เดียวกันกับ Dev 1 และ Dev 2
ให้ Dev 3 Clone ตัว Repository ที่ Dev 1 สร้างไว้ลงมาบนเครื่องของตัวเอง

ให้ Dev 3 สร้าง Branch ชื่อว่า feature/user-profile-page จากนั้นให้เข้าไปแก้ไขข้อมูลผู้ใช้งานในไฟล์ที่ชื่อว่า user-profile-page.html เขียนโค้ด HTML เพิ่มเติม (ในส่วนที่ Highlight สีฟ้า) ดังนี้

Copy
จากนั้นให้ Commit แล้ว Push ตัว Branch feature/user-profile-page ขึ้นไปบน Remote Repository ให้เรียบร้อย

Exercise #4 : Fixing Code on Main Branch
ขั้นตอนด้านล่างต่อไปนี้ Dev 1 เป็นคนทำทั้งหมด
สถานการณ์คือให้ Dev 1 เข้าไปแก้ไขข้อมูลผู้ใช้งานและข้อมูลสัตว์เลี้ยงบน Branch main
Dev 1 เข้าไปแก้ไขข้อมูลสัตว์เลี้ยงในไฟล์ที่ชื่อว่า pet-profile-page.html เขียนโค้ด HTML เพิ่มเติม (ในส่วนที่ Highlight สีฟ้า) ดังนี้

Copy
Dev 1 เข้าไปแก้ไขข้อมูลสัตว์เลี้ยงในไฟล์ที่ชื่อว่า user-profile-page.html เขียนโค้ด HTML เพิ่มเติม (ในส่วนที่ Highlight สีฟ้า) ดังนี้

Copy
ให้ Dev 1 ทำการ Commit และ Push การแก้ไขบน Branch main ขึ้นไปบน Remote Repository ให้เรียบร้อย

Exercise #5 : Fetching and Pulling the Code from Remote Repo
ขั้นตอนด้านล่างต่อไปนี้ให้ในทีมช่วยกันทำ
ถ้าทีมมี 3 คน ให้ดูตามขั้นตอนนี้ (Dev 1, Dev 2, Dev 3)

ถ้าทีมมี 2 คน ให้ดูตามขั้นตอนนี้ (Dev 1, Dev 2)
Exercise #6 : Merging to Main Branch
ขั้นตอนด้านล่างต่อไปนี้ให้ Dev 1 และ Dev 2 ช่วยกันทำ
สถานการณ์คือ Dev 2 ต้องการที่จะรวมโค้ดใน Branch feature/pet-profile-page ของเราเอง กลับเข้าไปยัง Branch main
ให้ Dev 2 ทำการ Checkout ไปที่ Branch main และ Merge ตัว Branch feature/pet-profile-page เข้าไปยัง Branch main
จะสังเกตได้ว่าขั้นตอนการ Merge มี Conflict เกิดขึ้น เนื่องจากการแก้ไขโค้ดที่ไฟล์เดียวกัน จะถูกรวมเข้าด้วยกัน
ให้ Dev 1 และ Dev 2 ช่วยกันแก้ไข Conflict ให้ตกลงกันว่าอยากใช้โค้ดที่ใครเป็นคนเขียนขึ้นมา
ตัวอย่างการแก้ไข Merge Conflict สามารถดูได้จากลิงก์นี้
หลังจากที่ Dev 2 ได้ Merge โค้ดเสร็จเรียบร้อย ให้ Push Branch main ขึ้นไปบน Remote Repo
จากนั้นให้ Dev 1 และ Dev 3 (ถ้ามี) ลอง Fetch และ Pull โค้ดล่าสุดบน Remote Repo จะเห็นได้ว่า Branch feature/pet-profile-page ถูก Merge เข้าไปยัง Branchmainเรียบร้อย
Exercise #7 : Merging to Main Branch
ถ้าทีมมีแค่ 2 คน ไม่ต้องทำ Exercise ข้อนี้
ขั้นตอนด้านล่างต่อไปนี้ให้ Dev 1 และ Dev 3 ช่วยกันทำ
สถานการณ์คือ Dev 3 ต้องการที่จะรวมโค้ดใน Branch feature/user-profile-page ของเราเอง กลับเข้าไปยัง Branch main
ให้ Dev 3 ทำการ Checkout ไปที่ Branch main และ Merge ตัว Branch feature/user-profile-page เข้าไปยัง Branch main
จะสังเกตได้ว่าขั้นตอนการ Merge มี Conflict เกิดขึ้น เนื่องจากการแก้ไขโค้ดที่ไฟล์เดียวกัน จะถูกรวมเข้าด้วยกัน
ให้ Dev 1 และ Dev 3 ช่วยกันแก้ไข Conflict ให้ตกลงกันว่าอยากใช้โค้ดที่ใครเป็นคนเขียนขึ้นมา
ตัวอย่างการแก้ไข Merge Conflict สามารถดูได้จากลิงก์นี้
หลังจากที่ Dev 3 ได้ Merge เสร็จเรียบร้อย ให้ Push Branch main ขึ้นไปบน Remote Repo
จากนั้นให้ Dev 1 และ Dev 2 ลอง Fetch และ Pull โค้ดล่าสุดบน Remote Repo จะเห็นได้ว่า Branch feature/user-profile-page ถูก Merge เข้าไปยัง Branch main เรียบร้อย
