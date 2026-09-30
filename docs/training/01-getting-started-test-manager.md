# Getting Started with Test Manager

## What is Test Manager?

**Test Manager** is a web application, part of UiPath Test Cloud, where you can **plan**, **run**, **manage**, and **analyze** testing of applications.

Test Cloud offers a strong automation and testing ecosystem for managing all your testing operations: from **automating tests**, to **distributing** them, **executing**, and **managing** — you can perform all of these things in the context of a customizable cloud organization.

## Why is Test Manager useful?

Testing involves a wide range of activities, from the **creation** and **execution** of manual and automated test cases to reporting, requirement and defect management, CI/CD integration, and others.

One of the biggest challenges is making testing an integral part of the development process. This requires linking software development assets (e.g. user stories, epics, requirements) to software testing assets (e.g. test cases, test results, test executions), as well as a solution to manage and synchronize all the data generated in both processes. Test Manager is the component serving these purposes.

## How does Test Manager work?

![Test Manager](../assets/images/Test%20Manager_Full.png)

## The typical testing flow with Test Manager

!!! note "Your Testing Journey"

    ### Planning & Design

    ✅ Requirements are created either in Test Manager (TM) or in an external tool and imported into TM.

    ✅ The tester defines, generates (using Autopilot), or imports test cases in TM, and optionally documents them with Task Capture.

    ### Automation

    ✅ The test developer reviews the documentation and automates the defined test cases (from the previous step) in Studio.

    ✅ The test developer links the test case (automation) from Studio to the test case (design) in TM.

    ✅ The test developer publishes automated test cases from Studio to Orchestrator.

    ### Execution & Reporting

    ✅ The test developer creates test sets in Test Manager.

    ✅ Test sets are executed — automated and/or manual — from Test Manager.

    ✅ Based on the test execution results, reports are generated. If needed, defects are generated (optional, and only if you link to an external ALM tool).

## Create a Project

A **test project** in Test Manager is the top-level container for all the artifacts that serve a common testing goal — requirements, test cases, test sets, and test executions. Every artifact you create gets an ID that starts with the project's **prefix** (for example, `SAP:1`, `SAP:2`), which makes it easy to trace work back to its project.

Keep in mind:

✅ Any user role can create a project, but only Administrators and Project Owners can edit or delete it.

✅ A new project is visible only to its creator and to Administrators until you grant other users access.

✅ The prefix is permanent — you can change a project's name and description later, but not its prefix.

!!! example "It's your turn now!"
    Create the project you'll be working on for the rest of the day.

    1. Log in to **Test Manager** from your Automation Cloud / Test Cloud tenant.
    2. On the **Home** page, click **Create new project**.
    3. Configure the project:
        - **Name** — `SAP_PO_{your name}`, e.g. `SAP_PO_Maria`
        - **Prefix** — `SAP{initials}`, e.g. `SAPMP` (3–5 characters; this cannot be changed later)
        - **Description** *(optional)* — e.g. `Test project for SAP purchase order verification (ME23N)`
    4. Click **Create**. Test Manager saves the project and opens its dashboard.
    5. *(Optional)* Mark the project as a **Favorite** so it's easy to find from the **Favorite projects** page.

    ✅ Your project is empty for now. In the next step, you'll add your first requirement and use Autopilot to generate test cases for it.

---

[Next → 02. Agentic Testing](02-agentic-testing.md){: .md-button .md-button--primary}

---

