# CosmWasm Tracing - README

## Introduction

CosmWasm Tracing enhances blockchain development by simplifying error detection and transaction analysis within the Cosmos SDK and CosmWasm framework. Distinguished by its real-time monitoring capabilities and comprehensive analytics, it stands as an indispensable tool for developers looking to diagnose issues swiftly, comprehend transaction flows with greater depth, and optimize smart contracts with unprecedented efficiency.

**Supported Chains**

1. Kujira
2. Neutron
3. Terra

*Note: Supported chains are part of the CosmWasm Subscription program*

## Problem Statement

Developers working with Cosmos SDK-based and CosmWasm-enabled networks encounter significant hurdles in tracing and debugging, particularly when navigating the complexities of smart contract interactions. The limitations of existing tools, which offer only surface-level insights without the detail needed for in-depth analysis, compound these challenges. CosmWasm Tracing is designed to fill this critical void, enhancing the observability within these ecosystems by providing a comprehensive toolset for detailed examination and diagnostics, ensuring developers can efficiently pinpoint and resolve issues.

## Solution Overview

CosmWasm Tracing is built on three key components: an instrumented full node for collecting detailed logs, a database that archives this data, and a user interface (UI) designed to make data discovery intuitive. Together, these elements form a cohesive system that enhances the debugging and analysis capabilities of developers within the Cosmos SDK and CosmWasm ecosystems. This structure ensures that every level of transaction and contract interaction is observable, analyzable, and actionable, streamlining the development process and elevating the efficiency of blockchain network optimization.

### **Collected Data**

CosmWasm Tracing collects detailed logs for various operations, including but not limited to:

- **`all`**: General data encompassing all operations.
- **`abci_*`**: Begin and end block operations.
- **`ante_handler`**: Initial transaction handling.
- **`messenger`**: Message routing information.
- **`module_*`**: Module lifecycle events.
- **`new_msg_router`**: Message routing for new messages.
- **`service`**: Service calls within the ecosystem.
- **`wasm*`**: Operations specific to WebAssembly smart contracts.

Each data type provides a window into the functioning of smart contracts and transactions, allowing for thorough analysis and debugging.

### Searchable Tags

To enhance search capabilities and debugging accuracy, CosmWasm Tracing utilizes searchable tags, enabling developers to filter transactions based on specific criteria:

- **Errored Transactions** (**`errored=true/false`**): Use this tag to filter transactions by their error status, allowing for quick identification of issues.
- **Transaction Identification** (**`tx`**): This tag enables searching for transactions using their unique hash, facilitating detailed transaction analysis.
- **Contract-Originated Transactions** (**`sender_contract`**): Apply this tag to find transactions initiated by a particular contract, aiding in contract behavior analysis.

These searchable tags, alongside information on operations like original messages, gas usage, events, and error logs, equip developers with the tools needed for detailed and efficient troubleshooting within the Cosmos SDK and CosmWasm-enabled networks.

## Features

1. **Enhanced Log Collection**: *Improved instrumentation of the full node for more comprehensive log data, capturing finer details of smart contract interactions.*
2. **Advanced Data Storage Solutions**: *Upgrades to the database for more efficient storage and retrieval, ensuring faster access to historical transaction data.*
3. **Intuitive UI for Data Discovery**: *Revamped user interface designed for greater usability, enabling developers to navigate and discover data with ease, streamlining the debugging process.*

## UI Navigation

Navigating the CosmWasm Tracing UI is designed to be intuitive, allowing users to conduct focused and effective searches through a variety of commands. Here are some tailored examples to guide you through the process:

- **To Locate a Specific Transaction**:
    - Input **`tx=NNN`** in the search field, replacing **`NNN`** with the actual transaction hash you're seeking. This directs you to a detailed view of that transaction.
- **For Identifying Transactions with Errors**:
    - Use the command **`errored=true`** to filter transactions that have encountered errors. This efficient approach helps in pinpointing issues needing resolution.
- **To Find Transactions Initiated by a Specific Contract**:
    - Typing **`sender_contract=NNN`**, where **`NNN`** is the contract's identifier, filters the transactions to those initiated by the specified contract. This is invaluable for tracking contract activity.
- **Combining Search Parameters**:
    - For more complex searches, combine different parameters with a space, which acts as an AND operator. For example, **`errored=true sender_contract=NNN`** will show transactions that are both errored and initiated by the specified contract.

## Vision for Improvement

**Elevating Developer Experience and Flexibility:**

- **UI Improvements**: To make the tool more intuitive and easier to navigate.
- **Local Deployment**: To allow flexible use in various development environments.

## Contact

For more information, support, or questions, please feel free to contact us through our GitHub repository or connect with us on [X](https://twitter.com/confio_tech). Our team is dedicated to providing assistance and answering any queries related to CosmWasm Tracing.
