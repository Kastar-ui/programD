#Contoh Modul untuk menghitung Luas 
#Pendeklarasian VARIABEL 
PHI = 3.14 
######################## 
 
def L_lingk(radius): 
 return PHI * (radius*radius) 
 
def K_lingk(radius): 
 return PHI * (radius*2) 
 
def L_SegiEmpat(sisi): 
 return sisi*sisi 
 
def K_SegiEmpat(sisi): 
 print 4 * sisi 
 
def usage():

print "Usage : %s [-options] [nilai]" %PROG_NAME 
 print """options : 
 -k kelilingS4=sisi Menghitung 
keliling segi empat 
 -L Luaslingkaran=radius Membaca satu 
baris dari isi file 
 -K --kelilinglingkaran=r Menentukan 
nama file 
 -h help Menampilkan help 
ini 
""" 
 sys.exit(2) 
 
 
def main(): 
 if len(sys.argv[1:]) == 0 : 
 usage() 
 try : 
 optlist, args = getopt.getopt(sys.argv[1:], 
'k:L:K:h', ['kelilingS4=','Luaslingkaran','kelilinglingk', 
'help']) 
 
 except getopt.GetoptError : 
 usage() 
 
 
 for o, arg in optlist : 
 if o in ['-k', '--kelilingS4='] :
K_SegiEmpat (float(arg)) 
 if o in ['-L', '--Luaslingkaran'] : 
 L_lingk(float(arg)) 
 
 
 if o in ['-K', '--kelilinglingk'] : 
 K_lingk(float(arg)) 
 
 if o in ['-h', '--help'] : 
 usage() 
 
 
 
 
 
 
if __name__ == '__main__' : 
 main()
