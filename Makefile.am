AUTOMAKE_OPTIONS = check-news
ACLOCAL_AMFLAGS = -I local_m4

MNI_MODELS := mni-models

# mess with the data install directory
pkgdatadir = $(prefix)/share/ICBM

# installed data
pkgdata_DATA := \
	icbm_nlin_template_0.50mm.mnc \
	icbm_nlin_template_0.75mm.mnc \
	icbm_nlin_template_1.00mm.mnc \
	icbm_nlin_template_1.50mm.mnc \
	icbm_nlin_template_2.00mm.mnc \
	icbm_nlin_template_3.00mm.mnc \
	icbm_nlin_template_4.00mm.mnc \
	icbm_nlin_template_6.00mm.mnc \
	icbm_template_0.50mm.mnc \
	icbm_template_0.75mm.mnc \
	icbm_template_1.00mm.mnc \
	icbm_template_1.50mm.mnc \
	icbm_template_2.00mm.mnc \
	icbm_template_3.00mm.mnc \
	icbm_template_4.00mm.mnc \
	icbm_template_6.00mm.mnc

EXTRA_DIST = $(m4_files) \
	icbm_nlin_template_0.50mm.mnc.gz \
	icbm_nlin_template_0.75mm.mnc.gz \
	icbm_nlin_template_1.00mm.mnc.gz \
	icbm_nlin_template_1.50mm.mnc.gz \
	icbm_nlin_template_2.00mm.mnc.gz \
	icbm_nlin_template_3.00mm.mnc.gz \
	icbm_nlin_template_4.00mm.mnc.gz \
	icbm_nlin_template_6.00mm.mnc.gz \
	icbm_template_0.50mm.mnc.gz \
	icbm_template_0.75mm.mnc.gz \
	icbm_template_1.00mm.mnc.gz \
	icbm_template_1.50mm.mnc.gz \
	icbm_template_2.00mm.mnc.gz \
	icbm_template_3.00mm.mnc.gz \
	icbm_template_4.00mm.mnc.gz \
	icbm_template_6.00mm.mnc.gz \
	epm-header.in

m4_files = local_m4/ac_prog_gzip.m4

# be tidy
CLEANFILES = $(pkgdata_DATA)

# gunzip rule
%: %.gz
	$(gzip) -d -c $< > $@

#### all: $(dist_pkgdata_DATA:.gz=) $(DATE)
