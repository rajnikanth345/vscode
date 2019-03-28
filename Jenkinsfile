node {
    stage ('update')
    {
        sh 'sudo apt-get install git -y'
    }
    stage ('checkout')
    {
        git 'https://github.com/Microsoft/vscode.git'
    }
     stage ('nodejs install')
    {
        sh 'sudo wget https://nodejs.org/dist/v10.15.3/node-v10.15.3-linux-x64.tar.xz'
        sh 'sudo tar -xvf node-v10.15.3-linux-x64.tar.xz'
        sh 'cd node-v10.15.3-linux-x64'
        sh 'sudo cp -rf /home/ubuntu/node-v10.15.3-linux-x64/bin/* /usr/bin/'
        sh 'sudo cp -rf /home/ubuntu/node-v10.15.3-linux-x64/include/* /usr/include/'
        sh 'sudo cp -rf /home/ubuntu/node-v10.15.3-linux-x64/share/* /usr/share/'
        sh 'sudo cp -rf /home/ubuntu/node-v10.15.3-linux-x64/lib/* /usr/lib/'
        sh 'nodejs --version'
    }
     stage ('yarn install')
    {
        sh 'sudo curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -'
        sh 'echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list'
        sh 'sudo apt-get update'
        sh 'sudo apt-get install yarn -y'
        sh 'yarn --version'
    }  
    stage ('install pkg-config')
    {
        sh 'sudo apt-get install pkg-config'
    }
    stage ('install gcc')
    {
        sh 'sudo apt-get install -y software-properties-common'
        sh 'sudo add-apt-repository ppa:ubuntu-toolchain-r/test'
        sh 'sudo apt update'
        sh 'sudo apt install g++-7 -y'
        sh 'gcc --version'
    }
    stage ('install native-keymap')
    {
        sh 'sudo apt-get install libx11-dev libxkbfile-dev'
    }
    stage ('install keytar')
    {
        sh 'sudo apt-get install libsecret-1-dev'
    }
    stage ('install npm packages')
    {
        sh 'sudo apt-get install fakeroot rpm'
    }
}
