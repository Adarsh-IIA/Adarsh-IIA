<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Compliance Due Diligence - Partner, Equity, Acquire -2025-26</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f2f2;
      margin: 0;
      padding: 20px;
    }
    h1 {
      text-align: center;
      color: #333;
    }
    .company-container {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: center;
    }
    .company-card {
      background: #fff;
      border-radius: 10px;
      padding: 20px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      width: 300px;
      cursor: pointer;
    }
    .company-card h2 {
      font-size: 18px;
      margin: 0 0 10px;
      color: #0056b3;
      text-decoration: underline;
    }
    .company-card p {
      margin: 5px 0;
    }
    .company-details {
      display: none;
      background-color: #fff;
      border-radius: 10px;
      padding: 20px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      margin-top: 20px;
    }
    .close-btn {
      background-color: #ff6347;
      color: white;
      border: none;
      padding: 10px;
      cursor: pointer;
      border-radius: 5px;
    }
    .close-btn:hover {
      background-color: #ff4500;
    }
  </style>
</head>
<body>

<h1>Compliance Due Diligence - Partner, Equity, Acquire -2025-26</h1>

<!-- Company List Section -->
<div class="company-container" id="companyList">
  <!-- Cards will be injected dynamically using JavaScript -->
</div>

<!-- Company Details Section -->
<div class="company-details" id="companyDetails">
  <button class="close-btn" onclick="closeDetails()">Close</button>
  <h2 id="companyName"></h2>
  <p><strong>Status:</strong> <span id="companyStatus"></span></p>
  <p><strong>Date of Incorporation:</strong> <span id="companyIncorporationDate"></span></p>
  <p><strong>Address:</strong> <span id="companyAddress"></span></p>
  <p><strong>Director Name:</strong> <span id="companyDirector"></span></p>
  <p><strong>Area:</strong> <span id="companyArea"></span></p>
  <p><strong>Authorised Capital:</strong> <span id="companyAuthorisedCapital"></span></p>
  <p><strong>Paid up Capital:</strong> <span id="companyPaidUpCapital"></span></p>
  <p><strong>Listing Status:</strong> <span id="companyListingStatus"></span></p>
  <p><strong>Date of Last Annual General Meeting:</strong> <span id="companyAGMDate"></span></p>
  <p><strong>Date of Latest Balance Sheet:</strong> <span id="companyBalanceSheetDate"></span></p>
  <p><strong>Email ID:</strong> <span id="companyEmail"></span></p>
  <p><strong>Website:</strong> <a href="#" id="companyWebsite" target="_blank"></a></p>
  <p><strong>Number of Employees:</strong> <span id="companyEmployees"></span></p>
  <p><strong>Reviews - Rate:</strong> <span id="companyReviewsRate"></span></p>
  <p><strong>CIN:</strong> <span id="companyCIN"></span></p>
  <p><strong>Charges:</strong> <span id="companyCharges"></span></p>
  <p><strong>Top Employees:</strong> <span id="companyTopEmployees"></span></p>
</div>

<script>
  // Example company data with all additional details
  const companies = [
    {
      name: 'ALIGNMINDS TECHNOLOGIES PRIVATE LIMITED',
      status: 'Active',
      incorporationDate: '22/05/2009',
      address: 'XIV/239-A9, 5TH FLOOR, ASSET IRIS MAIN ROAD, NORTH FORT GATE, TRIPUNITHURA, Kerala, India, 682301',
      director: 'DEVANARAYANAN GOPAKUMAR KRISHNAGOPALAN',
      area: 'Product Engineering, Cloud & DevOps, AI',
      authorisedCapital: '20,00,000',
      paidUpCapital: '20,00,000',
      listingStatus: 'Active',
      AGMDate: '30/09/2024',
      balanceSheetDate: '31/03/2024',
      email: 'info@alignminds.com',
      website: 'https://alignminds.com',
      employees: '51-200',
      reviewsRate: '4.4',
      CIN: 'U72200KL2009PTC024209',
      charges: 'KOTAK MAHINDRA BANK LIMITED, Amount - 25,00,000',
      topEmployees: 'Pradeep Kumar - Senior Technology Lead'
    },
    {
      name: 'IPIX TECH SERVICES PRIVATE LIMITED',
      status: 'Active',
      incorporationDate: '27/12/2007',
      address: 'KSITIL Special Economic Zone, 1st Floor, Sahya Building Govt Cyber Park, Nellikode, PO, Kozhikode, Kerala 673016',
      director: 'RAJU MENON, ETTUVEETTIL MADHAVA MENON UNNIKRISHNAN',
      area: 'Web App Development, E-Commerce, UI/UX Design',
      authorisedCapital: '10,00,000',
      paidUpCapital: '10,00,000',
      listingStatus: 'Not Listed',
      AGMDate: '30/11/2024',
      balanceSheetDate: 'NIL',
      email: 'info@ipixtechnologies.com',
      website: 'https://www.ipixtechnologies.com',
      employees: '51-200',
      reviewsRate: '4.6',
      CIN: 'U72900KL2007PTC021606',
      charges: 'None',
      topEmployees: 'Kavitha Gopan, Jishnu B'
    },
{
        name: "MOVYTECH INNOVATIONS PRIVATE LIMITED",
        status: "Active",
        incorporation: "31/07/2023",
        address: "CDAC Building, Technpark Phase 1, Thiruvananthapuram, 695581",
        directors: ["HAFEEZ ABDUL HASHIM", "AKHIL ANILKUMAR PRAJITHA"],
        area: "Python, Flutter, Go, .NET",
        capital: "10,00,000",
        paidUp: "Not Specified",
        listing: "NO",
        agmDate: "",
        balanceSheet: "",
        email: "hello@movytech.com",
        website: "https://movytech.co/",
        employees: "11-50 employees",
        rating: "4.6",
        cin: "U63999KL2023PTC082739",
        charges: "",
        topEmployees: ["Jishnu B", "Hafeez Abdul Ha"]
      },
      {
        name: "NXTGENIX SOLUTIONS PRIVATE LIMITED",
        status: "Active",
        incorporation: "09/09/2021",
        address: "STPI Building, Technopark, Trivandrum - 695581",
        directors: ["SADANANDAN SAJAN", "SURENDRAN LAL KRISHNA", "SULOCHANABAI JUSTUS HELEN"],
        area: "UI/UX Design, Webflow Development",
        capital: "Not Available",
        paidUp: "Not Available",
        listing: "NO",
        agmDate: "",
        balanceSheet: "",
        email: "s.sajan615@gmail.com",
        website: "https://www.nxtgenix.design/",
        employees: "2-10 employees",
        rating: "",
        cin: "U72900KL2021PTC070815",
        charges: "",
        topEmployees: ["Akhil AP", "Sajan S Nandan"]
      },
      {
        name: "BZANALYTICS PRIVATE LIMITED",
        status: "Active",
        incorporation: "14/05/2021",
        address: "PERUNGUZHY , CHIRAYINKEEZHU, Kerala, India - 695304.",
        directors: ["SULTHANA SHAFI", "SUBUHAN SHAFI"],
        area: "Artificial Intelligence",
        capital: "Not Available",
        paidUp: "Not Available",
        listing: "NO",
        agmDate: "",
        balanceSheet: "",
        email: "sulthanashf91@gmail.com",
        website: "https://www.bzanalytics.ai/",
        employees: "11-50 employees",
        rating: "",
        cin: "U72900KL2021PTC068996",
        charges: "",
        topEmployees: ["Sulthana Shafi"]
      },
      {
        name: "XMINDS INFOTECH PRIVATE LIMITED",
        status: "Active",
        incorporation: "07/10/2006",
        address: "TC 42/23-2, MANGALAVILA, JAGATHY, Trivandrum, 695014",
        directors: ["RAMGOVIND NARAYAN", "JAYAKRISHNAN SUKUMARAN NAIR", "SANJITH KRISHNAKUMARAN NAIR SUDAMONY"],
        area: "Metaverse, Blockchain, Cloud, Data Solutions",
        capital: "Not Available",
        paidUp: "Not Available",
        listing: "No",
        agmDate: "",
        balanceSheet: "",
        email: "finance@xminds.com",
        website: "https://www.xminds.com",
        employees: "51-200 employees",
        rating: "",
        cin: "U72200KL2006PTC019607",
        charges: "",
        topEmployees: ["Shahanas S", "Renjith Kumar"]
      },
      {
        name: "WEFT TECHNOLOGIES (OPC) PRIVATE LIMITED",
        status: "Active",
        incorporation: "10/04/2018",
        address: "65, ELAVANAPARAMBIL HOUSE, CHERUVALOOR, KORATTY, Kerala, 680321",
        directors: ["NIDHIN RAVI"],
        area: "Web & App Development, DevOps, SaaS, QA",
        capital: "Not Available",
        paidUp: "Not Available",
        listing: "No",
        agmDate: "",
        balanceSheet: "",
        email: "nidhin@wefttechnologies.com",
        website: "",
        employees: "51-200 employees",
        rating: "",
        cin: "U72900KL2018OPC052844",
        charges: "",
        topEmployees: ["Nikhil Ravi"]
      },
      {
        name: "LIVARES TECHNOLOGIES",
        status: "Active",
        incorporation: "07/11/2012",
        address: "MODULE NOS. 2501 (B) & (C) YAMUNA BUILDING, TECHNOPARK PHASE III , TRIVANDRUM, Kerala - 695581",
        directors: ["JASEEL ABDUL RAFEEK", "RINEEZ AHMED NAZEEMUDEEN"],
        area: "IOT, RPA, DevOps, Analytics",
        capital: "50,00,000",
        paidUp: "50,00,000",
        listing: "No",
        agmDate: "30/09/2023",
        balanceSheet: "30/09/2023",
        email: "email@gspco.in",
        website: "http://www.livares.com",
        employees: "11-50 employees",
        rating: "",
        cin: "U72200KL2012PTC032569",
        charges: "Yes",
        topEmployees: ["Rineez Ahmed N", "Sumesh Ramachandran Nair"]
      },
      {
        name: "SCIPY TECHNOLOGIES",
        status: "Active",
        incorporation: "",
        address: "TC 26/981, First floor, Plammoodu - PMG Road, TVM - 04, Kerala 695033",
        directors: [],
        area: "Web & Mobile Development, AI, ERP, Branding",
        capital: "Not Available",
        paidUp: "Not Available",
        listing: "No",
        agmDate: "",
        balanceSheet: "",
        email: "email@gspco.in",
        website: "https://www.scipytechnologies.com/",
        employees: "11-50 employees",
        rating: "",
        cin: "",
        charges: "",
        topEmployees: ["Ashtamy Rahul", "Rahul Bose CP"]
      }
    // Add more companies here...
  ];

  // Load company cards
  function loadCompanies() {
    const companyList = document.getElementById('companyList');
    companyList.innerHTML = '';  // Clear current list

    companies.forEach((company, index) => {
      const companyCard = document.createElement('div');
      companyCard.classList.add('company-card');
      companyCard.onclick = () => showCompanyDetails(index);
      companyCard.innerHTML = `
        <h2>${company.name}</h2>
        <p><strong>Status:</strong> ${company.status}</p>
        <p><strong>Employees:</strong> ${company.employees}</p>
      `;
      companyList.appendChild(companyCard);
    });
  }

  // Show company details
  function showCompanyDetails(index) {
    const company = companies[index];
    document.getElementById('companyName').innerText = company.name;
    document.getElementById('companyStatus').innerText = company.status;
    document.getElementById('companyIncorporationDate').innerText = company.incorporationDate;
    document.getElementById('companyAddress').innerText = company.address;
    document.getElementById('companyDirector').innerText = company.director;
    document.getElementById('companyArea').innerText = company.area;
    document.getElementById('companyAuthorisedCapital').innerText = company.authorisedCapital;
    document.getElementById('companyPaidUpCapital').innerText = company.paidUpCapital;
    document.getElementById('companyListingStatus').innerText = company.listingStatus;
    document.getElementById('companyAGMDate').innerText = company.AGMDate;
    document.getElementById('companyBalanceSheetDate').innerText = company.balanceSheetDate;
    document.getElementById('companyEmail').innerText = company.email;
    document.getElementById('companyWebsite').innerText = company.website;
    document.getElementById('companyWebsite').href = company.website;
    document.getElementById('companyEmployees').innerText = company.employees;
    document.getElementById('companyReviewsRate').innerText = company.reviewsRate;
    document.getElementById('companyCIN').innerText = company.CIN;
    document.getElementById('companyCharges').innerText = company.charges;
    document.getElementById('companyTopEmployees').innerText = company.topEmployees;

    // Show the details section
    document.getElementById('companyDetails').style.display = 'block';
  }

  // Close company details
  function closeDetails() {
    document.getElementById('companyDetails').style.display = 'none';
  }

  // Load companies on page load
  window.onload = loadCompanies;
</script>

</body>
</html>
