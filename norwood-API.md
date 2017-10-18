a**Title**
----
  <_Additional information about your API call. Try to use verbs that match both request type (fetching vs modifying) and plurality (one vs multiple)._>

* **URL**

  https://o3krin2rid.execute-api.us-east-1.amazonaws.com/prod/norwood

* **AUTHENTICATION**

  The API key provided, send it in the header `x-api-key`

* **Method:**

  `POST`

* **Data Params**

   **Required:**

   `firstName=[string]`

   `lastName=[string]`

   `phoneNumber=[string]`

   `optIn=[string]`

   `email=[string]`

   **Optional:**

   `title=[string]`

* **Success Response:**

  <_What should the status code be on success and is there any returned data? This is useful when people need to to know what their callbacks should expect!_>

  * **Code:** 200 <br />
    **Content:** `{"userId":"USER-SUB-1234","noteId":"f4db15c0-b3e9-11e7-bfdc-959b75ce137a","title":"Mr.","firstName":"Daniel","lastName":"Chen","phoneNumber":"4162501432","email":"daniel@norwoodsolutions.com","optIn":"true","createdAt":1508320307484}`

* **Error Response:**

  <_Most endpoints will have many ways they can fail. From unauthorized access, to wrongful parameters etc. All of those should be liste d here. It might seem repetitive, but it helps prevent assumptions from being made where they should be._>

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Error Message" }`

  OR

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "Error Message" }`

* **Sample Call:**

  curl -H "Content-Type: application/json" -X POST -d '{"firstName":"Daniel","lastName":"Chen","title":"Mr.","phoneNumber":"4162501432","email":"daniel@myshyft.com","optIn":"true"}' https://o3krin2rid.execute-api.us-east-1.amazonaws.com/prod/norwood
