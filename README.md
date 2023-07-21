# Apple

> **NOTE**: This project is neither maintained nor endorsed by Apple.

This repository contains a [Vale-compatible](https://github.com/errata-ai/vale) implementation of the [*Apple Style Guide*](https://support.apple.com/guide/applestyleguide/welcome/web).

## Getting Started

To get started, add the package to your configuration file (as shown below) and then run `vale sync`.

```ini
StylesPath = styles
MinAlertLevel = suggestion

Packages = Google

[*]
BasedOnStyles = Vale, Google
```

## Repository Structure

<dl>
  <dt><a href="https://github.com/errata-ai/Google/tree/master/Google"><code>/Google</code></a></dt>
  <dd>The <a href="http://yaml.org/">YAML</a>-based rule implementations that make up our style.</dd>

  <dt><a href="https://github.com/errata-ai/Google/tree/master/fixtures"><code>/fixtures</code></a></dt>
  <dd>The individual unit tests. Each directory should be named after a rule found in <code>/Google</code> and include its own <code>.vale.ini</code> file that isolates its target rule.</dd>

  <dt><a href="https://github.com/errata-ai/Google/tree/master/features"><code>/features</code></a></dt>
  <dd>The <a href="https://docs.cucumber.io/cucumber/step-definitions/">Cucumber Step Definitions</a> we use to test our fixtures. Essentially, we use the <a href="https://github.com/cucumber/aruba">aruba</a> framework to test Vale's output after running it on each of our fixture directories.</dd>
</dl>
