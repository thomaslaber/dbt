# dbt Study guide

### Links

* source: https://www.biztory.com/blog/how-to-pass-the-dbt-analytics-engineering-certification
* slides: https://www.getdbt.com/dbt-learn/lessons/
  * intro: https://www.getdbt.com/dbt-learn/lessons/dbt-fundamentals

### Checklist

* staging:
  * file names: `stg_[source]__[entity]s.sql`
  * Subdirectories based on the source system.
  * Tasks:
    * Renaming
    * ✅ Type casting
    * ✅ Basic computations
    * ✅ Categorizing
    * ❌ Joins 
    * ❌ Aggregations
  * ✅ Materialized as views
  * 1-to-1 relationship to our `source`  tables
* intermediate:
  * ❌ Exposed to end users.
  * ✅ Materialized ephemerally
  * ✅ Materialized as views in a custom schema with special permissions
  * ✅ Structural simplification
  * ✅ Re-graining
  * ✅ Isolating complex operations
* marts:
  * ✅ Group by department or area of concern
  * ✅ Name by entity
  * ❌ Build the same concept differently for different teams
  * ✅ Materialized as tables or incremental models
  * ✅ Wide and denormalized
  * ❌ Too many joins in one mart
  * ✅ Build on separate marts thoughtfully

<details>
    <summary>materializations</summary>
    
    the 5 types of materializations

    * 🔍 views
    * ⚒️ tables
    * 📚 incremental model
    * ephemeral
    * python

    source: https://docs.getdbt.com/docs/build/materializations#materializations
</details>

<details>
    <summary>Jinja basic concepts<</summary>
    Delimiters, variables, IF-THEN statements, FOR loops, macros.
</details>

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```