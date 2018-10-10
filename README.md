# clock
class Timer:
    def _init_(self, hour, minute):
        self.hour = hour
        self.minute = minute

    def setTimer(self, hour, minute):
        self.Timer = Timer

    def setHour(self, hour):
        self.hour = hour

    def setMinute(self, minute):
        self.minute = minute

    def getTimer(self):
        return self.Timer

    def getHour(self):
        return self.hour

    def getMinute(self):
        return self.minute

    def PluseTime(self, addHour, addMinute):
        if (minute + addMinute>=60):
            if (hour + addHour >= 24):
                self.hour = hour + addHour - 23
                self.minute = minute + addMinute - 60
            else:
                self.hour = hour + addHour + 1
                self.minute = minute + addMinute - 60
        else:
            if (hour + addHour >=24):
                self.hour = hour + addHour + 1
                self.minute += addMinute
            else:
                self.hour += addHour
                self.minute += addMinute

    def minusTime(self, minusHour, minusMinute):
        if(minute - minusMinute < 0):
            if (hour - minusHour < 0):
                self.hour = hour - minusHour + 23
                self.minute = minute - minusMinutes + 60
            else:
                self.hour = hour - minusHour - 1
                self.minute = minute - minusMinutes + 60
        else:
            if (hour - minusHour < 0):
                self.hour = hour - minusHour + 24
                self.minute = minute - minusMinutes
            else:
                self.hour = hour - minusHour
                self.minute = minute - minusMinutes


myTimer1 = Timer()
myTimer1.setTimer(23,25)
print('myTimer1:',myTimer1.getHour(),'시',myTimer1.getMinute(),'분')
myTimer1.pluseTime(1,40)
print('myTimer1:',myTimer1.getHour(),'시',myTimer1.getMinute(),'분')
    

