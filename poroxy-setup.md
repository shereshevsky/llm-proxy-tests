1. Follow the installation instructions on the [website](https://mitmproxy.org/)

2. Start the interactive UI by running mitmweb in the terminal. Pay attention to the url of the interactive UI in the logs which will look something like this: Web server listening at http://127.0.0.1:8081/

3. Next, you need to configure your device (i.e. your laptop) to route all traffic through mitproxy, which listens on http://localhost:8080. Per the documentation:
4. Next, navigate to http://mitm.it and it will give you instructions on how to install the mitmproxy Certificate Authority (CA), which you will need for intercepting HTTPS requests. (You can also do this manually [here](https://docs.mitmproxy.org/stable/concepts-certificates/#quick-setup).) Also, take note of the location of the CA file as we will reference it later.
5. You can test that everything works by browsing to a website like https://mitmproxy.org/, and seeing the corresponding output in the mtimweb UI which for me is located at http://127.0.0.1:8081/ (look at the logs in your terminal to get the URL).
6. Now that you set everything up, you can disable the proxy that you previously enabled on your network. I do this on my mac by toggling the proxy buttons in the screenshot I showed above. This is because we want to scope the proxy to only the python program to eliminate unnecessary noise.