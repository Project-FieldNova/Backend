# Backend

<div align="center">
  
## Database Relationships
![Database Relationship](database\plannedTableRelationships.png)
</div>

## Database Resources
    managers:
        id
        firstName
        lastName
        email
        password
        profilePicture
        title
    providers:
        id
        firstName
        lastName
        email
        password
        profilePicture
        type
    clients:
        id
        firstName
        lastName
        email
        password
        profilePicture
        business
    workorders:
        id
        clients_id
        title
        address
        city
        state
        zip
        dateTime
        businessName
        corporateId
        contactName
        contactPhone
        description
        createDate
        notes
    invoices:
        id
        clients_id
        title
        description
        createDate
        dueDate
        notes
    tickets:
        id
        clients_id
        title
        severity
        status
        description
        createDate
        notes
    reports:
        id
        title
        createDate
        graphType
        workorders_id
        invoices_id
        tickets_id
        providers_id
        notes
    lineItems:
        id
        invoices_id
        price
        quantity
        title
        description
        notes
    notes:
        id
        tickets_id
        managers_id
        createDate
        editDate
        note
    attachments:
        id
        workorders_id
        tickets_id
        invoices_id
        source
        title
        description
        createDate
## Database Resources - Many to Many
    managers_workorders:
        id
        managers_id
        workorders_id
    managers_invoices:
        id
        managers_id
        invoices_id
    managers_tickets:
        id
        managers_id
        tickets_id
    managers_reports:
        id
        managers_id
        reports_id
    workorders_invoices:
        id
        workorders_id
        invoices_id
    workorders_tickets:
        id
        workorders_id
        tickets_id
    invoices_tickets:
        id
        invoices_id
        tickets_id
    workorders_providers:
        id
        workorders_id
        providers_id
    tickets_providers:
        id
        tickets_id
        providers_id


<div align="center">
  
## Tech. Stack
</div>

### Node/Express.js
### PostGreSQL
### Knex
### Firebase (Authentication Only)
