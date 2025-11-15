add_llvm_component_library(LLVMBambooAsmParser
  #BambooAsmParser.cpp

  LINK_COMPONENTS
  CodeGenTypes
  BambooCodeGen
  BambooInfo
  MC
  MCParser
  Support

  ADD_TO_COMPONENT
  Bamboo
  )
