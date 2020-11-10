# test-results
Repository to persist test results for existing dotCMS projects.

Currently starting with the `core` repo to persit its test results.

## Directory Structure
Since this repo might be used to keep results from multiple dotCMS repos, branches/commits, test type and sometimes database type, we need to introduce a directory structure similar to this one:
```
projects
└──core
|  └──current
|  |  └──curl
|  |  |  └──postgres
|  |  |     └──reports
|  |  |        └──html
|  |  |           └──index.html
|  |  └──integration
|  |  |  └──mssql
|  |  |  |  └──reports
|  |  |  |     └──html
|  |  |  |        └──index.html
|  |  |  └──mysql
|  |  |  |  └──reports
|  |  |  |     └──html
|  |  |  |        └──index.html
|  |  |  └──oracle
|  |  |  |  └──reports
|  |  |  |     └──html
|  |  |  |        └──index.html
|  |  |  └──postgres
|  |  |     └──reports
|  |  |        └──html
|  |  |           └──index.html
|  |  └──unit
|  |     └──reports
|  |        └──html
|  |           └──index.html
|  └──<commit/sha>
|     └──curl
|     |  └──mysql
|     |  |  └──reports
|     |  |     └──html
|     |  |        └──index.html
|     └──integration
|     |  └──postgres
|     |     └──reports
|     |        └──html
|     |           └──index.html
|     └──unit
|        └──reports
|           └──html
|              └──index.html
|
|
└──core-web
   └──...
```
Similar to the tests running at **Travis**, it will create a folder for the current commit and clean up the branch folder (is it does not exists it creates it) and store the latest test results there.
