Public API Changes:
---
  - Version 1.9.4.91: Breaking, short name of an option must be defined as character (``System.Char``). Non breaking, added support for verbs.
  - Version 1.9.4.99: Breaking, removed dependency from ``CommandLineOptionsBase``, introduced [ParseStateAttribute](https://github.com/gsscoder/commandline/blob/master/src/sample/Program.cs).
  - Version 1.9.4.107: Non breaking, implemented [strict parsing](https://github.com/gsscoder/commandline/blob/master/src/tests/Parser/StrictFixture.cs) (see issue #32).
  - Version 1.9.4.109: Non breaking, pull request #44.
  - Version 1.9.4.111: Non breaking, ``CommandLineParserSettings``, ``CommandLineParser`` implements ``IDisposable``.
  - Version 1.9.4.113: Non breaking, added ``CommandLineParser::WasVerbOptionInvoked`` helper method.
  - Version 1.9.4.123: Breaking, ``HandleParsingErrorsDelegate`` renamed to ``ParsingErrorsHandler``, ``MultiLineTextAttribute`` renamed to ``MultilineTextAttribute``. Non breaking, refactoring (see ChangeLog).
  - Version 1.9.4.127: 'Partially' non breaking, ``OptionAttribute`` is now sealed. ``OptionArrayAttribute`` and ``OptionListAttribute`` derives from ``BaseOptionAttribute`` (update your custom types too).
  - Version 1.9.4.201: Non breaking, introduced ``ValueOptionAttribute`` enhancement of issue #33.
  - Version 1.9.4.207: Breaking: ``CommandLineParser``, ``ICommandLineParser``, ``CommandLineParserSettings``, ``CommandLineParserException`` renamed to ``Parser``, ``IParser``, ``ParserSettings``, ``ParserException`` as explained [here](https://github.com/gsscoder/commandline/issues/48).
  - Version 1.9.4.209: Non breaking, added fluent builder (``ParserConfigurator``, see issue #42).
  - Version 1.9.4.211: 'Partially' non breaking, ParsingErrorsHandler delegate replaced by Action<HelpText>.
  - Version 1.9.4.217: Non breaking, Extracted interface ``IParserSettings`` from ``ParserSettings``. Changed consumers to depends on ``IParserSettings`` rather on concrete default implementation.
  - Version 1.9.4.219: Non breaking, ``ValueOption`` supports ``Index`` (Remarks: in next Dtable will mandatory).
  - Version 1.9.4.223: Non breaking, added ``IParserSettings::ParsingCulture`` and ``ParserConfigurator::UseCulture``.
  - Version 1.9.4.225: Breaking, default singleton parsing culture is ``CultureInfo.InvariantCulture``; this is not general default only the one of default singleton.
  - Version 1.9.4.223: 'Partially' non breaking, all attributes are now in root namespace.
  - Version 1.9.5.0: Breaking (in some cases), removed ``IParser::ParseArguments`` overloads (see ChangeLog); removed ``::WasVerbOptionInvoked``; use new  ``HelpText::AutoBuild(object,string)`` instead of obsolete ``::GetVerbOptionsInstanceByName``.
  - Version 1.9.6.1: Non breaking (if implicit syntax), reverting back genericity from IParser.
  - Version 1.9.61.1: Non breaking, omitting longname default -> property name lower case.
  - Version 1.9.62.2: 'Partially' breaking, ``IParserConfigurator`` made nested type of Parser; ``ParserConfigurator::HelpWriter(...)`` renamed to ``ParserConfigurator::UseHelpWriter(...)``.
  - Version 1.9.69.1: Breaking (in some cases), removed ``IParser``,  ``IParserSettings`` and ``ParserConfigurator``.