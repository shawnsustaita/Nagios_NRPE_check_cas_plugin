# Nagios_NRPE_check_cas_plugin
Nagios NRPE check_cas plugin

# Description
check_cas is used to authenticate to a CAS (Central Authentication Service)
server via an HTTP(S) POST of credentials (ie username and password).

# Testing
check_cas has only been tested in a very limited fashion with Jasig Central
Authentication Service version 3.5.2.1.

# Caveats
The fillout form portion of the code depends on finding the form.  The form
is found based on its present fields.  WWW::Mechanize's form_with_fields()
is used to find the correct form.  It's utilized as follows and may need
to be modified accordingly.

$mech->form_with_fields('username', 'password');

# Examples
check_cas --help
check_cas --login https://example.com/cas/login --username neo --password TheOne
check_cas --login https://$HOSTADDRESS$/cas/login --username neo --password TheOne
