from building import *
import os

cwd = GetCurrentDir()
group = []
src = Glob('*.c')
CPPPATH = [cwd]

list = os.listdir(cwd)
for d in list:
    path = os.path.join(cwd, d)
    if os.path.isfile(os.path.join(path, 'SConscript')):
        group = group + SConscript(os.path.join(d, 'SConscript'))

group = group + DefineGroup('UIDemo', src, depend = ['BSP_USING_LVGL'], CPPPATH = CPPPATH)

Return('group')
