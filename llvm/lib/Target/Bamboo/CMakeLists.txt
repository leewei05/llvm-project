add_llvm_component_group(Bamboo)

set(LLVM_TARGET_DEFINITIONS Bamboo.td)

tablegen(LLVM BambooGenRegisterInfo.inc     -gen-register-info)
tablegen(LLVM BambooGenInstrInfo.inc        -gen-instr-info)
tablegen(LLVM BambooGenSubtargetInfo.inc    -gen-subtarget)
tablegen(LLVM BambooGenAsmWriter.inc        -gen-asm-writer)
tablegen(LLVM BambooGenMCCodeEmitter.inc    -gen-emitter)
tablegen(LLVM BambooGenDAGISel.inc          -gen-dag-isel)
tablegen(LLVM BambooGenAsmMatcher.inc       -gen-asm-matcher)
tablegen(LLVM BambooGenDisassemblerTables.inc -gen-disassembler)

add_public_tablegen_target(BambooCommonTableGen)

add_llvm_target(BambooCodeGen
  #BambooAsmPrinter.cpp
  #BambooFrameLowering.cpp
  #BambooInstrInfo.cpp
  #BambooISelLowering.cpp
  #BambooRegisterInfo.cpp
  #BambooSubtarget.cpp
  #BambooTargetMachine.cpp

  LINK_COMPONENTS
  AsmPrinter
  CodeGen
  Core
  MC
  SelectionDAG
  Support
  Target
  TargetParser
  )

add_subdirectory(TargetInfo)
add_subdirectory(MCTargetDesc)
add_subdirectory(AsmParser)
add_subdirectory(Disassembler)