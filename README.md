# MavenMovies Data Analysis Project

## Subtopic: Business Intelligence and Operational Insights

## Introduction
**Situation:** My business partner and I were recently approached by a local business owner interested in purchasing Maven Movies. He primarily owns restaurants and bars and has numerous questions about our business and the rental industry. His offer seems generous, so we are considering his proposal.

**Objective:** Use MySQL to extract and analyze data from various tables in the Maven Movies database to answer the potential acquirer’s questions. Each question requires writing a multi-table SQL query, joining at least two tables.

![Project Screenshot](https://github.com/danartech/Maven-Movies-Business-Intelligence-Project/blob/main/Maven%20Movie%20BI.png) 

## Project Scope and Steps

### 1. Managers' Details
**Question:** My partner and I want to come by each of the stores in person and meet the managers. Please send over the managers’ names at each store, with the full address of each property (street address, district, city, and country please).

**Approach:**
- Join the `stores` table with the `staff` table to get manager details.
- Include the full address from the `addresses` table.

### 2. Inventory List
**Question:** I would like to get a better understanding of all of the inventory that would come along with the business. Please pull together a list of each inventory item you have stocked, including the store_id number, the inventory_id, the name of the film, the film’s rating, its rental rate, and replacement cost.

**Approach:**
- Join the `inventory` table with the `films` table to get film details.
- Include the `stores` table to associate inventory with store IDs.

### 3. Inventory Summary
**Question:** From the same list of films you just pulled, please roll that data up and provide a summary-level overview of your inventory. We would like to know how many inventory items you have with each rating at each store.

**Approach:**
- Group the inventory list by `store_id` and `rating`.
- Count the number of inventory items per group.

### 4. Replacement Cost Analysis
**Question:** We want to understand how diversified the inventory is in terms of replacement cost. We want to see how big of a hit it would be if a certain category of film became unpopular at a certain store. We would like to see the number of films, as well as the average replacement cost, and total replacement cost, sliced by store and film category.

**Approach:**
- Group the inventory by `store_id` and `category`.
- Calculate the number of films, average replacement cost, and total replacement cost for each group.

### 5. Customer Information
**Question:** We want to make sure you folks have a good handle on who your customers are. Please provide a list of all customer names, which store they go to, whether or not they are currently active, and their full addresses – street address, city, and country.

**Approach:**
- Join the `customers` table with the `stores` and `addresses` tables to get customer details.

### 6. Customer Spending
**Question:** We would like to understand how much your customers are spending with you, and also to know who your most valuable customers are. Please pull together a list of customer names, their total lifetime rentals, and the sum of all payments you have collected from them. It would be great to see this ordered on total lifetime value, with the most valuable customers at the top of the list.

**Approach:**
- Join the `customers`, `rentals`, and `payments` tables to calculate total rentals and payments.
- Order the results by total payments collected.

### 7. Advisors and Investors
**Question:** My partner and I would like to get to know your board of advisors and any current investors. Could you please provide a list of advisor and investor names in one table? Could you please note whether they are an investor or an advisor, and for the investors, it would be good to include which company they work with.

**Approach:**
- Combine `advisors` and `investors` tables.
- Include the role and company details for each investor.

### 8. Awarded Actors Coverage
**Question:** We're interested in how well you have covered the most-awarded actors. Of all the actors with three types of awards, for what percentage of them do we carry a film? And how about for actors with two types of awards? Same questions. Finally, how about actors with just one award?

**Approach:**
- Calculate the percentage of awarded actors covered by our films.
- Group actors by the number of awards they have received.

## Tools Used
- **MySQL:** Used for database querying and analysis.

## Outcome
I successfully utilized MySQL to extract and analyze data, answering critical questions from the potential acquirer. This project showcased my proficiency in MySQL data querying and analysis, providing valuable insights into the business operations of Maven Movies.

## Project Link
[GitHub Repository](https://github.com/danartech/Maven-Movies-Business-Intelligence-Project)
