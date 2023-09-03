# FinOps-using-InfraCost

Why? empower engineering teams to use cloud infrastructure economically and efficiently.

<hr>

#Decision

| TF-Name                 | Cloud  | Cost($)    | Remarks                     |
| ---                     | ---    | ---        | ---                         |
| Aerospike-quick-start   | AWS    | 89.97      |  730 hrs                    |
| Aerospike-quick-start   | GCP    | 87.12      |  730 hrs                    |
| Aerospike-instance-types| AWS    | 1261.44    |  730 hrs c5d.9xlarge        |
| Aerospike-instance-types| AWS    | 1979.76    |  730 hrs m5d.12xlarge       |
| Aerospike-instance-types| AWS    | 2522.88    |  730 hrs r5d.12xlarge       |
| Wordpress               | AWS    | 86.75      |  t3.xlarge                  |
| Wordpress               | AWS    | 54.04      |  t3.medium                  |
| Wordpress               | AWS    | 152.15     |  t3.large                   |

<br>

Depending upon the Operating System and the Arch-type, download the infracost binary. <br>
<u>Refer:</u> <br>
https://www.infracost.io/docs/#1-install-infracost and <br>
https://www.infracost.io/docs/#quick-start <br><br>

In my case am using MacBook Pro (chip M1, 2020) , so downloading the file below <br>

(to binaries folder - mkdir binaries, cd binaries). <br>
wget https://github.com/infracost/infracost/releases/download/v0.10.28/infracost-darwin-arm64.tar.gz


For Other Operating Systems and releases Refer: <br>
(https://github.com/infracost/infracost/releases) <br>

Example for version 0.10.28 <br>
https://github.com/infracost/infracost/releases/tag/v0.10.28

Example for version 0.10.29 <br>
https://github.com/infracost/infracost/releases/tag/v0.10.29
<br>

Extract the downloaded tar.gz file using tar command below <br>
sureshadapa@localhost binaries % tar -xzf infracost-darwin-arm64.tar.gz

Check/List for the files <br>
sureshadapa@localhost binaries % ls <br>                                    
infracost-darwin-arm64		infracost-darwin-arm64.tar.gz <br>

Check if its an executable <br>
sureshadapa@localhost binaries % file infracost-darwin-arm64 <br>
infracost-darwin-arm64: Mach-O 64-bit executable arm64 <br>

Check Version <br>
sureshadapa@localhost binaries % ./infracost-darwin-arm64 --version <br>
Infracost v0.10.28 <br>

If new version is available it would give update message like below <br>
sureshadapa@localhost binaries % ./infracost-darwin-arm64 --version <br>
Infracost v0.10.28

Update: A new version of Infracost is available: v0.10.28 → v0.10.29 <br>
  $ curl -fsSL https://raw.githubusercontent.com/infracost/infracost/master/scripts/install.sh | sh <br>

If there is no new Version, it would give message like below <br>
sureshadapa@localhost binaries % ./infracost-darwin-arm64 --version <br>
Infracost v0.10.28 <br>

<hr>
#Download terraform examples <br>

Create a  folder for tf-examples (cd ../; mkdir tf-examples;cd tf-examples) <br>

Terraform examples are from below locations <br>
git clone https://github.com/aerospike/act <br>
git clone https://github.com/devbhusal/terraform-ec2-RDS-wordpress <br>

<hr>
#Run and Compare the cost (decision)) <br>

![image1](images/Aero-Cost-1.png)

<hr>

![image2](images/Aero-Cost-2.png)

