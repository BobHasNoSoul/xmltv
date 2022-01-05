# xmltv
this is a guide for using mc2xml in 2022 and making your own xmltv guides from it.

Step one: download the zip file of this repo, or use gitclone

step two: copy or move the mc2xml (this "installs" the program.. well just makes it easier to call later)
 `sudo cp ./mc2xml /usr/bin/`

step three: move the crontab script and fix permissions of the files using `sudo cp ./tvguide.sh /tvguide.sh && sudo chmod +x /tvguide.sh && sudo chmod +x /usr/bin/mc2xml`
inside the tvguide.sh file you will see a line ( `/usr/bin/mc2xml -3 -o /PATH/TO/SAVE/tvguide.xml <<< $'43'` )
in there edit the path to a path you want it to be saved in just be sure you have the read write permissions for that dir. You will also need to edit the number 43 (freeview east) in the last line too and replace it with one of the following numbers if you do not want the freeview east listings but another region / provider.


````
Select lineup:

  0: BT TV - Cambridgeshire
  1: BT TV - Channel Islands
  2: BT TV - Cumbria
  3: BT TV - East
  4: BT TV - East Midlands
  5: BT TV - London
  6: BT TV - North East
  7: BT TV - North West
  8: BT TV - Northern Ireland
  9: BT TV - Oxfordshire
 10: BT TV - Scotland (Borders)
 11: BT TV - Scotland (Central)
 12: BT TV - Scotland (North)
 13: BT TV - South
 14: BT TV - South East
 15: BT TV - South West
 16: BT TV - Wales
 17: BT TV - West
 18: BT TV - West Midlands
 19: BT TV - Yorkshire
 20: BT TV - Yorkshire & Lincolnshire
 21: Freesat - Cambridge
 22: Freesat - Channel Islands
 23: Freesat - East
 24: Freesat - East Midlands
 25: Freesat - London
 26: Freesat - North East
 27: Freesat - North West
 28: Freesat - Northern Ireland
 29: Freesat - Oxfordshire
 30: Freesat - Scotland (Central)
 31: Freesat - Scotland (North)
 32: Freesat - South East
 33: Freesat - South England
 34: Freesat - South West
 35: Freesat - Wales
 36: Freesat - West
 37: Freesat - West Midlands
 38: Freesat - Yorkshire
 39: Freesat - Yorkshire & Lincolnshire
 40: Freeview - Cambridgeshire
 41: Freeview - Channel Islands
 42: Freeview - Cumbria
 43: Freeview - East
 44: Freeview - East Midlands
 45: Freeview - London
 46: Freeview - North East
 47: Freeview - North West
 48: Freeview - Northern Ireland
 49: Freeview - Oxfordshire
 50: Freeview - Scotland (Borders)
 51: Freeview - Scotland (Central)
 52: Freeview - Scotland (North)
 53: Freeview - South
 54: Freeview - South East
 55: Freeview - South West
 56: Freeview - Wales
 57: Freeview - West
 58: Freeview - West Midlands
 59: Freeview - Yorkshire
 60: Freeview - Yorkshire & Lincolnshire
 61: Sky HD - Anglia
 62: Sky HD - Cambridgeshire
 63: Sky HD - Channel Islands
 64: Sky HD - Cumbria
 65: Sky HD - East Midlands
 66: Sky HD - Henley on Thames
 67: Sky HD - London
 68: Sky HD - London (Essex)
 69: Sky HD - London (Kent)
 70: Sky HD - London (Thames Valley)
 71: Sky HD - Meridian (East)
 72: Sky HD - Meridian (West)
 73: Sky HD - North East
 74: Sky HD - North East Midlands
 75: Sky HD - North West
 76: Sky HD - North Yorkshire
 77: Sky HD - Northern Ireland
 78: Sky HD - Oxford
 79: Sky HD - Republic of Ireland
 80: Sky HD - Scotland (Borders)
 81: Sky HD - Scotland (Central)
 82: Sky HD - Scotland (North)
 83: Sky HD - South Lakeland
 84: Sky HD - Wales
 85: Sky HD - West Dorset
 86: Sky HD - West England
 87: Sky HD - West Midlands
 88: Sky HD - Yorkshire
 89: Sky HD - Yorkshire & Lincolnshire
 90: Sky SD - Anglia
 91: Sky SD - Cambridgeshire
 92: Sky SD - Channel Islands
 93: Sky SD - Cumbria
 94: Sky SD - East Midlands
 95: Sky SD - Henley on Thames
 96: Sky SD - London
 97: Sky SD - London (Essex)
 98: Sky SD - London (Kent)
 99: Sky SD - London (Thames Valley)
100: Sky SD - Meridian (East)
101: Sky SD - Meridian (West)
102: Sky SD - North East
103: Sky SD - North East Midlands
104: Sky SD - North West
105: Sky SD - North Yorkshire
106: Sky SD - Northern Ireland
107: Sky SD - Oxford
108: Sky SD - Republic of Ireland
109: Sky SD - Scotland (Borders)
110: Sky SD - Scotland (Central)
111: Sky SD - Scotland (North)
112: Sky SD - South Lakeland
113: Sky SD - Wales
114: Sky SD - West Dorset
115: Sky SD - West England
116: Sky SD - West Midlands
117: Sky SD - Yorkshire
118: Sky SD - Yorkshire & Lincolnshire
119: TalkTalk YouView - Cambridgeshire
120: TalkTalk YouView - Channel Islands
121: TalkTalk YouView - Cumbria
122: TalkTalk YouView - East
123: TalkTalk YouView - East Midlands
124: TalkTalk YouView - London
125: TalkTalk YouView - North East
126: TalkTalk YouView - North West
127: TalkTalk YouView - Northern Ireland
128: TalkTalk YouView - Oxfordshire
129: TalkTalk YouView - Scotland (Borders)
130: TalkTalk YouView - Scotland (Central)
131: TalkTalk YouView - Scotland (North)
132: TalkTalk YouView - South
133: TalkTalk YouView - South East
134: TalkTalk YouView - South West
135: TalkTalk YouView - Wales
136: TalkTalk YouView - West
137: TalkTalk YouView - West Midlands
138: TalkTalk YouView - Yorkshire
139: TalkTalk YouView - Yorkshire & Lincolnshire
140: Virgin - Cambridge
141: Virgin - East
142: Virgin - East Midlands
143: Virgin - London
144: Virgin - North East
145: Virgin - North West
146: Virgin - Northern Ireland
147: Virgin - Oxfordshire
148: Virgin - Scotland (Central)
149: Virgin - Scotland (North)
150: Virgin - South East
151: Virgin - South England
152: Virgin - South West
153: Virgin - Wales
154: Virgin - West
155: Virgin - West Midlands
156: Virgin - Yorkshire
157: Virgin - Yorkshire & Lincolnshire
158: YouView - Cambridgeshire
159: YouView - Channel Islands
160: YouView - Cumbria
161: YouView - East
162: YouView - East Midlands
163: YouView - London
164: YouView - North East
165: YouView - North West
166: YouView - Northern Ireland
167: YouView - Oxfordshire
168: YouView - Scotland (Borders)
169: YouView - Scotland (Central)
170: YouView - Scotland (North)
171: YouView - South
172: YouView - South East
173: YouView - South West
174: YouView - Wales
175: YouView - West
176: YouView - West Midlands
177: YouView - Yorkshire
178: YouView - Yorkshire & Lincolnshire
````

once edited with your desired listing save it and we can move on to the next step.

Step four: adding the crontab, we add the crontab with `sudo crontab -e` and we add a line like the following `1 2 * * * /tvguide.sh` and save it now you have a guide that will auto refresh but oh no no guide just yet.. run it once manually with `sudo /tvguide.sh` if all goes well it will finish and you will have a generated tvguide.xml file where ever you told it to be saved in the tvguide.sh file.

---

Notes:
mc2xml can be found here https://web.archive.org/web/20200426003902/http://mc2xml.awardspace.info/ it is also packed in this repo for ease of use and to avoid any confusion but if you dont randomly trust strangers on github i understand if you need the original source the guide should work the same anyway.
