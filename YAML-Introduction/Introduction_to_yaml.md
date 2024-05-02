# YAML Introduction

YAML stands for YAML Ain't Markup Language, but it originally stood for Yet Another Markup Language. It's designed to be easily readable by both humans and machines, making it a popular choice for configuration files, particularly in environments like Kubernetes.

## What is YAML?

YAML is a human-readable data serialization language, just like XML and JSON. Serialization is a process where one application or service that has different data structures and is written in a different set of technologies can transfer data to another application using a standard format. The data in the new format can be stored in a file or transmitted to another application or service over a network. YAML is a widely used format for writing configuration files for different DevOps tools, programs, and applications because of its human-readable and intuitive syntax.

## XML VS JSON VS YAML - What's The Difference?

XML, JSON, and YAML are all used for creating configuration files and transferring data between applications. Each language has its advantages and disadvantages.

## XML

XML, short for Extensible Markup Language

Functioning as a broad markup language, XML presents a structured yet adaptable syntax alongside a specified document schema. These attributes render it advantageous for managing intricate configurations necessitating a structured layout and meticulous schema validation to uphold consistent formatting standards.

However, XML's syntax tends to be verbose, repetitive, and less legible when contrasted with alternative serialization languages. XML has a more rigid structure with opening and closing tags.

```XML
<Employees>
    <Employee> 
        <name> John Doe </name>
        <department> Engineering </department>
        <country> USA </country>
    </Employee>
     <Employee> 
        <name> Kate Kateson </name>
        <department> IT Support </department>
        <country> United Kingdom </country>
    </Employee>
</Employees>
```

## JSON

JSON, which expands to JavaScript Object Notation

Initially influenced by the JavaScript programming language, JSON isn't confined to a single language but instead serves as a language-agnostic format. Nearly all contemporary programming languages feature libraries for processing and generating JSON data.

Compared to XML, JSON boasts a significantly clearer, user-friendly, concise, and straightforward syntax. It serves as an excellent choice for storing and transmitting data between web applications and servers via a network.

However, it might not provide optimal assistance for intricate configurations.

```JSON
{
	"Employees": [
    {
			"name": "John Doe",
			"department": "Engineering",
			"country": "USA"
		},

		{
			"name": "Kate Kateson",
			"department": "IT support",
			"country": "United Kingdom"
		}
	]
}
```

## YAML

YAML is an official strict superset of JSON despite looking very different from JSON.

YAML can do everything that JSON can and more. A valid YAML file can contain JSON, and JSON can transform into YAML.

YAML has the most human-readable, intuitive, and compact syntax for defining configurations compared to XML and JSON.

YAML uses indentation to define structure in the file, which is helpful if you are used to writing Python code and are familiar with the indentation style the language uses.

With that said, if you don't get the indentation and format right, it can lead to validation errors, making it not the friendliest for beginners.

```YAML
Employees:
- name: John Doe
  department: Engineering
  country: USA
- name: Kate Kateson
  department: IT support
  country: United Kingdom
```

YAML allows multiple YAML documents in a singe YAML file, making file organization much easier. This can be done by using the `---` separator or by using the `...` separator.

```YAML
---
Employees:
- name: John Doe
  department: Engineering
  country: USA
- name: Kate Kateson
  department: IT support
  country: United Kingdom
---
Fruit:
 - Oranges
 - Pears
 - Apples
```

## Indentation in YAML

In YAML, there is an emphasis on indentation and line separation to denote levels and structure in data. The indentation system is quite similar to the one Python uses.

YAML doesn't use symbols such as curly braces, square brackets, or opening or closing tags - just indentation. YAML doesn't allow to use any tabs when creating indentation in YAML files. YAML uses spaces to denote indentation.

## How to write a comment in YAML

To add a comment to comment out a line of code, use the # character.

```YAML
# This is a comment
```

## Collections

Collections in YAML can be:

Sequences (lists/arrays)
Mappings (dictionaries/hashes)

### Sequences

Sequences are lists of values. To write a sequence, use a dash (-) followed by a space: `- item1`

```YAML
- item1
- item2
- item3
```

Each item in the sequence (list) is placed on a separate line, with a dash in front of the value.
And each item in the list is on the same level.

### Mappings

Mappings are dictionaries. To write a mapping, use a colon (:) followed by a space: `key: value`

```YAML
key1: value1
key2: value2
key3: value3
```
Each key-value pair in the mapping is placed on a separate line, with a colon in front of the value. And each key-value pair in the mapping is on the same level.

### List of dictionaries

```YAML
cars:
  - brand: Toyota
    model: 
        name: Corolla
        year: 2022
    color: blue
    mileage: 15000
  - brand: Honda
    model: 
        name: Civic
        year: 2021
    color: silver
    mileage: 18000
  - brand: Ford
    model: 
        name: Mustang
        year: 2020
    color: red
    mileage: 20000
```
The YAML code is using the - character to indicate that each car is an item in the list, and it is using the : character to indicate that each key-value pair is a dictionary.

In summary, the provided YAML code is valid and defines a list of three cars, where each car is represented as a dictionary with the keys brand, model, color, and mileage.

## Conclusion?

In conclusion, YAML offers a simple and readable way to represent data and configurations, making it a popular choice for various applications, especially in environments like Kubernetes where human readability and machine interpretability are crucial.
