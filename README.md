# oci-get-vnics

oci-get-vnics enables you to retrieve the unique identifiers (OCIDs) of each VNIC and its associated compute instance, which are associated with a user-specified Virtual Cloud Network (VCN) on Oracle Cloud Infrastructure (OCI).

You can specify multiple VCNs, multiple Compartments, and multiple Regions in your search.

Instructions:
- Clone this project
- Make sure the ./get-vnics script is executable:
<pre>
chmod +x ./get-vnics
</pre>
- Assign values to the variables in ./env.sh:
<pre>
export get_vnics_compartment_id=&ltyour compartment id&gt
export get_vnics_region=&ltyour region identifier&gt
export get_vnics_vcn_id=&ltyour vcn id&gt
</pre>
- Run the ./get-vnics script using the command-line options:
<pre>
Usage Examples:

# all parameter values come from environment variables defined in ./env.sh
./get-vnics

# all parameter values are passed in using the command-line flags.
./get-vnics -cp ${get_vnics_compartment_id} -n ${get_vnics_vcn_id} -r ${get_vnics_region}

# all parameter values come from environment variables,
# except for the vcn parameter, which is passed in using the command-line flags.
./get-vnics -n ${get_vnics_vcn_id}

Note that you may pass multiple values to the command-line flags
once the variables in env.sh have been assigned values.

Options:

Flag                          Description

-cp          Specify the ocid of the compartment your vcn is in.
-h           Show options.
-n           Specify the ocid of the vcn whose vnic ocids you are searching for.
-r           Specify the region identifier your vcn is in.
</pre>
