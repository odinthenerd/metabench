# Copyright Bruno Dutra 2016
# Distributed under the Boost Software License, Version 1.0.
# (See accompanying file LICENSE.md or copy at http://boost.org/LICENSE_1_0.txt)

set(datasets)
add_dataset(datasets type replace_if brigand list   brigand.list.cpp.erb 12 "(0..50).step(10).to_a + (100..500).step(50).to_a")
add_dataset(datasets type replace_if hana    types  hana.types.cpp.erb   12 "(0..50).step(10).to_a + (100..500).step(50).to_a")
add_dataset(datasets type replace_if kvasir  list   kvasir.list.cpp.erb  12 "(0..50).step(10).to_a + (100..500).step(50).to_a")
add_dataset(datasets type replace_if meta    list   meta.list.cpp.erb    12 "(0..50).step(10).to_a + (100..500).step(50).to_a")
add_dataset(datasets type replace_if metal   list   metal.list.cpp.erb   12 "(0..50).step(10).to_a + (100..500).step(50).to_a")
add_dataset(datasets type replace_if mp11    list   mp11.list.cpp.erb    12 "(0..50).step(10).to_a + (100..500).step(50).to_a")
add_dataset(datasets type replace_if mpl     list   mpl.list.cpp.erb     10 "(0..50).step(10)")
add_dataset(datasets type replace_if mpl     vector mpl.vector.cpp.erb   10 "(0..50).step(10)")
add_dataset(datasets type replace_if tmp     list   tmp.list.cpp.erb     12 "(0..50).step(10).to_a + (100..500).step(50).to_a")

add_chart(type replace_if DATASETS ${datasets})
