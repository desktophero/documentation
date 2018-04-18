---
title: J'ai un downtime prévu sur mon monitor, pourquoi alerte-t-il encore ?!
kind: faq
further_reading:
- link: "monitors/monitor_types"
  tag: "Documentation"
  text: Apprenez à créer un monitor
- link: "monitors/notifications"
  tag: "Documentation"
  text: Configurez les notifications de votre monitor
- link: "monitors/downtimes"
  tag: "Documentation"
  text: En savoir plus sur les downtimes
---

When you [schedule a downtime][1] over a specific tag scope, the downtime will apply "AND" logic to those tags. So if you wanted to set up a downtime over `host:A` and `host:B`, then the downtime will silence only those monitors that alert on evaluation groups that contain both tags **`host:A` AND `host:B`** (and such a downtime would likely not silence any alerts).  

If you want to schedule a downtime over a subset of hosts, a good way to do so is to find a host-tag common to all those hosts and scope the downtime by that tag.

One easy way you can take advantage of to create new host-tags directly in the Datadog UI from your [Infrastructure List][2] and [Host Map][3] by selecting a host and hitting the **Edit Tags** button (shown below), or via [our API][4].

{{< img src="monitors/faq/edit_tag.png" alt="edit tag" responsive="true" popup="true" >}}

{{< partial name="whats-next/whats-next.html" >}}

[1]: /monitors/downtimes
[2]: /graphing/infrastructure
[3]: /graphing/infrastructure/hostmap
[4]: /api/#tags-add