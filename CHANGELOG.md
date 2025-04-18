# Change log

<!---
  Do NOT edit this CHANGELOG.md file by hand directly, as it is automatically updated.

  Please add an entry file to the https://github.com/rubocop/rubocop/blob/master/changelog/
  named `{change_type}_{change_description}.md` if the new code introduces user-observable changes.

  See https://github.com/rubocop/rubocop/blob/master/CONTRIBUTING.md#changelog-entry-format for details.
-->

## master (unreleased)

## 1.75.2 (2025-04-03)

### Changes

* [#14065](https://github.com/rubocop/rubocop/pull/14065): Update `Lint/RedundantTypeConversion` to register an offense for `to_json.to_s`. ([@lovro-bikic][])

### Bug fixes

* [#14041](https://github.com/rubocop/rubocop/issues/14041): Fix an error when using ERB templated config YAML with server mode. ([@koic][])
* [#14048](https://github.com/rubocop/rubocop/pull/14048): Do not emit a warning for a zero-sized file while checking if it is executable. ([@viralpraxis][])
* [#14053](https://github.com/rubocop/rubocop/issues/14053): Fix incorrect autocorrect for `Lint/DeprecatedOpenSSLConstant` cipher constant argument is not `cbc`. ([@koic][])
* [#14051](https://github.com/rubocop/rubocop/issues/14051): Fix incorrect autocorrect for `Style/RedundantCondition` when true is used as the true branch and the condition takes arguments. ([@koic][])
* [#14062](https://github.com/rubocop/rubocop/issues/14062): Fix false positives for `Lint/ReturnInVoidContext` when returning inside `define_method` or a nested singleton method. ([@earlopain][])
* [#14057](https://github.com/rubocop/rubocop/pull/14057): Fix `Style/ConditionalAssignment` cop error on dynamic string node in branch. ([@viralpraxis][])
* [#14047](https://github.com/rubocop/rubocop/pull/14047): Fix `Style/FrozenStringLiteralComment` cop errors on emacs-styled magic comment. ([@viralpraxis][])

## 1.75.1 (2025-03-26)

### Changes

* [#14038](https://github.com/rubocop/rubocop/pull/14038): Rename `EnforcedStyle: allow_named_parameter` to `EnforcedStyle: only_numbered_parameters` in `Style/ItBlockParameter`. ([@koic][])

## 1.75.0 (2025-03-26)

### New features

* [#12049](https://github.com/rubocop/rubocop/issues/12049): Add new `Style/HashFetchChain` cop to detect chained `fetch` calls that can be replaced with a single call to `dig`. ([@dvandersluis][])
* [#13597](https://github.com/rubocop/rubocop/issues/13597): Add new `Style/ItBlockParameter` cop. ([@koic][])
* [#13899](https://github.com/rubocop/rubocop/pull/13899): Enable reusable Prism parse result for Ruby LSP add-on. ([@koic][])
* [#14015](https://github.com/rubocop/rubocop/pull/14015): Support `it` block parameter in `Layout` cops. ([@koic][])
* [#14017](https://github.com/rubocop/rubocop/pull/14017): Support `it` block parameter in `Lint` cops. ([@koic][])
* [#14018](https://github.com/rubocop/rubocop/pull/14018): Support `it` block parameter in `Metrics` cops. ([@koic][])
* [#14013](https://github.com/rubocop/rubocop/pull/14013): Support `it` block parameter in `Style` cops. ([@koic][])
* [#14025](https://github.com/rubocop/rubocop/pull/14025): Support `TargetRubyVersion: 3.5` (experimental). ([@earlopain][])

### Bug fixes

* [#14022](https://github.com/rubocop/rubocop/pull/14022): Fix an error for `Style/HashFetchChain` when no arguments are given to `fetch`. ([@koic][])
* [#14028](https://github.com/rubocop/rubocop/pull/14028): Fix false negative for `Layout/MultilineMethodParameterLineBreaks` when class method definitions are used. ([@vlad-pisanov][])
* [#14027](https://github.com/rubocop/rubocop/pull/14027): Fix false negative for `Layout/LineLength` when autocorrecting class method definitions. ([@vlad-pisanov][])
* [#8099](https://github.com/rubocop/rubocop/issues/8099): Fix infinite loop between `Layout/SpaceAroundOperators` and `Layout/HashAlignment` with `EnforcedHashRocketStyle` being an array containing `table`. ([@dvandersluis][])
* [#14021](https://github.com/rubocop/rubocop/pull/14021): Fix handling of long heredoc lines with SplitStrings enabled. ([@mauro-oto][])
* [#13968](https://github.com/rubocop/rubocop/pull/13968): Fix `InternalAffairs/RedundantDescribedClassAsSubject` cop error on missing `describe`. ([@viralpraxis][])
* [#14036](https://github.com/rubocop/rubocop/pull/14036): Fix false negative for `Lint/ShadowingOuterLocalVariable` when block local variable is used inside a condition. ([@lovro-bikic][])
* [#13990](https://github.com/rubocop/rubocop/issues/13990): Fix a false positive for `Lint/UselessAssignment` when a variable is reassigned in a different branch. ([@eugeneius][])
* [#14012](https://github.com/rubocop/rubocop/pull/14012): Fix incorrect autocorrections for `Style/SoleNestedConditional`. ([@lovro-bikic][])
* [#14020](https://github.com/rubocop/rubocop/pull/14020): Fix comment autocorrection for `Style/IfInsideElse`. ([@lovro-bikic][])

### Changes

* [#12358](https://github.com/rubocop/rubocop/issues/12358): Add `does` as a forbidden prefix to `Naming/PredicateName`. ([@dvandersluis][])
* [#13621](https://github.com/rubocop/rubocop/issues/13621): Add `ForbiddenIdentifiers` and `ForbiddenPatterns` config options to `Naming/MethodName` cop. ([@tejasbubane][])
* [#13986](https://github.com/rubocop/rubocop/issues/13986): Add support for `Array#intersection` to `Style/ArrayIntersect`. ([@dvandersluis][])
* [#14006](https://github.com/rubocop/rubocop/pull/14006): Allow cop renames to trigger warnings instead of fatal errors. ([@dvandersluis][])
* [#13617](https://github.com/rubocop/rubocop/issues/13617): Use the `prism` translation layer to analyze Ruby 3.4+ by default. ([@earlopain][])
* [#14024](https://github.com/rubocop/rubocop/pull/14024): Change `Style/RedundantParentheses` to offend parentheses for chained `&&` expressions. ([@lovro-bikic][])
* [#14029](https://github.com/rubocop/rubocop/pull/14029): Add `AllowConsecutiveConditionals` setting to `Style/Next` to allow consecutive conditional statements. ([@vlad-pisanov][])
* [#14016](https://github.com/rubocop/rubocop/pull/14016): Update `Style/RedundantFormat` to register offenses when the only argument to `format` or `sprintf` is a constant. ([@dvandersluis][])

## 1.74.0 (2025-03-13)

### New features

* [#13936](https://github.com/rubocop/rubocop/pull/13936): Adds new cop `Style/ComparableBetween`. ([@lovro-bikic][])
* [#13943](https://github.com/rubocop/rubocop/pull/13943): Allow writing steep annotation to method definition for `Style/CommentedKeyword`. ([@dak2][])

### Bug fixes

* [#13969](https://github.com/rubocop/rubocop/issues/13969): Fix a false positive for `Lint/SharedMutableDefault` when `capacity` keyword argument is used. ([@koic][])
* [#13945](https://github.com/rubocop/rubocop/pull/13945): Fix a false positive for `Style/DoubleNegation` when calling `define_method`/`define_singleton_method` with a numblock. ([@earlopain][])
* [#13971](https://github.com/rubocop/rubocop/pull/13971): Fix false alarm for config obsoletion. ([@koic][])
* [#13960](https://github.com/rubocop/rubocop/pull/13960): Fix a false negative for `Lint/ReturnInVoidContext` when returning out of a block. ([@earlopain][])
* [#13947](https://github.com/rubocop/rubocop/pull/13947): Fix a false negative for `Lint/UselessConstantScoping` for constants defined in `class << self`. ([@earlopain][])
* [#13949](https://github.com/rubocop/rubocop/pull/13949): Fix a false negative for `Lint/NonLocalExitFromIterator` with numblocks. ([@earlopain][])
* [#13975](https://github.com/rubocop/rubocop/issues/13975): Fix false positives for `Style/RedundantCurrentDirectoryInPath` when using a complex current directory path in `require_relative`. ([@koic][])
* [#13963](https://github.com/rubocop/rubocop/issues/13963): Fix wrong autocorrect for `Lint/LiteralAsCondition` when the literal is followed by `return`, `break`, or `next`. ([@earlopain][])
* [#13946](https://github.com/rubocop/rubocop/pull/13946): Fix some false positives for `Style/MethodCallWithArgsParentheses` with `EnforcedStyle: omit_parentheses` style and numblocks. ([@earlopain][])
* [#13950](https://github.com/rubocop/rubocop/pull/13950): Fix sporadic errors about `rubocop-rails` or `rubocop-performance` extraction, even if they are already part of the Gemfile. ([@earlopain][])
* [#13981](https://github.com/rubocop/rubocop/pull/13981): Prevent redundant plugin loading when a duplicate plugin is specified in an inherited config. ([@koic][])
* [#13965](https://github.com/rubocop/rubocop/issues/13965): Update `Lint/RedundantCopDisableDirective` to register an offense when cop names are given with improper casing. ([@dvandersluis][])
* [#13948](https://github.com/rubocop/rubocop/pull/13948): Fix wrong autocorrect for `Style/RescueModifier` when using parallel assignment and the right-hand-side is not a bracketed array. ([@earlopain][])

### Changes

* [#12851](https://github.com/rubocop/rubocop/issues/12851): Add `EnforcedStyleForClasses` and `EnforcedStyleForModules` configuration options to `Style/ClassAndModuleChildren`. ([@dvandersluis][])
* [#13979](https://github.com/rubocop/rubocop/pull/13979): Add `Mode: conservative` configuration to `Style/FormatStringToken` to make the cop only register offenses for strings given to `printf`, `sprintf`, `format`, and `%`. ([@dvandersluis][])
* [#13977](https://github.com/rubocop/rubocop/issues/13977): Allow `TLS1_1` and `TLS1_2` by default in `Naming/VariableNumber` to accommodate OpenSSL version parameter names. ([@koic][])
* [#13967](https://github.com/rubocop/rubocop/pull/13967): Make `Lint/RedundantTypeConversion` aware of redundant `to_d`. ([@koic][])

## 1.73.2 (2025-03-04)

### Bug fixes

* [#13942](https://github.com/rubocop/rubocop/pull/13942): Fix incorrect disabling of departments when inheriting configuration. ([@koic][])
* [#13766](https://github.com/rubocop/rubocop/issues/13766): Fix false positives for `Style/InverseMethods` when using `any?` or `none?` with safe navigation operator. ([@koic][])
* [#13938](https://github.com/rubocop/rubocop/pull/13938): Fix false positives for `Style/RedundantCondition` when a variable or a constant is used. ([@koic][])
* [#13935](https://github.com/rubocop/rubocop/pull/13935): Fix a false negative for `Style/RedundantFreeze` when calling methods that produce frozen objects with numblocks. ([@earlopain][])
* [#13928](https://github.com/rubocop/rubocop/issues/13928): Fix `end pattern with unmatched parenthesis: / (RegexpError)` on Ruby 3.2.0. ([@dvandersluis][])
* [#13933](https://github.com/rubocop/rubocop/issues/13933): Fix wrong autocorrect for `Style/KeywordParametersOrder` when the arguments are on multiple lines and contain comments. ([@earlopain][])

### Changes

* [#12669](https://github.com/rubocop/rubocop/issues/12669): Update autocorrection for `Lint/EmptyConditionalBody` to be safe. ([@dvandersluis][])

## 1.73.1 (2025-02-27)

### Bug fixes

* [#13920](https://github.com/rubocop/rubocop/issues/13920): Fix an error for `Lint/MixedCaseRange` when `/[[ ]]/` is used. ([@koic][])
* [#13912](https://github.com/rubocop/rubocop/pull/13912): Fix wrong autocorrect for `Lint/EmptyConditionalBody` when assigning to a variable with only a single branch. ([@earlopain][])
* [#13913](https://github.com/rubocop/rubocop/issues/13913): Fix false positives for `Style/RedundantCondition` when using when true is used as the true branch and the condition is not a predicate method. ([@koic][])
* [#13909](https://github.com/rubocop/rubocop/issues/13909): Fix false positive with `Layout/ClosingParenthesisIndentation` when first parameter is a hash. ([@tejasbubane][])
* [#13915](https://github.com/rubocop/rubocop/pull/13915): Fix writing generics type of rbs-inline annotation for nested class in `Style/CommentedKeyword`. ([@dak2][])
* [#13916](https://github.com/rubocop/rubocop/issues/13916): Fix `Lint/LiteralAsCondition` acting on the right hand side of && nodes. ([@zopolis4][])

## 1.73.0 (2025-02-26)

### New features

* [#11024](https://github.com/rubocop/rubocop/issues/11024): Add `require_always` option to `Style/EndlessMethod`. ([@koic][])
* [#11024](https://github.com/rubocop/rubocop/issues/11024): Add `require_single_line` option to `Style/EndlessMethod`. ([@jtannas][])
* [#9935](https://github.com/rubocop/rubocop/issues/9935): Introduce EnforcedStyleForMultiline "diff_comma". ([@flavorjones][])

### Bug fixes

* [#13867](https://github.com/rubocop/rubocop/issues/13867): Fix an error for plugins when not running RuboCop through Bundler. ([@earlopain][])
* [#13902](https://github.com/rubocop/rubocop/pull/13902): Fix false negative for `Style/RedundantSelfAssignment` when the method receives a block. ([@vlad-pisanov][])
* [#13826](https://github.com/rubocop/rubocop/issues/13826): Fix false positives for regex cops when `Lint/MixedCaseRange` is enabled. ([@earlopain][])
* [#13818](https://github.com/rubocop/rubocop/issues/13818): Fix false positives for `Lint/Void` when using operator method call without argument. ([@koic][])
* [#13896](https://github.com/rubocop/rubocop/pull/13896): Fix a false positive for `Style/TrivialAccessors` with `instance_eval` and numblocks. ([@earlopain][])
* [#13910](https://github.com/rubocop/rubocop/pull/13910): Fix false positives for `Style/EndlessMethod` when using setter method definitions. ([@koic][])
* [#13889](https://github.com/rubocop/rubocop/pull/13889): Fix autocorrection for `Layout/LineLength` with interpolated strings when not on the first line. ([@dvandersluis][])
* [#13900](https://github.com/rubocop/rubocop/issues/13900): Fix infinite loop between `Layout/EmptyLinesAroundAccessModifier` and `Layout/EmptyLinesAroundBlockBody` with `EnforcedStyle: no_empty_lines`. ([@dvandersluis][])
* [#12692](https://github.com/rubocop/rubocop/issues/12692): Fix `Style/AccessorGrouping` with constants. ([@tejasbubane][])
* [#13882](https://github.com/rubocop/rubocop/issues/13882): Fix `Style/RedundantFormat` for annotated template strings with missing hash keys. ([@dvandersluis][])
* [#13880](https://github.com/rubocop/rubocop/issues/13880): Fix `Style/RedundantFormat` when given double-splatted arguments. ([@dvandersluis][])
* [#13907](https://github.com/rubocop/rubocop/pull/13907): Don't offer autocorrect for `Style/StringConcatenation` when numblocks are used. ([@earlopain][])
* [#13876](https://github.com/rubocop/rubocop/issues/13876): Don't consider `require 'pp'` to be redundant for `Lint/RedundantRequireStatement`. ([@earlopain][])
* [#13885](https://github.com/rubocop/rubocop/issues/13885): Update `Style/HashExcept` and `Style/HashSlice` to not register an offense if selecting over the hash value. ([@dvandersluis][])

### Changes

* [#12948](https://github.com/rubocop/rubocop/issues/12948): Add `ForbiddenNames` configuration to `Naming/VariableName` to specify names that are forbidden. ([@dvandersluis][])
* [#13117](https://github.com/rubocop/rubocop/issues/13117): Add partial autocorrect support to `Lint/LiteralAsCondition` cop to check for redundant conditions. ([@zopolis4][])
* [#13892](https://github.com/rubocop/rubocop/pull/13892): Allow merging of configured arrays and non-arrays. ([@sambostock][])
* [#13833](https://github.com/rubocop/rubocop/pull/13833): Add `Reference` to common params. ([@sambostock][])
* [#13890](https://github.com/rubocop/rubocop/pull/13890): Update `Lint/RedundantTypeConversion` to not register an offense when given a constructor with `exception: false`. ([@dvandersluis][])
* [#13729](https://github.com/rubocop/rubocop/pull/13729): Update `Style/RedundantCondition` cop to detect conditional expressions where the true branch is `true` and suggest replacing them with a logical OR. ([@datpmt][])

## 1.72.2 (2025-02-17)

### Bug fixes

* [#13853](https://github.com/rubocop/rubocop/pull/13853): Fix exclusion of relative paths in plugin's `AllCops: Exclude` as expected. ([@koic][])
* [#13844](https://github.com/rubocop/rubocop/issues/13844): Fix an error for `Style/RedundantFormat` when a template argument is used without keyword arguments. ([@koic][])
* [#13857](https://github.com/rubocop/rubocop/pull/13857): Fix an error for `Style/RedundantFormat` when numeric placeholders is used in the template argument. ([@koic][])
* [#13861](https://github.com/rubocop/rubocop/issues/13861): Fix `ArgumentError` related to two deprecated `AllowedPattern` APIs. ([@koic][])
* [#13849](https://github.com/rubocop/rubocop/issues/13849): Fix an error for `Lint/UselessConstantScoping` when multiple assigning to constants after `private` access modifier. ([@koic][])
* [#13856](https://github.com/rubocop/rubocop/issues/13856): Fix false positives for `Lint/UselessConstantScoping` when a constant is used after `private` access modifier with arguments. ([@koic][])

### Changes

* [#13846](https://github.com/rubocop/rubocop/issues/13846): Mark `Style/RedundantFormat` as unsafe autocorrect. ([@koic][])

## 1.72.1 (2025-02-15)

### Bug fixes

* [#13836](https://github.com/rubocop/rubocop/issues/13836): Fix an error for `Style/RedundantParentheses` when a different expression appears before a range literal. ([@koic][])
* [#13839](https://github.com/rubocop/rubocop/issues/13839): Fix false positives for `Lint/RedundantTypeConversion` when passing block arguments when generating a Hash or a Set. ([@koic][])

### Changes

* [#13839](https://github.com/rubocop/rubocop/pull/13839): Extension plugin is loaded automatically with `require 'rubocop/rspec/support'. ([@koic][])

## 1.72.0 (2025-02-14)

### New features

* [#13740](https://github.com/rubocop/rubocop/pull/13740): Add new `Lint/CopDirectiveSyntax` cop. ([@kyanagi][])
* [#13800](https://github.com/rubocop/rubocop/issues/13800): Add new `Lint/SuppressedExceptionInNumberConversion` cop. ([@koic][])
* [#13702](https://github.com/rubocop/rubocop/pull/13702): Add new `Lint/RedundantTypeConversion` cop. ([@dvandersluis][])
* [#13831](https://github.com/rubocop/rubocop/pull/13831): Add new `Lint/UselessConstantScoping` cop. ([@koic][])
* [#13793](https://github.com/rubocop/rubocop/pull/13793): Add new `Style/RedundantFormat` cop to check for uses of `format` or `sprintf` with only a single string argument. ([@dvandersluis][])
* [#13581](https://github.com/rubocop/rubocop/pull/13581): Add new `InternalAffairs/LocationExists` cop to check for code that can be replaced with `Node#loc?` or `Node#loc_is?`. ([@dvandersluis][])
* [#13661](https://github.com/rubocop/rubocop/issues/13661): Make server mode detect local paths in .rubocop.yml under `inherit_from` and `require` for automatically restart. ([@koic][])
* [#13721](https://github.com/rubocop/rubocop/pull/13721): `Naming/PredicateName`: Optionally use Sorbet to detect predicate methods. ([@issyl0][])
* [#6012](https://github.com/rubocop/rubocop/issues/6012): Support RuboCop extension plugin. ([@koic][])

### Bug fixes

* [#13807](https://github.com/rubocop/rubocop/issues/13807): Fix false negatives for `Style/RedundantParentheses` when chaining `[]` method calls. ([@koic][])
* [#13788](https://github.com/rubocop/rubocop/issues/13788): Fix false negatives for `Style/RedundantParentheses` when `[]` method is called with variable or constant receivers. ([@koic][])
* [#13811](https://github.com/rubocop/rubocop/issues/13811): Fix false negatives for `Style/RedundantParentheses` when handling range literals with redundant parentheses. ([@koic][])
* [#13796](https://github.com/rubocop/rubocop/pull/13796): Fix crash in `Layout/EmptyLinesAroundMethodBody` for endless methods. ([@dvandersluis][])
* [#13817](https://github.com/rubocop/rubocop/pull/13817): Fix false positive for format specifier with non-numeric precision. ([@dvandersluis][])
* [#12672](https://github.com/rubocop/rubocop/issues/12672): Fix false positives for `Lint/FormatParameterMismatch` when the width value is interpolated. ([@dvandersluis][])
* [#12795](https://github.com/rubocop/rubocop/issues/12795): Fix `Layout/BlockAlignment` for blocks that are the body of an endless method. ([@dvandersluis][])
* [#13822](https://github.com/rubocop/rubocop/pull/13822): Fix undefined method Logger when processing watched file notifications. ([@vinistock][])
* [#13805](https://github.com/rubocop/rubocop/pull/13805): Make the language_server-protocol dependency version stricter. ([@koic][])

## 1.71.2 (2025-02-04)

### Bug fixes

* [#13782](https://github.com/rubocop/rubocop/pull/13782): Fix an error `Layout/ElseAlignment` when `else` is part of a numblock. ([@earlopain][])
* [#13395](https://github.com/rubocop/rubocop/issues/13395): Fix a false positive for `Lint/UselessAssignment` when assigning in branch and block. ([@pCosta99][])
* [#13783](https://github.com/rubocop/rubocop/pull/13783): Fix a false positive for `Lint/Void` when `each` numblock with conditional expressions that has multiple statements. ([@earlopain][])
* [#13787](https://github.com/rubocop/rubocop/issues/13787): Fix incorrect autocorrect for `Style/ExplicitBlockArgument` when using arguments of `zsuper` in method definition. ([@koic][])
* [#13785](https://github.com/rubocop/rubocop/pull/13785): Fix `Style/EachWithObject` cop error in case of single block argument. ([@viralpraxis][])
* [#13781](https://github.com/rubocop/rubocop/pull/13781): Fix a false positive for `Lint/UnmodifiedReduceAccumulator` when omitting the accumulator in a nested numblock. ([@earlopain][])

## 1.71.1 (2025-01-31)

### Bug fixes

* [#10081](https://github.com/rubocop/rubocop/issues/10081): Add the missing `include RuboCop::RSpec::ExpectOffense` in rubocop/rspec/support.rb. ([@d4rky-pl][])
* [#13765](https://github.com/rubocop/rubocop/pull/13765): Fix a false negative for `Lint/AmbiguousBlockAssociation` with numblocks. ([@earlopain][])
* [#13759](https://github.com/rubocop/rubocop/pull/13759): Fix a false negative for `Lint/ConstantDefinitionInBlock` with numblocks. ([@earlopain][])
* [#13741](https://github.com/rubocop/rubocop/pull/13741): Register an offense for `Naming/BlockForwarding` and `Style/ArgumentsForwarding` with Ruby >= 3.4 when the block argument is referenced inside a block. This was previously disabled because of a bug in Ruby 3.3.0. ([@earlopain][])
* [#13777](https://github.com/rubocop/rubocop/pull/13777): Fix a false negative for `Layout/EmptyLineBetweenDefs` with `DefLikeMacros` and numblocks. ([@earlopain][])
* [#13769](https://github.com/rubocop/rubocop/pull/13769): Fix a false negative for `Style/RedundantParentheses` with numblocks. ([@earlopain][])
* [#13780](https://github.com/rubocop/rubocop/pull/13780): Fix a false positive `Style/AccessModifierDeclarations` when using access modifier in a numblock. ([@earlopain][])
* [#13775](https://github.com/rubocop/rubocop/pull/13775): Fix a false positive for `Lint/AssignmentInCondition` when assigning in numblocks. ([@earlopain][])
* [#13773](https://github.com/rubocop/rubocop/pull/13773): Fix false positives for `Layout/RedundantLineBreak` when using numbered block parameter. ([@koic][])
* [#13761](https://github.com/rubocop/rubocop/pull/13761): Fix a false positive for `Style/SuperArguments` when calling super in a numblock. ([@earlopain][])
* [#13768](https://github.com/rubocop/rubocop/pull/13768): Fix a false positive for `Lint/UnreachableCode` with `instance_eval` numblock. ([@earlopain][])
* [#13750](https://github.com/rubocop/rubocop/issues/13750): Fix false positives for `Style/RedundantSelfAssignment` when assigning to attribute of `self`. ([@koic][])
* [#13739](https://github.com/rubocop/rubocop/issues/13739): Fix false positive for `Style/HashExcept` and `Style/HashSlice` when checking for inclusion with a range. ([@dvandersluis][])
* [#13751](https://github.com/rubocop/rubocop/issues/13751): Fix false positive in `Layout/ExtraSpacing` with `ForceEqualSignAlignment: true` for endless methods. ([@dvandersluis][])
* [#13767](https://github.com/rubocop/rubocop/pull/13767): Fix `Style/IdenticalConditionalBranches` autocorrect when condition is inside assignment. ([@dvandersluis][])
* [#13764](https://github.com/rubocop/rubocop/pull/13764): Fix a false negative for `Layout/SingleLineBlockChain` with numblocks. ([@earlopain][])
* [#13771](https://github.com/rubocop/rubocop/pull/13771): Fix wrong autocorrect for `Style/SoleNestedConditional` when using numblocks. ([@earlopain][])

## 1.71.0 (2025-01-22)

### New features

* [#13735](https://github.com/rubocop/rubocop/pull/13735): Add new `Lint/ArrayLiteralInRegexp` cop. ([@dvandersluis][])
* [#13507](https://github.com/rubocop/rubocop/pull/13507): Add new `Style/HashSlice` cop. ([@lovro-bikic][])

### Bug fixes

* [#13684](https://github.com/rubocop/rubocop/issues/13684): Fix a false positive for `Style/FrozenStringLiteralComment` when using the frozen string literal magic comment in Active Admin's arb files. ([@koic][])
* [#13372](https://github.com/rubocop/rubocop/issues/13372): Add `rubocop_cache` to the path given by `--cache-root` when pruning cache. ([@capncavedan][])
* [#13257](https://github.com/rubocop/rubocop/issues/13257): Fix department disable/enable comments enabling the cop for the whole file even if that file is excluded by the cop. ([@earlopain][])
* [#13704](https://github.com/rubocop/rubocop/issues/13704): Fix false positives for `Lint/OutOfRangeRegexpRef` when matching with `match` using safe navigation. ([@koic][])
* [#13720](https://github.com/rubocop/rubocop/issues/13720): Fix false positives for `Style/BlockDelimiters` when using brace blocks as conditions under `EnforcedStyle: semantic`. ([@koic][])
* [#13688](https://github.com/rubocop/rubocop/issues/13688): Fix false negative on `Style/RedundantLineContinuation` when the continuation is preceded by an interpolated string. ([@dvandersluis][])
* [#13677](https://github.com/rubocop/rubocop/issues/13677): Fix false negative on `Style/RedundantLineContinuation` when the continuation is followed by a percent array. ([@dvandersluis][])
* [#13692](https://github.com/rubocop/rubocop/pull/13692): Fix false positive in `Style/RedundantLineContinuation` when the ruby code ends with a commented continuation. ([@dvandersluis][])
* [#13675](https://github.com/rubocop/rubocop/pull/13675): Fix invalid autocorrect for `Style/ArrayFirstLast` when calling `.[]` or `&.[]` with 0 or -1. ([@dvandersluis][])
* [#13685](https://github.com/rubocop/rubocop/issues/13685): Fix syntax error introduced by `Lint/SafeNavigationChain` when adding safe navigation to an operator call inside a hash. ([@dvandersluis][])
* [#13725](https://github.com/rubocop/rubocop/issues/13725): Fix an incorrect autocorrect for `Style/IfUnlessModifier` when using omitted hash values in an assignment. ([@elliottt][])
* [#13667](https://github.com/rubocop/rubocop/issues/13667): Maintain precedence in autocorrect for `Style/SoleNestedConditional`. ([@tejasbubane][])
* [#13679](https://github.com/rubocop/rubocop/issues/13679): Fix false positive for `Style/RedundantLineContinuation` when calling methods with fully qualified constants. ([@earlopain][])
* [#13728](https://github.com/rubocop/rubocop/pull/13728): Fix a RuboCop error on provided glob pattern which matches directory. ([@viralpraxis][])
* [#13693](https://github.com/rubocop/rubocop/pull/13693): Fix `Style/ConditionalAssignment` cop error on `unless` without `else` and `assign_inside_condition` enforced style. ([@viralpraxis][])
* [#13669](https://github.com/rubocop/rubocop/pull/13669): Fix `Style/FrozenStringLiteralComment` cop error on unnormalized magic comment and `never` enforced style. ([@viralpraxis][])
* [#13696](https://github.com/rubocop/rubocop/pull/13696): Update `Metrics/CollectionLiteralLength` to only register for `[]` when called on `Set`. ([@dvandersluis][])

### Changes

* [#13709](https://github.com/rubocop/rubocop/pull/13709): Add support for safe navigation to `Lint/FloatComparison`. ([@dvandersluis][])
* [#13711](https://github.com/rubocop/rubocop/pull/13711): Add support for safe navigation to `Layout/MultilineMethodCallBraceLayout`. ([@dvandersluis][])
* [#13712](https://github.com/rubocop/rubocop/pull/13712): Add support for safe navigation to `Layout/MultilineMethodArgumentLineBreaks`. ([@dvandersluis][])
* [#13714](https://github.com/rubocop/rubocop/pull/13714): Add support for safe navigation to `Security/CompoundHash`. ([@dvandersluis][])
* [#13674](https://github.com/rubocop/rubocop/pull/13674): Add support for safe navigation to `Style/BlockDelimiters`. ([@dvandersluis][])
* [#13673](https://github.com/rubocop/rubocop/pull/13673): Add support for safe navigation to `Style/CollectionMethods`. ([@dvandersluis][])
* [#13672](https://github.com/rubocop/rubocop/pull/13672): Add support for safe navigation to `Style/MapToSet`. ([@dvandersluis][])
* [#13671](https://github.com/rubocop/rubocop/pull/13671): Add support for safe navigation to `Style/MethodCallWithoutArgsParentheses`. ([@dvandersluis][])
* [#13701](https://github.com/rubocop/rubocop/pull/13701): Add support for safe navigation to `Lint/NumericOperationWithConstantResult`. ([@dvandersluis][])
* [#13700](https://github.com/rubocop/rubocop/pull/13700): Add support for safe navigation to `Lint/RedundantStringCoercion`. ([@dvandersluis][])
* [#13698](https://github.com/rubocop/rubocop/pull/13698): Add support for safe navigation to `Lint/UselessNumericOperation`. ([@dvandersluis][])
* [#13686](https://github.com/rubocop/rubocop/pull/13686): Add wildcard support to `--show-cops`. ([@kyanagi][])
* [#13724](https://github.com/rubocop/rubocop/pull/13724): Make `Style/RedundantParentheses` aware of parenthesized assignment. ([@koic][])
* [#13732](https://github.com/rubocop/rubocop/pull/13732): Update `Style/RedundantLineContinuation` to handle required continuations following `super`. ([@dvandersluis][])

## 1.70.0 (2025-01-10)

### New features

* [#13474](https://github.com/rubocop/rubocop/pull/13474): Add new `Style/ItAssignment` cop to detect local assignments to `it` inside blocks. ([@dvandersluis][])
* [#11013](https://github.com/rubocop/rubocop/issues/11013): Add new `Lint/SharedMutableDefault` cop to alert on mutable Hash defaults. ([@corsonknowles][])
* [#13612](https://github.com/rubocop/rubocop/pull/13612): Create new cop `Lint/ConstantReassignment`. ([@lovro-bikic][])
* [#13628](https://github.com/rubocop/rubocop/pull/13628): Make LSP server support quick fix code action. ([@koic][])
* [#13607](https://github.com/rubocop/rubocop/pull/13607): Support passing the target ruby version through an environment variable. ([@elliottt][])
* [#13628](https://github.com/rubocop/rubocop/pull/13628): Add support for Ruby LSP as a built-in add-on. ([@koic][])
* [#13284](https://github.com/rubocop/rubocop/issues/13284): Add new `target_gem_version` API to change behavior of a cop at runtime depending on which gem version is present. ([@earlopain][])

### Bug fixes

* [#13589](https://github.com/rubocop/rubocop/pull/13589): Fix `Lint/NonAtomicFileOperation` to detect offenses with fully qualified constants. ([@viralpraxis][])
* [#13630](https://github.com/rubocop/rubocop/pull/13630): Fix CLI `--format` option to accept fully qualified formatter class names. ([@viralpraxis][])
* [#13624](https://github.com/rubocop/rubocop/pull/13624): Don't show warnings from `Lint/Syntax` when a syntax error occurs. ([@earlopain][])
* [#13605](https://github.com/rubocop/rubocop/pull/13605): Fix `RuboCop::Cop::Util.to_string_literal` to work correctly with frozen strings. ([@viralpraxis][])
* [#12393](https://github.com/rubocop/rubocop/issues/12393): Fix false negatives for `Lint/Void` inside of non-modifier conditionals. ([@GabeIsman][])
* [#13623](https://github.com/rubocop/rubocop/issues/13623): Fix false negatives for `Style/MultipleComparison` when setting `AllowMethodComparison: false` and comparing with simple method calls. ([@koic][])
* [#13644](https://github.com/rubocop/rubocop/pull/13644): Fix a false positive for `Layout/EmptyLinesAroundAccessModifier` when an access modifier and an expression are on the same line. ([@koic][])
* [#13645](https://github.com/rubocop/rubocop/issues/13645): Fix a false positive for `Style/MethodCallWithArgsParentheses` when setting `EnforcedStyle: omit_parentheses` and last argument is an endless range. ([@earlopain][])
* [#13614](https://github.com/rubocop/rubocop/issues/13614): Fix false positives for `Style/RaiseArgs` with anonymous splat and triple dot forwarding. ([@earlopain][])
* [#13591](https://github.com/rubocop/rubocop/pull/13591): Fix false positives for `Lint/NestedMethodDefinition` when defining a method on a constant or a method call. ([@koic][])
* [#13594](https://github.com/rubocop/rubocop/pull/13594): Fix false positives for `Style/MultipleComparison` when using multiple safe navigation method calls. ([@koic][])
* [#13654](https://github.com/rubocop/rubocop/pull/13654): Fix false positives for `Style/RedundantInitialize` when empty initialize method has arguments. ([@marocchino][])
* [#13608](https://github.com/rubocop/rubocop/pull/13608): Fix crash when running `rubocop -d` on a config with a remote `inherit_from` that causes a duplicate setting warning. ([@dvandersluis][])
* [#12430](https://github.com/rubocop/rubocop/issues/12430): Fix false negatives in `Style/RedundantLineContinuation` with multiple line continuations. ([@dvandersluis][])
* [#13638](https://github.com/rubocop/rubocop/pull/13638): Fix false positive for `Naming/BlockForwarding` when method just returns the block argument. ([@mvz][])
* [#13599](https://github.com/rubocop/rubocop/issues/13599): Fix incorrect autocorrect for `Layout/HashAlignment` when there is a multiline positional argument and `Layout/ArgumentAlignment` is configured with `EnforcedStyle: with_fixed_indentation`. ([@dvandersluis][])
* [#13586](https://github.com/rubocop/rubocop/issues/13586): Fix regression in `Layout/SpaceAroundOperators` when different comparison operators were aligned with each other. ([@dvandersluis][])
* [#13603](https://github.com/rubocop/rubocop/pull/13603): Fix `Lint/LiteralInInterpolation` cop error on invalid string literal. ([@viralpraxis][])
* [#13582](https://github.com/rubocop/rubocop/pull/13582): Fix `Lint/NonAtomicFileOperation` cop error on non-constant receiver. ([@viralpraxis][])
* [#13598](https://github.com/rubocop/rubocop/pull/13598): Fix `Lint/Void` cop error on `if` without body. ([@viralpraxis][])
* [#13634](https://github.com/rubocop/rubocop/pull/13634): Fix `Style/ClassAndModuleChildren` cop error on `compact` enforced style and unindented body. ([@viralpraxis][])
* [#13642](https://github.com/rubocop/rubocop/pull/13642): Fix `Style/FloatDivision` cop error if `#to_f` has implicit receiver. ([@viralpraxis][])
* [#13517](https://github.com/rubocop/rubocop/pull/13517): Fixes `Style/HashExcept` to recognize safe navigation when `ActiveSupportExtensionsEnabled` config is enabled. ([@lovro-bikic][])
* [#13585](https://github.com/rubocop/rubocop/pull/13585): Fix `Style/HashSyntax` cop error on implicit `call` method. ([@viralpraxis][])
* [#13632](https://github.com/rubocop/rubocop/pull/13632): Fix `Style/MissingElse` cop error if `Style/EmptyElse`'s `EnforcedStyle` is not `both` and `if` expression contains `elsif`. ([@viralpraxis][])
* [#13659](https://github.com/rubocop/rubocop/pull/13659): Fix `Style/MissingElse` cop error if `Style/EmptyElse`'s `EnforcedStyle` is not `both` and `if` expression contains multiple `elsif`. ([@viralpraxis][])
* [#13596](https://github.com/rubocop/rubocop/pull/13596): Fix `Style/RedundantCondition` cop error on parentheses and modifier `if` in `else`. ([@viralpraxis][])
* [#13616](https://github.com/rubocop/rubocop/pull/13616): Fix incorrect autocorrect for `Style/RedundantRegexpArgument` when the regex contains a single quote. ([@mrzasa][])
* [#13619](https://github.com/rubocop/rubocop/pull/13619): Fix `Style/YodaExpression` cop error in case of suffix form of operator. ([@viralpraxis][])
* [#13578](https://github.com/rubocop/rubocop/issues/13578): Update `Layout/LineContinuationSpacing` to ignore continuations inside a `regexp` or `xstr`. ([@dvandersluis][])
* [#13601](https://github.com/rubocop/rubocop/issues/13601): Update `Style/SuperArguments` to handle `super` with a block or with a chained method with a block. ([@dvandersluis][])
* [#13568](https://github.com/rubocop/rubocop/pull/13568): Fix `NoMethodError` in `ConfigValidator` when a Cop's config is not a `Hash` and raise `ValidationError` instead. ([@amomchilov][])

### Changes

* [#13665](https://github.com/rubocop/rubocop/pull/13665): Add support for safe navigation to `Style/ObjectThen`. ([@dvandersluis][])
* [#13657](https://github.com/rubocop/rubocop/pull/13657): Add support for safe navigation to `Layout/HashAlignment`. ([@dvandersluis][])
* [#13656](https://github.com/rubocop/rubocop/pull/13656): Add support for safe navigation to `Layout/HeredocArgumentClosingParenthesis`. ([@dvandersluis][])
* [#13655](https://github.com/rubocop/rubocop/pull/13655): Add support for safe navigation to `Layout/LineLength`. ([@dvandersluis][])
* [#13662](https://github.com/rubocop/rubocop/pull/13662): Add support for safe navigation to `Style/SendWithLiteralMethodName`. ([@dvandersluis][])
* [#13557](https://github.com/rubocop/rubocop/issues/13557): Fix false positives for `Lint/NumericOperationWithConstantResult`. ([@earlopain][])
* [#13658](https://github.com/rubocop/rubocop/pull/13658): Fix invalid autocorrect for `Style/SlicingWithRange` when calling `.[]` or `&.[]` with a correctable range. ([@dvandersluis][])
* [#13548](https://github.com/rubocop/rubocop/pull/13548): Enhance `Lint/DuplicateSetElement` to detect offences within `SortedSet`. ([@viralpraxis][])
* [#13646](https://github.com/rubocop/rubocop/pull/13646): Update `Layout/TrailingWhitespace` to support blank characters other than space and tab. ([@krororo][])
* [#13652](https://github.com/rubocop/rubocop/pull/13652): Update `Metrics/MethodLength` to make use of `AllowedMethods` and `AllowedPatterns` for methods defined dynamically with `define_method`. ([@dvandersluis][])
* [#13606](https://github.com/rubocop/rubocop/issues/13606): Update `Style/AccessModifierDeclarations` to add `AllowModifiersOnAliasMethod` configuration (default `true`). ([@dvandersluis][])
* [#13663](https://github.com/rubocop/rubocop/pull/13663): Update `Style/RedundantSelfAssignment` to handle safe navigation on the right-hand side of the assignment. ([@dvandersluis][])

## 1.69.2 (2024-12-12)

### Bug fixes

* [#13553](https://github.com/rubocop/rubocop/issues/13553): Fix an incorrect autocorrect for `Style/MultipleComparison` when a variable is compared multiple times after a method call. ([@koic][])
* [#13562](https://github.com/rubocop/rubocop/pull/13562): Fix `Bundler/DuplicatedGem` cop error in case of empty branch. ([@viralpraxis][])
* [#13573](https://github.com/rubocop/rubocop/pull/13573): Fix `Lint/UnescapedBracketInRegexp` cop failure with invalid multibyte escape. ([@earlopain][])
* [#13556](https://github.com/rubocop/rubocop/issues/13556): Fix false positives for `Style/FileNull` when using `'nul'` string. ([@koic][])
* [#12995](https://github.com/rubocop/rubocop/issues/12995): Fix `--disable-uncorrectable` to not insert directives inside a string. ([@dvandersluis][])
* [#13320](https://github.com/rubocop/rubocop/issues/13320): Fix incorrect autocorrect when `Layout/LineContinuationLeadingSpace` and `Style/StringLiterals` autocorrects in the same pass. ([@dvandersluis][])
* [#13299](https://github.com/rubocop/rubocop/issues/13299): Fix `Style/BlockDelimiters` to always accept braces when an operator method argument is chained. ([@dvandersluis][])
* [#13565](https://github.com/rubocop/rubocop/pull/13565): Fix `Style/RedundantLineContinuation` false negatives when a redundant continuation follows a required continuation. ([@dvandersluis][])
* [#13551](https://github.com/rubocop/rubocop/pull/13551): Fix an incorrect autocorrect for `Style/IfWithSemicolon` when using multi value assignment in `if` with a semicolon is used. ([@koic][])
* [#13534](https://github.com/rubocop/rubocop/pull/13534): Fix `Layout/LineLength` cop failure in case of YARD-comment-like string. ([@viralpraxis][])
* [#13558](https://github.com/rubocop/rubocop/pull/13558): Fix `Lint/NonAtomicFileOperation` cop error in case of implicit receiver. ([@viralpraxis][])
* [#13564](https://github.com/rubocop/rubocop/pull/13564): Fix `Metrics/ClassLength` cop error in case of chained assignments. ([@viralpraxis][])
* [#13570](https://github.com/rubocop/rubocop/pull/13570): Fix `Naming/RescuedExceptionsVariableName` cop error when exception is assigned with writer method. ([@viralpraxis][])
* [#13559](https://github.com/rubocop/rubocop/pull/13559): Fix a false positive for `Style/RedundantLineContinuation` when a method definition is used as an argument for a method call. ([@davidrunger][])
* [#13574](https://github.com/rubocop/rubocop/pull/13574): Fix `Style/ExactRegexpMatch` cop error on invalid regular expression literal. ([@viralpraxis][])
* [#13554](https://github.com/rubocop/rubocop/pull/13554): Fix `Style/FrozenStringLiteralComment` false positive in case of non-downcased value literal. ([@viralpraxis][])
* [#13569](https://github.com/rubocop/rubocop/pull/13569): Fix `Style/MethodCallWithoutArgsParentheses` cop error in case of mass hash assignment. ([@viralpraxis][])
* [#13542](https://github.com/rubocop/rubocop/pull/13542): Fix `Style/RedundantCondition` cop failure in case of empty arguments. ([@viralpraxis][])
* [#13509](https://github.com/rubocop/rubocop/issues/13509): Update `Layout/ExtraSpacing` and `Layout/SpaceAroundOperators` to handle preceding operators inside strings. ([@dvandersluis][])

## 1.69.1 (2024-12-03)

### Bug fixes

* [#13502](https://github.com/rubocop/rubocop/issues/13502): Fix an incorrect autocorrect for `Style/DigChain` when using safe navigation method chain with `dig` method. ([@koic][])
* [#13505](https://github.com/rubocop/rubocop/issues/13505): Fix an error for `Style/ParallelAssignment` when using the anonymous splat operator. ([@earlopain][])
* [#13184](https://github.com/rubocop/rubocop/pull/13184): Fix some false positives in  `Lint/UnreachableCode`. ([@isuckatcs][])
* [#13494](https://github.com/rubocop/rubocop/pull/13494): Fix false positives for `Style/HashExcept` cop when using `reject/!include?`, `reject/!in?` or `select/!exclude?` combinations. ([@lovro-bikic][])
* [#13522](https://github.com/rubocop/rubocop/pull/13522): Fix `Lint/UnescapedBracketInRegexp` cop failure with invalid regular expression. ([@viralpraxis][])
* [#13523](https://github.com/rubocop/rubocop/pull/13523): Fix `Style::AccessModifierDeclarations` cop failure in case of `if` node without `else`. ([@viralpraxis][])
* [#13524](https://github.com/rubocop/rubocop/pull/13524): Fix `Style/RedundantArgument` cop failure while inspecting string literal with invalid encoding. ([@viralpraxis][])
* [#13528](https://github.com/rubocop/rubocop/pull/13528): Fix `Style/RedundantParentheses` cop failure in case of splatted `case` node without condition. ([@viralpraxis][])
* [#13521](https://github.com/rubocop/rubocop/pull/13521): Fix `Style/RedundantSelf` cop failure with `kwnilarg` argument node. ([@viralpraxis][])
* [#13526](https://github.com/rubocop/rubocop/pull/13526): Fix `Style/StringConcatenation` cop failure when there are mixed implicit and explicit concatenations. ([@viralpraxis][])
* [#13511](https://github.com/rubocop/rubocop/issues/13511): Fix false positive in `Lint/UnescapedBracketInRegexp` when using regexp_parser 2.9.2 and earlier. ([@dvandersluis][])
* [#13096](https://github.com/rubocop/rubocop/issues/13096): Update `Style/BlockDelimiters` to not change braces when they are required for syntax. ([@dvandersluis][])
* [#13512](https://github.com/rubocop/rubocop/pull/13512): Update `Style/LambdaCall` to be aware of safe navigation. ([@dvandersluis][])

## 1.69.0 (2024-11-26)

### New features

* [#13439](https://github.com/rubocop/rubocop/pull/13439): Add new `Lint/HashNewWithKeywordArgumentsAsDefault` cop. ([@koic][])
* [#11191](https://github.com/rubocop/rubocop/issues/11191): Add new `Lint/NumericOperationWithConstantResult` cop. ([@zopolis4][])
* [#13486](https://github.com/rubocop/rubocop/issues/13486): Add new `Style/DigChain` cop. ([@dvandersluis][])
* [#13490](https://github.com/rubocop/rubocop/issues/13490): Add new `Style/FileNull` cop. ([@dvandersluis][])
* [#13484](https://github.com/rubocop/rubocop/pull/13484): Add new `Style/FileTouch` cop. ([@lovro-bikic][])
* [#13437](https://github.com/rubocop/rubocop/issues/13437): Add a new cop `Lint/UselessDefined` to detect cases such as `defined?('Foo')` when `defined?(Foo)` was intended. ([@earlopain][])

### Bug fixes

* [#13455](https://github.com/rubocop/rubocop/pull/13455): Fix a false positive for `Layout/EmptyLineAfterGuardClause` when using a guard clause outside oneliner block. ([@koic][])
* [#13412](https://github.com/rubocop/rubocop/issues/13412): Fix a false positive for `Style/RedundantLineContinuation` when there is a line continuation at the end of Ruby code followed by `__END__` data. ([@koic][])
* [#13476](https://github.com/rubocop/rubocop/pull/13476): Allow to write generics type of RBS::Inline annotation after subclass definition in `Style/CommentedKeyword`. ([@dak2][])
* [#13441](https://github.com/rubocop/rubocop/pull/13441): Fix an incorrect autocorrect for `Style/IfWithSemicolon` when using `return` with value in `if` with a semicolon is used. ([@koic][])
* [#13448](https://github.com/rubocop/rubocop/pull/13448): Fix an incorrect autocorrect for `Style/IfWithSemicolon` when the then body contains an arithmetic operator method call with an argument. ([@koic][])
* [#13199](https://github.com/rubocop/rubocop/issues/13199): Make `Style/RedundantCondition` skip autocorrection when a branch has a comment. ([@koic][])
* [#13411](https://github.com/rubocop/rubocop/pull/13411): Fix `Style/BitwisePredicate` when having regular method. ([@d4be4st][])
* [#13432](https://github.com/rubocop/rubocop/pull/13432): Fix false positive for `Lint/FloatComparison` against nil. ([@lovro-bikic][])
* [#13461](https://github.com/rubocop/rubocop/pull/13461): Fix false positives for `Lint/InterpolationCheck` when using invalid syntax in interpolation. ([@koic][])
* [#13402](https://github.com/rubocop/rubocop/issues/13402): Fix a false positive for `Lint/SafeNavigationConsistency` when using unsafe navigation with both `&&` and `||`. ([@koic][])
* [#13434](https://github.com/rubocop/rubocop/issues/13434): Fix a false positive for `Naming/MemoizedInstanceVariableName` for assignment methods`. ([@earlopain][])
* [#13415](https://github.com/rubocop/rubocop/issues/13415): Fix false positives for `Naming/MemoizedInstanceVariableName` when using `initialize_clone`, `initialize_copy`, or `initialize_dup`. ([@koic][])
* [#13421](https://github.com/rubocop/rubocop/issues/13421): Fix false positives for `Style/SafeNavigation` when using a method chain that exceeds the `MaxChainLength` value and includes safe navigation operator. ([@koic][])
* [#13433](https://github.com/rubocop/rubocop/issues/13433): Fix autocorrection for `Style/AccessModifierDeclarations` for multiple inline symbols. ([@dvandersluis][])
* [#13430](https://github.com/rubocop/rubocop/issues/13430): Fix EmptyLinesAroundMethodBody for methods with arguments spanning multiple lines. ([@aduth][])
* [#13438](https://github.com/rubocop/rubocop/pull/13438): Fix incorrect correction in `Lint/Void` if an operator is called in a void context using a dot. ([@dvandersluis][])
* [#13419](https://github.com/rubocop/rubocop/pull/13419): Fix `Lint/DeprecatedOpenSSLConstant` false positive when the argument is a safe navigation method call. ([@dvandersluis][])
* [#13404](https://github.com/rubocop/rubocop/pull/13404): Fix `Style/AccessModifierDeclarations` to register (as positive or negative, depending on `AllowModifiersOnSymbols` value) access modifiers with multiple symbols. ([@dvandersluis][])
* [#13436](https://github.com/rubocop/rubocop/pull/13436): Fix incorrect offense and autocorrect for `Lint/RedundantSplatExpansion` when percent literal array is used in a safe navigation method call. ([@lovro-bikic][])
* [#13442](https://github.com/rubocop/rubocop/pull/13442): Fix an incorrect autocorrect for `Style/NestedTernaryOperator` when ternary operators are nested and the inner condition is parenthesized. ([@koic][])
* [#13444](https://github.com/rubocop/rubocop/pull/13444): Fix an incorrect autocorrect for `Style/OneLineConditional` when the else branch of a ternary operator has multiple expressions. ([@koic][])
* [#13483](https://github.com/rubocop/rubocop/issues/13483): Fix an incorrect autocorrect for `Style/RedundantRegexpArgument` when using escaped double quote character. ([@koic][])
* [#13497](https://github.com/rubocop/rubocop/pull/13497): Fix infinite loop error for `Style/IfWithSemicolon` when using nested if/;/end in if body. ([@koic][])
* [#13477](https://github.com/rubocop/rubocop/issues/13477): Update `Layout/LeadingCommentSpace` to accept multiline shebangs at the top of the file. ([@dvandersluis][])
* [#13453](https://github.com/rubocop/rubocop/issues/13453): Update `Style/AccessModifierDeclarations` to handle `attr_*` methods with multiple parameters. ([@dvandersluis][])
* [#12597](https://github.com/rubocop/rubocop/issues/12597): Update `Style/SingleLineDoEndBlock` to not register an offense if it will introduce a conflicting `Layout/RedundantLineBreak` offense. ([@dvandersluis][])

### Changes

* [#11680](https://github.com/rubocop/rubocop/issues/11680): Add autocorrection for strings to `Layout/LineLength` when `SplitStrings` is set to `true`. ([@dvandersluis][])
* [#13470](https://github.com/rubocop/rubocop/pull/13470): Make `Style/ArrayIntersect` aware of `none?`. ([@earlopain][])
* [#13481](https://github.com/rubocop/rubocop/pull/13481): Support unicode-display_width v3. ([@gemmaro][])
* [#13473](https://github.com/rubocop/rubocop/pull/13473): Update `Lint/ItWithoutArgumentsInBlock` to not register offenses in Ruby 3.4. ([@dvandersluis][])
* [#13420](https://github.com/rubocop/rubocop/pull/13420): Update `Lint/RedundantSafeNavigation` to register an offense when the receiver is `self`. ([@dvandersluis][])
* [#11393](https://github.com/rubocop/rubocop/issues/11393): Update `Lint/UnusedMethodArgument` to allow the class names for `IgnoreNotImplementedMethods` to be configured. ([@dvandersluis][])
* [#13058](https://github.com/rubocop/rubocop/issues/13058): Update `Style/AccessModifierDeclarations` to accept modifier with splatted method call. ([@dvandersluis][])

## 1.68.0 (2024-10-31)

### New features

* [#13050](https://github.com/rubocop/rubocop/issues/13050): Add new `Style/BitwisePredicate` cop. ([@koic][])
* [#12140](https://github.com/rubocop/rubocop/issues/12140): Add new `Style/CombinableDefined` cop. ([@dvandersluis][])
* [#12988](https://github.com/rubocop/rubocop/issues/12988): Add new `Style/AmbiguousEndlessMethodDefinition` cop. ([@dvandersluis][])
* [#11514](https://github.com/rubocop/rubocop/issues/11514): Add new `Lint/UnescapedBracketInRegexp` cop. ([@dvandersluis][])
* [#13360](https://github.com/rubocop/rubocop/pull/13360): Add `AllowSteepAnnotation` config option to `Layout/LeadingCommentSpace`. ([@tk0miya][])
* [#13146](https://github.com/rubocop/rubocop/issues/13146): Add new `IgnoreDuplicateElseBranch` option to `Lint/DuplicateBranch`. ([@fatkodima][])
* [#13171](https://github.com/rubocop/rubocop/issues/13171): Add new `Style/SafeNavigationChainLength` cop. ([@fatkodima][])
* [#13252](https://github.com/rubocop/rubocop/pull/13252): Add new `Style/KeywordArgumentsMerging` cop. ([@fatkodima][])

### Bug fixes

* [#13401](https://github.com/rubocop/rubocop/pull/13401): Fix a false negative for `Style/RedundantLineContinuation` when there is a line continuation at the EOF. ([@koic][])
* [#13368](https://github.com/rubocop/rubocop/issues/13368): Fix an incorrect autocorrect for `Naming/BlockForwarding` with `Style/ExplicitBlockArgument`. ([@koic][])
* [#13391](https://github.com/rubocop/rubocop/pull/13391): Fix deserialization of unknown encoding offenses. ([@earlopain][])
* [#13348](https://github.com/rubocop/rubocop/issues/13348): Ensure `Style/BlockDelimiters` autocorrection does not move other code between the block and comment. ([@dvandersluis][])
* [#13382](https://github.com/rubocop/rubocop/pull/13382): Fix an error during error handling for custom ruby extractors when the extractor is a class. ([@earlopain][])
* [#13309](https://github.com/rubocop/rubocop/issues/13309): Fix a false negative for `Lint/UselessAssignment` cop when there is a useless assignment followed by a block. ([@pCosta99][])
* [#13255](https://github.com/rubocop/rubocop/pull/13255): Fix false negatives for `Style/MapIntoArray` when using non-splatted arguments. ([@vlad-pisanov][])
* [#13356](https://github.com/rubocop/rubocop/issues/13356): Fix a false positive for `Layout/SpaceBeforeBrackets` when there is a dot before `[]=`. ([@earlopain][])
* [#13365](https://github.com/rubocop/rubocop/issues/13365): Fix false positives for `Lint/SafeNavigationConsistency` when using safe navigation on the LHS with operator method on the RHS of `&&`. ([@koic][])
* [#13390](https://github.com/rubocop/rubocop/issues/13390): Fix false positives for `Style/GuardClause` when using a local variable assigned in a conditional expression in a branch. ([@koic][])
* [#13337](https://github.com/rubocop/rubocop/issues/13337): Fix false positives for `Style/RedundantLineContinuation` when required line continuations for `&&` is used with an assignment after a line break. ([@koic][])
* [#13387](https://github.com/rubocop/rubocop/issues/13387): Fix false positives in `Style/RedundantParentheses` when parentheses are used around method chain with `do`...`end` block in keyword argument. ([@koic][])
* [#13341](https://github.com/rubocop/rubocop/issues/13341): Fix false positives for `Lint/SafeNavigationChain` when a safe navigation operator is used with a method call as the RHS operand of `&&` for the same receiver. ([@koic][])
* [#13324](https://github.com/rubocop/rubocop/issues/13324): Fix `--disable-uncorrectable` to not insert a comment inside a string continuation. ([@dvandersluis][])
* [#13364](https://github.com/rubocop/rubocop/issues/13364): Fix incorrect autocorrect with `Lint/UselessAssignment` a multiple assignment or `for` contains an inner assignment. ([@dvandersluis][])
* [#13353](https://github.com/rubocop/rubocop/issues/13353): Fix an incorrect autocorrect for `Style/BlockDelimiters` when `EnforcedStyle: semantic` is set and used with `Layout/SpaceInsideBlockBraces`. ([@koic][])
* [#13361](https://github.com/rubocop/rubocop/issues/13361): Fix false positives for `Style/RedundantInterpolationUnfreeze` and `Style/RedundantFreeze` when strings contain interpolated global, instance, and class variables. ([@vlad-pisanov][])
* [#13343](https://github.com/rubocop/rubocop/issues/13343): Prevent `Layout/LineLength` from breaking up a method with arguments chained onto a heredoc delimiter. ([@dvandersluis][])
* [#13374](https://github.com/rubocop/rubocop/issues/13374): Return exit code 0 with `--display-only-correctable` and `--display-only-safe-correctable` when no offenses are displayed. ([@dvandersluis][])
* [#13193](https://github.com/rubocop/rubocop/issues/13193): Fix false positive in `Style/MultipleComparison` when `ComparisonsThreshold` exceeds 2. ([@fatkodima][], [@vlad-pisanov][])
* [#13325](https://github.com/rubocop/rubocop/pull/13325): Fix an incorrect autocorrect for `Lint/NonAtomicFileOperation` when using a postfix `unless` for file existence checks before creating a file, in cases with `Dir.mkdir`. ([@kotaro0522][])
* [#13397](https://github.com/rubocop/rubocop/pull/13397): Update `PercentLiteralCorrector` to be able to write pairs of delimiters without excessive escaping. ([@dvandersluis][])
* [#13336](https://github.com/rubocop/rubocop/issues/13336): Update `Style/SafeNavigation` to not autocorrect if the RHS of an `and` node is an `or` node. ([@dvandersluis][])
* [#13378](https://github.com/rubocop/rubocop/issues/13378): When removing parens in `Style/TernaryParentheses` with a `send` node condition, ensure its arguments are parenthesized. ([@dvandersluis][])

### Changes

* [#13347](https://github.com/rubocop/rubocop/pull/13347): When running `rubocop -V`, show the analysis Ruby version of the current directory. ([@earlopain][])

## 1.67.0 (2024-10-15)

### New features

* [#13259](https://github.com/rubocop/rubocop/issues/13259): Add new `Lint/DuplicateSetElement` cop. ([@koic][])
* [#13223](https://github.com/rubocop/rubocop/pull/13223): Add `AllowRBSInlineAnnotation` config option to `Layout/LeadingCommentSpace` to support RBS::Inline style annotation comments. ([@tk0miya][])
* [#13310](https://github.com/rubocop/rubocop/issues/13310): Display analysis Ruby version in `rubocop -V`. ([@koic][])

### Bug fixes

* [#13314](https://github.com/rubocop/rubocop/pull/13314): Fix a false negative for `Style/Semicolon` when using a semicolon between a closing parenthesis after a line break and a consequent expression. ([@koic][])
* [#13217](https://github.com/rubocop/rubocop/pull/13217): Fix a false positive in `Lint/ParenthesesAsGroupedExpression` with compound ranges. ([@gsamokovarov][])
* [#13268](https://github.com/rubocop/rubocop/pull/13268): Fix a false positive for `Style/BlockDelimiters` when a single line do-end block with an inline `rescue` with a semicolon before `rescue`. ([@koic][])
* [#13298](https://github.com/rubocop/rubocop/pull/13298): Fix an error for `Layout/AccessModifierIndentation` when the access modifier is on the same line as the class definition. ([@koic][])
* [#13198](https://github.com/rubocop/rubocop/pull/13198): Fix an error for `Style/OneLineConditional` when using nested if/then/else/end. ([@koic][])
* [#13316](https://github.com/rubocop/rubocop/issues/13316): Fix an incorrect autocorrect for `Lint/ImplicitStringConcatenation` with `Lint/TripleQuotes` when string literals with triple quotes are used. ([@koic][])
* [#13220](https://github.com/rubocop/rubocop/issues/13220): Fix an incorrect autocorrect for `Style/ArgumentsForwarding` when using only forwarded arguments in brackets. ([@koic][])
* [#13202](https://github.com/rubocop/rubocop/issues/13202): Fix an incorrect autocorrect for `Style/CombinableLoops` when looping over the same data with different block variable names. ([@koic][])
* [#13291](https://github.com/rubocop/rubocop/issues/13291): Fix an incorrect autocorrect for `Style/RescueModifier` when using modifier rescue for method call with heredoc argument. ([@koic][])
* [#13226](https://github.com/rubocop/rubocop/pull/13226): Fix `--auto-gen-config` when passing an absolute config path. ([@earlopain][])
* [#13225](https://github.com/rubocop/rubocop/issues/13225): Avoid syntax error when correcting `Style/OperatorMethodCall` with `/` operations followed by a parenthesized argument. ([@dvandersluis][])
* [#13235](https://github.com/rubocop/rubocop/issues/13235): Fix an error for `Style/IfUnlessModifier` when multiline `if` that fits on one line and using implicit method call with hash value omission syntax. ([@koic][])
* [#13219](https://github.com/rubocop/rubocop/pull/13219): Fix a false positive for `Style/ArgumentsForwarding` with Ruby 3.0 and optional position arguments. ([@earlopain][])
* [#13271](https://github.com/rubocop/rubocop/issues/13271): Fix a false positive for `Lint/AmbiguousRange` when using rational literals. ([@koic][])
* [#13260](https://github.com/rubocop/rubocop/issues/13260): Fix a false positive for `Lint/RedundantSafeNavigation` with namespaced constants. ([@earlopain][])
* [#13224](https://github.com/rubocop/rubocop/pull/13224): Fix false positives for `Style/OperatorMethodCall` with named forwarding. ([@earlopain][])
* [#13213](https://github.com/rubocop/rubocop/issues/13213): Fix false positives for `Style/AccessModifierDeclarations` when `AllowModifiersOnAttrs: true` and using splat with a percent symbol array, or with a constant. ([@koic][])
* [#13145](https://github.com/rubocop/rubocop/issues/13145): Fix false positives for `Style/RedundantLineContinuation` when line continuations with comparison operator and the LHS is wrapped in parentheses. ([@koic][])
* [#12875](https://github.com/rubocop/rubocop/issues/12875): Fix false positive for `Style/ArgumentsForwarding` when argument is used inside a block. ([@dvandersluis][])
* [#13239](https://github.com/rubocop/rubocop/pull/13239): Fix false positive for `Style/CollectionCompact` when using `delete_if`. ([@masato-bkn][])
* [#13210](https://github.com/rubocop/rubocop/pull/13210): Fix omit_parentheses style for pattern match with value omission in single-line branch. ([@gsamokovarov][])
* [#13149](https://github.com/rubocop/rubocop/issues/13149): Handle crashes in custom Ruby extractors more gracefully. ([@earlopain][])
* [#13319](https://github.com/rubocop/rubocop/issues/13319): Handle literal forward slashes inside a `regexp` in `Lint/LiteralInInterpolation`. ([@dvandersluis][])
* [#13208](https://github.com/rubocop/rubocop/pull/13208): Fix an incorrect autocorrect for `Style/IfWithSemicolon` when single-line `if/;/end` when the then body contains a method call with `[]` or `[]=`. ([@koic][])
* [#13318](https://github.com/rubocop/rubocop/issues/13318): Prevent modifying blocks with `Style/HashEachMethods` if the hash is modified within the block. ([@dvandersluis][])
* [#13293](https://github.com/rubocop/rubocop/pull/13293): Fix `TargetRubyVersion` from a gemspec when the gemspec is not named like the folder it is located in. ([@earlopain][])
* [#13211](https://github.com/rubocop/rubocop/pull/13211): Fix wrong autocorrect for `Style/GuardClause` when using heredoc without `else` branch. ([@earlopain][])
* [#13215](https://github.com/rubocop/rubocop/pull/13215): Fix wrong autocorrect for `Lint/BigDecimalNew` when using `::BigDecimal.new`. ([@earlopain][])
* [#13215](https://github.com/rubocop/rubocop/pull/13215): Fix wrong autocorrect for `Style/MethodCallWithArgsParentheses` with `EnforcedStyle: omit_parentheses` and whitespace. ([@earlopain][])
* [#13302](https://github.com/rubocop/rubocop/issues/13302): Fix incompatible autocorrect between `Style/RedundantBegin` and `Style/BlockDelimiters` with `EnforcedStyle: braces_for_chaining`. ([@earlopain][])

### Changes

* [#13221](https://github.com/rubocop/rubocop/pull/13221): Do not group accessors having RBS::Inline annotation comments in `Style/AccessorGrouping`. ([@tk0miya][])
* [#13286](https://github.com/rubocop/rubocop/issues/13286): Add `AllowedMethods` configuration to `Layout/FirstMethodArgumentLineBreak`. ([@dvandersluis][])
* [#13110](https://github.com/rubocop/rubocop/issues/13110): Add support in `Style/ArgumentsForwarding` for detecting forwarding of all anonymous arguments. ([@dvandersluis][])
* [#13222](https://github.com/rubocop/rubocop/pull/13222): Allow to write RBS::Inline annotation comments after method definition in `Style/CommentedKeyword`. ([@tk0miya][])
* [#13253](https://github.com/rubocop/rubocop/pull/13253): Emit a deprecation when custom cops inherit from `RuboCop::Cop::Cop`. ([@earlopain][])
* [#13300](https://github.com/rubocop/rubocop/pull/13300): Set `EnforcedShorthandSyntax: either` by default for `Style/HashSyntax`. ([@koic][])
* [#13254](https://github.com/rubocop/rubocop/pull/13254): Enhance the autocorrect for `Naming/InclusiveLanguage` when a sole suggestion is set. ([@koic][])
* [#13232](https://github.com/rubocop/rubocop/issues/13232): Make server mode aware of auto-restart for local config update. ([@koic][])
* [#13270](https://github.com/rubocop/rubocop/pull/13270): Make `Style/SelectByRegexp` aware of `filter` in Ruby version 2.6 or above. ([@masato-bkn][])
* [#9816](https://github.com/rubocop/rubocop/issues/9816): Refine `Lint/SafeNavigationConsistency` cop to check that the safe navigation operator is applied consistently and without excess or deficiency. ([@koic][])
* [#13256](https://github.com/rubocop/rubocop/issues/13256): Report and correct more `Style/SafeNavigation` offenses. ([@dvandersluis][])
* [#13245](https://github.com/rubocop/rubocop/pull/13245): Support `filter/filter!` in `Style/CollectionCompact`. ([@masato-bkn][])
* [#13281](https://github.com/rubocop/rubocop/pull/13281): Support Ruby 3.4 for `Lint/UriRegexp` to avoid obsolete API. ([@koic][])
* [#13229](https://github.com/rubocop/rubocop/issues/13229): Update `Style/MapIntoArray` to be able to handle arrays created using `[].tap`. ([@dvandersluis][])
* [#13305](https://github.com/rubocop/rubocop/pull/13305): Update `Style/ReturnNilInPredicateMethodDefinition` to detect implicit `nil` returns inside `if`. ([@dvandersluis][])
* [#13327](https://github.com/rubocop/rubocop/pull/13327): Make server mode aware of auto-restart for .rubocop_todo.yml update. ([@koic][])

## 1.66.1 (2024-09-04)

### Bug fixes

* [#13191](https://github.com/rubocop/rubocop/pull/13191): Fix an error for `Style/IfWithSemicolon` when using nested single-line if/;/end in block of if/else branches. ([@koic][])
* [#13178](https://github.com/rubocop/rubocop/pull/13178): Fix false positive for `Style/EmptyLiteral` with `Hash.new([])`. ([@earlopain][])
* [#13176](https://github.com/rubocop/rubocop/issues/13176): Fix crash in `Style/EmptyElse` when `AllowComments: true` and the else clause is missing. ([@vlad-pisanov][])
* [#13185](https://github.com/rubocop/rubocop/pull/13185): Fix false negatives in `Style/MapIntoArray` autocorrection when using `ensure`, `def`, `defs` and `for`. ([@vlad-pisanov][])

## 1.66.0 (2024-08-31)

### New features

* [#13077](https://github.com/rubocop/rubocop/pull/13077): Add new global `StringLiteralsFrozenByDefault` option for correct analysis with `RUBYOPT=--enable=frozen-string-literal`. ([@earlopain][])
* [#13080](https://github.com/rubocop/rubocop/pull/13080): Add new `DocumentationExtension` global option to serve documentation with extensions different than `.html`. ([@earlopain][])
* [#13074](https://github.com/rubocop/rubocop/issues/13074): Add new `Lint/UselessNumericOperation` cop to check for inconsequential numeric operations. ([@zopolis4][])
* [#13061](https://github.com/rubocop/rubocop/issues/13061): Add new `Style/RedundantInterpolationUnfreeze` cop to check for `dup` and `@+` on interpolated strings in Ruby >= 3.0. ([@earlopain][])

### Bug fixes

* [#13093](https://github.com/rubocop/rubocop/issues/13093): Fix an error for `Lint/ImplicitStringConcatenation` when implicitly concatenating a string literal with a line break and string interpolation. ([@koic][])
* [#13098](https://github.com/rubocop/rubocop/issues/13098): Fix an error for `Style/IdenticalConditionalBranches` when handling empty case branches. ([@koic][])
* [#13113](https://github.com/rubocop/rubocop/pull/13113): Fix an error for `Style/IfWithSemicolon` when a nested `if` with a semicolon is used. ([@koic][])
* [#13097](https://github.com/rubocop/rubocop/issues/13097): Fix an error for `Style/InPatternThen` when using alternative pattern matching deeply. ([@koic][])
* [#13159](https://github.com/rubocop/rubocop/pull/13159): Fix an error for `Style/OneLineConditional` when using if/then/else/end with multiple expressions in the `then` body. ([@koic][])
* [#13092](https://github.com/rubocop/rubocop/pull/13092): Fix an incorrect autocorrect for `Layout/EmptyLineBetweenDefs` when two method definitions are on the same line separated by a semicolon. ([@koic][])
* [#13116](https://github.com/rubocop/rubocop/pull/13116): Fix an incorrect autocorrect for `Style/IfWithSemicolon` when a single-line `if/;/end` has an argument in the then body expression. ([@koic][])
* [#13161](https://github.com/rubocop/rubocop/pull/13161): Fix incorrect autocorrect for `Style/IfWithSemicolon` when using multiple expressions in the `else` body. ([@koic][])
* [#13132](https://github.com/rubocop/rubocop/pull/13132): Fix incorrect autocorrect for `Style/TrailingBodyOnMethodDefinition` when an expression precedes a method definition on the same line with a semicolon. ([@koic][])
* [#13164](https://github.com/rubocop/rubocop/pull/13164): Fix incorrect autocorrect behavior for `Layout/BlockAlignment` when `EnforcedStyleAlignWith: either (default)`. ([@koic][])
* [#13087](https://github.com/rubocop/rubocop/pull/13087): Fix an incorrect autocorrect for `Style/MultipleComparison` when expression with more comparisons precedes an expression with less comparisons. ([@fatkodima][])
* [#13172](https://github.com/rubocop/rubocop/pull/13172): Fix an error for `Layout/EmptyLinesAroundExceptionHandlingKeywords` when `ensure` or `else` and `end` are on the same line. ([@koic][])
* [#13107](https://github.com/rubocop/rubocop/issues/13107): Fix an error for `Lint/ImplicitStringConcatenation` when there are multiple adjacent string interpolation literals on the same line. ([@koic][])
* [#13111](https://github.com/rubocop/rubocop/pull/13111): Fix an error for `Style/GuardClause` when if clause is empty and correction would not fit on single line because of `Layout/LineLength`. ([@earlopain][])
* [#13137](https://github.com/rubocop/rubocop/pull/13137): Fix an error for `Style/ParallelAssignment` when using `__FILE__`. ([@earlopain][])
* [#13143](https://github.com/rubocop/rubocop/pull/13143): Fix an error during `TargetRubyVersion` detection if the gemspec is not valid syntax. ([@earlopain][])
* [#13131](https://github.com/rubocop/rubocop/pull/13131): Fix false negatives for `Lint/Void` when using `ensure`, `defs` and `numblock`. ([@vlad-pisanov][])
* [#13174](https://github.com/rubocop/rubocop/pull/13174): Fix false negatives for `Style/MapIntoArray` when initializing the destination using `Array[]`, `Array([])`, or `Array.new([])`. ([@vlad-pisanov][])
* [#13173](https://github.com/rubocop/rubocop/pull/13173): Fix false negatives for `Style/EmptyLiteral` when using `Array[]`, `Hash[]`, `Array.new([])` and `Hash.new([])`. ([@vlad-pisanov][])
* [#13126](https://github.com/rubocop/rubocop/issues/13126): Fix a false positive for `Style/Alias` when using multiple `alias` in `def`. ([@koic][])
* [#13085](https://github.com/rubocop/rubocop/issues/13085): Fix a false positive for `Style/EmptyElse` when a comment-only `else` is used after `elsif` and `AllowComments: true` is set. ([@koic][])
* [#13118](https://github.com/rubocop/rubocop/issues/13118): Fix a false positive for `Style/MapIntoArray` when splatting. ([@earlopain][])
* [#13105](https://github.com/rubocop/rubocop/issues/13105): Fix false positives for `Style/ArgumentsForwarding` when forwarding kwargs/block arg with non-matching additional args. ([@koic][])
* [#13139](https://github.com/rubocop/rubocop/issues/13139): Fix false positives for `Style/RedundantCondition` when using modifier `if` or `unless`. ([@koic][])
* [#13134](https://github.com/rubocop/rubocop/pull/13134): Fix false negative for `Lint/Void` when using using frozen literals. ([@vlad-pisanov][])
* [#13148](https://github.com/rubocop/rubocop/pull/13148): Fix incorrect autocorrect for `Lint/EmptyConditionalBody` when missing `elsif` body with `end` on the same line. ([@koic][])
* [#13109](https://github.com/rubocop/rubocop/pull/13109): Fix an error for the `Lockfile` parser when it contains incompatible `BUNDLED WITH` versions. ([@earlopain][])
* [#13112](https://github.com/rubocop/rubocop/pull/13112): Fix detection of `TargetRubyVersion` through the gemfile if the gemfile ruby version is below 2.7. ([@earlopain][])
* [#13155](https://github.com/rubocop/rubocop/pull/13155): Fixes an error when the server cache directory has too long path, causing rubocop to fail even with caching disabled. ([@protocol7][])

### Changes

* [#13150](https://github.com/rubocop/rubocop/issues/13150): Allow `get_!`, `set_!`, `get_?`, `set_?`, `get_=`, and `set_=` in `Naming/AccessorMethodName`. ([@koic][])
* [#13103](https://github.com/rubocop/rubocop/issues/13103): Make `Lint/UselessAssignment` autocorrection safe. ([@koic][])
* [#13099](https://github.com/rubocop/rubocop/issues/13099): Make `Style/RedundantRegexpArgument` respect the `EnforcedStyle` of `Style/StringLiterals`. ([@koic][])
* [#13165](https://github.com/rubocop/rubocop/pull/13165): Remove dependency on the `rexml` gem. ([@bquorning][])
* [#13090](https://github.com/rubocop/rubocop/pull/13090): Require RuboCop AST 1.32.0+ to use `RuboCop::AST::RationalNode`. ([@koic][])

## 1.65.1 (2024-08-01)

### New features

* [#13068](https://github.com/rubocop/rubocop/pull/13068): Add config validation to `Naming/PredicateName` to check that all `ForbiddenPrefixes` are being checked. ([@maxjacobson][])

### Bug fixes

* [#13051](https://github.com/rubocop/rubocop/issues/13051): Fix an error for `Lint/FloatComparison` when comparing with rational literal. ([@koic][])
* [#13065](https://github.com/rubocop/rubocop/issues/13065): Fix an error for `Lint/UselessAssignment` when same name variables are assigned using chained assignment. ([@koic][])
* [#13062](https://github.com/rubocop/rubocop/pull/13062): Fix an error for `Style/InvertibleUnlessCondition` when using empty parenthesis as condition. ([@earlopain][])
* [#11438](https://github.com/rubocop/rubocop/issues/11438): Explicitly load `fileutils` before calculating `before_us`. ([@r7kamura][])
* [#13044](https://github.com/rubocop/rubocop/issues/13044): Fix false negatives for `Lint/ImplicitStringConcatenation` when using adjacent string interpolation literals on the same line. ([@koic][])
* [#13083](https://github.com/rubocop/rubocop/pull/13083): Fix a false positive for `Style/GlobalStdStream` when using namespaced constants like `Foo::STDOUT`. ([@earlopain][])
* [#13081](https://github.com/rubocop/rubocop/pull/13081): Fix a false positive for `Style/ZeroLengthPredicate` when using safe navigation and non-zero comparison. ([@fatkodima][])
* [#13041](https://github.com/rubocop/rubocop/issues/13041): Fix false positives for `Lint/UselessAssignment` when pattern match variable is assigned and used in a block. ([@koic][])
* [#13076](https://github.com/rubocop/rubocop/issues/13076): Fix an incorrect autocorrect for `Naming/RescuedExceptionsVariableName` when using hash value omission. ([@koic][])

## 1.65.0 (2024-07-10)

### New features

* [#13030](https://github.com/rubocop/rubocop/pull/13030): Add new `Gemspec/AddRuntimeDependency` cop. ([@koic][])

### Bug fixes

* [#12954](https://github.com/rubocop/rubocop/issues/12954): Fix a false negative for `Style/ArgumentsForwarding` when arguments forwarding in `yield`. ([@koic][])
* [#13033](https://github.com/rubocop/rubocop/issues/13033): Fix a false positive for `Layout/SpaceAroundOperators` when using multiple spaces between an operator and a tailing comment. ([@koic][])
* [#12885](https://github.com/rubocop/rubocop/issues/12885): Fix a false positive for `Lint/ToEnumArguments` when enumerator is created for another method. ([@koic][])
* [#13018](https://github.com/rubocop/rubocop/issues/13018): Fix a false positive for `Style/MethodCallWithArgsParentheses` when `EnforcedStyle: omit_parentheses` is set and parenthesized method call is used before constant resolution. ([@koic][])
* [#12986](https://github.com/rubocop/rubocop/issues/12986): Fix a false positive for `Style/RedundantBegin` when endless method definition with `rescue`. ([@koic][])
* [#12985](https://github.com/rubocop/rubocop/issues/12985): Fix an error for `Style/RedundantRegexpCharacterClass` when using regexp_parser gem 2.3.1 or older. ([@koic][])
* [#13010](https://github.com/rubocop/rubocop/issues/13010): Fix an error for `Style/SuperArguments` when the hash argument is or-assigned. ([@koic][])
* [#13023](https://github.com/rubocop/rubocop/issues/13023): Fix an error for `Style/SymbolProc` when using lambda `->` with one argument and multiline `do`...`end` block. ([@koic][])
* [#12989](https://github.com/rubocop/rubocop/issues/12989): Fix an error for the `inherit_gem` config when the Gemfile contains an uninstalled git gem. ([@earlopain][])
* [#12975](https://github.com/rubocop/rubocop/issues/12975): Fix an error for the `inherit_gem` config when running RuboCop without bundler and no Gemfile exists. ([@earlopain][])
* [#12997](https://github.com/rubocop/rubocop/pull/12997): Fix an error for `Lint/UnmodifiedReduceAccumulator` when the block is empty. ([@earlopain][])
* [#12979](https://github.com/rubocop/rubocop/issues/12979): Fix false negatives for `Lint/Void` when void expression with guard clause is not on last line. ([@koic][])
* [#12716](https://github.com/rubocop/rubocop/issues/12716): Fix false negatives for `Lint/Void` when using parenthesized void operators. ([@koic][])
* [#12471](https://github.com/rubocop/rubocop/issues/12471): Fix false negatives for `Style/ZeroLengthPredicate` when using safe navigation operator. ([@koic][])
* [#12960](https://github.com/rubocop/rubocop/issues/12960): Fix false positives for `Lint/NestedMethodDefinition` when definition of method on variable. ([@koic][])
* [#13012](https://github.com/rubocop/rubocop/issues/13012): Fix false positives for `Style/HashExcept` when using `reject` and calling `include?` method with bang. ([@koic][])
* [#12983](https://github.com/rubocop/rubocop/issues/12983): Fix false positives for `Style/SendWithLiteralMethodName` using `send` with writer method name. ([@koic][])
* [#12957](https://github.com/rubocop/rubocop/issues/12957): Fix false positives for `Style/SuperArguments` when calling super in a block. ([@koic][])

### Changes

* [#12970](https://github.com/rubocop/rubocop/issues/12970): Add `CountModifierForms` option to `Metrics/BlockNesting` and set it to `false` by default. ([@koic][])
* [#13032](https://github.com/rubocop/rubocop/pull/13032): Display warning messages for deprecated APIs. ([@koic][])
* [#13031](https://github.com/rubocop/rubocop/pull/13031): Enable YJIT by default in server mode. ([@koic][])
* [#12557](https://github.com/rubocop/rubocop/issues/12557): Make server mode aware of auto-restart for `bundle update`. ([@koic][])
* [#12616](https://github.com/rubocop/rubocop/issues/12616): Make `Style/MapCompactWithConditionalBlock` aware of `filter_map`. ([@koic][])
* [#13035](https://github.com/rubocop/rubocop/issues/13035): Support autocorrect for `Lint/ImplicitStringConcatenation`. ([@koic][])

## 1.64.1 (2024-05-31)

### Bug fixes

* [#12951](https://github.com/rubocop/rubocop/pull/12951): Fix an error for `Style/Copyright` when `AutocorrectNotice` is missing. ([@koic][])
* [#12932](https://github.com/rubocop/rubocop/pull/12932): Fix end position of diagnostic for LSP. ([@ksss][])
* [#12926](https://github.com/rubocop/rubocop/issues/12926): Fix a false positive for `Style/SuperArguments` when the methods block argument is reassigned before `super`. ([@earlopain][])
* [#12931](https://github.com/rubocop/rubocop/issues/12931): Fix false positives for `Style/RedundantLineContinuation` when line continuations involve `break`, `next`, or `yield` with a return value. ([@koic][])
* [#12924](https://github.com/rubocop/rubocop/issues/12924): Fix false positives for `Style/SendWithLiteralMethodName` when `public_send` argument is a method name that cannot be autocorrected. ([@koic][])

## 1.64.0 (2024-05-23)

### New features

* [#12904](https://github.com/rubocop/rubocop/pull/12904): Add new `either_consistent` `SupportedShorthandSyntax` to `Style/HashSyntax`. ([@pawelma][])
* [#12842](https://github.com/rubocop/rubocop/issues/12842): Add new `Style/SendWithLiteralMethodName` cop. ([@koic][])
* [#12309](https://github.com/rubocop/rubocop/issues/12309): Add new `Style/SuperArguments` cop. ([@earlopain][])
* [#12917](https://github.com/rubocop/rubocop/pull/12917): Suggest correct formatter name for `--format` command line option. ([@koic][])
* [#12242](https://github.com/rubocop/rubocop/issues/12242): Support `AllowModifiersOnAttrs` option for `Style/AccessModifierDeclarations`. ([@krororo][])
* [#11585](https://github.com/rubocop/rubocop/issues/11585): Support `AllowedMethods` for `Style/DocumentationMethod`. ([@koic][])

### Bug fixes

* [#7189](https://github.com/rubocop/rubocop/issues/7189): Fix a false positive for `Style/Copyright` when using multiline copyright notice. ([@koic][])
* [#12914](https://github.com/rubocop/rubocop/pull/12914): Fix a false negative for `Layout/EmptyComment` when using an empty comment next to code after comment line. ([@koic][])
* [#12919](https://github.com/rubocop/rubocop/issues/12919): Fix false negatives for `Style/ArgumentsForwarding` when forward target is `super`. ([@koic][])
* [#12923](https://github.com/rubocop/rubocop/pull/12923): Fix false negatives for `Style/ArgumentsForwarding` when forward target is safe navigation method. ([@koic][])
* [#12894](https://github.com/rubocop/rubocop/issues/12894): Fix false positives for `Style/MapIntoArray` when using `each` without receiver with `<<` to build an array. ([@koic][])
* [#12876](https://github.com/rubocop/rubocop/issues/12876): Fix an error for the lockfile parser if a gemfile exists but a lockfile doesn't. ([@earlopain][])
* [#12888](https://github.com/rubocop/rubocop/issues/12888): Fix `--no-exclude-limit` generating a todo with `Max` config instead of listing everything out with `Exclude`. ([@earlopain][])
* [#12898](https://github.com/rubocop/rubocop/issues/12898): Fix an error for `TargetRailsVersion` when parsing from the lockfile with prerelease rails. ([@earlopain][])

### Changes

* [#12908](https://github.com/rubocop/rubocop/pull/12908): Add rubocop-rspec back to suggested extensions when rspec-rails is in use. ([@pirj][])
* [#12884](https://github.com/rubocop/rubocop/issues/12884): Align output from `cop.documentation_url` with `--show-docs-url` when passing a config as argument. ([@earlopain][])
* [#12905](https://github.com/rubocop/rubocop/pull/12905): Support `ActiveSupportExtensionsEnabled` for `Style/SymbolProc`. ([@koic][])
* [#12897](https://github.com/rubocop/rubocop/pull/12897): Respect user's intentions with `workspace/executeCommand` LSP method. ([@koic][])

## 1.63.5 (2024-05-09)

### Bug fixes

* [#12877](https://github.com/rubocop/rubocop/pull/12877): Fix an infinite loop error for `Layout/FirstArgumentIndentation` when specifying `EnforcedStyle: with_fixed_indentation` of `Layout/ArrayAlignment`. ([@koic][])
* [#12873](https://github.com/rubocop/rubocop/issues/12873): Fix an error for `Metrics/BlockLength` when the `CountAsOne` config is invalid. ([@koic][])
* [#12881](https://github.com/rubocop/rubocop/pull/12881): Fix incorrect autocorrect when `Style/NumericPredicate` is used with negations. ([@fatkodima][])
* [#12882](https://github.com/rubocop/rubocop/pull/12882): Fix `Layout/CommentIndentation` for comment-only pattern matching. ([@nekketsuuu][])

## 1.63.4 (2024-04-28)

### Bug fixes

* [#12871](https://github.com/rubocop/rubocop/pull/12871): Fix an error for `rubocop -V` when `.rubocop.yml` contains ERB. ([@earlopain][])
* [#12862](https://github.com/rubocop/rubocop/issues/12862): Fix a false positive for `Style/RedundantLineContinuation` when line continuations involve `return` with a return value. ([@koic][])
* [#12664](https://github.com/rubocop/rubocop/pull/12664): Fix handling of `textDocument/diagnostic`. ([@muxcmux][])
* [#12865](https://github.com/rubocop/rubocop/issues/12865): Fix Rails Cops, which weren't reporting any violations unless running with `bundle exec`. ([@amomchilov][])

## 1.63.3 (2024-04-22)

### Bug fixes

* [#12857](https://github.com/rubocop/rubocop/pull/12857): Fix false negatives for `Lint/UnreachableCode` when using pattern matching. ([@koic][])
* [#12852](https://github.com/rubocop/rubocop/issues/12852): Fix an error for `Lint/EmptyFile` in formatters when using cache. ([@earlopain][])
* [#12848](https://github.com/rubocop/rubocop/issues/12848): Fix an error that occurs in `RuboCop::Lockfile` when the constant Bundler is uninitialized. ([@koic][])

### Changes

* [#12855](https://github.com/rubocop/rubocop/pull/12855): Set custom program name for the built-in LSP server. ([@koic][])

## 1.63.2 (2024-04-16)

### Bug fixes

* [#12843](https://github.com/rubocop/rubocop/issues/12843): Fix an error for `Lint/MixedCaseRange` when a character between `Z` and `a` is used in the regexp range. ([@koic][])
* [#12846](https://github.com/rubocop/rubocop/issues/12846): Fix an error for `RuboCop::Lockfile` when there is no Bundler environment. ([@koic][])
* [#12832](https://github.com/rubocop/rubocop/issues/12832): Fix an error for `Style/ArgumentsForwarding` when using block arg in nested method definitions. ([@koic][])
* [#12841](https://github.com/rubocop/rubocop/pull/12841): Fix false negatives for `Lint/UnreachableLoop` when using pattern matching. ([@koic][])
* [#12835](https://github.com/rubocop/rubocop/issues/12835): Allow global offenses to be disabled by directive comments. ([@earlopain][])

### Changes

* [#12845](https://github.com/rubocop/rubocop/pull/12845): Exclude `debug/open_nonstop` from `Lint/Debugger` by default. ([@koic][])

## 1.63.1 (2024-04-10)

### Bug fixes

* [#12828](https://github.com/rubocop/rubocop/pull/12828): Fix a false positive for `Lint/AssignmentInCondition` if assigning inside a method call. ([@earlopain][])
* [#12823](https://github.com/rubocop/rubocop/issues/12823): Fixed "uninitialized constant `RuboCop::Lockfile::Bundler`", caused when running RuboCop without `bundler exec` on codebases that use `rubocop-rails`. ([@amomchilov][])

## 1.63.0 (2024-04-08)

### New features

* [#11878](https://github.com/rubocop/rubocop/issues/11878): Add new `Style/MapIntoArray` cop. ([@ymap][])
* [#12186](https://github.com/rubocop/rubocop/pull/12186): Add new `requires_gem` API for declaring which gems a Cop needs. ([@amomchilov][])

### Bug fixes

* [#12769](https://github.com/rubocop/rubocop/issues/12769): Fix a false positive for `Lint/RedundantWithIndex` when calling `with_index` with receiver and a block. ([@koic][])
* [#12547](https://github.com/rubocop/rubocop/issues/12547): Added a comment recommending upgrading to the latest version of Rubocop in the error text when an Infinite loop detected error occurs. ([@Hiroto-Iizuka][])
* [#12782](https://github.com/rubocop/rubocop/pull/12782): Fix an error for `Style/Alias` with `EnforcedStyle: prefer_alias` when calling `alias_method` with fewer than 2 arguments. ([@earlopain][])
* [#12781](https://github.com/rubocop/rubocop/pull/12781): Fix an error for `Style/ExactRegexpMatch` when calling `match` without a receiver. ([@earlopain][])
* [#12780](https://github.com/rubocop/rubocop/issues/12780): Fix an error for `Style/RedundantEach` when using `reverse_each.each` without a block. ([@earlopain][])
* [#12731](https://github.com/rubocop/rubocop/pull/12731): Treat `&.` the same way as `.` for setter methods in `Lint/AssignmentInCondition`. ([@jonas054][])
* [#12793](https://github.com/rubocop/rubocop/issues/12793): Fix false positives for `Style/RedundantLineContinuation` when using line continuation with modifier. ([@koic][])
* [#12807](https://github.com/rubocop/rubocop/issues/12807): Fix false positives for `Naming/BlockForwarding` when using explicit block forwarding in block method and others. ([@koic][])
* [#12796](https://github.com/rubocop/rubocop/pull/12796): Fix false positives for `Style/EvalWithLocation` when using `eval` with a line number from a method call or a variable. ([@koic][])
* [#12794](https://github.com/rubocop/rubocop/issues/12794): Fix false positives for `Style/RedundantArgument` when when single-quoted strings for cntrl character. ([@koic][])
* [#12797](https://github.com/rubocop/rubocop/issues/12797): Fix false positives for `Style/RedundantLineContinuation` when using line continuations with `&&` or `||` operator in assignment. ([@koic][])
* [#12793](https://github.com/rubocop/rubocop/issues/12793): Fix false positives for `Style/RedundantLineContinuation` when multi-line continuations with operators. ([@koic][])
* [#12801](https://github.com/rubocop/rubocop/issues/12801): Fix incorrect autocorrect for `Style/CollectionCompact` when using `delete_if`. ([@koic][])
* [#12789](https://github.com/rubocop/rubocop/pull/12789): Make `Style/RedundantPercentQ` safe on multiline strings. ([@boardfish][])
* [#12802](https://github.com/rubocop/rubocop/pull/12802): Return global offenses for `Naming/FileName` and `Naming/InclusiveLanguage` for empty files. ([@earlopain][])
* [#12804](https://github.com/rubocop/rubocop/pull/12804): Return global offenses for `Style/Copyright` when the file is empty. ([@earlopain][])

### Changes

* [#12813](https://github.com/rubocop/rubocop/pull/12813): Add rubocop-rspec_rails to suggested extensions and extension doc. ([@ydah][])
* [#12820](https://github.com/rubocop/rubocop/pull/12820): Add support more Capybara debugger entry points for `Lint/Debugger`. ([@ydah][])
* [#12676](https://github.com/rubocop/rubocop/issues/12676): Adjust offending range in LSP. ([@koic][])
* [#12815](https://github.com/rubocop/rubocop/issues/12815): Ignore `Rakefile.rb` in `Naming/FileName` in the default config. ([@artur-intech][])
* [#12800](https://github.com/rubocop/rubocop/pull/12800): Handle empty obsoletion config. ([@sambostock][])
* [#12721](https://github.com/rubocop/rubocop/issues/12721): Make `Lint/Debugger` aware of `ruby/debug` requires. ([@earlopain][])
* [#12817](https://github.com/rubocop/rubocop/pull/12817): Make `rubocop -V` display rubocop-rspec_rails version when using it. ([@ydah][])
* [#12180](https://github.com/rubocop/rubocop/pull/12180): Replace regex with `Bundler::LockfileParser`. ([@amomchilov][])

## 1.62.1 (2024-03-11)

### Bug fixes

* [#12761](https://github.com/rubocop/rubocop/issues/12761): Fix a false positive for `Style/HashEachMethods` when the key block argument of `Enumerable#each` method is unused after `chunk`. ([@koic][])
* [#12768](https://github.com/rubocop/rubocop/pull/12768): Fix a false positive for `Style/NilComparison` without receiver and `EnforcedStyle: comparison`. ([@earlopain][])
* [#12752](https://github.com/rubocop/rubocop/pull/12752): Fix an error for `Gemspec/RequiredRubyVersion` when the file is empty. ([@earlopain][])
* [#12770](https://github.com/rubocop/rubocop/pull/12770): Fix an error for `Lint/RedundantWithIndex` when the method has no receiver. ([@earlopain][])
* [#12775](https://github.com/rubocop/rubocop/pull/12775): Fix an error for `Lint/UselessTimes` when no block is present. ([@earlopain][])
* [#12772](https://github.com/rubocop/rubocop/pull/12772): Fix an error for `Style/ClassVars` when calling `class_variable_set` without arguments. ([@earlopain][])
* [#12773](https://github.com/rubocop/rubocop/pull/12773): Fix an error for `Style/For` with `EnforcedStyle: for` when no receiver. ([@earlopain][])
* [#12765](https://github.com/rubocop/rubocop/pull/12765): Fix an error for `Layout/MultilineMethodCallIndentation` with safe navigation and assignment method. ([@earlopain][])
* [#12703](https://github.com/rubocop/rubocop/issues/12703): Fix an error for `Lint/MixedCaseRange` with invalid byte sequence in UTF-8. ([@earlopain][])
* [#12755](https://github.com/rubocop/rubocop/pull/12755): Fix an exception for `RedundantCurrentDirectoryInPath` in case of `require_relative` without arguments. ([@viralpraxis][])
* [#12710](https://github.com/rubocop/rubocop/issues/12710): Fix a false negative for `Layout/EmptyLineAfterMagicComment` when the file is comments only. ([@earlopain][])
* [#12758](https://github.com/rubocop/rubocop/issues/12758): Fix false positives for `Layout/RedundantLineBreak` when using `&&` or `||` after a backslash newline. ([@koic][])
* [#12763](https://github.com/rubocop/rubocop/pull/12763): Fix an infinite loop for `Style/MultilineMethodSignature` when there is a newline directly after the def keyword. ([@earlopain][])
* [#12774](https://github.com/rubocop/rubocop/pull/12774): Fix an infinite loop for `Style/RaiseArgs` with `EnforcedStyle: compact` when passing more than 2 arguments to `raise`. ([@earlopain][])
* [#12663](https://github.com/rubocop/rubocop/issues/12663): Fix `Lint/Syntax` getting disabled by `rubocop:disable Lint/Syntax`. ([@earlopain][])
* [#12756](https://github.com/rubocop/rubocop/pull/12756): Only parse target Ruby from gemspec if array elements are strings. ([@davidrunger][])

### Changes

* [#12730](https://github.com/rubocop/rubocop/pull/12730): Skip `LineLength` phase on `--auto-gen-only-exclude`. ([@sambostock][])

## 1.62.0 (2024-03-06)

### New features

* [#12600](https://github.com/rubocop/rubocop/issues/12600): Support Prism as a Ruby parser (experimental). ([@koic][])
* [#12725](https://github.com/rubocop/rubocop/pull/12725): Support `TargetRubyVersion 3.4` (experimental). ([@koic][])

### Bug fixes

* [#12746](https://github.com/rubocop/rubocop/pull/12746): Fix a false positive for `Lint/ToEnumArguments` when enumerator is created for another method in no arguments method definition. ([@koic][])
* [#12726](https://github.com/rubocop/rubocop/issues/12726): Fix a false positive for `Style/RedundantLineContinuation` when using line concatenation and calling a method with keyword arguments without parentheses. ([@koic][])
* [#12738](https://github.com/rubocop/rubocop/issues/12738): Fix an error for `Style/Encoding` when magic encoding with mixed case present. ([@koic][])
* [#12732](https://github.com/rubocop/rubocop/pull/12732): Fix error determining target Ruby when gemspec `required_ruby_version` is read from another file. ([@davidrunger][])
* [#12736](https://github.com/rubocop/rubocop/issues/12736): Fix invalid autocorrect in `Layout/SpaceInsideHashLiteralBraces`. ([@bquorning][])
* [#12667](https://github.com/rubocop/rubocop/issues/12667): Don't load excluded configuration. ([@jonas054][])

## 1.61.0 (2024-02-29)

### New features

* [#12682](https://github.com/rubocop/rubocop/issues/12682): Add `--editor-mode` CLI option. ([@koic][])
* [#12657](https://github.com/rubocop/rubocop/pull/12657): Support `AutoCorrect: contextual` option for LSP. ([@koic][])
* [#12273](https://github.com/rubocop/rubocop/issues/12273): Make `OffenseCountFormatter` display autocorrection information. ([@koic][])
* [#12679](https://github.com/rubocop/rubocop/pull/12679): Publish `RuboCop::LSP.enable` API to enable LSP mode. ([@koic][])
* [#12699](https://github.com/rubocop/rubocop/issues/12699): Support searching for `.rubocop.yml` and `rubocop/config.yml` in compliance with dot-config. ([@koic][])

### Bug fixes

* [#12720](https://github.com/rubocop/rubocop/issues/12720): Fix a false positive for `Style/ArgumentsForwarding` when using block arg forwarding to within block with Ruby 3.3.0. ([@koic][])
* [#12714](https://github.com/rubocop/rubocop/issues/12714): Fix an error for `Gemspec/RequiredRubyVersion` when `required_ruby_version` is specified with `Gem::Requirement.new` and is higher than `TargetRubyVersion`. ([@koic][])
* [#12690](https://github.com/rubocop/rubocop/issues/12690): Fix an error for `Style/CaseLikeIf` when using `==` with literal and using ternary operator. ([@koic][])
* [#12668](https://github.com/rubocop/rubocop/issues/12668): Fix an incorrect autocorrect for `Lint/EmptyConditionalBody` when missing `if` body with conditional `else` body. ([@koic][])
* [#12683](https://github.com/rubocop/rubocop/issues/12683): Fix an incorrect autocorrect for `Style/MapCompactWithConditionalBlock` when using guard clause with `next` implicitly nil. ([@koic][])
* [#12693](https://github.com/rubocop/rubocop/issues/12693): Fix an incorrect autocorrect for `Style/ObjectThen` when using `yield_self` without receiver. ([@koic][])
* [#12646](https://github.com/rubocop/rubocop/issues/12646): Fix `--auto-gen-config` bug for `Layout/SpaceBeforeBlockBraces`. ([@jonas054][])
* [#12717](https://github.com/rubocop/rubocop/issues/12717): Fix regexp for inline disable comments in `Style/CommentedKeyword`. ([@jonas054][])
* [#12695](https://github.com/rubocop/rubocop/issues/12695): Fix bug in `Include` from inherited file in a parent directory. ([@jonas054][])
* [#12656](https://github.com/rubocop/rubocop/pull/12656): Fix an error for `Layout/RedundantLineBreak` when using index access call chained on multiline hash literal. ([@koic][])
* [#12691](https://github.com/rubocop/rubocop/issues/12691): Fix an error for `Style/MultilineTernaryOperator` when nesting multiline ternary operators. ([@koic][])
* [#12707](https://github.com/rubocop/rubocop/pull/12707): Fix false negative for `Style/RedundantAssignment` when using pattern matching. ([@koic][])
* [#12674](https://github.com/rubocop/rubocop/pull/12674): Fix false negatives for `Style/RedundantReturn` when using pattern matching. ([@koic][])
* [#12673](https://github.com/rubocop/rubocop/pull/12673): Fix false negatives for `Lint/RedundantSafeNavigation` when using safe navigation operator for literal receiver. ([@koic][])
* [#12719](https://github.com/rubocop/rubocop/pull/12719): Fix false negatives for `Style/ArgumentsForwarding` when using forwardable block arguments with Ruby 3.2+. ([@koic][])
* [#12687](https://github.com/rubocop/rubocop/issues/12687): Fix a false positive for `Lint/Void` when `each` block with conditional expressions that has multiple statements. ([@koic][])
* [#12649](https://github.com/rubocop/rubocop/issues/12649): Fix false positives for `Style/InverseMethods` when using relational comparison operator with safe navigation. ([@koic][])
* [#12711](https://github.com/rubocop/rubocop/pull/12711): Handle implicit receivers in `Style/InvertibleUnlessCondition`. ([@sambostock][])
* [#12648](https://github.com/rubocop/rubocop/pull/12648): Fix numblock regressions in `omit_parentheses` `Style/MethodCallWithArgsParentheses`. ([@gsamokovarov][])

### Changes

* [#12641](https://github.com/rubocop/rubocop/pull/12641): Make error message clearer when the namespace is incorrect. ([@maruth-stripe][])
* [#12637](https://github.com/rubocop/rubocop/pull/12637): Mark `Style/RaiseArgs` as unsafe. ([@r7kamura][])
* [#12645](https://github.com/rubocop/rubocop/pull/12645): Change source order for target ruby to check gemspec after RuboCop configuration. ([@jenshenny][])

## 1.60.2 (2024-01-24)

### Bug fixes

* [#12627](https://github.com/rubocop/rubocop/issues/12627): Fix a false positive for `Layout/RedundantLineBreak` when using index access call chained on multiple lines with backslash. ([@koic][])
* [#12626](https://github.com/rubocop/rubocop/pull/12626): Fix a false positive for `Style/ArgumentsForwarding` when naming a block argument `&`. ([@koic][])
* [#12635](https://github.com/rubocop/rubocop/pull/12635): Fix a false positive for `Style/HashEachMethods` when both arguments are unused. ([@earlopain][])
* [#12636](https://github.com/rubocop/rubocop/pull/12636): Fix an error for `Style/HashEachMethods` when a block with both parameters has no body. ([@earlopain][])
* [#12638](https://github.com/rubocop/rubocop/issues/12638): Fix an `Errno::ENOENT` error when using server mode. ([@koic][])
* [#12628](https://github.com/rubocop/rubocop/pull/12628): Fix a false positive for `Style/ArgumentsForwarding` when using block arg forwarding with positional arguments forwarding to within block. ([@koic][])
* [#12642](https://github.com/rubocop/rubocop/pull/12642): Fix false positives for `Style/HashEachMethods` when using array converter method. ([@koic][])
* [#12632](https://github.com/rubocop/rubocop/issues/12632): Fix an infinite loop error when `EnforcedStyle: explicit` of `Naming/BlockForwarding` with `Style/ArgumentsForwarding`. ([@koic][])

## 1.60.1 (2024-01-17)

### Bug fixes

* [#12625](https://github.com/rubocop/rubocop/pull/12625): Fix an error when server cache dir has read-only file system. ([@Strzesia][])
* [#12618](https://github.com/rubocop/rubocop/issues/12618): Fix false positives for `Style/ArgumentsForwarding` when using block argument forwarding with other arguments. ([@koic][])
* [#12614](https://github.com/rubocop/rubocop/issues/12614): Fix false positiveis for `Style/RedundantParentheses` when parentheses in control flow keyword with multiline style argument. ([@koic][])

### Changes

* [#12617](https://github.com/rubocop/rubocop/issues/12617): Make `Style/CollectionCompact` aware of `grep_v` with nil. ([@koic][])

## 1.60.0 (2024-01-15)

### Bug fixes

* [#12603](https://github.com/rubocop/rubocop/issues/12603): Fix an infinite loop error for `Style/MultilineTernaryOperator` when using a method call as a ternary operator condition with a line break between receiver and method. ([@koic][])
* [#12549](https://github.com/rubocop/rubocop/issues/12549): Fix a false positive for `Style/RedundantLineContinuation` when line continuations for multiline leading dot method chain with a blank line. ([@koic][])
* [#12610](https://github.com/rubocop/rubocop/pull/12610): Accept parentheses in argument calls with blocks for `Style/MethodCallWithArgsParentheses` `omit_parentheses` style. ([@gsamokovarov][])
* [#12580](https://github.com/rubocop/rubocop/pull/12580): Fix an infinite loop error for `Layout/EndAlignment` when misaligned in singleton class assignments with `EnforcedStyleAlignWith: variable`. ([@koic][])
* [#12548](https://github.com/rubocop/rubocop/issues/12548): Fix an infinite loop error for `Layout/FirstArgumentIndentation` when specifying `EnforcedStyle: with_fixed_indentation` of `Layout/ArrayAlignment`. ([@koic][])
* [#12236](https://github.com/rubocop/rubocop/issues/12236): Fix an error for `Lint/ShadowedArgument` when self assigning to a block argument in `for`. ([@koic][])
* [#12569](https://github.com/rubocop/rubocop/issues/12569): Fix an error for `Style/IdenticalConditionalBranches` when using `if`...`else` with identical leading lines that assign to `self.foo`. ([@koic][])
* [#12437](https://github.com/rubocop/rubocop/issues/12437): Fix an infinite loop error for `EnforcedStyle: omit_parentheses` of `Style/MethodCallWithArgsParentheses` with `Style/SuperWithArgsParentheses`. ([@koic][])
* [#12558](https://github.com/rubocop/rubocop/issues/12558): Fix an incorrect autocorrect for `Style/MapToHash` when using `map.to_h` without receiver. ([@koic][])
* [#12179](https://github.com/rubocop/rubocop/issues/12179): Let `--auto-gen-config` generate `Exclude` when `Max` is overridden. ([@jonas054][])
* [#12574](https://github.com/rubocop/rubocop/issues/12574): Fix bug for unrecognized style in --auto-gen-config. ([@jonas054][])
* [#12542](https://github.com/rubocop/rubocop/issues/12542): Fix false positive for `Lint/MixedRegexpCaptureTypes` when using look-ahead matcher. ([@marocchino][])
* [#12607](https://github.com/rubocop/rubocop/pull/12607): Fix a false positive for `Style/RedundantParentheses` when regexp literal attempts to match against a parenthesized condition. ([@koic][])
* [#12539](https://github.com/rubocop/rubocop/pull/12539): Fix false positives for `Lint/LiteralAssignmentInCondition` when a collection literal contains non-literal elements. ([@koic][])
* [#12571](https://github.com/rubocop/rubocop/issues/12571): Fix false positives for `Naming/BlockForwarding` when using explicit block forwarding in block method. ([@koic][])
* [#12537](https://github.com/rubocop/rubocop/issues/12537): Fix false positives for `Style/RedundantParentheses` when `AllowInMultilineConditions: true` of `Style/ParenthesesAroundCondition`. ([@koic][])
* [#12578](https://github.com/rubocop/rubocop/pull/12578): Fix false positives for `Style/ArgumentsForwarding` when rest arguments forwarding to a method in block. ([@koic][])
* [#12540](https://github.com/rubocop/rubocop/issues/12540): Fix false positives for `Style/HashEachMethods` when rest block argument of `Enumerable#each` method is used. ([@koic][])
* [#12529](https://github.com/rubocop/rubocop/issues/12529): Fix false positives for `Style/ParenthesesAroundCondition`. ([@koic][])
* [#12556](https://github.com/rubocop/rubocop/issues/12556): Fix false positives for `Style/RedundantParentheses` when parentheses are used around a semantic operator in expressions within assignments. ([@koic][])
* [#12541](https://github.com/rubocop/rubocop/pull/12541): Fix false negative in `Style/ArgumentsForwarding` when a block is forwarded but other args aren't. ([@dvandersluis][])
* [#12581](https://github.com/rubocop/rubocop/pull/12581): Handle trailing line continuation in `Layout/LineContinuationLeadingSpace`. ([@eugeneius][])
* [#12601](https://github.com/rubocop/rubocop/issues/12601): Make `Style/EachForSimpleLoop` accept block with no parameters. ([@koic][])

### Changes

* [#12535](https://github.com/rubocop/rubocop/pull/12535): Allow --autocorrect with --display-only-fail-level-offenses. ([@naveg][])
* [#12572](https://github.com/rubocop/rubocop/pull/12572): Follow a Ruby 3.3 warning for `Security/Open` when `open` with a literal string starting with a pipe. ([@koic][])
* [#12453](https://github.com/rubocop/rubocop/issues/12453): Make `Style/RedundantEach` aware of safe navigation operator. ([@koic][])
* [#12233](https://github.com/rubocop/rubocop/issues/12233): Make `Style/SlicingWithRange` aware of redundant and beginless range. ([@koic][])
* [#12388](https://github.com/rubocop/rubocop/pull/12388): Reject additional 'expanded' `EnforcedStyle` options when `--no-auto-gen-enforced-style` is given. ([@kpost][])
* [#12593](https://github.com/rubocop/rubocop/pull/12593): Require Parser 3.3.0.2 or higher. ([@koic][])

## 1.59.0 (2023-12-11)

### New features

* [#12518](https://github.com/rubocop/rubocop/pull/12518): Add new `Lint/ItWithoutArgumentsInBlock` cop. ([@koic][])

### Bug fixes

* [#12434](https://github.com/rubocop/rubocop/issues/12434): Fix a false positive for `Lint/LiteralAssignmentInCondition` when using interpolated string or xstring literals. ([@koic][])
* [#12435](https://github.com/rubocop/rubocop/issues/12435): Fix a false positive for `Lint/SelfAssignment` when using attribute assignment with method call with arguments. ([@koic][])
* [#12444](https://github.com/rubocop/rubocop/issues/12444): Fix false positive for `Style/HashEachMethods` when receiver literal is not a hash literal. ([@koic][])
* [#12524](https://github.com/rubocop/rubocop/issues/12524): Fix a false positive for `Style/MethodCallWithArgsParentheses` when `EnforcedStyle: omit_parentheses` and parens in `when` clause is used to pass an argument. ([@koic][])
* [#12505](https://github.com/rubocop/rubocop/pull/12505): Fix a false positive for `Style/RedundantParentheses` when using parenthesized `lambda` or `proc` with `do`...`end` block. ([@koic][])
* [#12442](https://github.com/rubocop/rubocop/issues/12442): Fix an incorrect autocorrect for `Style/CombinableLoops` when looping over the same data as previous loop in `do`...`end` and `{`...`}` blocks. ([@koic][])
* [#12432](https://github.com/rubocop/rubocop/pull/12432): Fix a false positive for `Lint/LiteralAssignmentInCondition` when using parallel assignment with splat operator in block of guard condition. ([@koic][])
* [#12441](https://github.com/rubocop/rubocop/issues/12441): Fix false positives for `Style/HashEachMethods` when using destructed block arguments. ([@koic][])
* [#12436](https://github.com/rubocop/rubocop/issues/12436): Fix false positives for `Style/RedundantParentheses` when a part of range is a parenthesized condition. ([@koic][])
* [#12429](https://github.com/rubocop/rubocop/issues/12429): Fix incorrect autocorrect for `Style/MapToHash` when using dot method calls for `to_h`. ([@koic][])
* [#12488](https://github.com/rubocop/rubocop/issues/12488): Make `Lint/HashCompareByIdentity` aware of safe navigation operator. ([@koic][])
* [#12489](https://github.com/rubocop/rubocop/issues/12489): Make `Lint/NextWithoutAccumulator` aware of safe navigation operator. ([@koic][])
* [#12490](https://github.com/rubocop/rubocop/issues/12490): Make `Lint/NumberConversion` aware of safe navigation operator. ([@koic][])
* [#12491](https://github.com/rubocop/rubocop/issues/12491): Make `Lint/RedundantWithIndex` aware of safe navigation operator. ([@koic][])
* [#12492](https://github.com/rubocop/rubocop/issues/12492): Make `Lint/RedundantWithObject` aware of safe navigation operator. ([@koic][])
* [#12493](https://github.com/rubocop/rubocop/issues/12493): Make `Lint/UnmodifiedReduceAccumulator` aware of safe navigation operator. ([@koic][])
* [#12473](https://github.com/rubocop/rubocop/issues/12473): Make `Style/ClassCheck` aware of safe navigation operator. ([@koic][])
* [#12445](https://github.com/rubocop/rubocop/issues/12445): Make `Style/CollectionCompact` aware of safe navigation operator. ([@koic][])
* [#12474](https://github.com/rubocop/rubocop/issues/12474): Make `Style/ConcatArrayLiterals` aware of safe navigation operator. ([@koic][])
* [#12476](https://github.com/rubocop/rubocop/issues/12476): Make `Style/DateTime` aware of safe navigation operator. ([@koic][])
* [#12479](https://github.com/rubocop/rubocop/issues/12479): Make `Style/EachWithObject` aware of safe navigation operator. ([@koic][])
* [#12446](https://github.com/rubocop/rubocop/issues/12446): Make `Style/HashExcept` aware of safe navigation operator. ([@koic][])
* [#12447](https://github.com/rubocop/rubocop/issues/12447): Make `Style/MapCompactWithConditionalBlock` aware of safe navigation operator. ([@koic][])
* [#12484](https://github.com/rubocop/rubocop/issues/12484): Make `Style/Next` aware of safe navigation operator. ([@koic][])
* [#12486](https://github.com/rubocop/rubocop/issues/12486): Make `Style/RedundantArgument` aware of safe navigation operator. ([@koic][])
* [#12454](https://github.com/rubocop/rubocop/issues/12454): Make `Style/RedundantFetchBlock` aware of safe navigation operator. ([@koic][])
* [#12495](https://github.com/rubocop/rubocop/issues/12495): Make `Layout/RedundantLineBreak` aware of safe navigation operator. ([@koic][])
* [#12455](https://github.com/rubocop/rubocop/issues/12455): Make `Style/RedundantSortBy` aware of safe navigation operator. ([@koic][])
* [#12456](https://github.com/rubocop/rubocop/issues/12456): Make `Style/RedundantSortBy` aware of safe navigation operator. ([@koic][])
* [#12480](https://github.com/rubocop/rubocop/issues/12480): Make `Style/ExactRegexpMatch` aware of safe navigation operator. ([@koic][])
* [#12457](https://github.com/rubocop/rubocop/issues/12457): Make `Style/Sample` aware of safe navigation operator. ([@koic][])
* [#12458](https://github.com/rubocop/rubocop/issues/12458): Make `Style/SelectByRegexp` cops aware of safe navigation operator. ([@koic][])
* [#12494](https://github.com/rubocop/rubocop/issues/12494): Make `Layout/SingleLineBlockChain` aware of safe navigation operator. ([@koic][])
* [#12461](https://github.com/rubocop/rubocop/issues/12461): Make `Style/StringChars` aware of safe navigation operator. ([@koic][])
* [#12468](https://github.com/rubocop/rubocop/issues/12468): Make `Style/Strip` aware of safe navigation operator. ([@koic][])
* [#12469](https://github.com/rubocop/rubocop/issues/12469): Make `Style/UnpackFirst` aware of safe navigation operator. ([@koic][])

### Changes

* [#12522](https://github.com/rubocop/rubocop/pull/12522): Make `Style/MethodCallWithoutArgsParentheses` allow the parenthesized `it` method in a block. ([@koic][])
* [#12523](https://github.com/rubocop/rubocop/pull/12523): Make `Style/RedundantSelf` allow the `self.it` method in a block. ([@koic][])

## 1.58.0 (2023-12-01)

### New features

* [#12420](https://github.com/rubocop/rubocop/pull/12420): Add new `Lint/LiteralAssignmentInCondition` cop. ([@koic][])
* [#12353](https://github.com/rubocop/rubocop/issues/12353): Add new `Style/SuperWithArgsParentheses` cop. ([@koic][])
* [#12406](https://github.com/rubocop/rubocop/issues/12406): Add new `Style/ArrayFirstLast` cop. ([@fatkodima][])

### Bug fixes

* [#12372](https://github.com/rubocop/rubocop/issues/12372): Fix a false negative for `Lint/Debugger` when used within method arguments a `begin`...`end` block. ([@koic][])
* [#12378](https://github.com/rubocop/rubocop/pull/12378): Fix a false negative for `Style/Semicolon` when a semicolon at the beginning of a lambda block. ([@koic][])
* [#12146](https://github.com/rubocop/rubocop/issues/12146): Fix a false positive for `Lint/FloatComparison` when comparing against zero. ([@earlopain][])
* [#12404](https://github.com/rubocop/rubocop/issues/12404): Fix a false positive for `Layout/RescueEnsureAlignment` when aligned `rescue` in `do`-`end` numbered block in a method. ([@koic][])
* [#12374](https://github.com/rubocop/rubocop/issues/12374): Fix a false positive for `Layout/SpaceBeforeSemicolon` when a space between an opening lambda brace and a semicolon. ([@koic][])
* [#12326](https://github.com/rubocop/rubocop/pull/12326): Fix an error for `Style/RedundantDoubleSplatHashBraces` when method call for parenthesized no hash double double splat. ([@koic][])
* [#12361](https://github.com/rubocop/rubocop/issues/12361): Fix an incorrect autocorrect for `Naming/BlockForwarding` and `Style/ArgumentsForwarding` when autocorrection conflicts for anonymous arguments. ([@koic][])
* [#12324](https://github.com/rubocop/rubocop/issues/12324): Fix an error for `Layout/RescueEnsureAlignment` when using `rescue` in `do`...`end` block assigned to object attribute. ([@koic][])
* [#12322](https://github.com/rubocop/rubocop/issues/12322): Fix an error for `Style/CombinableLoops` when looping over the same data for the third consecutive time or more. ([@koic][])
* [#12366](https://github.com/rubocop/rubocop/pull/12366): Fix a false negative for `Layout/ExtraSpacing` when a file has exactly two comments. ([@eugeneius][])
* [#12373](https://github.com/rubocop/rubocop/issues/12373): Fix a false negative for `Lint/SymbolConversion` when using string interpolation. ([@earlopain][])
* [#12402](https://github.com/rubocop/rubocop/issues/12402): Fix false negatives for `Style/RedundantLineContinuation` when redundant line continuations for a block are used, especially without parentheses around first argument. ([@koic][])
* [#12311](https://github.com/rubocop/rubocop/issues/12311): Fix false negatives for `Style/RedundantParentheses` when parentheses around logical operator keywords in method definition. ([@koic][])
* [#12394](https://github.com/rubocop/rubocop/issues/12394): Fix false negatives for `Style/RedundantReturn` when `lambda` (`->`) ending with `return`. ([@koic][])
* [#12377](https://github.com/rubocop/rubocop/issues/12377): Fix false positives for `Lint/Void` when a collection literal that includes non-literal elements in a method definition. ([@koic][])
* [#12407](https://github.com/rubocop/rubocop/pull/12407): Fix an incorrect autocorrect for `Style/MapToHash` with `Layout/SingleLineBlockChain`. ([@koic][])
* [#12409](https://github.com/rubocop/rubocop/issues/12409): Fix an incorrect autocorrect for `Lint/SafeNavigationChain` when ordinary method chain exists after safe navigation leading dot method call. ([@koic][])
* [#12363](https://github.com/rubocop/rubocop/issues/12363): Fix incorrect rendering of HTML character entities in `HTMLFormatter` formatter. ([@koic][])
* [#12424](https://github.com/rubocop/rubocop/issues/12424): Make `Style/HashEachMethods` aware of safe navigation operator. ([@koic][])
* [#12413](https://github.com/rubocop/rubocop/issues/12413): Make `Style/InverseMethods` aware of safe navigation operator. ([@koic][])
* [#12408](https://github.com/rubocop/rubocop/pull/12408): Make `Style/MapToHash` aware of safe navigation operator. ([@koic][])

### Changes

* [#12328](https://github.com/rubocop/rubocop/issues/12328): Make `Style/AutoResourceCleanup` aware of `Tempfile.open`. ([@koic][])
* [#12412](https://github.com/rubocop/rubocop/issues/12412): Enhance `Lint/RedundantSafeNavigation` to handle conversion methods with defaults. ([@fatkodima][])
* [#12410](https://github.com/rubocop/rubocop/issues/12410): Enhance `Lint/SelfAssignment` to check attribute assignment and key assignment. ([@fatkodima][])
* [#12370](https://github.com/rubocop/rubocop/issues/12370): Make `Style/HashEachMethods` aware of unused block value. ([@koic][])
* [#12380](https://github.com/rubocop/rubocop/issues/12380): Make `Style/RedundantParentheses` aware of lambda or proc. ([@koic][])
* [#12421](https://github.com/rubocop/rubocop/pull/12421): Make `Style/SelfAssignment` aware of `%`, `^`, `<<`, and `>>` operators. ([@koic][])
* [#12305](https://github.com/rubocop/rubocop/pull/12305): Require `rubocop-ast` version 1.30 or greater. ([@sambostock][])
* [#12337](https://github.com/rubocop/rubocop/issues/12337): Supports `EnforcedStyleForRationalLiterals` option for `Layout/SpaceAroundOperators`. ([@koic][])
* [#12296](https://github.com/rubocop/rubocop/issues/12296): Support `RedundantRestArgumentNames`, `RedundantKeywordRestArgumentNames`, and `RedundantBlockArgumentNames` options for `Style/ArgumentsForwarding`. ([@koic][])

## 1.57.2 (2023-10-26)

### Bug fixes

* [#12274](https://github.com/rubocop/rubocop/issues/12274): Fix a false positive for `Lint/Void` when `each`'s receiver is an object of `Enumerator` to which `filter` has been applied. ([@koic][])
* [#12291](https://github.com/rubocop/rubocop/issues/12291): Fix a false positive for `Metrics/ClassLength` when a class with a singleton class definition. ([@koic][])
* [#12293](https://github.com/rubocop/rubocop/issues/12293): Fix a false positive for `Style/RedundantDoubleSplatHashBraces` when using double splat hash braces with `merge` and method chain. ([@koic][])
* [#12298](https://github.com/rubocop/rubocop/issues/12298): Fix a false positive for `Style/RedundantParentheses` when using a parenthesized hash literal as the first argument in a method call without parentheses. ([@koic][])
* [#12283](https://github.com/rubocop/rubocop/pull/12283): Fix an error for `Style/SingleLineDoEndBlock` when using single line `do`...`end` with no body. ([@koic][])
* [#12312](https://github.com/rubocop/rubocop/issues/12312): Fix an incorrect autocorrect for `Style/HashSyntax` when braced hash key and value are the same and it is used in `if`...`else`. ([@koic][])
* [#12307](https://github.com/rubocop/rubocop/issues/12307): Fix an infinite loop error for `Layout/EndAlignment` when `EnforcedStyleAlignWith: variable` and using a conditional statement in a method argument on the same line and `end` with method call is not aligned. ([@koic][])
* [#11652](https://github.com/rubocop/rubocop/issues/11652): Make `--auto-gen-config` generate `inherit_from` correctly inside ERB `if`. ([@jonas054][])
* [#12310](https://github.com/rubocop/rubocop/issues/12310): Drop `base64` gem from runtime dependency. ([@koic][])
* [#12300](https://github.com/rubocop/rubocop/issues/12300): Fix an error for `Style/IdenticalConditionalBranches` when `if`...`else` with identical leading lines and using index assign. ([@koic][])
* [#12286](https://github.com/rubocop/rubocop/issues/12286): Fix false positives for `Style/RedundantDoubleSplatHashBraces` when using double splat with a hash literal enclosed in parenthesized ternary operator. ([@koic][])
* [#12279](https://github.com/rubocop/rubocop/issues/12279): Fix false positives for `Lint/EmptyConditionalBody` when missing 2nd `if` body with a comment. ([@koic][])
* [#12275](https://github.com/rubocop/rubocop/issues/12275): Fix a false positive for `Style/RedundantDoubleSplatHashBraces` when using double splat within block argument containing a hash literal in an array literal. ([@koic][])
* [#12284](https://github.com/rubocop/rubocop/issues/12284): Fix false positives for `Style/SingleArgumentDig` when using some anonymous argument syntax. ([@koic][])
* [#12301](https://github.com/rubocop/rubocop/issues/12301): Make `Style/RedundantFilterChain` aware of safe navigation operator. ([@koic][])

## 1.57.1 (2023-10-13)

### Bug fixes

* [#12271](https://github.com/rubocop/rubocop/issues/12271): Fix a false positive for `Lint/RedundantSafeNavigation` when using snake case constant receiver. ([@koic][])
* [#12265](https://github.com/rubocop/rubocop/issues/12265): Fix an error for `Layout/MultilineMethodCallIndentation` when usingarithmetic operation with block inside a grouped expression. ([@koic][])
* [#12177](https://github.com/rubocop/rubocop/pull/12177): Fix an incorrect autocorrect for `Style/RedundantException`. ([@ydah][])
* [#12261](https://github.com/rubocop/rubocop/issues/12261): Fix an infinite loop for `Layout/MultilineMethodCallIndentation` when multiline method chain with a block argument and method chain. ([@ydah][])
* [#12263](https://github.com/rubocop/rubocop/issues/12263): Fix false positives for `Style/RedundantDoubleSplatHashBraces` when method call for no hash braced double splat receiver. ([@koic][])
* [#12262](https://github.com/rubocop/rubocop/pull/12262): Fix an incorrect autocorrect for `Style/RedundantDoubleSplatHashBraces` when using double splat hash braces with `merge` method call twice. ([@koic][])

## 1.57.0 (2023-10-11)

### New features

* [#12227](https://github.com/rubocop/rubocop/pull/12227): Add new `Style/SingleLineDoEndBlock` cop. ([@koic][])
* [#12246](https://github.com/rubocop/rubocop/pull/12246): Make `Lint/RedundantSafeNavigation` aware of constant receiver. ([@koic][])
* [#12257](https://github.com/rubocop/rubocop/issues/12257): Make `Style/RedundantDoubleSplatHashBraces` aware of `merge` methods. ([@koic][])

### Bug fixes

* [#12244](https://github.com/rubocop/rubocop/issues/12244): Fix a false negative for `Lint/Debugger` when using debugger method inside block. ([@koic][])
* [#12231](https://github.com/rubocop/rubocop/issues/12231): Fix a false negative for `Metrics/ModuleLength` when defining a singleton class in a module. ([@koic][])
* [#12249](https://github.com/rubocop/rubocop/issues/12249): Fix a false positive `Style/IdenticalConditionalBranches` when `if`..`else` with identical leading lines and assign to condition value. ([@koic][])
* [#12253](https://github.com/rubocop/rubocop/pull/12253): Fix `Lint/LiteralInInterpolation` to accept an empty string literal interpolated in words literal. ([@knu][])
* [#12198](https://github.com/rubocop/rubocop/issues/12198): Fix an error for flip-flop with beginless or endless ranges. ([@koic][])
* [#12259](https://github.com/rubocop/rubocop/issues/12259): Fix an error for `Lint/MixedCaseRange` when using nested character class in regexp. ([@koic][])
* [#12237](https://github.com/rubocop/rubocop/issues/12237): Fix an error for `Style/NestedTernaryOperator` when a ternary operator has a nested ternary operator within an `if`. ([@koic][])
* [#12228](https://github.com/rubocop/rubocop/pull/12228): Fix false negatives for `Style/MultilineBlockChain` when using multiline block chain with safe navigation operator. ([@koic][])
* [#12247](https://github.com/rubocop/rubocop/pull/12247): Fix false negatives for `Style/RedundantParentheses` when using logical or comparison expressions with redundant parentheses. ([@koic][])
* [#12226](https://github.com/rubocop/rubocop/issues/12226): Fix false positives for `Layout/MultilineMethodCallIndentation` when aligning methods in multiline block chain. ([@koic][])
* [#12076](https://github.com/rubocop/rubocop/issues/12076): Fixed an issue where the top-level cache folder was named differently during two consecutive rubocop runs. ([@K-S-A][])

### Changes

* [#12235](https://github.com/rubocop/rubocop/pull/12235): Enable auto parallel inspection when config file is specified. ([@aboutNisblee][])
* [#12234](https://github.com/rubocop/rubocop/pull/12234): Enhance `Style/FormatString`'s autocorrection when using known conversion methods whose return value is not an array. ([@koic][])
* [#12128](https://github.com/rubocop/rubocop/issues/12128): Make `Style/GuardClause` aware of `define_method`. ([@koic][])
* [#12126](https://github.com/rubocop/rubocop/pull/12126): Make `Style/RedundantFilterChain` aware of `select.present?` when `ActiveSupportExtensionsEnabled` config is `true`. ([@koic][])
* [#12250](https://github.com/rubocop/rubocop/pull/12250): Mark `Lint/RedundantRequireStatement` as unsafe autocorrect. ([@koic][])
* [#12097](https://github.com/rubocop/rubocop/issues/12097): Mark unsafe autocorrect for `Style/ClassEqualityComparison`. ([@koic][])
* [#12210](https://github.com/rubocop/rubocop/issues/12210): Mark `Style/RedundantFilterChain` as unsafe autocorrect. ([@koic][])

## 1.56.4 (2023-09-28)

### Bug fixes

* [#12221](https://github.com/rubocop/rubocop/issues/12221): Fix a false positive for `Layout/EmptyLineAfterGuardClause` when using `return` before guard condition with heredoc. ([@koic][])
* [#12213](https://github.com/rubocop/rubocop/issues/12213): Fix a false positive for `Lint/OrderedMagicComments` when comment text `# encoding: ISO-8859-1` is embedded within example code as source code comment. ([@koic][])
* [#12205](https://github.com/rubocop/rubocop/issues/12205): Fix an error for `Style/OperatorMethodCall` when using `foo bar./ baz`. ([@koic][])
* [#12208](https://github.com/rubocop/rubocop/issues/12208): Fix an incorrect autocorrect for the `--disable-uncorrectable` command line option when registering an offense is outside a percent array. ([@koic][])
* [#12203](https://github.com/rubocop/rubocop/pull/12203): Fix an incorrect autocorrect for `Lint/SafeNavigationChain` when using safe navigation with comparison operator as an expression of logical operator or comparison operator's operand. ([@koic][])
* [#12206](https://github.com/rubocop/rubocop/pull/12206): Fix an incorrect autocorrect for `Style/OperatorMethodCall` when using `foo./bar`. ([@koic][])
* [#12202](https://github.com/rubocop/rubocop/pull/12202): Fix an incorrect autocorrect for `Style/RedundantConditional` when unless/else with boolean results. ([@ydah][])
* [#12199](https://github.com/rubocop/rubocop/issues/12199): Fix false negatives for `Layout/MultilineMethodCallIndentation` when using safe navigation operator. ([@koic][])

### Changes

* [#12197](https://github.com/rubocop/rubocop/pull/12197): Make `Style/CollectionMethods` aware of `collect_concat`. ([@koic][])

## 1.56.3 (2023-09-11)

### Bug fixes

* [#12151](https://github.com/rubocop/rubocop/issues/12151): Make `Layout/EmptyLineAfterGuardClause` allow `:nocov:` directive after guard clause. ([@koic][])
* [#12195](https://github.com/rubocop/rubocop/issues/12195): Fix a false negative for `Layout/SpaceAfterNot` when a newline is present after `!`. ([@ymap][])
* [#12192](https://github.com/rubocop/rubocop/issues/12192): Fix a false positive for `Layout/RedundantLineBreak` when using quoted symbols with a single newline. ([@ymap][])
* [#12190](https://github.com/rubocop/rubocop/issues/12190): Fix a false positive for `Layout/SpaceAroundOperators` when aligning operators vertically. ([@koic][])
* [#12171](https://github.com/rubocop/rubocop/issues/12171): Fix a false positive for `Style/ArrayIntersect` when using block argument for `Enumerable#any?`. ([@koic][])
* [#12172](https://github.com/rubocop/rubocop/issues/12172): Fix a false positive for `Style/EmptyCaseCondition` when using `return`, `break`, `next` or method call before empty case condition. ([@koic][])
* [#12162](https://github.com/rubocop/rubocop/issues/12162): Fix an error for `Bundler/DuplicatedGroup` when there's a duplicate set of groups and the `group` value contains a splat. ([@koic][])
* [#12182](https://github.com/rubocop/rubocop/issues/12182): Fix an error for `Lint/UselessAssignment` when variables are assigned using chained assignment and remain unreferenced. ([@koic][])
* [#12181](https://github.com/rubocop/rubocop/issues/12181): Fix an incorrect autocorrect for `Lint/UselessAssignment` when variables are assigned with sequential assignment using the comma operator and unreferenced. ([@koic][])
* [#12187](https://github.com/rubocop/rubocop/issues/12187): Fix an incorrect autocorrect for `Style/SoleNestedConditional` when comment is in an empty nested `if` body. ([@ymap][])
* [#12183](https://github.com/rubocop/rubocop/pull/12183): Fix an incorrect autocorrect for `Style/MultilineTernaryOperator` when returning a multiline ternary operator expression with safe navigation method call. ([@koic][])
* [#12168](https://github.com/rubocop/rubocop/issues/12168): Fix bug in `Style/ArgumentsForwarding` when there are repeated send nodes. ([@owst][])
* [#12185](https://github.com/rubocop/rubocop/pull/12185): Set target version for `Layout/HeredocIndentation`. ([@tagliala][])

## 1.56.2 (2023-08-29)

### Bug fixes

* [#12138](https://github.com/rubocop/rubocop/issues/12138): Fix a false positive for `Layout/LineContinuationLeadingSpace` when a backslash is part of a multiline string literal. ([@ymap][])
* [#12155](https://github.com/rubocop/rubocop/pull/12155): Fix false positive for `Layout/RedundantLineBreak` when using a modified singleton method definition. ([@koic][])
* [#12143](https://github.com/rubocop/rubocop/issues/12143): Fix a false positive for `Lint/ToEnumArguments` when using anonymous keyword arguments forwarding. ([@koic][])
* [#12148](https://github.com/rubocop/rubocop/pull/12148): Fix an incorrect autocorrect for `Lint/NonAtomicFileOperation` when using `FileUtils.remove_dir`, `FileUtils.remove_entry`, or `FileUtils.remove_entry_secure`. ([@koic][])
* [#12141](https://github.com/rubocop/rubocop/issues/12141): Fix false positive for `Style/ArgumentsForwarding` when method def includes additional kwargs. ([@owst][])
* [#12154](https://github.com/rubocop/rubocop/issues/12154): Fix incorrect `diagnosticProvider` value of LSP. ([@koic][])

## 1.56.1 (2023-08-21)

### Bug fixes

* [#12136](https://github.com/rubocop/rubocop/pull/12136): Fix a false negative for `Layout/LeadingCommentSpace` when using `#+` or `#-` as they are not RDoc comments. ([@koic][])
* [#12113](https://github.com/rubocop/rubocop/issues/12113): Fix a false positive for `Bundler/DuplicatedGroup` when groups are duplicated but `source`, `git`, `platforms`, or `path` values are different. ([@koic][])
* [#12134](https://github.com/rubocop/rubocop/issues/12134): Fix a false positive for `Style/MethodCallWithArgsParentheses` when parentheses are used in one-line `in` pattern matching. ([@koic][])
* [#12111](https://github.com/rubocop/rubocop/issues/12111): Fix an error for `Bundler/DuplicatedGroup` group declaration has keyword option. ([@koic][])
* [#12109](https://github.com/rubocop/rubocop/issues/12109): Fix an error for `Style/ArgumentsForwarding` cop when forwarding kwargs/block arg and an additional arg. ([@ydah][])
* [#12117](https://github.com/rubocop/rubocop/issues/12117): Fix a false positive for `Style/ArgumentsForwarding` cop when not always forwarding block. ([@owst][])
* [#12115](https://github.com/rubocop/rubocop/pull/12115): Fix an error for `Style/Lambda` when using numbered parameter with a multiline `->` call. ([@koic][])
* [#12124](https://github.com/rubocop/rubocop/issues/12124): Fix false positives for `Style/RedundantParentheses` when parentheses in `super` or `yield` call with multiline style argument. ([@koic][])
* [#12120](https://github.com/rubocop/rubocop/pull/12120): Fix false positives for `Style/SymbolArray` when `%i` array containing unescaped `[`, `]`, `(`, or `)`. ([@koic][])
* [#12133](https://github.com/rubocop/rubocop/pull/12133): Fix `Style/RedundantSelfAssignmentBranch` to handle heredocs. ([@r7kamura][])
* [#12105](https://github.com/rubocop/rubocop/issues/12105): Fix target ruby `Gem::Requirement` matcher and version parsing to support multiple version constraints. ([@ItsEcholot][])

## 1.56.0 (2023-08-09)

### New features

* [#12074](https://github.com/rubocop/rubocop/pull/12074): Add new `Bundler/DuplicatedGroup` cop. ([@OwlKing][])
* [#12078](https://github.com/rubocop/rubocop/pull/12078): Make LSP server support `rubocop.formatAutocorrectsAll` execute command. ([@koic][])

### Bug fixes

* [#12106](https://github.com/rubocop/rubocop/issues/12106): Fix a false negative for `Style/RedundantReturn` when returning value with guard clause and `return` is used. ([@koic][])
* [#12095](https://github.com/rubocop/rubocop/pull/12095): Fix a false positive for `Style/Alias` when `EncforcedStyle: prefer_alias` and using `alias` with interpolated symbol argument. ([@koic][])
* [#12098](https://github.com/rubocop/rubocop/pull/12098): Fix a false positive for `Style/ClassEqualityComparison` when comparing interpolated string class name for equality. ([@koic][])
* [#12102](https://github.com/rubocop/rubocop/pull/12102): Fix an error for `Style/LambdaCall` when using nested lambda call `x.().()`. ([@koic][])
* [#12099](https://github.com/rubocop/rubocop/pull/12099): Fix an incorrect autocorrect for `Style/Alias` when `EncforcedStyle: prefer_alias_method` and using `alias` with interpolated symbol argument. ([@koic][])
* [#12085](https://github.com/rubocop/rubocop/issues/12085): Fix an error for `Lint/SuppressedException` when `AllowNil: true` is set and endless method definition is used. ([@koic][])
* [#12087](https://github.com/rubocop/rubocop/issues/12087): Fix false positives for `Style/ArgumentsForwarding` with additional args/kwargs in def/send nodes. ([@owst][])
* [#12071](https://github.com/rubocop/rubocop/issues/12071): Fix `Style/SymbolArray` false positives when using square brackets or interpolation in a symbol literal in a percent style array. ([@jasondoc3][])
* [#12061](https://github.com/rubocop/rubocop/issues/12061): Support regex in StringLiteralsInInterpolation. ([@jonas054][])
* [#12091](https://github.com/rubocop/rubocop/pull/12091): With `--fail-level A` ignore non-correctable offenses at :info severity. ([@naveg][])

### Changes

* [#12094](https://github.com/rubocop/rubocop/pull/12094): Add `base64` gem to runtime dependency to suppress Ruby 3.3's warning. ([@koic][])

## 1.55.1 (2023-07-31)

### Bug fixes

* [#12068](https://github.com/rubocop/rubocop/pull/12068): Fix a false positive for `Style/ReturnNilInPredicateMethodDefinition` when the last method argument in method definition is `nil`. ([@koic][])
* [#12082](https://github.com/rubocop/rubocop/issues/12082): Fix an error for `Lint/UselessAssignment` when a variable is assigned and unreferenced in `for` with multiple variables. ([@koic][])
* [#12079](https://github.com/rubocop/rubocop/issues/12079): Fix an error for `Style/MixinGrouping` when mixin method has no arguments. ([@koic][])
* [#11637](https://github.com/rubocop/rubocop/pull/11637): Correct Rubocop for `private_class_method` method documentation. ([@bigzed][])
* [#12070](https://github.com/rubocop/rubocop/pull/12070): Fix false positive in `Style/ArgumentsForwarding` when receiver forwards args/kwargs. ([@owst][])

## 1.55.0 (2023-07-25)

### New features

* [#11794](https://github.com/rubocop/rubocop/pull/11794): Add support to `Style/ArgumentsForwarding` for anonymous arg/kwarg forwarding in Ruby 3.2. ([@owst][])
* [#12044](https://github.com/rubocop/rubocop/issues/12044): Make LSP server support `layoutMode` option to run layout cops. ([@koic][])
* [#12056](https://github.com/rubocop/rubocop/pull/12056): Make LSP server support `lintMode` option to run lint cops. ([@koic][])
* [#12046](https://github.com/rubocop/rubocop/issues/12046): Make `ReturnNilInPredicateMethodDefinition` aware of `nil` at the end of predicate method definition. ([@koic][])

### Bug fixes

* [#12055](https://github.com/rubocop/rubocop/pull/12055): Allow parentheses in single-line match patterns when using the `omit_parentheses` style of `Style/MethodCallWithArgsParentheses`. ([@gsamokovarov][])
* [#12050](https://github.com/rubocop/rubocop/pull/12050): Fix a false positive for `Layout/RedundantLineBreak` when inspecting the `%` form string `%\n\n`. ([@koic][])
* [#12063](https://github.com/rubocop/rubocop/pull/12063): Fix `Style/CombinableLoops` when one of the loops is empty. ([@fatkodima][])
* [#12059](https://github.com/rubocop/rubocop/issues/12059): Fix a false negative for `Style/StringLiteralsInInterpolation` for symbols with interpolation. ([@fatkodima][])
* [#11834](https://github.com/rubocop/rubocop/issues/11834): Fix false positive for when variable in inside conditional branch in nested node. ([@alexeyschepin][])
* [#11802](https://github.com/rubocop/rubocop/issues/11802): Improve handling of `[]` and `()` with percent symbol arrays. ([@jasondoc3][])
* [#12052](https://github.com/rubocop/rubocop/issues/12052): Fix "Subfolders can't include glob special characters". ([@meric426][], [@loveo][])
* [#12062](https://github.com/rubocop/rubocop/pull/12062): Fix `LoadError` when loading RuboCop from a symlinked location on Windows. ([@p0deje][])

### Changes

* [#12064](https://github.com/rubocop/rubocop/pull/12064): Make `Style/RedundantArgument` aware of `exit` and `exit!`. ([@koic][])
* [#12015](https://github.com/rubocop/rubocop/issues/12015): Mark `Style/HashConversion` as unsafe autocorrection. ([@koic][])

## 1.54.2 (2023-07-13)

### Bug fixes

* [#12043](https://github.com/rubocop/rubocop/pull/12043): Fix a false negative for `Layout/ExtraSpacing` when some characters are vertically aligned. ([@koic][])
* [#12040](https://github.com/rubocop/rubocop/pull/12040): Fix a false positive for `Layout/TrailingEmptyLines` to prevent the following incorrect autocorrection when inspecting the `%` form string `%\n\n`. ([@koic][])
* [#1867](https://github.com/rubocop/rubocop/issues/1867): Fix an error when `AllCops:Exclude` is empty in .rubocop.yml. ([@koic][])
* [#12034](https://github.com/rubocop/rubocop/issues/12034): Fix invalid byte sequence in UTF-8 error when using an invalid encoding string. ([@koic][])
* [#12038](https://github.com/rubocop/rubocop/pull/12038): Output the "server restarting" message to stderr. ([@knu][])

## 1.54.1 (2023-07-04)

### Bug fixes

* [#12024](https://github.com/rubocop/rubocop/issues/12024): Fix a false positive for `Lint/RedundantRegexpQuantifiers` when interpolation is used in a regexp literal. ([@koic][])
* [#12020](https://github.com/rubocop/rubocop/issues/12020): This PR fixes an infinite loop error for `Layout/SpaceAfterComma` with `Layout/SpaceBeforeSemicolon` when autocorrection conflicts. ([@koic][])
* [#12014](https://github.com/rubocop/rubocop/pull/12014): Fix an error for `Lint/UselessAssignment` when part of a multiple assignment is enclosed in parentheses. ([@koic][])
* [#12011](https://github.com/rubocop/rubocop/pull/12011): Fix an error for `Metrics/MethodLength` when using a heredoc in a block without block arguments. ([@koic][])
* [#12010](https://github.com/rubocop/rubocop/pull/12010): Fix false negatives for `Style/RedundantRegexpArgument` when using safe navigation operator. ([@koic][])

## 1.54.0 (2023-07-01)

### New features

* [#12000](https://github.com/rubocop/rubocop/pull/12000): Support safe or unsafe autocorrect config for LSP. ([@koic][])

### Bug fixes

* [#12005](https://github.com/rubocop/rubocop/issues/12005): Fix a false negative for `Lint/Debugger` when using debugger method inside lambda. ([@koic][])
* [#11986](https://github.com/rubocop/rubocop/issues/11986): Fix a false positive for `Lint/MixedCaseRange` when the number of characters at the start or end of range is other than 1. ([@koic][])
* [#11992](https://github.com/rubocop/rubocop/issues/11992): Fix an unexpected `NoMethodError` for built-in language server when an internal error occurs. ([@koic][])
* [#11994](https://github.com/rubocop/rubocop/issues/11994): Fix an error for `Layout/LineEndStringConcatenationIndentation` when inspecting the `%` from string `%\n\n`. ([@koic][])
* [#12007](https://github.com/rubocop/rubocop/issues/12007): Fix an error for `Layout/SpaceAroundOperators` when using unary operator with double colon. ([@koic][])
* [#11996](https://github.com/rubocop/rubocop/issues/11996): Fix an error for `Style/IfWithSemicolon` when without branch bodies. ([@koic][])
* [#12009](https://github.com/rubocop/rubocop/pull/12009): Fix an error for `Style/YodaCondition` when equality check method is used without the first argument. ([@koic][])
* [#11998](https://github.com/rubocop/rubocop/issues/11998): Fix an error when inspecting blank heredoc delimiter. ([@koic][])
* [#11989](https://github.com/rubocop/rubocop/issues/11989): Fix an incorrect autocorrect for `Style/RedundantRegexpArgument` when using unicode chars. ([@koic][])
* [#12001](https://github.com/rubocop/rubocop/issues/12001): Fix code length calculator for method calls with heredoc. ([@fatkodima][])
* [#12002](https://github.com/rubocop/rubocop/pull/12002): Fix `Lint/Void` cop for `__ENCODING__` constant. ([@fatkodima][])

### Changes

* [#11983](https://github.com/rubocop/rubocop/pull/11983): Add Ridgepole files to default `Include` list. ([@ydah][])
* [#11738](https://github.com/rubocop/rubocop/issues/11738): Enhances empty_line_between_defs to treat configured macros like defs. ([@catwomey][])

## 1.53.1 (2023-06-26)

### Bug fixes

* [#11974](https://github.com/rubocop/rubocop/issues/11974): Fix an error for `Style/RedundantCurrentDirectoryInPath` when using string interpolation in `require_relative`. ([@koic][])
* [#11981](https://github.com/rubocop/rubocop/issues/11981): Fix an incorrect autocorrect for `Style/RedundantRegexpArgument` when using double quote and single quote characters. ([@koic][])
* [#11836](https://github.com/rubocop/rubocop/issues/11836): Should not offense single-quoted symbol containing double quotes in `Lint/SymbolConversion` . ([@KessaPassa][])

## 1.53.0 (2023-06-23)

### New features

* [#11561](https://github.com/rubocop/rubocop/pull/11561): Add new `Lint/MixedCaseRange` cop. ([@rwstauner][])
* [#11565](https://github.com/rubocop/rubocop/pull/11565): Add new `Lint/RedundantRegexpQuantifiers` cop. ([@jaynetics][])
* [#11925](https://github.com/rubocop/rubocop/issues/11925): Add new `Style/RedundantCurrentDirectoryInPath` cop. ([@koic][])
* [#11595](https://github.com/rubocop/rubocop/pull/11595): Add new `Style/RedundantRegexpArgument` cop. ([@koic][])
* [#11967](https://github.com/rubocop/rubocop/pull/11967): Add new `Style/ReturnNilInPredicateMethodDefinition` cop. ([@koic][])
* [#11745](https://github.com/rubocop/rubocop/pull/11745): Add new `Style/YAMLFileRead` cop. ([@koic][])
* [#11926](https://github.com/rubocop/rubocop/pull/11926): Support built-in LSP server. ([@koic][])

### Bug fixes

* [#11953](https://github.com/rubocop/rubocop/issues/11953): Fix a false negative for `Lint/DuplicateHashKey` when there is a duplicated constant key in the hash literal. ([@koic][])
* [#11945](https://github.com/rubocop/rubocop/issues/11945): Fix a false negative for `Style/RedundantSelfAssignmentBranch` when using method chaining or arguments in ternary branch. ([@koic][])
* [#11949](https://github.com/rubocop/rubocop/issues/11949): Fix a false positive for `Layout/RedundantLineBreak` when using a line broken string. ([@koic][])
* [#11931](https://github.com/rubocop/rubocop/pull/11931): Fix a false positive for `Lint/RedundantRequireStatement` when using `PP.pp`. ([@koic][])
* [#11946](https://github.com/rubocop/rubocop/pull/11946): Fix an error for `Lint/NumberConversion` when using multiple number conversion methods. ([@koic][])
* [#11972](https://github.com/rubocop/rubocop/issues/11972): Fix an error for `Lint/Void` when `CheckForMethodsWithNoSideEffects: true` and using a method definition. ([@koic][])
* [#11958](https://github.com/rubocop/rubocop/pull/11958): Fix error for `Style/IdenticalConditionalBranches` when using empty parentheses in the `if` branch. ([@koic][])
* [#11962](https://github.com/rubocop/rubocop/issues/11962): Fix an error for `Style/RedundantStringEscape` when an escaped double quote precedes interpolation in a symbol literal. ([@koic][])
* [#11947](https://github.com/rubocop/rubocop/issues/11947): Fix an error for `Style/ConditionalAssignment` with an assignment that uses `if` branch bodies, which include a block. ([@koic][])
* [#11959](https://github.com/rubocop/rubocop/pull/11959): Fix false negatives for `Layout/EmptyLinesAroundExceptionHandlingKeywords` when using Ruby 2.5's `rescue` inside block and Ruby 2.7's numbered block. ([@koic][])
* [#10902](https://github.com/rubocop/rubocop/issues/10902): Fix an error for `Style/RedundantRegexpEscape` string with invalid byte sequence in UTF-8. ([@ydah][])
* [#11562](https://github.com/rubocop/rubocop/pull/11562): Fixed escaped octal handling and detection in `Lint/DuplicateRegexpCharacterClassElement`. ([@rwstauner][])

### Changes

* [#11904](https://github.com/rubocop/rubocop/pull/11904): Mark `Layout/ClassStructure` as unsafe to autocorrect. ([@nevans][])
* [#8506](https://github.com/rubocop/rubocop/issues/8506): Add `AllowedParentClasses` config to `Lint/MissingSuper`. ([@iMacTia][])

## 1.52.1 (2023-06-12)

### Bug fixes

* [#11944](https://github.com/rubocop/rubocop/pull/11944): Fix an incorrect autocorrect for `Style/SoleNestedConditional` with `Style/MethodCallWithArgsParentheses`. ([@koic][])
* [#11930](https://github.com/rubocop/rubocop/pull/11930): Fix exception on `Lint/InheritException` when class definition has non-constant siblings. ([@rafaelfranca][])
* [#11919](https://github.com/rubocop/rubocop/issues/11919): Fix an error for `Lint/UselessAssignment` when a variable is assigned and unreferenced in `for`. ([@koic][])
* [#11928](https://github.com/rubocop/rubocop/pull/11928): Fix an incorrect autocorrect for `Lint/AmbiguousBlockAssociation`. ([@koic][])
* [#11915](https://github.com/rubocop/rubocop/pull/11915): Fix a false positive for `Lint/RedundantSafeNavigation` when `&.` is used for `to_s`, `to_i`, `to_d`, and other coercion methods. ([@lucthev][])

### Changes

* [#11942](https://github.com/rubocop/rubocop/pull/11942): Require Parser 3.2.2.3 or higher. ([@koic][])

## 1.52.0 (2023-06-02)

### New features

* [#11873](https://github.com/rubocop/rubocop/pull/11873): Add `ComparisonsThreshold` config option to `Style/MultipleComparison`. ([@fatkodima][])
* [#11886](https://github.com/rubocop/rubocop/pull/11886): Add new `Style/RedundantArrayConstructor` cop. ([@koic][])
* [#11873](https://github.com/rubocop/rubocop/pull/11873): Add new `Style/RedundantRegexpConstructor` cop. ([@koic][])
* [#11841](https://github.com/rubocop/rubocop/pull/11841): Add new `Style/RedundantFilterChain` cop. ([@fatkodima][])
* [#11908](https://github.com/rubocop/rubocop/issues/11908): Support `AllowedReceivers` for `Style/CollectionMethods`. ([@koic][])

### Bug fixes

* [#11890](https://github.com/rubocop/rubocop/pull/11890): Fix a false negative for `Lint/RedundantSafeNavigation` when `&.` is used for `to_d`. ([@koic][])
* [#11880](https://github.com/rubocop/rubocop/issues/11880): Fix a false positive for `Style/ExactRegexpMatch` when using literal with quantifier in regexp. ([@koic][])
* [#11902](https://github.com/rubocop/rubocop/pull/11902): Fix a false positive for `Style/RequireOrder` when single-quoted string and double-quoted string are mixed. ([@koic][])
* [#11879](https://github.com/rubocop/rubocop/pull/11879): Fix a false positive for `Style/SelectByRegexp` when Ruby 2.2 or lower analysis. ([@koic][])
* [#11891](https://github.com/rubocop/rubocop/issues/11891): Fix `Style/AccessorGrouping` to accept macros separated from accessors by space. ([@fatkodima][])
* [#11905](https://github.com/rubocop/rubocop/issues/11905): Fix an error for `Lint/UselessAssignment` when a variable is assigned with rest assignment and unreferenced. ([@koic][])
* [#11899](https://github.com/rubocop/rubocop/issues/11899): Fix an incorrect autocorrect for `Style/SingleLineMethods` when using Ruby 3.0 and `Style/EndlessMethod` is disabled. ([@koic][])
* [#11884](https://github.com/rubocop/rubocop/issues/11884): Make `rubocop -V` display rubocop-factory_bot version when using it. ([@koic][])
* [#11893](https://github.com/rubocop/rubocop/issues/11893): Fix a false positive for `Lint/InheritException` when inheriting `Exception` with omitted namespace. ([@koic][])
* [#11898](https://github.com/rubocop/rubocop/pull/11898): Fix offences in calls inside blocks with braces for `Style/MethodCallWithArgsParentheses` with `omit_parentheses` enforced style. ([@gsamokovarov][])
* [#11857](https://github.com/rubocop/rubocop/pull/11857): Server mode: only read $stdin when -s or --stdin argument provided. ([@naveg][])

## 1.51.0 (2023-05-13)

### New features

* [#11819](https://github.com/rubocop/rubocop/pull/11819): Add autocorrection for `Lint/AmbiguousBlockAssociation`. ([@r7kamura][])
* [#11597](https://github.com/rubocop/rubocop/issues/11597): Add autocorrection for `Lint/UselessAssignment`. ([@r7kamura][])
* [#11848](https://github.com/rubocop/rubocop/pull/11848): Add autocorrection for `Lint/Void`. ([@r7kamura][])
* [#11851](https://github.com/rubocop/rubocop/pull/11851): Add autocorrection for `Naming/MemoizedInstanceVariableName`. ([@r7kamura][])
* [#11856](https://github.com/rubocop/rubocop/pull/11856): Add autocorrection for `Style/CombinableLoops`. ([@r7kamura][])
* [#11824](https://github.com/rubocop/rubocop/pull/11824): Add autocorrection for `Lint/TopLevelReturnWithArgument`. ([@r7kamura][])
* [#11869](https://github.com/rubocop/rubocop/pull/11869): Add new `Style/ExactRegexpMatch` cop. ([@koic][])
* [#11814](https://github.com/rubocop/rubocop/pull/11814): Make `Style/CollectionCompact` aware of `delete_if`. ([@koic][])
* [#11866](https://github.com/rubocop/rubocop/pull/11866): Make `Style/Semicolon` aware of redundant semicolons in string interpolation braces. ([@koic][])

### Bug fixes

* [#11812](https://github.com/rubocop/rubocop/issues/11812): Fix a false negative for `Style/Attr` when using `attr` and method definitions. ([@koic][])
* [#11861](https://github.com/rubocop/rubocop/issues/11861): Fix a false positive for `Layout/SpaceAfterSemicolon` when no space between a semicolon and a closing brace of string interpolation. ([@koic][])
* [#11830](https://github.com/rubocop/rubocop/pull/11830): Fix a false positive for `Lint/IncompatibleIoSelectWithFiberScheduler`. ([@koic][])
* [#11846](https://github.com/rubocop/rubocop/issues/11846): Fix a false positive for `Lint/RedundantStringCoercion` when using `to_s(argument)` in `puts` argument. ([@koic][])
* [#11865](https://github.com/rubocop/rubocop/pull/11865): Fix an error for `Naming/ConstantName` when assigning a constant from an empty branch of `else`. ([@koic][])
* [#11844](https://github.com/rubocop/rubocop/issues/11844): Fix a false positive for `Style/RedundantLineContinuation` when using line concatenation for assigning a return value and without argument parentheses. ([@koic][])
* [#11808](https://github.com/rubocop/rubocop/pull/11808): Fix a false positive for `Style/RegexpLiteral` when using a regexp starts with equal as a method argument. ([@koic][])
* [#11822](https://github.com/rubocop/rubocop/issues/11822): Fix an error for `Layout/SpaceInsideBlockBraces` when a method call with a multiline block is used as an argument. ([@koic][])
* [#11849](https://github.com/rubocop/rubocop/issues/11849): Fix an error for `Style/ConditionalAssignment` when `EnforcedStyle: assign_inside_condition` and using empty `case` condition. ([@koic][])
* [#11967](https://github.com/rubocop/rubocop/pull/11967): Fix error for `Style/IfInsideElse` when a deep nested multiline `if...then...elsif...else...end`. ([@koic][])
* [#11842](https://github.com/rubocop/rubocop/pull/11842): Fix an error for `Style/IfUnlessModifier` when using multiple `if` modifier in the long one line. ([@koic][])
* [#11835](https://github.com/rubocop/rubocop/pull/11835): Fix an error for `Style/RequireOrder` when multiple `require` are not sorted. ([@koic][])
* [#11809](https://github.com/rubocop/rubocop/issues/11809): Fix an incorrect autocorrect for `Naming/RescuedExceptionsVariableName` when exception variable is referenced after `rescue` statement. ([@koic][])
* [#11852](https://github.com/rubocop/rubocop/issues/11852): Fix an incorrect autocorrect for `Style/EvalWithLocation` when using `eval` without line number and with parenthesized method call. ([@koic][])
* [#11862](https://github.com/rubocop/rubocop/issues/11862): Fix an incorrect autocorrect for `Style/GuardClause` when using `raise` in `else` branch in a one-liner with `then`. ([@koic][])
* [#11868](https://github.com/rubocop/rubocop/issues/11868): Fix a false positive for `Style/HashExcept` when method's receiver/argument is not the same as block key argument. ([@fatkodima][])
* [#11858](https://github.com/rubocop/rubocop/pull/11858): Fix false positives when using source comments in blocks. ([@reitermarkus][])
* [#11510](https://github.com/rubocop/rubocop/pull/11510): Fix `Lint/UselessAssignment` false positive when using numbered block parameters. ([@sambostock][])
* [#11872](https://github.com/rubocop/rubocop/pull/11872): Fix `Gemspec/DevelopmentDependencies` not trigger when add_development_dependency has more then one arguments. ([@Bhacaz][])
* [#11820](https://github.com/rubocop/rubocop/issues/11820): Fix `Lint/EmptyConditionalBody` false-positives for commented empty `elsif` body. ([@r7kamura][])

### Changes

* [#11859](https://github.com/rubocop/rubocop/pull/11859): Add rubocop-factory_bot to suggested extensions. ([@ydah][])
* [#11791](https://github.com/rubocop/rubocop/pull/11791): **(Breaking)** Drop runtime support for Ruby 2.6 and JRuby 9.3 (CRuby 2.6 compatible). ([@koic][])
* [#11826](https://github.com/rubocop/rubocop/pull/11826): Exclude `**/*.jb` from `Lint/TopLevelReturnWithArgument`. ([@r7kamura][])
* [#11871](https://github.com/rubocop/rubocop/pull/11871): Mark `Style/DataInheritance` as unsafe autocorrect, `Style/OpenStructUse` as unsafe, and `Security/CompoundHash` as unsafe. ([@koic][])

## 1.50.2 (2023-04-17)

### Bug fixes

* [#11799](https://github.com/rubocop/rubocop/pull/11799): Fix a false positive for `Style/CollectionCompact` when using `reject` on hash to reject nils in Ruby 2.3 analysis. ([@koic][])
* [#11792](https://github.com/rubocop/rubocop/issues/11792): Fix an error for `Lint/DuplicateMatchPattern` when using hash pattern with `if` guard. ([@koic][])
* [#11800](https://github.com/rubocop/rubocop/issues/11800): Mark `Style/InvertibleUnlessCondition` as unsafe. ([@koic][])

## 1.50.1 (2023-04-12)

### Bug fixes

* [#11787](https://github.com/rubocop/rubocop/issues/11787): Fix a false positive for `Lint/DuplicateMatchPattern` when repeated `in` patterns but different `if` guard is used. ([@koic][])
* [#11789](https://github.com/rubocop/rubocop/pull/11789): Fix false negatives for `Style/ParallelAssignment` when Ruby 2.7+. ([@koic][])
* [#11783](https://github.com/rubocop/rubocop/issues/11783): Fix a false positive for `Style/RedundantLineContinuation` using line concatenation for assigning a return value and without argument parentheses. ([@koic][])

## 1.50.0 (2023-04-11)

### New features

* [#11749](https://github.com/rubocop/rubocop/pull/11749): Add new `Lint/DuplicateMatchPattern` cop. ([@koic][])
* [#11773](https://github.com/rubocop/rubocop/pull/11773): Make `Layout/ClassStructure` aware of singleton class. ([@koic][])
* [#11779](https://github.com/rubocop/rubocop/pull/11779): Make `Lint/RedundantStringCoercion` aware of print method arguments. ([@koic][])
* [#11776](https://github.com/rubocop/rubocop/pull/11776): Make `Metrics/ClassLength` aware of singleton class. ([@koic][])
* [#11775](https://github.com/rubocop/rubocop/pull/11775): Make `Style/TrailingBodyOnClass` aware of singleton class. ([@koic][])

### Bug fixes

* [#11758](https://github.com/rubocop/rubocop/issues/11758): Fix a false positive for `Style/RedundantLineContinuation` when line continuations for string. ([@koic][])
* [#11754](https://github.com/rubocop/rubocop/pull/11754): Fix a false positive for `Style/RedundantLineContinuation` when using `&&` and `||` with a multiline condition. ([@ydah][])
* [#11765](https://github.com/rubocop/rubocop/issues/11765): Fix an error for `Style/MultilineMethodSignature` when line break after `def` keyword. ([@koic][])
* [#11762](https://github.com/rubocop/rubocop/issues/11762): Fix an incorrect autocorrect for `Style/ClassEqualityComparison`  when comparing a variable or return value for equality. ([@koic][])
* [#11752](https://github.com/rubocop/rubocop/pull/11752): Fix a false positive for `Style/RedundantLineContinuation` when using line concatenation and calling a method without parentheses. ([@koic][])

## 1.49.0 (2023-04-03)

### New features

* [#11122](https://github.com/rubocop/rubocop/issues/11122): Add new `Style/RedundantLineContinuation` cop. ([@ydah][])
* [#11696](https://github.com/rubocop/rubocop/issues/11696): Add new `Style/DataInheritance` cop. ([@ktopolski][])
* [#11746](https://github.com/rubocop/rubocop/pull/11746): Make `Layout/EndAlignment` aware of pattern matching. ([@koic][])
* [#11750](https://github.com/rubocop/rubocop/pull/11750): Make `Metrics/BlockNesting` aware of numbered parameter. ([@koic][])
* [#11699](https://github.com/rubocop/rubocop/issues/11699): Make `Style/ClassEqualityComparison` aware of `Class#to_s` and `Class#inspect` for class equality comparison. ([@koic][])
* [#11737](https://github.com/rubocop/rubocop/pull/11737): Make `Style/MapToHash` and `Style/MapToSet` aware of numbered parameters. ([@koic][])
* [#11732](https://github.com/rubocop/rubocop/issues/11732): Make `Style/MapToHash` and `Style/MapToSet` aware of symbol proc. ([@koic][])
* [#11703](https://github.com/rubocop/rubocop/pull/11703): Make `Naming/InclusiveLanguage` support autocorrection when there is only one suggestion. ([@koic][])

### Bug fixes

* [#11730](https://github.com/rubocop/rubocop/issues/11730): Fix an error for `Layout/HashAlignment` when using anonymous keyword rest arguments. ([@koic][])
* [#11704](https://github.com/rubocop/rubocop/issues/11704): Fix a false positive for `Lint/UselessMethodDefinition` when method definition with non access modifier containing only `super` call. ([@koic][])
* [#11723](https://github.com/rubocop/rubocop/issues/11723): Fix a false positive for `Style/IfUnlessModifier` when using one-line pattern matching as a `if` condition. ([@koic][])
* [#11725](https://github.com/rubocop/rubocop/issues/11725): Fix an error when insufficient permissions to server cache dir are granted. ([@koic][])
* [#11715](https://github.com/rubocop/rubocop/issues/11715): Ensure default configuration loads. ([@koic][])
* [#11742](https://github.com/rubocop/rubocop/pull/11742): Fix error handling in bundler standalone mode. ([@composerinteralia][])
* [#11712](https://github.com/rubocop/rubocop/pull/11712): Fix a crash in `Lint/EmptyConditionalBody`. ([@gsamokovarov][])
* [#11641](https://github.com/rubocop/rubocop/issues/11641): Fix a false negative for `Layout/ExtraSpacing` when there are many comments with extra spaces. ([@nobuyo][])
* [#11740](https://github.com/rubocop/rubocop/pull/11740): Fix a false positive for `Lint/NestedMethodDefinition` when nested definition inside `*_eval` and `*_exec` method call with a numblock. ([@ydah][])
* [#11685](https://github.com/rubocop/rubocop/issues/11685): Fix incorrect directive comment insertion when percent array violates `Layout/LineLength` cop. ([@nobuyo][])
* [#11706](https://github.com/rubocop/rubocop/issues/11706): Fix infinite loop when `--disable-uncorrectable` option and there is a multi-line percent array violates `Layout/LineLength`. ([@nobuyo][])
* [#11697](https://github.com/rubocop/rubocop/issues/11697): Fix `Lint/Syntax` behavior when `--only` is not given the cop name. ([@koic][])
* [#11709](https://github.com/rubocop/rubocop/pull/11709): Fix value omission false positive in `Style/MethodCallWithArgsParentheses`. ([@gsamokovarov][])

### Changes

* [#11739](https://github.com/rubocop/rubocop/pull/11739): Make `Style/RedundantParentheses` aware of redundant method argument parentheses. ([@koic][])
* [#10766](https://github.com/rubocop/rubocop/issues/10766): Use the path given by `--cache-root` to be the parent for `rubocop_cache` dir like other ways to specify it. ([@nobuyo][])

## 1.48.1 (2023-03-13)

### Bug fixes

* [#11673](https://github.com/rubocop/rubocop/pull/11673): Fix incorrect `Style/HashSyntax` autocorrection for assignment methods. ([@gsamokovarov][])
* [#11682](https://github.com/rubocop/rubocop/issues/11682): Fix a false positive for `Lint/UselessRescue` when using `Thread#raise` in `rescue` clause. ([@koic][])
* [#11672](https://github.com/rubocop/rubocop/issues/11672): Fix an error for `Layout/BlockEndNewline` when multiline block `}` is not on its own line and it is used as multiple arguments. ([@koic][])
* [#11675](https://github.com/rubocop/rubocop/pull/11675): `Style/AccessorGrouping`: Fix sibling detection for methods with type sigs. ([@issyl0][])
* [#11658](https://github.com/rubocop/rubocop/issues/11658): Fix `Lint/Debugger` should not allow pry. ([@ThHareau][])
* [#11689](https://github.com/rubocop/rubocop/pull/11689): Fix `Lint/Syntax` behavior when `Enabled: false` of `Lint` department. ([@koic][])
* [#11677](https://github.com/rubocop/rubocop/issues/11677): Fix the severity for `Lint/Syntax`. ([@koic][])
* [#11691](https://github.com/rubocop/rubocop/pull/11691): Fix an error for `Gemspec/DependencyVersion` when method called on gem name argument for `add_dependency`. ([@koic][])

## 1.48.0 (2023-03-06)

### New features

* [#11628](https://github.com/rubocop/rubocop/issues/11628): Add new `Style/DirEmpty` cop. ([@ydah][])
* [#11629](https://github.com/rubocop/rubocop/issues/11629): Add new `Style/FileEmpty` cop. ([@ydah][])

### Bug fixes

* [#11654](https://github.com/rubocop/rubocop/pull/11654): Fix a false positive for `Lint/MissingSuper` when no `super` call and when defining some method. ([@koic][])
* [#11661](https://github.com/rubocop/rubocop/pull/11661): Fix an error for `Style/Documentation` when namespace is a variable. ([@koic][])
* [#11647](https://github.com/rubocop/rubocop/pull/11647): Fix an error for `Style/IfWithBooleanLiteralBranches` when using `()` as a condition. ([@koic][])
* [#11646](https://github.com/rubocop/rubocop/pull/11646): Fix an error for `Style/NegatedIfElseCondition` when using `()` as a condition. ([@koic][])
* [#11659](https://github.com/rubocop/rubocop/pull/11659): Fix an incorrect autocorrect for `Lint/OrAssignmentToConstant` when using or-assignment to a constant in method definition. ([@koic][])
* [#11663](https://github.com/rubocop/rubocop/issues/11663): Fix an incorrect autocorrect for `Style/BlockDelimiters` when multi-line blocks to `{` and `}` with arithmetic operation method chain. ([@koic][])
* [#11638](https://github.com/rubocop/rubocop/pull/11638): Fix a false positive for `Lint/UselessAccessModifier` when using same access modifier inside and outside the `included` block. ([@ydah][])
* [#11164](https://github.com/rubocop/rubocop/issues/11164): Suppress server mode message with `-f json`. ([@jasondoc3][])
* [#11643](https://github.com/rubocop/rubocop/pull/11643): Fix incorrect shorthand autocorrections in calls inside parentheses. ([@gsamokovarov][])
* [#11650](https://github.com/rubocop/rubocop/pull/11650): `Style/AccessorGrouping`: Fix detection of Sorbet `sig {}` blocks. ([@issyl0][])
* [#11657](https://github.com/rubocop/rubocop/issues/11657): Use cop name to check if cop inside registry is enabled. Previously, it was able to cause large memory usage during linting. ([@fatkodima][])

### Changes

* [#11482](https://github.com/rubocop/rubocop/issues/11482): Avoid comment deletion by `Style/IfUnlessModifier` when the modifier form expression has long comment. ([@nobuyo][])
* [#11649](https://github.com/rubocop/rubocop/issues/11649): Support `MinBranchesCount` config for `Style/CaseLikeIf` cop. ([@fatkodima][])

## 1.47.0 (2023-03-01)

### New features

* [#11475](https://github.com/rubocop/rubocop/pull/11475): Add autocorrect for hash in `Lint/LiteralInInterpolation`. ([@KessaPassa][])
* [#11584](https://github.com/rubocop/rubocop/pull/11584): Add `Metrics/CollectionLiteralLength` cop. ([@sambostock][])

### Bug fixes

* [#11615](https://github.com/rubocop/rubocop/issues/11615): Fix a false negative for `Lint/MissingSuper` when no `super` call with `Class.new` block. ([@koic][])
* [#11615](https://github.com/rubocop/rubocop/issues/11615): Fix a false negative for `Lint/MissingSuper` when using `Class.new` without parent class argument. ([@koic][])
* [#11040](https://github.com/rubocop/rubocop/issues/11040): Fix a false positive for `Style/IfUnlessModifier` when `defined?`'s argument value is undefined. ([@koic][])
* [#11607](https://github.com/rubocop/rubocop/issues/11607): Fix a false positive for `Style/RedundantRegexpEscape` when an escaped hyphen follows after an escaped opening square bracket within a character class. ([@SparLaimor][])
* [#11626](https://github.com/rubocop/rubocop/issues/11626): Fix a false positive for `Style/ZeroLengthPredicate` when using `File.new(path).size.zero?`. ([@koic][])
* [#11620](https://github.com/rubocop/rubocop/pull/11620): Fix an error for `Lint/ConstantResolution` when using `__ENCODING__`. ([@koic][])
* [#11625](https://github.com/rubocop/rubocop/pull/11625): Fix an error for `Lint/EmptyConditionalBody` when missing `if` body and using method call for return value. ([@koic][])
* [#11631](https://github.com/rubocop/rubocop/issues/11631): Fix an incorrect autocorrect for `Style/ArgumentsForwarding` when using arguments forwarding for `.()` call. ([@koic][])
* [#11621](https://github.com/rubocop/rubocop/issues/11621): Fix an incorrect autocorrect for `Layout/ClassStructure` using heredoc inside method. ([@fatkodima][])
* [#3591](https://github.com/rubocop/rubocop/issues/3591): Handle modifier `while` and `until` expressions in `Lint/UselessAssignment`. ([@bfad][])
* [#11202](https://github.com/rubocop/rubocop/issues/11202): Fixed usage of `--only` flag with `--auto-gen-config`. ([@istvanfazakas][])

### Changes

* [#11623](https://github.com/rubocop/rubocop/pull/11623): Add rubocop-capybara to suggested extensions and extension doc. ([@ydah][])

## 1.46.0 (2023-02-22)

### New features

* [#11569](https://github.com/rubocop/rubocop/pull/11569): Support `TargetRubyVersion 3.3` (experimental). ([@koic][])

### Bug fixes

* [#11574](https://github.com/rubocop/rubocop/pull/11574): Fix a broken shorthand syntax autocorrection. ([@gsamokovarov][])
* [#11599](https://github.com/rubocop/rubocop/pull/11599): Fix a false positive for `Layout/LineContinuationSpacing` when using percent literals. ([@koic][])
* [#11556](https://github.com/rubocop/rubocop/issues/11556): Fix a false positive for `Lint/Debugger` when `p` is an argument of method call. ([@koic][])
* [#11591](https://github.com/rubocop/rubocop/issues/11591): Fix a false positive for `Lint/ToEnumArguments` when enumerator is not created for `__callee__` and `__callee__` methods. ([@koic][])
* [#11603](https://github.com/rubocop/rubocop/pull/11603): Actually run temporarily enabled cops. ([@tdeo][])
* [#11579](https://github.com/rubocop/rubocop/pull/11579): Fix an error for `Layout/HeredocArgumentClosingParenthesis` when heredoc is a method argument in a parenthesized block argument. ([@koic][])
* [#11576](https://github.com/rubocop/rubocop/pull/11576): Fix an error for `Lint/UselessRescue` when `rescue` does not exception variable and `ensure` has empty body. ([@koic][])
* [#11608](https://github.com/rubocop/rubocop/pull/11608): Fix an error for `Lint/RefinementImportMethods` when using `include` on the top level. ([@koic][])
* [#11589](https://github.com/rubocop/rubocop/pull/11589): Fix an error for `Layout/HeredocArgumentClosingParenthesis` when heredoc is a branch body in a method argument of a parenthesized argument. ([@koic][])
* [#11567](https://github.com/rubocop/rubocop/issues/11567): Fix `Layout/EndAlignment` false negative. ([@j-miyake][])
* [#11582](https://github.com/rubocop/rubocop/issues/11582): Fix checking if token with large offset begins its line. ([@fatkodima][])
* [#11412](https://github.com/rubocop/rubocop/issues/11412): Mark `Style/ArrayIntersect` as unsafe. ([@koic][])
* [#11559](https://github.com/rubocop/rubocop/pull/11559): Fixed false positives and negatives in `Style/RedundantRegexpCharacterClass` when using octal escapes (e.g. "\0"). ([@jaynetics][])
* [#11575](https://github.com/rubocop/rubocop/pull/11575): Fix parentheses in value omissions for multiple assignments. ([@gsamokovarov][])

### Changes

* [#11586](https://github.com/rubocop/rubocop/issues/11586): Handle `ruby2_keywords` in `Style/DocumentationMethod` cop. ([@fatkodima][])
* [#11604](https://github.com/rubocop/rubocop/issues/11604): Make `Naming/VariableNumber` to allow `x86_64` CPU architecture name by default. ([@koic][])
* [#11596](https://github.com/rubocop/rubocop/issues/11596): Make `Style/AccessorGrouping` aware of method call before accessor. ([@koic][])
* [#11588](https://github.com/rubocop/rubocop/pull/11588): Optimize `Style/WordArray` complex matrix check. ([@sambostock][])
* [#11573](https://github.com/rubocop/rubocop/pull/11573): Handle hash patterns and pins in `Lint/OutOfRangeRegexpRef` cop. ([@fatkodima][])
* [#11564](https://github.com/rubocop/rubocop/pull/11564): Remove print debug methods from default for `Lint/Debugger`. ([@koic][])

## 1.45.1 (2023-02-08)

### Bug fixes

* [#11552](https://github.com/rubocop/rubocop/pull/11552): Fix a false positive for `Lint/Debugger` when methods containing different method chains. ([@ydah][])
* [#11548](https://github.com/rubocop/rubocop/pull/11548): Fix an error for `Style/AccessModifierDeclarations` when if a non method definition was included. ([@ydah][])
* [#11554](https://github.com/rubocop/rubocop/issues/11554): Fix an error for `Style/RedundantCondition` when the branches contains empty hash literal argument. ([@koic][])
* [#11549](https://github.com/rubocop/rubocop/issues/11549): Fix an error for third party cops when inheriting `RuboCop::Cop::Cop`. ([@koic][])

## 1.45.0 (2023-02-08)

### New features

* [#10839](https://github.com/rubocop/rubocop/pull/10839): Add API for 3rd party template support. ([@r7kamura][])
* [#11528](https://github.com/rubocop/rubocop/pull/11528): Add new `Style/RedundantHeredocDelimiterQuotes` cop. ([@koic][])
* [#11188](https://github.com/rubocop/rubocop/issues/11188): Add a `--no-detach` option for `--start-server`. This will start the server process in the foreground, which can be helpful when running within Docker where detaching the process terminates the container. ([@f1sherman][])
* [#11546](https://github.com/rubocop/rubocop/pull/11546): Make `Lint/UselessAccessModifier` aware of Ruby 3.2's `Data.define`. ([@koic][])
* [#11396](https://github.com/rubocop/rubocop/pull/11396): Add ability to profile rubocop execution via `--profile` and `--memory` options. ([@fatkodima][])

### Bug fixes

* [#11491](https://github.com/rubocop/rubocop/pull/11491): Fix a crash on `Lint/UselessAssignment`. ([@gsamokovarov][])
* [#11515](https://github.com/rubocop/rubocop/pull/11515): Fix a false negative for `Naming/HeredocDelimiterNaming` when using lowercase. ([@koic][])
* [#11511](https://github.com/rubocop/rubocop/issues/11511): Fix a false negative for `Style/YodaCondition` when using constant. ([@koic][])
* [#11520](https://github.com/rubocop/rubocop/pull/11520): Fix a false negative for `Style/YodaExpression` when using constant. ([@koic][])
* [#11521](https://github.com/rubocop/rubocop/issues/11521): Fix a false positive for `Lint/FormatParameterMismatch` when using `Kernel.format` with the interpolated number of decimal places fields match. ([@koic][])
* [#11545](https://github.com/rubocop/rubocop/pull/11545): Fix the following false positive for `Lint/NestedMethodDefinition` when using numbered parameter. ([@koic][])
* [#11535](https://github.com/rubocop/rubocop/issues/11535): Fix a false positive for `Style/NumberedParametersLimit` when only `_2` or higher numbered parameter is used. ([@koic][])
* [#11508](https://github.com/rubocop/rubocop/issues/11508): Fix a false positive for `Style/OperatorMethodCall` when using multiple arguments for operator method. ([@koic][])
* [#11503](https://github.com/rubocop/rubocop/issues/11503): Fix a false positive for `Style/RedundantCondition` when using method argument with operator. ([@koic][])
* [#11529](https://github.com/rubocop/rubocop/pull/11529): Fix an incorrect autocorrect for `Layout/ClassStructure` when definitions that need to be sorted are defined alternately. ([@ydah][])
* [#11530](https://github.com/rubocop/rubocop/pull/11530): Fix an incorrect autocorrect for `Style/AccessModifierDeclarations` when multiple groupable access modifiers are defined. ([@ydah][])
* [#10910](https://github.com/rubocop/rubocop/pull/10910): Fix an incorrect autocorrect for `Style/MultilineTernaryOperator`  when contains a comment. ([@ydah][])
* [#11522](https://github.com/rubocop/rubocop/pull/11522): Don't flag default keyword arguments in `Style/ArgumentsForwarding`. ([@splattael][])
* [#11547](https://github.com/rubocop/rubocop/pull/11547): Fix a false positive for `Lint/NestedMethodDefinition` when using Ruby 3.2's `Data.define`. ([@koic][])
* [#11537](https://github.com/rubocop/rubocop/pull/11537): Fix an infinite loop error for `Layout/ArrayAlignment` when using assigning unbracketed array elements. ([@koic][])
* [#11516](https://github.com/rubocop/rubocop/pull/11516): Fix missing parentheses in shorthand hash syntax as argument calls. ([@gsamokovarov][])

### Changes

* [#11504](https://github.com/rubocop/rubocop/issues/11504): Allow `initialize` method in `Style/DocumentationMethod`. ([@koic][])
* [#11541](https://github.com/rubocop/rubocop/pull/11541): Enable autocorrection for `Layout/LineContinuationLeadingSpace`. ([@eugeneius][])
* [#11542](https://github.com/rubocop/rubocop/pull/11542): Mark `Layout/AssignmentIndentation` as safe and `Lint/AssignmentInCondition` as unsafe for autocorrection. ([@eugeneius][])
* [#11517](https://github.com/rubocop/rubocop/issues/11517): Make `Lint/Debugger` aware of `p`, `PP.pp`, and `pp` methods. ([@koic][])
* [#11539](https://github.com/rubocop/rubocop/pull/11539): Remove `bundler` from default `AllowedGems` of `Gemspec/DevelopmentDependencies`. ([@koic][])

## 1.44.1 (2023-01-25)

### Bug fixes

* [#11492](https://github.com/rubocop/rubocop/issues/11492): Fix an error for `Lint/Void` when configuring `CheckForMethodsWithNoSideEffects: true`. ([@koic][])
* [#11400](https://github.com/rubocop/rubocop/issues/11400): Fix an incorrect autocorrect for `Naming/BlockForwarding` and `Lint/AmbiguousOperator` when autocorrection conflicts for ambiguous splat argument. ([@fatkodima][])
* [#11483](https://github.com/rubocop/rubocop/issues/11483): Fix `Layout/ClosingParenthesisIndentation` for keyword splat arguments. ([@fatkodima][])
* [#11487](https://github.com/rubocop/rubocop/pull/11487): Fix a false positive for `Lint/FormatParameterMismatch` when format string is only interpolated string. ([@ydah][])
* [#11485](https://github.com/rubocop/rubocop/issues/11485): Fix a false positive for `Lint/UselessAssignment` when using numbered block parameter. ([@koic][])

## 1.44.0 (2023-01-23)

### New features

* [#11410](https://github.com/rubocop/rubocop/issues/11410): Add new `Style/InvertibleUnlessCondition` cop. ([@fatkodima][])
* [#11338](https://github.com/rubocop/rubocop/issues/11338): Add new `Style/ComparableClamp` cop. ([@koic][])
* [#11350](https://github.com/rubocop/rubocop/issues/11350): Make `Lint/DeprecatedClassMethods` aware of deprecated `attr` with boolean 2nd argument. ([@koic][])
* [#11457](https://github.com/rubocop/rubocop/pull/11457): Make `Metrics/BlockNesting` aware of pattern matching. ([@koic][])
* [#11458](https://github.com/rubocop/rubocop/pull/11458): Make `Metrics/CyclomaticComplexity` aware of pattern matching. ([@koic][])
* [#11469](https://github.com/rubocop/rubocop/pull/11469): Add `Gemspec/DevelopmentDependencies` cop. ([@sambostock][])

### Bug fixes

* [#11445](https://github.com/rubocop/rubocop/issues/11445): Fix an incorrect autocorrect for `Style/BlockDelimiters` when there is a comment after the closing brace and bracket. ([@koic][])
* [#11428](https://github.com/rubocop/rubocop/pull/11428): Apply value omission exceptions in super invocations. ([@gsamokovarov][])
* [#11420](https://github.com/rubocop/rubocop/issues/11420): Fix a false positive for `Lint/UselessRescue`  when using exception variable in `ensure` clause. ([@koic][])
* [#11460](https://github.com/rubocop/rubocop/issues/11460): Fix an error for `Style/OperatorMethodCall` when using `foo.> 42`. ([@koic][])
* [#11456](https://github.com/rubocop/rubocop/pull/11456): Fix value omissions in `yield` invocations. ([@gsamokovarov][])
* [#11467](https://github.com/rubocop/rubocop/issues/11467): Fix a false negative for `Style/MethodCallWithoutArgsParentheses` when calling method on a receiver and assigning to a variable with the same name. ([@koic][])
* [#11430](https://github.com/rubocop/rubocop/issues/11430): Fix an infinite loop error for `Layout/BlockEndNewline` when multiline blocks with newlines before the `; end`. ([@koic][])
* [#11442](https://github.com/rubocop/rubocop/pull/11442): Fix a crash during anonymous rest argument forwarding. ([@gsamokovarov][])
* [#11447](https://github.com/rubocop/rubocop/pull/11447): Fix an incorrect autocorrect for `Style/RedundantDoubleSplatHashBraces` when using nested double splat hash braces. ([@koic][])
* [#11459](https://github.com/rubocop/rubocop/pull/11459): Make `Lint/UselessRuby2Keywords` aware of conditions. ([@splattael][])
* [#11415](https://github.com/rubocop/rubocop/issues/11415): Fix a false positive for `Lint/UselessMethodDefinition` when method definition contains rest arguments. ([@koic][])
* [#11418](https://github.com/rubocop/rubocop/issues/11418): Fix a false positive for `Style/MethodCallWithArgsParentheses` when using anonymous rest arguments or anonymous keyword rest arguments. ([@koic][])
* [#11431](https://github.com/rubocop/rubocop/pull/11431): Fix a crash in `Style/HashSyntax`. ([@gsamokovarov][])
* [#11444](https://github.com/rubocop/rubocop/issues/11444): Fix a false positive for `Lint/ShadowingOuterLocalVariable` when using numbered block parameter. ([@koic][])
* [#11477](https://github.com/rubocop/rubocop/issues/11477): Fix an error when using YAML alias with server mode. ([@koic][])
* [#11419](https://github.com/rubocop/rubocop/issues/11419): Fix a false positive for `Lint/RedundantRequireStatement` when using `pretty_inspect`. ([@koic][])
* [#11439](https://github.com/rubocop/rubocop/issues/11439): Fix an incorrect autocorrect for `Style/MinMaxComparison` when using `a < b a : b` with `elsif/else`. ([@ydah][])
* [#11464](https://github.com/rubocop/rubocop/pull/11464): Fix a false negative for `Lint/FormatParameterMismatch` when include interpolated string. ([@ydah][])
* [#11425](https://github.com/rubocop/rubocop/pull/11425): Fix a false negative for `Lint/Void` when using methods that takes blocks. ([@krishanbhasin-shopify][])
* [#11437](https://github.com/rubocop/rubocop/pull/11437): Fix an error for `Style/AccessModifierDeclarations` when access modifier is inlined with a method on the top level. ([@koic][])
* [#11455](https://github.com/rubocop/rubocop/pull/11455): Fix crash with `super value_omission:` followed by a method call. ([@gsamokovarov][])

### Changes

* [#11465](https://github.com/rubocop/rubocop/pull/11465): Make `Style/Semicolon` aware of redundant semicolon in block. ([@koic][])
* [#11471](https://github.com/rubocop/rubocop/pull/11471): Change to not output not configured warning when renamed and pending cop. ([@ydah][])

## 1.43.0 (2023-01-10)

### New features

* [#11359](https://github.com/rubocop/rubocop/issues/11359): Add new `Lint/UselessRescue` cop. ([@fatkodima][])
* [#11389](https://github.com/rubocop/rubocop/pull/11389): Add autocorrect for `Style/MissingElse`. ([@FnControlOption][])

### Bug fixes

* [#11386](https://github.com/rubocop/rubocop/pull/11386): Fix a false positive for `Style/OperatorMethodCall` when using anonymous forwarding. ([@koic][])
* [#11409](https://github.com/rubocop/rubocop/issues/11409): Fix an incorrect autocorrect for `Style/HashSyntax` when using hash value omission and `EnforcedStyle: no_mixed_keys`. ([@koic][])
* [#11405](https://github.com/rubocop/rubocop/issues/11405): Fix undefined method `range_between' for `Style/WhileUntilModifier`. ([@such][])
* [#11374](https://github.com/rubocop/rubocop/pull/11374): Fix an error for `Style/StringHashKeys` when using invalid symbol in encoding UTF-8 as keys. ([@koic][])
* [#11392](https://github.com/rubocop/rubocop/pull/11392): Fix an incorrect autocorrect for `Style/RedundantDoubleSplatHashBraces` using double splat in double splat hash braces. ([@koic][])
* [#8990](https://github.com/rubocop/rubocop/issues/8990): Make `Style/HashEachMethods` aware of built-in `Thread.current`. ([@koic][])
* [#11390](https://github.com/rubocop/rubocop/issues/11390): Fix an incorrect autocorrect for `Style/HashSyntax` when hash first argument key and hash value only are the same which has a method call on the next line. ([@koic][])
* [#11379](https://github.com/rubocop/rubocop/pull/11379): Fix a false negative for `Style/OperatorMethodCall` when using `a.+ b.something`. ([@koic][])
* [#11180](https://github.com/rubocop/rubocop/issues/11180): Fix an error for `Style/RedundantRegexpEscape` when using `%r` to provide regexp expressions. ([@si-lens][])
* [#11403](https://github.com/rubocop/rubocop/pull/11403): Fix bad offense for parenthesised calls in literals for `omit_parentheses` style in `Style/MethodCallWithArgsParentheses`. ([@gsamokovarov][])
* [#11407](https://github.com/rubocop/rubocop/pull/11407): Fix an error for `Style/HashSyntax` when expression follows hash key assignment. ([@fatkodima][])
* [#11377](https://github.com/rubocop/rubocop/issues/11377): Fix `Style/OperatorMethodCall` when forwarding arguments. ([@sambostock][])

### Changes

* [#11382](https://github.com/rubocop/rubocop/pull/11382): Require `unicode-display_width` 2.4.0 or higher. ([@fatkodima][])
* [#11381](https://github.com/rubocop/rubocop/pull/11381): Require Parser 3.2.0.0 or higher. ([@koic][])
* [#11380](https://github.com/rubocop/rubocop/pull/11380): Disable `Style/YodaExpression` by default. ([@koic][])
* [#11303](https://github.com/rubocop/rubocop/issues/11303): Make `Metrics/ParameterLists` aware of `Struct.new` and `Data.define` blocks. ([@koic][])

## 1.42.0 (2023-01-01)

### New features

* [#11339](https://github.com/rubocop/rubocop/issues/11339): Add new `Style/MapToSet` cop. ([@koic][])
* [#11341](https://github.com/rubocop/rubocop/pull/11341): Add new `Style/MinMaxComparison` cop. ([@koic][])
* [#9222](https://github.com/rubocop/rubocop/issues/9222): Add new `Style/YodaExpression` cop. ([@fatkodima][])
* [#11261](https://github.com/rubocop/rubocop/pull/11261): Allow inherit_from to accept a glob. ([@alexevanczuk][])

### Bug fixes

* [#11204](https://github.com/rubocop/rubocop/issues/11204): Fix a false negative for `Lint/RedundantCopDisableDirective` when using `--except` command line option. ([@koic][])
* [#11369](https://github.com/rubocop/rubocop/pull/11369): Fix an error for `Lint/UselessRuby2Keywords` when using `Proc#ruby2_keywords`. ([@koic][])
* [#11351](https://github.com/rubocop/rubocop/pull/11351): Fix an incorrect autocorrect for `Lint/RegexpAsCondition` when using regexp literal with bang. ([@koic][])
* [#11329](https://github.com/rubocop/rubocop/pull/11329): Accept simple freezed constants in `Layout/ClassStructure` and correctly handle class methods. ([@fatkodima][])
* [#11344](https://github.com/rubocop/rubocop/pull/11344): Fix an error for `Style/GuardClause` when using heredoc as an argument of raise in `then` branch and it does not have `else` branch. ([@koic][])
* [#11335](https://github.com/rubocop/rubocop/pull/11335): Fix an error for `Style/RequireOrder` when only one `require`. ([@koic][])
* [#11348](https://github.com/rubocop/rubocop/pull/11348): Fix an error for `Style/SelectByRegexp` when block body is empty. ([@koic][])
* [#11320](https://github.com/rubocop/rubocop/issues/11320): Fix a false positive for `Lint/RequireParentheses` when assigning ternary operator. ([@koic][])
* [#11361](https://github.com/rubocop/rubocop/issues/11361): Make `Style/MethodDefParentheses` aware of Ruby 3.2's anonymous rest and keyword rest arguments. ([@koic][])
* [#11346](https://github.com/rubocop/rubocop/issues/11346): Fix a false positive for `Style/RedundantStringEscape` when using escaped space in heredoc. ([@koic][])
* [#10858](https://github.com/rubocop/rubocop/issues/10858): Fix `Style/IdenticalConditionalBranches` to ignore identical leading lines when branch has single child and is used in return context. ([@fatkodima][])
* [#11237](https://github.com/rubocop/rubocop/issues/11237): Fix `Layout/CommentIndentation` comment aligned with access modifier indentation when EnforcedStyle is outdent. ([@soroktree][])
* [#11330](https://github.com/rubocop/rubocop/pull/11330): Fix an error for `Style/RequireOrder` when using `require` inside `rescue` body. ([@fatkodima][])
* [#8751](https://github.com/rubocop/rubocop/issues/8751): Accept `super` within ranges for `Layout/SpaceAroundKeyword` cop. ([@fatkodima][])
* [#10194](https://github.com/rubocop/rubocop/issues/10194): Accept bracketed arrays within 2d arrays containing subarrays with complex content for `Style/WordArray` cop. ([@fatkodima][])

### Changes

* [#8366](https://github.com/rubocop/rubocop/issues/8366): Ignore private constants in `Layout/ClassStructure` cop. ([@fatkodima][])
* [#11325](https://github.com/rubocop/rubocop/issues/11325): Support autocorrection for percent literals in `Style/ConcatArrayLiterals`. ([@fatkodima][])
* [#11327](https://github.com/rubocop/rubocop/pull/11327): Make `Style/ZeroLengthPredicate` aware of `array.length.zero?`. ([@koic][])
* [#10976](https://github.com/rubocop/rubocop/issues/10976): Support pattern matching for `Lint/OutOfRangeRegexpRef` cop. ([@fatkodima][])

## 1.41.1 (2022-12-22)

### Bug fixes

* [#11293](https://github.com/rubocop/rubocop/issues/11293): Fix a false negative for `Style/Documentation` when using macro. ([@koic][])
* [#11313](https://github.com/rubocop/rubocop/issues/11313): Fix a false positive for `Naming/BlockForwarding` when the block argument is reassigned. ([@fatkodima][])
* [#11014](https://github.com/rubocop/rubocop/pull/11014): Fix a false positive for `Style/Alias`cop when alias in a method def. ([@ydah][])
* [#11309](https://github.com/rubocop/rubocop/issues/11309): Fix a false positive for `Style/RedundantStringEscape` when using a redundant escaped string interpolation `\#\{foo}`. ([@koic][])
* [#11307](https://github.com/rubocop/rubocop/pull/11307): Fix an error for `Style/GuardClause` when using lvar as an argument of raise in `else` branch. ([@ydah][])
* [#11308](https://github.com/rubocop/rubocop/issues/11308): Fix disabling departments via comment. ([@fatkodima][])

### Changes

* [#11312](https://github.com/rubocop/rubocop/issues/11312): Mark `Style/ConcatArrayLiterals` as unsafe. ([@koic][])

## 1.41.0 (2022-12-20)

### New features

* [#11305](https://github.com/rubocop/rubocop/pull/11305): Add new `Style/RedundantDoubleSplatHashBraces` cop. ([@koic][])
* [#10812](https://github.com/rubocop/rubocop/pull/10812): New AllowMultilineFinalElement option for all LineBreaks cops. ([@Korri][])
* [#11277](https://github.com/rubocop/rubocop/issues/11277): Add new `Style/ConcatArrayLiterals` cop. ([@koic][])

### Bug fixes

* [#11255](https://github.com/rubocop/rubocop/pull/11255): Fix an error for `Style/RequireOrder` when `require` with no arguments is put between `require`. ([@ydah][])
* [#11273](https://github.com/rubocop/rubocop/issues/11273): Fix a false positive for `Lint/DuplicateMethods` when there are same `alias_method` name outside `rescue` or `ensure` scopes. ([@koic][])
* [#11267](https://github.com/rubocop/rubocop/issues/11267): Fix an error for `Style/RequireOrder` when modifier conditional is used between `require`. ([@ydah][])
* [#11254](https://github.com/rubocop/rubocop/pull/11254): Fix an error for `Style/RequireOrder` when `require` is a method argument. ([@koic][])
* [#11266](https://github.com/rubocop/rubocop/issues/11266): Fix a false positive for `Style/RedundantConstantBase` when enabling `Lint/ConstantResolution`. ([@koic][])
* [#11296](https://github.com/rubocop/rubocop/pull/11296): Fix an error for `Lint/NonAtomicFileOperation` when use file existence checks line break `unless` by postfix before creating file. ([@koic][])
* [#11284](https://github.com/rubocop/rubocop/issues/11284): Fix an incorrect autocorrect for `Style/WordArray` when assigning `%w()` array. ([@koic][])
* [#11299](https://github.com/rubocop/rubocop/pull/11299): Fix `base_dir` in `TargetFinder#find_files()`. ([@dukaev][])
* [#11250](https://github.com/rubocop/rubocop/pull/11250): Fix an error for `Style/GuardClause` when a method call whose last argument is not a string is in the condition body. ([@ydah][])
* [#11298](https://github.com/rubocop/rubocop/issues/11298): Fix `Lint/SafeNavigationChain` to correctly handle `[]` operator followed by save navigation and method chain. ([@fatkodima][])
* [#11256](https://github.com/rubocop/rubocop/issues/11256): Fix an incorrect autocorrect for `Style/HashSyntax` when without parentheses call expr follows after multiple keyword arguments method call. ([@koic][])
* [#11289](https://github.com/rubocop/rubocop/pull/11289): Correctly detect Rails version when using only parts of the framework, instead of the "rails" gem. ([@bdewater][])
* [#11262](https://github.com/rubocop/rubocop/pull/11262): Fix an error for `Style/IfUnlessModifier` when the body is a method call with hash splat. ([@fatkodima][])
* [#11281](https://github.com/rubocop/rubocop/pull/11281): Fix `NoMethodError` for `Style/Documentation` when a class nested under non-constant values. ([@arika][])

### Changes

* [#11306](https://github.com/rubocop/rubocop/pull/11306): Make `Style/IfWithSemicolon` aware of one line without `else` body. ([@koic][])

## 1.40.0 (2022-12-08)

### New features

* [#11179](https://github.com/rubocop/rubocop/pull/11179): Add `Style/RedundantConstantBase` cop. ([@r7kamura][])
* [#11205](https://github.com/rubocop/rubocop/pull/11205): Add `--[no-]auto-gen-enforced-style` CLI option. ([@ydah][])
* [#11235](https://github.com/rubocop/rubocop/pull/11235): Add `Style/RequireOrder` cop. ([@r7kamura][])
* [#11219](https://github.com/rubocop/rubocop/issues/11219): Make `Style/SelectByRegexp` aware of `!~` method. ([@koic][])
* [#11224](https://github.com/rubocop/rubocop/pull/11224): Add new cop `Style/ArrayIntersect` which replaces `(array1 & array2).any?` with `array1.intersect?(array2)`, method `Array#intersect?` was added in ruby 3.1. ([@KirIgor][])
* [#11211](https://github.com/rubocop/rubocop/pull/11211): Add autocorrect for `Lint/AssignmentInCondition`. ([@r7kamura][])

### Bug fixes

* [#5251](https://github.com/rubocop/rubocop/issues/5251): Fix loading of configuration in multi-file edge case. ([@NobodysNightmare][])
* [#11192](https://github.com/rubocop/rubocop/issues/11192): Fix a false positive for `Lint/ParenthesesAsGroupedExpression` when using a block argument. ([@ydah][])
* [#11143](https://github.com/rubocop/rubocop/issues/11143): Fix RedundantCopDisableDirective errors when encountering several department comments. ([@isarcasm][])
* [#11230](https://github.com/rubocop/rubocop/issues/11230): Fix an incorrect autocorrect for `Lint/SafeNavigationChain` when using safe navigation with `[]` operator followed by method chain. ([@koic][])
* [#11181](https://github.com/rubocop/rubocop/pull/11181): Fix pattern to match .tool-versions files that specify multiple runtimes. ([@noelblaschke][])
* [#11239](https://github.com/rubocop/rubocop/issues/11239): Fix an incorrect autocorrect for `Style/GuardClause` when using heredoc as an argument of raise in branch body. ([@koic][])
* [#11182](https://github.com/rubocop/rubocop/issues/11182): Fix an incorrect autocorrect for `EnforcedShorthandSyntax: always` of `Style/HashSyntax` with `Style/IfUnlessModifier` when using Ruby 3.1. ([@koic][])
* [#11184](https://github.com/rubocop/rubocop/issues/11184): Fix an error for `Lint/ShadowingOuterLocalVariable` when a block local variable has same name as an outer `until` scope variable. ([@koic][])
* [#11198](https://github.com/rubocop/rubocop/pull/11198): Fix an error for `Lint/EmptyConditionalBody` when one using line if/;/end without then body. ([@koic][])
* [#11196](https://github.com/rubocop/rubocop/issues/11196): Fix a false positive for `Style/GuardClause` when using `raise` in `then` body of `if..elsif..end` form. ([@koic][])
* [#11213](https://github.com/rubocop/rubocop/pull/11213): Support redundant department disable in scope of `Lint/RedundantCopDisableDirective` cop. ([@isarcasm][])
* [#11200](https://github.com/rubocop/rubocop/issues/11200): Fix an incorrect autocorrect for `Layout/MultilineMethodCallBraceLayout` when using method chain for heredoc argument in multiline literal brace layout. ([@koic][])
* [#11190](https://github.com/rubocop/rubocop/pull/11190): Fix an error for `Style/IfWithSemicolon` when using one line if/;/end without then body. ([@koic][])
* [#11244](https://github.com/rubocop/rubocop/pull/11244): Fix a false negative for `Style/RedundantReturn` when dynamic define methods. ([@ydah][])

### Changes

* [#11218](https://github.com/rubocop/rubocop/pull/11218): Update severity of `Bundler/DuplicatedGem`, `Bundler/InsecureProtocolSource`, `Gemspec/DeprecatedAttributeAssignment`, `Gemspec/DuplicatedAssignment`, `Gemspec/RequireMFA`, `Gemspec/RequiredRubyVersion`, and `Gemspec/RubyVersionGlobalsUsage` cops to warning. ([@koic][])
* [#11222](https://github.com/rubocop/rubocop/pull/11222): Make `Style/RedundantArgument` aware of `Array#sum`. ([@koic][])
* [#11070](https://github.com/rubocop/rubocop/issues/11070): Add ability to count method calls as one line to code length related `Metric` cops. ([@fatkodima][])
* [#11226](https://github.com/rubocop/rubocop/pull/11226): Make `Lint/Void` aware of used lambda and proc in void context. ([@koic][])
* [#11206](https://github.com/rubocop/rubocop/pull/11206): Change `Lint/InterpolationCheck` from `Safe: false` to `SafeAutoCorrect: false`. ([@r7kamura][])
* [#11212](https://github.com/rubocop/rubocop/issues/11212): Make `Lint/DeprecatedConstants` aware of deprecated `Struct::Group` and `Struct::Passwd` classes. ([@koic][])
* [#11236](https://github.com/rubocop/rubocop/pull/11236): Remove `respond_to` from default value of `AllowedMethods` for `Style/SymbolProc`. ([@koic][])
* [#11185](https://github.com/rubocop/rubocop/pull/11185): Make `Style/HashSyntax` aware of without parentheses call expr follows. ([@koic][])
* [#11203](https://github.com/rubocop/rubocop/pull/11203): Support multiple arguments on `Lint/SendWithMixinArgument`. ([@r7kamura][])
* [#11229](https://github.com/rubocop/rubocop/pull/11229): Add `cc` to `AllowedNames` of `MethodParameterName` cop. ([@tjschuck][])
* [#11116](https://github.com/rubocop/rubocop/issues/11116): Handle ternaries in `Style/SafeNavigation`. ([@fatkodima][])

## 1.39.0 (2022-11-14)

### New features

* [#11091](https://github.com/rubocop/rubocop/pull/11091): Add autocorrect for `Layout/LineContinuationLeadingSpace`. ([@FnControlOption][])

### Bug fixes

* [#11150](https://github.com/rubocop/rubocop/issues/11150): Improve `Style/RedundantRegexpEscape` to catch unnecessarily escaped hyphens within a character class. ([@si-lens][])
* [#11168](https://github.com/rubocop/rubocop/issues/11168): Fix an incorrect autocorrect for `Style/ClassEqualityComparison` when using instance variable comparison in module. ([@koic][])
* [#11176](https://github.com/rubocop/rubocop/pull/11176): Fix a false positive cases for `Lint/DuplicateMethods` when using duplicate nested method. ([@koic][])
* [#11164](https://github.com/rubocop/rubocop/issues/11164): Suppress "RuboCop server starting..." message with `--server --format json`. ([@koic][])
* [#11156](https://github.com/rubocop/rubocop/pull/11156): Fix `Style/OperatorMethodCall` autocorrection when operators are chained. ([@gsamokovarov][])
* [#11139](https://github.com/rubocop/rubocop/issues/11139): Fix a false negative for `Style/HashEachMethods` when using each with a symbol proc argument. ([@ydah][])
* [#11161](https://github.com/rubocop/rubocop/issues/11161): Fix a false positive for `Style/HashAsLastArrayItem` when using double splat operator. ([@koic][])
* [#11151](https://github.com/rubocop/rubocop/pull/11151): Fix a false positive for `Lint/SuppressedException`. ([@akihikodaki][])
* [#11123](https://github.com/rubocop/rubocop/issues/11123): Fix autocorrection bug for `Style/StringLiterals` when using multiple escape characters. ([@si-lens][])
* [#11165](https://github.com/rubocop/rubocop/issues/11165): Fix a false positive for `Style/RedundantEach` when any method is used between methods containing `each` in the method name. ([@koic][])
* [#11177](https://github.com/rubocop/rubocop/pull/11177): Fix a false positive for `Style/ObjectThen` cop with TargetRubyVersion < 2.6. ([@epaew][])
* [#11173](https://github.com/rubocop/rubocop/issues/11173): Fix an incorrect autocorrect for `Style/CollectionCompact` when using `reject` with block pass arg and no parentheses. ([@koic][])
* [#11137](https://github.com/rubocop/rubocop/issues/11137): Fix a false positive for `Style/RedundantEach` when using a symbol proc argument. ([@ydah][])
* [#11142](https://github.com/rubocop/rubocop/pull/11142): Fix `Style/RedundantEach` for non-chained `each_` calls. ([@fatkodima][])

### Changes

* [#11130](https://github.com/rubocop/rubocop/pull/11130): Check blank percent literal by `Layout/SpaceInsidePercentLiteralDelimiters`. ([@r7kamura][])
* [#11163](https://github.com/rubocop/rubocop/pull/11163): Mark `Style/HashExcept` as unsafe. ([@r7kamura][])
* [#11171](https://github.com/rubocop/rubocop/pull/11171): Support inline visibility definition on checking visibility. ([@r7kamura][])
* [#11158](https://github.com/rubocop/rubocop/pull/11158): Add `if` to allowed names list for MethodParameterName. ([@okuramasafumi][])

## 1.38.0 (2022-11-01)

### New features

* [#11110](https://github.com/rubocop/rubocop/pull/11110): Add new `Style/RedundantEach` cop. ([@koic][])
* [#10255](https://github.com/rubocop/rubocop/pull/10255): Add simple autocorrect for `Style/GuardClause`. ([@FnControlOption][])
* [#11126](https://github.com/rubocop/rubocop/pull/11126): Have `Lint/RedundantRequireStatement` mark `set` as a redundant require in Ruby 3.2+. ([@drenmi][])
* [#11001](https://github.com/rubocop/rubocop/pull/11001): Add option to raise cop errors `--raise-cop-error`. ([@wildmaples][])
* [#10987](https://github.com/rubocop/rubocop/pull/10987): Opt-in cop compatibility in redundant directives. ([@tdeo][])

### Bug fixes

* [#11125](https://github.com/rubocop/rubocop/pull/11125): Fix an error for `Layout/SpaceInsideHashLiteralBraces` when using method argument that both key and value are hash literals. ([@koic][])
* [#11132](https://github.com/rubocop/rubocop/issues/11132): Fix clobbering error on `Lint/EmptyConditionalBody`. ([@r7kamura][])
* [#11117](https://github.com/rubocop/rubocop/issues/11117): Fix a false positive for `Style/BlockDelimiters` when specifying `EnforcedStyle: semantic` and using a single line block with {} followed by a safe navigation method call. ([@koic][])
* [#11120](https://github.com/rubocop/rubocop/issues/11120): Fix an incorrect autocorrect for `Lint/RedundantRequireStatement` when using redundant `require` with modifier form. ([@koic][])

### Changes

* [#11131](https://github.com/rubocop/rubocop/pull/11131): Check newline in empty reference bracket on `Layout/SpaceInsideReferenceBrackets`. ([@r7kamura][])
* [#11045](https://github.com/rubocop/rubocop/pull/11045): Update the `Style/ModuleFunction` documentation to suggest `class << self` as an alternative. ([@rdeckard][])
* [#11006](https://github.com/rubocop/rubocop/issues/11006): Allow multiple `elsif` for `Style/IfWithBooleanLiteralBranches`. ([@koic][])
* [#11113](https://github.com/rubocop/rubocop/pull/11113): Report the count of files in the Worst and the Offense Count formatters. ([@hosamaly][])

## 1.37.1 (2022-10-24)

### Bug fixes

* [#11102](https://github.com/rubocop/rubocop/issues/11102): Fix an error for `Style/AccessModifierDeclarations` when using access modifier in a block. ([@koic][])
* [#11107](https://github.com/rubocop/rubocop/issues/11107): Fix a false positive for `Style/OperatorMethodCall` when a constant receiver uses an operator method. ([@koic][])
* [#11104](https://github.com/rubocop/rubocop/issues/11104): Fix an error for `Style/CollectionCompact` when using `reject` method and receiver is a variable. ([@koic][])
* [#11114](https://github.com/rubocop/rubocop/issues/11114): Fix an error for `Style/OperatorMethodCall` when using `obj.!`. ([@koic][])
* [#11088](https://github.com/rubocop/rubocop/issues/11088): Fix an error when specifying `SuggestExtensions: true`. ([@koic][])
* [#11089](https://github.com/rubocop/rubocop/issues/11089): Fix an error for `Style/RedundantStringEscape` when using character literals (e.g. `?a`). ([@ydah][])
* [#11098](https://github.com/rubocop/rubocop/issues/11098): Fix false positive for `Style/RedundantStringEscape`. ([@tdeo][])
* [#11095](https://github.com/rubocop/rubocop/pull/11095): Fix an error for `Style/RedundantStringEscape` cop when using `?\n` string character literal. ([@koic][])

## 1.37.0 (2022-10-20)

### New features

* [#11043](https://github.com/rubocop/rubocop/issues/11043): Add new `Lint/DuplicateMagicComment` cop. ([@koic][])
* [#10409](https://github.com/rubocop/rubocop/issues/10409): Add `--no-exclude-limit` CLI option. ([@r7kamura][])
* [#10986](https://github.com/rubocop/rubocop/pull/10986): Add autocorrect for `Style/StaticClass`. ([@FnControlOption][])
* [#11018](https://github.com/rubocop/rubocop/issues/11018): Add `AllowedMethods` and `AllowedPatterns` for `Lint/NestedMethodDefinition`. ([@koic][])
* [#11055](https://github.com/rubocop/rubocop/pull/11055): Implement `Lint/DuplicateMethods` for object singleton class. ([@tdeo][])
* [#10997](https://github.com/rubocop/rubocop/pull/10997): Make `rubocop` command aware of `--server` option from .rubocop and RUBOCOP_OPTS. ([@koic][])
* [#11079](https://github.com/rubocop/rubocop/issues/11079): Add new `Style/OperatorMethodCall` cop. ([@koic][])
* [#10439](https://github.com/rubocop/rubocop/issues/10439): Add new `Style/RedundantStringEscape` cop. ([@owst][])

### Bug fixes

* [#11034](https://github.com/rubocop/rubocop/issues/11034): Fix server mode behavior when using `--stderr`. ([@tdeo][])
* [#11028](https://github.com/rubocop/rubocop/issues/11028): Fix a false positive for `Lint/RequireParentheses` when using ternary operator in square brackets. ([@koic][])
* [#11051](https://github.com/rubocop/rubocop/issues/11051): Preserve comments on `Style/AccessModifierDeclarations` autocorrection. ([@r7kamura][])
* [#9116](https://github.com/rubocop/rubocop/issues/9116): Support `super` method in `Layout/FirstArgumentIndentation`. ([@tdeo][])
* [#11068](https://github.com/rubocop/rubocop/pull/11068): Fix a false positive for `Style/RedundantRegexpCharacterClass` when using starting with "\0" number. ([@koic][])
* [#11082](https://github.com/rubocop/rubocop/pull/11082): Fix an incorrect autocorrect for `Lint/SafeNavigationChain` when safe navigation on the right-hand side of the arithmetic operator. ([@ydah][])
* [#10982](https://github.com/rubocop/rubocop/pull/10982): Do not autocorrect parentheses for calls in assignments in conditional branches for `Style/MethodCallWithArgsParentheses` with `omit_parentheses`. ([@gsamokovarov][])
* [#11084](https://github.com/rubocop/rubocop/issues/11084): Fix an error for `Style/ParallelAssignment` when using parallel assignment in singleton method. ([@koic][])
* [#11078](https://github.com/rubocop/rubocop/pull/11078): Fix a false positive for `Style/RedundantBegin` when using endless method definition for `begin` with multiple statements. ([@koic][])
* [#11074](https://github.com/rubocop/rubocop/issues/11074): Fix a false positive for `Lint/RedundantDirGlobSort` when using `Dir.glob` with multiple arguments. ([@koic][])
* [#11025](https://github.com/rubocop/rubocop/issues/11025): Check comments for disables in `RedundantInitialize` cop. ([@HeroProtagonist][])
* [#11003](https://github.com/rubocop/rubocop/issues/11003): Fix clobbering exception in EmptyConditionalBody cop when if branch is empty but else is not. ([@srcoley][])
* [#11026](https://github.com/rubocop/rubocop/issues/11026): Fix an error occurred for `Style/SymbolArray` and `Style/WordArray` when empty percent array. ([@ydah][])
* [#11022](https://github.com/rubocop/rubocop/issues/11022): Fix an incorrect autocorrect for `Style/RedundantCondition`  when using redundant brackets access condition. ([@koic][])
* [#11037](https://github.com/rubocop/rubocop/issues/11037): Fix a false positive for `Style/CollectionCompact` when using `to_enum.reject` or `lazy.reject` methods with Ruby 3.0 or lower. ([@koic][])
* [#11017](https://github.com/rubocop/rubocop/pull/11017): Fix an autocorrect for `Lint/EmptyConditionalBody` that causes a SyntaxError when missing `if` and `else` body. ([@ydah][])
* [#11047](https://github.com/rubocop/rubocop/issues/11047): Fix an incorrect autocorrect for `Lint/SafeNavigationChain` when using `+@` and `-@` methods. ([@koic][])
* [#11015](https://github.com/rubocop/rubocop/pull/11015): Fix a false positive for `Style/HashSyntax` when without parentheses call expr follows after nested method call. ([@koic][])
* [#11067](https://github.com/rubocop/rubocop/issues/11067): Fix a false positive for `Lint/DuplicateRegexpCharacterClassElement` when using regexp character starts with escaped zero number. ([@koic][])
* [#11030](https://github.com/rubocop/rubocop/issues/11030): Fix an incorrect autocorrect for `Lint/UnusedMethodArgument` and `Style::ExplicitBlockArgument` when autocorrection conflicts for `&block` argument. ([@koic][])
* [#11069](https://github.com/rubocop/rubocop/issues/11069): Fix an incorrect autocorrect for `Lint/RedundantCopDisableDirective` when disable directive contains free comment. ([@koic][])
* [#11063](https://github.com/rubocop/rubocop/pull/11063): Preserve comments on `Style/AccessorGrouping` autocorrection. ([@r7kamura][])
* [#10994](https://github.com/rubocop/rubocop/issues/10994): Fix an error when running 3rd party gem that does not require server. ([@koic][])

### Changes

* [#11054](https://github.com/rubocop/rubocop/pull/11054): Implement correct behavior for compact mode for `Layout/SpaceInsideArrayLiteralBrackets`. ([@tdeo][])
* [#10924](https://github.com/rubocop/rubocop/issues/10924): `Style/NegatedIfElseCondition` also checks negative conditions inside parentheses. ([@tsugimoto][])
* [#11042](https://github.com/rubocop/rubocop/pull/11042): Mark `Lint/OrderedMagicComments` as unsafe autocorrection. ([@koic][])
* [#11057](https://github.com/rubocop/rubocop/pull/11057): Make `Lint/RedundantRequireStatement` aware of `pp`, `ruby2_keywords`, and `fiber`. ([@koic][])
* [#10988](https://github.com/rubocop/rubocop/pull/10988): Raise error when both safe and unsafe autocorrect options are specified. ([@koic][])
* [#11032](https://github.com/rubocop/rubocop/pull/11032): Detect empty Hash literal braces containing only newlines and spaces on `Layout/SpaceInsideHashLiteralBraces`. ([@r7kamura][])

## 1.36.0 (2022-09-01)

### New features

* [#10931](https://github.com/rubocop/rubocop/pull/10931): Add `AllowOnSelfClass` option to `Style/CaseEquality`. ([@sambostock][])

### Bug fixes

* [#10958](https://github.com/rubocop/rubocop/issues/10958): Fix an infinite loop for `Layout/SpaceInsideBlockBraces` when `EnforcedStyle` is `no_space` and using multiline block. ([@ydah][])
* [#10903](https://github.com/rubocop/rubocop/pull/10903): Skip forking off extra processes for parallel inspection when only a single file needs to be inspected. ([@wjwh][])
* [#10919](https://github.com/rubocop/rubocop/issues/10919): Fix a huge performance regression between 1.32.0 and 1.33.0. ([@ydah][])
* [#10951](https://github.com/rubocop/rubocop/issues/10951): Fix an autocorrection error for `Lint/EmptyConditionalBody` when some conditional branch is empty. ([@ydah][])
* [#10927](https://github.com/rubocop/rubocop/issues/10927): Fix a false positive for `Style/HashTransformKeys` and `Style/HashTransformValues` when not using transformed block argument. ([@koic][])
* [#10979](https://github.com/rubocop/rubocop/issues/10979): Fix a false positive for `Style/RedundantParentheses` when using parentheses with pin operator except for variables. ([@Tietew][])
* [#10962](https://github.com/rubocop/rubocop/pull/10962): Fix a false positive for `Lint/ShadowingOuterLocalVariable` when conditional with if/elsif/else branches. ([@ydah][])
* [#10969](https://github.com/rubocop/rubocop/issues/10969): Fix a false negative for `AllowedPatterns` of `Lint/AmbiguousBlockAssociation` when using a method chain. ([@jcalvert][])
* [#10963](https://github.com/rubocop/rubocop/issues/10963): Fix a false positive for `Layout/IndentationWidth` when using aligned empty `else` in pattern matching. ([@koic][])
* [#10975](https://github.com/rubocop/rubocop/pull/10975): Fix possible wrong autocorrection in namespace on `Style/PerlBackrefs`. ([@r7kamura][])

### Changes

* [#10928](https://github.com/rubocop/rubocop/pull/10928): Add more autocorrect support on `Style/EachForSimpleLoop`. ([@r7kamura][])
* [#10960](https://github.com/rubocop/rubocop/issues/10960): Add `as` to `AllowedNames` in default configuration for `Naming/MethodParameterName` cop. ([@koic][])
* [#10966](https://github.com/rubocop/rubocop/pull/10966): Add autocorrect support to `Style/AccessModifierDeclarations`. ([@r7kamura][])
* [#10940](https://github.com/rubocop/rubocop/pull/10940): Add server mode status to `-V` option. ([@koic][])

## 1.35.1 (2022-08-22)

### Bug fixes

* [#10926](https://github.com/rubocop/rubocop/issues/10926): Make `Style/SafeNavigation` aware of a redundant nil check. ([@koic][])
* [#10944](https://github.com/rubocop/rubocop/issues/10944): Fix an incorrect autocorrect for `Lint/LiteralInInterpolation` when using `"#{nil}"`. ([@koic][])
* [#10921](https://github.com/rubocop/rubocop/issues/10921): Fix an error when ERB pre-processing of the configuration file. ([@koic][])
* [#10936](https://github.com/rubocop/rubocop/issues/10936): Fix an error for `Lint/NonAtomicFileOperation` when using `FileTest.exist?` as a condition for `elsif`. ([@koic][])
* [#10920](https://github.com/rubocop/rubocop/issues/10920): Fix an incorrect autocorrect for `Style/SoleNestedConditional` when using nested conditional and branch contains a comment. ([@koic][])
* [#10939](https://github.com/rubocop/rubocop/issues/10939): Fix an error for `Style/Next` when line break before condition. ([@koic][])

## 1.35.0 (2022-08-12)

### New features

* [#9364](https://github.com/rubocop/rubocop/pull/9364): Add `Style/MagicCommentFormat` cop. ([@dvandersluis][], [@mattbearman][])
* [#10776](https://github.com/rubocop/rubocop/pull/10776): New option (`consistent`) for `EnforcedShorthandSyntax` in `Style/HashSyntax` to avoid mixing shorthand and non-shorthand hash keys in ruby 3.1. ([@h-lame][])

### Bug fixes

* [#10899](https://github.com/rubocop/rubocop/issues/10899): Fix an error for `Lint/ShadowingOuterLocalVariable` when the same variable name as a block variable is used in return value assignment of `if`. ([@koic][])
* [#10916](https://github.com/rubocop/rubocop/pull/10916): Fix an error when .rubocop.yml is empty. ([@koic][])
* [#10915](https://github.com/rubocop/rubocop/pull/10915): Fix numblock support to `Layout/BlockAlignment`, `Layout/BlockEndNewline`, `Layout/EmptyLinesAroundAccessModifier`, `Layout/EmptyLinesAroundBlockBody`, `Layout/IndentationWidth`, `Layout/LineLength`, `Layout/MultilineBlockLayout`, `Layout/SpaceBeforeBlockBraces`, `Lint/NextWithoutAccumulator`, `Lint/NonDeterministicRequireOrder`, `Lint/RedundantWithIndex`, `Lint/RedundantWithObject`, `Lint/UnreachableLoop`, `Lint/UselessAccessModifier`, `Lint/Void`, `Metrics/AbcSize`, `Metrics/CyclomaticComplexity`, `Style/CollectionMethods`, `Style/CombinableLoops`, `Style/EachWithObject`, `Style/For`, `Style/HashEachMethods`, `Style/InverseMethods`, `Style/MethodCalledOnDoEndBlock`, `Style/MultilineBlockChain`, `Style/Next`, `Style/ObjectThen`, `Style/Proc`, `Style/RedundantBegin`, `Style/RedundantSelf`, `Style/RedundantSortBy` and `Style/TopLevelMethodDefinition`. ([@gsamokovarov][])
* [#10895](https://github.com/rubocop/rubocop/issues/10895): Fix incorrect autocomplete in `Style/RedundantParentheses` when a heredoc is used in an array. ([@dvandersluis][])
* [#10909](https://github.com/rubocop/rubocop/pull/10909): Fix loading behavior on running without `bundle exec`. ([@r7kamura][])
* [#10913](https://github.com/rubocop/rubocop/issues/10913): Make `Style/ArgumentsForwarding` aware of anonymous block argument. ([@koic][])
* [#10911](https://github.com/rubocop/rubocop/pull/10911): Fix `Style/ClassMethodsDefinitions` for non-self receivers. ([@sambostock][])

### Changes

* [#10915](https://github.com/rubocop/rubocop/pull/10915): Depend on rubocop-ast 1.20.1 for numblocks support in #macro?. ([@gsamokovarov][])

## 1.34.1 (2022-08-09)

### Bug fixes

* [#10893](https://github.com/rubocop/rubocop/issues/10893): Fix an error when running `rubocop` without `bundle exec`. ([@koic][])

## 1.34.0 (2022-08-09)

### New features

* [#10170](https://github.com/rubocop/rubocop/pull/10170): Add new `InternalAffairs/SingleLineComparison` cop. ([@dvandersluis][])

### Bug fixes

* [#10552](https://github.com/rubocop/rubocop/issues/10552): Require RuboCop AST 1.20.0+ to fix a false positive for `Lint/OutOfRangeRegexpRef` when using fixed-encoding regopt. ([@koic][])
* [#10512](https://github.com/rubocop/rubocop/issues/10512): Fix a false positive for `Lint/ShadowingOuterLocalVariable` conditional statement and block variable. ([@ydah][])
* [#10864](https://github.com/rubocop/rubocop/pull/10864): `min` and `max` results in false positives for `Style/SymbolProc` similarly to `select` and `reject`. ([@mollerhoj][])
* [#10846](https://github.com/rubocop/rubocop/issues/10846): Fix a false negative for `Style/DoubleNegation` when there is a hash or an array at return location of method. ([@nobuyo][])
* [#10875](https://github.com/rubocop/rubocop/pull/10875): Fix an obsolete option configuration values are duplicated when generating `.rubocop_todo.yml`. ([@ydah][])
* [#10877](https://github.com/rubocop/rubocop/issues/10877): Fix crash with `Layout/BlockEndNewline` heredoc detection. ([@dvandersluis][])
* [#10859](https://github.com/rubocop/rubocop/issues/10859): Fix `Lint/Debugger` to be able to handle method chains correctly. ([@dvandersluis][])
* [#10883](https://github.com/rubocop/rubocop/issues/10883): Fix `Style/RedundantParentheses` to be able to detect offenses and properly correct when the end parentheses and comma are on their own line. ([@dvandersluis][])
* [#10881](https://github.com/rubocop/rubocop/issues/10881): Fix `Style/SoleNestedConditional` to properly wrap `block` and `csend` nodes when necessary. ([@dvandersluis][])
* [#10867](https://github.com/rubocop/rubocop/pull/10867): Mark autocorrection for `Lint/EmptyConditionalBody` as unsafe. ([@dvandersluis][])
* [#10871](https://github.com/rubocop/rubocop/issues/10871): Restore `RuboCop::ConfigLoader.project_root` as deprecated. ([@koic][])

### Changes

* [#10857](https://github.com/rubocop/rubocop/issues/10857): Add `AllowedPatterns` to `Style/NumericLiterals`. ([@dvandersluis][])
* [#10648](https://github.com/rubocop/rubocop/issues/10648): Allow `Style/TernaryParentheses` to take priority over `Style/RedundantParentheses` when parentheses are enforced. ([@dvandersluis][])
* [#10731](https://github.com/rubocop/rubocop/issues/10731): Show tip for suggested extensions that are installed but not loaded in .rubocop.yml. ([@nobuyo][])
* [#10845](https://github.com/rubocop/rubocop/pull/10845): Support Bundler-like namespaced feature on require config. ([@r7kamura][])
* [#10773](https://github.com/rubocop/rubocop/issues/10773): Require Parser 3.1.2.1 or higher. ([@dvandersluis][])

## 1.33.0 (2022-08-04)

### Bug fixes

* [#10830](https://github.com/rubocop/rubocop/issues/10830): Fix an incorrect autocorrect for `Layout/FirstArgumentIndentation` when specifying `EnforcedStyle: with_fixed_indentation` of `Layout/ArgumentAlignment` and `EnforcedStyle: consistent` of `Layout/FirstArgumentIndentation` and enabling `Layout/FirstMethodArgumentLineBreak`. ([@koic][])
* [#10825](https://github.com/rubocop/rubocop/issues/10825): Fix an incorrect autocorrect for `Style/ClassAndModuleChildren` when using nested one-liner class. ([@koic][])
* [#10843](https://github.com/rubocop/rubocop/issues/10843): Fix a false positive for `Style/HashExcept` when using `reject` and calling `include?` method with symbol array and second block value. ([@koic][])
* [#10853](https://github.com/rubocop/rubocop/pull/10853): Fix an autocorrect for `Style/RedundantSort` with logical operator. ([@ydah][])
* [#10842](https://github.com/rubocop/rubocop/issues/10842): Make server mode aware of `CacheRootDirectory` config option value, `RUBOCOP_CACHE_ROOT`, and `XDG_CACHE_HOME` environment variables. ([@koic][])
* [#10833](https://github.com/rubocop/rubocop/issues/10833): Fix an incorrect autocorrect for `Style/RedundantCondition` when branches contains arithmetic operation. ([@koic][])
* [#10864](https://github.com/rubocop/rubocop/issues/10864): Fix a false positive for `Style/SymbolProc` when using `Hash#reject`. ([@koic][])
* [#10771](https://github.com/rubocop/rubocop/issues/10771): Make server mode aware of `--cache-root` command line option. ([@koic][])
* [#10831](https://github.com/rubocop/rubocop/pull/10831): Fix an error when using `changed_parameters` in obsoletion.yml by external library. ([@koic][])
* [#10850](https://github.com/rubocop/rubocop/pull/10850): Fix `Style/ClassEqualityComparison` autocorrection within module. ([@r7kamura][])
* [#10832](https://github.com/rubocop/rubocop/issues/10832): Fix an incorrect autocorrect for `Layout/BlockEndNewline` when multiline block `}` is not on its own line and using heredoc argument. ([@koic][])

### Changes

* [#10841](https://github.com/rubocop/rubocop/pull/10841): Don't hash shared libraries for cache key. ([@ChrisBr][])
* [#10862](https://github.com/rubocop/rubocop/pull/10862): Add autocorrection to `Lint/EmptyConditionalBody`. ([@dvandersluis][])
* [#10829](https://github.com/rubocop/rubocop/pull/10829): Deprecate `IgnoredMethods` option in favor of the `AllowedMethods` and `AllowedPatterns` options. ([@ydah][])

## 1.32.0 (2022-07-21)

### New features

* [#10820](https://github.com/rubocop/rubocop/pull/10820): Add new `Style/EmptyHeredoc` cop. ([@koic][])
* [#10691](https://github.com/rubocop/rubocop/pull/10691): Add new `Layout/MultilineMethodParameterLineBreaks` cop. ([@Korri][])
* [#10790](https://github.com/rubocop/rubocop/pull/10790): Support `AllowComments` option for `Style/EmptyElse`. ([@ydah][])
* [#10792](https://github.com/rubocop/rubocop/pull/10792): Add new `Lint/RequireRangeParentheses` cop. ([@koic][])
* [#10692](https://github.com/rubocop/rubocop/pull/10692): Break long method definitions when auto-correcting. ([@Korri][])

### Bug fixes

* [#10824](https://github.com/rubocop/rubocop/pull/10824): Make `Lint/DeprecatedClassMethods` aware of `ENV.clone` and `ENV.dup`. ([@koic][])
* [#10788](https://github.com/rubocop/rubocop/issues/10788): Relax `Style/FetchEnvVar` to allow `ENV[]` in LHS of `||`. ([@j-miyake][])
* [#10813](https://github.com/rubocop/rubocop/issues/10813): Fix recursive deletion to suppression in `Lint/NonAtomicFileOperation`. ([@ydah][])
* [#10791](https://github.com/rubocop/rubocop/issues/10791): Fix an incorrect autocorrect for `Style/Semicolon` when using endless range before semicolon. ([@koic][])
* [#10781](https://github.com/rubocop/rubocop/pull/10781): Fix a suggestions for safer conversions for `Lint/NonAtomicFileOperation`. ([@ydah][])
* [#10263](https://github.com/rubocop/rubocop/pull/10263): Fix the value of `Enabled` leaking between configurations. ([@jonas054][])

### Changes

* [#10613](https://github.com/rubocop/rubocop/issues/10613): Allow autocorrecting with -P/--parallel and make it the default. ([@jonas054][])
* Add EnforcedStyle (leading/trailing) configuration to `Layout::LineContinuationLeadingSpace`. ([@bquorning][])
* [#10784](https://github.com/rubocop/rubocop/pull/10784): Preserve multiline semantics on `Style/SymbolArray` and `Style/WordArray`. ([@r7kamura][])
* [#10814](https://github.com/rubocop/rubocop/pull/10814): Avoid buffering stdout when running in server mode. ([@ccutrer][])
* [#10817](https://github.com/rubocop/rubocop/pull/10817): Add autocorrect support for `Lint/SafeNavigationChain`. ([@r7kamura][])
* [#10810](https://github.com/rubocop/rubocop/pull/10810): Support safe navigation operator on `Style/SymbolProc`. ([@r7kamura][])
* [#10803](https://github.com/rubocop/rubocop/pull/10803): Require RuboCop AST 1.9.1 or higher. ([@koic][])

## 1.31.2 (2022-07-07)

### Bug fixes

* [#10774](https://github.com/rubocop/rubocop/pull/10774): Fix false negatives in `Style/DocumentationMethod` when a public method is defined after a private one. ([@Darhazer][])
* [#10764](https://github.com/rubocop/rubocop/issues/10764): Fix performance issue for `Layout/FirstHashElementIndentation` and `Layout/FirstArrayElementIndentation`. ([@j-miyake][])
* [#10780](https://github.com/rubocop/rubocop/issues/10780): Fix an error when using `rubocop:auto_correct` deprecated custom rake task. ([@koic][])
* [#10786](https://github.com/rubocop/rubocop/issues/10786): Fix a false positive for `Lint/NonAtomicFileOperation` when using complex conditional. ([@koic][])
* [#10785](https://github.com/rubocop/rubocop/pull/10785): Fix a false negative for `Style/RedundantParentheses` when parens around a receiver of a method call with an argument. ([@koic][])
* [#10026](https://github.com/rubocop/rubocop/issues/10026): Fix merging of array parameters in either parent of default config. ([@jonas054][])

## 1.31.1 (2022-06-29)

### Bug fixes

* [#10763](https://github.com/rubocop/rubocop/issues/10763): Fix a false positive for `Layout/LineContinuationSpacing` when using continuation keyword `\` after `__END__`. ([@koic][])
* [#10755](https://github.com/rubocop/rubocop/issues/10755): Fix a false positive for `Lint/LiteralAsCondition` when using a literal in `case-in` condition where the match variable is used in `in` are accepted as a pattern matching. ([@koic][])
* [#10760](https://github.com/rubocop/rubocop/issues/10760): Fix a false positive for `Lint/NonAtomicFileOperation` when using `FileTest.exist?` with `if` condition that has `else` branch. ([@koic][])
* [#10745](https://github.com/rubocop/rubocop/issues/10745): Require JSON 2.3 or higher to fix an incompatible JSON API error. ([@koic][])
* [#10754](https://github.com/rubocop/rubocop/issues/10754): Fix an incorrect autocorrect for `Style/HashExcept` when using a non-literal collection receiver for `include?`. ([@koic][])
* [#10751](https://github.com/rubocop/rubocop/issues/10751): Fix autocorrect for `Layout/FirstHashElementIndentation`. ([@j-miyake][])
* [#10750](https://github.com/rubocop/rubocop/pull/10750): Recover 7x slow running `rubocop`. ([@koic][])

## 1.31.0 (2022-06-27)

### New features

* [#10699](https://github.com/rubocop/rubocop/pull/10699): Add new global `ActiveSupportExtensionsEnabled` option. ([@nobuyo][])
* [#10245](https://github.com/rubocop/rubocop/pull/10245): Add specification_version and rubygems_version to `Gemspec/DeprecatedAttributeAssignment`. ([@kaitielth][])
* [#10696](https://github.com/rubocop/rubocop/pull/10696): Add new `Lint/NonAtomicFileOperation` cop. ([@ydah][])
* [#6420](https://github.com/rubocop/rubocop/issues/6420): Add new `Layout/LineContinuationLeadingSpace` cop. ([@bquorning][])
* [#6420](https://github.com/rubocop/rubocop/issues/6420): Add new `Layout/LineContinuationSpacing` cop. ([@bquorning][])
* [#10706](https://github.com/rubocop/rubocop/pull/10706): Integrate rubocop-daemon to add server options. ([@koic][])
* [#10722](https://github.com/rubocop/rubocop/pull/10722): Add new `Lint/ConstantOverwrittenInRescue` cop. ([@ydah][])

### Bug fixes

* [#10700](https://github.com/rubocop/rubocop/issues/10700): Update `Style/EmptyMethod` to not correct if the correction would exceed the configuration for `Layout/LineLength`. ([@dvandersluis][])
* [#10698](https://github.com/rubocop/rubocop/issues/10698): Enhance `Style/HashExcept` to support array inclusion checks. ([@nobuyo][])
* [#10734](https://github.com/rubocop/rubocop/issues/10734): Handle `ClobberingError` in `Style/NestedTernaryOperator` when there are multiple nested ternaries. ([@dvandersluis][])
* [#10689](https://github.com/rubocop/rubocop/issues/10689): Fix autocorrect for `Layout/FirstHashElementIndentation` and `Layout/FirstArrayElementIndentation`. ([@j-miyake][])
* Fix `rubocop -V` not displaying the version information for rubocop-graphql, rubocop-md and rubocop-thread_safety. ([@Darhazer][])
* [#10711](https://github.com/rubocop/rubocop/issues/10711): Fix an error for `Style/MultilineTernaryOperator` when the false branch is on a separate line. ([@koic][])
* [#10719](https://github.com/rubocop/rubocop/issues/10719): Fix a false positive for `Lint/ParenthesesAsGroupedExpression` when using safe navigation operator. ([@koic][])
* [#10736](https://github.com/rubocop/rubocop/pull/10736): Fix `Layout/SpaceInsideBlockBraces` for blocks with numbered arguments. ([@gsamokovarov][])
* [#10749](https://github.com/rubocop/rubocop/pull/10749): Fix `Style/BlockDelimiters` for blocks with numbered arguments. ([@gsamokovarov][])
* [#10737](https://github.com/rubocop/rubocop/issues/10737): Fix crash in `Style/ConditionalAssignment` with `EnforcedStyle: assign_inside_condition` when op-assigning a variable inside a `resbody`. ([@dvandersluis][])
* [#7900](https://github.com/rubocop/rubocop/issues/7900): Fix `Style/FormatStringToken` false positive with formatted input and `template` style enforced, and add autocorrection. ([@FnControlOption][])

### Changes

* [#10730](https://github.com/rubocop/rubocop/pull/10730): Change output timing of GitHubActionsFormatter. ([@r7kamura][])
* [#10709](https://github.com/rubocop/rubocop/pull/10709): Deprecate `rubocop:auto_correct` custom rake task and newly split `rubocop:autocorrect` and `rubocop:autocorrect-all` custom rake tasks. ([@koic][])
* [#9760](https://github.com/rubocop/rubocop/issues/9760): Change RangeHelp#range_with_surrounding_space to allow passing the range as a positional argument. ([@pirj][])
* [#10693](https://github.com/rubocop/rubocop/issues/10693): Add ignore case for `Layout/EmptyLinesAroundAttributeAccessor` when there is a comment line on the next line. ([@ydah][])
* [#10245](https://github.com/rubocop/rubocop/pull/10245): **(Breaking)** integrate `Gemspec/DateAssignment` into `Gemspec/DeprecatedAttributeAssignment`. ([@kaitielth][])
* [#10697](https://github.com/rubocop/rubocop/pull/10697): Restore `Lint/UselessElseWithoutRescue` cop. ([@koic][])
* [#10740](https://github.com/rubocop/rubocop/pull/10740): Make `Style/GuardClause` a bit more lenient when the replacement would make the code more verbose. ([@dvandersluis][])

## 1.30.1 (2022-06-06)

### Bug fixes

* [#10685](https://github.com/rubocop/rubocop/issues/10685): Fix a false positive for `Style/StringConcatenation` when `Mode: conservative` and first operand is not string literal. ([@koic][])
* [#10670](https://github.com/rubocop/rubocop/pull/10670): Fix a false positive for `Style/FetchEnvVar` in the body with assignment method. ([@ydah][])
* [#10671](https://github.com/rubocop/rubocop/issues/10671): Fix an incorrect autocorrect for `EnforcedStyle: with_first_argument` of `Layout/ArgumentAlignment` and `EnforcedColonStyle: separator` of `Layout/HashAlignment`. ([@koic][])
* [#10676](https://github.com/rubocop/rubocop/pull/10676): Fix `--ignore-unrecognized-cops` option always showing empty warning even if there was no problem. ([@nobuyo][])
* [#10674](https://github.com/rubocop/rubocop/issues/10674): Fix a false positive for `Naming/AccessorMethodName` with type of the first argument is other than `arg`. ([@ydah][])
* [#10679](https://github.com/rubocop/rubocop/issues/10679): Fix a false positive for `Style/SafeNavigation` when `TargetRubyVersion: 2.2` or lower. ([@koic][])

### Changes

* [#10673](https://github.com/rubocop/rubocop/pull/10673): Update auto-gen-config's comment re auto-correct for `SafeAutoCorrect: false`. ([@ydah][])

## 1.30.0 (2022-05-26)

### New features

* [#10065](https://github.com/rubocop/rubocop/issues/10065): Add new `Gemspec/DeprecatedAttributeAssignment` cop. ([@koic][])
* [#10608](https://github.com/rubocop/rubocop/pull/10608): Add new `Style/MapCompactWithConditionalBlock` cop. ([@nobuyo][])
* [#10627](https://github.com/rubocop/rubocop/issues/10627): Add command-line option `--ignore-unrecognized-cops` to ignore any unknown cops or departments in .rubocop.yml. ([@nobuyo][])
* [#10620](https://github.com/rubocop/rubocop/pull/10620): Add Sorbet's `typed` sigil as a magic comment. ([@zachahn][])

### Bug fixes

* [#10662](https://github.com/rubocop/rubocop/pull/10662): Recover Ruby 2.1 code analysis using `TargetRubyVersion: 2.1`. ([@koic][])
* [#10396](https://github.com/rubocop/rubocop/issues/10396): Fix autocorrect for `Layout/IndentationWidth` to leave module/class body unchanged to avoid infinite autocorrect loop with `Layout/IndentationConsistency` when body trails after class/module definition. ([@johnny-miyake][])
* [#10636](https://github.com/rubocop/rubocop/issues/10636): Fix false positive in `Style/RedundantCondition` when the branches call the same method on different receivers. ([@dvandersluis][])
* [#10651](https://github.com/rubocop/rubocop/issues/10651): Fix autocorrect for `Style/For` when using array with operator methods as collection. ([@nobuyo][])
* [#10629](https://github.com/rubocop/rubocop/pull/10629): Fix default Ruby version from 2.5 to 2.6. ([@koic][])
* [#10661](https://github.com/rubocop/rubocop/pull/10661): Fix a false negative for `Style/SymbolProc` when method has no arguments and `AllowMethodsWithArguments: true`. ([@koic][])
* [#10631](https://github.com/rubocop/rubocop/issues/10631): Fix autocorrect for `Style/RedundantBegin`. ([@johnny-miyake][])
* [#10652](https://github.com/rubocop/rubocop/issues/10652): Fix a false positive for `Style/FetchEnvVar` in conditions. ([@ydah][])
* [#10665](https://github.com/rubocop/rubocop/issues/10665): Fix an incorrect autocorrect for `EnforcedStyle: with_first_argument` of `Layout/ArgumentAlignment` and `EnforcedColonStyle: separator` of `Layout/HashAlignment`. ([@koic][])
* [#10258](https://github.com/rubocop/rubocop/issues/10258): Recover Ruby 2.4 code analysis using `TargetRubyVersion: 2.4`. ([@koic][])
* [#10668](https://github.com/rubocop/rubocop/pull/10668): Recover Ruby 2.0 code analysis using `TargetRubyVersion: 2.0`. ([@koic][])
* [#10644](https://github.com/rubocop/rubocop/pull/10644): Recover Ruby 2.2 code analysis using `TargetRubyVersion: 2.2`. ([@koic][])
* [#10639](https://github.com/rubocop/rubocop/issues/10639): Fix `Style/HashSyntax` to exclude files that violate it with `EnforceHashShorthandSyntax` when running `auto-gen-config`. ([@nobuyo][])
* [#10633](https://github.com/rubocop/rubocop/issues/10633): Fix infinite autocorrection loop in `Style/AccessorGrouping` when combining multiple of the same accessor. ([@dvandersluis][])
* [#10618](https://github.com/rubocop/rubocop/issues/10618): Fix `LineBreakCorrector` so that it won't remove a semicolon in the class/module body. ([@johnny-miyake][])
* [#10646](https://github.com/rubocop/rubocop/issues/10646): Fix an incorrect autocorrect for `Style/SoleNestedConditional` when using `unless` and `&&` without parens in the outer condition and nested modifier condition. ([@koic][])
* [#10659](https://github.com/rubocop/rubocop/issues/10659): Fix automatically appended path for `inherit_from` by `auto-gen-config` is incorrect if specified config file in a subdirectory as an option. ([@nobuyo][])
* [#10640](https://github.com/rubocop/rubocop/pull/10640): Recover Ruby 2.3 code analysis using `TargetRubyVersion: 2.3`. ([@koic][])
* [#10657](https://github.com/rubocop/rubocop/issues/10657): Fix `--auto-gen-config` command option ignores specified config file by option. ([@nobuyo][])

### Changes

* [#10095](https://github.com/rubocop/rubocop/issues/10095): Change "auto-correct" to "autocorrect" in arguments, documentation, messages, comments, and specs. ([@chris-hewitt][])
* [#10656](https://github.com/rubocop/rubocop/issues/10656): Mark `Style/RedundantInterpolation` as unsafe autocorrection. ([@koic][])
* [#10616](https://github.com/rubocop/rubocop/pull/10616): Markdown formatter: skip files with no offenses. ([@rickselby][])

## 1.29.1 (2022-05-12)

### Bug fixes

* [#10625](https://github.com/rubocop/rubocop/issues/10625): Restore the specification to `TargetRubyVersion: 2.5`. ([@koic][])
* [#10569](https://github.com/rubocop/rubocop/issues/10569): Fix a false positive for `Style/FetchEnvVar` when using the same `ENV` var as `if` condition in the body. ([@koic][])
* [#10614](https://github.com/rubocop/rubocop/issues/10614): Make `Lint/NonDeterministicRequireOrder` aware of `require_relative`. ([@koic][])
* [#10607](https://github.com/rubocop/rubocop/issues/10607): Fix autocorrect for `Style/RedundantCondition` when there are parenthesized method calls in each branch. ([@nobuyo][])
* [#10622](https://github.com/rubocop/rubocop/issues/10622): Fix a false positive for `Style/RaiseArgs` when error type class constructor with keyword arguments and message argument. ([@koic][])
* [#10610](https://github.com/rubocop/rubocop/pull/10610): Fix an error for `Naming/InclusiveLanguage` string with invalid byte sequence in UTF-8. ([@ydah][])
* [#10605](https://github.com/rubocop/rubocop/issues/10605): Fix autocorrect for `Style/RedundantCondition` if argument for method in else branch is hash without braces. ([@nobuyo][])

## 1.29.0 (2022-05-06)

### New features

* [#10570](https://github.com/rubocop/rubocop/issues/10570): Add new `Gemspec/DependencyVersion` cop. ([@nobuyo][])
* [#10542](https://github.com/rubocop/rubocop/pull/10542): Add markdown formatter. ([@joe-sharp][])
* [#10539](https://github.com/rubocop/rubocop/issues/10539): Add `AllowedPatterns` configuration option to `Naming/VariableNumber` and `Naming/VariableName`. ([@henrahmagix][])
* [#10568](https://github.com/rubocop/rubocop/issues/10568): Add new `Style/EnvHome` cop. ([@koic][])

### Bug fixes

* [#10586](https://github.com/rubocop/rubocop/issues/10586): Fix a false positive for `Style/DoubleNegation` when using `define_method` or `define_singleton_method`. ([@ydah][])
* [#10579](https://github.com/rubocop/rubocop/issues/10579): Fix a false positive for `Style/FetchEnvVar` when calling a method with safe navigation. ([@koic][])
* [#10581](https://github.com/rubocop/rubocop/issues/10581): Fix a false positive for `Style/FetchEnvVar` when comparing with `ENV['TERM']`. ([@koic][])
* [#10589](https://github.com/rubocop/rubocop/issues/10589): Fix autocorrect for `Style/RaiseArgs` with `EnforcedStyle: compact` and exception object is assigned to a local variable. ([@nobuyo][])
* [#10325](https://github.com/rubocop/rubocop/issues/10325): Enhance `Style/RedundantCondition` by considering the case that variable assignments in each branch. ([@nobuyo][])
* [#10592](https://github.com/rubocop/rubocop/issues/10592): Fix infinite loop on `Style/MultilineTernaryOperator` if using assignment method and condition/branch is multiline. ([@nobuyo][])
* [#10536](https://github.com/rubocop/rubocop/issues/10536): Fix validation for command-line options combination of `--display-only-fail-level-offenses` and `--auto-correct`. ([@nobuyo][])

### Changes

* [#10577](https://github.com/rubocop/rubocop/pull/10577): **(Compatibility)** Drop support for Ruby 2.5 and JRuby 9.2 (CRuby 2.5 compatible). ([@koic][])
* [#10585](https://github.com/rubocop/rubocop/pull/10585): Enhance the autocorrect for `Style/FetchEnvVar`. ([@johnny-miyake][])
* [#10577](https://github.com/rubocop/rubocop/pull/10577): **(Breaking)** Retire `Lint/UselessElseWithoutRescue` cop. ([@koic][])

## 1.28.2 (2022-04-25)

### Bug fixes

* [#10566](https://github.com/rubocop/rubocop/issues/10566): Fix a false positive for `Lint/AmbiguousBlockAssociation` when using proc is used as a last argument. ([@koic][])
* [#10573](https://github.com/rubocop/rubocop/issues/10573): Fix a false positive for `Layout/SpaceBeforeBrackets` when there is a dot before brackets. ([@nobuyo][])
* [#10563](https://github.com/rubocop/rubocop/issues/10563): Fix `Style/BlockDelimiters` unexpectedly deletes block on moving comment if methods with block are chained. ([@nobuyo][])
* [#10574](https://github.com/rubocop/rubocop/issues/10574): Fix a false positive for `Style/SingleArgumentDig` when using dig with arguments forwarding. ([@ydah][])
* [#10565](https://github.com/rubocop/rubocop/pull/10565): Fix a false positive and a true negative for `Style/FetchEnvVar`. ([@koic][])

## 1.28.1 (2022-04-21)

### Bug fixes

* [#10559](https://github.com/rubocop/rubocop/issues/10559): Fix crash on CodeLengthCalculator if method call is not parenthesized. ([@nobuyo][])
* [#10557](https://github.com/rubocop/rubocop/issues/10557): Fix a false positive for `Style/FetchEnvVar` when `ENV['key']` is a receiver of `||=`. ([@koic][])

## 1.28.0 (2022-04-21)

### New features

* [#10551](https://github.com/rubocop/rubocop/pull/10551): Add `AllowComments` option to `Style/RedundantInitialize` is true by default. ([@koic][])
* [#10552](https://github.com/rubocop/rubocop/pull/10552): Support autocorrection for `Style/RedundantInitialize`. ([@koic][])
* [#10441](https://github.com/rubocop/rubocop/pull/10441): Add `Security/CompoundHash` cop. ([@sambostock][], [@chrisseaton][])
* [#10521](https://github.com/rubocop/rubocop/pull/10521): Add `use_builtin_english_names` style to `Style/SpecialGlobalVars`. ([@splattael][])
* [#10522](https://github.com/rubocop/rubocop/issues/10522): Add new `Style/ObjectThen` cop. ([@ydah][])
* [#10502](https://github.com/rubocop/rubocop/pull/10502): Add new `Style/FetchEnvVar` cop. ([@johnny-miyake][])
* [#10544](https://github.com/rubocop/rubocop/pull/10544): Support auto-correction for `Lint/DuplicateRequire`. ([@koic][])
* [#10481](https://github.com/rubocop/rubocop/issues/10481): Add command line options `--display-only-correctable` and `--display-only-safe-correctable`. ([@nobuyo][])

### Bug fixes

* [#10528](https://github.com/rubocop/rubocop/issues/10528): Fix an infinite loop at autocorrect for `Layout/CaseIndentation`. ([@ydah][])
* [#10537](https://github.com/rubocop/rubocop/pull/10537): Fix an incorrect auto-correct for `Style/MultilineTernaryOperator` when returning a multiline ternary operator expression with `break`, `next`, or method call. ([@koic][])
* [#10529](https://github.com/rubocop/rubocop/issues/10529): Fix autocorrect for `Style/SoleNestedConditional` causes logical error when using a outer condition of method call by omitting parentheses for method arguments. ([@nobuyo][])
* [#10530](https://github.com/rubocop/rubocop/issues/10530): Fix a false positive for `Style/RedundantRegexpCharacterClass` when using regexp character class with a character class containing multiple unicode code-points. ([@koic][])
* [#10518](https://github.com/rubocop/rubocop/pull/10518): Fix a false positive for `Style/DoubleNegation` when inside returned conditional clauses with Ruby 2.7's pattern matching. ([@koic][])
* [#10510](https://github.com/rubocop/rubocop/issues/10510): Fix an error for `Style/SingleArgumentDig` when using multiple `dig` in a method chain. ([@koic][])
* [#10553](https://github.com/rubocop/rubocop/issues/10553): Fix crash with trailing tabs in heredocs for `Layout/TrailingWhitespace`. ([@dvandersluis][])
* [#10488](https://github.com/rubocop/rubocop/issues/10488): Fix autocorrection for `Layout/MultilineMethodCallIndentation` breaks indentation for nesting of method calls. ([@nobuyo][])
* [#10543](https://github.com/rubocop/rubocop/pull/10543): Fix incorrect code length calculation for few more patterns of hash folding asked. ([@nobuyo][])
* [#10541](https://github.com/rubocop/rubocop/pull/10541): Fix an incorrect autocorrect for `Style/SpecialGlobalVars` when global variable as Perl name is used multiple times. ([@koic][])
* [#10514](https://github.com/rubocop/rubocop/issues/10514): Fix an error for `Lint/EmptyConditionalBody` when missing second `elsif` body. ([@koic][])
* [#10469](https://github.com/rubocop/rubocop/issues/10469): Fix code length calculation when kwargs written in single line. ([@nobuyo][])

### Changes

* [#10555](https://github.com/rubocop/rubocop/pull/10555): Deprecate `IgnoredPatterns` in favour of `AllowedPatterns`. ([@dvandersluis][])
* [#10356](https://github.com/rubocop/rubocop/issues/10356): Add `AllowConsecutiveConditionals` option to `Style/GuardClause` and the option is false by default. ([@ydah][])
* [#10524](https://github.com/rubocop/rubocop/issues/10524): Mark `Style/RedundantInitialize` as unsafe. ([@koic][])
* [#10280](https://github.com/rubocop/rubocop/issues/10280): Add `AllowComments` option to `Style/SymbolProc` and the option is false by default. ([@ydah][])

## 1.27.0 (2022-04-08)

### New features

* [#10500](https://github.com/rubocop/rubocop/pull/10500): Add new `Lint/RefinementImportMethods` cop. ([@koic][])
* [#10438](https://github.com/rubocop/rubocop/issues/10438): Add new `Style/RedundantInitialize` cop to check for unnecessary `initialize` methods. ([@dvandersluis][])

### Bug fixes

* [#10464](https://github.com/rubocop/rubocop/issues/10464): Fix an incorrect autocorrect for `Lint/IncompatibleIoSelectWithFiberScheduler` when using `IO.select` with read (or write) argument and using return value. ([@koic][])
* [#10506](https://github.com/rubocop/rubocop/issues/10506): Fix an error for `Style/RaiseArgs` when `raise` with `new` method without receiver. ([@koic][])
* [#10479](https://github.com/rubocop/rubocop/issues/10479): Fix a false positive for `Lint/ShadowingOuterLocalVariable` conditional statement and block variable. ([@ydah][])
* [#10189](https://github.com/rubocop/rubocop/issues/10189): Fix `--display-style-guide` so it works together with `--format offenses`. ([@jonas054][])
* [#10465](https://github.com/rubocop/rubocop/issues/10465): Fix false positive for `Naming/BlockForwarding` when the block argument is assigned. ([@dvandersluis][])
* [#10491](https://github.com/rubocop/rubocop/pull/10491): Improve the handling of comments in `Lint/EmptyConditionalBody`, `Lint/EmptyInPattern` and `Lint/EmptyWhen` when `AllowComments` is set to `true`. ([@Darhazer][])
* [#10504](https://github.com/rubocop/rubocop/issues/10504): Fix a false positive for `Lint/UnusedMethodArgument` when using `raise NotImplementedError` with optional arguments. ([@koic][])
* [#10494](https://github.com/rubocop/rubocop/issues/10494): Fix a false positive for `Style/HashSyntax` when `return` with one line `if` condition follows (without parentheses). ([@koic][])
* [#10311](https://github.com/rubocop/rubocop/issues/10311): Fix false negative inside `do`..`end` for `Layout/RedundantLineBreak`. ([@jonas054][])
* [#10468](https://github.com/rubocop/rubocop/issues/10468): Fix a false positive for `Style/FileWrite` when a splat argument is passed to `f.write`. ([@koic][])
* [#10474](https://github.com/rubocop/rubocop/issues/10474): Fix a false positive for `Style/DoubleNegation` with `EnforcedStyle: allowed_in_returns` when inside returned conditional clauses. ([@ydah][])
* [#10388](https://github.com/rubocop/rubocop/issues/10388): Fix an incorrectly adds a disable statement for `Layout/SpaceInsideArrayLiteralBrackets` with `--disable-uncorrectable`. ([@ydah][])
* [#10489](https://github.com/rubocop/rubocop/issues/10489): Fix a false positive for `Lint/LambdaWithoutLiteralBlock` when using lambda with a symbol proc. ([@koic][])

### Changes

* [#10191](https://github.com/rubocop/rubocop/issues/10191): Add `MaxChainLength` option to `Style/SafeNavigation` and the option is 2 by default. ([@ydah][])

## 1.26.1 (2022-03-22)

### Bug fixes

* [#10375](https://github.com/rubocop/rubocop/pull/10375): Fix error for auto-correction of `unless`/`else` nested inside each other. ([@jonas054][])
* [#10457](https://github.com/rubocop/rubocop/pull/10457): Make `Style/SelectByRegexp` aware of `ENV` const. ([@koic][])
* [#10462](https://github.com/rubocop/rubocop/issues/10462): Fix an incorrect autocorrect for `Lint/SymbolConversion` when using a quoted symbol key with hash rocket. ([@koic][])
* [#10456](https://github.com/rubocop/rubocop/issues/10456): Fix a false positive for `Layout/MultilineMethodCallIndentation` when using `EnforcedStyle: indented` with indented assignment method. ([@koic][])
* [#10459](https://github.com/rubocop/rubocop/pull/10459): Fix a false positive for `Layout/LineLength` when long URIs in yardoc comments to have titles. ([@ydah][])
* [#10447](https://github.com/rubocop/rubocop/pull/10447): Fix an error for `Style/SoleNestedConditional` raises exception when inspecting `if ... end if ...`. ([@ydah][])

## 1.26.0 (2022-03-09)

### New features

* [#10419](https://github.com/rubocop/rubocop/pull/10419): Add new `Style/NestedFileDirname` cop. ([@koic][])
* [#10433](https://github.com/rubocop/rubocop/pull/10433): Support `TargetRubyVersion 3.2` (experimental). ([@koic][])

### Bug fixes

* [#10406](https://github.com/rubocop/rubocop/pull/10406): Fix a false positive for `Lint/InheritException` when inheriting a standard lib exception class that is not a subclass of `StandardError`. ([@koic][])
* [#10421](https://github.com/rubocop/rubocop/issues/10421): Make `Style/DefWithParentheses` aware of endless method definition. ([@koic][])
* [#10401](https://github.com/rubocop/rubocop/issues/10401): Fix a false positive for `Style/HashSyntax` when local variable hash key and hash value are the same. ([@koic][])
* [#10424](https://github.com/rubocop/rubocop/pull/10424): Fix a false positive for `Security/YAMLLoad` when using Ruby 3.1+ (Psych 4). ([@koic][])
* [#10446](https://github.com/rubocop/rubocop/pull/10446): `Lint/RedundantDirGlobSort` unset SafeAutoCorrect. ([@friendlyantz][])
* [#10403](https://github.com/rubocop/rubocop/issues/10403): Fix an error for `Style/StringConcatenation` when string concatenation with multiline heredoc text. ([@koic][])
* [#10432](https://github.com/rubocop/rubocop/pull/10432): Fix an error when using regexp with non-encoding option. ([@koic][])
* [#10415](https://github.com/rubocop/rubocop/issues/10415): Fix an error for `Lint/UselessTimes` when using `1.times` with method chain. ([@koic][])

### Changes

* [#10408](https://github.com/rubocop/rubocop/pull/10408): Mark `Lint/InheritException` as unsafe auto-correction. ([@koic][])
* [#10407](https://github.com/rubocop/rubocop/pull/10407): Change `EnforcedStyle` from `runtime_error` to `standard_error` for `Lint/InheritException`. ([@koic][])
* [#10414](https://github.com/rubocop/rubocop/pull/10414): Update auto-gen-config's auto-correction comments to be more clear. ([@maxjacobson][])
* [#10427](https://github.com/rubocop/rubocop/issues/10427): Mark `Style/For` as unsafe auto-correction. ([@issyl0][])
* [#10410](https://github.com/rubocop/rubocop/issues/10410): Improve help string for `--fail-level` CLI option. ([@tejasbubane][])

## 1.25.1 (2022-02-03)

### Bug fixes

* [#10359](https://github.com/rubocop/rubocop/issues/10359): Fix a false positive and negative for `Style/HashSyntax` when using hash value omission. ([@koic][])
* [#10387](https://github.com/rubocop/rubocop/issues/10387): Fix an error for `Style/RedundantBegin` when assigning nested `begin` blocks. ([@koic][])
* [#10366](https://github.com/rubocop/rubocop/issues/10366): Fix a false positive for `Style/MethodCallWithArgsParentheses` when setting `EnforcedStyle: omit_parentheses` and using hash value omission with modifier from. ([@koic][])
* [#10376](https://github.com/rubocop/rubocop/issues/10376): Fix an error for `Layout/RescueEnsureAlignment` when using `.()` call with block. ([@koic][])
* [#10364](https://github.com/rubocop/rubocop/issues/10364): Fix an infinite loop error for `Layout/HashAlignment` when `EnforcedStyle: with_fixed_indentation` is specified for `Layout/ArgumentAlignment`. ([@koic][])
* [#10371](https://github.com/rubocop/rubocop/pull/10371): Fix a false negative for `Style/HashSyntax` when `Hash[foo: foo]` or `{foo: foo}` is followed by a next expression. ([@koic][])
* [#10394](https://github.com/rubocop/rubocop/issues/10394): Fix an error for `Style/SwapValues` when assigning receiver object at `def`. ([@koic][])
* [#10379](https://github.com/rubocop/rubocop/issues/10379): Fix an error for `Layout/EmptyLinesAroundExceptionHandlingKeywords` when `rescue` and `end` are on the same line. ([@koic][])

## 1.25.0 (2022-01-18)

### New features

* [#10351](https://github.com/rubocop/rubocop/pull/10351): Support `EnforcedShorthandSyntax: either` option for `Style/HashSyntax`. ([@koic][])
* [#10339](https://github.com/rubocop/rubocop/issues/10339): Support auto-correction for `EnforcedStyle: explicit` of `Naming/BlockForwarding`. ([@koic][])

### Bug fixes

* [#10344](https://github.com/rubocop/rubocop/pull/10344): Fix a false positive for `Style/CollectionCompact` when without receiver for bad methods. ([@koic][])
* [#10353](https://github.com/rubocop/rubocop/pull/10353): Use `:ambiguous_regexp` to detect ambiguous Regexp in Ruby 3. ([@danieldiekmeier][], [@joergschiller][])
* [#10336](https://github.com/rubocop/rubocop/issues/10336): Fix a false positive for `Style/TernaryParentheses` when using `in` keyword pattern matching as a ternary condition. ([@koic][])
* [#10317](https://github.com/rubocop/rubocop/issues/10317): Fix a false positive for `Style/MethodCallWithArgsParentheses` when using hash value omission. ([@koic][])
* [#8032](https://github.com/rubocop/rubocop/issues/8032): Improve ArgumentAlignment detection and correction for keyword arguments. ([@mvz][])
* [#10331](https://github.com/rubocop/rubocop/pull/10331): Fix cop generator for nested departments. ([@fatkodima][])
* [#10357](https://github.com/rubocop/rubocop/pull/10357): Fix a false positive for `Style/HashSyntax` when omitting the value. ([@berkos][])
* [#10335](https://github.com/rubocop/rubocop/issues/10335): Fix a false positive for `Naming/BlockForwarding` when using multiple proc arguments. ([@koic][])
* [#10350](https://github.com/rubocop/rubocop/pull/10350): Fix a false negative for `Lint/IncompatibleIoSelectWithFiberScheduler` when using `IO.select` with the first argument only. ([@koic][])
* [#10358](https://github.com/rubocop/rubocop/pull/10358): Fix `Style/Sample` crash on beginless and endless range shuffle indexes. ([@gsamokovarov][])
* [#10354](https://github.com/rubocop/rubocop/pull/10354): Fix `Gemspec/RequiredRubyVersion` version matcher when Gem::Requirement.new is used and initialised with multiple requirements. ([@nickpellant][])

### Changes

* [#10343](https://github.com/rubocop/rubocop/pull/10343): Require Parser 3.1.0.0 or higher. ([@koic][])

## 1.24.1 (2021-12-31)

### Bug fixes

* [#10313](https://github.com/rubocop/rubocop/issues/10313): Fix autocorrect `Style/MapToHash` with multiline code. ([@tejasbubane][])
* [#10251](https://github.com/rubocop/rubocop/issues/10251): Fix an incorrect autocorrect for `Gemspec/RequireMFA` when .gemspec file contains `metadata` keys assignments. ([@fatkodima][])
* [#10329](https://github.com/rubocop/rubocop/issues/10329): Fix a false positive for `Lint/ParenthesesAsGroupedExpression` and an incorrect autocorrect for the cop with `Style/TernaryParentheses` when using ternary expression as a first argument. ([@koic][])
* [#10317](https://github.com/rubocop/rubocop/issues/10317): Fix a false positive for `Style/MethodCallWithArgsParentheses` when using hash value omission. ([@koic][])
* [#10333](https://github.com/rubocop/rubocop/pull/10333): Fix an incorrect autocorrect for `Naming/BlockForwarding` using explicit block forwarding without method definition parentheses. ([@koic][])
* [#10321](https://github.com/rubocop/rubocop/issues/10321): Make `Style/MethodDefParentheses` aware of Ruby 3.1's anonymous block forwarding. ([@koic][])
* [#10320](https://github.com/rubocop/rubocop/issues/10320): Fix an incorrect autocorrect for `Style/FileWrite` when using heredoc argument. ([@koic][])
* [#10319](https://github.com/rubocop/rubocop/issues/10319): Require rubocop-ast 1.15.1 to fix a false positive for `Style/CombinableLoops` when the same method with different arguments and safe navigation. ([@koic][])

## 1.24.0 (2021-12-23)

### New features

* [#10279](https://github.com/rubocop/rubocop/pull/10279): Support Ruby 3.1's anonymous block forwarding syntax. ([@koic][])
* [#10295](https://github.com/rubocop/rubocop/pull/10295): Support Ruby 3.1's hash value omission syntax for `Layout/HashAlignment`. ([@koic][])
* [#10303](https://github.com/rubocop/rubocop/issues/10303): Add `AllowedNumbers` option to `Style/NumericLiterals`. ([@koic][])
* [#10290](https://github.com/rubocop/rubocop/pull/10290): Add new `Naming/BlockForwarding` cop. ([@koic][])
* [#10289](https://github.com/rubocop/rubocop/pull/10289): Add `EnforcedShorthandSyntax` option to `Style/HashSyntax` cop to support Ruby 3.1's hash value omission syntax by default. ([@koic][])
* [#10257](https://github.com/rubocop/rubocop/pull/10257): Add new `Style/MapToHash` cop. ([@dvandersluis][])
* [#10261](https://github.com/rubocop/rubocop/pull/10261): Add new `Style/FileRead` cop. ([@leoarnold][])
* [#10291](https://github.com/rubocop/rubocop/pull/10291): Support Ruby 3.1's hash value omission syntax for `Layout/SpaceAfterColon`. ([@koic][])
* [#10260](https://github.com/rubocop/rubocop/pull/10260): Add new `Style/FileWrite` cop. ([@leoarnold][])
* [#10307](https://github.com/rubocop/rubocop/pull/10307): Support Ruby 2.7's numbered parameter for `Metrics/BlockLength`, `Metrics/ClassLength`, `Metrics/MethodLength`, and `Metrics/ModuleLength` cops. ([@koic][])
* [#7671](https://github.com/rubocop/rubocop/issues/7671): Add cli option `--show-docs-url` to print out documentation url for given cops. ([@HeroProtagonist][])
* [#10308](https://github.com/rubocop/rubocop/pull/10308): Make `Style/CollectionCompact` aware of block pass argument. ([@koic][])

### Bug fixes

* [#10285](https://github.com/rubocop/rubocop/issues/10285): Fix an incorrect autocorrect for `Style/SoleNestedConditional` when using nested `if` within `if foo = bar`. ([@koic][])
* [#10309](https://github.com/rubocop/rubocop/pull/10309): Fix a false positive for `Bundler/DuplicatedGem` when a gem conditionally duplicated within multi-statement bodies. ([@fatkodima][])
* [#10300](https://github.com/rubocop/rubocop/issues/10300): Fix an incorrect autocorrect for `Layout/DotPosition` and `Style/RedundantSelf` when auto-correction conflicts. ([@koic][])
* [#10284](https://github.com/rubocop/rubocop/issues/10284): Fix an incorrect autocorrect for `Style/RedundantRegexpCharacterClass` when regexp containing an unescaped `#`. ([@koic][])
* [#10265](https://github.com/rubocop/rubocop/issues/10265): Fix `Style/IfInsideElse` to be able to handle `if-then` nested inside an `else` without clobbering. ([@dvandersluis][])
* [#10297](https://github.com/rubocop/rubocop/issues/10297): Fix a false positive for `Lint/DeprecatedOpenSSLConstant` when building digest using an algorithm string and nested digest constants. ([@koic][])
* [#10282](https://github.com/rubocop/rubocop/issues/10282): Fix an incorrect autocorrect for `Style/EmptyCaseCondition` when using `when ... then` in `case` in a method call. ([@koic][])
* [#10273](https://github.com/rubocop/rubocop/issues/10273): Fix a false positive for `InternalAffairs/UndefinedConfig` to suppress a false wrong namespace warning. ([@koic][])
* [#10305](https://github.com/rubocop/rubocop/issues/10305): Fix an incorrect autocorrect for `Style/HashConversion` when using `Hash[a || b]`. ([@koic][])
* [#10264](https://github.com/rubocop/rubocop/pull/10264): Fix the following incorrect auto-correct for `Style/MethodCallWithArgsParentheses` with `Layout/SpaceBeforeFirstArg`. ([@koic][])
* [#10276](https://github.com/rubocop/rubocop/issues/10276): Fix an incorrect autocorrect for `Style/RedundantInterpolation` when using a method call without parentheses in string interpolation. ([@koic][])

### Changes

* [#10253](https://github.com/rubocop/rubocop/pull/10253): Deprecate `RuboCop::Cop::EnforceSuperclass` module. ([@koic][])
* [#10248](https://github.com/rubocop/rubocop/pull/10248): Make `Lint/DeprecatedClassMethods` aware of `ENV.freeze`. ([@koic][])
* [#10269](https://github.com/rubocop/rubocop/issues/10269): Mark `Lint/IncompatibleIoSelectWithFiberScheduler` as unsafe auto-correction. ([@koic][])
* [#8586](https://github.com/rubocop/rubocop/issues/8586): Add configuration parameter `AllowForAlignment` in `Layout/CommentIndentation`. ([@jonas054][])

## 1.23.0 (2021-11-15)

### New features

* [#10202](https://github.com/rubocop/rubocop/issues/10202): Add new `Lint/UselessRuby2Keywords` cop. ([@dvandersluis][])
* [#10217](https://github.com/rubocop/rubocop/pull/10217): Add new `Style/OpenStructUse` cop. ([@mttkay][])
* [#10243](https://github.com/rubocop/rubocop/pull/10243): Add new `Gemspec/RequireMFA` cop. ([@dvandersluis][])

### Bug fixes

* [#10203](https://github.com/rubocop/rubocop/issues/10203): Fix `Style/FormatStringToken` to respect `IgnoredMethods` with nested structures. ([@tejasbubane][])
* [#10242](https://github.com/rubocop/rubocop/pull/10242): Fix `last_column` value for `JSONFormatter`. ([@koic][])
* [#10229](https://github.com/rubocop/rubocop/pull/10229): Fix a false positive for `Style/StringLiterals` when `EnforcedStyle: double_quotes` and using single quoted string with backslash. ([@koic][])
* [#10174](https://github.com/rubocop/rubocop/issues/10174): Fix inherit_from_remote should follow remote includes path starting with `./`. ([@hirasawayuki][])
* [#10234](https://github.com/rubocop/rubocop/pull/10234): Fix an error for `Style/Documentation` when using a cbase class. ([@koic][])
* [#10227](https://github.com/rubocop/rubocop/issues/10227): Fix a false positive for `Style/ParenthesesAroundCondition` when parentheses in multiple expressions separated by semicolon. ([@koic][])
* [#10230](https://github.com/rubocop/rubocop/issues/10230): Fix a false positive for `Lint/AmbiguousRange` when a range is composed of all literals except basic literals. ([@koic][])

### Changes

* [#10221](https://github.com/rubocop/rubocop/issues/10221): Update `Naming::FileName` to recognize `Struct`s as classes that satisfy the `ExpectMatchingDefinition` requirement. ([@dvandersluis][])
* [#10220](https://github.com/rubocop/rubocop/issues/10220): Update `Naming/FileName` to make `CheckDefinitionPathHierarchy` roots configurable. ([@grosser][])
* [#10199](https://github.com/rubocop/rubocop/pull/10199): Change `AllowAdjacentOneLineDefs` config parameter of `Layout/EmptyLineBetweenDefs` to `true` by default . ([@koic][])
* [#10236](https://github.com/rubocop/rubocop/pull/10236): Make `Lint/NumberConversion` aware of `to_r`. ([@koic][])

## 1.22.3 (2021-10-27)

### Bug fixes

* [#10166](https://github.com/rubocop/rubocop/pull/10166): Fix a false positive for `Style/StringLiterals` when using some meta characters (e.g. `'\s'`, `'\z'`) with `EnforcedStyle: double_quotes`. ([@koic][])
* [#10216](https://github.com/rubocop/rubocop/issues/10216): Fix an incorrect autocorrect for `Style/SelectByRegexp` when using `lvar =~ blockvar` in a block. ([@koic][])
* [#10207](https://github.com/rubocop/rubocop/pull/10207): Fix false positive in `Layout/DotPosition` when the selector is on the same line as the closing bracket of the receiver. ([@mvz][])

### Changes

* [#10209](https://github.com/rubocop/rubocop/pull/10209): Make `Lint/DeprecatedConstants` aware of `Net::HTTPServerException`. ([@koic][])

## 1.22.2 (2021-10-22)

### Bug fixes

* [#10165](https://github.com/rubocop/rubocop/issues/10165): Fix `Layout/DotPosition` false positives when the selector and receiver are on the same line. ([@dvandersluis][])
* [#10171](https://github.com/rubocop/rubocop/pull/10171): Fix `Style/HashTransformKeys` and `Style/HashTransformValues` incorrect auto-correction when inside block body. ([@franzliedke][])
* [#10180](https://github.com/rubocop/rubocop/issues/10180): Fix an error for `Style/SelectByRegexp` when using `match?` without a receiver. ([@koic][])
* [#10193](https://github.com/rubocop/rubocop/pull/10193): Fix an error for `Layout/EmptyLinesAroundExceptionHandlingKeywords` when `begin` and `rescue` are on the same line. ([@koic][])
* [#10185](https://github.com/rubocop/rubocop/issues/10185): Fix a false positive for `Lint/AmbiguousRange` when using `self` in a range literal. ([@koic][])
* [#10200](https://github.com/rubocop/rubocop/issues/10200): Fix an error when inspecting a directory named `*`. ([@koic][])
* [#10149](https://github.com/rubocop/rubocop/pull/10149): Fix `Bundler/GemComment` where it would not detect an offense in some cases when `OnlyFor` is set to `restrictive_version_specifiers`. ([@Drowze][])

### Changes

* [#10157](https://github.com/rubocop/rubocop/pull/10157): Updated `Gemspec/RequiredRubyVersion` handle being set to blank values. ([@dvandersluis][])
* [#10176](https://github.com/rubocop/rubocop/pull/10176): Unmark `AutoCorrect: false` from `Security/JSONLoad`. ([@koic][])
* [#10186](https://github.com/rubocop/rubocop/issues/10186): Explicit block arg is not counted for `Metrics/ParameterLists`. ([@koic][])

## 1.22.1 (2021-10-04)

### Bug fixes

* [#10143](https://github.com/rubocop/rubocop/issues/10143): Fix an error for `Lint/RequireRelativeSelfPath` when using a variable as an argument of `require_relative`. ([@koic][])
* [#10140](https://github.com/rubocop/rubocop/issues/10140): Fix false positive for `Layout/DotPosition` when a heredoc receives a method on the same line as the start sigil in `trailing` style. ([@dvandersluis][])
* [#10148](https://github.com/rubocop/rubocop/issues/10148): Fix `Style/QuotedSymbols` handling escaped characters incorrectly. ([@dvandersluis][])
* [#10145](https://github.com/rubocop/rubocop/issues/10145): Update `Style/SelectByRegexp` to ignore cases where the receiver appears to be a hash. ([@dvandersluis][])

## 1.22.0 (2021-09-29)

### New features

* [#8431](https://github.com/rubocop/rubocop/issues/8431): Add `Safety` section to documentation for all cops that are `Safe: false` or `SafeAutoCorrect: false`. ([@dvandersluis][])
* [#10132](https://github.com/rubocop/rubocop/issues/10132): Reorganize output of `rubocop --help` for better clarity. ([@dvandersluis][])
* [#10111](https://github.com/rubocop/rubocop/pull/10111): Add new `Style/NumberedParametersLimit` cop. ([@dvandersluis][])
* [#10025](https://github.com/rubocop/rubocop/pull/10025): Changed cop `SpaceInsideParens` to include a `compact` style. ([@itay-grudev][])
* [#10084](https://github.com/rubocop/rubocop/issues/10084): Add new `Lint/RequireRelativeSelfPath` cop. ([@koic][])
* [#8327](https://github.com/rubocop/rubocop/issues/8327): Add new cop `Style/SelectByRegexp`. ([@dvandersluis][])
* [#10100](https://github.com/rubocop/rubocop/pull/10100): Add new `Style/NumberedParameters` cop. ([@Hugo-Hache][])
* [#10103](https://github.com/rubocop/rubocop/issues/10103): Add `AllowHttpProtocol` option to `Bundler/InsecureProtocolSource`. ([@koic][])
* [#10102](https://github.com/rubocop/rubocop/pull/10102): Add new `Security/IoMethods` cop. ([@koic][])

### Bug fixes

* [#10110](https://github.com/rubocop/rubocop/issues/10110): Update `Layout/DotPosition` to be able to handle heredocs. ([@dvandersluis][])
* [#10134](https://github.com/rubocop/rubocop/issues/10134): Update `Style/MutableConstant` to not consider multiline uninterpolated strings as unfrozen in ruby 3.0. ([@dvandersluis][])
* [#10124](https://github.com/rubocop/rubocop/pull/10124): Fix `Layout/RedundantLineBreak` adding extra space within method chains. ([@dvandersluis][])
* [#10118](https://github.com/rubocop/rubocop/issues/10118): Fix crash with `Style/RedundantSort` when the block doesn't only contain a single `send` node. ([@dvandersluis][])
* [#10135](https://github.com/rubocop/rubocop/issues/10135): Fix `Style/WordArray` to exclude files in `--auto-gen-config` when `percent` style is given but brackets are required. ([@dvandersluis][])
* [#10090](https://github.com/rubocop/rubocop/issues/10090): Fix a false negative for `Style/ArgumentsForwarding` when using only kwrest arg. ([@koic][])
* [#10099](https://github.com/rubocop/rubocop/pull/10099): Update`Style/RedundantFreeze` to stop considering `ENV` values as immutable. ([@byroot][])
* [#10078](https://github.com/rubocop/rubocop/pull/10078): Fix `Layout/LineLength` reported length when ignoring directive comments. ([@dvandersluis][])
* [#9934](https://github.com/rubocop/rubocop/issues/9934): Fix configuration loading to not raise an error for an obsolete ruby version that is subsequently overridden. ([@dvandersluis][])
* [#10136](https://github.com/rubocop/rubocop/issues/10136): Update `Lint/AssignmentInCondition` to not consider assignments within blocks in conditions. ([@dvandersluis][])
* [#9588](https://github.com/rubocop/rubocop/issues/9588): Fix causing a variable to be shadowed from outside the rescue block in the logic of `Naming/RescuedExceptionsVariableName`. ([@lilisako][])
* [#10096](https://github.com/rubocop/rubocop/issues/10096): Fix `Lint/AmbiguousOperatorPrecedence` with `and`/`or` operators. ([@dvandersluis][])
* [#10106](https://github.com/rubocop/rubocop/issues/10106): Fix `Style/RedundantSelf` for pattern matching. ([@dvandersluis][])
* [#10066](https://github.com/rubocop/rubocop/issues/10066): Fix how `MinDigits` is calculated for `Style/NumericLiterals` when generating a configuration file. ([@dvandersluis][])

### Changes

* [#10088](https://github.com/rubocop/rubocop/pull/10088): Update `Lint/BooleanSymbol` to be `SafeAutoCorrect: false` rather than `Safe: false`. ([@dvandersluis][])
* [#10122](https://github.com/rubocop/rubocop/pull/10122): Update `Style/RedundantSort` to be unsafe, and revert the special case for `size` from [#10061](https://github.com/rubocop/rubocop/pull/10061). ([@dvandersluis][])
* [#10130](https://github.com/rubocop/rubocop/issues/10130): Update `Lint/ElseLayout` to be able to handle an `else` with only a single line. ([@dvandersluis][])

## 1.21.0 (2021-09-13)

### New features

* [#7849](https://github.com/rubocop/rubocop/issues/7849): Add new `Lint/AmbiguousOperatorPrecedence` cop. ([@dvandersluis][])
* [#9061](https://github.com/rubocop/rubocop/issues/9061): Add new `Lint/IncompatibleIoSelectWithFiberScheduler` cop. ([@koic][])

### Bug fixes

* [#10067](https://github.com/rubocop/rubocop/pull/10067): Fix an error for `Lint/NumberConversion` when using nested number conversion methods. ([@koic][])
* [#10054](https://github.com/rubocop/rubocop/pull/10054): Fix a false positive for `Layout/SpaceAroundOperators` when match operators between `<<` and `+=`. ([@koic][])
* [#10061](https://github.com/rubocop/rubocop/issues/10061): Fix a false positive for `Style/RedundantSort` when using `size` method in the block. ([@koic][])
* [#10063](https://github.com/rubocop/rubocop/pull/10063): Fix a false positive for `Layout/SingleLineBlockChain` when method call chained on a new line after a single line block with trailing dot. ([@koic][])
* [#10064](https://github.com/rubocop/rubocop/pull/10064): Fix `Style/ExplicitBlockArgument` corrector assuming any existing block argument was named `block`. ([@byroot][])
* [#10070](https://github.com/rubocop/rubocop/issues/10070): Fix a false positive for `Style/MutableConstant` when using non-interpolated heredoc in Ruby 3.0. ([@koic][])

### Changes

* [#9674](https://github.com/rubocop/rubocop/issues/9674): Disable `Style/AsciiComments` by default. ([@dvandersluis][])
* [#10051](https://github.com/rubocop/rubocop/pull/10051): Improve the messaging for `Style/Documentation` to be more clear about what class/module needs documentation. ([@dvandersluis][])
* [#10074](https://github.com/rubocop/rubocop/pull/10074): Update `Naming/InclusiveLanguage` to be disabled by default. ([@dvandersluis][])
* [#10068](https://github.com/rubocop/rubocop/pull/10068): Mark `Style/AndOr` as unsafe auto-correction. ([@koic][])

## 1.20.0 (2021-08-26)

### New features

* [#10040](https://github.com/rubocop/rubocop/pull/10040): Make `Lint/Debugger` aware of debug.rb. ([@koic][])
* [#9580](https://github.com/rubocop/rubocop/issues/9580): Add a new cop that enforces which bundler gem file to use. ([@gregfletch][])

### Bug fixes

* [#10033](https://github.com/rubocop/rubocop/issues/10033): Fix an incorrect auto-correct for `Style/BlockDelimiters` when there is a comment after the closing brace and using method chaining. ([@koic][])
* [#6630](https://github.com/rubocop/rubocop/issues/6630): Updated `Style/CommentAnnotation` to be able to handle multiword keyword phrases. ([@dvandersluis][])
* [#7836](https://github.com/rubocop/rubocop/issues/7836): Update `Style/BlockDelimiters` to add `begin`...`end` when converting a block containing `rescue` or `ensure` to braces. ([@dvandersluis][])
* [#10031](https://github.com/rubocop/rubocop/issues/10031): Fix a false positive for `Style/HashExcept` when comparing with hash value. ([@koic][])

### Changes

* [#10034](https://github.com/rubocop/rubocop/pull/10034): Add `RubyJard` debugger calls to `DebuggerMethods` of `Lint/Debugger`. ([@DanielVartanov][])
* [#10006](https://github.com/rubocop/rubocop/pull/10006): Interpolated string literals are no longer frozen since Ruby 3.0. ([@splattael][])
* [#9328](https://github.com/rubocop/rubocop/issues/9328): Recognize shareable_constant_value magic comment. ([@thearjunmdas][], [@caalberts][])
* [#10036](https://github.com/rubocop/rubocop/issues/10036): Mark `Style/StructInheritance` as unsafe auto-correction. ([@koic][])

## 1.19.1 (2021-08-19)

### Bug fixes

* [#10017](https://github.com/rubocop/rubocop/pull/10017): Fix an error for `Layout/RescueEnsureAlignment` when using zsuper with block. ([@koic][])
* [#10011](https://github.com/rubocop/rubocop/issues/10011): Fix a false positive for `Style/RedundantSelfAssignmentBranch` when using instance variable, class variable, and global variable. ([@koic][])
* [#10010](https://github.com/rubocop/rubocop/issues/10010): Fix a false positive for `Style/DoubleNegation` when `!!` is used at return location and before `rescue` keyword. ([@koic][])
* [#10014](https://github.com/rubocop/rubocop/issues/10014): Fix `Style/Encoding` to handle more situations properly. ([@dvandersluis][])
* [#10016](https://github.com/rubocop/rubocop/issues/10016): Fix conflict between `Style/SoleNestedConditional` and `Style/NegatedIf`/`Style/NegatedUnless`. ([@dvandersluis][])
* [#10024](https://github.com/rubocop/rubocop/issues/10024): Fix an incorrect auto-correct for `Style/RedundantSelfAssignmentBranch` when using multiline `if` / `else` conditional assignment. ([@koic][])
* [#10004](https://github.com/rubocop/rubocop/issues/10004): Fix a false positive for `Style/RedundantBegin` when using one-liner with semicolon. ([@koic][])

## 1.19.0 (2021-08-12)

### New features

* [#4182](https://github.com/rubocop/rubocop/issues/4182): Add `Lint/AmbiguousRange` cop to check for ranges with ambiguous boundaries. ([@dvandersluis][])
* [#10000](https://github.com/rubocop/rubocop/pull/10000): Parallel static analysis by default. ([@koic][])
* [#9948](https://github.com/rubocop/rubocop/pull/9948): Support Ruby 2.7's pattern matching for `Style/ConditionalAssignment` cop. ([@koic][])
* [#9999](https://github.com/rubocop/rubocop/pull/9999): Add new `Style/RedundantSelfAssignmentBranch` cop. ([@koic][])

### Bug fixes

* [#9927](https://github.com/rubocop/rubocop/issues/9927): Indent hash values in `Layout/LineEndStringConcatenationIndentation`. ([@jonas054][])
* [#9959](https://github.com/rubocop/rubocop/issues/9959): Make `Style/IdenticalConditionalBranches` able to handle ternary `if`s. ([@dvandersluis][])
* [#9946](https://github.com/rubocop/rubocop/issues/9946): Avoid slow regexp matches in `Style/CommentedKeyword`. ([@jonas054][])
* [#7422](https://github.com/rubocop/rubocop/issues/7422): Treat constant assignment like other assignment in `Layout/SpaceAroundOperators`. ([@dvandersluis][])
* [#9953](https://github.com/rubocop/rubocop/issues/9953): Fix an infinite loop error and a false auto-correction behavior for `Layout/EndAlignment` when using a conditional statement in a method argument. ([@koic][])
* [#9958](https://github.com/rubocop/rubocop/issues/9958): Prevent an infinite loop when a detected method has fewer arguments than expected. ([@dvandersluis][])
* [#9977](https://github.com/rubocop/rubocop/issues/9977): Update `Layout/EmptyLineAfterGuardClause` to not register an offense if there is another expression following the guard clause on the same line. ([@dvandersluis][])
* [#9980](https://github.com/rubocop/rubocop/issues/9980): Fix a false positive for `Style/IdenticalConditionalBranches` when assigning to a variable used in a condition. ([@koic][])
* [#9975](https://github.com/rubocop/rubocop/issues/9975): Parentheses are always required for `Style/MethodDefParentheses` when a forwarding argument (`...`) is used. ([@dvandersluis][])
* [#9984](https://github.com/rubocop/rubocop/pull/9984): Fix false negatives involving heredocs for `Layout/SpaceBeforeComma`, `Layout/SpaceBeforeComment`, `Layout/SpaceBeforeSemicolon` and `Layout/SpaceInsideParens`. ([@dvandersluis][])
* [#9954](https://github.com/rubocop/rubocop/issues/9954): Fix infinite loop error for `Layout/HashAlignment` when `EnforcedStyle: with_fixed_indentation` is specified for `Layout/ArgumentAlignment`. ([@koic][])
* [#10002](https://github.com/rubocop/rubocop/issues/10002): Fix an incorrect auto-correct for `Lint/AmbiguousRegexpLiteral` when using nested method arguments without parentheses. ([@koic][])
* [#9952](https://github.com/rubocop/rubocop/pull/9952) [rubocop-rspec#1126](https://github.com/rubocop/rubocop-rspec/issues/1126): Fix `inherit_mode` for deeply nested configuration defined in extensions' default configuration. ([@pirj][])
* [#9957](https://github.com/rubocop/rubocop/issues/9957): Add `WholeWord` configuration to `Naming/InclusiveLanguage`'s `FlaggedTerms` config. ([@dvandersluis][])
* [#9970](https://github.com/rubocop/rubocop/pull/9970): Don't register an offense when sort method has arguments for `Style/RedundantSort` cop. ([@mtsmfm][])
* [#4097](https://github.com/rubocop/rubocop/issues/4097): Add require English for special globals. ([@biinari][])
* [#9955](https://github.com/rubocop/rubocop/issues/9955): Fix `Style/ExplicitBlockArgument` adding a second set of parentheses. ([@dvandersluis][])
* [#9973](https://github.com/rubocop/rubocop/issues/9973): Fix a false positive for `Layout/RescueEnsureAlignment` when aligned `rescue` keyword and leading dot. ([@koic][])
* [#9945](https://github.com/rubocop/rubocop/issues/9945): Fix auto-correction of lines in heredocs with only spaces in `Layout/TrailingWhitespace`. ([@jonas054][])

### Changes

* [#9989](https://github.com/rubocop/rubocop/issues/9989): Mark `Style/CommentedKeyword` as unsafe auto-correction. ([@koic][])
* [#9964](https://github.com/rubocop/rubocop/pull/9964): Make `Layout/LeadingCommentSpace` aware of `#:nodoc`. ([@koic][])
* [#9985](https://github.com/rubocop/rubocop/pull/9985): Mark `Style/IdenticalConditionalBranches` as unsafe auto-correction. ([@koic][])
* [#9962](https://github.com/rubocop/rubocop/issues/9962): Update `Style/WordArray` to register an offense in `percent` style if any values contain spaces. ([@dvandersluis][])
* [#9979](https://github.com/rubocop/rubocop/pull/9979): Enable basic autocorrection for `Style/Semicolon`. ([@dvandersluis][])

## 1.18.4 (2021-07-23)

### New features

* [#9930](https://github.com/rubocop/rubocop/pull/9930): Support Ruby 2.7's pattern matching for `Lint/DuplicateBranch` cop. ([@koic][])

### Bug fixes

* [#9938](https://github.com/rubocop/rubocop/pull/9938): Fix an incorrect auto-correct for `Layout/LineLength` when a heredoc is used as the first element of an array. ([@koic][])
* [#9940](https://github.com/rubocop/rubocop/issues/9940): Fix an incorrect auto-correct for `Style/HashTransformValues` when value is a hash literal for `_.to_h{...}`. ([@koic][])
* [#9752](https://github.com/rubocop/rubocop/issues/9752): Improve error message for top level department used in configuration. ([@jonas054][])
* [#9933](https://github.com/rubocop/rubocop/pull/9933): Fix GitHub Actions formatter when running in non-default directory. ([@ojab][])
* [#9922](https://github.com/rubocop/rubocop/issues/9922): Make better auto-corrections in `Style/DoubleCopDisableDirective`. ([@jonas054][])
* [#9848](https://github.com/rubocop/rubocop/issues/9848): Fix handling of comments in `Layout/ClassStructure` auto-correct. ([@jonas054][])
* [#9926](https://github.com/rubocop/rubocop/pull/9926): Fix an incorrect auto-correct for `Style/SingleLineMethods` when method body is enclosed in parentheses. ([@koic][])
* [#9928](https://github.com/rubocop/rubocop/issues/9928): Fix an infinite loop error and a false auto-correction behavior for `Layout/EndAlignment` when using operator methods and `EnforcedStyleAlignWith: variable`. ([@koic][])
* [#9434](https://github.com/rubocop/rubocop/issues/9434): Fix false positive for setter calls in `Layout/FirstArgumentIndentation`. ([@jonas054][])

## 1.18.3 (2021-07-06)

### Bug fixes

* [#9891](https://github.com/rubocop/rubocop/issues/9891): Fix `--auto-gen-config` bug for `Style/HashSyntax`. ([@jonas054][])
* [#9905](https://github.com/rubocop/rubocop/issues/9905): Fix false positive for single line concatenation in `Layout/LineEndStringConcatenationIndentation`. ([@jonas054][])
* [#9907](https://github.com/rubocop/rubocop/issues/9907): Fix an incorrect auto-correct for `Lint/UselessTimes` when using block argument for `1.times`. ([@koic][])
* [#9869](https://github.com/rubocop/rubocop/issues/9869): Fix reference to file in configuration override warning. ([@jonas054][])
* [#9902](https://github.com/rubocop/rubocop/issues/9902): Fix an incorrect auto-correct for `Style/BlockDelimiters` when there is a comment after the closing brace. ([@koic][])
* [#8469](https://github.com/rubocop/rubocop/issues/8469): Add inspection of `class <<` to `Layout/SpaceAroundOperators`. ([@jonas054][])
* [#9909](https://github.com/rubocop/rubocop/pull/9909): This PR fixes an incorrect auto-correct for `Style/SingleLineMethods` when using `return`, `break`, or `next` for one line method body in Ruby 3.0. ([@koic][])
* [#9914](https://github.com/rubocop/rubocop/issues/9914): Fix an error for `Layout/HashAlignment` when using aligned hash argument for `proc.()`. ([@koic][])

## 1.18.2 (2021-07-02)

### Bug fixes

* [#9894](https://github.com/rubocop/rubocop/issues/9894): Handle multiline string literals in `Layout/LineEndStringConcatenationIndentation`. ([@jonas054][])
* [#9890](https://github.com/rubocop/rubocop/issues/9890): Make colon after comment annotation configurable. ([@gregfletch][])

## 1.18.1 (2021-06-30)

### Bug fixes

* [#9897](https://github.com/rubocop/rubocop/pull/9897): Fix an incorrect auto-correct for `Layout/HashAlignment` when setting `EnforcedStyle: with_fixed_indentation` of `Layout/ArgumentAlignment` and using misaligned keyword arguments. ([@koic][])

### Changes

* [#9895](https://github.com/rubocop/rubocop/issues/9895): Set `CheckStrings: false` and Remove `master` from `FlaggedTerms` for `Naming/InclusiveLanguage`. ([@koic][])

## 1.18.0 (2021-06-29)

### New features

* [#9842](https://github.com/rubocop/rubocop/pull/9842): Add new `Naming/InclusiveLanguage` cop. ([@tjwp][])

### Bug fixes

* [#9803](https://github.com/rubocop/rubocop/pull/9803): Fix `Bundler/GemVersion` cop not respecting git tags. ([@tejasbubane][], [@timlkelly][])
* [#9882](https://github.com/rubocop/rubocop/pull/9882): Fix an incorrect auto-correct for `Layout/LineLength` when using heredoc as the first method argument and omitting parentheses. ([@koic][])
* [#7592](https://github.com/rubocop/rubocop/pull/7592): Add cop `Layout/LineEndStringConcatenationIndentation`. ([@jonas054][])
* [#9880](https://github.com/rubocop/rubocop/pull/9880): Fix a false positive for `Style/RegexpLiteral` when using a regexp starts with a blank as a method argument. ([@koic][])
* [#9888](https://github.com/rubocop/rubocop/pull/9888): Fix a false positive for `Layout/ClosingParenthesisIndentation` when using keyword arguments. ([@koic][])
* [#9886](https://github.com/rubocop/rubocop/pull/9886): Fix indentation in `Style/ClassAndModuleChildren`. ([@markburns][])

### Changes

* [#9144](https://github.com/rubocop/rubocop/issues/9144): Add `aggressive` and `conservative` modes of operation for `Style/StringConcatenation` cop. ([@tejasbubane][])

## 1.17.0 (2021-06-15)

### New features

* [#9626](https://github.com/rubocop/rubocop/pull/9626): Disable all cop department with directive comment. ([@AndreiEres][])
* [#9827](https://github.com/rubocop/rubocop/issues/9827): Add basic auth support to download raw yml config from private repo. ([@AirWick219][])
* [#9873](https://github.com/rubocop/rubocop/pull/9873): Support one-line pattern matching syntax for `Layout/SpaceAroundKeyword` and `Layout/SpaceAroundOperators`. ([@koic][])
* [#9857](https://github.com/rubocop/rubocop/pull/9857): Support Ruby 2.7's pattern matching for `Layout/IndentationWidth` cop. ([@koic][])
* [#9877](https://github.com/rubocop/rubocop/pull/9877): Support Ruby 2.7's `in` pattern syntax for `Lint/LiteralAsCondition`. ([@koic][])
* [#9855](https://github.com/rubocop/rubocop/pull/9855): Support Ruby 2.7's pattern matching for `Style/IdenticalConditionalBranches` cop. ([@koic][])

### Bug fixes

* [#9874](https://github.com/rubocop/rubocop/issues/9874): Fix a false positive for `Style/RegexpLiteral` when using `%r` regexp literal with `EnforcedStyle: omit_parentheses` of `Style/MethodCallWithArgsParentheses`. ([@koic][])
* [#9876](https://github.com/rubocop/rubocop/pull/9876): Fix empty line after guard clause with `and return` and heredoc. ([@AndreiEres][])
* [#9861](https://github.com/rubocop/rubocop/issues/9861): Fix error in `Layout/HashAlignment` with an empty hash literal. ([@dvandersluis][])
* [#9867](https://github.com/rubocop/rubocop/pull/9867): Fix an incorrect auto-correct for `Layout/DotPosition` when using only dot line. ([@koic][])

## 1.16.1 (2021-06-09)

### Bug fixes

* [#9843](https://github.com/rubocop/rubocop/issues/9843): Fix `Style/RedundantSelf` to allow conditional nodes to use `self` in the condition when a variable named is shadowed inside. ([@dvandersluis][])
* [#9845](https://github.com/rubocop/rubocop/issues/9845): Fix `Style/QuotedSymbols` for hash-rocket hashes. ([@dvandersluis][])
* [#9849](https://github.com/rubocop/rubocop/pull/9849): Fix a false negative for `Layout/HashAlignment` when setting `EnforcedStyle: with_fixed_indentation` of `Layout/ArgumentAlignment` and using misaligned keyword arguments. ([@koic][])
* [#9854](https://github.com/rubocop/rubocop/pull/9854): Allow braced numeric blocks in `omit_parentheses` style of `Style/MethodCallWithArgsParentheses`. ([@gsamokovarov][])
* [#9850](https://github.com/rubocop/rubocop/issues/9850): Fix missing `AllowComments` option for `Lint/EmptyInPattern`. ([@koic][])

## 1.16.0 (2021-06-01)

### New features

* [#9841](https://github.com/rubocop/rubocop/pull/9841): Support guard `if` and `unless` syntax keywords of Ruby 2.7's pattern matching for `Layout/SpaceAroundKeyword`. ([@koic][])
* [#9812](https://github.com/rubocop/rubocop/pull/9812): Support auto-correction for `Style/IdenticalConditionalBranches`. ([@koic][])
* [#9833](https://github.com/rubocop/rubocop/pull/9833): Add new `Style/InPatternThen` cop. ([@koic][])
* [#9840](https://github.com/rubocop/rubocop/issues/9840): Adds `AllowedReceivers` option for `Style/HashEachMethods`. ([@koic][])
* [#9818](https://github.com/rubocop/rubocop/pull/9818): Support Ruby 2.7's `in` pattern syntax for `Layout/CaseIndentation`. ([@koic][])
* [#9838](https://github.com/rubocop/rubocop/pull/9838): Support Ruby 2.7's pattern matching syntax for `Layout/SpaceAroundKeyword`. ([@koic][])
* [#9793](https://github.com/rubocop/rubocop/issues/9793): Add `Style/QuotedSymbols` to enforce consistency in quoted symbols. ([@dvandersluis][])
* [#9825](https://github.com/rubocop/rubocop/pull/9825): Add new `Lint/EmptyInPattern` cop. ([@koic][])
* [#9834](https://github.com/rubocop/rubocop/pull/9834): Add new `Style/MultilineInPatternThen` cop. ([@koic][])

### Bug fixes

* [#9822](https://github.com/rubocop/rubocop/issues/9822): Fix a false directive comment range for `Lint/RedundantCopDisableDirective`. ([@koic][])
* [#9819](https://github.com/rubocop/rubocop/issues/9819): Fix a false negative for `Style/TopLevelMethodDefinition` when defining a top-level method after a class definition. ([@koic][])
* [#9836](https://github.com/rubocop/rubocop/issues/9836): Fix incorrect corrections for `Layout/HashAlignment` when a `kwsplat` node is on the same line as a `pair` node with table style. ([@dvandersluis][])
* [#9805](https://github.com/rubocop/rubocop/pull/9805): Fix a false negative for `Layout/HashAlignment` when set `EnforcedStyle: with_fixed_indentation` of `ArgumentAlignment`. ([@koic][])
* [#9811](https://github.com/rubocop/rubocop/issues/9811): Fix an error for `Layout/ArgumentAlignment` with `Layout/FirstHashElementIndentation` when setting `EnforcedStyle: with_fixed_indentation`. ([@koic][])

### Changes

* [#9809](https://github.com/rubocop/rubocop/pull/9809): Change `Lint/SymbolConversion` to only quote with double quotes, since `Style/QuotedSymbols` can now correct those to the correct quotes as per configuration. ([@dvandersluis][])

## 1.15.0 (2021-05-17)

### New features

* [#9734](https://github.com/rubocop/rubocop/pull/9734): Add `Style/TopLevelMethodDefinition` cop. ([@tejasbubane][])
* [#9780](https://github.com/rubocop/rubocop/issues/9780): Support summary report for `JUnitFormatter`. ([@koic][])
* [#9798](https://github.com/rubocop/rubocop/pull/9798): Make `Layout/ArgumentAlignment` aware of kwargs. ([@koic][])

### Bug fixes

* [#9749](https://github.com/rubocop/rubocop/issues/9749): Fix autocorrection for `Layout/LineLength` to not move the first argument of an unparenthesized `send` node to the next line, which changes behaviour. ([@dvandersluis][])
* [#9799](https://github.com/rubocop/rubocop/issues/9799): Fix invalid line splitting by `Layout/LineLength` for `send` nodes with heredoc arguments. ([@dvandersluis][])
* [#9773](https://github.com/rubocop/rubocop/issues/9773): Fix `Style/EmptyLiteral` to not register offenses for `String.new` when `Style/FrozenStringLiteralComment` is enabled. ([@dvandersluis][])
* [#9771](https://github.com/rubocop/rubocop/issues/9771): Change `AllowDSLWriters` to true by default for `Style/TrivialAccessors`. ([@koic][])
* [#9777](https://github.com/rubocop/rubocop/pull/9777): Fix an incorrect auto-correct for `Style/RedundantBegin` when using multi-line `if` in `begin` block. ([@koic][])
* [#9791](https://github.com/rubocop/rubocop/pull/9791): Fix a false negative for `Layout/IndentationWidth` when using `ensure` in `do` ... `end` block. ([@koic][])
* [#9766](https://github.com/rubocop/rubocop/pull/9766): Fix a clobbering error for `Style/ClassAndModuleChildren` cop with compact style. ([@tejasbubane][])
* [#9767](https://github.com/rubocop/rubocop/issues/9767): Fix `Style/ClassAndModuleChildren` cop to preserve comments. ([@tejasbubane][])
* [#9792](https://github.com/rubocop/rubocop/issues/9792): Fix false positive for `Lint/Void` cop with ranges. ([@tejasbubane][])

### Changes

* [#9770](https://github.com/rubocop/rubocop/issues/9770): Update `Lint/EmptyBlock` to handle procs the same way as lambdas. ([@dvandersluis][])
* [#9776](https://github.com/rubocop/rubocop/pull/9776): Update `Style/NilLambda` to handle procs as well. ([@dvandersluis][])
* [#9744](https://github.com/rubocop/rubocop/pull/9744): The parallel flag will now be automatically ignored when combined with `--cache false`. Previously, an error was raised and execution stopped. ([@rrosenblum][])

## 1.14.0 (2021-05-05)

### New features

* [#7669](https://github.com/rubocop/rubocop/issues/7669): New cop `Bundler/GemVersion` requires or forbids specifying gem versions. ([@timlkelly][])
* [#9758](https://github.com/rubocop/rubocop/pull/9758): Support `TargetRubyVersion 3.1` (experimental). ([@koic][])
* [#9733](https://github.com/rubocop/rubocop/issues/9733): Add cop `Layout/SingleLineBlockChain`. ([@jonas054][])

### Bug fixes

* [#9751](https://github.com/rubocop/rubocop/pull/9751): `Style/StringLiterals` doesn't autocorrect global variable interpolation. ([@etiennebarrie][])
* [#9731](https://github.com/rubocop/rubocop/issues/9731): Fix two autocorrection issues for `Style/NegatedIfElseCondition`. ([@dvandersluis][])
* [#9740](https://github.com/rubocop/rubocop/pull/9740): Fix an incorrect auto-correct for `Style/SingleLineMethods` when defining setter method. ([@koic][])
* [#9757](https://github.com/rubocop/rubocop/pull/9757): Fix a false positive for `Lint/NumberConversion` when `:to_f` is one of multiple method arguments. ([@koic][])
* [#9761](https://github.com/rubocop/rubocop/issues/9761): Fix `Style/ClassAndModuleChildren` false negative for `compact` style when a class/module is partially nested. ([@dvandersluis][])
* [#9748](https://github.com/rubocop/rubocop/pull/9748): Prevent infinite loops during symlink traversal. ([@Tonkpils][])
* [#9762](https://github.com/rubocop/rubocop/issues/9762): Update `VariableForce` to be able to handle `case-match` nodes. ([@dvandersluis][])
* [#9729](https://github.com/rubocop/rubocop/issues/9729): Fix an error for `Style/IfUnlessModifier` when variable assignment is used in the branch body of if modifier. ([@koic][])
* [#9750](https://github.com/rubocop/rubocop/issues/9750): Fix an incorrect auto-correct for `Style/SoleNestedConditional` when using nested `if` within `unless foo == bar`. ([@koic][])
* [#9751](https://github.com/rubocop/rubocop/pull/9751): `Style/StringLiterals` autocorrects `'\\'` into `"\\"`. ([@etiennebarrie][])
* [#9732](https://github.com/rubocop/rubocop/pull/9732): Support deprecated Socket.gethostbyaddr and Socket.gethostbyname. ([@AndreiEres][])
* [#9713](https://github.com/rubocop/rubocop/issues/9713): Fix autocorrection for block local variables in `Lint/UnusedBlockArgument`. ([@tejasbubane][])
* [#9746](https://github.com/rubocop/rubocop/pull/9746): Fix a false positive for `Lint/UnreachableLoop` when using conditional `next` in a loop. ([@koic][])

## 1.13.0 (2021-04-20)

### New features

* [#7977](https://github.com/rubocop/rubocop/issues/7977): Add `Layout/RedundantLineBreak` cop. ([@jonas054][])
* [#9691](https://github.com/rubocop/rubocop/issues/9691): Add configuration parameter `InspectBlocks` to `Layout/RedundantLineBreak`. ([@jonas054][])
* [#9684](https://github.com/rubocop/rubocop/issues/9684): Support `IgnoredMethods` option for `Lint/AmbiguousBlockAssociation`. ([@gprado][])
* [#9358](https://github.com/rubocop/rubocop/pull/9358): Support `restrictive_version_specifiers` option in `Bundler/GemComment` cop. ([@RobinDaugherty][])

### Bug fixes

* [#5576](https://github.com/rubocop/rubocop/issues/5576): Fix problem with inherited `Include` parameters. ([@jonas054][])
* [#9690](https://github.com/rubocop/rubocop/pull/9690): Fix an incorrect auto-correct for `Style/IfUnlessModifier` when using a method with heredoc argument. ([@koic][])
* [#9681](https://github.com/rubocop/rubocop/issues/9681): Fix an incorrect auto-correct for `Style/RedundantBegin` when using modifier `if` single statement in `begin` block. ([@koic][])
* [#9698](https://github.com/rubocop/rubocop/issues/9698): Fix an error for `Style/StructInheritance` when extending instance of `Struct` without `do` ... `end` and class body is empty and single line definition. ([@koic][])
* [#9700](https://github.com/rubocop/rubocop/issues/9700): Avoid warning about Ruby version mismatch. ([@marcandre][])
* [#9636](https://github.com/rubocop/rubocop/issues/9636): Resolve symlinks when excluding directories. ([@ob-stripe][])
* [#9707](https://github.com/rubocop/rubocop/issues/9707): Fix false positive for `Style/MethodCallWithArgsParentheses` with `omit_parentheses` style on an endless `defs` node. ([@dvandersluis][])
* [#9689](https://github.com/rubocop/rubocop/issues/9689): Treat parens around array items the same for children and deeper descendants. ([@dvandersluis][])
* [#9676](https://github.com/rubocop/rubocop/issues/9676): Fix an error for `Style/StringChars` when using `split` without parentheses. ([@koic][])
* [#9712](https://github.com/rubocop/rubocop/pull/9712): Fix an incorrect auto-correct for `Style/HashConversion` when `Hash[]` as a method argument without parentheses. ([@koic][])
* [#9704](https://github.com/rubocop/rubocop/pull/9704): Fix an incorrect auto-correct for `Style/SingleLineMethods` when single line method call without parentheses. ([@koic][])
* [#9683](https://github.com/rubocop/rubocop/issues/9683): Fix an incorrect auto-correct for `Style/HashConversion` when using `zip` method without argument in `Hash[]`. ([@koic][])
* [#9715](https://github.com/rubocop/rubocop/pull/9715): Fix an incorrect auto-correct for `EnforcedStyle: require_parentheses` of `Style/MethodCallWithArgsParentheses` with `Style/RescueModifier`. ([@koic][])

### Changes

* [#7544](https://github.com/rubocop/rubocop/pull/7544): Add --no-parallel (-P/--parallel cannot be combined with --auto-correct). ([@kwerle][])
* [#9648](https://github.com/rubocop/rubocop/pull/9648): **(Compatibility)** Drop support for Ruby 2.4. ([@koic][])
* [#9647](https://github.com/rubocop/rubocop/pull/9647): The parallel flag will now be automatically ignored when combined with `--auto-correct`, `--auto-gen-config`, or `-F/--fail-fast`. Previously, an error was raised and execution stopped. ([@rrosenblum][])

## 1.12.1 (2021-04-04)

### Bug fixes

* [#9649](https://github.com/rubocop/rubocop/pull/9649): Fix when highlights contain multibyte characters. ([@osyo-manga][])
* [#9646](https://github.com/rubocop/rubocop/pull/9646): Fix an incorrect auto-correct for `EnforcedStyle: require_parentheses` of `Style/MethodCallWithArgsParentheses` with `EnforcedStyle: conditionals` of `Style/AndOr`. ([@koic][])
* [#9608](https://github.com/rubocop/rubocop/issues/9608): Fix a false positive for `Layout/EmptyLineAfterGuardClause` when using guard clause is after `rubocop:enable` comment. ([@koic][])
* [#9637](https://github.com/rubocop/rubocop/issues/9637): Allow parentheses for forwarded args in `Style/MethodCallWithArgsParentheses`'s `omit_parentheses` style to avoid endless range ambiguity. ([@gsamokovarov][])
* [#9641](https://github.com/rubocop/rubocop/issues/9641): Fix `Layout/MultilineMethodCallIndentation` triggering on method calls that look like operators. ([@dvandersluis][])
* [#9638](https://github.com/rubocop/rubocop/pull/9638): Fix an error for `Layout/LineLength` when over limit at right hand side of multiple assignment. ([@koic][])
* [#9639](https://github.com/rubocop/rubocop/pull/9639): Fix `Style/RedundantBegin` removing comments on assignment statement correction. ([@marcotc][])
* [#9671](https://github.com/rubocop/rubocop/pull/9671): Fix an incorrect auto-correct for `Lint/AmbiguousOperator` with `Style/MethodCallWithArgsParentheses`. ([@koic][])
* [#9645](https://github.com/rubocop/rubocop/pull/9645): Fix an incorrect auto-correct for `Style/SingleLineMethods` when using single line class method definition. ([@koic][])
* [#9644](https://github.com/rubocop/rubocop/pull/9644): Fix an error and an incorrect auto-correct for `Style/MultilineMethodSignature` when line break after opening parenthesis. ([@koic][])
* [#9672](https://github.com/rubocop/rubocop/issues/9672): Fix an incorrect auto-correct for `Style/HashConversion` when using  multi-argument `Hash[]` as a method argument. ([@koic][])

## 1.12.0 (2021-03-24)

### New features

* [#9615](https://github.com/rubocop/rubocop/pull/9615): Add new `Style/StringChars` cop. ([@koic][])
* [#9629](https://github.com/rubocop/rubocop/issues/9629): Add `AllowParenthesesInStringInterpolation` configuration to `Style/MethodCallWithArgsParentheses` to allow parenthesized calls in string interpolation. ([@gsamokovarov][])
* [#9219](https://github.com/rubocop/rubocop/pull/9219): Allow excluding some constants from `Style/Documentation`. ([@fsateler][])
* Add `AllowNil` option for `Lint/SuppressedException` to allow/disallow `rescue nil`. ([@corroded][])

### Bug fixes

* [#9560](https://github.com/rubocop/rubocop/pull/9560): Fix an error for `Style/ClassMethodsDefinitions` when defining class methods with `class << self` with comment only body. ([@koic][])
* [#9551](https://github.com/rubocop/rubocop/issues/9551): Fix a false positive for `Style/UnlessLogicalOperators` when using `||` operator and invoked method name includes "or" in the conditional branch. ([@koic][])
* [#9620](https://github.com/rubocop/rubocop/pull/9620): Allow parentheses in operator methods calls for `Style/MethodCallWithArgsParentheses` `EnforcedStyle: omit_parentheses`. ([@gsamokovarov][])
* [#9622](https://github.com/rubocop/rubocop/issues/9622): Fixed `Style/BisectedAttrAccessor` autocorrection to handle multiple bisected attrs in the same macro. ([@dvandersluis][])
* [#9606](https://github.com/rubocop/rubocop/issues/9606): Fix an error for `Layout/IndentationConsistency` when using access modifier at the top level. ([@koic][])
* [#9619](https://github.com/rubocop/rubocop/pull/9619): Fix infinite loop between `Layout/IndentationWidth` and `Layout/RescueEnsureAlignment` autocorrection. ([@dvandersluis][])
* [#9633](https://github.com/rubocop/rubocop/pull/9633): Fix an incorrect auto-correct for `Lint/NumberConversion` when `to_i` method in symbol form. ([@koic][])
* [#9616](https://github.com/rubocop/rubocop/pull/9616): Fix an incorrect auto-correct for `Style/EvalWithLocation` when using `#instance_eval` with a string argument in parentheses. ([@koic][])
* [#9429](https://github.com/rubocop/rubocop/issues/9429): Fix `Style/NegatedIfElseCondition` autocorrect to keep comments in correct branch. ([@tejasbubane][])
* [#9631](https://github.com/rubocop/rubocop/issues/9631): Fix an incorrect auto-correct for `Style/RedundantReturn` when using `return` with splat argument. ([@koic][])
* [#9627](https://github.com/rubocop/rubocop/issues/9627): Fix an incorrect auto-correct for `Style/StructInheritance` when extending instance of Struct without `do` ... `end` and class body is empty. ([@koic][])
* [#5953](https://github.com/rubocop/rubocop/issues/5953): Fix a false positive for `Style/AccessModifierDeclarations` when using `module_function` with symbol. ([@koic][])
* [#9593](https://github.com/rubocop/rubocop/issues/9593): Fix an error when processing a directory is named `{}`. ([@koic][])
* [#9599](https://github.com/rubocop/rubocop/issues/9599): Fix an error for `Style/CaseLikeIf` when using `include?` without a receiver. ([@koic][])
* [#9582](https://github.com/rubocop/rubocop/issues/9582): Fix incorrect auto-correct for `Style/ClassEqualityComparison` when comparing `Module#name` for equality. ([@koic][])
* [#9603](https://github.com/rubocop/rubocop/issues/9603): Fix a false positive for `Style/SoleNestedConditional` when using nested modifier on value assigned in condition. ([@koic][])
* [#9598](https://github.com/rubocop/rubocop/pull/9598): Fix RuboCop::MagicComment#valid_shareable_constant_value?. ([@kachick][])
* [#9625](https://github.com/rubocop/rubocop/pull/9625): Allow parentheses in yield arguments with `Style/MethodCallWithArgsParentheses` `EnforcedStyle: omit_parentheses` to fix invalid Ruby auto-correction. ([@gsamokovarov][])
* [#9558](https://github.com/rubocop/rubocop/issues/9558): Fix inconsistency when dealing with URIs that are wrapped in single quotes vs double quotes. ([@dvandersluis][])
* [#9613](https://github.com/rubocop/rubocop/issues/9613): Fix a false positive for `Style/RedundantSelf` when a self receiver on an lvalue of mlhs arguments. ([@koic][])
* [#9586](https://github.com/rubocop/rubocop/issues/9586): Update `Naming/RescuedExceptionsVariableName` to not register on inner rescues when nested. ([@dvandersluis][])

### Changes

* [#9487](https://github.com/rubocop/rubocop/issues/9487): Mark `Naming/MemoizedInstanceVariableName` as unsafe. ([@marcandre][])
* [#9601](https://github.com/rubocop/rubocop/issues/9601): Make `Style/RedundantBegin` aware of redundant `begin`/`end` blocks around memoization. ([@koic][])
* [#9617](https://github.com/rubocop/rubocop/issues/9617): Disable suggested extensions when using the `--stdin` option. ([@dvandersluis][])

## 1.11.0 (2021-03-01)

### New features

* [#5388](https://github.com/rubocop/rubocop/issues/5388): Add new `Style/UnlessLogicalOperators` cop. ([@caalberts][])
* [#9525](https://github.com/rubocop/rubocop/issues/9525): Add `AllowMethodsWithArguments` option to `Style/SymbolProc`. ([@koic][])

### Bug fixes

* [#9520](https://github.com/rubocop/rubocop/issues/9520): Fix an incorrect auto-correct for `Style/MultipleComparison` when comparing a variable with multiple items in `if` and `elsif` conditions. ([@koic][])
* [#9548](https://github.com/rubocop/rubocop/pull/9548): Fix a false positive for `Style/TrailingBodyOnMethodDefinition` when endless method definition body is after newline in opening parenthesis. ([@koic][])
* [#9541](https://github.com/rubocop/rubocop/issues/9541): Fix `Style/HashConversion` when the correction needs to be wrapped in parens. ([@dvandersluis][])
* [#9533](https://github.com/rubocop/rubocop/issues/9533): Make metrics length cops aware of multi-line kwargs. ([@koic][])
* [#9523](https://github.com/rubocop/rubocop/issues/9523): Fix an error for `Style/TrailingMethodEndStatement` when endless method definition signature and body are on different lines. ([@koic][])
* [#9482](https://github.com/rubocop/rubocop/issues/9482): Return minimal known ruby version from gemspecs `required_ruby_version`. ([@HeroProtagonist][])
* [#9539](https://github.com/rubocop/rubocop/issues/9539): Fix an error for `Style/RedundantBegin` when using body of `begin` is empty. ([@koic][])
* [#9542](https://github.com/rubocop/rubocop/pull/9542): Fix `Layout/FirstArgumentIndentation` for operator methods not called as operators. ([@dvandersluis][], [@TSMMark][])

### Changes

* [#9526](https://github.com/rubocop/rubocop/issues/9526): Add `AllowSplatArgument` option to `Style/HashConversion` and the option is true by default. ([@koic][])

## 1.10.0 (2021-02-15)

### New features

* [#9478](https://github.com/rubocop/rubocop/pull/9478): Add new `Style/HashConversion` cop. ([@zverok][])
* [#9496](https://github.com/rubocop/rubocop/pull/9496): Add new `Gemspec/DateAssignment` cop. ([@koic][])
* [#8724](https://github.com/rubocop/rubocop/issues/8724): Add `IgnoreModules` configuration to `Style/ConstantVisibility` to not register offense for module definitions. ([@tejasbubane][])
* [#9403](https://github.com/rubocop/rubocop/issues/9403): Add autocorrect for `Style/EvalWithLocation` cop. ([@cteece][])

### Bug fixes

* [#9500](https://github.com/rubocop/rubocop/issues/9500): Update `Lint/Debugger` so that only specific receivers for debug methods lead to offenses. ([@dvandersluis][])
* [#9499](https://github.com/rubocop/rubocop/issues/9499): Fix a false positive for `Layout/SpaceBeforeBrackets` when multiple spaces are inserted inside the left bracket. ([@koic][])
* [#9507](https://github.com/rubocop/rubocop/issues/9507): Fix an incorrect auto-correct for `Lint/RedundantSplatExpansion` when expanding `Array.new` call on method argument. ([@koic][])
* [#9490](https://github.com/rubocop/rubocop/issues/9490): Fix incorrect auto-correct for `Layout/FirstArgumentIndentation` when specifying `EnforcedStyle: with_fixed_indentation` of `Layout/ArgumentAlignment` and `EnforcedStyle: consistent` of `Layout/FirstArgumentIndentation`. ([@koic][])
* [#9497](https://github.com/rubocop/rubocop/issues/9497): Fix an error for `Style/ExplicitBlockArgument` when `yield` is inside block of `super`. ([@koic][])
* [#9349](https://github.com/rubocop/rubocop/issues/9349): Fix a false positive for `Lint/MultipleComparison` when using `&`, `|`, and `^` set operation operators in multiple comparison. ([@koic][])
* [#9511](https://github.com/rubocop/rubocop/pull/9511): Fix a false negative for `Lint/ElseLayout` when using multiple `elsif`s. ([@koic][])
* [#9513](https://github.com/rubocop/rubocop/issues/9513): Fix an incorrect auto-correct for `Style/HashConversion` when using hash argument `Hash[]`. ([@koic][])
* [#9492](https://github.com/rubocop/rubocop/issues/9492): Fix an incorrect auto-correct for `Lint/DeprecatedOpenSSLConstant` when using no argument algorithm. ([@koic][])

### Changes

* [#9405](https://github.com/rubocop/rubocop/pull/9405): Improve documentation for `Style/EvalWithLocation` cop. ([@taichi-ishitani][])

## 1.9.1 (2021-02-01)

### New features

* [#9459](https://github.com/rubocop/rubocop/issues/9459): Add `AllowedMethods` option to `Style/IfWithBooleanLiteralBranches` and set `nonzero?` as default value. ([@koic][])

### Bug fixes

* [#9431](https://github.com/rubocop/rubocop/issues/9431): Fix an error for `Style/DisableCopsWithinSourceCodeDirective` when using leading source comment. ([@koic][])
* [#9444](https://github.com/rubocop/rubocop/issues/9444): Fix error on colorization for offenses with `Severity: info`. ([@tejasbubane][])
* [#9448](https://github.com/rubocop/rubocop/issues/9448): Fix an error for `Style/SoleNestedConditional` when using nested `unless` modifier with a single expression condition. ([@koic][])
* [#9449](https://github.com/rubocop/rubocop/issues/9449): Fix an error for `Style/NilComparison` when using `x == nil` as a guard condition'. ([@koic][])
* [#9440](https://github.com/rubocop/rubocop/issues/9440): Fix `Lint/SymbolConversion` for implicit `to_sym` without a receiver. ([@dvandersluis][])
* [#9453](https://github.com/rubocop/rubocop/issues/9453): Fix infinite loop error for `Layout/FirstParameterIndentation` when `EnforcedStyle: with_fixed_indentation` is specified for `Layout/ArgumentAlignment`. ([@koic][])
* [#9466](https://github.com/rubocop/rubocop/issues/9466): Don't correct `Style/SingleLineMethods` using endless methods if the target ruby is < 3.0. ([@dvandersluis][])
* [#9455](https://github.com/rubocop/rubocop/issues/9455): Fix a false positive for `Lint/SymbolConversion` when hash keys that contain `":"`. ([@koic][])
* [#9454](https://github.com/rubocop/rubocop/issues/9454): Fix an incorrect auto-correct for `Style/IfWithBooleanLiteralBranches` when using `elsif do_something?` with boolean literal branches. ([@koic][])
* [#9438](https://github.com/rubocop/rubocop/issues/9438): Fix a false positive for `Layout/SpaceBeforeBrackets` when space is used in left bracket. ([@koic][])
* [#9457](https://github.com/rubocop/rubocop/issues/9457): Fix a false positive for `Lint/SymbolConversion` when hash keys that end with `=`. ([@koic][])
* [#9473](https://github.com/rubocop/rubocop/issues/9473): Fix an error for `Lint/DeprecatedConstants` when using `__ENCODING__`. ([@koic][])
* [#9452](https://github.com/rubocop/rubocop/pull/9452): Fix `StyleGuideBaseURL` not functioning with nested departments. ([@tas50][])
* [#9465](https://github.com/rubocop/rubocop/issues/9465): Update `Metrics/ParameterLists` to be able to write `MaxOptionalParameters` in rubocop_todo.yml. ([@dvandersluis][])
* [#9433](https://github.com/rubocop/rubocop/issues/9433): Fix an error for `Style/EvalWithLocation` when using eval with block argument. ([@koic][])

### Changes

* [#9437](https://github.com/rubocop/rubocop/issues/9437): Improve offense message when there is an allowed range of empty lines. ([@dvandersluis][])
* [#9476](https://github.com/rubocop/rubocop/pull/9476): Mark `Style/IfWithBooleanLiteralBranches` as unsafe auto-correction. ([@koic][])

## 1.9.0 (2021-01-28)

### New features

* [#9396](https://github.com/rubocop/rubocop/pull/9396): Add new `Style/IfWithBooleanLiteralBranches` cop. ([@koic][])
* [#9402](https://github.com/rubocop/rubocop/pull/9402): Add new `Lint/TripleQuotes` cop. ([@dvandersluis][])
* [#7827](https://github.com/rubocop/rubocop/pull/7827): Add pre-commit hook. ([@jdufresne][], [@adithyabsk][])
* [#7452](https://github.com/rubocop/rubocop/issues/7452): Support `IgnoredMethods` option for `Style/FormatStringToken`. ([@koic][])
* [#9340](https://github.com/rubocop/rubocop/pull/9340): Added `info` Severity level to allow offenses to be listed but not return a non-zero error code. ([@dvandersluis][])
* [#9353](https://github.com/rubocop/rubocop/issues/9353): Add new `Lint/SymbolConversion` cop. ([@dvandersluis][])
* [#9363](https://github.com/rubocop/rubocop/pull/9363): Add new cop `Lint/OrAssignmentToConstant`. ([@uplus][])
* [#9326](https://github.com/rubocop/rubocop/pull/9326): Add new `Lint/NumberedParameterAssignment` cop. ([@koic][])

### Bug fixes

* [#9366](https://github.com/rubocop/rubocop/issues/9366): Fix an incorrect auto-correct for `Style/SoleNestedConditional` when using method arguments without parentheses for outer condition. ([@koic][])
* [#9372](https://github.com/rubocop/rubocop/issues/9372): Fix an error for `Style/IfInsideElse` when nested `if` branch code is empty. ([@koic][])
* [#9374](https://github.com/rubocop/rubocop/issues/9374): Fix autocorrection for `Layout/LineLength` when the first argument to a send node is a overly long hash pair. ([@dvandersluis][])
* [#9387](https://github.com/rubocop/rubocop/issues/9387): Fix incorrect auto-correct for `Style/NilComparison` when using `!x.nil?` and `EnforcedStyle: comparison`. ([@koic][])
* [#9411](https://github.com/rubocop/rubocop/pull/9411): Fix false negatives for `Style/EvalWithLocation` for `Kernel.eval` and when given improper arguments. ([@dvandersluis][])
* [#7766](https://github.com/rubocop/rubocop/issues/7766): Fix `Naming/RescuedExceptionsVariableName` autocorrection when the rescue body returns the exception variable. ([@asterite][])
* [#7766](https://github.com/rubocop/rubocop/issues/7766): Fix `Naming/RescuedExceptionsVariableName` autocorrection to not change variables if the exception variable has been reassigned. ([@dvandersluis][])
* [#9389](https://github.com/rubocop/rubocop/pull/9389): Fix an infinite loop error for `IncludeSemanticChanges: false` of `Style/NonNilCheck` with `EnforcedStyle: comparison` of `Style/NilComparison`. ([@koic][])
* [#9384](https://github.com/rubocop/rubocop/pull/9384): Fix a suggestion message when not auto-correctable. ([@koic][])
* [#9424](https://github.com/rubocop/rubocop/pull/9424): Fix an incorrect auto-correct for `Style/ClassMethodsDefinitions` when defining class methods with `class << self` and there is no blank line between method definition and attribute accessor. ([@koic][])
* [#9370](https://github.com/rubocop/rubocop/issues/9370): Fix an incorrect auto-correct for `Style/SoleNestedConditional` when using nested `unless` modifier multiple conditional. ([@koic][])
* [#9406](https://github.com/rubocop/rubocop/pull/9406): Fix rubocop_todo link injection when YAML doc start sigil exists. ([@dduugg][])
* [#9229](https://github.com/rubocop/rubocop/pull/9229): Fix errors being reported with `rubocop -V` with an invalid config. ([@dvandersluis][])
* [#9425](https://github.com/rubocop/rubocop/issues/9425): Fix error in `Layout/ClassStructure` when initializer comes after private attribute macro. ([@tejasbubane][])

### Changes

* [#9415](https://github.com/rubocop/rubocop/issues/9415): Change `Layout/ClassStructure` to detect inline modifiers. ([@AndreiEres][])
* [#9380](https://github.com/rubocop/rubocop/issues/9380): Mark `Style/FloatDivision` as unsafe. ([@koic][])
* [#9345](https://github.com/rubocop/rubocop/issues/9345): Make `Style/AsciiComments` allow copyright notice by default. ([@koic][])
* [#9399](https://github.com/rubocop/rubocop/issues/9399): Added `AllowedCops` configuration to `Style/DisableCopsWithinSourceCodeDirective`. ([@dvandersluis][])
* [#9327](https://github.com/rubocop/rubocop/issues/9327): Change `Layout/EmptyLineAfterMagicComment` to accept top-level `shareable_constant_values` directive. ([@tejasbubane][])
* [#7902](https://github.com/rubocop/rubocop/issues/7902): Change `Lint/NumberConversion` to detect symbol form of conversion methods. ([@tejasbubane][])

## 1.8.1 (2021-01-11)

### Bug fixes

* [#9342](https://github.com/rubocop/rubocop/issues/9342): Fix an error for `Lint/RedundantDirGlobSort` when using `collection.sort`. ([@koic][])
* [#9304](https://github.com/rubocop/rubocop/issues/9304): Do not register an offense for `Style/ExplicitBlockArgument` when the `yield` arguments are not an exact match with the block arguments. ([@dvandersluis][])
* [#8281](https://github.com/rubocop/rubocop/issues/8281): Fix `Style/WhileUntilModifier` handling comments and assignment when correcting to modifier form. ([@Darhazer][])
* [#8229](https://github.com/rubocop/rubocop/issues/8229): Fix faulty calculation in UncommunicativeName. ([@ohbarye][])
* [#9350](https://github.com/rubocop/rubocop/pull/9350): Wrap in parens before replacing `unless` with `if` and `!`. ([@magneland][])
* [#9356](https://github.com/rubocop/rubocop/pull/9356): Fix duplicate extension cop versions when using `rubocop -V`. ([@koic][])
* [#9355](https://github.com/rubocop/rubocop/issues/9355): Fix `Style/SingleLineMethods` autocorrection to endless method when the original code had parens. ([@dvandersluis][])
* [#9346](https://github.com/rubocop/rubocop/pull/9346): Fix an incorrect auto-correct for `Style/StringConcatenation` when concat string include double quotes and interpolation. ([@k-karen][])

## 1.8.0 (2021-01-07)

### New features

* [#9324](https://github.com/rubocop/rubocop/pull/9324): Add new `Lint/DeprecatedConstants` cop. ([@koic][])
* [#9319](https://github.com/rubocop/rubocop/pull/9319): Support asdf's .tool-versions file. ([@noon-ng][])
* [#9301](https://github.com/rubocop/rubocop/pull/9301): Add new `Lint/RedundantDirGlobSort` cop. ([@koic][])
* [#9281](https://github.com/rubocop/rubocop/pull/9281): Add new cop `Style/EndlessMethod`. ([@dvandersluis][])
* [#9321](https://github.com/rubocop/rubocop/pull/9321): Add new `Lint/LambdaWithoutLiteralBlock` cop. ([@koic][])

### Bug fixes

* [#9298](https://github.com/rubocop/rubocop/issues/9298): Fix an incorrect auto-correct for `Lint/RedundantCopDisableDirective` when there is a blank line before inline comment. ([@koic][])
* [#9233](https://github.com/rubocop/rubocop/issues/9233): Fix `Style/SoleNestedConditional` copying non-relevant comments during auto-correction. ([@Darhazer][])
* [#9312](https://github.com/rubocop/rubocop/issues/9312): Fix `Layout/FirstHashElementLineBreak` to apply to multi-line hashes with only a single element. ([@muirdm][])
* [#9316](https://github.com/rubocop/rubocop/issues/9316): Fix `Style/EmptyLiteral` registering wrong offense when using a numbered block for Hash.new, i.e. `Hash.new { _1[_2] = [] }`. ([@agargiulo][])
* [#9308](https://github.com/rubocop/rubocop/issues/9308): Fix an error for `Layout/EmptyLineBetweenDefs` when using endless class method. ([@koic][])
* [#9314](https://github.com/rubocop/rubocop/issues/9314): Fix an incorrect auto-correct for `Style/RedundantReturn` when multiple return values have a parenthesized return value. ([@koic][])
* [#9335](https://github.com/rubocop/rubocop/issues/9335): Fix an incorrect auto-correct for `EnforcedStyle: require_parentheses` of `Style/MethodCallWithArgsParentheses` with `Style/NestedParenthesizedCalls`. ([@koic][])
* [#9290](https://github.com/rubocop/rubocop/issues/9290): Fix a false positive for `Layout/SpaceBeforeBrackets` when using array literal method argument. ([@koic][])
* [#9333](https://github.com/rubocop/rubocop/issues/9333): Fix an error for `Style/IfInsideElse` when using a modifier `if` nested inside an `else` after `elsif`. ([@koic][])
* [#9303](https://github.com/rubocop/rubocop/issues/9303): Fix an incorrect auto-correct for `Style/RaiseArgs` with `EnforcedStyle: compact` when using exception instantiation argument. ([@koic][])

### Changes

* [#9300](https://github.com/rubocop/rubocop/pull/9300): Make `Lint/NonDeterministicRequireOrder` not to register offense when using Ruby 3.0 or higher. ([@koic][])
* [#9320](https://github.com/rubocop/rubocop/pull/9320): Support unicode-display_width v2. ([@dduugg][])
* [#9288](https://github.com/rubocop/rubocop/pull/9288): Require Parser 3.0.0.0 or higher. ([@koic][])
* [#9337](https://github.com/rubocop/rubocop/issues/9337): Add `AllowedIdentifiers` to `Naming/VariableName`. ([@dvandersluis][])
* [#9295](https://github.com/rubocop/rubocop/pull/9295): Update `Style/SingleLineMethods` to correct to an endless method definition if they are allowed. ([@dvandersluis][])
* [#9331](https://github.com/rubocop/rubocop/pull/9331): Mark `Style/MutableConstant` as unsafe. ([@koic][])

## 1.7.0 (2020-12-25)

### New features

* [#9260](https://github.com/rubocop/rubocop/pull/9260): Support auto-correction for `Style/MultilineMethodSignature`. ([@koic][])
* [#9282](https://github.com/rubocop/rubocop/pull/9282): Make `Style/RedundantFreeze` and `Style/MutableConstant` cops aware of frozen regexp and range literals when using Ruby 3.0. ([@koic][])
* [#9223](https://github.com/rubocop/rubocop/issues/9223): Add new `Lint/AmbiguousAssignment` cop. ([@fatkodima][])
* [#9243](https://github.com/rubocop/rubocop/pull/9243): Support auto-correction for `Style/CommentedKeyword`. ([@koic][])
* [#9283](https://github.com/rubocop/rubocop/pull/9283): Add new `Style/HashExcept` cop. ([@koic][])
* [#9231](https://github.com/rubocop/rubocop/pull/9231): Add new `Layout/SpaceBeforeBrackets` cop. ([@koic][])

### Bug fixes

* [#9232](https://github.com/rubocop/rubocop/pull/9232): Fix `Style/SymbolProc` registering wrong offense when using a symbol numbered block argument greater than 1, i.e. `[[1, 2]].map { _2.succ }`. ([@tdeo][])
* [#9274](https://github.com/rubocop/rubocop/issues/9274): Fix error in `Metrics/ClassLength` when the class only contains comments. ([@dvandersluis][])
* [#9213](https://github.com/rubocop/rubocop/issues/9213): Fix a false positive for `Style/RedundantFreeze` when using `Array#*`. ([@koic][])
* [#9279](https://github.com/rubocop/rubocop/pull/9279): Add support for endless methods to `Style/MethodCallWithArgsParentheses`. ([@dvandersluis][])
* [#9245](https://github.com/rubocop/rubocop/issues/9245): Fix `Lint/AmbiguousRegexpLiteral` when given a `match_with_lvasgn` node. ([@dvandersluis][])
* [#9276](https://github.com/rubocop/rubocop/pull/9276): Add support for endless methods to `Style/SingleLineMethods`. ([@dvandersluis][])
* [#9225](https://github.com/rubocop/rubocop/issues/9225): Fix `Style/LambdaCall` ignoring further offenses after opposite style is detected. ([@sswander][])
* [#9234](https://github.com/rubocop/rubocop/issues/9234): Fix the error for `Style/KeywordParametersOrder` and make it aware of block keyword parameters. ([@koic][])
* [#8938](https://github.com/rubocop/rubocop/pull/8938): Fix some ConfigurableEnforcedStyle cops to output `Exclude` file lists in `--auto-gen-config` runs. ([@h-lame][])
* [#9257](https://github.com/rubocop/rubocop/issues/9257): Fix false positive for `Style/SymbolProc` when the block uses a variable from outside the block. ([@dvandersluis][])
* [#9251](https://github.com/rubocop/rubocop/issues/9251): Fix extracted cop warning when the extension is loaded using `--require`. ([@dvandersluis][])
* [#9244](https://github.com/rubocop/rubocop/issues/9244): When a cop defined in an extension is explicitly enabled, ensure that it remains enabled. ([@dvandersluis][])
* [#8046](https://github.com/rubocop/rubocop/issues/8046): Fix an error for `Layout/HeredocArgumentClosingParenthesis` when there is an argument between a heredoc argument and the closing parentheses. ([@koic][])
* [#9261](https://github.com/rubocop/rubocop/pull/9261): Fix an incorrect auto-correct for `Style/MultilineWhenThen` when one line for multiple candidate values of `when` statement. ([@makicamel][])
* [#9258](https://github.com/rubocop/rubocop/pull/9258): Fix calculation of cop department for nested departments. ([@mvz][])
* [#9277](https://github.com/rubocop/rubocop/pull/9277): Fix `Layout/EmptyLineBetweenDefs` error with endless method definitions. ([@dvandersluis][])
* [#9278](https://github.com/rubocop/rubocop/pull/9278): Update `Style/MethodDefParentheses` to ignore endless method definitions since parentheses are always required. ([@dvandersluis][])

### Changes

* [#9212](https://github.com/rubocop/rubocop/pull/9212): Make `Style/RedundantArgument` aware of `String#chomp` and `String#chomp!`. ([@koic][])
* [#8482](https://github.com/rubocop/rubocop/issues/8482): Allow simple math for `Lint/BinaryOperatorWithIdenticalOperands` cop. ([@fatkodima][])
* [#9237](https://github.com/rubocop/rubocop/issues/9237): Add `IgnoredPatterns` configuration to `Lint/UnreachableLoop` to allow for block methods that share a name with an `Enumerable` method. ([@dvandersluis][])
* [#9206](https://github.com/rubocop/rubocop/pull/9206): Allow extensions to disable cop obsoletions. ([@dvandersluis][])
* [#9262](https://github.com/rubocop/rubocop/issues/9262): Update `Style/CollectionMethods` to be handle additional arguments and methods that accept a symbol instead of a block. ([@dvandersluis][])
* [#9235](https://github.com/rubocop/rubocop/issues/9235): Allow `--only` and `--except` to be able to properly qualify cops added by require. ([@dvandersluis][])
* [#9205](https://github.com/rubocop/rubocop/issues/9205): Update `Naming/MemoizedInstanceVariableName` to handle dynamically defined methods. ([@dvandersluis][])
* [#9285](https://github.com/rubocop/rubocop/pull/9285): Add `AllowPercentLiteralArrayArgument` option for `Lint/RedundantSplatExpansion` to enable the option by default. ([@koic][])
* [#9208](https://github.com/rubocop/rubocop/issues/9208): Use Array#bsearch instead of Array#include? to detect hidden files. ([@dark-panda][])
* [#9228](https://github.com/rubocop/rubocop/pull/9228): Suppress any config warnings for `rubocop -V`. ([@dvandersluis][])
* [#9193](https://github.com/rubocop/rubocop/pull/9193): Add `IgnoreLiteralBranches` and `IgnoreConstantBranches` options to `Lint/DuplicateBranch`. ([@dvandersluis][])

## 1.6.1 (2020-12-10)

### Bug fixes

* [#9196](https://github.com/rubocop/rubocop/issues/9196): Fix `ConfigObsoletion::ExtractedCop` raising errors for loaded features when bundler is not activated. ([@dvandersluis][])

## 1.6.0 (2020-12-09)

### New features

* [#9125](https://github.com/rubocop/rubocop/issues/9125): Allow ConfigObsoletion to be extended by other RuboCop libraries. ([@dvandersluis][])
* [#9182](https://github.com/rubocop/rubocop/pull/9182): Support auto-correction for `Style/RedundantArgument`. ([@koic][])
* [#9186](https://github.com/rubocop/rubocop/pull/9186): Support auto-correction for `Style/FloatDivision`. ([@koic][])
* [#9167](https://github.com/rubocop/rubocop/pull/9167): Support auto-correct for `StyleSingleLineBlockParams`. ([@koic][])

### Bug fixes

* [#9177](https://github.com/rubocop/rubocop/pull/9177): Remove back-ref related code from `Style/SpecialGlobalVars`. ([@r7kamura][])
* [#9160](https://github.com/rubocop/rubocop/issues/9160): Fix an incorrect auto-correct for `Style/IfUnlessModifier` and `Style/SoleNestedConditional` when auto-correction conflicts for guard condition. ([@koic][])
* [#9174](https://github.com/rubocop/rubocop/issues/9174): Handle send nodes with unparenthesized arguments in `Style/SoleNestedConditional`. ([@dvandersluis][])
* [#9184](https://github.com/rubocop/rubocop/issues/9184): `Layout/EmptyLinesAroundAttributeAccessor` fails if the attr_accessor is the last line of the file. ([@tas50][])

### Changes

* [#9171](https://github.com/rubocop/rubocop/pull/9171): Add "did you mean" message when failing due to invalid cops in configuration. ([@dvandersluis][])
* [#8897](https://github.com/rubocop/rubocop/issues/8897): Change `Style/StringConcatenation` to accept line-end concatenation between two strings so that `Style/LineEndConcatenation` can handle it instead. ([@dvandersluis][])
* [#9172](https://github.com/rubocop/rubocop/pull/9172): Add `Style/PerlBackrefs` targets and change message more detailed. ([@r7kamura][])
* [#9187](https://github.com/rubocop/rubocop/pull/9187): Update formatters to output `[Correctable]` for correctable offenses. ([@dvandersluis][])
* [#9169](https://github.com/rubocop/rubocop/pull/9169): Add obsoletion warnings for `Performance/*` and `Rails/*` which are in separate gems now. ([@dvandersluis][])

## 1.5.2 (2020-12-04)

### Bug fixes

* [#9152](https://github.com/rubocop/rubocop/issues/9152): Fix an incorrect auto-correct for `Style/SoleNestedConditional` when nested `||` operator modifier condition. ([@koic][])
* [#9161](https://github.com/rubocop/rubocop/issues/9161): Fix a false positive for `Layout/HeredocArgumentClosingParenthesis` when using subsequence closing parentheses in the same line. ([@koic][])
* [#9151](https://github.com/rubocop/rubocop/issues/9151): Fix `SuggestExtensions` to not suggest extensions that are installed but not direct dependencies. ([@dvandersluis][])
* [#8985](https://github.com/rubocop/rubocop/issues/8985): Fix `Style/StringConcatenation` autocorrect generating invalid ruby. ([@tejasbubane][])
* [#9155](https://github.com/rubocop/rubocop/issues/9155): Fix a false positive for `Layout/MultilineMethodCallIndentation` when multiline method chain has expected indent width and the method is preceded by splat for `EnforcedStyle: indented_relative_to_receiver`. ([@koic][])

### Changes

* [#9080](https://github.com/rubocop/rubocop/issues/9080): Make `Lint/ShadowingOuterLocalVariable` aware of `Ractor`. ([@tejasbubane][])
* [#9102](https://github.com/rubocop/rubocop/pull/9102): Relax regexp_parser requirement. ([@marcandre][])

## 1.5.1 (2020-12-02)

### Bug fixes

* [#8684](https://github.com/rubocop/rubocop/issues/8684): Fix an error for `Lint/InterpolationCheck` cop. ([@tejasbubane][])
* [#9145](https://github.com/rubocop/rubocop/issues/9145): Fix issues with SuggestExtensions when bundler is not available, or when there is no gemfile. ([@dvandersluis][])
* [#9140](https://github.com/rubocop/rubocop/issues/9140): Fix an error for `Layout/EmptyLinesAroundArguments` when multiline style argument for method call without selector. ([@koic][])
* [#9136](https://github.com/rubocop/rubocop/pull/9136): Fix `AllowedIdentifiers` in `Naming/VariableNumber` to include variable assignments. ([@PhilCoggins][])

## 1.5.0 (2020-12-01)

### New features

* [#9112](https://github.com/rubocop/rubocop/pull/9112): Add new cop `Lint/UnexpectedBlockArity`. ([@dvandersluis][])
* [#9010](https://github.com/rubocop/rubocop/pull/9010): `Metrics/ParameterLists` supports `MaxOptionalParameters` config parameter. ([@fatkodima][])
* [#9114](https://github.com/rubocop/rubocop/pull/9114): Support auto-correction for `Style/SoleNestedConditional`. ([@koic][])
* [#8564](https://github.com/rubocop/rubocop/issues/8564): `Metrics/AbcSize`: Add optional discount for repeated "attributes". ([@marcandre][])

### Bug fixes

* [#8820](https://github.com/rubocop/rubocop/issues/8820): Fixes `IfWithSemicolon` autocorrection when `elsif` is present. ([@adrian-rivera][], [@dvandersluis][])
* [#9113](https://github.com/rubocop/rubocop/pull/9113): Fix a false positive for `Style/MethodCallWithoutArgsParentheses` when assigning to a default argument with the same name. ([@koic][])
* [#9115](https://github.com/rubocop/rubocop/issues/9115): Fix a false positive for `Layout/FirstArgumentIndentation` when argument has expected indent width and the method is preceded by splat for `EnforcedStyle: consistent_relative_to_receiver`. ([@koic][])
* [#9128](https://github.com/rubocop/rubocop/issues/9128): Fix an incorrect auto-correct for `Style/ClassAndModuleChildren` when namespace is defined as a class in the same file. ([@koic][])
* [#9105](https://github.com/rubocop/rubocop/issues/9105): Fix an incorrect auto-correct for `Style/RedundantCondition` when using operator method in `else`. ([@koic][])
* [#9096](https://github.com/rubocop/rubocop/pull/9096): Fix #9095 use merged_config instead of config for pending new cop check. ([@ThomasKoppensteiner][])
* [#8053](https://github.com/rubocop/rubocop/issues/8053): Fix an incorrect auto-correct for `Style/AndOr` when `or` precedes `and`. ([@koic][])
* [#9097](https://github.com/rubocop/rubocop/issues/9097): Fix a false positive for `Layout/EmptyLinesAroundArguments` when blank line is inserted between method with arguments and receiver. ([@koic][])

### Changes

* [#9122](https://github.com/rubocop/rubocop/issues/9122): Added tip message if any gems are loaded that have RuboCop extensions. ([@dvandersluis][])
* [#9104](https://github.com/rubocop/rubocop/issues/9104): Preset some stdlib method names for `Naming/VariableNumber`. ([@koic][])
* [#9127](https://github.com/rubocop/rubocop/pull/9127): Update `Style/SymbolProc` to be aware of numblocks. ([@dvandersluis][])
* [#9102](https://github.com/rubocop/rubocop/pull/9102): Upgrade regexp_parser to 2.0. ([@knu][])
* [#9100](https://github.com/rubocop/rubocop/pull/9100): Update `ConfigObsoletion` so that parameters can be deprecated but still accepted. ([@dvandersluis][])
* [#9108](https://github.com/rubocop/rubocop/pull/9108): Update `Lint/UnmodifiedReduceAccumulator` to handle numblocks and more than 2 arguments. ([@dvandersluis][])
* [#9098](https://github.com/rubocop/rubocop/pull/9098): Update `Metrics/BlockLength` and `Metrics/MethodLength` to use `IgnoredMethods` instead of `ExcludedMethods` in configuration. The previous key is retained for backwards compatibility. ([@dvandersluis][])
* [#9098](https://github.com/rubocop/rubocop/pull/9098): Update `IgnoredMethods` so that every cop that uses it will accept both strings and regexes in the configuration. ([@dvandersluis][])

## 1.4.2 (2020-11-25)

### Bug fixes

* [#9083](https://github.com/rubocop/rubocop/pull/9083): Fix `Style/RedundantArgument` cop raising offense for more than one argument. ([@tejasbubane][])
* [#9089](https://github.com/rubocop/rubocop/issues/9089): Fix an incorrect auto-correct for `Style/FormatString` when using sprintf with second argument that uses an operator. ([@koic][])
* [#7670](https://github.com/rubocop/rubocop/issues/7670): Handle offenses inside heredocs for `-a --disable-uncorrectable`. ([@jonas054][])
* [#9070](https://github.com/rubocop/rubocop/issues/9070): Fix `Lint/UnmodifiedReduceAccumulator` error when the block does not have enough arguments. ([@dvandersluis][])

### Changes

* [#9091](https://github.com/rubocop/rubocop/pull/9091): Have `Naming/VariableNumber` accept _1, _2, ... ([@marcandre][])
* [#9087](https://github.com/rubocop/rubocop/pull/9087): Deprecate `EnforceSuperclass` module. ([@koic][])

## 1.4.1 (2020-11-23)

### Bug fixes

* [#9082](https://github.com/rubocop/rubocop/pull/9082): Fix gemspec to include assets directory. ([@javierav][])

## 1.4.0 (2020-11-23)

### New features

* [#7737](https://github.com/rubocop/rubocop/issues/7737): Add new `Style/RedundantArgument` cop. ([@tejasbubane][])
* [#9064](https://github.com/rubocop/rubocop/issues/9064): Add `EmptyLineBetweenMethodDefs`, `EmptyLineBetweenClassDefs` and `EmptyLineBetweenModuleDefs` config options for `Layout/EmptyLineBetweenDefs` cop. ([@tejasbubane][])
* [#9043](https://github.com/rubocop/rubocop/pull/9043): Add `--stderr` to write all output to stderr except for the autocorrected source. ([@knu][])

### Bug fixes

* [#9067](https://github.com/rubocop/rubocop/pull/9067): Fix an incorrect auto-correct for `Lint::AmbiguousRegexpLiteral` when passing in a regexp to a method with no receiver. ([@amatsuda][])
* [#9060](https://github.com/rubocop/rubocop/issues/9060): Fix an error for `Layout/SpaceAroundMethodCallOperator` when using `__ENCODING__`. ([@koic][])
* [#7338](https://github.com/rubocop/rubocop/issues/7338): Handle assignment with `[]=` in `MultilineMethodCallIndentation`. ([@jonas054][])
* [#7726](https://github.com/rubocop/rubocop/issues/7726): Fix `MultilineMethodCallIndentation` indentation inside square brackets. ([@jonas054][])
* [#8857](https://github.com/rubocop/rubocop/issues/8857): Improve how `Exclude` properties are generated by `--auto-gen-config`. ([@jonas054][])

### Changes

* [#8788](https://github.com/rubocop/rubocop/issues/8788): Change `Style/Documentation` to not trigger offense with only macros. ([@tejasbubane][])
* [#8993](https://github.com/rubocop/rubocop/issues/8993): Allow `ExcludedMethods` config of `Metrics/MethodLength` cop to contain regex. ([@tejasbubane][])
* [#9073](https://github.com/rubocop/rubocop/issues/9073): Enable `Layout/LineLength`'s auto-correct by default. ([@bbatsov][])
* [#9079](https://github.com/rubocop/rubocop/pull/9079): Improve the gemspec to load only the necessary files without the git utility. ([@piotrmurach][])
* [#9059](https://github.com/rubocop/rubocop/pull/9059): Update `Lint/UnmodifiedReduceAccumulator` to accept blocks which return in the form `accumulator[element]`. ([@dvandersluis][])
* [#9072](https://github.com/rubocop/rubocop/pull/9072): `Lint/MissingSuper`: exclude `method_missing` and `respond_to_missing?`. ([@marcandre][])
* [#9074](https://github.com/rubocop/rubocop/pull/9074): Allow specifying a pull request ID when calling `rake changelog:*`. ([@marcandre][])

## 1.3.1 (2020-11-16)

### Bug fixes

* [#9037](https://github.com/rubocop/rubocop/pull/9037): Fix `required_ruby_version` issue when using `Gem::Requirement`. ([@cetinajero][])
* [#9039](https://github.com/rubocop/rubocop/pull/9039): Fix stack level too deep error if target directory contains `**`. ([@unasuke][])
* [#6962](https://github.com/rubocop/rubocop/issues/6962): Limit `Layout/ClassStructure` constant order autocorrect to literal constants. ([@tejasbubane][])
* [#9032](https://github.com/rubocop/rubocop/issues/9032): Fix an error for `Style/DocumentDynamicEvalDefinition` when using eval-type method with interpolated string that is not heredoc without comment doc. ([@koic][])
* [#9049](https://github.com/rubocop/rubocop/issues/9049): Have `Lint/ToEnumArguments` accept `__callee__`. ([@marcandre][])
* [#9050](https://github.com/rubocop/rubocop/issues/9050): Fix a false positive for `Style/NegatedIfElseCondition` when `if` with `!!` condition. ([@koic][])
* [#9041](https://github.com/rubocop/rubocop/issues/9041): Fix a false positive for `Naming/VariableNumber` when using integer symbols. ([@koic][])

### Changes

* [#9045](https://github.com/rubocop/rubocop/pull/9045): Have `cut_release` handle "config/default" and generate cops doc. ([@marcandre][])
* [#9036](https://github.com/rubocop/rubocop/pull/9036): Allow `enums` method by default for `Lint/ConstantDefinitionInBlock`. ([@koic][])
* [#9035](https://github.com/rubocop/rubocop/issues/9035): Only complain about `SafeYAML` if it causes issues. ([@marcandre][])

## 1.3.0 (2020-11-12)

### New features

* [#8761](https://github.com/rubocop/rubocop/issues/8761): Read `required_ruby_version` from gemspec file if it exists. ([@HeroProtagonist][])
* [#9001](https://github.com/rubocop/rubocop/pull/9001): Add new `Lint/EmptyClass` cop. ([@fatkodima][])
* [#9025](https://github.com/rubocop/rubocop/issues/9025): Add `AllowedMethods` option to `Lint/ConstantDefinitionInBlock`. ([@koic][])
* [#9014](https://github.com/rubocop/rubocop/pull/9014): Support auto-correction for `Style/IfInsideElse`. ([@koic][])
* [#8483](https://github.com/rubocop/rubocop/pull/8483): Add new `Style/StaticClass` cop. ([@fatkodima][])
* [#9020](https://github.com/rubocop/rubocop/pull/9020): Add new `Style/NilLambda` cop to check for lambdas that always return nil. ([@dvandersluis][])
* [#8404](https://github.com/rubocop/rubocop/pull/8404): Add new `Lint/DuplicateBranch` cop. ([@fatkodima][])

### Bug fixes

* [#8499](https://github.com/rubocop/rubocop/issues/8499): Fix `Style/IfUnlessModifier` and `Style/WhileUntilModifier` to prevent an offense if there are both first-line comment and code after `end` block. ([@dsavochkin][])
* [#8996](https://github.com/rubocop/rubocop/issues/8996): Fix a false positive for `Style/MultipleComparison` when comparing two sides of the disjunction is unrelated. ([@koic][])
* [#8975](https://github.com/rubocop/rubocop/issues/8975): Fix an infinite loop when autocorrecting `Layout/TrailingWhitespace` + `Lint/LiteralInInterpolation`. ([@fatkodima][])
* [#8998](https://github.com/rubocop/rubocop/issues/8998): Fix an error for `Style/NegatedIfElseCondition` when using negated condition and `if` branch body is empty. ([@koic][])
* [#9008](https://github.com/rubocop/rubocop/pull/9008): Mark `Style/InfiniteLoop` as unsafe. ([@marcandre][])

### Changes

* [#8978](https://github.com/rubocop/rubocop/issues/8978): Update `Layout/LineLength` autocorrection to be able to handle method calls with long argument lists. ([@dvandersluis][])
* [#9015](https://github.com/rubocop/rubocop/issues/9015): Update `Lint/EmptyBlock` to allow for empty lambdas. ([@dvandersluis][])
* [#9022](https://github.com/rubocop/rubocop/issues/9022): Add `NOTE` to keywords of `Style/CommentAnnotation`. ([@koic][])
* [#9011](https://github.com/rubocop/rubocop/issues/9011): Mark autocorrection for `Lint/Loop` as unsafe. ([@dvandersluis][])
* [#9026](https://github.com/rubocop/rubocop/issues/9026): Update `Style/DocumentDynamicEvalDefinition` to detect comment blocks that document the evaluation. ([@dvandersluis][])
* [#9004](https://github.com/rubocop/rubocop/pull/9004): Remove obsolete gem `SafeYAML` compatibility. ([@marcandre][])
* [#9023](https://github.com/rubocop/rubocop/issues/9023): Mark unsafe for `Style/CollectionCompact`. ([@koic][])
* [#9012](https://github.com/rubocop/rubocop/issues/9012): Allow `AllowedIdentifiers` to be specified for `Naming/VariableNumber`. ([@dvandersluis][])

## 1.2.0 (2020-11-05)

### New features

* [#8983](https://github.com/rubocop/rubocop/pull/8983): Support auto-correction for `Naming/HeredocDelimiterCase`. ([@koic][])
* [#8004](https://github.com/rubocop/rubocop/issues/8004): Add new `GitHubActionsFormatter` formatter. ([@lautis][])
* [#8175](https://github.com/rubocop/rubocop/pull/8175): Add new `AllowedCompactTypes` option for `Style/RaiseArgs`. ([@pdobb][])
* [#8566](https://github.com/rubocop/rubocop/issues/8566): Add new `Style/CollectionCompact` cop. ([@fatkodima][])
* [#8925](https://github.com/rubocop/rubocop/issues/8925): Add `--display-time` option for displaying elapsed time of `rubocop` command. ([@joshuapinter][])
* [#8967](https://github.com/rubocop/rubocop/pull/8967): Add new `Style/NegatedIfElseCondition` cop. ([@fatkodima][])
* [#8984](https://github.com/rubocop/rubocop/pull/8984): Support auto-correction for `Style/DoubleNegation`. ([@koic][])
* [#8992](https://github.com/rubocop/rubocop/pull/8992): Support auto-correction for `Lint/ElseLayout`. ([@koic][])
* [#8988](https://github.com/rubocop/rubocop/pull/8988): Support auto-correction for `Lint/UselessSetterCall`. ([@koic][])
* [#8982](https://github.com/rubocop/rubocop/pull/8982): Support auto-correction for `Naming/BinaryOperatorParameterName`. ([@koic][])

### Bug fixes

* [#8989](https://github.com/rubocop/rubocop/pull/8989): Fix multibyte support in the regexp node handler that led `Style/RedundantRegexpEscape` to malfunction and corrupt a program in auto-correction. ([@knu][])
* [#8912](https://github.com/rubocop/rubocop/pull/8912): Fix `Layout/ElseAlignment` for `rescue/else/ensure` inside `do/end` blocks with assignment. ([@miry][])
* [#8971](https://github.com/rubocop/rubocop/issues/8971): Fix a false alarm for `# rubocop:disable Lint/EmptyBlock` inline comment with `Lint/RedundantCopDisableDirective`. ([@koic][])
* [#8976](https://github.com/rubocop/rubocop/issues/8976): Fix an incorrect auto-correct for `Style/KeywordParametersOrder` when `kwoptarg` is before `kwarg` and argument parentheses omitted. ([@koic][])
* [#8084](https://github.com/rubocop/rubocop/pull/8084): Fix a bug in how `Layout/SpaceAroundBlockParameters` handles block parameters with a trailing comma. ([@bquorning][])
* [#8966](https://github.com/rubocop/rubocop/issues/8966): Fix `Layout/SpaceInsideParens` to enforce no spaces in empty parens for all styles. ([@joshuapinter][])

### Changes

* [#5717](https://github.com/rubocop/rubocop/issues/5717): Support `defined?`-based memoization for `Naming/MemoizedInstanceVariableName` cop. ([@fatkodima][])
* [#8964](https://github.com/rubocop/rubocop/pull/8964): Extend `Naming/VariableNumber` cop to handle method names and symbols. ([@fatkodima][])

## 1.1.0 (2020-10-29)

### New features

* [#8896](https://github.com/rubocop/rubocop/pull/8896): Add new `Lint/DuplicateRegexpCharacterClassElement` cop. ([@owst][])
* [#8895](https://github.com/rubocop/rubocop/pull/8895): Add new `Lint/EmptyBlock` cop. ([@fatkodima][])
* [#8934](https://github.com/rubocop/rubocop/pull/8934): Add new `Style/SwapValues` cop. ([@fatkodima][])
* [#7549](https://github.com/rubocop/rubocop/issues/7549): Add new `Style/ArgumentsForwarding` cop. ([@koic][])
* [#8859](https://github.com/rubocop/rubocop/issues/8859): Add new `Lint/UnmodifiedReduceAccumulator` cop. ([@dvandersluis][])
* [#8951](https://github.com/rubocop/rubocop/pull/8951): Support auto-correction for `Style/MultipleComparison`. ([@koic][])
* [#8953](https://github.com/rubocop/rubocop/pull/8953): Add `AllowMethodComparison` option for `Lint/MultipleComparison`. ([@koic][])
* [#8960](https://github.com/rubocop/rubocop/pull/8960): Add `Regexp::Expression#loc` and `#expression` to replace `parsed_tree_expr_loc`. ([@marcandre][])
* [#8930](https://github.com/rubocop/rubocop/pull/8930): Add rake tasks for alternative way to specify Changelog entries. ([@marcandre][])
* [#8940](https://github.com/rubocop/rubocop/pull/8940): Add new `Style/DocumentDynamicEvalDefinition` cop. ([@fatkodima][])
* [#7753](https://github.com/rubocop/rubocop/issues/7753): Add new `Lint/ToEnumArguments` cop. ([@fatkodima][])

### Bug fixes

* [#8921](https://github.com/rubocop/rubocop/pull/8921): Prevent `Lint/LiteralInInterpolation` from removing necessary interpolation in `%W[]` and `%I[]` literals. ([@knu][])
* [#8708](https://github.com/rubocop/rubocop/pull/8708): Fix bad regexp recognition in `Lint/OutOfRangeRegexpRef` when there are multiple regexps. ([@dvandersluis][])
* [#8945](https://github.com/rubocop/rubocop/pull/8945): Fix changelog task to build a correct changelog item when `Fix #123` is encountered. ([@dvandersluis][])
* [#8914](https://github.com/rubocop/rubocop/pull/8914): Fix autocorrection for `Layout/TrailingWhitespace` in heredocs. ([@marcandre][])
* [#8913](https://github.com/rubocop/rubocop/pull/8913): Fix an incorrect auto-correct for `Style/RedundantRegexpCharacterClass` due to quantifier. ([@ysakasin][])
* [#8917](https://github.com/rubocop/rubocop/issues/8917): Fix rubocop comment directives handling of cops with multiple levels in department name. ([@fatkodima][])
* [#8918](https://github.com/rubocop/rubocop/issues/8918): Fix a false positives for `Bundler/DuplicatedGem` when a gem conditionally duplicated within `if-elsif` or `case-when` statements. ([@fatkodima][])
* [#8933](https://github.com/rubocop/rubocop/pull/8933): Fix an error for `Layout/EmptyLinesAroundAccessModifier` when the first line is a comment. ([@matthieugendreau][])
* [#8954](https://github.com/rubocop/rubocop/pull/8954): Fix autocorrection for `Style/RedundantRegexpCharacterClass` with %r. ([@ysakasin][])

### Changes

* [#8920](https://github.com/rubocop/rubocop/pull/8920): Remove Capybara's `save_screenshot` from `Lint/Debugger`. ([@ybiquitous][])
* [#8919](https://github.com/rubocop/rubocop/issues/8919): Require RuboCop AST 1.0.1 or higher. ([@koic][])
* [#8939](https://github.com/rubocop/rubocop/pull/8939): Accept comparisons of multiple method calls for `Style/MultipleComparison`. ([@koic][])
* [#8950](https://github.com/rubocop/rubocop/issues/8950): Add `IgnoredMethods` and `IgnoredClasses` to `Lint/NumberConversion`. ([@dvandersluis][])

## 1.0.0 (2020-10-21)

### New features

* [#7944](https://github.com/rubocop/rubocop/issues/7944): Add `MaxUnannotatedPlaceholdersAllowed` option to `Style/FormatStringToken` cop. ([@Tietew][])
* [#8379](https://github.com/rubocop/rubocop/issues/8379): Handle redundant parentheses around an interpolated expression for `Style/RedundantParentheses` cop. ([@fatkodima][])

### Bug fixes

* [#8892](https://github.com/rubocop/rubocop/issues/8892): Fix an error for `Style/StringConcatenation` when correcting nested concatenatable parts. ([@fatkodima][])
* [#8781](https://github.com/rubocop/rubocop/issues/8781): Fix handling of comments in `Style/SafeNavigation` autocorrection. ([@dvandersluis][])
* [#8907](https://github.com/rubocop/rubocop/pull/8907): Fix an incorrect auto-correct for `Layout/ClassStructure` when heredoc constant is defined after public method. ([@koic][])
* [#8889](https://github.com/rubocop/rubocop/pull/8889): Cops can use new `after_<type>` callbacks (only for nodes that may have children nodes, like `:send` and unlike `:sym`). ([@marcandre][])
* [#8906](https://github.com/rubocop/rubocop/pull/8906): Fix a false positive for `Layout/SpaceAroundOperators` when upward alignment. ([@koic][])
* [#8585](https://github.com/rubocop/rubocop/pull/8585): Fix false positive in `Style/RedundantSelf` cop with nested `self` access. ([@marcotc][])
* [#8692](https://github.com/rubocop/rubocop/pull/8692): Fix `Layout/TrailingWhitespace` auto-correction in heredoc. ([@marcandre][])

### Changes

* [#8882](https://github.com/rubocop/rubocop/pull/8882): **(Potentially breaking)** RuboCop assumes that Cop classes do not define new `on_<type>` methods at runtime (e.g. via `extend` in `initialize`). ([@marcandre][])
* [#7966](https://github.com/rubocop/rubocop/issues/7966): **(Breaking)** Enable all pending cops for RuboCop 1.0. ([@koic][])
* [#8490](https://github.com/rubocop/rubocop/pull/8490): **(Breaking)** Change logic for cop department name computation. Cops inside deep namespaces (5 or more levels deep) now belong to departments with names that are calculated by joining module names starting from the third one with slashes as separators. For example, cop `RuboCop::Cop::Foo::Bar::Baz` now belongs to `Foo/Bar` department (previously it was `Bar`). ([@dsavochkin][])
* [#8692](https://github.com/rubocop/rubocop/pull/8692): Default changed to disallow `Layout/TrailingWhitespace` in heredoc. ([@marcandre][])
* [#8894](https://github.com/rubocop/rubocop/issues/8894): Make `Security/Open` aware of `URI.open`. ([@koic][])
* [#8901](https://github.com/rubocop/rubocop/issues/8901): Fix false positive for `Naming/BinaryOperatorParameterName` when defining `=~`. ([@zajn][])
* [#8908](https://github.com/rubocop/rubocop/pull/8908): Show extension cop versions when using `--verbose-version` option. ([@koic][])

## 0.93.1 (2020-10-12)

### Bug fixes

* [#8782](https://github.com/rubocop/rubocop/issues/8782): Fix incorrect autocorrection for `Style/TernaryParentheses` with `defined?`. ([@dvandersluis][])
* [#8867](https://github.com/rubocop/rubocop/issues/8867): Rework `Lint/RedundantSafeNavigation` to be more safe. ([@fatkodima][])
* [#8864](https://github.com/rubocop/rubocop/issues/8864): Fix false positive for `Style/RedundantBegin` with a postfix `while` or `until`. ([@dvandersluis][])
* [#8869](https://github.com/rubocop/rubocop/issues/8869): Fix a false positive for `Style/RedundantBegin` when using `begin` for or assignment and method call. ([@koic][])
* [#8862](https://github.com/rubocop/rubocop/issues/8862): Fix an error for `Lint/AmbiguousRegexpLiteral` when using regexp without method calls in nested structure. ([@koic][])
* [#8872](https://github.com/rubocop/rubocop/issues/8872): Fix an error for `Metrics/ClassLength` when multiple assignments to constants. ([@koic][])
* [#8871](https://github.com/rubocop/rubocop/issues/8871): Fix a false positive for `Style/RedundantBegin` when using `begin` for method argument or part of conditions. ([@koic][])
* [#8875](https://github.com/rubocop/rubocop/issues/8875): Fix an incorrect auto-correct for `Style/ClassEqualityComparison` when comparing class name. ([@koic][])
* [#8880](https://github.com/rubocop/rubocop/issues/8880): Fix an error for `Style/ClassLength` when overlapping constant assignments. ([@koic][])

## 0.93.0 (2020-10-08)

### New features

* [#8796](https://github.com/rubocop/rubocop/pull/8796): Add new `Lint/HashCompareByIdentity` cop. ([@fatkodima][])
* [#8833](https://github.com/rubocop/rubocop/pull/8833): Add new `Style/ClassEqualityComparison` cop. ([@fatkodima][])
* [#8668](https://github.com/rubocop/rubocop/pull/8668): Add new `Lint/RedundantSafeNavigation` cop. ([@fatkodima][])
* [#8842](https://github.com/rubocop/rubocop/issues/8842): Add notification about cache being used to debug mode. ([@hatkyinc2][])
* [#8822](https://github.com/rubocop/rubocop/pull/8822): Make `Style/RedundantBegin` aware of `begin` without `rescue` or `ensure`. ([@koic][])
* [#7940](https://github.com/rubocop/rubocop/pull/7940): Add new `Lint/NoReturnInBeginEndBlocks` cop. ([@jcfausto][])

### Bug fixes

* [#8810](https://github.com/rubocop/rubocop/pull/8810): Fix multiple offense detection for `Style/RaiseArgs`. ([@pbernays][])
* [#8151](https://github.com/rubocop/rubocop/issues/8151): Fix a false positive for `Lint/BooleanSymbol` when used within `%i[...]`. ([@fatkodima][])
* [#8809](https://github.com/rubocop/rubocop/pull/8809): Fix multiple offense detection for `Style/For`. ([@pbernays][])
* [#8801](https://github.com/rubocop/rubocop/issues/8801): Fix `Layout/SpaceAroundEqualsInParameterDefault` only registered once in a line. ([@rdunlop][])
* [#8514](https://github.com/rubocop/rubocop/issues/8514): Correct multiple `Style/MethodDefParentheses` per file. ([@rdunlop][])
* [#8825](https://github.com/rubocop/rubocop/issues/8825): Fix crash in `Style/ExplicitBlockArgument` when code is called outside of a method. ([@ghiculescu][])
* [#8718](https://github.com/rubocop/rubocop/issues/8718): Fix undefined methods of pseudo location. ([@ybiquitous][])
* [#8354](https://github.com/rubocop/rubocop/issues/8354): Detect regexp named captures in `Style/CaseLikeIf` cop. ([@dsavochkin][])
* [#8821](https://github.com/rubocop/rubocop/issues/8821): Fix an incorrect autocorrect for `Style/NestedTernaryOperator` when using a nested ternary operator expression with no parentheses on the outside. ([@koic][])
* [#8834](https://github.com/rubocop/rubocop/issues/8834): Fix a false positive for `Style/ParenthesesAsGroupedExpression` when method argument parentheses are omitted and hash argument key is enclosed in parentheses. ([@koic][])
* [#8830](https://github.com/rubocop/rubocop/issues/8830): Fix bad autocorrect of `Style/StringConcatenation` when string includes double quotes. ([@tleish][])
* [#8807](https://github.com/rubocop/rubocop/pull/8807): Fix a false positive for `Style/RedundantCondition` when using assignment by hash key access. ([@koic][])
* [#8848](https://github.com/rubocop/rubocop/issues/8848): Fix a false positive for `Style/CombinableLoops` when using the same method with different arguments. ([@dvandersluis][])
* [#8843](https://github.com/rubocop/rubocop/issues/8843): Fix an incorrect autocorrect for `Lint/AmbiguousRegexpLiteral` when sending method to regexp literal receiver. ([@koic][])
* [#8842](https://github.com/rubocop/rubocop/issues/8842): Save actual status to cache, except corrected. ([@hatkyinc2][])
* [#8835](https://github.com/rubocop/rubocop/issues/8835): Fix an incorrect autocorrect for `Style/RedundantInterpolation` when using string interpolation for non-operator methods. ([@koic][])
* [#7495](https://github.com/rubocop/rubocop/issues/7495): Example for `Lint/AmbiguousBlockAssociation` cop. ([@AllanSiqueira][])
* [#8855](https://github.com/rubocop/rubocop/issues/8855): Fix an error for `Layout/EmptyLinesAroundAccessModifier` and `Style/AccessModifierDeclarations` when using only access modifier. ([@koic][])

### Changes

* [#8803](https://github.com/rubocop/rubocop/pull/8803): **(Breaking)** `RegexpNode#parsed_tree` now processes regexps including interpolation (by blanking the interpolation before parsing, rather than skipping). ([@owst][])
* [#8625](https://github.com/rubocop/rubocop/pull/8625): Improve `Style/RedundantRegexpCharacterClass` and `Style/RedundantRegexpEscape` by using `regexp_parser` gem. ([@owst][])
* [#8646](https://github.com/rubocop/rubocop/issues/8646): Faster find of all files in `TargetFinder` class which improves initial startup speed. ([@tleish][])
* [#8102](https://github.com/rubocop/rubocop/issues/8102): Consider class length instead of block length for `Struct.new`. ([@tejasbubane][])
* [#7408](https://github.com/rubocop/rubocop/issues/7408): Make `Gemspec/RequiredRubyVersion` cop aware of `Gem::Requirement`. ([@tejasbubane][])

## 0.92.0 (2020-09-25)

### New features

* [#8778](https://github.com/rubocop/rubocop/pull/8778): Add command line option `--regenerate-todo`. ([@dvandersluis][])
* [#8790](https://github.com/rubocop/rubocop/pull/8790): Add `AllowedMethods` option to `Style/OptionalBooleanParameter` cop. ([@fatkodima][])
* [#8738](https://github.com/rubocop/rubocop/issues/8738): Add autocorrection to `Style/DateTime`. ([@dvandersluis][])

### Bug fixes

* [#8774](https://github.com/rubocop/rubocop/issues/8774): Fix a false positive for `Layout/ArrayAlignment` with parallel assignment. ([@dvandersluis][])

### Changes

* [#8785](https://github.com/rubocop/rubocop/pull/8785): Update TargetRubyVersion 2.8 to 3.0 (experimental). ([@koic][])
* [#8650](https://github.com/rubocop/rubocop/issues/8650): Faster find of hidden files in `TargetFinder` class which improves rubocop initial startup speed. ([@tleish][])
* [#8783](https://github.com/rubocop/rubocop/pull/8783): Disable `Style/ArrayCoercion` cop by default. ([@koic][])

## 0.91.1 (2020-09-23)

### Bug fixes

* [#8720](https://github.com/rubocop/rubocop/issues/8720): Fix an error for `Lint/IdentityComparison` when calling `object_id` method without receiver in LHS or RHS. ([@koic][])
* [#8767](https://github.com/rubocop/rubocop/issues/8767): Fix a false positive for `Style/RedundantReturn` when a rescue has an else clause. ([@fatkodima][])
* [#8710](https://github.com/rubocop/rubocop/issues/8710): Fix a false positive for `Layout/RescueEnsureAlignment` when `Layout/BeginEndAlignment` cop is not enabled status. ([@koic][])
* [#8726](https://github.com/rubocop/rubocop/issues/8726): Fix a false positive for `Naming/VariableNumber` when naming multibyte character variable name. ([@koic][])
* [#8730](https://github.com/rubocop/rubocop/issues/8730): Fix an error for `Lint/UselessTimes` when there is a blank line in the method definition. ([@koic][])
* [#8740](https://github.com/rubocop/rubocop/issues/8740): Fix a false positive for `Style/HashAsLastArrayItem` when the hash is in an implicit array. ([@dvandersluis][])
* [#8739](https://github.com/rubocop/rubocop/issues/8739): Fix an error for `Lint/UselessTimes` when using empty block argument. ([@koic][])
* [#8742](https://github.com/rubocop/rubocop/issues/8742): Fix some assignment counts for `Metrics/AbcSize`. ([@marcandre][])
* [#8750](https://github.com/rubocop/rubocop/pull/8750): Fix an incorrect auto-correct for `Style/MultilineWhenThen` when line break for multiple candidate values of `when` statement. ([@koic][])
* [#8754](https://github.com/rubocop/rubocop/pull/8754): Fix an error for `Style/RandomWithOffset` when using a range with non-integer bounds. ([@eugeneius][])
* [#8756](https://github.com/rubocop/rubocop/issues/8756): Fix an infinite loop error for `Layout/EmptyLinesAroundAccessModifier` with `Layout/EmptyLinesAroundBlockBody` when using access modifier with block argument. ([@koic][])
* [#8372](https://github.com/rubocop/rubocop/issues/8372): Fix `Lint/RedundantCopEnableDirective` autocorrection to not leave orphaned empty `# rubocop:enable` comments. ([@dvandersluis][])
* [#8372](https://github.com/rubocop/rubocop/issues/8372): Fix `Lint/RedundantCopDisableDirective` autocorrection. ([@dvandersluis][])
* [#8764](https://github.com/rubocop/rubocop/issues/8764): Fix `Layout/CaseIndentation` not showing the cop name in output messages. ([@dvandersluis][])
* [#8771](https://github.com/rubocop/rubocop/issues/8771): Fix an error for `Style/OneLineConditional` when using `if-then-elsif-then-end`. ([@koic][])
* [#8576](https://github.com/rubocop/rubocop/issues/8576): Fix `Style/IfUnlessModifier` to ignore cop disable comment directives when considering conversion to the modifier form. ([@dsavochkin][])

### Changes

* [#8489](https://github.com/rubocop/rubocop/issues/8489): Exclude method `respond_to_missing?` from `OptionalBooleanParameter` cop. ([@em-gazelle][])
* [#7914](https://github.com/rubocop/rubocop/issues/7914): `Style/SafeNavigation` marked as having unsafe auto-correction. ([@marcandre][])
* [#8749](https://github.com/rubocop/rubocop/issues/8749): Disable `Style/IpAddresses` by default in `Gemfile` and gemspec files. ([@dvandersluis][])

## 0.91.0 (2020-09-15)

### New features

* New option `--cache-root` and support for the `RUBOCOP_CACHE_ROOT` environment variable. Both can be used to override the `AllCops: CacheRootDirectory` config, especially in a CI setting. ([@sascha-wolf][])
* [#8582](https://github.com/rubocop/rubocop/issues/8582): Add new `Layout/BeginEndAlignment` cop. ([@koic][])
* [#8699](https://github.com/rubocop/rubocop/pull/8699): Add new `Lint/IdentityComparison` cop. ([@koic][])
* Add new `Lint/UselessTimes` cop. ([@dvandersluis][])
* [#8707](https://github.com/rubocop/rubocop/pull/8707): Add new `Lint/ConstantDefinitionInBlock` cop. ([@eugeneius][])

### Bug fixes

* [#8627](https://github.com/rubocop/rubocop/issues/8627): Fix a false positive for `Lint/DuplicateRequire` when same feature argument but different require method. ([@koic][])
* [#8674](https://github.com/rubocop/rubocop/issues/8674): Fix an error for `Layout/EmptyLineAfterMultilineCondition` when conditional is at the top level. ([@fatkodima][])
* [#8658](https://github.com/rubocop/rubocop/pull/8658): Fix a false positive for `Style/RedundantSelfAssignment` when calling coercion methods. ([@fatkodima][])
* [#8669](https://github.com/rubocop/rubocop/issues/8669): Fix an offense creation for `Lint/EmptyFile`. ([@fatkodima][])
* [#8607](https://github.com/rubocop/rubocop/issues/8607): Fix a false positive for `Lint/UnreachableLoop` when conditional branch includes continue statement preceding break statement. ([@fatkodima][])
* [#8572](https://github.com/rubocop/rubocop/issues/8572): Fix a false positive for `Style/RedundantParentheses` when parentheses are used like method argument parentheses. ([@koic][])
* [#8630](https://github.com/rubocop/rubocop/issues/8630): Fix some false positives for `Style/HashTransformKeys` and `Style/HashTransformValues` when the receiver is an array. ([@eugeneius][])
* [#8653](https://github.com/rubocop/rubocop/pull/8653): Fix a false positive for `Layout/DefEndAlignment` when using refinements and `private def`. ([@koic][])
* [#8655](https://github.com/rubocop/rubocop/pull/8655): Fix a false positive for `Style/ClassAndModuleChildren` when using cbase class name. ([@koic][])
* [#8654](https://github.com/rubocop/rubocop/pull/8654): Fix a false positive for `Style/SafeNavigation` when checking `foo&.empty?` in a conditional. ([@koic][])
* [#8660](https://github.com/rubocop/rubocop/pull/8660): Fix a false positive for `Style/ClassAndModuleChildren` when using cbase module name. ([@koic][])
* [#8664](https://github.com/rubocop/rubocop/issues/8664): Fix a false positive for `Naming/BinaryOperatorParameterName` when naming multibyte character method name. ([@koic][])
* [#8604](https://github.com/rubocop/rubocop/issues/8604): Fix a false positive for `Bundler/DuplicatedGem` when gem is duplicated in condition. ([@tejasbubane][])
* [#8671](https://github.com/rubocop/rubocop/issues/8671): Fix an error for `Style/ExplicitBlockArgument` when using safe navigation method call. ([@koic][])
* [#8681](https://github.com/rubocop/rubocop/pull/8681): Fix an error for `Style/HashAsLastArrayItem` with `no_braces` for empty hash. ([@fsateler][])
* [#8682](https://github.com/rubocop/rubocop/pull/8682): Fix a positive for `Style/HashTransformKeys` and `Style/HashTransformValues` when the `each_with_object` hash is used in the transformed key or value. ([@eugeneius][])
* [#8688](https://github.com/rubocop/rubocop/issues/8688): Mark `Style/GlobalStdStream` as unsafe autocorrection. ([@marcandre][])
* [#8642](https://github.com/rubocop/rubocop/issues/8642): Fix a false negative for `Style/SpaceInsideHashLiteralBraces` when a correct empty hash precedes the incorrect hash. ([@dvandersluis][])
* [#8683](https://github.com/rubocop/rubocop/issues/8683): Make naming cops work with non-ascii characters. ([@tejasbubane][])
* [#8626](https://github.com/rubocop/rubocop/issues/8626): Fix false negatives for `Lint/UselessMethodDefinition`. ([@marcandre][])
* [#8698](https://github.com/rubocop/rubocop/pull/8698): Fix cache to avoid encoding exception. ([@marcandre][])
* [#8704](https://github.com/rubocop/rubocop/issues/8704): Fix an error for `Lint/AmbiguousOperator` when using safe navigation operator with a unary operator. ([@koic][])
* [#8661](https://github.com/rubocop/rubocop/pull/8661): Fix an incorrect auto-correct for `Style/MultilineTernaryOperator` when returning a multiline ternary operator expression. ([@koic][])
* [#8526](https://github.com/rubocop/rubocop/pull/8526): Fix a false positive for `Style/CaseEquality` cop when the receiver is not a camel cased constant. ([@koic][])
* [#8673](https://github.com/rubocop/rubocop/issues/8673): Fix the JSON parse error when specifying `--format=json` and `--stdin` options. ([@koic][])

### Changes

* [#8470](https://github.com/rubocop/rubocop/issues/8470): Do not autocorrect `Style/StringConcatenation` when parts of the expression are too complex. ([@dvandersluis][])
* [#8561](https://github.com/rubocop/rubocop/issues/8561): Fix `Lint/UselessMethodDefinition` to not register an offense when method definition includes optional arguments. ([@fatkodima][])
* [#8617](https://github.com/rubocop/rubocop/issues/8617): Fix `Style/HashAsLastArrayItem` to not register an offense when all items in an array are hashes. ([@dvandersluis][])
* [#8500](https://github.com/rubocop/rubocop/issues/8500): Add `in?` to AllowedMethods for `Lint/SafeNavigationChain` cop. ([@tejasbubane][])
* [#8629](https://github.com/rubocop/rubocop/pull/8629): Fix the cache being reusable in CI by using crc32 to calculate file hashes rather than `mtime`, which changes each CI build. ([@dvandersluis][])
* [#8663](https://github.com/rubocop/rubocop/issues/8663): Fix multiple autocorrection bugs with `Style/ClassMethodsDefinitions`. ([@dvandersluis][])
* [#8621](https://github.com/rubocop/rubocop/issues/8621): Add helpful Infinite Loop error message. ([@iSarCasm][])

## 0.90.0 (2020-09-01)

### New features

* [#8451](https://github.com/rubocop/rubocop/issues/8451): Add new `Style/RedundantSelfAssignment` cop. ([@fatkodima][])
* [#8384](https://github.com/rubocop/rubocop/issues/8384): Add new `Layout/EmptyLineAfterMultilineCondition` cop. ([@fatkodima][])
* [#8390](https://github.com/rubocop/rubocop/pull/8390): Add new `Style/SoleNestedConditional` cop. ([@fatkodima][])
* [#8563](https://github.com/rubocop/rubocop/pull/8563): Add new `Style/KeywordParametersOrder` cop. ([@fatkodima][])
* [#8486](https://github.com/rubocop/rubocop/pull/8486): Add new `Style/CombinableLoops` cop. ([@fatkodima][])
* [#8381](https://github.com/rubocop/rubocop/pull/8381): Add new `Style/ClassMethodsDefinitions` cop. ([@fatkodima][])
* [#8474](https://github.com/rubocop/rubocop/pull/8474): Add new `Lint/DuplicateRequire` cop. ([@fatkodima][])
* [#8472](https://github.com/rubocop/rubocop/issues/8472): Add new `Lint/UselessMethodDefinition` cop. ([@fatkodima][])
* [#8531](https://github.com/rubocop/rubocop/issues/8531): Add new `Lint/EmptyFile` cop. ([@fatkodima][])
* Add new `Lint/TrailingCommaInAttributeDeclaration` cop. ([@drenmi][])
* [#8578](https://github.com/rubocop/rubocop/pull/8578): Add `:restore_registry` context and `stub_cop_class` helper class. ([@marcandre][])
* [#8579](https://github.com/rubocop/rubocop/pull/8579): Add `Cop.documentation_url`. ([@marcandre][])
* [#8510](https://github.com/rubocop/rubocop/pull/8510):  Add `RegexpNode#each_capture` and `parsed_tree`. ([@marcandre][])
* [#8365](https://github.com/rubocop/rubocop/pull/8365): Cops defining `on_send` can be optimized by defining the constant `RESTRICT_ON_SEND` with a list of acceptable method names. ([@marcandre][])

### Bug fixes

* [#8508](https://github.com/rubocop/rubocop/pull/8508): Fix a false positive for `Style/CaseLikeIf` when conditional contains comparison with a class. Mark `Style/CaseLikeIf` as not safe. ([@fatkodima][])
* [#8618](https://github.com/rubocop/rubocop/issues/8618): Fix an infinite loop error for `Layout/EmptyLineBetweenDefs`. ([@fatkodima][])
* [#8534](https://github.com/rubocop/rubocop/issues/8534): Fix `Lint/BinaryOperatorWithIdenticalOperands` for binary operators used as unary operators. ([@marcandre][])
* [#8537](https://github.com/rubocop/rubocop/pull/8537): Allow a trailing comment as a description comment for `Bundler/GemComment`. ([@pocke][])
* [#8507](https://github.com/rubocop/rubocop/issues/8507): Fix `Style/RescueModifier` to handle parentheses around rescue modifiers. ([@dsavochkin][])
* [#8527](https://github.com/rubocop/rubocop/pull/8527): Prevent an incorrect auto-correction for `Style/CaseEquality` cop when comparing with `===` against a regular expression receiver. ([@koic][])
* [#8524](https://github.com/rubocop/rubocop/issues/8524): Fix `Layout/EmptyLinesAroundClassBody`  and `Layout/EmptyLinesAroundModuleBody` to correctly handle an access modifier as a first child. ([@dsavochkin][])
* [#8518](https://github.com/rubocop/rubocop/issues/8518): Fix `Lint/ConstantResolution` cop reporting offense for `module` and `class` definitions. ([@tejasbubane][])
* [#8158](https://github.com/rubocop/rubocop/issues/8158): Fix `Style/MultilineWhenThen` cop to correctly handle cases with multiline body. ([@dsavochkin][])
* [#7705](https://github.com/rubocop/rubocop/issues/7705): Fix `Style/OneLineConditional` cop to handle if/then/elsif/then/else/end cases. Add `AlwaysCorrectToMultiline` config option to this cop to always convert offenses to the multi-line form (false by default). ([@Lykos][], [@dsavochkin][])
* [#8590](https://github.com/rubocop/rubocop/issues/8590): Fix an error when auto-correcting encoding mismatch file. ([@koic][])
* [#8321](https://github.com/rubocop/rubocop/issues/8321): Enable auto-correction for `Layout/{Def}EndAlignment`, `Lint/EmptyEnsure`, `Style/ClassAndModuleChildren`. ([@marcandre][])
* [#8583](https://github.com/rubocop/rubocop/issues/8583): Fix `Style/RedundantRegexpEscape` false positive for line continuations. ([@owst][])
* [#8593](https://github.com/rubocop/rubocop/issues/8593): Fix `Style/RedundantRegexpCharacterClass` false positive for interpolated multi-line expressions. ([@owst][])
* [#8624](https://github.com/rubocop/rubocop/pull/8624): Fix an error with the `Style/CaseLikeIf` cop where it does not properly handle overridden equality methods with no arguments. ([@Skipants][])

### Changes

* [#8413](https://github.com/rubocop/rubocop/issues/8413): Pending cops warning now contains snippet that can be directly copied into `.rubocop.yml` as well as a notice about `NewCops: enable` config option. ([@colszowka][])
* [#8362](https://github.com/rubocop/rubocop/issues/8362): Add numbers of correctable offenses to summary. ([@nguyenquangminh0711][])
* [#8513](https://github.com/rubocop/rubocop/pull/8513): Clarify the ruby warning mentioned in the `Lint/ShadowingOuterLocalVariable` documentation. ([@chocolateboy][])
* [#8517](https://github.com/rubocop/rubocop/pull/8517): Make `Style/HashTransformKeys` and `Style/HashTransformValues` aware of `to_h` with block. ([@eugeneius][])
* [#8529](https://github.com/rubocop/rubocop/pull/8529): Mark `Style/FrozenStringLiteralComment` as `Safe`, but with unsafe auto-correction. ([@marcandre][])
* [#8602](https://github.com/rubocop/rubocop/pull/8602): Fix usage of `to_enum(:scan, regexp)` to work on TruffleRuby. ([@jaimerave][])

## 0.89.1 (2020-08-10)

### Bug fixes

* [#8463](https://github.com/rubocop/rubocop/pull/8463): Fix false positives for `Lint/OutOfRangeRegexpRef` when a regexp is defined and matched in separate steps. ([@eugeneius][])
* [#8464](https://github.com/rubocop/rubocop/pull/8464): Handle regexps matched with `when`, `grep`, `gsub`, `gsub!`, `sub`, `sub!`, `[]`, `slice`, `slice!`, `scan`, `index`, `rindex`, `partition`, `rpartition`, `start_with?`, and `end_with?` in `Lint/OutOfRangeRegexpRef`. ([@eugeneius][])
* [#8466](https://github.com/rubocop/rubocop/issues/8466): Fix a false positive for `Lint/UriRegexp` when using `regexp` method without receiver. ([@koic][])
* [#8478](https://github.com/rubocop/rubocop/issues/8478): Relax `Lint/BinaryOperatorWithIdenticalOperands` for mathematical operations. ([@marcandre][])
* [#8480](https://github.com/rubocop/rubocop/issues/8480): Tweak callback list of `Lint/MissingSuper`. ([@marcandre][])
* [#8481](https://github.com/rubocop/rubocop/pull/8481): Fix autocorrect for elements with newlines in `Style/SymbolArray` and `Style/WordArray`. ([@biinari][])
* [#8475](https://github.com/rubocop/rubocop/issues/8475): Fix a false positive for `Style/HashAsLastArrayItem` when there are duplicate hashes in the array. ([@wcmonty][])
* [#8497](https://github.com/rubocop/rubocop/issues/8497): Fix `Style/IfUnlessModifier` to add parentheses when converting if-end condition inside a parenthesized method argument list. ([@dsavochkin][])

### Changes

* [#8487](https://github.com/rubocop/rubocop/pull/8487): Detect `<` and `>` as comparison operators in `Style/ConditionalAssignment` cop. ([@biinari][])

## 0.89.0 (2020-08-05)

### New features

* [#8322](https://github.com/rubocop/rubocop/pull/8322): Support autocorrect for `Style/CaseEquality` cop. ([@fatkodima][])
* [#7876](https://github.com/rubocop/rubocop/issues/7876): Enhance `Gemspec/RequiredRubyVersion` cop with check that `required_ruby_version` is specified. ([@fatkodima][])
* [#8291](https://github.com/rubocop/rubocop/pull/8291): Add new `Lint/SelfAssignment` cop. ([@fatkodima][])
* [#8389](https://github.com/rubocop/rubocop/pull/8389): Add new `Lint/DuplicateRescueException` cop. ([@fatkodima][])
* [#8433](https://github.com/rubocop/rubocop/pull/8433): Add new `Lint/BinaryOperatorWithIdenticalOperands` cop. ([@fatkodima][])
* [#8430](https://github.com/rubocop/rubocop/pull/8430): Add new `Lint/UnreachableLoop` cop. ([@fatkodima][])
* [#8412](https://github.com/rubocop/rubocop/pull/8412): Add new `Style/OptionalBooleanParameter` cop. ([@fatkodima][])
* [#8432](https://github.com/rubocop/rubocop/pull/8432): Add new `Lint/FloatComparison` cop. ([@fatkodima][])
* [#8376](https://github.com/rubocop/rubocop/pull/8376): Add new `Lint/MissingSuper` cop. ([@fatkodima][])
* [#8415](https://github.com/rubocop/rubocop/pull/8415): Add new `Style/ExplicitBlockArgument` cop. ([@fatkodima][])
* [#8383](https://github.com/rubocop/rubocop/pull/8383): Support autocorrect for `Lint/Loop` cop. ([@fatkodima][])
* [#8339](https://github.com/rubocop/rubocop/pull/8339): Add `Config#for_badge` as an efficient way to get a cop's config merged with its department's. ([@marcandre][])
* [#5067](https://github.com/rubocop/rubocop/issues/5067): Add new `Style/StringConcatenation` cop. ([@fatkodima][])
* [#7425](https://github.com/rubocop/rubocop/pull/7425): Add new `Lint/TopLevelReturnWithArgument` cop. ([@iamravitejag][])
* [#8417](https://github.com/rubocop/rubocop/pull/8417): Add new `Style/GlobalStdStream` cop. ([@fatkodima][])
* [#7949](https://github.com/rubocop/rubocop/issues/7949): Add new `Style/SingleArgumentDig` cop. ([@volfgox][])
* [#8341](https://github.com/rubocop/rubocop/pull/8341): Add new `Lint/EmptyConditionalBody` cop. ([@fatkodima][])
* [#7755](https://github.com/rubocop/rubocop/issues/7755):  Add new `Lint/OutOfRangeRegexpRef` cop. ([@sonalinavlakhe][])

### Bug fixes

* [#8346](https://github.com/rubocop/rubocop/pull/8346): Allow parentheses in single-line inheritance with `Style/MethodCallWithArgsParentheses` `EnforcedStyle: omit_parentheses` to fix invalid Ruby auto-correction. ([@gsamokovarov][])
* [#8324](https://github.com/rubocop/rubocop/issues/8324): Fix crash for `Layout/SpaceAroundMethodCallOperator` when using `Proc#call` shorthand syntax. ([@fatkodima][])
* [#8332](https://github.com/rubocop/rubocop/pull/8332): Fix auto-correct in `Style/ConditionalAssignment` to preserve constant namespace. ([@biinari][])
* [#8344](https://github.com/rubocop/rubocop/issues/8344): Fix crash for `Style/CaseLikeIf` when checking against `equal?` and `match?` without a receiver. ([@fatkodima][])
* [#8323](https://github.com/rubocop/rubocop/issues/8323): Fix a false positive for `Style/HashAsLastArrayItem` when hash is not a last array item. ([@fatkodima][])
* [#8299](https://github.com/rubocop/rubocop/issues/8299): Fix an incorrect auto-correct for `Style/RedundantCondition` when using `raise`, `rescue`, or `and` without argument parentheses in `else`. ([@koic][])
* [#8335](https://github.com/rubocop/rubocop/issues/8335): Fix incorrect character class detection for nested or POSIX bracket character classes in `Style/RedundantRegexpEscape`. ([@owst][])
* [#8347](https://github.com/rubocop/rubocop/issues/8347): Fix an incorrect auto-correct for `EnforcedStyle: hash_rockets` of `Style/HashSyntax` with `Layout/HashAlignment`. ([@koic][])
* [#8375](https://github.com/rubocop/rubocop/pull/8375): Fix an infinite loop error for `Style/EmptyMethod`. ([@koic][])
* [#8385](https://github.com/rubocop/rubocop/pull/8385): Remove auto-correction for `Lint/EnsureReturn`. ([@marcandre][])
* [#8391](https://github.com/rubocop/rubocop/issues/8391): Mark `Style/ArrayCoercion` as not safe. ([@marcandre][])
* [#8406](https://github.com/rubocop/rubocop/issues/8406): Improve `Style/AccessorGrouping`'s auto-correction to remove redundant blank lines. ([@koic][])
* [#8330](https://github.com/rubocop/rubocop/issues/8330): Fix a false positive for `Style/MissingRespondToMissing` when defined method with inline access modifier. ([@koic][])
* [#8422](https://github.com/rubocop/rubocop/issues/8422): Fix an error for `Lint/SelfAssignment` when using or-assignment for constant. ([@koic][])
* [#8423](https://github.com/rubocop/rubocop/issues/8423): Fix an error for `Style/SingleArgumentDig` when without a receiver. ([@koic][])
* [#8424](https://github.com/rubocop/rubocop/issues/8424): Fix an error for `Lint/IneffectiveAccessModifier` when there is `begin...end` before a method definition. ([@koic][])
* [#8006](https://github.com/rubocop/rubocop/issues/8006): Fix line length calculation for `Style/IfUnlessModifier` to correctly take into account code before the if condition when considering conversation to a single-line form. ([@dsavochkin][])
* [#8283](https://github.com/rubocop/rubocop/issues/8283): Fix line length calculation for `Style/IfUnlessModifier` to correctly take into account a comment on the first line when considering conversation to a single-line form. ([@dsavochkin][])
* [#7957](https://github.com/rubocop/rubocop/issues/7957): Fix line length calculation for `Style/IfUnlessModifier` to correctly take into account code on the last line after the end keyword when considering conversion to a single-line form. ([@dsavochkin][])
* [#8226](https://github.com/rubocop/rubocop/issues/8226): Fix `Style/IfUnlessModifier` to add parentheses when converting if-end condition inside an array or a hash to a single-line form. ([@dsavochkin][])
* [#8443](https://github.com/rubocop/rubocop/pull/8443): Fix an incorrect auto-correct for `Style/StructInheritance` when there is a comment before class declaration. ([@koic][])
* [#8444](https://github.com/rubocop/rubocop/issues/8444): Fix an error for `Layout/FirstMethodArgumentLineBreak` when using kwargs in `super`. ([@koic][])
* [#8448](https://github.com/rubocop/rubocop/pull/8448): Fix `Style/NestedParenthesizedCalls` to include line continuations in whitespace for auto-correct. ([@biinari][])

### Changes

* [#8376](https://github.com/rubocop/rubocop/pull/8376): `Style/MethodMissingSuper` cop is removed in favor of new `Lint/MissingSuper` cop. ([@fatkodima][])
* [#8433](https://github.com/rubocop/rubocop/pull/8433): `Lint/UselessComparison` cop is removed in favor of new `Lint/BinaryOperatorWithIdenticalOperands` cop. ([@fatkodima][])
* [#8350](https://github.com/rubocop/rubocop/pull/8350): Set default max line length to 120 for `Style/MultilineMethodSignature`. ([@koic][])
* [#8338](https://github.com/rubocop/rubocop/pull/8338): **potentially breaking**. Config#for_department now returns only the config specified for that department; the 'Enabled' attribute is no longer calculated. ([@marcandre][])
* [#8037](https://github.com/rubocop/rubocop/pull/8037): **(Breaking)** Cop `Metrics/AbcSize` now counts ||=, &&=, multiple assignments, for, yield, iterating blocks. `&.` now count as conditions too (unless repeated on the same variable). Default bumped from 15 to 17. Consider using `rubocop -a --disable-uncorrectable` to ease transition. ([@marcandre][])
* [#8276](https://github.com/rubocop/rubocop/issues/8276): Cop `Metrics/CyclomaticComplexity` not longer counts `&.` when repeated on the same variable. ([@marcandre][])
* [#8204](https://github.com/rubocop/rubocop/pull/8204): **(Breaking)** Cop `Metrics/PerceivedComplexity` now counts `else` in `case` statements, `&.`, `||=`, `&&=` and blocks known to iterate. Default bumped from 7 to 8. Consider using `rubocop -a --disable-uncorrectable` to ease transition. ([@marcandre][])
* [#8416](https://github.com/rubocop/rubocop/issues/8416): Cop `Lint/InterpolationCheck` marked as unsafe. ([@marcandre][])
* [#8442](https://github.com/rubocop/rubocop/pull/8442): Remove `RuboCop::Cop::ParserDiagnostic` mixin module. ([@koic][])

## 0.88.0 (2020-07-13)

### New features

* [#8279](https://github.com/rubocop/rubocop/pull/8279): Recognise require method passed as argument in `Lint/NonDeterministicRequireOrder` cop. ([@biinari][])
* [#7333](https://github.com/rubocop/rubocop/issues/7333): Add new `Style/RedundantFileExtensionInRequire` cop. ([@fatkodima][])
* [#8316](https://github.com/rubocop/rubocop/pull/8316): Support autocorrect for `Lint/DisjunctiveAssignmentInConstructor` cop. ([@fatkodima][])
* [#8242](https://github.com/rubocop/rubocop/pull/8242): Internal profiling available with `bin/rubocop-profile` and rake tasks. ([@marcandre][])
* [#8295](https://github.com/rubocop/rubocop/pull/8295): Add new `Style/ArrayCoercion` cop. ([@fatkodima][])
* [#8293](https://github.com/rubocop/rubocop/pull/8293): Add new `Lint/DuplicateElsifCondition` cop. ([@fatkodima][])
* [#7736](https://github.com/rubocop/rubocop/issues/7736): Add new `Style/CaseLikeIf` cop. ([@fatkodima][])
* [#4286](https://github.com/rubocop/rubocop/issues/4286): Add new `Style/HashAsLastArrayItem` cop. ([@fatkodima][])
* [#8247](https://github.com/rubocop/rubocop/issues/8247): Add new `Style/HashLikeCase` cop. ([@fatkodima][])
* [#8286](https://github.com/rubocop/rubocop/issues/8286): Internal method `expect_offense` allows abbreviated offense messages. ([@marcandre][])

### Bug fixes

* [#8232](https://github.com/rubocop/rubocop/issues/8232): Fix a false positive for `Layout/EmptyLinesAroundAccessModifier` when `end` immediately after access modifier. ([@koic][])
* [#7777](https://github.com/rubocop/rubocop/issues/7777): Fix crash for `Layout/MultilineArrayBraceLayout` when comment is present after last element. ([@shekhar-patil][])
* [#7776](https://github.com/rubocop/rubocop/issues/7776): Fix crash for `Layout/MultilineMethodCallBraceLayout` when comment is present before closing braces. ([@shekhar-patil][])
* [#8282](https://github.com/rubocop/rubocop/issues/8282): Fix `Style/IfUnlessModifier` bad precedence detection. ([@tejasbubane][])
* [#8289](https://github.com/rubocop/rubocop/issues/8289): Fix `Style/AccessorGrouping` to not register offense for accessor with comment. ([@tejasbubane][])
* [#8310](https://github.com/rubocop/rubocop/pull/8310): Handle major version requirements in `Gemspec/RequiredRubyVersion`. ([@eugeneius][])
* [#8315](https://github.com/rubocop/rubocop/pull/8315): Fix crash for `Style/PercentLiteralDelimiters` when the source contains invalid characters. ([@eugeneius][])
* [#8239](https://github.com/rubocop/rubocop/pull/8239): Don't load `.rubocop.yml` files at all outside of the current project, unless they are personal configuration files and the project has no configuration. ([@deivid-rodriguez][])

### Changes

* [#8021](https://github.com/rubocop/rubocop/issues/8021): Rewrite `Layout/SpaceAroundMethodCallOperator` cop to make it faster. ([@fatkodima][])
* [#8294](https://github.com/rubocop/rubocop/pull/8294): Add `of` to `AllowedNames` of `MethodParameterName` cop. ([@AlexWayfer][])

## 0.87.1 (2020-07-07)

### Bug fixes

* [#8189](https://github.com/rubocop/rubocop/issues/8189): Fix an error for `Layout/MultilineBlockLayout` where spaces for a new line where not considered. ([@knejad][])
* [#8252](https://github.com/rubocop/rubocop/issues/8252): Fix a command line option name from `--safe-autocorrect` to `--safe-auto-correct`, which is compatible with RuboCop 0.86 and lower. ([@koic][])
* [#8259](https://github.com/rubocop/rubocop/issues/8259): Fix false positives for `Style/BisectedAttrAccessor` when accessors have different access modifiers. ([@fatkodima][])
* [#8253](https://github.com/rubocop/rubocop/issues/8253): Fix false positives for `Style/AccessorGrouping` when accessors have different access modifiers. ([@fatkodima][])
* [#8257](https://github.com/rubocop/rubocop/issues/8257): Fix an error for `Style/BisectedAttrAccessor` when using `attr_reader` and `attr_writer` with splat arguments. ([@fatkodima][])
* [#8239](https://github.com/rubocop/rubocop/pull/8239): Don't load `.rubocop.yml` from personal folders to check for exclusions if given a custom configuration file. ([@deivid-rodriguez][])
* [#8256](https://github.com/rubocop/rubocop/issues/8256): Fix an error for `--auto-gen-config` when running a cop who do not support auto-correction. ([@koic][])
* [#8262](https://github.com/rubocop/rubocop/pull/8262): Fix `Lint/DeprecatedOpenSSLConstant` auto-correction of `OpenSSL::Cipher` to use lower case, as some Linux-based systems do not accept upper cased cipher names. ([@bdewater][])

## 0.87.0 (2020-07-06)

### New features

* [#7868](https://github.com/rubocop/rubocop/pull/7868): `Cop::Base` is the new recommended base class for cops. ([@marcandre][])
* [#3983](https://github.com/rubocop/rubocop/issues/3983): Add new `Style/AccessorGrouping` cop. ([@fatkodima][])
* [#8244](https://github.com/rubocop/rubocop/pull/8244): Add new `Style/BisectedAttrAccessor` cop. ([@fatkodima][])
* [#7458](https://github.com/rubocop/rubocop/issues/7458): Add new `AsciiConstants` option for `Naming/AsciiIdentifiers`. ([@fatkodima][])
* [#7373](https://github.com/rubocop/rubocop/issues/7373): Add new `Style/RedundantAssignment` cop. ([@fatkodima][])
* [#8213](https://github.com/rubocop/rubocop/pull/8213): Permit to specify TargetRubyVersion 2.8 (experimental). ([@koic][])
* [#8159](https://github.com/rubocop/rubocop/pull/8159): Add new `CountAsOne` option for code length related `Metric` cops. ([@fatkodima][])
* [#8164](https://github.com/rubocop/rubocop/pull/8164): Support auto-correction for `Lint/InterpolationCheck`. ([@koic][])
* [#8223](https://github.com/rubocop/rubocop/pull/8223): Support auto-correction for `Style/IfUnlessModifierOfIfUnless`. ([@koic][])
* [#8172](https://github.com/rubocop/rubocop/pull/8172): Support auto-correction for `Lint/SafeNavigationWithEmpty`. ([@koic][])

### Bug fixes

* [#8039](https://github.com/rubocop/rubocop/pull/8039): Fix false positives for `Lint/ParenthesesAsGroupedExpression` in when using operators or chain functions. ([@CamilleDrapier][])
* [#8196](https://github.com/rubocop/rubocop/issues/8196): Fix a false positive for `Style/RedundantFetchBlock` when using with `Rails.cache`. ([@fatkodima][])
* [#8195](https://github.com/rubocop/rubocop/issues/8195): Fix an error for `Style/RedundantFetchBlock` when using `#fetch` with empty block. ([@koic][])
* [#8193](https://github.com/rubocop/rubocop/issues/8193): Fix a false positive for `Style/RedundantRegexpCharacterClass` when using `[\b]`. ([@owst][])
* [#8205](https://github.com/rubocop/rubocop/issues/8205): Fix a false positive for `Style/RedundantRegexpCharacterClass` when using a leading escaped `]`. ([@owst][])
* [#8208](https://github.com/rubocop/rubocop/issues/8208): Fix `Style/RedundantParentheses` with hash literal as first argument to `yield`. ([@karlwithak][])
* [#8176](https://github.com/rubocop/rubocop/pull/8176): Don't load `.rubocop.yml` from personal folders to check for exclusions if there's a project configuration. ([@deivid-rodriguez][])

### Changes

* [#7868](https://github.com/rubocop/rubocop/pull/7868): **(Breaking)** Extensive refactoring of internal classes `Team`, `Commissioner`, `Corrector`. `Cop::Cop#corrections` not completely compatible. See Upgrade Notes. ([@marcandre][])
* [#8156](https://github.com/rubocop/rubocop/issues/8156): **(Breaking)** `rubocop -a / --auto-correct` no longer run unsafe corrections; `rubocop -A / --auto-correct-all` run both safe and unsafe corrections. Options `--safe-autocorrect` is deprecated. ([@marcandre][])
* [#8207](https://github.com/rubocop/rubocop/pull/8207): **(Breaking)** Order for gems names now disregards underscores and dashes unless `ConsiderPunctuation` setting is set to `true`. ([@marcandre][])
* [#8211](https://github.com/rubocop/rubocop/pull/8211): `Style/ClassVars` cop now detects `class_variable_set`. ([@biinari][])
* [#8245](https://github.com/rubocop/rubocop/pull/8245): Detect top-level constants like `::Const` in various cops. ([@biinari][])

## 0.86.0 (2020-06-22)

### New features

* [#8147](https://github.com/rubocop/rubocop/pull/8147): Add new `Style/RedundantFetchBlock` cop. ([@fatkodima][])
* [#8111](https://github.com/rubocop/rubocop/pull/8111): Add auto-correct for `Style/StructInheritance`. ([@tejasbubane][])
* [#8113](https://github.com/rubocop/rubocop/pull/8113): Let `expect_offense` templates add variable-length whitespace with `_{foo}`. ([@eugeneius][])
* [#8148](https://github.com/rubocop/rubocop/pull/8148): Support auto-correction for `Style/MultilineTernaryOperator`. ([@koic][])
* [#8151](https://github.com/rubocop/rubocop/pull/8151): Support auto-correction for `Style/NestedTernaryOperator`. ([@koic][])
* [#8142](https://github.com/rubocop/rubocop/pull/8142): Add `Lint/ConstantResolution` cop. ([@robotdana][])
* [#8170](https://github.com/rubocop/rubocop/pull/8170): Support auto-correction for `Lint/RegexpAsCondition`. ([@koic][])
* [#8169](https://github.com/rubocop/rubocop/pull/8169): Support auto-correction for `Lint/RaiseException`. ([@koic][])

### Bug fixes

* [#8132](https://github.com/rubocop/rubocop/issues/8132): Fix the problem with `Naming/MethodName: EnforcedStyle: camelCase` and `_` or `i` variables. ([@avrusanov][])
* [#8115](https://github.com/rubocop/rubocop/issues/8115): Fix false negative for `Lint::FormatParameterMismatch` when argument contains formatting. ([@andrykonchin][])
* [#8131](https://github.com/rubocop/rubocop/pull/8131): Fix false positive for `Style/RedundantRegexpEscape` with escaped delimiters. ([@owst][])
* [#8124](https://github.com/rubocop/rubocop/issues/8124): Fix a false positive for `Lint/FormatParameterMismatch` when using named parameters with escaped `%`. ([@koic][])
* [#7979](https://github.com/rubocop/rubocop/issues/7979): Fix "uninitialized constant DidYouMean::SpellChecker" exception. ([@bquorning][])
* [#8098](https://github.com/rubocop/rubocop/issues/8098): Fix a false positive for `Style/RedundantRegexpCharacterClass` when using interpolations. ([@owst][])
* [#8150](https://github.com/rubocop/rubocop/pull/8150): Fix a false positive for `Layout/EmptyLinesAroundAttributeAccessor` when using attribute accessors in `if` ... `else` branches. ([@koic][])
* [#8179](https://github.com/rubocop/rubocop/issues/8179): Fix an infinite correction loop error for `Layout/MultilineBlockLayout` when missing newline before opening parenthesis `(` for block body. ([@koic][])
* [#8185](https://github.com/rubocop/rubocop/issues/8185): Fix a false positive for `Style/YodaCondition` when interpolation is used on the left hand side. ([@koic][])

### Changes

* [#8149](https://github.com/rubocop/rubocop/pull/8149): **(Breaking)** Cop `Metrics/CyclomaticComplexity` now counts `&.`, `||=`, `&&=` and blocks known to iterate. Default bumped from 6 to 7. Consider using `rubocop -a --disable-uncorrectable` to ease transition. ([@marcandre][])
* [#8146](https://github.com/rubocop/rubocop/pull/8146): Use UTC in RuboCop todo file generation. ([@mauro-oto][])
* [#8178](https://github.com/rubocop/rubocop/pull/8178): Mark unsafe for `Lint/RaiseException`. ([@koic][])

## 0.85.1 (2020-06-07)

### Bug fixes

* [#8083](https://github.com/rubocop/rubocop/issues/8083): Fix an error for `Lint/MixedRegexpCaptureTypes` cop when using a regular expression that cannot be processed by regexp_parser gem. ([@koic][])
* [#8081](https://github.com/rubocop/rubocop/issues/8081): Fix a false positive for `Lint/SuppressedException` when empty rescue block in `do` block. ([@koic][])
* [#8096](https://github.com/rubocop/rubocop/issues/8096): Fix a false positive for `Lint/SuppressedException` when empty rescue block in defs. ([@koic][])
* [#8108](https://github.com/rubocop/rubocop/issues/8108): Fix infinite loop in `Layout/HeredocIndentation` auto-correct. ([@jonas054][])
* [#8042](https://github.com/rubocop/rubocop/pull/8042): Fix raising error in `Lint::FormatParameterMismatch` when it handles invalid format strings and add new offense. ([@andrykonchin][])

## 0.85.0 (2020-06-01)

### New features

* [#6289](https://github.com/rubocop/rubocop/issues/6289): Add new `CheckDefinitionPathHierarchy` option for `Naming/FileName`. ([@jschneid][])
* [#8055](https://github.com/rubocop/rubocop/pull/8055): Add new `Style/RedundantRegexpCharacterClass` cop. ([@owst][])
* [#8069](https://github.com/rubocop/rubocop/issues/8069): New option for `expect_offense` to help format offense templates. ([@marcandre][])
* [#7908](https://github.com/rubocop/rubocop/pull/7908): Add new `Style/RedundantRegexpEscape` cop. ([@owst][])
* [#7978](https://github.com/rubocop/rubocop/pull/7978): Add new option `OnlyFor` to the `Bundler/GemComment` cop. ([@ric2b][])
* [#8063](https://github.com/rubocop/rubocop/issues/8063): Add new `AllowedNames` option for `Naming/ClassAndModuleCamelCase`. ([@tejasbubane][])
* [#8050](https://github.com/rubocop/rubocop/pull/8050): New option `--display-only-failed` that can be used with `--format junit`. Speeds up test report processing for large codebases and helps address the sorts of concerns raised at [mikian/rubocop-junit-formatter #18](https://github.com/mikian/rubocop-junit-formatter/issues/18). ([@burnettk][])
* [#7746](https://github.com/rubocop/rubocop/issues/7746): Add new `Lint/MixedRegexpCaptureTypes` cop. ([@pocke][])

### Bug fixes

* [#8008](https://github.com/rubocop/rubocop/issues/8008): Fix an error for `Lint/SuppressedException` when empty rescue block in `def`. ([@koic][])
* [#8012](https://github.com/rubocop/rubocop/issues/8012): Fix an incorrect auto-correct for `Lint/DeprecatedOpenSSLConstant` when deprecated OpenSSL constant is used in a block. ([@koic][])
* [#8017](https://github.com/rubocop/rubocop/pull/8017): Fix a false positive for `Lint/SuppressedException` when empty rescue with comment in `def`. ([@koic][])
* [#7990](https://github.com/rubocop/rubocop/issues/7990): Fix resolving `inherit_gem` in remote configs. ([@CvX][])
* [#8035](https://github.com/rubocop/rubocop/issues/8035): Fix a false positive for `Lint/DeprecatedOpenSSLConstant` when using double quoted string argument. ([@koic][])
* [#7971](https://github.com/rubocop/rubocop/issues/7971): Fix an issue where `--disable-uncorrectable` would not update uncorrected code with `rubocop:todo`. ([@rrosenblum][])
* [#8035](https://github.com/rubocop/rubocop/issues/8035): Fix a false positive for `Lint/DeprecatedOpenSSLConstant` when argument is a variable, method, or constant. ([@koic][])

### Changes

* [#8056](https://github.com/rubocop/rubocop/pull/8056): **(Breaking)** Remove support for unindent/active_support/powerpack from `Layout/HeredocIndentation`, so it only recommends using squiggly heredoc. ([@bquorning][])

## 0.84.0 (2020-05-21)

### New features

* [#7735](https://github.com/rubocop/rubocop/issues/7735): `NodePattern` and `AST` classes have been moved to the [`rubocop-ast` gem](https://github.com/rubocop/rubocop-ast). ([@marcandre][])
* [#7950](https://github.com/rubocop/rubocop/pull/7950): Add new `Lint/DeprecatedOpenSSLConstant` cop. ([@bdewater][])
* [#7976](https://github.com/rubocop/rubocop/issues/7976): Add `AllowAliasSyntax` and `AllowedMethods` options for `Layout/EmptyLinesAroundAttributeAccessor`. ([@koic][])
* [#7984](https://github.com/rubocop/rubocop/pull/7984): New `rake` task "check_commit" will run `rspec` and `rubocop` on files touched by the last commit. Currently available when developing from the main repository only. ([@marcandre][])

### Bug fixes

* [#7953](https://github.com/rubocop/rubocop/issues/7953): Fix an error for `Lint/AmbiguousOperator` when a method with no arguments is used in advance. ([@koic][])
* [#7962](https://github.com/rubocop/rubocop/issues/7962): Fix a false positive for `Lint/ParenthesesAsGroupedExpression` when heredoc has a space between the same string as the method name and `(`. ([@koic][])
* [#7967](https://github.com/rubocop/rubocop/pull/7967): `Style/SlicingWithRange` cop now supports any expression as its first index. ([@zverok][])
* [#7972](https://github.com/rubocop/rubocop/issues/7972): Fix an incorrect autocorrect for `Style/HashSyntax` when using a return value uses `return`. ([@koic][])
* [#7886](https://github.com/rubocop/rubocop/issues/7886): Fix a bug in `AllowComments` logic in `Lint/SuppressedException`. ([@jonas054][])
* [#7991](https://github.com/rubocop/rubocop/issues/7991): Fix an error for `Layout/EmptyLinesAroundAttributeAccessor` when attribute method is method chained. ([@koic][])
* [#7993](https://github.com/rubocop/rubocop/issues/7993): Fix a false positive for `Migration/DepartmentName` when a disable comment contains an unexpected character for department name. ([@koic][])
* [#7983](https://github.com/rubocop/rubocop/pull/7983): Make the config loader Bundler-aware. ([@CvX][])

### Changes

* [#7952](https://github.com/rubocop/rubocop/pull/7952): **(Breaking)** Change the max line length of `Layout/LineLength` to 120 by default. ([@koic][])
* [#7959](https://github.com/rubocop/rubocop/pull/7959): Change enforced style to conditionals for `Style/AndOr`. ([@koic][])
* [#7985](https://github.com/rubocop/rubocop/pull/7985): Add `EnforcedStyle` for `Style/DoubleNegation` cop and allow double negation in contexts that use boolean as a return value. ([@koic][])

## 0.83.0 (2020-05-11)

### New features

* [#7951](https://github.com/rubocop/rubocop/pull/7951): Include `rakefile` file by default. ([@jethrodaniel][])
* [#7921](https://github.com/rubocop/rubocop/pull/7921): Add new `Style/SlicingWithRange` cop. ([@zverok][])
* [#7895](https://github.com/rubocop/rubocop/pull/7895): Include `.simplecov` file by default. ([@robotdana][])
* [#7916](https://github.com/rubocop/rubocop/pull/7916): Support auto-correction for `Lint/AmbiguousRegexpLiteral`. ([@koic][])
* [#7917](https://github.com/rubocop/rubocop/pull/7917): Support auto-correction for `Lint/UselessAccessModifier`. ([@koic][])
* [#595](https://github.com/rubocop/rubocop/issues/595): Add ERB pre-processing for configuration files. ([@jonas054][])
* [#7918](https://github.com/rubocop/rubocop/pull/7918): Support auto-correction for `Lint/AmbiguousOperator`. ([@koic][])
* [#7937](https://github.com/rubocop/rubocop/pull/7937): Support auto-correction for `Style/IfWithSemicolon`. ([@koic][])
* [#3696](https://github.com/rubocop/rubocop/issues/3696): Add `AllowComments` option to `Lint/EmptyWhen` cop. ([@koic][])
* [#7910](https://github.com/rubocop/rubocop/pull/7910): Support auto-correction for `Lint/ParenthesesAsGroupedExpression`. ([@koic][])
* [#7925](https://github.com/rubocop/rubocop/pull/7925): Support auto-correction for `Layout/ConditionPosition`. ([@koic][])
* [#7934](https://github.com/rubocop/rubocop/pull/7934): Support auto-correction for `Lint/EnsureReturn`. ([@koic][])
* [#7922](https://github.com/rubocop/rubocop/pull/7922): Add new `Layout/EmptyLineAroundAttributeAccessor` cop. ([@koic][])

### Bug fixes

* [#7929](https://github.com/rubocop/rubocop/issues/7929): Fix `Style/FrozenStringLiteralComment` to accept frozen_string_literal anywhere in leading comment lines. ([@jeffcarbs][])
* [#7882](https://github.com/rubocop/rubocop/pull/7882): Fix `Style/CaseEquality` when `AllowOnConstant` is `true` and the method receiver is implicit. ([@rafaelfranca][])
* [#7790](https://github.com/rubocop/rubocop/issues/7790): Fix `--parallel` and `--ignore-parent-exclusion` combination. ([@jonas054][])
* [#7881](https://github.com/rubocop/rubocop/issues/7881): Fix `--parallel` and `--force-default-config` combination. ([@jonas054][])
* [#7635](https://github.com/rubocop/rubocop/issues/7635): Fix a false positive for `Style/MultilineWhenThen` when `then` required for a body of `when` is used. ([@koic][])
* [#7905](https://github.com/rubocop/rubocop/pull/7905): Fix an error when running `rubocop --only` or `rubocop --except` options without cop name argument. ([@koic][])
* [#7903](https://github.com/rubocop/rubocop/pull/7903): Fix an incorrect auto-correct for `Style/HashTransformKeys` and `Style/HashTransformValues` cops when line break before `to_h` method. ([@diogoosorio][], [@koic][])
* [#7899](https://github.com/rubocop/rubocop/issues/7899): Fix an infinite loop error for `Layout/SpaceAroundOperators` with `Layout/ExtraSpacing` when using `ForceEqualSignAlignment: true`. ([@koic][])
* [#7885](https://github.com/rubocop/rubocop/issues/7885): Fix `Style/IfUnlessModifier` logic when tabs are used for indentation. ([@jonas054][])
* [#7909](https://github.com/rubocop/rubocop/pull/7909): Fix a false positive for `Lint/ParenthesesAsGroupedExpression` when using an intended grouped parentheses. ([@koic][])
* [#7913](https://github.com/rubocop/rubocop/pull/7913): Fix a false positive for `Lint/LiteralAsCondition` when using `true` literal in `while` and similar cases. ([@koic][])
* [#7928](https://github.com/rubocop/rubocop/issues/7928): Fix a false message for `Style/GuardClause` when using `and` or `or` operators for guard clause in `then` or `else` branches. ([@koic][])
* [#7928](https://github.com/rubocop/rubocop/issues/7928): Fix a false positive for `Style/GuardClause` when assigning the result of a guard condition with `else`. ([@koic][])

### Changes

* [#7860](https://github.com/rubocop/rubocop/issues/7860): Change `AllowInHeredoc` option of `Layout/TrailingWhitespace` to `true` by default. ([@koic][])
* [#7094](https://github.com/rubocop/rubocop/issues/7094): Clarify alignment in `Layout/MultilineOperationIndentation`. ([@jonas054][])
* [#4245](https://github.com/rubocop/rubocop/issues/4245): **(Breaking)** Inspect all files given on command line unless `--only-recognized-file-types` is given. ([@jonas054][])
* [#7390](https://github.com/rubocop/rubocop/issues/7390): **(Breaking)** Enabling a cop overrides disabling its department. ([@jonas054][])
* [#7936](https://github.com/rubocop/rubocop/issues/7936): Mark `Lint/BooleanSymbol` as unsafe. ([@laurmurclar][])
* [#7948](https://github.com/rubocop/rubocop/pull/7948): Mark unsafe for `Style/OptionalArguments`. ([@koic][])
* [#7931](https://github.com/rubocop/rubocop/pull/7931): Remove dependency on the `jaro_winkler` gem, instead depending on `did_you_mean`. This may be a breaking change for RuboCop libraries calling `NameSimilarity#find_similar_name`. ([@bquorning][])

## 0.82.0 (2020-04-16)

### New features

* [#7867](https://github.com/rubocop/rubocop/pull/7867): Add support for tabs in indentation. ([@DracoAter][])
* [#7863](https://github.com/rubocop/rubocop/issues/7863): Corrector now accepts nodes in addition to ranges. ([@marcandre][])
* [#7862](https://github.com/rubocop/rubocop/issues/7862): Corrector now has a `wrap` method. ([@marcandre][])
* [#7850](https://github.com/rubocop/rubocop/issues/7850): Make it possible to enable/disable pending cops. ([@koic][])
* [#7861](https://github.com/rubocop/rubocop/issues/7861): Make it to allow `Style/CaseEquality` when the receiver is a constant. ([@rafaelfranca][])
* [#7851](https://github.com/rubocop/rubocop/pull/7851): Add a new `Style/ExponentialNotation` cop. ([@tdeo][])
* [#7384](https://github.com/rubocop/rubocop/pull/7384): Add new `Style/DisableCopsWithinSourceCodeDirective` cop. ([@egze][])
* [#7826](https://github.com/rubocop/rubocop/issues/7826): Add new `Layout/SpaceAroundMethodCallOperator` cop. ([@saurabhmaurya15][])

### Bug fixes

* [#7871](https://github.com/rubocop/rubocop/pull/7871): Fix an auto-correction bug in `Lint/BooleanSymbol`. ([@knu][])
* [#7842](https://github.com/rubocop/rubocop/issues/7842): Fix a false positive for `Lint/RaiseException` when raising Exception with explicit namespace. ([@koic][])
* [#7834](https://github.com/rubocop/rubocop/issues/7834): Fix `Lint/UriRegexp` to register offense with array arguments. ([@tejasbubane][])
* [#7841](https://github.com/rubocop/rubocop/issues/7841): Fix an error for `Style/TrailingCommaInBlockArgs` when lambda literal (`->`) has multiple arguments. ([@koic][])
* [#7842](https://github.com/rubocop/rubocop/issues/7842): Fix a false positive for `Lint/RaiseException` when Exception without cbase specified under the namespace `Gem` by adding  `AllowedImplicitNamespaces` option. ([@koic][])
* `Style/IfUnlessModifier` does not infinite-loop when auto-correcting long lines which use if/unless modifiers and have multiple statements separated by semicolons. ([@alexdowad][])
* [rubocop/rubocop-rails#127](https://github.com/rubocop/rubocop-rails/issues/127): Use `ConfigLoader.default_configuration` for the default config. ([@hanachin][])

### Changes

* [#7867](https://github.com/rubocop/rubocop/pull/7867): **(Breaking)** Renamed `Layout/Tab` cop to `Layout/IndentationStyle`. ([@DracoAter][])
* [#7869](https://github.com/rubocop/rubocop/pull/7869): **(Compatibility)** Drop support for Ruby 2.3. ([@koic][])

## 0.81.0 (2020-04-01)

### New features

* [#7299](https://github.com/rubocop/rubocop/issues/7299): Add new `Lint/RaiseException` cop. ([@denys281][])
* [#7793](https://github.com/rubocop/rubocop/pull/7793): Prefer `include?` over `member?` in `Style/CollectionMethods`. ([@dmolesUC][])
* [#7654](https://github.com/rubocop/rubocop/issues/7654): Support `with_fixed_indentation` option for `Layout/ArrayAlignment` cop. ([@nikitasakov][])
* [#7783](https://github.com/rubocop/rubocop/pull/7783): Support Ruby 2.7's numbered parameter for `Style/RedundantSort`. ([@koic][])
* [#7795](https://github.com/rubocop/rubocop/issues/7795): Make `Layout/EmptyLineAfterGuardClause` aware of case where `and` or `or` is used before keyword that break control (e.g. `and return`). ([@koic][])
* [#7786](https://github.com/rubocop/rubocop/pull/7786): Support Ruby 2.7's pattern match for `Layout/ElseAlignment` cop. ([@koic][])
* [#7784](https://github.com/rubocop/rubocop/pull/7784): Support Ruby 2.7's numbered parameter for `Lint/SafeNavigationChain`. ([@koic][])
* [#7331](https://github.com/rubocop/rubocop/issues/7331): Add `forbidden` option to `Style/ModuleFunction` cop. ([@weh][])
* [#7699](https://github.com/rubocop/rubocop/pull/7699): Add new `Lint/StructNewOverride` cop. ([@ybiquitous][])
* [#7637](https://github.com/rubocop/rubocop/pull/7637): Add new `Style/TrailingCommaInBlockArgs` cop. ([@pawptart][])
* [#7809](https://github.com/rubocop/rubocop/pull/7809): Add auto-correction for `Style/EndBlock` cop. ([@tejasbubane][])
* [#7739](https://github.com/rubocop/rubocop/pull/7739): Add `IgnoreNotImplementedMethods` configuration to `Lint/UnusedMethodArgument`. ([@tejasbubane][])
* [#7740](https://github.com/rubocop/rubocop/issues/7740): Add `AllowModifiersOnSymbols` configuration to `Style/AccessModifierDeclarations`. ([@tejasbubane][])
* [#7812](https://github.com/rubocop/rubocop/pull/7812): Add auto-correction for `Lint/BooleanSymbol` cop. ([@tejasbubane][])
* [#7823](https://github.com/rubocop/rubocop/pull/7823): Add `IgnoredMethods` configuration in `Metrics/AbcSize`, `Metrics/CyclomaticComplexity`, and `Metrics/PerceivedComplexity` cops. ([@drenmi][])
* [#7816](https://github.com/rubocop/rubocop/pull/7816): Support Ruby 2.7's numbered parameter for `Style/Lambda`. ([@koic][])
* [#7829](https://github.com/rubocop/rubocop/issues/7829): Fix an error for `Style/OneLineConditional` when one of the branches contains `next` keyword. ([@koic][])

### Bug fixes

* [#7236](https://github.com/rubocop/rubocop/pull/7236): Mark `Style/InverseMethods` auto-correct as incompatible with `Style/SymbolProc`. ([@drenmi][])
* [#7144](https://github.com/rubocop/rubocop/issues/7144): Fix `Style/Documentation` constant visibility declaration in namespace. ([@AdrienSldy][])
* [#7779](https://github.com/rubocop/rubocop/issues/7779): Fix a false positive for `Style/MultilineMethodCallIndentation` when using Ruby 2.7's numbered parameter. ([@koic][])
* [#7733](https://github.com/rubocop/rubocop/issues/7733): Fix rubocop-junit-formatter incompatibility XML for JUnit formatter. ([@koic][])
* [#7767](https://github.com/rubocop/rubocop/issues/7767): Skip array literals in `Style/HashTransformValues` and `Style/HashTransformKeys`. ([@tejasbubane][])
* [#7791](https://github.com/rubocop/rubocop/issues/7791): Fix an error on auto-correction for `Layout/BlockEndNewline` when `}` of multiline block without processing is not on its own line. ([@koic][])
* [#7778](https://github.com/rubocop/rubocop/issues/7778): Fix a false positive for `Layout/EndAlignment` when a non-whitespace is used before the `end` keyword. ([@koic][])
* [#7806](https://github.com/rubocop/rubocop/pull/7806): Fix an error for `Lint/ErbNewArguments` cop when inspecting `ActionView::Template::Handlers::ERB.new`. ([@koic][])
* [#7814](https://github.com/rubocop/rubocop/issues/7814): Fix a false positive for `Migrate/DepartmentName` cop when inspecting an unexpected disabled comment format. ([@koic][])
* [#7728](https://github.com/rubocop/rubocop/issues/7728): Fix an error for `Style/OneLineConditional` when one of the branches contains a self keyword. ([@koic][])
* [#7825](https://github.com/rubocop/rubocop/issues/7825): Fix crash for `Layout/MultilineMethodCallIndentation` with key access to hash. ([@tejasbubane][])
* [#7831](https://github.com/rubocop/rubocop/issues/7831): Fix a false positive for `Style/HashEachMethods` when receiver is implicit. ([@koic][])

### Changes

* [#7797](https://github.com/rubocop/rubocop/pull/7797): Allow unicode-display_width dependency version 1.7.0. ([@yuritomanek][])
* [#7805](https://github.com/rubocop/rubocop/pull/7805): Change `AllowComments` option of `Lint/SuppressedException` to true by default. ([@koic][])
* [#7320](https://github.com/rubocop/rubocop/issues/7320): `Naming/MethodName` now flags `attr_reader/attr_writer/attr_accessor/attr`. ([@denys281][])
* [#7813](https://github.com/rubocop/rubocop/issues/7813): **(Breaking)** Remove `Lint/EndInMethod` cop. ([@tejasbubane][])

## 0.80.1 (2020-02-29)

### Bug fixes

* [#7719](https://github.com/rubocop/rubocop/issues/7719): Fix `Style/NestedParenthesizedCalls` cop for newline. ([@tejasbubane][])
* [#7709](https://github.com/rubocop/rubocop/issues/7709): Fix correction of `Style/RedundantCondition` when the else branch contains a range. ([@rrosenblum][])
* [#7682](https://github.com/rubocop/rubocop/issues/7682): Fix `Style/InverseMethods` autofix leaving parenthesis. ([@tejasbubane][])
* [#7745](https://github.com/rubocop/rubocop/issues/7745): Suppress a pending cop warnings when pending cop's department is disabled. ([@koic][])
* [#7759](https://github.com/rubocop/rubocop/issues/7759): Fix an error for `Layout/LineLength` cop when using lambda syntax that argument is not enclosed in parentheses. ([@koic][])

### Changes

* [#7765](https://github.com/rubocop/rubocop/pull/7765): When warning about a pending cop, display the version with the cop added. ([@koic][])

## 0.80.0 (2020-02-18)

### New features

* [#7693](https://github.com/rubocop/rubocop/pull/7693): NodePattern: Add `` ` `` for descendant search. ([@marcandre][])
* [#7577](https://github.com/rubocop/rubocop/pull/7577): Add `AllowGemfileRubyComment` configuration on `Layout/LeadingCommentSpace`. ([@cetinajero][])
* [#7663](https://github.com/rubocop/rubocop/pull/7663): Add new `Style/HashTransformKeys` and `Style/HashTransformValues` cops. ([@djudd][], [@eugeneius][])
* [#7619](https://github.com/rubocop/rubocop/issues/7619): Support auto-correct of legacy cop names for `Migration/DepartmentName`. ([@koic][])
* [#7659](https://github.com/rubocop/rubocop/pull/7659): `Layout/LineLength` auto-correct now breaks up long lines with blocks. ([@maxh][])
* [#7677](https://github.com/rubocop/rubocop/pull/7677): Add new `Style/HashEachMethods` cop for `Hash#each_key` and `Hash#each_value`. ([@jemmaissroff][])
* Add `BracesRequiredMethods` parameter to `Style/BlockDelimiters` to require braces for specific methods such as Sorbet's `sig`. ([@maxh][])
* [#7686](https://github.com/rubocop/rubocop/pull/7686): Add new `JUnitFormatter` formatter based on `rubocop-junit-formatter` gem. ([@koic][])
* [#7715](https://github.com/rubocop/rubocop/pull/7715): Add `Steepfile` to default `Include` list. ([@ybiquitous][])

### Bug fixes

* [#7644](https://github.com/rubocop/rubocop/issues/7644): Fix patterns with named wildcards in unions. ([@marcandre][])
* [#7639](https://github.com/rubocop/rubocop/pull/7639): Fix logical operator edge case in `omit_parentheses` style of `Style/MethodCallWithArgsParentheses`. ([@gsamokovarov][])
* [#7661](https://github.com/rubocop/rubocop/pull/7661): Fix to return correct info from multi-line regexp. ([@Tietew][])
* [#7655](https://github.com/rubocop/rubocop/issues/7655): Fix an error when processing a regexp with a line break at the start of capture parenthesis. ([@koic][])
* [#7647](https://github.com/rubocop/rubocop/issues/7647): Fix an `undefined method on_numblock` error when using Ruby 2.7's numbered parameters. ([@hanachin][])
* [#7675](https://github.com/rubocop/rubocop/issues/7675): Fix a false negative for `Layout/SpaceBeforeFirstArg` when a vertical argument positions are aligned. ([@koic][])
* [#7688](https://github.com/rubocop/rubocop/issues/7688): Fix a bug in `Style/MethodCallWithArgsParentheses` that made `--auto-gen-config` crash. ([@buehmann][])
* [#7203](https://github.com/rubocop/rubocop/issues/7203): Fix an infinite loop error for `Style/TernaryParentheses` with `Style/RedundantParentheses` when using `EnforcedStyle: require_parentheses_when_complex`. ([@koic][])
* [#7708](https://github.com/rubocop/rubocop/issues/7708): Make it possible to use EOL `rubocop:disable` comments on comment lines. ([@jonas054][])
* [#7712](https://github.com/rubocop/rubocop/issues/7712): Fix an incorrect auto-correct for `Style/OrAssignment` when using `elsif` branch. ([@koic][])

### Changes

* [#7636](https://github.com/rubocop/rubocop/issues/7636): Remove `console` from `Lint/Debugger` to prevent false positives. ([@gsamokovarov][])
* [#7641](https://github.com/rubocop/rubocop/issues/7641): **(Breaking)** Remove `Style/BracesAroundHashParameters` cop. ([@pocke][])
* Add the method name to highlight area of `Layout/EmptyLineBetweenDefs` to help provide more context. ([@rrosenblum][])
* [#7652](https://github.com/rubocop/rubocop/pull/7652): Allow `pp` to allowed names of `Naming/MethodParameterName` cop in default config. ([@masarakki][])
* [#7309](https://github.com/rubocop/rubocop/pull/7309): Mark `Lint/UselessSetterCall` an "not safe" and improve documentation. ([@jonas054][])
* [#7723](https://github.com/rubocop/rubocop/pull/7723): Enable `Migration/DepartmentName` cop by default. ([@koic][])

## 0.79.0 (2020-01-06)

### New features

* [#7296](https://github.com/rubocop/rubocop/issues/7296): Recognize `console` and `binding.console` ([rails/web-console](https://github.com/rails/web-console)) calls in `Lint/Debuggers`. ([@gsamokovarov][])
* [#7567](https://github.com/rubocop/rubocop/pull/7567): Introduce new `pending` status for new cops. ([@Darhazer][], [@pirj][])
* [#7426](https://github.com/rubocop/rubocop/issues/7426): Add `always_true` style to Style/FrozenStringLiteralComment. ([@parkerfinch][], [@gfyoung][])

### Bug fixes

* [#7193](https://github.com/rubocop/rubocop/issues/7193): Prevent `Style/PercentLiteralDelimiters` from changing `%i` literals that contain escaped delimiters. ([@buehmann][])
* [#7590](https://github.com/rubocop/rubocop/issues/7590): Fix an error for `Layout/SpaceBeforeBlockBraces` when using with `EnforcedStyle: line_count_based` of `Style/BlockDelimiters` cop. ([@koic][])
* [#7569](https://github.com/rubocop/rubocop/issues/7569): Make `Style/YodaCondition` accept `__FILE__ == $0`. ([@koic][])
* [#7576](https://github.com/rubocop/rubocop/issues/7576): Fix an error for `Gemspec/OrderedDependencies` when using a local variable in an argument of dependent gem. ([@koic][])
* [#7595](https://github.com/rubocop/rubocop/issues/7595): Make `Style/NumericPredicate` aware of ignored methods when specifying ignored methods. ([@koic][])
* [#7607](https://github.com/rubocop/rubocop/issues/7607): Fix `Style/FrozenStringLiteralComment` infinite loop when magic comments are newline-separated. ([@pirj][])
* [#7602](https://github.com/rubocop/rubocop/pull/7602): Ensure proper handling of Ruby 2.7 syntax. ([@drenmi][])
* [#7620](https://github.com/rubocop/rubocop/issues/7620): Fix a false positive for `Migration/DepartmentName` when a disable comment contains a plain comment. ([@koic][])
* [#7616](https://github.com/rubocop/rubocop/issues/7616): Fix an incorrect auto-correct for `Style/MultilineWhenThen` for when statement with then is an array or a hash. ([@koic][])
* [#7628](https://github.com/rubocop/rubocop/issues/7628): Fix an incorrect auto-correct for `Layout/MultilineBlockLayout` removing trailing comma with single argument. ([@pawptart][])
* [#7627](https://github.com/rubocop/rubocop/issues/7627): Fix a false negative for `Migration/DepartmentName` when there is space around `:` (e.g. `# rubocop : disable`). ([@koic][])

### Changes

* [#7287](https://github.com/rubocop/rubocop/issues/7287): `Style/FrozenStringLiteralComment` is now considered unsafe. ([@buehmann][])

## 0.78.0 (2019-12-18)

### New features

* [#7528](https://github.com/rubocop/rubocop/pull/7528): Add new `Lint/NonDeterministicRequireOrder` cop. ([@mangara][])
* [#7559](https://github.com/rubocop/rubocop/pull/7559): Add `EnforcedStyleForExponentOperator` parameter to `Layout/SpaceAroundOperators` cop. ([@khiav223577][])

### Bug fixes

* [#7530](https://github.com/rubocop/rubocop/issues/7530): Typo in `Style/TrivialAccessors`'s `AllowedMethods`. ([@movermeyer][])
* [#7532](https://github.com/rubocop/rubocop/issues/7532): Fix an error for `Style/TrailingCommaInArguments` when using an anonymous function with multiple line arguments with `EnforcedStyleForMultiline: consistent_comma`. ([@koic][])
* [#7534](https://github.com/rubocop/rubocop/issues/7534): Fix an incorrect auto-correct for `Style/BlockDelimiters` cop and `Layout/SpaceBeforeBlockBraces` cop with `EnforcedStyle: no_space` when using multiline braces. ([@koic][])
* [#7231](https://github.com/rubocop/rubocop/issues/7231): Fix the exit code to be `2` rather when `0` when the config file contains an unknown cop. ([@jethroo][])
* [#7513](https://github.com/rubocop/rubocop/issues/7513): Fix abrupt error on auto-correcting with `--disable-uncorrectable`. ([@tejasbubane][])
* [#7537](https://github.com/rubocop/rubocop/issues/7537): Fix a false positive for `Layout/SpaceAroundOperators` when using a Rational literal with `/` (e.g. `2/3r`). ([@koic][])
* [#7029](https://github.com/rubocop/rubocop/issues/7029): Make `Style/Attr` not flag offense for custom `attr` method. ([@tejasbubane][])
* [#7574](https://github.com/rubocop/rubocop/issues/7574): Fix a corner case that made `Style/GuardClause` crash. ([@buehmann][])

### Changes

* [#7514](https://github.com/rubocop/rubocop/pull/7514): Expose correctable status on offense and in formatters. ([@tyler-ball][])
* [#7542](https://github.com/rubocop/rubocop/pull/7542): **(Breaking)** Move `LineLength` cop from `Metrics` department to `Layout` department. ([@koic][])

## 0.77.0 (2019-11-27)

### Bug fixes

* [#7493](https://github.com/rubocop/rubocop/issues/7493): Fix `Style/RedundantReturn` to inspect conditional constructs that are preceded by other statements. ([@buehmann][])
* [#7509](https://github.com/rubocop/rubocop/issues/7509): Fix `Layout/SpaceInsideArrayLiteralBrackets` to correct empty lines. ([@ayacai115][])
* [#7517](https://github.com/rubocop/rubocop/issues/7517): `Style/SpaceAroundKeyword` allows `::` after `super`. ([@ozydingo][])
* [#7515](https://github.com/rubocop/rubocop/issues/7515): Fix a false negative for `Style/RedundantParentheses` when calling a method with safe navigation operator. ([@koic][])
* [#7477](https://github.com/rubocop/rubocop/issues/7477): Fix line length auto-correct for semicolons in string literals. ([@maxh][])
* [#7522](https://github.com/rubocop/rubocop/pull/7522): Fix a false-positive edge case (`n % 2 == 2`) for `Style/EvenOdd`. ([@buehmann][])
* [#7506](https://github.com/rubocop/rubocop/issues/7506): Make `Style/IfUnlessModifier` respect all settings in `Metrics/LineLength`. ([@jonas054][])

### Changes

* [#7077](https://github.com/rubocop/rubocop/issues/7077): **(Breaking)** Further standardisation of cop names. ([@scottmatthewman][])
* [#7469](https://github.com/rubocop/rubocop/pull/7469): **(Breaking)** Replace usages of the terms `Whitelist` and `Blacklist` with better alternatives. ([@koic][])
* [#7502](https://github.com/rubocop/rubocop/pull/7502): Remove `SafeMode` module. ([@koic][])

## 0.76.0 (2019-10-28)

### Bug fixes

* [#7439](https://github.com/rubocop/rubocop/issues/7439): Make `Style/FormatStringToken` ignore percent escapes (`%%`). ([@buehmann][])
* [#7438](https://github.com/rubocop/rubocop/issues/7438): Fix assignment edge-cases in `Layout/MultilineAssignmentLayout`. ([@gsamokovarov][])
* [#7449](https://github.com/rubocop/rubocop/pull/7449): Make `Style/IfUnlessModifier` respect `rubocop:disable` comments for `Metrics/LineLength`. ([@jonas054][])
* [#7442](https://github.com/rubocop/rubocop/issues/7442): Fix an incorrect auto-correct for `Style/SafeNavigation` when an object check followed by a method call with a comment at EOL. ([@koic][])
* [#7434](https://github.com/rubocop/rubocop/issues/7434): Fix an incorrect auto-correct for `Style/MultilineWhenThen` when the body of `when` branch starts with `then`. ([@koic][])
* [#7464](https://github.com/rubocop/rubocop/pull/7464): Let `Performance/StartWith` and `Performance/EndWith` correct regexes that contain forward slashes. ([@eugeneius][])

### Changes

* [#7465](https://github.com/rubocop/rubocop/pull/7465): Add `os` to allowed names of `Naming/UncommunicativeMethodParamName` cop in default config. ([@nijikon][])
* [#7446](https://github.com/rubocop/rubocop/issues/7446): Add `merge` to list of non-mutating methods. ([@cstyles][])
* [#7077](https://github.com/rubocop/rubocop/issues/7077): **(Breaking)** Rename `Unneeded*` cops to `Redundant*` (e.g., `Style/UnneededPercentQ` becomes `Style/RedundantPercentQ`). ([@scottmatthewman][])
* [#7396](https://github.com/rubocop/rubocop/issues/7396): Display assignments, branches, and conditions values with the offense. ([@avmnu-sng][])

## 0.75.1 (2019-10-14)

### Bug fixes

* [#7391](https://github.com/rubocop/rubocop/issues/7391): Support pacman formatter on Windows. ([@laurenball][])
* [#7407](https://github.com/rubocop/rubocop/issues/7407): Make `Style/FormatStringToken` work inside hashes. ([@buehmann][])
* [#7389](https://github.com/rubocop/rubocop/issues/7389): Fix an issue where passing a formatter might result in an error depending on what character it started with. ([@jfhinchcliffe][])
* [#7397](https://github.com/rubocop/rubocop/issues/7397): Fix extra comments being added to the correction of `Style/SafeNavigation`. ([@rrosenblum][])
* [#7378](https://github.com/rubocop/rubocop/pull/7378): Fix heredoc edge cases in `Layout/EmptyLineAfterGuardClause`. ([@gsamokovarov][])
* [#7404](https://github.com/rubocop/rubocop/issues/7404): Fix a false negative for `Layout/IndentAssignment` when multiple assignment with line breaks on each line. ([@koic][])

### Changes

* [#7410](https://github.com/rubocop/rubocop/issues/7410): `Style/FormatStringToken` now finds unannotated format sequences in `printf` arguments. ([@buehmann][])
* [#6964](https://github.com/rubocop/rubocop/issues/6964): Set default `IgnoreCopDirectives` to `true` for `Metrics/LineLength`. ([@jdkaplan][])

## 0.75.0 (2019-09-30)

### New features

* [#7274](https://github.com/rubocop/rubocop/issues/7274): Add new `Lint/SendWithMixinArgument` cop. ([@koic][])
* [#7272](https://github.com/rubocop/rubocop/pull/7272): Show warning message if passed string to `Enabled`, `Safe`, `SafeAuto-Correct`, and `Auto-Correct` keys in .rubocop.yml. ([@unasuke][])
* [#7295](https://github.com/rubocop/rubocop/pull/7295): Make it possible to set `StyleGuideBaseURL` per department. ([@koic][])
* [#7301](https://github.com/rubocop/rubocop/pull/7301): Add check for calls to `remote_byebug` to `Lint/Debugger` cop. ([@riley-klingler][])
* [#7321](https://github.com/rubocop/rubocop/issues/7321): Allow YAML aliases in `.rubocop.yml`. ([@raymondfallon][])
* [#7317](https://github.com/rubocop/rubocop/pull/7317): Add new formatter `pacman`. ([@crojasaragonez][])
* [#6075](https://github.com/rubocop/rubocop/issues/6075): Support `IgnoredPatterns` option for `Naming/MethodName` cop. ([@koic][])
* [#7335](https://github.com/rubocop/rubocop/pull/7335): Add todo as an alias to disable. `--disable-uncorrectable` will now disable cops using `rubocop:todo` instead of `rubocop:disable`. ([@desheikh][])

### Bug fixes

* [#7391](https://github.com/rubocop/rubocop/issues/7391): Support pacman formatter on Windows. ([@laurenball][])
* [#7256](https://github.com/rubocop/rubocop/issues/7256): Fix an error of `Style/RedundantParentheses` on method calls where the first argument begins with a hash literal. ([@halfwhole][])
* [#7263](https://github.com/rubocop/rubocop/issues/7263): Make `Layout/SpaceInsideArrayLiteralBrackets` properly handle tab-indented arrays. ([@buehmann][])
* [#7252](https://github.com/rubocop/rubocop/issues/7252): Prevent infinite loops by making `Layout/SpaceInsideStringInterpolation` skip over interpolations that start or end with a line break. ([@buehmann][])
* [#7262](https://github.com/rubocop/rubocop/issues/7262): `Lint/FormatParameterMismatch` did not recognize named format sequences like `%.2<name>f` where the name appears after some modifiers. ([@buehmann][])
* [#7253](https://github.com/rubocop/rubocop/issues/7253): Fix an error for `Lint/NumberConversion` when `#to_i` called without a receiver. ([@koic][])
* [#7271](https://github.com/rubocop/rubocop/issues/7271), [#6498](https://github.com/rubocop/rubocop/issues/6498): Fix an interference between `Style/TrailingCommaIn*Literal` and `Layout/Multiline*BraceLayout` for arrays and hashes. ([@buehmann][])
* [#7241](https://github.com/rubocop/rubocop/issues/7241): Make `Style/FrozenStringLiteralComment` match only true & false. ([@tejasbubane][])
* [#7290](https://github.com/rubocop/rubocop/issues/7290): Handle inner conditional inside `else` in `Style/ConditionalAssignment`. ([@jonas054][])
* [#5788](https://github.com/rubocop/rubocop/issues/5788): Allow block arguments on separate lines if line would be too long in `Layout/MultilineBlockLayout`. ([@jonas054][])
* [#7305](https://github.com/rubocop/rubocop/issues/7305): Register `Style/BlockDelimiters` offense when block result is assigned to an attribute. ([@mvz][])
* [#4802](https://github.com/rubocop/rubocop/issues/4802): Don't leave any `Lint/UnneededCopEnableDirective` offenses undetected/uncorrected. ([@jonas054][])
* [#7326](https://github.com/rubocop/rubocop/issues/7326): Fix a false positive for `Style/AccessModifierDeclarations` when access modifier name is used for hash literal value. ([@koic][])
* [#3591](https://github.com/rubocop/rubocop/issues/3591): Handle modifier `if`/`unless` correctly in `Lint/UselessAssignment`. ([@jonas054][])
* [#7161](https://github.com/rubocop/rubocop/issues/7161): Fix `Style/SafeNavigation` cop for preserve comments inside if expression. ([@tejasbubane][])
* [#5212](https://github.com/rubocop/rubocop/issues/5212): Avoid false positive for braces that are needed to preserve semantics in `Style/BracesAroundHashParameters`. ([@jonas054][])
* [#7353](https://github.com/rubocop/rubocop/issues/7353): Fix a false positive for `Style/RedundantSelf` when receiver and multiple assigned lvalue have the same name. ([@koic][])
* [#7353](https://github.com/rubocop/rubocop/issues/7353): Fix a false positive for `Style/RedundantSelf` when a self receiver is used as a method argument. ([@koic][])
* [#7358](https://github.com/rubocop/rubocop/issues/7358): Fix an incorrect auto-correct for `Style/NestedModifier` when parentheses are required in method arguments. ([@koic][])
* [#7361](https://github.com/rubocop/rubocop/issues/7361): Fix a false positive for `Style/TernaryParentheses` when only the closing parenthesis is used in the last line of condition. ([@koic][])
* [#7369](https://github.com/rubocop/rubocop/issues/7369): Fix an infinite loop error for `Layout/IndentAssignment` with `Layout/IndentFirstArgument` when using multiple assignment. ([@koic][])
* [#7177](https://github.com/rubocop/rubocop/issues/7177), [#7370](https://github.com/rubocop/rubocop/issues/7370): When correcting alignment, do not insert spaces into string literals. ([@buehmann][])
* [#7367](https://github.com/rubocop/rubocop/issues/7367): Fix an error for `Style/OrAssignment` cop when `then` branch body is empty. ([@koic][])
* [#7363](https://github.com/rubocop/rubocop/issues/7363): Fix an incorrect auto-correct for `Layout/SpaceInsideBlockBraces` and `Style/BlockDelimiters` when using multiline empty braces. ([@koic][])
* [#7212](https://github.com/rubocop/rubocop/issues/7212): Fix a false positive for `Layout/EmptyLinesAroundAccessModifier` and `UselessAccessModifier` when using method with the same name as access modifier around a method definition. ([@koic][])

### Changes

* [#7312](https://github.com/rubocop/rubocop/pull/7312): Mark `Style/StringHashKeys` as unsafe. ([@prathamesh-sonpatki][])
* [#7275](https://github.com/rubocop/rubocop/issues/7275): Make `Style/VariableName` aware argument names when invoking a method. ([@koic][])
* [#3534](https://github.com/rubocop/rubocop/issues/3534): Make `Style/IfUnlessModifier` report and auto-correct modifier lines that are too long. ([@jonas054][])
* [#7261](https://github.com/rubocop/rubocop/issues/7261): `Style/FrozenStringLiteralComment` no longer inserts an empty line after the comment. This is left to `Layout/EmptyLineAfterMagicComment`. ([@buehmann][])
* [#7091](https://github.com/rubocop/rubocop/issues/7091): `Style/FormatStringToken` now detects format sequences with flags and modifiers. ([@buehmann][])
* [#7319](https://github.com/rubocop/rubocop/pull/7319): Rename `IgnoredMethodPatterns` option to `IgnoredPatterns` option for `Style/MethodCallWithArgsParentheses`. ([@koic][])
* [#7345](https://github.com/rubocop/rubocop/issues/7345): Mark unsafe for `Style/YodaCondition`. ([@koic][])

## 0.74.0 (2019-07-31)

### New features

* [#7219](https://github.com/rubocop/rubocop/issues/7219): Support auto-correct for `Lint/ErbNewArguments`. ([@koic][])

### Bug fixes

* [#7217](https://github.com/rubocop/rubocop/pull/7217): Make `Style/TrailingMethodEndStatement` work on more than the first `def`. ([@buehmann][])
* [#7190](https://github.com/rubocop/rubocop/issues/7190): Support lower case drive letters on Windows. ([@jonas054][])
* Fix the auto-correction of `Lint/UnneededSplatExpansion` when the splat expansion of `Array.new` with a block is assigned to a variable. ([@rrosenblum][])
* [#5628](https://github.com/rubocop/rubocop/issues/5628): Fix an error of `Layout/SpaceInsideStringInterpolation` on interpolations with multiple statements. ([@buehmann][])
* [#7128](https://github.com/rubocop/rubocop/issues/7128): Make `Metrics/LineLength` aware of shebang. ([@koic][])
* [#6861](https://github.com/rubocop/rubocop/issues/6861): Fix a false positive for `Layout/IndentationWidth` when using `EnforcedStyle: outdent` of `Layout/AccessModifierIndentation`. ([@koic][])
* [#7235](https://github.com/rubocop/rubocop/issues/7235): Fix an error where `Style/ConditionalAssignment` would swallow a nested `if` condition. ([@buehmann][])
* [#7242](https://github.com/rubocop/rubocop/issues/7242): Make `Style/ConstantVisibility` work on non-trivial class and module bodies. ([@buehmann][])

### Changes

* [#5265](https://github.com/rubocop/rubocop/issues/5265): Improved `Layout/ExtraSpacing` cop to handle nested consecutive assignments. ([@jfelchner][])
* [#7215](https://github.com/rubocop/rubocop/issues/7215): Make it clear what's wrong in the message from `Style/GuardClause`. ([@jonas054][])
* [#7245](https://github.com/rubocop/rubocop/pull/7245): Make cops detect string interpolations in more contexts: inside of backticks, regular expressions, and symbols. ([@buehmann][])
* Deprecate the `SafeMode` option. Users will need to upgrade `rubocop-performance` to 1.5.0+ before the `SafeMode` module is removed. ([@rrosenblum][])

## 0.73.0 (2019-07-16)

### New features

* Add `AllowDoxygenCommentStyle` configuration on `Layout/LeadingCommentSpace`. ([@anthony-robin][])
* [#7114](https://github.com/rubocop/rubocop/pull/7114): Add `MultilineWhenThen` cop. ([@okuramasafumi][])
* [#4127](https://github.com/rubocop/rubocop/pull/4127): Add `--disable-uncorrectable` flag to generate `rubocop:disable` comments. ([@vergenzt][], [@jonas054][])

### Bug fixes

* [#7170](https://github.com/rubocop/rubocop/issues/7170): Fix a false positive for `Layout/RescueEnsureAlignment` when def line is preceded with `private_class_method`. ([@tatsuyafw][])
* [#7186](https://github.com/rubocop/rubocop/issues/7186): Fix a false positive for `Style/MixinUsage` when using inside multiline block and `if` condition is after `include`. ([@koic][])
* [#7099](https://github.com/rubocop/rubocop/issues/7099): Fix an error of `Layout/RescueEnsureAlignment` on assigned blocks. ([@tatsuyafw][])
* [#5088](https://github.com/rubocop/rubocop/issues/5088): Fix an error of `Layout/MultilineMethodCallIndentation` on method chains inside an argument. ([@buehmann][])
* [#4719](https://github.com/rubocop/rubocop/issues/4719): Make `Layout/Tab` detect tabs between string literals. ([@buehmann][])
* [#7203](https://github.com/rubocop/rubocop/pull/7203): Fix an infinite loop error for `Layout/SpaceInsideBlockBraces` when `EnforcedStyle: no_space` with `SpaceBeforeBlockParameters: false` are set in multiline block. ([@koic][])
* [#6653](https://github.com/rubocop/rubocop/issues/6653): Fix a bug where `Layout/IndentHeredoc` would remove empty lines when auto-correcting heredocs. ([@buehmann][])

### Changes

* [#7181](https://github.com/rubocop/rubocop/pull/7181): Sort analyzed file alphabetically. ([@pocke][])
* [#7188](https://github.com/rubocop/rubocop/pull/7188): Include inspected file location in auto-correction error. ([@pocke][])

## 0.72.0 (2019-06-25)

### New features

* [#7137](https://github.com/rubocop/rubocop/issues/7137): Add new `Gemspec/RubyVersionGlobalsUsage` cop. ([@malyshkosergey][])
* [#7150](https://github.com/rubocop/rubocop/pull/7150): Add `AllowIfModifier` option to `Style/IfInsideElse` cop. ([@koic][])
* [#7153](https://github.com/rubocop/rubocop/pull/7153): Add new cop `Style/FloatDivision` that checks coercion. ([@tejasbubane][])

### Bug fixes

* [#7121](https://github.com/rubocop/rubocop/pull/7121): Fix `Style/TernaryParentheses` cop to allow safe navigation operator without parentheses. ([@timon][])
* [#7063](https://github.com/rubocop/rubocop/issues/7063): Fix auto-correct in `Style/TernaryParentheses` cop. ([@parkerfinch][])
* [#7106](https://github.com/rubocop/rubocop/issues/7106): Fix an error for `Lint/NumberConversion` when `#to_i` called on a variable on a hash. ([@koic][])
* [#7107](https://github.com/rubocop/rubocop/issues/7107): Fix parentheses offence for numeric arguments with an operator in `Style/MethodCallWithArgsParentheses`. ([@gsamokovarov][])
* [#7119](https://github.com/rubocop/rubocop/pull/7119): Fix cache with non UTF-8 offense message. ([@pocke][])
* [#7118](https://github.com/rubocop/rubocop/pull/7118): Fix `Style/WordArray` with `encoding: binary` magic comment and non-ASCII string. ([@pocke][])
* [#7159](https://github.com/rubocop/rubocop/issues/7159): Fix an error for `Lint/DuplicatedKey` when using endless range. ([@koic][])
* [#7151](https://github.com/rubocop/rubocop/issues/7151): Fix `Style/WordArray` to also consider words containing hyphens. ([@fwitzke][])
* [#6893](https://github.com/rubocop/rubocop/issues/6893): Handle implicit rescue correctly in `Naming/RescuedExceptionsVariableName`. ([@pocke][], [@anthony-robin][])
* [#7165](https://github.com/rubocop/rubocop/issues/7165): Fix an auto-correct error for `Style/ConditionalAssignment` when without `else` branch'. ([@koic][])
* [#7171](https://github.com/rubocop/rubocop/issues/7171): Fix an error for `Style/SafeNavigation` when using `unless nil?` as a safeguarded'. ([@koic][])
* [#7130](https://github.com/rubocop/rubocop/pull/7130): Skip auto-correct in `Style/FormatString` if second argument to `String#%` is a variable. ([@tejasbubane][])
* [#7171](https://github.com/rubocop/rubocop/issues/7171): Fix an error for `Style/SafeNavigation` when using `unless nil?` as a safeguarded'. ([@koic][])

### Changes

* [#5976](https://github.com/rubocop/rubocop/issues/5976): Remove Rails cops. ([@koic][])
* [#5976](https://github.com/rubocop/rubocop/issues/5976): Remove `rubocop -R/--rails` option. ([@koic][])
* [#7113](https://github.com/rubocop/rubocop/pull/7113): Rename `EnforcedStyle: rails` to `EnabledStyle: indented_internal_methods` for `Layout/IndentationConsistency`. ([@koic][])

## 0.71.0 (2019-05-30)

### New features

* [#7084](https://github.com/rubocop/rubocop/pull/7084): Permit to specify TargetRubyVersion 2.7. ([@koic][])
* [#7092](https://github.com/rubocop/rubocop/pull/7092): Node patterns can now use `*`, `+` and `?` for repetitions. ([@marcandre][])

### Bug fixes

* [#7066](https://github.com/rubocop/rubocop/issues/7066): Fix `Layout/AlignHash` when mixed Hash styles are used. ([@rmm5t][])
* [#7073](https://github.com/rubocop/rubocop/issues/7073): Fix false positive in `Naming/RescuedExceptionsVariableName` cop. ([@tejasbubane][])
* [#7090](https://github.com/rubocop/rubocop/pull/7090): Fix `Layout/EmptyLinesAroundBlockBody` for multi-line method calls. ([@eugeneius][])
* [#6936](https://github.com/rubocop/rubocop/issues/6936): Fix `Layout/MultilineMethodArgumentLineBreaks` when bracket hash assignment on multiple lines. ([@maxh][])
* Mark `Layout/HeredocArgumentClosingParenthesis` incompatible with `Style/TrailingCommaInArguments`. ([@maxh][])

### Changes

* [#5976](https://github.com/rubocop/rubocop/issues/5976): Warn for Rails Cops. ([@koic][])
* [#5976](https://github.com/rubocop/rubocop/issues/5976): Warn for `rubocop -R/--rails` option. ([@koic][])
* [#7078](https://github.com/rubocop/rubocop/issues/7078): Mark `Lint/PercentStringArray` as unsafe. ([@mikegee][])

## 0.70.0 (2019-05-21)

### New features

* [#6649](https://github.com/rubocop/rubocop/pull/6649): `Layout/AlignHash` supports list of options. ([@stoivo][])
* Add `IgnoreMethodPatterns` config option to `Style/MethodCallWithArgsParentheses`. ([@tejasbubane][])
* [#7059](https://github.com/rubocop/rubocop/pull/7059): Add `EnforcedStyle` to `Layout/EmptyLinesAroundAccessModifier`. ([@koic][])
* [#7052](https://github.com/rubocop/rubocop/issues/7052): Add `AllowComments` option to ` Lint/HandleExceptions`. ([@tejasbubane][])

### Bug fixes

* [#7013](https://github.com/rubocop/rubocop/pull/7013): Respect DisabledByDefault for custom cops. ([@XrXr][])
* [#7043](https://github.com/rubocop/rubocop/issues/7043): Prevent RDoc error when installing RuboCop 0.69.0 on Ubuntu. ([@koic][])
* [#7023](https://github.com/rubocop/rubocop/issues/7023): Auto-Correction for `Lint/NumberConversion`. ([@Bhacaz][])

### Changes

* [#6359](https://github.com/rubocop/rubocop/issues/6359): Mark `Style/PreferredHashMethods` as unsafe. ([@tejasbubane][])

## 0.69.0 (2019-05-13)

### New features

* Add support for subclassing using `Class.new` to `Lint/InheritException`. ([@houli][])
* [#6779](https://github.com/rubocop/rubocop/issues/6779): Add new cop `Style/NegatedUnless` that checks for unless with negative condition. ([@tejasbubane][])

### Bug fixes

* [#6900](https://github.com/rubocop/rubocop/issues/6900): Fix `Rails/TimeZone` auto-correct `Time.current` to `Time.zone.now`. ([@vfonic][])
* [#6900](https://github.com/rubocop/rubocop/issues/6900): Fix `Rails/TimeZone` to prefer `Time.zone.#{method}` over other acceptable corrections. ([@vfonic][])
* [#7007](https://github.com/rubocop/rubocop/pull/7007): Fix `Style/BlockDelimiters` with `braces_for_chaining` style false positive, when chaining using safe navigation. ([@Darhazer][])
* [#6880](https://github.com/rubocop/rubocop/issues/6880): Fix `.rubocop` file parsing. ([@hoshinotsuyoshi][])
* [#5782](https://github.com/rubocop/rubocop/issues/5782): Do not auto-correct `Lint/UnifiedInteger` if `TargetRubyVersion < 2.4`. ([@lavoiesl][])
* [#6387](https://github.com/rubocop/rubocop/issues/6387): Prevent `Lint/NumberConversion` from reporting error with `Time`/`DateTime`. ([@tejasbubane][])
* [#6980](https://github.com/rubocop/rubocop/issues/6980): Fix `Style/StringHashKeys` to allow string as keys for hash arguments to gsub methods. ([@tejasbubane][])
* [#6969](https://github.com/rubocop/rubocop/issues/6969): Fix a false positive with block methods in `Style/InverseMethods`. ([@dduugg][])
* [#6729](https://github.com/rubocop/rubocop/pull/6729): Handle array spread for `change_column_default` in `Rails/ReversibleMigration` cop. ([@tejasbubane][])
* [#7033](https://github.com/rubocop/rubocop/issues/7033): Fix an error for `Layout/EmptyLineAfterGuardClause` when guard clause is a ternary operator. ([@koic][])
* Replace `Time.zone.current` with `Time.zone.today` on `Rails::Date` cop message. ([@vfonic][])

### Changes

* [#6945](https://github.com/rubocop/rubocop/issues/6945): Drop support for Ruby 2.2. ([@koic][])
* [#6945](https://github.com/rubocop/rubocop/issues/6945): Set default `EnforcedStyle` to `squiggly` option for `Layout/IndentHeredoc` and `auto_detection` option is removed. ([@koic][])
* [#6945](https://github.com/rubocop/rubocop/issues/6945): Set default `EnforcedStyle` to `always` option for `Style/FrozenStringLiteralComment` and `when_needed` option is removed. ([@koic][])
* [#7027](https://github.com/rubocop/rubocop/pull/7027): Allow `unicode/display_width` dependency version 1.6.0. ([@tagliala][])

## 0.68.1 (2019-04-30)

### Bug fixes

* [#6993](https://github.com/rubocop/rubocop/pull/6993): Allowing for empty if blocks, preventing `Style/SafeNavigation` from crashing. ([@RicardoTrindade][])
* [#6995](https://github.com/rubocop/rubocop/pull/6995): Fix an incorrect auto-correct for `Style/RedundantParentheses` when enclosed in parentheses at `while-post` or `until-post`. ([@koic][])
* [#6996](https://github.com/rubocop/rubocop/pull/6996): Fix a false positive for `Style/RedundantFreeze` when freezing the result of `String#*`. ([@bquorning][])
* [#6998](https://github.com/rubocop/rubocop/pull/6998): Fix auto-correct of `Naming/RescuedExceptionsVariableName` to also rename all references to the variable. ([@Darhazer][])
* [#6992](https://github.com/rubocop/rubocop/pull/6992): Fix unknown default configuration for `Layout/IndentFirstParameter` cop. ([@drenmi][])
* [#6972](https://github.com/rubocop/rubocop/issues/6972): Fix a false positive for `Style/MixinUsage` when using inside block and `if` condition is after `include`. ([@koic][])
* [#6738](https://github.com/rubocop/rubocop/issues/6738): Prevent auto-correct conflict of `Style/Next` and `Style/SafeNavigation`. ([@hoshinotsuyoshi][])
* [#6847](https://github.com/rubocop/rubocop/pull/6847): Fix `Style/BlockDelimiters` to properly check if the node is chained when `braces_for_chaining` is set. ([@att14][])


## 0.68.0 (2019-04-29)

### New features

* [#6973](https://github.com/rubocop/rubocop/pull/6973): Add `always_braces` to `Style/BlockDelimiter`. ([@iGEL][])
* [#6841](https://github.com/rubocop/rubocop/issues/6841): Node patterns can now match children in any order using `<>`. ([@marcandre][])
* [#6928](https://github.com/rubocop/rubocop/pull/6928): Add `--init` option for generate `.rubocop.yml` file in the current directory. ([@koic][])
* Add new `Layout/HeredocArgumentClosingParenthesis` cop. ([@maxh][])
* [#6895](https://github.com/rubocop/rubocop/pull/6895): Add support for XDG config home for user-config. ([@Mange][], [@tejasbubane][])
* Add initial auto-correction support to `Metrics/LineLength`. ([@maxh][])
* Add `Layout/IndentFirstParameter`. ([@maxh][])
* [#6974](https://github.com/rubocop/rubocop/issues/6974): Make `Layout/FirstMethodArgumentLineBreak` aware of calling using `super`. ([@koic][])
* Add new `Lint/HeredocMethodCallPosition` cop. ([@maxh][])


### Bug fixes

* Do not annotate message with cop name in JSON output. ([@elebow][])
* [#6914](https://github.com/rubocop/rubocop/issues/6914): Fix an error for `Rails/RedundantAllowNil` when with interpolations. ([@Blue-Pix][])
* [#6888](https://github.com/rubocop/rubocop/issues/6888): Fix an error for `Rails/ActiveRecordOverride ` when no `parent_class` present. ([@diachini][])
* [#6941](https://github.com/rubocop/rubocop/issues/6941): Add missing absence validations to `Rails/Validation`. ([@jmanian][])
* [#6926](https://github.com/rubocop/rubocop/issues/6926): Allow nil values to unset config defaults. ([@dduugg][])
* [#6946](https://github.com/rubocop/rubocop/pull/6946): Allow `Rails/ReflectionClassName` to use string interpolation for `class_name`. ([@r7kamura][])
* [#6778](https://github.com/rubocop/rubocop/issues/6778): Fix a false positive in `Style/HashSyntax` cop when a hash key is an interpolated string and EnforcedStyle is ruby19_no_mixed_keys. ([@tatsuyafw][])
* [#6902](https://github.com/rubocop/rubocop/issues/6902): Fix a bug where `Naming/RescuedExceptionsVariableName` would handle an only first rescue for multiple rescue groups. ([@tatsuyafw][])
* [#6860](https://github.com/rubocop/rubocop/issues/6860): Prevent auto-correct conflict of `Style/InverseMethods` and `Style/Not`. ([@hoshinotsuyoshi][])
* [#6935](https://github.com/rubocop/rubocop/issues/6935): `Layout/AccessModifierIndentation` should ignore access modifiers that apply to specific methods. ([@deivid-rodriguez][])
* [#6956](https://github.com/rubocop/rubocop/issues/6956): Prevent auto-correct conflict of `Lint/Lambda` and `Lint/UnusedBlockArgument`. ([@koic][])
* [#6915](https://github.com/rubocop/rubocop/issues/6915): Fix false positive in `Style/SafeNavigation` when a modifier if is safe guarding a method call being passed to `break`, `fail`, `next`, `raise`, `return`, `throw`, and `yield`. ([@rrosenblum][])
* [#6822](https://github.com/rubocop/rubocop/issues/6822): Fix Lint/LiteralInInterpolation auto-correction for single quotes. ([@hoshinotsuyoshi][])
* [#6985](https://github.com/rubocop/rubocop/issues/6985): Fix an incorrect auto-correct for `Lint/LiteralInInterpolation` if contains array percent literal. ([@yakout][])
* [#7003](https://github.com/rubocop/rubocop/pull/7003): Fix an incorrect auto-correct for `Style/InverseMethods` when using `BasicObject#!`. ([@koic][])

### Changes

* [#6966](https://github.com/rubocop/rubocop/pull/6966): Mark Rails/TimeZone as unsafe. ([@vfonic][])
* [#5977](https://github.com/rubocop/rubocop/issues/5977): Remove Performance cops. ([@koic][])
* Add auto-correction to `Naming/RescuedExceptionsVariableName`. ([@anthony-robin][])
* [#6903](https://github.com/rubocop/rubocop/issues/6903): Handle variables prefixed with `_` in `Naming/RescuedExceptionsVariableName` cop. ([@anthony-robin][])
* [#6917](https://github.com/rubocop/rubocop/issues/6917): Bump Bundler dependency to >= 1.15.0. ([@koic][])
* Add `--auto-gen-only-exclude` to the command outputted in `rubocop_todo.yml` if the option is specified. ([@dvandersluis][])
* [#6887](https://github.com/rubocop/rubocop/pull/6887): Allow `Lint/UnderscorePrefixedVariableName` cop to be configured to allow use of block keyword args. ([@dduugg][])
* [#6885](https://github.com/rubocop/rubocop/pull/6885): Revert adding psych >= 3.1 as runtime dependency. ([@andreaseger][])
* Rename `Layout/FirstParameterIndentation` to `Layout/IndentFirstArgument`. ([@maxh][])
* Extract method call argument alignment behavior from `Layout/AlignParameters` into `Layout/AlignArguments`. ([@maxh][])
* Rename `IndentArray` and `IndentHash` to `IndentFirstArrayElement` and `IndentFirstHashElement`. ([@maxh][])

## 0.67.2 (2019-04-05)

### Bug fixes

* [#6882](https://github.com/rubocop/rubocop/issues/6882): Fix an error for `Rails/RedundantAllowNil` when not using both `allow_nil` and `allow_blank`. ([@koic][])

## 0.67.1 (2019-04-04)

### Changes

* [#6881](https://github.com/rubocop/rubocop/pull/6881): Set default `PreferredName` to `e` for `Naming/RescuedExceptionsVariableName`. ([@koic][])

## 0.67.0 (2019-04-04)

### New features

* [#5184](https://github.com/rubocop/rubocop/issues/5184): Add new multiline element line break cops. ([@maxh][])
* Add new cop `Rails/ActiveRecordOverride` that checks for overriding Active Record methods instead of using callbacks. ([@elebow][])
* Add new cop `Rails/RedundantAllowNil` that checks for cases when `allow_blank` makes `allow_nil` unnecessary in model validations. ([@elebow][])
* Add new `Naming/RescuedExceptionsVariableName` cop. ([@AdrienSldy][])

### Bug fixes

* [#6761](https://github.com/rubocop/rubocop/issues/6761): Make `Naming/UncommunicativeMethodParamName` account for param names prefixed with underscores. ([@thomthom][])
* [#6855](https://github.com/rubocop/rubocop/pull/6855): Fix an exception in `Rails/RedundantReceiverInWithOptions` when the body is empty. ([@ericsullivan][])
* [#6856](https://github.com/rubocop/rubocop/pull/6856): Fix auto-correction for `Style/BlockComments` when the file is missing a trailing blank line. ([@ericsullivan][])
* [#6858](https://github.com/rubocop/rubocop/issues/6858): Fix an incorrect auto-correct for `Lint/ToJSON` when there are no `to_json` arguments. ([@koic][])
* [#6865](https://github.com/rubocop/rubocop/pull/6865): Fix deactivated `StyleGuideBaseURL` for `Layout/ClassStructure`. ([@aeroastro][])
* [#6868](https://github.com/rubocop/rubocop/pull/6868): Fix `Rails/LinkToBlank` auto-correct bug when using symbol for target. ([@r7kamura][])
* [#6869](https://github.com/rubocop/rubocop/pull/6869): Fix false positive for `Rails/LinkToBlank` when rel is a symbol value. ([@r7kamura][])
* Add `IncludedMacros` param to default rubocop config for `Style/MethodCallWithArgsParentheses`. ([@maxh][])
* [#6785](https://github.com/rubocop/rubocop/issues/6785): Do not register an offense for `Rails/Present` or `Rails/Blank` in an `unless else` context when `Style/UnlessElse` is enabled. ([@rrosenblum][])

### Changes

* [#6854](https://github.com/rubocop/rubocop/pull/6854): Mark Rails/LexicallyScopedActionFilter as unsafe and document risks. ([@urbanautomaton][])
* [#5977](https://github.com/rubocop/rubocop/issues/5977): Warn for Performance Cops. ([@koic][])
* [#6637](https://github.com/rubocop/rubocop/issues/6637): Move `LstripRstrip` from `Performance` to `Style` department and rename it to `Strip`. ([@anuja-joshi][])
* [#6875](https://github.com/rubocop/rubocop/pull/6875): Mention block form of `Struct.new` in ` Style/StructInheritance`. ([@XrXr][])
* [#6871](https://github.com/rubocop/rubocop/issues/6871): Move `Performance/RedundantSortBy`, `Performance/UnneededSort` and `Performance/Sample` to the Style department. ([@bbatsov][])

## 0.66.0 (2019-03-18)

### New features

* [#6393](https://github.com/rubocop/rubocop/issues/6393): Add `AllowBracesOnProceduralOneLiners` option to fine-tune `Style/BlockDelimiter`'s semantic mode. ([@davearonson][])
* [#6383](https://github.com/rubocop/rubocop/issues/6383): Add `AllowBeforeTrailingComments` option on `Layout/ExtraSpacing` cop. ([@davearonson][])
* New cop `Lint/SafeNavigationWithEmpty` checks for `foo&.empty?` in conditionals. ([@rspeicher][])
* Add new `Style/ConstantVisibility` cop for enforcing visibility declarations of class and module constants. ([@drenmi][])
* [#6378](https://github.com/rubocop/rubocop/issues/6378): Add `Lint/ToJSON` cop to enforce an argument when overriding `#to_json`. ([@allcentury][])
* [#6346](https://github.com/rubocop/rubocop/issues/6346): Add auto-correction to `Rails/TimeZone`. ([@dcluna][])
* [#6840](https://github.com/rubocop/rubocop/issues/6840): Node patterns now allow unlimited elements after `...`. ([@marcandre][])

### Bug fixes

* [#4321](https://github.com/rubocop/rubocop/pull/4321): Fix false offense for `Style/RedundantSelf` when the method is also defined on `Kernel`. ([@mikegee][])
* [#6821](https://github.com/rubocop/rubocop/pull/6821): Fix false negative for `Rails/LinkToBlank` when `_blank` is a symbol. ([@Intrepidd][])
* [#6699](https://github.com/rubocop/rubocop/issues/6699): Fix infinite loop for `Layout/IndentationWidth` and `Layout/IndentationConsistency` when bad modifier indentation before good method definition. ([@koic][])
* [#6777](https://github.com/rubocop/rubocop/issues/6777): Fix a false positive for `Style/TrivialAccessors` when using trivial reader/writer methods at the top level. ([@koic][])
* [#6799](https://github.com/rubocop/rubocop/pull/6799): Fix errors for `Style/ConditionalAssignment`, `Style/IdenticalConditionalBranches`, `Lint/ElseLayout`, and `Layout/IndentationWidth` with empty braces. ([@pocke][])
* [#6802](https://github.com/rubocop/rubocop/pull/6802): Fix auto-correction for `Style/SymbolArray` with array contains interpolation when `EnforcedStyle` is `brackets`. ([@pocke][])
* [#6797](https://github.com/rubocop/rubocop/pull/6797): Fix false negative for Layout/SpaceAroundBlockParameters on block parameter with parens. ([@pocke][])
* [#6798](https://github.com/rubocop/rubocop/pull/6798): Fix infinite loop for `Layout/SpaceAroundBlockParameters` with `EnforcedStyleInsidePipes: :space`. ([@pocke][])
* [#6803](https://github.com/rubocop/rubocop/pull/6803): Fix error for `Style/NumericLiterals` on a literal that contains spaces. ([@pocke][])
* [#6801](https://github.com/rubocop/rubocop/pull/6801): Fix auto-correction for `Style/Lambda` with no-space argument. ([@pocke][])
* [#6804](https://github.com/rubocop/rubocop/pull/6804): Fix auto-correction of `Style/NumericLiterals` on numeric literal with exponent. ([@pocke][])
* [#6800](https://github.com/rubocop/rubocop/issues/6800): Fix an incorrect auto-correct for `Rails/Validation` when method arguments are enclosed in parentheses. ([@koic][])
* [#6808](https://github.com/rubocop/rubocop/issues/6808): Prevent false positive in `Naming/ConstantName` when assigning a frozen range. ([@drenmi][])
* Fix the calculation of `Metrics/AbcSize`. Comparison methods and `else` branches add to the comparison count. ([@rrosenblum][])
* [#6791](https://github.com/rubocop/rubocop/pull/6791): Allow `Rails/ReflectionClassName` to use symbol argument for `class_name`. ([@unasuke][])
* [#5465](https://github.com/rubocop/rubocop/issues/5465): Fix `Layout/ClassStructure` to allow grouping macros by their visibility. ([@gprado][])
* [#6461](https://github.com/rubocop/rubocop/pull/6461): Restrict `Ctrl-C` handling to RuboCop's loop and simplify it to a single phase. ([@deivid-rodriguez][])

### Changes

* Add `$stdout`/`$stderr` and `STDOUT`/`STDERR` method calls to `Rails/Output`. ([@elebow][])
* [#6688](https://github.com/rubocop/rubocop/pull/6688): Add `iterator?` to deprecated methods and prefer `block_given?` instead. ([@tejasbubane][])
* [#6806](https://github.com/rubocop/rubocop/pull/6806): Remove `powerpack` dependency. ([@dduugg][])
* [#6810](https://github.com/rubocop/rubocop/pull/6810): Exclude gemspec file by default for `Metrics/BlockLength` cop. ([@koic][])
* [#6813](https://github.com/rubocop/rubocop/pull/6813): Allow unicode/display_width dependency version 1.5.0. ([@tagliala][])
* Make `Style/RedundantFreeze` aware of methods that will produce frozen objects. ([@rrosenblum][])
* [#6675](https://github.com/rubocop/rubocop/issues/6675): Avoid printing deprecation warnings about constants. ([@elmasantos][])
* [#6746](https://github.com/rubocop/rubocop/issues/6746): Avoid offense on `$stderr.puts` with no arguments. ([@luciamo][])
* Replace md5 with sha1 for FIPS compliance. ([@dirtyharrycallahan][])

## 0.65.0 (2019-02-19)

### New features

* [#6126](https://github.com/rubocop/rubocop/pull/6126): Add an experimental strict mode to `Style/MutableConstant` that will freeze all constants, rather than just literals. ([@rrosenblum][])
* Add `IncludedMacros` to `Style/MethodCallWithArgsParentheses` to allow including specific macros when `IgnoreMacros` is true. ([@maxh][])

### Bug fixes

* [#6765](https://github.com/rubocop/rubocop/pull/6765): Fix false positives in keyword arguments for `Style/MethodCallWithArgsParentheses` `omit_parentheses`. ([@gsamokovarov][])
* [#6763](https://github.com/rubocop/rubocop/pull/6763): Fix false positives in range literals for `Style/MethodCallWithArgsParentheses` `omit_parentheses`. ([@gsamokovarov][])
* [#6748](https://github.com/rubocop/rubocop/issues/6748): Fix `Style/RaiseArgs` auto-correction breaking in contexts that require parentheses. ([@drenmi][])
* [#6751](https://github.com/rubocop/rubocop/issues/6751): Prevent `Style/OneLineConditional` from breaking on `retry` and `break` keywords. ([@drenmi][])
* [#6755](https://github.com/rubocop/rubocop/issues/6755): Prevent `Style/TrailingCommaInArgument` from breaking when a safe method call is chained on the offending method. ([@drenmi][], [@hoshinotsuyoshi][])

### Changes

* [#6766](https://github.com/rubocop/rubocop/pull/6766): Drop support for Ruby 2.2.0 and 2.2.1. ([@pocke][])
* [#6733](https://github.com/rubocop/rubocop/pull/6733): Warn duplicated keys in `.rubocop.yml`. ([@pocke][])
* [#6613](https://github.com/rubocop/rubocop/pull/6613): Mark `Style/ModuleFunction` as `SafeAuto-Correct: false` and disable auto-correct by default. ([@dduugg][])

## 0.64.0 (2019-02-10)

### New features

* [#6704](https://github.com/rubocop/rubocop/pull/6704): Add new `Rails/ReflectionClassName` cop. ([@Bhacaz][])
* [#6643](https://github.com/rubocop/rubocop/pull/6643): Support `AllowParenthesesInCamelCaseMethod` option on `Style/MethodCallWithArgsParentheses` `omit_parentheses`. ([@dazuma][])

### Bug fixes

* [#6254](https://github.com/rubocop/rubocop/issues/6254): Fix `Layout/RescueEnsureAlignment` for non-local assignments. ([@marcotc][])
* [#6648](https://github.com/rubocop/rubocop/issues/6648): Fix auto-correction of `Style/EmptyLiteral` when `Hash.new` is passed as the first argument to `super`. ([@rrosenblum][])
* [#6351](https://github.com/rubocop/rubocop/pull/6351): Fix a false positive for `Layout/ClosingParenthesisIndentation` when first argument is multiline. ([@antonzaytsev][])
* [#6689](https://github.com/rubocop/rubocop/pull/6689): Support more complex argument patterns on `Rails/Validation` auto-correction. ([@r7kamura][])
* [#6668](https://github.com/rubocop/rubocop/issues/6668): Fix auto-correction for `Style/UnneededCondition` when conditional has the `unless` form. ([@mvz][])
* [#6382](https://github.com/rubocop/rubocop/issues/6382): Fix `Layout/IndentationWidth` with `Layout/EndAlignment` set to start_of_line. ([@dischorde][], [@siegfault][], [@mhelmetag][])
* [#6710](https://github.com/rubocop/rubocop/issues/6710): Fix `Naming/MemoizedInstanceVariableName` on method starts with underscore. ([@pocke][])
* [#6722](https://github.com/rubocop/rubocop/issues/6722): Fix an error for `Style/OneLineConditional` when `then` branch has no body. ([@koic][])
* [#6702](https://github.com/rubocop/rubocop/pull/6702): Fix `TrailingComma` regression where heredoc with commas caused false positives. ([@abrom][])
* [#6737](https://github.com/rubocop/rubocop/issues/6737): Fix an incorrect auto-correct for `Rails/LinkToBlank` when `link_to` method arguments are enclosed in parentheses. ([@koic][])
* [#6720](https://github.com/rubocop/rubocop/issues/6720): Fix detection of `:native` line ending for `Layout/EndOfLine` on JRuby. ([@enkessler][])

### Changes

* [#6597](https://github.com/rubocop/rubocop/issues/6597): `Style/LineEndConcatenation` is now known to be unsafe for auto-correct. ([@jaredbeck][])
* [#6725](https://github.com/rubocop/rubocop/issues/6725): Mark `Style/SymbolProc` as unsafe for auto-correct. ([@drenmi][])
* [#6708](https://github.com/rubocop/rubocop/issues/6708): Make `Style/CommentedKeyword` allow the `:yields:` RDoc comment. ([@bquorning][])
* [#6749](https://github.com/rubocop/rubocop/pull/6749): Make some cops aware of safe navigation operator. ([@hoshinotsuyoshi][])

## 0.63.1 (2019-01-22)

### Bug fixes

* [#6678](https://github.com/rubocop/rubocop/issues/6678): Fix `Lint/DisjunctiveAssignmentInConstructor` when it finds an empty constructor. ([@rmm5t][])
* Do not attempt to auto-correct mass assignment or optional assignment in `Rails/RelativeDateConstant`. ([@rrosenblum][])
* Fix auto-correction of `Style/WordArray` and `Style/SymbolArray` when all elements are on separate lines and there is a trailing comment after the closing bracket. ([@rrosenblum][])
* Fix an exception that occurs when auto-correcting `Layout/ClosingParenthesesIndentation` when there are no arguments. ([@rrosenblum][])

## 0.63.0 (2019-01-16)

### New features

* [#6604](https://github.com/rubocop/rubocop/pull/6604): Add auto-correct support to `Rails/LinkToBlank`. ([@Intrepidd][])
* [#6660](https://github.com/rubocop/rubocop/pull/6660): Add new `Rails/IgnoredSkipActionFilterOption` cop. ([@wata727][])
* [#6363](https://github.com/rubocop/rubocop/issues/6363): Allow `Style/YodaCondition` cop to be configured to enforce yoda conditions. ([@tejasbubane][])
* [#6150](https://github.com/rubocop/rubocop/issues/6150): Add support to enforce disabled cops to be executed. ([@roooodcastro][])
* [#6596](https://github.com/rubocop/rubocop/pull/6596): Add new `Rails/BelongsTo` cop with auto-correct for Rails >= 5. ([@petehamilton][])

### Bug fixes

* [#6627](https://github.com/rubocop/rubocop/pull/6627): Fix handling of hashes in trailing comma. ([@abrom][])
* [#6638](https://github.com/rubocop/rubocop/pull/6638): Fix `Rails/LinkToBlank` detection to allow `rel: 'noreferrer`. ([@fwininger][])
* [#6623](https://github.com/rubocop/rubocop/pull/6623): Fix heredoc detection in trailing comma. ([@palkan][])
* [#6100](https://github.com/rubocop/rubocop/issues/6100): Fix a false positive in `Naming/ConstantName` cop when rhs is a conditional expression. ([@tatsuyafw][])
* [#6526](https://github.com/rubocop/rubocop/issues/6526): Fix a wrong line highlight in `Lint/ShadowedException` cop. ([@tatsuyafw][])
* [#6617](https://github.com/rubocop/rubocop/issues/6617): Prevent traversal error on infinite ranges. ([@drenmi][])
* [#6625](https://github.com/rubocop/rubocop/issues/6625): Revert the "auto-exclusion of files ignored by git" feature. ([@bbatsov][])
* [#4460](https://github.com/rubocop/rubocop/issues/4460): Fix the determination of unsafe auto-correct in `Style/TernaryParentheses`. ([@jonas054][])
* [#6651](https://github.com/rubocop/rubocop/issues/6651): Fix auto-correct issue in `Style/RegexpLiteral` cop when there is string interpolation. ([@roooodcastro][])
* [#6670](https://github.com/rubocop/rubocop/issues/6670): Fix a false positive for `Style/SafeNavigation` when a method call safeguarded with a negative check for the object. ([@koic][])
* [#6633](https://github.com/rubocop/rubocop/issues/6633): Fix `Lint/SafeNavigation` complaining about use of `to_d`. ([@tejasbubane][])
* [#6575](https://github.com/rubocop/rubocop/issues/6575): Fix `Naming/PredicateName` suggesting invalid rename. ([@tejasbubane][])
* [#6673](https://github.com/rubocop/rubocop/issues/6673): Fix `Style/DocumentationMethod` cop to recognize documentation comments for `def` inline with `module_function`. ([@tejasbubane][])
* [#6648](https://github.com/rubocop/rubocop/issues/6648): Fix auto-correction of `Style/EmptyLiteral` when `Hash.new` is passed as the first argument to `super`. ([@rrosenblum][])

### Changes

* [#6607](https://github.com/rubocop/rubocop/pull/6607): Improve CLI usage message for --stdin option. ([@jaredbeck][])
* [#6641](https://github.com/rubocop/rubocop/issues/6641): Specify `Performance/RangeInclude` as unsafe because `Range#include?` and `Range#cover?` are not equivalent. ([@koic][])
* [#6636](https://github.com/rubocop/rubocop/pull/6636): Move `FlipFlop` cop from `Style` to `Lint` department because flip-flop is deprecated since Ruby 2.6.0. ([@koic][])
* [#6661](https://github.com/rubocop/rubocop/pull/6661): Abandon making frozen string literals default for Ruby 3.0. ([@koic][])

## 0.62.0 (2019-01-01)

### New features

* [#6580](https://github.com/rubocop/rubocop/pull/6580): New cop `Rails/LinkToBlank` checks for `link_to` calls with `target: '_blank'` and no `rel: 'noopener'`. ([@Intrepidd][])
* [#6586](https://github.com/rubocop/rubocop/issues/6586): New cop `Lint/DisjunctiveAssignmentInConstructor` checks constructors for disjunctive assignments that should be plain assignments. ([@jaredbeck][])

### Bug fixes

* [#6560](https://github.com/rubocop/rubocop/issues/6560): Consider file count, not offense count, for `--exclude-limit` in combination with `--auto-gen-only-exclude`. ([@jonas054][])
* [#4229](https://github.com/rubocop/rubocop/issues/4229): Fix unexpected Style/HashSyntax consistency offence. ([@timon][])
* [#6500](https://github.com/rubocop/rubocop/issues/6500): Add offense to use `in_time_zone` instead of deprecated `to_time_in_current_zone`. ([@nadiyaka][])
* [#6577](https://github.com/rubocop/rubocop/pull/6577): Prevent Rails/Blank cop from adding offense when define the blank method. ([@jonatas][])
* [#6554](https://github.com/rubocop/rubocop/issues/6554): Prevent Layout/RescueEnsureAlignment cop from breaking on block assignment when assignment is on a separate line. ([@timmcanty][])
* [#6343](https://github.com/rubocop/rubocop/pull/6343): Optimise `--auto-gen-config` when `Metrics/LineLength` cop is disabled. ([@tom-lord][])
* [#6389](https://github.com/rubocop/rubocop/pull/6389): Fix false negative for `Style/TrailingCommaInHashLiteral`/`Style/TrailingCommaInArrayLiteral` when there is a comment in the last line. ([@bayandin][])
* [#6566](https://github.com/rubocop/rubocop/issues/6566): Fix false positive for `Layout/EmptyLinesAroundAccessModifier` when at the end of specifying a superclass is missing blank line. ([@koic][])
* [#6571](https://github.com/rubocop/rubocop/issues/6571): Fix a false positive for `Layout/TrailingCommaInArguments` when a line break before a method call and `EnforcedStyleForMultiline` is set to `consistent_comma`. ([@koic][])
* [#6573](https://github.com/rubocop/rubocop/pull/6573): Make `Layout/AccessModifierIndentation` work for dynamic module or class definitions. ([@deivid-rodriguez][])
* [#6562](https://github.com/rubocop/rubocop/pull/6562): Fix a false positive for `Style/MethodCallWithArgsParentheses` `omit_parentheses` enforced style after safe navigation call. ([@gsamokovarov][])
* [#6570](https://github.com/rubocop/rubocop/pull/6570): Fix a false positive for `Style/MethodCallWithArgsParentheses` `omit_parentheses` enforced style while splatting the result of a method invocation. ([@gsamokovarov][])
* [#6598](https://github.com/rubocop/rubocop/pull/6598): Fix a false positive for `Style/MethodCallWithArgsParentheses` `omit_parentheses` enforced style for calls with regexp slash literals argument. ([@gsamokovarov][])
* [#6598](https://github.com/rubocop/rubocop/pull/6598): Fix a false positive for `Style/MethodCallWithArgsParentheses` `omit_parentheses` enforced style for default argument value calls. ([@gsamokovarov][])
* [#6598](https://github.com/rubocop/rubocop/pull/6598): Fix a false positive for `Style/MethodCallWithArgsParentheses` `omit_parentheses` enforced style for argument calls with braced blocks. ([@gsamokovarov][])
* [#6594](https://github.com/rubocop/rubocop/pull/6594): Fix a false positive for `Rails/OutputSafety` when the receiver is a non-interpolated string literal. ([@amatsuda][])
* [#6574](https://github.com/rubocop/rubocop/pull/6574): Fix `Style/AccessModifierIndentation` not handling arbitrary blocks. ([@deivid-rodriguez][])
* [#6370](https://github.com/rubocop/rubocop/issues/6370): Fix the enforcing style from `extend self` into `module_function` when there are private methods. ([@Ruffeng][])

### Changes

* [#595](https://github.com/rubocop/rubocop/issues/595): Exclude files ignored by `git`. ([@AlexWayfer][])
* [#6429](https://github.com/rubocop/rubocop/issues/6429): Fix auto-correct in Rails/Validation to not wrap hash options with braces in an extra set of braces. ([@bquorning][])
* [#6533](https://github.com/rubocop/rubocop/issues/6533): Improved warning message for unrecognized cop parameters to include Supported parameters. ([@MagedMilad][])

## 0.61.1 (2018-12-06)

### Bug fixes

* [#6550](https://github.com/rubocop/rubocop/issues/6550): Prevent Layout/RescueEnsureAlignment cop from breaking on assigned begin-end. ([@drenmi][])

## 0.61.0 (2018-12-05)

### New features

* [#6457](https://github.com/rubocop/rubocop/pull/6457): Support inner slash correction on `Style/RegexpLiteral`. ([@r7kamura][])
* [#6475](https://github.com/rubocop/rubocop/pull/6475): Support brace correction on `Style/Lambda`. ([@r7kamura][])
* [#6469](https://github.com/rubocop/rubocop/pull/6469): Enforce no parentheses style in the `Style/MethodCallWithArgsParentheses` cop. ([@gsamokovarov][])
* New cop `Performance/OpenStruct` checks for `OpenStruct.new` calls. ([@xlts][])

### Bug fixes

* [#6433](https://github.com/rubocop/rubocop/issues/6433): Fix Ruby 2.5 `Layout/RescueEnsureAlignment` error on assigned blocks. ([@gmcgibbon][])
* [#6405](https://github.com/rubocop/rubocop/issues/6405): Fix a false positive for `Lint/UselessAssignment` when using a variable in a module name. ([@itsWill][])
* [#5934](https://github.com/rubocop/rubocop/issues/5934): Handle the combination of `--auto-gen-config` and `--config FILE` correctly. ([@jonas054][])
* [#5970](https://github.com/rubocop/rubocop/issues/5970): Make running `--auto-gen-config` in a subdirectory work. ([@jonas054][])
* [#6412](https://github.com/rubocop/rubocop/issues/6412): Fix an `unknown keywords` error when using `Psych.safe_load` with Ruby 2.6.0-preview2. ([@koic][])
* [#6436](https://github.com/rubocop/rubocop/pull/6436): Fix exit status code to be 130 when rubocop is interrupted. ([@deivid-rodriguez][])
* [#6443](https://github.com/rubocop/rubocop/pull/6443): Fix an incorrect auto-correct for `Style/BracesAroundHashParameters` when the opening brace is before the first hash element at same line. ([@koic][])
* [#6445](https://github.com/rubocop/rubocop/pull/6445): Treat `yield` and `super` like regular method calls in `Style/AlignHash`. ([@mvz][])
* [#3301](https://github.com/rubocop/rubocop/issues/3301): Don't suggest or make semantic changes to the code in `Style/InfiniteLoop`. ([@jonas054][])
* [#3586](https://github.com/rubocop/rubocop/issues/3586): Handle single argument spanning multiple lines in `Style/TrailingCommaInArguments`. ([@jonas054][])
* [#6478](https://github.com/rubocop/rubocop/pull/6478): Fix EmacsComment#encoding to match the `coding` variable. ([@akihiro17][])
* Don't show "unrecognized parameter" warning for `inherit_mode` parameter to individual cop configurations. ([@maxh][])
* [#6449](https://github.com/rubocop/rubocop/pull/6449): Fix a false negative for `Layout/IndentationWidth` when setting `EnforcedStyle: rails` of `Layout/IndentationConsistency` and method definition indented to access modifier in a singleton class. ([@koic][])
* [#6482](https://github.com/rubocop/rubocop/issues/6482): Fix a false positive for `Lint/FormatParameterMismatch` when using (digit)$ flag. ([@koic][])
* [#6489](https://github.com/rubocop/rubocop/issues/6489): Fix an error for `Style/UnneededCondition` when `if` condition and `then` branch are the same and it has no `else` branch. ([@koic][])
* Fix NoMethodError for `Style/FrozenStringLiteral` when a file contains only a shebang. ([@takaram][])
* [#6511](https://github.com/rubocop/rubocop/issues/6511): Fix an incorrect auto-correct for `Style/EmptyCaseCondition` when used as an argument of a method. ([@koic][])
* [#6509](https://github.com/rubocop/rubocop/issues/6509): Fix an incorrect auto-correct for `Style/RaiseArgs` when an exception object is assigned to a local variable. ([@koic][])
* [#6534](https://github.com/rubocop/rubocop/issues/6534): Fix a false positive for `Lint/UselessAccessModifier` when using `private_class_method`. ([@dduugg][])
* [#6545](https://github.com/rubocop/rubocop/issues/6545): Fix a regression where `Performance/RedundantMerge` raises an error on a sole double splat argument passed to `merge!`. ([@mmedal][])
* [#6360](https://github.com/rubocop/rubocop/issues/6360): Detect bad indentation in `if` nodes even if the first branch is empty. ([@bquorning][])

### Changes

* [#6492](https://github.com/rubocop/rubocop/issues/6492): Auto-correct chunks of comment lines in `Layout/CommentIndentation` to avoid unnecessary iterations for `rubocop -a`. ([@jonas054][])
* Fix `--auto-gen-config` when individual cops have regexp literal exclude paths. ([@maxh][])

## 0.60.0 (2018-10-26)

### New features

* [#5980](https://github.com/rubocop/rubocop/issues/5980): Add `--safe` and `--safe-auto-correct` options. ([@Darhazer][])
* [#4156](https://github.com/rubocop/rubocop/issues/4156): Add command line option `--auto-gen-only-exclude`. ([@Ana06][], [@jonas054][])
* [#6386](https://github.com/rubocop/rubocop/pull/6386): Add `VersionAdded` meta data to config/default.yml when running `rake new_cop`. ([@koic][])
* [#6395](https://github.com/rubocop/rubocop/pull/6395): Permit to specify TargetRubyVersion 2.6. ([@koic][])
* [#6392](https://github.com/rubocop/rubocop/pull/6392): Add `Whitelist` config to `Rails/SkipsModelValidations` rule. ([@DiscoStarslayer][])

### Bug fixes

* [#6330](https://github.com/rubocop/rubocop/issues/6330): Fix an error for `Rails/ReversibleMigration` when using variable assignment. ([@koic][], [@scottmatthewman][])
* [#6331](https://github.com/rubocop/rubocop/issues/6331): Fix a false positive for `Style/RedundantFreeze` and a false negative for `Style/MutableConstant` when assigning a regexp object to a constant. ([@koic][])
* [#6334](https://github.com/rubocop/rubocop/pull/6334): Fix a false negative for `Style/RedundantFreeze` when assigning a range object to a constant. ([@koic][])
* [#5538](https://github.com/rubocop/rubocop/issues/5538): Fix false negatives in modifier cops when line length cop is disabled. ([@drenmi][])
* [#6340](https://github.com/rubocop/rubocop/pull/6340): Fix an error for `Rails/ReversibleMigration` when block argument is empty. ([@koic][])
* [#6274](https://github.com/rubocop/rubocop/issues/6274): Fix "[Corrected]" message being displayed even when nothing has been corrected. ([@jekuta][])
* [#6380](https://github.com/rubocop/rubocop/pull/6380): Allow use of a hyphen-separated frozen string literal in Emacs style magic comment. ([@y-yagi][])
* Fix and improve `LineLength` cop for tab-indented code. ([@AlexWayfer][])

### Changes

* [#3727](https://github.com/rubocop/rubocop/issues/3727): Enforce single spaces for `key` option in `Layout/AlignHash` cop. ([@albaer][])
* [#6321](https://github.com/rubocop/rubocop/pull/6321): Fix run of RuboCop when cache directory is not writable. ([@Kevinrob][])

## 0.59.2 (2018-09-24)

### New features

* Update `Style/MethodCallWithoutArgsParentheses` to highlight the closing parentheses in addition to the opening parentheses. ([@rrosenblum][])

### Bug fixes

* [#6266](https://github.com/rubocop/rubocop/issues/6266): Fix a false positive for `Rails/HasManyOrHasOneDependent` when using associations of Active Resource. ([@tejasbubane][], [@koic][])
* [#6296](https://github.com/rubocop/rubocop/issues/6296): Fix an auto-correct error for `Style/For` when setting `EnforcedStyle: each` and `for` dose not have `do` or semicolon. ([@autopp][])
* [#6300](https://github.com/rubocop/rubocop/pull/6300): Fix a false positive for `Layout/EmptyLineAfterGuardClause` when guard clause including heredoc. ([@koic][])
* [#6287](https://github.com/rubocop/rubocop/pull/6287): Fix `AllowURI` option for `Metrics/LineLength` cop with disabled `Layout/Tab` cop. ([@AlexWayfer][])
* [#5338](https://github.com/rubocop/rubocop/pull/5338): Move checking of class- and module defining blocks from `Metrics/BlockLength` into the respective length cops. ([@drenmi][])
* [#2841](https://github.com/rubocop/rubocop/pull/2841): Fix `Style/ZeroLengthPredicate` false positives when inspecting `Tempfile`, `StringIO`, and `File::Stat` objects. ([@drenmi][])
* [#6305](https://github.com/rubocop/rubocop/pull/6305): Fix infinite loop for `Layout/EmptyLinesAroundAccessModifier` and `Layout/EmptyLinesAroundAccessModifier` when specifying a superclass that breaks the line. ([@koic][])
* [#6007](https://github.com/rubocop/rubocop/pull/6007): Fix false positive in `Style/IfUnlessModifier` when using named capture. ([@drenmi][])
* [#6311](https://github.com/rubocop/rubocop/pull/6311): Prevent `Style/Semicolon` from breaking on single line if-then-else in assignment. ([@drenmi][])
* [#6315](https://github.com/rubocop/rubocop/pull/6315): Fix an error for `Rails/HasManyOrHasOneDependent` when an Active Record model does not have any relations. ([@koic][])
* [#6316](https://github.com/rubocop/rubocop/issues/6316): Fix an auto-correct error for `Style/For` when setting `EnforcedStyle: each` with range provided to the `for` loop without a `do` keyword or semicolon and without enclosing parenthesis. ([@lukasz-wojcik][])
* [#6326](https://github.com/rubocop/rubocop/issues/6326): Fix an alignment source for `Layout/RescueEnsureAlignment` when using inline access modifier. ([@andrew-aladev][])

### Changes

* [#6286](https://github.com/rubocop/rubocop/pull/6286): Allow exclusion of certain methods for `Metrics/MethodLength`. ([@akanoi][])

## 0.59.1 (2018-09-15)

### Bug fixes

* [#6267](https://github.com/rubocop/rubocop/pull/6267): Fix undefined method 'method_name' for `Rails/FindEach`. ([@Knack][])
* [#6278](https://github.com/rubocop/rubocop/pull/6278): Fix false positive for `Naming/FileName` when investigating gemspecs. ([@kddeisz][])
* [#6256](https://github.com/rubocop/rubocop/pull/6256): Fix false positive for `Naming/FileName` when investigating dotfiles. ([@sinsoku][])
* [#6242](https://github.com/rubocop/rubocop/pull/6242): Fix `Style/EmptyCaseCondition` auto-correction removes comment between `case` and first `when`. ([@koic][])
* [#6261](https://github.com/rubocop/rubocop/pull/6261): Fix undefined method error for `Style/RedundantBegin` when calling `super` with a block. ([@eitoball][])
* [#6263](https://github.com/rubocop/rubocop/issues/6263): Fix an error `Layout/EmptyLineAfterGuardClause` when guard clause is after heredoc including string interpolation. ([@koic][])
* [#6281](https://github.com/rubocop/rubocop/pull/6281): Fix false negative in `Style/MultilineMethodSignature`. ([@drenmi][])
* [#6264](https://github.com/rubocop/rubocop/issues/6264): Fix an incorrect auto-correct for `Layout/EmptyLineAfterGuardClause` cop when `if` condition is after heredoc. ([@koic][])

### Changes

* [#6272](https://github.com/rubocop/rubocop/pull/6272): Make `Lint/UnreachableCode` detect `exit`, `exit!` and `abort`. ([@hoshinotsuyoshi][])
* [#6295](https://github.com/rubocop/rubocop/pull/6295): Exclude `#===` from `Naming/BinaryOperatorParameterName`. ([@zverok][])
* Add `+` to allowed file names of `Naming/FileName`. ([@yensaki][])
* [#5303](https://github.com/rubocop/rubocop/issues/5303): Extract `PercentLiteralCorrector` class from `PercentLiteral` mixin. ([@ryanhageman][])

## 0.59.0 (2018-09-09)

### New features

* [#6109](https://github.com/rubocop/rubocop/pull/6109): Add new `Bundler/GemComment` cop. ([@sunny][])
* [#6148](https://github.com/rubocop/rubocop/pull/6148): Add `IgnoredMethods` option to `Style/NumericPredicate` cop. ([@AlexWayfer][])
* [#6174](https://github.com/rubocop/rubocop/pull/6174): Add `--display-only-fail-level-offenses` to only output offenses at or above the fail level. ([@robotdana][])
* Add auto-correct to `Style/For`. ([@rrosenblum][])
* [#6173](https://github.com/rubocop/rubocop/pull/6173): Add `AllowImplicitReturn` option to `Rails/SaveBang` cop. ([@robotdana][])
* [#6218](https://github.com/rubocop/rubocop/pull/6218): Add `comparison` style to `Style/NilComparison`. ([@khiav223577][])
* Add new `Style/MultilineMethodSignature` cop. ([@drenmi][])
* [#6234](https://github.com/rubocop/rubocop/pull/6234): Add `Performance/ChainArrayAllocation` cop. ([@schneems][])
* [#6136](https://github.com/rubocop/rubocop/pull/6136): Add remote url in remote url download error message. ([@ShockwaveNN][])
* [#5659](https://github.com/rubocop/rubocop/issues/5659): Make `Layout/EmptyLinesAroundClassBody` aware of specifying a superclass that breaks the line. ([@koic][])

### Bug fixes

* [#6107](https://github.com/rubocop/rubocop/pull/6107): Fix indentation of multiline postfix conditionals. ([@jaredbeck][])
* [#6140](https://github.com/rubocop/rubocop/pull/6140): Fix `Style/DateTime` not detecting `#to_datetime`. It can be configured to allow this. ([@bdewater][])
* [#6132](https://github.com/rubocop/rubocop/issues/6132): Fix a false negative for `Naming/FileName` when `Include` of `AllCops` is the default setting. ([@koic][])
* [#4115](https://github.com/rubocop/rubocop/issues/4115): Fix false positive for unary operations in `Layout/MultilineOperationIndentation`. ([@jonas054][])
* [#6127](https://github.com/rubocop/rubocop/issues/6127): Fix an error for `Layout/ClosingParenthesisIndentation` when method arguments are empty with newlines. ([@tatsuyafw][])
* [#6152](https://github.com/rubocop/rubocop/pull/6152): Fix a false negative for `Layout/AccessModifierIndentation` when using access modifiers with arguments within nested classes. ([@gmalette][])
* [#6124](https://github.com/rubocop/rubocop/issues/6124): Fix `Style/IfUnlessModifier` cop for disabled `Layout/Tab` cop when there is no `IndentationWidth` config. ([@AlexWayfer][])
* [#6133](https://github.com/rubocop/rubocop/pull/6133): Fix `AllowURI` option of `Metrics/LineLength` cop for files with tabs indentation. ([@AlexWayfer][])
* [#6164](https://github.com/rubocop/rubocop/issues/6164): Fix incorrect auto-correct for `Style/UnneededCondition` when using operator method higher precedence than `||`. ([@koic][])
* [#6138](https://github.com/rubocop/rubocop/issues/6138): Fix a false positive for assigning a block local variable in `Lint/ShadowedArgument`. ([@jonas054][])
* [#6022](https://github.com/rubocop/rubocop/issues/6022): Fix `Layout/MultilineHashBraceLayout` and `Layout/MultilineArrayBraceLayout` auto-correct syntax error when there is a comment on the last element. ([@bacchir][])
* [#6175](https://github.com/rubocop/rubocop/issues/6175): Fix `Style/BracesAroundHashParameters` auto-correct syntax error when there is a trailing comma. ([@bacchir][])
* [#6192](https://github.com/rubocop/rubocop/issues/6192): Make `Style/RedundantBegin` aware of stabby lambdas. ([@drenmi][])
* [#6208](https://github.com/rubocop/rubocop/pull/6208): Ignore assignment methods in `Naming/PredicateName`. ([@sunny][])
* [#6196](https://github.com/rubocop/rubocop/issues/6196): Fix incorrect auto-correct for `Style/EmptyCaseCondition` when using `return` in `when` clause and assigning the return value of `case`. ([@koic][])
* [#6142](https://github.com/rubocop/rubocop/issues/6142): Ignore keyword arguments in `Rails/Delegate`. ([@sunny][])
* [#6240](https://github.com/rubocop/rubocop/issues/6240): Fix an auto-correct error for `Style/WordArray` when setting `EnforcedStyle: brackets` and using string interpolation in `%W` literal. ([@koic][])
* [#6202](https://github.com/rubocop/rubocop/issues/6202): Fix infinite loop when auto-correcting `Lint/RescueEnsureAlignment` when `end` is misaligned. The alignment and message are now based on the beginning position rather than the `end` position. ([@rrosenblum][])
* [#6199](https://github.com/rubocop/rubocop/issues/6199): Don't recommend `Date` usage in `Style/DateTime`. ([@deivid-rodriguez][])

### Changes

* [#6161](https://github.com/rubocop/rubocop/pull/6161): Add scope methods to `Rails/FindEach` cop. Makes the cop also check for the following scopes: `eager_load`, `includes`, `joins`, `left_joins`, `left_outer_joins`, `preload`, `references`, and `unscoped`. ([@repinel][])
* [#6137](https://github.com/rubocop/rubocop/pull/6137): Allow `db` to allowed names of `Naming/UncommunicativeMethodParamName` cop in default config. ([@mkenyon][])
* Update the highlighting of `Lint/DuplicateMethods` to include the method name. ([@rrosenblum][])
* [#6057](https://github.com/rubocop/rubocop/issues/6057): Return 0 when running `rubocop --auto-gen-conf` if the todo file is successfully created even if there are offenses. ([@MagedMilad][])
* [#4301](https://github.com/rubocop/rubocop/issues/4301): Turn off auto-correct for `Rails/RelativeDateConstant` by default. ([@koic][])
* [#4832](https://github.com/rubocop/rubocop/issues/4832): Change the path pattern (`*`) to match the hidden file. ([@koic][])
* `Style/For` now highlights the entire statement rather than just the keyword. ([@rrosenblum][])
* Disable `Performance/CaseWhenSplat` and its auto-correction by default. ([@rrosenblum][])
* [#6235](https://github.com/rubocop/rubocop/pull/6235): Enable `Layout/EmptyLineAfterGuardClause` cop by default. ([@koic][])
* [#6199](https://github.com/rubocop/rubocop/pull/6199): `Style/DateTime` has been moved to disabled by default. ([@deivid-rodriguez][])

## 0.58.2 (2018-07-23)

### New features

* [#6105](https://github.com/rubocop/rubocop/issues/6105): Support `{a,b}` file name globs in `Exclude` and `Include` config. ([@mikeyhew][])

### Bug fixes

* [#6103](https://github.com/rubocop/rubocop/pull/6103): Fix a false positive for `Layout/IndentationWidth` when multiple modifiers are used in a block and a method call is made at end of the block. ([@koic][])
* [#6084](https://github.com/rubocop/rubocop/issues/6084): Fix `Naming/MemoizedInstanceVariableName` cop to allow methods to have leading underscores. ([@kenman345][])
* [#6098](https://github.com/rubocop/rubocop/issues/6098): Fix an error for `Layout/ClassStructure` when there is a comment in the macro method to be auto-correct. ([@koic][])
* [#6115](https://github.com/rubocop/rubocop/issues/6115): Fix a false positive for `Lint/OrderedMagicComments` when using `{ encoding: Encoding::SJIS }` hash object after `frozen_string_literal` magic comment. ([@koic][])

### Changes

* [#6116](https://github.com/rubocop/rubocop/pull/6116): Add `ip` to allowed names of `Naming/UncommunicativeMethodParamName` cop in default config. ([@nijikon][])

## 0.58.1 (2018-07-10)

### Bug fixes

* [#6071](https://github.com/rubocop/rubocop/issues/6071): Fix auto-correct `Style/MethodCallWithArgsParentheses` when arguments are method calls. ([@maxh][])
* Fix `Style/RedundantParentheses` with hash literal as first argument to `super`. ([@maxh][])
* [#6086](https://github.com/rubocop/rubocop/issues/6086): Fix an error for `Gemspec/OrderedDependencies` when using method call to gem names in gemspec. ([@koic][])
* [#6089](https://github.com/rubocop/rubocop/issues/6089): Make `Rails/BulkChangeTable` aware of variable table name. ([@wata727][])
* [#6088](https://github.com/rubocop/rubocop/issues/6088): Fix an error for `Layout/MultilineAssignmentLayout` cop when using multi-line block defines on separate lines. ([@koic][])
* [#6092](https://github.com/rubocop/rubocop/issues/6092): Don't use the broken parser 2.5.1.1 version. ([@bbatsov][])

## 0.58.0 (2018-07-07)

### New features

* [#5973](https://github.com/rubocop/rubocop/issues/5973): Add new `Style/IpAddresses` cop. ([@dvandersluis][])
* [#5843](https://github.com/rubocop/rubocop/issues/5843): Add configuration options to `Naming/MemoizedInstanceVariableName` cop to allow leading underscores. ([@leklund][])
* [#5843](https://github.com/rubocop/rubocop/issues/5843): Add `EnforcedStyleForLeadingUnderscores` to `Naming/MemoizedInstanceVariableName` cop to allow leading underscores. ([@leklund][])
* `Performance/Sample` will now register an offense when using `shuffle` followed by `at` or `slice`. ([@rrosenblum][])

### Bug fixes

* [#5987](https://github.com/rubocop/rubocop/issues/5987): Suppress errors when using ERB template in Rails/BulkChangeTable. ([@wata727][])
* [#4878](https://github.com/rubocop/rubocop/issues/4878): Fix false positive in `Layout/IndentationWidth` when multiple modifiers and def are on the same line. ([@tatsuyafw][])
* [#5966](https://github.com/rubocop/rubocop/issues/5966): Fix a false positive for `Layout/ClosingHeredocIndentation` when heredoc content is outdented compared to the closing. ([@koic][])
* Fix auto-correct support check for custom cops on --auto-gen-config. ([@r7kamura][])
* Fix exception that occurs when auto-correcting a modifier if statement in `Style/UnneededCondition`. ([@rrosenblum][])
* [#6025](https://github.com/rubocop/rubocop/pull/6025): Fix an incorrect auto-correct for `Lint/UnneededCondition` when using if_branch in `else` branch. ([@koic][])
* [#6029](https://github.com/rubocop/rubocop/issues/6029): Fix a false positive for `Lint/ShadowedArgument` when reassigning to splat variable. ([@koic][])
* [#6035](https://github.com/rubocop/rubocop/issues/6035): Fix error on auto-correction when `Layout/LeadingBlankLines` is the first cop to act. ([@Vasfed][])
* [#6036](https://github.com/rubocop/rubocop/issues/6036): Make `Rails/BulkChangeTable` aware of string table name. ([@wata727][])
* [#5467](https://github.com/rubocop/rubocop/issues/5467): Fix a false negative for `Style/MultipleComparison` when multiple comparison is not part of a conditional. ([@koic][])
* [#6042](https://github.com/rubocop/rubocop/pull/6042): Fix `Lint/RedundantWithObject` error on missing parameter to `each_with_object`. ([@Vasfed][])
* [#6056](https://github.com/rubocop/rubocop/pull/6056): Support string timestamps in `Rails/CreateTableWithTimestamps` cop. ([@drn][])
* [#6052](https://github.com/rubocop/rubocop/issues/6052): Fix a false positive for `Style/SymbolProc` when using  block with adding a comma after the sole argument. ([@koic][])
* [#2743](https://github.com/rubocop/rubocop/issues/2743): Support `<<` as a kind of assignment operator in `Layout/EndAlignment`. ([@jonas054][])
* [#6067](https://github.com/rubocop/rubocop/issues/6067): Prevent auto-correct error for `Performance/InefficientHashSearch` when a method by itself and `include?` method are method chaining. ([@koic][])

### Changes

* [#6006](https://github.com/rubocop/rubocop/pull/6006): Remove `rake repl` task. ([@koic][])
* [#5990](https://github.com/rubocop/rubocop/pull/5990): Drop support for MRI 2.1. ([@drenmi][])
* [#3299](https://github.com/rubocop/rubocop/issues/3299): `Lint/UselessAccessModifier` now warns when `private_class_method` is used without arguments. ([@Darhazer][])
* [#6026](https://github.com/rubocop/rubocop/pull/6026): Exclude `refine` by default from `Metrics/BlockLength` cop. ([@kddeisz][])
* [#4882](https://github.com/rubocop/rubocop/issues/4882): Use `IndentationWidth` of `Layout/Tab` for other cops. ([@AlexWayfer][])

## 0.57.2 (2018-06-12)

### Bug fixes

* [#5968](https://github.com/rubocop/rubocop/issues/5968): Prevent `Layout/ClosingHeredocIndentation` from raising an error on `<<` heredocs. ([@dvandersluis][])
* [#5965](https://github.com/rubocop/rubocop/issues/5965): Prevent `Layout/ClosingHeredocIndentation` from raising an error on heredocs containing only a newline. ([@drenmi][])
* Prevent a crash in `Layout/IndentationConsistency` cop triggered by an empty expression string interpolation. ([@alexander-lazarov][])
* [#5951](https://github.com/rubocop/rubocop/issues/5951): Prevent `Style/MethodCallWithArgsParentheses` from raising an error in certain cases. ([@drenmi][])

## 0.57.1 (2018-06-07)

### Bug fixes

* [#5963](https://github.com/rubocop/rubocop/issues/5963): Allow Performance/ReverseEach to apply to any receiver. ([@dvandersluis][])
* [#5917](https://github.com/rubocop/rubocop/issues/5917): Fix erroneous warning for `inherit_mode` directive. ([@jonas054][])
* [#5380](https://github.com/rubocop/rubocop/issues/5380): Fix false negative in `Layout/IndentationWidth` when an access modifier section has an invalid indentation body. ([@tatsuyafw][])
* [#5909](https://github.com/rubocop/rubocop/pull/5909): Even when a module has no public methods, `Layout/IndentationConsistency` should still register an offense for private methods. ([@jaredbeck][])
* [#5958](https://github.com/rubocop/rubocop/issues/5958): Handle empty method body in `Rails/BulkChangeTable`. ([@wata727][])
* [#5954](https://github.com/rubocop/rubocop/issues/5954): Make `Style/UnneededCondition` cop accepts a case of condition and `if_branch` are same when using `elsif` branch. ([@koic][])

## 0.57.0 (2018-06-06)

### New features

* [#5881](https://github.com/rubocop/rubocop/pull/5881): Add new `Rails/BulkChangeTable` cop. ([@wata727][])
* [#5444](https://github.com/rubocop/rubocop/pull/5444): Add new `Style/AccessModifierDeclarations` cop. ([@brandonweiss][])
* [#5803](https://github.com/rubocop/rubocop/issues/5803): Add new `Style/UnneededCondition` cop. ([@balbesina][])
* [#5406](https://github.com/rubocop/rubocop/issues/5406): Add new `Layout/ClosingHeredocIndentation` cop. ([@siegfault][])
* [#5823](https://github.com/rubocop/rubocop/issues/5823): Add new `slashes` style to `Rails/FilePath` since Ruby accepts forward slashes even on Windows. ([@sunny][])
* New cop `Layout/LeadingBlankLines` checks for empty lines at the beginning of a file. ([@rrosenblum][])

### Bug fixes

* [#5897](https://github.com/rubocop/rubocop/issues/5897): Fix `Style/SymbolArray` and `Style/WordArray` not working on arrays of size 1. ([@TikiTDO][])
* [#5894](https://github.com/rubocop/rubocop/pull/5894): Fix `Rails/AssertNot` to allow it to have failure message. ([@koic][])
* [#5888](https://github.com/rubocop/rubocop/issues/5888): Do not register an offense for `headers` or `env` keyword arguments in `Rails/HttpPositionalArguments`. ([@rrosenblum][])
* Fix the indentation of auto-corrected closing squiggly heredocs. ([@garettarrowood][])
* [#5908](https://github.com/rubocop/rubocop/pull/5908): Fix `Style/BracesAroundHashParameters` auto-correct going past the end of the file when the closing curly brace is on the last line of a file. ([@EiNSTeiN-][])
* Fix a bug where `Style/FrozenStringLiteralComment` would be added to the second line if the first line is empty. ([@rrosenblum][])
* [#5914](https://github.com/rubocop/rubocop/issues/5914): Make `Layout/SpaceInsideReferenceBrackets` aware of `no_space` when using nested reference brackets. ([@koic][])
* [#5799](https://github.com/rubocop/rubocop/issues/5799): Fix false positive in `Style/MixinGrouping` when method named `include` accepts block. ([@Darhazer][])

### Changes

* [#5937](https://github.com/rubocop/rubocop/pull/5937): Add new `--fix-layout/-x` command line alias. ([@scottmatthewman][])
* [#5887](https://github.com/rubocop/rubocop/issues/5887): Remove `Lint/SplatKeywordArguments` cop. ([@koic][])
* [#5761](https://github.com/rubocop/rubocop/pull/5761): Add `httpdate` to accepted `Rails/TimeZone` methods. ([@cupakromer][])
* [#5899](https://github.com/rubocop/rubocop/pull/5899): Add `xmlschema` to accepted `Rails/TimeZone` methods. ([@koic][])
* [#5906](https://github.com/rubocop/rubocop/pull/5906): Move REPL command from `rake repl` task to `bin/console` command. ([@koic][])
* [#5917](https://github.com/rubocop/rubocop/issues/5917): Let `inherit_mode` work for default configuration too. ([@jonas054][])
* [#5929](https://github.com/rubocop/rubocop/pull/5929): Stop including string extensions from `unicode/display_width`. ([@nroman-stripe][])

## 0.56.0 (2018-05-14)

### New features

* [#5848](https://github.com/rubocop/rubocop/pull/5848): Add new `Performance/InefficientHashSearch` cop. ([@JacobEvelyn][])
* [#5801](https://github.com/rubocop/rubocop/pull/5801): Add new `Rails/RefuteMethods` cop. ([@koic][])
* [#5805](https://github.com/rubocop/rubocop/pull/5805): Add new `Rails/AssertNot` cop. ([@composerinteralia][])
* [#4136](https://github.com/rubocop/rubocop/issues/4136): Allow more robust `Layout/ClosingParenthesisIndentation` detection including method chaining. ([@jfelchner][])
* [#5699](https://github.com/rubocop/rubocop/pull/5699): Add `consistent_relative_to_receiver` style option to `Layout/FirstParameterIndentation`. ([@jfelchner][])
* [#5821](https://github.com/rubocop/rubocop/pull/5821): Support `AR::Migration#up_only` for `Rails/ReversibleMigration` cop. ([@koic][])
* [#5800](https://github.com/rubocop/rubocop/issues/5800): Don't show a stacktrace for invalid command-line params. ([@shanecav84][])
* [#5845](https://github.com/rubocop/rubocop/pull/5845): Add new `Lint/ErbNewArguments` cop. ([@koic][])
* [#5871](https://github.com/rubocop/rubocop/pull/5871): Add new `Lint/SplatKeywordArguments` cop. ([@koic][])
* [#4247](https://github.com/rubocop/rubocop/issues/4247): Remove hard-coded file patterns and use only `Include`, `Exclude` and the new `RubyInterpreters` parameters for file selection. ([@jonas054][])

### Bug fixes

* Fix bug in `Style/EmptyMethod` which concatenated the method name and first argument if no method def parentheses are used. ([@thomasbrus][])
* [#5819](https://github.com/rubocop/rubocop/issues/5819): Fix `Rails/SaveBang` when using negated if. ([@Edouard-chin][])
* [#5286](https://github.com/rubocop/rubocop/issues/5286): Fix `Lint/SafeNavigationChain` not detecting chained operators after block. ([@Darhazer][])
* Fix bug where `Lint/SafeNavigationConsistency` registers multiple offenses for the same method call. ([@rrosenblum][])
* [#5713](https://github.com/rubocop/rubocop/issues/5713): Fix `Style/CommentAnnotation` reporting only the first of multiple consecutive offending lines. ([@svendittmer][])
* [#5791](https://github.com/rubocop/rubocop/issues/5791): Fix exception in `Lint/SafeNavigationConsistency` when there is code around the condition. ([@rrosenblum][])
* [#5784](https://github.com/rubocop/rubocop/issues/5784): Fix a false positive for `Rails/HasManyOrHasOneDependent` when using nested `with_options`. ([@koic][])
* [#4666](https://github.com/rubocop/rubocop/issues/4666): `--stdin` always treats input as Ruby source irregardless of filename. ([@PointlessOne][])
* Fix auto-correction for `Style/MethodCallWithArgsParentheses` adding extra parentheses if the method argument was already parenthesized. ([@dvandersluis][])
* [#5668](https://github.com/rubocop/rubocop/issues/5668): Fix an issue where files with unknown extensions, listed in `AllCops/Include` were not inspected when passing the file name as an option. ([@drenmi][])
* [#5809](https://github.com/rubocop/rubocop/issues/5809): Fix exception `Lint/PercentStringArray` and `Lint/PercentSymbolArray` when the inspected file is binary encoded. ([@akhramov][])
* [#5840](https://github.com/rubocop/rubocop/issues/5840): Do not register an offense for methods that `nil` responds to in `Lint/SafeNavigationConsistency`. ([@rrosenblum][])
* [#5862](https://github.com/rubocop/rubocop/issues/5862): Fix an incorrect auto-correct for `Lint/LiteralInInterpolation` if contains numbers. ([@koic][])
* [#5868](https://github.com/rubocop/rubocop/pull/5868): Fix `Rails/CreateTableWithTimestamps` when using hash options. ([@wata727][])
* [#5708](https://github.com/rubocop/rubocop/issues/5708): Fix exception in `Lint/UnneededCopEnableDirective` for instruction '# rubocop:enable **all**'. ([@balbesina][])
* Fix auto-correction of `Rails/HttpPositionalArguments` to use `session` instead of `header`. ([@rrosenblum][])

### Changes

* Split `Style/MethodMissing` into two cops, `Style/MethodMissingSuper` and `Style/MissingRespondToMissing`. ([@rrosenblum][])
* [#5757](https://github.com/rubocop/rubocop/issues/5757): Add `AllowInMultilineConditions` option to `Style/ParenthesesAroundCondition` cop. ([@Darhazer][])
* [#5806](https://github.com/rubocop/rubocop/issues/5806): Fix `Layout/SpaceInsideReferenceBrackets` when assigning a reference bracket to a reference bracket. ([@joshuapinter][])
* [#5082](https://github.com/rubocop/rubocop/issues/5082): Allow caching together with `--auto-correct`. ([@jonas054][])
* Add `try!` to the list of whitelisted methods for `Lint/SafeNavigationChain` and `Style/SafeNavigation`. ([@rrosenblum][])
* [#5886](https://github.com/rubocop/rubocop/pull/5886): Move `Style/EmptyLineAfterGuardClause` cop to `Layout` department. ([@koic][])

## 0.55.0 (2018-04-16)

### New features

* [#5753](https://github.com/rubocop/rubocop/pull/5753): Add new `Performance/UnneededSort` cop. ([@parkerfinch][])
* Add new `Lint/SafeNavigationConsistency` cop. ([@rrosenblum][])

### Bug fixes

* [#5759](https://github.com/rubocop/rubocop/pull/5759): Fix `Performance/RegexpMatch` cop not correcting negated match operator. ([@bdewater][])
* [#5726](https://github.com/rubocop/rubocop/issues/5726): Fix false positive for `:class_name` option in Rails/InverseOf cop. ([@bdewater][])
* [#5686](https://github.com/rubocop/rubocop/issues/5686): Fix a regression for `Style/SymbolArray` and `Style/WordArray` for multiline Arrays. ([@istateside][])
* [#5730](https://github.com/rubocop/rubocop/pull/5730): Stop `Rails/InverseOf` cop allowing `inverse_of: nil` to opt-out. ([@bdewater][])
* [#5561](https://github.com/rubocop/rubocop/issues/5561): Fix `Lint/ShadowedArgument` false positive with shorthand assignments. ([@akhramov][])
* [#5403](https://github.com/rubocop/rubocop/issues/5403): Fix `Naming/HeredocDelimiterNaming` blacklist patterns. ([@mcfisch][])
* [#4298](https://github.com/rubocop/rubocop/issues/4298): Fix auto-correction of `Performance/RegexpMatch` to produce code that safe guards against the receiver being `nil`. ([@rrosenblum][])
* [#5738](https://github.com/rubocop/rubocop/issues/5738): Make `Rails/HttpStatus` ignoring hash order to fix false negative. ([@pocke][])
* [#5720](https://github.com/rubocop/rubocop/pull/5720): Fix false positive for `Style/EmptyLineAfterGuardClause` when guard clause is after heredoc. ([@koic][])
* [#5760](https://github.com/rubocop/rubocop/pull/5760): Fix incorrect offense location for `Style/EmptyLineAfterGuardClause` when guard clause is after heredoc argument. ([@koic][])
* [#5764](https://github.com/rubocop/rubocop/pull/5764): Fix `Style/UnpackFirst` false positive of `unpack('h*').take(1)`. ([@parkerfinch][])
* [#5766](https://github.com/rubocop/rubocop/issues/5766): Update `Style/FrozenStringLiteralComment` auto-correction to insert a new line between the comment and the code. ([@rrosenblum][])
* [#5551](https://github.com/rubocop/rubocop/issues/5551): Fix `Lint/Void` not detecting void context in blocks with single expression. ([@Darhazer][])

### Changes

* [#5752](https://github.com/rubocop/rubocop/pull/5752): Add `String#delete_{prefix,suffix}` to Lint/Void cop. ([@bdewater][])
* [#5734](https://github.com/rubocop/rubocop/pull/5734): Add `by`, `on`, `in` and `at` to allowed names of `Naming/UncommunicativeMethodParamName` cop in default config. ([@AlexWayfer][])
* [#5666](https://github.com/rubocop/rubocop/issues/5666): Add spaces as an `EnforcedStyle` option to `Layout/SpaceInsideParens`, allowing you to enforce spaces inside of parentheses. ([@joshuapinter][])
* [#4257](https://github.com/rubocop/rubocop/issues/4257): Allow specifying module name in `Metrics/BlockLength`'s `ExcludedMethods` configuration option. ([@akhramov][])
* [#4753](https://github.com/rubocop/rubocop/issues/4753): Add `IgnoredMethods` option to `Style/MethodCallWithoutArgsParentheses` cop. ([@Darhazer][])
* [#4517](https://github.com/rubocop/rubocop/issues/4517): Add option to allow trailing whitespaces inside heredoc strings. ([@Darhazer][])
* [#5652](https://github.com/rubocop/rubocop/issues/5652): Make `Style/OptionHash` aware of implicit parameter passing to super. ([@Wei-LiangChew][])
* [#5451](https://github.com/rubocop/rubocop/issues/5451): When using --auto-gen-config, do not output offenses unless the --output-offenses flag is also passed. ([@drewpterry][])

## 0.54.0 (2018-03-21)

### New features

* [#5597](https://github.com/rubocop/rubocop/pull/5597): Add new `Rails/HttpStatus` cop. ([@anthony-robin][])
* [#5643](https://github.com/rubocop/rubocop/pull/5643): Add new `Style/UnpackFirst` cop. ([@bdewater][])

### Bug fixes

* [#5744](https://github.com/rubocop/rubocop/pull/5744): Teach `Performance/StartWith` and `EndWith` cops to look for `Regexp#match?`. ([@bdewater][])
* [#5683](https://github.com/rubocop/rubocop/issues/5683): Fix message for `Naming/UncommunicativeXParamName` cops. ([@jlfaber][])
* [#5680](https://github.com/rubocop/rubocop/issues/5680): Fix `Layout/ElseAlignment` for `rescue/else/ensure` inside `do/end` blocks. ([@YukiJikumaru][])
* [#5642](https://github.com/rubocop/rubocop/pull/5642): Fix `Style/Documentation` `:nodoc:` for compact-style nested modules/classes. ([@ojab][])
* [#5648](https://github.com/rubocop/rubocop/issues/5648): Suggest valid memoized instance variable for predicate method. ([@satyap][])
* [#5670](https://github.com/rubocop/rubocop/issues/5670): Suggest valid memoized instance variable for bang method. ([@pocke][])
* [#5623](https://github.com/rubocop/rubocop/pull/5623): Fix `Bundler/OrderedGems` when a group includes duplicate gems. ([@colorbox][])
* [#5633](https://github.com/rubocop/rubocop/pull/5633): Fix broken `--fail-fast`. ([@mmyoji][])
* [#5630](https://github.com/rubocop/rubocop/issues/5630): Fix false positive for `Style/FormatStringToken` when using placeholder arguments in `format` method. ([@koic][])
* [#5651](https://github.com/rubocop/rubocop/pull/5651): Fix NoMethodError when specified config file that does not exist. ([@onk][])
* [#5647](https://github.com/rubocop/rubocop/pull/5647): Fix encoding method of RuboCop::MagicComment::SimpleComment. ([@htwroclau][])
* [#5619](https://github.com/rubocop/rubocop/issues/5619): Do not register an offense in `Style/InverseMethods` when comparing constants with `<`, `>`, `<=`, or `>=`. If the code is being used to determine class hierarchy, the correction might not be accurate. ([@rrosenblum][])
* [#5641](https://github.com/rubocop/rubocop/issues/5641): Disable `Style/TrivialAccessors` auto-correction for `def` with `private`. ([@pocke][])
* Fix bug where `Style/SafeNavigation` does not auto-correct all chained methods resulting in a `Lint/SafeNavigationChain` offense. ([@rrosenblum][])
* [#5436](https://github.com/rubocop/rubocop/issues/5436): Allow empty kwrest args in `UncommunicativeName` cops. ([@pocke][])
* [#5674](https://github.com/rubocop/rubocop/issues/5674): Fix auto-correction of `Layout/EmptyComment` when the empty comment appears on the same line as code. ([@rrosenblum][])
* [#5679](https://github.com/rubocop/rubocop/pull/5679): Fix a false positive for `Style/EmptyLineAfterGuardClause` when guard clause is before `rescue` or `ensure`. ([@koic][])
* [#5694](https://github.com/rubocop/rubocop/issues/5694): Match Rails versions with multiple digits when reading the TargetRailsVersion from the bundler lock files. ([@roberts1000][])
* [#5700](https://github.com/rubocop/rubocop/pull/5700): Fix a false positive for `Style/EmptyLineAfterGuardClause` when guard clause is before `else`. ([@koic][])
* Fix false positive in `Naming/ConstantName` when using conditional assignment. ([@drenmi][])

### Changes

* [#5626](https://github.com/rubocop/rubocop/pull/5626): Change `Naming/UncommunicativeMethodParamName` add `to` to allowed names in default config. ([@unused][])
* [#5640](https://github.com/rubocop/rubocop/issues/5640): Warn about user configuration overriding other user configuration only with `--debug`. ([@jonas054][])
* [#5637](https://github.com/rubocop/rubocop/issues/5637): Fix error for `Layout/SpaceInsideArrayLiteralBrackets` when contains an array literal as an argument after a heredoc is started. ([@koic][])
* [#5610](https://github.com/rubocop/rubocop/issues/5610): Use `gems.locked` or `Gemfile.lock` to determine the best `TargetRubyVersion` when it is not specified in the config. ([@roberts1000][])
* [#5390](https://github.com/rubocop/rubocop/issues/5390): Allow exceptions to `Style/InlineComment` for inline comments which enable or disable rubocop cops. ([@jfelchner][])
* Add progress bar to offenses formatter. ([@drewpterry][])
* [#5498](https://github.com/rubocop/rubocop/issues/5498): Correct `IndentHeredoc` message for Ruby 2.3 when using `<<~` operator with invalid indentation. ([@hamada14][])

## 0.53.0 (2018-03-05)

### New features

* [#3666](https://github.com/rubocop/rubocop/issues/3666): Add new `Naming/UncommunicativeBlockParamName` cop. ([@garettarrowood][])
* [#3666](https://github.com/rubocop/rubocop/issues/3666): Add new `Naming/UncommunicativeMethodParamName` cop. ([@garettarrowood][])
* [#5356](https://github.com/rubocop/rubocop/issues/5356): Add new `Lint/UnneededCopEnableDirective` cop. ([@garettarrowood][])
* [#5248](https://github.com/rubocop/rubocop/pull/5248): Add new `Lint/BigDecimalNew` cop. ([@koic][])
* Add new `Style/TrailingBodyOnClass` cop. ([@garettarrowood][])
* Add new `Style/TrailingBodyOnModule` cop. ([@garettarrowood][])
* [#3394](https://github.com/rubocop/rubocop/issues/3394): Add new `Style/TrailingCommaInArrayLiteral` cop. ([@garettarrowood][])
* [#3394](https://github.com/rubocop/rubocop/issues/3394): Add new `Style/TrailingCommaInHashLiteral` cop. ([@garettarrowood][])
* [#5319](https://github.com/rubocop/rubocop/pull/5319): Add new `Security/Open` cop. ([@mame][])
* Add `EnforcedStyleForEmptyBrackets` configuration to `Layout/SpaceInsideReferenceBrackets`. ([@garettarrowood][])
* [#5050](https://github.com/rubocop/rubocop/issues/5050): Add auto-correction to `Style/ModuleFunction`. ([@garettarrowood][])
* [#5358](https://github.com/rubocop/rubocop/pull/5358):  `--no-auto-gen-timestamp` CLI option suppresses the inclusion of the date and time it was generated in auto-generated config. ([@dominicsayers][])
* [#4274](https://github.com/rubocop/rubocop/issues/4274): Add new `Layout/EmptyComment` cop. ([@koic][])
* [#4477](https://github.com/rubocop/rubocop/issues/4477): Add new configuration directive: `inherit_mode` for merging arrays. ([@leklund][])
* [#5532](https://github.com/rubocop/rubocop/pull/5532): Include `.axlsx` file by default. ([@georf][])
* [#5490](https://github.com/rubocop/rubocop/issues/5490): Add new `Lint/OrderedMagicComments` cop. ([@koic][])
* [#4008](https://github.com/rubocop/rubocop/issues/4008): Add new `Style/ExpandPathArguments` cop. ([@koic][])
* [#4812](https://github.com/rubocop/rubocop/issues/4812): Add `beginning_only` and `ending_only` style options to `Layout/EmptyLinesAroundClassBody` cop. ([@jmks][])
* [#5591](https://github.com/rubocop/rubocop/pull/5591): Include `.arb` file by default. ([@deivid-rodriguez][])
* [#5473](https://github.com/rubocop/rubocop/issues/5473): Use `gems.locked` or `Gemfile.lock` to determine the best `TargetRailsVersion` when it is not specified in the config. ([@roberts1000][])
* Add new `Naming/MemoizedInstanceVariableName` cop. ([@satyap][])
* [#5376](https://github.com/rubocop/rubocop/issues/5376): Add new `Style/EmptyLineAfterGuardClause` cop. ([@unkmas][])
* Add new `Rails/ActiveRecordAliases` cop. ([@elebow][])

### Bug fixes

* [#4105](https://github.com/rubocop/rubocop/issues/4105): Fix `Lint/IndentationWidth` when `Lint/EndAlignment` is configured with `start_of_line`. ([@brandonweiss][])
* [#5453](https://github.com/rubocop/rubocop/issues/5453): Fix erroneous downcase in `Performance/Casecmp` auto-correction. ([@walinga][])
* [#5343](https://github.com/rubocop/rubocop/issues/5343): Fix offense detection in `Style/TrailingMethodEndStatement`. ([@garettarrowood][])
* [#5334](https://github.com/rubocop/rubocop/issues/5334): Fix semicolon removal for `Style/TrailingBodyOnMethodDefinition` auto-correction. ([@garettarrowood][])
* [#5350](https://github.com/rubocop/rubocop/issues/5350): Fix `Metric/LineLength` false offenses for URLs in double quotes. ([@garettarrowood][])
* [#5333](https://github.com/rubocop/rubocop/issues/5333): Fix `Layout/EmptyLinesAroundArguments` false positives for inline access modifiers. ([@garettarrowood][])
* [#5339](https://github.com/rubocop/rubocop/issues/5339): Fix `Layout/EmptyLinesAroundArguments` false positives for multiline heredoc arguments. ([@garettarrowood][])
* [#5383](https://github.com/rubocop/rubocop/issues/5383): Fix `Rails/Presence` false detection of receiver for locally defined `blank?` & `present?` methods. ([@garettarrowood][])
* [#5314](https://github.com/rubocop/rubocop/issues/5314): Fix false positives for `Lint/NestedPercentLiteral` when percent characters are nested. ([@asherkach][])
* [#5357](https://github.com/rubocop/rubocop/issues/5357): Fix `Lint/InterpolationCheck` false positives on escaped interpolations. ([@pocke][])
* [#5409](https://github.com/rubocop/rubocop/issues/5409): Fix multiline indent for `Style/SymbolArray` and `Style/WordArray` auto-correct. ([@flyerhzm][])
* [#5393](https://github.com/rubocop/rubocop/issues/5393): Fix `Rails/Delegate`'s false positive with a method call with arguments. ([@pocke][])
* [#5348](https://github.com/rubocop/rubocop/issues/5348): Fix false positive for `Style/SafeNavigation` when safe guarding more comparison methods. ([@rrosenblum][])
* [#4889](https://github.com/rubocop/rubocop/issues/4889): Auto-correcting `Style/SafeNavigation` will add safe navigation to all methods in a method chain. ([@rrosenblum][])
* [#5287](https://github.com/rubocop/rubocop/issues/5287): Do not register an offense in `Style/SafeNavigation` if there is an unsafe method used in a method chain. ([@rrosenblum][])
* [#5401](https://github.com/rubocop/rubocop/issues/5401): Fix `Style/RedundantReturn` to trigger when begin-end, rescue, and ensure blocks present. ([@asherkach][])
* [#5426](https://github.com/rubocop/rubocop/issues/5426): Make `Rails/InverseOf` accept `inverse_of: nil` to opt-out. ([@wata727][])
* [#5448](https://github.com/rubocop/rubocop/issues/5448): Improve `Rails/LexicallyScopedActionFilter`. ([@wata727][])
* [#3947](https://github.com/rubocop/rubocop/issues/3947): Fix false positive for `Rails/FilePath` when using `Rails.root.join` in string interpolation of argument. ([@koic][])
* [#5479](https://github.com/rubocop/rubocop/issues/5479): Fix false positives for `Rails/Presence` when using with `elsif`. ([@wata727][])
* [#5427](https://github.com/rubocop/rubocop/pull/5427): Fix exception when executing from a different drive on Windows. ([@orgads][])
* [#5429](https://github.com/rubocop/rubocop/issues/5429): Detect tabs other than indentation by `Layout/Tab`. ([@pocke][])
* [#5496](https://github.com/rubocop/rubocop/pull/5496): Fix a false positive of `Style/FormatStringToken` with unrelated `format` call. ([@pocke][])
* [#5503](https://github.com/rubocop/rubocop/issues/5503): Fix `Rails/CreateTableWithTimestamps` false positive when using `to_proc` syntax. ([@wata727][])
* [#5512](https://github.com/rubocop/rubocop/issues/5512): Improve `Lint/Void` to detect `Kernel#tap` as method that ignores the block's value. ([@untitaker][])
* [#5520](https://github.com/rubocop/rubocop/issues/5520): Fix `Style/RedundantException` auto-correction does not keep parenthesization. ([@dpostorivo][])
* [#5524](https://github.com/rubocop/rubocop/issues/5524): Return the instance based on the new type when calls `RuboCop::AST::Node#updated`. ([@wata727][])
* [#5527](https://github.com/rubocop/rubocop/issues/5527): Avoid behavior-changing corrections in `Style/SafeNavigation`. ([@jonas054][])
* [#5539](https://github.com/rubocop/rubocop/pull/5539): Fix compilation error and ruby code generation when passing args to funcall and predicates. ([@Edouard-chin][])
* [#4669](https://github.com/rubocop/rubocop/issues/4669): Use binary file contents for cache key so changing EOL characters invalidates the cache. ([@jonas054][])
* [#3947](https://github.com/rubocop/rubocop/issues/3947): Fix false positive for `Performance::RegexpMatch` when using `MatchData` before guard clause. ([@koic][])
* [#5515](https://github.com/rubocop/rubocop/issues/5515): Fix `Style/EmptyElse` auto-correct for nested if and case statements. ([@asherkach][])
* [#5582](https://github.com/rubocop/rubocop/issues/5582): Fix `end` alignment for variable assignment with line break after `=` in `Layout/EndAlignment`. ([@jonas054][])
* [#5602](https://github.com/rubocop/rubocop/pull/5602): Fix false positive for `Style/ColonMethodCall` when using Java package namespace. ([@koic][])
* [#5603](https://github.com/rubocop/rubocop/pull/5603): Fix falsey offense for `Style/RedundantSelf` with pseudo variables. ([@pocke][])
* [#5547](https://github.com/rubocop/rubocop/issues/5547): Fix auto-correction of `Layout/BlockEndNewline` when there is top level code outside of a class. ([@rrosenblum][])
* [#5599](https://github.com/rubocop/rubocop/issues/5599): Fix the suggestion being used by `Lint/NumberConversion` to use base 10 with Integer. ([@rrosenblum][])
* [#5534](https://github.com/rubocop/rubocop/issues/5534): Fix `Style/EachWithObject` auto-correction leaves an empty line. ([@flyerhzm][])
* Fix `Layout/EmptyLinesAroundAccessModifier` false-negative when next string after access modifier started with end. ([@unkmas][])

### Changes

* [#5589](https://github.com/rubocop/rubocop/issues/5589): Remove `Performance/HashEachMethods` cop as it no longer provides a performance benefit. ([@urbanautomaton][])
* [#3394](https://github.com/rubocop/rubocop/issues/3394): Remove `Style/TrailingCommaInLiteral` in favor of two new cops. ([@garettarrowood][])
* Rename `Lint/UnneededDisable` to `Lint/UnneededCopDisableDirective`. ([@garettarrowood][])
* [#5365](https://github.com/rubocop/rubocop/pull/5365): Add `*.gemfile` to Bundler cop target. ([@sue445][])
* [#4477](https://github.com/rubocop/rubocop/issues/4477): Warn when user configuration overrides other user configuration. ([@jonas054][])
* [#5240](https://github.com/rubocop/rubocop/pull/5240): Make `Style/StringHashKeys` to accepts environment variables. ([@pocke][])
* [#5395](https://github.com/rubocop/rubocop/pull/5395): Always exit 2 when specified configuration file does not exist. ([@pocke][])
* [#5402](https://github.com/rubocop/rubocop/pull/5402): Remove undefined `ActiveSupport::TimeZone#strftime` method from defined dangerous methods of `Rails/TimeZone` cop. ([@koic][])
* [#4704](https://github.com/rubocop/rubocop/issues/4704): Move `Lint/EndAlignment`, `Lint/DefEndAlignment`, `Lint/BlockAlignment`, and `Lint/ConditionPosition` to the `Layout` namespace. ([@bquorning][])
* [#5283](https://github.com/rubocop/rubocop/issues/5283): Change file path output by `Formatter::JSONFormatter` from relative path to smart path. ([@koic][])
* `Style/SafeNavigation` will now register an offense for methods that `nil` responds to. ([@rrosenblum][])
* [#5542](https://github.com/rubocop/rubocop/pull/5542): Exclude `.git/` by default. ([@pocke][])
* Tell Read the Docs to build downloadable docs. ([@eostrom][])
* Change `Style/SafeNavigation` to no longer register an offense for method chains exceeding 2 methods. ([@rrosenblum][])
* Remove auto-correction from `Lint/SafeNavigationChain`. ([@rrosenblum][])
* Change the highlighting of `Lint/SafeNavigationChain` to highlight the entire method chain beyond the safe navigation portion. ([@rrosenblum][])

## 0.52.1 (2017-12-27)

### Bug fixes

* [#5241](https://github.com/rubocop/rubocop/issues/5241): Fix an error for `Layout/AlignHash` when using a hash including only a keyword splat. ([@wata727][])
* [#5245](https://github.com/rubocop/rubocop/issues/5245): Make `Style/FormatStringToken` to allow regexp token. ([@pocke][])
* [#5224](https://github.com/rubocop/rubocop/pull/5224): Fix false positives for `Layout/EmptyLinesAroundArguments` operating on blocks. ([@garettarrowood][])
* [#5234](https://github.com/rubocop/rubocop/issues/5234): Fix a false positive for `Rails/HasManyOrHasOneDependent` when using `class_name` option. ([@koic][])
* [#5273](https://github.com/rubocop/rubocop/issues/5273): Fix `Style/EvalWithLocation` reporting bad line offset. ([@pocke][])
* [#5228](https://github.com/rubocop/rubocop/issues/5228): Handle overridden `Metrics/LineLength:Max` for `--auto-gen-config`. ([@jonas054][])
* [#5226](https://github.com/rubocop/rubocop/issues/5226): Suppress false positives for `Rails/RedundantReceiverInWithOptions` when including another receiver in `with_options`. ([@wata727][])
* [#5259](https://github.com/rubocop/rubocop/pull/5259): Fix false positives in `Style/CommentedKeyword`. ([@garettarrowood][])
* [#5238](https://github.com/rubocop/rubocop/pull/5238): Fix error when #present? or #blank? is used in if or unless modifier. ([@eitoball][])
* [#5261](https://github.com/rubocop/rubocop/issues/5261): Fix a false positive for `Style/MixinUsage` when using inside class or module. ([@koic][])
* [#5289](https://github.com/rubocop/rubocop/issues/5289): Fix `Layout/SpaceInsideReferenceBrackets` and `Layout/SpaceInsideArrayLiteralBrackets` configuration conflicts. ([@garettarrowood][])
* [#4444](https://github.com/rubocop/rubocop/issues/4444): Fix `Style/AutoResourceCleanup` shouldn't flag `File.open(...).close`. ([@dpostorivo][])
* [#5278](https://github.com/rubocop/rubocop/pull/5278): Fix deprecation check to use `loaded_path` in warning. ([@chrishulton][])
* [#5293](https://github.com/rubocop/rubocop/issues/5293): Fix a regression for `Rails/HasManyOrHasOneDependent` when using a option of `has_many` or `has_one` association. ([@koic][])
* [#5223](https://github.com/rubocop/rubocop/issues/5223): False offences in :unannotated Style/FormatStringToken. ([@nattfodd][])
* [#5258](https://github.com/rubocop/rubocop/issues/5258): Fix incorrect auto-correction for `Rails/Presence` when the else block is multiline. ([@wata727][])
* [#5297](https://github.com/rubocop/rubocop/pull/5297): Improve inspection for `Rails/InverseOf` when including `through` or `polymorphic` options. ([@wata727][])
* [#5281](https://github.com/rubocop/rubocop/issues/5281): Fix issue where `--auto-gen-config` might fail on invalid YAML. ([@bquorning][])
* [#5313](https://github.com/rubocop/rubocop/issues/5313): Fix `Style/HashSyntax` from stripping quotes off of symbols during auto-correction for ruby22+. ([@garettarrowood][])
* [#5315](https://github.com/rubocop/rubocop/issues/5315): Fix a false positive of `Layout/RescueEnsureAlignment` in Ruby 2.5. ([@pocke][])
* [#5236](https://github.com/rubocop/rubocop/issues/5236): Fix false positives for `Rails/InverseOf` when using `with_options`. ([@wata727][])
* [#5291](https://github.com/rubocop/rubocop/issues/5291): Fix multiline indent for `Style/BracesAroundHashParameters` auto-correct. ([@flyerhzm][])
* [#3318](https://github.com/rubocop/rubocop/issues/3318): Look for `.ruby-version` in parent directories. ([@ybiquitous][])

### Changes

* [#5300](https://github.com/rubocop/rubocop/pull/5300): Display correction candidate if an incorrect cop name is given. ([@yhirano55][])
* [#5233](https://github.com/rubocop/rubocop/pull/5233): Remove `Style/ExtendSelf` cop. ([@pocke][])
* [#5221](https://github.com/rubocop/rubocop/issues/5221): Change `Layout/SpaceBeforeBlockBraces`'s `EnforcedStyleForEmptyBraces` from `no_space` to `space`. ([@garettarrowood][])
* [#3558](https://github.com/rubocop/rubocop/pull/3558): Create `Corrector` classes and move all `autocorrect` methods out of mixin Modules. ([@garettarrowood][])
* [#3437](https://github.com/rubocop/rubocop/issues/3437): Add new `Lint/NumberConversion` cop. ([@albertpaulp][])

## 0.52.0 (2017-12-12)

### New features

* [#5101](https://github.com/rubocop/rubocop/pull/5101): Allow to specify `TargetRubyVersion` 2.5. ([@walf443][])
* [#1575](https://github.com/rubocop/rubocop/issues/1575): Add new `Layout/ClassStructure` cop that checks whether definitions in a class are in the configured order. This cop is disabled by default. ([@jonatas][])
* New cop `Rails/InverseOf` checks for association arguments that require setting the `inverse_of` option manually. ([@bdewater][])
* [#4811](https://github.com/rubocop/rubocop/issues/4811): Add new `Layout/SpaceInsideReferenceBrackets` cop. ([@garettarrowood][])
* [#4811](https://github.com/rubocop/rubocop/issues/4811): Add new `Layout/SpaceInsideArrayLiteralBrackets` cop. ([@garettarrowood][])
* [#4252](https://github.com/rubocop/rubocop/issues/4252): Add new `Style/TrailingBodyOnMethodDefinition` cop. ([@garettarrowood][])
* Add new `Style/TrailingMethodEndStatement` cop. ([@garettarrowood][])
* [#5074](https://github.com/rubocop/rubocop/issues/5074): Add Layout/EmptyLinesAroundArguments cop. ([@garettarrowood][])
* [#4650](https://github.com/rubocop/rubocop/issues/4650): Add new `Style/StringHashKeys` cop. ([@donjar][])
* [#1583](https://github.com/rubocop/rubocop/issues/1583): Add a quiet formatter. ([@drenmi][])
* Add new `Style/RandomWithOffset` cop. ([@donjar][])
* [#4892](https://github.com/rubocop/rubocop/issues/4892): Add new `Lint/ShadowedArgument` cop and remove argument shadowing detection from `Lint/UnusedBlockArgument` and `Lint/UnusedMethodArgument`. ([@akhramov][])
* [#4674](https://github.com/rubocop/rubocop/issues/4674): Add a new `Lint/MissingCopEnableDirective` cop. ([@tdeo][])
* Add new `Rails/EnvironmentComparison` cop. ([@tdeo][])
* Add `AllowedChars` option to `Style/AsciiComments` cop. ([@hedgesky][])
* [#5031](https://github.com/rubocop/rubocop/pull/5031): Add new `Style/EmptyBlockParameter` and `Style/EmptyLambdaParameter` cops. ([@pocke][])
* [#5057](https://github.com/rubocop/rubocop/pull/5057): Add new `Gemspec/RequiredRubyVersion` cop. ([@koic][])
* [#5087](https://github.com/rubocop/rubocop/pull/5087): Add new `Gemspec/RedundantAssignment` cop. ([@koic][])
* Add `unannotated` option to `Style/FormatStringToken` cop. ([@drenmi][])
* [#5077](https://github.com/rubocop/rubocop/pull/5077): Add new `Rails/CreateTableWithTimestamps` cop. ([@wata727][])
* Add new `Style/ColonMethodDefinition` cop. ([@rrosenblum][])
* Add new `Style/ExtendSelf` cop. ([@drenmi][])
* [#5185](https://github.com/rubocop/rubocop/pull/5185): Add new `Rails/RedundantReceiverInWithOptions` cop. ([@koic][])
* [#5177](https://github.com/rubocop/rubocop/pull/5177): Add new `Rails/LexicallyScopedActionFilter` cop. ([@wata727][])
* [#5173](https://github.com/rubocop/rubocop/pull/5173): Add new `Style/EvalWithLocation` cop. ([@pocke][])
* [#5208](https://github.com/rubocop/rubocop/pull/5208): Add new `Rails/Presence` cop. ([@wata727][])
* Allow auto-correction of ClassAndModuleChildren. ([@siegfault][], [@melch][])

### Bug fixes

* [#5096](https://github.com/rubocop/rubocop/issues/5096): Fix incorrect detection and auto-correction of multiple extend/include/prepend. ([@marcandre][])
* [#5219](https://github.com/rubocop/rubocop/issues/5219): Fix incorrect empty line detection for block arguments in `Layout/EmptyLinesAroundArguments`. ([@garettarrowood][])
* [#4662](https://github.com/rubocop/rubocop/issues/4662): Fix incorrect indent level detection when first line of heredoc is blank. ([@sambostock][])
* [#5016](https://github.com/rubocop/rubocop/issues/5016): Fix a false positive for `Style/ConstantName` with constant names using non-ASCII capital letters with accents. ([@timrogers][])
* [#4866](https://github.com/rubocop/rubocop/issues/4866): Prevent `Layout/BlockEndNewline` cop from introducing trailing whitespaces. ([@bgeuken][])
* [#3396](https://github.com/rubocop/rubocop/issues/3396): Concise error when config. file not found. ([@jaredbeck][])
* [#4881](https://github.com/rubocop/rubocop/issues/4881): Fix a false positive for `Performance/HashEachMethods` when unused argument(s) exists in other blocks. ([@pocke][])
* [#4883](https://github.com/rubocop/rubocop/pull/4883): Fix auto-correction for `Performance/HashEachMethods`. ([@pocke][])
* [#4896](https://github.com/rubocop/rubocop/pull/4896): Fix Style/DateTime wrongly triggered on classes `...::DateTime`. ([@dpostorivo][])
* [#4938](https://github.com/rubocop/rubocop/pull/4938): Fix behavior of `Lint/UnneededDisable`, which was returning offenses even after being disabled in a comment. ([@tdeo][])
* [#4887](https://github.com/rubocop/rubocop/pull/4887): Add undeclared configuration option `EnforcedStyleForEmptyBraces` for `Layout/SpaceBeforeBlockBraces` cop. ([@drenmi][])
* [#4987](https://github.com/rubocop/rubocop/pull/4987): Skip permission check when using stdin option. ([@mtsmfm][])
* [#4909](https://github.com/rubocop/rubocop/issues/4909): Make `Rails/HasManyOrHasOneDependent` aware of multiple associations in `with_options`. ([@koic][])
* [#4794](https://github.com/rubocop/rubocop/issues/4794): Fix an error in `Layout/MultilineOperationIndentation` when an operation spans multiple lines and contains a ternary expression. ([@rrosenblum][])
* [#4885](https://github.com/rubocop/rubocop/issues/4885): Fix false offense detected by `Style/MixinUsage` cop. ([@koic][])
* [#3363](https://github.com/rubocop/rubocop/pull/3363): Fix `Style/EmptyElse` auto-correction removes comments from branches. ([@dpostorivo][])
* [#5025](https://github.com/rubocop/rubocop/issues/5025): Fix error with Layout/MultilineMethodCallIndentation cop and lambda.(...). ([@dpostorivo][])
* [#4781](https://github.com/rubocop/rubocop/issues/4781): Prevent `Style/UnneededPercentQ` from breaking on strings that are concatenated with backslash. ([@pocke][])
* [#4363](https://github.com/rubocop/rubocop/issues/4363): Fix `Style/PercentLiteralDelimiters` incorrectly automatically modifies escaped percent literal delimiter. ([@koic][])
* [#5053](https://github.com/rubocop/rubocop/issues/5053): Fix `Naming/ConstantName` false offense on assigning to a nonoffensive assignment. ([@garettarrowood][])
* [#5019](https://github.com/rubocop/rubocop/pull/5019): Fix auto-correct for `Style/HashSyntax` cop when hash is used as unspaced argument. ([@drenmi][])
* [#5052](https://github.com/rubocop/rubocop/pull/5052): Improve accuracy of `Style/BracesAroundHashParameters` auto-correction. ([@garettarrowood][])
* [#5059](https://github.com/rubocop/rubocop/issues/5059): Fix a false positive for `Style/MixinUsage` when `include` call is a method argument. ([@koic][])
* [#5071](https://github.com/rubocop/rubocop/pull/5071): Fix a false positive in `Lint/UnneededSplatExpansion`, when `Array.new` resides in an array literal. ([@akhramov][])
* [#4071](https://github.com/rubocop/rubocop/issues/4071): Prevent generating wrong code by Style/ColonMethodCall and Style/RedundantSelf. ([@pocke][])
* [#5089](https://github.com/rubocop/rubocop/issues/5089): Fix false positive for `Style/SafeNavigation` when safe guarding arithmetic operation or assignment. ([@tiagotex][])
* [#5099](https://github.com/rubocop/rubocop/pull/5099): Prevent `Style/MinMax` from breaking on implicit receivers. ([@drenmi][])
* [#5079](https://github.com/rubocop/rubocop/issues/5079): Fix false positive for `Style/SafeNavigation` when safe guarding comparisons. ([@tiagotex][])
* [#5075](https://github.com/rubocop/rubocop/issues/5075): Fix auto-correct for `Style/RedundantParentheses` cop when unspaced ternary is present. ([@tiagotex][])
* [#5155](https://github.com/rubocop/rubocop/issues/5155): Fix a false negative for `Naming/ConstantName` cop when using frozen object assignment. ([@koic][])
* Fix a false positive in `Style/SafeNavigation` when the right hand side is negated. ([@rrosenblum][])
* [#5128](https://github.com/rubocop/rubocop/issues/5128): Fix `Bundler/OrderedGems` when gems are references from variables (ignores them in the sorting). ([@tdeo][])

### Changes

* [#4848](https://github.com/rubocop/rubocop/pull/4848): Exclude lambdas and procs from `Metrics/ParameterLists`. ([@reitermarkus][])
* [#5120](https://github.com/rubocop/rubocop/pull/5120):  Improve speed of RuboCop::PathUtil#smart_path. ([@walf443][])
* [#4888](https://github.com/rubocop/rubocop/pull/4888): Improve offense message of `Style/StderrPuts`. ([@jaredbeck][])
* [#4886](https://github.com/rubocop/rubocop/issues/4886): Fix false offense for Style/CommentedKeyword. ([@michniewicz][])
* [#4977](https://github.com/rubocop/rubocop/pull/4977): Make `Lint/RedundantWithIndex` cop aware of offset argument. ([@koic][])
* [#2679](https://github.com/rubocop/rubocop/issues/2679): Handle dependencies to `Metrics/LineLength: Max` when generating `.rubocop_todo.yml`. ([@jonas054][])
* [#4943](https://github.com/rubocop/rubocop/pull/4943): Make cop generator compliant with the repo's rubocop config. ([@tdeo][])
* [#5011](https://github.com/rubocop/rubocop/pull/5011): Remove `SupportedStyles` from "Configuration parameters" in `.rubocop_todo.yml`. ([@pocke][])
* `Lint/RescueWithoutErrorClass` has been replaced by `Style/RescueStandardError`. ([@rrosenblum][])
* [#4811](https://github.com/rubocop/rubocop/issues/4811): Remove `Layout/SpaceInsideBrackets` in favor of two new configurable cops. ([@garettarrowood][])
* [#5042](https://github.com/rubocop/rubocop/pull/5042): Make offense locations of metrics cops to contain whole a method. ([@pocke][])
* [#5044](https://github.com/rubocop/rubocop/pull/5044): Add last_line and last_column into outputs of the JSON formatter. ([@pocke][])
* [#4633](https://github.com/rubocop/rubocop/issues/4633): Make metrics cops aware of `define_method`. ([@pocke][])
* [#5037](https://github.com/rubocop/rubocop/pull/5037): Make display cop names to enable by default. ([@pocke][])
* [#4449](https://github.com/rubocop/rubocop/issues/4449): Make `Layout/IndentHeredoc` aware of line length. ([@pocke][])
* [#5146](https://github.com/rubocop/rubocop/pull/5146): Make `--show-cops` option aware of `--force-default-config`. ([@pocke][])
* [#3001](https://github.com/rubocop/rubocop/issues/3001): Add configuration to `Lint/MissingCopEnableDirective` cop. ([@tdeo][])
* [#4932](https://github.com/rubocop/rubocop/issues/4932): Do not fail if configuration contains `Lint/Syntax` cop with the same settings as the default. ([@tdeo][])
* [#5175](https://github.com/rubocop/rubocop/pull/5175): Make Style/RedundantBegin aware of do-end block in Ruby 2.5. ([@pocke][])

## 0.51.0 (2017-10-18)

### New features

* [#4791](https://github.com/rubocop/rubocop/pull/4791): Add new `Rails/UnknownEnv` cop. ([@pocke][])
* [#4690](https://github.com/rubocop/rubocop/issues/4690): Add new `Lint/UnneededRequireStatement` cop. ([@koic][])
* [#4813](https://github.com/rubocop/rubocop/pull/4813): Add new `Style/StderrPuts` cop. ([@koic][])
* [#4796](https://github.com/rubocop/rubocop/pull/4796): Add new `Lint/RedundantWithObject` cop. ([@koic][])
* [#4663](https://github.com/rubocop/rubocop/issues/4663): Add new `Style/CommentedKeyword` cop. ([@donjar][])
* Add `IndentationWidth` configuration for `Layout/Tab` cop. ([@rrosenblum][])
* [#4854](https://github.com/rubocop/rubocop/pull/4854): Add new `Lint/RegexpAsCondition` cop. ([@pocke][])
* [#4862](https://github.com/rubocop/rubocop/pull/4862): Add `MethodDefinitionMacros` option to `Naming/PredicateName` cop. ([@koic][])
* [#4874](https://github.com/rubocop/rubocop/pull/4874): Add new `Gemspec/OrderedDependencies` cop. ([@sue445][])
* [#4840](https://github.com/rubocop/rubocop/pull/4840): Add new `Style/MixinUsage` cop. ([@koic][])
* [#1952](https://github.com/rubocop/rubocop/issues/1952): Add new `Style/DateTime` cop. ([@dpostorivo][])
* [#4727](https://github.com/rubocop/rubocop/issues/4727): Make `Lint/Void` check for nonmutating methods as well. ([@donjar][])

### Bug fixes

* [#3312](https://github.com/rubocop/rubocop/issues/3312): Make `Rails/Date` Correct false positive on `#to_time` for strings ending in UTC-"Z". ([@erikdstock][])
* [#4741](https://github.com/rubocop/rubocop/issues/4741): Make `Style/SafeNavigation` correctly exclude methods called without dot. ([@drenmi][])
* [#4740](https://github.com/rubocop/rubocop/issues/4740): Make `Lint/RescueWithoutErrorClass` aware of modifier form `rescue`. ([@drenmi][])
* [#4745](https://github.com/rubocop/rubocop/issues/4745): Make `Style/SafeNavigation` ignore negated continuations. ([@drenmi][])
* [#4732](https://github.com/rubocop/rubocop/issues/4732): Prevent `Performance/HashEachMethods` from registering an offense when `#each` follows `#to_a`. ([@drenmi][])
* [#4730](https://github.com/rubocop/rubocop/issues/4730): False positive on Lint/InterpolationCheck. ([@koic][])
* [#4751](https://github.com/rubocop/rubocop/issues/4751): Prevent `Rails/HasManyOrHasOneDependent` cop from registering offense if `:through` option was specified. ([@smakagon][])
* [#4737](https://github.com/rubocop/rubocop/issues/4737): Fix ReturnInVoidContext cop when `return` is in top scope. ([@frodsan][])
* [#4776](https://github.com/rubocop/rubocop/issues/4776): Non utf-8 magic encoding comments are now respected. ([@deivid-rodriguez][])
* [#4241](https://github.com/rubocop/rubocop/issues/4241): Prevent `Rails/Blank` and `Rails/Present` from breaking when there is no explicit receiver. ([@rrosenblum][])
* [#4814](https://github.com/rubocop/rubocop/issues/4814): Prevent `Rails/Blank` from breaking on send with an argument. ([@pocke][])
* [#4759](https://github.com/rubocop/rubocop/issues/4759): Make `Naming/HeredocDelimiterNaming` and `Naming/HeredocDelimiterCase` aware of more delimiter patterns. ([@drenmi][])
* [#4823](https://github.com/rubocop/rubocop/issues/4823): Make `Lint/UnusedMethodArgument` and `Lint/UnusedBlockArgument` aware of overriding assignments. ([@akhramov][])
* [#4830](https://github.com/rubocop/rubocop/issues/4830): Prevent `Lint/BooleanSymbol` from truncating symbol's value in the message when offense is located in the new syntax hash. ([@akhramov][])
* [#4747](https://github.com/rubocop/rubocop/issues/4747): Fix `Rails/HasManyOrHasOneDependent` cop incorrectly flags `with_options` blocks. ([@koic][])
* [#4836](https://github.com/rubocop/rubocop/issues/4836): Make `Rails/OutputSafety` aware of safe navigation operator. ([@drenmi][])
* [#4843](https://github.com/rubocop/rubocop/issues/4843): Make `Lint/ShadowedException` cop aware of same system error code. ([@koic][])
* [#4757](https://github.com/rubocop/rubocop/issues/4757): Make `Style/TrailingUnderscoreVariable` work for nested assignments. ([@donjar][])
* [#4597](https://github.com/rubocop/rubocop/pull/4597): Fix `Style/StringLiterals` cop not registering an offense on single quoted strings containing an escaped single quote when configured to use double quotes. ([@promisedlandt][])
* [#4850](https://github.com/rubocop/rubocop/issues/4850): `Lint/UnusedMethodArgument` respects `IgnoreEmptyMethods` setting by ignoring unused method arguments for singleton methods. ([@jmks][])
* [#2040](https://github.com/rubocop/rubocop/issues/2040): Document how to write a custom cop. ([@jonatas][])

### Changes

* [#4746](https://github.com/rubocop/rubocop/pull/4746): The `Lint/InvalidCharacterLiteral` cop has been removed since it was never being actually triggered. ([@deivid-rodriguez][])
* [#4789](https://github.com/rubocop/rubocop/pull/4789): Analyzing code that needs to support MRI 1.9 is no longer supported. ([@deivid-rodriguez][])
* [#4582](https://github.com/rubocop/rubocop/issues/4582): `Severity` and other common parameters can be configured on department level. ([@jonas054][])
* [#4787](https://github.com/rubocop/rubocop/pull/4787): Analyzing code that needs to support MRI 2.0 is no longer supported. ([@deivid-rodriguez][])
* [#4787](https://github.com/rubocop/rubocop/pull/4787): RuboCop no longer installs on MRI 2.0. ([@deivid-rodriguez][])
* [#4266](https://github.com/rubocop/rubocop/issues/4266): Download the inherited config files of a remote file from the same remote. ([@tdeo][])
* [#4853](https://github.com/rubocop/rubocop/pull/4853): Make `Lint/LiteralInCondition` cop aware of `!` and `not`. ([@pocke][])
* [#4864](https://github.com/rubocop/rubocop/pull/4864): Rename `Lint/LiteralInCondition` to `Lint/LiteralAsCondition`. ([@pocke][])

## 0.50.0 (2017-09-14)

### New features

* [#4464](https://github.com/rubocop/rubocop/pull/4464): Add `EnforcedStyleForEmptyBraces` parameter to `Layout/SpaceBeforeBlockBraces` cop. ([@palkan][])
* [#4453](https://github.com/rubocop/rubocop/pull/4453): New cop `Style/RedundantConditional` checks for conditionals that return true/false. ([@petehamilton][])
* [#4448](https://github.com/rubocop/rubocop/pull/4448): Add new `TapFormatter`. ([@cyberdelia][])
* [#4467](https://github.com/rubocop/rubocop/pull/4467): Add new `Style/HeredocDelimiters` cop(Note: This cop was renamed to `Naming/HeredocDelimiterNaming`). ([@drenmi][])
* [#4153](https://github.com/rubocop/rubocop/issues/4153): New cop `Lint/ReturnInVoidContext` checks for the use of a return with a value in a context where it will be ignored. ([@harold-s][])
* [#4506](https://github.com/rubocop/rubocop/pull/4506): Add auto-correct support to `Lint/ScriptPermission`. ([@rrosenblum][])
* [#4514](https://github.com/rubocop/rubocop/pull/4514): Add configuration options to `Style/YodaCondition` to support checking all comparison operators or equality operators only. ([@smakagon][])
* [#4515](https://github.com/rubocop/rubocop/pull/4515): Add new `Lint/BooleanSymbol` cop. ([@droptheplot][])
* [#4535](https://github.com/rubocop/rubocop/pull/4535): Make `Rails/PluralizationGrammar` use singular methods for `-1` / `-1.0`. ([@promisedlandt][])
* [#4541](https://github.com/rubocop/rubocop/pull/4541): Add new `Rails/HasManyOrHasOneDependent` cop. ([@oboxodo][])
* [#4552](https://github.com/rubocop/rubocop/pull/4552): Add new `Style/Dir` cop. ([@drenmi][])
* [#4548](https://github.com/rubocop/rubocop/pull/4548): Add new `Style/HeredocDelimiterCase` cop(Note: This cop is renamed to `Naming/HeredocDelimiterCase`). ([@drenmi][])
* [#2943](https://github.com/rubocop/rubocop/pull/2943): Add new `Lint/RescueWithoutErrorClass` cop. ([@drenmi][])
* [#4568](https://github.com/rubocop/rubocop/pull/4568): Fix auto-correction for `Style/TrailingUnderscoreVariable`. ([@smakagon][])
* [#4586](https://github.com/rubocop/rubocop/pull/4586): Add new `Performance/UnfreezeString` cop. ([@pocke][])
* [#2976](https://github.com/rubocop/rubocop/issues/2976): Add `Whitelist` configuration option to `Style/NestedParenthesizedCalls` cop. ([@drenmi][])
* [#3965](https://github.com/rubocop/rubocop/issues/3965): Add new `Style/OrAssignment` cop. ([@donjar][])
* [#4655](https://github.com/rubocop/rubocop/pull/4655): Make `rake new_cop` create parent directories if they do not already exist. ([@highb][])
* [#4368](https://github.com/rubocop/rubocop/issues/4368): Make `Performance/HashEachMethod` inspect send nodes with any receiver. ([@gohdaniel15][])
* [#4508](https://github.com/rubocop/rubocop/issues/4508): Add new `Style/ReturnNil` cop. ([@donjar][])
* [#4629](https://github.com/rubocop/rubocop/issues/4629): Add Metrics/MethodLength cop for `define_method`. ([@jekuta][])
* [#4702](https://github.com/rubocop/rubocop/pull/4702): Add new `Lint/UriEscapeUnescape` cop. ([@koic][])
* [#4696](https://github.com/rubocop/rubocop/pull/4696): Add new `Performance/UriDefaultParser` cop. ([@koic][])
* [#4694](https://github.com/rubocop/rubocop/pull/4694): Add new `Lint/UriRegexp` cop. ([@koic][])
* [#4711](https://github.com/rubocop/rubocop/pull/4711): Add new `Style/MinMax` cop. ([@drenmi][])
* [#4720](https://github.com/rubocop/rubocop/pull/4720): Add new `Bundler/InsecureProtocolSource` cop. ([@koic][])
* [#4708](https://github.com/rubocop/rubocop/pull/4708): Add new `Lint/RedundantWithIndex` cop. ([@koic][])
* [#4480](https://github.com/rubocop/rubocop/pull/4480): Add new `Lint/InterpolationCheck` cop. ([@GauthamGoli][])
* [#4628](https://github.com/rubocop/rubocop/issues/4628): Add new `Lint/NestedPercentLiteral` cop. ([@asherkach][])

### Bug fixes

* [#4709](https://github.com/rubocop/rubocop/pull/4709): Use cached remote config on network failure. ([@kristjan][])
* [#4688](https://github.com/rubocop/rubocop/pull/4688): Accept yoda condition which isn't commutative. ([@fujimura][])
* [#4676](https://github.com/rubocop/rubocop/issues/4676): Make `Style/RedundantConditional` cop work with elsif. ([@akhramov][])
* [#4656](https://github.com/rubocop/rubocop/issues/4656): Modify `Style/ConditionalAssignment` auto-correction to work with unbracketed arrays. ([@akhramov][])
* [#4615](https://github.com/rubocop/rubocop/pull/4615): Don't consider `<=>` a comparison method. ([@iGEL][])
* [#4664](https://github.com/rubocop/rubocop/pull/4664): Fix typos in Rails/HttpPositionalArguments. ([@JoeCohen][])
* [#4618](https://github.com/rubocop/rubocop/pull/4618): Fix `Lint/FormatParameterMismatch` false positive if format string includes `%%5B` (CGI encoded left bracket). ([@barthez][])
* [#4604](https://github.com/rubocop/rubocop/pull/4604): Fix `Style/LambdaCall` to auto-correct `obj.call` to `obj.`. ([@iGEL][])
* [#4443](https://github.com/rubocop/rubocop/pull/4443): Prevent `Style/YodaCondition` from breaking `not LITERAL`. ([@pocke][])
* [#4434](https://github.com/rubocop/rubocop/issues/4434): Prevent bad auto-correct in `Style/Alias` for non-literal arguments. ([@drenmi][])
* [#4451](https://github.com/rubocop/rubocop/issues/4451): Make `Style/AndOr` cop aware of comparison methods. ([@drenmi][])
* [#4457](https://github.com/rubocop/rubocop/pull/4457): Fix false negative in `Lint/Void` with initialize and setter methods. ([@pocke][])
* [#4418](https://github.com/rubocop/rubocop/issues/4418): Register an offense in `Style/ConditionalAssignment` when the assignment line is the longest line, and it does not exceed the max line length. ([@rrosenblum][])
* [#4491](https://github.com/rubocop/rubocop/issues/4491): Prevent bad auto-correct in `Style/EmptyElse` for nested `if`. ([@pocke][])
* [#4485](https://github.com/rubocop/rubocop/pull/4485): Handle 304 status for remote config files. ([@daniloisr][])
* [#4529](https://github.com/rubocop/rubocop/pull/4529): Make `Lint/UnreachableCode` aware of `if` and `case`. ([@pocke][])
* [#4469](https://github.com/rubocop/rubocop/issues/4469): Include permissions in file cache. ([@pocke][])
* [#4270](https://github.com/rubocop/rubocop/issues/4270): Fix false positive in `Performance/RegexpMatch` for named captures. ([@pocke][])
* [#4525](https://github.com/rubocop/rubocop/pull/4525): Fix regexp for checking comment config of `rubocop:disable all` in `Lint/UnneededDisable`. ([@meganemura][])
* [#4555](https://github.com/rubocop/rubocop/issues/4555): Make `Style/VariableName` aware of optarg, kwarg and other arguments. ([@pocke][])
* [#4481](https://github.com/rubocop/rubocop/issues/4481): Prevent `Style/WordArray` and `Style/SymbolArray` from registering offenses where percent arrays don't work. ([@drenmi][])
* [#4447](https://github.com/rubocop/rubocop/issues/4447): Prevent `Layout/EmptyLineBetweenDefs` from removing too many lines. ([@drenmi][])
* [#3892](https://github.com/rubocop/rubocop/issues/3892): Make `Style/NumericPredicate` ignore numeric comparison of global variables. ([@drenmi][])
* [#4101](https://github.com/rubocop/rubocop/issues/4101): Skip auto-correct for literals with trailing comment and chained method call in `Layout/Multiline*BraceLayout`. ([@jonas054][])
* [#4518](https://github.com/rubocop/rubocop/issues/4518): Fix bug where `Style/SafeNavigation` does not register an offense when there are chained method calls. ([@rrosenblum][])
* [#3040](https://github.com/rubocop/rubocop/issues/3040): Ignore safe navigation in `Rails/Delegate`. ([@cgriego][])
* [#4587](https://github.com/rubocop/rubocop/pull/4587): Fix false negative for void unary operators in `Lint/Void` cop. ([@pocke][])
* [#4589](https://github.com/rubocop/rubocop/issues/4589): Fix false positive in `Performance/RegexpMatch` cop for `=~` is in a class method. ([@pocke][])
* [#4578](https://github.com/rubocop/rubocop/issues/4578): Fix false positive in `Lint/FormatParameterMismatch` for format with "asterisk" (`*`) width and precision. ([@smakagon][])
* [#4285](https://github.com/rubocop/rubocop/issues/4285): Make `Lint/DefEndAlignment` aware of multiple modifiers. ([@drenmi][])
* [#4634](https://github.com/rubocop/rubocop/issues/4634): Handle heredoc that contains empty lines only in `Layout/IndentHeredoc` cop. ([@pocke][])
* [#4646](https://github.com/rubocop/rubocop/issues/4646): Make `Lint/Debugger` aware of `Kernel` and cbase. ([@pocke][])
* [#4643](https://github.com/rubocop/rubocop/issues/4643): Modify `Style/InverseMethods` to not register a separate offense for an inverse method nested inside of the block of an inverse method offense. ([@rrosenblum][])
* [#4593](https://github.com/rubocop/rubocop/issues/4593): Fix false positive in `Rails/SaveBang` when `save/update_attribute` is used with a `case` statement. ([@theRealNG][])
* [#4322](https://github.com/rubocop/rubocop/issues/4322): Fix Style/MultilineMemoization from auto-correcting to invalid ruby. ([@dpostorivo][])
* [#4722](https://github.com/rubocop/rubocop/pull/4722): Fix `rake new_cop` problem that doesn't add `require` line. ([@koic][])
* [#4723](https://github.com/rubocop/rubocop/issues/4723): Fix `RaiseArgs` auto-correction issue for `raise` with 3 arguments. ([@smakagon][])

### Changes

* [#4470](https://github.com/rubocop/rubocop/issues/4470): Improve the error message for `Lint/AssignmentInCondition`. ([@brandonweiss][])
* [#4553](https://github.com/rubocop/rubocop/issues/4553): Add `node_modules` to default excludes. ([@iainbeeston][])
* [#4445](https://github.com/rubocop/rubocop/pull/4445): Make `Style/Encoding` cop enabled by default. ([@deivid-rodriguez][])
* [#4452](https://github.com/rubocop/rubocop/pull/4452): Add option to `Rails/Delegate` for enforcing the prefixed method name case. ([@klesse413][])
* [#4493](https://github.com/rubocop/rubocop/pull/4493): Make `Lint/Void` cop aware of `Enumerable#each` and `for`. ([@pocke][])
* [#4492](https://github.com/rubocop/rubocop/pull/4492): Make `Lint/DuplicateMethods` aware of `alias` and `alias_method`. ([@pocke][])
* [#4478](https://github.com/rubocop/rubocop/issues/4478): Fix confusing message of `Performance/Caller` cop. ([@pocke][])
* [#4543](https://github.com/rubocop/rubocop/pull/4543): Make `Lint/DuplicateMethods` aware of `attr_*` methods. ([@pocke][])
* [#4550](https://github.com/rubocop/rubocop/pull/4550): Mark `RuboCop::CLI#run` as a public API. ([@yujinakayama][])
* [#4551](https://github.com/rubocop/rubocop/pull/4551): Make `Performance/Caller` aware of `caller_locations`. ([@pocke][])
* [#4547](https://github.com/rubocop/rubocop/pull/4547): Rename `Style/HeredocDelimiters` to `Style/HeredocDelimiterNaming`. ([@drenmi][])
* [#4157](https://github.com/rubocop/rubocop/issues/4157): Enhance offense message for `Style/RedundantReturn` cop. ([@gohdaniel15][])
* [#4521](https://github.com/rubocop/rubocop/issues/4521): Move naming related cops into their own `Naming` department. ([@drenmi][])
* [#4600](https://github.com/rubocop/rubocop/pull/4600): Make `Style/RedundantSelf` aware of arguments of a block. ([@Envek][])
* [#4658](https://github.com/rubocop/rubocop/issues/4658): Disable auto-correction for `Performance/TimesMap` by default. ([@Envek][])

## 0.49.1 (2017-05-29)

### Bug fixes

* [#4411](https://github.com/rubocop/rubocop/issues/4411): Handle properly safe navigation in `Style/YodaCondition`. ([@bbatsov][])
* [#4412](https://github.com/rubocop/rubocop/issues/4412): Handle properly literal comparisons in `Style/YodaCondition`. ([@bbatsov][])
* Handle properly class variables and global variables in `Style/YodaCondition`. ([@bbatsov][])
* [#4392](https://github.com/rubocop/rubocop/issues/4392): Fix the auto-correct of `Style/Next` when the `end` is misaligned. ([@rrosenblum][])
* [#4407](https://github.com/rubocop/rubocop/issues/4407): Prevent `Performance/RegexpMatch` from blowing up on `match` without arguments. ([@pocke][])
* [#4414](https://github.com/rubocop/rubocop/issues/4414): Handle pseudo-assignments in `for` loops in `Style/ConditionalAssignment`. ([@bbatsov][])
* [#4419](https://github.com/rubocop/rubocop/issues/4419): Handle combination `AllCops: DisabledByDefault: true` and `Rails: Enabled: true`. ([@jonas054][])
* [#4422](https://github.com/rubocop/rubocop/issues/4422): Fix missing space in message for `Style/MultipleComparison`. ([@timrogers][])
* [#4420](https://github.com/rubocop/rubocop/issues/4420): Ensure `Style/EmptyMethod` honours indentation when auto-correcting. ([@drenmi][])
* [#4442](https://github.com/rubocop/rubocop/pull/4442): Prevent `Style/WordArray` from breaking on strings that aren't valid UTF-8. ([@pocke][])
* [#4441](https://github.com/rubocop/rubocop/pull/4441): Prevent `Layout/SpaceAroundBlockParameters` from breaking on lambda. ([@pocke][])

### Changes

* [#4436](https://github.com/rubocop/rubocop/pull/4436): Display 'Running parallel inspection' only with --debug. ([@pocke][])

## 0.49.0 (2017-05-24)

### New features

* [#117](https://github.com/rubocop/rubocop/issues/117): Add `--parallel` option for running RuboCop in multiple processes or threads. ([@jonas054][])
* Add auto-correct support to `Style/MixinGrouping`. ([@rrosenblum][])
* [#4236](https://github.com/rubocop/rubocop/issues/4236): Add new `Rails/ApplicationJob` and `Rails/ApplicationRecord` cops. ([@tjwp][])
* [#4078](https://github.com/rubocop/rubocop/pull/4078): Add new `Performance/Caller` cop. ([@alpaca-tc][])
* [#4314](https://github.com/rubocop/rubocop/pull/4314): Check slow hash accessing in `Array#sort` by `Performance/CompareWithBlock`. ([@pocke][])
* [#3438](https://github.com/rubocop/rubocop/issues/3438): Add new `Style/FormatStringToken` cop. ([@backus][])
* [#4342](https://github.com/rubocop/rubocop/pull/4342): Add new `Lint/ScriptPermission` cop. ([@yhirano55][])
* [#4145](https://github.com/rubocop/rubocop/issues/4145): Add new `Style/YodaCondition` cop. ([@smakagon][])
* [#4403](https://github.com/rubocop/rubocop/pull/4403): Add public API `Cop.autocorrect_incompatible_with` for specifying other cops that should not auto-correct together. ([@backus][])
* [#4354](https://github.com/rubocop/rubocop/pull/4354): Add auto-correct to `Style/FormatString`. ([@hoshinotsuyoshi][])
* [#4021](https://github.com/rubocop/rubocop/pull/4021): Add new `Style/MultipleComparison` cop. ([@dabroz][])
* New `Lint/RescueType` cop. ([@rrosenblum][])
* [#4328](https://github.com/rubocop/rubocop/issues/4328): Add `--ignore-parent-exclusion` flag to ignore AllCops/Exclude inheritance. ([@nelsonjr][])

### Changes

* [#4262](https://github.com/rubocop/rubocop/pull/4262): Add new `MinSize` configuration to `Style/SymbolArray`, consistent with the same configuration in `Style/WordArray`. ([@scottmatthewman][])
* [#3400](https://github.com/rubocop/rubocop/issues/3400): Remove auto-correct support from Lint/Debugger. ([@ilansh][])
* [#4278](https://github.com/rubocop/rubocop/pull/4278): Move all cops dealing with whitespace into a new department called `Layout`. ([@jonas054][])
* [#4320](https://github.com/rubocop/rubocop/pull/4320): Update `Rails/OutputSafety` to disallow wrapping `raw` or `html_safe` with `safe_join`. ([@klesse413][])
* [#4336](https://github.com/rubocop/rubocop/issues/4336): Store `rubocop_cache` in safer directories. ([@jonas054][])
* [#4361](https://github.com/rubocop/rubocop/pull/4361): Use relative path for offense message in `Lint/DuplicateMethods`. ([@pocke][])
* [#4385](https://github.com/rubocop/rubocop/pull/4385): Include `.jb` file by default. ([@pocke][])

### Bug fixes

* [#4265](https://github.com/rubocop/rubocop/pull/4265): Require a space before first argument of a method call in `Style/SpaceBeforeFirstArg` cop. ([@cjlarose][])
* [#4237](https://github.com/rubocop/rubocop/pull/4237): Fix false positive in `Lint/AmbiguousBlockAssociation` cop for lambdas. ([@smakagon][])
* [#4242](https://github.com/rubocop/rubocop/issues/4242): Add `Capfile` to the list of known Ruby filenames. ([@bbatsov][])
* [#4240](https://github.com/rubocop/rubocop/issues/4240): Handle `||=` in `Rails/RelativeDateConstant`. ([@bbatsov][])
* [#4241](https://github.com/rubocop/rubocop/issues/4241): Prevent `Rails/Blank` and `Rails/Present` from breaking when there is no explicit receiver. ([@rrosenblum][])
* [#4249](https://github.com/rubocop/rubocop/issues/4249): Handle multiple assignment in `Rails/RelativeDateConstant`. ([@bbatsov][])
* [#4250](https://github.com/rubocop/rubocop/issues/4250): Improve a bit the Ruby code detection config. ([@bbatsov][])
* [#4283](https://github.com/rubocop/rubocop/issues/4283): Fix `Style/EmptyCaseCondition` auto-correct bug - when first `when` branch includes comma-delimited alternatives. ([@ilansh][])
* [#4268](https://github.com/rubocop/rubocop/issues/4268): Handle end-of-line comments when auto-correcting Style/EmptyLinesAroundAccessModifier. ([@vergenzt][])
* [#4275](https://github.com/rubocop/rubocop/issues/4275): Prevent `Style/MethodCallWithArgsParentheses` from blowing up on `yield`. ([@drenmi][])
* [#3969](https://github.com/rubocop/rubocop/issues/3969): Handle multiline method call alignment for arguments to methods. ([@jonas054][])
* [#4304](https://github.com/rubocop/rubocop/pull/4304): Allow enabling whole departments when `DisabledByDefault` is `true`. ([@jonas054][])
* [#4264](https://github.com/rubocop/rubocop/issues/4264): Prevent `Rails/SaveBang` from blowing up when using the assigned variable in a hash. ([@drenmi][])
* [#4310](https://github.com/rubocop/rubocop/pull/4310): Treat paths containing invalid byte sequences as non-matches. ([@mclark][])
* [#4063](https://github.com/rubocop/rubocop/issues/4063): Fix Rails/ReversibleMigration misdetection. ([@gprado][])
* [#4339](https://github.com/rubocop/rubocop/pull/4339): Fix false positive in `Security/Eval` cop for multiline string literal. ([@pocke][])
* [#4339](https://github.com/rubocop/rubocop/pull/4339): Fix false negative in `Security/Eval` cop for `Binding#eval`. ([@pocke][])
* [#4327](https://github.com/rubocop/rubocop/issues/4327): Prevent `Layout/SpaceInsidePercentLiteralDelimiters` from registering offenses on execute-strings. ([@drenmi][])
* [#4371](https://github.com/rubocop/rubocop/issues/4371): Prevent `Style/MethodName` from complaining about unary operator definitions. ([@drenmi][])
* [#4366](https://github.com/rubocop/rubocop/issues/4366): Prevent `Performance/RedundantMerge` from blowing up on double splat arguments. ([@drenmi][])
* [#4352](https://github.com/rubocop/rubocop/issues/4352): Fix the auto-correct of `Style/AndOr` when Enumerable accessors (`[]`) are used. ([@rrosenblum][])
* [#4393](https://github.com/rubocop/rubocop/issues/4393): Prevent `Style/InverseMethods` from registering an offense for methods that are double negated. ([@rrosenblum][])
* [#4394](https://github.com/rubocop/rubocop/issues/4394): Prevent some cops from breaking on safe navigation operator. ([@drenmi][])
* [#4260](https://github.com/rubocop/rubocop/issues/4260): Prevent `Rails/SkipsModelValidations` from registering an offense for `FileUtils.touch`. ([@rrosenblum][])

## 0.48.1 (2017-04-03)

### Changes

* [#4219](https://github.com/rubocop/rubocop/issues/4219): Add a link to style guide for `Style/IndentationConsistency` cop. ([@pocke][])
* [#4168](https://github.com/rubocop/rubocop/issues/4168): Removed `-n` option. ([@sadovnik][])
* [#4039](https://github.com/rubocop/rubocop/pull/4039): Change `Style/PercentLiteralDelimiters` default configuration to match Style Guide update. ([@drenmi][])
* [#4235](https://github.com/rubocop/rubocop/pull/4235): Improved copy of offense message in `Lint/AmbiguousBlockAssociation` cop. ([@smakagon][])

### Bug fixes

* [#4171](https://github.com/rubocop/rubocop/pull/4171): Prevent `Rails/Blank` from breaking when RHS of `or` is a naked falsiness check. ([@drenmi][])
* [#4189](https://github.com/rubocop/rubocop/pull/4189): Make `Lint/AmbiguousBlockAssociation` aware of lambdas passed as arguments. ([@drenmi][])
* [#4179](https://github.com/rubocop/rubocop/pull/4179): Prevent `Rails/Blank` from breaking when LHS of `or` is a naked falsiness check. ([@rrosenblum][])
* [#4172](https://github.com/rubocop/rubocop/pull/4172): Fix false positives in `Style/MixinGrouping` cop. ([@drenmi][])
* [#4185](https://github.com/rubocop/rubocop/pull/4185): Make `Lint/NestedMethodDefinition` aware of `#*_exec` class of methods. ([@drenmi][])
* [#4197](https://github.com/rubocop/rubocop/pull/4197): Fix false positive in `Style/RedundantSelf` cop with parallel assignment. ([@drenmi][])
* [#4199](https://github.com/rubocop/rubocop/issues/4199): Fix incorrect auto correction in `Style/SymbolArray` and `Style/WordArray` cop. ([@pocke][])
* [#4218](https://github.com/rubocop/rubocop/pull/4218): Make `Lint/NestedMethodDefinition` aware of class shovel scope. ([@drenmi][])
* [#4198](https://github.com/rubocop/rubocop/pull/4198): Make `Lint/AmbiguousBlockAssociation` aware of operator methods. ([@drenmi][])
* [#4152](https://github.com/rubocop/rubocop/pull/4152): Make `Style/MethodCallWithArgsParentheses` not require parens on setter methods. ([@drenmi][])
* [#4226](https://github.com/rubocop/rubocop/pull/4226): Show in `--help` output that `--stdin` takes a file name argument. ([@jonas054][])
* [#4217](https://github.com/rubocop/rubocop/pull/4217): Fix false positive in `Rails/FilePath` cop with non string argument. ([@soutaro][])
* [#4106](https://github.com/rubocop/rubocop/pull/4106): Make `Style/TernaryParentheses` unsafe auto-correct detector aware of literals and constants. ([@drenmi][])
* [#4228](https://github.com/rubocop/rubocop/pull/4228): Fix false positive in `Lint/AmbiguousBlockAssociation` cop. ([@smakagon][])
* [#4234](https://github.com/rubocop/rubocop/pull/4234): Fix false positive in `Rails/RelativeDate` for lambdas and procs. ([@smakagon][])

## 0.48.0 (2017-03-26)

### New features

* [#4107](https://github.com/rubocop/rubocop/pull/4107): New `TargetRailsVersion` configuration parameter can be used to specify which version of Rails the inspected code is intended to run on. ([@maxbeizer][])
* [#4104](https://github.com/rubocop/rubocop/pull/4104): Add `prefix` and `postfix` styles to `Style/NegatedIf`. ([@brandonweiss][])
* [#4083](https://github.com/rubocop/rubocop/pull/4083): Add new configuration `NumberOfEmptyLines` for `Style/EmptyLineBetweenDefs`. ([@dorian][])
* [#4045](https://github.com/rubocop/rubocop/pull/4045): Add new configuration `Strict` for `Style/NumericLiteral` to make the change to this cop in 0.47.0 configurable. ([@iGEL][])
* [#4005](https://github.com/rubocop/rubocop/issues/4005): Add new `AllCops/EnabledByDefault` option. ([@betesh][])
* [#3893](https://github.com/rubocop/rubocop/issues/3893): Add a new configuration, `IncludeActiveSupportAliases`, to `Performance/DoubleStartEndWith`. This configuration will check for ActiveSupport's `starts_with?` and `ends_with?`. ([@rrosenblum][])
* [#3889](https://github.com/rubocop/rubocop/pull/3889): Add new `Style/EmptyLineAfterMagicComment` cop. ([@backus][])
* [#3800](https://github.com/rubocop/rubocop/issues/3800): Make `Style/EndOfLine` configurable with `lf`, `crlf`, and `native` (default) styles. ([@jonas054][])
* [#3936](https://github.com/rubocop/rubocop/issues/3936): Add new `Style/MixinGrouping` cop. ([@drenmi][])
* [#4003](https://github.com/rubocop/rubocop/issues/4003): Add new `Rails/RelativeDateConstant` cop. ([@sinsoku][])
* [#3984](https://github.com/rubocop/rubocop/pull/3984): Add new `Style/EmptyLinesAroundBeginBody` cop. ([@pocke][])
* [#3995](https://github.com/rubocop/rubocop/pull/3995): Add new `Style/EmptyLinesAroundExceptionHandlingKeywords` cop. ([@pocke][])
* [#4019](https://github.com/rubocop/rubocop/pull/4019): Make configurable `Style/MultilineMemoization` cop. ([@pocke][])
* [#4018](https://github.com/rubocop/rubocop/pull/4018): Add auto-correct `Lint/EmptyEnsure` cop. ([@pocke][])
* [#4028](https://github.com/rubocop/rubocop/pull/4028): Add new `Style/IndentHeredoc` cop. ([@pocke][])
* [#3931](https://github.com/rubocop/rubocop/issues/3931): Add new `Lint/AmbiguousBlockAssociation` cop. ([@smakagon][])
* Add new `Style/InverseMethods` cop. ([@rrosenblum][])
* [#4038](https://github.com/rubocop/rubocop/pull/4038): Allow `default` key in the `Style/PercentLiteralDelimiters` cop config to set all preferred delimiters. ([@kddeisz][])
* Add `IgnoreMacros` option to `Style/MethodCallWithArgsParentheses`. ([@drenmi][])
* [#3937](https://github.com/rubocop/rubocop/issues/3937): Add new `Rails/ActiveSupportAliases` cop. ([@tdeo][])
* Add new `Rails/Blank` cop. ([@rrosenblum][])
* Add new `Rails/Present` cop. ([@rrosenblum][])
* [#4004](https://github.com/rubocop/rubocop/issues/4004): Allow not treating comment lines as group separators in `Bundler/OrderedGems` cop. ([@konto-andrzeja][])

### Changes

* [#4100](https://github.com/rubocop/rubocop/issues/4100): Rails/SaveBang should flag `update_attributes`. ([@andriymosin][])
* [#4083](https://github.com/rubocop/rubocop/pull/4083): `Style/EmptyLineBetweenDefs` doesn't allow more than one empty line between method definitions by default (see `NumberOfEmptyLines`). ([@dorian][])
* [#3997](https://github.com/rubocop/rubocop/pull/3997): Include all ruby files by default and exclude non-ruby files. ([@dorian][])
* [#4012](https://github.com/rubocop/rubocop/pull/4012): Mark `foo[:bar]` as not complex in `Style/TernaryParentheses` cop with `require_parentheses_when_complex` style. ([@onk][])
* [#3915](https://github.com/rubocop/rubocop/issues/3915): Make configurable whitelist for `Lint/SafeNavigationChain` cop. ([@pocke][])
* [#3944](https://github.com/rubocop/rubocop/issues/3944): Allow keyword arguments in `Style/RaiseArgs` cop. ([@mikegee][])
* Add auto-correct to `Performance/DoubleStartEndWith`. ([@rrosenblum][])
* [#3951](https://github.com/rubocop/rubocop/pull/3951): Make `Rails/Date` cop to register an offence for a string without timezone. ([@sinsoku][])
* [#4020](https://github.com/rubocop/rubocop/pull/4020): Fixed `new_cop.rake` suggested path. ([@dabroz][])
* [#4055](https://github.com/rubocop/rubocop/pull/4055): Add parameters count to offense message for `Metrics/ParameterLists` cop. ([@pocke][])
* [#4081](https://github.com/rubocop/rubocop/pull/4081): Allow `Marshal.load` if argument is a `Marshal.dump` in `Security/MarshalLoad` cop. ([@droptheplot][])
* [#4124](https://github.com/rubocop/rubocop/issues/4124): Make `Style/SymbolArray` cop to enable by default. ([@pocke][])
* [#3331](https://github.com/rubocop/rubocop/issues/3331): Change `Style/MultilineMethodCallIndentation` `indented_relative_to_receiver` to indent relative to the receiver and not relative to the caller. ([@jfelchner][])
* [#4137](https://github.com/rubocop/rubocop/pull/4137): Allow lines to be exempted from `IndentationWidth` by regex. ([@jfelchner][])

### Bug fixes

* [#4007](https://github.com/rubocop/rubocop/pull/4007): Skip `Rails/SkipsModelValidations` for methods that don't accept arguments. ([@dorian][])
* [#3923](https://github.com/rubocop/rubocop/issues/3923): Allow asciibetical sorting in `Bundler/OrderedGems`. ([@mikegee][])
* [#3855](https://github.com/rubocop/rubocop/issues/3855): Make `Lint/NonLocalExitFromIterator` aware of method definitions. ([@drenmi][])
* [#2643](https://github.com/rubocop/rubocop/issues/2643): Allow uppercase and dashes in `MagicComment`. ([@mikegee][])
* [#3959](https://github.com/rubocop/rubocop/issues/3959): Don't wrap "percent arrays" with extra brackets when auto-correcting `Style/MutableConstant`. ([@mikegee][])
* [#3978](https://github.com/rubocop/rubocop/pull/3978): Fix false positive in `Performance/RegexpMatch` with `English` module. ([@pocke][])
* [#3242](https://github.com/rubocop/rubocop/issues/3242): Ignore `Errno::ENOENT` during cache cleanup from `File.mtime` too. ([@mikegee][])
* [#3958](https://github.com/rubocop/rubocop/issues/3958): `Style/SpaceInsideHashLiteralBraces` doesn't add and offence when checking an hash where a value is a left brace string (e.g. { k: '{' }). ([@nodo][])
* [#4006](https://github.com/rubocop/rubocop/issues/4006): Prevent `Style/WhileUntilModifier` from breaking on a multiline modifier. ([@drenmi][])
* [#3345](https://github.com/rubocop/rubocop/issues/3345): Allow `Style/WordArray`'s `WordRegex` configuration value to be an instance of `String`. ([@mikegee][])
* [#4013](https://github.com/rubocop/rubocop/pull/4013): Follow redirects for RemoteConfig. ([@buenaventure][])
* [#3917](https://github.com/rubocop/rubocop/issues/3917): Rails/FilePath Match nodes in a method call only once. ([@unmanbearpig][])
* [#3673](https://github.com/rubocop/rubocop/issues/3673): Fix regression on `Style/RedundantSelf` when assigning to same local variable. ([@bankair][])
* [#4047](https://github.com/rubocop/rubocop/issues/4047): Allow `find_zone` and `find_zone!` methods in `Rails/TimeZone`. ([@attilahorvath][])
* [#3457](https://github.com/rubocop/rubocop/issues/3457): Clear a warning and prevent new warnings. ([@mikegee][])
* [#4066](https://github.com/rubocop/rubocop/issues/4066): Register an offense in `Lint/ShadowedException` when an exception is shadowed and there is an implicit begin. ([@rrosenblum][])
* [#4001](https://github.com/rubocop/rubocop/issues/4001): Lint/UnneededDisable of Metrics/LineLength that isn't unneeded. ([@wkurniawan07][])
* [#3960](https://github.com/rubocop/rubocop/issues/3960): Let `Include`/`Exclude` paths in all files beginning with `.rubocop` be relative to the configuration file's directory and not to the current directory. ([@jonas054][])
* [#4049](https://github.com/rubocop/rubocop/pull/4049): Bugfix for `Style/EmptyLiteral` cop. ([@ota42y][])
* [#4112](https://github.com/rubocop/rubocop/pull/4112): Fix false positives about double quotes in `Style/StringLiterals`, `Style/UnneededCapitalW` and `Style/UnneededPercentQ` cops. ([@pocke][])
* [#4109](https://github.com/rubocop/rubocop/issues/4109): Fix incorrect auto correction in `Style/SelfAssignment` cop. ([@pocke][])
* [#4110](https://github.com/rubocop/rubocop/issues/4110): Fix incorrect auto correction in `Style/BracesAroundHashParameters` cop. ([@musialik][])
* [#4084](https://github.com/rubocop/rubocop/issues/4084): Fix incorrect auto correction in `Style/TernaryParentheses` cop. ([@musialik][])
* [#4102](https://github.com/rubocop/rubocop/issues/4102): Fix `Security/JSONLoad`, `Security/MarshalLoad` and `Security/YAMLLoad` cops patterns not matching ::Const. ([@musialik][])
* [#3580](https://github.com/rubocop/rubocop/issues/3580): Handle combinations of `# rubocop:disable all` and `# rubocop:disable SomeCop`. ([@jonas054][])
* [#4124](https://github.com/rubocop/rubocop/issues/4124): Fix auto correction bugs in `Style/SymbolArray` cop. ([@pocke][])
* [#4128](https://github.com/rubocop/rubocop/issues/4128): Prevent `Style/CaseIndentation` cop from registering offenses on single-line case statements. ([@drenmi][])
* [#4143](https://github.com/rubocop/rubocop/issues/4143): Prevent `Style/IdenticalConditionalBranches` from registering offenses when a case statement has an empty when. ([@dpostorivo][])
* [#4160](https://github.com/rubocop/rubocop/pull/4160): Fix a regression where `UselessAssignment` cop may not properly detect useless assignments when there's only a single conditional expression in the top level scope. ([@yujinakayama][])
* [#4162](https://github.com/rubocop/rubocop/pull/4162): Fix a false negative in `UselessAssignment` cop with nested conditionals. ([@yujinakayama][])

## 0.47.1 (2017-01-18)

### Bug fixes

* [#3911](https://github.com/rubocop/rubocop/issues/3911): Prevent a crash in `Performance/RegexpMatch` cop with module definition. ([@pocke][])
* [#3908](https://github.com/rubocop/rubocop/issues/3908): Prevent `Style/AlignHash` from breaking on a keyword splat when using enforced `table` style. ([@drenmi][])
* [#3918](https://github.com/rubocop/rubocop/issues/3918): Prevent `Rails/EnumUniqueness` from breaking on a non-literal hash value. ([@drenmi][])
* [#3914](https://github.com/rubocop/rubocop/pull/3914): Fix department resolution for third party cops required through configuration. ([@backus][])
* [#3846](https://github.com/rubocop/rubocop/issues/3846): `NodePattern` works for hyphenated node types. ([@alexdowad][])
* [#3922](https://github.com/rubocop/rubocop/issues/3922): Prevent `Style/NegatedIf` from breaking on negated ternary. ([@drenmi][])
* [#3915](https://github.com/rubocop/rubocop/issues/3915): Fix a false positive in `Lint/SafeNavigationChain` cop with `try` method. ([@pocke][])

## 0.47.0 (2017-01-16)

### New features

* [#3822](https://github.com/rubocop/rubocop/pull/3822): Add `Rails/FilePath` cop. ([@iguchi1124][])
* [#3821](https://github.com/rubocop/rubocop/pull/3821): Add `Security/YAMLLoad` cop. ([@cyberdelia][])
* [#3816](https://github.com/rubocop/rubocop/pull/3816): Add `Security/MarshalLoad` cop. ([@cyberdelia][])
* [#3757](https://github.com/rubocop/rubocop/pull/3757): Add Auto-Correct for `Bundler/OrderedGems` cop. ([@pocke][])
* `Style/FrozenStringLiteralComment` now supports the style `never` that will remove the `frozen_string_literal` comment. ([@rrosenblum][])
* [#3795](https://github.com/rubocop/rubocop/pull/3795): Add `Lint/MultipleCompare` cop. ([@pocke][])
* [#3772](https://github.com/rubocop/rubocop/issues/3772): Allow exclusion of certain methods for `Metrics/BlockLength`. ([@NobodysNightmare][])
* [#3804](https://github.com/rubocop/rubocop/pull/3804): Add new `Lint/SafeNavigationChain` cop. ([@pocke][])
* [#3670](https://github.com/rubocop/rubocop/pull/3670): Add `CountBlocks` boolean option to `Metrics/BlockNesting`. It allows blocks to be counted towards the nesting limit. ([@georgyangelov][])
* [#2992](https://github.com/rubocop/rubocop/issues/2992): Add a configuration to `Style/ConditionalAssignment` to toggle offenses for ternary expressions. ([@rrosenblum][])
* [#3824](https://github.com/rubocop/rubocop/pull/3824): Add new `Performance/RegexpMatch` cop. ([@pocke][])
* [#3825](https://github.com/rubocop/rubocop/pull/3825): Add new `Rails/SkipsModelValidations` cop. ([@rahulcs][])
* [#3737](https://github.com/rubocop/rubocop/issues/3737): Add new `Style/MethodCallWithArgsParentheses` cop. ([@dominh][])
* Renamed `MethodCallParentheses` to `MethodCallWithoutArgsParentheses`. ([@dominh][])
* [#3854](https://github.com/rubocop/rubocop/pull/3854): Add new `Rails/ReversibleMigration` cop. ([@sue445][])
* [#3872](https://github.com/rubocop/rubocop/pull/3872): Detect `String#%` with hash literal. ([@backus][])
* [#2731](https://github.com/rubocop/rubocop/issues/2731): Allow configuration of method calls that create methods for `Lint/UselessAccessModifier`. ([@pat][])

### Changes

* [#3820](https://github.com/rubocop/rubocop/pull/3820): Rename `Lint/Eval` to `Security/Eval`. ([@cyberdelia][])
* [#3725](https://github.com/rubocop/rubocop/issues/3725): Disable `Style/SingleLineBlockParams` by default. ([@tejasbubane][])
* [#3765](https://github.com/rubocop/rubocop/pull/3765): Add a validation for supported styles other than EnforcedStyle. `AlignWith`, `IndentWhenRelativeTo` and `EnforcedMode` configurations are renamed. ([@pocke][])
* [#3782](https://github.com/rubocop/rubocop/pull/3782): Add check for `add_reference` method by `Rails/NotNullColumn` cop. ([@pocke][])
* [#3761](https://github.com/rubocop/rubocop/pull/3761): Update `Style/RedundantFreeze` message from `Freezing immutable objects is pointless.` to `Do not freeze immutable objects, as freezing them has no effect.`. ([@lucasuyezu][])
* [#3753](https://github.com/rubocop/rubocop/issues/3753): Change error message of `Bundler/OrderedGems` to mention `Alphabetize Gems`. ([@tejasbubane][])
* [#3802](https://github.com/rubocop/rubocop/pull/3802): Ignore case when checking Gemfile order. ([@breckenedge][])
* Add missing examples in `Lint` cops documentation. ([@enriikke][])
* Make `Style/EmptyMethod` cop aware of class methods. ([@drenmi][])
* [#3871](https://github.com/rubocop/rubocop/pull/3871): Add check for void `defined?` and `self` by `Lint/Void` cop. ([@pocke][])
* Allow ignoring methods in `Style/BlockDelimiters` when using any style. ([@twe4ked][])

### Bug fixes

* [#3751](https://github.com/rubocop/rubocop/pull/3751): Avoid crash in `Rails/EnumUniqueness` cop. ([@pocke][])
* [#3766](https://github.com/rubocop/rubocop/pull/3766): Avoid crash in `Style/ConditionalAssignment` cop with masgn. ([@pocke][])
* [#3770](https://github.com/rubocop/rubocop/pull/3770): `Style/RedundantParentheses` Don't flag raised to a power negative numeric literals, since removing the parentheses would change the meaning of the expressions. ([@amogil][])
* [#3750](https://github.com/rubocop/rubocop/issues/3750): Register an offense in `Style/ConditionalAssignment` when the assignment spans multiple lines. ([@rrosenblum][])
* [#3775](https://github.com/rubocop/rubocop/pull/3775): Avoid crash in `Style/HashSyntax` cop with an empty hash. ([@pocke][])
* [#3783](https://github.com/rubocop/rubocop/pull/3783): Maintain parentheses in `Rails/HttpPositionalArguments` when methods are defined with them. ([@kevindew][])
* [#3786](https://github.com/rubocop/rubocop/pull/3786): Avoid crash `Style/ConditionalAssignment` cop with mass assign method. ([@pocke][])
* [#3749](https://github.com/rubocop/rubocop/pull/3749): Detect corner case of `Style/NumericLiterals`. ([@kamaradclimber][])
* [#3788](https://github.com/rubocop/rubocop/pull/3788): Prevent bad auto-correct in `Style/Next` when block has nested conditionals. ([@drenmi][])
* [#3807](https://github.com/rubocop/rubocop/pull/3807): Prevent `Style/Documentation` and `Style/DocumentationMethod` from mistaking RuboCop directives for class documentation. ([@drenmi][])
* [#3815](https://github.com/rubocop/rubocop/pull/3815): Fix false positive in `Style/IdenticalConditionalBranches` cop when branches have same line at leading. ([@pocke][])
* Fix false negative in `Rails/HttpPositionalArguments` where offense would go undetected if one of the request parameter names matched one of the special keyword arguments. ([@deivid-rodriguez][])
* Fix false negative in `Rails/HttpPositionalArguments` where offense would go undetected if the `:format` keyword was used with other non-special keywords. ([@deivid-rodriguez][])
* [#3406](https://github.com/rubocop/rubocop/issues/3406): Enable cops if Enabled is not explicitly set to false. ([@metcalf][])
* Fix `Lint/FormatParameterMismatch` for splatted last argument. ([@zverok][])
* [#3853](https://github.com/rubocop/rubocop/pull/3853): Fix false positive in `RedundantParentheses` cop with multiple expression. ([@pocke][])
* [#3870](https://github.com/rubocop/rubocop/pull/3870): Avoid crash in `Rails/HttpPositionalArguments`. ([@pocke][])
* [#3869](https://github.com/rubocop/rubocop/pull/3869): Prevent `Lint/FormatParameterMismatch` from breaking when `#%` is passed an empty array. ([@drenmi][])
* [#3879](https://github.com/rubocop/rubocop/pull/3879): Properly handle Emacs and Vim magic comments for `FrozenStringLiteralComment`. ([@backus][])
* [#3736](https://github.com/rubocop/rubocop/issues/3736): Fix to remove accumulator return value by auto-correction in `Style/EachWithObject`. ([@pocke][])

## 0.46.0 (2016-11-30)

### New features

* [#3600](https://github.com/rubocop/rubocop/issues/3600): Add new `Bundler/DuplicatedGem` cop. ([@jmks][])
* [#3624](https://github.com/rubocop/rubocop/pull/3624): Add new configuration option `empty_lines_special` to `Style/EmptyLinesAroundClassBody` and `Style/EmptyLinesAroundModuleBody`. ([@legendetm][])
* Add new `Style/EmptyMethod` cop. ([@drenmi][])
* `Style/EmptyLiteral` will now auto-correct `Hash.new` when it is the first argument being passed to a method. The arguments will be wrapped with parenthesis. ([@rrosenblum][])
* [#3713](https://github.com/rubocop/rubocop/pull/3713): Respect `DisabledByDefault` in parent configs. ([@aroben][])
* New cop `Rails/EnumUniqueness` checks for duplicate values defined in enum config. ([@olliebennett][])
* New cop `Rails/EnumUniqueness` checks for duplicate values defined in enum config hash. ([@olliebennett][])
* [#3451](https://github.com/rubocop/rubocop/issues/3451): Add new `require_parentheses_when_complex` style to `Style/TernaryParentheses` cop. ([@swcraig][])
* [#3600](https://github.com/rubocop/rubocop/issues/3600): Add new `Bundler/OrderedGems` cop. ([@tdeo][])
* [#3479](https://github.com/rubocop/rubocop/issues/3479): Add new configuration option `IgnoredPatterns` to `Metrics/LineLength`. ([@jonas054][])

### Changes

* The offense range for `Performance/FlatMap` now includes any parameters that are passed to `flatten`. ([@rrosenblum][])
* [#1747](https://github.com/rubocop/rubocop/issues/1747): Update `Style/SpecialGlobalVars` messages with a reminder to `require 'English'`. ([@ivanovaleksey][])
* Checks `binding.irb` call by `Lint/Debugger` cop. ([@pocke][])
* [#3742](https://github.com/rubocop/rubocop/pull/3742): Checks `min` and `max` call by `Performance/CompareWithBlock` cop. ([@pocke][])

### Bug fixes

* [#3662](https://github.com/rubocop/rubocop/issues/3662): Fix the auto-correction of `Lint/UnneededSplatExpansion` when the splat expansion is inside of another array. ([@rrosenblum][])
* [#3699](https://github.com/rubocop/rubocop/issues/3699): Fix false positive in `Style/VariableNumber` on variable names ending with an underscore. ([@bquorning][])
* [#3687](https://github.com/rubocop/rubocop/issues/3687): Fix the fact that `Style/TernaryParentheses` cop claims to correct uncorrected offenses. ([@Ana06][])
* [#3568](https://github.com/rubocop/rubocop/issues/3568): Fix `--auto-gen-config` behavior for `Style/VariableNumber`. ([@jonas054][])
* Add `format` as an acceptable keyword argument for `Rails/HttpPositionalArguments`. ([@aesthetikx][])
* [#3598](https://github.com/rubocop/rubocop/issues/3598): In `Style/NumericPredicate`, don't report `x != 0` or `x.nonzero?` as the expressions have different values. ([@jonas054][])
* [#3690](https://github.com/rubocop/rubocop/issues/3690): Do not register an offense for multiline braces with content in `Style/SpaceInsideBlockBraces`. ([@rrosenblum][])
* [#3746](https://github.com/rubocop/rubocop/issues/3746): `Lint/NonLocalExitFromIterator` does not warn about `return` in a block which is passed to `Object#define_singleton_method`. ([@AlexWayfer][])

## 0.45.0 (2016-10-31)

### New features

* [#3615](https://github.com/rubocop/rubocop/pull/3615): Add auto-correction for `Lint/EmptyInterpolation`. ([@pocke][])
* Make `PercentLiteralDelimiters` enforce delimiters around `%I()` too. ([@bronson][])
* [#3408](https://github.com/rubocop/rubocop/issues/3408): Add check for repeated values in case conditionals. ([@swcraig][])
* [#3646](https://github.com/rubocop/rubocop/pull/3646): Add new `Lint/EmptyWhen` cop. ([@drenmi][])
* [#3246](https://github.com/rubocop/rubocop/issues/3246): Add list of all cops to the manual (generated automatically from a rake task). ([@sihu][])
* [#3647](https://github.com/rubocop/rubocop/issues/3647): Add `--force-default-config` option. ([@jawshooah][])
* [#3570](https://github.com/rubocop/rubocop/issues/3570): Add new `MultilineIfModifier` cop to avoid usage of if/unless-modifiers on multiline statements. ([@tessi][])
* [#3631](https://github.com/rubocop/rubocop/issues/3631): Add new `Style/SpaceInLambdaLiteral` cop to check for spaces in lambda literals. ([@swcraig][])
* Add new `Lint/EmptyExpression` cop. ([@drenmi][])

### Bug fixes

* [#3553](https://github.com/rubocop/rubocop/pull/3553): Make `Style/RedundantSelf` cop to not register an offence for `self.()`. ([@iGEL][])
* [#3474](https://github.com/rubocop/rubocop/issues/3474): Make the `Rails/TimeZone` only analyze functions which have "Time" in the receiver. ([@b-t-g][])
* [#3607](https://github.com/rubocop/rubocop/pull/3607): Fix `Style/RedundantReturn` cop for empty if body. ([@pocke][])
* [#3291](https://github.com/rubocop/rubocop/issues/3291): Improve detection of `raw` and `html_safe` methods in `Rails/OutputSafety`. ([@lumeet][])
* Redundant return style now properly handles empty `when` blocks. ([@albus522][])
* [#3622](https://github.com/rubocop/rubocop/pull/3622): Fix false positive for `Metrics/MethodLength` and `Metrics/BlockLength`. ([@meganemura][])
* [#3625](https://github.com/rubocop/rubocop/pull/3625): Fix some cops errors when condition is empty brace. ([@pocke][])
* [#3468](https://github.com/rubocop/rubocop/issues/3468): Fix bug regarding alignment inside `begin`..`end` block in `Style/MultilineMethodCallIndentation`. ([@jonas054][])
* [#3644](https://github.com/rubocop/rubocop/pull/3644): Fix generation incorrect documentation. ([@pocke][])
* [#3637](https://github.com/rubocop/rubocop/issues/3637): Fix Style/NonNilCheck crashing for ternary condition. ([@tejasbubane][])
* [#3654](https://github.com/rubocop/rubocop/pull/3654): Add missing keywords for `Rails/HttpPositionalArguments`. ([@eitoball][])
* [#3652](https://github.com/rubocop/rubocop/issues/3652): Avoid crash Rails/HttpPositionalArguments for lvar params when auto-correct. ([@pocke][])
* Fix bug in `Style/SafeNavigation` where there is a check for an object in an elsif statement with a method call on that object in the branch. ([@rrosenblum][])
* [#3660](https://github.com/rubocop/rubocop/pull/3660): Fix false positive for Rails/SafeNavigation when without receiver. ([@pocke][])
* [#3650](https://github.com/rubocop/rubocop/issues/3650): Fix `Style/VariableNumber` registering an offense for variables with double digit numbers. ([@rrosenblum][])
* [#3494](https://github.com/rubocop/rubocop/issues/3494): Check `rails` style indentation also inside blocks in `Style/IndentationWidth`. ([@jonas054][])
* [#3676](https://github.com/rubocop/rubocop/issues/3676): Ignore raw and html_safe invocations when wrapped inside a safe_join. ([@b-t-g][])

### Changes

* [#3601](https://github.com/rubocop/rubocop/pull/3601): Change default args for `Style/SingleLineBlockParams`. This cop checks that `reduce` and `inject` use the variable names `a` and `e` for block arguments. These defaults are uncommunicative variable names and thus conflict with the ["Uncommunicative Variable Name" check in Reek](https://github.com/troessner/reek/blob/master/docs/Uncommunicative-Variable-Name.md). Default args changed to `acc` and `elem`. ([@jessieay][])
* [#3645](https://github.com/rubocop/rubocop/pull/3645): Fix bug with empty case when nodes in `Style/RedundantReturn`. ([@tiagocasanovapt][])
* [#3263](https://github.com/rubocop/rubocop/issues/3263): Fix auto-correct of if statements inside of unless else statements in `Style/ConditionalAssignment`. ([@rrosenblum][])
* Bump default Ruby version to 2.1. ([@drenmi][])

## 0.44.1 (2016-10-13)

### Bug fixes

* Remove a debug `require`. ([@bbatsov][])

## 0.44.0 (2016-10-13)

### New features

* [#3560](https://github.com/rubocop/rubocop/pull/3560): Add a configuration option `empty_lines_except_namespace` to `Style/EmptyLinesAroundClassBody` and `Style/EmptyLinesAroundModuleBody`. ([@legendetm][])
* [#3370](https://github.com/rubocop/rubocop/issues/3370): Add new `Rails/HttpPositionalArguments` cop to check your Rails 5 test code for existence of positional args usage. ([@logicminds][])
* [#3510](https://github.com/rubocop/rubocop/issues/3510): Add a configuration option, `ConvertCodeThatCanStartToReturnNil`, to `Style/SafeNavigation` to check for code that could start returning `nil` if safe navigation is used. ([@rrosenblum][])
* Add a new `AllCops/StyleGuideBaseURL` setting that allows the use of relative paths and/or fragments within each cop's `StyleGuide` setting, to make forking of custom style guides easier. ([@scottmatthewman][])
* [#3566](https://github.com/rubocop/rubocop/issues/3566): Add new `Metric/BlockLength` cop to ensure blocks don't get too long. ([@savef][])
* [#3428](https://github.com/rubocop/rubocop/issues/3428): Add support for configuring `Style/PreferredHashMethods` with either `short` or `verbose` style method names. ([@abrom][])
* [#3455](https://github.com/rubocop/rubocop/issues/3455): Add new `Rails/DynamicFindBy` cop. ([@pocke][])
* [#3542](https://github.com/rubocop/rubocop/issues/3542): Add a configuration option, `IgnoreCopDirectives`, to `Metrics/LineLength` to stop cop directives (`# rubocop:disable Metrics/AbcSize`) from being counted when considering line length. ([@jmks][])
* Add new `Rails/DelegateAllowBlank` cop. ([@connorjacobsen][])
* Add new `Style/MultilineMemoization` cop. ([@drenmi][])

### Bug fixes

* [#3103](https://github.com/rubocop/rubocop/pull/3103): Make `Style/ExtraSpacing` cop register an offense for extra spaces present in single-line hash literals. ([@tcdowney][])
* [#3513](https://github.com/rubocop/rubocop/pull/3513): Fix false positive in `Style/TernaryParentheses` for a ternary with ranges. ([@dreyks][])
* [#3520](https://github.com/rubocop/rubocop/issues/3520): Fix regression causing `Lint/AssignmentInCondition` false positive. ([@savef][])
* [#3514](https://github.com/rubocop/rubocop/issues/3514): Make `Style/VariableNumber` cop not register an offense when valid normal case variable names have an integer after the first `_`. ([@b-t-g][])
* [#3516](https://github.com/rubocop/rubocop/issues/3516): Make `Style/VariableNumber` cop not register an offense when valid normal case variable names have an integer in the middle. ([@b-t-g][])
* [#3436](https://github.com/rubocop/rubocop/issues/3436): Make `Rails/SaveBang` cop not register an offense when return value of a non-bang method is returned by the parent method. ([@coorasse][])
* [#3540](https://github.com/rubocop/rubocop/issues/3540): Fix `Style/GuardClause` to register offense for instance and singleton methods. ([@tejasbubane][])
* [#3311](https://github.com/rubocop/rubocop/issues/3311): Detect incompatibilities with the external encoding to prevent bad auto-corrections in `Style/StringLiterals`. ([@deivid-rodriguez][])
* [#3499](https://github.com/rubocop/rubocop/issues/3499): Ensure `Lint/UnusedBlockArgument` doesn't make recommendations that would change arity for methods defined using `#define_method`. ([@drenmi][])
* [#3430](https://github.com/rubocop/rubocop/issues/3430): Fix exception in `Performance/RedundantMerge` when inspecting a `#merge!` with implicit receiver. ([@drenmi][])
* [#3411](https://github.com/rubocop/rubocop/issues/3411): Avoid auto-correction crash for single `when` in `Performance/CaseWhenSplat`. ([@jonas054][])
* [#3286](https://github.com/rubocop/rubocop/issues/3286): Allow `self.a, self.b = b, a` in `Style/ParallelAssignment`. ([@jonas054][])
* [#3419](https://github.com/rubocop/rubocop/issues/3419): Report offense for `unless x.nil?` in `Style/NonNilCheck` if `IncludeSemanticChanges` is `true`. ([@jonas054][])
* [#3382](https://github.com/rubocop/rubocop/issues/3382): Avoid auto-correction crash for multiple elsifs in `Style/EmptyElse`. ([@lumeet][])
* [#3334](https://github.com/rubocop/rubocop/issues/3334): Do not register an offense for a literal space (`\s`) in `Style/UnneededCapitalW`. ([@rrosenblum][])
* [#3390](https://github.com/rubocop/rubocop/issues/3390): Fix SaveBang cop for multiple conditional. ([@tejasbubane][])
* [#3577](https://github.com/rubocop/rubocop/issues/3577): Fix `Style/RaiseArgs` not allowing compact raise with splatted args. ([@savef][])
* [#3578](https://github.com/rubocop/rubocop/issues/3578): Fix safe navigation method call counting in `Metrics/AbcSize`. ([@savef][])
* [#3592](https://github.com/rubocop/rubocop/issues/3592): Fix `Style/RedundantParentheses` for indexing with literals. ([@thegedge][])
* [#3597](https://github.com/rubocop/rubocop/issues/3597): Fix the auto-correct of `Performance/CaseWhenSplat` when trying to rearrange splat expanded variables to the end of a when condition. ([@rrosenblum][])

### Changes

* [#3512](https://github.com/rubocop/rubocop/issues/3512): Change error message of `Lint/UnneededSplatExpansion` for array in method parameters. ([@tejasbubane][])
* [#3510](https://github.com/rubocop/rubocop/issues/3510): Fix some issues with `Style/SafeNavigation`. Fix auto-correct of multiline if expressions, and do not register an offense for scenarios using `||` and ternary expression. ([@rrosenblum][])
* [#3503](https://github.com/rubocop/rubocop/issues/3503): Change misleading message of `Style/EmptyLinesAroundAccessModifier`. ([@bquorning][])
* [#3407](https://github.com/rubocop/rubocop/issues/3407): Turn off auto-correct for unsafe rules by default. ([@ptarjan][])
* [#3521](https://github.com/rubocop/rubocop/issues/3521): Turn off auto-correct for `Security/JSONLoad` by default. ([@savef][])
* [#2903](https://github.com/rubocop/rubocop/issues/2903): `Style/RedundantReturn` looks for redundant `return` inside conditional branches. ([@lumeet][])

## 0.43.0 (2016-09-19)

### New features

* [#3379](https://github.com/rubocop/rubocop/issues/3379): Add table of contents at the beginning of HTML formatted output. ([@hedgesky][])
* [#2968](https://github.com/rubocop/rubocop/issues/2968): Add new `Style/DocumentationMethod` cop. ([@sooyang][])
* [#3360](https://github.com/rubocop/rubocop/issues/3360): Add `RequireForNonPublicMethods` configuration option to `Style/DocumentationMethod` cop. ([@drenmi][])
* Add new `Rails/SafeNavigation` cop to convert `try!` to `&.`. ([@rrosenblum][])
* [#3415](https://github.com/rubocop/rubocop/pull/3415): Add new `Rails/NotNullColumn` cop. ([@pocke][])
* [#3167](https://github.com/rubocop/rubocop/issues/3167): Add new `Style/VariableNumber` cop. ([@sooyang][])
* Add new style `no_mixed_keys` to `Style/HashSyntax` to only check for hashes with mixed keys. ([@daviddavis][])
* Allow including multiple configuration files from a single gem. ([@tjwallace][])
* Add check for `persisted?` method call when using a create method in `Rails/SaveBang`. ([@QuinnHarris][])
* Add new `Style/SafeNavigation` cop to convert method calls safeguarded by a non `nil` check for the object to `&.`. ([@rrosenblum][])
* Add new `Performance/SortWithBlock` cop to use `sort_by(&:foo)` instead of `sort { |a, b| a.foo <=> b.foo }`. ([@koic][])
* [#3492](https://github.com/rubocop/rubocop/pull/3492): Add new `UnifiedInteger` cop. ([@pocke][])

### Bug fixes

* [#3383](https://github.com/rubocop/rubocop/issues/3383): Fix the local variable reset issue with `Style/RedundantSelf` cop. ([@bankair][])
* [#3445](https://github.com/rubocop/rubocop/issues/3445): Fix bad auto-correct for `Style/AndOr` cop. ([@mikezter][])
* [#3349](https://github.com/rubocop/rubocop/issues/3349): Fix bad auto-correct for `Style/Lambda` cop. ([@metcalf][])
* [#3351](https://github.com/rubocop/rubocop/issues/3351): Fix bad auto-correct for `Performance/RedundantMatch` cop. ([@annaswims][])
* [#3347](https://github.com/rubocop/rubocop/issues/3347): Prevent infinite loop in `Style/TernaryParentheses` cop when used together with `Style/RedundantParentheses`. ([@drenmi][])
* [#3209](https://github.com/rubocop/rubocop/issues/3209): Remove faulty line length check from `Style/GuardClause` cop. ([@drenmi][])
* [#3366](https://github.com/rubocop/rubocop/issues/3366): Make `Style/MutableConstant` cop aware of splat assignments. ([@drenmi][])
* [#3372](https://github.com/rubocop/rubocop/pull/3372): Fix RuboCop crash with empty brackets in `Style/Next` cop. ([@pocke][])
* [#3358](https://github.com/rubocop/rubocop/issues/3358): Make `Style/MethodMissing` cop aware of class scope. ([@drenmi][])
* [#3342](https://github.com/rubocop/rubocop/issues/3342): Fix error in `Lint/ShadowedException` cop if last rescue does not have parameter. ([@soutaro][])
* [#3380](https://github.com/rubocop/rubocop/issues/3380): Fix false positive in `Style/TrailingUnderscoreVariable` cop. ([@drenmi][])
* [#3388](https://github.com/rubocop/rubocop/issues/3388): Fix bug where `Lint/ShadowedException` would register an offense when rescuing different numbers of custom exceptions in multiple rescue groups. ([@rrosenblum][])
* [#3386](https://github.com/rubocop/rubocop/issues/3386): Make `VariableForce` understand an empty RegExp literal as LHS to `=~`. ([@drenmi][])
* [#3421](https://github.com/rubocop/rubocop/pull/3421): Fix clobbering `inherit_from` additions when not using Namespaces in the configs. ([@nicklamuro][])
* [#3425](https://github.com/rubocop/rubocop/pull/3425): Fix bug for invalid bytes in UTF-8 in `Lint/PercentStringArray` cop. ([@pocke][])
* [#3374](https://github.com/rubocop/rubocop/issues/3374): Make `SpaceInsideBlockBraces` and `SpaceBeforeBlockBraces` not depend on `BlockDelimiters` configuration. ([@jonas054][])
* Fix error in `Lint/ShadowedException` cop for higher number of rescue groups. ([@groddeck][])
* [#3456](https://github.com/rubocop/rubocop/pull/3456): Don't crash on a multiline empty brace in `Style/MultilineMethodCallBraceLayout`. ([@pocke][])
* [#3423](https://github.com/rubocop/rubocop/issues/3423): Checks if .rubocop is a file before parsing. ([@joejuzl][])
* [#3439](https://github.com/rubocop/rubocop/issues/3439): Fix variable assignment check not working properly when a block is used in `Rails/SaveBang`. ([@QuinnHarris][])
* [#3401](https://github.com/rubocop/rubocop/issues/3401): Read file contents in binary mode so `Style/EndOfLine` works on Windows. ([@jonas054][])
* [#3450](https://github.com/rubocop/rubocop/issues/3450): Prevent `Style/TernaryParentheses` cop from making unsafe corrections. ([@drenmi][])
* [#3460](https://github.com/rubocop/rubocop/issues/3460): Fix false positives in `Style/InlineComment` cop. ([@drenmi][])
* [#3485](https://github.com/rubocop/rubocop/issues/3485): Make OneLineConditional cop not register offense for empty else. ([@tejasbubane][])
* [#3508](https://github.com/rubocop/rubocop/pull/3508): Fix false negatives in `Rails/NotNullColumn`. ([@pocke][])
* [#3462](https://github.com/rubocop/rubocop/issues/3462): Don't create MultilineMethodCallBraceLayout offenses for single-line method calls when receiver spans multiple lines. ([@maxjacobson][])

### Changes

* [#3341](https://github.com/rubocop/rubocop/issues/3341): Exclude RSpec tests from inspection by `Style/NumericPredicate` cop. ([@drenmi][])
* Rename `Lint/UselessArraySplat` to `Lint/UnneededSplatExpansion`, and add functionality to check for unnecessary expansion of other literals. ([@rrosenblum][])
* No longer register an offense for splat expansion of an array literal in `Performance/CaseWhenSplat`. `Lint/UnneededSplatExpansion` now handles this behavior. ([@rrosenblum][])
* `Lint/InheritException` restricts inheriting from standard library subclasses of `Exception`. ([@metcalf][])
* No longer register an offense if the first line of code starts with `#\` in `Style/LeadingCommentSpace`. `config.ru` files consider such lines as options. ([@scottohara][])
* [#3292](https://github.com/rubocop/rubocop/issues/3292): Remove `Performance/PushSplat` as it can produce code that is slower or even cause failure. ([@jonas054][])

## 0.42.0 (2016-07-25)

### New features

* [#3306](https://github.com/rubocop/rubocop/issues/3306): Add auto-correction for `Style/EachWithObject`. ([@owst][])
* Add new `Style/TernaryParentheses` cop. ([@drenmi][])
* [#3136](https://github.com/rubocop/rubocop/issues/3136): Add config for `UselessAccessModifier` so it can be made aware of ActiveSupport's `concerning` and `class_methods` methods. ([@maxjacobson][])
* [#3128](https://github.com/rubocop/rubocop/issues/3128): Add new `Rails/SaveBang` cop. ([@QuinnHarris][])
* Add new `Style/NumericPredicate` cop. ([@drenmi][])

### Bug fixes

* [#3271](https://github.com/rubocop/rubocop/issues/3271): Fix bad auto-correct for `Style/EachForSimpleLoop` cop. ([@drenmi][])
* [#3288](https://github.com/rubocop/rubocop/issues/3288): Fix auto-correct of word and symbol arrays in `Style/ParallelAssignment` cop. ([@jonas054][])
* [#3307](https://github.com/rubocop/rubocop/issues/3307): Fix exception when inspecting an operator assignment with `Style/MethodCallParentheses` cop. ([@drenmi][])
* [#3316](https://github.com/rubocop/rubocop/issues/3316): Fix error for blocks without arguments in `Style/SingleLineBlockParams` cop. ([@owst][])
* [#3320](https://github.com/rubocop/rubocop/issues/3320): Make `Style/OpMethod` aware of the backtick method. ([@drenmi][])
* Do not register an offense in `Lint/ShadowedException` when rescuing an exception built into Ruby before a custom exception. ([@rrosenblum][])

### Changes

* [#2645](https://github.com/rubocop/rubocop/issues/2645): `Style/EmptyLiteral` no longer generates an offense for `String.new` when using frozen string literals. ([@drenmi][])
* [#3308](https://github.com/rubocop/rubocop/issues/3308): Make `Lint/NextWithoutAccumulator` aware of nested enumeration. ([@drenmi][])
* Extend `Style/MethodMissing` cop to check for the conditions in the style guide. ([@drenmi][])
* [#3325](https://github.com/rubocop/rubocop/issues/3325): Drop support for MRI 1.9.3. ([@drenmi][])
* Add support for MRI 2.4. ([@dvandersluis][])
* [#3256](https://github.com/rubocop/rubocop/issues/3256): Highlight the closing brace in `Style/Multiline...BraceLayout` cops. ([@jonas054][])
* Always register an offense when rescuing `Exception` before or along with any other exception in `Lint/ShadowedException`. ([@rrosenblum][])

## 0.41.2 (2016-07-07)

### Bug fixes

* [#3248](https://github.com/rubocop/rubocop/issues/3248): Support 'ruby-' prefix in `.ruby-version`. ([@tjwp][])
* [#3250](https://github.com/rubocop/rubocop/pull/3250): Make regexp for cop names less restrictive in CommentConfig lines. ([@tjwp][])
* [#3261](https://github.com/rubocop/rubocop/pull/3261): Prefer `TargetRubyVersion` to `.ruby-version`. ([@tjwp][])
* [#3249](https://github.com/rubocop/rubocop/issues/3249): Account for `rescue nil` in `Style/ShadowedException`. ([@rrosenblum][])
* Modify the highlighting in `Style/ShadowedException` to be more useful. Highlight just `rescue` area. ([@rrosenblum][])
* [#3129](https://github.com/rubocop/rubocop/issues/3129): Fix `Style/MethodCallParentheses` to work with multiple assignments. ([@tejasbubane][])
* [#3247](https://github.com/rubocop/rubocop/issues/3247): Ensure whitespace after beginning of block in `Style/BlockDelimiters`. ([@tjwp][])
* [#2941](https://github.com/rubocop/rubocop/issues/2941): Make sure `Lint/UnneededDisable` can do auto-correction. ([@jonas054][])
* [#3269](https://github.com/rubocop/rubocop/pull/3269):  Fix `Lint/ShadowedException` to block arbitrary code execution. ([@pocke][])
* [#3266](https://github.com/rubocop/rubocop/issues/3266): Handle empty parentheses in `Performance/RedundantBlockCall` auto-correct. ([@jonas054][])
* [#3272](https://github.com/rubocop/rubocop/issues/3272): Add escape character missing to LITERAL_REGEX. ([@pocke][])
* [#3255](https://github.com/rubocop/rubocop/issues/3255): Fix auto-correct for `Style/RaiseArgs` when constructing exception without arguments. ([@drenmi][])
* [#3294](https://github.com/rubocop/rubocop/pull/3294): Allow to use `Time.zone_default`. ([@Tei][])
* [#3300](https://github.com/rubocop/rubocop/issues/3300): Do not replace `%q()`s containing escaped non-backslashes. ([@owst][])

### Changes

* [#3230](https://github.com/rubocop/rubocop/issues/3230): Improve highlighting for `Style/AsciiComments` cop. ([@drenmi][])
* Improve highlighting for `Style/AsciiIdentifiers` cop. ([@drenmi][])
* [#3265](https://github.com/rubocop/rubocop/issues/3265): Include --no-offense-counts in .rubocop_todo.yml. ([@vergenzt][])

## 0.41.1 (2016-06-26)

### Bug fixes

* [#3245](https://github.com/rubocop/rubocop/pull/3245): Fix `UniqBeforePluck` cop by solving difference of config name. ([@pocke][])

## 0.41.0 (2016-06-25)

### New features

* [#2956](https://github.com/rubocop/rubocop/issues/2956): Prefer `.ruby-version` to `TargetRubyVersion`. ([@pclalv][])
* [#3095](https://github.com/rubocop/rubocop/issues/3095): Add `IndentationWidth` configuration parameter for `Style/AlignParameters` cop. ([@alexdowad][])
* [#3066](https://github.com/rubocop/rubocop/issues/3066): Add new `Style/ImplicitRuntimeError` cop which advises the use of an explicit exception class when raising an error. ([@alexdowad][])
* [#3018](https://github.com/rubocop/rubocop/issues/3018): Add new `Style/EachForSimpleLoop` cop which advises the use of `Integer#times` for simple loops which iterate a fixed number of times. ([@alexdowad][])
* [#2595](https://github.com/rubocop/rubocop/issues/2595): New `compact` style for `Style/SpaceInsideLiteralHashBraces`. ([@alexdowad][])
* [#2927](https://github.com/rubocop/rubocop/issues/2927): Add auto-correct for `Rails/Validation` cop. ([@neodelf][])
* [#3135](https://github.com/rubocop/rubocop/pull/3135): Add new `Rails/OutputSafety` cop. ([@josh][])
* [#3164](https://github.com/rubocop/rubocop/pull/3164): Add [Fastlane](https://fastlane.tools/)'s Fastfile to the default Includes. ([@jules2689][])
* [#3173](https://github.com/rubocop/rubocop/pull/3173): Make `Style/ModuleFunction` configurable with `module_function` and `extend_self` styles. ([@tjwp][])
* [#3105](https://github.com/rubocop/rubocop/issues/3105): Add new `Rails/RequestReferrer` cop. ([@giannileggio][])
* [#3200](https://github.com/rubocop/rubocop/pull/3200): Add auto-correct for `Style/EachForSimpleLoop` cop. ([@tejasbubane][])
* [#3058](https://github.com/rubocop/rubocop/issues/3058): Add new `Style/SpaceInsideArrayPercentLiteral` cop. ([@owst][])
* [#3058](https://github.com/rubocop/rubocop/issues/3058): Add new `Style/SpaceInsidePercentLiteralDelimiters` cop. ([@owst][])
* [#3179](https://github.com/rubocop/rubocop/pull/3179): Expose files to support testings Cops using RSpec. ([@tjwp][])
* [#3191](https://github.com/rubocop/rubocop/issues/3191): Allow arbitrary comments after cop names in CommentConfig lines (e.g. rubocop:enable). ([@owst][])
* [#3165](https://github.com/rubocop/rubocop/pull/3165): Add new `Lint/PercentStringArray` cop. ([@owst][])
* [#3165](https://github.com/rubocop/rubocop/pull/3165): Add new `Lint/PercentSymbolArray` cop. ([@owst][])
* [#3177](https://github.com/rubocop/rubocop/pull/3177): Add new `Style/NumericLiteralPrefix` cop. ([@tejasbubane][])
* [#1646](https://github.com/rubocop/rubocop/issues/1646): Add configuration style `indented_relative_to_receiver` for `Style/MultilineMethodCallIndentation`. ([@jonas054][])
* New cop `Lint/ShadowedException` checks for the order which exceptions are rescued to avoid rescuing a less specific exception before a more specific exception. ([@rrosenblum][])
* [#3127](https://github.com/rubocop/rubocop/pull/3127): New cop `Lint/InheritException` checks for error classes inheriting from `Exception`, and instead suggests `RuntimeError` or `StandardError`. ([@drenmi][])
* Add new `Performance/PushSplat` cop. ([@segiddins][])
* [#3089](https://github.com/rubocop/rubocop/issues/3089): Add new `Rails/Exit` cop. ([@sgringwe][])
* [#3104](https://github.com/rubocop/rubocop/issues/3104): Add new `Style/MethodMissing` cop. ([@haziqhafizuddin][])

### Bug fixes

* [#3005](https://github.com/rubocop/rubocop/issues/3005): Symlink protection prevents use of caching in CI context. ([@urbanautomaton][])
* [#3037](https://github.com/rubocop/rubocop/issues/3037): `Style/StringLiterals` understands that a bare '#', not '#@variable' or '#{interpolation}', does not require double quotes. ([@alexdowad][])
* [#2722](https://github.com/rubocop/rubocop/issues/2722): `Style/ExtraSpacing` does not attempt to align an equals sign in an argument list with one in an assignment statement. ([@alexdowad][])
* [#3133](https://github.com/rubocop/rubocop/issues/3133): `Style/MultilineMethodCallBraceLayout` does not register offenses for single-line calls. ([@alexdowad][])
* [#3170](https://github.com/rubocop/rubocop/issues/3170): `Style/MutableConstant` does not infinite-loop when correcting an array with no brackets. ([@alexdowad][])
* [#3150](https://github.com/rubocop/rubocop/issues/3150): Fix auto-correct for Style/MultilineArrayBraceLayout. ([@jspanjers][])
* [#3192](https://github.com/rubocop/rubocop/pull/3192): Fix `Lint/UnusedBlockArgument`'s `IgnoreEmptyBlocks` parameter from being removed from configuration. ([@jfelchner][])
* [#3114](https://github.com/rubocop/rubocop/issues/3114): Fix alignment `end` when auto-correcting `Style/EmptyElse`. ([@rrosenblum][])
* [#3120](https://github.com/rubocop/rubocop/issues/3120): Fix `Lint/UselessAccessModifier` reporting useless access modifiers inside {Class,Module,Struct}.new blocks. ([@owst][])
* [#3125](https://github.com/rubocop/rubocop/issues/3125): Fix `Rails/UniqBeforePluck` to ignore `uniq` with block. ([@tejasbubane][])
* [#3116](https://github.com/rubocop/rubocop/issues/3116): `Style/SpaceAroundKeyword` allows `&.` method calls after `super` and `yield`. ([@segiddins][])
* [#3131](https://github.com/rubocop/rubocop/issues/3131): Fix `Style/ZeroLengthPredicate` to ignore `size` and `length` variables. ([@tejasbubane][])
* [#3146](https://github.com/rubocop/rubocop/pull/3146): Fix `NegatedIf` and `NegatedWhile` to ignore double negations. ([@natalzia-paperless][])
* [#3140](https://github.com/rubocop/rubocop/pull/3140): `Style/FrozenStringLiteralComment` works with file doesn't have any tokens. ([@pocke][])
* [#3154](https://github.com/rubocop/rubocop/issues/3154): Fix handling of `()` in `Style/RedundantParentheses`. ([@lumeet][])
* [#3155](https://github.com/rubocop/rubocop/issues/3155): Fix `Style/SpaceAfterNot` reporting on the `not` keyword. ([@NobodysNightmare][])
* [#3160](https://github.com/rubocop/rubocop/pull/3160): `Style/Lambda` fix whitespacing when auto-correcting unparenthesized arguments. ([@palkan][])
* [#2944](https://github.com/rubocop/rubocop/issues/2944): Don't crash on strings that span multiple lines but only have one pair of delimiters in `Style/StringLiterals`. ([@jonas054][])
* [#3157](https://github.com/rubocop/rubocop/issues/3157): Don't let `LineEndConcatenation` and `UnneededInterpolation` make changes to the same string during auto-correct. ([@jonas054][])
* [#3187](https://github.com/rubocop/rubocop/issues/3187): Let `Style/BlockDelimiters` ignore blocks in *all* method arguments. ([@jonas054][])
* Modify `Style/ParallelAssignment` to use implicit begins when parallel assignment uses a `rescue` modifier and is the only thing in the method. ([@rrosenblum][])
* [#3217](https://github.com/rubocop/rubocop/pull/3217): Fix output of ellipses for multi-line offense ranges in HTML formatter. ([@jonas054][])
* [#3207](https://github.com/rubocop/rubocop/issues/3207): Auto-correct modifier `while`/`until` and `begin`..`end` + `while`/`until` in `Style/InfiniteLoop`. ([@jonas054][])
* [#3202](https://github.com/rubocop/rubocop/issues/3202): Fix `Style/EmptyElse` registering wrong offenses and thus making RuboCop crash. ([@deivid-rodriguez][])
* [#3183](https://github.com/rubocop/rubocop/issues/3183): Ensure `Style/SpaceInsideBlockBraces` reports offenses for multi-line blocks. ([@owst][])
* [#3017](https://github.com/rubocop/rubocop/issues/3017): Fix `Style/StringLiterals` to register offenses on non-ascii strings. ([@deivid-rodriguez][])
* [#3056](https://github.com/rubocop/rubocop/issues/3056): Fix `Style/StringLiterals` to register offenses on non-ascii strings. ([@deivid-rodriguez][])
* [#2986](https://github.com/rubocop/rubocop/issues/2986): Fix `RedundantBlockCall` to not report calls that pass block arguments, or where the block has been overridden. ([@owst][])
* [#3223](https://github.com/rubocop/rubocop/issues/3223): Return can take many arguments. ([@ptarjan][])
* [#3239](https://github.com/rubocop/rubocop/pull/3239): Fix bug with --auto-gen-config and a file that does not exist. ([@meganemura][])
* [#3138](https://github.com/rubocop/rubocop/issues/3138): Fix RuboCop crashing when config file contains utf-8 characters and external encoding is not utf-8. ([@deivid-rodriguez][])
* [#3175](https://github.com/rubocop/rubocop/pull/3175): Generate 'Exclude' list for the cops with configurable enforced style to `.rubocop_todo.yml` if different styles are used. ([@flexoid][])
* [#3231](https://github.com/rubocop/rubocop/pull/3231): Make `Rails/UniqBeforePluck` more conservative. ([@tjwp][])

### Changes

* [#3149](https://github.com/rubocop/rubocop/pull/3149): Make `Style/HashSyntax` configurable to not report hash rocket syntax for symbols ending with ? or ! when using ruby19 style. ([@owst][])
* [#1758](https://github.com/rubocop/rubocop/issues/1758): Let `Style/ClosingParenthesisIndentation` follow `Style/AlignParameters` configuration for method calls. ([@jonas054][])
* [#3224](https://github.com/rubocop/rubocop/issues/3224): Rename `Style/DeprecatedHashMethods` to `Style/PreferredHashMethods`. ([@tejasbubane][])

## 0.40.0 (2016-05-09)

### New features

* [#2997](https://github.com/rubocop/rubocop/pull/2997): `Performance/CaseWhenSplat` can now identify multiple offenses in the same branch and offenses that do not occur as the first argument. ([@rrosenblum][])
* [#2928](https://github.com/rubocop/rubocop/issues/2928): `Style/NestedParenthesizedCalls` cop can auto-correct. ([@drenmi][])
* `Style/RaiseArgs` cop can auto-correct. ([@drenmi][])
* [#2993](https://github.com/rubocop/rubocop/pull/2993): `Style/SpaceAfterColon` now checks optional keyword arguments. ([@owst][])
* [#3003](https://github.com/rubocop/rubocop/pull/3003): Read command line options from `.rubocop` file and `RUBOCOP_OPTS` environment variable. ([@bolshakov][])
* [#2857](https://github.com/rubocop/rubocop/issues/2857): `Style/MultilineArrayBraceLayout` enforced style is configurable and supports `symmetrical` and `new_line` options. ([@panthomakos][])
* [#2857](https://github.com/rubocop/rubocop/issues/2857): `Style/MultilineHashBraceLayout` enforced style is configurable and supports `symmetrical` and `new_line` options. ([@panthomakos][])
* [#2857](https://github.com/rubocop/rubocop/issues/2857): `Style/MultilineMethodCallBraceLayout` enforced style is configurable and supports `symmetrical` and `new_line` options. ([@panthomakos][])
* [#2857](https://github.com/rubocop/rubocop/issues/2857): `Style/MultilineMethodDefinitionBraceLayout` enforced style is configurable and supports `symmetrical` and `new_line` options. ([@panthomakos][])
* [#3052](https://github.com/rubocop/rubocop/pull/3052): `Style/MultilineArrayBraceLayout` enforced style supports `same_line` option. ([@panthomakos][])
* [#3052](https://github.com/rubocop/rubocop/pull/3052): `Style/MultilineHashBraceLayout` enforced style supports `same_line` option. ([@panthomakos][])
* [#3052](https://github.com/rubocop/rubocop/pull/3052): `Style/MultilineMethodCallBraceLayout` enforced style supports `same_line` option. ([@panthomakos][])
* [#3052](https://github.com/rubocop/rubocop/pull/3052): `Style/MultilineMethodDefinitionBraceLayout` enforced style supports `same_line` option. ([@panthomakos][])
* [#3019](https://github.com/rubocop/rubocop/issues/3019): Add new `Style/EmptyCaseCondition` cop. ([@owst][], [@rrosenblum][])
* [#3072](https://github.com/rubocop/rubocop/pull/3072): Add new `Lint/UselessArraySplat` cop. ([@owst][])
* [#3022](https://github.com/rubocop/rubocop/issues/3022): `Style/Lambda` enforced style supports `literal` option. ([@drenmi][])
* [#2909](https://github.com/rubocop/rubocop/issues/2909): `Style/Lambda` enforced style supports `lambda` option. ([@drenmi][])
* [#3092](https://github.com/rubocop/rubocop/pull/3092): Allow `Style/Encoding` to enforce using no encoding comments. ([@NobodysNightmare][])
* New cop `Rails/UniqBeforePluck` checks that `uniq` is used before `pluck`. ([@tjwp][])

### Bug fixes

* [#3112](https://github.com/rubocop/rubocop/issues/3112): Fix `Style/ClassAndModuleChildren` for nested classes with explicit superclass. ([@jspanjers][])
* [#3032](https://github.com/rubocop/rubocop/issues/3032): Fix auto-correcting parentheses for predicate methods without space before args. ([@graemeboy][])
* [#3000](https://github.com/rubocop/rubocop/pull/3000): Fix encoding crash on HTML output. ([@gerrywastaken][])
* [#2983](https://github.com/rubocop/rubocop/pull/2983): `Style/AlignParameters` message was clarified for `with_fixed_indentation` style. ([@dylanahsmith][])
* [#2314](https://github.com/rubocop/rubocop/pull/2314): Ignore `UnusedBlockArgument` for keyword arguments. ([@volkert][])
* [#2975](https://github.com/rubocop/rubocop/issues/2975): Make comment indentation before `)` consistent with comment indentation before `}` or `]`. ([@jonas054][])
* [#3010](https://github.com/rubocop/rubocop/issues/3010): Fix double reporting/correction of spaces after ternary operator colons (now only reported by `Style/SpaceAroundOperators`, and not `Style/SpaceAfterColon` too). ([@owst][])
* [#3006](https://github.com/rubocop/rubocop/issues/3006): Register an offense for calling `merge!` on a method on a variable inside `each_with_object` in `Performance/RedundantMerge`. ([@lumeet][], [@rrosenblum][])
* [#2886](https://github.com/rubocop/rubocop/issues/2886): Custom cop changes now bust the cache. ([@ptarjan][])
* [#3043](https://github.com/rubocop/rubocop/issues/3043): `Style/SpaceAfterNot` will now register an offense for a receiver that is wrapped in parentheses. ([@rrosenblum][])
* [#3039](https://github.com/rubocop/rubocop/issues/3039): Accept `match` without a receiver in `Performance/EndWith`. ([@lumeet][])
* [#3039](https://github.com/rubocop/rubocop/issues/3039): Accept `match` without a receiver in `Performance/StartWith`. ([@lumeet][])
* [#3048](https://github.com/rubocop/rubocop/issues/3048): `Lint/NestedMethodDefinition` shouldn't flag methods defined on Structs. ([@owst][])
* [#2912](https://github.com/rubocop/rubocop/issues/2912): Check whether a line is aligned with the following line if the preceding line is not an assignment. ([@akihiro17][])
* [#3036](https://github.com/rubocop/rubocop/issues/3036): Don't let `Lint/UnneededDisable` inspect files that are excluded for the cop. ([@jonas054][])
* [#2874](https://github.com/rubocop/rubocop/issues/2874): Fix bug when the closing parenthesis is preceded by a newline in array and hash literals in `Style/RedundantParentheses`. ([@lumeet][])
* [#3049](https://github.com/rubocop/rubocop/issues/3049): Make `Lint/UselessAccessModifier` detect conditionally defined methods and correctly handle dynamically defined methods and singleton class methods. ([@owst][])
* [#3004](https://github.com/rubocop/rubocop/pull/3004): Don't add `Style/Alias` offenses for use of `alias` in `instance_eval` blocks, since object instances don't respond to `alias_method`. ([@magni-][])
* [#3061](https://github.com/rubocop/rubocop/pull/3061): Custom cops now show up in --show-cops. ([@ptarjan][])
* [#3088](https://github.com/rubocop/rubocop/pull/3088): Ignore offenses that involve conflicting HEREDOCs in the `Style/Multiline*BraceLayout` cops. ([@panthomakos][])
* [#3083](https://github.com/rubocop/rubocop/issues/3083): Do not register an offense for splat block args in `Style/SymbolProc`. ([@rrosenblum][])
* [#3063](https://github.com/rubocop/rubocop/issues/3063): Don't auto-correct `a + \` into `a + \\` in `Style/LineEndConcatenation`. ([@jonas054][])
* [#3034](https://github.com/rubocop/rubocop/issues/3034): Report offenses for `RuntimeError.new(msg)` in `Style/RedundantException`. ([@jonas054][])
* [#3016](https://github.com/rubocop/rubocop/issues/3016): `Style/SpaceAfterComma` now uses `Style/SpaceInsideHashLiteralBraces`'s setting. ([@ptarjan][])

### Changes

* [#2995](https://github.com/rubocop/rubocop/issues/2995): Removed deprecated path matching syntax. ([@gerrywastaken][])
* [#3025](https://github.com/rubocop/rubocop/pull/3025): Removed deprecation warnings for `rubocop-todo.yml`. ([@ptarjan][])
* [#3028](https://github.com/rubocop/rubocop/pull/3028): Add `define_method` to the default list of `IgnoredMethods` of `Style/SymbolProc`. ([@jastkand][])
* [#3064](https://github.com/rubocop/rubocop/pull/3064): `Style/SpaceAfterNot` highlights the entire expression instead of just the exclamation mark. ([@rrosenblum][])
* [#3085](https://github.com/rubocop/rubocop/pull/3085): Enable `Style/MultilineArrayBraceLayout` and `Style/MultilineHashBraceLayout` with the `symmetrical` style by default. ([@panthomakos][])
* [#3091](https://github.com/rubocop/rubocop/pull/3091): Enable `Style/MultilineMethodCallBraceLayout` and `Style/MultilineMethodDefinitionBraceLayout` with the `symmetrical` style by default. ([@panthomakos][])
* [#1830](https://github.com/rubocop/rubocop/pull/1830): `Style/PredicateName` now ignores the `spec/` directory, since there is a strong convention for using `have_*` and `be_*` helper methods in RSpec. ([@gylaz][])

## 0.39.0 (2016-03-27)

### New features

* `Performance/TimesMap` cop can auto-correct. ([@lumeet][])
* `Style/ZeroLengthPredicate` cop can auto-correct. ([@lumeet][])
* [#2828](https://github.com/rubocop/rubocop/issues/2828): `Style/ConditionalAssignment` is now configurable to enforce assignment inside of conditions or to enforce assignment to conditions. ([@rrosenblum][])
* [#2862](https://github.com/rubocop/rubocop/pull/2862): `Performance/Detect` and `Performance/Count` have a new configuration `SafeMode` that is defaulted to `true`. These cops have known issues with `Rails` and other ORM frameworks. With this default configuration, these cops will not run if the `Rails` cops are enabled. ([@rrosenblum][])
* `Style/IfUnlessModifierOfIfUnless` cop added. ([@amuino][])

### Bug fixes

* [#2948](https://github.com/rubocop/rubocop/issues/2948): `Style/SpaceAroundKeyword` should allow `yield[n]` and `super[n]`. ([@laurelfan][])
* [#2950](https://github.com/rubocop/rubocop/issues/2950): Fix auto-correcting cases in which precedence has changed in `Style/OneLineConditional`. ([@lumeet][])
* [#2947](https://github.com/rubocop/rubocop/issues/2947): Fix auto-correcting `if-then` in `Style/Next`. ([@lumeet][])
* [#2904](https://github.com/rubocop/rubocop/issues/2904): `Style/RedundantParentheses` doesn't flag `-(1.method)` or `+(1.method)`, since removing the parentheses would change the meaning of these expressions. ([@alexdowad][])
* [#2958](https://github.com/rubocop/rubocop/issues/2958): `Style/MultilineMethodCallIndentation` doesn't fail when inspecting unary ops which span multiple lines. ([@alexdowad][])
* [#2959](https://github.com/rubocop/rubocop/issues/2959): `Lint/LiteralInInterpolation` doesn't report offenses for iranges and eranges with non-literal endpoints. ([@alexdowad][])
* [#2960](https://github.com/rubocop/rubocop/issues/2960): `Lint/AssignmentInCondition` catches method assignments (like `obj.attr = val`) in a condition. ([@alexdowad][])
* [#2871](https://github.com/rubocop/rubocop/issues/2871): Second solution for possible encoding incompatibility when outputting an HTML report. ([@jonas054][])
* [#2967](https://github.com/rubocop/rubocop/pull/2967): Fix auto-correcting of `===`, `<=`, and `>=` in `Style/ConditionalAssignment`. ([@rrosenblum][])
* [#2977](https://github.com/rubocop/rubocop/issues/2977): Fix auto-correcting of `"#{$!}"` in `Style/SpecialGlobalVars`. ([@lumeet][])
* [#2935](https://github.com/rubocop/rubocop/issues/2935): Make configuration loading work if `SafeYAML.load` is private. ([@jonas054][])

### Changes

* `require:` only does relative includes when it starts with a `.`. ([@ptarjan][])
* `Style/IfUnlessModifier` does not trigger if the body is another conditional. ([@amuino][])
* [#2963](https://github.com/rubocop/rubocop/pull/2963): `Performance/RedundantMerge` will now register an offense inside of `each_with_object`. ([@rrosenblum][])

## 0.38.0 (2016-03-09)

### New features

* `Style/UnlessElse` cop can auto-correct. ([@lumeet][])
* [#2629](https://github.com/rubocop/rubocop/pull/2629): Add a new public API method, `highlighted_area` to offense. This method returns the range of the highlighted portion of an offense. ([@rrosenblum][])
* `Style/OneLineConditional` cop can auto-correct. ([@lumeet][])
* [#2905](https://github.com/rubocop/rubocop/issues/2905): `Style/ZeroLengthPredicate` flags code like `array.length < 1`, `1 > array.length`, and so on. ([@alexdowad][])
* [#2892](https://github.com/rubocop/rubocop/issues/2892): `Lint/BlockAlignment` cop can be configured to be stricter. ([@ptarjan][])
* `Style/Not` is able to auto-correct in cases where parentheses must be added to preserve the meaning of an expression. ([@alexdowad][])
* `Style/Not` auto-corrects comparison expressions by removing `not` and using the opposite comparison. ([@alexdowad][])

### Bug fixes

* Add `require 'time'` to `remote_config.rb` to avoid "undefined method \`rfc2822'". ([@necojackarc][])
* Replace `Rake::TaskManager#last_comment` with `Rake::TaskManager#last_description` for Rake 11 compatibility. ([@tbrisker][])
* Fix false positive in `Style/TrailingCommaInArguments` & `Style/TrailingCommaInLiteral` cops with consistent_comma style. ([@meganemura][])
* [#2861](https://github.com/rubocop/rubocop/pull/2861): Fix false positive in `Style/SpaceAroundKeyword` for `rescue(...`. ([@rrosenblum][])
* [#2832](https://github.com/rubocop/rubocop/issues/2832): `Style/MultilineOperationIndentation` treats operations inside blocks inside other operations correctly. ([@jonas054][])
* [#2865](https://github.com/rubocop/rubocop/issues/2865): Change `require:` in config to be relative to the `.rubocop.yml` file itself. ([@ptarjan][])
* [#2845](https://github.com/rubocop/rubocop/issues/2845): Handle heredocs in `Style/MultilineLiteralBraceLayout` auto-correct. ([@jonas054][])
* [#2848](https://github.com/rubocop/rubocop/issues/2848): Handle comments inside arrays in `Style/MultilineArrayBraceLayout` auto-correct. ([@jonas054][])
* `Style/TrivialAccessors` allows predicate methods by default. ([@alexdowad][])
* [#2869](https://github.com/rubocop/rubocop/issues/2869): Offenses which occur in the body of a `when` clause with multiple arguments will not be missed. ([@alexdowad][])
* `Lint/UselessAccessModifier` recognizes method defs inside a `begin` block. ([@alexdowad][])
* [#2870](https://github.com/rubocop/rubocop/issues/2870): `Lint/UselessAccessModifier` recognizes method definitions which are passed as an argument to a method call. ([@alexdowad][])
* [#2859](https://github.com/rubocop/rubocop/issues/2859): `Style/RedundantParentheses` doesn't consider the parentheses in `(!receiver.method arg)` to be redundant, since they might change the meaning of an expression, depending on precedence. ([@alexdowad][])
* [#2852](https://github.com/rubocop/rubocop/issues/2852): `Performance/Casecmp` doesn't flag uses of `downcase`/`upcase` which are not redundant. ([@alexdowad][])
* [#2850](https://github.com/rubocop/rubocop/issues/2850): `Style/FileName` doesn't choke on empty files with spaces in their names. ([@alexdowad][])
* [#2834](https://github.com/rubocop/rubocop/issues/2834): When configured as `ConsistentQuotesInMultiline: true`, `Style/StringLiterals` doesn't error out when inspecting a heredoc with differing indentation across multiple lines. ([@alexdowad][])
* [#2876](https://github.com/rubocop/rubocop/issues/2876): `Style/ConditionalAssignment` behaves correctly when assignment statement uses a character which has a special meaning in a regex. ([@alexdowad][])
* [#2877](https://github.com/rubocop/rubocop/issues/2877): `Style/SpaceAroundKeyword` doesn't flag `!super.method`, `!yield.method`, and so on. ([@alexdowad][])
* [#2631](https://github.com/rubocop/rubocop/issues/2631): `Style/Encoding` can remove unneeded encoding comment when auto-correcting with `when_needed` style. ([@alexdowad][])
* [#2860](https://github.com/rubocop/rubocop/issues/2860): Fix false positive in `Rails/Date` when `to_time` is chained with safe method. ([@palkan][])
* [#2898](https://github.com/rubocop/rubocop/issues/2898): `Lint/NestedMethodDefinition` allows methods defined inside `Class.new(S)` blocks. ([@segiddins][])
* [#2894](https://github.com/rubocop/rubocop/issues/2894): Fix auto-correct an unless with a comparison operator. ([@jweir][])
* [#2911](https://github.com/rubocop/rubocop/issues/2911): `Style/ClassAndModuleChildren` doesn't flag nested class definitions, where the outer class has an explicit superclass (because such definitions can't be converted to `compact` style). ([@alexdowad][])
* [#2871](https://github.com/rubocop/rubocop/issues/2871): Don't crash when offense messages are read back from cache with `ASCII-8BIT` encoding and output as HTML or JSON. ([@jonas054][])
* [#2901](https://github.com/rubocop/rubocop/issues/2901): Don't crash when `ENV['HOME']` is undefined. ([@mikegee][])
* [#2627](https://github.com/rubocop/rubocop/issues/2627): `Style/BlockDelimiters` does not flag blocks delimited by `{}` when a block call is the final value in a hash with implicit braces (one which is the last argument to an outer method call). ([@alexdowad][])

### Changes

* Update Rake to version 11. ([@tbrisker][])
* [#2629](https://github.com/rubocop/rubocop/pull/2629): Change the offense range for metrics cops to default to `expression` instead of `keyword` (the offense now spans the entire method, class, or module). ([@rrosenblum][])
* [#2891](https://github.com/rubocop/rubocop/pull/2891): Change the caching of remote configs to live alongside the parent file. ([@Fryguy][])
* [#2662](https://github.com/rubocop/rubocop/issues/2662): When setting options for Rake task, nested arrays can be used in the `options`, `formatters`, and `requires` arrays. ([@alexdowad][])
* [#2925](https://github.com/rubocop/rubocop/pull/2925): Bump unicode-display_width dependency to >= 1.0.1. ([@jspanjers][])
* [#2875](https://github.com/rubocop/rubocop/issues/2875): `Style/SignalException` does not flag calls to `fail` if a custom method named `fail` is defined in the same file. ([@alexdowad][])
* [#2923](https://github.com/rubocop/rubocop/issues/2923): `Style/FileName` considers file names which contain a ? or ! character to still be "snake case". ([@alexdowad][])
* [#2879](https://github.com/rubocop/rubocop/issues/2879): When auto-correcting, `Lint/UnusedMethodArgument` removes unused block arguments rather than simply prefixing them with an underscore. ([@alexdowad][])

## 0.37.2 (2016-02-11)

### Bug fixes

* Fix auto-correction of array and hash literals in `Lint/LiteralInInterpolation`. ([@lumeet][])
* [#2815](https://github.com/rubocop/rubocop/pull/2815): Fix missing assets for html formatter. ([@prsimp][])
* `Style/RedundantParentheses` catches offenses involving the 2nd argument to a method call without parentheses, if the 2nd argument is a hash. ([@alexdowad][])
* `Style/RedundantParentheses` catches offenses inside an array literal. ([@alexdowad][])
* `Style/RedundantParentheses` doesn't flag `method (:arg) {}`, since removing the parentheses would change the meaning of the expression. ([@alexdowad][])
* `Performance/Detect` doesn't flag code where `first` or `last` takes an argument, as it cannot be transformed to equivalent code using `detect`. ([@alexdowad][])
* `Style/SpaceAroundOperators` ignores aref assignments. ([@alexdowad][])
* `Style/RescueModifier` indents code correctly when auto-correcting. ([@alexdowad][])
* `Style/RedundantMerge` indents code correctly when auto-correcting, even if the corrected hash had multiple keys, and even if the corrected code was indented to start with. ([@alexdowad][])
* [#2831](https://github.com/rubocop/rubocop/issues/2831): `Performance/RedundantMerge` doesn't break code by auto-correcting a `#merge!` call which occurs at tail position in a block. ([@alexdowad][])

### Changes

* Handle auto-correction of nested interpolations in `Lint/LiteralInInterpolation`. ([@lumeet][])
* RuboCop results cache uses different directory names when there are many (or long) CLI options, to avoid a very long path which could cause failures on some filesystems. ([@alexdowad][])

## 0.37.1 (2016-02-09)

### New features

* [#2798](https://github.com/rubocop/rubocop/pull/2798): `Rails/FindEach` cop works with `where.not`. ([@pocke][])
* `Style/MultilineBlockLayout` can correct offenses which involve argument destructuring. ([@alexdowad][])
* `Style/SpaceAroundKeyword` checks `super` nodes with no args. ([@alexdowad][])
* `Style/SpaceAroundKeyword` checks `defined?` nodes. ([@alexdowad][])
* [#2719](https://github.com/rubocop/rubocop/issues/2719): `Style/ConditionalAssignment` handles correcting the alignment of `end`. ([@rrosenblum][])

### Bug fixes

* Fix auto-correction of `not` with parentheses in `Style/Not`. ([@lumeet][])
* [#2784](https://github.com/rubocop/rubocop/issues/2784): RuboCop can inspect `super { ... }` and `super(arg) { ... }`. ([@alexdowad][])
* [#2781](https://github.com/rubocop/rubocop/issues/2781): `Performance/RedundantMerge` doesn't flag calls to `#update`, since many classes have methods by this name (not only `Hash`). ([@alexdowad][])
* [#2780](https://github.com/rubocop/rubocop/issues/2780): `Lint/DuplicateMethods` does not flag method definitions inside dynamic `Class.new` blocks. ([@alexdowad][])
* [#2775](https://github.com/rubocop/rubocop/issues/2775): `Style/SpaceAroundKeyword` doesn't flag `yield.method`. ([@alexdowad][])
* [#2774](https://github.com/rubocop/rubocop/issues/2774): `Style/SpaceAroundOperators` doesn't flag calls to `#[]`. ([@alexdowad][])
* [#2772](https://github.com/rubocop/rubocop/issues/2772): RuboCop doesn't crash when `AllCops` section in configuration file is empty (rather, it displays a warning as intended). ([@alexdowad][])
* [#2737](https://github.com/rubocop/rubocop/issues/2737): `Style/GuardClause` handles `elsif` clauses correctly. ([@alexdowad][])
* [#2735](https://github.com/rubocop/rubocop/issues/2735): `Style/MultilineBlockLayout` doesn't cause an infinite loop by moving `end` onto the same line as the block args. ([@alexdowad][])
* [#2715](https://github.com/rubocop/rubocop/issues/2715): `Performance/RedundantMatch` doesn't flag calls to `#match` which take a block. ([@alexdowad][])
* [#2704](https://github.com/rubocop/rubocop/issues/2704): `Lint/NestedMethodDefinition` doesn't flag singleton defs which define a method on the value of a local variable. ([@alexdowad][])
* [#2660](https://github.com/rubocop/rubocop/issues/2660): `Style/TrailingUnderscoreVariable` shows recommended code in its offense message. ([@alexdowad][])
* [#2671](https://github.com/rubocop/rubocop/issues/2671): `Style/WordArray` doesn't attempt to inspect strings with invalid encoding, to avoid failing with an encoding error. ([@alexdowad][])

### Changes

* [#2739](https://github.com/rubocop/rubocop/issues/2739): Change the configuration option `when_needed` in `Style/FrozenStringLiteralComment` to add a `frozen_string_literal` comment to all files when the `TargetRubyVersion` is set to 2.3+. ([@rrosenblum][])

## 0.37.0 (2016-02-04)

### New features

* [#2620](https://github.com/rubocop/rubocop/pull/2620): New cop `Style/ZeroLengthPredicate` checks for `object.size == 0` and variants, and suggests replacing them with an appropriate `empty?` predicate. ([@drenmi][])
* [#2657](https://github.com/rubocop/rubocop/pull/2657): Floating headers in HTML output. ([@mattparlane][])
* Add new `Style/SpaceAroundKeyword` cop. ([@lumeet][])
* [#2745](https://github.com/rubocop/rubocop/pull/2745): New cop `Style/MultilineHashBraceLayout` checks that the closing brace in a hash literal is symmetrical with respect to the opening brace and the hash elements. ([@panthomakos][])
* [#2761](https://github.com/rubocop/rubocop/pull/2761): New cop `Style/MultilineMethodDefinitionBraceLayout` checks that the closing brace in a method definition is symmetrical with respect to the opening brace and the method parameters. ([@panthomakos][])
* [#2699](https://github.com/rubocop/rubocop/pull/2699): `Performance/Casecmp` can register offenses when `str.downcase` or `str.upcase` are passed to an equality method. ([@rrosenblum][])
* [#2766](https://github.com/rubocop/rubocop/pull/2766): New cop `Style/MultilineMethodCallBraceLayout` checks that the closing brace in a method call is symmetrical with respect to the opening brace and the method arguments. ([@panthomakos][])
* `Style/Semicolon` can auto-correct useless semicolons at the beginning of a line. ([@alexdowad][])

### Bug fixes

* [#2723](https://github.com/rubocop/rubocop/issues/2723): Fix NoMethodError in Style/GuardClause. ([@drenmi][])
* [#2674](https://github.com/rubocop/rubocop/issues/2674): Also check for Hash#update alias in `Performance/RedundantMerge`. ([@drenmi][])
* [#2630](https://github.com/rubocop/rubocop/issues/2630): Take frozen string literals into account in `Style/MutableConstant`. ([@segiddins][])
* [#2642](https://github.com/rubocop/rubocop/issues/2642): Support assignment via `||=` in `Style/MutableConstant`. ([@segiddins][])
* [#2646](https://github.com/rubocop/rubocop/issues/2646): Fix auto-correcting assignment to a constant in `Style/ConditionalAssignment`. ([@segiddins][])
* [#2614](https://github.com/rubocop/rubocop/issues/2614): Check for zero return value from `casecmp` in `Performance/casecmp`. ([@segiddins][])
* [#2647](https://github.com/rubocop/rubocop/issues/2647): Allow `xstr` interpolations in `Lint/LiteralInInterpolation`. ([@segiddins][])
* Report a violation when `freeze` is called on a frozen string literal in `Style/RedundantFreeze`. ([@segiddins][])
* [#2641](https://github.com/rubocop/rubocop/issues/2641): Fix crashing on empty methods with block args in `Performance/RedundantBlockCall`. ([@segiddins][])
* `Lint/DuplicateMethods` doesn't crash when `class_eval` is used with an implicit receiver. ([@lumeet][])
* [#2654](https://github.com/rubocop/rubocop/issues/2654): Fix handling of unary operations in `Style/RedundantParentheses`. ([@lumeet][])
* [#2661](https://github.com/rubocop/rubocop/issues/2661): `Style/Next` doesn't crash when auto-correcting modifier `if/unless`. ([@lumeet][])
* [#2665](https://github.com/rubocop/rubocop/pull/2665): Make specs pass when running on Windows. ([@jonas054][])
* [#2691](https://github.com/rubocop/rubocop/pull/2691): Do not register an offense in `Performance/TimesMap` for calling `map` or `collect` on a variable named `times`. ([@rrosenblum][])
* [#2689](https://github.com/rubocop/rubocop/pull/2689): Change `Performance/RedundantBlockCall` to respect parentheses usage. ([@rrosenblum][])
* [#2694](https://github.com/rubocop/rubocop/issues/2694): Fix caching when using a different JSON gem such as Oj. ([@georgyangelov][])
* [#2707](https://github.com/rubocop/rubocop/pull/2707): Change `Lint/NestedMethodDefinition` to respect `Class.new` and `Module.new`. ([@owst][])
* [#2701](https://github.com/rubocop/rubocop/pull/2701): Do not consider assignments to the same variable as useless if later assignments are within a loop. ([@owst][])
* [#2696](https://github.com/rubocop/rubocop/issues/2696): `Style/NestedModifier` adds parentheses around a condition when needed. ([@lumeet][])
* [#2666](https://github.com/rubocop/rubocop/issues/2666): Fix bug when auto-correcting symbol literals in `Lint/LiteralInInterpolation`. ([@lumeet][])
* [#2664](https://github.com/rubocop/rubocop/issues/2664): `Performance/Casecmp` can auto-correct case comparison to variables and method calls without error. ([@rrosenblum][])
* [#2729](https://github.com/rubocop/rubocop/issues/2729): Fix handling of hash literal as the first argument in `Style/RedundantParentheses`. ([@lumeet][])
* [#2703](https://github.com/rubocop/rubocop/issues/2703): Handle byte order mark in `Style/IndentationWidth`, `Style/ElseAlignment`, `Lint/EndAlignment`, and `Lint/DefEndAlignment`. ([@jonas054][])
* [#2710](https://github.com/rubocop/rubocop/pull/2710): Fix handling of fullwidth characters in some cops. ([@seikichi][])
* [#2690](https://github.com/rubocop/rubocop/issues/2690): Fix alignment of operands that are part of an assignment in `Style/MultilineOperationIndentation`. ([@jonas054][])
* [#2228](https://github.com/rubocop/rubocop/issues/2228): Use the config of a related cop whether it's enabled or not. ([@madwort][])
* [#2721](https://github.com/rubocop/rubocop/issues/2721): Do not register an offense for constants wrapped in parentheses passed to `rescue` in `Style/RedundantParentheses`. ([@rrosenblum][])
* [#2742](https://github.com/rubocop/rubocop/issues/2742): Fix `Style/TrailingCommaInArguments` & `Style/TrailingCommaInLiteral` for inline single element arrays. ([@annih][])
* [#2768](https://github.com/rubocop/rubocop/issues/2768): Allow parentheses after keyword `not` in `Style/MethodCallParentheses`. ([@lumeet][])
* [#2758](https://github.com/rubocop/rubocop/issues/2758): Allow leading underscores in camel case variable names. ([@mmcguinn][])

### Changes

* Remove `Style/SpaceAfterControlKeyword` and `Style/SpaceBeforeModifierKeyword` as the more generic `Style/SpaceAroundKeyword` handles the same cases. ([@lumeet][])
* Handle comparisons with `!=` in `Performance/casecmp`. ([@segiddins][])
* [#2684](https://github.com/rubocop/rubocop/pull/2684): Do not base `Style/FrozenStringLiteralComment` on the version of Ruby that is running. ([@rrosenblum][])
* [#2732](https://github.com/rubocop/rubocop/issues/2732): Change the default style of `Style/SignalException` to `only_raise`. ([@bbatsov][])

## 0.36.0 (2016-01-14)

### New features

* [#2598](https://github.com/rubocop/rubocop/pull/2598): New cop `Lint/RandOne` checks for `rand(1)`, `Kernel.rand(1.0)` and similar calls. Such call are most likely a mistake because they always return `0`. ([@DNNX][])
* [#2590](https://github.com/rubocop/rubocop/pull/2590): New cop `Performance/DoubleStartEndWith` checks for two `start_with?` (or `end_with?`) calls joined by `||` with the same receiver, like `str.start_with?('x') || str.start_with?('y')` and suggests using one call instead: `str.start_with?('x', 'y')`. ([@DNNX][])
* [#2583](https://github.com/rubocop/rubocop/pull/2583): New cop `Performance/TimesMap` checks for `x.times.map{}` and suggests replacing them with `Array.new(x){}`. ([@DNNX][])
* [#2581](https://github.com/rubocop/rubocop/pull/2581): New cop `Lint/NextWithoutAccumulator` finds bare `next` in `reduce`/`inject` blocks which assigns `nil` to the accumulator. ([@mvidner][])
* [#2529](https://github.com/rubocop/rubocop/pull/2529): Add EnforcedStyle config parameter to IndentArray. ([@jawshooah][])
* [#2479](https://github.com/rubocop/rubocop/pull/2479): Add option `AllowHeredoc` to `Metrics/LineLength`. ([@fphilipe][])
* [#2416](https://github.com/rubocop/rubocop/pull/2416): New cop `Style/ConditionalAssignment` checks for assignment of the same variable in all branches of conditionals and replaces them with a single assignment to the return of the conditional. ([@rrosenblum][])
* [#2410](https://github.com/rubocop/rubocop/pull/2410): New cop `Style/IndentAssignment` checks the indentation of the first line of the right-hand-side of a multi-line assignment. ([@panthomakos][])
* [#2431](https://github.com/rubocop/rubocop/issues/2431): Add `IgnoreExecutableScripts` option to `Style/FileName`. ([@sometimesfood][])
* [#2460](https://github.com/rubocop/rubocop/pull/2460): New cop `Style/UnneededInterpolation` checks for strings that are just an interpolated expression. ([@cgriego][])
* [#2361](https://github.com/rubocop/rubocop/pull/2361): `Style/MultilineAssignmentLayout` cop checks for a newline after the assignment operator in a multi-line assignment. ([@panthomakos][])
* [#2462](https://github.com/rubocop/rubocop/issues/2462): `Lint/UselessAccessModifier` can catch more types of useless access modifiers. ([@alexdowad][])
* [#1677](https://github.com/rubocop/rubocop/issues/1677): Add new `Performance/Casecmp` cop. ([@alexdowad][])
* [#1677](https://github.com/rubocop/rubocop/issues/1677): Add new `Performance/RangeInclude` cop. ([@alexdowad][])
* [#1677](https://github.com/rubocop/rubocop/issues/1677): Add new `Performance/RedundantSortBy` cop. ([@alexdowad][])
* [#1677](https://github.com/rubocop/rubocop/issues/1677): Add new `Performance/LstripRstrip` cop. ([@alexdowad][])
* [#1677](https://github.com/rubocop/rubocop/issues/1677): Add new `Performance/StartWith` cop. ([@alexdowad][])
* [#1677](https://github.com/rubocop/rubocop/issues/1677): Add new `Performance/EndWith` cop. ([@alexdowad][])
* [#1677](https://github.com/rubocop/rubocop/issues/1677): Add new `Performance/RedundantMerge` cop. ([@alexdowad][])
* `Lint/Debugger` cop can now auto-correct offenses. ([@alexdowad][])
* [#1677](https://github.com/rubocop/rubocop/issues/1677): Add new `Performance/RedundantMatch` cop. ([@alexdowad][])
* [#1677](https://github.com/rubocop/rubocop/issues/1677): Add new `Performance/RedundantBlockCall` cop. ([@alexdowad][])
* [#1954](https://github.com/rubocop/rubocop/issues/1954): `Lint/UnneededDisable` can now auto-correct. ([@alexdowad][])
* [#2501](https://github.com/rubocop/rubocop/issues/2501): Add new `Lint/ImplicitStringConcatenation` cop. ([@alexdowad][])
* Add new `Style/RedundantParentheses` cop. ([@lumeet][])
* [#1346](https://github.com/rubocop/rubocop/issues/1346): `Style/SpecialGlobalVars` can be configured to use either `use_english_names` or `use_perl_names` styles. ([@alexdowad][])
* [#2426](https://github.com/rubocop/rubocop/issues/2426): New `Style/NestedParenthesizedCalls` cop checks for non-parenthesized method calls nested inside a parenthesized call, like `method1(method2 arg)`. ([@alexdowad][])
* [#2502](https://github.com/rubocop/rubocop/issues/2502): The `--stdin` and `--auto-correct` CLI options can be combined, and if you do so, corrected code is printed to stdout. ([@alexdowad][])
* `Style/ConditionalAssignment` works on conditionals with a common aref assignment (like `array[index] = val`) or attribute assignment (like `self.attribute = val`). ([@alexdowad][])
* [#2476](https://github.com/rubocop/rubocop/issues/2476): `Style/GuardClause` catches if..else nodes with one branch which terminates the execution of the current scope. ([@alexdowad][])
* New `Style/IdenticalConditionalBranches` flags `if..else` and `case..when..else` constructs with an identical line at the end of each branch. ([@alexdowad][])
* [#207](https://github.com/rubocop/rubocop/issues/207): Add new `Lint/FloatOutOfRange` cop which catches floating-point literals which are too large or too small for Ruby to represent. ([@alexdowad][])
* `Style/GuardClause` doesn't report offenses in places where correction would make a line too long. ([@alexdowad][])
* `Lint/DuplicateMethods` can find duplicate method definitions in many more circumstances, even across multiple files; however, it ignores definitions inside `if` or something which could be a DSL method. ([@alexdowad][])
* A warning is printed if an invalid `EnforcedStyle` is configured. ([@alexdowad][])
* [#1367](https://github.com/rubocop/rubocop/issues/1367): New `Lint/IneffectiveAccessModifier` checks for access modifiers which are erroneously applied to a singleton method, where they have no effect. ([@alexdowad][])
* [#1614](https://github.com/rubocop/rubocop/issues/1614): `Lint/BlockAlignment` aligns block end with splat operator when applied to a splatted method call. ([@alexdowad][])
* [#2263](https://github.com/rubocop/rubocop/issues/2263): Warn if `task.options = %w(--format ...)` is used when configuring `RuboCop::RakeTask`; this should be `task.formatters = ...` instead. ([@alexdowad][])
* [#2511](https://github.com/rubocop/rubocop/issues/2511): `--no-offense-counts` CLI option suppresses the inclusion of offense count lines in auto-generated config. ([@alexdowad][])
* [#2504](https://github.com/rubocop/rubocop/issues/2504): New `AllowForAlignment` config parameter for `Style/SingleSpaceBeforeFirstArg` allows the insertion of extra spaces before the first argument if it aligns it with something on the preceding or following line. ([@alexdowad][])
* [#2478](https://github.com/rubocop/rubocop/issues/2478): `Style/ExtraSpacing` has new `ForceEqualSignAlignment` config parameter which forces = signs on consecutive lines to be aligned, and it can auto-correct. ([@alexdowad][])
* `Lint/BlockAlignment` aligns block end with unary operators like ~, -, or ! when such operators are applied to the method call taking the block. ([@alexdowad][])
* [#1460](https://github.com/rubocop/rubocop/issues/1460): `Style/Alias` supports both `prefer_alias` and `prefer_alias_method` styles. ([@alexdowad][])
* [#1569](https://github.com/rubocop/rubocop/issues/1569): New `ExpectMatchingDefinition` config parameter for `Style/FileName` makes it check for a class or module definition in each file which corresponds to the file name and path. ([@alexdowad][])
* [#2480](https://github.com/rubocop/rubocop/pull/2480): Add a configuration to `Style/ConditionalAssignment` to check and correct conditionals that contain multiple assignments. ([@rrosenblum][])
* [#2480](https://github.com/rubocop/rubocop/pull/2480): Allow `Style/ConditionalAssignment` to correct assignment in ternary operations. ([@rrosenblum][])
* [#2480](https://github.com/rubocop/rubocop/pull/2480): Allow `Style/ConditionalAssignment` to correct comparable methods. ([@rrosenblum][])
* [#1633](https://github.com/rubocop/rubocop/issues/1633): New cop `Style/MultilineMethodCallIndentation` takes over the responsibility for checking alignment of methods from the `Style/MultilineOperationIndentation` cop. ([@jonas054][])
* [#2472](https://github.com/rubocop/rubocop/pull/2472): New cop `Style/MultilineArrayBraceLayout` checks that the closing brace in an array literal is symmetrical with respect to the opening brace and the array elements. ([@panthomakos][])
* [#1543](https://github.com/rubocop/rubocop/issues/1543): `Style/WordArray` has both `percent` and `brackets` (which enforces the use of bracketed arrays for strings) styles. ([@alexdowad][])
* `Style/SpaceAroundOperators` has `AllowForAlignment` config parameter which allows extra spaces on the left if they serve to align the operator with another. ([@alexdowad][])
* `Style/SymbolArray` has both `percent` and `brackets` (which enforces the user of bracketed arrays for symbols) styles. ([@alexdowad][])
* [#2343](https://github.com/rubocop/rubocop/issues/2343): Entire cop types (or "departments") can be disabled using in .rubocop.yml using config like `Style: Enabled: false`. ([@alexdowad][])
* [#2399](https://github.com/rubocop/rubocop/issues/2399): New `start_of_line` style for `Lint/EndAlignment` aligns a closing `end` keyword with the start of the line where the opening keyword appears. ([@alexdowad][])
* [#1545](https://github.com/rubocop/rubocop/issues/1545): New `Regex` config parameter for `Style/FileName` allows user to provide their own regex for validating file names. ([@alexdowad][])
* [#2253](https://github.com/rubocop/rubocop/issues/2253): New `DefaultFormatter` config parameter can be used to set formatter from within .rubocop.yml. ([@alexdowad][])
* [#2481](https://github.com/rubocop/rubocop/issues/2481): New `WorstOffendersFormatter` prints a list of files with offenses (and offense counts), showing the files with the most offenses first. ([@alexdowad][])
* New `IfInsideElse` cop catches `if..end` nodes which can be converted into an `elsif` instead, reducing the nesting level. ([@alexdowad][])
* [#1725](https://github.com/rubocop/rubocop/issues/1725): --color CLI option forces color output, even when not printing to a TTY. ([@alexdowad][])
* [#2549](https://github.com/rubocop/rubocop/issues/2549): New `ConsistentQuotesInMultiline` config param for `Style/StringLiterals` forces all literals which are concatenated using \ to use the same quote style. ([@alexdowad][])
* [#2560](https://github.com/rubocop/rubocop/issues/2560): `Style/AccessModifierIndentation`, `Style/CaseIndentation`, `Style/FirstParameterIndentation`, `Style/IndentArray`, `Style/IndentAssignment`, `Style/IndentHash`, `Style/MultilineMethodCallIndentation`, and `Style/MultilineOperationIndentation` all have a new `IndentationWidth` parameter which can be used to override the indentation width from `Style/IndentationWidth`. ([@alexdowad][])
* Add new `Performance/HashEachMethods` cop. ([@ojab][])
* New cop `Style/FrozenStringLiteralComment` will check for and add the comment `# frozen_string_literal: true` to the top of files. This will help with upgrading to Ruby 3.0. ([@rrosenblum][])

### Bug Fixes

* [#2594](https://github.com/rubocop/rubocop/issues/2594): `Style/EmptyLiteral` auto-corrector respects `Style/StringLiterals:EnforcedStyle` config. ([@DNNX][])
* [#2411](https://github.com/rubocop/rubocop/issues/2411): Make local inherited configuration override configuration loaded from gems. ([@jonas054][])
* [#2413](https://github.com/rubocop/rubocop/issues/2413): Allow `%Q` for dynamic strings with double quotes inside them. ([@jonas054][])
* [#2404](https://github.com/rubocop/rubocop/issues/2404): `Style/Next` does not remove comments when auto-correcting. ([@lumeet][])
* `Style/Next` handles auto-correction of nested offenses. ([@lumeet][])
* `Style/VariableInterpolation` now detects non-numeric regex back references. ([@cgriego][])
* `ProgressFormatter` fully respects the `--no-color` switch. ([@savef][])
* Replace `Time.zone.current` with `Time.current` on `Rails::TimeZone` cop message. ([@volmer][])
* [#2451](https://github.com/rubocop/rubocop/issues/2451): `Style/StabbyLambdaParentheses` does not treat method calls named `lambda` as lambdas. ([@domcleal][])
* [#2463](https://github.com/rubocop/rubocop/issues/2463): Allow comments before an access modifier. ([@codebeige][])
* [#2471](https://github.com/rubocop/rubocop/issues/2471): `Style/MethodName` doesn't choke on methods which are defined inside methods. ([@alexdowad][])
* [#2449](https://github.com/rubocop/rubocop/issues/2449): `Style/StabbyLambdaParentheses` only checks lambdas in the arrow form. ([@lumeet][])
* [#2456](https://github.com/rubocop/rubocop/issues/2456): `Lint/NestedMethodDefinition` doesn't register offenses for method definitions inside an eval block (either `instance_eval`, `class_eval`, or `module_eval`). ([@alexdowad][])
* [#2464](https://github.com/rubocop/rubocop/issues/2464): `Style/ParallelAssignment` understands aref and attribute assignments, and doesn't warn if they can't be correctly rearranged into a series of single assignments. ([@alexdowad][])
* [#2482](https://github.com/rubocop/rubocop/issues/2482): `Style/AndOr` doesn't raise an exception when trying to auto-correct `!variable or ...`. ([@alexdowad][])
* [#2446](https://github.com/rubocop/rubocop/issues/2446): `Style/Tab` doesn't register errors for leading tabs which occur inside a string literal (including heredoc). ([@alexdowad][])
* [#2452](https://github.com/rubocop/rubocop/issues/2452): `Style/TrailingComma` incorrectly categorizes single-line hashes in methods calls. ([@panthomakos][])
* [#2441](https://github.com/rubocop/rubocop/issues/2441): `Style/AlignParameters` doesn't crash if it finds nested offenses. ([@alexdowad][])
* [#2436](https://github.com/rubocop/rubocop/issues/2436): `Style/SpaceInsideHashLiteralBraces` doesn't mangle a hash literal which is not surrounded by curly braces, but has another hash literal which does as its first key. ([@alexdowad][])
* [#2483](https://github.com/rubocop/rubocop/issues/2483): `Style/Attr` differentiate between attr_accessor and attr_reader. ([@weh][])
* `Style/ConditionalAssignment` doesn't crash if it finds a `case` with an empty branch. ([@lumeet][])
* [#2506](https://github.com/rubocop/rubocop/issues/2506): `Lint/FormatParameterMismatch` understands `%{}` and `%<>` interpolations. ([@alexdowad][])
* [#2145](https://github.com/rubocop/rubocop/issues/2145): `Lint/ParenthesesAsGroupedExpression` ignores calls with multiple arguments, since they are not ambiguous. ([@alexdowad][])
* [#2484](https://github.com/rubocop/rubocop/issues/2484): Remove two vulnerabilities in cache handling. ([@jonas054][])
* [#2517](https://github.com/rubocop/rubocop/issues/2517): `Lint/UselessAccessModifier` doesn't think that an access modifier applied to `attr_writer` is useless. ([@alexdowad][])
* [#2518](https://github.com/rubocop/rubocop/issues/2518): `Style/ConditionalAssignment` doesn't think that branches using `<<` and `[]=` should be combined. ([@alexdowad][])
* `CharacterLiteral` auto-corrector now properly corrects `?'`. ([@bfontaine][])
* [#2313](https://github.com/rubocop/rubocop/issues/2313): `Rails/FindEach` doesn't break code which uses `order(...).each`, `limit(...).each`, and so on. ([@alexdowad][])
* [#1938](https://github.com/rubocop/rubocop/issues/1938): `Rails/FindBy` doesn't auto-correct `where(...).first` to `find_by`, since the returned record is often different. ([@alexdowad][])
* [#1801](https://github.com/rubocop/rubocop/issues/1801): `EmacsFormatter` strips newlines out of error messages, if there are any. ([@alexdowad][])
* [#2534](https://github.com/rubocop/rubocop/issues/2534): `Style/RescueEnsureAlignment` works on `rescue` nested inside a `class` or `module` block. ([@alexdowad][])
* `Lint/BlockAlignment` does not refer to a block terminator as `end` when it is actually `}`. ([@alexdowad][])
* [#2540](https://github.com/rubocop/rubocop/issues/2540): `Lint/FormatParameterMismatch` understands format specifiers with multiple flags. ([@alexdowad][])
* [#2538](https://github.com/rubocop/rubocop/issues/2538): `Style/SpaceAroundOperators` doesn't eat newlines. ([@alexdowad][])
* [#2531](https://github.com/rubocop/rubocop/issues/2531): `Style/AndOr` auto-corrects in cases where parentheses must be added, even inside a nested begin node. ([@alexdowad][])
* [#2450](https://github.com/rubocop/rubocop/issues/2450): `Style/Next` adjusts indentation when auto-correcting, to avoid introducing new offenses. ([@alexdowad][])
* [#2066](https://github.com/rubocop/rubocop/issues/2066): `Style/TrivialAccessors` doesn't flag what appear to be trivial accessor method definitions, if they are nested inside a call to `instance_eval`. ([@alexdowad][])
* `Style/SymbolArray` doesn't flag arrays of symbols if a symbol contains a space character. ([@alexdowad][])
* `Style/SymbolArray` can auto-correct offenses. ([@alexdowad][])
* [#2546](https://github.com/rubocop/rubocop/issues/2546): Report when two `rubocop:disable` comments (not the single line kind) for a given cop appear in a file with no `rubocop:enable` in between. ([@jonas054][])
* [#2552](https://github.com/rubocop/rubocop/issues/2552): `Style/Encoding` can auto-correct files with a blank first line. ([@alexdowad][])
* [#2556](https://github.com/rubocop/rubocop/issues/2556): `Style/SpecialGlobalVariables` generates auto-config correctly. ([@alexdowad][])
* [#2565](https://github.com/rubocop/rubocop/issues/2565): Let `Style/SpaceAroundOperators` leave spacing around `=>` to `Style/AlignHash`. ([@jonas054][])
* [#2569](https://github.com/rubocop/rubocop/issues/2569): `Style/MethodCallParentheses` doesn't register warnings for `object.()` syntax, since it is handled by `Style/LambdaCall`. ([@alexdowad][])
* [#2570](https://github.com/rubocop/rubocop/issues/2570): `Performance/RedundantMerge` doesn't break code with a modifier `if` when auto-correcting. ([@alexdowad][])
* `Performance/RedundantMerge` doesn't break code with a modifier `while` or `until` when auto-correcting. ([@alexdowad][])
* [#2574](https://github.com/rubocop/rubocop/issues/2574): `variable` style for `Lint/EndAlignment` is working again. ([@alexdowad][])
* `Lint/EndAlignment` can auto-correct offenses on the RHS of an assignment to an instance variable, class variable, constant, and so on; previously, it only worked if the LHS was a local variable. ([@alexdowad][])
* [#2580](https://github.com/rubocop/rubocop/issues/2580): `Style/StringReplacement` doesn't break code when auto-correction involves a regex with embedded escapes (like /\n/). ([@alexdowad][])
* [#2582](https://github.com/rubocop/rubocop/issues/2582): `Style/AlignHash` doesn't move a key so far left that it goes onto the previous line (in an attempt to align). ([@alexdowad][])
* [#2588](https://github.com/rubocop/rubocop/issues/2588): `Style/SymbolProc` doesn't break code when auto-correcting a method call with a trailing comma in the argument list. ([@alexdowad][])
* [#2448](https://github.com/rubocop/rubocop/issues/2448): `Style/TrailingCommaInArguments` and `Style/TrailingCommaInLiteral` don't special-case single-item lists in a way which contradicts the documentation. ([@alexdowad][])
* Fix for remote config files to only load from on http and https URLs. ([@ptrippett][])
* [#2604](https://github.com/rubocop/rubocop/issues/2604): `Style/FileName` doesn't fail on empty files when `ExpectMatchingDefinition` is true. ([@alexdowad][])
* `Style/RedundantFreeze` registers offences for frozen dynamic symbols. ([@segiddins][])
* [#2609](https://github.com/rubocop/rubocop/issues/2609): All cops which rely on the `AutoCorrectUnlessChangingAST` module can now auto-correct files which contain `__FILE__`. ([@alexdowad][])
* [#2608](https://github.com/rubocop/rubocop/issues/2608): `Style/ConditionalAssignment` can auto-correct `=~` within a ternary expression. ([@alexdowad][])

### Changes

* [#2427](https://github.com/rubocop/rubocop/pull/2427): Allow non-snake-case file names (e.g. `some-random-script`) for Ruby scripts that have a shebang. ([@sometimesfood][])
* [#2430](https://github.com/rubocop/rubocop/pull/2430): `Lint/UnneededDisable` now adds "unknown cop" to messages if cop names in `rubocop:disable` comments are unrecognized, or "did you mean ..." if they are misspelled names of existing cops. ([@jonas054][])
* [#947](https://github.com/rubocop/rubocop/issues/947): `Style/Documentation` considers classes and modules which only define constants to be "namespaces", and doesn't flag them for lack of a documentation comment. ([@alexdowad][])
* [#2467](https://github.com/rubocop/rubocop/issues/2467): Explicitly inheriting configuration from the rubocop gem in .rubocop.yml is not allowed. ([@alexdowad][])
* [#2322](https://github.com/rubocop/rubocop/issues/2322): Output of --auto-gen-config shows content of default config parameters which are Arrays; this is especially useful for SupportedStyles. ([@alexdowad][])
* [#1566](https://github.com/rubocop/rubocop/issues/1566): When auto-correcting on Windows, line endings are not converted to "\r\n" in untouched portions of the source files; corrected portions may use "\n" rather than "\r\n". ([@alexdowad][])
* New `rake repl` task can be used for experimentation when working on RuboCop. ([@alexdowad][])
* `Lint/SpaceBeforeFirstArg` cop has been removed, since it just duplicates `Style/SingleSpaceBeforeFirstArg`. ([@alexdowad][])
* `Style/SingleSpaceBeforeFirstArg` cop has been renamed to `Style/SpaceBeforeFirstArg`, which more accurately reflects what it now does. ([@alexdowad][])
* `Style/UnneededPercentQ` reports `%q()` strings with what only appears to be an escape, but is not really (there are no escapes in `%q()` strings). ([@alexdowad][])
* `Performance/StringReplacement`, `Performance\StartWith`, and `Performance\EndWith` more accurately identify code which can be improved. ([@alexdowad][])
* The `MultiSpaceAllowedForOperators` config parameter for `Style/SpaceAroundOperators` has been removed, as it is made redundant by `AllowForAlignment`. If someone attempts to use it, config validation will fail with a helpful message. ([@alexdowad][])
* The `RunRailsCops` config parameter in .rubocop.yml is now obsolete. If someone attempts to use it, config validation will fail with a helpful message. ([@alexdowad][])
* If .rubocop.yml contains configuration for a custom cop, no warning regarding "unknown cop" will be printed. The custom cop must inherit from RuboCop::Cop::Cop, and must be loaded into memory for this to work. ([@alexdowad][])
* [#2102](https://github.com/rubocop/rubocop/issues/2102): If .rubocop.yml exists in the working directory when running --auto-gen-config, any `Exclude` config parameters in .rubocop.yml will be merged into the generated .rubocop_todo.yml. ([@alexdowad][])
* [#1895](https://github.com/rubocop/rubocop/issues/1895): Remove `Rails/DefaultScope` cop. ([@alexdowad][])
* [#2550](https://github.com/rubocop/rubocop/issues/2550): New `TargetRubyVersion` configuration parameter can be used to specify which version of the Ruby interpreter the inspected code is intended to run on. ([@alexdowad][])
* [#2557](https://github.com/rubocop/rubocop/issues/2557): `Style/GuardClause` does not warn about `if` nodes whose condition spans multiple lines. ([@alexdowad][])
* `Style/EmptyLinesAroundClassBody`, `Style/EmptyLinesAroundModuleBody`, and `Style/EmptyLinesAroundBlockBody` accept an empty body with no blank line, even if configured to `empty_lines` style. This is because the empty lines only serve to provide a break between the header, body, and footer, and are redundant if there is no body. ([@alexdowad][])
* [#2554](https://github.com/rubocop/rubocop/issues/2554): `Style/FirstMethodArgumentLineBreak` handles implicit hash arguments without braces; `Style/FirstHashElementLineBreak` still handles those with braces. ([@alexdowad][])
* `Style/TrailingComma` has been split into `Style/TrailingCommaInArguments` and `Style/TrailingCommaInLiteral`. ([@alexdowad][])
* RuboCop returns process exit code 2 if it fails due to bad configuration, bad CLI options, or an internal error. If it runs successfully but finds one or more offenses, it still exits with code 1, as was previously the case. This is helpful when invoking RuboCop programmatically, perhaps from a script. ([@alexdowad][])

## 0.35.1 (2015-11-10)

### Bug Fixes

* [#2407](https://github.com/rubocop/rubocop/issues/2407): Use `Process.uid` rather than `Etc.getlogin` for simplicity and compatibility. ([@jujugrrr][])

## 0.35.0 (2015-11-07)

### New features

* [#2028](https://github.com/rubocop/rubocop/issues/2028): New config `ExtraDetails` supports addition of `Details` param to all cops to allow extra details on offense to be displayed. ([@tansaku][])
* [#2036](https://github.com/rubocop/rubocop/issues/2036): New cop `Style/StabbyLambdaParentheses` will find and correct cases where a stabby lambda's parameters are not wrapped in parentheses. ([@hmadison][])
* [#2246](https://github.com/rubocop/rubocop/pull/2246): `Style/TrailingUnderscoreVariable` will now register an offense for `*_`. ([@rrosenblum][])
* [#2246](https://github.com/rubocop/rubocop/pull/2246): `Style/TrailingUnderscoreVariable` now has a configuration to remove named underscore variables (Defaulted to false). ([@rrosenblum][])
* [#2276](https://github.com/rubocop/rubocop/pull/2276): New cop `Performance/FixedSize` will register an offense when calling `length`, `size`, or `count` on statically sized objected (strings, symbols, arrays, and hashes). ([@rrosenblum][])
* New cop `Style/NestedModifier` checks for nested `if`, `unless`, `while` and `until` modifier statements. ([@lumeet][])
* [#2270](https://github.com/rubocop/rubocop/pull/2270): Add a new `inherit_gem` configuration to inherit a config file from an installed gem [(originally requested in #290)](https://github.com/rubocop/rubocop/issues/290). ([@jhansche][])
* Allow `StyleGuide` parameters in local configuration for all cops, so users can add references to custom style guide documents. ([@cornelius][])
* `UnusedMethodArgument` cop allows configuration to skip keyword arguments. ([@apiology][])
* [#2318](https://github.com/rubocop/rubocop/pull/2318): `Lint/Debugger` cop now checks for `Pry.rescue`. ([@rrosenblum][])
* [#2277](https://github.com/rubocop/rubocop/pull/2277): New cop `Style/FirstArrayElementLineBreak` checks for a line break before the first element in a multi-line array. ([@panthomakos][])
* [#2277](https://github.com/rubocop/rubocop/pull/2277): New cop `Style/FirstHashElementLineBreak` checks for a line break before the first element in a multi-line hash. ([@panthomakos][])
* [#2277](https://github.com/rubocop/rubocop/pull/2277): New cop `Style/FirstMethodArgumentLineBreak` checks for a line break before the first argument in a multi-line method call. ([@panthomakos][])
* [#2277](https://github.com/rubocop/rubocop/pull/2277): New cop `Style/FirstMethodParameterLineBreak` checks for a line break before the first parameter in a multi-line method parameter definition. ([@panthomakos][])
* Add `Rails/PluralizationGrammar` cop, checks for incorrect grammar when using methods like `3.day.ago`, when you should write `3.days.ago`. ([@maxjacobson][])
* [#2347](https://github.com/rubocop/rubocop/pull/2347): `Lint/Eval` cop does not warn about "security risk" when eval argument is a string literal without interpolations. ([@alexdowad][])
* [#2335](https://github.com/rubocop/rubocop/issues/2335): `Style/VariableName` cop checks naming style of method parameters. ([@alexdowad][])
* [#2329](https://github.com/rubocop/rubocop/pull/2329): New style `braces_for_chaining` for `Style/BlockDelimiters` cop enforces braces on a multi-line block if its return value is being chained with another method. ([@panthomakos][])
* `Lint/LiteralInCondition` warns if a symbol or dynamic symbol is used as a condition. ([@alexdowad][])
* [#2369](https://github.com/rubocop/rubocop/issues/2369): `Style/TrailingComma` doesn't add a trailing comma to a multiline method chain which is the only arg to a method call. ([@alexdowad][])
* `CircularArgumentReference` cop updated to lint for ordinal circular argument references on top of optional keyword arguments. ([@maxjacobson][])
* Added ability to download shared rubocop config files from remote urls. ([@ptrippett][])
* [#1601](https://github.com/rubocop/rubocop/issues/1601): Add `IgnoreEmptyMethods` config parameter for `Lint/UnusedMethodArgument` and `IgnoreEmptyBlocks` config parameter for `Lint/UnusedBlockArgument` cops. ([@alexdowad][])
* [#1729](https://github.com/rubocop/rubocop/issues/1729): `Style/MethodDefParentheses` supports new 'require_no_parentheses_except_multiline' style. ([@alexdowad][])
* [#2173](https://github.com/rubocop/rubocop/issues/2173): `Style/AlignParameters` also checks parameter alignment for method definitions. ([@alexdowad][])
* [#1825](https://github.com/rubocop/rubocop/issues/1825): New `NameWhitelist` configuration parameter for `Style/PredicateName` can be used to suppress errors on known-good predicate names. ([@alexdowad][])
* `Style/Documentation` recognizes 'Constant = Class.new' as a class definition. ([@alexdowad][])
* [#1608](https://github.com/rubocop/rubocop/issues/1608): Add new 'align_braces' style for `Style/IndentHash`. ([@alexdowad][])
* `Style/Next` can auto-correct. ([@alexdowad][])

### Bug Fixes

* [#2265](https://github.com/rubocop/rubocop/issues/2265): Handle unary `+` in `ExtraSpacing` cop. ([@jonas054][])
* [#2275](https://github.com/rubocop/rubocop/pull/2275): Copy default `Exclude` into `Exclude` lists in `.rubocop_todo.yml`. ([@jonas054][])
* `Style/IfUnlessModifier` accepts blocks followed by a chained call. ([@lumeet][])
* [#2261](https://github.com/rubocop/rubocop/issues/2261): Make relative `Exclude` paths in `$HOME/.rubocop_todo.yml` be relative to current directory. ([@jonas054][])
* [#2286](https://github.com/rubocop/rubocop/issues/2286): Handle auto-correction of empty method when `AllowIfMethodIsEmpty` is `false` in `Style/SingleLineMethods`. ([@jonas054][])
* [#2246](https://github.com/rubocop/rubocop/pull/2246): Do not register an offense for `Style/TrailingUnderscoreVariable` when the underscore variable is preceded by a splat variable. ([@rrosenblum][])
* [#2292](https://github.com/rubocop/rubocop/pull/2292): Results should not be stored in the cache if affected by errors (crashes). ([@jonas054][])
* [#2280](https://github.com/rubocop/rubocop/issues/2280): Avoid reporting space between hash literal keys and values in `Style/ExtraSpacing`. ([@jonas054][])
* [#2284](https://github.com/rubocop/rubocop/issues/2284): Fix result cache being shared between ruby versions. ([@miquella][])
* [#2285](https://github.com/rubocop/rubocop/issues/2285): Fix `ConfigurableNaming#class_emitter_method?` error when handling singleton class methods. ([@palkan][])
* [#2295](https://github.com/rubocop/rubocop/issues/2295): Fix Performance/Detect auto-correct to handle rogue newlines. ([@palkan][])
* [#2294](https://github.com/rubocop/rubocop/issues/2294): Do not register an offense in `Performance/StringReplacement` for regex with options. ([@rrosenblum][])
* Fix `Style/UnneededPercentQ` condition for single-quoted literal containing interpolation-like string. ([@eagletmt][])
* [#2324](https://github.com/rubocop/rubocop/issues/2324): Handle `--only Lint/Syntax` and `--except Lint/Syntax` correctly. ([@jonas054][])
* [#2317](https://github.com/rubocop/rubocop/issues/2317): Handle `case` as an argument correctly in `Lint/EndAlignment`. ([@lumeet][])
* [#2287](https://github.com/rubocop/rubocop/issues/2287): Fix auto-correct of lines with only whitespace in `Style/IndentationWidth`. ([@lumeet][])
* [#2331](https://github.com/rubocop/rubocop/issues/2331): Do not register an offense in `Performance/Size` for `count` with an argument. ([@rrosenblum][])
* Handle a backslash at the end of a line in `Style/SpaceAroundOperators`. ([@lumeet][])
* Don't warn about lack of "leading space" in a =begin/=end comment. ([@alexdowad][])
* [#2307](https://github.com/rubocop/rubocop/issues/2307): In `Lint/FormatParameterMismatch`, don't register an offense if either argument to % is not a literal. ([@alexdowad][])
* [#2356](https://github.com/rubocop/rubocop/pull/2356): `Style/Encoding` will now place the encoding comment on the second line if the first line is a shebang. ([@rrosenblum][])
* `Style/InitialIndentation` cop doesn't error out when a line begins with an integer literal. ([@alexdowad][])
* [#2296](https://github.com/rubocop/rubocop/issues/2296): In `Style/DotPosition`, don't "correct" (and break) a method call which has a line comment (or blank line) between the dot and the selector. ([@alexdowad][])
* [#2272](https://github.com/rubocop/rubocop/issues/2272): `Lint/NonLocalExitFromIterator` does not warn about `return` in a block which is passed to `Module#define_method`. ([@alexdowad][])
* [#2262](https://github.com/rubocop/rubocop/issues/2262): Replace `Rainbow` reference with `Colorizable#yellow`. ([@minustehbare][])
* [#2068](https://github.com/rubocop/rubocop/issues/2068): Display warning if `Style/Copyright` is misconfigured. ([@alexdowad][])
* [#2321](https://github.com/rubocop/rubocop/issues/2321): In `Style/EachWithObject`, don't replace reduce with each_with_object if the accumulator parameter is assigned to in the block. ([@alexdowad][])
* [#1981](https://github.com/rubocop/rubocop/issues/1981): `Lint/UselessAssignment` doesn't erroneously identify assignments in identical if branches as useless. ([@alexdowad][])
* [#2323](https://github.com/rubocop/rubocop/issues/2323): `Style/IfUnlessModifier` cop parenthesizes auto-corrected code when necessary due to operator precedence, to avoid changing its meaning. ([@alexdowad][])
* [#2003](https://github.com/rubocop/rubocop/issues/2003): Make `Lint/UnneededDisable` work with `--auto-correct`. ([@jonas054][])
* Default RuboCop cache dir moved to per-user folders. ([@br3nda][])
* [#2393](https://github.com/rubocop/rubocop/pull/2393): `Style/MethodCallParentheses` doesn't fail on `obj.method ||= func()`. ([@alexdowad][])
* [#2344](https://github.com/rubocop/rubocop/pull/2344): When auto-correcting, `Style/ParallelAssignment` reorders assignment statements, if necessary, to avoid breaking code. ([@alexdowad][])
* `Style/MultilineOperationAlignment` does not try to align the receiver and selector of a method call if both are on the LHS of an assignment. ([@alexdowad][])

### Changes

* [#2194](https://github.com/rubocop/rubocop/issues/2194): Allow any options with `--auto-gen-config`. ([@agrimm][])

## 0.34.2 (2015-09-21)

### Bug Fixes

* [#2232](https://github.com/rubocop/rubocop/issues/2232): Fix false positive in `Lint/FormatParameterMismatch` for argument with splat operator. ([@dreyks][])
* [#2237](https://github.com/rubocop/rubocop/pull/2237): Allow `Lint/FormatParameterMismatch` to be called using `Kernel.format` and `Kernel.sprintf`. ([@rrosenblum][])
* [#2234](https://github.com/rubocop/rubocop/issues/2234): Do not register an offense for `Lint/FormatParameterMismatch` when the format string is a variable. ([@rrosenblum][])
* [#2240](https://github.com/rubocop/rubocop/pull/2240): `Lint/UnneededDisable` should not report non-`Lint` `rubocop:disable` comments when running `rubocop --lint`. ([@jonas054][])
* [#2121](https://github.com/rubocop/rubocop/issues/2121): Allow space before values in hash literals in `Style/ExtraSpacing` to avoid correction conflict. ([@jonas054][])
* [#2241](https://github.com/rubocop/rubocop/issues/2241): Read cache in binary format. ([@jonas054][])
* [#2247](https://github.com/rubocop/rubocop/issues/2247): Fix auto-correct of `Performance/CaseWhenSplat` for percent arrays (`%w`, `%W`, `%i`, and `%I`). ([@rrosenblum][])
* [#2244](https://github.com/rubocop/rubocop/issues/2244): Disregard annotation keywords in `Style/CommentAnnotation` if they don't start a comment. ([@jonas054][])
* [#2257](https://github.com/rubocop/rubocop/pull/2257): Fix bug where `Style/RescueEnsureAlignment` will register an offense for `rescue` and `ensure` on the same line. ([@rrosenblum][])
* [#2255](https://github.com/rubocop/rubocop/issues/2255): Refine the offense highlighting for `Style/SymbolProc`. ([@bbatsov][])
* [#2260](https://github.com/rubocop/rubocop/pull/2260): Make `Exclude` in `.rubocop_todo.yml` work when running from a subdirectory. ([@jonas054][])

### Changes

* [#2248](https://github.com/rubocop/rubocop/issues/2248): Allow block-pass in `Style/AutoResourceCleanup`. ([@lumeet][])
* [#2258](https://github.com/rubocop/rubocop/pull/2258): `Style/Documentation` will exclude test directories by default. ([@rrosenblum][])
* [#2260](https://github.com/rubocop/rubocop/issues/2260): Disable `Style/StringMethods` by default. ([@bbatsov][])

## 0.34.1 (2015-09-09)

### Bug Fixes

* [#2212](https://github.com/rubocop/rubocop/issues/2212): Handle methods without parentheses in auto-correct. ([@karreiro][])
* [#2214](https://github.com/rubocop/rubocop/pull/2214): Fix `File name too long error` when `STDIN` option is provided. ([@mrfoto][])
* [#2217](https://github.com/rubocop/rubocop/issues/2217): Allow block arguments in `Style/SymbolProc`. ([@lumeet][])
* [#2213](https://github.com/rubocop/rubocop/issues/2213): Write to cache with binary encoding to avoid transcoding exceptions in some locales. ([@jonas054][])
* [#2218](https://github.com/rubocop/rubocop/issues/2218): Fix loading config error when safe yaml is only partially loaded. ([@maxjacobson][])
* [#2161](https://github.com/rubocop/rubocop/issues/2161): Allow an explicit receiver (except `Kernel`) in `Style/SignalException`. ([@lumeet][])

## 0.34.0 (2015-09-05)

### New features

* [#2143](https://github.com/rubocop/rubocop/pull/2143): New cop `Performance/CaseWhenSplat` will identify and rearrange `case` `when` statements that contain a `when` condition with a splat. ([@rrosenblum][])
* New cop `Lint/DuplicatedKey` checks for duplicated keys in hashes, which Ruby 2.2 warns against. ([@sliuu][])
* [#2106](https://github.com/rubocop/rubocop/issues/2106): Add `SuspiciousParamNames` option to `Style/OptionHash`. ([@wli][])
* [#2193](https://github.com/rubocop/rubocop/pull/2193): `Style/Next` supports more `Enumerable` methods. ([@rrosenblum][])
* [#2179](https://github.com/rubocop/rubocop/issues/2179): Add `--list-target-files` option to CLI, which prints the files which will be inspected. ([@maxjacobson][])
* New cop `Style/MutableConstant` checks for assignment of mutable objects to constants. ([@bbatsov][])
* New cop `Style/RedundantFreeze` checks for usages of `Object#freeze` on immutable objects. ([@bbatsov][])
* [#1924](https://github.com/rubocop/rubocop/issues/1924): New option `--cache` and configuration parameter `AllCops: UseCache` turn result caching on (default) or off. ([@jonas054][])
* [#2204](https://github.com/rubocop/rubocop/pull/2204): New cop `Style/StringMethods` will check for preferred method `to_sym` over `intern`. ([@imtayadeway][])

### Changes

* [#1351](https://github.com/rubocop/rubocop/issues/1351): Allow class emitter methods in `Style/MethodName`. ([@jonas054][])
* [#2126](https://github.com/rubocop/rubocop/pull/2126): `Style/RescueModifier` can now auto-correct. ([@rrosenblum][])
* [#2109](https://github.com/rubocop/rubocop/issues/2109): Allow alignment with a token on the nearest line with same indentation in `Style/ExtraSpacing`. ([@jonas054][])
* `Lint/EndAlignment` handles the `case` keyword. ([@lumeet][])
* [#2146](https://github.com/rubocop/rubocop/pull/2146): Add STDIN support. ([@caseywebdev][])
* [#2175](https://github.com/rubocop/rubocop/pull/2175): Files that are excluded from a cop (e.g. using the `Exclude:` config option) are no longer being processed by that cop. ([@bquorning][])
* `Rails/ActionFilter` now handles complete list of methods found in the Rails 4.2 [release notes](https://github.com/rails/rails/blob/4115a12da1409c753c747fd4bab6e612c0c6e51a/guides/source/4_2_release_notes.md#notable-changes-1). ([@MGerrior][])
* [#2138](https://github.com/rubocop/rubocop/issues/2138): Change the offense in `Style/Next` to highlight the condition instead of the iteration. ([@rrosenblum][])
* `Style/EmptyLineBetweenDefs` now handles class methods as well. ([@unmanbearpig][])
* Improve handling of `super` in `Style/SymbolProc`. ([@lumeet][])
* `Style/SymbolProc` is applied to methods receiving arguments. ([@lumeet][])
* [#1839](https://github.com/rubocop/rubocop/issues/1839): Remove Rainbow monkey patching of String which conflicts with other gems like colorize. ([@daviddavis][])
* `Style/HashSyntax` is now a bit faster when checking Ruby 1.9 syntax hash keys. ([@bquorning][])
* `Lint/DeprecatedClassMethods` is now a whole lot faster. ([@bquorning][])
* `Lint/BlockAlignment`, `Style/IndentationWidth`, and `Style/MultilineOperationIndentation` are now quite a bit faster. ([@bquorning][])

### Bug Fixes

* [#2123](https://github.com/rubocop/rubocop/pull/2123): Fix handing of dynamic widths `Lint/FormatParameterMismatch`. ([@edmz][])
* [#2116](https://github.com/rubocop/rubocop/pull/2116): Fix named params (using hash) `Lint/FormatParameterMismatch`. ([@edmz][])
* [#2135](https://github.com/rubocop/rubocop/issues/2135): Ignore `super` and `zsuper` nodes in `Style/SymbolProc`. ([@bbatsov][])
* [#2165](https://github.com/rubocop/rubocop/issues/2165): Fix a NPE in `Style/Alias`. ([@bbatsov][])
* [#2168](https://github.com/rubocop/rubocop/issues/2168): Fix a NPE in `Rails/TimeZone`. ([@bbatsov][])
* [#2169](https://github.com/rubocop/rubocop/issues/2169): Fix a NPE in `Rails/Date`. ([@bbatsov][])
* [#2105](https://github.com/rubocop/rubocop/pull/2105): Fix a warning that was thrown when enabling `Style/OptionHash`. ([@wli][])
* [#2107](https://github.com/rubocop/rubocop/pull/2107): Fix auto-correct of `Style/ParallelAssignment` for nested expressions. ([@rrosenblum][])
* [#2111](https://github.com/rubocop/rubocop/issues/2111): Deal with byte order mark in `Style/InitialIndentation`. ([@jonas054][])
* [#2113](https://github.com/rubocop/rubocop/issues/2113): Handle non-string tokens in `Style/ExtraSpacing`. ([@jonas054][])
* [#2129](https://github.com/rubocop/rubocop/issues/2129): Handle empty interpolations in `Style/SpaceInsideStringInterpolation`. ([@lumeet][])
* [#2119](https://github.com/rubocop/rubocop/issues/2119): Do not raise an error in `Style/RescueEnsureAlignment` and `Style/RescueModifier` when processing an excluded file. ([@rrosenblum][])
* [#2149](https://github.com/rubocop/rubocop/issues/2149): Do not register an offense in `Rails/Date` when `Date#to_time` is called with a time zone argument. ([@maxjacobson][])
* Do not register a `Rails/TimeZone` offense when using Time.new safely. ([@maxjacobson][])
* [#2124](https://github.com/rubocop/rubocop/issues/2124): Fix bug in `Style/EmptyLineBetweenDefs` when there are only comments between method definitions. ([@lumeet][])
* [#2154](https://github.com/rubocop/rubocop/issues/2154): `Performance/StringReplacement` can auto-correct replacements with backslash in them. ([@rrosenblum][])
* [#2009](https://github.com/rubocop/rubocop/issues/2009): Fix bug in `RuboCop::ConfigLoader.load_file` when `safe_yaml` is required. ([@eitoball][])
* [#2155](https://github.com/rubocop/rubocop/issues/2155): Configuration `EndAlignment: AlignWith: variable` only applies when the operands of `=` are on the same line. ([@jonas054][])
* Fix bug in `Style/IndentationWidth` when `rescue` or `ensure` is preceded by an empty body. ([@lumeet][])
* [#2183](https://github.com/rubocop/rubocop/issues/2183): Fix bug in `Style/BlockDelimiters` when auto-correcting adjacent braces. ([@lumeet][])
* [#2199](https://github.com/rubocop/rubocop/issues/2199): Make `rubocop` exit with error when there are only `Lint/UnneededDisable` offenses. ([@jonas054][])
* Fix handling of empty parentheses when auto-correcting in `Style/SymbolProc`. ([@lumeet][])

## 0.33.0 (2015-08-05)

### New features

* [#2081](https://github.com/rubocop/rubocop/pull/2081): New cop `Style/Send` checks for the use of `send` and instead encourages changing it to `BasicObject#__send__` or `Object#public_send` (disabled by default). ([@syndbg][])
* [#2057](https://github.com/rubocop/rubocop/pull/2057): New cop `Lint/FormatParameterMismatch` checks for a mismatch between the number of fields expected in format/sprintf/% and what was passed to it. ([@edmz][])
* [#2010](https://github.com/rubocop/rubocop/pull/2010): Add `space` style for SpaceInsideStringInterpolation. ([@gotrevor][])
* [#2007](https://github.com/rubocop/rubocop/pull/2007): Allow any modifier before `def`, not only visibility modifiers. ([@fphilipe][])
* [#1980](https://github.com/rubocop/rubocop/pull/1980): `--auto-gen-config` now outputs an excluded files list for failed cops (up to a maximum of 15 files). ([@bmorrall][])
* [#2004](https://github.com/rubocop/rubocop/pull/2004): Introduced `--exclude-limit COUNT` to configure how many files `--auto-gen-config` will exclude. ([@awwaiid][], [@jonas054][])
* [#1918](https://github.com/rubocop/rubocop/issues/1918): New configuration parameter `AllCops:DisabledByDefault` when set to `true` makes only cops found in user configuration enabled, which makes cop selection *opt-in*. ([@jonas054][])
* New cop `Performance/StringReplacement` checks for usages of `gsub` that can be replaced with `tr` or `delete`. ([@rrosenblum][])
* [#2001](https://github.com/rubocop/rubocop/issues/2001): New cop `Style/InitialIndentation` checks for indentation of the first non-blank non-comment line in a file. ([@jonas054][])
* [#2060](https://github.com/rubocop/rubocop/issues/2060): New cop `Style/RescueEnsureAlignment` checks for bad alignment of `rescue` and `ensure` keywords. ([@lumeet][])
* New cop `Style/OptionalArguments` checks for optional arguments that do not appear at the end of an argument list. ([@rrosenblum][])
* New cop `Lint/CircularArgumentReference` checks for "circular argument references" in keyword arguments, which Ruby 2.2 warns against. ([@maxjacobson][], [@sliuu][])
* [#2030](https://github.com/rubocop/rubocop/issues/2030): New cop `Style/OptionHash` checks for option hashes and encourages changing them to keyword arguments (disabled by default). ([@maxjacobson][])

### Changes

* [#2052](https://github.com/rubocop/rubocop/pull/2052): `Style/RescueModifier` uses token stream to identify offenses. ([@urbanautomaton][])
* Rename `Rails/Date` and `Rails/TimeZone` style names to "strict" and "flexible" and make "flexible" to be default. ([@palkan][])
* [#2035](https://github.com/rubocop/rubocop/issues/2035): `Style/ExtraSpacing` is now enabled by default and has a configuration parameter `AllowForAlignment` that is `true` by default, making it allow extra spacing if it's used for alignment purposes. ([@jonas054][])

### Bugs fixed

* [#2014](https://github.com/rubocop/rubocop/pull/2014): Fix `Style/TrivialAccessors` to support AllowPredicates: false. ([@gotrevor][])
* [#1988](https://github.com/rubocop/rubocop/issues/1988): Fix bug in `Style/ParallelAssignment` when assigning from `Module::CONSTANT`. ([@rrosenblum][])
* [#1995](https://github.com/rubocop/rubocop/pull/1995): Improve message for `Rails/TimeZone`. ([@palkan][])
* [#1977](https://github.com/rubocop/rubocop/issues/1977): Fix bugs in `Rails/Date` and `Rails/TimeZone` when using namespaced Time/Date. ([@palkan][])
* [#1973](https://github.com/rubocop/rubocop/issues/1973): Do not register an offense in `Performance/Detect` when `select` is called on `Enumerable::Lazy`. ([@palkan][])
* [#2015](https://github.com/rubocop/rubocop/issues/2015): Fix bug occurring for auto-correction of a misaligned `end` in a file with only one method. ([@jonas054][])
* Allow string interpolation segments inside single quoted string literals when double quotes are preferred. ([@segiddins][])
* [#2026](https://github.com/rubocop/rubocop/issues/2026): Allow `Time.current` when style is "acceptable". ([@palkan][])
* [#2029](https://github.com/rubocop/rubocop/issues/2029): Fix bug where `Style/RedundantReturn` auto-corrects returning implicit hashes to invalid syntax. ([@rrosenblum][])
* [#2021](https://github.com/rubocop/rubocop/issues/2021): Fix bug in `Style/BlockDelimiters` when a `semantic` expression is used in an array or a range. ([@lumeet][])
* [#1992](https://github.com/rubocop/rubocop/issues/1992): Allow parentheses in assignment to a variable with the same name as the method's in `Style/MethodCallParentheses`. ([@lumeet][])
* [#2045](https://github.com/rubocop/rubocop/issues/2045): Fix crash in `Style/IndentationWidth` when using `private_class_method def self.foo` syntax. ([@unmanbearpig][])
* [#2006](https://github.com/rubocop/rubocop/issues/2006): Fix crash in `Style/FirstParameterIndentation` in case of nested offenses. ([@unmanbearpig][])
* [#2059](https://github.com/rubocop/rubocop/issues/2059): Don't check for trivial accessors in modules. ([@bbatsov][])
* Add proper punctuation to the end of offense messages, where it is missing. ([@lumeet][])
* [#2071](https://github.com/rubocop/rubocop/pull/2071): Keep line breaks in place on WordArray auto-correct. ([@unmanbearpig][])
* [#2075](https://github.com/rubocop/rubocop/pull/2075): Properly correct `Style/PercentLiteralDelimiters` with escape characters in them. ([@rrosenblum][])
* [#2023](https://github.com/rubocop/rubocop/issues/2023): Avoid auto-correction corruption in `IndentationWidth`. ([@jonas054][])
* [#2080](https://github.com/rubocop/rubocop/issues/2080): Properly parse code in `Performance/Count` when calling `select..count` in a class that extends an enumerable. ([@rrosenblum][])
* [#2093](https://github.com/rubocop/rubocop/issues/2093): Fix bug in `Style/OneLineConditional` which should not raise an offense with an 'if/then/end' statement. ([@sliuu][])

## 0.32.1 (2015-06-24)

### New features

* `Debugger` cop now checks catches methods called with arguments. ([@crazydog115][])

### Bugs fixed

* Make it possible to disable `Lint/UnneededDisable`. ([@jonas054][])
* [#1958](https://github.com/rubocop/rubocop/issues/1958): Show name of `Lint/UnneededDisable` when `-D/--display-cop-names` is given. ([@jonas054][])
* Do not show `Style/NonNilCheck` offenses as corrected when the source code is not modified. ([@rrosenblum][])
* Fix auto-correct in `Style/RedundantReturn` when `return` has no arguments. ([@lumeet][])
* [#1955](https://github.com/rubocop/rubocop/issues/1955): Fix false positive for `Style/TrailingComma` cop. ([@mattjmcnaughton][])
* [#1928](https://github.com/rubocop/rubocop/issues/1928): Avoid auto-correcting two alignment offenses in the same area at the same time. ([@jonas054][])
* [#1964](https://github.com/rubocop/rubocop/issues/1964): Fix `RedundantBegin` auto-correct issue with comments by doing a smaller correction. ([@jonas054][])
* [#1978](https://github.com/rubocop/rubocop/pull/1978): Don't count disabled offences if fail-level is auto-correct. ([@sch1zo][])
* [#1986](https://github.com/rubocop/rubocop/pull/1986): Fix Date false positives on variables. ([@palkan][])

### Changes

* [#1708](https://github.com/rubocop/rubocop/issues/1708): Improve message for `FirstParameterIndentation`. ([@tejasbubane][])
* [#1959](https://github.com/rubocop/rubocop/issues/1959): Allow `Lint/UnneededDisable` to be inline disabled. ([@rrosenblum][])

## 0.32.0 (2015-06-06)

### New features

* Adjust behavior of `TrailingComma` cop to account for multi-line hashes nested within method calls. ([@panthomakos][])
* [#1719](https://github.com/rubocop/rubocop/pull/1719): Display an error and abort the program if input file can't be found. ([@matugm][])
* New cop `SpaceInsideStringInterpolation` checks for spaces within string interpolations. ([@glasnt][])
* New cop `NestedMethodDefinition` checks for method definitions inside other methods. ([@ojab][])
* `LiteralInInterpolation` cop does auto-correction. ([@tmr08c][])
* [#1865](https://github.com/rubocop/rubocop/issues/1865): New cop `Lint/UnneededDisable` checks for `rubocop:disable` comments that can be removed. ([@jonas054][])
* `EmptyElse` cop does auto-correction. ([@lumeet][])
* Show reference links when displaying style guide links. ([@rrosenblum][])
* `Debugger` cop now checks for the Capybara debug method `save_screenshot`. ([@crazydog115][])
* [#1282](https://github.com/rubocop/rubocop/issues/1282): `CaseIndentation` cop does auto-correction. ([@lumeet][])
* [#1928](https://github.com/rubocop/rubocop/issues/1928): Do auto-correction one offense at a time (rather than one cop at a time) if there are tabs in the code. ([@jonas054][])

### Changes

* Prefer `SpaceInsideBlockBraces` to `SpaceBeforeSemicolon` and `SpaceAfterSemicolon` to avoid an infinite loop when auto-correcting. ([@lumeet][])
* [#1873](https://github.com/rubocop/rubocop/issues/1873): Move `ParallelAssignment` cop from Performance to Style. ([@rrosenblum][])
* Add `getlocal` to acceptable methods of `Rails/TimeZone`. ([@ojab][])
* [#1851](https://github.com/rubocop/rubocop/issues/1851), [#1948](https://github.com/rubocop/rubocop/issues/1948): Change offense message for `ClassLength` and `ModuleLength` to match that of `MethodLength`. ([@bquorning][])

### Bugs fixed

* Don't count required keyword args when specifying `CountKeywordArgs: false` for `ParameterLists`. ([@sumeet][])
* [#1879](https://github.com/rubocop/rubocop/issues/1879): Avoid auto-correcting hash with trailing comma into invalid code in `BracesAroundHashParameters`. ([@jonas054][])
* [#1868](https://github.com/rubocop/rubocop/issues/1868): Do not register an offense in `Performance/Count` when `select` is called with symbols or strings as the parameters. ([@rrosenblum][])
* `Sample` rewritten to properly handle shuffle randomness source, first/last params and non-literal ranges. ([@chastell][])
* [#1873](https://github.com/rubocop/rubocop/issues/1873): Modify `ParallelAssignment` to properly auto-correct when the assignment is protected by a modifier statement. ([@rrosenblum][])
* Configure `ParallelAssignment` to work with non-standard `IndentationWidths`. ([@rrosenblum][])
* [#1899](https://github.com/rubocop/rubocop/issues/1899): Be careful about comments when auto-correcting in `BracesAroundHashParameters`. ([@jonas054][])
* [#1897](https://github.com/rubocop/rubocop/issues/1897): Don't report that semicolon separated statements can be converted to modifier form in `IfUnlessModifier` (and don't auto-correct them). ([@jonas054][])
* [#1644](https://github.com/rubocop/rubocop/issues/1644): Don't search the entire file system when a folder is named `,` (fix for jruby and rbx). ([@rrosenblum][])
* [#1803](https://github.com/rubocop/rubocop/issues/1803): Don't warn for `return` from `lambda` block in `NonLocalExitFromIterator`. ([@ypresto][])
* [#1905](https://github.com/rubocop/rubocop/issues/1905): Ignore sparse and trailing comments in `Style/Documentation`. ([@RGBD][])
* [#1923](https://github.com/rubocop/rubocop/issues/1923): Handle properly `for` without body in `Style/Next`. ([@bbatsov][])
* [#1901](https://github.com/rubocop/rubocop/issues/1901): Do not auto correct comments that are missing a note. ([@rrosenblum][])
* [#1926](https://github.com/rubocop/rubocop/issues/1926): Fix crash in `Style/AlignHash` when correcting a hash with a splat in it. ([@rrosenblum][])
* [#1935](https://github.com/rubocop/rubocop/issues/1935): Allow `Symbol#to_proc` blocks in Performance/Size. ([@m1foley][])

## 0.31.0 (2015-05-05)

### New features

* `Rails/TimeZone` emits acceptable methods on a violation when `EnforcedStyle` is `:acceptable`. ([@l8nite][])
* Recognize rackup file (config.ru) out of the box. ([@carhartl][])
* [#1788](https://github.com/rubocop/rubocop/pull/1788): New cop `ModuleLength` checks for overly long module definitions. ([@sdeframond][])
* New cop `Performance/Count` to convert `Enumerable#select...size`, `Enumerable#reject...size`, `Enumerable#select...count`, `Enumerable#reject...count` `Enumerable#select...length`, and `Enumerable#reject...length` to `Enumerable#count`. ([@rrosenblum][])
* `CommentAnnotation` cop does auto-correction. ([@dylandavidson][])
* New cop `Style/TrailingUnderscoreVariable` to remove trailing underscore variables from mass assignment. ([@rrosenblum][])
* [#1136](https://github.com/rubocop/rubocop/issues/1136): New cop `Performance/ParallelAssignment` to avoid usages of unnecessary parallel assignment. ([@rrosenblum][])
* [#1278](https://github.com/rubocop/rubocop/issues/1278): `DefEndAlignment` and `EndAlignment` cops do auto-correction. ([@lumeet][])
* `IndentationWidth` cop follows the `AlignWith` option of the `DefEndAlignment` cop. ([@lumeet][])
* [#1837](https://github.com/rubocop/rubocop/issues/1837): New cop `EachWithObjectArgument` checks that `each_with_object` isn't called with an immutable object as argument. ([@jonas054][])
* `ArrayJoin` cop does auto-correction. ([@tmr08c][])

### Bugs fixed

* [#1816](https://github.com/rubocop/rubocop/issues/1816): Fix bug in `Sample` when calling `#shuffle` with something other than an element selector. ([@rrosenblum][])
* [#1768](https://github.com/rubocop/rubocop/pull/1768): `DefEndAlignment` recognizes preceding `private_class_method` or `public_class_method` before `def`. ([@til][])
* [#1820](https://github.com/rubocop/rubocop/issues/1820): Correct the logic in `AlignHash` for when to ignore a key because it's not on its own line. ([@jonas054][])
* [#1829](https://github.com/rubocop/rubocop/pull/1829): Fix bug in `Sample` and `FlatMap` that would cause them to report having been auto-corrected when they were not. ([@rrosenblum][])
* [#1832](https://github.com/rubocop/rubocop/pull/1832): Fix bug in `UnusedMethodArgument` that would cause them to report having been auto-corrected when they were not. ([@jonas054][])
* [#1834](https://github.com/rubocop/rubocop/issues/1834): Support only boolean values for `Auto-Correct` configuration parameter, and remove warning for unknown parameter. ([@jonas054][])
* [#1843](https://github.com/rubocop/rubocop/issues/1843): Fix crash in `TrailingBlankLines` when a file ends with a block comment without final newline. ([@jonas054][])
* [#1849](https://github.com/rubocop/rubocop/issues/1849): Fix bug where you cannot have nested arrays in the Rake task configuration. ([@rrosenblum][])
* Fix bug in `MultilineTernaryOperator` where it will not register an offense when only the false branch is on a separate line. ([@rrosenblum][])
* Fix crash in `MultilineBlockLayout` when using new lambda literal syntax without parentheses. ([@hbd225][])
* [#1859](https://github.com/rubocop/rubocop/pull/1859): Fix bugs in `IfUnlessModifier` concerning comments and empty lines. ([@jonas054][])
* Fix handling of trailing comma in `SpaceAroundBlockParameters` and `SpaceAfterComma`. ([@lumeet][])

## 0.30.1 (2015-04-21)

### Bugs fixed

* [#1691](https://github.com/rubocop/rubocop/issues/1691): For assignments with line break after `=`, use `keyword` alignment in `EndAlignment` regardless of configured style. ([@jonas054][])
* [#1769](https://github.com/rubocop/rubocop/issues/1769): Fix bug where `LiteralInInterpolation` registers an offense for interpolation of `__LINE__`. ([@rrosenblum][])
* [#1773](https://github.com/rubocop/rubocop/pull/1773): Fix typo ('strptime' -> 'strftime') in `Rails/TimeZone`. ([@palkan][])
* [#1777](https://github.com/rubocop/rubocop/pull/1777): Fix offense message from Rails/TimeZone. ([@mzp][])
* [#1784](https://github.com/rubocop/rubocop/pull/1784): Add an explicit error message when config contains an empty section. ([@bankair][])
* [#1791](https://github.com/rubocop/rubocop/pull/1791): Fix auto-correction of `PercentLiteralDelimiters` with no content. ([@cshaffer][])
* Fix handling of `while` and `until` with assignment in `IndentationWidth`. ([@lumeet][])
* [#1793](https://github.com/rubocop/rubocop/pull/1793): Fix bug in `TrailingComma` that caused `,` in comment to count as a trailing comma. ([@jonas054][])
* [#1765](https://github.com/rubocop/rubocop/pull/1765): Update 1.9 hash to stop triggering when the symbol is not valid in the 1.9 hash syntax. ([@crimsonknave][])
* [#1806](https://github.com/rubocop/rubocop/issues/1806): Require a newer version of `parser` and use its corrected solution for comment association in `Style/Documentation`. ([@jonas054][])
* [#1792](https://github.com/rubocop/rubocop/issues/1792): Fix bugs in `Sample` that did not account for array selectors with a range and passing random to shuffle. ([@rrosenblum][])
* [#1770](https://github.com/rubocop/rubocop/pull/1770): Add more acceptable methods to `Rails/TimeZone` (`utc`, `localtime`, `to_i`, `iso8601` etc). ([@palkan][])
* [#1767](https://github.com/rubocop/rubocop/pull/1767): Do not register offenses on non-enumerable select/find_all by `Performance/Detect`. ([@palkan][])
* [#1795](https://github.com/rubocop/rubocop/pull/1795): Fix bug in `TrailingBlankLines` that caused a crash for files containing only newlines. ([@renuo][])

## 0.30.0 (2015-04-06)

### New features

* [#1600](https://github.com/rubocop/rubocop/issues/1600): Add `line_count_based` and `semantic` styles to the `BlockDelimiters` (formerly `Blocks`) cop. ([@clowder][], [@mudge][])
* [#1712](https://github.com/rubocop/rubocop/pull/1712): Set `Offense#corrected?` to `true`, `false`, or `nil` when it was, wasn't, or can't be auto-corrected, respectively. ([@vassilevsky][])
* [#1669](https://github.com/rubocop/rubocop/pull/1669): Add command-line switch `--display-style-guide`. ([@marxarelli][])
* [#1405](https://github.com/rubocop/rubocop/issues/1405): Add Rails TimeZone and Date cops. ([@palkan][])
* [#1641](https://github.com/rubocop/rubocop/pull/1641): Add ruby19_no_mixed_keys style to `HashStyle` cop. ([@iainbeeston][])
* [#1604](https://github.com/rubocop/rubocop/issues/1604): Add `IgnoreClassMethods` option to `TrivialAccessors` cop. ([@bbatsov][])
* [#1651](https://github.com/rubocop/rubocop/issues/1651): The `Style/SpaceAroundOperators` cop now also detects extra spaces around operators. A list of operators that *may* be surrounded by multiple spaces is configurable. ([@bquorning][])
* Add auto-correct to `Encoding` cop. ([@rrosenblum][])
* [#1621](https://github.com/rubocop/rubocop/issues/1621): `TrailingComma` has a new style `consistent_comma`. ([@tamird][])
* [#1611](https://github.com/rubocop/rubocop/issues/1611): Add `empty`, `nil`, and `both` `SupportedStyles` to `EmptyElse` cop. Default is `both`. ([@rrosenblum][])
* [#1611](https://github.com/rubocop/rubocop/issues/1611): Add new `MissingElse` cop. Default is to have this cop be disabled. ([@rrosenblum][])
* [#1602](https://github.com/rubocop/rubocop/issues/1602): Add support for `# :nodoc` in `Documentation`. ([@lumeet][])
* [#1437](https://github.com/rubocop/rubocop/issues/1437): Modify `HashSyntax` cop to allow the use of hash rockets for hashes that have symbol values when using ruby19 syntax. ([@rrosenblum][])
* New cop `Style/SymbolLiteral` makes sure you're not using the string within symbol syntax unless it's needed. ([@bbatsov][])
* [#1657](https://github.com/rubocop/rubocop/issues/1657): Auto-Correct can be turned off on a specific cop via the configuration. ([@jdoconnor][])
* New cop `Style/AutoResourceCleanup` suggests the use of block taking versions of methods that do resource cleanup. ([@bbatsov][])
* [#1275](https://github.com/rubocop/rubocop/issues/1275): `WhileUntilModifier` cop does auto-correction. ([@lumeet][])
* New cop `Performance/ReverseEach` to convert `reverse.each` to `reverse_each`. ([@rrosenblum][])
* [#1281](https://github.com/rubocop/rubocop/issues/1281): `IfUnlessModifier` cop does auto-correction. ([@lumeet][])
* New cop `Performance/Detect` to detect usage of `select.first`, `select.last`, `find_all.first`, and `find_all.last` and convert them to use `detect` instead. ([@palkan][], [@rrosenblum][])
* [#1728](https://github.com/rubocop/rubocop/pull/1728): New cop `NonLocalExitFromIterator` checks for misused `return` in block. ([@ypresto][])
* New cop `Performance/Size` to convert calls to `count` on `Array` and `Hash` to `size`. ([@rrosenblum][])
* New cop `Performance/Sample` to convert usages of `shuffle.first`, `shuffle.last`, and `shuffle[Fixnum]` to `sample`. ([@rrosenblum][])
* New cop `Performance/FlatMap` to convert `Enumerable#map...Array#flatten` and `Enumerable#collect...Array#flatten` to `Enumerable#flat_map`. ([@rrosenblum][])
* [#1144](https://github.com/rubocop/rubocop/issues/1144): New cop `ClosingParenthesisIndentation` checks the indentation of hanging closing parentheses. ([@jonas054][])
* New Rails cop `FindBy` identifies usages of `where.first` and `where.take`. ([@bbatsov][])
* New Rails cop `FindEach` identifies usages of `all.each`. ([@bbatsov][])
* [#1342](https://github.com/rubocop/rubocop/issues/1342): `IndentationConsistency` is now configurable with the styles `normal` and `rails`. ([@jonas054][])

### Bugs fixed

* [#1705](https://github.com/rubocop/rubocop/issues/1705): Fix crash when reporting offenses of `MissingElse` cop. ([@gerry3][])
* [#1659](https://github.com/rubocop/rubocop/pull/1659): Fix stack overflow with JRuby and Windows 8, during initial config validation. ([@pimterry][])
* [#1694](https://github.com/rubocop/rubocop/issues/1694): Ignore methods with a `blockarg` in `TrivialAccessors`. ([@bbatsov][])
* [#1617](https://github.com/rubocop/rubocop/issues/1617): Always read the html output template using utf-8. ([@bbatsov][])
* [#1684](https://github.com/rubocop/rubocop/issues/1684): Ignore symbol keys like `:"string"` in `HashSyntax`. ([@bbatsov][])
* Handle explicit `begin` blocks in `Lint/Void`. ([@bbatsov][])
* Handle symbols in `Lint/Void`. ([@bbatsov][])
* [#1695](https://github.com/rubocop/rubocop/pull/1695): Fix bug with `--auto-gen-config` and `SpaceInsideBlockBraces`. ([@meganemura][])
* Correct issues with whitespace around multi-line lambda arguments. ([@zvkemp][])
* [#1579](https://github.com/rubocop/rubocop/issues/1579): Fix handling of similar-looking blocks in `BlockAlignment`. ([@lumeet][])
* [#1676](https://github.com/rubocop/rubocop/pull/1676): Fix auto-correct in `Lambda` when a new multi-line lambda is used as an argument. ([@lumeet][])
* [#1656](https://github.com/rubocop/rubocop/issues/1656): Fix bug that would include hidden directories implicitly. ([@jonas054][])
* [#1728](https://github.com/rubocop/rubocop/pull/1728): Fix bug in `LiteralInInterpolation` and `AssignmentInCondition`. ([@ypresto][])
* [#1735](https://github.com/rubocop/rubocop/issues/1735): Handle trailing space in `LineEndConcatenation` auto-correct. ([@jonas054][])
* [#1750](https://github.com/rubocop/rubocop/issues/1750): Escape offending code lines output by the HTML formatter in case they contain markup. ([@jonas054][])
* [#1541](https://github.com/rubocop/rubocop/issues/1541): No inspection of text that follows `__END__`. ([@jonas054][])
* Fix comment detection in `Style/Documentation`. ([@lumeet][])
* [#1637](https://github.com/rubocop/rubocop/issues/1637): Fix handling of `binding` calls in `UnusedBlockArgument` and `UnusedMethodArgument`. ([@lumeet][])

### Changes

* [#1397](https://github.com/rubocop/rubocop/issues/1397): `UnneededPercentX` renamed to `CommandLiteral`. The cop can be configured to enforce using either `%x` or backticks around command literals, or using `%x` around multi-line commands and backticks around single-line commands. The cop ignores heredoc commands. ([@bquorning][])
* [#1020](https://github.com/rubocop/rubocop/issues/1020): Removed the `MaxSlashes` configuration option for `RegexpLiteral`. Instead, the cop can be configured to enforce using either `%r` or slashes around regular expressions, or using `%r` around multi-line regexes and slashes around single-line regexes. ([@bquorning][])
* [#1734](https://github.com/rubocop/rubocop/issues/1734): The default exclusion of hidden directories has been optimized for speed. ([@jonas054][])
* [#1673](https://github.com/rubocop/rubocop/issues/1673): `Style/TrivialAccessors` now requires matching names by default. ([@bbatsov][])

## 0.29.1 (2015-02-13)

### Bugs fixed

* [#1638](https://github.com/rubocop/rubocop/issues/1638): Use Parser functionality rather than regular expressions for matching comments in `FirstParameterIndentation`. ([@jonas054][])
* [#1642](https://github.com/rubocop/rubocop/issues/1642): Raise the correct exception if the configuration file is malformed. ([@bquorning][])
* [#1647](https://github.com/rubocop/rubocop/issues/1647): Skip `SpaceAroundBlockParameters` when lambda has no argument. ([@eitoball][])
* [#1649](https://github.com/rubocop/rubocop/issues/1649): Handle exception assignments in `UselessSetterCall`. ([@bbatsov][])
* [#1644](https://github.com/rubocop/rubocop/issues/1644): Don't search the entire file system when a folder is named `,`. ([@bquorning][])

## 0.29.0 (2015-02-05)

### New features

* [#1430](https://github.com/rubocop/rubocop/issues/1430): Add `--except` option for disabling cops on the command line. ([@jonas054][])
* [#1506](https://github.com/rubocop/rubocop/pull/1506): Add auto-correct from `EvenOdd` cop. ([@blainesch][])
* [#1507](https://github.com/rubocop/rubocop/issues/1507): `Debugger` cop now checks for the Capybara debug methods `save_and_open_page` and `save_and_open_screenshot`. ([@rrosenblum][])
* [#1539](https://github.com/rubocop/rubocop/pull/1539): Implement auto-correction for Rails/ReadWriteAttribute cop. ([@huerlisi][])
* [#1324](https://github.com/rubocop/rubocop/issues/1324): Add `AllCops/DisplayCopNames` configuration option for showing cop names in reports, like `--display-cop-names`. ([@jonas054][])
* [#1271](https://github.com/rubocop/rubocop/issues/1271): `Lambda` cop does auto-correction. ([@lumeet][])
* [#1284](https://github.com/rubocop/rubocop/issues/1284): Support namespaces, e.g. `Lint`, in the arguments to `--only` and `--except`. ([@jonas054][])
* [#1276](https://github.com/rubocop/rubocop/issues/1276): `SelfAssignment` cop does auto-correction. ([@lumeet][])
* Add auto-correct to `RedundantException`. ([@mattjmcnaughton][])
* [#1571](https://github.com/rubocop/rubocop/pull/1571): New cop `StructInheritance` checks for inheritance from Struct.new. ([@mmozuras][])
* [#1575](https://github.com/rubocop/rubocop/issues/1575): New cop `DuplicateMethods` points out duplicate method name in class and module. ([@d4rk5eed][])
* [#1144](https://github.com/rubocop/rubocop/issues/1144): New cop `FirstParameterIndentation` checks the indentation of the first parameter in a method call. ([@jonas054][])
* [#1627](https://github.com/rubocop/rubocop/issues/1627): New cop `SpaceAroundBlockParameters` checks the spacing inside and after block parameters pipes. ([@jonas054][])

### Changes

* [#1492](https://github.com/rubocop/rubocop/pull/1492): Abort when auto-correct causes an infinite loop. ([@dblock][])
* Options `-e`/`--emacs` and `-s`/`--silent` are no longer recognized. Using them will now raise an error. ([@bquorning][])
* [#1565](https://github.com/rubocop/rubocop/issues/1565): Let `--fail-level A` cause exit with error if all offenses are auto-corrected. ([@jonas054][])
* [#1309](https://github.com/rubocop/rubocop/issues/1309): Add argument handling to `MultilineBlockLayout`. ([@lumeet][])

### Bugs fixed

* [#1634](https://github.com/rubocop/rubocop/pull/1634): Fix `PerlBackrefs` cop auto-corrections to not raise. ([@cshaffer][])
* [#1553](https://github.com/rubocop/rubocop/pull/1553): Fix bug where `Style/EmptyLinesAroundAccessModifier` interfered with `Style/EmptyLinesAroundBlockBody` when there is and access modifier at the beginning of a block. ([@volkert][])
* Handle element assignment in `Lint/AssignmentInCondition`. ([@jonas054][])
* [#1484](https://github.com/rubocop/rubocop/issues/1484): Fix `EmptyLinesAroundAccessModifier` incorrectly finding a violation inside method calls with names identical to an access modifier. ([@dblock][])
* Fix bug concerning `Exclude` properties inherited from a higher directory level. ([@jonas054][])
* [#1500](https://github.com/rubocop/rubocop/issues/1500): Fix crashing `--auto-correct --only IndentationWidth`. ([@jonas054][])
* [#1512](https://github.com/rubocop/rubocop/issues/1512): Fix false negative for typical string formatting examples. ([@kakutani][], [@jonas054][])
* [#1504](https://github.com/rubocop/rubocop/issues/1504): Fail with a meaningful error if the configuration file is malformed. ([@bquorning][])
* Fix bug where `auto_correct` Rake tasks does not take in the options specified in its parent task. ([@rrosenblum][])
* [#1054](https://github.com/rubocop/rubocop/issues/1054): Handle comments within concatenated strings in `LineEndConcatenation`. ([@yujinakayama][], [@jonas054][])
* [#1527](https://github.com/rubocop/rubocop/issues/1527): Make auto-correct `BracesAroundHashParameter` leave the correct number of spaces. ([@mattjmcnaughton][])
* [#1547](https://github.com/rubocop/rubocop/issues/1547): Don't print `[Corrected]` when auto-correction was avoided in `Style/Semicolon`. ([@jonas054][])
* [#1573](https://github.com/rubocop/rubocop/issues/1573): Fix assignment-related auto-correction for `BlockAlignment`. ([@lumeet][])
* [#1587](https://github.com/rubocop/rubocop/pull/1587): Exit with exit code 1 if there were errors ("crashing" cops). ([@jonas054][])
* [#1574](https://github.com/rubocop/rubocop/issues/1574): Avoid auto-correcting `Hash.new` to `{}` when braces would be interpreted as a block. ([@jonas054][])
* [#1591](https://github.com/rubocop/rubocop/issues/1591): Don't check parameters inside `[]` in `MultilineOperationIndentation`. ([@jonas054][])
* [#1509](https://github.com/rubocop/rubocop/issues/1509): Ignore class methods in `Rails/Delegate`. ([@bbatsov][])
* [#1594](https://github.com/rubocop/rubocop/issues/1594): Fix `@example` warnings in Yard Doc documentation generation. ([@mattjmcnaughton][])
* [#1598](https://github.com/rubocop/rubocop/issues/1598): Fix bug in file inclusion when running from another directory. ([@jonas054][])
* [#1580](https://github.com/rubocop/rubocop/issues/1580): Don't print `[Corrected]` when auto-correction was avoided in `TrivialAccessors`. ([@lumeet][])
* [#1612](https://github.com/rubocop/rubocop/issues/1612): Allow `expand_path` on `inherit_from` in `.rubocop.yml`. ([@mattjmcnaughton][])
* [#1610](https://github.com/rubocop/rubocop/issues/1610): Check that class method names actually match the name of the containing class/module in `Style/ClassMethods`. ([@bbatsov][])

## 0.28.0 (2014-12-10)

### New features

* [#1450](https://github.com/rubocop/rubocop/issues/1450): New cop `ExtraSpacing` points out unnecessary spacing in files. ([@blainesch][])
* New cop `EmptyLinesAroundBlockBody` provides same functionality as the EmptyLinesAround(Class|Method|Module)Body but for blocks. ([@jcarbo][])
* New cop `Style/EmptyElse` checks for empty `else`-clauses. ([@Koronen][])
* [#1454](https://github.com/rubocop/rubocop/issues/1454): New `--only-guide-cops` and `AllCops/StyleGuideCopsOnly` options that will only enforce cops that link to a style guide. ([@marxarelli][])

### Changes

* [#801](https://github.com/rubocop/rubocop/issues/801): New style `context_dependent` for `Style/BracesAroundHashParameters` looks at preceding parameter to determine if braces should be used for final parameter. ([@jonas054][])
* [#1427](https://github.com/rubocop/rubocop/issues/1427): Excluding directories on the top level is now done earlier, so that these file trees are not searched, thus saving time when inspecting projects with many excluded files. ([@jonas054][])
* [#1325](https://github.com/rubocop/rubocop/issues/1325): When running with `--auto-correct`, only offenses *that cannot be corrected* will result in a non-zero exit code. ([@jonas054][])
* [#1445](https://github.com/rubocop/rubocop/issues/1445): Allow sprockets directive comments (starting with `#=`) in `Style/LeadingCommentSpace`. ([@bbatsov][])

### Bugs fixed

* Fix `%W[]` auto corrected to `%w(]`. ([@toy][])
* Fix Style/ElseAlignment Cop to find the right parent on def/rescue/else/ensure/end. ([@oneamtu][])
* [#1181](https://github.com/rubocop/rubocop/issues/1181): *(fix again)* `Style/StringLiterals` cop stays away from strings inside interpolated expressions. ([@jonas054][])
* [#1441](https://github.com/rubocop/rubocop/issues/1441): Correct the logic used by `Style/Blocks` and other cops to determine if an auto-correction would alter the meaning of the code. ([@jonas054][])
* [#1449](https://github.com/rubocop/rubocop/issues/1449): Handle the case in `MultilineOperationIndentation` where instances of both correct style and unrecognized (plain wrong) style are detected during an `--auto-gen-config` run. ([@jonas054][])
* [#1456](https://github.com/rubocop/rubocop/pull/1456): Fix auto-correct in `SymbolProc` when there are multiple offenses on the same line. ([@jcarbo][])
* [#1459](https://github.com/rubocop/rubocop/issues/1459): Handle parenthesis around the condition in `--auto-correct` for `NegatedWhile`. ([@jonas054][])
* [#1465](https://github.com/rubocop/rubocop/issues/1465): Fix auto-correct of code like `#$1` in `PerlBackrefs`. ([@bbatsov][])
* Fix auto-correct of code like `#$:` in `SpecialGlobalVars`. ([@bbatsov][])
* [#1466](https://github.com/rubocop/rubocop/issues/1466): Allow leading underscore for unused parameters in `SingleLineBlockParams`. ([@jonas054][])
* [#1470](https://github.com/rubocop/rubocop/issues/1470): Handle `elsif` + `else` in `ElseAlignment`. ([@jonas054][])
* [#1474](https://github.com/rubocop/rubocop/issues/1474): Multiline string with both `<<` and `\` caught by `Style/LineEndConcatenation` cop. ([@katieschilling][])
* [#1485](https://github.com/rubocop/rubocop/issues/1485): Ignore procs in `SymbolProc`. ([@bbatsov][])
* [#1473](https://github.com/rubocop/rubocop/issues/1473): `Style/MultilineOperationIndentation` doesn't recognize assignment to array/hash element. ([@jonas054][])

## 0.27.1 (2014-11-08)

### Changes

* [#1343](https://github.com/rubocop/rubocop/issues/1343): Remove auto-correct from `RescueException` cop. ([@bbatsov][])
* [#1425](https://github.com/rubocop/rubocop/issues/1425): `AllCops/Include` configuration parameters are only taken from the project `.rubocop.yml` and files it inherits from, not from `.rubocop.yml` files in subdirectories. ([@jonas054][])

### Bugs fixed

* [#1411](https://github.com/rubocop/rubocop/issues/1411): Handle lambda calls without a selector in `MultilineOperationIndentation`. ([@bbatsov][])
* [#1401](https://github.com/rubocop/rubocop/issues/1401): Files in hidden directories, i.e. ones beginning with dot, can now be selected through configuration, but are still not included by default. ([@jonas054][])
* [#1415](https://github.com/rubocop/rubocop/issues/1415): String literals concatenated with backslashes are now handled correctly by `StringLiteralsInInterpolation`. ([@jonas054][])
* [#1416](https://github.com/rubocop/rubocop/issues/1416): Fix handling of `begin/rescue/else/end` in `ElseAlignment`. ([@jonas054][])
* [#1413](https://github.com/rubocop/rubocop/issues/1413): Support empty elsif branches in `MultilineIfThen`. ([@janraasch][], [@jonas054][])
* [#1406](https://github.com/rubocop/rubocop/issues/1406): Allow a newline in `SpaceInsideRangeLiteral`. ([@bbatsov][])

## 0.27.0 (2014-10-30)

### New features

* [#1348](https://github.com/rubocop/rubocop/issues/1348): New cop `ElseAlignment` checks alignment of `else` and `elsif` keywords. ([@jonas054][])
* [#1321](https://github.com/rubocop/rubocop/issues/1321): New cop `MultilineOperationIndentation` checks indentation/alignment of binary operations if they span more than one line. ([@jonas054][])
* [#1077](https://github.com/rubocop/rubocop/issues/1077): New cop `Metrics/AbcSize` checks the ABC metric, based on assignments, branches, and conditions. ([@jonas054][], [@jfelchner][])
* [#1352](https://github.com/rubocop/rubocop/issues/1352): `WordArray` is now configurable with the `WordRegex` option. ([@bquorning][])
* [#1181](https://github.com/rubocop/rubocop/issues/1181): New cop `Style/StringLiteralsInInterpolation` checks quotes inside interpolated expressions in strings. ([@jonas054][])
* [#872](https://github.com/rubocop/rubocop/issues/872): `Style/IndentationWidth` is now configurable with the `Width` option. ([@jonas054][])
* [#1396](https://github.com/rubocop/rubocop/issues/1396): Include `.opal` files by default. ([@bbatsov][])
* [#771](https://github.com/rubocop/rubocop/issues/771): Three new `Style` cops, `EmptyLinesAroundMethodBody` , `EmptyLinesAroundClassBody` , and `EmptyLinesAroundModuleBody` replace the `EmptyLinesAroundBody` cop. ([@jonas054][])

### Changes

* [#1084](https://github.com/rubocop/rubocop/issues/1084): Disabled `Style/CollectionMethods` by default. ([@bbatsov][])

### Bugs fixed

* `AlignHash` no longer skips multiline hashes that contain some elements on the same line. ([@mvz][])
* [#1349](https://github.com/rubocop/rubocop/issues/1349): `BracesAroundHashParameters` no longer cleans up whitespace in auto-correct, as these extra corrections are likely to interfere with other cops' corrections. ([@jonas054][])
* [#1350](https://github.com/rubocop/rubocop/issues/1350): Guard against `Blocks` cop introducing syntax errors in auto-correct. ([@jonas054][])
* [#1374](https://github.com/rubocop/rubocop/issues/1374): To eliminate interference, auto-correction is now done by one cop at a time, with saving and re-parsing in between. ([@jonas054][])
* [#1388](https://github.com/rubocop/rubocop/issues/1388): Fix a false positive in `FormatString`. ([@bbatsov][])
* [#1389](https://github.com/rubocop/rubocop/issues/1389): Make `--out` to create parent directories. ([@yous][])
* Refine HTML formatter. ([@yujinakayama][])
* [#1410](https://github.com/rubocop/rubocop/issues/1410): Handle specially Java primitive type references in `ColonMethodCall`. ([@bbatsov][])

## 0.26.1 (2014-09-18)

### Bugs fixed

* [#1326](https://github.com/rubocop/rubocop/issues/1326): Fix problem in `SpaceInsideParens` with detecting space inside parentheses used for grouping expressions. ([@jonas054][])
* [#1335](https://github.com/rubocop/rubocop/issues/1335): Restrict URI schemes permitted by `LineLength` when `AllowURI` is enabled. ([@smangelsdorf][])
* [#1339](https://github.com/rubocop/rubocop/issues/1339): Handle `eql?` and `equal?` in `OpMethod`. ([@bbatsov][])
* [#1340](https://github.com/rubocop/rubocop/issues/1340): Fix crash in `Style/SymbolProc` cop when the block calls a method with no explicit receiver. ([@smangelsdorf][])

## 0.26.0 (2014-09-03)

### New features

* New formatter `HTMLFormatter` generates a html file with a list of files with offences in them. ([@SkuliOskarsson][])
* New cop `SpaceInsideRangeLiteral` checks for spaces around `..` and `...` in range literals. ([@bbatsov][])
* New cop `InfiniteLoop` checks for places where `Kernel#loop` should have been used. ([@bbatsov][])
* New cop `SymbolProc` checks for places where a symbol can be used as proc instead of a block. ([@bbatsov][])
* `UselessAssignment` cop now suggests a variable name for possible typos if there's a variable-ish identifier similar to the unused variable name in the same scope. ([@yujinakayama][])
* `PredicateName` cop now has separate configurations for prefixes that denote predicate method names and predicate prefixes that should be removed. ([@bbatsov][])
* [#1272](https://github.com/rubocop/rubocop/issues/1272): `Tab` cop does auto-correction. ([@yous][])
* [#1274](https://github.com/rubocop/rubocop/issues/1274): `MultilineIfThen` cop does auto-correction. ([@bbatsov][])
* [#1279](https://github.com/rubocop/rubocop/issues/1279): `DotPosition` cop does auto-correction. ([@yous][])
* [#1277](https://github.com/rubocop/rubocop/issues/1277): `SpaceBeforeFirstArg` cop does auto-correction. ([@yous][])
* [#1310](https://github.com/rubocop/rubocop/issues/1310): Handle `module_function` in `Style/AccessModifierIndentation` and `Style/EmptyLinesAroundAccessModifier`. ([@bbatsov][])

### Changes

* [#1289](https://github.com/rubocop/rubocop/issues/1289): Use utf-8 as default encoding for inspected files. ([@jonas054][])
* [#1304](https://github.com/rubocop/rubocop/issues/1304): `Style/Encoding` is no longer a no-op on Ruby 2.x. It's also disabled by default, as projects not supporting 1.9 don't need to run it. ([@bbatsov][])

### Bugs fixed

* [#1263](https://github.com/rubocop/rubocop/issues/1263): Do not report `%W` literals with special escaped characters in `UnneededCapitalW`. ([@jonas054][])
* [#1286](https://github.com/rubocop/rubocop/issues/1286): Fix a false positive in `VariableName`. ([@bbatsov][])
* [#1211](https://github.com/rubocop/rubocop/issues/1211): Fix false negative in `UselessAssignment` when there's a reference for the variable in an exclusive branch. ([@yujinakayama][])
* [#1307](https://github.com/rubocop/rubocop/issues/1307): Fix auto-correction of `RedundantBegin` cop deletes new line. ([@yous][])
* [#1283](https://github.com/rubocop/rubocop/issues/1283): Fix auto-correction of indented expressions in `PercentLiteralDelimiters`. ([@jonas054][])
* [#1315](https://github.com/rubocop/rubocop/pull/1315): `BracesAroundHashParameters` auto-correction removes whitespace around content inside braces. ([@jspanjers][])
* [#1313](https://github.com/rubocop/rubocop/issues/1313): Fix a false positive in `AndOr` when enforced style is `conditionals`. ([@bbatsov][])
* Handle post-conditional `while` and `until` in `AndOr` when enforced style is `conditionals`. ([@yujinakayama][])
* [#1319](https://github.com/rubocop/rubocop/issues/1319): Fix a false positive in `FormatString`. ([@bbatsov][])
* [#1287](https://github.com/rubocop/rubocop/issues/1287): Allow missing blank line for EmptyLinesAroundAccessModifier if next line closes a block. ([@sch1zo][])

## 0.25.0 (2014-08-15)

### New features

* [#1259](https://github.com/rubocop/rubocop/issues/1259): Allow AndOr cop to auto-correct by adding method call parenthesis. ([@vrthra][])
* [#1232](https://github.com/rubocop/rubocop/issues/1232): Add EnforcedStyle option to cop `AndOr` to restrict it to conditionals. ([@vrthra][])
* [#835](https://github.com/rubocop/rubocop/issues/835): New cop `PercentQLiterals` checks if use of `%Q` and `%q` matches configuration. ([@jonas054][])
* [#835](https://github.com/rubocop/rubocop/issues/835): New cop `BarePercentLiterals` checks if usage of `%()` or `%Q()` matches configuration. ([@jonas054][])
* [#1079](https://github.com/rubocop/rubocop/pull/1079): New cop `MultilineBlockLayout` checks if a multiline block has an expression on the same line as the start of the block. ([@barunio][])
* [#1217](https://github.com/rubocop/rubocop/pull/1217): `Style::EmptyLinesAroundAccessModifier` cop does auto-correction. ([@tamird][])
* [#1220](https://github.com/rubocop/rubocop/issues/1220): New cop `PerceivedComplexity` is similar to `CyclomaticComplexity`, but reports when methods have a high complexity for a human reader. ([@jonas054][])
* `Debugger` cop now checks for `binding.pry_remote`. ([@yous][])
* [#1238](https://github.com/rubocop/rubocop/issues/1238): Add `MinBodyLength` option to `Next` cop. ([@bbatsov][])
* [#1241](https://github.com/rubocop/rubocop/issues/1241): `TrailingComma` cop does auto-correction. ([@yous][])
* [#1078](https://github.com/rubocop/rubocop/pull/1078): New cop `BlockEndNewline` checks if the end statement of a multiline block is on its own line. ([@barunio][])
* [#1078](https://github.com/rubocop/rubocop/pull/1078): `BlockAlignment` cop does auto-correction. ([@barunio][])

### Changes

* [#1220](https://github.com/rubocop/rubocop/issues/1220): New namespace `Metrics` created and some `Style` cops moved there. ([@jonas054][])
* Drop support for Ruby 1.9.2 in accordance with [the end of the security maintenance extension](https://www.ruby-lang.org/en/news/01-07-2014/eol-for-1-8-7-and-1-9-2/). ([@yujinakayama][])

### Bugs fixed

* [#1251](https://github.com/rubocop/rubocop/issues/1251): Fix `PercentLiteralDelimiters` auto-correct indentation error. ([@hannestyden][])
* [#1197](https://github.com/rubocop/rubocop/issues/1197): Fix false positive for new lambda syntax in `SpaceInsideBlockBraces`. ([@jonas054][])
* [#1201](https://github.com/rubocop/rubocop/issues/1201): Fix error at anonymous keyword splat arguments in some variable cops. ([@yujinakayama][])
* Fix false positive in `UnneededPercentQ` for `/%Q(something)/`. ([@jonas054][])
* Fix `SpacesInsideBrackets` for `Hash#[]` calls with spaces after left bracket. ([@mcls][])
* [#1210](https://github.com/rubocop/rubocop/issues/1210): Fix false positive in `UnneededPercentQ` for `%Q(\t")`. ([@jonas054][])
* Fix false positive in `UnneededPercentQ` for heredoc strings with `%q`/`%Q`. ([@jonas054][])
* [#1214](https://github.com/rubocop/rubocop/issues/1214): Don't destroy code in `AlignHash` auto-correct. ([@jonas054][])
* [#1219](https://github.com/rubocop/rubocop/issues/1219): Don't report bad alignment for `end` or `}` in `BlockAlignment` if it doesn't begin its line. ([@jonas054][])
* [#1227](https://github.com/rubocop/rubocop/issues/1227): Don't permanently change yamler as it can affect other apps. ([@jonas054][])
* [#1184](https://github.com/rubocop/rubocop/issues/1184): Fix a false positive in `Output` cop. ([@bbatsov][])
* [#1256](https://github.com/rubocop/rubocop/issues/1256): Ignore block-pass in `TrailingComma`. ([@tamird][])
* [#1255](https://github.com/rubocop/rubocop/issues/1255): Compare without context in `Auto-CorrectUnlessChangingAST`. ([@jonas054][])
* [#1262](https://github.com/rubocop/rubocop/issues/1262): Handle regexp and backtick literals in `VariableInterpolation`. ([@bbatsov][])

## 0.24.1 (2014-07-03)

### Bugs fixed

* [#1174](https://github.com/rubocop/rubocop/issues/1174): Fix `--auto-correct` crash in `AlignParameters`. ([@jonas054][])
* [#1176](https://github.com/rubocop/rubocop/issues/1176): Fix `--auto-correct` crash in `IndentationWidth`. ([@jonas054][])
* [#1177](https://github.com/rubocop/rubocop/issues/1177): Avoid suggesting underscore-prefixed name for unused keyword arguments and auto-correcting in that way. ([@yujinakayama][])
* [#1157](https://github.com/rubocop/rubocop/issues/1157): Validate `--only` arguments later when all cop names are known. ([@jonas054][])
* [#1188](https://github.com/rubocop/rubocop/issues/1188), [#1190](https://github.com/rubocop/rubocop/issues/1190): Fix crash in `LineLength` cop when `AllowURI` option is enabled. ([@yujinakayama][])
* [#1191](https://github.com/rubocop/rubocop/issues/1191): Fix crash on empty body branches in a loop in `Next` cop. ([@yujinakayama][])

## 0.24.0 (2014-06-25)

### New features

* [#639](https://github.com/rubocop/rubocop/issues/639): Support square bracket setters in `UselessSetterCall`. ([@yujinakayama][])
* [#835](https://github.com/rubocop/rubocop/issues/835): `UnneededCapitalW` cop does auto-correction. ([@sfeldon][])
* [#1092](https://github.com/rubocop/rubocop/issues/1092): New cop `DefEndAlignment` takes over responsibility for checking alignment of method definition `end`s from `EndAlignment`, and is configurable. ([@jonas054][])
* [#1145](https://github.com/rubocop/rubocop/issues/1145): New cop `ClassCheck` enforces consistent use of `is_a?` or `kind_of?`. ([@bbatsov][])
* [#1161](https://github.com/rubocop/rubocop/pull/1161): New cop `SpaceBeforeComma` detects spaces before a comma. ([@agrimm][])
* [#1161](https://github.com/rubocop/rubocop/pull/1161): New cop `SpaceBeforeSemicolon` detects spaces before a semicolon. ([@agrimm][])
* [#835](https://github.com/rubocop/rubocop/issues/835): New cop `UnneededPercentQ` checks for usage of the `%q`/`%Q` syntax when `''` or `""` would do. ([@jonas054][])
* [#977](https://github.com/rubocop/rubocop/issues/977): Add `AllowURI` option (enabled by default) to `LineLength` cop. ([@yujinakayama][])

### Changes

* Unused block local variables (`obj.each { |arg; this| }`) are now handled by `UnusedBlockArgument` cop instead of `UselessAssignment` cop. ([@yujinakayama][])
* [#1141](https://github.com/rubocop/rubocop/issues/1141): Clarify in the message from `TrailingComma` that a trailing comma is never allowed for lists where some items share a line. ([@jonas054][])

### Bugs fixed

* [#1133](https://github.com/rubocop/rubocop/issues/1133): Handle `reduce/inject` with no arguments in `EachWithObject`. ([@bbatsov][])
* [#1152](https://github.com/rubocop/rubocop/issues/1152): Handle `while/until` with no body in `Next`. ([@tamird][])
* Fix a false positive in `UselessSetterCall` for setter call on a local variable that contains a non-local object. ([@yujinakayama][])
* [#1158](https://github.com/rubocop/rubocop/issues/1158): Fix auto-correction of floating-point numbers. ([@bbatsov][])
* [#1159](https://github.com/rubocop/rubocop/issues/1159): Fix checking of `begin`..`end` structures, blocks, and parenthesized expressions in `IndentationWidth`. ([@jonas054][])
* [#1159](https://github.com/rubocop/rubocop/issues/1159): More rigid conditions for when `attr` is considered an offense. ([@jonas054][])
* [#1167](https://github.com/rubocop/rubocop/issues/1167): Fix handling of parameters spanning multiple lines in `TrailingComma`. ([@jonas054][])
* [#1169](https://github.com/rubocop/rubocop/issues/1169): Fix handling of ternary op conditions in `ParenthesesAroundCondition`. ([@bbatsov][])
* [#1147](https://github.com/rubocop/rubocop/issues/1147): WordArray checks arrays with special characters. ([@camilleldn][])
* Fix a false positive against `return` in a loop in `Next` cop. ([@yujinakayama][])
* [#1165](https://github.com/rubocop/rubocop/issues/1165): Support `rescue`/`else`/`ensure` bodies in `IndentationWidth`. ([@jonas054][])
* Fix false positive for aligned list of values after `when` in `IndentationWidth`. ([@jonas054][])

## 0.23.0 (2014-06-02)

### New features

* [#1117](https://github.com/rubocop/rubocop/issues/1117): `BlockComments` cop does auto-correction. ([@jonas054][])
* [#1124](https://github.com/rubocop/rubocop/pull/1124): `TrivialAccessors` cop auto-corrects class-level accessors. ([@ggilder][])
* [#1062](https://github.com/rubocop/rubocop/pull/1062): New cop `InlineComment` checks for inline comments. ([@salbertson][])
* [#1118](https://github.com/rubocop/rubocop/issues/1118): Add checking and auto-correction of right brackets in `IndentArray` and `IndentHash`. ([@jonas054][])

### Changes

* [#1097](https://github.com/rubocop/rubocop/issues/1097): Add optional namespace prefix to cop names: `Style/LineLength` instead of `LineLength` in config files, `--only` argument, `--show-cops` output, and `# rubocop:disable`. ([@jonas054][])
* [#1075](https://github.com/rubocop/rubocop/issues/1075): More strict limits on when to require trailing comma. ([@jonas054][])
* Renamed `Rubocop` module to `RuboCop`. ([@bbatsov][])

### Bugs fixed

* [#1126](https://github.com/rubocop/rubocop/pull/1126): Fix `--auto-gen-config` bug with `RegexpLiteral` where only the last file's results would be used. ([@ggilder][])
* [#1104](https://github.com/rubocop/rubocop/issues/1104): Fix `EachWithObject` with modifier if as body. ([@geniou][])
* [#1106](https://github.com/rubocop/rubocop/issues/1106): Fix `EachWithObject` with single method call as body. ([@geniou][])
* Avoid the warning about ignoring syck YAML engine from JRuby. ([@jonas054][])
* [#1111](https://github.com/rubocop/rubocop/issues/1111): Fix problem in `EndOfLine` with reading non-UTF-8 encoded files. ([@jonas054][])
* [#1115](https://github.com/rubocop/rubocop/issues/1115): Fix `Next` to ignore super nodes. ([@geniou][])
* [#1117](https://github.com/rubocop/rubocop/issues/1117): Don't auto-correct indentation in scopes that contain block comments (`=begin`..`=end`). ([@jonas054][])
* [#1123](https://github.com/rubocop/rubocop/pull/1123): Support setter calls in safe assignment in `ParenthesesAroundCondition`. ([@jonas054][])
* [#1090](https://github.com/rubocop/rubocop/issues/1090): Correct handling of documentation vs annotation comment. ([@jonas054][])
* [#1118](https://github.com/rubocop/rubocop/issues/1118): Never write invalid ruby to a file in auto-correct. ([@jonas054][])
* [#1120](https://github.com/rubocop/rubocop/issues/1120): Don't change indentation of heredoc strings in auto-correct. ([@jonas054][])
* [#1109](https://github.com/rubocop/rubocop/issues/1109): Handle conditions with modifier ops in them in `ParenthesesAroundCondition`. ([@bbatsov][])

## 0.22.0 (2014-05-20)

### New features

* [#974](https://github.com/rubocop/rubocop/pull/974): New cop `CommentIndentation` checks indentation of comments. ([@jonas054][])
* Add new cop `EachWithObject` to prefer `each_with_object` over `inject` or `reduce`. ([@geniou][])
* [#1010](https://github.com/rubocop/rubocop/issues/1010): New Cop `Next` check for conditions at the end of an iteration and propose to use `next` instead. ([@geniou][])
* The `GuardClause` cop now also looks for unless and it is configurable how many lines the body of an if / unless needs to have to not be ignored. ([@geniou][])
* [#835](https://github.com/rubocop/rubocop/issues/835): New cop `UnneededPercentX` checks for `%x` when backquotes would do. ([@jonas054][])
* Add auto-correct to `UnusedBlockArgument` and `UnusedMethodArgument` cops. ([@hannestyden][])
* [#1074](https://github.com/rubocop/rubocop/issues/1074): New cop `SpaceBeforeComment` checks for missing space between code and a comment on the same line. ([@jonas054][])
* [#1089](https://github.com/rubocop/rubocop/pull/1089): New option `-F`/`--fail-fast` inspects files in modification time order and stop after the first file with offenses. ([@jonas054][])
* Add optional `require` directive to `.rubocop.yml` to load custom ruby files. ([@geniou][])

### Changes

* `NonNilCheck` offense reporting and auto-correct are configurable to include semantic changes. ([@hannestyden][])
* The parameters `AllCops/Excludes` and `AllCops/Includes` with final `s` only give a warning and don't halt `rubocop` execution. ([@jonas054][])
* The `GuardClause` cop is no longer ignoring a one-line body by default - see configuration. ([@geniou][])
* [#1050](https://github.com/rubocop/rubocop/issues/1050): Rename `rubocop-todo.yml` file to `.rubocop_todo.yml`. ([@geniou][])
* [#1064](https://github.com/rubocop/rubocop/issues/1064): Adjust default max line length to 80. ([@bbatsov][])

### Bugs fixed

* Allow assignment in `AlignParameters` cop. ([@tommeier][])
* Fix `Void` and `SpaceAroundOperators` for short call syntax `lambda.()`. ([@biinari][])
* Fix `Delegate` for delegation with assignment or constant. ([@geniou][])
* [#1032](https://github.com/rubocop/rubocop/issues/1032): Avoid duplicate reporting when code moves around due to `--auto-correct`. ([@jonas054][])
* [#1036](https://github.com/rubocop/rubocop/issues/1036): Handle strings like `__FILE__` in `LineEndConcatenation`. ([@bbatsov][])
* [#1006](https://github.com/rubocop/rubocop/issues/1006): Fix LineEndConcatenation to handle chained concatenations. ([@barunio][])
* [#1066](https://github.com/rubocop/rubocop/issues/1066): Fix auto-correct for `NegatedIf` when the condition has parentheses around it. ([@jonas054][])
* Fix `AlignParameters` `with_fixed_indentation` for multi-line method calls. ([@molawson][])
* Fix problem that appears in some installations when reading empty YAML files. ([@jonas054][])
* [#1022](https://github.com/rubocop/rubocop/issues/1022): A Cop will no longer auto-correct a file that's excluded through an `Exclude` setting in the cop's configuration. ([@jonas054][])
* Fix paths in `Exclude` config section not being recognized on Windows. ([@wndhydrnt][])
* [#1094](https://github.com/rubocop/rubocop/issues/1094): Fix ClassAndModuleChildren for classes with a single method. ([@geniou][])

## 0.21.0 (2014-04-24)

### New features

* [#835](https://github.com/rubocop/rubocop/issues/835): New cop `UnneededCapitalW` checks for `%W` when interpolation not necessary and `%w` would do. ([@sfeldon][])
* [#934](https://github.com/rubocop/rubocop/issues/934): New cop `UnderscorePrefixedVariableName` checks for `_`-prefixed variables that are actually used. ([@yujinakayama][])
* [#934](https://github.com/rubocop/rubocop/issues/934): New cop `UnusedMethodArgument` checks for unused method arguments. ([@yujinakayama][])
* [#934](https://github.com/rubocop/rubocop/issues/934): New cop `UnusedBlockArgument` checks for unused block arguments. ([@yujinakayama][])
* [#964](https://github.com/rubocop/rubocop/issues/964): `RedundantBegin` cop does auto-correction. ([@tamird][])
* [#966](https://github.com/rubocop/rubocop/issues/966): `RescueException` cop does auto-correction. ([@tamird][])
* [#967](https://github.com/rubocop/rubocop/issues/967): `TrivialAccessors` cop does auto-correction. ([@tamird][])
* [#963](https://github.com/rubocop/rubocop/issues/963): Add `AllowDSLWriters` options to `TrivialAccessors`. ([@tamird][])
* [#969](https://github.com/rubocop/rubocop/issues/969): Let the `Debugger` cop check for forgotten calls to byebug. ([@bquorning][])
* [#971](https://github.com/rubocop/rubocop/issues/971): Configuration format deprecation warnings include the path to the problematic config file. ([@bcobb][])
* [#490](https://github.com/rubocop/rubocop/issues/490): Add EnforcedStyle config option to TrailingBlankLines. ([@jonas054][])
* Add `auto_correct` task to Rake integration. ([@irrationalfab][])
* [#986](https://github.com/rubocop/rubocop/issues/986): The `--only` option can take a comma-separated list of cops. ([@jonas054][])
* New Rails cop `Delegate` that checks for delegations that could be replaced by the `delegate` method. ([@geniou][])
* Add configuration to `Encoding` cop to only enforce encoding comment if there are non ASCII characters. ([@geniou][])

### Changes

* Removed `FinalNewline` cop as its check is now performed by `TrailingBlankLines`. ([@jonas054][])
* [#1011](https://github.com/rubocop/rubocop/issues/1011): Pattern matching with `Dir#[]` for config parameters added. ([@jonas054][])

### Bugs fixed

* Update description on `LineEndConcatenation` cop. ([@mockdeep][])
* [#978](https://github.com/rubocop/rubocop/issues/978): Fix regression in `IndentationWidth` handling method calls. ([@tamird][])
* [#976](https://github.com/rubocop/rubocop/issues/976): Fix `EndAlignment` not handling element assignment correctly. ([@tamird][])
* [#976](https://github.com/rubocop/rubocop/issues/976): Fix `IndentationWidth` not handling element assignment correctly. ([@tamird][])
* [#800](https://github.com/rubocop/rubocop/issues/800): Do not report `[Corrected]` in `--auto-correct` mode if correction wasn't done. ([@jonas054][])
* [#968](https://github.com/rubocop/rubocop/issues/968): Fix bug when running RuboCop with `-c .rubocop.yml`. ([@bquorning][])
* [#975](https://github.com/rubocop/rubocop/pull/975): Fix infinite correction in `IndentationWidth`. ([@jonas054][])
* [#986](https://github.com/rubocop/rubocop/issues/986): When `--lint` is used together with `--only`, all lint cops are run in addition to the given cops. ([@jonas054][])
* [#997](https://github.com/rubocop/rubocop/issues/997): Fix handling of file paths for matching against `Exclude` property when `rubocop .` is called. ([@jonas054][])
* [#1000](https://github.com/rubocop/rubocop/issues/1000): Support modifier (e.g., `private`) and `def` on the same line (Ruby >= 2.1) in `IndentationWidth`. ([@jonas054][])
* [#1001](https://github.com/rubocop/rubocop/issues/1001): Fix `--auto-gen-config` logic for `RegexpLiteral`. ([@jonas054][])
* [#993](https://github.com/rubocop/rubocop/issues/993): Do not report any offenses for the contents of an empty file. ([@jonas054][])
* [#1016](https://github.com/rubocop/rubocop/issues/1016): Fix a false positive in `ConditionPosition` regarding statement modifiers. ([@bbatsov][])
* [#1014](https://github.com/rubocop/rubocop/issues/1014): Fix handling of strings nested in `dstr` nodes. ([@bbatsov][])

## 0.20.1 (2014-04-05)

### Bugs fixed

* [#940](https://github.com/rubocop/rubocop/issues/940): Fixed `UselessAccessModifier` not handling `attr_*` correctly. ([@fshowalter][])
* `NegatedIf` properly handles negated `unless` condition. ([@bbatsov][])
* `NegatedWhile` properly handles negated `until` condition. ([@bbatsov][])
* [#925](https://github.com/rubocop/rubocop/issues/925): Do not disable the `Syntax` cop in output from `--auto-gen-config`. ([@jonas054][])
* [#943](https://github.com/rubocop/rubocop/issues/943): Fix auto-correction interference problem between `SpaceAfterComma` and other cops. ([@jonas054][])
* [#954](https://github.com/rubocop/rubocop/pull/954): Fix auto-correction bug in `NilComparison`. ([@bbatsov][])
* [#953](https://github.com/rubocop/rubocop/pull/953): Fix auto-correction bug in `NonNilCheck`. ([@bbatsov][])
* [#952](https://github.com/rubocop/rubocop/pull/952): Handle implicit receiver in `StringConversionInInterpolation`. ([@bbatsov][])
* [#956](https://github.com/rubocop/rubocop/pull/956): Apply `ClassMethods` check only on `class`/`module` bodies. ([@bbatsov][])
* [#945](https://github.com/rubocop/rubocop/issues/945): Fix SpaceBeforeFirstArg cop for multiline argument and exclude assignments. ([@cschramm][])
* [#948](https://github.com/rubocop/rubocop/issues/948): `Blocks` cop avoids auto-correction if it would introduce a semantic change. ([@jonas054][])
* [#946](https://github.com/rubocop/rubocop/issues/946): Allow non-nil checks that are the final expressions of predicate method definitions in `NonNilCheck`. ([@bbatsov][])
* [#957](https://github.com/rubocop/rubocop/issues/957): Allow space + comment inside parentheses, braces, and square brackets. ([@jonas054][])

## 0.20.0 (2014-04-02)

### New features

* New cop `GuardClause` checks for conditionals that can be replaced by guard clauses. ([@bbatsov][])
* New cop `EmptyInterpolation` checks for empty interpolation in double-quoted strings. ([@bbatsov][])
* [#899](https://github.com/rubocop/rubocop/issues/899): Make `LineEndConcatenation` cop `<<` aware. ([@mockdeep][])
* [#896](https://github.com/rubocop/rubocop/issues/896): New option `--fail-level` changes minimum severity for exit with error code. ([@hiroponz][])
* [#893](https://github.com/rubocop/rubocop/issues/893): New option `--force-exclusion` forces excluding files specified in the configuration `Exclude` even if they are explicitly passed as arguments. ([@yujinakayama][])
* `VariableInterpolation` cop does auto-correction. ([@bbatsov][])
* `Not` cop does auto-correction. ([@bbatsov][])
* `ClassMethods` cop does auto-correction. ([@bbatsov][])
* `StringConversionInInterpolation` cop does auto-correction. ([@bbatsov][])
* `NilComparison` cop does auto-correction. ([@bbatsov][])
* `NonNilComparison` cop does auto-correction. ([@bbatsov][])
* `NegatedIf` cop does auto-correction. ([@bbatsov][])
* `NegatedWhile` cop does auto-correction. ([@bbatsov][])
* New lint cop `SpaceBeforeFirstArg` checks for space between the method name and the first argument in method calls without parentheses. ([@jonas054][])
* New style cop `SingleSpaceBeforeFirstArg` checks that no more than one space is used between the method name and the first argument in method calls without parentheses. ([@jonas054][])
* New formatter `disabled_lines` displays cops and line ranges disabled by inline comments. ([@fshowalter][])
* New cop `UselessAccessModifiers` checks for access modifiers that have no effect. ([@fshowalter][])

### Changes

* [#913](https://github.com/rubocop/rubocop/issues/913): `FileName` accepts multiple extensions. ([@tamird][])
* `AllCops/Excludes` and `AllCops/Includes` were renamed to `AllCops/Exclude` and `AllCops/Include` for consistency with standard cop params. ([@bbatsov][])
* Extract `NonNilCheck` cop from `NilComparison`. ([@bbatsov][])
* Renamed `FavorJoin` to `ArrayJoin`. ([@bbatsov][])
* Renamed `FavorUnlessOverNegatedIf` to `NegatedIf`. ([@bbatsov][])
* Renamed `FavorUntilOverNegatedWhile`to `NegatedWhile`. ([@bbatsov][])
* Renamed `HashMethods` to `DeprecatedHashMethods`. ([@bbatsov][])
* Renamed `ReadAttribute` to `ReadWriteAttribute` and extended it to check for uses of `write_attribute`. ([@bbatsov][])
* Add experimental support for Ruby 2.2 (development version) by falling back to Ruby 2.1 parser. ([@yujinakayama][])

### Bugs fixed

* [#926](https://github.com/rubocop/rubocop/issues/926): Fixed `BlockNesting` not auto-generating correctly. ([@tmorris-fiksu][])
* [#904](https://github.com/rubocop/rubocop/issues/904): Fixed a NPE in `LiteralInInterpolation`. ([@bbatsov][])
* [#904](https://github.com/rubocop/rubocop/issues/904): Fixed a NPE in `StringConversionInInterpolation`. ([@bbatsov][])
* [#892](https://github.com/rubocop/rubocop/issues/892): Make sure `Include` and `Exclude` paths in a `.rubocop.yml` are interpreted as relative to the directory of that file. ([@jonas054][])
* [#906](https://github.com/rubocop/rubocop/issues/906): Fixed a false positive in `LiteralInInterpolation`. ([@bbatsov][])
* [#909](https://github.com/rubocop/rubocop/issues/909): Handle properly multiple `rescue` clauses in `SignalException`. ([@bbatsov][])
* [#876](https://github.com/rubocop/rubocop/issues/876): Do a deep merge of hashes when overriding default configuration in a `.rubocop.yml` file. ([@jonas054][])
* [#912](https://github.com/rubocop/rubocop/issues/912): Fix a false positive in `LineEndConcatenation` for `%` string literals. ([@bbatsov][])
* [#912](https://github.com/rubocop/rubocop/issues/912): Handle top-level constant resolution in `DeprecatedClassMethods` (e.g. `::File.exists?`). ([@bbatsov][])
* [#914](https://github.com/rubocop/rubocop/issues/914): Fixed rdoc error during gem installation. ([@bbatsov][])
* The `--only` option now enables the given cop in case it is disabled in configuration. ([@jonas054][])
* Fix path resolution so that the default exclusion of `vendor` directories works. ([@jonas054][])
* [#908](https://github.com/rubocop/rubocop/issues/908): Fixed hanging while auto correct for `SpaceAfterComma` and `SpaceInsideBrackets`. ([@hiroponz][])
* [#919](https://github.com/rubocop/rubocop/issues/919): Don't avoid auto-correction in `HashSyntax` when there is missing space around operator. ([@jonas054][])
* Fixed handling of floats in `NumericLiterals`. ([@bbatsov][])
* [#927](https://github.com/rubocop/rubocop/issues/927): Let `--auto-gen-config` overwrite an existing `rubocop-todo.yml` file instead of asking the user to remove it. ([@jonas054][])
* [#936](https://github.com/rubocop/rubocop/issues/936): Allow `_other` as well as `other` in `OpMethod`. ([@bbatsov][])

## 0.19.1 (2014-03-17)

### Bugs fixed

* [#884](https://github.com/rubocop/rubocop/issues/884): Fix --auto-gen-config for `NumericLiterals` so MinDigits is correct. ([@tmorris-fiksu][])
* [#879](https://github.com/rubocop/rubocop/issues/879): Fix --auto-gen-config for `RegexpLiteral` so we don't generate illegal values for `MaxSlashes`. ([@jonas054][])
* Fix the name of the `Include` param in the default config of the Rails cops. ([@bbatsov][])
* [#878](https://github.com/rubocop/rubocop/pull/878): Blacklist `Rakefile`, `Gemfile` and `Capfile` by default in the `FileName` cop. ([@bbatsov][])
* [#875](https://github.com/rubocop/rubocop/issues/875): Handle `separator` style hashes in `IndentHash`. ([@jonas054][])
* Fix a bug where multiple cli options that result in exit can be specified at once (e.g. `-vV`, `-v --show-cops`). ([@jkogara][])
* [#889](https://github.com/rubocop/rubocop/issues/889): Fix a false positive for `LiteralInCondition` when the condition is non-primitive array. ([@bbatsov][])

## 0.19.0 (2014-03-13)

### New features

* New cop `FileName` makes sure that source files have snake_case names. ([@bbatsov][])
* New cop `DeprecatedClassMethods` checks for deprecated class methods. ([@bbatsov][])
* New cop `StringConversionInInterpolation` checks for redundant `Object#to_s` in string interpolation. ([@bbatsov][])
* New cop `LiteralInInterpolation` checks for interpolated string literals. ([@bbatsov][])
* New cop `SelfAssignment` checks for places where the self-assignment shorthand should have been used. ([@bbatsov][])
* New cop `DoubleNegation` checks for uses of `!!`. ([@bbatsov][])
* New cop `PercentLiteralDelimiters` enforces consistent usage of `%`-literal delimiters. ([@hannestyden][])
* New Rails cop `ActionFilter` enforces the use of `_filter` or `_action` action filter methods. ([@bbatsov][])
* New Rails cop `ScopeArgs` makes sure you invoke the `scope` method properly. ([@bbatsov][])
* Add `with_fixed_indentation` style to `AlignParameters` cop. ([@hannestyden][])
* Add `IgnoreLastArgumentHash` option to `AlignHash` cop. ([@hannestyden][])
* [#743](https://github.com/rubocop/rubocop/issues/743): `SingleLineMethods` cop does auto-correction. ([@jonas054][])
* [#743](https://github.com/rubocop/rubocop/issues/743): `Semicolon` cop does auto-correction. ([@jonas054][])
* [#743](https://github.com/rubocop/rubocop/issues/743): `EmptyLineBetweenDefs` cop does auto-correction. ([@jonas054][])
* [#743](https://github.com/rubocop/rubocop/issues/743): `IndentationWidth` cop does auto-correction. ([@jonas054][])
* [#743](https://github.com/rubocop/rubocop/issues/743): `IndentationConsistency` cop does auto-correction. ([@jonas054][])
* [#809](https://github.com/rubocop/rubocop/issues/809): New formatter `fuubar` displays a progress bar and shows details of offenses as soon as they are detected. ([@yujinakayama][])
* [#797](https://github.com/rubocop/rubocop/issues/797): New cop `IndentHash` checks the indentation of the first key in multi-line hash literals. ([@jonas054][])
* [#797](https://github.com/rubocop/rubocop/issues/797): New cop `IndentArray` checks the indentation of the first element in multi-line array literals. ([@jonas054][])
* [#806](https://github.com/rubocop/rubocop/issues/806): Now excludes files in `vendor/**` by default. ([@jeremyolliver][])
* [#795](https://github.com/rubocop/rubocop/issues/795): `IfUnlessModifier` and `WhileUntilModifier` supports `MaxLineLength`, which is independent of `LineLength` parameter `Max`. ([@agrimm][])
* [#868](https://github.com/rubocop/rubocop/issues/868): New cop `ClassAndModuleChildren` checks the style of children definitions at classes and modules: nested / compact. ([@geniou][])

### Changes

* [#793](https://github.com/rubocop/rubocop/issues/793): Add printing total count when `rubocop --format offences`. ([@ma2gedev][])
* Remove `Ignore` param from the Rails `Output` cop. The standard `Exclude/Include` should be used instead. ([@bbatsov][])
* Renamed `FavorSprintf` to `FormatString` and made it configurable. ([@bbatsov][])
* Renamed `Offence` to `Offense`. ([@bbatsov][])
* Use `offense` in all messages instead of `offence`. ([@bbatsov][])
* For indentation of `if`/`unless`/`while`/`until` bodies when the result is assigned to a variable, instead of supporting two styles simultaneously, `IndentationWidth` now supports one style of indentation at a time, specified by `EndAlignment`/`AlignWith`. ([@jonas054][])
* Renamed `Style` param of `DotPosition` cop to `EnforcedStyle`. ([@bbatsov][])
* Add `length` value to locations of offense in JSON formatter. ([@yujinakayama][])
* `SpaceAroundBlockBraces` cop replaced by `SpaceBeforeBlockBraces` and `SpaceInsideBlockBraces`. ([@jonas054][])
* `SpaceAroundEqualsInParameterDefault` cop is now configurable with the `EnforcedStyle` option. ([@jonas054][])

### Bugs fixed

* [#790](https://github.com/rubocop/rubocop/issues/790): Fix auto-correction interference problem between `MethodDefParentheses` and other cops. ([@jonas054][])
* [#794](https://github.com/rubocop/rubocop/issues/794): Fix handling of modifier keywords with required parentheses in `ParenthesesAroundCondition`. ([@bbatsov][])
* [#804](https://github.com/rubocop/rubocop/issues/804): Fix a false positive with operator assignments in a loop (including `begin..rescue..end` with `retry`) in `UselessAssignment`. ([@yujinakayama][])
* [#815](https://github.com/rubocop/rubocop/issues/815): Fix a false positive for heredocs with blank lines in them in `EmptyLines`. ([@bbatsov][])
* Auto-correction is now more robust and less likely to die because of `RangeError` or "clobbering". ([@jonas054][])
* Offenses always reported in order of position in file, also during `--auto-correct` runs. ([@jonas054][])
* Fix problem with `[Corrected]` tag sometimes missing in output from `--auto-correct` runs. ([@jonas054][])
* Fix message from `EndAlignment` cop when `AlignWith` is `keyword`. ([@jonas054][])
* Handle `case` conditions in `LiteralInCondition`. ([@bbatsov][])
* [#822](https://github.com/rubocop/rubocop/issues/822): Fix a false positive in `DotPosition` when enforced style is set to `trailing`. ([@bbatsov][])
* Handle properly dynamic strings in `LineEndConcatenation`. ([@bbatsov][])
* [#832](https://github.com/rubocop/rubocop/issues/832): Fix auto-correction interference problem between `BracesAroundHashParameters` and `SpaceInsideHashLiteralBraces`. ([@jonas054][])
* Fix bug in auto-correction of alignment so that only space can be removed. ([@jonas054][])
* Fix bug in `IndentationWidth` auto-correction so it doesn't correct things that `IndentationConsistency` should correct. ([@jonas054][])
* [#847](https://github.com/rubocop/rubocop/issues/847): Fix bug in `RegexpLiteral` concerning `--auto-gen-config`. ([@jonas054][])
* [#848](https://github.com/rubocop/rubocop/issues/848): Fix bug in `--show-cops` that made it print the default configuration rather than the current configuration. ([@jonas054][])
* [#862](https://github.com/rubocop/rubocop/issues/862): Fix a bug where single line `rubocop:disable` comments with indentations were treated as multiline cop disabling comments. ([@yujinakayama][])
* Fix a bug where `rubocop:disable` comments with a cop name including `all` (e.g. `MethodCallParentheses`) were disabling all cops. ([@yujinakayama][])
* Fix a bug where string and regexp literals including `# rubocop:disable` were confused with real comments. ([@yujinakayama][])
* [#877](https://github.com/rubocop/rubocop/issues/877): Fix bug in `PercentLiteralDelimiters` concerning auto-correct of regular expressions with interpolation. ([@hannestyden][])

## 0.18.1 (2014-02-02)

### Bugs fixed

* Remove double reporting in `EmptyLinesAroundBody` of empty line inside otherwise empty class/module/method that caused crash in auto-correct. ([@jonas054][])
* [#779](https://github.com/rubocop/rubocop/issues/779): Fix a false positive in `LineEndConcatenation`. ([@bbatsov][])
* [#751](https://github.com/rubocop/rubocop/issues/751): Fix `Documentation` cop so that a comment followed by an empty line and then a class definition is not considered to be class documentation. ([@jonas054][])
* [#783](https://github.com/rubocop/rubocop/issues/783): Fix a false positive in `ParenthesesAroundCondition` when the parentheses are actually required. ([@bbatsov][])
* [#781](https://github.com/rubocop/rubocop/issues/781): Fix problem with back-and-forth auto-correction in `AccessModifierIndentation`. ([@jonas054][])
* [#785](https://github.com/rubocop/rubocop/issues/785): Fix false positive on `%w` arrays in `TrailingComma`. ([@jonas054][])
* [#782](https://github.com/rubocop/rubocop/issues/782): Fix false positive in `AlignHash` for single line hashes. ([@jonas054][])

## 0.18.0 (2014-01-30)

### New features

* [#714](https://github.com/rubocop/rubocop/issues/714): New cop `RequireParentheses` checks for method calls without parentheses together with a boolean operator indicating that a mistake about precedence may have been made. ([@jonas054][])
* [#743](https://github.com/rubocop/rubocop/issues/743): `WordArray` cop does auto-correction. ([@jonas054][])
* [#743](https://github.com/rubocop/rubocop/issues/743): `Proc` cop does auto-correction. ([@bbatsov][])
* [#743](https://github.com/rubocop/rubocop/issues/743): `AccessModifierIndentation` cop does auto-correction. ([@jonas054][])
* [#768](https://github.com/rubocop/rubocop/issues/768): Rake task now supports `requires` and `options`. ([@nevir][])
* [#759](https://github.com/rubocop/rubocop/issues/759): New cop `EndLineConcatenation` checks for string literal concatenation with `+` at line end. ([@bbatsov][])

### Changes

* [#762](https://github.com/rubocop/rubocop/issues/762): Support Rainbow gem both 1.99.x and 2.x. ([@yujinakayama][])
* [#761](https://github.com/rubocop/rubocop/issues/761): Relax `json` requirement to `>= 1.7.7`. ([@bbatsov][])
* [#757](https://github.com/rubocop/rubocop/issues/757): `Include/Exclude` supports relative globbing to some extent. ([@nevir][])

### Bugs fixed

* [#764](https://github.com/rubocop/rubocop/issues/764): Handle heredocs in `TrailingComma`. ([@jonas054][])
* Guide for contributors now points to correct issues page. ([@scottmatthewman][])

## 0.17.0 (2014-01-25)

### New features

* New cop `ConditionPosition` checks for misplaced conditions in expressions like `if/unless/when/until`. ([@bbatsov][])
* New cop `ElseLayout` checks for odd arrangement of code in the `else` branch of a conditional expression. ([@bbatsov][])
* [#694](https://github.com/rubocop/rubocop/issues/694): Support Ruby 1.9.2 until June 2014. ([@yujinakayama][])
* [#702](https://github.com/rubocop/rubocop/issues/702): Improve `rubocop-todo.yml` with comments about offence count, configuration parameters, and auto-correction support. ([@jonas054][])
* Add new command-line flag `-D/--display-cop-names` to trigger the display of cop names in offence messages. ([@bbatsov][])
* [#733](https://github.com/rubocop/rubocop/pull/733): `NumericLiterals` cop does auto-correction. ([@dblock][])
* [#713](https://github.com/rubocop/rubocop/issues/713): New cop `TrailingComma` checks for comma after the last item in a hash, array, or method call parameter list. ([@jonas054][])

### Changes

* [#581](https://github.com/rubocop/rubocop/pull/581): Extracted a new cop `AmbiguousOperator` from `Syntax` cop. It checks for ambiguous operators in the first argument of a method invocation without parentheses. ([@yujinakayama][])
* Extracted a new cop `AmbiguousRegexpLiteral` from `Syntax` cop. It checks for ambiguous regexp literals in the first argument of a method invocation without parentheses. ([@yujinakayama][])
* Extracted a new cop `UselessElseWithoutRescue` from `Syntax` cop. It checks for useless `else` in `begin..end` without `rescue`. ([@yujinakayama][])
* Extracted a new cop `InvalidCharacterLiteral` from `Syntax` cop. It checks for invalid character literals with a non-escaped whitespace character (e.g. `? `). ([@yujinakayama][])
* Removed `Syntax` cop from the configuration. It no longer can be disabled and it reports only invalid syntax offences. ([@yujinakayama][])
* [#688](https://github.com/rubocop/rubocop/issues/688): Output from `rubocop --show-cops` now looks like a YAML configuration file. The `--show-cops` option takes a comma separated list of cops as optional argument. ([@jonas054][])
* New cop `IndentationConsistency` extracted from `IndentationWidth`, which has checked two kinds of offences until now. ([@jonas054][])

### Bugs fixed

* [#698](https://github.com/rubocop/rubocop/pull/698): Support Windows paths on command-line. ([@rifraf][])
* [#498](https://github.com/rubocop/rubocop/issues/498): Disable terminal ANSI escape sequences when a formatter's output is not a TTY. ([@yujinakayama][])
* [#703](https://github.com/rubocop/rubocop/issues/703): BracesAroundHashParameters auto-correction broken with trailing comma. ([@jonas054][])
* [#709](https://github.com/rubocop/rubocop/issues/709): When `EndAlignment` has configuration `AlignWith: variable`, it now handles `@@a = if ...` and `a, b = if ...`. ([@jonas054][])
* `SpaceAroundOperators` now reports an offence for `@@a=0`. ([@jonas054][])
* [#707](https://github.com/rubocop/rubocop/issues/707): Fix error on operator assignments in top level scope in `UselessAssignment`. ([@yujinakayama][])
* Fix a bug where some offences were discarded when any cop that has specific target file path (by `Include` or `Exclude` under each cop configuration) had run. ([@yujinakayama][])
* [#724](https://github.com/rubocop/rubocop/issues/724): Accept colons denoting required keyword argument (a new feature in Ruby 2.1) without trailing space in `SpaceAfterColon`. ([@jonas054][])
* The `--no-color` option works again. ([@jonas054][])
* [#716](https://github.com/rubocop/rubocop/issues/716): Fixed a regression in the auto-correction logic of `MethodDefParentheses`. ([@bbatsov][])
* Inspected projects that lack a `.rubocop.yml` file, and therefore get their configuration from RuboCop's `config/default.yml`, no longer get configuration from RuboCop's `.rubocop.yml` and `rubocop-todo.yml`. ([@jonas054][])
* [#730](https://github.com/rubocop/rubocop/issues/730): `EndAlignment` now handles for example `private def some_method`, which is allowed in Ruby 2.1. It requires `end` to be aligned with `private`, not `def`, in such cases. ([@jonas054][])
* [#744](https://github.com/rubocop/rubocop/issues/744): Any new offences created by `--auto-correct` are now handled immediately and corrected when possible, so running `--auto-correct` once is enough. ([@jonas054][])
* [#748](https://github.com/rubocop/rubocop/pull/748): Auto-correction conflict between `EmptyLinesAroundBody` and `TrailingWhitespace` resolved. ([@jonas054][])
* `ParenthesesAroundCondition` no longer crashes on parentheses around the condition in a ternary if. ([@jonas054][])
* [#738](https://github.com/rubocop/rubocop/issues/738): Fix a false positive in `StringLiterals`. ([@bbatsov][])

## 0.16.0 (2013-12-25)

### New features

* [#612](https://github.com/rubocop/rubocop/pull/612): `BracesAroundHashParameters` cop does auto-correction. ([@dblock][])
* [#614](https://github.com/rubocop/rubocop/pull/614): `ParenthesesAroundCondition` cop does auto-correction. ([@dblock][])
* [#624](https://github.com/rubocop/rubocop/pull/624): `EmptyLines` cop does auto-correction. ([@dblock][])
* New Rails cop `DefaultScope` ensures `default_scope` is called properly with a block argument. ([@bbatsov][])
* All cops now support the `Include` param, which specifies the files on which they should operate. ([@bbatsov][])
* All cops now support the `Exclude` param, which specifies the files on which they should not operate. ([@bbatsov][])
* [#631](https://github.com/rubocop/rubocop/issues/631): `IndentationWidth` cop now detects inconsistent indentation between lines that should have the same indentation. ([@jonas054][])
* [#649](https://github.com/rubocop/rubocop/pull/649): `EmptyLinesAroundBody` cop does auto-correction. ([@dblock][])
* [#657](https://github.com/rubocop/rubocop/pull/657): `Alias` cop does auto-correction. ([@dblock][])
* Rake task now support setting formatters. ([@pmenglund][])
* [#653](https://github.com/rubocop/rubocop/issues/653): `CaseIndentation` cop is now configurable with parameters `IndentWhenRelativeTo` and `IndentOneStep`. ([@jonas054][])
* [#654](https://github.com/rubocop/rubocop/pull/654): `For` cop is now configurable to enforce either `each` (default) or `for`. ([@jonas054][])
* [#661](https://github.com/rubocop/rubocop/issues/661): `EndAlignment` cop is now configurable for alignment with `keyword` (default) or `variable`. ([@jonas054][])
* Allow to overwrite the severity of a cop with the new `Severity` param. ([@codez][])
* New cop `FlipFlop` checks for flip flops. ([@agrimm][])
* [#577](https://github.com/rubocop/rubocop/issues/577): Introduced `MethodDefParentheses` to allow for requiring either parentheses or no parentheses in method definitions. Replaces `DefWithoutParentheses`. ([@skanev][])
* [#693](https://github.com/rubocop/rubocop/pull/693): Generation of parameter values (i.e., not only `Enabled: false`) in `rubocop-todo.yml` by the `--auto-gen-config` option is now supported for some cops. ([@jonas054][])
* New cop `AccessorMethodName` checks accessor method names for non-idiomatic names like `get_attribute` and `set_attribute`. ([@bbatsov][])
* New cop `PredicateName` checks the names of predicate methods for non-idiomatic names like `is_something`, `has_something`, etc. ([@bbatsov][])
* Support Ruby 2.1 with Parser 2.1. ([@yujinakayama][])

### Changes

* Removed `SymbolNames` as it was generating way too many false positives. ([@bbatsov][])
* Renamed `ReduceArguments` to `SingleLineBlockParams` and made it configurable. ([@bbatsov][])

### Bugs fixed

* Handle properly heredocs in `StringLiterals` cop. ([@bbatsov][])
* Fix `SpaceAroundOperators` to not report missing space around operator for `def self.method *args`. ([@jonas054][])
* Properly handle `['AllCops']['Includes']` and `['AllCops']['Excludes']` when passing config via `-c`. ([@fancyremarker][], [@codez][])
* [#611](https://github.com/rubocop/rubocop/pull/611): Fix crash when loading an empty config file. ([@sinisterchipmunk][])
* Fix `DotPosition` cop with `trailing` style for method calls on same line. ([@vonTronje][])
* [#627](https://github.com/rubocop/rubocop/pull/627): Fix counting of slashes in complicated regexps in `RegexpLiteral` cop. ([@jonas054][])
* [#638](https://github.com/rubocop/rubocop/issues/638): Fix bug in auto-correct that changes `each{ |x|` to `each d o |x|`. ([@jonas054][])
* [#418](https://github.com/rubocop/rubocop/issues/418): Stop searching for configuration files above the work directory of the isolated environment when running specs. ([@jonas054][])
* Fix error on implicit match conditionals (e.g. `if /pattern/; end`) in `MultilineIfThen`. ([@agrimm][])
* [#651](https://github.com/rubocop/rubocop/issues/651): Handle properly method arguments in `RedundantSelf`. ([@bbatsov][])
* [#628](https://github.com/rubocop/rubocop/issues/628): Allow `self.Foo` in `RedundantSelf` cop. ([@chulkilee][])
* [#668](https://github.com/rubocop/rubocop/issues/668): Fix crash in `EndOfLine` that occurs when default encoding is `US_ASCII` and an inspected file has non-ascii characters. ([@jonas054][])
* [#664](https://github.com/rubocop/rubocop/issues/664): Accept oneline while when condition has local variable assignment. ([@emou][])
* Fix auto-correct for `MethodDefParentheses` when parentheses are required. ([@skanev][])

## 0.15.0 (2013-11-06)

### New features

* New cop `Output` checks for calls to print, puts, etc. in Rails. ([@daviddavis][])
* New cop `EmptyLinesAroundBody` checks for empty lines around the bodies of class, method and module definitions. ([@bbatsov][])
* `LeadingCommentSpace` cop does auto-correction. ([@jonas054][])
* `SpaceAfterControlKeyword` cop does auto-correction. ([@jonas054][])
* `SpaceAfterColon` cop does auto-correction. ([@jonas054][])
* `SpaceAfterComma` cop does auto-correction. ([@jonas054][])
* `SpaceAfterSemicolon` cop does auto-correction. ([@jonas054][])
* `SpaceAfterMethodName` cop does auto-correction. ([@jonas054][])
* `SpaceAroundBlockBraces` cop does auto-correction. ([@jonas054][])
* `SpaceAroundEqualsInParameterDefault` cop does auto-correction. ([@jonas054][])
* `SpaceAroundOperators` cop does auto-correction. ([@jonas054][])
* `SpaceBeforeModifierKeyword` cop does auto-correction. ([@jonas054][])
* `SpaceInsideHashLiteralBraces` cop does auto-correction. ([@jonas054][])
* `SpaceInsideBrackets` cop does auto-correction. ([@jonas054][])
* `SpaceInsideParens` cop does auto-correction. ([@jonas054][])
* `TrailingWhitespace` cop does auto-correction. ([@jonas054][])
* `TrailingBlankLines` cop does auto-correction. ([@jonas054][])
* `FinalNewline` cop does auto-correction. ([@jonas054][])
* New cop `CyclomaticComplexity` checks the cyclomatic complexity of methods against a configurable max value. ([@jonas054][])
* [#594](https://github.com/rubocop/rubocop/pull/594): New parameter `EnforcedStyleForEmptyBraces` with values `space` and `no_space` (default) added to `SpaceAroundBlockBraces`. ([@jonas054][])
* [#603](https://github.com/rubocop/rubocop/pull/603): New parameter `MinSize` added to `WordArray` to allow small string arrays, retaining the default (0). ([@claco][])

### Changes

* [#557](https://github.com/rubocop/rubocop/pull/557): Configuration files for excluded files are no longer loaded. ([@jonas054][])
* [#571](https://github.com/rubocop/rubocop/pull/571): The default rake task now runs RuboCop over itself!. ([@nevir][])
* Encoding errors are reported as fatal offences rather than printed with red text. ([@jonas054][])
* `AccessControl` cop is now configurable with the `EnforcedStyle` option. ([@sds][])
* Split `AccessControl` cop to `AccessModifierIndentation` and `EmptyLinesAroundAccessModifier`. ([@bbatsov][])
* [#594](https://github.com/rubocop/rubocop/pull/594): Add configuration parameter `EnforcedStyleForEmptyBraces` to `SpaceInsideHashLiteralBraces` cop, and change `EnforcedStyleIsWithSpaces` (values `true`, `false`) to `EnforcedStyle` (values `space`, `no_space`). ([@jonas054][])
* Coverage builds linked from the README page are enabled again. ([@jonas054][])

### Bugs fixed

* [#561](https://github.com/rubocop/rubocop/pull/561): Handle properly negative literals in `NumericLiterals` cop. ([@bbatsov][])
* [#567](https://github.com/rubocop/rubocop/pull/567): Register an offence when the last hash parameter has braces in `BracesAroundHashParameters` cop. ([@dblock][])
* `StringLiterals` cop no longer reports errors for character literals such as ?/. That should be done only by the `CharacterLiterals` cop. ([@jonas054][])
* Made auto-correct much less likely to crash due to conflicting corrections ("clobbering"). ([@jonas054][])
* [#565](https://github.com/rubocop/rubocop/pull/565): `$GLOBAL_VAR from English library` should no longer be inserted when auto-correcting short-form global variables like `$!`. ([@nevir][])
* [#566](https://github.com/rubocop/rubocop/pull/566): Methods that just assign a splat to an ivar are no longer considered trivial writers. ([@nevir][])
* [#585](https://github.com/rubocop/rubocop/pull/585): `MethodCallParentheses` should allow methods starting with uppercase letter. ([@bbatsov][])
* [#574](https://github.com/rubocop/rubocop/issues/574): Fix error on multiple-assignment with non-array right hand side in `UselessSetterCall`. ([@yujinakayama][])
* [#576](https://github.com/rubocop/rubocop/issues/576): Output config validation warning to STDERR so that it won't be mixed up with formatter's output. ([@yujinakayama][])
* [#599](https://github.com/rubocop/rubocop/pull/599): `EndOfLine` cop is operational again. ([@jonas054][])
* [#604](https://github.com/rubocop/rubocop/issues/604): Fix error on implicit match conditionals (e.g. `if /pattern/; end`) in `FavorModifier`. ([@yujinakayama][])
* [#600](https://github.com/rubocop/rubocop/pull/600): Don't require an empty line for access modifiers at the beginning of class/module body. ([@bbatsov][])
* [#608](https://github.com/rubocop/rubocop/pull/608): `RescueException` no longer crashes when the namespace of a rescued class is in a local variable. ([@jonas054][])
* [#173](https://github.com/rubocop/rubocop/issues/173): Allow the use of `alias` in the body of an `instance_exec`. ([@bbatsov][])
* [#554](https://github.com/rubocop/rubocop/issues/554): Handle properly multi-line arrays with comments in them in `WordArray`. ([@bbatsov][])

## 0.14.1 (2013-10-10)

### New features

* [#551](https://github.com/rubocop/rubocop/pull/551): New cop `BracesAroundHashParameters` checks for braces in function calls with hash parameters. ([@dblock][])
* New cop `SpaceAfterNot` tracks redundant space after the `!` operator. ([@bbatsov][])

### Bugs fixed

* Fix bug concerning table and separator alignment of multi-line hash with multiple keys on the same line. ([@jonas054][])
* [#550](https://github.com/rubocop/rubocop/pull/550): Fix a bug where `ClassLength` counted lines of inner classes/modules. ([@yujinakayama][])
* [#550](https://github.com/rubocop/rubocop/pull/550): Fix a false positive for namespace class in `Documentation`. ([@yujinakayama][])
* [#556](https://github.com/rubocop/rubocop/pull/556): Fix "Parser::Source::Range spans more than one line" bug in clang formatter. ([@yujinakayama][])
* [#552](https://github.com/rubocop/rubocop/pull/552): `RaiseArgs` allows exception constructor calls with more than one 1 argument. ([@bbatsov][])

## 0.14.0 (2013-10-07)

### New features

* [#491](https://github.com/rubocop/rubocop/issues/491): New cop `MethodCalledOnDoEndBlock` keeps track of methods called on `do`...`end` blocks.
* [#456](https://github.com/rubocop/rubocop/issues/456): New configuration parameter `AllCops`/`RunRailsCops` can be set to `true` for a project, removing the need to give the `-R`/`--rails` option with every invocation of `rubocop`.
* [#501](https://github.com/rubocop/rubocop/issues/501): `simple`/`clang`/`progress`/`emacs` formatters now print `[Corrected]` along with offence message when the offence is automatically corrected.
* [#501](https://github.com/rubocop/rubocop/issues/501): `simple`/`clang`/`progress` formatters now print count of auto-corrected offences in the final summary.
* [#501](https://github.com/rubocop/rubocop/issues/501): `json` formatter now outputs `corrected` key with boolean value in offence objects whether the offence is automatically corrected.
* New cop `ClassLength` checks for overly long class definitions.
* New cop `Debugger` checks for forgotten calls to debugger or pry.
* New cop `RedundantException` checks for code like `raise RuntimeError, message`.
* [#526](https://github.com/rubocop/rubocop/issues/526): New cop `RaiseArgs` checks the args passed to `raise/fail`.

### Changes

* Cop `MethodAndVariableSnakeCase` replaced by `MethodName` and `VariableName`, both having the configuration parameter `EnforcedStyle` with values `snake_case` (default) and `camelCase`.
* [#519](https://github.com/rubocop/rubocop/issues/519): `HashSyntax` cop is now configurable and can enforce the use of the classic hash rockets syntax.
* [#520](https://github.com/rubocop/rubocop/issues/520): `StringLiterals` cop is now configurable and can enforce either single-quoted or double-quoted strings.
* [#528](https://github.com/rubocop/rubocop/issues/528): Added a config option to `RedundantReturn` to allow a `return` with multiple values.
* [#524](https://github.com/rubocop/rubocop/issues/524): Added a config option to `Semicolon` to allow the use of `;` as an expression separator.
* [#525](https://github.com/rubocop/rubocop/issues/525): `SignalException` cop is now configurable and can enforce the semantic rule or an exclusive use of `raise` or `fail`.
* `LambdaCall` is now configurable and enforce either `Proc#call` or `Proc#()`.
* [#529](https://github.com/rubocop/rubocop/issues/529): Added config option `EnforcedStyle` to `SpaceAroundBraces`.
* [#529](https://github.com/rubocop/rubocop/issues/529): Changed config option `NoSpaceBeforeBlockParameters` to `SpaceBeforeBlockParameters`.
* Support Parser 2.0.0 (non-beta).

### Bugs fixed

* [#514](https://github.com/rubocop/rubocop/issues/514): Fix alignment of the hash containing different key lengths in one line.
* [#496](https://github.com/rubocop/rubocop/issues/496): Fix corner case crash in `AlignHash` cop: single key/value pair when configuration is `table` for '=>' and `separator` for `:`.
* [#502](https://github.com/rubocop/rubocop/issues/502): Don't check non-decimal literals with `NumericLiterals`.
* [#448](https://github.com/rubocop/rubocop/issues/448): Fix auto-correction of parameters spanning more than one line in `AlignParameters` cop.
* [#493](https://github.com/rubocop/rubocop/issues/493): Support disabling `Syntax` offences with `warning` severity.
* Fix bug appearing when there were different values for the `AllCops`/`RunRailsCops` configuration parameter in different directories.
* [#512](https://github.com/rubocop/rubocop/issues/512): Fix bug causing crash in `AndOr` auto-correction.
* [#515](https://github.com/rubocop/rubocop/issues/515): Fix bug causing `AlignParameters` and `AlignArray` auto-correction to destroy code.
* [#516](https://github.com/rubocop/rubocop/issues/516): Fix bug causing `RedundantReturn` auto-correction to produce invalid code.
* [#527](https://github.com/rubocop/rubocop/issues/527): Handle `!=` expressions in `EvenOdd` cop.
* `SignalException` cop now finds `raise` calls anywhere, not only in `begin` sections.
* [#538](https://github.com/rubocop/rubocop/issues/538): Fix bug causing `Blocks` auto-correction to produce invalid code.

## 0.13.1 (2013-09-19)

### New features

* `HashSyntax` cop does auto-correction.
* [#484](https://github.com/rubocop/rubocop/pull/484): Allow calls to self to fix name clash with argument.
* Renamed `SpaceAroundBraces` to `SpaceAroundBlockBraces`.
* `SpaceAroundBlockBraces` now has a `NoSpaceBeforeBlockParameters` config option to enforce a style for blocks with parameters like `{|foo| puts }`.
* New cop `LambdaCall` tracks uses of the obscure `lambda.(...)` syntax.

### Bugs fixed

* Fix crash on empty input file in `FinalNewline`.
* [#485](https://github.com/rubocop/rubocop/issues/485): Fix crash on multiple-assignment and op-assignment in `UselessSetterCall`.
* [#497](https://github.com/rubocop/rubocop/issues/497): Fix crash in `UselessComparison` and `NilComparison`.

## 0.13.0 (2013-09-13)

### New features

* New configuration parameter `AllowAdjacentOneLineDefs` for `EmptyLineBetweenDefs`.
* New cop `MultilineBlockChain` keeps track of chained blocks spanning multiple lines.
* `RedundantSelf` cop does auto-correction.
* `AvoidPerlBackrefs` cop does auto-correction.
* `AvoidPerlisms` cop does auto-correction.
* `RedundantReturn` cop does auto-correction.
* `Blocks` cop does auto-correction.
* New cop `TrailingBlankLines` keeps track of extra blanks lines at the end of source file.
* New cop `AlignHash` keeps track of bad alignment in multi-line hash literals.
* New cop `AlignArray` keeps track of bad alignment in multi-line array literals.
* New cop `SpaceBeforeModifierKeyword` keeps track of missing space before a modifier keyword (`if`, `unless`, `while`, `until`).
* New cop `FinalNewline` keeps tracks of the required final newline in a source file.
* Highlighting corrected in `SpaceInsideHashLiteralBraces` and `SpaceAroundBraces` cops.

### Changes

* [#447](https://github.com/rubocop/rubocop/issues/447): `BlockAlignment` cop now allows `end` to be aligned with the start of the line containing `do`.
* `SymbolName` now has an `AllowDots` config option to allow symbols like `:'whatever.submit_button'`.
* [#469](https://github.com/rubocop/rubocop/issues/469): Extracted useless setter call tracking part of `UselessAssignment` cop to `UselessSetterCall`.
* [#469](https://github.com/rubocop/rubocop/issues/469): Merged `UnusedLocalVariable` cop into `UselessAssignment`.
* [#458](https://github.com/rubocop/rubocop/issues/458): The merged `UselessAssignment` cop now has advanced logic that tracks not only assignment at the end of the method but also every assignment in every scope.
* [#466](https://github.com/rubocop/rubocop/issues/466): Allow built-in JRuby global vars in `AvoidGlobalVars`.
* Added a config option `AllowedVariables` to `AvoidGlobalVars` to allow users to whitelist certain global variables.
* Renamed `AvoidGlobalVars` to `GlobalVars`.
* Renamed `AvoidPerlisms` to `SpecialGlobalVars`.
* Renamed `AvoidFor` to `For`.
* Renamed `AvoidClassVars` to `ClassVars`.
* Renamed `AvoidPerlBackrefs` to `PerlBackrefs`.
* `NumericLiterals` now accepts a config param `MinDigits` - the minimal number of digits in the integer portion of number for the cop to check it.

### Bugs fixed

* [#449](https://github.com/rubocop/rubocop/issues/449): Remove whitespaces between condition and `do` with `WhileUntilDo` auto-correction.
* Continue with file inspection after parser warnings. Give up only on syntax errors.
* Don't trigger the HashSyntax cop on digit-starting keys.
* Fix crashes while inspecting class definition subclassing another class stored in a local variable in `UselessAssignment` (formerly of `UnusedLocalVariable`) and `ShadowingOuterLocalVariable` (like `clazz = Array; class SomeClass < clazz; end`).
* [#463](https://github.com/rubocop/rubocop/issues/463): Do not warn if using destructuring in second `reduce` argument (`ReduceArguments`).

## 0.12.0 (2013-08-23)

### New features

* [#439](https://github.com/rubocop/rubocop/issues/439): Added formatter 'OffenceCount' which outputs a summary list of cops and their offence count.
* [#395](https://github.com/rubocop/rubocop/issues/395): Added `--show-cops` option to show available cops.
* New cop `NilComparison` keeps track of comparisons like `== nil`.
* New cop `EvenOdd` keeps track of occasions where `Fixnum#even?` or `Fixnum#odd?` should have been used (like `x % 2 == 0`).
* New cop `IndentationWidth` checks for files using indentation that is not two spaces.
* New cop `SpaceAfterMethodName` keeps track of method definitions with a space between the method name and the opening parenthesis.
* New cop `ParenthesesAsGroupedExpression` keeps track of method calls with a space before the opening parenthesis.
* New cop `HashMethods` keeps track of uses of deprecated `Hash` methods.
* New Rails cop `HasAndBelongsToMany` checks for uses of `has_and_belongs_to_many`.
* New Rails cop `ReadAttribute` tracks uses of `read_attribute`.
* `Attr` cop does auto-correction.
* `CollectionMethods` cop does auto-correction.
* `SignalException` cop does auto-correction.
* `EmptyLiteral` cop does auto-correction.
* `MethodCallParentheses` cop does auto-correction.
* `DefWithParentheses` cop does auto-correction.
* `DefWithoutParentheses` cop does auto-correction.

### Changes

* Dropped `-s`/`--silent` option. Now `progress`/`simple`/`clang` formatters always report summary and `emacs`/`files` formatters no longer report.
* Dropped the `LineContinuation` cop.

### Bugs fixed

* [#432](https://github.com/rubocop/rubocop/issues/432): Fix false positive for constant assignments when rhs is a method call with block in `ConstantName`.
* [#434](https://github.com/rubocop/rubocop/issues/434): Support classes and modules defined with `Class.new`/`Module.new` in `AccessControl`.
* Fix which ranges are highlighted in reports from IfUnlessModifier, WhileUntilModifier, and MethodAndVariableSnakeCase cop.
* [#438](https://github.com/rubocop/rubocop/issues/438): Accept setting attribute on method argument in `UselessAssignment`.

## 0.11.1 (2013-08-12)

### Changes

* [#425](https://github.com/rubocop/rubocop/issues/425): `ColonMethodCalls` now allows constructor methods (like `Nokogiri::HTML()` to be called with double colon.

### Bugs fixed

* [#427](https://github.com/rubocop/rubocop/issues/427): FavorUnlessOverNegatedIf triggered when using elsifs.
* [#429](https://github.com/rubocop/rubocop/issues/429): Fix `LeadingCommentSpace` offence reporting.
* Fixed `AsciiComments` offence reporting.
* Fixed `BlockComments` offence reporting.

## 0.11.0 (2013-08-09)

### New features

* [#421](https://github.com/rubocop/rubocop/issues/421): `TrivialAccessors` now ignores methods on user-configurable whitelist (such as `to_s` and `to_hash`).
* [#369](https://github.com/rubocop/rubocop/issues/369): New option `--auto-gen-config` outputs RuboCop configuration that disables all cops that detect any offences.
* The list of annotation keywords recognized by the `CommentAnnotation` cop is now configurable.
* Configuration file names are printed as they are loaded in `--debug` mode.
* Auto-correct support added in `AlignParameters` cop.
* New cop `UselessComparison` checks for comparisons of the same arguments.
* New cop `UselessAssignment` checks for useless assignments to local variables.
* New cop `SignalException` checks for proper usage of `fail` and `raise`.
* New cop `ModuleFunction` checks for usage of `extend self` in modules.

### Bugs fixed

* [#374](https://github.com/rubocop/rubocop/issues/374): Fixed error at post condition loop (`begin-end-while`, `begin-end-until`) in `UnusedLocalVariable` and `ShadowingOuterLocalVariable`.
* [#373](https://github.com/rubocop/rubocop/issues/373) and [#376](https://github.com/rubocop/rubocop/issues/376): Allow braces around multi-line blocks if `do`-`end` would change the meaning of the code.
* `RedundantSelf` now allows `self.` followed by any ruby keyword.
* [#391](https://github.com/rubocop/rubocop/issues/391): Fix bug in counting slashes in a regexp.
* [#394](https://github.com/rubocop/rubocop/issues/394): `DotPosition` cop handles correctly code like `l.(1)`.
* [#390](https://github.com/rubocop/rubocop/issues/390): `CommentAnnotation` cop allows keywords (e.g. Review, Optimize) if they just begin a sentence.
* [#400](https://github.com/rubocop/rubocop/issues/400): Fix bug concerning nested defs in `EmptyLineBetweenDefs` cop.
* [#399](https://github.com/rubocop/rubocop/issues/399): Allow assignment inside blocks in `AssignmentInCondition` cop.
* Fix bug in favor_modifier.rb regarding missed offences after else etc.
* [#393](https://github.com/rubocop/rubocop/issues/393): Retract support for multiline chaining of blocks (which fixed [#346](https://github.com/rubocop/rubocop/issues/346)), thus rejecting issue 346.
* [#389](https://github.com/rubocop/rubocop/issues/389): Ignore symbols that are arguments to Module#private_constant in `SymbolName` cop.
* [#387](https://github.com/rubocop/rubocop/issues/387): Do auto-correct in `AndOr` cop only if it does not change the meaning of the code.
* [#398](https://github.com/rubocop/rubocop/issues/398): Don't display blank lines in the output of the clang formatter.
* [#283](https://github.com/rubocop/rubocop/issues/283): Refine `StringLiterals` string content check.

## 0.10.0 (2013-07-17)

### New features

* New cop `RedundantReturn` tracks redundant `return`s in method bodies.
* New cop `RedundantBegin` tracks redundant `begin` blocks in method definitions.
* New cop `RedundantSelf` tracks redundant uses of `self`.
* New cop `EmptyEnsure` tracks empty `ensure` blocks.
* New cop `CommentAnnotation` tracks formatting of annotation comments such as TODO.
* Added custom rake task.
* New formatter `FileListFormatter` outputs just a list of files with offences in them (related to [#357](https://github.com/rubocop/rubocop/issues/357)).

### Changes

* `TrivialAccessors` now has an `ExactNameMatch` config option (related to [#308](https://github.com/rubocop/rubocop/issues/308)).
* `TrivialAccessors` now has an `ExcludePredicates` config option (related to [#326](https://github.com/rubocop/rubocop/issues/326)).
* Cops don't inherit from `Parser::AST::Rewriter` anymore. All 3rd party Cops should remove the call to `super` in their callbacks. If you implement your own processing you need to define the `#investigate` method instead of `#inspect`. Refer to the documentation of `Cop::Commissioner` and `Cop::Cop` classes for more information.
* `EndAlignment` cop split into `EndAlignment` and `BlockAlignment` cops.

### Bugs fixed

* [#288](https://github.com/rubocop/rubocop/issues/288): Work with absolute Excludes paths internally (2nd fix for this issue).
* `TrivialAccessors` now detects class attributes as well as instance attributes.
* [#338](https://github.com/rubocop/rubocop/issues/338): Fix end alignment of blocks in chained assignments.
* [#345](https://github.com/rubocop/rubocop/issues/345): Add `$SAFE` to the list of built-in global variables.
* [#340](https://github.com/rubocop/rubocop/issues/340): Override config parameters rather than merging them.
* [#349](https://github.com/rubocop/rubocop/issues/349): Fix false positive for `CharacterLiteral` (`%w(?)`).
* [#346](https://github.com/rubocop/rubocop/issues/346): Support method chains for block end alignment checks.
* [#350](https://github.com/rubocop/rubocop/issues/350): Support line breaks between variables on left hand side for block end alignment checks.
* [#356](https://github.com/rubocop/rubocop/issues/356): Allow safe assignment in `ParenthesesAroundCondition`.

### Misc

* Improved performance on Ruby 1.9 by about 20%.
* Improved overall performance by about 35%.

## 0.9.1 (2013-07-05)

### New features

* Added `-l/--lint` option to allow doing only linting with no style checks (similar to running `ruby -wc`).

### Changes

* Removed the `BlockAlignSchema` configuration option from `EndAlignment`. We now support only the default alignment schema - `StartOfAssignment`.
* Made the preferred collection methods in `CollectionMethods` configurable.
* Made the `DotPosition` cop configurable - now both `leading` and `trailing` styles are supported.

### Bugs fixed

* [#318](https://github.com/rubocop/rubocop/issues/318): Correct some special cases of block end alignment.
* [#317](https://github.com/rubocop/rubocop/issues/317): Fix a false positive in `LiteralInCondition`.
* [#321](https://github.com/rubocop/rubocop/issues/321): Ignore variables whose name start with `_` in `ShadowingOuterLocalVariable`.
* [#322](https://github.com/rubocop/rubocop/issues/322): Fix exception of `UnusedLocalVariable` and `ShadowingOuterLocalVariable` when inspecting keyword splat argument.
* [#316](https://github.com/rubocop/rubocop/issues/316): Correct nested postfix unless in `MultilineIfThen`.
* [#327](https://github.com/rubocop/rubocop/issues/327): Fix false offences for block expression that span on two lines in `EndAlignment`.
* [#332](https://github.com/rubocop/rubocop/issues/332): Fix exception of `UnusedLocalVariable` and `ShadowingOuterLocalVariable` when inspecting named captures.
* [#333](https://github.com/rubocop/rubocop/issues/333): Fix a case that `EnsureReturn` throws an exception when ensure has no body.

## 0.9.0 (2013-07-01)

### New features

* Introduced formatter feature, enables custom formatted output and multiple outputs.
* Added progress formatter and now it's the default. (`--format progress`).
* Added JSON formatter. (`--format json`).
* Added clang style formatter showing the offending source. code. (`--format clang`). The `clang` formatter marks a whole range rather than just the starting position, to indicate more clearly where the problem is.
* Added `-f`/`--format` option to specify formatter.
* Added `-o`/`--out` option to specify output file for each formatter.
* Added `-r/--require` option to inject external Ruby code into RuboCop.
* Added `-V/--verbose-version` option that displays Parser version and Ruby version as well.
* Added `-R/--rails` option that enables extra Rails-specific cops.
* Added support for auto-correction of some offences with `-a`/`--auto-correct`.
* New cop `CaseEquality` checks for explicit use of `===`.
* New cop `AssignmentInCondition` checks for assignment in conditions.
* New cop `EndAlignment` tracks misaligned `end` keywords.
* New cop `Void` tracks uses of literals/variables/operators in possibly void context.
* New cop `Documentation` checks for top level class/module doc comments.
* New cop `UnreachableCode` tracks unreachable code segments.
* New cop `MethodCallParentheses` tracks unwanted braces in method calls.
* New cop `UnusedLocalVariable` tracks unused local variables for each scope.
* New cop `ShadowingOuterLocalVariable` tracks use of the same name as outer local variables for block arguments or block local variables.
* New cop `WhileUntilDo` tracks uses of `do` with multi-line `while/until`.
* New cop `CharacterLiteral` tracks uses of character literals (`?x`).
* New cop `EndInMethod` tracks uses of `END` in method definitions.
* New cop `LiteralInCondition` tracks uses of literals in the conditions of `if/while/until`.
* New cop `BeginBlock` tracks uses of `BEGIN` blocks.
* New cop `EndBlock` tracks uses of `END` blocks.
* New cop `DotPosition` tracks the dot position in multi-line method calls.
* New cop `Attr` tracks uses of `Module#attr`.
* Add support for auto-correction of some offences with `-a`/`--auto-correct`.

### Changes

* Deprecated `-e`/`--emacs` option. (Use `--format emacs` instead).
* Made `progress` formatter the default.
* Most formatters (`progress`, `simple` and `clang`) now print relative file paths if the paths are under the current working directory.
* Migrate all cops to new namespaces. `RuboCop::Cop::Lint` is for cops that emit warnings. `RuboCop::Cop::Style` is for cops that do not belong in other namespaces.
* Merge `FavorPercentR` and `PercentR` into one cop called `RegexpLiteral`, and add configuration parameter `MaxSlashes`.
* Add `CountKeywordArgs` configuration option to `ParameterLists` cop.

### Bugs fixed

* [#239](https://github.com/rubocop/rubocop/issues/239): Fixed double quotes false positives.
* [#233](https://github.com/rubocop/rubocop/issues/233): Report syntax cop offences.
* Fix off-by-one error in favor_modifier.
* [#229](https://github.com/rubocop/rubocop/issues/229): Recognize a line with CR+LF as a blank line in AccessControl cop.
* [#235](https://github.com/rubocop/rubocop/issues/235): Handle multiple constant assignment in ConstantName cop.
* [#246](https://github.com/rubocop/rubocop/issues/246): Correct handling of unicode escapes within double quotes.
* Fix crashes in Blocks, CaseEquality, CaseIndentation, ClassAndModuleCamelCase, ClassMethods, CollectionMethods, and ColonMethodCall.
* [#263](https://github.com/rubocop/rubocop/issues/263): Do not check for space around operators called with method syntax.
* [#271](https://github.com/rubocop/rubocop/issues/271): Always allow line breaks inside hash literal braces.
* [#270](https://github.com/rubocop/rubocop/issues/270): Fixed a false positive in ParenthesesAroundCondition.
* [#288](https://github.com/rubocop/rubocop/issues/288): Get config parameter AllCops/Excludes from highest config file in path.
* [#276](https://github.com/rubocop/rubocop/issues/276): Let columns start at 1 instead of 0 in all output of column numbers.
* [#292](https://github.com/rubocop/rubocop/issues/292): Don't check non-regular files (like sockets, etc).
* Fix crashes in WordArray on arrays of character literals such as `[?\r, ?\n]`.
* Fix crashes in Documentation on empty modules.

## 0.8.3 (2013-06-18)

### Bug fixes

* Lock Parser dependency to version 2.0.0.beta5.

## 0.8.2 (2013-06-05)

### New features

* New cop `BlockNesting` checks for excessive block nesting.

### Bug fixes

* Correct calculation of whether a modifier version of a conditional statement will fit.
* Fix an error in `MultilineIfThen` cop that occurred in some special cases.
* [#231](https://github.com/rubocop/rubocop/issues/231): Fix a false positive for modifier if.

## 0.8.1 (2013-05-30)

### New features

* New cop `Proc` tracks uses of `Proc.new`.

### Changes

* Renamed `NewLambdaLiteral` to `Lambda`.
* Aligned the `Lambda` cop more closely to the style guide - it now allows the use of `lambda` for multi-line blocks.

### Bugs fixed

* [#210](https://github.com/rubocop/rubocop/issues/210): Fix a false positive for double quotes in regexp literals.
* [#211](https://github.com/rubocop/rubocop/issues/211): Fix a false positive for `initialize` method looking like a trivial writer.
* [#215](https://github.com/rubocop/rubocop/issues/215): Fixed a lot of modifier `if/unless/while/until` issues.
* [#213](https://github.com/rubocop/rubocop/issues/213): Make sure even disabled cops get their configuration set.
* [#214](https://github.com/rubocop/rubocop/issues/214): Fix SpaceInsideHashLiteralBraces to handle string interpolation right.

## 0.8.0 (2013-05-28)

### Changes

* Folded `ArrayLiteral` and `HashLiteral` into `EmptyLiteral` cop.
* The maximum number of params `ParameterLists` accepts in now configurable.
* Reworked `SymbolSnakeCase` into `SymbolName`, which has an option `AllowCamelCase` enabled by default.
* Migrated from `Ripper` to the portable [Parser](https://github.com/whitequark/parser).

### New features

* New cop `ConstantName` checks for constant which are not using `SCREAMING_SNAKE_CASE`.
* New cop `AccessControl` checks private/protected indentation and surrounding blank lines.
* New cop `Loop` checks for `begin/end/while(until)` and suggests the use of `Kernel#loop`.

## 0.7.2 (2013-05-13)

### Bugs fixed

* [#155](https://github.com/rubocop/rubocop/issues/155): 'Do not use semicolons to terminate expressions.' is not implemented correctly.
* `OpMethod` now handles definition of unary operators without crashing.
* `SymbolSnakeCase` now handles aliasing of operators without crashing.
* `RescueException` now handles the splat operator `*` in a `rescue` clause without crashing.
* [#159](https://github.com/rubocop/rubocop/issues/159): AvoidFor cop misses many violations.

## 0.7.1 (2013-05-11)

### Bugs fixed

* Added missing files to the gemspec.

## 0.7.0 (2013-05-11)

### New features

* Added ability to include or exclude files/directories through `.rubocop.yml`.
* Added option --only for running a single cop.
* Relax semicolon rule for one line methods, classes and modules.
* Configuration files, such as `.rubocop.yml`, can now include configuration from other files through the `inherit_from` directive. All configuration files implicitly inherit from `config/default.yml`.
* New cop `ClassMethods` checks for uses for class/module names in definitions of class/module methods.
* New cop `SingleLineMethods` checks for methods implemented on a single line.
* New cop `FavorJoin` checks for usages of `Array#*` with a string argument.
* New cop `BlockComments` tracks uses of block comments(`=begin/=end` comments).
* New cop `EmptyLines` tracks consecutive blank lines.
* New cop `WordArray` tracks arrays of words.
* [#108](https://github.com/rubocop/rubocop/issues/108): New cop `SpaceInsideHashLiteralBraces` checks for spaces inside hash literal braces - style is configurable.
* New cop `LineContinuation` tracks uses of the line continuation character (`\`).
* New cop `SymbolArray` tracks arrays of symbols.
* Print warnings for unrecognized names in configuration files.
* New cop `TrivialAccessors` tracks method definitions that could be automatically generated with `attr_*` methods.
* New cop `LeadingCommentSpace` checks for missing space after `#` in comments.
* New cop `ColonMethodCall` tracks uses of `::` for method calls.
* New cop `AvoidGlobalVars` tracks uses of non built-in global variables.
* New cop `SpaceAfterControlKeyword` tracks missing spaces after `if/elsif/case/when/until/unless/while`.
* New cop `Not` tracks uses of the `not` keyword.
* New cop `Eval` tracks uses of the `eval` function.

### Bugs fixed

* [#101](https://github.com/rubocop/rubocop/issues/101): `SpaceAroundEqualsInParameterDefault` doesn't work properly with empty string.
* Fix `BraceAfterPercent` for `%W`, `%i` and `%I` and added more tests.
* Fix a false positive in the `Alias` cop. `:alias` is no longer treated as keyword.
* `ArrayLiteral` now properly detects `Array.new`.
* `HashLiteral` now properly detects `Hash.new`.
* `VariableInterpolation` now detects regexp back references and doesn't crash.
* Don't generate pathnames like some/project//some.rb.
* [#151](https://github.com/rubocop/rubocop/issues/151): Don't print the unrecognized cop warning several times for the same `.rubocop.yml`.

### Misc

* Renamed `Indentation` cop to `CaseIndentation` to avoid confusion.
* Renamed `EmptyLines` cop to `EmptyLineBetweenDefs` to avoid confusion.

## 0.6.1 (2013-04-28)

### New features

* Split `AsciiIdentifiersAndComments` cop in two separate cops.

### Bugs fixed

* [#90](https://github.com/rubocop/rubocop/issues/90): Two cops crash when scanning code using `super`.
* [#93](https://github.com/rubocop/rubocop/issues/93): Issue with `whitespace?': undefined method`.
* [#97](https://github.com/rubocop/rubocop/issues/97): Build fails.
* [#100](https://github.com/rubocop/rubocop/issues/100): `OpMethod` cop doesn't work if method arg is not in braces.
* `SymbolSnakeCase` now tracks Ruby 1.9 hash labels as well as regular symbols.

### Misc

* [#88](https://github.com/rubocop/rubocop/issues/88): Abort gracefully when interrupted with Ctrl-C.
* No longer crashes on bugs within cops. Now problematic checks are skipped and a message is displayed.
* Replaced `Term::ANSIColor` with `Rainbow`.
* Add an option to disable colors in the output.
* Cop names are now displayed alongside messages when `-d/--debug` is passed.

## 0.6.0 (2013-04-23)

### New features

* New cop `ReduceArguments` tracks argument names in reduce calls.
* New cop `MethodLength` tracks number of LOC (lines of code) in methods.
* New cop `RescueModifier` tracks uses of `rescue` in modifier form.
* New cop `PercentLiterals` tracks uses of `%q`, `%Q`, `%s` and `%x`.
* New cop `BraceAfterPercent` tracks uses of % literals with delimiters other than ().
* Support for disabling cops locally in a file with rubocop:disable comments.
* New cop `EnsureReturn` tracks usages of `return` in `ensure` blocks.
* New cop `HandleExceptions` tracks suppressed exceptions.
* New cop `AsciiIdentifiersAndComments` tracks uses of non-ascii characters in identifiers and comments.
* New cop `RescueException` tracks uses of rescuing the `Exception` class.
* New cop `ArrayLiteral` tracks uses of Array.new.
* New cop `HashLiteral` tracks uses of Hash.new.
* New cop `OpMethod` tracks the argument name in operator methods.
* New cop `PercentR` tracks uses of %r literals with zero or one slash in the regexp.
* New cop `FavorPercentR` tracks uses of // literals with more than one slash in the regexp.

### Bugs fixed

* [#62](https://github.com/rubocop/rubocop/issues/62): Config files in ancestor directories are ignored if another exists in home directory.
* [#65](https://github.com/rubocop/rubocop/issues/65): Suggests to convert symbols `:==`, `:<=>` and the like to snake_case.
* [#66](https://github.com/rubocop/rubocop/issues/66): Does not crash on unreadable or unparsable files.
* [#70](https://github.com/rubocop/rubocop/issues/70): Support `alias` with bareword arguments.
* [#64](https://github.com/rubocop/rubocop/issues/64): Performance issue with Bundler.
* [#75](https://github.com/rubocop/rubocop/issues/75): Make it clear that some global variables require the use of the English library.
* [#79](https://github.com/rubocop/rubocop/issues/79): Ternary operator missing whitespace detection.

### Misc

* Dropped Jeweler for gem release management since it's no longer actively maintained.
* Handle pluralization properly in the final summary.

## 0.5.0 (2013-04-17)

### New features

* New cop `FavorSprintf` that checks for usages of `String#%`.
* New cop `Semicolon` that checks for usages of `;` as expression separator.
* New cop `VariableInterpolation` that checks for variable interpolation in double quoted strings.
* New cop `Alias` that checks for uses of the keyword `alias`.
* Automatically detect extensionless Ruby files with shebangs when search for Ruby source files in a directory.

### Bugs fixed

* [#59](https://github.com/rubocop/rubocop/issues/59): Interpolated variables not enclosed in braces are not noticed.
* [#42](https://github.com/rubocop/rubocop/issues/42): Received malformed format string ArgumentError from rubocop.

[@bbatsov]: https://github.com/bbatsov
[@jonas054]: https://github.com/jonas054
[@yujinakayama]: https://github.com/yujinakayama
[@dblock]: https://github.com/dblock
[@nevir]: https://github.com/nevir
[@daviddavis]: https://github.com/daviddavis
[@sds]: https://github.com/sds
[@fancyremarker]: https://github.com/fancyremarker
[@sinisterchipmunk]: https://github.com/sinisterchipmunk
[@vonTronje]: https://github.com/vonTronje
[@agrimm]: https://github.com/agrimm
[@pmenglund]: https://github.com/pmenglund
[@chulkilee]: https://github.com/chulkilee
[@codez]: https://github.com/codez
[@cyberdelia]: https://github.com/cyberdelia
[@emou]: https://github.com/emou
[@skanev]: https://github.com/skanev
[@claco]: https://github.com/claco
[@rifraf]: https://github.com/rifraf
[@scottmatthewman]: https://github.com/scottmatthewman
[@ma2gedev]: https://github.com/ma2gedev
[@jeremyolliver]: https://github.com/jeremyolliver
[@hannestyden]: https://github.com/hannestyden
[@geniou]: https://github.com/geniou
[@jkogara]: https://github.com/jkogara
[@tmorris-fiksu]: https://github.com/tmorris-fiksu
[@mockdeep]: https://github.com/mockdeep
[@hiroponz]: https://github.com/hiroponz
[@tamird]: https://github.com/tamird
[@fshowalter]: https://github.com/fshowalter
[@cschramm]: https://github.com/cschramm
[@bquorning]: https://github.com/bquorning
[@bcobb]: https://github.com/bcobb
[@irrationalfab]: https://github.com/irrationalfab
[@tommeier]: https://github.com/tommeier
[@sfeldon]: https://github.com/sfeldon
[@biinari]: https://github.com/biinari
[@barunio]: https://github.com/barunio
[@molawson]: https://github.com/molawson
[@wndhydrnt]: https://github.com/wndhydrnt
[@ggilder]: https://github.com/ggilder
[@salbertson]: https://github.com/salbertson
[@camilleldn]: https://github.com/camilleldn
[@mcls]: https://github.com/mcls
[@yous]: https://github.com/yous
[@vrthra]: https://github.com/vrthra
[@SkuliOskarsson]: https://github.com/SkuliOskarsson
[@jspanjers]: https://github.com/jspanjers
[@sch1zo]: https://github.com/sch1zo
[@smangelsdorf]: https://github.com/smangelsdorf
[@mvz]: https://github.com/mvz
[@jfelchner]: https://github.com/jfelchner
[@janraasch]: https://github.com/janraasch
[@jcarbo]: https://github.com/jcarbo
[@oneamtu]: https://github.com/oneamtu
[@toy]: https://github.com/toy
[@Koronen]: https://github.com/Koronen
[@blainesch]: https://github.com/blainesch
[@marxarelli]: https://github.com/marxarelli
[@katieschilling]: https://github.com/katieschilling
[@kakutani]: https://github.com/kakutani
[@rrosenblum]: https://github.com/rrosenblum
[@mattjmcnaughton]: https://github.com/mattjmcnaughton
[@huerlisi]: https://github.com/huerlisi
[@volkert]: https://github.com/volkert
[@lumeet]: https://github.com/lumeet
[@mmozuras]: https://github.com/mmozuras
[@d4rk5eed]: https://github.com/d4rk5eed
[@cshaffer]: https://github.com/cshaffer
[@eitoball]: https://github.com/eitoball
[@iainbeeston]: https://github.com/iainbeeston
[@pimterry]: https://github.com/pimterry
[@palkan]: https://github.com/palkan
[@jdoconnor]: https://github.com/jdoconnor
[@meganemura]: https://github.com/meganemura
[@zvkemp]: https://github.com/zvkemp
[@vassilevsky]: https://github.com/vassilevsky
[@gerry3]: https://github.com/gerry3
[@ypresto]: https://github.com/ypresto
[@clowder]: https://github.com/clowder
[@mudge]: https://github.com/mudge
[@mzp]: https://github.com/mzp
[@bankair]: https://github.com/bankair
[@crimsonknave]: https://github.com/crimsonknave
[@renuo]: https://github.com/renuo
[@sdeframond]: https://github.com/sdeframond
[@til]: https://github.com/til
[@carhartl]: https://github.com/carhartl
[@dylandavidson]: https://github.com/dylandavidson
[@tmr08c]: https://github.com/tmr08c
[@hbd225]: https://github.com/hbd225
[@l8nite]: https://github.com/l8nite
[@sumeet]: https://github.com/sumeet
[@ojab]: https://github.com/ojab
[@chastell]: https://github.com/chastell
[@glasnt]: https://github.com/glasnt
[@crazydog115]: https://github.com/crazydog115
[@RGBD]: https://github.com/RGBD
[@panthomakos]: https://github.com/panthomakos
[@matugm]: https://github.com/matugm
[@m1foley]: https://github.com/m1foley
[@tejasbubane]: https://github.com/tejasbubane
[@bmorrall]: https://github.com/bmorrall
[@fphilipe]: https://github.com/fphilipe
[@gotrevor]: https://github.com/gotrevor
[@awwaiid]: https://github.com/awwaiid
[@segiddins]: https://github.com/segiddins
[@urbanautomaton]: https://github.com/urbanautomaton.com
[@unmanbearpig]: https://github.com/unmanbearpig
[@maxjacobson]: https://github.com/maxjacobson
[@sliuu]: https://github.com/sliuu
[@edmz]: https://github.com/edmz
[@syndbg]: https://github.com/syndbg
[@wli]: https://github.com/wli
[@caseywebdev]: https://github.com/caseywebdev
[@MGerrior]: https://github.com/MGerrior
[@imtayadeway]: https://github.com/imtayadeway
[@mrfoto]: https://github.com/mrfoto
[@karreiro]: https://github.com/karreiro
[@dreyks]: https://github.com/dreyks
[@hmadison]: https://github.com/hmadison
[@miquella]: https://github.com/miquella
[@jhansche]: https://github.com/jhansche
[@cornelius]: https://github.com/cornelius
[@eagletmt]: https://github.com/eagletmt
[@apiology]: https://github.com/apiology
[@alexdowad]: https://github.com/alexdowad
[@minustehbare]: https://github.com/minustehbare
[@tansaku]: https://github.com/tansaku
[@ptrippett]: https://github.com/ptrippett
[@br3nda]: https://github.com/br3nda
[@jujugrrr]: https://github.com/jujugrrr
[@sometimesfood]: https://github.com/sometimesfood
[@cgriego]: https://github.com/cgriego
[@savef]: https://github.com/savef
[@volmer]: https://github.com/volmer
[@domcleal]: https://github.com/domcleal
[@codebeige]: https://github.com/codebeige
[@weh]: https://github.com/weh
[@bfontaine]: https://github.com/bfontaine
[@jawshooah]: https://github.com/jawshooah
[@DNNX]: https://github.com/DNNX
[@mvidner]: https://github.com/mvidner
[@mattparlane]: https://github.com/mattparlane
[@drenmi]: https://github.com/drenmi
[@georgyangelov]: https://github.com/georgyangelov
[@owst]: https://github.com/owst
[@seikichi]: https://github.com/seikichi
[@madwort]: https://github.com/madwort
[@annih]: https://github.com/annih
[@mmcguinn]: https://github.com/mmcguinn
[@pocke]: https://github.com/pocke
[@prsimp]: https://github.com/prsimp
[@ptarjan]: https://github.com/ptarjan
[@jweir]: https://github.com/jweir
[@Fryguy]: https://github.com/Fryguy
[@mikegee]: https://github.com/mikegee
[@tbrisker]: https://github.com/tbrisker
[@necojackarc]: https://github.com/necojackarc
[@laurelfan]: https://github.com/laurelfan
[@amuino]: https://github.com/amuino
[@dylanahsmith]: https://github.com/dylanahsmith
[@gerrywastaken]: https://github.com/gerrywastaken
[@bolshakov]: https://github.com/bolshakov
[@jastkand]: https://github.com/jastkand
[@graemeboy]: https://github.com/graemeboy
[@akihiro17]: https://github.com/akihiro17
[@magni-]: https://github.com/magni-
[@NobodysNightmare]: https://github.com/NobodysNightmare
[@gylaz]: https://github.com/gylaz
[@tjwp]: https://github.com/tjwp
[@neodelf]: https://github.com/neodelf
[@josh]: https://github.com/josh
[@natalzia-paperless]: https://github.com/natalzia-paperless
[@jules2689]: https://github.com/jules2689
[@giannileggio]: https://github.com/giannileggio
[@deivid-rodriguez]: https://github.com/deivid-rodriguez
[@pclalv]: https://github.com/pclalv
[@flexoid]: https://github.com/flexoid
[@sgringwe]: https://github.com/sgringwe
[@Tei]: https://github.com/Tei
[@haziqhafizuddin]: https://github.com/haziqhafizuddin
[@dvandersluis]: https://github.com/dvandersluis
[@QuinnHarris]: https://github.com/QuinnHarris
[@sooyang]: https://github.com/sooyang
[@metcalf]: https://github.com/metcalf
[@annaswims]: https://github.com/annaswims
[@soutaro]: https://github.com/soutaro
[@nicklamuro]: https://github.com/nicklamuro
[@mikezter]: https://github.com/mikezter
[@joejuzl]: https://github.com/joejuzl
[@hedgesky]: https://github.com/hedgesky
[@tjwallace]: https://github.com/tjwallace
[@scottohara]: https://github.com/scottohara
[@koic]: https://github.com/koic
[@groddeck]: https://github.com/groddeck
[@b-t-g]: https://github.com/b-t-g
[@coorasse]: https://github.com/coorasse
[@tcdowney]: https://github.com/tcdowney
[@logicminds]: https://github.com/logicminds
[@abrom]: https://github.com/abrom
[@thegedge]: https://github.com/thegedge
[@jmks]: https://github.com/jmks/
[@connorjacobsen]: https://github.com/connorjacobsen
[@legendetm]: https://github.com/legendetm
[@bronson]: https://github.com/bronson
[@albus522]: https://github.com/albus522
[@sihu]: https://github.com/sihu
[@kamaradclimber]: https://github.com/kamaradclimber
[@swcraig]: https://github.com/swcraig
[@jessieay]: https://github.com/jessieay
[@tiagocasanovapt]: https://github.com/tiagocasanovapt
[@iGEL]: https://github.com/iGEL
[@tessi]: https://github.com/tessi
[@ivanovaleksey]: https://github.com/ivanovaleksey
[@Ana06]: https://github.com/Ana06
[@aroben]: https://github.com/aroben
[@olliebennett]: https://github.com/olliebennett
[@aesthetikx]: https://github.com/aesthetikx
[@tdeo]: https://github.com/tdeo
[@AlexWayfer]: https://github.com/AlexWayfer
[@amogil]: https://github.com/amogil
[@kevindew]: https://github.com/kevindew
[@lucasuyezu]: https://github.com/lucasuyezu
[@breckenedge]: https://github.com/breckenedge
[@enriikke]: https://github.com/enriikke
[@iguchi1124]: https://github.com/iguchi1124
[@vergenzt]: https://github.com/vergenzt
[@rahulcs]: https://github.com/rahulcs
[@dominh]: https://github.com/dominh
[@sue445]: https://github.com/sue445
[@zverok]: https://github.com/zverok
[@backus]: https://github.com/backus
[@AdrienSldy]: https://github.com/adriensldy
[@pat]: https://github.com/pat
[@sinsoku]: https://github.com/sinsoku
[@nodo]: https://github.com/nodo
[@onk]: https://github.com/onk
[@dabroz]: https://github.com/dabroz
[@buenaventure]: https://github.com/buenaventure
[@dorian]: https://github.com/dorian
[@attilahorvath]: https://github.com/attilahorvath
[@droptheplot]: https://github.com/droptheplot
[@wkurniawan07]: https://github.com/wkurniawan07
[@kddeisz]: https://github.com/kddeisz
[@ota42y]: https://github.com/ota42y
[@smakagon]: https://github.com/smakagon
[@musialik]: https://github.com/musialik
[@twe4ked]: https://github.com/twe4ked
[@maxbeizer]: https://github.com/maxbeizer
[@andriymosin]: https://github.com/andriymosin
[@brandonweiss]: https://github.com/brandonweiss
[@betesh]: https://github.com/betesh
[@dpostorivo]: https://github.com/dpostorivo
[@konto-andrzeja]: https://github.com/konto-andrzeja
[@sadovnik]: https://github.com/sadovnik
[@cjlarose]: https://github.com/cjlarose
[@alpaca-tc]: https://github.com/alpaca-tc
[@ilansh]: https://github.com/ilansh
[@mclark]: https://github.com/mclark
[@klesse413]: https://github.com/klesse413
[@gprado]: https://github.com/gprado
[@yhirano55]: https://github.com/yhirano55
[@hoshinotsuyoshi]: https://github.com/hoshinotsuyoshi
[@timrogers]: https://github.com/timrogers
[@harold-s]: https://github.com/harold-s
[@daniloisr]: https://github.com/daniloisr
[@promisedlandt]: https://github.com/promisedlandt
[@oboxodo]: https://github.com/oboxodo
[@gohdaniel15]: https://github.com/gohdaniel15
[@barthez]: https://github.com/barthez
[@Envek]: https://github.com/Envek
[@petehamilton]: https://github.com/petehamilton
[@donjar]: https://github.com/donjar
[@highb]: https://github.com/highb
[@JoeCohen]: https://github.com/JoeCohen
[@theRealNG]: https://github.com/theRealNG
[@akhramov]: https://github.com/akhramov
[@jekuta]: https://github.com/jekuta
[@fujimura]: https://github.com/fujimura
[@kristjan]: https://github.com/kristjan
[@frodsan]: https://github.com/frodsan
[@erikdstock]: https://github.com/erikdstock
[@GauthamGoli]: https://github.com/GauthamGoli
[@nelsonjr]: https://github.com/nelsonjr
[@jonatas]: https://github.com/jonatas
[@jaredbeck]: https://www.jaredbeck.com
[@michniewicz]: https://github.com/michniewicz
[@bgeuken]: https://github.com/bgeuken
[@mtsmfm]: https://github.com/mtsmfm
[@bdewater]: https://github.com/bdewater
[@garettarrowood]: https://github.com/garettarrowood
[@sambostock]: https://github.com/sambostock
[@asherkach]: https://github.com/asherkach
[@tiagotex]: https://github.com/tiagotex
[@wata727]: https://github.com/wata727
[@marcandre]: https://github.com/marcandre
[@walf443]: https://github.com/walf443
[@reitermarkus]: https://github.com/reitermarkus
[@chrishulton]: https://github.com/chrishulton
[@siegfault]: https://github.com/siegfault
[@melch]: https://github.com/melch
[@nattfodd]: https://github.com/nattfodd
[@flyerhzm]: https://github.com/flyerhzm
[@ybiquitous]: https://github.com/ybiquitous
[@mame]: https://github.com/mame
[@dominicsayers]: https://github.com/dominicsayers
[@albertpaulp]: https://github.com/albertpaulp
[@orgads]: https://github.com/orgads
[@leklund]: https://github.com/leklund
[@untitaker]: https://github.com/untitaker
[@walinga]: https://github.com/walinga
[@georf]: https://github.com/georf
[@Edouard-chin]: https://github.com/Edouard-chin
[@eostrom]: https://github.com/eostrom
[@roberts1000]: https://github.com/roberts1000
[@satyap]: https://github.com/satyap
[@unkmas]: https://github.com/unkmas
[@elebow]: https://github.com/elebow
[@colorbox]: https://github.com/colorbox
[@mmyoji]: https://github.com/mmyoji
[@unused]: https://github.com/unused
[@htwroclau]: https://github.com/htwroclau
[@hamada14]: https://github.com/hamada14
[@anthony-robin]: https://github.com/anthony-robin
[@YukiJikumaru]: https://github.com/YukiJikumaru
[@jlfaber]: https://github.com/jlfaber
[@drewpterry]: https://github.com/drewpterry
[@mcfisch]: https://github.com/mcfisch
[@istateside]: https://github.com/istateside
[@parkerfinch]: https://github.com/parkerfinch
[@joshuapinter]: https://github.com/joshuapinter
[@Darhazer]: https://github.com/Darhazer
[@Wei-LiangChew]: https://github.com/Wei-LiangChew
[@svendittmer]: https://github.com/svendittmer
[@composerinteralia]: https://github.com/composerinteralia
[@PointlessOne]: https://github.com/PointlessOne
[@JacobEvelyn]: https://github.com/JacobEvelyn
[@shanecav84]: https://github.com/shanecav84
[@thomasbrus]: https://github.com/thomasbrus
[@balbesina]: https://github.com/balbesina
[@cupakromer]: https://github.com/cupakromer
[@TikiTDO]: https://github.com/TikiTDO
[@EiNSTeiN-]: https://github.com/EiNSTeiN-
[@nroman-stripe]: https://github.com/nroman-stripe
[@sunny]: https://github.com/sunny
[@tatsuyafw]: https://github.com/tatsuyafw
[@alexander-lazarov]: https://github.com/alexander-lazarov
[@r7kamura]: https://github.com/r7kamura
[@Vasfed]: https://github.com/Vasfed
[@drn]: https://github.com/drn
[@maxh]: https://github.com/maxh
[@kenman345]: https://github.com/kenman345
[@nijikon]: https://github.com/nijikon
[@mikeyhew]: https://github.com/mikeyhew
[@mkenyon]: https://github.com/mkenyon
[@repinel]: https://github.com/repinel
[@gmalette]: https://github.com/gmalette
[@MagedMilad]: https://github.com/MagedMilad
[@robotdana]: https://github.com/robotdana
[@bacchir]: https://github.com/bacchir
[@khiav223577]: https://github.com/khiav223577
[@schneems]: https://github.com/schneems
[@ShockwaveNN]: https://github.com/ShockwaveNN
[@Knack]: https://github.com/Knack
[@akanoi]: https://github.com/akanoi
[@yensaki]: https://github.com/yensaki
[@ryanhageman]: https://github.com/ryanhageman
[@autopp]: https://github.com/autopp
[@lukasz-wojcik]: https://github.com/lukasz-wojcik
[@albaer]: https://github.com/albaer
[@Kevinrob]: https://github.com/Kevinrob
[@andrew-aladev]: https://github.com/andrew-aladev
[@y-yagi]: https://github.com/y-yagi
[@DiscoStarslayer]: https://github.com/DiscoStarslayer
[@davearonson]: https://github.com/davearonson
[@timon]: https://github.com/timon
[@gsamokovarov]: https://github.com/gsamokovarov
[@itsWill]: https://github.com/itsWill
[@xlts]: https://github.com/xlts
[@takaram]: https://github.com/takaram
[@gmcgibbon]: https://github.com/gmcgibbon
[@dduugg]: https://github.com/dduugg
[@mmedal]: https://github.com/mmedal
[@timmcanty]: https://github.com/timmcanty
[@tom-lord]: https://github.com/tom-lord
[@bayandin]: https://github.com/bayandin
[@rspeicher]: https://github.com/rspeicher
[@nadiyaka]: https://github.com/nadiyaka
[@allcentury]: https://github.com/allcentury
[@antonzaytsev]: https://github.com/antonzaytsev
[@amatsuda]: https://github.com/amatsuda
[@Intrepidd]: https://github.com/Intrepidd
[@Ruffeng]: https://github.com/Ruffeng
[@roooodcastro]: https://github.com/roooodcastro
[@rmm5t]: https://github.com/rmm5t
[@marcotc]: https://github.com/marcotc
[@dazuma]: https://github.com/dazuma
[@dischorde]: https://github.com/dischorde
[@mhelmetag]: https://github.com/mhelmetag
[@Bhacaz]: https://github.com/bhacaz
[@enkessler]: https://github.com/enkessler
[@dcluna]: https://github.com/dcluna
[@tagliala]: https://github.com/tagliala
[@unasuke]: https://github.com/unasuke
[@elmasantos]: https://github.com/elmasantos
[@luciamo]: https://github.com/luciamo
[@dirtyharrycallahan]: https://github.com/dirtyharrycallahan
[@ericsullivan]: https://github.com/ericsullivan
[@aeroastro]: https://github.com/aeroastro
[@anuja-joshi]: https://github.com/anuja-joshi
[@XrXr]: https://github.com/XrXr
[@thomthom]: https://github.com/thomthom
[@Blue-Pix]: https://github.com/Blue-Pix
[@diachini]: https://github.com/diachini
[@Mange]: https://github.com/Mange
[@jmanian]: https://github.com/jmanian
[@vfonic]: https://github.com/vfonic
[@andreaseger]: https://github.com/andreaseger
[@yakout]: https://github.com/yakout
[@RicardoTrindade]: https://github.com/RicardoTrindade
[@att14]: https://github.com/att14
[@houli]: https://github.com/houli
[@lavoiesl]: https://github.com/lavoiesl
[@fwininger]: https://github.com/fwininger
[@stoivo]: https://github.com/stoivo
[@eugeneius]: https://github.com/eugeneius
[@malyshkosergey]: https://github.com/malyshkosergey
[@fwitzke]: https://github.com/fwitzke
[@okuramasafumi]: https://github.com/okuramasafumi
[@buehmann]: https://github.com/buehmann
[@halfwhole]: https://github.com/halfwhole
[@riley-klingler]: https://github.com/riley-klingler
[@prathamesh-sonpatki]: https://github.com/prathamesh-sonpatki
[@raymondfallon]: https://github.com/raymondfallon
[@crojasaragonez]: https://github.com/crojasaragonez
[@desheikh]: https://github.com/desheikh
[@laurenball]: https://github.com/laurenball
[@jfhinchcliffe]: https://github.com/jfhinchcliffe
[@jdkaplan]: https://github.com/jdkaplan
[@cstyles]: https://github.com/cstyles
[@avmnu-sng]: https://github.com/avmnu-sng
[@denys281]: https://github.com/denys281
[@tyler-ball]: https://github.com/tyler-ball
[@ayacai115]: https://github.com/ayacai115
[@ozydingo]: https://github.com/ozydingo
[@movermeyer]: https://github.com/movermeyer
[@jethroo]: https://github.com/jethroo
[@mangara]: https://github.com/mangara
[@pirj]: https://github.com/pirj
[@pawptart]: https://github.com/pawptart
[@cetinajero]: https://github.com/cetinajero
[@gfyoung]: https://github.com/gfyoung
[@Tietew]: https://github.com/Tietew
[@hanachin]: https://github.com/hanachin
[@masarakki]: https://github.com/masarakki
[@djudd]: https://github.com/djudd
[@jemmaissroff]: https://github.com/jemmaissroff
[@nikitasakov]: https://github.com/nikitasakov
[@dmolesUC]: https://github.com/dmolesUC
[@yuritomanek]: https://github.com/yuritomanek
[@egze]: https://github.com/egze
[@rafaelfranca]: https://github.com/rafaelfranca
[@knu]: https://github.com/knu
[@saurabhmaurya15]: https://github.com/saurabhmaurya15
[@DracoAter]: https://github.com/DracoAter
[@diogoosorio]: https://github.com/diogoosorio
[@jeffcarbs]: https://github.com/jeffcarbs
[@jcfausto]: https://github.com/jcfausto
[@laurmurclar]: https://github.com/laurmurclar
[@jethrodaniel]: https://github.com/jethrodaniel
[@CvX]: https://github.com/CvX
[@jschneid]: https://github.com/jschneid
[@ric2b]: https://github.com/ric2b
[@burnettk]: https://github.com/burnettk
[@andrykonchin]: https://github.com/andrykonchin
[@avrusanov]: https://github.com/avrusanov
[@mauro-oto]: https://github.com/mauro-oto
[@fatkodima]: https://github.com/fatkodima
[@karlwithak]: https://github.com/karlwithak
[@CamilleDrapier]: https://github.com/CamilleDrapier
[@shekhar-patil]: https://github.com/shekhar-patil
[@knejad]: https://github.com/knejad
[@iamravitejag]: https://github.com/iamravitejag
[@volfgox]: https://github.com/volfgox
[@colszowka]: https://github.com/colszowka
[@dsavochkin]: https://github.com/dmytro-savochkin
[@sonalinavlakhe]: https://github.com/sonalinavlakhe
[@wcmonty]: https://github.com/wcmonty
[@nguyenquangminh0711]: https://github.com/nguyenquangminh0711
[@chocolateboy]: https://github.com/chocolateboy
[@Lykos]: https://github.com/Lykos
[@jaimerave]: https://github.com/jaimerave
[@Skipants]: https://github.com/Skipants
[@sascha-wolf]: https://github.com/sascha-wolf
[@fsateler]: https://github.com/fsateler
[@iSarCasm]: https://github.com/iSarCasm
[@em-gazelle]: https://github.com/em-gazelle
[@tleish]: https://github.com/tleish
[@pbernays]: https://github.com/pbernays
[@rdunlop]: https://github.com/rdunlop
[@ghiculescu]: https://github.com/ghiculescu
[@hatkyinc2]: https://github.com/hatkyinc2
[@AllanSiqueira]: https://github.com/allansiqueira
[@zajn]: https://github.com/zajn
[@ysakasin]: https://github.com/ysakasin
[@matthieugendreau]: https://github.com/matthieugendreau
[@miry]: https://github.com/miry
[@lautis]: https://github.com/lautis
[@pdobb]: https://github.com/pdobb
[@HeroProtagonist]: https://github.com/HeroProtagonist
[@piotrmurach]: https://github.com/piotrmurach
[@javierav]: https://github.com/javierav
[@adrian-rivera]: https://github.com/adrian-rivera
[@ThomasKoppensteiner]: https://github.com/ThomasKoppensteiner
[@PhilCoggins]: https://github.com/PhilCoggins
[@tas50]: https://github.com/tas50
[@dark-panda]: https://github.com/dark-panda
[@sswander]: https://github.com/sswander
[@makicamel]: https://github.com/makicamel
[@h-lame]: https://github.com/h-lame
[@agargiulo]: https://github.com/agargiulo
[@muirdm]: https://github.com/muirdm
[@noon-ng]: https://github.com/noon-ng
[@ohbarye]: https://github.com/ohbarye
[@magneland]: https://github.com/magneland
[@k-karen]: https://github.com/k-karen
[@uplus]: https://github.com/uplus
[@asterite]: https://github.com/asterite
[@AndreiEres]: https://github.com/AndreiEres
[@jdufresne]: https://github.com/jdufresne
[@adithyabsk]: https://github.com/adithyabsk
[@cteece]: https://github.com/ceteece
[@taichi-ishitani]: https://github.com/taichi-ishitani
[@cteece]: https://github.com/cteece
[@TSMMark]: https://github.com/TSMMark
[@caalberts]: https://github.com/caalberts
[@kachick]: https://github.com/kachick
[@corroded]: https://github.com/corroded
[@osyo-manga]: https://github.com/osyo-manga
[@ob-stripe]: https://github.com/ob-stripe
[@kwerle]: https://github.com/kwerle
[@RobinDaugherty]: https://github.com/RobinDaugherty
[@etiennebarrie]: https://github.com/etiennebarrie
[@Tonkpils]: https://github.com/Tonkpils
[@timlkelly]: https://github.com/timlkelly
[@AirWick219]: https://github.com/AirWick219
[@markburns]: https://github.com/markburns
[@gregfletch]: https://github.com/gregfletch
[@thearjunmdas]: https://github.com/thearjunmdas
[@DanielVartanov]: https://github.com/DanielVartanov
[@splattael]: https://github.com/splattael
[@byroot]: https://github.com/byroot
[@itay-grudev]: https://github.com/itay-grudev
[@lilisako]: https://github.com/lilisako
[@Hugo-Hache]: https://github.com/Hugo-Hache
[@franzliedke]: https://github.com/franzliedke
[@Drowze]: https://github.com/Drowze
[@hirasawayuki]: https://github.com/hirasawayuki
[@grosser]: https://github.com/grosser
[@mttkay]: https://github.com/mttkay
[@leoarnold]: https://github.com/leoarnold
[@danieldiekmeier]: https://github.com/danieldiekmeier
[@joergschiller]: https://github.com/joergschiller
[@berkos]: https://github.com/berkos
[@nickpellant]: https://github.com/nickpellant
[@friendlyantz]: https://github.com/friendlyantz
[@issyl0]: https://github.com/issyl0
[@ydah]: https://github.com/ydah
[@chrisseaton]: https://github.com/chrisseaton
[@nobuyo]: https://github.com/nobuyo
[@johnny-miyake]: https://github.com/johnny-miyake
[@joe-sharp]: https://github.com/joe-sharp
[@henrahmagix]: https://github.com/henrahmagix
[@chris-hewitt]: https://github.com/chris-hewitt
[@rickselby]: https://github.com/rickselby
[@zachahn]: https://github.com/zachahn
[@kaitielth]: https://github.com/kaitielth
[@j-miyake]: https://github.com/j-miyake
[@FnControlOption]: https://github.com/FnControlOption
[@ccutrer]: https://github.com/ccutrer
[@Korri]: https://github.com/Korri
[@ChrisBr]: https://github.com/ChrisBr
[@mollerhoj]: https://github.com/mollerhoj
[@mattbearman]: https://github.com/mattbearman
[@wjwh]: https://github.com/wjwh
[@jcalvert]: https://github.com/jcalvert
[@tsugimoto]: https://github.com/tsugimoto
[@srcoley]: https://github.com/srcoley
[@rdeckard]: https://github.com/rdeckard
[@wildmaples]: https://github.com/wildmaples
[@hosamaly]: https://github.com/hosamaly
[@si-lens]: https://github.com/si-lens
[@akihikodaki]: https://github.com/akihikodaki
[@epaew]: https://github.com/epaew
[@isarcasm]: https://github.com/isarcasm
[@noelblaschke]: https://github.com/noelblaschke
[@KirIgor]: https://github.com/KirIgor
[@tjschuck]: https://github.com/tjschuck
[@dukaev]: https://github.com/dukaev
[@arika]: https://github.com/arika
[@soroktree]: https://github.com/soroktree
[@alexevanczuk]: https://github.com/alexevanczuk
[@such]: https://github.com/such
[@krishanbhasin-shopify]: https://github.com/krishanbhasin-shopify
[@f1sherman]: https://github.com/f1sherman
[@jaynetics]: https://github.com/jaynetics
[@SparLaimor]: https://github.com/SparLaimor
[@bfad]: https://github.com/bfad
[@istvanfazakas]: https://github.com/istvanfazakas
[@KessaPassa]: https://github.com/KessaPassa
[@jasondoc3]: https://github.com/jasondoc3
[@ThHareau]: https://github.com/ThHareau
[@ktopolski]: https://github.com/ktopolski
[@Bhacaz]: https://github.com/Bhacaz
[@naveg]: https://github.com/naveg
[@lucthev]: https://github.com/lucthev
[@nevans]: https://github.com/nevans
[@iMacTia]: https://github.com/iMacTia
[@rwstauner]: https://github.com/rwstauner
[@catwomey]: https://github.com/catwomey
[@alexeyschepin]: https://github.com/alexeyschepin
[@meric426]: https://github.com/meric426
[@loveo]: https://github.com/loveo
[@p0deje]: https://github.com/p0deje
[@bigzed]: https://github.com/bigzed
[@OwlKing]: https://github.com/OwlKing
[@ItsEcholot]: https://github.com/ItsEcholot
[@ymap]: https://github.com/ymap
[@aboutNisblee]: https://github.com/aboutNisblee
[@K-S-A]: https://github.com/K-S-A
[@earlopain]: https://github.com/earlopain
[@kpost]: https://github.com/kpost
[@marocchino]: https://github.com/marocchino
[@Strzesia]: https://github.com/Strzesia
[@maruth-stripe]: https://github.com/maruth-stripe
[@jenshenny]: https://github.com/jenshenny
[@davidrunger]: https://github.com/davidrunger
[@viralpraxis]: https://github.com/viralpraxis
[@artur-intech]: https://github.com/artur-intech
[@amomchilov]: https://github.com/amomchilov
[@Hiroto-Iizuka]: https://github.com/Hiroto-Iizuka
[@boardfish]: https://github.com/boardfish
[@muxcmux]: https://github.com/muxcmux
[@nekketsuuu]: https://github.com/nekketsuuu
[@pawelma]: https://github.com/pawelma
[@krororo]: https://github.com/krororo
[@ksss]: https://github.com/ksss
[@vlad-pisanov]: https://github.com/vlad-pisanov
[@protocol7]: https://github.com/protocol7
[@zopolis4]: https://github.com/zopolis4
[@tk0miya]: https://github.com/tk0miya
[@masato-bkn]: https://github.com/masato-bkn
[@pCosta99]: https://github.com/pCosta99
[@kotaro0522]: https://github.com/kotaro0522
[@gemmaro]: https://github.com/gemmaro
[@dak2]: https://github.com/dak2
[@d4be4st]: https://github.com/d4be4st
[@lovro-bikic]: https://github.com/lovro-bikic
[@aduth]: https://github.com/aduth
[@isuckatcs]: https://github.com/isuckatcs
[@GabeIsman]: https://github.com/GabeIsman
[@mrzasa]: https://github.com/mrzasa
[@corsonknowles]: https://github.com/corsonknowles
[@elliottt]: https://github.com/elliottt
[@kyanagi]: https://github.com/kyanagi
[@capncavedan]: https://github.com/capncavedan
[@d4rky-pl]: https://github.com/d4rky-pl
[@vinistock]: https://github.com/vinistock
[@datpmt]: https://github.com/datpmt
[@jtannas]: https://github.com/jtannas
[@flavorjones]: https://github.com/flavorjones
