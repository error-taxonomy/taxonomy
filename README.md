# Faceted Error Taxonomy

[![License: GNU](https://img.shields.io/badge/License-GNU-yellow.svg)]([https://opensource.org/licenses/MIT](https://opensource.org/license/gpl-3-0))
<!---
[![Contributors](https://img.shields.io/github/contributors/username/faceted-taxonomy-project)](https://github.com/username/faceted-taxonomy-project/graphs/contributors)
-->

Welcome to Faceted Error Taxonomy project! This project aims to build and maintain a faceted error taxonomy for errors in language use. It can be used to  create both fine- and coarse-grained error annotation schemes, depending on specific requirements.

Classification of errors in language use plays a crucial role in language learning \& teaching, error analysis studies, and language technology development.
However, there is no standard and inclusive error classification method agreed upon among different disciplines, which causes repetition of similar efforts and a barrier in front of a common understanding in the field.

This project is based on the article [Error Annotation: A Review and Faceted Taxonomy](https://github.com/error-taxonomy/) which brings a new and holistic perspective to error classifications and annotation schemes across different fields (i.e., learner corpora research, error analysis, grammar error correction, and machine translation), all serving the same purpose but employing different methods and approaches.

We hope that this project as being based on the principles of universality and diversity will address the emerging need for a common framework in error annotation.

# Taxonomy XML Structure Reference

This document serves as a guide to understanding the XML-based taxonomy structure in taxonomy.xml file. It outlines the primary elements, attributes, and their purpose within the XML schema.

## Table of Contents

1. [Overview](#overview)
2. [Taxonomy Structure](#taxonomy-structure)
3. [Key Attributes](#key-attributes)

---

## Overview

This taxonomy organizes different categories and subcategories to describe various linguistic features. It is structured hierarchically, where each facet may contain subfacets or values, and each value represents a distinct feature.

XML defines facets (high-level categories) and subfacets (subcategories within facets), each with unique identifiers and names.

## Taxonomy Structure

The structure consists of the following key elements:

### `<taxonomy>`
- **Attributes**:
  - `name`: A string representing the name of the taxonomy.
  - `version`: The version of the taxonomy (e.g., "1.0").

### `<facet>`
- Represents a high-level category in the taxonomy.
- **Attributes**:
  - `id`: A unique identifier for the facet (e.g., "ID", "MF", "UNI").
  - `name`: The human-readable name of the facet (e.g., "Identifier", "MorphologicalFeature").
  - `dependency` (optional): Describes whether the facet is dependent on an external system (e.g., "[UDv2](https://universaldependencies.org/v2/)", "[ISO639-3](https://iso639-3.sil.org/code_tables/639/data)").
  - `multiValued` (optional): Indicates if a facet can have multiple values (e.g., `true` or `false`).

### `<subfacet>`
- Subcategories within a facet.
- **Attributes**:
  - `id`: A unique identifier for the subfacet (e.g., "POS", "IF", "LF").
  - `name`: The human-readable name of the subfacet (e.g., "PartOfSpeech", "InflectionalFeature").
  - `dependency` (optional): Describes whether the subfacet is dependent on an external system (e.g., "UDv2").
  - `allValuesFromDependencyAccepted` (optional): If `true`, it indicates that all values from the dependent system are valid.

### `<value>`
- Represents a specific value or feature within a facet or subfacet.
- **Attributes**:
  - `id`: A unique identifier for the value (e.g., "ADJ", "ADV").
  - `name`: The human-readable name of the value (e.g., "adjective", "adverb").
  - `linkedFacet` (optional): Links this value to another facet, indicating a relationship between them.

### `<subfacets>`
- A container for subfacets within a facet.

## Key Attributes

- **id**: A short string used as a unique identifier for facets, subfacets, and values.
- **name**: The descriptive name of the facet, subfacet, or value.
- **dependency**: Describes any external system that this element is related to (e.g., "UDv2", "ISO639-3").
- **multiValued**: A Boolean attribute (e.g., `true` or `false`) indicating whether a facet can have multiple values.
- **linkedFacet**: Indicates a relationship with another facet.

## How to Contribute

We welcome contributions from everyone! Please read our [CONTRIBUTING.md](CONTRIBUTING.md) for details on how to get started. 

### Steps to Contribute:

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/YourFeature`).
3. Make your changes in the taxonomy.xml.
4. Commit your changes (`git commit -m 'Add YourFeature'`).
5. Push to your branch (`git push origin feature/YourFeature`).
6. Open a Pull Request.

## License

This project is licensed under the GNU License - see the [LICENSE](LICENSE) file for details.

## Contact

If you have any questions or suggestions, feel free to open an issue or reach out to us at [faceted-error-taxonomy@outlook.com].
