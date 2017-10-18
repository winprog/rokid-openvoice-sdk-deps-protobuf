project (protobuf-android5.0)

add_definitions (-D_USING_LIBCXX)

set (CC_LITE_SRC_FILES     src/google/protobuf/stubs/common.cc
    src/google/protobuf/stubs/once.cc                                
    src/google/protobuf/stubs/hash.cc                                 
    src/google/protobuf/stubs/hash.h                                 
    src/google/protobuf/stubs/map_util.h                             
    src/google/protobuf/stubs/stl_util-inl.h                             
    src/google/protobuf/extension_set.cc                             
    src/google/protobuf/generated_message_util.cc                    
    src/google/protobuf/message_lite.cc                              
    src/google/protobuf/repeated_field.cc                            
    src/google/protobuf/wire_format_lite.cc                          
    src/google/protobuf/io/coded_stream.cc                           
    src/google/protobuf/io/coded_stream_inl.h                        
    src/google/protobuf/io/zero_copy_stream.cc                       
    src/google/protobuf/io/zero_copy_stream_impl_lite.cc)

set (protobuf_cc_full_src_files ${CC_LITE_SRC_FILES}
    src/google/protobuf/stubs/strutil.cc                             
    src/google/protobuf/stubs/strutil.h                              
    src/google/protobuf/stubs/substitute.cc                          
    src/google/protobuf/stubs/substitute.h                           
    src/google/protobuf/stubs/structurally_valid.cc                  
    src/google/protobuf/descriptor.cc                                
    src/google/protobuf/descriptor.pb.cc                             
    src/google/protobuf/descriptor_database.cc                       
    src/google/protobuf/dynamic_message.cc                           
    src/google/protobuf/extension_set_heavy.cc                       
    src/google/protobuf/generated_message_reflection.cc              
    src/google/protobuf/message.cc                                   
    src/google/protobuf/reflection_ops.cc                            
    src/google/protobuf/service.cc                                   
    src/google/protobuf/text_format.cc                               
    src/google/protobuf/unknown_field_set.cc                         
    src/google/protobuf/wire_format.cc                               
    src/google/protobuf/io/gzip_stream.cc                            
    src/google/protobuf/io/printer.cc                                
    src/google/protobuf/io/tokenizer.cc                              
    src/google/protobuf/io/zero_copy_stream_impl.cc                  
    src/google/protobuf/compiler/importer.cc                         
    src/google/protobuf/compiler/parser.cc)

add_library (libprotobuf-rokid-cpp-full ${protobuf_cc_full_src_files})
target_link_libraries (libprotobuf-rokid-cpp-full z dl)
