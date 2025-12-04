```
frappe.ui.form.on('Donor', {
    custom_customer: function(frm) {
        if (!frm.doc.custom_customer) return;

        frappe.db.get_value('Customer', frm.doc.custom_customer, 
            ['customer_name', 'custom_phone', 'custom_email'], function(r) {
            if (r) {
                frm.set_value('donor_name', r.customer_name);
                frm.set_value('email', r.custom_email);
                frm.set_value('donor_type', 'Individual');
                frm.refresh_field('email');
                frm.refresh_field('donor_type');
            }
        });
    }
});
```
