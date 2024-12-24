# ML-Driven-Optimization-of-Childcare-Allocation-and-Labor-Demand
This is the result of a project that utilized and applied public data related to childcare centers and labor (job opening, job search) to machine learning algorithms.

This result was also applied to the "2024 National Happiness Service Discovery and Entrepreneurship Contest" hosted by the Korea Social Security Information Service and was selected as the final entry.

Contest Link

Motivation
In a situation where orphanage leavers and those requiring guardians continue to experience economic difficulties, and in South Korea, where labor shortages are worsening as we enter a super-aging society, the introduction of a job matching system for orphanage leavers is an urgent task.

Output
Step 1. Data Curation (Reference to Data Source)

Step 2. Data Preprocessing (Reference to Algorithm)

Step 3. Modeling

#1. Perform regional latitude/longitude-based clustering using the KMeans algorithm
그림1

#1. Using K-Means algorithm
#2. Perform clustering based on cluster latitude/longitude and labor values
그림2

Step 4. Analysis and visualization

By looking at the visualized data, you can see which regions have a low labor demand ratio (Red and green areas represent high and low labor demand, respectively).
Therefore, population should be allocated to these regions first.
그림3
Step 5. Childcare facility matching

Distance calculation

The figure below shows the step for calculating the distance between child care facilities and labor demand areas.
그림4

Ranking calculation
그림5

This figure shows ranking calculations based on distance and labor demand ratio. Each cluster is ranked, which helps determine which areas should receive priority attention for employment placement.

The value in the “노동수치_군집” column represents the unique number of each cluster, and the value in the “배치” column represents the rank in which each cluster will be assigned labor. For example, Cluster 0 ranks 81st to receive labor.

Final result

The figure below is 3 childcare centers closest to cluster number 49 as an example.
(The value in the “노동수치 군집 번호, 보육 시설, 거리” column means Labor figures "Cluster number, childcare facilities, distance".)
스크린샷 2024-06-16 오후 11 46 19

Algorithm
스크린샷 2024-06-15 오후 4 55 54

In the case of clustering, K-Means Clustering was used. For distance calculation, KNN (K-Nearest Neighbors) was employed. Data preprocessing was conducted using job opening and job search data from each region.

Labor Demand Ratio: This was calculated by dividing the number of job searches by the number of job openings. A lower value indicates a more severe labor supply shortage.
Required Workforce: This is an additional column added arbitrarily, representing the number of workers needed by subtracting the number of job searches from the number of job openings.
👥 Team Member
201934219 Kim Joonhee

202031503 Kang Jiwon

202034305 Kim Dabin

202031512 Kim Minjae

✔️ Data Source
Childcare Facility Data

Status of child welfare facilities in 2022. (Ministry of Health and Welfare): Data Link
List of Child Welfare Facilities in Seoul (Source: Seoul Open Data Plaza): Data Link
Status of Child Care Facilities (Source: Gyeonggi Data Dream): Data Link
Busan Child Care Facilities (Source: Public Data Portal): Data Link
Daegu Child Welfare Facilities (Source: Daegu Metropolitan City Website): Data Link
Incheon Metropolitan City_Child Welfare Facilities (Statistics)_20221231 (Source: Public Data Portal): Data Link
Gwangju Metropolitan City_Child Care Facilities Status_20231124 (Source: Public Data Portal): Data Link
Daejeon Child Care Facilities (Source: Daejeon Metropolitan City Child Association of Child Welfare): Data Link
Sejong Child Welfare Facilities Status (As of April 2023) (Source: Sejong City): Data Link
Chungcheongbuk-do Child Welfare Facilities (Source: Chungcheongbuk Province Government): Data Link
Chungcheongnam-do Child Care Facilities (Source: adongbokji): Data Link
Jeollanam-do Child Care Facilities (Source: Jeonnam Association of Child Welfare): Data Link
Gyeongsangbuk-do_Child Care Facilities Status_20231208 (Source: Public Data Portal): Data Link
Gyeongsangnam-do_Child Care Facilities_20221231 (Source: Public Data Portal): Data Link
Gangwon-do Child Care Facilities (Source: Korea Child Welfare Facilities): Data Link
Jeju Special Self-Governing Province_Child Care Facilities Status_20230803 (Source: Public Data Portal): Data Link
Jeollabuk-do Child Care Facilities (Source: adongbokji): Data Link
Number of Children in Need by Gender and Placement (202201~202212) (Source: Bokjiro): Data Link
Labor-related Data

Labor market status_recruitment_recruitment, job search, placement, employment status (Source: Korea Employment Information Service) Data Link
