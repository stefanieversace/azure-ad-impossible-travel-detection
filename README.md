# 🧠 Impossible Travel Detection (Azure AD / KQL)

Detection logic to identify suspicious login behaviour where a user appears to log in from geographically distant locations within an impossible timeframe.

## 🚨 Problem
Attackers often use stolen credentials from different regions. Detecting rapid location changes helps identify compromised accounts.

## 🔍 Detection Logic
- Analyse Azure AD SigninLogs
- Compare consecutive login locations per user
- Identify country changes within short time windows
- Apply severity scoring based on time difference

## 🧪 Example Scenario
User logs in from UK → then Germany within 30 minutes → flagged as HIGH severity.

## 🛠️ Query
See: `queries/impossible_travel.kql`

## 📊 Output
- UserPrincipalName
- Previous Location → Current Location
- Time difference
- Severity classification

## 🎯 Skills Demonstrated
- KQL (Kusto Query Language)
- Microsoft Sentinel / Azure AD
- Threat detection engineering
- Behavioural analytics
- Identity security monitoring
