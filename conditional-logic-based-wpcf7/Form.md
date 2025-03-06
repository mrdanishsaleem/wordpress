# This is for conditional based field form

## Form fields

```
<label> First Name (Given Name)* [text* first-name] </label>
<label> Last Name (Surname)* [text* last-name] </label>
<label> Company Name [text company-name] </label>
<label> Your Role [radio role use_label_element default:0 "Business Principal" "Business Employee" "Business Banker" "Broker" "Other"] </label>

<label> Phone* [tel* phone] </label>
<label> Phone Type [radio phone-type use_label_element default:0 "Office" "Mobile"] </label>

<label> Email* [email* email] </label>
<label> Website [url website] </label>
<label> What Time Zone are you in? [text timezone] </label>

<!-- Inquiry Type Selection -->
<label> Inquiry Type:
[select inquiry-type "Select Inquiry Type" "General Inquiry|najam" "Private Credit Inquiry|investments" "Equity Investment Inquiry|investments" "Asset Sale Inquiry|investments"]
</label>

<!-- General Inquiry -->
[group general-inquiry clear_on_hide]
  <label> Message [textarea message] </label>
  <label> Do you require a response? [radio response use_label_element default:0 "Yes" "No"] </label>
  <label> Preferred Response Method: [radio preferred-response use_label_element default:0 "Email" "Phone" "No Preference"] </label>
[/group]

<!-- Private Credit Inquiry -->
[group private-credit clear_on_hide]
  <label> Name of Business [text business-name] </label>
  <label> Business Type [select business-type "Select Business Type…" "Operating Business" "Startup" "Real Estate Development Project" "Real Estate Operating Company (OpCo)" "Investment Fund" "Other"] </label>
  <label> Industry [text industry] </label>
  <label> Description (What does the business do?) [textarea description] </label>
  <label> Based in (City/State/Country) [text based-in] </label>
  <label> 2+ Year Operating History? [radio operating-history use_label_element default:0 "Yes" "No" "Not Applicable"] </label>
  <label> Average Annual Revenue for last 2 Years [number average-annual-revenue] </label>
  <label> Can you provide last 2 Years of Financial Statements? [radio financial-statements use_label_element default:0 "Yes" "No"] </label>
  <label> Can you provide last 2 Years of Tax Filings? [radio tax-filings use_label_element default:0 "Yes" "No"] </label>
  <label> Do you have a business plan and future forecast ready? [radio business-plan-future-forecast use_label_element default:0 "Yes" "No"] </label>
  <label> Purpose of Loan [text purpose-of-loan] </label>
  <label> Specific Use of Proceeds [textarea proceeds] </label>
  <label> Loan Amount Sought (USD) [number loan-amount-sought] </label>
  <label> Collateral Pledged [textarea collateral-pledged] </label>
  <label> Collateral Location (City/State/Country) [text collateral-location] </label>
  <label> Value of Collateral (If known in USD) [number collateral-value] </label>
  <label> Is Business currently in default of any loans? [radio default-loans use_label_element default:0 "Yes" "No" "Not Applicable"] </label>
  <label> Is Business currently in bankruptcy proceedings? [radio bankruptcy-proceedings use_label_element default:0 "Yes" "No" "Not Applicable"] </label>
  <label> Is Business currently in any litigation? [radio business-litigation use_label_element default:0 "Yes" "No" "Not Applicable"] </label>
  <label> How soon would you like to close [select close "Select Transaction Timing…" "30-90 Days" "2-6 Months" "6+ Months" "Not Sure"] </label>
  <label> Preferred Response Method: [radio preferred-response use_label_element default:0 "Email" "Phone" "No Preference"] </label>
[/group]

<!-- Equity Investment Inquiry -->
[group equity-investment clear_on_hide]
  <label> Name of Business/Venture [text business-name] </label>
  <label> Business/Venture Type [select business-venture-type "Select Business/Venture Type…" "Operating Business" "Startup" "Real Estate Development Project" "Real Estate Operating Company (OpCo)" "Investment Fund" "Other"] </label>
  <label> Industry [text industry] </label>

  <!-- Real Estate Investments Only -->
  [group real-estate-investments clear_on_hide]
    <label><strong>Real Estate Investments Only</strong></label>
    <label> Type of Investment Sought [select investment-sought-type "Select Type of Investment Sought…" "Direct Ownership/Stake" "Co-GP (General Partner)" "LP (Limited Partner)" "JV (Joint Venture)" "Seed" "Not Sure"] </label>
    <label> Use of Proceeds [select proceeds "Use of Investment Proceeds…" "Construction / Development" "Acquisition / Purchase" "Land Banking" "Partner/GP/LP Buyout" "Sale-Leaseback" "Other"] </label>
    <label> Asset Type [select asset-type "Asset Type…" "Mixed-Use" "Multifamily" "Condo Development" "SFR - Built to Rent" "SFR - For Sale" "Student Housing" "Industrial" "Office" "Retail" "Raw Land" "Agricultural" "Energy - Solar Farm" "Energy - Oil & Gas Asset" "Marina (Ocean/Lake)" "Other / Special Purpose"] </label>

    <label> Investment Sought ($USD) [number investment-sought] </label>
    <label> Total Acquisition/Development Costs ($USD) [number total-acquisition-development-cost] </label>
    <label> Completion/Exit Valuation of Asset ($USD) [number completion-exit-valuation] </label>
    <label> Is Senior Debt Secured? [text senior-debt-secured] </label>
    <label> Project Start Date (Past or Projected) [date project-start-date] </label>
    <label> Projected IRR/Equity Multiple [text projected-irr-equity-multiple] </label>
    <label> Projected Hold Period (Years) [number projected-hold-period] </label>
    <label> Address of Project (If applicable) [text project-address] </label>
    <label> Do you have a Pitch Deck/Model ready? [radio pitch-deck-model use_label_element default:0 "Yes" "No" "Not Applicable"] </label>
    <label> Notes / Additional Info: [textarea notes-additional-info] </label>
  [/group]

  <!-- Operating Businesses & Startups -->
  [group operating-businesses-startups clear_on_hide]
    <label><strong>Operating Businesses & Startups</strong></label>
    <label> Type of Investment Sought [select investment-sought-type-business "Select Type of Investment Sought…" "Direct Ownership/Stake" "Co-GP (General Partner)" "LP (Limited Partner)" "JV (Joint Venture)" "Seed" "Not Sure"] </label>
    <label> Use of Proceeds [select proceeds-business "Use of Investment Proceeds…" "Construction / Development" "Acquisition / Purchase" "Land Banking" "Partner/GP/LP Buyout" "Sale-Leaseback" "Other"] </label>
    <label> Description (What does the business do?) [text description] </label>
    <label> What type of customer does business cater to? [text type-of-customer] </label>

    <label> Investment Sought ($USD) [number investment-sought-business] </label>
    <label> Current Valuation ($USD) [number current-valuation] </label>
    <label> Year Business/Venture began operating? [number business-venture-operating] </label>
    <label> Currently Revenue Positive? [radio currently-revenue-positive use_label_element default:0 "Yes" "No" "Not Applicable"] </label>
    <label> Currently Profitable? [radio currently-profitable use_label_element default:0 "Yes" "No" "Not Applicable"] </label>

    <label> Projected IRR/Equity Multiple [text projected-irr-equity-multiple-business] </label>
    <label> Projected Hold Period (Years) [number projected-hold-period-business] </label>
    <label> Business HQ Location (City/State/Country) [text business-hq-location] </label>
    <label> Do you have a Pitch Deck/Model ready? [radio pitch-deck-model-business use_label_element default:0 "Yes" "No" "Not Applicable"] </label>
    <label> Notes / Additional Info: [textarea notes-additional-info-business] </label>
  [/group]
[/group]

<!-- Asset Sale Inquiry -->
[group asset-sale clear_on_hide]
  <label> Type of Asset for Sale [radio asset-sale use_label_element default:0 "Operating Business" "Real Estate (Single Asset/Portfolio)" "Intellectual Property" "Business Assets" "Other"] </label>
  <label> Industry (If Applicable) [text industry] </label>
  <label> Location of Asset(s) (City/State/Country) [text location-of-assets] </label>

  <label> Asset(s) currently being marketed publicly? [radio marketed-publicly use_label_element default:0 "Yes" "No" "Not Applicable"] </label>
  <label> Is Asset currently in bankruptcy proceedings? [radio bankruptcy-proceedings use_label_element default:0 "Yes" "No" "Not Applicable"] </label>
  <label> Is Asset currently in default of any loans? [radio default-loans use_label_element default:0 "Yes" "No" "Not Applicable"] </label>
  <label> Is Asset part of any Probate proceedings? [radio probate-proceedings use_label_element default:0 "Yes" "No" "Not Applicable"] </label>

  <label> Asking Price ($USD) [number asking-price] </label>
  <label> Does Asset have any assumable debt? [radio assumable-debt use_label_element default:0 "Yes" "No" "Not Applicable"] </label>
  <label> Seller Financing Available? [radio seller-financing use_label_element default:0 "Yes" "No" "Not Applicable"] </label>

  <label> Additional details on prospective sale of asset(s): [textarea details-prospective-sale-of-assets] </label>
  <label> Preferred Response Method: [radio preferred-response use_label_element default:0 "Email" "Phone" "No Preference"] </label>
[/group]

[submit "Submit Message"]
```

### Mail Tab Settings

```
To: [inquiry-type]@crenexcapital.com
From: [_site_title] <wordpress@website.com>
Subject: [_site_title] "[inquiry-type]"
Additional headers: Reply-To: [email]
Message body:
```

Full Name: [first-name] [last-name]
Email: [email]
Company: [company-name]
Role: [role]
Phone: [phone] ([phone-type])
Website: [website]
Timezone: [timezone]

Inquiry Type: [inquiry-type]

[general-inquiry]
Message: [message]
Do you require a response? [response]
Preferred Response Method: [preferred-response]
[/general-inquiry]

[private-credit]
Business Name: [business-name]
Business Type: [business-type]
Industry: [industry]
Description: [description]
Based in: [based-in]
2+ Year Operating History?: [operating-history]
Average Annual Revenue (Last 2 Years): [average-annual-revenue]
Can provide last 2 Years of Financial Statements?: [financial-statements]
Can provide last 2 Years of Tax Filings?: [tax-filings]
Business Plan & Future Forecast Ready?: [business-plan-future-forecast]
Purpose of Loan: [purpose-of-loan]
Specific Use of Proceeds: [proceeds]
Loan Amount Sought (USD): [loan-amount-sought]
Collateral Pledged: [collateral-pledged]
Collateral Location: [collateral-location]
Value of Collateral (USD): [collateral-value]
Is Business in Default on Loans?: [default-loans]
Is Business in Bankruptcy Proceedings?: [bankruptcy-proceedings]
Is Business in Litigation?: [business-litigation]
How soon would you like to close?: [close]
Preferred Response Method: [preferred-response]
[/private-credit]

[equity-investment]
Business/Venture Name: [business-name]
Business/Venture Type: [business-venture-type]
Industry: [industry]

[real-estate-investments]
**Real Estate Investments Only**
Type of Investment Sought: [investment-sought-type]
Use of Proceeds: [proceeds]
Asset Type: [asset-type]
Investment Sought (USD): [investment-sought]
Total Acquisition/Development Costs (USD): [total-acquisition-development-cost]
Completion/Exit Valuation (USD): [completion-exit-valuation]
Is Senior Debt Secured?: [senior-debt-secured]
Project Start Date: [project-start-date]
Projected IRR/Equity Multiple: [projected-irr-equity-multiple]
Projected Hold Period (Years): [projected-hold-period]
Project Address: [project-address]
Pitch Deck/Model Ready?: [pitch-deck-model]
Notes / Additional Info: [notes-additional-info]
[/real-estate-investments]

[operating-businesses-startups]
**Operating Businesses & Startups**
Type of Investment Sought: [investment-sought-type-business]
Use of Proceeds: [proceeds-business]
Business Description: [description]
Customer Type: [type-of-customer]
Investment Sought (USD): [investment-sought-business]
Current Valuation (USD): [current-valuation]
Year Business/Venture Began Operating: [business-venture-operating]
Currently Revenue Positive?: [currently-revenue-positive]
Currently Profitable?: [currently-profitable]
Projected IRR/Equity Multiple: [projected-irr-equity-multiple-business]
Projected Hold Period (Years): [projected-hold-period-business]
Business HQ Location: [business-hq-location]
Pitch Deck/Model Ready?: [pitch-deck-model-business]
Notes / Additional Info: [notes-additional-info-business]
[/operating-businesses-startups]
[/equity-investment]

[asset-sale]
Type of Asset for Sale: [asset-sale]
Industry (If Applicable): [industry]
Location of Asset(s): [location-of-assets]
Asset(s) Publicly Marketed?: [marketed-publicly]
Asset in Bankruptcy Proceedings?: [bankruptcy-proceedings]
Asset in Default on Loans?: [default-loans]
Asset in Probate Proceedings?: [probate-proceedings]
Asking Price (USD): [asking-price]
Assumable Debt?: [assumable-debt]
Seller Financing Available?: [seller-financing]
Additional Sale Details: [details-prospective-sale-of-assets]
Preferred Response Method: [preferred-response]
[/asset-sale]

--
This is a notification that a contact form was submitted on your website ([ _site_title] [ _site_url ]).

```

```

### Conditional Fields Logic

```
show [general-inquiry] if [inquiry-type] equals "General Inquiry"
show [private-credit] if [inquiry-type] equals "Private Credit Inquiry"
show [equity-investment] if [inquiry-type] equals "Equity Investment Inquiry"
show [asset-sale] if [inquiry-type] equals "Asset Sale Inquiry"
show [real-estate-investments] if [business-venture-type] equals "Real Estate Development Project"
show [real-estate-investments] if [business-venture-type] equals "Real Estate Operating Company (OpCo)"
show [operating-businesses-startups] if [business-venture-type] equals "Operating Business"
show [operating-businesses-startups] if [business-venture-type] equals "Startup"
show [operating-businesses-startups] if [business-venture-type] equals "Investment Fund"
```

### Plugins Required:

- [Contact Form 7](https://wordpress.org/plugins/contact-form-7/)
- [Conditional Fields for Contact Form 7](https://wordpress.org/plugins/cf7-conditional-fields/)
