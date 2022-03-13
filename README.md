# makine-gormesi-2

"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""" BİR FOTOĞRAFI RENKLİDEN SİYAH BEYAZ FORMATA ÇEVİRME """""""""""""""""""""""""""""""""""""""""""""""""""""""

import cv2

from matplotlib import pyplot as plt

I=cv2.imread("10147259973682.jpg")

gray_image = cv2.cvtColor(I, cv2.COLOR_BGR2GRAY)

cv2.imshow('RESİM',I)

cv2.imshow('gri format',gray_image)

cv2.waitKey(0)

![image](https://user-images.githubusercontent.com/49070852/158074040-e8cca88a-c805-450b-a507-5faa90dbf7da.png)



"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""" BİR FOTOĞRAFIN CONTRAST AYARLARI """""""""""""""""""""""""""""""""""""""""""""""""""""""""


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

"""""""""""""""" POLYGON KARE OLUŞTURMA """"""""""""""""""""""""""""""""""""

import matplotlib.patches

import numpy as np

import cv2

from matplotlib.patches import Polygon

from matplotlib import pyplot as plt

polygon1 = Polygon([(1,5), (1,1), (5,1),(5,5)])

fig, ax = plt.subplots(1,1)

ax.add_patch(polygon1)

plt.ylim(0,6)

plt.xlim(0,6)

plt.show()



![image](https://user-images.githubusercontent.com/49070852/158072319-980d1f01-e139-4cdb-861d-de9f61643663.png)

""""""""""""""""""""" MASKELEME """"""""""""""""""""""""""""""""""

import numpy as np

import cv2 as cv

img=cv.imread("10147259973682.jpg")

az=np.array([246,78,243])

cok=np.array([255,255,255])

istenen=cv.inRange(img,az,cok)

sonuc=cv.bitwise_and(img,img,mask=istenen)

cv.imshow("Orijinal",img)

cv.imshow("inrange",istenen)

cv.imshow("sonuc",sonuc)

cv.waitKey(0)



![image](https://user-images.githubusercontent.com/49070852/158072841-691dc09f-f990-41e4-8c68-21ac6d342afa.png)


""""""""""""""""""""""""""""""" BLURLAŞTIRMA """"""""""""""""""""""""""""

import cv2

from matplotlib import pyplot as plt

I=cv2.imread("101472599736821.jpg")

blur = cv2.GaussianBlur(I,(5,5),0)

cv2.imshow('BLUR',blur)

cv2.waitKey(0)



![image](https://user-images.githubusercontent.com/49070852/158073962-77c6f9a7-657c-4139-a15b-e76bebcd9b11.png)








