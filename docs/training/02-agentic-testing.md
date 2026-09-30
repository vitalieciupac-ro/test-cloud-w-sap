# Agentic Testing: From Requirement to Test Cases

## What is agentic testing?

**Agentic Testing** means augmenting testers with AI agents to extend, accelerate, and simplify their work ultimately helping them be more productive and find greater joy in testing.

## 1. Out-of-the-Box Agents: Autopilot for Testers

Autopilot for Testers is a collection of AI-powered digital systems (agents) designed to boost the productivity of testers throughout the entire testing lifecycle.

These capabilities are integrated into UiPath Studio Desktop and UiPath Test Manager.

![Agent Type OOTB](../assets/images/Agent%20type%20OOTB.png)

### Agents you'll explore in hands-on

In the hands-on exercises ahead, you'll work with two key agents:

✅ **Evaluation Agent** Analyzes and evaluates requirements to ensure clarity, completeness, and testability

✅ **Test Case Generation Agent** Automatically generates comprehensive test cases based on requirements, saving time and improving coverage

### Hands-on: From Requirement to Test Cases

Let's see how Autopilot for Testers helps you move from requirements to test cases with a real-world example.

<div style="background-color: #f5f5f5; border: 1px solid #ddd; border-radius: 4px; margin: 16px 0; overflow: hidden;">
  <div style="position: relative; padding: 16px; background-color: #f5f5f5;">
    <button type="button" id="copyBtn" style="position: absolute; top: 12px; right: 12px; background-color: white; border: 2px solid #ff6b35; color: #ff6b35; padding: 10px 18px; border-radius: 6px; cursor: pointer; font-weight: 600; font-size: 13px; z-index: 1001; transition: all 0.3s ease; letter-spacing: 0.3px; pointer-events: auto; outline: none;">📋 Copy</button>
    <pre id="requirementBlock" style="margin: 0; padding: 40px 16px 16px 16px; font-family: 'Courier New', monospace; font-size: 13px; line-height: 1.5; color: #333; white-space: pre-wrap; word-wrap: break-word;">As an SAP procurement user, I want to display a purchase order in SAP GUI and review the account assignment and location details of its first line item, so that I can confirm the purchase order matches the approved test data.

## Preconditions

* The approved test data is available: the purchase order (PO) number and the expected account assignment and location for Line Item 1.

* The user has valid SAP GUI credentials and is authorized to use transaction ME23N.

## User Flow

* The user logs in to SAP GUI with valid credentials.

* The system displays the SAP home screen.

* The user opens transaction ME23N.

* The system opens the Purchase Order display screen.

* The user clicks 'Other Purchase Order' and enters the provided PO number.

* The system displays the purchase order and its details.

* The user opens Line Item 1 and reviews its account assignment and location.

## Acceptance Criteria

* User logs in with valid credentials:
  * Login succeeds and the SAP home screen is displayed.

* User logs in with invalid credentials:
  * Login fails, an error message is displayed, and the user remains on the login screen.

* User opens transaction ME23N:
  * The Purchase Order display screen opens successfully.

* User enters a valid PO number using 'Other Purchase Order':
  * The correct purchase order and its details are displayed.

* User enters a PO number that does not exist:
  * An error message is displayed and no purchase order details are shown.

* Line Item 1 details match the approved test data:
  * The account assignment and location are confirmed as correct.

* Any Line Item 1 detail does not match the approved test data:
  * The mismatch is reported, naming the field, the expected value, and the displayed value.</pre>
  </div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const copyBtn = document.getElementById('copyBtn');
  const requirementBlock = document.getElementById('requirementBlock');

  if (copyBtn && requirementBlock) {
    copyBtn.addEventListener('click', async function(e) {
      e.preventDefault();
      e.stopPropagation();

      const text = requirementBlock.textContent || requirementBlock.innerText || '';
      const originalText = copyBtn.innerHTML;

      try {
        if (navigator.clipboard && window.isSecureContext) {
          await navigator.clipboard.writeText(text);
        } else {
          const temp = document.createElement('textarea');
          temp.value = text;
          temp.setAttribute('readonly', '');
          temp.style.position = 'fixed';
          temp.style.left = '-9999px';
          document.body.appendChild(temp);
          temp.select();
          document.execCommand('copy');
          document.body.removeChild(temp);
        }

        copyBtn.innerHTML = '✅ Copied!';
        copyBtn.style.borderColor = '#4caf50';
        copyBtn.style.color = '#4caf50';

        setTimeout(() => {
          copyBtn.innerHTML = originalText;
          copyBtn.style.borderColor = '#ff6b35';
          copyBtn.style.color = '#ff6b35';
        }, 2000);
      } catch (err) {
        console.error('Copy failed:', err);
        copyBtn.innerHTML = '⚠️ Failed';
        copyBtn.style.borderColor = '#d32f2f';
        copyBtn.style.color = '#d32f2f';

        setTimeout(() => {
          copyBtn.innerHTML = originalText;
          copyBtn.style.borderColor = '#ff6b35';
          copyBtn.style.color = '#ff6b35';
        }, 2000);
      }
    });
  }
});
</script>


## 2. Built Your Way – Custom AI Agents

Beyond the out-of-the-box capabilities, you have the full power to build your own AI agents tailored specifically to your unique testing needs.

![Agent Type BYOM](../assets/images/Agent%20type%20BYOM.png)

Custom agents give you the flexibility to:

✅ Solve problems specific to your testing processes

✅ Integrate with your existing tools and workflows

✅ Automate repetitive testing tasks your way

✅ Extend Test Cloud with agent-driven innovation

---

[Next → Getting Started in Studio](03-getting-started-studio.md){: .md-button .md-button--primary}

---

