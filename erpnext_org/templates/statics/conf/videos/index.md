# ERPNext Conf 2014 Videos

{% set erpnext = [{
		"label": "Rushabh Mehta",
		"name": "rushabh-mehta",
		"text": "ERPNext founder, Rushabh Mehta introduces ERPNext explains the key themes that drives ERPNext as a product - ERPnext is Open, Mobile and Connected."},
	{
		"label": "Nabin Hait",
		"name": "nabin-hait",
		"text": "ERPNext Core Developer, Nabin Hait shares the journey of ERPNext from a developer of custom software to an open source product company. Nabin covers the major strategic and architectural changes in ERPNext as it has evolved into a modern web application."
	},
	{
		"label": "Anand Doshi",
		"name": "anand-doshi",
		"text": "ERPNext Core Developer, Anand Doshi walks us through some of the highlights of ERPNext Version 4 including the new UI, introduction of Frappe Framework and the plugin / app architecture."
	},
	{
		"label": "Umair Sayyed",
		"name": "umair-sayyed",
		"text": "ERPNext Support Analyst Umair Sayyed explains how ERPNext uses ERPNext to manage its own day to day operations and cloud services. Covers accounting, sales, support, HR, website and custom apps."
	},
	] %}

{% set users = [{
		"label": "Aditya Duggal",
		"name": "aditya-duggal",
		"text": "Early ERPNext user and community member Aditya Duggal walks us through his journey evaluating various ERP softwares and finally getting it right with ERPNext. He also explains that he did a phase wise implementation instead of a big bang approach, going in the order of Sales, Inventory, Accounting."},
	{
		"label": "Sonal Ramnathkar",
		"name": "sonal-ramnathkar",
		"text": "After evaluating a bunch of ERPs including TCS, Tally and many others, Sonal Ramnathkar finally found the right ERP for her furniture manufacturing startup. Sonal shares why she loves using ERPNext and why she would recommend it to any disrete manufacturing company."
	},
	{
		"label": "Deepak Gupta",
		"name": "deepak-gupta",
		"text": "Bullows Paint Equipment is a 50 year old manufacturing company that implemented ERPNext in 2010. Finance Controller and Charted Accountant Deepak Gupta shares his valuable insights on how Bullows moved from legacy FoxPro, evaluated SAP and many others and finally chose Open Source ERPNext."
	},
	{
		"label": "Mahesh Malani",
		"name": "mahesh-malani",
		"text": "Entrepreneur and engineer Mahesh Malani, the founder of Mahesh Engineering in Kolhapur shares his journey in getting his business in order using accounting and inventory systems. After many different attempts, he got his match in ERPNext."
	},
	{
		"label": "Tarun Gupta",
		"name": "tarun-gupta",
		"text": "When Tarun Gupta's security services startup Neural Integrated Services started growing, his ERP could not keep pace and was full of bugs in spite of spending a lot of money. Thats when Tarun decided he wanted to move to something better and discovered ERPNext."
	},
	{
		"label": "Prashant Thakkar",
		"name": "prashant-thakkar",
		"text": "Second Generation Owner Prashant Thakkar of Mukund / Magnum shares how he pushed his organization to implement ERPNext and his frustrations with other ERP vendors."
	},
] %}

{% set community = [{
		"label": "Global Community",
		"name": "global-community",
		"text": "ERPNext Users from across the globe took time to say hello and share their experiences with ERPNext for the 2014 Conference."},
] %}

{% macro videohtml(l) %}
{% for v in l %}
<div class="row">
	<div class="col-sm-3">
		<a href="/conf/videos/{{ v.name }}">
			<img src="/assets/erpnext_org/images/conf/videos/{{ v.name }}.jpg" class="no-shadow">
		</a>
	</div>
	<div class="col-sm-9">
		<h4><a href="/conf/videos/{{ v.name }}">{{ v.label }}</a></h4>
		{{ v.text }}
	</div>
</div>
{% endfor %}
{% endmacro %}

### Team Videos

---

{{ videohtml(erpnext) }}

---

<a name="user"></a>

### User Videos

---

{{ videohtml(users) }}

---

### Global Community

{{ videohtml(community) }}
