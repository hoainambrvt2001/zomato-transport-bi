# Data dictionary / Từ điển dữ liệu

The project combines two public Kaggle datasets, plus external operating signals
(weather, traffic) described in the report.

## Datasets

| Dataset | Author (Kaggle) | Grain | Used by |
|---------|-----------------|-------|---------|
| Zomato Delivery Operations Analytics Dataset | Saurabh Badole | One row per delivery order | BR1, BR2, BR3, BR5–6 |
| Zomato Bangalore Restaurants | Himanshu Poddar | One row per restaurant | BR4, BR7 |

---

## Delivery‑operations data / Nhóm dữ liệu vận hành giao hàng

| Field group | Fields (examples) | Description |
|-------------|-------------------|-------------|
| Driver / shipper | driver ID, age, rating | Driver identity and performance rating |
| Location | restaurant latitude/longitude, delivery latitude/longitude | Pickup and drop‑off coordinates |
| Order timing | order date, order time, pickup time | When the order was placed and picked up |
| Operating conditions | weather conditions, traffic density, vehicle condition | Environmental factors affecting delivery |
| Order attributes | order type, vehicle type, multiple‑deliveries flag | Characteristics of the order |
| Special events | festival flag | Whether the order occurred during a festival |
| Area | city / city type | Area classification |
| Performance | time taken (minutes) | Total delivery time — the BR3 target |

## Restaurant data / Nhóm dữ liệu nhà hàng

| Field group | Fields (examples) | Description |
|-------------|-------------------|-------------|
| Basic info | url, name, address | Restaurant identity |
| Online services | online order, table booking | Whether online order / booking is supported |
| Ratings & reviews | average rating, votes, reviews list | Customer feedback signals |
| Contact & activity | phone, location, restaurant type, favourite dish | Contact and operating attributes |
| Cost | approx. cost for two | Estimated cost for two people |
| Menu | menu item list, cuisine types | Available dishes and cuisines |
| Area grouping | listed‑in (neighbourhood / area) | Restaurant area within the city |

## External signals / Dữ liệu bên ngoài

| Source | Fields | Used for |
|--------|--------|----------|
| Weather | temperature, cloud cover, rainfall, wind speed, update time | BR3 — delivery‑time prediction |
| Traffic | traffic density | BR2, BR3 — zoning and ETA |

> Field names above are summarized from the project report. Exact column names follow the
> original Kaggle datasets and the cleaned versions loaded inside each notebook.
