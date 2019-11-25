import sys
from PyQt5.QtWidgets import QWidget, QMainWindow, QApplication, QPushButton
from PyQt5.QtGui import QPainter, QColor
from random import randint
from UI import Ui_MainWindow

class Example(QMainWindow, Ui_MainWindow):
    def __init__(self):
        super().__init__()
        self.setupUi(self)
        self.flag = False
        self.pushButton.clicked.connect(self.drawf)
        self.show()

    def drawf(self):
        self.flag = True
        self.update()

    def paintEvent(self, event):
        if self.flag:
            qp = QPainter()
            qp.begin(self)
            self.drawFlag(qp)
            qp.end()

    def drawFlag(self,qp):
        self.size = randint(20, 60)
        qp.setBrush(QColor(randint(0, 255), randint(0, 255), randint(0, 255)))
        qp.drawEllipse(randint(0, (540 - self.size)), randint(0, (600 - self.size)), self.size, self.size)


if __name__ == '__main__':
    app = QApplication(sys.argv)
    ex = Example()
    sys.exit(app.exec_())
