# Raspberry-Orb-keyboard-controlleod-robot-cpp-NL

                 WAARSCUWING!
deze  project is gebruikt met
met 9v battery so wees voorzichtg.
meeste links zijn in de video description of github page.

deze project gebruikt WiringPi voor  GPIO programeren (installeer guide is in this guide https://github.com/Dawsatek22/NL_wiringpiblinkv3_cpp_setup-vscode-version.)

de 3d onderdelen zijn geprint met de Open Robotic Platform site.(meer info hier: https://openroboticplatform.com/).    
Meeste links zijn in video description of github page.      
                 SUMMARY:
deze   project gaat over hoe je een   bestuurt Robot met een Keyboard in
in c++ met een  raspberry Pi 4model B/5 met vs code.
    
VAARDIGHEDEN NODIG:
kennis met ssh in VScode en raspberry pi en Terminal,
c++,3d printen, solderen, ervaring in raspberry Pi os/Ubuntu Server.

Vscode EXTENSION AANGERADEN:
C/C++ Extension Pack,Remote - SSH.


GEREEDSCAP EN MATERIAAL NODIG:

laptop/pc (to ssh into the robot ).
1x Raspberrypi 3/4Model b/5.
1 x 1m usb naar usb c cable 
1x power bank 5v en een minium of 2A;
1x 3d printer( om de onderdelen te printen).
6x f/f 20mm dupont wires https://www.amazon.nl/-/en/AZDelivery-compatible-Arduino-Raspberry-Including/dp/B07KYHBVR7/ref=sr_1_2?crid=2AOCVAZW70EAQ&dib=eyJ2IjoiMSJ9.A7UL3aW1haA5anJ9pwVrL3cqp__C93PO_QMWIVBqGLXgOcJC2-2jWXKieyrPCoNmRq9zBopBEZEqDD-veNiSvDvIxDRHYof6g7RTGrrT3Hqin-m-CWi1ab8wB8cZw_lWOJK3lnjMCl2-xcwSzwxDMlF5-1z9KVDpopdRiMk2eFbEk25a6cPT3N_Ah-KUpQ_mxOr9bQA_vjvOqiSmyJthouwZu2OeNqFVSGKtPw_2AwEWF1_EN0WzGRf6czhzxfEIfsptJIkr3tTJgmH8zXzAOm4EiyPPAzwseQhJOUgktgY.iCCLNDA6-mLkiyJ2RK3Mzm9bHpC7fuy1zaTn4B5k1kI&dib_tag=se&keywords=dupont+wire+female+to+female&qid=1712479977&sprefix=dupont+wire+fe%2Caps%2C73&sr=8-2.

2x m/f dupont jumper wires 20mm https://www.amazon.nl/-/en/AZDelivery-compatible-Arduino-Raspberry-Including/dp/B07K8PVKBP/ref=sr_1_3?crid=2AOCVAZW70EAQ&dib=eyJ2IjoiMSJ9.A7UL3aW1haA5anJ9pwVrL3cqp__C93PO_QMWIVBqGLXgOcJC2-2jWXKieyrPCoNmRq9zBopBEZEqDD-veNiSvDvIxDRHYof6g7RTGrrT3Hqin-m-CWi1ab8wB8cZw_lWOJK3lnjMCl2-xcwSzwxDMlF5-1z9KVDpopdRiMk2eFbEk25a6cPT3N_Ah-KUpQ_mxOr9bQA_vjvOqiSmyJthouwZu2OeNqFVSGKtPw_2AwEWF1_EN0WzGRf6czhzxfEIfsptJIkr3tTJgmH8zXzAOm4EiyPPAzwseQhJOUgktgY.iCCLNDA6-mLkiyJ2RK3Mzm9bHpC7fuy1zaTn4B5k1kI&dib_tag=se&keywords=dupont+wire+female+to+female&qid=1712479977&sprefix=dupont+wire+fe%2Caps%2C73&sr=8-3.

6x m/m dupont jumper wires 20mm (4 moeten gesoldeert zijn aan de  tt motors) https://www.amazon.nl/-/en/RELAND-2-54mm-Jumper-Cables-Female/dp/B09T3QCLWW/ref=sr_1_1?crid=2AOCVAZW70EAQ&dib=eyJ2IjoiMSJ9.nLfQiLoNR8TlYdcydZ17vjoUCFqTxpV8CnlmVtCs2oyKzJalWfTF0mUwLsXSuVIt9XzWwarPub7CtR_WtuGRbwBESoH-gVDQq8Xg-M3Zulo0bURBejZHmI4Bm4aUBiKEA8xzo6vF91TleRgfh04_8uIMoiNDqdEE-s-IObJ7nhaSUD3icm1SQrd-405CL_sf2AT0Y23dj3KivfEHtFEQ9jDMOCjtE_kxLRE1jQsSAKbILJstzzlRVnUCVr3Xwsmp4w8tQ7dFH1DtmaNnOz0ZQMDFqcJ81rlGKjwaOPYrNro.DzbjQ0zwJVdng3t-3zZPCkX5FvHT3hv4ZQ_sYcmM8mE&dib_tag=se&keywords=dupont+wire+female+to+female&qid=1712480166&sprefix=dupont+wire+fe%2Caps%2C73&sr=8-1.

1x 9v batterij https://www.amazon.nl/-/en/Panasonic-NB-191017-0059-Block-General-Purpose/dp/B000PS0Y5S/ref=sr_1_12?crid=1N77ATUUN1PJP&dib=eyJ2IjoiMSJ9.j8vMX8z2zcfPnh5wG_O--TnmxtlppICEODhKFwonpyj78eL4iR5jcr7s5vFwyw4XCJg_6SZ7Gqni4O1Laptt2heJHRK0uAp48HxPBvGrYMMoxuIWQAXZ66IpBY_WhqLBoao60jA69j1PkJq-VCWF1s17vh2aFH3pk7_r4Y_2EiB2IbCJKXPKfCq_mT4aNuI9NlWXU0hJ6GEaQ8BI0cIbNXZGdLYt6qgi-UNOaEzdDD2UnTcu8KZss0NIXfU4El9YF8H_yND9-18e8Wd42N1eTzBz_TSH6ctux8BqjLr7JwA.7FfgbD7mJskwuGrmcNstenvnh4vKAhQCitOG__NBGtg&dib_tag=se&keywords=9v+battery&qid=1712479719&sprefix=9v%2Caps%2C81&sr=8-12.

1x 9v battery clip with Dc jack https://www.amazon.nl/-/en/DollaTek-10pcs-Battery-Connection-Arduino/dp/B07DK55VMK/ref=sr_1_4?crid=2OBNIVJDT4I7R&dib=eyJ2IjoiMSJ9.sSY3egPCR5-Hqg9oOgiIl95LRTDbtf5XT6eDtapUMJnPRp0Dq7fGNF9BrmOZRrbbABRkkDVpanCbWfI0xxHyuK2EFYyZCoPa82_ufgZBUCzbGrl-XoNbpisUQfeen55MSx3bU2NR-ObqZDSwLOSnr_0UEYy8MDKD94XikuNwPso_AB7h0pvVok9k6iN-8o6AdrJOyqWlzjcmbJnu-nzIBe-nYNUPkSNBEl39yoOsWLnzLlqvZJ20aU9ySAkIvTpo5TQOpzCknIW9otzA5cyixm6MdAMUhAPmq4lkw4VeEp4.iKNZeAkVO6fnHihFl7xyV7bKzJcX9pCVkbk6p1ZUKLY&dib_tag=se&keywords=9v+clip+with+plug&qid=1712479675&sprefix=9v+clip+with+plug%2Caps%2C67&sr=8-4. 

1x l298n Dc motor driver https://www.amazon.nl/-/en/sspa/click?ie=UTF8&spc=MTo4OTMwMTg0MzI1NDgzMDk3OjE3MTI0Nzk2MTQ6c3BfYXRmOjMwMDA4NzM0Mzc5NTgzMjo6MDo6&url=%2FModule-Bridge-Driver-Stepper-Controller%2Fdp%2FB07PRXMH9P%2Fref%3Dsr_1_1_sspa%3Fcrid%3D1XLFUFODV4G34%26dib%3DeyJ2IjoiMSJ9.bbka0d3gULnVv_08qK2TNZSUvQ3Opa6WqmBkr7XaNIrBIqAOgNAzNa3FcDcYHOZHwo0r0I0-74xiT1q_ZlVaKCtxcjm0GOr6aV1_2_ojCXBk_B1Knezsa3uYMEB9At-QvUd9_XqYelfK7iI9vAojtId4Wl2GKlF4eexOhyvF0AJTEBvppbrXU8QlSqUy3dsZQYZrnAGe3uOw5XqlSmX9IULkqVea-lFVb4ncvl1kktbwSsKL2oLGJ8msiDNl0Xm3wjiM6kQ7QpT0LeznfxCs7tWN12umhf8NVHsA4gTZoQE.QsYCkIgc2SjWFNLskzpwd1j1wx6qB_dJIIHtDcLBhd4%26dib_tag%3Dse%26keywords%3Dl298n%2Bmotor%2Bdriver%26qid%3D1712479614%26sprefix%3Dl2%252Caps%252C91%26sr%3D8-1-spons%26sp_csd%3Dd2lkZ2V0TmFtZT1zcF9hdGY%26psc%3D1.

2x yellow tt motor(2 m/m 20mm jumper wires need to be soldered on each motor) https://www.amazon.nl/-/en/Motor-Intelligent-Vehicle-Robot-Single/dp/B0BLWF4XW1/ref=sr_1_1?crid=1ZI11OUGCM69W&dib=eyJ2IjoiMSJ9.ktNkx-HMYcegTPcAoXoqyTgSrlbj5pWJ-x-VGvBADHeX_52dwbccqkVC8Ud1P-WPRj4DRK7wyYn0FcPH8YGhzE4Bcge4-qxuY3fmqysefRqLQjVezLOjJiTJ1xLAYmbpWOBWbvw5E8mNggl_-tL72OhnFJ-OFBUhkFaB2k05zR7CqUbmHZTBm9VY3pKmUMduzYt7Xl_VW7nsc3YImRPnoqU66wix6ZMgJiaONO6p4cs1iVaNZO84QuYNYBvg-w1CylkK31GsXlcRkImBUGViVlCwWx3Nw9mAkgl2vXmhMR8.7U9TZPR39PUuZocCUl9FEMLrLemEkq1metecu1T1heg&dib_tag=se&keywords=tt+motor&qid=1712479817&sprefix=tt%2Caps%2C75&sr=8-1.

1x 2.1mm DC Socket Power Female Connector Adapter Screw Terminal Plug https://www.amazon.nl/-/en/Connector-Terminal-Compatible-Security-Projector/dp/B08LKVPXMS/ref=sr_1_1?crid=34FRIGV8HZUFR&dib=eyJ2IjoiMSJ9.VaecFBlxfMOnmggfUBiFLNmfe71XoAr6ZJpgmp0ke_20Vrx5ldpgiDRQlfw9Y32Bn9G-2rzXqqaLKbcXFyGpgQrwD_OLtjoMU7c9ZxtGl5Q5Dqbz8jIS9GEST0kpfUfzL8TOonPSGF5Cs-q02c4sn3DmMle9lIjTU8LLaT-zzjYAu18lkj2vpM1LnMMNoSFtbStyAyajnJ1qCqhPiRemXEfPZOJXAeavERuJZEwUY2yJf1S70r3pbmrpmcrofK0FkpRlcppb1FrX7lhcDvRx88sLeSrBhMPfPWhlxkEcUxA.XVD4U9Bc3vFKH4J32Su0kDfCGWl7tZQTtgkpYsC0rIQ&dib_tag=se&keywords=dc+terminal+female+connector+2.1&qid=1712480812&sprefix=dc+terminal+female+connector+2.1%2Caps%2C63&sr=8-1.

2x wheels https://www.tinytronics.nl/nl/mechanica-en-actuatoren/onderdelen/wielen/reservewiel-auto-kit-zelfbouw.
schroevendraaiers of inbussleutels en moeren voor bouten :
4x m2.5 6mm
4x m3  8mm
4x m3 12mm
4x m3 16mm

3D GEPRINTE ONDERDELEN(PlA or PETG):
(de files zijn opgeslagen in  github repository )

1x dt22-79-d22powerbankholdeWidthV1-powerbankholder.stl https://openroboticplatform.com/part:79.
1x dt22-76-d22Rpiholderforhatsupport-Body.stl https://openroboticplatform.com/part:76.
1x dt22-72-d22.2to4wheelerplate.stl.
1x9 volt batteries holder. https://openroboticplatform.com/.
1x L298 Holder https://openroboticplatform.com/.


github link voor project https://github.com/Dawsatek22/Raspberry-Orb-keyboard-controlled-robot-c-ENG:

als je mijn  projects leuk vind ik post mijn c++ robotics projecteb 1 week eerder op deze platforms(aangeraden voor 12+ of voogt permissie):

joshwhotv: https://www.joshwhotv.com/channel/Dawsatek22.

corder.tv: https://corder.tv/channel/Dawsabot22.

dat was alles dank je wel
