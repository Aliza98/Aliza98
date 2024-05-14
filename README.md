from PyQt5.QtWidgets import *
from PyQt5.QtCore import *
from PyQt5.QtGui import *

#Tampilan
app = QApplication([])
window = QMainWindow()
window.setWindowTitle("Dasboard Keuangan")
window.setGeometry(500,250,400,500)
window.setFixedSize(400,500)

#Tombol
btn_enter = QPushButton("MASUK", window)
btn_enter.setMinimumSize(QSize( 200,50))
btn_enter.setStyleSheet("background-color:#FAEBD0")
btn_enter.move(90, 250)

#Perulangan
def masuk():
        import halaman_2
        window.hide()
        halaman_2.window.show()

#Tampilan
btn_enter.clicked.connect(masuk)
window.show()
app.exec()
