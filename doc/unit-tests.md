Compiling/running goobycoind unit tests
------------------------------------

goobycoind unit tests are in the `src/test/` directory; they
use the Boost::Test unit-testing framework.

To compile and run the tests:

	cd src
	make -f makefile.unix test_goobycoin  # Replace makefile.unix if you're not on unix
	./test_goobycoin   # Runs the unit tests

If all tests succeed the last line of output will be:
`*** No errors detected`

To add more tests, add `BOOST_AUTO_TEST_CASE` functions to the existing
.cpp files in the test/ directory or add new .cpp files that
implement new BOOST_AUTO_TEST_SUITE sections (the makefiles are
set up to add test/*.cpp to test_goobycoin automatically).


Compiling/running GoobyCoin-Qt unit tests
---------------------------------------

GoobyCoin-Qt unit tests are in the src/qt/test/ directory; they
use the Qt unit-testing framework.

To compile and run the tests:

	qmake goobycoin-qt.pro BITCOIN_QT_TEST=1
	make
	./goobycoin-qt_test

To add more tests, add them to the `src/qt/test/` directory,
the `src/qt/test/test_main.cpp` file, and goobycoin-qt.pro.
