-include ../tools.mk

all: $(call DYLIB,cfoo)
	$(RUSTC) foo.rs
	$(RUSTC) bar.rs
	LD_LIBRARY_PATH=$(TMPDIR) $(call RUN,bar)
	rm $(TMPDIR)/$(call DYLIB_GLOB,cfoo)
	$(call FAIL,bar)
