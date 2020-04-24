# Validate **Grant**

---

## Background

+++

### DB to Key

---

## Hash

+++
@snap[north-west span-50 text-smallcaps text-08]
Concept
@snapend

![](assets/img/HashConcept.PNG)

+++

![](assets/img/Hash1.PNG)

+++

![](assets/img/Hash2.PNG)

+++

![](assets/img/Hash3.PNG)

---

## HMAC

+++
@snap[north-west span-50 text-smallcaps text-08]
Concept
@snapend

![](assets/img/HMACConcept.PNG)

+++

![](assets/img/HowToHMACUse.PNG)

---

## Derived Key

---

## Validate Grant
### (HMAC + Derived Key)

---

## Validate Grant

- Who   : Service
- What  : Validate Grant by HMAC + Derived Key
- Where : System
- When  : Biz(user) send CMD
- Why   : ตรวจสอบว่า CMD นี้ส่งมาจาก user ที่มีสิทธิ์เข้าถึง service นั้นๆ และข้อมูลไม่ได้ถูกเปลี่ยนระหว่างทาง
- how   : ...