# Mongilyov Andrey, report on Lab1, TIMP
curl -L https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz == output boost.tar.gz
tar -xf boost.tar.gz
ls boost_1_69_0 | wc -l
18
find boost_1_69_0 | sed -n '$='
66829
find boost_1_69_0 -name '*.hpp' | sed -n '$='
14912
find boost_1_69_0 -name '*.cpp' | sed -n '$='
13774
find boost_1_69_0 -not -name '*.hpp' -not -name '*.cpp' | sed -n '$='
38143
find boost_1_69_0 -name 'any.hpp'
boost_1_69_0/boost/fusion/include/any.hpp
boost_1_69_0/boost/fusion/algorithm/query/any.hpp
boost_1_69_0/boost/fusion/algorithm/query/detail/any.hpp
boost_1_69_0/boost/spirit/home/support/algorithm/any.hpp
boost_1_69_0/boost/proto/detail/any.hpp
boost_1_69_0/boost/type_erasure/any.hpp
boost_1_69_0/boost/hana/fwd/any.hpp
boost_1_69_0/boost/hana/any.hpp
boost_1_69_0/boost/any.hpp
boost_1_69_0/boost/xpressive/detail/utility/any.hpp
find boost_1_69_0 -name '*asio'
boost_1_69_0/boost/asio
boost_1_69_0/boost/asio.hpp
boost_1_69_0/boost/log/detail/asio_fwd.hpp
boost_1_69_0/boost/process/detail/posix/asio_fwd.hpp
boost_1_69_0/boost/process/detail/windows/asio_fwd.hpp
boost_1_69_0/libs/beast/doc/html/beast/using_io/asio_refresher.html
boost_1_69_0/libs/beast/doc/qbk/03_core/1_asio.qbk
boost_1_69_0/libs/asio
boost_1_69_0/libs/asio/doc/asio.qbk
boost_1_69_0/libs/fiber/examples/asio
boost_1_69_0/libs/fiber/doc/asio.qbk
boost_1_69_0/libs/fiber/doc/html/fiber/callbacks/then_there_s____boost_asio__.html
boost_1_69_0/libs/fiber/doc/html/fiber/integration/deeper_dive_into___boost_asio__.html
boost_1_69_0/boost_build_directory/include/boost/asio
boost_1_69_0/boost_build_directory/include/boost/asio.hpp
boost_1_69_0/boost_build_directory/include/boost/log/detail/asio_fwd.hpp
boost_1_69_0/boost_build_directory/include/boost/process/detail/posix/asio_fwd.hpp
boost_1_69_0/boost_build_directory/include/boost/process/detail/windows/asio_fwd.hpp
boost_1_69_0/doc/html/boost_asio
boost_1_69_0/doc/html/boost_asio/reference/asio_handler_invoke.html
boost_1_69_0/doc/html/boost_asio/reference/asio_handler_is_continuation.html
boost_1_69_0/doc/html/boost_asio/reference/is_error_code_enum_lt__boost__asio__ssl__error__stream_errors__gt_
boost_1_69_0/doc/html/boost_asio/reference/is_error_code_enum_lt__boost__asio__ssl__error__stream_errors__gt_.html
boost_1_69_0/doc/html/boost_asio/reference/asio_handler_deallocate.html
boost_1_69_0/doc/html/boost_asio/reference/asio_handler_allocate.html
boost_1_69_0/doc/html/boost_asio/reference/asio_handler_invoke
boost_1_69_0/doc/html/boost_asio.html
boost_1_69_0/doc/html/asio_HTML.manifest
./booststrap.sh --with-toolset=clang --prefix=~/boost_build_directory
./b2 install
cd boost_build_directory
ls
include lib
cd
mkdir boost-libs
mv boost_1_69_0/boost_build_directory/lib/* boost-libs
ls -l | sort -k5 -r | head
-rw-r--r--  1 mongilyov  staff  3063776 20 фев 23:53 libboost_wave.a
-rw-r--r--  1 mongilyov  staff  2384128 20 фев 23:53 libboost_log.a
-rw-r--r--  1 mongilyov  staff  2108048 20 фев 23:53 libboost_log_setup.a
-rwxr-xr-x  1 mongilyov  staff  1611456 20 фев 23:53 libboost_wave.dylib
-rw-r--r--  1 mongilyov  staff  1392112 20 фев 23:53 libboost_math_tr1f.a
-rw-r--r--  1 mongilyov  staff  1352488 20 фев 23:53 libboost_math_tr1l.a
-rw-r--r--  1 mongilyov  staff  1352440 20 фев 23:53 libboost_math_tr1.a
-rw-r--r--  1 mongilyov  staff  1326536 20 фев 23:53 libboost_test_exec_monitor.a
-rw-r--r--  1 mongilyov  staff  1314392 20 фев 23:53 libboost_unit_test_framework.a
-rwxr-xr-x  1 mongilyov  staff  1273413 20 фев 23:53 libboost_log_setup.dylib
