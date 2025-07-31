# Dimensionalidade-em-imagens-de-redes-neural
Projeto para curso
#imagem em 50 tons de cinza
import cv2
import numpy as np

# Carregar a imagem
img = cv2.imread("ponte.jpg")

# Converter a imagem para tons de cinza
img_gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Aplicar Gaussian Blur
suave = cv2.GaussianBlur(img_gray, (7, 7), 0)

# Mostrar a imagem suavizada em tons de cinza
cv2.imshow("Imagem em Tons de Cinza", suave)
cv2.waitKey(0)
cv2.destroyAllWindows()

#imagem em preto e branco 
img=cv2.imread("ponte.jpg')
img=v2.cvtColor(img, cv2.COLOR_BGR2GRAY)
suave=cv2.GaussianBlur(img, (7, 71, 0)#aplica blur
(T, bin) = cv2.threshold (suave, 160, 255, cv2.THRESH_BINARY)
(T. bini) = cv2.threshold (suave, 160, 255,
cv2.THRESH BINARY INV)
resultado = np.vstack([
np.hstack([suave, bin]),
np.hstack([bini,cv2.bitwise_and(img, img, mask = bini)])
])

cv2.imshow("Binarização da imagem", resultado)
cv2.waitKey(0)
