# qrpy
generador de qr con python

El módulo qrcode nos permite modificar el tamaño de la imagen, que datos estarán dentro de ella y el error de corrección que determina la capacidad que tiene el código para restaurar información si ha sido dañado
import qrcode

#  Creamos un objeto codigo QR
qr = qrcode.QRCode(
    version = 1,
    error_correction = qrcode.constants.ERROR_CORRECT_H,
    box_size = 10,
    border = 4
)

# Podemos crear la informacion que queremos 
# en el codigo de manera separada
info = 'Necesitamos guardar este texto en el codigo QR'

# Agregamos la informacion
qr.add_data(info)
qr.make(fit=True)

# Creamos una imagen para el objeto código QR
imagen = qr.make_image()

# Guardemos la imagen con la extension que queramos
imagen.save('codigo.png')
![image](https://user-images.githubusercontent.com/77991838/120045924-0eb09d80-bfdf-11eb-90cd-f546c66a7893.png)
