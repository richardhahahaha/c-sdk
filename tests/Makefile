SOURCE_FILES=\
	../b64/urlsafe_b64.c\
	../cJSON/cJSON.c\
	../qbox/conf.c\
	../qbox/base.c\
	../qbox/base_io.c\
	../qbox/oauth2.c\
	../qbox/oauth2_digest.c\
	../qbox/rs.c\
	../qbox/rs_token.c\
	../qbox/io.c\
	test.c\

CUNIT_LIB=../CUnit/CUnit/Sources/.libs

all: $(SOURCE_FILES)
	gcc $^ -o qiniutest -L$(CUNIT_LIB) -lcurl -lssl -lcrypto -lcunit -lm

install: all
	@echo

clean:
	rm -f test

test: all
	LD_LIBRARY_PATH=$(CUNIT_LIB) ./qiniutest

