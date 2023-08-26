Folder Structure Conventions

### Example Path Api

# METHOD

First Character set At Filename.

[method]-request-[type]

# URI

api.domain.com/:version/:prefix/:endpoint
api.domain.com/:version/:prefix/:endpoint/:params

# URL

api.domain.com/v1/auth/login
api.domain.com/v1/dashboard/ or api.domain.com/v1/dashboard
api.domain.com/v1/reports/bill-history
api.domain.com/v1/inventories/inventory-doc-in/1

### Example Folder

|--mock/ ---------------------------------------------- # Version
| ├── auth/ ------------------------------------------- # Prefix of Endpoint
│ | ├── login/ ---------------------------------------- # Endpoint
| | | |-- post-request-body.json ---------------------- # Body Request
| | | |-- post-response-success.json ------------------ # Response
...
│ ├── dashboard/ -------------------------------------- # Endpoint ------------------------- [example# POST: api.domain.com/v1/dashboard]
| | |-- post-request-body.json ------------------------ # Body Request of index
| | |-- post-response-success.json -------------------- # Response of index
...
| |-- inventories/ ------------------------------------ # Prefix of Endpoint
| | |-- inventory-doc-in/ ----------------------------- # Endpoint
| | | |-- [id] ---------------------------------------- # Params Request
| | | | |-- get-request-query-string.md --------------- # Query string Request ------------- [example# GET: api.domain.com/v1/inventories/inventory-doc-in/1?merchantId=9]
| | | | |-- get-response-success-description.json ----- # Response field description
| | | | |-- get-response-success.json ----------------- # Response
| | | | |-- put-request-body -------------------------- # Body Request --------------------- [example# PUT: api.domain.com/v1/inventories/inventory-doc-in/1]
| | | | |-- put-response-error.json ------------------- # Error Response
| | | | |-- put-response-success.json ----------------- # Response
| | | |-- get-request-query-string.md ----------------- # Query string Request
| | | |-- get-response-success-description.json ------- # Response field description
| | | |-- get-response-success.json ------------------- # Response
| | | |-- post-request-body --------------------------- # Body Request --------------------- [example# POST: api.domain.com/v1/inventories/inventory-doc-in/1]
| | | |-- post-response-error.json -------------------- # Error Response
| | | |-- post-response-success.json ------------------ # Response
...
| |-- reports/ ---------------------------------------- # Prefix of Endpoint
| | |-- bill-history/ --------------------------------- # Endpoint
| | | |-- get-request-query-string.md ----------------- # Query string Request
| | | |-- get-response-success-description.json ------- # Response field description
| | | |-- get-response-success.json ------------------- # Response
└── ...a
