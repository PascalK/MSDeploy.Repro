MSDeploy.Repro
==============

Example project to reproduce an MSDeploy error

Commands:
Build / Package:
msbuild /nologo /t:Package /p:Configuration=Release Test.Web.csproj

Deploy:
msdeploy -verb:sync -source:package=Test.Web.zip -dest:auto -setParamFile=Test.Web.SetParameters.xml
msdeploy -verb:sync -source:package=Test.Web.zip -dest:auto=computerName=https://localhost:8172/msdeploy.axd,authType=NTLM -setParamFile=Test.Web.SetParameters.xml
