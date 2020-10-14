# How-To fix terminology issues in the Jenkins docs

Defined below process shows one of possible ways contributing to the Jenkins project. It involves submitting pull request after fixing terminology [issue #3862](https://github.com/jenkins-infra/jenkins.io/issues/3862). You may see below specific steps of the entire process.

## Steps to Execute This Process

- Pick up an issue from [jenkins.io issues](https://github.com/jenkins-infra/jenkins.io/issues)
  and notify community you are going to work on this issue.

- (Optional) Fork [jenkins-infra/jenkins.io](https://github.com/jenkins-infra/jenkins.io)

- (Optional) Clone your repo by using e.g. SSH method:

            git clone git@github.com:jenkins-infra/jenkins.io.git
            cd jenkins.io

- (Optional) Sync your repo if it is not even with jenkins-infra:master.

            hub sync
            git push

- Create a new github branch dedicated to fixing selected issue. This complies with DevOps Best Practices.

            git checkout -b fix-dev-doc

- Replace whitelist with allowlist for every file in the selected set of files. Be careful!

- Build your static local site by executing:

            make run

- Do simple visual testing of your modifications by exploring [localhost:4242](localhost:4242)

- Push modified content to yur repo on Github:

            git status
            git add ./content/
            git commit -am "Fixed terms in 'Development' Docs"
            git push

- Open your jenkins.io repo and submit pull request, asking to merge your modifications into master branch of [jenkins-infra/jenkins.io](https://github.com/jenkins-infra/jenkins.io). Don't forget to say that you PR "fixes #3862". Wait for PR approval, sussefull tests completion and the final merge notifications.  Most likely you'll receive those in email.
