# Spring Project of PNU student Bakai Yurii


## Functional Requirements for the Backend

1. **Retrieve List of Buildings**:
   - **Functionality**: Return a list of all buildings.
   - **Description**: Users can retrieve a list of all buildings stored in the database.

2. **Retrieve Building Details**:
   - **Functionality**: Return details of a specific building by its ID.
   - **Description**: Users can view the name and location of a specific building.

3. **Add New Building**:
   - **Functionality**: Add a new building to the database.
   - **Description**: Admin can add a new building specifying its name and location.

4. **Update Building Information**:
   - **Functionality**: Update information of an existing building.
   - **Description**: Admin can update the name or location of an existing building.

5. **Delete Building**:
   - **Functionality**: Delete a building from the database.
   - **Description**: Admin can delete a building by its ID.

6. **Retrieve List of Rooms in a Building**:
   - **Functionality**: Return a list of all rooms in a specific building.
   - **Description**: Users can retrieve a list of all rooms located in a specified building.

7. **Add New Room**:
   - **Functionality**: Add a new room to a specific building.
   - **Description**: Admin can add a new room specifying it's number, capacity, and type.

8. **Update Room Information**:
   - **Functionality**: Update information of an existing room.
   - **Description**: Admin can update the room number, capacity, or type.

9. **Delete Room**:
   - **Functionality**: Delete a room from the database.
   - **Description**: Admin can delete a room by its ID.

10. **Add Equipment to Room**:
    - **Functionality**: Add new equipment to a specific room.
    - **Description**: Admin can add new equipment specifying its name and quantity.

11. **Retrieve Room Conditions**:
    - **Functionality**: Return a list of conditions for a specific room.
    - **Description**: Users can view all conditions (issues) of a specific room, including the description and date reported.

12. **Handle Maintenance Requests**:
    - **Functionality**: Add, update, and delete maintenance requests.
    - **Description**: Admin can add new requests, update the status of existing requests (e.g., from "Pending" to "Completed"), and delete maintenance requests.

---

## System Behaviors

1. **Manage Buildings**
   - Retrieve all buildings
   - Retrieve details of a specific building
   - Add a new building
   - Update an existing building
   - Delete a building

2. **Manage Rooms**
   - Retrieve all rooms in a building
   - Retrieve details of a specific room
   - Add a new room to a building
   - Update an existing room
   - Delete a room

3. **Manage Room Equipment**
   - Retrieve all equipment in a room
   - Add new equipment to a room
   - Update equipment in a room
   - Delete equipment from a room

4. **Manage Room Conditions**
   - Retrieve all conditions of a room
   - Add a new condition to a room
   - Update a condition of a room
   - Delete a condition from a room

5. **Manage Maintenance Requests**
   - Retrieve all maintenance requests for a room
   - Add a new maintenance request
   - Update a maintenance request
   - Delete a maintenance request

---

## REST API Endpoints

### Buildings

- **GET /api/buildings**
  - Retrieve all buildings
- **GET /api/buildings/{id}**
  - Retrieve details of a specific building
- **POST /api/buildings**
  - Add a new building
- **PUT /api/buildings/{id}**
  - Update an existing building
- **DELETE /api/buildings/{id}**
  - Delete a building

### Rooms

- **GET /api/buildings/{buildingId}/rooms**
  - Retrieve all rooms in a building
- **GET /api/rooms/{id}**
  - Retrieve details of a specific room
- **POST /api/buildings/{buildingId}/rooms**
  - Add a new room to a building
- **PUT /api/rooms/{id}**
  - Update an existing room
- **DELETE /api/rooms/{id}**
  - Delete a room

### Room Equipment

- **GET /api/rooms/{roomId}/equipment**
  - Retrieve all equipment in a room
- **POST /api/rooms/{roomId}/equipment**
  - Add new equipment to a room
- **PUT /api/rooms/{roomId}/equipment/{equipmentId}**
  - Update equipment in a room
- **DELETE /api/rooms/{roomId}/equipment/{equipmentId}**
  - Delete equipment from a room

### Room Conditions

- **GET /api/rooms/{roomId}/conditions**
  - Retrieve all conditions of a room
- **POST /api/rooms/{roomId}/conditions**
  - Add a new condition to a room
- **PUT /api/rooms/{roomId}/conditions/{conditionId}**
  - Update a condition of a room
- **DELETE /api/rooms/{roomId}/conditions/{conditionId}**
  - Delete a condition from a room

### Maintenance Requests

- **GET /api/rooms/{roomId}/maintenance-requests**
  - Retrieve all maintenance requests for a room
- **POST /api/rooms/{roomId}/maintenance-requests**
  - Add a new maintenance request
- **PUT /api/maintenance-requests/{requestId}**
  - Update a maintenance request
- **DELETE /api/maintenance-requests/{requestId}**
  - Delete a maintenance request