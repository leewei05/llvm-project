add_llvm_component_library(LLVMBambooDisassembler
  #BambooDisassembler.cpp

  LINK_COMPONENTS
  CodeGenTypes
  BambooDesc
  BambooInfo
  MCDisassembler
  Support

  ADD_TO_COMPONENT
  Bamboo
)

