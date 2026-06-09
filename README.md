<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Illinois Business Startup Guide</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display&family=Inter:wght@400;500;600;700&display=swap');

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --navy: #0f1f3d;
    --navy-mid: #1a3260;
    --gold: #c9a84c;
    --gold-light: #f0d98a;
    --cream: #f8f5ef;
    --white: #ffffff;
    --gray-100: #f1f1f1;
    --gray-300: #d0d0d0;
    --gray-500: #888;
    --gray-700: #444;
    --green: #2e7d52;
    --green-light: #e8f5ee;
    --red: #b84040;
    --red-light: #fdeaea;
    --courier: #1a6b9a;
    --courier-light: #e6f2fa;
    --charcuterie: #7a3e22;
    --charcuterie-light: #fdf0e8;
  }

  body {
    font-family: 'Inter', sans-serif;
    background: var(--cream);
    color: var(--navy);
    min-height: 100vh;
  }

  /* HEADER */
  header {
    background: var(--navy);
    padding: 28px 24px 24px;
    text-align: center;
    border-bottom: 3px solid var(--gold);
  }

  .state-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: var(--gold);
    color: var(--navy);
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    padding: 5px 14px;
    border-radius: 2px;
    margin-bottom: 14px;
  }

  header h1 {
    font-family: 'DM Serif Display', serif;
    color: var(--white);
    font-size: clamp(22px, 5vw, 36px);
    line-height: 1.2;
    margin-bottom: 8px;
  }

  header p {
    color: var(--gold-light);
    font-size: 14px;
    opacity: 0.85;
    max-width: 520px;
    margin: 0 auto;
  }

  /* TABS */
  .tabs-wrapper {
    background: var(--navy-mid);
    padding: 0 20px;
    display: flex;
    justify-content: center;
    gap: 4px;
  }

  .tab-btn {
    background: none;
    border: none;
    cursor: pointer;
    padding: 16px 24px 14px;
    font-family: 'Inter', sans-serif;
    font-size: 14px;
    font-weight: 600;
    color: rgba(255,255,255,0.55);
    border-bottom: 3px solid transparent;
    transition: all 0.2s;
    display: flex;
    align-items: center;
    gap: 8px;
    white-space: nowrap;
  }

  .tab-btn:hover { color: rgba(255,255,255,0.85); }

  .tab-btn.active {
    color: var(--gold);
    border-bottom-color: var(--gold);
  }

  .tab-icon {
    font-size: 18px;
  }

  /* MAIN */
  main {
    max-width: 860px;
    margin: 0 auto;
    padding: 28px 16px 60px;
  }

  /* PROGRESS CARD */
  .progress-card {
    border-radius: 10px;
    padding: 20px 24px;
    margin-bottom: 24px;
    display: flex;
    align-items: center;
    gap: 20px;
    flex-wrap: wrap;
  }

  .progress-card.courier { background: var(--courier-light); border-left: 4px solid var(--courier); }
  .progress-card.charcuterie { background: var(--charcuterie-light); border-left: 4px solid var(--charcuterie); }

  .progress-info { flex: 1; min-width: 160px; }
  .progress-label {
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    margin-bottom: 6px;
  }
  .courier .progress-label { color: var(--courier); }
  .charcuterie .progress-label { color: var(--charcuterie); }

  .progress-bar-track {
    background: rgba(0,0,0,0.1);
    border-radius: 99px;
    height: 8px;
    overflow: hidden;
  }

  .progress-bar-fill {
    height: 100%;
    border-radius: 99px;
    transition: width 0.4s ease;
  }
  .courier .progress-bar-fill { background: var(--courier); }
  .charcuterie .progress-bar-fill { background: var(--charcuterie); }

  .progress-fraction {
    font-size: 28px;
    font-family: 'DM Serif Display', serif;
    line-height: 1;
  }
  .courier .progress-fraction { color: var(--courier); }
  .charcuterie .progress-fraction { color: var(--charcuterie); }

  .progress-sublabel { font-size: 11px; color: var(--gray-500); margin-top: 2px; }

  /* SECTION */
  .section {
    margin-bottom: 20px;
  }

  .section-header {
    display: flex;
    align-items: center;
    gap: 10px;
    cursor: pointer;
    padding: 14px 18px;
    background: var(--white);
    border-radius: 8px 8px 0 0;
    border: 1px solid var(--gray-300);
    user-select: none;
    transition: background 0.15s;
  }

  .section-header:hover { background: var(--gray-100); }

  .section-header.collapsed {
    border-radius: 8px;
  }

  .section-num {
    width: 26px;
    height: 26px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 12px;
    font-weight: 700;
    flex-shrink: 0;
  }
  .courier .section-num { background: var(--courier); color: white; }
  .charcuterie .section-num { background: var(--charcuterie); color: white; }

  .section-title-group { flex: 1; }
  .section-title { font-size: 15px; font-weight: 700; }
  .section-subtitle { font-size: 12px; color: var(--gray-500); margin-top: 2px; }

  .section-chevron {
    font-size: 12px;
    color: var(--gray-500);
    transition: transform 0.2s;
  }
  .section-header.collapsed .section-chevron { transform: rotate(-90deg); }

  .section-mini-progress {
    font-size: 12px;
    font-weight: 600;
    padding: 3px 10px;
    border-radius: 99px;
  }
  .courier .section-mini-progress { background: var(--courier-light); color: var(--courier); }
  .charcuterie .section-mini-progress { background: var(--charcuterie-light); color: var(--charcuterie); }
  .section-mini-progress.done { background: var(--green-light); color: var(--green); }

  .section-body {
    border: 1px solid var(--gray-300);
    border-top: none;
    border-radius: 0 0 8px 8px;
    overflow: hidden;
  }

  /* CHECKLIST ITEMS */
  .check-item {
    display: flex;
    gap: 14px;
    align-items: flex-start;
    padding: 14px 18px;
    border-bottom: 1px solid var(--gray-100);
    transition: background 0.15s;
    cursor: pointer;
  }

  .check-item:last-child { border-bottom: none; }
  .check-item:hover { background: #fafafa; }
  .check-item.checked { background: var(--green-light); }

  .check-box {
    width: 20px;
    height: 20px;
    border-radius: 4px;
    border: 2px solid var(--gray-300);
    flex-shrink: 0;
    margin-top: 1px;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.2s;
    background: white;
  }

  .check-item.checked .check-box {
    background: var(--green);
    border-color: var(--green);
    color: white;
  }

  .check-box-inner { font-size: 12px; display: none; }
  .check-item.checked .check-box-inner { display: block; }

  .check-content { flex: 1; }

  .check-title {
    font-size: 14px;
    font-weight: 600;
    line-height: 1.4;
  }

  .check-item.checked .check-title {
    color: var(--green);
    text-decoration: line-through;
    opacity: 0.7;
  }

  .check-desc {
    font-size: 13px;
    color: var(--gray-700);
    margin-top: 4px;
    line-height: 1.5;
  }

  .check-item.checked .check-desc { opacity: 0.5; }

  .check-link {
    display: inline-flex;
    align-items: center;
    gap: 4px;
    margin-top: 6px;
    font-size: 12px;
    font-weight: 600;
    text-decoration: none;
    padding: 3px 10px;
    border-radius: 4px;
    transition: opacity 0.15s;
  }
  .check-link:hover { opacity: 0.8; }
  .courier .check-link { background: var(--courier-light); color: var(--courier); }
  .charcuterie .check-link { background: var(--charcuterie-light); color: var(--charcuterie); }

  .check-tag {
    display: inline-block;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    padding: 2px 7px;
    border-radius: 3px;
    margin-left: 8px;
    vertical-align: middle;
  }
  .tag-cost { background: #fff3cd; color: #856404; }
  .tag-required { background: var(--red-light); color: var(--red); }
  .tag-optional { background: var(--gray-100); color: var(--gray-500); }
  .tag-tip { background: #e8eaf6; color: #3949ab; }

  /* NOTES BOX */
  .notes-box {
    background: white;
    border: 1px solid var(--gray-300);
    border-radius: 8px;
    padding: 16px 18px;
    margin-bottom: 20px;
  }
  .notes-box h3 {
    font-size: 13px;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    color: var(--gray-500);
    margin-bottom: 10px;
  }
  .notes-box textarea {
    width: 100%;
    border: 1px solid var(--gray-300);
    border-radius: 6px;
    padding: 10px 12px;
    font-family: 'Inter', sans-serif;
    font-size: 13px;
    color: var(--navy);
    resize: vertical;
    min-height: 80px;
    outline: none;
    transition: border-color 0.2s;
  }
  .notes-box textarea:focus { border-color: var(--navy-mid); }

  /* RESOURCE LINKS */
  .resources {
    background: white;
    border: 1px solid var(--gray-300);
    border-radius: 8px;
    padding: 16px 18px;
    margin-bottom: 20px;
  }
  .resources h3 {
    font-size: 13px;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    color: var(--gray-500);
    margin-bottom: 12px;
  }
  .resource-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(210px, 1fr));
    gap: 8px;
  }
  .resource-link {
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 10px 12px;
    background: var(--cream);
    border-radius: 6px;
    text-decoration: none;
    color: var(--navy);
    font-size: 12px;
    font-weight: 600;
    border: 1px solid var(--gray-300);
    transition: background 0.15s;
  }
  .resource-link:hover { background: var(--gray-100); }
  .resource-link span { font-size: 15px; }

  /* HIDDEN */
  .tab-panel { display: none; }
  .tab-panel.active { display: block; }

  /* DISCLAIMER */
  .disclaimer {
    background: #fff8e1;
    border: 1px solid #ffe082;
    border-radius: 8px;
    padding: 12px 16px;
    font-size: 12px;
    color: #5d4037;
    margin-bottom: 20px;
    line-height: 1.5;
  }
  .disclaimer strong { color: #4e342e; }

  /* RESET */
  .reset-btn {
    background: none;
    border: 1px solid var(--gray-300);
    border-radius: 6px;
    padding: 7px 14px;
    font-size: 12px;
    font-weight: 600;
    color: var(--gray-500);
    cursor: pointer;
    transition: all 0.15s;
    margin-top: 4px;
  }
  .reset-btn:hover { background: var(--red-light); border-color: var(--red); color: var(--red); }
</style>
</head>
<body>

<header>
  <div class="state-badge">🏛️ State of Illinois</div>
  <h1>Business Startup Guide</h1>
  <p>Step-by-step checklists to legally launch your businesses in Illinois — check off tasks as you complete them.</p>
</header>

<div class="tabs-wrapper">
  <button class="tab-btn active" onclick="switchTab('courier')" id="tab-courier">
    <span class="tab-icon">🚑</span> Medical Courier
  </button>
  <button class="tab-btn" onclick="switchTab('charcuterie')" id="tab-charcuterie">
    <span class="tab-icon">🧀</span> Charcuterie Cart
  </button>
</div>

<main>

  <!-- ======== MEDICAL COURIER ======== -->
  <div class="tab-panel courier active" id="panel-courier">

    <div class="disclaimer">
      <strong>⚠️ Disclaimer:</strong> This guide is for informational purposes only and is not legal or regulatory advice. Requirements can change — always verify with the relevant Illinois state agency, your county, and your municipality before proceeding.
    </div>

    <div class="progress-card courier">
      <div class="progress-info">
        <div class="progress-label">Your Progress</div>
        <div class="progress-bar-track">
          <div class="progress-bar-fill" id="courier-bar" style="width:0%"></div>
        </div>
        <div style="font-size:12px;color:var(--gray-500);margin-top:4px;" id="courier-pct">0% complete</div>
      </div>
      <div style="text-align:center;">
        <div class="progress-fraction" id="courier-frac">0/0</div>
        <div class="progress-sublabel">steps done</div>
      </div>
      <button class="reset-btn" onclick="resetTab('courier')">Reset</button>
    </div>

    <!-- SECTION 1 -->
    <div class="section courier" id="courier-sec-1">
      <div class="section-header" onclick="toggleSection('courier-sec-1')">
        <div class="section-num">1</div>
        <div class="section-title-group">
          <div class="section-title">Choose Your Business Structure</div>
          <div class="section-subtitle">LLC, sole proprietor, corporation — pick what fits</div>
        </div>
        <span class="section-mini-progress" id="courier-sec-1-prog">0/3</span>
        <span class="section-chevron">▼</span>
      </div>
      <div class="section-body">
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Decide on business structure <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">Most medical couriers choose an LLC for liability protection. An S-Corp may offer tax advantages once profitable. Sole proprietor has unlimited personal liability — not recommended for medical transport.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Register your business with the Illinois Secretary of State <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">File Articles of Organization (LLC) or Articles of Incorporation (Corp). LLC filing fee is $150. Must include a registered agent with an Illinois address.</div>
            <a class="check-link" href="https://www.ilsos.gov/departments/business_services/home.html" target="_blank">→ IL Secretary of State</a>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Get a Federal EIN (Employer Identification Number) <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">Free from the IRS. Required to open a business bank account, hire employees, and file taxes. Apply online — takes about 15 minutes.</div>
            <a class="check-link" href="https://www.irs.gov/businesses/small-businesses-self-employed/apply-for-an-employer-identification-number-ein-online" target="_blank">→ IRS EIN Application (Free)</a>
          </div>
        </div>
      </div>
    </div>

    <!-- SECTION 2 -->
    <div class="section courier" id="courier-sec-2">
      <div class="section-header" onclick="toggleSection('courier-sec-2')">
        <div class="section-num">2</div>
        <div class="section-title-group">
          <div class="section-title">Illinois State Licensing & Registration</div>
          <div class="section-subtitle">State-level requirements for operating in IL</div>
        </div>
        <span class="section-mini-progress" id="courier-sec-2-prog">0/4</span>
        <span class="section-chevron">▼</span>
      </div>
      <div class="section-body">
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Register with Illinois Department of Revenue <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">Register for a business tax account with IDOR. Required even if you don't collect sales tax. Handles your state income tax withholding if you have employees.</div>
            <a class="check-link" href="https://mytax.illinois.gov" target="_blank">→ MyTax Illinois</a>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Determine if you transport regulated medical specimens <span class="check-tag tag-tip">Key Decision</span></div>
            <div class="check-desc">If transporting non-emergency medical items (lab samples, pharmaceuticals, documents), you typically do NOT need an EMS license. If transporting patients or blood/organs for transplant, additional IDPH licensing applies.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Review Illinois Dept. of Public Health (IDPH) rules for your cargo <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">IDPH regulates transport of biological specimens, pharmaceuticals, and medical devices in Illinois. Confirm whether your specific cargo triggers licensing under the Illinois EMS Systems Act or IDPH rules.</div>
            <a class="check-link" href="https://dph.illinois.gov/topics-services/emergency-preparedness-response/ems.html" target="_blank">→ IDPH EMS Division</a>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Check if HIPAA compliance is required <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">If handling patient records or anything with protected health information (PHI), you are a HIPAA Business Associate. You'll need to sign Business Associate Agreements (BAAs) with healthcare clients and implement HIPAA safeguards.</div>
          </div>
        </div>
      </div>
    </div>

    <!-- SECTION 3 -->
    <div class="section courier" id="courier-sec-3">
      <div class="section-header" onclick="toggleSection('courier-sec-3')">
        <div class="section-num">3</div>
        <div class="section-title-group">
          <div class="section-title">Local Licenses & Permits</div>
          <div class="section-subtitle">City and county requirements where you operate</div>
        </div>
        <span class="section-mini-progress" id="courier-sec-3-prog">0/3</span>
        <span class="section-chevron">▼</span>
      </div>
      <div class="section-body">
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Obtain a City Business License <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">Most Illinois cities require a general business license. In Chicago, this is the Chicago Business License. Check with your specific city/village hall. Fees vary by location ($75–$400+/year).</div>
            <a class="check-link" href="https://www.chicago.gov/city/en/depts/bacp/sbc/business_licensing.html" target="_blank">→ Chicago Business License (if applicable)</a>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Register a DBA ("Doing Business As") if needed <span class="check-tag tag-optional">Optional</span></div>
            <div class="check-desc">If operating under a name different from your registered LLC name, file an Assumed Name Certificate with your county clerk. Cook County fee is ~$50.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Open a dedicated business bank account <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">Essential for LLC liability protection and clean accounting. Bring your EIN, LLC articles, and operating agreement. Many banks offer free small business checking.</div>
          </div>
        </div>
      </div>
    </div>

    <!-- SECTION 4 -->
    <div class="section courier" id="courier-sec-4">
      <div class="section-header" onclick="toggleSection('courier-sec-4')">
        <div class="section-num">4</div>
        <div class="section-title-group">
          <div class="section-title">Vehicles, Drivers & DOT Compliance</div>
          <div class="section-subtitle">Fleet, licensing, and federal transport requirements</div>
        </div>
        <span class="section-mini-progress" id="courier-sec-4-prog">0/5</span>
        <span class="section-chevron">▼</span>
      </div>
      <div class="section-body">
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Determine if you need a USDOT Number <span class="check-tag tag-required">Required if applicable</span></div>
            <div class="check-desc">Required if operating vehicles over 10,001 lbs, transporting hazardous materials, or crossing state lines for commercial purposes. Register free through FMCSA.</div>
            <a class="check-link" href="https://www.fmcsa.dot.gov/registration" target="_blank">→ FMCSA Registration</a>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Register vehicles commercially in Illinois <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">Vehicles used for business must be registered as commercial vehicles with the Illinois Secretary of State. Consider titling vehicles under the LLC name.</div>
            <a class="check-link" href="https://www.ilsos.gov/vehicles/" target="_blank">→ IL Vehicle Registration</a>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Verify driver qualifications and background checks <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">Drivers should have clean driving records. Run MVR (Motor Vehicle Record) checks and criminal background checks on all drivers — especially important for HIPAA-covered transport.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Establish chain-of-custody procedures for specimens <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">Labs and hospitals will require documented pickup/delivery logs, temperature control records, and tamper-evident packaging protocols. Create written SOPs before approaching clients.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">If transporting hazardous materials (HazMat): obtain proper training/placards <span class="check-tag tag-required">Required if applicable</span></div>
            <div class="check-desc">Biological specimens classified as Category A or B require HazMat training under DOT/IATA regulations (49 CFR). Contact IDOT or a certified HazMat trainer.</div>
          </div>
        </div>
      </div>
    </div>

    <!-- SECTION 5 -->
    <div class="section courier" id="courier-sec-5">
      <div class="section-header" onclick="toggleSection('courier-sec-5')">
        <div class="section-num">5</div>
        <div class="section-title-group">
          <div class="section-title">Insurance</div>
          <div class="section-subtitle">Protect your business, clients, and drivers</div>
        </div>
        <span class="section-mini-progress" id="courier-sec-5-prog">0/4</span>
        <span class="section-chevron">▼</span>
      </div>
      <div class="section-body">
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Commercial Auto Insurance <span class="check-tag tag-required">Required</span> <span class="check-tag tag-cost">Cost: $2,000–$8,000+/yr per vehicle</span></div>
            <div class="check-desc">Personal auto insurance does NOT cover commercial use. Get commercial auto coverage for each vehicle used. Minimum state liability: $25K/$50K/$20K, but get more for medical transport.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">General Liability Insurance <span class="check-tag tag-required">Required</span> <span class="check-tag tag-cost">Cost: $500–$2,000/yr</span></div>
            <div class="check-desc">Covers third-party bodily injury and property damage claims. Most healthcare clients will require at least $1M per occurrence before signing a contract with you.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Cargo / Bailee Insurance <span class="check-tag tag-required">Strongly Recommended</span></div>
            <div class="check-desc">Covers loss or damage to medical specimens, drugs, or equipment you're transporting. Clients may require this. Especially important if transporting high-value pharmaceuticals.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Workers' Compensation Insurance <span class="check-tag tag-required">Required if you have employees</span></div>
            <div class="check-desc">Illinois requires workers' comp for all employers with employees. Independent contractors may still require it depending on contract terms with healthcare clients.</div>
            <a class="check-link" href="https://www2.illinois.gov/sites/iwcc/Pages/default.aspx" target="_blank">→ IL Workers' Comp Commission</a>
          </div>
        </div>
      </div>
    </div>

    <!-- SECTION 6 -->
    <div class="section courier" id="courier-sec-6">
      <div class="section-header" onclick="toggleSection('courier-sec-6')">
        <div class="section-num">6</div>
        <div class="section-title-group">
          <div class="section-title">Launch & Get Clients</div>
          <div class="section-subtitle">Contracts, pricing, and finding your first accounts</div>
        </div>
        <span class="section-mini-progress" id="courier-sec-6-prog">0/4</span>
        <span class="section-chevron">▼</span>
      </div>
      <div class="section-body">
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Draft a Master Service Agreement (MSA) template <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">All clients should sign a contract covering: scope, liability limits, HIPAA BAA, chain-of-custody terms, payment terms, and insurance requirements. Have an attorney review it.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Set your pricing model <span class="check-tag tag-tip">Strategy</span></div>
            <div class="check-desc">Common models: per-route flat rate, per-mile, or monthly retainer. Research competitors in your area. Medical couriers typically charge $25–$75/run or $0.75–$1.50/mile depending on cargo type.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Target your first clients: labs, clinics, hospitals, pharmacies <span class="check-tag tag-tip">Growth</span></div>
            <div class="check-desc">Start with independent labs (Quest Diagnostics subs, local labs), medical clinics, urgent care centers, and long-term care pharmacies. Cold-call purchasing/operations managers — not front desk staff.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'courier')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content courier">
            <div class="check-title">Set up accounting and tracking software <span class="check-tag tag-tip">Operations</span></div>
            <div class="check-desc">Use QuickBooks or Wave for accounting. Use route tracking software (Onfleet, Routific, or Google Maps) to document delivery times and build your proof-of-delivery record — essential for client trust.</div>
          </div>
        </div>
      </div>
    </div>

    <div class="resources courier">
      <h3>🔗 Key Resources for Medical Courier</h3>
      <div class="resource-grid">
        <a class="resource-link" href="https://www.ilsos.gov/departments/business_services/home.html" target="_blank"><span>🏛️</span> IL Secretary of State</a>
        <a class="resource-link" href="https://dph.illinois.gov" target="_blank"><span>🏥</span> IL Dept. of Public Health</a>
        <a class="resource-link" href="https://www.fmcsa.dot.gov/registration" target="_blank"><span>🚛</span> FMCSA / DOT Registration</a>
        <a class="resource-link" href="https://mytax.illinois.gov" target="_blank"><span>💰</span> MyTax Illinois</a>
        <a class="resource-link" href="https://www.hhs.gov/hipaa/for-professionals/covered-entities/index.html" target="_blank"><span>🔒</span> HIPAA Business Associates</a>
        <a class="resource-link" href="https://www2.illinois.gov/dceo/SmallBizAssistance/Pages/default.aspx" target="_blank"><span>📋</span> IL DCEO Small Business</a>
      </div>
    </div>

    <div class="notes-box">
      <h3>📝 Your Notes</h3>
      <textarea id="courier-notes" placeholder="Track contacts, questions, important dates, attorney info..." oninput="saveNotes('courier')"></textarea>
    </div>

  </div><!-- end courier panel -->


  <!-- ======== CHARCUTERIE CART ======== -->
  <div class="tab-panel charcuterie" id="panel-charcuterie">

    <div class="disclaimer">
      <strong>⚠️ Disclaimer:</strong> This guide is for informational purposes only and is not legal or regulatory advice. Food business requirements vary significantly by county and municipality in Illinois — always verify with your local health department and city hall.
    </div>

    <div class="progress-card charcuterie">
      <div class="progress-info">
        <div class="progress-label">Your Progress</div>
        <div class="progress-bar-track">
          <div class="progress-bar-fill" id="charcuterie-bar" style="width:0%"></div>
        </div>
        <div style="font-size:12px;color:var(--gray-500);margin-top:4px;" id="charcuterie-pct">0% complete</div>
      </div>
      <div style="text-align:center;">
        <div class="progress-fraction" id="charcuterie-frac">0/0</div>
        <div class="progress-sublabel">steps done</div>
      </div>
      <button class="reset-btn" onclick="resetTab('charcuterie')">Reset</button>
    </div>

    <!-- SECTION 1 -->
    <div class="section charcuterie" id="charcuterie-sec-1">
      <div class="section-header" onclick="toggleSection('charcuterie-sec-1')">
        <div class="section-num">1</div>
        <div class="section-title-group">
          <div class="section-title">Business Formation</div>
          <div class="section-subtitle">Register your legal entity and get your EIN</div>
        </div>
        <span class="section-mini-progress" id="charcuterie-sec-1-prog">0/3</span>
        <span class="section-chevron">▼</span>
      </div>
      <div class="section-body">
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Choose a business structure <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">An LLC is the most common choice for food cart businesses — it separates your personal assets from the business. Sole proprietor is simplest but offers no liability protection.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Register with the Illinois Secretary of State <span class="check-tag tag-required">Required</span> <span class="check-tag tag-cost">Cost: $150 (LLC)</span></div>
            <div class="check-desc">File Articles of Organization online. Your LLC name must be unique in Illinois. Designate a registered agent with an Illinois street address.</div>
            <a class="check-link" href="https://www.ilsos.gov/departments/business_services/home.html" target="_blank">→ IL Secretary of State</a>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Obtain Federal EIN from the IRS <span class="check-tag tag-required">Required</span> <span class="check-tag tag-cost">Free</span></div>
            <div class="check-desc">Apply online at IRS.gov — free and instant. Needed for business bank accounts, taxes, and hiring employees.</div>
            <a class="check-link" href="https://www.irs.gov/businesses/small-businesses-self-employed/apply-for-an-employer-identification-number-ein-online" target="_blank">→ IRS EIN Application</a>
          </div>
        </div>
      </div>
    </div>

    <!-- SECTION 2 -->
    <div class="section charcuterie" id="charcuterie-sec-2">
      <div class="section-header" onclick="toggleSection('charcuterie-sec-2')">
        <div class="section-num">2</div>
        <div class="section-title-group">
          <div class="section-title">Food Safety Licensing (IDPH & Local Health Dept)</div>
          <div class="section-subtitle">The most critical step — food businesses are heavily regulated</div>
        </div>
        <span class="section-mini-progress" id="charcuterie-sec-2-prog">0/5</span>
        <span class="section-chevron">▼</span>
      </div>
      <div class="section-body">
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Obtain a Food Service Sanitation Manager Certificate <span class="check-tag tag-required">Required</span> <span class="check-tag tag-cost">Cost: ~$150–$200</span></div>
            <div class="check-desc">Illinois requires at least one person in your operation to hold a certified food manager credential (e.g., ServSafe Manager Certification). You must pass an exam. Valid for 5 years.</div>
            <a class="check-link" href="https://www.servsafe.com/servsafe-manager" target="_blank">→ ServSafe Certification</a>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Apply for a Retail Food Establishment License from your local health department <span class="check-tag tag-required">Required</span> <span class="check-tag tag-cost">Cost: $100–$300+/yr</span></div>
            <div class="check-desc">Every county/city in Illinois has its own health department that licenses food businesses. Contact your specific county health department — this is NOT a state-level application. Expect an inspection before approval.</div>
            <a class="check-link" href="https://dph.illinois.gov/topics-services/environmental-health/food.html" target="_blank">→ IDPH Food Division</a>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Determine if you qualify as a Cottage Food business <span class="check-tag tag-tip">Important Decision</span></div>
            <div class="check-desc">Illinois Cottage Food Law allows home kitchen production of certain non-hazardous foods (jams, baked goods) with up to $50K/year in sales — but charcuterie with meats and cheeses typically does NOT qualify due to temperature control requirements. Verify with your county health dept.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Secure a licensed commercial kitchen for food prep <span class="check-tag tag-required">Almost Always Required</span></div>
            <div class="check-desc">Because charcuterie involves TCS (Temperature Control for Safety) foods like meats and cheeses, you'll almost certainly need to prep in a licensed commercial kitchen. Rent commissary kitchen space ($15–$30/hr) or partner with a local restaurant. Health depts will ask for your commissary agreement.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Pass your health department cart inspection <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">Your cart/booth will be physically inspected before you're licensed. Requirements typically include: handwashing station, food thermometers, covered cold storage, sneeze guards, and proper labeling. Get the inspection checklist from your local health dept before purchasing equipment.</div>
          </div>
        </div>
      </div>
    </div>

    <!-- SECTION 3 -->
    <div class="section charcuterie" id="charcuterie-sec-3">
      <div class="section-header" onclick="toggleSection('charcuterie-sec-3')">
        <div class="section-num">3</div>
        <div class="section-title-group">
          <div class="section-title">Local Permits & Vendor Licensing</div>
          <div class="section-subtitle">City and event-specific permits for your cart</div>
        </div>
        <span class="section-mini-progress" id="charcuterie-sec-3-prog">0/4</span>
        <span class="section-chevron">▼</span>
      </div>
      <div class="section-body">
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Obtain a City Business License <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">Most Illinois cities require a general business license. If you're in Chicago, look into the Peddler's License or Mobile Food Vendor License depending on your setup. Check with your specific city hall.</div>
            <a class="check-link" href="https://www.chicago.gov/city/en/depts/bacp/sbc/business_licensing.html" target="_blank">→ Chicago Mobile Food License</a>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Understand where you can legally vend <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">Selling on public property (parks, sidewalks, streets) requires permits from your park district or city. Private events and private property may require permission from the property owner. Some cities restrict cart locations to specific zones.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Register with Illinois Department of Revenue for sales tax <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">Food sold for immediate consumption (at events/markets) is generally taxable in Illinois. Register with IDOR to collect and remit sales tax. Illinois state rate is 6.25%; local rates vary.</div>
            <a class="check-link" href="https://mytax.illinois.gov" target="_blank">→ MyTax Illinois</a>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Apply for Temporary Food Establishment permits for events <span class="check-tag tag-required">Required per event</span></div>
            <div class="check-desc">For each farmers market, festival, or pop-up event, you may need a Temporary Food Service Establishment permit from the local health dept. Some vendors prefer getting a permanent mobile vendor license to simplify this. Apply at least 2–3 weeks before each event.</div>
          </div>
        </div>
      </div>
    </div>

    <!-- SECTION 4 -->
    <div class="section charcuterie" id="charcuterie-sec-4">
      <div class="section-header" onclick="toggleSection('charcuterie-sec-4')">
        <div class="section-num">4</div>
        <div class="section-title-group">
          <div class="section-title">Equipment, Labeling & Food Safety</div>
          <div class="section-subtitle">Physical requirements and safe food handling</div>
        </div>
        <span class="section-mini-progress" id="charcuterie-sec-4-prog">0/4</span>
        <span class="section-chevron">▼</span>
      </div>
      <div class="section-body">
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Purchase compliant cart/display equipment <span class="check-tag tag-cost">Cost: $500–$3,000+</span></div>
            <div class="check-desc">Must include: refrigeration to keep meats/cheeses at or below 41°F, a portable handwashing station with soap/water/paper towels, food-grade display surfaces, and sneeze guards if required by your health dept.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Implement proper allergen labeling <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">Illinois requires allergen labeling for packaged food. Even for served-to-order boards, be prepared to disclose the "Big 9" allergens (dairy, eggs, fish, shellfish, tree nuts, peanuts, wheat, soybeans, sesame) verbally or on signage.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Source from licensed food suppliers <span class="check-tag tag-required">Required</span></div>
            <div class="check-desc">All meats, cheeses, and other ingredients must come from licensed, inspected sources. Keep supplier invoices on file — health inspectors may ask for them. Avoid sourcing from farmers markets or unlicensed producers.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Create a food safety plan / HACCP documentation <span class="check-tag tag-tip">Recommended</span></div>
            <div class="check-desc">Document temperature logs, cleaning schedules, supplier records, and food handling procedures. Even if not required at your scale, this protects you in case of a complaint and demonstrates professionalism.</div>
          </div>
        </div>
      </div>
    </div>

    <!-- SECTION 5 -->
    <div class="section charcuterie" id="charcuterie-sec-5">
      <div class="section-header" onclick="toggleSection('charcuterie-sec-5')">
        <div class="section-num">5</div>
        <div class="section-title-group">
          <div class="section-title">Insurance</div>
          <div class="section-subtitle">Protect yourself at events and beyond</div>
        </div>
        <span class="section-mini-progress" id="charcuterie-sec-5-prog">0/3</span>
        <span class="section-chevron">▼</span>
      </div>
      <div class="section-body">
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">General Liability Insurance <span class="check-tag tag-required">Required by most venues</span> <span class="check-tag tag-cost">Cost: $500–$1,200/yr</span></div>
            <div class="check-desc">Covers customer injury (slip/fall, allergic reaction) and property damage claims. Most farmers markets, festivals, and event venues will require at least $1M coverage and may need to be listed as "additionally insured."</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Product Liability Insurance <span class="check-tag tag-required">Strongly Recommended</span></div>
            <div class="check-desc">Specifically covers claims arising from food you sell causing illness or injury. Often included in General Liability for food businesses — verify with your insurer. Critical for a food product business.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Commercial Auto Insurance (if driving cart to events) <span class="check-tag tag-required">Required if applicable</span></div>
            <div class="check-desc">If you're towing or transporting your cart setup with a vehicle for business purposes, your personal auto policy won't cover it. Get a commercial auto endorsement or separate policy.</div>
          </div>
        </div>
      </div>
    </div>

    <!-- SECTION 6 -->
    <div class="section charcuterie" id="charcuterie-sec-6">
      <div class="section-header" onclick="toggleSection('charcuterie-sec-6')">
        <div class="section-num">6</div>
        <div class="section-title-group">
          <div class="section-title">Launch: Markets, Events & Sales Channels</div>
          <div class="section-subtitle">Finding your first customers and revenue streams</div>
        </div>
        <span class="section-mini-progress" id="charcuterie-sec-6-prog">0/4</span>
        <span class="section-chevron">▼</span>
      </div>
      <div class="section-body">
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Apply to local farmers markets <span class="check-tag tag-tip">Revenue Channel</span></div>
            <div class="check-desc">Illinois has hundreds of farmers markets. Apply to 2–3 markets for your first season. Markets often have waiting lists, so apply early. Typical booth fees: $25–$150/day. Great for recurring weekly revenue and building a following.</div>
            <a class="check-link" href="https://www.ilfarmersmarkets.org" target="_blank">→ IL Farmers Markets Directory</a>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Market catering/grazing boards for private events <span class="check-tag tag-tip">High-Margin Channel</span></div>
            <div class="check-desc">Corporate events, weddings, bridal showers, and birthday parties are extremely lucrative for charcuterie. A catered board can run $15–$30 per person. Partner with event planners and wedding venues for referrals.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Build your Instagram / social media presence <span class="check-tag tag-tip">Marketing</span></div>
            <div class="check-desc">Charcuterie is extremely visual — Instagram and TikTok are your best marketing tools. Start posting setup photos, finished boards, and behind-the-scenes content before you launch. Reach out to local food bloggers for a feature.</div>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this,'charcuterie')">
          <div class="check-box"><span class="check-box-inner">✓</span></div>
          <div class="check-content charcuterie">
            <div class="check-title">Set up a simple booking/order system <span class="check-tag tag-tip">Operations</span></div>
            <div class="check-desc">Use Square, Stripe, or a simple website (Squarespace/Wix) to take online orders and deposits. Require a 50% deposit for all custom orders. Track expenses and revenue from day one with free tools like Wave or QuickBooks Simple Start.</div>
          </div>
        </div>
      </div>
    </div>

    <div class="resources charcuterie">
      <h3>🔗 Key Resources for Charcuterie Cart</h3>
      <div class="resource-grid">
        <a class="resource-link" href="https://dph.illinois.gov/topics-services/environmental-health/food.html" target="_blank"><span>🍽️</span> IDPH Food Division</a>
        <a class="resource-link" href="https://www.ilsos.gov/departments/business_services/home.html" target="_blank"><span>🏛️</span> IL Secretary of State</a>
        <a class="resource-link" href="https://mytax.illinois.gov" target="_blank"><span>💰</span> MyTax Illinois (Sales Tax)</a>
        <a class="resource-link" href="https://www.servsafe.com/servsafe-manager" target="_blank"><span>📜</span> ServSafe Manager Cert</a>
        <a class="resource-link" href="https://www.ilfarmersmarkets.org" target="_blank"><span>🌽</span> IL Farmers Markets</a>
        <a class="resource-link" href="https://www2.illinois.gov/dceo/SmallBizAssistance/Pages/default.aspx" target="_blank"><span>📋</span> IL DCEO Small Business</a>
      </div>
    </div>

    <div class="notes-box">
      <h3>📝 Your Notes</h3>
      <textarea id="charcuterie-notes" placeholder="Health dept contact info, market names, commissary kitchen leads, event ideas..." oninput="saveNotes('charcuterie')"></textarea>
    </div>

  </div><!-- end charcuterie panel -->

</main>

<script>
  // ---- STATE ----
  const state = {
    courier: {},
    charcuterie: {}
  };

  const sections = {
    courier: ['courier-sec-1','courier-sec-2','courier-sec-3','courier-sec-4','courier-sec-5','courier-sec-6'],
    charcuterie: ['charcuterie-sec-1','charcuterie-sec-2','charcuterie-sec-3','charcuterie-sec-4','charcuterie-sec-5','charcuterie-sec-6']
  };

  // ---- TABS ----
  function switchTab(tab) {
    document.querySelectorAll('.tab-panel').forEach(p => p.classList.remove('active'));
    document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
    document.getElementById('panel-' + tab).classList.add('active');
    document.getElementById('tab-' + tab).classList.add('active');
  }

  // ---- ACCORDION ----
  function toggleSection(secId) {
    const header = document.querySelector('#' + secId + ' .section-header');
    const body = document.querySelector('#' + secId + ' .section-body');
    if (!body) return;
    const isCollapsed = header.classList.contains('collapsed');
    if (isCollapsed) {
      header.classList.remove('collapsed');
      body.style.display = '';
    } else {
      header.classList.add('collapsed');
      body.style.display = 'none';
    }
  }

  // ---- CHECKLIST ----
  function toggleCheck(item, tab) {
    item.classList.toggle('checked');
    updateProgress(tab);
  }

  function updateProgress(tab) {
    const panel = document.getElementById('panel-' + tab);
    const allItems = panel.querySelectorAll('.check-item');
    const checkedItems = panel.querySelectorAll('.check-item.checked');
    const total = allItems.length;
    const done = checkedItems.length;
    const pct = total > 0 ? Math.round((done / total) * 100) : 0;

    document.getElementById(tab + '-bar').style.width = pct + '%';
    document.getElementById(tab + '-pct').textContent = pct + '% complete';
    document.getElementById(tab + '-frac').textContent = done + '/' + total;

    // Update section mini-progress
    sections[tab].forEach(secId => {
      const secEl = document.getElementById(secId);
      if (!secEl) return;
      const secItems = secEl.querySelectorAll('.check-item');
      const secDone = secEl.querySelectorAll('.check-item.checked');
      const progEl = document.getElementById(secId + '-prog');
      if (progEl) {
        progEl.textContent = secDone.length + '/' + secItems.length;
        progEl.classList.toggle('done', secDone.length === secItems.length && secItems.length > 0);
      }
    });
  }

  function resetTab(tab) {
    if (!confirm('Reset all progress for this business checklist?')) return;
    const panel = document.getElementById('panel-' + tab);
    panel.querySelectorAll('.check-item').forEach(item => item.classList.remove('checked'));
    updateProgress(tab);
  }

  // ---- NOTES (session only) ----
  function saveNotes(tab) {
    // Notes exist for the session in the textarea - no localStorage needed
  }

  // ---- INIT ----
  updateProgress('courier');
  updateProgress('charcuterie');
</script>
</body>
</html>
