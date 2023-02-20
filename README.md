<h2>Go Web Scarper</h2>
<p>This Go program uses the <code>gocolly</code> package to scrape product data from a website. The program takes in a URL for the website to scrape and an output format (either CSV or JSON), and outputs a file with the scraped data in the specified format.</p>
<p>The program first defines a struct called <code>Product</code> to represent a product on the website. The <code>Product</code> struct has fields for the name, price, details, brand, description, image URL, and availability of the product.</p>
<p>The program then parses command-line arguments using the <code>flag</code> package, and checks that the website URL is specified. It initializes a new <code>Collector</code> from the <code>gocolly</code> package, which limits the rate at which requests are made to the website to avoid overloading it. The program also creates a file to store the scraped data, using either a CSV writer or a JSON encoder depending on the specified output format.</p>
<p>The program sets up request handlers for the list of products and the "next" link, and an error handler to handle any errors that occur during scraping. It starts the scraper by visiting the first page of the website, and waits for all the requests to finish before signaling that it is done.</p> 
<p>Once the program has finished scraping the website, it writes the scraped data to the specified output file in the specified format. If the output format is CSV, it writes the data to a CSV file using the CSV writer. If the output format is JSON, it writes the data to a JSON file using the JSON encoder.</p>
  </body>
</html>
