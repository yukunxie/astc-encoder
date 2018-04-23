PROJECT (astcenc)

#SET (HEADER_LIST  render.h)
SET (SRC_LIST 
astc_averages_and_directions.cpp
astc_block_sizes2.cpp
astc_codec_internals.h
astc_color_quantize.cpp
astc_color_unquantize.cpp
astc_compress_symbolic.cpp
astc_compute_variance.cpp
astc_decompress_symbolic.cpp
astc_encoding_choice_error.cpp
astc_find_best_partitioning.cpp
astc_ideal_endpoints_and_weights.cpp
astc_image_load_store.cpp
astc_integer_sequence.cpp
astc_kmeans_partitioning.cpp
astc_ktx_dds.cpp
astc_partition_tables.cpp
astc_percentile_tables.cpp
astc_pick_best_endpoint_format.cpp
astc_quantization.cpp
astc_stb_tga.cpp
astc_symbolic_physical.cpp
astc_weight_align.cpp
astc_weight_quant_xfer_tables.cpp
mathlib.cpp
mathlib.h
softfloat.cpp
softfloat.h
stb_image.c
vectypes.h
stdint.h
astc_toplevel.cpp
)

ADD_EXECUTABLE(astcenc ${SRC_LIST})

#set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} ${OpenMP_C_FLAGS}")  
#set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${OpenMP_CXX_FLAGS}")  
#set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} ${OpenMP_EXE_LINKER_FLAGS}")  
#
set_target_properties(astcenc PROPERTIES
			RUNTIME_OUTPUT_DIRECTORY "../bin"
			PDB_OUTPUT_DIRECTORY "../output"
		)

add_definitions(-D)
