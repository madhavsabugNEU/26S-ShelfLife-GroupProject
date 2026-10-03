# ShelfLife

ShelfLife is a course materials marketplace built for Northeastern students. It makes it easier to buy and sell textbooks, calculators, lab kits, software access codes, and other class materials, without relying on general resale apps that aren't organized around courses.

Built as a team project for CS 3200 (Database Design) at Northeastern University, Spring 2026.

**Demo video:** https://www.youtube.com/watch?v=jpNh5U-58YQ

## My Contributions

I was one of five team members. My main work was on the database and data quality:

- **Database design:** Designed the relational database schema, with linked tables and foreign keys connecting users, courses, listings, and price history.
- **Mock data:** Generated realistic mock data so the team could test the application's features.
- **Data integrity:** Found and fixed data issues in the SQL tables, such as missing price-history records, so the app's data stayed accurate.
- **Dashboard debugging:** Reviewed and debugged the Streamlit analytics dashboard with the team, fixing functional bugs in the reporting page.

## Project Overview

Many students finish a class and no longer need its materials, while other students are just starting that same course and need those exact items. ShelfLife connects those two groups.

Listings are tied to specific courses, so buyers can look up materials by course and sellers can price items with more context. Seller ratings and price history help users make informed decisions.

## User Roles

- **Seller:** creates listings, checks past prices before posting, and manages active or sold items.
- **Buyer:** searches by course, compares listings, saves items to a wishlist, and views seller ratings.
- **Data Analyst:** views marketplace activity, pricing trends, course-level demand, and seller performance.
- **Admin:** manages the course catalog, reviews flagged listings, and handles account or listing issues.

## Core Features

- Course-based search for materials
- Historical price information to judge whether a listing is reasonable
- Seller ratings and reviews
- Wishlist support for buyers
- Analytics views for trends, demand, and seller activity
- Admin tools for course management and moderation

## Tech Stack

- **Python**
- **MySQL** – relational database
- **Flask** – REST API and backend routes
- **Streamlit** – front end and analytics dashboard
- **Docker / Docker Compose** – running all services together

## Repository Structure

- `app/` – Streamlit front end
- `api/` – Flask API and backend routes
- `database-files/` – SQL files for the schema and sample data
- `datasets/` – data files used by the project
- `docs/` – supporting documentation
- `ml-src/` – space for analytics or model-related work

## Running the Project

**Prerequisites:** Docker Desktop, and Python 3.11 if you want to run parts of the project outside Docker.

From the root of the repository, run:

```
docker compose up -d
```

Any `.sql` files in `database-files/` run automatically when a new database container is created. If the schema or sample data changes, recreate the database container so those files run again.

## Testing

We tested ShelfLife manually by walking through the main user flows for each role: searching by course and opening listings as a buyer, creating and updating listings as a seller, and checking that analytics pages loaded and their summary numbers matched the underlying sample data.

## Team

Ariz Nawaz, Madhav Sabu, Vineeth Kanpa, Jiya Bhan, Keila Olaverria
