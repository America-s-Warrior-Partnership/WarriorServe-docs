# ⚡ Post-Install Setup

Complete the following steps after installing WarriorServe.

---

## 1. Assign Administrative Access

Assign the `WarriorServe Configuration` permission set to the primary system administrator responsible for setup and maintenance.

---

## 2. Configure Core Settings

1. Open the **WarriorServe Settings and Tools** app.
2. Enable the features your organization plans to use.
3. Save changes.

Examples may include:
- Enable WarriorServe
- Enable Case Auto Create
- Enable Event Logging
- Enable Task Auto Create
- Advanced integration settings

---

## 3. Create End User Permission Set

Create a permission set for staff users and grant access as needed.

### Recommended App Access
- WarriorServe

### Recommended Object Access
- Account
- Case
- Case Referral
- Contact
- Service Record
- Event Log *(Read Only recommended)*

### Recommended Named Credential Access
- VA_API_Key - VA_API_Named_Principle

Adjust Create, Read, Edit, Delete, and field-level security based on your operating model.

---

## 4. Review and Activate Flows

Review each included flow and customize as needed for your organization. If changes are required, save as a new version and activate it.

### Recommended Flows to Review/Activate
- AL Get Contact
- RT Case Referral After Save Partner Notification
- RT Contact After Save WWP Registration Requested
- RT Service Record Before Save Prevent Overlapping Dates
- Screen Flow Intake Guided Entry
- Screen Flow Partner Search and Referral Creation

---

## 5. Configure Intake Quick Actions

Create and place intake actions where users can easily access them.

### Contact
Setup → Object Manager → Contact → Buttons, Links, and Actions → New Action

### Case
Setup → Object Manager → Case → Buttons, Links, and Actions → New Action

### Placement Recommendations
- Add the Intake action to Contact page layouts
- Add the Intake action to Case record pages
- Use Dynamic Actions on Lightning pages when available

### Additional Recommendation
Add the **Refer to AWP** action to Case actions if used by your process.

---

## 6. Configure Partner Search and Referral Actions

Create actions used for referral workflows.

### Case Action
Create a Quick Action on Case for launching referral creation.

### Case Referral List View Button
Create a custom button or link for launching the Case action from related contexts.

#### Button URL
/lightning/action/quick/Case.Partner_Search?objectApiName=Case&context=RECORD_DETAIL&recordId={!CASESAFEID(Case.Id)}&backgroundContext=%2Flightning%2Fr%2FCase%2F{!CASESAFEID(Case.Id)}%2Fview

#### Optional Custom Button / Link

Some orgs may choose to launch the Case Quick Action with a custom button or link. This approach should be considered optional and must be tested in the target org, as Lightning navigation behavior can vary by context.

Example:

/lightning/action/quick/Case.Partner_Search?recordId={!CASESAFEID(Case.Id)}

#### What This Does
- Opens the Partner Search quick action
- Passes the current Case record ID
- Returns the user to the Case record after completion

### Lightning Record Page
Edit the Case Lightning Record Page:

Related Lists → Case Referrals → Add Action

This allows users to launch referral actions directly from the related list.