..
    SPDX-FileCopyrightText: Copyright (c) 2024-2025 NVIDIA CORPORATION & AFFILIATES. All rights reserved.
    SPDX-License-Identifier: Apache-2.0

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

KV Block Manager: Intelligent Memory Management for LLMs
=====================================================

What is the KV Block Manager?
--------------------------

The KV Block Manager (KVBM) is Dynamo's intelligent memory management system that optimizes how LLMs store and access their key-value cache data. It's designed to:

* Maximize performance across different hardware setups
* Scale efficiently in distributed environments
* Support multiple LLM frameworks seamlessly

Key Benefits
----------

1. **Unified Memory Management**
   * Single API for all memory types (GPU, CPU, SSD, remote)
   * Seamless data movement between memory tiers
   * Optimized for your specific hardware setup

2. **Intelligent Caching**
   * Smart block allocation and deallocation
   * Efficient cache reuse across requests
   * Automatic memory tier optimization

3. **Framework Compatibility**
   * Works with vLLM, SGLang, and TRT-LLM
   * Consistent API across frameworks
   * Easy integration with existing systems

4. **Distributed Operation**
   * Efficient remote memory access
   * Automatic block sharing between nodes
   * Built-in RDMA support via NIXL

Technical Features
---------------

1. **Memory Hierarchy Support**
   * GPU Memory (HBM)
   * CPU Memory (RAM)
   * Local Storage (NVMe)
   * Remote Storage (Object/Cloud)

2. **Block Management**
   * Lifecycle tracking (allocate → register → match)
   * Event-based state transitions
   * Customizable storage subscriptions

3. **NIXL Integration**
   * High-speed memory exchange
   * Remote block access
   * Dynamic memory sharing

Getting Started
-------------

The KVBM documentation is organized into the following sections:

.. toctree::
   :hidden:

   Why KVBM? <kvbm_motivation.md>
   Architecture Overview <kvbm_architecture.md>
   Component Details <kvbm_components.md>
   Further Reading <kvbm_reading>