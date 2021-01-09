Import('RTT_ROOT')
Import('rtconfig')
from building import *

objs = []
cwd     = GetCurrentDir()
list = os.listdir(cwd)
src     = []
CPPPATH = [cwd, str(Dir('#'))]
CPPPATH += [cwd + '/inc']

src     += Glob('./src/*.c')
if GetDepend('KDB_ENABLE_PORT') == True:
    src += Glob('./kdb_port.c')

group = DefineGroup('kdb', src, depend = [''], CPPPATH = CPPPATH)

Return('group')
