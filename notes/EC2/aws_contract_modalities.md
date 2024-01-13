# Contract Modalities
There are multiple purchasing options, each covering a specific set of needs and obligations.



## On-Demand
* This is the default contract modality.

* You pay ***only*** for the EC2 instances that you **use**.

* Even if the instances are turned off, you have to pay for disk storage.

* You pay hourly or per second (minimum 60sec).

* The price is based on computacional capicity of each instance.

* Each ***partial hour*** that you use is priced **per second on Linux instances**.

* Each ***partial hour*** that you use is priced **per whole hour on Windows instances**.



## Reserved
* Even if you hire and doesn't use, you will be charged.

* Cheaper than On-Demand (up to 72%)

* **Must** be hired for at **least** ***1 year*** and at **maximum** ***3 years***.

* There are 3 **modalities**:
    * **Default:** Up to 72% cheaper, ***doesn't*** allows instance configuration changes.
    * **Conversible:** Up to 54% cheaper, ***does*** allows instance configuration changes.
    * **Programmed:** Allows instance reserve for a brief amount of time.

* There are 3 **payment options**:
    * **No Upfront**.
    * **Partial Upfront**.
    * **Full Upfront**.

* You **can't** cancel a reserved instance, you can only **sell** it in the **AWS Marketplace**.



## Spot
* Up to 90% cheaper than On-Demand

* Recommended for applications **tolerant to failure**.

* Your instances **could** be terminated at any given moment.

* You define the maximum price you want to pay for the instance, based on price or time used.

* You can define work loads up to 6 hours.

* AWS **always** gives you a notification ***2 minutes*** before the interruption.