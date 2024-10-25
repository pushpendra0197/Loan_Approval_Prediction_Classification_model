I have made Loan_Approval_prediction model after checking with all classification supervised machine learning algorithm and chose best accuracy given algorithm.and deployed over Modelbit deployment platform.

Model is accessible from anywhere.
Kindly install modelbit in your IDE(jupyter,colab) by using (pip install modelbit) import modelbit module.



Command for Curl-


curl -s -XPOST "https://pushpendradhamanya.us-east-2.aws.modelbit.com/v1/Loan_Approval_Predictor/latest" -d '{"data": [age, gender, marital_status, income, credit_score]}' | json_pp

Python-

modelbit.get_inference(
  region="us-east-2.aws",
  workspace="pushpendradhamanya",
  deployment="Loan_Approval_Predictor",
  data=[age, gender, marital_status, income, credit_score]
)


Enter the value according -- "Male":1,"Female":0,"Married":0,"Single":1 in data field.
Model will show you status of your loan by "Approved":1,"Denied":0.

