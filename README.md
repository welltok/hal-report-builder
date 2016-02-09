# ReportBuilder
Ruby gem to merge Cucumber JSON reports and build single HTML Test Report

## Installation

```bash
gem install report_builder
```

## Information

* Ruby gem [![Gem Version](https://badge.fury.io/rb/report_builder.svg)](https://badge.fury.io/rb/report_builder)
* RDoc documentation [available on RubyDoc.info](http://www.rubydoc.info/gems/report_builder)
* Source code [available on GitHub](http://github.com/rajatthareja/ReportBuilder)
* Sample report [available here](http://www.rajatthareja.com/reportbuilder/sample.html)

## Usage

**Note:** Works with cucumber(>= 2.1.0) test results in JSON format.

### Code Examples:

```ruby
    require 'report_builder'

   # 1
    ReportBuilder.build_report('path/of/json/files/dir')
    ReportBuilder.build_report('path/of/json/files/dir','my_test_report_name','json_html')
    ReportBuilder.build_report('path/of/json/files/dir','my_test_report_name','json')
    ReportBuilder.build_report('path/of/json/files/dir','my_test_report_name','html')

   # 2
    ReportBuilder.build_report('path/of/json/cucumber.json', 'my_test_report')

   # 3
    ReportBuilder.build_report([
            'path/of/json/cucumber1.json',
            'path/of/json/cucumber2.json',
            'path/of/json/files/dir/'
            ])

   # 4
    ReportBuilder.build_report()

   # 5
    ReportBuilder::COLOR[:passed] = '#ffffff'
    ReportBuilder.build_report()
```

### Command Example:

```bash
     report_builder 'path/of/json/files/dir' 'report_file'
```

### Rake Example:

```ruby
   # Add in Rakefile
      require 'report_builder'
      load 'report_builder.rake'
   # Then run rake task report_builder
```

```bash
   rake report_builder ['path/of/json/files/dir','report_file','json_html']
```

## Contributing

We're open to any contribution. It has to be tested properly though.

## Maintainer

[Rajat Thareja](http://www.rajatthareja.com)

## License

Copyright (c) 2016 [MIT LICENSE](LICENSE)