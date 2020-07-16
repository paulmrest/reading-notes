# Read 09 - LINQ & Delegates

## [Language Integrated Query (LINQ)](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/)
## [Introduction to LINQ Queries (C#)](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/introduction-to-linq-queries)
## [Basic LINQ Query Operations (C#)](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/basic-linq-query-operations)
## [Walkthrough: Writing Queries in C# (LINQ)](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/walkthrough-writing-queries-linq)
## C# 7.0 in a Nutshell by Joseph and Ben Albahari
### Chapter 8: LINQ Queries

We're here! LINQ, and I'm so exhausted I can barely understand what I'm reading.

One thing that did immediately jump out at me is that the queries are IEnumerable references. I am assuming we're going to be building out our knowledge of that interface for LINQ queries.

I also didn't get before this how close LINQ queries are to SQL. Slightly different order of terms, but otherwise a lot of the same basic elements are there (SELECT, FROM, WHERE, JOIN, GROUP, etc...). Also the terms that MS uses in their documentation for LINQ queries is quite similar to what they use in SQL Server Management Studio and SQL Server Reporting Services.

It's a little funny that you iterate over the LINQ query, but that makes sense with it being an IEnumerable reference.