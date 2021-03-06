# API Design Workshop


## Requirements

- Read [Adidas API Guidelines](https://adidas-group.gitbooks.io/api-guidelines/content/)
- [Draw.io](https://www.draw.io/)
- Git
- Code editor
- Docker 


## Setup

1. Fork this repo and pull in your local machine

2. Edit and check the swagger file `swagger.yaml`

3. Build the api image

This is only needed if you want to try the implementation of the designed API + API contract testing

```
make build
```

4. Run the API

```
make run
```


## Design challenge

As a new assignement you are asked to add a wishlist feature to our adidas ecom (website, native apps).

You've decided wisly to think [API First](https://adidas-group.gitbooks.io/api-guidelines/content/core-principles/api-first.html) and [API Design First](https://adidas-group.gitbooks.io/api-guidelines/content/core-principles/design-maturity.html).

You've assigned 4 user stories:

- As a user, I want to add a product in my wishlist
- As a user, I want to retrieve my wishlist
- As a user, I want to delete a specific product from mt wishlist
- As a user, I want to clear my wishlist


## Existing affordances (actions)

The existing core Product API privides this affordances:

- Retrieve the list of products
- Retrieve a single product
- Create a product
- Update an existing product (status...)
- Retrieve reviews about a product
- Add a product review
- Create a user
- Retrieve user profile


## Step1. Let's describe what actions our API affords

**TASK**: List the new API affodrances



## Step2. Let's draw!

> The state machine diagram will help you to identify the main REST ressources and their relations.

**TASK**: In this step we extend an existing state diagrams for the proposed API. Each box in the diagram represents a possible representation. You can use arrows to indicate transitions from one box to the next.

![Product API](./product_draw.png)

- Open this [link](https://www.draw.io/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1#G1PrwwIysZV_unl5e8lXabjLYzwA2hAQUq)
- Edit the diagram



## Step3. Formalize the design in the [Open API Specification](http://swagger.io/specification/)

> The OAS file can be edited in whatever tool you like *BUT NOT GENERATED FROM YOUR CODE*, the most important thing is that the aprouved one (the contract) *MUST* be in Apiary.

**TASK**: Extend the existing swagger.yaml



## Step4. Verify the design using Apiary Documentation and Apiary Mock Service

**TASK**: Try the Apiary mock service



## Step5. Review the API Design

At this stage you:

- Ask feedback from your API users by sending them the documentation link.
- Ask feedback from your product owner

If your API looks like this remote control then your design is affordant!

![Grandma Remote control](https://raw.githubusercontent.com/Amzani/api-lifecycle-tutorial/master/img/remote.webp)



## Step6. Sync your API contract

> Every API description MUST be published in adidas API design platform (apiary.io) and SHOULD be stored in version control system (Bitbucket, GitHub) in the same repository as the API implementation.

**TASKS**:

- Host your API in github
- Setup up Github/apiary Sync


## Step7. Setup API contract testing

>Every API description (contract) using HTTP(S) protocol MUST be tested against its API implementation. The tests MUST be executed using the Dredd testing framework. The Dredd MUST report the test results to Apiary. In addition to local runs, the tests SHOULD be an integral part the API implementation's CI/CD pipeline. The CI/CD pipeline SHOULD be configured to run the test whenever there is a change to either API description (contract) or its implementation.

- **TASK**: Install and run [dredd](https://github.com/apiaryio/dredd)


## Some example of bad designed APIs

### [[Sales and Distribution] Returns Confirmation API](https://returnsconfirmation.docs.apiary.io/)
Missing description
Missing examples
Missing HAL
Exposing internal model
Missing support contact

### [ATP Notification Service](https://atpnotificationservice.docs.apiary.io/)
Usage of acronyms, what's ATP stands for ?
Missing description / context
Missing HAL
Missing support contact


## Some example of good designed APIs

Sample APIs following the guidelines are available at [adidas-group GitHub](https://github.com/adidas-group). The samples include the following:


### [Simple API](https://github.com/adidas-group/demo-simple-api)
Very simple API including implementation, testing, and full CI/CD lifecycle.

### [Approval API](https://github.com/adidas-group/demo-approval-api)
Real-world API with state transition, API key client app authentication, exposed via API management.

### [Orders API](https://github.com/adidas-group/demo-orders-api)
Sample API used as the template for newly created projects at Apiary.

### [Inventory API](https://eainventoryapi.docs.apiary.io/)
Real-world Adidas Inventory API (WIP)

### [Appointment Service](https://github.com/adidas-group/demo-appointment-service)
Demo API, including implementation and testing used during training.

### [Complex Search Parameters](https://github.com/adidas-group/demo-complex-search)
Sample API showcasing description of complex query parameter rules.

### [CPM] Asset Trafficker https://assetmanager4.docs.apiary.io/






