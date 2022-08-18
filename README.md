## Installing Scala and scala script oacking using sbt 

### Steps: 
- Install sbt 
- Update the build.sbt file with required spark versions, dependencies 
- Run `/usr/local/bin/sbt assembly` (`where sbt`) to determine the sbt installation folder
- Once build complete successfully, should be able to find the `.jar` file under respective `target` directory 
- Try running the generated `.jar` file with spark-submit either in the cluster or locally installation of Spark (make sure of same spark version installation here !)
- Rename the `.jar` as required, here we are maintaining as `wordcount-assembly.jar` 
`

## Now that we have setup the `.jar` file, spin up the docker compose for the spark cluster
`docker-compose up -d` 

## Once Spark cluster is up in the docker-compose, get into spark-master container 
## Run below script (assuming all dependencies are handled in the docker-compose mounts )
`bin/spark-submit wordcount-assembly.jar`
