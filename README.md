# makine-gormesi-2

""" BİR FOTOĞRAFI RENKLİDEN SİYAH BEYAZ FORMATA ÇEVİRME """

import cv2

from matplotlib import pyplot as plt


I=cv2.imread("10147259973682.jpg")

gray_image = cv2.cvtColor(I, cv2.COLOR_BGR2GRAY)

cv2.imshow('RESİM',I)

cv2.imshow('gri format',gray_image)

cv2.waitKey(2000)


""" BİR FOTOĞRAFIN CONTRAST AYARLARI """


import numpy as np

import cv2

from matplotlib import pyplot as plt

img=cv2.imread("10147259973682.jpg")

b,g,r=cv2.split(img)

cv2.imshow("b",b)

cv2.imshow("g",g)

cv2.imshow("r",r)

plt.hist(img.ravel(),255,[0,255])

plt.hist(b.ravel(),255,[0,255])

plt.hist(g.ravel(),255,[0,255])

plt.hist(r.ravel(),255,[0,255])

plt.show()

cv2.imshow("img",img)

cv2.waitKey(0)

cv2.destroyAllWindows()




![image](https://user-images.githubusercontent.com/49070852/158058124-4459774e-bedf-421e-8ec2-5f3d7a4b5f2c.png)

