### Ride Management

Ride management

### Installation

You can install this app using the [bench](https://github.com/frappe/bench) CLI:

```bash
cd $PATH_TO_YOUR_BENCH
bench get-app $URL_OF_THIS_REPO --branch develop
bench install-app ride_management
```

### Contributing

This app uses `pre-commit` for code formatting and linting. Please [install pre-commit](https://pre-commit.com/#installation) and enable it for this repository:

```bash
cd apps/ride_management
pre-commit install
```

Pre-commit is configured to use the following tools for checking and formatting your code:

- ruff
- eslint
- prettier
- pyupgrade

### License

mit






As client Script is not get pushed 
i have written i client script on Ride Booking Document


frappe.ui.form.on('Ride Booking', {
	price_per_km(frm){
	    total_amount = 0
	    if (frm.doc.price_per_km && frm.doc.estimated_km) {
	        frm.doc.service.forEach(function(row) {
	            total_amount = frm.doc.price_per_km * frm.doc.estimated_km + row.amount
	            
	        })
	    }
	    frm.set_value("total_amount", total_amount)
	},
	estimated_km(frm){
	    total_amount = 0
	    if (frm.doc.price_per_km && frm.doc.estimated_km) {
	        frm.doc.service.forEach(function(row) {
	            total_amount = frm.doc.price_per_km * frm.doc.estimated_km + row.amount
	            
	        })
	    }
	    frm.set_value("total_amount", total_amount)
	}
	
})

