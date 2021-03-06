project('corgids', 'cpp', default_options : ['cpp_std=c++11'])
qt5 = import('qt5')
qt5dep = dependency('qt5', modules: ['Core','Gui', 'Widgets'])

src = ['src/main.cpp',
      'src/cartridge.cpp',
      'src/cp15.cpp',
      'src/cpu.cpp',
      'src/cpuinstrs.cpp',
      'src/dma.cpp',
      'src/firmware.cpp',
      'src/instrthumb.cpp',
      'src/main.cpp',
      'src/rtc.cpp',
      'src/spi.cpp',
      'src/timers.cpp',
      'src/emulator.cpp',
      'src/emuwindow.cpp',
      'src/configwindow.cpp',
      'src/config.cpp',
      'src/gpu.cpp',
      'src/arm9rw.cpp',
      'src/arm7rw.cpp',
      'src/ipc.cpp',
      'src/spu.cpp',
      'src/wifi.cpp',
      'src/touchscreen.cpp',
      'src/debugwindow.cpp',
      'src/disasm_arm.cpp',
      'src/gpueng.cpp',
      'src/gpu3d.cpp',
      'src/armtable.cpp',
      'src/emuthread.cpp',
      'src/bios.cpp']

ui = ['src/configwindow.ui',
      'src/debugwindow.ui']

headers = ['src/cartridge.hpp',
          'src/cp15.hpp',
          'src/cpu.hpp',
          'src/cpuinstrs.hpp',
          'src/dma.hpp',
          'src/emulator.hpp',
          'src/firmware.hpp',
          'src/instrtable.h',
          'src/interrupts.hpp',
          'src/memconsts.h',
          'src/rtc.hpp',
          'src/spi.hpp',
          'src/timers.hpp',
          'src/emuwindow.hpp',
          'src/configwindow.hpp',
          'src/config.hpp',
          'src/gpu.hpp',
          'src/ipc.hpp',
          'src/spu.hpp',
          'src/wifi.hpp',
          'src/touchscreen.hpp',
          'src/debugwindow.hpp',
          'src/disassembler.hpp',
          'src/gpueng.hpp',
          'src/gpu3d.hpp',
          'src/emuthread.hpp',
          'src/bios.hpp']

subdir('dist')

moc_files = qt5.preprocess(ui_files: ui,
                          moc_headers: headers)

executable('corgids', src, moc_files, dependencies : qt5dep, install : true)
