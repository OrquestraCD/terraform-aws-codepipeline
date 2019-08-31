[![Slalom][logo]](https://slalom.com)

# terraform-aws-codepipeline [![Build Status](https://travis-ci.com/JamesWoolfenden/terraform-aws-codepipeline.svg?branch=master)](https://travis-ci.com/JamesWoolfenden/terraform-aws-codepipeline) [![Latest Release](https://img.shields.io/github/release/JamesWoolfenden/terraform-aws-codepipeline.svg)](https://github.com/JamesWoolfenden/terraform-aws-codepipeline/releases/latest)

Terraform module to provision an AWS [`codepipeline`](https://aws.amazon.com/codepipeline/) CI/CD system.
The module also creates the build itself and and the example sets a deployment up for a fargate project.

---

It's 100% Open Source and licensed under the [APACHE2](LICENSE).

## Usage

Include this repository as a module in your existing terraform code:

```hcl
module "codepipeline" {
  source                 = "github.com/jameswoolfenden/terraform-aws-codepipeline"
  version                = "0.1.1"
  artifact_store         = var.artifact_store
  build_timeout          = var.build_timeout
  common_tags            = var.common_tags
  description            = var.description
  env                    = var.env
  environment            = var.environment
  name                   = var.name
  projectroot            = var.projectroot
  stage                  = var.stage
  type                   = var.type
}
```

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| artifact\_store | The Artifact store | map | n/a | yes |
| build\_timeout | Timeout set for the build to run | string | n/a | yes |
| common\_tags | Implements the common tags scheme | map | n/a | yes |
| description | Description of build project | string | n/a | yes |
| env |  | string | n/a | yes |
| environment |  | list | n/a | yes |
| name |  | string | n/a | yes |
| policypath |  | string | `""` | no |
| projectroot | The root path element for SSM variables | string | n/a | yes |
| role\_arn | Optionally supply an existing role | string | `""` | no |
| stages | This list describes each stage of the build | list | n/a | yes |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

## Related Projects

Check out these related projects.

- [terraform-aws-codebuild](https://github.com/jameswoolfenden/terraform-aws-codebuild) - Making a Build pipeline

## Help

**Got a question?**

File a GitHub [issue](https://github.com/jameswoolfenden/terraform-aws-codepipeline/issues).

## Contributing

### Bug Reports & Feature Requests

Please use the [issue tracker](https://github.com/jameswoolfenden/terraform-aws-codepipeline/issues) to report any bugs or file feature requests.

## Copyrights

Copyright © 2019-2019 [Slalom, LLC](https://slalom.com)

## License

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

See [LICENSE](LICENSE) for full details.

Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

<https://www.apache.org/licenses/LICENSE-2.0>

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.

### Contributors

  [![James Woolfenden][jameswoolfenden_avatar]][jameswoolfenden_homepage]<br/>[James Woolfenden][jameswoolfenden_homepage]

  [jameswoolfenden_homepage]: https://github.com/jameswoolfenden
  [jameswoolfenden_avatar]: https://github.com/jameswoolfenden.png?size=150

[logo]: https://gist.githubusercontent.com/JamesWoolfenden/5c457434351e9fe732ca22b78fdd7d5e/raw/15933294ae2b00f5dba6557d2be88f4b4da21201/slalom-logo.png
[website]: https://slalom.com
[github]: https://github.com/jameswoolfenden
[linkedin]: https://www.linkedin.com/company/slalom-consulting/
[twitter]: https://twitter.com/Slalom

[share_twitter]: https://twitter.com/intent/tweet/?text=terraform-aws-codepipeline&url=https://github.com/jameswoolfenden/terraform-aws-codepipeline
[share_linkedin]: https://www.linkedin.com/shareArticle?mini=true&title=terraform-aws-codepipeline&url=https://github.com/jameswoolfenden/terraform-aws-codepipeline
[share_reddit]: https://reddit.com/submit/?url=https://github.com/jameswoolfenden/terraform-aws-codepipeline
[share_facebook]: https://facebook.com/sharer/sharer.php?u=https://github.com/jameswoolfenden/terraform-aws-codepipeline
[share_email]: mailto:?subject=terraform-aws-codepipeline&body=https://github.com/jameswoolfenden/terraform-aws-codepipeline
