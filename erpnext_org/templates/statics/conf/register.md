<img src="/assets/erpnext_org/images/conf/erpnext-conf-14.png" class="img-responsive">

<p class="lead">Register for the 2014 ERPNext Conference on Thursday Sept 25th, 2014 at Mumbai</p>

<form style="max-width: 600px;" id="register">
	<div class="alert alert-info">We have limited seating capacity so register early</div>
<div class="row">
    <div class="col-md-12">
        <div style="position: static;" class="form-group">
            <label for="input-text-1" class="text-danger">Full Name</label>
            <input class="form-control" id="full_name" placeholder="Your Name" type="text">
        </div>
        <div style="position: static;" class="form-group">
            <label for="input-id-2" class="text-danger">Company Name</label>
            <input class="form-control" id="company_name" placeholder="Company Name" type="text">
        </div>
        <div style="position: static;" class="form-group">
            <label for="input-id-3" class="text-danger">Your Email Id</label>
            <input class="form-control" id="email_id" placeholder="you@example.com" type="email">
            <p class="help-block small">We will send the invite on this id.</p>
        </div>
        <div style="" class="form-group">
            <label for="input-id-4">Comments</label>
            <textarea class="form-control" id="comments" placeholder="Suggestions or feedback" style="height: 150px;"></textarea>
            <p class="help-block small">Let us know what topics, workshops you would like the conference to cover.</p>
        </div>
		<p><b>I am interested in:</b></p>
		<div class="row">
		    <div class="col-md-12">
		        <div style="position: static;" class="checkbox">
		            <label>
		                <input type="checkbox" id="is_user"> <span>User Sessions</span>
		            </label>
		        </div>
		    </div>
		</div>
		<div class="row">
		    <div class="col-md-12">
		        <div style="position: static;" class="checkbox">
		            <label>
		                <input type="checkbox" id="is_partner"> <span>Partner Sessions</span>
		            </label>
		        </div>
		    </div>
		</div>
		<div class="row">
		    <div class="col-md-12">
		        <div style="position: static;" class="checkbox">
		            <label>
		                <input type="checkbox" id="is_developer"> <span>Developer Sessions</span>
		            </label>
		        </div>
		    </div>
		</div>
		<br>
        <div class="form-group" style="padding-right: 20px; position: static;">
            <button type="submit" class="btn btn-primary btn-lg">Register</button>
        </div>
    </div>
</div>
</form>

<script>
frappe.ready(function() {
	$("form#register").on("submit", function() {
		var data = {};
		$.each(["full_name", "company_name", "email_id", "comments"], function(i, f) {
			data[f] = $("#" + f).val();
		});
		$.each(["is_user", "is_partner", "is_developer"], function(i, f) {
			data[f] = $("#" + f).prop("checked") ? 1 : 0;
		});

		if(!(data.full_name && data.company_name && data.email_id)) {
			frappe.msgprint("Please enter the mandatory fields (Your Name, Company Name and Email Id)");
			return false;
		};

		$.ajax({
			url: "/api/method/erpnext_org.helpers.register",
			method: "POST",
			data: {"data": JSON.stringify(data) },
			statusCode: {
				200: function(data) {
					if(data && data.message) {
						frappe.msgprint(data.message);
					} else {
						frappe.msgprint("Thank you for your registration. We will get in touch by email.");
						setTimeout(function() { location.href = "/conf" }, 3000);
					}
				}
			}
		}).always(function(data, status, xhr) {
			console.log(xhr);
			if(xhr.status!==200) {
				frappe.msgprint("There were errors. Please report at info@erpnext.com");
			}
		});

		return false;
	});
});
</script>
