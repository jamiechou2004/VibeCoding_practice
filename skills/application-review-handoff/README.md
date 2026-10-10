# Application Review Handoff

A Codex workflow skill for keeping multi-role job applications reviewable: who authorized what, which files were used, what submission evidence exists, and what still needs attention.

这是一个申请审核与交接工作流 Skill，聚焦多家公司申请之间容易混淆的授权、附件版本、提交证据和表格同步状态。

## Why this exists

A new résumé upload does not confirm the portfolio version. A failed network response does not prove the application failed. A successful submission does not mean the tracking sheet was updated. The skill keeps these states separate so a person or another agent can resume work with the right evidence.

## Name and invocation / 名称与调用

- 中文显示名称：**申请审核与交接**
- 唯一技能标识：`application-review-handoff`
- 精确调用：`$application-review-handoff`
- 自然语言示例：请用“申请审核与交接”整理这些岗位的材料版本、审核状态和下一步。需要明确指定技能时优先使用上面的精确调用。

```text
使用 $application-review-handoff 整理当前申请的逐岗审核与交接记录，
列明授权、材料版本、提交证据、未同步事项和下一步。
本次只准备审核包，不提交申请。
```

The UI display name and default invocation prompt are defined in `agents/openai.yaml`.

## Try it

Copy this directory to your Codex skills directory as `application-review-handoff`. In a task that can access it, ask:

> 使用 $application-review-handoff，依据 examples/input.md 中的虚构记录生成逐岗审核与交接表。仅进行文件演练，不访问网站、不提交、不更新在线表。

Read [the sample input](examples/input.md), then compare the result with [the demo output](examples/output.md). All sample companies, role IDs and file versions are fictional.

## What the skill produces

- A separate record for each role, with the scope of user authorization.
- Attachment versions and unresolved review items.
- Submission evidence, archive status and tracking-sheet status recorded separately.
- Concrete next actions and owners.

## Design decisions

**Per-role permission:** approval for one application does not extend to another.

**Evidence-based state:** a click is an attempted action; a receipt or application-center record is evidence of submission.

**Recoverable partial completion:** tracking failures stay visible without erasing a confirmed submission or triggering a duplicate application.

**Complementary scope:** `application-helper`, when available, handles fit assessment and material preparation. This skill handles final review and cross-task handoff. It can also use already prepared materials without that companion skill.

## Validation and limits

See [validation results](validation/RESULTS.md). The package includes format validation and an isolated synthetic scenario exercise. It has not been end-to-end tested against live recruiting sites or Google Sheets. It does not contain a browser automation implementation or a Google Sheets connector; those capabilities must be provided by the host environment.

This project makes no claim about interview rates, hiring outcomes or time saved. Private application evidence is excluded from the public package.
