# ONNX E2E Extensions

## Introduction

ONNX has a rich set of [Operators](https://onnx.ai/onnx/operators/index.html). With this set of operators,
ONNX can describe most ML models. However, when we see any trained model, it doesn not include pre/post processing.
ONNX & ONNXRuntime provide ways to add a new or a custom operator which can be leveraged to add pre/post processing
subgraphs to the ML model.

- [Add a new OP](https://onnx.ai/onnx/repo-docs/AddNewOp.html#adding-new-operator-or-function-to-onnx)
- [Add a Custom OP](https://onnxruntime.ai/docs/extensions/add-op.html)

ONNX E2E Extensions provides a way to create and add pre/post processing operators to the trained model which
enables running end-to-end ML inference on different Execution Providers.

- Create Pre/Post Ops as Functions
  - If the operator can be expressed in terms of existing ONNX operators

- Create Pre/Post Ops as Custom OP
  - If the operator cannot be expressed in terms of existing ONNX operators

The current pre/post processing OPs available can be found in [vitis_customop](./vitis_customop)

## Setup

Please ensure you have installed Ryzen-AI Software by following the official installation page

https://ryzenai.docs.amd.com/en/latest/inst.html

Ensure driver and [Vitis-AI Execution Provider](https://ryzenai.docs.amd.com/en/latest/manual_installation.html#install-vitis-ai-execution-provider) is installed properly

### Create conda environment


```powershell
conda env create --file setup/env.yml
```

- Activate conda environment

```powershell
conda activate onnx-vai
```

## Examples

[README](examples/README.md) for the steps to try out the examples.