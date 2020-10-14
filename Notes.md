aws s3 sync . s3://fa-imagens-dotr

aws rekognition create-collection --collection-id "faces"

aws rekognition list-collections

aws rekognition list-faces --collection-id faces

aws s3 cp _analise.png s3://fa-imagens-dotr

python faceanalise.py

aws s3 sync . s3://fa-site-dotr

aws lambda update-function-code --function-name faceAnalise --zip-file fileb://faceanalise.zip

aws lambda publish-version --function-name faceAnalise

aws lambda create-alias --function-name faceAnalise --function-version 1 --name PROD 