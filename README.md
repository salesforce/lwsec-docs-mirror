# lwsec-docs-mirror

Read-only external facing mirror for documentation from the internal Lightning Web Security (LWSec) monorepo. Primarily to expose ESLint and distortion related docs.

## Usage

To ensure you are viewing the documentation that matches the version of LWSec you are using, match the Github tag of this project with the LWSec release version. The Github tags can be viewed [here](https://github.com/salesforce/lwsec-docs-mirror/tags).

For example, if you are using `@locker/eslint-config-locker@0.18.24` in your project, view the repo at the [`v0.18.24` tag](https://github.com/salesforce/lwsec-docs-mirror/tree/v0.18.24).


## Contributing

To fix any documentation related issues, file an issue in this repository and the fix will be made to the internal repository this one mirrors. 

> :warning: Do not directly modify any contents under the `packages/` directory. These are updated with automated scripts and your changes will likely be overridden.
