First, I created an angular project using ng cli 

Then, I just run build and rsync it to this repo 

that's it! 


```bash 
cd ~/src/qlstudent;
ng build --aot=true --prod --build-optimizer --verbose --progress=true --deploy-url="qlstudent.github.io" --delete-output-path --extract-licenses --subresource-integrity --stats-json;
rsync -av /home/qlstudent/src/qlstudent/dist/ /home/qlstudent/src/site;
cd /home/qlstudent/src/site/qlstudent/;
git add .;
git commit -S;
git push origin master;
```

