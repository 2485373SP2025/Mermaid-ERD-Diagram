```mermaid 
erDiagram
    PRODUCT {
        string name
        string style
        string size
        string color
        string price
    }

    CUSTOMER {
        string first_name
        string last_name
        string email
        string phone
        string address
    }

    SALE {
        float total_price
        float tax
        string payment_method
    }

    INVENTORY {
        string quantity_available
        string warehouse_location
        float price_per_unit
    }

    PRODUCT ||--o{ SALE : "sold in"
    CUSTOMER ||--o{ SALE : "makes"
    PRODUCT ||--o{ INVENTORY : "comes from"
```
### Description of Diagram
* The product is what is (in this case shoes) sold to make the sale which generates profit for the company. 
* The customer completes a payment for the product which generates a sale, which is how a company makes its money. 
* The product is stored in the inventory before being sold. It is later shipped to the customer after the sale happens. 
