# Day 30: Final reflection

*Auto-extracted from "Cloud Security: A Beginner's Guide to Protecting AWS, Azure, and Google Cloud" (source lines 9372-9771). Review against the printed book before classroom use.*

Today you turn a month of work into a clear next step.

Read your folders from Day 1 to Day 29. Pick the five strongest
artifacts and explain why each one is safe, useful, and job-relevant.

Write a one-page learning reflection: what you understand now, what
still feels weak, and what you will practice next.

Evidence to save: final reflection, top-five artifact list, and a next-30-
days plan.

Safety check: review every artifact one more time for account IDs,
emails, keys, IPs, billing details, and customer data before sharing.

End with one sentence you can say in an interview: "I practiced cloud
security by..." Save as day30-final-reflection.

Expanded Entry-Level Practice Exam Bank
These questions are rewritten to test real beginner judgment, not
memorization. Read the situation, choose the safest answer, then read
the explanation. The explanations are part of the learning.

How to use this bank: Try 10 questions at a time. Write down why you
chose each answer before checking the explanation. If you miss a
question, return to the chapter that teaches that control.

Score guide: 40-50 correct means you are ready for an entry-level
review. 30-39 means review the weak chapters and repeat the labs.
Below 30 means slow down, rebuild the foundation, and practice more
before taking a certification-style exam.

Question 1

A new developer needs to read objects from one storage bucket but
should not upload or delete anything. Which permission approach is
best?

A. Give the developer administrator access for one week.

B. Create a read-only permission scoped to that single bucket.

C. Share the root account password and rotate it later.

D. Make the bucket public so no identity permission is needed.

Answer: B. Least privilege means granting only the exact action and
resource needed. Read-only access to one bucket limits damage if the
identity is misused.

Question 2

An AWS account has not enabled MFA on the root user. What is the
first security priority?

A. Delete all IAM users.

B. Enable MFA on the root user and stop using it for daily work.

C. Open port 22 to the internet for easier management.

D. Disable all logs until the account is configured.

Answer: B. The root user is the master key for the account. It should
be strongly protected and reserved for rare account-level tasks.

Question 3

A storage bucket contains private customer documents. A teammate
suggests turning on public access to fix an application error. What
should you do?

A. Approve it because public buckets are easier to test.

B. Turn on public access only during business hours.

C. Find the exact identity or service that needs access and grant that
access privately.

D. Move the documents to a virtual machine instead.

Answer: C. Private data should not become public to solve an access
problem. The safer fix is to identify the real caller and grant narrow
access.

Question 4

Which statement best explains the shared responsibility model?

A. The provider secures everything after you create an account.

B. The customer secures only physical hardware.

C. The provider secures the cloud infrastructure, while the customer
secures data, identities, and configurations in the cloud.

D. The model applies only to SaaS applications.

Answer: C. Cloud security is shared. Providers handle facilities and
infrastructure; customers handle what they configure and store.

Question 5

A virtual machine has SSH open to 0.0.0.0/0. Why is this risky?

A. It blocks all administrators from connecting.

B. It allows connection attempts from anywhere on the internet.

C. It encrypts the disk automatically.

D. It turns the machine into a managed database.

Answer: B. 0.0.0.0/0 means any IPv4 address. Management ports
should be restricted to trusted sources or accessed through safer
methods.

Question 6

A program needs cloud access. Which option avoids storing a long-
lived secret in code?

A. Hard-code an access key and hide the file name.

B. Use a role, managed identity, or service account with short-lived
credentials.

C. Email the secret to the team.

D. Paste the key into a screenshot for documentation.

Answer: B. Machine identities and roles provide temporary credentials
without placing permanent secrets in source code.

Question 7

Which control helps detect who changed a security group rule
yesterday?

A. Object storage versioning

B. Activity or audit logs

C. A larger virtual machine size

D. A public IP address

Answer: B. Activity logs such as CloudTrail, Azure Activity Log, and
Google Cloud Audit Logs record management actions.

Question 8

A team stores database passwords in a text file inside a repository.
What is the best replacement?

A. Rename the file to passwords-old.txt.

B. Move the passwords to a secrets manager and remove them from
the repository history where possible.

C. Compress the repository.

D. Give the repository to fewer people but keep the passwords there.

Answer: B. Secrets belong in a managed secret store, not in code or
shared files. Leaked repository secrets should also be rotated.

Question 9

Why should cloud learners set a billing alert before running labs?

A. Billing alerts make virtual machines faster.

B. Billing alerts prevent every charge automatically.

C. Billing alerts warn early when usage or cost rises unexpectedly.

D. Billing alerts replace cleanup steps.

Answer: C. Alerts do not replace careful cleanup, but they help
beginners catch cost surprises quickly.

Question 10

Which design is best for a simple web app with a database?

A. Place both the web server and database in public subnets.

B. Place the web server where users can reach it and keep the
database private.

C. Make the database public and hide its name.

D. Disable all firewall rules.

Answer: B. Only the front end that must serve users should be
reachable. Databases should normally stay private.

Question 11

Which item is usually the customer’s responsibility in all cloud service
models?

A. Physical data center guards

B. The provider backbone network

C. Data classification and access decisions

D. Replacing failed physical disks

Answer: C. Customers decide what data means, who can access it, and
how it should be protected.

Question 12

A team keeps old access keys for former contractors. What should
happen?

A. Keep them in case someone needs them later.

B. Disable and delete unused keys after confirming they are no longer
needed.

C. Print them for backup.

D. Attach administrator policy to make them easy to test.

Answer: B. Unused credentials are unnecessary risk. Remove them as
part of identity hygiene.

Question 13

Which term means proving identity with more than one kind of
evidence?

A. CIDR

B. MFA

C. Subnetting

D. Object versioning

Answer: B. Multi-factor authentication uses more than one proof,
such as a password plus an authenticator app or security key.

Question 14

A security group allows inbound traffic from the entire internet to a
database port. What is the safest beginner fix?

A. Allow all outbound traffic too.

B. Restrict inbound traffic to only the application tier that needs the
database.

C. Change the database name.

D. Move the rule to a spreadsheet.

Answer: B. Database ports should not be exposed broadly. Allow only
known sources that truly need access.

Question 15

What is the main purpose of encryption in transit?

A. Protect data while it moves across a network.

B. Delete old data automatically.

C. Grant administrator access.

D. Show cloud costs.

Answer: A. Encryption in transit protects data while it moves between
clients, services, and networks.

Question 16

What does encryption at rest protect?

A. Data while it is stored on disks or storage services.

B. Only keyboard input.

C. Only public websites.

D. Only account passwords.

Answer: A. Encryption at rest protects stored data, such as files,
database records, backups, and disks.

Question 17

A company wants evidence that controls are working. What should it
collect?

A. Only opinions from the team.

B. Screenshots, logs, configuration exports, and notes that show the
control state.

C. A list of favorite cloud services.

D. The root password.

Answer: B. Evidence makes security reviewable. It should prove what
was checked and what was found.

Question 18

Why is public object storage a common cloud risk?

A. Object storage cannot hold files.

B. Public settings are easy to misunderstand and can expose data
directly to the internet.

C. Object storage always disables encryption.

D. All public buckets are required for backups.

Answer: B. The risk is not the storage service itself; it is accidental
broad access to data.

Question 19

Which action is safest before sharing a screenshot in a portfolio?

A. Post the screenshot immediately.

B. Review and blur account IDs, emails, IP addresses, secret values,
customer names, and bills.

C. Add more sensitive details to prove skill.

D. Turn off MFA temporarily.

Answer: B. Portfolio evidence should be useful without exposing
secrets or private information.

Question 20

A container image came from an unknown public source. What should
you do before using it?

A. Run it as administrator to test quickly.

B. Scan it, review its source, and prefer trusted or official images.

C. Disable logging.

D. Store credentials inside it.

Answer: B. Containers can carry vulnerable or malicious software.
Trust and scanning matter.

Question 21

Which Kubernetes idea reduces the power of a compromised
workload?

A. Giving every pod cluster-admin.

B. Using least privilege service accounts and network policies.

C. Turning off all namespaces.

D. Putting secrets in image layers.

Answer: B. Kubernetes workloads need narrow identities and
controlled communication paths.

Question 22

A serverless function can read every storage bucket in the account,
but it only needs one. What is wrong?
