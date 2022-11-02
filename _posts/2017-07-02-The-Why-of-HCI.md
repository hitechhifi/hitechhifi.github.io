---
published: true
---
The “why” of HCI
================

Helping businesses solve problems and make well informed decisions has been my job for the better part of the last decade. While I find this ultimately enjoyable, there still remains quite a bit of misinformation in the field: just a few months ago a customer informed me that “virtualization just isn’t ready for production environments.” – this, after almost 20 years of x86 virtualization!

![omg-1934214-300x200.jpg]({{site.baseurl}}/images/omg-1934214-300x200.jpg)


OMG Becky…

Hearing comments like this made me want to help dispel some of the FUD out there, clear the fog of war and get things straight. So let’s start with a technology du jour: Hyperconverged Infrastructure.

Hyperconverged Infrastructure, or HCI as it is commonly known today, is the collapse and consolidation of traditional storage architecture into x86 compute architecture. Plainly put: traditional storage architecture is a boxcar attached by couplings to a locomotive engine. SAN/NAS architecture has historically been coupled by transport mechanism (Fibre Channel, FCoE, IP networks, etc). HCI is a cargo plane, engines attached to the same fuselage that provides the storage.

![barcode-616035-300x215.png]({{site.baseurl}}/images/barcode-616035-300x215.png)


Planes, Trains and Automobiles! …and boats I guess. But boats are jerks.

Why give this example? Well with a train, I can add more engines (compute) without adding more boxcars (storage) or vice versa. I can scale these two domains independently of one another, within reasonable consideration of workload. With a cargo plane, if I need more space for shipping, or I need to get things moved faster, I simply buy a new plane. Now I can buy a plane with similar storage and larger engines, or the opposite is true as well. This can be good, bad, or otherwise, depending on your business application and needs.

![david-13710-225x300.jpg]({{site.baseurl}}/images/david-13710-225x300.jpg)


Nice beard, Goliath! How about a little off the top?

Much like the “virtualization isn’t ready” comment above, I have heard all throughout 2015 that HCI isn’t ready for lift-off, even though HCI sprouted its first wings nearly a decade ago. Common misconceptions abounded, from “linear scale/growth isn’t how data centers grow” to “the technology is too immature” or “why trust a startup vendor?” Now in the past year, major vendors made some radical marketing pushes, and the gloves have come off – igniting more than a few David and Goliath battles in the HCI space between strong incumbents and newcomers alike.

Automation and Orchestration, DevOps, Continuous Development and Continuous Integration (CI/CD), and private/hybrid cloud efforts have all created opportunity to help IT move as quickly as the business demands. This is commonly referred to as “at the speed of business,” but I’ve consulted for enough businesses to know that this speed is quite variable indeed!

As “software defined” becomes more and more the focus of IT, and not the hardware underlay itself, the HCI model becomes increasingly more compelling. The ability to deliver infrastructure capacity as a commodity (Compute hardware, Storage capacity, and in some cases a pre-installed/pre-configured hypervisor of choice) and “plug and play” is beating out traditional three tiered architectures simply by merit of design. HCI is _designed by nature_ to be node-based architecture that grows compute and storage by some degree with every node.

![panda-303949-288x300.png]({{site.baseurl}}/images/panda-303949-288x300.png)

But WHY?

Just like the panda said – why? Why HCI? Think about these choices from a business perspective for a second: traditional three-tiered architecture I need to size, architect and design each separate domain (compute, storage or network) which takes internal expertise or consulting know-how, then I need to cut a Purchase Order (which can take weeks to months, depending on your procurement cycles, management, legal, etc.) Afterwards my delivery lead time can take between weeks to months(!) to receive the new hardware. Next I need to physically rack and configure the hardware, cable (power, network, Out-of-Band management, Fibre, etc.) Now let’s go, right? Wrong! We need to configure OS’s for compute, configure storage arrays / LUNs / Disk Aggregates / Pools, etc. This is all before we even do burn-in testing (for piece of mind) and integration testing to ensure our new infrastructure is healthy before we release it into production.

HCI by design takes a lot of the guesswork out of the equation. Since storage and compute (don’t forget potentially virtualization) are combined into a SKU-able package, and scale-out by the node, you purchase what amounts to an appliance – a “block” of infrastructure. These nodes are all coupled within software, only physically tethered to each other by way of the upstream switches (usually Top of Rack switches).

So why do you care? Lifecycle management is made much easier by allowing nodes to be introduced and retired from these environments non-disruptively. I can consume infrastructure capacity on a per-project basis, capitalize the expense, and depreciate the asset easily vs. multiples or  portions of arrays, servers, switches etc. Alternately I can monitor my infrastructures expected growth, operationalize the expense back to different business units via a chargeback/showback mechanism, and move the visibility of IT value up the ladder.

Lead time to delivery on commodity hardware (servers and hard disks) is also much shorter than lead time on enterprise SAN arrays, full racks of disks (DAE’s), etc.  So from a project perspective, you are already saving yourself weeks of time just by adopting a rapidly deployable, scale-out model.

![business people standing in the dark, with colored arrows going  upward behind them]({{site.baseurl}}/images/arrows-1915360-300x200.jpg)

Can we get some light in here?

Lastly the integration of HCI products are normally highly tested before shipping out the door, meaning the amount of risk the business needs to be capable to absorb is minimal. Compare this to the traditional architecture knowledge set needed to architect, design, configure, deploy, manage and maintain/retire monolithic hardware sets. You might just be enabling an FTE to move from putting out fires daily to learning how to connect to a RESTful API with POSTman, or building their first cloud solution using Terraform and creating something of value for both them and your business.

A piece of advice I was given a long time ago is this: “If you are always reacting to events, then you have no time to create, and true value comes from creation.” The more we can move IT forward, create new innovations and enable positive growth, granular control, and the ability to dynamically shift with demand, the more we can win against our competitors in business.
