# Business requirements / Yêu cầu nghiệp vụ

This document details the eight business requirements (BR) that frame the project.
Stakeholders were grouped into five groups: the **delivery fleet**, **customers**,
the **HR department**, the **product/marketing department**, and **operations
management**.

| # | Requirement (VI) | Requirement (EN) | Primary stakeholder | Deliverable |
|---|------------------|------------------|---------------------|-------------|
| BR1 | Phân nhóm tài xế | Driver segmentation | Operations / Fleet | `notebooks/br1-driver-segmentation.ipynb` |
| BR2 | Phân vùng giao hàng | Delivery zoning | Operations | `notebooks/br2-delivery-zoning.ipynb` |
| BR3 | Dự đoán thời gian giao hàng | Delivery‑time prediction | Operations / Customers | `notebooks/br3-delivery-time-prediction.ipynb` |
| BR4 | Phân khúc khách hàng | Customer segmentation | Marketing | `notebooks/br4-customer-segmentation.ipynb` |
| BR5 | Tối ưu hóa quy trình tuyển dụng | Recruitment optimization | HR | `notebooks/br5-6-recruitment-and-demand-forecasting.ipynb` |
| BR6 | Dự đoán nhu cầu mua và đặt hàng | Purchase / order‑demand forecasting | Operations / Management | `notebooks/br5-6-recruitment-and-demand-forecasting.ipynb` |
| BR7 | Dự đoán sự thành công của nhà hàng | Restaurant‑success prediction | Management / Partners | `notebooks/br7-restaurant-success-prediction.ipynb` |
| BR8 | Giám sát vận hành giao hàng | Real‑time delivery‑operations monitoring | Management | `dashboard/zomato-bi-dashboard.pbix` |

---

## BR1 — Driver segmentation / Phân nhóm tài xế

Segment drivers based on performance criteria to support rewards and fair order
allocation, optimizing fleet resources and motivating drivers.
**Technique:** K‑Means clustering (elbow method via `kneed`).

## BR2 — Delivery zoning / Phân vùng giao hàng

Partition the operating area into delivery zones so drivers can be assigned by region,
optimizing routes and reducing delivery time.
**Technique:** K‑Means on geographic coordinates, visualized with Folium maps.

## BR3 — Delivery‑time prediction / Dự đoán thời gian giao hàng

Predict delivery time from factors such as weather, traffic density and vehicle type to
make more accurate delivery commitments to customers.
**Technique:** Regression models.

## BR4 — Customer segmentation / Phân khúc khách hàng

Segment customers by ordering behaviour to personalize the experience and recommend
relevant services, improving satisfaction and retention.
**Technique:** RFM features + K‑Means clustering.

## BR5 — Recruitment optimization / Tối ưu hóa quy trình tuyển dụng

Optimize driver recruitment by classifying candidate age and profile against job
requirements to speed up and improve hiring decisions.
**Technique:** Classification.

## BR6 — Demand forecasting / Dự đoán nhu cầu mua và đặt hàng

Forecast purchasing and order demand to support inventory and operational planning.
**Technique:** Forecasting / regression.

## BR7 — Restaurant‑success prediction / Dự đoán sự thành công của nhà hàng

Predict and score restaurant success to set quality standards, encouraging partner
restaurants to improve and raising customer satisfaction.
**Technique:** Gradient‑boosted trees (XGBoost / LightGBM) with SHAP explainability.

## BR8 — Operations monitoring / Giám sát vận hành giao hàng

Provide a real‑time monitoring dashboard over the whole delivery chain to surface risks
quickly and optimize end‑to‑end performance.
**Deliverable:** Power BI dashboard (`dashboard/zomato-bi-dashboard.pbix`).
