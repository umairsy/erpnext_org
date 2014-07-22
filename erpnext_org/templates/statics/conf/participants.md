# Who Is Coming

Registered Participants for the ERPNext Conference.

<table class="table table-bordered">
	<thead>
		<tr>
			<th style="width: 50%;">Name</th>
			<th>Company</th>
		</tr>
	</thead>
	<tbody>
		{%- for p in frappe.get_list("Registrant", fields=["full_name", "company_name"], order_by="company_name asc", ignore_permissions=True) %}
		<tr>
			<td>{{ p.full_name }}</td>
			<td>{{ p.company_name }}</td>
		</tr>
		{% endfor -%}
	</tbody>
</table>

[Register Now](/conf/register)

<!-- render-jinja -->
