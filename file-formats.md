# File Formatsin Big Data

### Agenda
* What are File Formats
* csv
* xml
* json
* avro
* parquet
* orc

### What are File Formats
* A file format is a standard way that information is encoded for storage in a computer file. It specifies how bits are used to encode information in a digital storage
* Files can be encoded in human readable (plaintext) or binary formats
* Human readable text files can have different encodings, like ASCII(meant for american english) or UTF8 (supports all languages)
* Many operating systems use the file extension as a way to determine the encoding of the file
* Many file formats also contain a positional/relative metadata section, usually as a header or footer. These can be used to define aspects and validate the data

1. Using VSCode create two files containing the string `MyBrand© units were sold for €40k`.
2. Save each of the files with a different encoding: UTF-8 and ISO 8859-1
3. Check the difference in file size for each
4. Try to close and re-open those files. What happened?
5. Which format should we default to when working with plaintext files?

### csv
* csv is the most common format for dsv: delimiter separated values
* they became extremely popular due to its tabular simplicity and compatibility with MSExcel and SQL database exports
* might contain headers or not
* can use different separators for values
* not well standardized, which causes a lot of issues in production environments

1. Open the <TBD> csv file using pandas and perform some basic exploration on the dataset.
2. Save it in excel format and take a look at the excel file contents and size. 

### xml
* xml is a markup language defining rules for encoding documents that are both human and machine readable with a strict standard
* written in plaintext usually encoded in utf8
* support dtd and xsd schemas to describe and validate data in xml files, both support datatypes to be added to data 
* is very verbose and can be very complex

1. Save your previous dataset in xml format using <TBD> 

### json
* json is a lightweight data-interchange format. It is easy for humans to read and write
* written in plaintext usually encoded in utf8
* uses key-value pairs and lists of values as nested data structures
* it's one of the most common formats used for web APIs, making json data widely available 

1. Save your previous dataset in json format using <TBD>

### avro
* avro is a row-oriented data format optimized to serialize large amounts of data
* schema is embedded within the file
* is binary and not human readable
* used on many apache hadoop/hive and apache kafka implementations

1. Save your previous dataset in avro format using <TBD> 

### parquet
* parquet is a column-oriented data format optimized to execute fast queries
* schema is embedded within the the file
* is binary and not human readable
* used on many apache hadoop/hive and apache spark implementations

1. Save your previous dataset in parquet format using <TBD> 

### orc
* orc is a column-oriented data format optimized to execute fast queries
* schema is embedded within the the file
* is binary and not human readable
* used on many apache hive implementations

1. Save your previous dataset in orc format using <TBD>

### Final Notes on File Formats
* There's no "best" file format, each of them has its strong points and deciding on the right file format for the right use case is a very important decision in a Big Data project
* Data exploration will benefit from human readable formats, while large scale production will benefit from optimized and compressed file formats
* Take your environment and tooling constraints into consideration when deciding the file formats to use in a project
* Several compression standards are available in the market: zip, bzip, gzip, lz4, Snappy, and those can be applied to most of the formats seen above

### Additional Exercises Material
* [Extra exercises](./5-pythonadv-exercises.md): Additional exercises to practice

### Recommended Readings
* [Json Data Format](https://www.json.org/json-en.html): specification
* [Big Data Formats](https://luminousmen.com/post/big-data-file-formats): overview and benchmark between Big Data formats 
* [Avro/Parquet/ORC](https://www.nexla.com/new-whitepaper-understanding-avro-parquet-orc/): comparison between the three formats

[Back To Main Page](./index.md)