# Get Started with Looker: Challenge Lab || [ARC107](https://www.cloudskillsboost.google/focuses/61470?parent=catalog) ||

### Log in to Google Cloud Console using Credentials

* Create a new [Looker Studio](http://lookerstudio.google.com/)
  
### go to `Blank Report` > select country as `INDIA` and any company name > check `Terms of service` > and `Continue` > `No to all` > Continue

### click `Blank Report` > cross it > Click Untitled Report in the top left corner of your screen and name your report > report named `Online Sales`

### Click on `Add Data` > Search `BigQuery` > `Authorize` > click on ID > From the left menu, click `Public Datasets` > ***`Your Project ID`*** > `thelook_ecommerce` > `orders` .

### Click `ADD` > click `Add to report`



## Click `Open Looker` > Click `Log In` 

### First, on the bottom left of the Looker User Interface, click the toggle button to enter Development mode.


![Development](development.jpg)



### ***In the `Looker navigation menu`, Click the `Develop` tab and then select the `qwiklabs-ecommerce`.***

### ***Click the 3dots of `Views` > Select `Create View` > Name the file ***```users_region```*** > Click `Create`***

### Replace the follwing
```
view: users_region {
  sql_table_name: cloud-training-demos.looker_ecomm.users ;;
  
  dimension: id {
    type: number
    sql: ${TABLE}.id ;;
    primary_key: yes
  }
  
  dimension: state {
    type: string
    sql: ${TABLE}.state ;;
  }
  
  dimension: country {
    type: string
    sql: ${TABLE}.country ;;
  }
  
  measure: count {
    type: count
    drill_fields: [id, state, country]
  }
}
```
## Click `Save Changes` 

### ***In the file browser, under the `models` folder, select ```training_ecommerce.model``` file.***

### Replace the follwing in `training_ecommerce.model` file:
```
connection: "bigquery_public_data_looker"

# include all the views
include: "/views/*.view"
include: "/z_tests/*.lkml"
include: "/**/*.dashboard"

datagroup: training_ecommerce_default_datagroup {
  # sql_trigger: SELECT MAX(id) FROM etl_log;;
  max_cache_age: "1 hour"
}

persist_with: training_ecommerce_default_datagroup

label: "E-Commerce Training"

explore: order_items {
  join: users {
    type: left_outer
    sql_on: ${order_items.user_id} = ${users.id} ;;
    relationship: many_to_one
  }

  join: inventory_items {
    type: left_outer
    sql_on: ${order_items.inventory_item_id} = ${inventory_items.id} ;;
    relationship: many_to_one
  }

  join: products {
    type: left_outer
    sql_on: ${inventory_items.product_id} = ${products.id} ;;
    relationship: many_to_one
  }

  join: distribution_centers {
    type: left_outer
    sql_on: ${products.distribution_center_id} = ${distribution_centers.id} ;;
    relationship: many_to_one
  }
}

explore: events {
  join: event_session_facts {
    type: left_outer
    sql_on: ${events.session_id} = ${event_session_facts.session_id} ;;
    relationship: many_to_one
  }
  join: event_session_funnel {
    type: left_outer
    sql_on: ${events.session_id} = ${event_session_funnel.session_id} ;;
    relationship: many_to_one
  }
  join: users {
    type: left_outer
    sql_on: ${events.user_id} = ${users.id} ;;
    relationship: many_to_one
  }
  join: users_region {
    type: left_outer
    sql_on: ${events.user_id} = ${users_region.id};;
    relationship: many_to_one
  }
}
```

### Click `Save Changes` >

### 1. Click **`Validate LookML`**.
### 2. Click **`Commit Changes & Push`**.
### 3. Add any commit message and click **`Commit`**.
### 4. Lastly, click **`Deploy to Production`**.




## In the `Looker navigation menu`, click `Explore` > Under `E-Commerce Training` > select `Events` > Under `Events` > Click `Event Type` > Under `Users Region` > Click `Count`

### Hover `Users Region Count` and make it `Descending` > Row Limit `3` 

### Click the arrow next to `Visualization` to expand the window > Click the `Bar` icon

### Click on the `settings gear icon` (settings gear icon) next to `Run`, and select `Save` > To an `existing dashboard` > Enter a title for the visualization: `top 3 event types based on the highest number of users` > Click `New Dashboard` > Enter a title for the new dashboard: `User Events` > Click `OK` > Click `Save to Dashboard`

### Congratulations 🎉 for completing the Lab !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

