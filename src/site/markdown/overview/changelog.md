# Changelog

## ???? - 5.2.0:

**Modularization of the source code:**

The source code of pmd was undergoing a major restructuring. Each language is separated
out into its own module. This reduces the size of the artifacts significantly, if only
one language is needed.

Therefore, the maven coordinates needed to change. In order to just use pmd with java support, you'll need
the following two dependencies:

    <dependency>
        <groupId>net.sourceforge.pmd</groupId>
        <artifactId>pmd-core</artifactId>
        <version>5.2.0</version>
    </dependency>
    <dependency>
        <groupId>net.sourceforge.pmd</groupId>
        <artifactId>pmd-java</artifactId>
        <version>5.2.0</version>
    </dependency>

The binary package still contains all languages and can be used as usual.

**New Languages**

* CPD supports now [Go](https://golang.org/).

**Bugfixes:**

**Feature Requests and Improvements:**

**Pull requests:**

* [#9](https://github.com/adangel/pmd/pull/9/): New rule: NoUnsanitizedJSPExpressionRule
* [#44](https://github.com/pmd/pmd/pull/44/): Add GoLang support to CPD

**New/Modified Rules:**

* JSP - Basic ruleset:
    * NoUnsanitizedJSPExpression: Using unsanitized JSP expression can lead to Cross Site Scripting (XSS) attacks