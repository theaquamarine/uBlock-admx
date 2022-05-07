# Group Policy Administrative Templates for uBlock Origin

Administrative Templates to make configuring uBlock Origin in Chrome, Edge, and Firefox on Windows easier.

## Usage

Add the contents of PolicyDefinitions to your Central Store or local PolicyDefinitions folder, then edit group policy as normal.

For details on the settings, see uBlock Origin's wiki.
- https://github.com/gorhill/uBlock/wiki/Deploying-uBlock-Origin
- https://github.com/gorhill/uBlock/wiki/Deploying-uBlock-Origin:-configuration

For more details on using the templates, see https://docs.microsoft.com/en-us/troubleshoot/windows-client/group-policy/create-and-manage-central-store

## Editing

Documentation on the admx/adml template file formats is available https://docs.microsoft.com/en-us/previous-versions/windows/desktop/policy/admx-schema and https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-gpreg/81d92810-a6d2-4301-a607-b3ba34dc2989

xsd schema definition files for validation are available
- here
  - BaseTypes.xsd https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-gpreg/81d92810-a6d2-4301-a607-b3ba34dc2989
  - PolicyDefinitionsFiles.xsd https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-gpreg/ddeb37b6-22ab-4936-adc4-b9d7fe1de6e6
  - PolicyDefinitions.xsd https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-gpreg/81a89003-5121-4216-b788-fde8daa71c78
- or here https://github.com/FSLogix/admxgen/tree/master/admxgen

VS Code can validate the files automatically by using [Red Hat's XML extension](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-xml) and adding the following to settings.json
```json
{"xml.fileAssociations":[{"pattern":"**.adml","systemId":"PolicyDefinitionFiles.xsd"},{"pattern":"**.admx","systemId":"PolicyDefinitionFiles.xsd"}]}
```
