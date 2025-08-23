Here’s your **exam-ready, structured breakdown** of the **"Policy evaluation logic basics"** section from the AWS IAM documentation, covering the sidebar structure (implied), core concepts, and a practical example:

---

## Page Structure & Sidebar Highlights

This documentation typically flows as follows (and the sidebar navigation mirrors this):

* **Policy evaluation for an IAM role**
* **Policy evaluation for an IAM user**
* **Example identity-based and resource-based policy evaluation**
  ([AWS Documentation][1])

---

## Core Principles of Policy Evaluation

### 1. **High-Level Evaluation Flow**

Whenever someone (a principal) requests access via the AWS Console, CLI, or API:

1. **Authentication** – AWS first verifies the principal’s identity.
2. **Processing the request context** – Includes details like the identity, requested action, target resource, and environmental context.
3. **Policy Enforcement Logic** – AWS evaluates all applicable policies in a defined order to decide whether to **Allow** or **Deny** the request.
   ([AWS Documentation][2])

---

### 2. **Evaluation Logic Rules**

* **Implicit Deny**: By default, any request is denied unless explicitly allowed.
* **Explicit Allow**: Required to grant access.
* **Explicit Deny**: Precedes and overrides any Allow.
* **Policy Types Evaluated**:

  * Identity-based (user, group, or role)
  * Resource-based (attached to the resource, e.g., S3 bucket policy)
  * Permissions boundaries
  * Session policies (from STS)
  * Service Control Policies (SCPs) or Resource Control Policies (RCPs) in AWS Organizations
    ([AWS Documentation][3])

---

### 3. **Identity-Based + Resource-Based Policies**

* In a single AWS account, AWS considers **both identity-based** and **resource-based policies** together.
* The effective permissions are the **union** of both.
* If *either* policy grants Allow, and no Deny exists, access is allowed.
* But if **any** policy contains an explicit Deny, it overrides all.
  ([AWS Documentation][4])

---

## 4. **Example Scenario: Carlos and S3 Buckets**

* **Context**: User `carlossalazar` wants to save a file to two buckets:

  1. `...-logs` bucket → contains "log"
  2. His personal bucket `...-carlossalazar`

* **Identity-based policy** includes:

  * Allow listing all buckets
  * Allow all actions on his own bucket
  * **Deny** any actions on buckets with "log" in their names

* **Bucket policy** (resource-based) allows only `carlossalazar` to access his bucket.

* **Outcome**:

  * For the `...-logs` bucket: AWS sees the explicit Deny → **Deny** the request.
  * For his own bucket: No Deny. Both identity and resource policies Allow → **Allow** the request.
    Even if one policy allowed and the other didn't, access would still be allowed—but Deny always wins.
    ([AWS Documentation][1])

---

## Summary Table

| Step / Concept    | Result / Interpretation                                                               |
| ----------------- | ------------------------------------------------------------------------------------- |
| **Implicit Deny** | Default unless explicitly allowed.                                                    |
| **Explicit Deny** | Always takes precedence.                                                              |
| **Union Rule**    | Allow if *either* identity-based or resource-based policy allows, and no Deny exists. |
| **Policy Types**  | Identity-based, resource-based, boundaries, session, SCP/RCP.                         |

---

### Exam Tips

* Always assume an **implicit Deny** exists—Allow must be explicit.
* Understand that **explicit Deny overrides everything**.
* Recognize how **identity-based** and **resource-based** policies combine.
* Real scenarios like the Carlos + S3 example help cement these principles.

---

Need a diagram to visualize the flow or want to walk through a different service—like EC2 or KMS—with these rules in action? Let me know!

[1]: https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic_policy-eval-basics.html "Policy evaluation for requests within a single account - AWS Identity and Access Management"
[2]: https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic.html?utm_source=chatgpt.com "Policy evaluation logic - AWS Identity and Access ..."
[3]: https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic_policy-eval-denyallow.html?utm_source=chatgpt.com "How AWS enforcement code logic evaluates requests to ..."
[4]: https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic_policy-eval-basics.html?utm_source=chatgpt.com "Policy evaluation for requests within a single account"
Here’s your **exam-ready, structured breakdown** of the **"Policy evaluation logic basics"** section from the AWS IAM documentation, covering the sidebar structure (implied), core concepts, and a practical example:

---

## Page Structure & Sidebar Highlights

This documentation typically flows as follows (and the sidebar navigation mirrors this):

* **Policy evaluation for an IAM role**
* **Policy evaluation for an IAM user**
* **Example identity-based and resource-based policy evaluation**
  ([AWS Documentation][1])

---

## Core Principles of Policy Evaluation

### 1. **High-Level Evaluation Flow**

Whenever someone (a principal) requests access via the AWS Console, CLI, or API:

1. **Authentication** – AWS first verifies the principal’s identity.
2. **Processing the request context** – Includes details like the identity, requested action, target resource, and environmental context.
3. **Policy Enforcement Logic** – AWS evaluates all applicable policies in a defined order to decide whether to **Allow** or **Deny** the request.
   ([AWS Documentation][2])

---

### 2. **Evaluation Logic Rules**

* **Implicit Deny**: By default, any request is denied unless explicitly allowed.
* **Explicit Allow**: Required to grant access.
* **Explicit Deny**: Precedes and overrides any Allow.
* **Policy Types Evaluated**:

  * Identity-based (user, group, or role)
  * Resource-based (attached to the resource, e.g., S3 bucket policy)
  * Permissions boundaries
  * Session policies (from STS)
  * Service Control Policies (SCPs) or Resource Control Policies (RCPs) in AWS Organizations
    ([AWS Documentation][3])

---

### 3. **Identity-Based + Resource-Based Policies**

* In a single AWS account, AWS considers **both identity-based** and **resource-based policies** together.
* The effective permissions are the **union** of both.
* If *either* policy grants Allow, and no Deny exists, access is allowed.
* But if **any** policy contains an explicit Deny, it overrides all.
  ([AWS Documentation][4])

---

## 4. **Example Scenario: Carlos and S3 Buckets**

* **Context**: User `carlossalazar` wants to save a file to two buckets:

  1. `...-logs` bucket → contains "log"
  2. His personal bucket `...-carlossalazar`

* **Identity-based policy** includes:

  * Allow listing all buckets
  * Allow all actions on his own bucket
  * **Deny** any actions on buckets with "log" in their names

* **Bucket policy** (resource-based) allows only `carlossalazar` to access his bucket.

* **Outcome**:

  * For the `...-logs` bucket: AWS sees the explicit Deny → **Deny** the request.
  * For his own bucket: No Deny. Both identity and resource policies Allow → **Allow** the request.
    Even if one policy allowed and the other didn't, access would still be allowed—but Deny always wins.
    ([AWS Documentation][1])

---

## Summary Table

| Step / Concept    | Result / Interpretation                                                               |
| ----------------- | ------------------------------------------------------------------------------------- |
| **Implicit Deny** | Default unless explicitly allowed.                                                    |
| **Explicit Deny** | Always takes precedence.                                                              |
| **Union Rule**    | Allow if *either* identity-based or resource-based policy allows, and no Deny exists. |
| **Policy Types**  | Identity-based, resource-based, boundaries, session, SCP/RCP.                         |

---

### Exam Tips

* Always assume an **implicit Deny** exists—Allow must be explicit.
* Understand that **explicit Deny overrides everything**.
* Recognize how **identity-based** and **resource-based** policies combine.
* Real scenarios like the Carlos + S3 example help cement these principles.

---

Need a diagram to visualize the flow or want to walk through a different service—like EC2 or KMS—with these rules in action? Let me know!

[1]: https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic_policy-eval-basics.html "Policy evaluation for requests within a single account - AWS Identity and Access Management"
[2]: https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic.html?utm_source=chatgpt.com "Policy evaluation logic - AWS Identity and Access ..."
[3]: https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic_policy-eval-denyallow.html?utm_source=chatgpt.com "How AWS enforcement code logic evaluates requests to ..."
[4]: https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic_policy-eval-basics.html?utm_source=chatgpt.com "Policy evaluation for requests within a single account"
