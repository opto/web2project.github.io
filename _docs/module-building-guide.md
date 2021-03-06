---
layout: page
title: Module Building Guide

status: draft
---

The goal of this section is to document a clear, repeatable way for developers to create modules to supplement and enhance the operation of the web2project system. There are numerous code samples included because showing is often more important than explaining. As certain non-core functionality becomes standardized, some of it will be added to the core system itself. This will not only simplify Add On development but also make sure that all modules adhere to the same standards and logic flows.

Failure to follow the recommendations in this section can lead to non-functioning modules, brittle code prone to breaking, security vulnerabilities, and even bad hair days. None of these are pleasant.

## Expectations

*  All input MUST be filtered before it is used in '''any''' capacity to help prevent security vulnerabilities such as [SQL injection](http://en.wikipedia.org/wiki/SQL_injection) and [Cross Site Scripting](http://en.wikipedia.org/wiki/Cross-site_scripting) attacks.
*  A module MUST NOT have raw SQL statements.
*  A module MUST NOT have references to the w2p_Database_Query class/object outside of the module's core class and (optional) subclasses.
*  A module SHOULD use core web2project function/method/API calls instead of copy/pasting logic into your own module.
*  A module SHOULD adhere to our custom [Naming Conventions](/docs/naming-conventions.html) for variables, methods, etc.
*  All code within a module SHOULD adhere to the formatting specified by the [PEAR Coding Standard](http://pear.php.net/manual/en/standards.php). To evaluate your own code, please use [Code Sniffer](http://pear.php.net/package/PHP_CodeSniffer/).

## Table of Contents

{% assign items = site.docs | where:"category","module building guide" %}

{% include dual-columns.md %}

## Hooks

**Available Since:** v1.1 (September 2009) - Calendar Hook, Cron Hook, Search Hook

**Available Since:** v3.0 (September 2013) - Pre-Store Hook, Post-Store Hook, Pre-Create Hook, Post-Create Hook, Pre-Update Hook, Post-Update Hook, Pre-Load Hook, Post-Load Hook, Pre-Delete Hook, Post-Delete Hook.

{% assign items = site.docs | where:"category","hooks" %}

{% include dual-columns.md %}