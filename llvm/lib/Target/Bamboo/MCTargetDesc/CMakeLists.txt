add_llvm_component_library(LLVMBambooDesc
  #BambooAsmBackend.cpp
  #BambooELFObjectWriter.cpp
  #BambooInstPrinter.cpp
  #BambooMCAsmInfo.cpp
  #BambooMCCodeEmitter.cpp
  #BambooMCTargetDesc.cpp

  LINK_COMPONENTS
  MC
  MCDisassembler
  Support
  TargetParser
  BambooInfo

  ADD_TO_COMPONENT
  Bamboo
)
