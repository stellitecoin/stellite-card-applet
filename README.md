# stellite-card-applet
StellitePay solution for secure, low cost hardware wallet.

This project is an attempt to create low cost, open source, and end to end secure hardware wallet, to be able to optionally do transaction with StellitePay. This is achieved by using [Javacard](https://en.wikipedia.org/wiki/Java_Card) smartcards technology used in secure credit/debit banking payment. 

Some advantages in using a smartcards to do transaction:
* **Offline device**. Use it like you are using your credit/debit card on merchant POS. Imagine you are overseas, your phone battery run out, not within cellular coverage, or in the need to pay using StellitePay, but with untrusted merchant.
* **Secure**. As all transaction is end to end encrypted by default. See [security design](https://github.com/Ereddon/stellite-card-applet/wiki/Security-Design), there is no way merchant could see and steal your data. 
* **Trustless**. Cryptocurrency is trustless, so be any technology all around it. You don't need to trust the merchant, as anybody could become the merchant, they won't be able to steal anything from you, even if they are intended to. Contrary to popular credit/debit card transaction which vulnerable to skimming and copying, stelliteCard will be skimming/copying-proof. 
* **Theft-proof**. The card is protected by PIN. Don't you worry about it being stolen. Just build another one. By yourself.
* **DIY**. Hell yeah, build one for yourself. Signed by yourself. Build plenty of it if needed. There is no limit. Built you own card offline at home is encouraged. Your credential are not to shared with anyone else.
* **User friendly**. Well, it is just a card reside in your pocket.

# a glimpse look at the security design

![](http://i65.tinypic.com/23ht9b4.png)

This is yet to be final design, but open, peer-reviewed security design are preferred to be used as a foundation. Pros review are encouraged to make it a really good security design. 

# Build applet

**Windows**

Download and install JCKit http://www.javacardos.com/JCIDE/downloads/JCKit.zip

* Create new project, select JC version with minimal java_card_kit-2_2_2. This depend on what version of Javacard you are using.
* set package name to "stellitecard" and package ID to "78 74 6C 61 70 00"
* set applet name to "Stellitecard" (note the uppercase) and applet ID to "78 74 6C 61 70 01"
* replace file Stellitecard.java using the one in this project
* edit userEmail and userPassword in the code according your StellitePay account
* build all packages

**Linux**

TBD

# Install applet to card

**Windows**

* Open pyApduTools (come with JCKit)
* Connect
* Navigate to Manager tab, browse for .cap file in your build folder above
* Download and install

**Linux**

TBD



