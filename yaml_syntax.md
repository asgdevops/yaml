# :book: YAML Syntax

Information source and credits [^footnote].

[^footnote]: :copyright: 2003, the information presented in this repository comes from [yaml.org:tm:](https://yaml.org/) and the [Simpl¡learn DevOps Post Graduate Program](https://www.simplilearn.com/devops) materials, All Rights Reserved.

# :bookmark_tabs: Table of contents
- [:book: YAML Syntax](#book-yaml-syntax)
- [:bookmark\_tabs: Table of contents](#bookmark_tabs-table-of-contents)
- [Basic rules](#basic-rules)
- [Syntax](#syntax)
  - [Maps](#maps)
  - [Lists](#lists)
- [Data types in YAML](#data-types-in-yaml)
  - [Scalar](#scalar)
  - [List](#list)
  - [Dictionary](#dictionary)
- [YAML Mapping](#yaml-mapping)
  - [Types of mapping](#types-of-mapping)
  - [Simple mapping](#simple-mapping)
  - [Sequence mapping](#sequence-mapping)
  - [Nested mapping](#nested-mapping)
  - [Mixed mapping](#mixed-mapping)
- [YAML Sequences](#yaml-sequences)
  - [Colections](#colections)
  - [Nested sequence](#nested-sequence)
- [References](#references)

# Basic rules
- The files in YAML are saved with `.yaml` or `.yml` extension.
- YAML is case sensitive.

# Syntax

The structure of a YAML file is a **Map** or a **List**.

Colon and single space define a scalar or a variable

```yaml
String: "70"

Integer: 70

float: 70.7

boolean: Yes
```

A `|` (pipe) character means to break a string into different lines, whereas a `>` (greater than) character indicates building a single paragraph from a group of lines.

- Pipe `|` example:

  ```yaml
  data: | 
  Experience 
  is the name 
  everyone gives 
  to their mistakes. 
  Oscar Wilde
  ```

- Greater than `>` example:

  ```yaml
  data: >
  This text
  is wrapped
  and will
  be formed into
  a single paragraph.
  ```

## Maps
Maps associate key-value pairs, which is an important part of setting up data.

A YAML configuration file can start like this:

```yaml
---
apiVersion: v3
kind: Pod
metadata:
name: rss-site
labels:
app: web
```

## Lists
A list is a collection of values in a specific order that can contain any number of entries.

- A list sequence starts with a dash (-) and a space.
- Indentation separates it from the parent.
- A list can be embedded into a map.

Example: Simple YAML script for student records that follows syntax rules:

```yaml
---
#Student Details
Student-Id: 202104
First-Name: John
Parents-Name:
  - Andrew
  - Cathy
Address:
  - street: 13 Main st.
city: Houston
state: TX
education: |
4 GCSEs
3 A-Levels
…
```

# Data types in YAML

- [Scalar](#scalar).
- [List](#lists).
- [Dictionary](#dictionary).

## Scalar

In YAML, scalar means a simple value for a key.

```yaml
# Numeric data type
integer: 70
float: 70.7

# String data type
string: "Hello"

# Boolean (numeric) data type
boolean: true
```

_Scalars are often called variables in programing._

Examples of numeric data types:

- Integer and floating.

  ```yaml
  ---
  age: 2023
  octal: 3747
  hex: 0x7E7
  floating: 33.33
  exp: 12.3015e+05
  ```

- Boolean.

  ```yaml
  ---
  canonical: y
  answer: NO
  logical: True
  option: on
  ```

  |!!Bool|Expression
  |--|--|
  |Canonical| \[ y \| Y \| n \| N \] |
  |Answer| \[ yes \| Yes \| YES \| no \| No \| NO \] |
  |Logical| \[ true \| True \|TRUE \| false \| False \| FALSE \]|
  |Option| \[ on \| On \| ON \| off \| Off \| OFF \]|

- Strings in YAML are unicode.

  ```yaml
  ---
  str1: here you have a good example
  str2: "Hello there\n"
  null1: null
  null2: ~
  ```

## List
In YAML, each item in the list is of key-value pairs, commonly called a “hash” or a “dictionary”.

- Exmaples:

  ```yaml
  ---
  # List in a single line
  items: [1, 2, 3, 4, 5]
  name: [one, two, three, four, five]

  # List in multiple lines
  items2:
    - 6
    - 7
    - 8
    
  # Complex objects
  items3:
    - values:
        value1:
        value2:
        value3:
  ```

## Dictionary
Dictionary is a collection of key-value pairs.

- Example:
  ```yaml
  ---
  - developer1:
    name: joe
    skills: 
      - python
      - java
      - yaml

  - developer2:
    name: jane
    skills: 
      - c
      - perl
      - ruby
  ```

# YAML Mapping
YAML mappings are associative arrays, hash tables, key-value pairs, or collections.

## Types of mapping
- [Simple mapping](#simple-mapping).
- [Sequence mapping](#sequence-mapping).
- [Nested mapping](#nested-mapping).
- [Mixed Mapping](#mixed-mapping).

_In mapping, the name of two keys can't be the same._

## Simple mapping

```yaml
---
hostname: vmubuntu2204
ipaddress: 192.168.56.23
cpus: 2
```

## Sequence mapping
```yaml
---
student: james
subjects: 
  - maths
  - science
```

## Nested mapping
```yaml
---
region: us
city: boston
hostname: vmubuntu2204
  ip: 172.16.15.21
  cpu: 2 
```

## Mixed mapping
```yaml
---
student: 458962

fullName: 
  firstName: joe
  lastName: doe

subjects:
  - ansible
  - docker
  - git
  - kubernetes
```

# YAML Sequences

## Colections

In YAML, collections are represented in sequences in the form of lists or arrays.

```yaml
---
hobbies:
  - dancing
  - music
  - singing
  - painting
```

## Nested sequence

Nested Sequence with items and subitems can be achieved by placing a single space before each dash in the sub-items.

```yaml
---
id: 458963
student: jane
  country: us
  age: 25
  married: no
skills:
  - python
  - java
  - sql
```

# References
- [yaml.org:tm:](https://yaml.org/) 
- [Boolean Language-Independent Type for YAML:tm: Version 1.1](https://yaml.org/type/bool.html)
