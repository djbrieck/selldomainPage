# sell domain without dedicated hosting using IPFS 

This is a basic project used to create a landing page for selling a domain that you own, without dedicated hosting. This will use IPFS to host.

General high level summary of what you will need to do in one place.
 
1. Get IPFS set up, install the Command line. ipns://ipfs.io/#install

2. Check out this project, and modify to suite your domain that is for sale.

3. Add your index.html file to ipfs. http://docs.ipfs.io.ipns.localhost:48084/reference/cli/#ipfs-add

4. Set up a ipns to reference your file. http://docs.ipfs.io.ipns.localhost:48084/concepts/ipns/#example-ipns-setup-with-cli

5. Set up your domain to forward to your ipns address.

6. Verify you and others can see your page.

7. Pin your file remotely on a pinning service.

I found that setting up the API was the only way to pin the ipns address on Pinata. Otherways never seemed to stick, would just time out and never add the files. See pinata docs on how to set up the api. 
Then you will run a command line like the following. 

ipfs pin remote add /ipns/yourAddressHere --service=pinata

8. Shut down your local IPFS and verify your page is still loading.
