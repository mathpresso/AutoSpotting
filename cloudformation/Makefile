all: upload

install:
		cp stacks/AutoSpotting/template.yaml ../build/s3/custom/

upload: install
		aws s3 sync ../build/s3/ s3://mathpresso-infra/autospotting/

create:
		clouds --region us-east-1 update -c AutoSpotting -ew

update:
		clouds --region us-east-1 update AutoSpotting -ew

