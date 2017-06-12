GRAPHITE = -fgraphite -fgraphite-identity -floop-interchange -ftree-loop-distribution -floop-strip-mine -floop-block -ftree-loop-linear -floop-nest-optimize
OPTIMIZATION_FLAGS = -O3 -mcpu=cortex-a15 -mtune=cortex-a15 -march=armv7ve -mfpu=neon-vfpv4 \
		     -mvectorize-with-neon-quad -DNDEBUG \
                     -fsingle-precision-constant \
                     -fgcse-sm -fgcse-las \
		     -fsched-spec-load -fforce-addr \
		     -fno-tree-vectorize $(GRAHPITE) \
		     -munaligned-access -marm \
		     -fipa-pta -fivopts \
		     -fsection-anchors -funsafe-loop-optimizations \
		     -ftracer -ftree-loop-im -ftree-loop-ivcanon -funroll-loops

ccflags-y := $(OPTIMIZATION_FLAGS)

obj-$(CONFIG_ION) +=	ion.o ion_heap.o ion_page_pool.o ion_system_heap.o \
			ion_carveout_heap.o ion_chunk_heap.o
obj-$(CONFIG_CMA) += ion_cma_heap.o ion_cma_secure_heap.o
obj-$(CONFIG_ION_TEGRA) += tegra/
obj-$(CONFIG_ION_MSM) += ion_cp_heap.o ion_removed_heap.o msm/
