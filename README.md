# NmapVis

## About

NmapVis is a super simple web GUI for importing and displaying nmap xml scan results.

![image](https://user-images.githubusercontent.com/696230/76523028-0f8efb00-643e-11ea-9537-36c4b8680d9d.png)

![Screen Shot 2020-03-12 at 8 43 51 AM](https://user-images.githubusercontent.com/696230/76522822-a1e2cf00-643d-11ea-9e1c-408703f4911e.png)

## Deploy

Build and run with Docker. Clone this repo, then from main directory:

```
docker build -t nmapvis .
docker run -d --name nmapvis -p 3000:3000 nmapvis
```

Then go to [http://localhost:3000/](http://localhost:3000/) in your browser.

## Usage

The UI *should* be intuitive, but if not:

- Click `Upload nmap scan results` button to import an nmap results xml file.
- Exit import modal and results will populate.
- Click an IP to filter results by specific IP.

## nmap xml results file

This application assumes you've run an nmap scan on a list of ips, e.g. `ips.txt`, with an nnmap command like the following:

```
nmap -Pn -p80,443,8443,4000,8000 -iL ips.txt -oA nmap-ouput -vvvvv
```
