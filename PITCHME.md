# Validate **Grant**

---

## Background

+++

### DB to Key

---

## Hash

+++

![](assets/img/HashConcept.PNG)

---

## HMAC

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