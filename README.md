<div align="center">

# Who&When Pro

### Can LLMs Really Attribute Failures in AI Agents?

Jiale Liu<sup>1,2</sup>, Huajun Xi<sup>3</sup>, Shaokun Zhang<sup>1</sup>,
Yifan Zeng<sup>4</sup>, Tianwei Yue<sup>5</sup>, Chi Wang<sup>2</sup>,
Jian Kang<sup>3</sup>, Qingyun Wu<sup>1,2</sup>, Huazheng Wang<sup>2,4</sup>

<sup>1</sup>Penn State University &nbsp;&nbsp;
<sup>2</sup>AG2ai, Inc. &nbsp;&nbsp;
<sup>3</sup>Mohamed bin Zayed University of Artificial Intelligence &nbsp;&nbsp;
<sup>4</sup>Oregon State University &nbsp;&nbsp;
<sup>5</sup>Mathos AI

[Project page](https://whowhenpro.github.io/) · Paper (coming soon) · Dataset (coming soon)

![Code status](https://img.shields.io/badge/code-coming%20soon-lightgrey)
![Data status](https://img.shields.io/badge/data-coming%20soon-lightgrey)

</div>

## Overview

When an AI agent fails, diagnosing the failure requires answering two questions:
**when** did the decisive error occur, and **who** (which agent or component)
caused it? **Who&When Pro** is a large-scale benchmark for evaluating whether
LLMs can perform this failure attribution automatically.

The benchmark contains **12,326 failed trajectories** with gold annotations,
covering **26 source benchmarks**, **nine task families**, **18 error modes**,
and **three modalities**: text, image, and video.

## Abstract

As AI agents become more capable, their failures become subtler and harder to
diagnose. Effective diagnosis requires identifying both the earliest action
whose correction would have changed a failed trajectory into a successful one
(the *when*) and the agent or sub-component responsible for that action (the
*who*). We introduce **Who&When Pro**, a large-scale benchmark for automated
failure attribution in agentic systems. Our warm-start injection pipeline
replays a successful trajectory exactly up to a selected step, replaces a
single action with an error, and then returns control to the agent. Because all
preceding steps match the successful run, the injected action provides an exact
label for the first decisive error rather than a post-hoc estimate. Who&When Pro
contains 12,326 failed trajectories with gold annotations across 26 source
benchmarks, nine task families, 18 error modes, and text, image, and video
modalities. We evaluate frontier LLMs on identifying the responsible agent,
localizing the decisive step, and classifying the underlying error. Our results
show that failure attribution remains challenging, particularly for image and
video traces and for recognizing the root error type, highlighting substantial
room for progress toward agents that can reliably learn from their own
mistakes.

## Benchmark Tasks

Given a failed agent trajectory, a model is evaluated on:

- **Agent attribution:** identify the responsible agent or component.
- **Step localization:** identify the first decisive error step.
- **Error classification:** identify the underlying failure mode.
- **Joint attribution:** answer all three correctly for the same trajectory.

## How to Use

> [!IMPORTANT]
> The evaluation code and benchmark data are not public yet. Installation and
> runnable commands will be added with the first release.

Once released, the expected workflow will be:

1. Install the package and its dependencies.
2. Download the benchmark data and configure model credentials.
3. Run inference on one or more benchmark splits.
4. Evaluate predictions with the official attribution metrics.

The release will include commands for reproducing the reported experiments,
evaluating a custom model, and scoring existing prediction files. Until then,
please follow the [project page](https://whowhenpro.github.io/) for updates.

## Repository Status

- [ ] Evaluation code
- [ ] Benchmark data and download instructions
- [ ] Environment and dependency specification
- [ ] Reproduction scripts and model configurations
- [ ] Prediction format and custom-model documentation
- [ ] Paper and citation

## Citation

Citation information will be added when the paper is released.

## Contact

For questions or release notifications, please open a GitHub issue.
