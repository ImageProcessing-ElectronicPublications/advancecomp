bin_PROGRAMS = advzip advpng advmng advdef

7z_SOURCES = \
	src/7z/7zdeflate.cc \
	src/7z/7zlzma.cc \
	src/7z/AriBitCoder.cc \
	src/7z/CRC.cc \
	src/7z/DeflateDecoder.cc \
	src/7z/DeflateEncoder.cc \
	src/7z/HuffmanEncoder.cc \
	src/7z/IInOutStreams.cc \
	src/7z/InByte.cc \
	src/7z/LSBFDecoder.cc \
	src/7z/LSBFEncoder.cc \
	src/7z/LZMA.cc \
	src/7z/LZMADecoder.cc \
	src/7z/LZMAEncoder.cc \
	src/7z/LenCoder.cc \
	src/7z/LiteralCoder.cc \
	src/7z/OutByte.cc \
	src/7z/WindowIn.cc \
	src/7z/WindowOut.cc

libdeflate_SOURCES = \
	src/libdeflate/adler32.c \
	src/libdeflate/crc32.c \
	src/libdeflate/deflate_compress.c\
	src/libdeflate/deflate_decompress.c \
	src/libdeflate/gzip_compress.c \
	src/libdeflate/gzip_decompress.c \
	src/libdeflate/utils.c \
	src/libdeflate/zlib_compress.c \
	src/libdeflate/zlib_decompress.c


zopfli_SOURCES = \
	src/zopfli/blocksplitter.c \
	src/zopfli/cache.c \
	src/zopfli/deflate.c \
	src/zopfli/gzip_container.c \
	src/zopfli/hash.c \
	src/zopfli/katajainen.c \
	src/zopfli/lz77.c \
	src/zopfli/squeeze.c \
	src/zopfli/tree.c \
	src/zopfli/util.c \
	src/zopfli/zlib_container.c \
	src/zopfli/zopfli.h \
	src/zopfli/zopfli_lib.c

advbase_SOURCES = \
	src/file.cc \
	src/data.cc \
	src/siglock.cc \
	src/compress.cc \
	src/getopt.c \
	src/snprintf.c \
	src/portable.c \
	$(7z_SOURCES) \
	$(libdeflate_SOURCES) \
	$(zopfli_SOURCES)

advzip_SOURCES = \
	src/rezip.cc \
	src/zip.cc \
	src/zipsh.cc \
	$(advbase_SOURCES)

advpng_SOURCES = \
	src/repng.cc \
	src/pngex.cc \
	src/lib/fz.c \
	src/lib/png.c \
	src/lib/error.c \
	src/lib/snstring.c \
	$(advbase_SOURCES)

advmng_SOURCES = \
	src/remng.cc \
	src/pngex.cc \
	src/mngex.cc \
	src/scroll.cc \
	src/lib/fz.c \
	src/lib/png.c \
	src/lib/mng.c \
	src/lib/error.c \
	src/lib/snstring.c \
	$(advbase_SOURCES)

advdef_SOURCES = \
	src/redef.cc \
	src/pngex.cc \
	src/lib/fz.c \
	src/lib/error.c \
	src/lib/snstring.c \
	src/lib/png.c \
	src/lib/mng.c \
	$(advbase_SOURCES)

# Add the .version file in the distribution
dist-hook:
	$(srcdir)/autover.sh > $(distdir)/.version

EXTRA_DIST = \
	README AUTHORS HISTORY INSTALL COPYING \
	doc/advdef.d doc/advzip.d doc/advpng.d doc/advmng.d doc/history.d doc/readme.d doc/authors.d doc/install.d \
	doc/advdef.1 doc/advzip.1 doc/advpng.1 doc/advmng.1 doc/history.1 doc/readme.1 doc/authors.1 doc/install.1 \
	doc/advdef.txt doc/advzip.txt doc/advpng.txt doc/advmng.txt doc/history.txt doc/readme.txt doc/authors.txt doc/install.txt \
	autogen.sh autover.sh \
	src/7z/README \
	src/libdeflate/README.md \
	src/libdeflate/COPYING \
	src/libdeflate/NEWS.md \
	src/zopfli/README \
	src/zopfli/COPYING \
	src/zopfli/CONTRIBUTORS \
	test/test.lst \
	test/archive.zip \
	test/italy.png \
	test/mappy.mng \
	test/basn2c08.png \
	test/basn3p01.png \
	test/basn3p02.png \
	test/basn3p04.png \
	test/basn3p08.png \
	test/basn6a08.png \
	test/basn6a04.png

noinst_HEADERS = \
	src/snprintf.c \
	src/pngex.h \
	src/mngex.h \
	src/scroll.h \
	src/compress.h \
	src/file.h \
	src/data.h \
	src/zip.h \
	src/except.h \
	src/siglock.h \
	src/portable.h \
	src/lib/png.h \
	src/lib/mng.h \
	src/lib/fz.h \
	src/lib/endianrw.h \
	src/lib/error.h \
	src/lib/snstring.h \
	src/lib/extra.h \
	src/7z/7z.h \
	src/7z/AriBitCoder.h \
	src/7z/AriConst.h \
	src/7z/AriPrice.h \
	src/7z/BinTree.h \
	src/7z/BinTree2.h \
	src/7z/BinTree2Main.h \
	src/7z/BinTree3.h \
	src/7z/BinTree3Main.h \
	src/7z/BinTree3Z.h \
	src/7z/BinTree3ZMain.h \
	src/7z/BinTree4.h \
	src/7z/BinTree4Main.h \
	src/7z/BinTree4b.h \
	src/7z/BinTree4bMain.h \
	src/7z/BinTreeMF.h \
	src/7z/BinTreeMFMain.h \
	src/7z/BinTreeMain.h \
	src/7z/BitTreeCoder.h \
	src/7z/CRC.h \
	src/7z/Const.h \
	src/7z/DeflateDecoder.h \
	src/7z/DeflateEncoder.h \
	src/7z/HuffmanDecoder.h \
	src/7z/HuffmanEncoder.h \
	src/7z/IInOutStreams.h \
	src/7z/InByte.h \
	src/7z/LSBFDecoder.h \
	src/7z/LSBFEncoder.h \
	src/7z/LZMA.h \
	src/7z/LZMADecoder.h \
	src/7z/LZMAEncoder.h \
	src/7z/LenCoder.h \
	src/7z/LiteralCoder.h \
	src/7z/OutByte.h \
	src/7z/Portable.h \
	src/7z/RCDefs.h \
	src/7z/RangeCoder.h \
	src/7z/WindowIn.h \
	src/7z/WindowOut.h \
	src/libdeflate/adler32_vec_template.h \
	src/libdeflate/bt_matchfinder.h \
	src/libdeflate/common_defs.h \
	src/libdeflate/cpu_features_common.h \
	src/libdeflate/crc32_multipliers.h \
	src/libdeflate/crc32_tables.h \
	src/libdeflate/decompress_template.h \
	src/libdeflate/deflate_compress.h \
	src/libdeflate/deflate_constants.h \
	src/libdeflate/gzip_constants.h \
	src/libdeflate/hc_matchfinder.h \
	src/libdeflate/ht_matchfinder.h \
	src/libdeflate/lib_common.h \
	src/libdeflate/libdeflate.h \
	src/libdeflate/matchfinder_common.h \
	src/libdeflate/zlib_constants.h \
	src/zopfli/blocksplitter.h \
	src/zopfli/cache.h \
	src/zopfli/deflate.h \
	src/zopfli/gzip_container.h \
	src/zopfli/hash.h \
	src/zopfli/katajainen.h \
	src/zopfli/lz77.h \
	src/zopfli/symbols.h \
	src/zopfli/squeeze.h \
	src/zopfli/tree.h \
	src/zopfli/util.h \
	src/zopfli/zlib_container.h \
	src/zopfli/zopfli.h

man_MANS = doc/advdef.1 doc/advzip.1 doc/advpng.1 doc/advmng.1

clean-local:
	rm -f check.lst check.zip archive.zip mappy.mng italy.png
	rm -f basn2c08.png basn3p01.png basn3p02.png basn3p04.png basn3p08.png basn6a08.png basn6a04.png
	rm -f advdef.exe advzip.exe advpng.exe advmng.exe
	rm -f mappy*.png

maintainer-clean-local:
	rm -f README AUTHORS HISTORY INSTALL doc/copying.txt
	rm -f doc/*.hh

# Rules for documentation

if HAVE_ADVD2
%.1 : %.d
	advd2 man < $(srcdir)/$< > $@

%.txt : %.d
	advd2 txt < $(srcdir)/$< | todos > $@

%.html : %.d
	advd2 html < $(srcdir)/$< > $@

%.hh : %.d
	advd2 frame < $(srcdir)/$< > $@
endif

# Archives

DTOU = tr -d '\015'

README: doc/readme.txt
	cat $< | $(DTOU) > $@

AUTHORS: doc/authors.txt
	cat $< | $(DTOU) > $@

INSTALL: doc/install.txt
	cat $< | $(DTOU) > $@

HISTORY: doc/history.txt
	cat $< | $(DTOU) > $@

doc/copying.txt: COPYING
	cat $< | todos > $@

# We don't test wth -L the with -3 and -4 because the result is depending on
# the compiler and/or optimization options.
# This is likely a defect of 7z/zopfli implementation.
# For zopfli a possible cause is the use of qsort() (not stable sorting),
# that may be different on different platforms.
check-local: ./advzip$(EXEEXT) test/test.lst
	@cp $(srcdir)/test/archive.zip .
	@echo CRC SIZE > check.lst
	$(TESTENV) ./advzip$(EXEEXT) -z archive.zip
	$(TESTENV) ./advzip$(EXEEXT) -L archive.zip >> check.lst
	$(TESTENV) ./advzip$(EXEEXT) -t -p archive.zip
	$(TESTENV) ./advzip$(EXEEXT) -z -3 archive.zip
	$(TESTENV) ./advzip$(EXEEXT) -t -p archive.zip
	$(TESTENV) ./advzip$(EXEEXT) -z -4 archive.zip
	$(TESTENV) ./advzip$(EXEEXT) -t -p archive.zip
	$(TESTENV) ./advzip$(EXEEXT) -a check.zip $(srcdir)/COPYING
	$(TESTENV) ./advzip$(EXEEXT) -t -p check.zip
	$(TESTENV) ./advzip$(EXEEXT) -L check.zip >> check.lst
	$(TESTENV) ./advzip$(EXEEXT) -a -N check.zip $(srcdir)/COPYING
	$(TESTENV) ./advzip$(EXEEXT) -t -p check.zip
	$(TESTENV) ./advzip$(EXEEXT) -L check.zip >> check.lst
	$(TESTENV) ./advzip$(EXEEXT) -z -3 check.zip
	$(TESTENV) ./advzip$(EXEEXT) -t -p check.zip
	$(TESTENV) ./advzip$(EXEEXT) -z -4 check.zip
	$(TESTENV) ./advzip$(EXEEXT) -t -p check.zip
	@cp $(srcdir)/test/mappy.mng .
	$(TESTENV) ./advmng$(EXEEXT) -v -z -f -S 8 mappy.mng
	$(TESTENV) ./advmng$(EXEEXT) -L mappy.mng >> check.lst
	$(TESTENV) ./advmng$(EXEEXT) -v -x mappy.mng
	$(TESTENV) ./advmng$(EXEEXT) -v -a 30 -S 8 mappy.mng mappy-*.png
	$(TESTENV) ./advmng$(EXEEXT) -L mappy.mng >> check.lst
	$(TESTENV) ./advmng$(EXEEXT) -v -a 30 -n -S 8 mappy.mng mappy-*.png
	$(TESTENV) ./advmng$(EXEEXT) -L mappy.mng >> check.lst
	$(TESTENV) ./advmng$(EXEEXT) -v -a 30 -n -r -S 8 mappy.mng mappy-*.png
	$(TESTENV) ./advmng$(EXEEXT) -L mappy.mng >> check.lst
	@cp $(srcdir)/test/italy.png .
	$(TESTENV) ./advpng$(EXEEXT) -z italy.png
	$(TESTENV) ./advpng$(EXEEXT) -L italy.png >> check.lst
	@cp $(srcdir)/test/basn2c08.png $(srcdir)/test/basn3p01.png $(srcdir)/test/basn3p02.png $(srcdir)/test/basn3p04.png $(srcdir)/test/basn3p08.png $(srcdir)/test/basn6a08.png $(srcdir)/test/basn6a04.png .
	$(TESTENV) ./advpng$(EXEEXT) -f -z basn2c08.png basn3p01.png basn3p02.png basn3p04.png basn3p08.png basn6a08.png basn6a04.png
	$(TESTENV) ./advpng$(EXEEXT) -L basn2c08.png basn3p01.png basn3p02.png basn3p04.png basn3p08.png basn6a08.png basn6a04.png >> check.lst
	cat check.lst | $(DTOU) | cmp $(srcdir)/test/test.lst
	@echo Success!

DISTDOS_ROOT = \
	doc/readme.txt doc/authors.txt doc/history.txt doc/copying.txt \
	advdef.exe advzip.exe advpng.exe advmng.exe

DISTDOS_DOC = \
	doc/advdef.txt doc/advzip.txt doc/advpng.txt doc/advmng.txt \
	doc/readme.txt doc/authors.txt doc/history.txt

distdos: $(DISTDOS_ROOT) $(DISTDOS_DOC)
	rm -f $(PACKAGE)-$(VERSION)-dos-x86.zip
	mkdir tmp
	cp $(DISTDOS_ROOT) tmp
	mkdir tmp/doc
	cp $(DISTDOS_DOC) tmp/doc
	cd tmp && zip -r ../$(PACKAGE)-$(VERSION)-dos-x86.zip *
	rm -r tmp

distwindows-x86: $(DISTDOS_ROOT) $(DISTDOS_DOC)
	rm -f $(PACKAGE)-$(VERSION)-windows-x86.zip
	mkdir tmp
	cp $(DISTDOS_ROOT) tmp
	mkdir tmp/doc
	cp $(DISTDOS_DOC) tmp/doc
	cd tmp && zip -r ../$(PACKAGE)-$(VERSION)-windows-x86.zip *
	rm -r tmp

distwindows-x64: $(DISTDOS_ROOT) $(DISTDOS_DOC)
	rm -f $(PACKAGE)-$(VERSION)-windows-x64.zip
	mkdir tmp
	cp $(DISTDOS_ROOT) tmp
	mkdir tmp/doc
	cp $(DISTDOS_DOC) tmp/doc
	cd tmp && zip -r ../$(PACKAGE)-$(VERSION)-windows-x64.zip *
	rm -r tmp

DISTWEB = \
	doc/advdef.hh doc/advzip.hh doc/advpng.hh doc/advmng.hh doc/history.hh

web: $(DISTWEB)

