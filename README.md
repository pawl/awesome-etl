# awesome-etl
A curated list of notable ETL (extract, transform, load) frameworks, libraries and software.

- [Awesome ETL](#awesome-etl)
    - [Workflow Management/Engines](#workflow-managementengines)
    - [Job Scheduling](#job-scheduling)
    - [Python](#python)
    - [Ruby](#ruby)
    - [Go](#go)
    - [Java](#java)
    - [Talks/Articles](#talksarticles-1)
    - [Cloud Services](#cloud-services)
    - [Big Data (Hadoop Stack)](#big-data-hadoop-stack)
    - [ETL Tools (GUI)](#etl-tools-gui)

## Related Lists
* [awesome-pipeline](https://github.com/pditommaso/awesome-pipeline)

## Workflow Management/Engines
* [Airflow](https://github.com/apache/airflow) - "Use airflow to author workflows as directed acyclic graphs (DAGs) of tasks. The airflow scheduler executes your tasks on an array of workers while following the specified dependencies. Rich command line utilities make performing complex surgeries on DAGs a snap. The rich user interface makes it easy to visualize pipelines running in production, monitor progress, and troubleshoot issues when needed."
* [Azkaban](https://azkaban.github.io/) - "a batch workflow job scheduler created at LinkedIn to run Hadoop jobs. Azkaban resolves the ordering through job dependencies and provides an easy to use web user interface to maintain and track your workflows."
* [Dray.it](http://dray.it/) - "Docker workflow engine. Allows users to separate a workflow into discrete steps each to be handled by a single container."
* [Luigi](https://github.com/spotify/luigi) - "a Python module that helps you build complex pipelines of batch jobs. It handles dependency resolution, workflow management, visualization etc. It also comes with Hadoop support built in."
* [Mara](https://github.com/mara/data-integration) - "A lightweight opinionated ETL framework, halfway between plain scripts and Apache Airflow"
* [Pinball](https://github.com/pinterest/pinball) - "a scalable workflow management platform developed at Pinterest. It is built based on layered approach."
* [TaskFlow](https://wiki.openstack.org/wiki/TaskFlow) - "allows the creation of lightweight task objects and/or functions that are combined together into flows (aka: workflows) in a declarative manner. It includes engines for running these flows in a manner that can be stopped, resumed, and safely reverted."
* [Toil](https://toil.readthedocs.io/en/latest/) - Similar to Luigi, jobs are classes with a run method. Supports executing jobs on other machines (workers) which can include AWS spot instances.

## Job Scheduling
* [Chronos](https://github.com/mesos/chronos) - "a distributed and fault-tolerant scheduler that runs on top of Apache Mesos that can be used for job orchestration."
* [Dagobah](https://github.com/thieman/dagobah) - "a simple dependency-based job scheduler written in Python. Dagobah allows you to schedule periodic jobs using Cron syntax. Each job then kicks off a series of tasks (subprocesses) in an order defined by a dependency graph you can easily draw with click-and-drag in the web interface."
* [Jenkins](https://github.com/jenkinsci/jenkins) - "the leading open-source automation server. Built with Java, it provides over 1000 plugins to support automating virtually anything, so that humans can actually spend their time doing things machines cannot."

## Java
* [GETL](https://github.com/ascrus/getl) - Groovy toolbox for ETL Tasks from practicing architectures
* [JSR 352](https://www.jcp.org/en/jsr/detail?id=352) - Java native API for batch processing
* [Scriptella](http://scriptella.org/) - Java-XML ETL toolbox for every day use.
* [Spring Batch](http://projects.spring.io/spring-batch/) - ETL on Spring ecosystem

## Python
### Libraries
* [BeautifulSoup](http://www.crummy.com/software/BeautifulSoup/) - Popular library used to extract data from web pages.
* [Blaze](https://github.com/blaze/blaze) - "translates a subset of modified NumPy and Pandas-like syntax to databases and other computing systems."
* [Bonobo](https://www.bonobo-project.org/) - Simple, modern and atomic data transformation graphs for Python 3.5+.
* [Bubbles](https://github.com/stiivi/bubbles) - "a Python ETL Framework and set of tools. It can be used for processing, auditing and inspecting data. Focus is on understandability and transparency of the process."
* [Celery](http://www.celeryproject.org/) - "an asynchronous task queue/job queue based on distributed message passing. It is focused on real-time operation, but supports scheduling as well."
* [Dask](https://github.com/blaze/dask) - Ever tried using Pandas to process data that won't fit into memory? Dask makes it easy. Dask also has functionality to make it easy to processing continuous streams of data.
* [dataset](https://dataset.readthedocs.org/en/latest/) - A wrapper around SQLAlchemy that simplifies database operations (including upserting).
* [ijson](https://github.com/isagalaev/ijson) - Allows processing JSON iteratively (as a stream) without loading the whole file into memory at once.
* [Joblib](https://pythonhosted.org/joblib/) - "a set of tools to provide lightweight pipelining in Python."
* [lxml](https://github.com/lxml/lxml) - Parses XML using C libraries libxml2 and libxslt, so it's very fast. Also supports a "recover" mode that will try its best to use invalid xml or discard it. Great for large XML files and advanced functionality (like using xpaths). IBM also has a great article on high-performance parsing with lxml here: http://www.ibm.com/developerworks/library/x-hiperfparse/
* [MrJob](https://pythonhosted.org/mrjob/) - "lets you write MapReduce jobs in Python 2.6+ and run them on several platforms. The easiest route to writing Python programs that run on Hadoop."
* [Odo](https://github.com/blaze/odo) - Moves data across containers (SQL, CSV, MongoDB, Pandas, etc). Claims to be the easiest and fastest way to load a CSV into your database.
* [Pandas](http://pandas.pydata.org/) - Implements dataframes in Python for easier data processing and includes a number of tools that make it easier to extract data from multiple file formats.
* [parse](https://github.com/r1chardj0n3s/parse) - The opposite of Python's format(). Easier to use than regex, but more limited.
* [PETL](https://github.com/alimanfoo/petl) - "a general purpose Python package for extracting, transforming and loading tables of data." Slower than Pandas and not as good for larger amounts of data, but simpler.
* [PyQuery](https://pythonhosted.org/pyquery/) - Extracts data from web pages with a jquery-like syntax.
* [Retrying](https://github.com/rholder/retrying) - Allows you to add a decorator to any function/method to retry on an exception.
* [Requests-HTML](https://github.com/kennethreitz/requests-html) - Combines PyQuery, Requests, parse, and other libraries for a pleasant and intuitive web scraping experience.
* [riko](https://github.com/nerevu/riko) - A python stream processing engine modeled after Yahoo! Pipes.
* [Ruffus](https://pypi.python.org/pypi/ruffus) - "The Ruffus module is a lightweight way to add support for running computational pipelines."
* [SQLAlchemy](http://www.sqlalchemy.org/) - "the Python SQL toolkit and Object Relational Mapper that gives application developers the full power and flexibility of SQL."
* [Toolz](https://toolz.readthedocs.org/en/latest/) - "A functional standard library for python." Includes a `pipe` function that allows you to pipe a value through a sequence of functions. There's also a cython implementation here: https://github.com/pytoolz/cytoolz
* [xmltodict](https://github.com/martinblech/xmltodict) - Makes working with XML as easy as working with JSON. Also allows streaming so you don't run out of memory on large XML files. Great for simple operations on small XML files.

### Talks/Articles
* https://vimeo.com/73628111
* http://www.parsely.com/misc/slides/streamparse/notes/

## Ruby
* [Kiba](https://github.com/thbar/kiba) - "Data processing & ETL framework for Ruby"
* [nokogiri](https://github.com/sparklemotion/nokogiri) - an excellent XML parser that "just works"
* [Square ETL](https://github.com/square/etl)
* [Sequel](https://github.com/jeremyevans/sequel) - "The Database Toolkit for Ruby"
* [Embulk](https://github.com/embulk/embulk) - "a parallel bulk data loader that helps data transfer between various storages, databases, NoSQL and cloud services."

## Go
* [Crunch](https://github.com/jondot/crunch) - "A fast to develop, fast to run, Go based toolkit for ETL and feature extraction on Hadoop."
* [Pachyderm](https://github.com/pachyderm/pachyderm) - A system for running processing pipeline jobs in containers and version controlling all data using a commit-based distributed filesystem.

## Javascript
* [Datapumps](https://github.com/agmen-hu/node-datapumps) - "Use pumps to import, export, transform or transfer data."
* [NoFlo](http://noflojs.org/) - "a JavaScript implementation of Flow-Based Programming"

## Talks/Articles
* https://medium.com/@samson_hu/building-analytics-at-500px-92e9a7005c83
* http://www.slideshare.net/g33ktalk/data-pipeline-acial-lyceum20140624
* http://chairnerd.seatgeek.com/building-out-the-seatgeek-data-pipeline/
* http://www.garynissen.com/etl-hand-code-or-tool/
* http://www.slideshare.net/CasertaConcepts/big-data-warehousing-meetup-bigetl-trad-tool-vs-pig-vs-hive-vs-python-what-to-use-when-slide-set-2
* https://deepfriedcode.com/books/darps/index.html
* http://blog.cloudera.com/wp-content/uploads/2010/01/IntroToPig.pdf
* http://tech.adroll.com/blog/data/2015/10/15/luigi.html?adrolldev

## Cloud Services
* [Alteryx](http://www.alteryx.com/) - Cloud ETL tool with an interface similar to GUI ETL tools.
* [AWS Data Pipeline](https://aws.amazon.com/datapipeline/) - "a web service that helps you reliably process and move data between different AWS compute and storage services, as well as on-premise data sources, at specified intervals."
* [AWS Glue](https://aws.amazon.com/glue/) - AWS Glue generates the code (using Python and Spark) to execute your data transformations and data loading processes.
* [Amazon Simple Workflow Service (SWF)](https://aws.amazon.com/swf/) - "helps developers build, run, and scale background jobs that have parallel or sequential steps. You can think of Amazon SWF as a fully-managed state tracker and task coordinator in the Cloud."
* [AWS Batch](https://aws.amazon.com/batch/) - Allows executing jobs as containerized applications running on Amazon ECS. Also includes features for dynamically bidding for Spot Instances, integration with existing workflow engines, scheduling, monitoring, dependency modeling, and dynamic scaling/provisioning based on amount of work.
* [Google Dataflow](https://cloud.google.com/dataflow/what-is-google-cloud-dataflow) - "Google Cloud Dataflow provides a simple, powerful model for building both batch and streaming parallel data processing pipelines."

## Big Data (Hadoop Stack)
* [Pig](https://pig.apache.org/) - "a platform for analyzing large data sets that consists of a high-level language for expressing data analysis programs, coupled with infrastructure for evaluating these programs."
* [Spark](https://spark.apache.org/docs/0.9.0/index.html) - "a fast and general-purpose cluster computing system. It provides high-level APIs in Scala, Java, and Python that make parallel jobs easy to write, and an optimized engine that supports general computation graphs. It also supports a rich set of higher-level tools including Shark (Hive on Spark), MLlib for machine learning, GraphX for graph processing, and Spark Streaming."

## ETL Tools (GUI)
*Warning*: If you're already familiar with a scripting language, GUI ETL tools are not a good replacement for a well structured application written with a scripting language. These tools lack flexibility and are a good example of the ["inner-platform effect"](https://en.wikipedia.org/wiki/Inner-platform_effect). With a large project, you will most likely run into instances where "the tool doesn't do that" and end up implementing something hacky with a script run by the GUI ETL tool. Also, the GUI can conceal complexity and the files these tools generate are impossible to code review. However, the GUI and out-of-the-box functionality can make some tasks simpler, especially for people not comfortable with writing code.
* [Apache NiFi](https://nifi.apache.org/) - "a rich, web-based interface for designing, controlling, and monitoring a dataflow."
* [Informatica PowerCenter](https://www.informatica.com/products/data-integration/powercenter.html) - "a toolset for establishing and maintaining enterprise-wide data warehouses. It has a customer base of over 5,000 companies."
* [Microsoft SSIS](https://technet.microsoft.com/en-us/library/ms141026.aspx) - "a component of the Microsoft SQL Server database software that can be used to perform a broad range of data migration tasks."
* [Pentaho Kettle](http://community.pentaho.com/projects/data-integration/) - The most popular open-source graphical ETL tool.
* [Talend](https://www.talend.com/products/talend-open-studio) - "an open source application for data integration job design with a graphical development environment"
