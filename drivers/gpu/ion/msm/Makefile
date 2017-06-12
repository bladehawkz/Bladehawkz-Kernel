obj-y += msm_ion.o ion_cp_common.o ion_iommu_map.o

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
