Folder Structure Conventions

### Example Path Api

# METHOD

First Character set At Filename.

[method]-request-[type]

# URI

api.domain.com/:version/:prefix/:endpoint

# URL

api.domain.com/v1/auth/login
api.domain.com/v1/dashboard/ or api.domain.com/v1/dashboard
api.domain.com/v1/reports/bill-history

### Example Folder

|--mock/ ---------------------------------------------- # Version
| ├── auth/ ------------------------------------------- # Prefix of Endpoint
│ | ├── login/ ---------------------------------------- # Endpoint
| | | |-- post-request-body.json ---------------------- # Body Request
| | | |-- post-response-success.json ------------------ # Response
...
│ ├── dashboard/ -------------------------------------- # Endpoint
| | |-- post-request-body.json ------------------------ # Body Request of index
| | |-- post-response-success.json -------------------- # Response of index
...
| |-- reports/ ---------------------------------------- # Prefix of Endpoint
| | |-- bill-history/ --------------------------------- # Endpoint
| | | |-- get-request-param.md ------------------------ # Params Request (when make get request)
| | | |-- get-response-success-description.json ------- # Response field description
| | | |-- get-response-success.json ------------------- # Response
└── ...
