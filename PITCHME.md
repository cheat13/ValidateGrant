# Validate **Grant**

---

## Background

+++

### DB to Key

---

## Hash

+++

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

![](assets/img/HMACConcept.PNG)

+++

![](assets/img/HowToHMACUse.PNG)

---

## Derived Key

+++

![](assets/img/DerivedKey.PNG)

---

## Validate Grant
### (HMAC + Derived Key)

+++?color=#EE5D58

## Subscription
### (Derived Key)
![](assets/img/Grant.PNG)

---

## Validate Grant

- Who   : Service
- What  : Validate Grant by HMAC + Derived Key
- Where : System
- When  : Biz(user) send CMD
- Why   : ตรวจสอบว่า CMD นี้ส่งมาจาก user ที่มีสิทธิ์เข้าถึง service นั้นๆ และข้อมูลไม่ได้ถูกเปลี่ยนระหว่างทาง
- how   : ...