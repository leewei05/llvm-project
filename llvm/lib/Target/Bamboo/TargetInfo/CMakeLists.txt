add_llvm_component_library(LLVMBambooInfo
  #BambooTargetInfo.cpp

  LINK_COMPONENTS
  MC
  Support

  ADD_TO_COMPONENT
  Bamboo
)
