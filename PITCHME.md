# Validate **Grant**

---

## Background

+++

![](assets/img/bg.PNG)

---

## Hash

+++

![](assets/img/Hash_Concept.PNG)

+++

![](assets/img/Hash1.PNG)

+++

![](assets/img/Hash2.PNG)

+++

![](assets/img/Hash3.PNG)

---

## HMAC
#### (**H**ash-based **M**essage **A**uthentication **C**ode)

+++

![](assets/img/HMACConcept.PNG)

+++

![](assets/img/HowToHMACUse.PNG)

---

## Derived **Key**

+++

![](assets/img/DerivedKey.PNG)

---

## Grant
### Derived Key

+++

![](assets/img/Grant1.PNG)

---

## Validate Grant
### HMAC + Derived Key

+++

![](assets/img/ValidateGrant.PNG)

--- 

## Rules of Derived key

+++


@snap[north-west]
#### Rules of Derived key
```cs zoom-0.5
Given:
    Owner: "[O1]/[O2]/.../[On]"
    Grant: "[G1]/[G2]/.../[Gm]"

for(i=1;;i++) {
    if (Gi == Oi)
        owner = "[O1]/[O2]/.../[Oi]"
        grant = "[G1]/[G2]/.../[Gi]"
    else if (Grant.length (m) < i)
        owner = "[O1]/[O2]/.../[Oi-1]/[Oi]"
        grant = "[G1]/[G2]/.../[Gm]"
    else if (Owner.length (n) < i)
        owner = "[O1]/[O2]/.../[On]"
        grant = "[G1]/[G2]/.../[Gi-1]/[Gi]"
    else if (Gi != Oi)
        for (j=i; j > Grant.length (m); j++) {
            owner = grant = "[G1]/[G2]/.../[Gj]"
        }
        for (k=i; k > Owner.length (n); k++) {
            owner = "[O1]/[O2]/.../[Ok]"
            grant = "[G1]/[G2]/.../[Gm]"
        }
        break;
    else break;
}
```

@snapend

@snap[north-east]
#### Example
```cs
Owner: "m.com/./bz/101"
Grant: "m.com/./bz/101"

key0 + o: "m.com"
key1 + g: "m.com"
key2 + o: "m.com/./bz/101"
key3 + g: "m.com/./bz/101"
key4
```
@snapend

@[1-3]
@[5,25]
@[5,6-8,25]
@[5,9-11,25]
@[5,12-14,25]
@[5,15-23,25]
@[5,24,25]