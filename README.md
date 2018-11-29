# -*- coding: utf-8 -*-

# Form implementation generated from reading ui file 'C:\Users\Kira\PycharmProjects\2.Felev\Harmadik Félév\Beadando.ui'
#
# Created by: PyQt5 UI code generator 5.11.3
#
# WARNING! All changes made in this file will be lost!

from PyQt5 import QtCore, QtGui, QtWidgets

class Auto:
    def __init__(self, marka, tipus, uzemanyag, szin, rendszam, engedely):
        self.__marka = marka
        self.__tipus = tipus
        self.__uzemanyag = uzemanyag
        self.__szin = szin
        self.__rendszam = rendszam
        self.__engedely = engedely

    def getMarka(self):
        return self.__marka

    def getTipus(self):
        return self.__tipus

    def getUzemanyag(self):
        return self.__uzemanyag

    def getSzin(self):
        return self.__szin

    def getRendszam(self):
        return self.__rendszam

    def getEngedely(self):
        return self.__engedely

    def setMarka(self, new):
        self.__marka = new

    def setTipus(self, new):
        self.__tipus = new

    def setUzemanyag(self, new):
        self.__uzemanyag = new

    def setSzin(self, new):
        self.__szin = new

    def setRendszam(self, new):
        self.__rendszam = new

    def setEngedely(self, new):
        self.__engedely = new

    def __str__(self):
        return 'Rendszám: ' + self.__rendszam + ' Márka: ' + self.__marka + ' Tipus: ' + self.__tipus


class HianyzoAdat(Exception):
    def __init__(self, value):
        self.__value = value

    def __str__(self):
        return "A " + self.__value + " nincs megadva!"



class Ui_Belepteto_rendszer(object):

    listaautok= []

    def setupUi(self, Belepteto_rendszer):
        Belepteto_rendszer.setObjectName("Belepteto_rendszer")
        Belepteto_rendszer.resize(764, 703)
        self.centralwidget = QtWidgets.QWidget(Belepteto_rendszer)
        self.centralwidget.setObjectName("centralwidget")
        self.Marka = QtWidgets.QLabel(self.centralwidget)
        self.Marka.setGeometry(QtCore.QRect(160, 30, 91, 31))
        self.Marka.setObjectName("Marka")
        self.Uzemanyag = QtWidgets.QLabel(self.centralwidget)
        self.Uzemanyag.setGeometry(QtCore.QRect(160, 110, 91, 31))
        self.Uzemanyag.setObjectName("Uzemanyag")
        self.Szin_2 = QtWidgets.QLabel(self.centralwidget)
        self.Szin_2.setGeometry(QtCore.QRect(160, 150, 91, 31))
        self.Szin_2.setObjectName("Szin_2")
        self.Tipus_2 = QtWidgets.QLabel(self.centralwidget)
        self.Tipus_2.setGeometry(QtCore.QRect(160, 70, 91, 31))
        self.Tipus_2.setObjectName("Tipus_2")
        self.Rendszam_2 = QtWidgets.QLabel(self.centralwidget)
        self.Rendszam_2.setGeometry(QtCore.QRect(160, 190, 91, 31))
        self.Rendszam_2.setObjectName("Rendszam_2")
        self.Engedely_2 = QtWidgets.QLabel(self.centralwidget)
        self.Engedely_2.setGeometry(QtCore.QRect(160, 240, 71, 16))
        self.Engedely_2.setObjectName("Engedely_2")
        self.Marka_2 = QtWidgets.QLineEdit(self.centralwidget)
        self.Marka_2.setGeometry(QtCore.QRect(280, 40, 113, 22))
        self.Marka_2.setObjectName("Marka_2")
        self.Tipus = QtWidgets.QLineEdit(self.centralwidget)
        self.Tipus.setGeometry(QtCore.QRect(280, 80, 113, 22))
        self.Tipus.setObjectName("Tipus")
        self.Szin = QtWidgets.QLineEdit(self.centralwidget)
        self.Szin.setGeometry(QtCore.QRect(280, 160, 113, 22))
        self.Szin.setObjectName("Szin")
        self.Rendszam = QtWidgets.QLineEdit(self.centralwidget)
        self.Rendszam.setGeometry(QtCore.QRect(280, 200, 113, 22))
        self.Rendszam.setObjectName("Rendszam")
        self.Uzemanyag_2 = QtWidgets.QComboBox(self.centralwidget)
        self.Uzemanyag_2.setGeometry(QtCore.QRect(280, 120, 111, 21))
        self.Uzemanyag_2.setObjectName("Uzemanyag_2")
        self.Uzemanyag_2.addItem("")
        self.Uzemanyag_2.addItem("")
        self.Uzemanyag_2.addItem("")
        self.Engedely = QtWidgets.QCheckBox(self.centralwidget)
        self.Engedely.setGeometry(QtCore.QRect(280, 240, 121, 20))
        self.Engedely.setObjectName("Engedely")
        self.Felvesz = QtWidgets.QPushButton(self.centralwidget)
        self.Felvesz.setGeometry(QtCore.QRect(40, 280, 93, 28))
        self.Felvesz.setObjectName("Felvesz")
        self.Modosit = QtWidgets.QPushButton(self.centralwidget)
        self.Modosit.setGeometry(QtCore.QRect(160, 280, 93, 28))
        self.Modosit.setObjectName("Modosit")
        self.Torol = QtWidgets.QPushButton(self.centralwidget)
        self.Torol.setGeometry(QtCore.QRect(380, 280, 93, 28))
        self.Torol.setObjectName("Torol")
        self.Modosit_2 = QtWidgets.QPushButton(self.centralwidget)
        self.Modosit_2.setGeometry(QtCore.QRect(270, 280, 93, 28))
        self.Modosit_2.setObjectName("Modosit_2")
        self.Adatok_2 = QtWidgets.QListWidget(self.centralwidget)
        self.Adatok_2.setGeometry(QtCore.QRect(50, 330, 421, 321))
        self.Adatok_2.setObjectName("Adatok_2")
        Belepteto_rendszer.setCentralWidget(self.centralwidget)
        self.menubar = QtWidgets.QMenuBar(Belepteto_rendszer)
        self.menubar.setGeometry(QtCore.QRect(0, 0, 764, 26))
        self.menubar.setObjectName("menubar")
        Belepteto_rendszer.setMenuBar(self.menubar)
        self.statusbar = QtWidgets.QStatusBar(Belepteto_rendszer)
        self.statusbar.setObjectName("statusbar")
        Belepteto_rendszer.setStatusBar(self.statusbar)

        self.retranslateUi(Belepteto_rendszer)
        QtCore.QMetaObject.connectSlotsByName(Belepteto_rendszer)

        self.Felvesz.clicked.connect(self.FelveszClicked)
        self.Modosit.clicked.connect(self.SzerkesztClicked)

    def retranslateUi(self, Belepteto_rendszer):
        _translate = QtCore.QCoreApplication.translate
        Belepteto_rendszer.setWindowTitle(_translate("Belepteto_rendszer", "Belepteto_rendszer"))
        self.Marka.setText(_translate("Belepteto_rendszer", "Márka:"))
        self.Uzemanyag.setText(_translate("Belepteto_rendszer", "Üzemanyag:"))
        self.Szin_2.setText(_translate("Belepteto_rendszer", "Szín:"))
        self.Tipus_2.setText(_translate("Belepteto_rendszer", "Típus:"))
        self.Rendszam_2.setText(_translate("Belepteto_rendszer", "Rendszám:"))
        self.Engedely_2.setText(_translate("Belepteto_rendszer", "Engedély:"))
        self.Uzemanyag_2.setItemText(0, _translate("Belepteto_rendszer", "Benzin"))
        self.Uzemanyag_2.setItemText(1, _translate("Belepteto_rendszer", "Elektromos"))
        self.Uzemanyag_2.setItemText(2, _translate("Belepteto_rendszer", "Diesel"))
        self.Engedely.setText(_translate("Belepteto_rendszer", "Engedélyezve"))
        self.Felvesz.setText(_translate("Belepteto_rendszer", "Felvesz"))
        self.Modosit.setText(_translate("Belepteto_rendszer", "Szerkeszt"))
        self.Torol.setText(_translate("Belepteto_rendszer", "Töröl"))
        self.Modosit_2.setText(_translate("Belepteto_rendszer", "Módosít"))


    def FelveszClicked(self):
        try:
            marka = self.Marka_2.text()
            tipus = self.Tipus.text()
            uzemanyag = self.Uzemanyag_2.currentText()
            szin = self.Szin.text()
            rendszam = self.Rendszam.text()
            engedely = self.Engedely.isChecked()

            if len(marka) == 0:
                raise HianyzoAdat('márka')
            if len(tipus) == 0:
                raise HianyzoAdat('típus')
            if len(szin) == 0:
                raise HianyzoAdat('szín')
            if len(rendszam) == 0:
                raise HianyzoAdat('rendszám')

        except HianyzoAdat as ha:
            msg = QtWidgets.QMessageBox()
            msg.setWindowTitle('Figyelmeztetés')
            msg.setIcon(QtWidgets.QMessageBox.Warning)
            msg.setText(ha.__str__())
            msg.exec()

        else:
            ujauto = Auto(marka, tipus, uzemanyag, szin, rendszam, engedely)
            if ujauto not in self.listaautok:
                self.listaautok.append(ujauto)
                self.listaautok.sort()
                self.Adatok_2.clear()
                for i in self.listaautok:
                    self.Adatok_2.addItem(i.__str__())

            else:
                msg = QtWidgets.QMessageBox()
                msg.setWindowTitle('Figyelmeztetés!')
                msg.setIcon(QtWidgets.QMessageBox.Warning)
                msg.setText("Ez az autó már szerepel az adatbázisban!")
                msg.exec()

    def SzerkesztClicked(self, item):
        if not self.Adatok_2.currentItem():
            msg = QtWidgets.QMessageBox()
            msg.setWindowTitle("Figyelmeztetés")
            msg.setIcon(QtWidgets.QMessageBox.Warning)
            msg.setText("Ki kell választanod egy autót a listából!")
            msg.exec()

        else:
            item = self.Adatok_2.currentItem()
            tmp = item.text()
            tmp = tmp.split(' ')
            rendsz = tmp[1]
            for i in self.listaautok:
                if rendsz== i.getRendszam():
                    self.Marka_2.setText(i.getMarka())
                    self.Tipus.setText(i.getTipus())
                    self.Uzemanyag_2.setCurrentText(i.getUzemanyag())
                    self.Szin.setText(i.getSzin())
                    self.Rendszam.setText(i.getRendszam)
                    self.Engedely.setText(i.getEngedely)


if __name__ == "__main__":
    import sys
    app = QtWidgets.QApplication(sys.argv)
    Belepteto_rendszer = QtWidgets.QMainWindow()
    ui = Ui_Belepteto_rendszer()
    ui.setupUi(Belepteto_rendszer)
    Belepteto_rendszer.show()
    sys.exit(app.exec_())

