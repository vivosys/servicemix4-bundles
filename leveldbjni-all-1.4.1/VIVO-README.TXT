vivosys repository: git@github.com:vivosys/servicemix4-bundles.git
branch: leveldbjni-all-vivo-local
URL https://github.com/vivosys/servicemix4-bundles/tree/leveldbjni-all-vivo-local

1. Add upstream repository

    git add upstream git@github.com:apache/servicemix4-bundles

2. Switch to the proper branch

    git checkout leveldbjni-all-vivo-local

3. Deploy

    REPO_ID=vivosys-repo
    REPO_URL=https://tools.vivosys.com/artifactory/ext-release-local
    mvn \
      -Dgpg.skip \
      -DaltDeploymentRepository=$REPO_ID::default::$REPO_URL \
      source:jar javadoc:jar deploy
