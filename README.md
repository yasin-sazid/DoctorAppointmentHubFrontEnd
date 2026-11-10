# Doctor Appointment Hub — Angular Client

A role-oriented web interface for doctor appointment management. Built with Angular, the application gives patients and administrators dedicated screens for account management, doctor information, and appointment workflows.

## User journeys

**Patients** can register, sign in, manage account information, and work with appointment records through patient-facing components.

**Administrators** have dashboards and screens for managing doctors, patients, administrator accounts, and their own account details.

The component layout mirrors these journeys: `patient-dashboard`, `patient-appointment-dashboard`, `admin-dashboard`, `admin-doctor-management`, `admin-patient-management`, and related forms keep each task in its own Angular component.

## Frontend architecture

```text
Routed components → Angular services → HttpClient → Doctor Appointment Hub API
```

[app-routing.module.ts](src/app/app-routing.module.ts) connects pages and dashboards. The four service modules under `src/app/services/` encapsulate patient, administrator, doctor, and appointment requests. They use Angular `HttpClient` and query parameters to communicate with the backend at **`http://localhost:5002/api`**.

## Run locally

Use a Node.js release compatible with Angular 12 and install the locked dependencies:

```bash
npm ci
npm start
```

Open `http://localhost:4200` and run the companion backend at port 5002 for data-backed workflows.

```bash
npm run build
npm test
```

The project includes Angular component/service specifications and a Jasmine/Karma test configuration. `npm run watch` supports development builds with file watching.

## Technologies and contributions

Angular 12, TypeScript 4.3, RxJS 6, Angular Router, Angular Forms, and HttpClient provide the client foundation. The project demonstrates reusable service boundaries, role-specific navigation, form-driven account workflows, and integration between a component-based frontend and an ASP.NET Core API.
