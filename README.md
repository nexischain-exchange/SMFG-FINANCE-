# SMFG-FINANCE-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Instant Application Form</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: #ffffff;
      color: #14231c;
      padding: 12px;
    }

    .application-card {
      width: 100%;
      max-width: 1100px;
      margin: 0 auto;
      padding: 70px 95px;
      border: 2px solid #e1e7e3;
      border-radius: 38px;
      background: #ffffff;
      box-shadow: 0 8px 35px rgba(0, 0, 0, 0.035);
    }

    .form-header h1 {
      color: #003b27;
      font-size: clamp(30px, 4vw, 48px);
      font-weight: 750;
      line-height: 1.25;
      margin-bottom: 32px;
    }

    .form-header p {
      color: #484f4b;
      font-size: clamp(18px, 2.5vw, 30px);
      line-height: 1.7;
      margin-bottom: 80px;
    }

    .form-group {
      display: flex;
      flex-direction: column;
      min-width: 0;
    }

    .form-group.full-width {
      grid-column: 1 / -1;
    }

    .form-group label {
      display: block;
      font-size: clamp(18px, 2.3vw, 27px);
      font-weight: 700;
      margin-bottom: 28px;
      color: #17211b;
    }

    .form-group input,
    .form-group select {
      width: 100%;
      height: 90px;
      padding: 0 30px;
      border: 3px solid #e0e6e2;
      border-radius: 20px;
      background: #fff;
      color: #171d19;
      font: inherit;
      font-size: clamp(18px, 2.4vw, 28px);
      outline: none;
      transition: border-color 0.2s, box-shadow 0.2s;
    }

    .form-group input::placeholder {
      color: #a8aaa9;
      opacity: 1;
    }

    .form-group input:focus,
    .form-group select:focus {
      border-color: #00452e;
      box-shadow: 0 0 0 4px rgba(0, 69, 46, 0.08);
    }

    .form-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      column-gap: 42px;
      row-gap: 62px;
    }

    .submit-button {
      width: 100%;
      min-height: 130px;
      margin-top: 84px;
      padding: 25px;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 30px;
      background: #003b27;
      color: #ffffff;
      border: none;
      border-radius: 21px;
      font-size: clamp(20px, 2.5vw, 30px);
      font-weight: 700;
      cursor: pointer;
      box-shadow: 0 12px 28px rgba(0, 45, 29, 0.14);
      transition: background 0.2s, transform 0.2s;
    }

    .submit-button:hover {
      background: #005238;
      transform: translateY(-2px);
    }

    .submit-button:active {
      transform: translateY(0);
    }

    .arrow {
      font-size: 38px;
      font-weight: 400;
      line-height: 1;
    }

    .message {
      display: none;
      margin-top: 24px;
      padding: 18px;
      border-radius: 12px;
      font-size: 16px;
      line-height: 1.6;
    }

    .message.error {
      display: block;
      color: #842029;
      background: #f8d7da;
    }

    .message.success {
      display: block;
      color: #0f5132;
      background: #d1e7dd;
    }

    @media (max-width: 700px) {
      body {
        padding: 10px;
      }

      .application-card {
        padding: 35px 22px;
        border-radius: 24px;
      }

      .form-header h1 {
        margin-bottom: 18px;
      }

      .form-header p {
        margin-bottom: 40px;
        line-height: 1.55;
      }

      .form-group label {
        margin-bottom: 12px;
        font-size: 16px;
      }

      .form-grid {
        column-gap: 14px;
        row-gap: 28px;
      }

      .form-group input,
      .form-group select {
        height: 58px;
        padding: 0 12px;
        border-width: 2px;
        border-radius: 12px;
        font-size: 15px;
      }

      .submit-button {
        min-height: 70px;
        margin-top: 40px;
        padding: 16px 10px;
        gap: 12px;
        border-radius: 13px;
        font-size: 16px;
      }

      .arrow {
        font-size: 25px;
      }
    }

    @media (max-width: 380px) {
      .application-card {
        padding: 28px 16px;
      }

      .form-grid {
        grid-template-columns: 1fr;
        row-gap: 22px;
      }

      .form-group.full-width {
        grid-column: auto;
      }

      .form-header p {
        font-size: 17px;
      }

      .submit-button {
        font-size: 15px;
      }
    }
  </style>
</head>

<body>

  <main class="application-card">

    <header class="form-header">
      <h1>Instant Application Form</h1>

      <p>
        Check your pre-approved credit limit without
        affecting your credit score.
      </p>
    </header>

    <form id="loanForm">

      <div class="form-grid">

        <div class="form-group full-width">
          <label for="fullName">Full Legal Name</label>
          <input
            type="text"
            id="fullName"
            name="fullName"
            placeholder="e.g. Rajesh Kumar"
            autocomplete="name"
            required
            minlength="2"
          >
        </div>

        <div class="form-group">
          <label for="email">Email Address</label>
          <input
            type="email"
            id="email"
            name="email"
            placeholder="rajesh@example.com"
            autocomplete="email"
            required
          >
        </div>

        <div class="form-group">
          <label for="phone">Phone Number</label>
          <input
            type="tel"
            id="phone"
            name="phone"
            placeholder="+91 98765 43210"
            autocomplete="tel"
            pattern="[+]?[0-9 ()-]{10,18}"
            title="Enter a valid phone number"
            required
          >
        </div>

        <div class="form-group">
          <label for="employment">Employment Type</label>
          <select id="employment" name="employment" required>
            <option value="salaried">Salaried Employee</option>
            <option value="self-employed">Self-Employed</option>
            <option value="business">Business Owner</option>
            <option value="professional">Professional</option>
            <option value="other">Other</option>
          </select>
        </div>

        <div class="form-group">
          <label for="loanAmount">Requested Loan (₹)</label>
          <input
            type="number"
            id="loanAmount"
            name="loanAmount"
            value="250000"
            min="1000"
            max="10000000"
            step="1000"
            required
          >
        </div>

      </div>

      <button type="submit" class="submit-button">
        <span>Get Pre-Approved Loan Offer</span>
        <span class="arrow" aria-hidden="true">→</span>
      </button>

      <div id="formMessage" class="message" role="status" aria-live="polite"></div>

    </form>

  </main>

  <script>
    const loanForm = document.getElementById("loanForm");
    const formMessage = document.getElementById("formMessage");

    loanForm.addEventListener("submit", function (event) {
      event.preventDefault();

      if (!loanForm.checkValidity()) {
        loanForm.reportValidity();
        return;
      }

      formMessage.className = "message success";
      formMessage.textContent =
        "Your form is valid. Connect a secure backend to submit your application and check eligibility.";
    });
  </script>

</body>
</html>