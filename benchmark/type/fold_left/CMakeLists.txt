# Copyright Louis Dionne 2017
# Distributed under the Boost Software License, Version 1.0.
# (See accompanying file LICENSE.md or copy at http://boost.org/LICENSE_1_0.txt)

set(datasets)
add_dataset(datasets type fold_left brigand list   brigand.list.cpp.erb 40 "(0..50).step(10).to_a + (100..500).step(50).to_a")
add_dataset(datasets type fold_left kvasir  list   kvasir.list.cpp.erb  40 "(0..50).step(10).to_a + (100..500).step(50).to_a")
add_dataset(datasets type fold_left meta    list   meta.list.cpp.erb    40 "(0..50).step(10).to_a + (100..500).step(50).to_a")
add_dataset(datasets type fold_left metal   list   metal.list.cpp.erb   40 "(0..50).step(10).to_a + (100..500).step(50).to_a")
add_dataset(datasets type fold_left mp11    list   mp11.list.cpp.erb    40 "(0..50).step(10).to_a + (100..500).step(50).to_a")
add_dataset(datasets type fold_left mpl     list   mpl.list.cpp.erb     90 "(0..50).step(10)")
add_dataset(datasets type fold_left mpl     vector mpl.vector.cpp.erb   30 "(0..50).step(10)")
add_dataset(datasets type fold_left tmp     list   tmp.list.cpp.erb     40 "(0..50).step(10).to_a + (100..500).step(50).to_a")

add_chart(type fold_left DATASETS ${datasets})
