# TbpgrUtils

[![Gem Version](https://badge.fury.io/rb/tbpgr_utils.svg)](http://badge.fury.io/rb/tbpgr_utils)
[![Build Status](https://travis-ci.org/tbpgr/tbpgr_utils.png?branch=master)](https://travis-ci.org/tbpgr/tbpgr_utils)
[![Coverage Status](https://coveralls.io/repos/tbpgr/tbpgr_utils/badge.png)](https://coveralls.io/r/tbpgr/tbpgr_utils)
[![Code Climate](https://codeclimate.com/github/tbpgr/tbpgr_utils.png)](https://codeclimate.com/github/tbpgr/tbpgr_utils)

TbpgrUtils is Utilities.

## Installation

Add this line to your application's Gemfile:

    gem 'tbpgr_utils'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install tbpgr_utils

## Usage
### List
| class/module/method                                                                                               | mean                                                                                                                |
|:-----------                                                                                                       |:------------                                                                                                        |
|[TbpgrUtils Array#>>](#array)                                                                                      |return ArrayContext for each execute                                                                                 |
|[TbpgrUtils Array#average](#arrayaverage)                                                                          |return average                                                                                                       |
|[TbpgrUtils Array#exchange](#arrayexchange )                                                                       |exchange array's elements                                                                                            |
|[TbpgrUtils Array#to_table](#arrayto_table)                                                                        |Array(Array, Array...) to table format.                                                                              |
|[TbpgrUtils Array#to_html_table](#arrayto_html_table)                                                              |Array(Array, Array...) to html table format.                                                                         |
|[TbpgrUtils Array#together](#arraytogether)                                                                        |loop all arrays by block                                                                                             |
|[TbpgrUtils Array#together_at](#arraytogether_at)                                                                  |together version of Array#at. together_at has alias :tat                                                             |
|[TbpgrUtils Array#together_clear](#arraytogether_clear)                                                            |together version of Array#clear. together_clear has alias :tclear                                                    |
|[TbpgrUtils Array#together_compact](#arraytogether_compact)                                                        |together version of Array#compact. together_compact has alias :tcompact. this is immutable.                          |
|[TbpgrUtils Array#together_compact!](#arraytogether_compact-1)                                                     |together version of Array#compact!. together_compact! has alias :tcompact! this is mutable.                          |
|[TbpgrUtils Array#together_concat](#arraytogether_concat)                                                          |together version of Array#concat. together_concat has alias :tconcat                                                 |
|[TbpgrUtils Array#together_delete](#arraytogether_delete)                                                          |together version of Array#delete. together_delete has alias :tdelete                                                 |
|[TbpgrUtils Array#together_delete_at](#arraytogether_delete_at)                                                    |together version of Array#delete_at. together_delete_at has alias :tdelete_at                                        |
|[TbpgrUtils Array#together_delete_if](#arraytogether_delete_if)                                                    |together version of Array#delete_if. together_delete_if has alias :tdelete_if                                        |
|[TbpgrUtils Array#together_empty?](#arraytogether_empty)                                                           |together version of Array#empty?. together_empty? has alias :tempty?                                                 |
|[TbpgrUtils Array#together_fill](#arraytogether_fill)                                                              |together version of Array#fill. together_fill has alias :tfill                                                       |
|[TbpgrUtils Array#together_first](#arraytogether_first)                                                            |together version of Array#first. together_first has alias :tfirst                                                    |
|[TbpgrUtils Array#together_include?](#arraytogether_include)                                                       |together version of Array#include?. together_include? has alias :tinclude?                                           |
|[TbpgrUtils Array#together_index](#arraytogether_index)                                                            |together version of Array#index. together_index has alias :tindex                                                    |
|[TbpgrUtils Array#together_insert](#arraytogether_insert)                                                          |together version of Array#insert. together_insert has alias :tinsert                                                 |
|[TbpgrUtils Array#together_last](#arraytogether_last)                                                              |together version of Array#last. together_last has alias :tlast                                                       |
|[TbpgrUtils Array#together_map](#arraytogether_mapor-tmap-together_collect-tcollect)                               |together version of Enumerable#map. together_map has aliases [:tmap, :together_collect, :tcollect]                   |
|[TbpgrUtils Array#together_map!](#arraytogether_mapor-tmap-together_collect-tcollect-1)                            |together version of Enumerable#map!. together_map! has aliases [:tmap!, :together_collect!, :tcollect!]              |
|[TbpgrUtils Array#together_pop](#arraytogether_popor-tpop)                                                         |together version of Array#pop. together_pop has alias :tpop                                                          |
|[TbpgrUtils Array#together_reduce](#arraytogether_reduceor-treduce-together_inject-tinject)                        |together version of Enumerable#reduce. together_reduce has aliases [:treduce, :together_inject, :tinject]            |
|[TbpgrUtils Array#together_reverse](#arraytogether_reverseor-treverse)                                             |together version of Array#reverse. together_reverse has alias :treverse                                              |
|[TbpgrUtils Array#together_reverse!](#arraytogether_reverseor-treverse-1)                                          |together version of Array#reverse!. together_reverse! has alias :treverse!                                           |
|[TbpgrUtils Array#together_sample](#arraytogether_sampleor-tsample)                                                |together version of Array#sample. together_sample has alias :tsample                                                 |
|[TbpgrUtils Array#together_select](#arraytogether_selector-tselect-together_find_all-tfindall)                     |together version of Enumerable#select. together_select has aliases [:tselect, :together_find_all, :tfindall]         |
|[TbpgrUtils Array#together_shift](#arraytogether_shift)                                                            |together version of Array#shift. together_shift has alias :tshift                                                    |
|[TbpgrUtils Array#together_shuffle](#arraytogether_shuffleor-tshuffle)                                             |together version of Array#shuffle. together_shuffle has alias :tshuffle                                              |
|[TbpgrUtils Array#together_slice](#arraytogether_sliceor-tslice)                                                   |together version of Array#slice. together_slice has alias :tslice                                                    |
|[TbpgrUtils Array#together_with_index](#arraytogether_with_index)                                                  |loop all arrays by block with index                                                                                  |
|[TbpgrUtils Array#uniq_size](#arrayuniq_size)                                                                      |return uniq size                                                                                                     |
|[TbpgrUtils Enumerable#if_else_map](#enumerableif_else_map)                                                        |alias of map {|v|v.condition ? a : b}                                                                                |
|[TbpgrUtils Enumerable#kernel_send](#enumerablekernel_send)                                                        |alias of map {|v|send :some_kernel_method, v}                                                                        |
|[TbpgrUtils Enumerable#sum](#enumerablesum)                                                                        |alias of Enumerable#reduce(&:+).                                                                                     |
|[AttrEnumerable.at_attr](#attrenumerableat_attr)                                                                   |define at_xxx. it returns Class attributes(collection)'s at result.                                                  |
|[AttrEnumerable.compact_attr](#attrenumerablecompact_attr)                                                         |define compact_xxx. it returns Class attributes(collection)'s that exclude nil elements.                             |
|[AttrEnumerable.concat_attr](#attrenumerableconcat_attr)                                                           |define concat_xxx. it returns Class attributes(collection) and argument array                                        |
|[AttrEnumerable.delete_attr](#attrenumerabledelete_attr)                                                           |define delete_xxx. it delete Class attributes(collection) that match delete condition                                |
|[AttrEnumerable.first_attr](#attrenumerablefirst_attr)                                                             |define first_xxx. it returns Class attributes(collection) first N element                                            |
|[AttrEnumerable.each_attr](#attrenumerableeach_attr)                                                               |define each_xxx. it call Class attributes(collection)'s attribute iterator                                           |
|[AttrEnumerable.each_attr_with_index](#attrenumerableeach_attr_with_index)                                         |define each_xxx_with_index. it call Class attributes(collection)'s attribute iterator with index                     |
|[AttrEnumerable.include_attr?](#attrenumerableinclude_attr)                                                        |define include_xxx?. it returns Class attributes(collection)'s attribute include value                               |
|[AttrEnumerable.last_attr](#attrenumerablelast_attr)                                                               |define last_xxx. it returns Class attributes(collection) last N elementt                                             |
|[AttrEnumerable.reverse_attr](#attrenumerablereverse_attr)                                                         |define reverse_xxx. it returns Class attributes(collection)'s reverse Array                                          |
|[AttrEnumerable.map_attr](#attrenumerablemap_attr)                                                                 |define map_xxx. it returns Class attributes(collection)'s Array map each value                                       |
|[AttrEnumerable.reduce_attr](#attrenumerablereduce_attr)                                                           |define reduce_xxx. it returns Class attributes(collection)'s Array reduce each value                                 |
|[AttrEnumerable.sample_attr](#attrenumerablesample_attr)                                                           |define sample_xxx. it returns Class attributes(collection)'s Array sample value                                      |
|[AttrEnumerable.select_attr](#attrenumerableselect_attr)                                                           |define select_xxx. it returns Class attributes(collection)'s Array select value                                      |
|[AttrEnumerable.shuffle_attr](#attrenumerableshuffle_attr)                                                         |define shuffle_xxx. it returns Class attributes(collection)'s Array shuffle value                                    |
|[AttrEnumerable.slice_attr](#attrenumerableslice_attr)                                                             |define slice_xxx. it returns Class attributes(collection)'s Array slice value                                        |
|[AttributesHashable.to_hash](#attributeshashableto_hash)                                                           |define to_hash method for get instance_values                                                                        |
|[AttributesInitializable::ClassMethods.attr_accessor_init](#attributesinitializableclassmethodsattr_accessor_init) |generate attr_accessor + initializer                                                                                 |
|[AttributesInitializable::ClassMethods.attr_reader_init](#attributesinitializableclassmethodsattr_reader_init)     |generate attr_reader + initializer                                                                                   |
|[AttributesInitializable::ClassMethods.attr_writer init](#attributesinitializableclassmethodsattr_writer_init)     |generate attr_writer + initializer                                                                                   |
|[EndERB.apply](#enderbapply)                                                                                       |for single template script using __END__ and DATA                                                                    |
|[EvalHelper Object](#evalhelper-object)                                                                            |enable to use EvalHelper in Object                                                                                   |
|[EvalHelper#attr_accessor_init_code](#evalhelperattr_accessor_init_code)                                           |create attr_accessor + initialize code, for eval                                                                     |
|[EvalHelper#each_do_code](#evalhelpereach_do_code)                                                                 |create each do code, for eval                                                                                        |
|[EvalHelper#each_brace_code](#evalhelpereach_brace_code)                                                           |create each brace single line code, for eval                                                                         |
|[EvalHelper#each_with_index_brace_code](#evalhelpereach_with_index_brace_code)                                     |create eachwith_index_ brace single line code, for eval                                                              |
|[EvalHelper#each_with_index_do_code](#evalhelpereach_with_index_do_code)                                           |create eachwith_index_ do code, for eval                                                                             |
|[EvalHelper#if_code](#evalhelperif_code)                                                                           |create if strings, for eval                                                                                          |
|[EvalHelper#if_code_after](#evalhelperif_code_after)                                                               |create after-if strings, for eval                                                                                    |
|[EvalHelper#require_code](#evalhelperrequire_code)                                                                 |create require strings, for eval                                                                                     |
|[EvalHelper#require_relative_code](#evalhelperrequire_relative_code)                                               |create require_relative strings, for eval                                                                            |
|[EvalHelper#set_variable_code](#evalhelperset_variable_code)                                                       |create set_variable_code strings, for eval                                                                           |
|[EvalHelper#set_variables_code](#evalhelperset_variables_code)                                                     |create set_variables_code strings, for eval                                                                          |
|[EvalHelper#times_code](#evalhelpertimes_code)                                                                     |create times_code strings, for eval                                                                                  |
|[EvalHelper#ternary_operator](#evalhelperternary_operator)                                                         |create ternary operator strings, for eval                                                                            |
|[EvalHelper#unless_code](#evalhelperunless_code)                                                                   |create unless strings, for eval                                                                                      |
|[EvalHelper#unless_code_after](#evalhelperunless_code_after)                                                       |create after-unless strings, for eval                                                                                |
|[Familyable](#familyable)                                                                                          |user family model(family, person, parents, children, brothers)                                                       |
|[TbpgrUtils Fixnum to_fixnum_html_table](#fixnum-to_fixnum_html_table)                                             |return value is fixnum html table                                                                                    |
|[TbpgrUtils Fixnum to_fixnum_table](#fixnumto_fixnum_table)                                                        |return value is fixnum table                                                                                         |
|[Ghostable module](#ghostable)                                                                                     |help to create ghost method(dynamic method define by ussing method_missing + pattern-method-name)                    |
|[TbpgrUtils Hash#>>](#hash)                                                                                        |return HashContext for each execute                                                                                  |
|[TbpgrUtils Hash#html_table](#hashhtml_table)                                                                      |get html table string from key + value                                                                               |
|[TbpgrUtils Hash#table](#hashtable)                                                                                |get pipe format table string from key + value                                                                        |
|[TbpgrUtils Integer#each_digit](#integereach_digit)                                                                |provide iterator for number's each digit                                                                             |
|[TbpgrUtils Integer#each_digit_with_index](#integereach_digit_with_index)                                          |provide iterator for number's each digit with index                                                                  |
|[TbpgrUtils Integer#palindromic_prime?](#integerpalindromic_prime)                                                 |Returns true if value is palindromic prime, false for a composite.                                                   |
|[TbpgrUtils Integer#reverse_each_digit](#integerreverse_each_digit)                                                |provide reverse iterator for number's each digit                                                                     |
|[TbpgrUtils Kernel booleans](#kerne-booleans)                                                                      |True or False instance aliases.                                                                                      |
|[TbpgrUtils Kernel#bulk_define_methods](#kernelbulk_define_methods)                                                |define methods to classes. methods have simple return value.                                                         |
|[TestToolbox Kernel#capture_stdout](#kernelcapture_stdout)                                                         |capture STDOUT                                                                                                       |
|[TestToolbox Kernel#dp_line](#kerneldp_line)                                                                       |debug print line for print-debugging                                                                                 |
|[TbpgrUtils Kernel#aa_ancestors](#kernelaa_ancestors)                                                              |Ascii Art Ancestors                                                                                                  |
|[TbpgrUtils Kernel#bulk_puts_eval](#kernelbulk_puts_eval)                                                          |Puts each-line-code + eval result                                                                                    |
|[TbpgrUtils Kernel#evalb](#kernelevalb)                                                                            |eval block version                                                                                                   |
|[TbpgrUtils Kernel#exchange](#kernelexchange)                                                                      |exchange variable a for b                                                                                            |
|[TbpgrUtils Kernel#hash_to_attributes](#kernelhash_to_attributes)                                                  |set attributes from hash                                                                                             |
|[TbpgrUtils Kernel#null](#kernelnull)                                                                              |null is alias of nil                                                                                                 |
|[TbpgrUtils Kernel#print_eval](#kernelprint_eval)                                                                  |Print code + eval result                                                                                             |
|[TbpgrUtils Kernel#puts_eval](#kernelputs_eval)                                                                    |Puts code + eval result                                                                                              |
|[MarkdownString.backquotes](#markdownstringbackquotes)                                                             |Return markdown backquotes                                                                                           |
|[MarkdownString.bold](#markdownstringbold)                                                                         |Return markdown bold                                                                                                 |
|[MarkdownString.code](#markdownstringcode)                                                                         |Return markdown code                                                                                                 |
|[MarkdownString.codes](#markdownstringcodes)                                                                       |Return markdown codes                                                                                                |
|[MarkdownString.heading1](#markdownstringheading1)                                                                 |Return markdown heading level1 from text                                                                             |
|[MarkdownString.heading2](#markdownstringheading2)                                                                 |Return markdown heading level2 from text                                                                             |
|[MarkdownString.heading3](#markdownstringheading3)                                                                 |Return markdown heading level3 from text                                                                             |
|[MarkdownString.heading4](#markdownstringheading4)                                                                 |Return markdown heading level4 from text                                                                             |
|[MarkdownString.heading5](#markdownstringheading5)                                                                 |Return markdown heading level5 from text                                                                             |
|[MarkdownString.heading6](#markdownstringheading6)                                                                 |Return markdown heading level6 from text                                                                             |
|[MarkdownString.hr](#markdownstringhr)                                                                             |Return markdown hr                                                                                                   |
|[MarkdownString.italic](#markdownstringitalic)                                                                     |Return markdown italic                                                                                               |
|[MarkdownString.link](#markdownstringlink)                                                                         |Return markdown link                                                                                                 |
|[MarkdownString.ol](#markdownstringol)                                                                             |Return markdown ol from array                                                                                        |
|[MarkdownString.ul](#markdownstringul)                                                                             |Return markdown ul from array                                                                                        |
|[MetasyntacticVariable](#metasyntacticvariable)                                                                    |META variable, META variable for classes                                                                             |
|[TbpgrUtils Module.alias_methods](#modulealias_methods)                                                            |create alias methods                                                                                                 |
|[TbpgrUtils Numeric#dice_back](#numericdice_back)                                                                  |return dice back number                                                                                              |
|[TbpgrUtils Numeric#dozen](#numericdozen)                                                                          |get dozen number                                                                                                     |
|[TbpgrUtils Numeric#ascii?](#numericascii)                                                                         |get ascii number                                                                                                     |
|[TbpgrUtils Numeric to_binary_html_table](#numeric-to_binary_html_table)                                           |binary html table                                                                                                    |
|[TbpgrUtils Numeric to_binary_table](#numeric-to_binary_table)                                                     |binary table                                                                                                         |
|[TbpgrUtils Numeric to_digit_html_table](#numeric-to_digit_html_table)                                             |digit html table                                                                                                     |
|[TbpgrUtils Numeric to_digit_table](#numeric-to_digit_table)                                                       |digit table                                                                                                          |
|[TbpgrUtils Numeric to_hex_html_table](#numeric-to_hex_html_table)                                                 |hex html table                                                                                                       |
|[TbpgrUtils Numeric to_hex_table](#numeric-to_hex_table)                                                           |hex table                                                                                                            |
|[TbpgrUtils Numeric to_oct_html_table](#numeric-to_oct_html_table)                                                 |oct html table                                                                                                       |
|[TbpgrUtils Numeric to_oct_table](#numeric-to_oct_table)                                                           |oct table                                                                                                            |
|[TbpgrUtils Object#any_of?](#objectany_of)                                                                         |if self match any one of items, return true                                                                          |
|[TbpgrUtils Object#boolean?](#objectboolean)                                                                       |data type check for boolean                                                                                          |
|[TbpgrUtils Object#grep_method](#objectgrep_method)                                                                |grep class method                                                                                                    |
|[TbpgrUtils Object#grep_private_instance_method](#objectgrep_private_instance_method)                              |grep private instance method                                                                                         |
|[TbpgrUtils Object#grep_protected_instance_method](#objectgrep_protected_instance_method)                          |grep protected instance method                                                                                       |
|[TbpgrUtils Object#grep_public_instance_method](#objectgrep_public_instance_method)                                |grep public instance method                                                                                          |
|[TbpgrUtils Object#guard](#objectguard)                                                                            |data type check for guard                                                                                            |
|[TbpgrUtils Object#method_nameable?](#objectmethod_nameable)                                                       |object can use method name or not                                                                                    |
|[TbpgrUtils Object#my_methods](#objectmy_methods)                                                                  |return public/protected/private self define methods                                                                  |
|[TbpgrUtils Object#null?](#objectnull)                                                                             |null? is alias of nil?                                                                                               |
|[TbpgrUtils Object#to_bool](#objectto_bool)                                                                        |syntax sugar of !!. convert [false, nil] => fasel, other => true.                                                    |
|[TbpgrUtils Object#unless_guard](#objectunless_guard)                                                              |data type check for unless_guard                                                                                     |
|[SimpleTournament](#simpletournament)                                                                              |simple tournament                                                                                                    |
|[TbpgrUtils String.>>](#string)                                                                                    |self converto to Array. and execute method                                                                           |
|[TbpgrUtils String#ascii1_other2_size](#stringascii1_other2_size)                                                  |count string size. ascii => count1, not ascii => count2                                                              |
|[TbpgrUtils String#ascii_unicode_html_table](#stringascii_unicode_html_table)                                      |get ascii_unicode_html_table                                                                                         |
|[TbpgrUtils String#ascii_unicode_table](#stringascii_unicode_table)                                                |get ascii_unicode_table                                                                                              |
|[TbpgrUtils String#comma_to_a](#stringcomma_to_a)                                                                  |comma-format string to array                                                                                         |
|[TbpgrUtils String#cygwinpath_to_winpath](#stringcygwinpath_to_winpath)                                            |convert cygwin path to windows path                                                                                  |
|[TbpgrUtils String#escape_quote](#stringescape_quote)                                                              |escape quote                                                                                                         |
|[TbpgrUtils String#escape_double_quote](#stringescape_double_quote)                                                |escape double quote                                                                                                  |
|[TbpgrUtils String#hyphen_to_a](#stringhyphen_to_a)                                                                |hyphen-format string to array                                                                                        |
|[TbpgrUtils String#meta_variable?](#stringmeta_variable)                                                           |is meta variable.                                                                                                    |
|[TbpgrUtils String#justify_char](#stringjustify_char)                                                              |justify pipe format char string                                                                                      |
|[TbpgrUtils String#justify_table](#stringjustify_table)                                                            |justify pipe format table string                                                                                     |
|[TbpgrUtils String#say](#stringsay)                                                                                |say string                                                                                                           |
|[TbpgrUtils String#spacing](#stringspacing)                                                                        |get spacing string                                                                                                   |
|[TbpgrUtils String#stripe](#stringstripe)                                                                          |stripe string                                                                                                        |
|[TbpgrUtils String#surround](#stringsurround)                                                                      |surround string                                                                                                      |
|[TbpgrUtils String#table_to_array](#stringtable_to_array)                                                          |convert table format string to array.                                                                                |
|[TbpgrUtils String#to_hatena_heading](#stringto_hatena_heading)                                                    |create hatena-format heading string with Emmet-like grammar                                                          |
|[TbpgrUtils String#to_markdown_heading](#stringto_markdown_heading)                                                |create markdown-format heading string with Emmet-like grammar                                                        |
|[TbpgrUtils String#to_space2_heading](#stringto_space2_heading)                                                    |create space2-format heading string with Emmet-like grammar                                                          |
|[TbpgrUtils String#to_space4_heading](#stringto_space4_heading)                                                    |create space4-format heading string with Emmet-like grammar                                                          |
|[TbpgrUtils String#to_tab_heading](#stringto_tab_heading)                                                          |create tab-format heading string with Emmet-like grammar                                                             |
|[TbpgrUtils String#unescape_double_quote](#stringunescape_double_quote)                                            |unescape double quote                                                                                                |
|[TbpgrUtils String#uniq](#stringuniq)                                                                              |return uniq string                                                                                                   |
|[TbpgrUtils String#uniq_size](#stringuniq)                                                                         |return uniq size                                                                                                     |
|[TbpgrUtils String#winpath_to_cygwinpath](#stringwinpath_to_cygwinpath)                                            |convert windows path to cygwin path                                                                                  |
|[TbpgrUtils Symbol#meta_variable?](#symbolmeta_variable)                                                           |is meta variable.                                                                                                    |
|[Templatable module](#templatable)                                                                                 |get result from template + placeholder                                                                               |
|[TemplateMethodable module](#templatemethodable)                                                                   |for Template Method Pattern                                                                                          |

### Array#>>
~~~ruby
require 'tbpgr_utils'
[*'a'..'c'].>>.ord # => [97, 98, 99]
[*'aa'..'ac'].>>.gsub("a", "c") # => ['cc', 'cb', 'cc']
~~~

[back to list](#list)

### Array#average
~~~ruby
require 'tbpgr_utils'
[*1..6].average # => 3.5
[1.5, 2.5].average # => 2.0
[*'a'..'z'].average # => raise TypeError
~~~

[back to list](#list)

### Array#exchange
~~~ruby
require 'tbpgr_utils'
[*1..6].exchange!(1, 5) # => [1, 6, 3, 4, 5, 2]
[*1..6].exchange!(1, -1) # => [1, 6, 3, 4, 5, 2]
[*1..6].exchange!(1, 6) # => [*1..6]
[].exchange!(1, 2) # => []
~~~

[back to list](#list)

### Array#to_table
~~~ruby
require 'tbpgr_utils'
[['header1', 'header2', 'header3'],['line1_1', 'line1_2', 'line1_3']].to_table
~~~

result  
~~~
|header1|header2|header3|
|line1_1|line1_2|line1_3|
~~~

[back to list](#list)

### Array#to_html_table
~~~ruby
[['header1', 'header2', 'header3'],['line1_1', 'line1_2', 'line1_3']].to_html_table
~~~

result  
~~~
<table>
  <tr>
    <th>header1</th>
    <th>header2</th>
    <th>header3</th>
  </tr>
  <tr>
    <td>line1_1</td>
    <td>line1_2</td>
    <td>line1_3</td>
  </tr>
</table>
~~~

no header case
~~~ruby
[['not_header1', 'not_header2', 'not_header3'],['line1_1', 'line1_2', 'line1_3']].to_html_table({no_header: true})
~~~

result  
~~~
<table>
  <tr>
    <td>not_header1</td>
    <td>not_header2</td>
    <td>not_header3</td>
  </tr>
  <tr>
    <td>line1_1</td>
    <td>line1_2</td>
    <td>line1_3</td>
  </tr>
</table>
~~~


[back to list](#list)

### Array#together
~~~ruby
require 'tbpgr_utils'

alpha = %w{one two three}
numbers = %w{1 4 3}
[alpha, numbers].together do |first, second|
  print "#{first}:#{second}\n"  # => output one:1, two:2, three:3
end
~~~

[back to list](#list)

### Array#together_at
~~~ruby
require 'tbpgr_utils'

# same elements size case
alpha = %w{one two three}
numbers = %w{1 2 3}
print [alpha, numbers].together_at 2 # => output ['three', 3]

# different elements size case
alpha = %w{one two three}
numbers = %w{1 2}
print [alpha, numbers].together_at 2 # => output ['three', nil]
~~~

[back to list](#list)

### Array#together_clear
~~~ruby
require 'tbpgr_utils'

alpha = %w{one two three}
numbers = %w{1 2 3}
[alpha, numbers].together_clear # => [[], []]
~~~

[back to list](#list)

### Array#together_compact
~~~ruby
require 'tbpgr_utils'

alpha = ['a','b','c', nil,'d']
numbers = [1, 2, nil, 3]
lists = [alpha, numbers]
ret = lists.together_compact
print lists # => output [['a','b','c', nil,'d'], [1, 2, nil, 3]]
print ret # => output [['a','b','c','d'], [1, 2, 3]]
~~~

[back to list](#list)

### Array#together_compact!
~~~ruby
require 'tbpgr_utils'

alpha = ['a','b','c', nil,'d']
numbers = [1, 2, nil, 3]
lists = [alpha, numbers]
ret = lists.together_compact!
print lists # => output [['a','b','c','d'], [1, 2, 3]]
print ret # => output [['a','b','c','d'], [1, 2, 3]]
~~~

[back to list](#list)

### Array#together_concat
~~~ruby
require 'tbpgr_utils'

alpha = %w{one two three}
numbers = %w{1 2 3}
[alpha, numbers].together_concat [4, 5, 6]

print alpha # => ["one", "two", "three", 4, 5, 6]
print numbers # => ["1", "2", "3", 4, 5, 6]
~~~

[back to list](#list)

### Array#together_delete
~~~ruby
require 'tbpgr_utils'

child1 = [1, 2, 3, 4]
child2 = [2, 3, 4, 5]
lists = [child1, child2]
ret = lists.together_delete 2
print lists # => output [[1, 3, 4], [3, 4, 5]]
~~~

if delete target is not exist  
~~~ruby
require 'tbpgr_utils'

child1 = [1, 2, 3, 4]
child2 = [2, 3, 4, 5]
lists = [child1, child2]
ret = lists.together_delete 6
print ret # => nil
print lists # => output [[1, 2, 3, 4], [2, 3, 4, 5]]
~~~

if delete target is not exist and use block  
~~~ruby
require 'tbpgr_utils'

child1 = [1, 2, 3, 4]
child2 = [2, 3, 4, 5]
lists = [child1, child2]
ret = lists.together_delete(6) { 999 }
print ret # => 999
print lists # => output [[1, 2, 3, 4], [2, 3, 4, 5]]
~~~

[back to list](#list)

### Array#together_delete_at
if delete_at target is exist  
~~~ruby
require 'tbpgr_utils'

child1 = [1, 2, 3, 4]
child2 = [2, 3, 4, 5]
lists = [child1, child2]
ret = lists.together_delete_at 2
print ret # => [3, 4]
print lists # => output [[1, 2, 4], [2, 3, 5]]
~~~

if delete_at target is not exist  
~~~ruby
require 'tbpgr_utils'

child1 = [1, 2, 3, 4]
child2 = [2, 3, 4, 5]
lists = [child1, child2]
ret = lists.together_delete_at 6
print ret # => [nil, nil]
print lists # => output [[1, 2, 3, 4], [2, 3, 4, 5]]
~~~

if delete_at target is exist(minus index)  
~~~ruby
require 'tbpgr_utils'

child1 = [1, 2, 3, 4]
child2 = [2, 3, 4, 5]
lists = [child1, child2]
ret = lists.together_delete_at -3
print ret # => [2, 3]
print lists # => output [[1, 3, 4], [2, 4, 5]]
~~~

[back to list](#list)

### Array#together_delete_if
if delete_if target is exist  
~~~ruby
require 'tbpgr_utils'

lists = [[1, 2, 3, 4], [6, 4, 6, 8]]
ret = lists.together_delete_if {|first, second|(first + second).odd?}
print ret # => [[2, 4], [4, 8]]
~~~

if delete_if target is not exist. return nil.  
~~~ruby
require 'tbpgr_utils'

lists = [[2, 2, 4, 4], [6, 4, 6, 8]]
ret = lists.together_delete_if {|first, second|(first + second).odd?}
print ret # => nil
~~~

[back to list](#list)

### Array#together_empty?
empty case  
~~~ruby
require 'tbpgr_utils'

lists = [[], []]
ret = lists.together_empty?
print ret # => true
~~~

not empty case  
~~~ruby
require 'tbpgr_utils'

lists = [[1], []]
ret = lists.together_empty?
print ret # => false
~~~

[back to list](#list)

### Array#together_fill
not use block case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*6..10]]
ret = lists.together_fill(99)
print ret # => [[99, 99, 99, 99, 99], [99, 99, 99, 99, 99]]
~~~

use block, no args case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*6..10]]
ret = lists.together_fill { |i|(i + 1) + 1 }
print ret # => [[2, 3, 4, 5, 6], [2, 3, 4, 5, 6]]
~~~

use block, has args case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*6..10]]
ret = lists.together_fill(2) { |i|(i + 1) + 1 }
print ret # => [[1, 2, 4, 5, 6], [6, 7, 4, 5, 6]]
~~~

[back to list](#list)

### Array#together_first
no args case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*6..10]]
ret = lists.together_first
print ret # => [1, 6]
~~~

has args 2 case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*6..10]]
ret = lists.together_first 2
print ret # => [[1, 2], [6, 7]]
~~~

has args 0 case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*6..10]]
ret = lists.together_first 0
print ret # => [[], []]
~~~

has args over size case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*6..10]]
ret = lists.together_first 6
print ret # => [[*1..5], [*6..10]]
~~~

[back to list](#list)

### Array#together_include?
together_include? is bulk version of Array#include?

together_include? has alias :tinclude?

both include single ret case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*5..9]]
ret = lists.together_include? 5
print ret # => true
~~~

one include single ret case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*5..9]]
ret = lists.together_include? 9
print ret # => true
~~~

both not include single ret case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*5..9]]
ret = lists.together_include? 10
print ret # => false
~~~

both include multi ret case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*5..9]]
ret = lists.together_include? 5, true
print ret # => [true, true]
~~~

one include multi ret case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*5..9]]
ret = lists.together_include? 9, true
print ret # => [false, true]
~~~

both not include multi ret case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*5..9]]
ret = lists.together_include? 10, true
print ret # => [false, false]
~~~

[back to list](#list)

### Array#together_index
together_index has alias :tindex

both index exist case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*5..9]]
ret = lists.together_index 5
print ret # => [4, 0]
~~~

one include single ret case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*5..9]]
ret = lists.together_index 4
print ret # => [3, nil]
~~~

both not include single ret case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*5..9]]
ret = lists.together_index 10
print ret # => [nil, nil]
~~~

[back to list](#list)

### Array#together_insert
together_insert has alias :tinsert

both insert exist case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*5..9]]
ret = lists.together_insert(1, 55, 66)
print ret # => [[1, 55, 66, 2, 3, 4, 5], [5, 55, 66, 6, 7, 8, 9]]
~~~

both insert exist and minus index case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*5..9]]
ret = lists.together_insert(-2, 55, 66)
print ret # => [[1, 2, 3, 4, 55, 66, 5], [5, 6, 7, 8, 55, 66, 9]]
~~~

both insert exist case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*5..9]]
ret = lists.together_insert(6, 55, 66)
print ret # => [[1, 2, 3, 4, 5, nil, 55, 66], [5, 6, 7, 8, 9, nil, 55, 66]],
~~~

[back to list](#list)

### Array#together_last
together_last has alias :tlast

no args case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*6..10]]
ret = lists.together_last
print ret # => [5, 10]
~~~

has args 2 case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*6..10]]
ret = lists.together_last 2
print ret # => [[4, 5], [9, 10]]
~~~

has args 0 case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*6..10]]
ret = lists.together_last 0
print ret # => [[], []]
~~~

has args over size case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*6..10]]
ret = lists.together_last 6
print ret # => [[*1..5], [*6..10]]
~~~

[back to list](#list)

### Array#together_map(or tmap, together_collect, tcollect)
~~~ruby
require 'tbpgr_utils'

alpha = %w{one two three}
numbers = %w{1 2 3}
ret = [alpha, numbers].together_map {|first, second|"#{first}:#{second}"}
print ret # => output [one:1, two:2, three:3]
~~~

if you want to return multi array, following.  
~~~ruby
require 'tbpgr_utils'

alpha = %w{one two three}
numbers = %w{1 2 3}
ret = [alpha, numbers].together_map {|first, second|[["#{first}:ret"], ["#{second}:ret"]]}
print ret # => output [["one:ret", "two:ret", "three:ret"],["1:ret", "2:ret", "3:ret"]]
~~~

[back to list](#list)

### Array#together_map!(or tmap!, together_collect!, tcollect!)
if you want to return single array, following.  
~~~ruby
require 'tbpgr_utils'

alpha = %w{one two three}
numbers = %w{1 2 3}
ary = [alpha, numbers]
ret = ary.together_map! do |first, second|
  "#{first}:#{second}"
end
print ret # => output ['one:1', 'two:2', 'three:3']
print ary # => output ['one:1', 'two:2', 'three:3']
~~~

if you want to return multi array, following.  
~~~ruby
require 'tbpgr_utils'

alpha = %w{one two three}
numbers = %w{1 2 3}
ary = [alpha, numbers]
ret = ary.together_map! do |first, second|
  ["#{first}:#{second}", "#{second}:#{first}"]
end
print ret # => output [['1:one', '2:two', '3:three'], ['one:1', 'two:2', 'three:3']]
print ary # => output [['1:one', '2:two', '3:three'], ['one:1', 'two:2', 'three:3']]
~~~

[back to list](#list)

### Array#together_pop(or tpop)
together_pop has alias :tpop

not empty case  
~~~ruby
require 'tbpgr_utils'

lists = [[1, 2], [5, 6]]
ret = lists.together_pop
print ret # => [2, 6]
print lists # => [1, 5]
~~~

empty case  
~~~ruby
require 'tbpgr_utils'

lists = [[], []]
ret = lists.together_pop
print ret # => [nil, nil]
print lists # => [[], []]
~~~

not empty case with args  
~~~ruby
require 'tbpgr_utils'

lists = [[1, 2], [5, 6]]
ret = lists.together_pop 2
print ret # => [[1, 2], [5, 6]]
print lists # => [[], []]
~~~

not empty case with args  
~~~ruby
require 'tbpgr_utils'

lists = [[], []]
ret = lists.together_pop 2
print ret # => [[], []]
print lists # => [[], []]
~~~

[back to list](#list)

### Array#together_reduce(or :treduce, :together_inject, :tinject)
* if you want to single return

~~~ruby
require 'tbpgr_utils'

firsts = [1, 2, 3, 4]
seconds =  [4, 2, 3, 1]
ret = [firsts, seconds].together_reduce{|memo, first, second|memo + first + second}
print ret # => output  20
~~~

* if you want to single return with init value

~~~ruby
require 'tbpgr_utils'

firsts = [1, 2, 3, 4]
seconds =  [4, 2, 3, 1]
ret = [firsts, seconds].together_reduce(10){|memo, first, second|memo + first + second}
print ret # => output  30
~~~

* if you want to single return with init string value

~~~ruby
require 'tbpgr_utils'

firsts = %w{a b c}
seconds =  %w{1 2 3}
ret = [firsts, seconds].together_reduce('start-'){|memo, first, second|memo + first + second}
print ret # => output 'start-a1b2c3'
~~~

* if you want to single return with init Array value

~~~ruby
require 'tbpgr_utils'

firsts = [1, 2, 3, 4]
seconds =  [4, 2, 3, 1]
ret = [firsts, seconds].together_reduce([]){|memo, first, second|memo << first + second}
print ret # => output [5, 4, 6, 5]
~~~

* if you want to single return with init Hash value

~~~ruby
require 'tbpgr_utils'

firsts = [1, 2, 3, 4]
seconds =  [4, 2, 3, 1]
ret = [firsts, seconds].together_reduce({}){|memo, first, second|memo[first] = second;memo}
print ret # => output {1=>4, 2=>2, 3=>3, 4=>1}
~~~

[back to list](#list)

### Array#together_reverse(or :treverse)
together_reverse has alias :treverse

not empty case  
~~~ruby
require 'tbpgr_utils'

lists = [[1, 2], [5, 6]]
ret = lists.together_reverse
print ret # => [[2, 1], [6, 5]]
print lists # => [[1, 2], [5, 6]]
~~~

one empty case  
~~~ruby
require 'tbpgr_utils'

lists = [[1, 2], []]
ret = lists.together_reverse
print ret # => [[2, 1], []]
print lists # => [[1, 2], []]
~~~

[back to list](#list)

### Array#together_reverse!(or :treverse!)
together_reverse! has alias :treverse!

not empty case  
~~~ruby
require 'tbpgr_utils'

lists = [[1, 2], [5, 6]]
ret = lists.together_reverse!
print ret # => [[2, 1], [6, 5]]
print lists # => [[2, 1], [6, 5]]
~~~

one empty case  
~~~ruby
require 'tbpgr_utils'

lists = [[1, 2], []]
ret = lists.together_reverse!
print ret # => [[2, 1], []]
print lists # => [[2, 1], []]
~~~

[back to list](#list)

### Array#together_sample(or :tsample)
together_sample has alias :tsample

not empty case  
~~~ruby
require 'tbpgr_utils'

lists = [[1, 2], [5, 6]]
ret = lists.together_sample
print ret # => [1 or 2, 5 or 6]
~~~

empty case  
~~~ruby
require 'tbpgr_utils'

lists = [[], []]
ret = lists.together_sample
print ret # => [nil, nil]
~~~

not empty case with args  
~~~ruby
require 'tbpgr_utils'

lists = [[1, 2], [5, 6]]
ret = lists.together_sample 2
print ret # => [[1 or 2, 1 or 2], [5 or 6, 5 or 6]] 
~~~

not empty case with args  
~~~ruby
require 'tbpgr_utils'

lists = [[], []]
ret = lists.together_sample 2
print ret # => [[], []]
~~~

not empty, over size case with args  
~~~ruby
require 'tbpgr_utils'

lists = [[1, 2], [5, 6]]
ret = lists.together_sample 3
print ret # => [[1 or 2, 1 or 2], [5 or 6, 5 or 6]] 
~~~

[back to list](#list)

### Array#together_select(or tselect, together_find_all, tfindall)
~~~ruby
require 'tbpgr_utils'

firsts = [1, 2, 3, 4]
seconds =  [4, 2, 3, 1]
ret = [firsts, seconds].together_select{|first, second|first == second}
print ret # => output  [[2, 3], [2, 3]]
~~~

if you want to return multi array, following.  
~~~ruby
require 'tbpgr_utils'

firsts = [1, 2, 3, 4]
seconds =  [4, 2, 3, 1]
ret = [firsts, seconds].together_select{|first, second|[first.odd?, second.even?]}
print ret # => output  [[1, 3], [4, 2]]
~~~

[back to list](#list)

### Array#together_shift(or tshift)
together_shift has alias :tshift

not empty case  
~~~ruby
require 'tbpgr_utils'

lists = [[1, 2], [5, 6]]
ret = lists.together_shift
print ret # => [1, 5]
print lists # => [2, 6]
~~~

empty case  
~~~ruby
require 'tbpgr_utils'

lists = [[], []]
ret = lists.together_shift
print ret # => [nil, nil]
print lists # => [[], []]
~~~

not empty case  
~~~ruby
require 'tbpgr_utils'

lists = [[1, 2], [5, 6]]
ret = lists.together_shift 2
print ret # => [[1, 2], [5, 6]]
print lists # => [[], []]
~~~

not empty case  
~~~ruby
require 'tbpgr_utils'

lists = [[], []]
ret = lists.together_shift 2
print ret # => [[], []]
print lists # => [[], []]
~~~

[back to list](#list)

### Array#together_shuffle(or :tshuffle)
together_shuffle has alias :tshuffle

~~~ruby
require 'tbpgr_utils'

lists = [[1, 2], [5, 6]]
ret = lists.together_shuffle
print ret # => [[1 or 2, 1 or 2], [5 or 6, 5 or 6]]
~~~

[back to list](#list)

### Array#together_slice(or :tslice)
single args case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*6..10]]
ret = lists.together_slice 2
print ret # => [3, 8]
~~~

multi args case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*6..10]]
ret = lists.together_slice 2, 2
print ret # => [[3, 4], [8, 9]]
~~~

range args case  
~~~ruby
require 'tbpgr_utils'

lists = [[*1..5], [*6..10]]
ret = lists.together_slice (2..3)
print ret # => [[3, 4], [8, 9]]
~~~

[back to list](#list)

### Array#together_with_index
~~~ruby
require 'tbpgr_utils'

alpha = %w{one two three}
numbers = %w{1 2 3}
[alpha, numbers].together_with_index do |first, second, index|
  print "#{index.to_s}:#{first}:#{second}\n"  # => output 0:one:1, 1:two:2, 2:three:3
end
~~~

[back to list](#list)

### Array#uniq_size
~~~ruby
require 'tbpgr_utils'

([*1..6] + [2,3]).uniq_size # => 6
[*1..6].uniq_size # => 6
[].uniq_size # => 0
~~~

[back to list](#list)

### AttrEnumerable.at_attr
~~~ruby
require 'attr_enumerable'
class Person
  attr_reader :name, :age
  def initialize(name, age)
    @name, @age = name, age
  end
end

class Persons
  attr_reader :persons
  include AttrEnumerable
  def initialize(persons = [])
    @persons = persons
  end

  def <<(person)
    @persons << person
  end
end

persons = Persons.new([Person.new("tanaka", 84), Person.new("suzuki", 103)])
persons.at_name 0 # => 'tanaka'
persons.at_name 1 # => 'suzuki'
persons.at_name -1 # => 'suzuki'
persons.at_age 0 # => 84
persons.at_age 2 # => nil

persons = Persons.new([])
persons.at_name 0 # => nil
~~~

[back to list](#list)

### AttrEnumerable.compact_attr
~~~ruby
require 'attr_enumerable'
class Person
  attr_reader :name, :age
  def initialize(name, age)
    @name, @age = name, age
  end
end

class Persons
  attr_reader :persons
  include AttrEnumerable
  def initialize(persons = [])
    @persons = persons
  end

  def <<(person)
    @persons << person
  end
end

persons = Persons.new([Person.new("tanaka", 84), Person.new(nil, 99), Person.new("suzuki", nil)])
persons.compact_name # => ['tanaka', 'suzuki']
persons.compact_age # => [84, 99]

persons = Persons.new([])
persons.compact_name 0 # => []
~~~

[back to list](#list)

### AttrEnumerable.concat_attr
~~~ruby
require 'attr_enumerable'
class Person
  attr_reader :name, :age
  def initialize(name, age)
    @name, @age = name, age
  end
end

class Persons
  attr_reader :persons
  include AttrEnumerable
  def initialize(persons = [])
    @persons = persons
  end

  def <<(person)
    @persons << person
  end
end

persons = Persons.new([Person.new("tanaka", 84), Person.new(nil, 99), Person.new("suzuki", nil)])
persons.concat_name(["sato", "matsumoto"]) # => ['tanaka', nil, 'suzuki', "sato", "matsumoto"]
persons.concat_age([20, 1]) # => [84, 99, nil, 20, 1]

persons = Persons.new([])
persons.concat_name(["sato", "matsumoto"]) # => ["sato", "matsumoto"]
~~~

[back to list](#list)

### AttrEnumerable.delete_attr
~~~ruby
require 'attr_enumerable'
class Person
  attr_reader :name, :age
  def initialize(name, age)
    @name, @age = name, age
  end
end

class Persons
  attr_reader :persons
  include AttrEnumerable
  def initialize(persons = [])
    @persons = persons
  end

  def <<(person)
    @persons << person
  end
end

persons = Persons.new([Person.new("tanaka", 84), Person.new("tanaka", 99), Person.new("suzuki", 99)])
persons.delete_name("tanaka") # => persons =  Persons.new(Person.new("suzuki", 99)])
persons = Persons.new([Person.new("tanaka", 84), Person.new("tanaka", 99), Person.new("suzuki", 99)])
persons.delete_age(99) # => persons =  Persons.new([Person.new("tanaka", 84)])
~~~

[back to list](#list)

### AttrEnumerable.each_attr
~~~ruby
require 'attr_enumerable'
class Person
  attr_reader :name, :age
  def initialize(name, age)
    @name, @age = name, age
  end
end

class Persons
  attr_reader :persons
  include AttrEnumerable
  def initialize(persons = [])
    @persons = persons
  end

  def <<(person)
    @persons << person
  end
end

persons = Persons.new([Person.new("tanaka", 84), Person.new("suzuki", 103)])
persons.each_name do |name|
  puts name # => "tanaka", "suzuki"
end

persons.each_age do |age|
  puts age # => 84, 103
end
~~~

[back to list](#list)

### AttrEnumerable.each_attr_with_index
~~~ruby
require 'attr_enumerable'
class Person
  attr_reader :name, :age
  def initialize(name, age)
    @name, @age = name, age
  end
end

class Persons
  attr_reader :persons
  include AttrEnumerable
  def initialize(persons = [])
    @persons = persons
  end

  def <<(person)
    @persons << person
  end
end

persons = Persons.new([Person.new("tanaka", 84), Person.new("suzuki", 103)])
persons.each_name_with_index do |name, i|
  puts "#{name}:#{i}" # => "tanaka:0", "suzuki:1"
end

persons.each_age_with_index do |age, i|
  puts "#{age.to_s}:#{i}" # => "84:0", "103:0"
end
~~~

[back to list](#list)

### AttrEnumerable.first_attr
~~~ruby
require 'attr_enumerable'

class Person
  attr_reader :name, :age
  def initialize(name, age)
    @name, @age = name, age
  end
end

class Persons
  attr_reader :persons
  include AttrEnumerable
  def initialize(persons = [])
    @persons = persons
  end

  def <<(person)
    @persons << person
  end
end

persons = Persons.new([Person.new("tanaka", 84), Person.new("tanaka", 20), Person.new("suzuki", 20)])
print persons.first_name # => 'tanaka'
print persons.first_name(2) # => ['tanaka', 'tanaka']
print persons.first_age(4) # => [84, 20, 20]

persons = Persons.new([])
print persons.first_age(4) # => []
~~~

[back to list](#list)

### AttrEnumerable.include_attr
~~~
require 'attr_enumerable'

class Person
  attr_reader :name, :age
  def initialize(name, age)
    @name, @age = name, age
  end
end

class Persons
  attr_reader :persons
  include AttrEnumerable
  def initialize(persons = [])
    @persons = persons
  end

  def <<(person)
    @persons << person
  end
end

persons = Persons.new([Person.new("tanaka", 84), Person.new("tanaka", 20), Person.new("suzuki", 20)])
print persons.include_name?('tanaka') # => true
print persons.include_name?('sato') # => false
print persons.include_age?(84) # => true
~~~


[back to list](#list)

### AttrEnumerable.first_attr
~~~ruby
require 'attr_enumerable'

class Person
  attr_reader :name, :age
  def initialize(name, age)
    @name, @age = name, age
  end
end

class Persons
  attr_reader :persons
  include AttrEnumerable
  def initialize(persons = [])
    @persons = persons
  end

  def <<(person)
    @persons << person
  end
end

persons = Persons.new([Person.new("tanaka", 84), Person.new("tanaka", 20), Person.new("suzuki", 20)])
print persons.last_name # => 'suzuki'
print persons.last_name(2) # => ['suzuki', 'tanaka']
print persons.last_age(4) # => [84, 20, 20]

persons = Persons.new([])
print persons.last_age(4) # => []
~~~

[back to list](#list)

### AttrEnumerable.reverse_attr
~~~ruby
require 'attr_enumerable'

class Person
  attr_reader :name, :age
  def initialize(name, age)
    @name, @age = name, age
  end
end

class Persons
  attr_reader :persons
  include AttrEnumerable
  def initialize(persons = [])
    @persons = persons
  end

  def <<(person)
    @persons << person
  end
end

persons = Persons.new([Person.new("tanaka", 84), Person.new("suzuki", 103)])
print persons.reverse_name # => ['suzuki', 'tanaka']

print persons.reverse_age # => [103, 84]
~~~

[back to list](#list)

### AttrEnumerable.map_attr
~~~ruby
require 'attr_enumerable'

class Person
  attr_reader :name, :age
  def initialize(name, age)
    @name, @age = name, age
  end
end

class Persons
  attr_reader :persons
  include AttrEnumerable
  def initialize(persons = [])
    @persons = persons
  end

  def <<(person)
    @persons << person
  end
end

persons = Persons.new([Person.new("tanaka", 84), Person.new("suzuki", 103)])
print persons.map_name { |v|v.upcase } # => ['TANAKA', 'SUZUKI']
print persons.map_age { |v|v += 1 } # => [85, 104]
~~~

[back to list](#list)

### AttrEnumerable.reduce_attr
~~~ruby
require 'attr_enumerable'

class Person
  attr_reader :name, :age
  def initialize(name, age)
    @name, @age = name, age
  end
end

class Persons
  attr_reader :persons
  include AttrEnumerable
  def initialize(persons = [])
    @persons = persons
  end

  def <<(person)
    @persons << person
  end
end

persons = Persons.new([Person.new("tanaka", 84), Person.new("suzuki", 103)])
print persons.reduce_name('') { |a, e|a = "#{a}#{e.upcase}"; a } # => 'TANAKASUZUKI'
print persons.reduce_age { |a, e|a += e + 1; a } # => 189
~~~

[back to list](#list)

### AttrEnumerable.sample_attr
~~~ruby
require 'attr_enumerable'

class Person
  attr_reader :name, :age
  def initialize(name, age)
    @name, @age = name, age
  end
end

class Persons
  attr_reader :persons
  include AttrEnumerable
  def initialize(persons = [])
    @persons = persons
  end

  def <<(person)
    @persons << person
  end
end

persons = Persons.new([Person.new("tanaka", 84), Person.new("suzuki", 103)])
print persons.sample_name # => 'tanaka' or 'suzuki'
print persons.sample_name(2) # => ['tanaka', 'suzuki'] or ['suzuki', 'tanaka']
print persons.sample_age(2) # => [84, 103] or [103, 84]
~~~

[back to list](#list)

### AttrEnumerable.select_attr
~~~ruby
require 'attr_enumerable'

class Person
  attr_reader :name, :age
  def initialize(name, age)
    @name, @age = name, age
  end
end

class Persons
  attr_reader :persons
  include AttrEnumerable
  def initialize(persons = [])
    @persons = persons
  end

  def <<(person)
    @persons << person
  end
end

persons = Persons.new([Person.new("tanaka", 84), Person.new("tanaka", 20), Person.new("suzuki", 20)])
print persons.select_name { |v|v == 'tanaka' } # => ['tanaka' ,'tanaka']
print persons.select_age { |v|v == 20 } # => [20 ,20]
~~~

[back to list](#list)

### AttrEnumerable.shuffle_attr
~~~ruby
require 'attr_enumerable'

class Person
  attr_reader :name, :age
  def initialize(name, age)
    @name, @age = name, age
  end
end

class Persons
  attr_reader :persons
  include AttrEnumerable
  def initialize(persons = [])
    @persons = persons
  end

  def <<(person)
    @persons << person
  end
end

persons = Persons.new([Person.new("tanaka", 84), Person.new("suzuki", 103)])
print persons.shuffle_name # => ['tanaka', 'suzuki'] or['suzuki', 'tanaka']
print persons.shuffle_age # => [84, 103] or [103, 84]
~~~


[back to list](#list)

### AttrEnumerable.slice_attr
~~~ruby
require 'attr_enumerable'

class Person
  attr_reader :name, :age
  def initialize(name, age)
    @name, @age = name, age
  end
end

class Persons
  attr_reader :persons
  include AttrEnumerable
  def initialize(persons = [])
    @persons = persons
  end

  def <<(person)
    @persons << person
  end
end

persons = Persons.new([Person.new("tanaka", 84), Person.new("suzuki", 33), Person.new("suzuki", 103)])
print persons.slice_name(1) # => 'suzuki'
print persons.slice_age(0, 2) # => [84, 33]
print persons.slice_age(1..2) # => [33, 103]
~~~

[back to list](#list)

### AttributesHashable.to_hash
~~~ruby
require 'attributes_initializable'
require 'attributes_hashable'

class Hoge
  include AttributesInitializable
  attr_accessor_init :hoge, :hige
  include AttributesHashable
end

hoge = Hoge.new do |h|
  h.hoge = 'hoge'
  h.hige = 'hige'
end

hoge.to_hash # => {:hoge=>"hoge", :hige=>"hige"}

# After include AttributesHashable, you can use Hash.try_convert.
Hash.try_convert hoge # => {:hoge=>"hoge", :hige=>"hige"}
~~~

[back to list](#list)

### AttributesInitializable::ClassMethods.attr_accessor_init
~~~ruby
require 'attributes_initializable'

class AccessorSample
  include AttributesInitializable
  attr_accessor_init :atr1, :atr2
end

atr_sample1 = AccessorSample.new :atr1 => 'atr1', :atr2 => 'atr2'
p atr_sample1.atr1 # => atr1
p atr_sample1.atr2 # => atr2

atr_sample2 = AccessorSample.new do |a|
  a.atr1 = 'atr1'
  a.atr2 = 'atr2'
end
p atr_sample2.atr1 # => atr1
p atr_sample2.atr2 # => atr2
~~~

same mean code is  
~~~ruby
class AccessorSample
  attr_accessor :atr1, :atr2

  def initialize(values = nil, &block)
    return yield self if block
    @atr1 = values[:atr1]
    @atr2 = values[:atr2]
  end
end

atr_sample1 = AccessorSample.new :atr1 => 'atr1', :atr2 => 'atr2'
p atr_sample1.atr1 # => atr1
p atr_sample1.atr2 # => atr2

atr_sample2 = AccessorSample.new do |a|
  a.atr1 = 'atr1'
  a.atr2 = 'atr2'
end
p atr_sample2.atr1 # => atr1
p atr_sample2.atr2 # => atr2
~~~

[back to list](#list)

### AttributesInitializable::ClassMethods.attr_reader_init
~~~ruby
require 'attributes_initializable'

class AccessorSample
  include AttributesInitializable
  attr_reader_init :atr1, :atr2
end

atr_sample1 = AccessorSample.new :atr1 => 'atr1', :atr2 => 'atr2'
p atr_sample1.atr1 # => atr1
p atr_sample1.atr2 # => atr2

# can not use writer.
# atr_sample2 = AccessorSample.new do |a|
#   a.atr1 = 'atr1'
#   a.atr2 = 'atr2'
# end
~~~

same mean code is  
~~~ruby
class AccessorSample
  attr_reader :atr1, :atr2

  def initialize(values = nil, &block)
    return yield self if block
    @atr1 = values[:atr1]
    @atr2 = values[:atr2]
  end
end

atr_sample1 = AccessorSample.new :atr1 => 'atr1', :atr2 => 'atr2'
p atr_sample1.atr1 # => atr1
p atr_sample1.atr2 # => atr2

# can not use writer.
# atr_sample2 = AccessorSample.new do |a|
#   a.atr1 = 'atr1'
#   a.atr2 = 'atr2'
# end
~~~

[back to list](#list)

### AttributesInitializable::ClassMethods.attr_writer_init
~~~ruby
require 'attributes_initializable'

class AccessorSample
  include AttributesInitializable
  attr_writer_init :atr1, :atr2
end

atr_sample1 = AccessorSample.new :atr1 => 'atr1', :atr2 => 'atr2'
# can not use reader
# p atr_sample1.atr1 # => atr1
# p atr_sample1.atr2 # => atr2
atr_sample1.instance_variable_get "@atr1" # => atr1
atr_sample1.instance_variable_get "@atr2" # => atr2

atr_sample2 = AccessorSample.new do |a|
  a.atr1 = 'atr1'
  a.atr2 = 'atr2'
end

# can not use reader
# p atr_sample2.atr1 # => atr1
# p atr_sample2.atr2 # => atr2
atr_sample2.instance_variable_get "@atr1" # => atr1
atr_sample2.instance_variable_get "@atr2" # => atr2
~~~

same mean code is  
~~~ruby
class AccessorSample
  attr_writer :atr1, :atr2

  def initialize(values = nil, &block)
    return yield self if block
    @atr1 = values[:atr1]
    @atr2 = values[:atr2]
  end
end

atr_sample1 = AccessorSample.new :atr1 => 'atr1', :atr2 => 'atr2'
# can not use reader
# p atr_sample1.atr1 # => atr1
# p atr_sample1.atr2 # => atr2
atr_sample1.instance_variable_get "@atr1" # => atr1
atr_sample1.instance_variable_get "@atr2" # => atr2

atr_sample2 = AccessorSample.new do |a|
  a.atr1 = 'atr1'
  a.atr2 = 'atr2'
end
# can not use reader
# p atr_sample2.atr1 # => atr1
# p atr_sample2.atr2 # => atr2
atr_sample2.instance_variable_get "@atr1" # => atr1
atr_sample2.instance_variable_get "@atr2" # => atr2
~~~

[back to list](#list)

### EndERB.apply
for single template script using __END__ and DATA

sample case

~~~ruby
require "end_erb"

def hoge
  hash = {
    hoge: '@hoge@',
    hige: '@hige@',
  }
  EndERB.apply(hash)
end

puts hoge

__END__
hoge=<%=hash[:hoge]%>
hige=<%=hash[:hige]%>
~~~

output

~~~
hoge=@hoge@
hige=@hige@
~~~

[back to list](#list)

### Familyable
5 person case

~~~ruby
require 'familyable'
persons = [
  a = Familyable::Person.new(id: 1, parent_ids: [2, 3]),
  b = Familyable::Person.new(id: 2, parent_ids: []),
  c = Familyable::Person.new(id: 3, parent_ids: [4],),
  d = Familyable::Person.new(id: 4, parent_ids: [3]),
  e = Familyable::Person.new(id: 5, parent_ids: [2]),
]

family = Familyable::Family.new(family: persons)
family.get_parents a # => return person [b, c]
family.get_children b # => return person [a, e]
family.get_brothers a # => return person [d, e]
~~~

If you want to use other model instead of person,  
Create model that has two fileds that are 'id' and 'parent_ids'.

[back to list](#list)

### Fixnum.to_fixnum_html_table
1 to 10 by 2 case  
~~~ruby
require 'tbpgr_utils'
Fixnum.to_fixnum_html_table(1, 10, 2)
~~~

result  
~~~
<table>
  <tr>
    <td>1</td>
    <td>2</td>
  </tr>
  <tr>
    <td>3</td>
    <td>4</td>
  </tr>
  <tr>
    <td>5</td>
    <td>6</td>
  </tr>
  <tr>
    <td>7</td>
    <td>8</td>
  </tr>
  <tr>
    <td>9</td>
    <td>10</td>
  </tr>
</table>
~~~

[back to list](#list)

### Fixnum.to_fixnum_table
1 to 100 by 10 case  
~~~ruby
Fixnum.to_fixnum_table(1, 100, 10)
~~~

result  
~~~
| 1| 2| 3| 4| 5| 6| 7| 8| 9| 10|
|11|12|13|14|15|16|17|18|19| 20|
|21|22|23|24|25|26|27|28|29| 30|
|31|32|33|34|35|36|37|38|39| 40|
|41|42|43|44|45|46|47|48|49| 50|
|51|52|53|54|55|56|57|58|59| 60|
|61|62|63|64|65|66|67|68|69| 70|
|71|72|73|74|75|76|77|78|79| 80|
|81|82|83|84|85|86|87|88|89| 90|
|91|92|93|94|95|96|97|98|99|100|
~~~

1 to 10 by 2 case  
~~~ruby
Fixnum.to_fixnum_table(1, 10, 2)
~~~

result  
~~~
|1| 2|
|3| 4|
|5| 6|
|7| 8|
|9|10|
~~~

[back to list](#list)

### Ghostable
* include Ghostable
* create ghost method by using Ghostable::ghost_method
* ghost_method first_args = method_name_pattern
* ghost_method second_args = method_base_name Symbol(using in Ghostable internal logic)
* ghost_method third = block. this block is main logic. block can use args[method_name, *args, &block]

sample ghost method define module.  
~~~ruby
require 'ghostable'
module Checkable
  include Ghostable
  ghost_method /check_range_.*\?$/, :check_range do |method_name, *args, &block|
    method_name.to_s =~ /(check_range_)(\d+)(_to_)(\d*)/
    from = $2.to_i
    to = $4.to_i
    value = args.first
    (from..to).include? value
  end

  ghost_method /^contain_.*\?$/, :check_contain do |method_name, *args, &block|
    method_name.to_s =~ /^(contain_)(.*)(\?)/
    word = $2
    value = args.first
    value.include? word
  end
end
~~~

* use ghost method

sample ghost method use class  
~~~ruby
class SampleChecker
  include Checkable
end

sample = SampleChecker.new
sample.check_range_3_to_5?(4) # => return true
sample.check_range_3_to_5?(6) # => return false
sample.check_range_3_to_6?(6) # => return true

sample.contain_hoge? "test_hoge_test" # => return true
sample.contain_hoge? "test_hige_test" # => return false
sample.contain_hige? "test_hige_test" # => return true
~~~

[back to list](#list)

### Kernel#capture_stdout
capture STDOUT to String. This method can use in STDOUT contents test.

~~~ruby
require 'test_toolbox'

result = capture_stdout {puts "test"} # => "test"

# no stdout case. return empty.
result = capture_stdout {sleep 0.1} # => ""(empty)
~~~

[back to list](#list)

### Kernel#dp_line
debug print line for print-debugging.

~~~ruby
require 'test_toolbox'

# default usage
dp_line __LINE__
# output is following. yy = line no.
# => --------------------|filename=|line=yy|--------------------\n

# output with filename
dp_line __LINE__, filename: __FILE__
# output is following. xx=filenamem, yy = line no.
# => --------------------|filename=xx|line=yy|--------------------\n

# output with specific line charactor.
dp_line __LINE__, filename: __FILE__, char: '@'
# output is following. xx=filenamem, yy = line no.
# => @@@@@@@@@@@@@@@@@@@@|filename=xx|line=yy$|@@@@@@@@@@@@@@@@@@@@\n
~~~

[back to list](#list)

### Hash#>>
~~~ruby
require 'tbpgr_utils'
h = {key1: "value1", key2: "value2"}
h.>>.upcase # => {key1: "VALUE1", key2: "VALUE2"}
h.>>.+('_hoge') # => {key1: "value1_hoge", key2: "value2_hoge"}
~~~

[back to list](#list)

### Hash#html_table
~~~ruby
require 'tbpgr_utils'
{
  :key_1 => :value1,
  :key__2 => :value2,
  :key___3 => :value3,
}.html_table
~~~

result  

~~~
<table>
  <tr>
    <td>key_1</td>
    <td>value1</td>
  </tr>
  <tr>
    <td>key__2</td>
    <td>value2</td>
  </tr>
  <tr>
    <td>key___3</td>
    <td>value3</td>
  </tr>
</table>
~~~

[back to list](#list)

### Hash#table
~~~ruby
require 'tbpgr_utils'
{
  :key_1 => :value1___________________,
  :key__2 => :value2,
  :key___3 => :value3,
}.table
~~~

result  

~~~ruby
|key_1  |value1___________________|
|key__2 |value2                   |
|key___3|value3                   |
~~~

[back to list](#list)

### Integer#each_digit_with_index
~~~ruby
require 'tbpgr_utils'
ret=[];
12345.each_digit_with_index { |v, i|ret << v + i };
print ret # => [1, 3, 5, 7, 9]
~~~

[back to list](#list)

### Integer#each_digit
~~~ruby
require 'tbpgr_utils'
ret=[];
12345.each_digit { |v|ret << v + 1 };
print ret # => [2,3,4,5,6]
~~~

[back to list](#list)

### Integer#palindromic_prime
~~~ruby
require 'tbpgr_utils'
0.palindromic_prime? # => false
1.palindromic_prime? # => false
2.palindromic_prime? # => true
11.palindromic_prime? # => true
757.palindromic_prime? # => true
758.palindromic_prime? # => false
~~~

[back to list](#list)

### Integer#reverse_each_digit
~~~ruby
require 'tbpgr_utils'
ret=[];
12345.reverse_each_digit { |v|ret << v + 1 };
print ret # => [6, 5, 4, 3, 2]
~~~

[back to list](#list)

### Kernel booleans
~~~ruby
require 'tbpgr_utils'
puts yes # return true
puts ok # return true
puts good # return true

puts no # return false
puts ng # return false
puts bad # return false
~~~

[back to list](#list)

### Kernel#bulk_define_methods
Define methods to classes. Methods have simple return value.

~~~ruby
require 'tbpgr_utils'
bulk_define_methods [NilClass, FalseClass], :blank?, true
bulk_define_methods [TrueClass, Numeric], "blank?", false

puts nil.blank?   # => true
puts false.blank? # => true
puts true.blank?  # => false
puts 1.blank?     # => false

bulk_define_methods [NilClass, FalseClass], [:blank?, :present?], [true, false]
bulk_define_methods [TrueClass, Numeric], [:blank?, :present?], [false, true]

puts nil.blank?     # => true
puts nil.present?   # => false
puts false.blank?   # => true
puts false.present? # => false
puts true.blank?    # => false
puts true.present?  # => true
puts 1.blank?       # => false
puts 1.present?     # => true
~~~

if you don't use bulk_define_methods, followinng code is same mean.  
~~~ruby
class NilClass
 def blank?
   true
 end

 def present?
   false
 end
end

class FalseClass
 def blank?
   true
 end

 def present?
   false
 end
end
~~~

[back to list](#list)

### Kernel#aa_ancestors
Ascii Art Ancestors

~~~ruby
class BaseHogeForAncestors;end
class HogeForAncestors < BaseHogeForAncestors;end

puts HogeForAncestors.aa_ancestors
~~~

result is ...

~~~
----------------------
|     BasicObject    |
----------------------
          |
----------------------
|       Kernel       |
----------------------
          |
----------------------
|       Object       |
----------------------
          |
----------------------
|BaseHogeForAncestors|
----------------------
          |
----------------------
|  HogeForAncestors  |
----------------------
~~~

[back to list](#list)

### Kernel#evalb
~~~ruby
require 'tbpgr_utils'
n = 1
actual = evalb(binding) do
  <<-EOS
n = n + 1
n = n + 2
     EOS
end

print actual # => 4
~~~

[back to list](#list)

### Kernel#exchange
~~~ruby
a = 1
b = 2
a, b = exchange(a, b)
a # => 2
b # => 1
~~~

[back to list](#list)

### Kernel#hash_to_attributes
~~~ruby
require 'tbpgr_utils'

class Person
  attr_accessor :name, :age
end

person = Person.new
person.hash_to_attributes({name: 'hoge', age: 33})
~~~

result  
~~~ruby
#<PersonForHashToAttributes:0x3957858 @age=33, @not_exists="hoge">
~~~

[back to list](#list)

### Kernel#null
~~~ruby
require 'tbpgr_utils'
null # => nil
~~~

[back to list](#list)

### Kernel#print_eval
This method for sample code. for manual, for blog-entry's-snippet  ...etc.

~~~ruby
print_eval 8/4, binding  # => 8/4 # => 2

message = 'msg'
print_eval "hoge-#{message}", binding # => "hoge-#{message}" # => "hoge-msg"
~~~

output  
~~~
8/4 # => 2"hoge-#{message}" # => "hoge-msg"
~~~

[back to list](#list)

### Kernel#puts_eval
This method for sample code. for manual, for blog-entry's-snippet  ...etc.

~~~ruby
puts_eval 8/4, binding

message = 'msg'
puts_eval "hoge-#{message}", binding # => "hoge-#{message}" # => "hoge-msg"
~~~

output  
~~~
8/4 # => 2
"hoge-#{message}" # => "hoge-msg"
~~~

[back to list](#list)

### Kernel#bulk_puts_eval
multi line version of puts_eval.

~~~ruby
message = "msg"
bulk_puts_eval binding, <<-EOS
"hoge-hige1" + "add" + message
"hoge-hige2" + "add" + message
EOS
~~~

output  
~~~
"hoge-hige1" + "add" + message # => "hoge-hige1addmsg"
"hoge-hige2" + "add" + message # => "hoge-hige2addmsg"
~~~

[back to list](#list)

### Enumerable#if_else_map
~~~ruby
require 'tbpgr_utils'
[*1..4].if_else_map(
        :odd?.to_proc,
        ->(odd){'odd'},
        ->(even){'even'}
      )
__END__
["odd", "even", "odd", "even"]
~~~

~~~ruby
require 'tbpgr_utils'
[*?a..?z].if_else_map(
        :vowel?.to_proc,
        ->(alph){ "#{alph} is vowel" },
        ->(alph){ "#{alph} is not vowel" }
      )

__END__
["a is vowel",
 "b is not vowel",
 "c is not vowel",
 "d is not vowel",
 "e is vowel",
 "f is not vowel",
 "g is not vowel",
 "h is not vowel",
 "i is vowel",
 "j is not vowel",
 "k is not vowel",
 "l is not vowel",
 "m is not vowel",
 "n is not vowel",
 "o is vowel",
 "p is not vowel",
 "q is not vowel",
 "r is not vowel",
 "s is not vowel",
 "t is not vowel",
 "u is vowel",
 "v is not vowel",
 "w is not vowel",
 "x is not vowel",
 "y is not vowel",
 "z is not vowel"]
~~~

[back to list](#list)

### Enumerable#kernel_send
~~~ruby
require 'tbpgr_utils'
[*1..3].kernel_send:Rational # => [(1/1), (2/1), (3/1)]
[*1..3].kernel_send:print # => 123
[*65..68].kernel_send :putc # => ABCD
~~~

[back to list](#list)

### Enumerable#sum
~~~ruby
require 'tbpgr_utils'
[*1..5].sum # => 15
[*?a..?e].sum # => "abcde"
~~~

[back to list](#list)

### EvalHelper Object

enable to use EvalHelper in Object
~~~ruby
require 'eval_helper_object'
require_code("hoge") # => 'require "hoge"'
~~~

[back to list](#list)

### EvalHelper#attr_accessor_init_code
single case

~~~ruby
class EvalHelperAttrAccessorInitTest
  include EvalHelper

  def hoge(args)
    attr_accessor_init_code(args)
  end
end

EvalHelperAttrAccessorInitTest.new.hoge('atr1')
~~~

result  

~~~ruby
attr_accessor :atr1

def initialize(atr1)
  @atr1 = atr1
end
~~~

multi case

~~~ruby
class EvalHelperAttrAccessorInitTest
  include EvalHelper

  def hoge(args)
    attr_accessor_init_code(args)
  end
end

EvalHelperAttrAccessorInitTest.new.hoge(['atr1', 'atr2'])
~~~

result  

~~~ruby
attr_accessor :atr1, :atr2

def initialize(atr1, atr2)
  @atr1 = atr1
  @atr2 = atr2
end
~~~

[back to list](#list)

### EvalHelper#each_do_code
~~~ruby
require 'eval_helper'
class EvalHelperEacjBraceTest
  include EvalHelper

  def hoge(hash)
    each_do_code(hash[:target], hash[:proc])
  end
end

hash = {
  target: '[:a, :b]',
  proc: "puts \"\#{v}1\"\nputs \"\#{v}2\"\n",
}
EvalHelperEacjBraceTest.new.hoge(hash) # => return "[:a, :b].each do |v|\n  puts \"\#{v}1\"\n  puts \"\#{v}2\"\nend"
~~~

[back to list](#list)

### EvalHelper#each_brace_code
~~~ruby
require 'eval_helper'
class EvalHelperEacjBraceTest
  include EvalHelper

  def hoge(hash)
    each_brace_code(hash[:target], hash[:proc])
  end
end

hash = {
  target: '[:a, :b]',
  proc: 'puts v',
}
EvalHelperEacjBraceTest.new.hoge(hash) # => return '[:a, :b].each { |v|puts v }'
~~~

[back to list](#list)

### EvalHelper#each_with_index_brace_code
~~~ruby
require 'eval_helper'
class EvalHelperEachWithIndexBraceTest
  include EvalHelper

  def hoge(hash)
    each_with_index_brace_code(hash[:target], hash[:proc])
  end
end

hash = {
  target: '[:a, :b]',
  proc: 'puts "#{i}:#{v}"',
}
EvalHelperEachWithIndexBraceTest.new.hoge(hash) # => return '[:a, :b].each_with_index { |v, i|puts "#{i}:#{v}" }'
~~~

[back to list](#list)

### EvalHelper#each_with_index_do_code
~~~ruby
require 'eval_helper'
class EvalHelperEachWithIndexDoTest
  include EvalHelper

  def hoge(hash)
    each_with_index_do_code(hash[:target], hash[:proc])
  end
end

hash = {
  target: '[:a, :b]',
  proc: "puts \"\#{i}:\#{v}1\"\nputs \"\#{i}:\#{v}2\"\n",
}
EvalHelperEachWithIndexDoTest.new.hoge(hash) # => return "[:a, :b].each_with_index do |v, i|\n  puts \"\#{i}:\#{v}1\"\n  puts \"\#{i}:\#{v}2\"\nend"
~~~

[back to list](#list)

### EvalHelper#if_code

if case

~~~ruby
require 'eval_helper'
class EvalHelperTest
  include EvalHelper

  def hoge(hash)
    msg = hash[:input]
    code = if_code(hash[:if_cond], hash[:if_proc], hash[:else_proc])
    instance_eval code
  end
end

hash = {
  input: "test",
  if_cond: "msg == 'test'",
  if_proc: "true",
  else_proc: "false",
}
EvalHelperTest.new.hoge(hash) # => return true
~~~

else case

~~~ruby
require 'eval_helper'
class EvalHelperTest
  include EvalHelper

  def hoge(hash)
    msg = hash[:input]
    code = if_code(hash[:if_cond], hash[:if_proc], hash[:else_proc])
    instance_eval code
  end
end

hash = {
  input: "not_test",
  if_cond: "msg == 'test'",
  if_proc: "true",
  else_proc: "false",
}
EvalHelperTest.new.hoge(hash) # => return false
~~~

[back to list](#list)

### EvalHelper#if_code_after
if case

~~~ruby
require 'eval_helper'

class EvalHelperTest
  include EvalHelper

  def hoge(hash)
    msg = hash[:input]
    code = if_code_after(hash[:if_cond], hash[:if_proc])
    ret = 'dafault'
    instance_eval code
    ret
  end
end

hash = {
  input: "test",
  if_cond: "msg == 'test'",
  if_proc: "ret = 'true'",
}
EvalHelperTest.new.hoge(hash) # => return 'true'
~~~

else case

~~~ruby
require 'eval_helper'

class EvalHelperTest
  include EvalHelper

  def hoge(hash)
    msg = hash[:input]
    code = if_code_after(hash[:if_cond], hash[:if_proc])
    ret = 'ret = "true"'
    instance_eval code
    ret
  end
end

hash = {
  input: "not_test",
  if_cond: "msg == 'test'",
  if_proc: "ret = 'true'",
}
EvalHelperTest.new.hoge(hash) # => return 'default'
~~~

[back to list](#list)

### EvalHelper#require_code
single require case

~~~ruby
require 'eval_helper'
class EvalHelperRequireTest
  include EvalHelper

  def hoge(*args)
    require_code(args)
  end
end

args = 'tbpgr_utils'
EvalHelperRequireTest.new.hoge(args) # => return "require 'tbpgr_utils'\n"
~~~

muiti require case

~~~ruby
require 'eval_helper'
class EvalHelperRequireTest
  include EvalHelper

  def hoge(*args)
    require_code(args)
  end
end

args =  ['tbpgr_utils', 'eval_helper']
EvalHelperRequireTest.new.hoge(args) # => return "require 'tbpgr_utils'\nrequire 'eval_helper'\n"
~~~

[back to list](#list)

### EvalHelper#require_relative_code
single require_relative case

~~~ruby
require 'eval_helper'
class EvalHelperRequireRelativeTest
  include EvalHelper

  def hoge(*args)
    require_relative_code(args)
  end
end

args = 'tbpgr_utils'
EvalHelperRequireRelativeTest.new.hoge(args) # => return "require_relative 'tbpgr_utils'\n"
~~~

muiti require_relative case

~~~ruby
require 'eval_helper'
class EvalHelperRequireRelativeTest
  include EvalHelper

  def hoge(*args)
    require_relative_code(args)
  end
end

args =  ['tbpgr_utils', 'eval_helper']
EvalHelperRequireRelativeTest.new.hoge(args) # => return "require_relative 'tbpgr_utils'\nrequire_relative 'eval_helper'\n"
~~~

[back to list](#list)

### EvalHelper#set_variable_code
set string variable case  
~~~ruby
require 'eval_helper'
class EvalHelperSetVariableTest
  include EvalHelper

  def hoge(name, value)
    set_variable_code(name, value)
  end
end

hash = {
  name: 'hoge',
  value: '"hoge"',
}
EvalHelperSetVariableTest.new.hoge(hash[:name], hash[:value])
~~~

return

~~~ruby
hoge = "hoge"
~~~

set numeric variable case  
~~~ruby
require 'eval_helper'
class EvalHelperSetVariableTest
  include EvalHelper

  def hoge(name, value)
    set_variable_code(name, value)
  end
end

hash = {
  name: 'hoge_num',
  value: '1',
}
EvalHelperSetVariableTest.new.hoge(hash[:name], hash[:value])
~~~

return

~~~ruby
hoge_num = 1
~~~

[back to list](#list)

### EvalHelper#set_variables_code
~~~ruby
require 'eval_helper'
class EvalHelperSetVariablesTest
  include EvalHelper

  def hoge(variables)
    set_variables_code(variables)
  end
end

variables = [
  {
    name: 'name1',
    value: '"value1"',
  },
  {
    name: 'name2',
    value: '"value2"',
  },
]
EvalHelperSetVariablesTest.new.hoge(variables)
~~~

[back to list](#list)

### EvalHelper#times_code

single_line_proc case  
~~~ruby
require 'eval_helper'

class EvalHelperTimesTest
  include EvalHelper

  def hoge(number, proc)
    times_code(number, proc)
  end
end

hash = {
  number: 2,
  proc: 'puts "#{i}times"',
}
EvalHelperTimesTest.new.hoge(hash[:number], hash[:proc])
~~~

return  
~~~
2.times { |i| puts "#{i}times" }
~~~

multi_line_proc case  
~~~ruby
require 'eval_helper'

class EvalHelperTimesTest
  include EvalHelper

  def hoge(number, proc)
    times_code(number, proc)
  end
end

hash = {
  number: 3,
  proc: 'puts "#{i}times"\nputs "#{i*2}times"',
}
EvalHelperTimesTest.new.hoge(hash[:number], hash[:proc])
~~~

return

~~~
3.times do |i|
  puts "#{i}times"
  puts "#{i*2}times"
end
~~~

[back to list](#list)

### EvalHelper#ternary_operator
true case

~~~ruby
require 'eval_helper'

class EvalHelperTernaryTest
  include EvalHelper

  def hoge(hash)
    msg = hash[:input]
    code = \
      if hash[:ret]
        ternary_operator(hash[:cond], hash[:true_case], hash[:false_case], hash[:ret])
      else
        ternary_operator(hash[:cond], hash[:true_case], hash[:false_case])
      end
    instance_eval code
  end
end

hash = {
  input: "test",
  cond: "msg == 'test'",
  true_case: "true",
  false_case: "false",
  ret: "ret",
}
EvalHelperTernaryTest.new.hoge(hash) # => return 'true'
~~~

false case

~~~ruby
require 'eval_helper'

class EvalHelperTernaryTest
  include EvalHelper

  def hoge(hash)
    msg = hash[:input]
    code = \
      if hash[:ret]
        ternary_operator(hash[:cond], hash[:true_case], hash[:false_case], hash[:ret])
      else
        ternary_operator(hash[:cond], hash[:true_case], hash[:false_case])
      end
    instance_eval code
  end
end

hash = {
  input: "not_test",
  cond: "msg == 'test'",
  true_case: "true",
  false_case: "false",
  ret: "ret",
}
EvalHelperTernaryTest.new.hoge(hash) # => return 'false'
~~~

[back to list](#list)

### EvalHelper#unless_code

unless case

~~~ruby
require 'eval_helper'
class EvalHelperTest
  include EvalHelper

  def hoge(hash)
    msg = hash[:input]
    code = unless_code(hash[:unless_cond], hash[:unless_proc], hash[:else_proc])
    instance_eval code
  end
end

hash = {
  input: "not_test",
  unless_cond: "msg == 'test'",
  unless_proc: "true",
  else_proc: "false",
}
EvalHelperTest.new.hoge(hash) # => return true
~~~

else case

~~~ruby
require 'eval_helper'
class EvalHelperTest
  include EvalHelper

  def hoge(hash)
    msg = hash[:input]
    code = unless_code(hash[:unless_cond], hash[:unless_proc], hash[:else_proc])
    instance_eval code
  end
end

hash = {
  input: "test",
  unless_cond: "msg == 'test'",
  unless_proc: "true",
  else_proc: "false",
}
EvalHelperTest.new.hoge(hash) # => return false
~~~

[back to list](#list)

### EvalHelper#unless_code_after
unless case

~~~ruby
require 'eval_helper'

class EvalHelperTest
  include EvalHelper

  def hoge(hash)
    msg = hash[:input]
    code = unless_code_after(hash[:unless_cond], hash[:unless_proc])
    ret = 'dafault'
    instance_eval code
    ret
  end
end

hash = {
  input: "not_test",
  unless_cond: "msg == 'test'",
  unless_proc: "ret = 'true'",
}
EvalHelperTest.new.hoge(hash) # => return 'true'
~~~

else case

~~~ruby
require 'eval_helper'

class EvalHelperTest
  include EvalHelper

  def hoge(hash)
    msg = hash[:input]
    code = unless_code_after(hash[:unless_cond], hash[:unless_proc])
    ret = 'ret = "true"'
    instance_eval code
    ret
  end
end

hash = {
  input: "test",
  unless_cond: "msg == 'test'",
  unless_proc: "ret = 'true'",
}
EvalHelperTest.new.hoge(hash) # => return 'default'
~~~

[back to list](#list)

### MarkdownString.backquotes
~~~ruby
require 'markdown_string'
MarkdownString.backquotes <<-EOS
hoge
hige
hage
EOS
~~~

result

~~~
>hoge  
>hige  
>hage  
~~~

[back to list](#list)

### MarkdownString.bold
~~~ruby
require 'markdown_string'
MarkdownString.bold("strong") # => "**strong**"
MarkdownString.bold("") # => "****"
MarkdownString.bold(nil) # => "****"
~~~

[back to list](#list)

### MarkdownString.code
~~~ruby
require 'markdown_string'
MarkdownString.code('print "hoge"') # => '`print "hoge"`'
~~~

[back to list](#list)

### MarkdownString.codes
~~~ruby
require 'markdown_string'
MarkdownString.codes("class Hoge\n  def hoge\n    'hoge'\n  end\nend\n")
~~~

result

~~~
 ~~~ruby
 class Hoge
   def hoge
     'hoge'
   end
 end
 ~~~
~~~

[back to list](#list)

### MarkdownString.heading1
~~~ruby
require 'markdown_string'
MarkdownString.heading1("title") # => "# title"
MarkdownString.heading1("") # => "# "
MarkdownString.heading1(nil) # => "# "
MarkdownString.heading1(12345) # => "# 12345"
~~~

[back to list](#list)

### MarkdownString.heading2
~~~ruby
require 'markdown_string'
MarkdownString.heading2("title") # => "## title"
MarkdownString.heading2("") # => "## "
MarkdownString.heading2(nil) # => "## "
MarkdownString.heading2(12345) # => "## 12345"
~~~

[back to list](#list)

### MarkdownString.heading3
~~~ruby
require 'markdown_string'
MarkdownString.heading3("title") # => "### title"
MarkdownString.heading3("") # => "### "
MarkdownString.heading3(nil) # => "### "
MarkdownString.heading3(12345) # => "### 12345"
~~~
[back to list](#list)

### MarkdownString.heading4
~~~ruby
require 'markdown_string'
MarkdownString.heading4("title") # => "#### title"
MarkdownString.heading4("") # => "#### "
MarkdownString.heading4(nil) # => "#### "
MarkdownString.heading4(12345) # => "#### 12345"
~~~
[back to list](#list)

### MarkdownString.heading5
~~~ruby
require 'markdown_string'
MarkdownString.heading5("title") # => "##### title"
MarkdownString.heading5("") # => "##### "
MarkdownString.heading5(nil) # => "##### "
MarkdownString.heading5(12345) # => "##### 12345"
~~~
[back to list](#list)

### MarkdownString.heading6
~~~ruby
require 'markdown_string'
MarkdownString.heading6("title") # => "###### title"
MarkdownString.heading6("") # => "###### "
MarkdownString.heading6(nil) # => "###### "
MarkdownString.heading6(12345) # => "###### 12345"
~~~

[back to list](#list)

### MarkdownString.hr
~~~ruby
require 'markdown_string'
MarkdownString.hr # => '---'
~~~

[back to list](#list)

### MarkdownString.italic
~~~ruby
require 'markdown_string'
MarkdownString.italic 'italic' # => '*italic*'
~~~

[back to list](#list)

### MarkdownString.link
~~~ruby
require 'markdown_string'
MarkdownString.link 'label', 'http://not_exists.com' # => '[label](http://not_exists.com)'
~~~

[back to list](#list)

### MarkdownString.ol
case list  
~~~ruby
require 'markdown_string'
MarkdownString.ol(%w{a b c})
~~~

result  
~~~
1. a
1. b
1. c
~~~

case not list  
~~~ruby
require 'markdown_string'
MarkdownString.ol("test") # => "test"

case nil list  
~~~ruby
require 'markdown_string'
MarkdownString.ol([nil, nil])
~~~

result  
~~~
1. 
1. 
~~~

case empty list  
~~~ruby
require 'markdown_string'
MarkdownString.ol([]) # => ""
~~~

[back to list](#list)

### MarkdownString.ul
case list  
~~~ruby
require 'markdown_string'
MarkdownString.ul(%w{a b c})
~~~

result  
~~~
* a
* b
* c
~~~

case not list  
~~~ruby
require 'markdown_string'
MarkdownString.ul("test") # => "test"

case nil list  
~~~ruby
require 'markdown_string'
MarkdownString.ul([nil, nil])
~~~

result  
~~~
* 
* 
~~~

case empty list  
~~~ruby
require 'markdown_string'
MarkdownString.ul([]) # => ""
~~~

[back to list](#list)

### MetasyntacticVariable
* META variable

~~~ruby
MetasyntacticVariable::META_VARIABLES  # => [:foo, :bar, :baz, :qux, :quux, :corge, :grault, :garply, :waldo, :fred, :plugh, :xyzzy, :thud]
MetasyntacticVariable.meta_variables  # => [:foo, :bar, :baz, :qux, :quux, :corge, :grault, :garply, :waldo, :fred, :plugh, :xyzzy, :thud]
~~~

* META variable for classes

~~~ruby
MetasyntacticVariable::META_CLASSES  # => [:foo, :bar, :baz, :qux, :quux, :corge, :grault, :garply, :waldo, :fred, :plugh, :xyzzy, :thud]
MetasyntacticVariable.meta_classes  # => [:foo, :bar, :baz, :qux, :quux, :corge, :grault, :garply, :waldo, :fred, :plugh, :xyzzy, :thud]
~~~

[back to list](#list)

### Module.alias_methods
create alias methods.

~~~ruby
require "tbpgr_utils"

class Hoge
  def hoge
    "hoge"
  end

  alias_methods [:hige, :hege, :huge], :hoge
end

Hoge.new.hoge # => "hoge"
Hoge.new.hige # => "hoge"
Hoge.new.hege # => "hoge"
Hoge.new.huge # => "hoge"
~~~

same code is...  
~~~
class Hoge
  def hoge
    "hoge"
  end

  alias_method :hige, :hoge
  alias_method :hege, :hoge
  alias_method :huge, :hoge
end
~~~

[back to list](#list)

### Numeric#dice_back
each 1-6 case

~~~ruby
1.dice_back # => return 6
2.dice_back # => return 5
3.dice_back # => return 4
4.dice_back # => return 3
5.dice_back # => return 2
6.dice_back # => return 1
~~~

other case

~~~ruby
7.dice_back # => return 7
~~~

[back to list](#list)

### Numeric#dozen
0,1,2 case

~~~ruby
require 'tbpgr_utils'

0.dozen # => return 0
1.dozen # => return 12
2.dozen # => return 24
~~~

[back to list](#list)

[back to list](#list)

### Numeric#ascii?

1,127,128 case  
~~~ruby
require 'tbpgr_utils'

1.ascii? # => return true
127.ascii? # => return true
128.ascii? # => return false
~~~

[back to list](#list)

### Numeric to_binary_html_table

[back to list](#list)
~~~ruby
require 'tbpgr_utils'
Numeric.to_binary_html_table(255, 256)
~~~

result  
~~~
<table>
  <tr>
    <th>10digit</th>
    <th>2digit</th>
  </tr>
  <tr>
    <td>255</td>
    <td>0000000011111111</td>
  </tr>
  <tr>
    <td>256</td>
    <td>0000000100000000</td>
  </tr>
</table>
~~~

[back to list](#list)

### Numeric to_binary_table
1 to 3 case
~~~ruby
require 'tbpgr_utils'
Numeric.to_binary_table(1, 3)
~~~

result  
~~~
|10digit|2digit  |
|1      |00000001|
|2      |00000010|
|3      |00000011|
~~~

[back to list](#list)

### Numeric to_digit_html_table
255 to 256 case
~~~ruby
require 'tbpgr_utils'
Numeric.to_digit_html_table(255, 256)
~~~

result  
~~~html
<table>
  <tr>
    <th>10digit</th>
    <th>2digit</th>
    <th>8digit</th>
    <th>16digit</th>
  </tr>
  <tr>
    <td>255</td>
    <td>0000000011111111</td>
    <td>377</td>
    <td>00ff</td>
  </tr>
  <tr>
    <td>256</td>
    <td>0000000100000000</td>
    <td>400</td>
    <td>0100</td>
  </tr>
</table>
~~~

[back to list](#list)

### Numeric to_digit_table
255 to 256 case  
~~~ruby
require 'tbpgr_utils'
Numeric.to_digit_table(255, 256)
~~~

result  
~~~
|10digit|          2digit|8digit|16digit|
|    255|0000000011111111|   377|   00ff|
|    256|0000000100000000|   400|   0100|
~~~

[back to list](#list)

### Numeric to_hex_html_table
65535 to 65536 case
~~~ruby
require 'tbpgr_utils'
Numeric.to_hex_html_table(65535, 65536)
~~~

result  
~~~
<table>
  <tr>
    <th>10digit</th>
    <th>16digit</th>
  </tr>
  <tr>
    <td>65535</td>
    <td>0000ffff</td>
  </tr>
  <tr>
    <td>65536</td>
    <td>00010000</td>
  </tr>
</table>
~~~

[back to list](#list)

### Numeric to_hex_table
65535 to 65536 case  
~~~ruby
require 'tbpgr_utils'
Numeric.to_hex_table(65535, 65536)
~~~

result  
~~~
|10digit| 16digit|
|  65535|0000ffff|
|  65536|00010000|
~~~

[back to list](#list)

### Numeric to_oct_html_table
65535 to 65536 case  
~~~ruby
require 'tbpgr_utils'
Numeric.to_oct_html_table(65535, 65536)
~~~

result  
~~~
<table>
  <tr>
    <th>10digit</th>
    <th>8digit</th>
  </tr>
  <tr>
    <td>65535</td>
    <td>177777</td>
  </tr>
  <tr>
    <td>65536</td>
    <td>200000</td>
  </tr>
</table>
~~~

[back to list](#list)

### Numeric to_oct_table
65535 to 65536 case  
~~~ruby
require 'tbpgr_utils'
Numeric.to_oct_table(65535, 65536)
~~~

result  
~~~
|10digit|8digit|
|  65535|177777|
|  65536|200000|
~~~

[back to list](#list)

### Object#any_of?
~~~ruby
require 'tbpgr_utils'

p 'hoge'.any_of? 'hoge', 'hige'    # =>true
p 'hoge'.any_of?(*%w{hoge hige})    # =>true
p 'hige'.any_of? 'hoge', 'hige'    # =>true
p 'hege'.any_of? 'hoge', 'hige'    # =>false
p 1.any_of? 1, 2, 3                # =>true
p 4.any_of? 1, 2, 3                # =>false
~~~

[back to list](#list)

### Object#boolean?
~~~ruby
require 'tbpgr_utils'

p true.boolean?    # =>true
p false.boolean?   # =>true
p nil.boolean?     # =>false
p "".boolean?      # =>false
p "true".boolean?  # =>false
~~~

[back to list](#list)

### Object#guard
guard return case

~~~ruby
def hoge(msg)
  guard(msg) {return "guard"}
  "not guard"
end

hoge true # => "guard"
hoge false # => "not guard"
~~~

guard fail case

~~~ruby
def hoge(msg)
  guard(msg) {fail ArgumentError, 'error!!'}
  "not guard"
end

hoge true # => raise ArgumentError. message = error!!
hoge false # => "not guard"
~~~

[back to list](#list)

### Object#grep_method
target class

~~~ruby
require 'tbpgr_utils'

class GrepMethod
  def self.public_method1;end
  def self.public_method2;end
  def self.public_method11;end
  protected
  def self.protected_method1;end
  def self.protected_method2;end
  def self.protected_method11;end
  private
  def self.private_method1;end
  def self.private_method2;end
  def self.private_method11;end
end

GrepMethod.new.grep_method :public_method1, false # => [:public_method1]
GrepMethod.grep_method :public_method1, false # => [:public_method1]
GrepMethod.new.grep_method /public_method1/, false # => [:public_method1, :public_method11]
GrepMethod.grep_method /public_method1/, false # => [:public_method1, :public_method11]
GrepMethod.new.grep_method /public_method3/, false # => []
GrepMethod.grep_method /public_method3/, false # => []
GrepMethod.new.grep_method :__send__, true # => [:__send__]
GrepMethod.grep_method :__send__, true # => [:__send__]
~~~

[back to list](#list)

### Object#grep_private_instance_method
~~~ruby
require 'tbpgr_utils'

# target class
class GrepInstanceMethod
  def public_method1;end
  def public_method2;end
  def public_method11;end
  protected
  def protected_method1;end
  def protected_method2;end
  def protected_method11;end
  private
  def private_method1;end
  def private_method2;end
  def private_method11;end
end

# method call
GrepInstanceMethod.new.grep_private_instance_method :private_method1, false # => [:private_method1]
GrepInstanceMethod.new.grep_private_instance_method /private_method1/, false # => [:private_method1, :private_method11]
GrepInstanceMethod.new.grep_private_instance_method /private_method3/, false # => []
GrepInstanceMethod.new.grep_private_instance_method :equal?, true # => [:equal?]
~~~

[back to list](#list)

### Object#grep_protected_instance_method
~~~ruby
require 'tbpgr_utils'

# target class
class GrepInstanceMethod
  def public_method1;end
  def public_method2;end
  def public_method11;end
  protected
  def protected_method1;end
  def protected_method2;end
  def protected_method11;end
  private
  def private_method1;end
  def private_method2;end
  def private_method11;end
end

# method call
GrepInstanceMethod.new.grep_protected_instance_method :protected_method1, false # => [:protected_method1]
GrepInstanceMethod.new.grep_protected_instance_method /protected_method1/, false # => [:protected_method1, :protected_method11]
GrepInstanceMethod.new.grep_protected_instance_method /protected_method3/, false # => []
GrepInstanceMethod.new.grep_protected_instance_method :equal?, true # => [:equal?]
~~~

[back to list](#list)

### Object#grep_public_instance_method
~~~ruby
require 'tbpgr_utils'

# target class
class GrepInstanceMethod
  def public_method1;end
  def public_method2;end
  def public_method11;end
  protected
  def protected_method1;end
  def protected_method2;end
  def protected_method11;end
  private
  def private_method1;end
  def private_method2;end
  def private_method11;end
end

# method call
GrepInstanceMethod.new.grep_public_instance_method :public_method1, false # => [:public_method1]
GrepInstanceMethod.new.grep_public_instance_method /public_method1/, false # => [:public_method1, :public_method11]
GrepInstanceMethod.new.grep_public_instance_method /public_method3/, false # => []
GrepInstanceMethod.new.grep_public_instance_method :equal?, true # => [:equal?]
~~~

[back to list](#list)

### Object#method_nameable?
~~~ruby
require 'tbpgr_utils'
"string".method_nameable? # => true
:symbol.method_nameable? # => true
1.method_nameable? # => false
~~~

[back to list](#list)

### Object#unless_guard
unless_guard return case

~~~ruby
def hoge(msg)
  unless_guard(msg) {return "unless_guard"}
  "not unless_guard"
end

hoge false # => "unless_guard"
hoge true # => "not unless_guard"
~~~

unless_guard fail case

~~~ruby
def hoge(msg)
  unless_guard(msg) {fail ArgumentError, 'error!!'}
  "not unless_guard"
end

hoge false # => raise ArgumentError. message = error!!
hoge true # => "not unless_guard"
~~~

[back to list](#list)

### Object#my_methods
~~~ruby
require 'tbpgr_utils'

class Hoge
  def hgoe
  end

  protected
  def hige
  end

  private
  def hege
  end
end

p Hoge.new.my_methods # =>[:hoge, :hige, :hege]
~~~

[back to list](#list)

### Object#null?
~~~ruby
hoge = nil
hoge.null? # true
hoge = 'hoge'
hoge.null? # false
~~~

[back to list](#list)

### Object#to_bool
~~~ruby
require 'tbpgr_utils'

p true.to_bool # => true
p false.to_bool # => false
p 'true'.to_bool # => true
p 'false'.to_bool # => true
p nil.to_bool # => false
p 0.to_bool # => true
~~~

[back to list](#list)

### SimpleTournament
init tournament

~~~ruby
require 'simple_tournament'

st = SimpleTournament.new 3
print st.tournament # => [[nil], [nil, nil], [nil, nil]]
~~~

apply challengers

~~~ruby
require 'simple_tournament'

st = SimpleTournament.new 3
st.apply_challengers [*1..3]
print st.tournament # => [[nil], [1, nil], [3, 2]]
~~~

start tournament match

~~~ruby
require 'simple_tournament'

st = SimpleTournament.new 3
st.apply_challengers [*1..3]
st.start_match Proc.new { |one, other|
  rets = []
  winner = (one > other ? one : other)
  rets << winner
  rets << "#{one} : #{other} 's winner is #{winner}"
  rets
}
print st.tournament # => [[3], [1, 3], [3, 2]]
~~~

[back to list](#list)

### String#>>
~~~ruby
require 'tbpgr_utils'

"abc".>> .next # => 'bcd'
"abc".>> :+, "a" # => 'adbdcd'
~~~

[back to list](#list)

### String#ascii1_other2_size
~~~ruby
require 'tbpgr_utils'

'abc'.ord.ascii1_other2_size # => 3
'ａｂｃ'.ord.ascii1_other2_size # => 6
'aａbｂcｃ'.ord.ascii1_other2_size # => 9
~~~

[back to list](#list)

### String#ascii_unicode_html_table
~~~ruby
require 'tbpgr_utils'

'aあb'.ascii_unicode_html_table
~~~

result  
~~~
<table>
  <tr>
    <th>char</th>
    <th>ASCII</th>
    <th>ascii2</th>
    <th>Unicode</th>
  </tr>
  <tr>
    <td>a</td>
    <td>97</td>
    <td>1100001</td>
    <td>--</td>
  </tr>
  <tr>
    <td>あ</td>
    <td>--</td>
    <td>--</td>
    <td>0x3042</td>
  </tr>
  <tr>
    <td>b</td>
    <td>98</td>
    <td>1100010</td>
    <td>--</td>
  </tr>
</table>
~~~

[back to list](#list)

### String#ascii_unicode_table
~~~ruby
require 'tbpgr_utils'

'aあb'.ascii_unicode_table
~~~

result  
~~~
|char|ASCII|ascii2 |Unicode|
| a  | 97  |1100001|  --   |
| あ | --  |  --   |0x3042 |
| b  | 98  |1100010|  --   |
~~~

[back to list](#list)

### String#comma_to_a
space commma case

~~~ruby
require 'tbpgr_utils'
'1, 5, 9'.comma_to_a # => ["1", "5", "9"]
~~~

commma case

~~~ruby
require 'tbpgr_utils'
'1,5,9'.comma_to_a # => ["1", "5", "9"]
~~~

[back to list](#list)

### String#cygwinpath_to_winpath
~~~ruby
require 'tbpgr_utils'
'/cygdrive/c/hoge/hoge.txt'.cygwinpath_to_winpath # => 'C:\hoge\hoge.txt'
~~~

[back to list](#list)

### String#escape_quote
~~~ruby
require 'tbpgr_utils'
"hoge'hige".escape_quote # => "hoge''hige"
~~~

[back to list](#list)

### String#escape_double_quote
~~~ruby
require 'tbpgr_utils'
'hoge"hige'.escape_double_quote # => 'hoge""hige'
~~~

[back to list](#list)

### String#hyphen_to_a
number case

~~~ruby
require 'tbpgr_utils'
'1-5'.hyphen_to_a # => [1, 2, 3, 4, 5]
~~~

alphabet case

~~~ruby
require 'tbpgr_utils'
'"a"-"e"'.hyphen_to_a # => ['a', 'b', 'c', 'd', 'e']
~~~

[back to list](#list)

### String#meta_variable?
~~~ruby
'foo'.meta_variable? # => true
'bar'.meta_variable? # => true
'baz'.meta_variable? # => true
'aaa'.meta_variable? # => false
''.meta_variable? # => false
~~~

[back to list](#list)

### String#justify_char
~~~ruby
require 'tbpgr_utils'

str =<<-EOS
print 'hoge' # => 'hoge'
print 'hoge' * 2 # => 'hogehoge'
print 'hoge' + 'hige' # => 'hogehige'
EOS

str.justify_char('#')
~~~

output  

~~~
print 'hoge'          # => 'hoge'
print 'hoge' * 2      # => 'hogehoge'
print 'hoge' + 'hige' # => 'hogehige'
~~~

[back to list](#list)

### String#justify_table
~~~ruby
require 'tbpgr_utils'

str =<<-EOS
|* hogehogehoge|* hege|* hige|
|test|tester|testest|
|test|tester|aaaaaaaaaaaaaaaaaaaaaaatestest|
EOS

puts str.justify_table
~~~

output  

~~~
|* hogehogehoge|* hage|* hige                        |
|test          |tester|testest                       |
|test          |tester|aaaaaaaaaaaaaaaaaaaaaaatestest|
~~~

[back to list](#list)

### String#say
default case  
~~~ruby
'hoge'.say # => 'hoge'
~~~

quote case  
~~~ruby
'hoge'.say(:quote) # => 'hoge'
~~~

dquote case  
~~~ruby
'hoge'.say(:dquote) # => "hoge"
~~~

bracket case  
~~~ruby
'hoge'.say(:bracket) # => [hoge]
~~~

hyphen case  
~~~ruby
'hoge'.say(:hyphen) # => -hoge-
~~~

[back to list](#list)

### String#spacing
~~~ruby
require 'tbpgr_utils'
hoge = 'hoge'
hoge.spacing # => 'h o g e'
hoge.spacing({char: '_', size: 2}) # => 'h__o__g__e'
~~~

[back to list](#list)

### String#stripe
default case  
~~~ ruby
require 'tbpgr_utils'

'hoge'.stripe # => HoGe
~~~

lower_cap case  
~~~ruby
require 'tbpgr_utils'

'hoge'.stripe :lower_cap # => hOgE
~~~

empty case  
~~~ruby
require 'tbpgr_utils'

''.stripe # => ''
~~~

nil case  
~~~ruby
require 'tbpgr_utils'

hoge = nil
hoge.stripe # => nil
~~~

[back to list](#list)

### String#surround
single line, no option case

~~~ruby
require 'tbpgr_utils'
'hoge'.surround
~~~

result  

~~~
------
|hoge|
------
~~~

multi line, no option case

~~~ruby
require 'tbpgr_utils'
"hoge\na".surround
~~~

result  

~~~
------
|hoge|
|a   |
------
~~~

single line, both option case

~~~ruby
require 'tbpgr_utils'
'hoge'.surround top_bottom: '=', side: '!'
~~~

result  

~~~
======
!hoge!
======
~~~

[back to list](#list)

### String#table_to_array
sample case.

~~~ruby
require 'tbpgr_utils'
BEFORE =<<-EOS
|header1|header2 |header3|
|line1_1| line1_2|line1_3|
EOS
BEFORE.table_to_array
~~~

result  
~~~ruby
[["header1", "header2", "header3"], ["line1_1", "line1_2", "line1_3"]]
~~~

[back to list](#list)

### String#to_hatena_heading
&gt; case  
~~~ruby
require 'tbpgr_utils'
'hoge>hige'.to_hatena_heading # => '*hoge\n**hige'
~~~

\+ case  
~~~ruby
require 'tbpgr_utils'

'hoge+hige'.to_hatena_heading # => '*hoge\n*hige'
~~~

^ case  
~~~ruby
require 'tbpgr_utils'
'hoge>hige^hege'.to_hatena_heading # => '*hoge\n**hige\n*hege'
~~~

[back to list](#list)

### String#to_markdown_heading
&gt; case  
~~~ruby
require 'tbpgr_utils'
'hoge>hige'.to_markdown_heading # => '# hoge\n## hige'
~~~

\+ case  
~~~ruby
require 'tbpgr_utils'

'hoge+hige'.to_markdown_heading # => '# hoge\n# hige'
~~~

^ case  
~~~ruby
require 'tbpgr_utils'
'hoge>hige^hege'.to_markdown_heading # => '# hoge\n## hige\n# hege'
~~~

[back to list](#list)

### String#to_space2_heading
&gt; case  
~~~ruby
require 'tbpgr_utils'
'hoge>hige'.to_space2_heading # => 'hoge\n  hige'
~~~

\+ case  
~~~ruby
require 'tbpgr_utils'

'hoge+hige'.to_space2_heading # => 'hoge\nhige'
~~~

^ case  
~~~ruby
require 'tbpgr_utils'
'hoge>hige^hege'.to_space2_heading # => 'hoge\n  hige\nhege'
~~~

[back to list](#list)

### String#to_space4_heading
&gt; case  
~~~ruby
require 'tbpgr_utils'
'hoge>hige'.to_space4_heading # => 'hoge\n    hige'
~~~

\+ case  
~~~ruby
require 'tbpgr_utils'
'hoge+hige'.to_space4_heading # => 'hoge\nhige'
~~~

^ case  
~~~ruby
require 'tbpgr_utils'
'hoge>hige^hege'.to_space4_heading # => 'hoge\n    hige\nhege'
~~~

[back to list](#list)

### String#to_tab_heading
&gt; case  
~~~ruby
require 'tbpgr_utils'
'hoge>hige'.to_tab_heading # => 'hoge\n\thige'
~~~

\+ case  
~~~ruby
require 'tbpgr_utils'
'hoge+hige'.to_tab_heading # => 'hoge\nhige'
~~~

^ case  
~~~ruby
require 'tbpgr_utils'
'hoge>hige^hege'.to_tab_heading # => 'hoge\n\thige\nhege'
~~~

[back to list](#list)

### String#unescape_double_quote
~~~ruby
require 'tbpgr_utils'
'hoge""hige'.unescape_double_quote # => 'hoge"hige'
~~~

[back to list](#list)

### String#unescape_quote
~~~ruby
require 'tbpgr_utils'
"hoge''h''ige".unescape_quote # => "hoge'h'ige"
~~~

[back to list](#list)

### String#uniq
~~~ruby
require 'tbpgr_utils'
'abcdac'.uniq # => 'abcd'
~~~

[back to list](#list)

### String#uniq_size
~~~ruby
require 'tbpgr_utils'
'abcdefa'.uniq_size # => 6
'abcdef'.uniq_size # => 6
''.uniq_size # => 0
~~~

[back to list](#list)

### String#winpath_to_cygwinpath
~~~ruby
require 'tbpgr_utils'
'C:\hoge\hoge.txt'.winpath_to_cygwinpath # => '/cygdrive/c/hoge/hoge.txt'
~~~

[back to list](#list)

### Symbol#meta_variable?
~~~ruby
:foo.meta_variable? # => true
:bar.meta_variable? # => true
:baz.meta_variable? # => true
:aaa.meta_variable? # => false
~~~

[back to list](#list)

### Templatable
* include Templatable
* set template by here-document
* in template, parameter must name 'placeholders[:xxxxx]'. xxxxx is your favorite name.
* when create instance, you must set materials to create template. after, you can get this value from @materials.
* you must create manufactured_xxx methods. xxx is each-placeholder name.
* you can get result by 'result' method.

~~~ruby
require 'templatable'

class TemplateUser
  include Templatable
  template <<-EOS
line1:<%=placeholders[:hoge]%>
line2:<%=placeholders[:hige]%>
  EOS

  def manufactured_hoge
    "hoge-#{@materials}"
  end

  def manufactured_hige
    "hige-#{@materials}"
  end
end

p TemplateUser.new('sample').result  
~~~

output  
~~~
line1:hoge-sample
line2:hige-sample
~~~

[back to list](#list)

## TemplateMethodable
sample usage

~~~ruby
require "template_methodable"
# sample BaseClass
class BaseDeveloper
  include TemplateMethodable
  must_impl :easy_coding, :difficult_coding, :normal_coding
  module DIFFICILTY
    EASY = 1
    NORMAL = 2
    DIFFICILT = 3
  end
  def coding(difficulty)
    ret = []
    ret << "start coding"
    case difficulty
    when DIFFICILTY::EASY
      ret << easy_coding
    when DIFFICILTY::NORMAL
      ret << normal_coding
    when DIFFICILTY::DIFFICILT
      ret << difficult_coding
    else
      fail 'error'
    end
    ret << "finish coding"
    ret.join("\n")
  end
end

# sample valid Concrete Class.
class StarDeveloper < BaseDeveloper
  def easy_coding
    "complete 1 minutes"
  end
  def normal_coding
    "complete 10 minutes"
  end
  def difficult_coding
    "complete 59 minutes"
  end
end

# sample invalid Concrete Class. if call NormalDeveloper#difficult_coding, it raises NotImplementedError.
class NormalDeveloper < BaseDeveloper
  def easy_coding
    "complete 10 minutes"
  end
  def normal_coding
    "complete 100 minutes"
  end
end
~~~

## Relation
if you are Sublime Text2 user, you can use snippet for TbpgrUtils.

https://github.com/tbpgr/tbpgr_utils_snippets

## History
* version 0.0.151 : add Enumerable#if_else_map, change class Array#sum to Enumerable#sum, change class Array#kernel_send to Enumerable#kernel_send
* version 0.0.150 : add AttrEnumerable.slice_attr
* version 0.0.149 : add AttrEnumerable.shuffle_attr
* version 0.0.148 : add AttrEnumerable.select_attr
* version 0.0.147 : add AttrEnumerable.sample_attr
* version 0.0.146 : add AttrEnumerable.reduce_attr
* version 0.0.145 : add AttrEnumerable.map_attr
* version 0.0.144 : add AttrEnumerable.last_attr
* version 0.0.143 : add AttrEnumerable.include_attr?
* version 0.0.142 : add AttrEnumerable.first_attr
* version 0.0.141 : add AttrEnumerable.delete_attr
* version 0.0.140 : add AttrEnumerable.concat_attr
* version 0.0.139 : add AttrEnumerable.compact_attr
* version 0.0.138 : add AttrEnumerable.at_attr
* version 0.0.137 : add AttrEnumerable.reverse_attr
* version 0.0.136 : add AttrEnumerable.each_attr_with_index
* version 0.0.135 : add AttrEnumerable.each_attr
* version 0.0.134 : add Integer#reverse_each_digit
* version 0.0.133 : add Integer#each_digit_with_index
* version 0.0.132 : add Integer#each_digit
* version 0.0.131 : add Object#grep_protected_instance_method, Object#grep_private_instance_method
* version 0.0.130 : add Object#grep_method
* version 0.0.129 : add Object#grep_public_instance_method
* version 0.0.128 : add Array#exchange, change Kernel#bulk_puts_eval output format(justify)
* version 0.0.127 : add String#uniq_size
* version 0.0.126 : add Array#uniq_size
* version 0.0.125 : add Hash#>>
* version 0.0.124 : change spec of Array#>>, String#>>
* version 0.0.123 : add String#>>
* version 0.0.122 : add String#justify_char
* version 0.0.121 : add Array#average
* version 0.0.120 : add Array#sum
* version 0.0.119 : add Kernel#exchange
* version 0.0.118 : add String#uniq
* version 0.0.117 : add Array#kernel_send
* version 0.0.116 : add Array#>>
* version 0.0.115 : add MarkdownString#codes
* version 0.0.114 : add MarkdownString#code
* version 0.0.113 : add MarkdownString#link
* version 0.0.112 : add MarkdownString#backquotes
* version 0.0.111 : add MarkdownString#bold
* version 0.0.110 : add MarkdownString#italic
* version 0.0.109 : add MarkdownString#hr
* version 0.0.108 : add MarkdownString#ol
* version 0.0.107 : add MarkdownString#ul
* version 0.0.106 : add MarkdownString#heading3, heading4, heading5, heading6
* version 0.0.105 : add MarkdownString#heading2
* version 0.0.104 : add MarkdownString#heading1. remove File.insert_bom.
* version 0.0.103 : add Integer#palindromic_prime
* version 0.0.102 : add String#cygwinpath_to_winpath
* version 0.0.101 : add String#winpath_to_cygwinpath
* version 0.0.100 : add String#ascii_unicode_html_table
* version 0.0.99 : add Numeric.to_oct_html_table
* version 0.0.98 : add Numeric.to_hex_html_table
* version 0.0.97 : add Numeric.to_digit_html_table
* version 0.0.96 : add Numeric.to_binary_html_table
* version 0.0.95 : add Hash#html_table
* version 0.0.94 : add String#unescape_quote
* version 0.0.93 : add String#unescape_double_quote
* version 0.0.92 : add Fixnum.to_fixnum_html_table
* version 0.0.91 : add Array#to_html_table
* version 0.0.90 : add Kernel#hash_to_attributes
* version 0.0.89 : add String#escape_quote
* version 0.0.88 : add String#escape_double_quote
* version 0.0.87 : add String#spacing
* version 0.0.86 : add Familyable
* version 0.0.85 : add String#table_to_array
* version 0.0.84 : add Fixnum to_fixnum_table
* version 0.0.83 : add Numeric to_digit_table
* version 0.0.82 : add Numeric to_oct_table
* version 0.0.81 : add Numeric to_hex_table
* version 0.0.80 : add Numeric to_binary_table
* version 0.0.79 : add Array#to_table
* version 0.0.78 : add String#ascii_unicode_table
* version 0.0.77 : add String#meta_variable?, Symbol#meta_variable?
* version 0.0.76 : add EvalHelper#attr_init_class_code, Numeric#ascii?, String#ascii1_other2_size
* version 0.0.75 : add Object#method_nameable?
* version 0.0.74 : add Hash#table
* version 0.0.73 : add Kernel#evalb
* version 0.0.72 : add Kernel#null, Object#null?
* version 0.0.71 : add Kernel booleans
* version 0.0.70 : add SimpleTournament
* version 0.0.69 : add Numeric#dozen
* version 0.0.68 : add Numeric#dice_back
* version 0.0.67 : add EvalHelper#attr_accessor_init_code
* version 0.0.66 : add EvalHelper#each_with_index_do_code
* version 0.0.65 : add EvalHelper#each_with_index_brace_code
* version 0.0.64 : add EvalHelper#each_do_code
* version 0.0.63 : add EvalHelper#each_brace_code, String#hyphen_to_a, String#commma_to_a
* version 0.0.62 : add EvalHelper#set_variables_code
* version 0.0.61 : add EvalHelper#set_variable_code
* version 0.0.60 : add EvalHelper#times_code
* version 0.0.59 : add EvalHelper Object
* version 0.0.58 : add EvalHelper#require_relative_code
* version 0.0.57 : add EvalHelper#require_code
* version 0.0.56 : add EvalHelper#toternary_operator
* version 0.0.55 : add EvalHelper#unless_code_after
* version 0.0.54 : add EvalHelper#unless_code
* version 0.0.53 : add EvalHelper#if_code_after
* version 0.0.52 : add EvalHelper#if_code
* version 0.0.51 : add String#to_hatena_heading
* version 0.0.50 : add String#to_markdown_heading
* version 0.0.49 : add String#to_tab_heading
* version 0.0.48 : add String#to_space4_heading
* version 0.0.47 : add String#to_space2_heading
* version 0.0.46 : add String#stripe
* version 0.0.45 : add String#say
* version 0.0.44 : add EndERB.apply
* version 0.0.43 : add Array#together_slice(alias tslice).
* version 0.0.42 : add MetasyntacticVariable
* version 0.0.41 : add Object#guard, unless_guard
* version 0.0.40 : add Kernel#aa_ancestors.
* version 0.0.39 : add String#surround.
* version 0.0.38 : add Array#together_shuffle(alias tshuffle).
* version 0.0.37 : add Array#together_sample(alias tsample).
* version 0.0.36 : add Array#together_reverse,Array#together_reverse!(alias treverse, alias treverse!).
* version 0.0.35 : add Array#together_pop(alias tpop).
* version 0.0.34 : add Array#together_last(alias tlast).
* version 0.0.33 : add Array#together_shift(alias tshift).
* version 0.0.32 : add Array#together_insert(alias tinsert).
* version 0.0.31 : add Array#together_index(alias tindex).
* version 0.0.30 : add Array#together_include?(alias tinclude?).
* version 0.0.29 : add Array#together_first(alias tfirst).
* version 0.0.28 : add Array#together_fill(alias tfill). add File.insert_bom.
* version 0.0.27 : add Array#together_empty?(alias tempty?)
* version 0.0.26 : add Array#together_delete_if(alias tdelete_if)
* version 0.0.25 : add Array#together_delete_at(alias tdelete_at)
* version 0.0.24 : add Array#together_delete(alias tdelete)
* version 0.0.23 : add Array#together_map!(aliases => [tmap!, together_collect!, tcollect!])
* version 0.0.22 : add Array#together_compact. together_compact has alias :tcompact. Array#together_compact!. together_compact! has alias :tcompact!.
* version 0.0.21 : add Array#together_clear. together_clear has alias :tclear
* version 0.0.20 : add Array#together_at. together_at has alias :tat
* version 0.0.19 : add AttributesHashable module.
* version 0.0.18 : add Array#together_concat. together_concat has alias tconcat
* version 0.0.17 : add Array#together_reduce(or treduce, together_inject, tinject)
* version 0.0.16 : add Array#together_select(or tselect, together_find_all, tfindall)
* version 0.0.15 : add Module.alias_methods
* version 0.0.14 : add Array#together_map(aliases => [tmap, together_collect, tcollect])
* version 0.0.13 : add Array#together_with_index, Kernel#bulk_puts_eval
* version 0.0.12 : AttributesInitializable::ClassMethods.attr_reader_init,attr_writer_init
* version 0.0.11 : add Object#to_bool.
* version 0.0.10 : add TemplateMethodable module.
* version 0.0.9  : add TestToolbox module. add Kernel#capture_stdout, Kernel#dp_line
* version 0.0.8  : add Kernel#bulk_define_methods
* version 0.0.7  : add Kernel#print_eval, Kernel#puts_eval
* version 0.0.6  : add Ghostable
* version 0.0.5  : add Templatable
* version 0.0.4  : AttributesInitializable::ClassMethods.attr_accessor_init
* version 0.0.3  : add Object#any_of?
* version 0.0.2  : loop all arrays by block.
* version 0.0.1  : first release.

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
