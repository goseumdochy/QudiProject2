# QudiProject2
Experiment control software for single photon source

*anaconda 가상환경설정
Python 3.4+
comtypes(Windows only), cycler, fysom, gitpython, influxdb, IPython, jedi, jupyter-client, lmfit, lxml, manhole,
matplotlib, numpy, PyDAQmx, pycallgraph(설치 못 함), pyqtgraph, PyQt4(->PyQt5), qtconsole, qtpy,
RPi.GPIO(Raspberry Pi only), rpyc, ruamel.yaml, scipy, spidev(Linux only), statsmodels, traitlets, visa,
pywin32(Windows only), zmq

*변경사항

core/garbage_collector.py 파일의
48번째 줄
self.timer.start(interval * 1000)	->
self.timer.start(int(interval) * 1000)

core/errordialog.py 파일의
50번째 줄
self.setGeometry((screenWidth - 500) / 2,
                         (screenHeight - 100) / 2, 500, 100)
->
self.setGeometry(int((screenWidth - 500) / 2),
                         int((screenHeight - 100) / 2), 500, 100)

으로 수정함.

