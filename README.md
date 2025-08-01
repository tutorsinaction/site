<a id="readme-top"></a>

<!--
*** Use markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

<!-- PROJECT SHIELDS -->

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![GNU General Public License v3.0][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/tutorsinaction/site">
    <img src="docs/images/logo.png" alt="Logo" width="80" height="80">
  </a>

<h3 align="center">Tutors In Action Malaysia Official Website</h3>

  <p align="center">
    We're an independent, student-led project aiming to assist SPM students who lack access to affordable tuition.
    <br />
    <a href="https://github.com/tutorsinaction/site"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://site-production.tutors-in-action-malaysia.workers.dev/">View Website</a>
    &middot;
    <a href="https://github.com/tutorsinaction/site/issues/new?labels=bug&template=bug_report.md">Report Bug</a>
    &middot;
    <a href="https://github.com/tutorsinaction/site/issues/new?labels=enhancement&template=feature_request.md">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li>
      <a href="#development">Development</a>
      <ul>
        <li><a href="#workflow">Workflow</a></li>
        <li><a href="#project-structure">Project Structure</a></li>
        <li><a href="#commands">Commands</a></li>
      </ul>
    </li>
    <li><a href="#deployment">Deployment</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->

## About The Project

[![Tutors In Action Malaysia][product-screenshot]][product-url]

TIA is a student-led organisation registered under Jabatan Pendaftaran Pertubuhan Malaysia (JPPM). Ever since our establishment in March 2020 to combat pandemic-related issues such as disrupted classes, TIA has been upholding SDG 4 – ‘Quality Education’ with the utmost earnestness and integrity. Our organisation is dedicated to providing free assistance to Form 5 students in their SPM preparation, addressing the challenges arising from disrupted classes and limited access to affordable tuition options. In addition to our core mission, we have and are currently venturing into other educational-themed side projects, expanding our impact and outreach.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

- [![Astro][astro-shield]][astro-url]
- [![React][react-shield]][react-url]
- [![Tailwind CSS][tailwind-shield]][tailwind-url]
- [![Cloudflare][cloudflare-shield]][cloudflare-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->

## Getting Started

### Prerequisites

- Node.js (v18 or later)
- pnpm

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/tutorsinaction/site.git
   ```
2. Install PNPM packages
   ```sh
   pnpm install
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->

## Development

### Workflow

**Contributor**

1. Create a new branch from `development`

```sh
git checkout development
git pull origin development
git checkout -b feature/landing-page

```

2. Make changes and test locally
3. Commit and push changes to `origin/feature/landing-page`
4. Create a pull request `development` <- `feature/landing-page`

**Maintainer**

1. Review, approve, merge, and test `development`
2. Create a pull request `staging` <- `development`
3. Review, approve, merge, and test `staging`
4. Create pull request `main` <- `staging`
5. Review, approve, merge, and test `main`

### Project Structure

```sh
docs/                 # Documentation assets
public/               # Static assets
src/
├── components/       # Reusable components
├── content/          # Markdown content collections
├── layouts/          # Page and section templates
├── pages/            # File-based routing
├── styles/           # Tailwind config and styles
├── consts.ts         # Shared constants
├── content.config.ts # Markdown content schema

```

`src/pages/`  
Astro converts files in the directory to accessible routes. e.g. `src/pages/about.astro` maps to `/about`. Refer to [Astro Pages](https://docs.astro.build/en/basics/astro-pages/) for more details.

`src/components/`  
Contains shared components written in Astro or React for reusability and maintainability. Refer to [Astro Components](https://docs.astro.build/en/basics/astro-components/) for more details.

`src/content/`  
Contains content collections written in Markdown or MDX e.g. blogs, reports. Use `getCollection()` to query content. Refer to [Astro Content Collections](https://docs.astro.build/en/guides/content-collections/) for more details.

`public/`  
Contains static files that do not require any processing e.g. images, fonts. CSS or JavaScript should live in `src/` directory to be bundled and optimized in final build.

`docs/`  
Contains documentation resources excluded from final build.

`consts.ts`  
Defines shared constants e.g site title, site description.

`content.config.ts`  
Defines typing for content collections to enable schema validation and editor autocompletion. Refer to [Astro Content Collections](https://docs.astro.build/en/guides/content-collections/#the-collection-config-file) for more details.

### Commands

All commands are run from the root of the project, from a terminal:

| Command                | Action                                           |
| :--------------------- | :----------------------------------------------- |
| `pnpm install`         | Installs dependencies                            |
| `pnpm dev`             | Starts local dev server at `localhost:4321`      |
| `pnpm build`           | Build your production site to `./dist/`          |
| `pnpm preview`         | Preview your build locally, before deploying     |
| `pnpm astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `pnpm astro -- --help` | Get help using the Astro CLI                     |

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- DEPLOYMENT -->

## Deployment

The project is deployed using Cloudflare Workers CI/CD pipeline and configured using `wrangler`.

| Branch        | Environment | Purpose             |
| ------------- | ----------- | ------------------- |
| `development` | Development | Feature testing     |
| `staging`     | Staging     | Integration testing |
| `main`        | Production  | Stable release      |

Each environment is linked to a separate Cloudflare Worker, and triggered automatically upon merging into the corresponding Git branch.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ROADMAP -->

## Roadmap

- [ ] Home
- [ ] Events
  - [ ] Listing
  - [ ] Detail
- [ ] Resources
  - [ ] Materials
  - [ ] Reports
- [ ] About
- [ ] Contact
- [ ] Donate

See the [open issues](https://github.com/tutorsinaction/site/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTRIBUTING -->

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/amazing-feature`)
3. Commit your Changes (`git commit -m 'feat: add some amazing feature'`)
4. Push to the Branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Top contributors:

<a href="https://github.com/tutorsinaction/site/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=tutorsinaction/site" alt="contrib.rocks image" />
</a>

<!-- LICENSE -->

## License

Distributed under the GNU General Public License v3.0. See [LICENSE.txt][license-url] for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->

## Contact

Tutors In Action Malaysia - [LinkedIn][linkedin-url] - tutors.in.action.malaysia@gmail.com

Project Link: [https://github.com/tutorsinaction/site](https://github.com/tutorsinaction/site)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->

## Acknowledgments

- [Astro](https://astro.build/)
- [MDX](https://mdxjs.com/)
- [Cloudflare Workers](https://workers.cloudflare.com/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[contributors-shield]: https://img.shields.io/github/contributors/tutorsinaction/site.svg?style=for-the-badge
[contributors-url]: https://github.com/tutorsinaction/site/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/tutorsinaction/site.svg?style=for-the-badge
[forks-url]: https://github.com/tutorsinaction/site/network/members
[stars-shield]: https://img.shields.io/github/stars/tutorsinaction/site.svg?style=for-the-badge
[stars-url]: https://github.com/tutorsinaction/site/stargazers
[issues-shield]: https://img.shields.io/github/issues/tutorsinaction/site.svg?style=for-the-badge
[issues-url]: https://github.com/tutorsinaction/site/issues
[license-shield]: https://img.shields.io/github/license/tutorsinaction/site.svg?style=for-the-badge
[license-url]: https://github.com/tutorsinaction/site/blob/main/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/company/tutors-in-action-malaysia/
[product-screenshot]: docs/images/screenshot.png
[product-url]: https://site-production.tutors-in-action-malaysia.workers.dev/
[astro-shield]: https://img.shields.io/badge/Astro-BC52EE?style=for-the-badge&logo=astro&logoColor=white
[astro-url]: https://astro.build/
[react-shield]: https://img.shields.io/badge/React-58C4DC?style=for-the-badge&logo=react&logoColor=white
[react-url]: https://react.dev/
[tailwind-shield]: https://img.shields.io/badge/Tailwind_CSS-38BDF8?style=for-the-badge&logo=tailwind-css&logoColor=white
[tailwind-url]: https://tailwindcss.com/
[cloudflare-shield]: https://img.shields.io/badge/Cloudflare-FF6633?style=for-the-badge&logo=cloudflare&logoColor=white
[cloudflare-url]: https://workers.cloudflare.com/
