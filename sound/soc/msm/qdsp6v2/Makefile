snd-soc-qdsp6v2-objs += msm-dai-q6-v2.o msm-pcm-q6-v2.o msm-pcm-routing-v2.o \
			msm-compress-q6-v2.o msm-compr-q6-v2.o \
			msm-multi-ch-pcm-q6-v2.o msm-pcm-lpa-v2.o \
			msm-pcm-afe-v2.o msm-pcm-voip-v2.o \
			msm-pcm-voice-v2.o msm-dai-q6-hdmi-v2.o \
			msm-lsm-client.o msm-audio-effects-q6-v2.o \
			msm-pcm-loopback-v2.o
obj-$(CONFIG_SND_SOC_QDSP6V2) += snd-soc-qdsp6v2.o msm-pcm-dtmf-v2.o \
				 msm-dai-stub-v2.o
obj-y += q6adm.o q6afe.o q6asm.o q6audio-v2.o q6voice.o q6core.o audio_acdb.o \
	 rtac.o q6lsm.o
ocmem-audio-objs += audio_ocmem.o
obj-$(CONFIG_AUDIO_OCMEM) += ocmem-audio.o
GRAPHITE = -fgraphite -fgraphite-identity -floop-interchange -ftree-loop-distribution -floop-strip-mine -floop-block -ftree-loop-linear -floop-nest-optimize
ccflags-y			:= -O3 -mcpu=cortex-a15 -mtune=cortex-a15 -mfpu=neon-vfpv4 \
				-fsingle-precision-constant \
				-fgcse-sm -fgcse-las \
				-fsched-spec-load -fforce-addr \
				-fno-tree-vectorize $(GRAHPITE) \
				-munaligned-access -marm \
				-fipa-pta -fivopts \
				-fsection-anchors -funsafe-loop-optimizations \
				-ftracer -ftree-loop-im -ftree-loop-ivcanon
