<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bespoke Order System</title>
    <style>
        body { font-family: 'Segoe UI', sans-serif; background: #f4f6f8; padding: 30px; margin: 0; display: flex; gap: 30px; }
        .pane { background: white; padding: 25px; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.05); flex: 1; }
        h2 { color: #064E3B; border-bottom: 2px solid #A7F3D0; padding-bottom: 8px; }
        label { display: block; margin-top: 15px; font-weight: bold; color: #374151; }
        input, select, button { width: 100%; padding: 10px; margin-top: 5px; border: 1px solid #D1D5DB; border-radius: 5px; box-sizing: border-box; }
        button { background: #064E3B; color: white; border: none; font-weight: bold; cursor: pointer; margin-top: 20px; }
        button:hover { background: #043e2f; }
        .order-card { background: #F9FAFB; border: 1px solid #E5E7EB; padding: 15px; margin-top: 15px; border-radius: 6px; position: relative; }
        .badge { display: inline-block; padding: 4px 8px; border-radius: 4px; font-size: 12px; font-weight: bold; margin-top: 10px; }
        .Pending { background: #FEF3C7; color: #92400E; }
        .Accepted { background: #D1FAE5; color: #065F46; }
        .Denied { background: #FEE2E2; color: #991B1B; }
        .admin-actions { margin-top: 10px; display: flex; gap: 10px; }
        .btn-accept { background: #10B981; }
        .btn-deny { background: #EF4444; }
    </style>
</head>
<body>

    <!-- CUSTOMER SIDE -->
    <div class="pane">
        <h2>Place Custom Clothing Order</h2>
        <form id="orderForm">
            <label>Your Name:</label>
            <input type="text" id="custName" required placeholder="e.g. John Doe">

            <label>Apparel Type:</label>
            <select id="apparelType">
                <option value="Bespoke Shirt">Bespoke Shirt</option>
                <option value="Custom Suit">Custom Suit</option>
                <option value="Handcrafted Trousers">Handcrafted Trousers</option>
            </select>

            <label>Chest Measurement (inches):</label>
            <input type="number" id="measurement" required placeholder="38">

            <button type="button" onclick="placeOrder()">Submit Custom Order</button>
        </form>
    </div>

    <!-- ADMIN SIDE -->
    <div class="pane">
        <h2>Admin Management Board</h2>
        <div id="orderQueue">
            <p style="color: #6B7280;">No orders placed yet...</p>
        </div>
    </div>

    <script>
        // Local temporary list to mimic a database brain
        let databaseOrders = [];
        let orderCounter = 1001;

        function placeOrder() {
            const name = document.getElementById('custName').value;
            const type = document.getElementById('apparelType').value;
            const size = document.getElementById('measurement').value;

            if(!name || !size) { alert("Please fill out all details!"); return; }

            // Step 1: Rule - Every new order starts strictly as "Pending"
            let newOrder = {
                id: orderCounter++,
                customer: name,
                item: type,
                measurement: size,
                status: "Pending"
            };

            databaseOrders.push(newOrder);
            document.getElementById('orderForm').reset();
            updateDashboard();
        }

        function updateStatus(orderId, newStatus) {
            // Find the order in our list and change its status word
            let order = databaseOrders.find(o => o.id === orderId);
            if(order) {
                order.status = newStatus;
            }
            updateDashboard();
        }

        function updateDashboard() {
            const queue = document.getElementById('orderQueue');
            if(databaseOrders.length === 0) {
                queue.innerHTML = '<p style="color: #6B7280;">No orders placed yet...</p>';
                return;
            }

            queue.innerHTML = ""; // Clear screen and rebuild layout
            databaseOrders.forEach(order => {
                let card = document.createElement('div');
                card.className = "order-card";
                
                let actionContent = '';
                // Step 2: Show buttons ONLY if status is Pending
                if(order.status === "Pending") {
                    actionContent = `
                        <div class="admin-actions">
                            <button class="btn-accept" onclick="updateStatus(${order.id}, 'Accepted')">Accept</button>
                            <button class="btn-deny" onclick="updateStatus(${order.id}, 'Denied')">Deny</button>
                        </div>
                    `;
                }

                card.innerHTML = `
                    <strong>Order #${order.id} - ${order.customer}</strong><br>
                    Item: ${order.item} (${order.measurement} inches)<br>
                    <span class="badge ${order.status}">${order.status}</span>
                    ${actionContent}
                `;
                queue.appendChild(card);
            });
        }
    </script>
</body>
</html>
