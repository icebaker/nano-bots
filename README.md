# Nano Bots

Repository for Nano Bots' Cartridges.

You can explore all Cartridges in this repository at https://nbots.io.

- [Using](#using)
  - [Implementations](#implementations)
- [Creating](#creating)
- [Sharing](#sharing)
- [Licensing](#licensing)

## Using

You can use any Cartridge from this repository by downloading the YAML file or copying and pasting its contents into a local YAML file. To run it, you will need an [implementation](#implementations).

### Implementations

To use Cartridges, you need an implementation to run them. Popular ones include:

- [Nano Bots CLI (Ruby)](https://github.com/icebaker/ruby-nano-bots)
- [Clinic (Live Editor)](https://clinic.nbots.io)
- [Nano Bots API](https://github.com/icebaker/nano-bots-api)
  - [Public API](https://api.nbots.io)
- [Nano Bots for Sublime Text](https://github.com/icebaker/sublime-nano-bots)
- [Nano Bots for Visual Studio Code](https://github.com/icebaker/vscode-nano-bots)

## Creating

To start creating your Cartridges, check the [oficial documentation](https://spec.nbots.io/#/README).

You can use an [implementation](#implementations) to run the Cartridge that you are creating, or the [Clinic (Live Editor)](https://clinic.nbots.io).

Successful Nano Bot creation usually comes from a solid background of the developer in [_Prompt Engineering_](https://en.wikipedia.org/wiki/Prompt_engineering). Here are some recommended content to learn about it:

- [Nano Bots Specification](https://spec.nbots.io/#/README)
- [Prompt Engineering Guide](https://www.promptingguide.ai)
- [ChatGPT Prompt Engineering for Developers](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/)

## Sharing

To share your Cartridges with the world, open a Pull Request in this repository. Inside the `/cartridges` path, create a new folder with the naming pattern `@your-nickname`. 

In the folder, create a `profile.yml` file with the following structure:
```yml
---
author:
  name: Ice Baker
  uri: icebaker
  github: https://github.com/icebaker
```

This folder is exclusively associated with your GitHub username, and its contents will only accept pull requests from your user. Therefore, make sure to provide accurate information.

Once you create your user folder, include a `/cartridges` folder within it, containing all your cartridges in the YAML format. You can organize your `/cartridges` folder as per your choice since we will perform a recursive search of YAML files within it, regardless of the directory structure.

To improve the display in the [Marketplace](https://nbots.io), you can include a `marketplace` section under `miscellaneous` in your Cartridge:

```yml
miscellaneous:
  marketplace:
    tags:
    - programming
    samples:
    - interface: eval
      input: Hi!
    - interface: repl
      input:
      - Hello!
      - How are you doing?
```

The `tags` will help with search, and should follow a [_Clean URL_](https://en.wikipedia.org/wiki/Clean_URL) pattern like `programming`, `personality`, `prompt-writing`, etc.

The `samples` section generates pre-built samples based on inputs. This is helpful in showcasing to users the capabilities of your Nano Bot. To ensure intellectual honesty, outputs cannot be specified as they will be automatically generated. Each input has the potential to generate up to five distinct outputs.

A recommended learning path is to check the current sources of Cartridges in this repository and their respective pages at http://nbots.io in order to infer what to expect.

## Licensing

The classification of _prompts_ for Large Language Models as code, art, or intellectual property, as well as their applicability to licensing, intellectual property rights, copyright, or patenting, remain subjects of ongoing and complex debate without a clear answer or definitive understanding at present.

When Nano Bots expand prompt writing into a more detailed scheme and add small pieces of code like [adapters](?id=adapters), the debate becomes even trickier and blurrier.

Due to the complexity of this debate, we recommend that authors publish their creations under licenses. This serves as a simple safeguard, ensuring that in the event these creations become subject to licensing considerations in the future, we have already established a licensing model that supports the authors' intention and can be adopted if necessary.

Here are some licenses that share common traits, such as enabling commercial exploration of the licensed works and the creation of derivative works without copyleft:

| License | SPDX | Commercial Usage | Derivative Work | No Attribution | No Copyleft |
|---------|:----:|:----------------:|:---------------:|:--------------:|:-----------:|
| [Creative Commons Zero v1.0 Universal](https://spdx.org/licenses/CC0-1.0.html) | `CC0-1.0` | ✅ | ✅ | ✅ | ✅ |
| [The Unlicense](https://spdx.org/licenses/Unlicense.html) | `Unlicense` | ✅ | ✅ | ✅ | ✅ |
| [Creative Commons Attribution 4.0 International](https://spdx.org/licenses/CC-BY-4.0.html) | `CC-BY-4.0` | ✅ | ✅ | ❌ | ✅ |
| [MIT License](https://spdx.org/licenses/MIT.html) | `MIT` | ✅ | ✅ | ❌ | ✅ |
| [Apache License 2.0](https://spdx.org/licenses/Apache-2.0.html) | `Apache-2.0` | ✅ | ✅ | ❌ | ✅ |
| [BSD 2-Clause "Simplified" License](https://spdx.org/licenses/BSD-2-Clause.html) | `BSD-2-Clause` | ✅ | ✅ | ❌ | ✅ |
| [BSD 3-Clause "New" or "Revised" License](https://spdx.org/licenses/BSD-3-Clause.html) | `BSD-3-Clause` | ✅ | ✅ | ❌ | ✅ |
| [ISC License](https://spdx.org/licenses/ISC.html) | `ISC` | ✅ | ✅ | ❌ | ✅ |
| [zlib License](https://spdx.org/licenses/Zlib.html) | `Zlib` | ✅ | ✅ | ❌ | ✅ |

In doubt, in the spirit of openness, sharing, and open source, we recommend the license [CC0-1.0](https://creativecommons.org/publicdomain/zero/1.0/). However, any [SPDX-known license](https://spdx.org/licenses/) may be chosen.

Please note that we are uncertain if this approach is practical or enforceable, so it should not be considered a guarantee of licensing but rather a statement of your intention.
