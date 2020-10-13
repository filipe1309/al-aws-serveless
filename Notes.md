aws s3 sync . s3://fa-imagens-dotr

aws rekognition create-collection --collection-id "faces"

aws rekognition list-collections

aws rekognition list-faces --collection-id faces

aws s3 cp _analise.png s3://fa-imagens-dotr