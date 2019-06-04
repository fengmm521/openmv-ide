# openmv-ide #
Qt Creator based OpenMV IDE

Instructions for Compiling OpenMV-IDE for Desktop
=================================================

* Install 7-Zip and add it to PATH.
* Install Python 2.7 and add it to PATH.
* Install Qt (to the default location).
* Install The Qt Installer Framework (to the default location).

In `/`, build the ide (using the standard bare terminal):

     ```
     $ git clone --recursive https://github.com/openmv/openmv-ide.git
     $ cd openmv-ide
     $ ./make.py
     ```

You'll find the installer in `build`.

Instructions for Compiling OpenMV-IDE for the RaspberryPi on Ubuntu (64-bit)
============================================================================

* Install QtRpi.
* Install Qt (to the default location).

In `/`, build the ide (using the standard bare terminal):

     ```
     $ git clone --recursive https://github.com/openmv/openmv-ide.git
     $ cd openmv-ide
     $ ./make.py --rpi <path-to-qtrpi-installdir e.g. /opt/qtrpi/raspi/qt5>
     ```

You'll find the installer in `build`.

Instructions for running the installer silently
===============================================

https://stackoverflow.com/a/34032216

Note that some modifications to the above solution may be needed.


注册码：
qt-creator/src/plugins/openmv/openmvplugin.cpp文件的3623行
                            if((reply->error() == QNetworkReply::NoError) && (!data.isEmpty()))
                            {
                                if(QString::fromUtf8(data).contains(QStringLiteral("<p>No</p>")))
                                {
//                                    QTimer::singleShot(0, this, [this, board, id] { registerOpenMVCam(board, id); });
                                }
                            }
