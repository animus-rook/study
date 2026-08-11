#### **Lab Objective**

- Set up a simple LAN with two PCs connected to a switch.
- Assign IP addresses and verify connectivity using `ping`.

---

### **Topology**

1. **PC1**: IP `192.168.1.10/24`, Gateway: `N/A`
2. **PC2**: IP `192.168.1.11/24`, Gateway: `N/A`
3. **Switch**: Default configuration.

---

### **Step-by-Step Instructions**

#### **Step 1: Create the Topology**

1. Open Cisco Packet Tracer.
2. Drag and drop the following devices onto the workspace:
    - Two PCs (`PC-PT`).
    - One switch (`2960` or similar).
3. Connect the devices using straight-through cables:
    - PC1 to Switch (FastEthernet0/1).
    - PC2 to Switch (FastEthernet0/2).

---

#### **Step 2: Configure PC1**

1. Click on **PC1** to open its configuration window.
2. Go to the **Desktop** tab → Click on **IP Configuration**.
3. Assign the following:
    - **IP Address**: `192.168.1.10`
    - **Subnet Mask**: `255.255.255.0`
    - **Default Gateway**: Leave blank.

---

#### **Step 3: Configure PC2**

1. Click on **PC2** to open its configuration window.
2. Go to the **Desktop** tab → Click on **IP Configuration**.
3. Assign the following:
    - **IP Address**: `192.168.1.11`
    - **Subnet Mask**: `255.255.255.0`
    - **Default Gateway**: Leave blank.

---

#### **Step 4: Test Connectivity**

1. Open the **Command Prompt** from the Desktop tab of PC1.
2. Use the `ping` command to test connectivity:
    - `ping 192.168.1.11`
3. If configured correctly, you should receive successful replies.

---

### **Troubleshooting**

- If `ping` fails:
    - Verify IP configurations on both PCs.
    - Check cable connections and ensure they are set to `FastEthernet`.
    - Use Packet Tracer's **simulation mode** to trace packets and find where they're being dropped.