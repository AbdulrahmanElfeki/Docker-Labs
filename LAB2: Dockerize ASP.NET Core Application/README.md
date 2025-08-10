## Requirements
Install .NET from https://dotnet.microsoft.com/en-us/download/dotnet

# Create .NET application
`dotnet new mvc --name hrapp --output dockerhrapp`

# Build the image
`cd dockerhrapp && docker build -t dockerhrapp .` 
<img width="1550" height="760" alt="image" src="https://github.com/user-attachments/assets/97d98a46-c3e2-449d-8cb3-7dfa840bb62c" />

# run container from Dockerfile
`docker run -d -p 8080:8080 --name hrapp dockerhrapp`
<img width="882" height="54" alt="image" src="https://github.com/user-attachments/assets/2ead7868-f8c3-4da4-a3b6-5df9dd7bbaa4" />
<img width="1919" height="903" alt="image" src="https://github.com/user-attachments/assets/94203229-f7b6-46ad-9797-ad264c59552f" />
