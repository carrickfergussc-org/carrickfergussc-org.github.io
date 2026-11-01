---
title: "Embedded"
date: 2020-06-14 08:55:53
status: draft
id: 525
slug: 
parent: 0
type: page
---

<div id="eventbrite-widget-container-109521162746"></div>

<script src="https://www.eventbrite.co.uk/static/widgets/eb_widgets.js"></script>

<script type="text/javascript">
    var exampleCallback = function() {
        console.log('Order complete!');
    };

    window.EBWidgets.createWidget({
        // Required
        widgetType: 'checkout',
        eventId: '109521162746',
        iframeContainerId: 'eventbrite-widget-container-109521162746',

        // Optional
        iframeContainerHeight: 425,  // Widget height in pixels. Defaults to a minimum of 425px if not provided
        onOrderComplete: exampleCallback  // Method called when an order has successfully completed
    });
</script>