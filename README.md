# assignment_designing_nosql_data_models
I'll have one data model hold the SQL please

Jeffrey Dederick
Gene Tinderholm


1). RELATIONSHIP: 1 User(collection) to many fields(documents);

    PROPERTIES: {[Username, FName, LName, Birthday, Gender, Phone Number, {Location: {City, State, Country}}, {Privacy: {Boolean: '', Applicables: [Birthday, Gender, FName, LName, Phone Number, Location]}]}

INTERMEDIATE
1). RELATIONSHIPS: 1 Restaurant to many tables.     
                   1 table to many customers.
                   1 Restaurant to many customers.

    USER PROPERTIES: {[Name, Phone Number, Number of Guest, Reservation Number]}

    TABLE PROPERTIES: {[Table Number, {Availability Times: []}, Seats]}

    RESTAURANT PROPERTIES: {[{Tables: []}, {Available Tables: []}, {Total Capacity: Number}, {Current Wait Times(Per Table): [{Tables: times}] ]}

2). RELATIONSHIPS: Many Student to many classes.     
                   Many class to many semesters.
                   1 class to many exams.
                   1 University to many semester.
                   1 University to many students.

    STUDENT PROPERTIES: {id: string, password: string, classes: {current: [], previous: []}, }

    CLASS PROPERTIES:{id: number, subject: string, {current students: []}, {exams: [{scores: [] } ] } }

    EXAM PROPERTIES:{exam_date: string, scores:[], requirements: number}

    UNIVERSITY PROPERTIES:{name:string, location: string, current_student: [], semesters: {current: [], previous: []}, alumni: []}

ADVANCED
1). RELATIONSHIPS: 1 Business to many departments.     
                   1 department to many products.
                   1 Business to many revenues.
                   1 product to 1 price.
                   1 receipt to 1 transaction.

    PRODUCT PROPERTIES: {cost: number, price: number, sku: number, in_stock: number, total_sales: number, department: number}

    RECEIPT PROPERTIES: {date: string, products: [], total: number, profits: [], id: number}

    DEPARTMENT PROPERTIES:{id: number, name: string, desc: string, products: []}

    BUSINESS PROPERTIES: {name: string, location: string, departments: [], receipts: []}

2). RELATIONSHIPS: 1 User to many activies.     
                   Many friends to many users.
                   1 feed to 1 user.
                   1 profile to 1 user.

    USER PROPERTIES: {id: number, Username: string, friends: [], {feed: props}, {profile: []}, {activities: []}}

    ACTIVITY PROPERTIES: {time_stamp: number, description: string, user_id: number}

    PROFILE PROPERTIES: {[Username, FName, LName, Birthday, Gender, Phone Number, {Location: {City, State, Country}}, {Privacy: {Boolean: '', Applicables: [Birthday, Gender, FName, LName, Phone Number, Location]}]}

    FEED PROPERTIES:{included_users: [], interests: [], current_activities: []}
