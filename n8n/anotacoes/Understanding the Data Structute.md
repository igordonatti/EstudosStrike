# Understanding the data structura
## Data structe of n8n
In a basic sense, n8n nodes function as an Extract, Transform, Load (ETL) tool. The nodes allow you to access (extract) data from multiples disparate sources, modify (transform) the data in a particulas way, and pass (load) it along to where it needs to be.

### Data structures in n8n
![Data structures in n8n](image.png)

## Transforming Data
- To create multiple items from a single item, you can use this JavaScript code:
```
return $input.all().map(item => {
  return {
    json: item
  }
})
```

- To create a single item from multiple items, you can use this JavaScript code:
```
return [
  {
    json: {
      data_object: $input.all().map(item => item.json)
    }
  }
]
```

## HTML and XML data
If you need to process HTML or XML data un yout n8n workflows, use the *HTML node* or the *XML node*.

Use the **HTML node** to extract HTML content of a webpage by referencing CSS selectors. This is useful if you want to collect structured information from a website (web-scraping).  

## Date, time and interval data
There are a few ways you can work with dates and times:
- Use the **Date & Time node** to convert date and time data to different formats and calculate dates.
- Use **Schedule Trigger node** to schedule workflows to run at a specific time, interval, or duration.

## Binary Data
In n8n, you can process binary data with the following nodes:
- *HTTP Request* to request and send files from/to web resources and APIs.
- *Read/Write files from Disk* to read and write files from/to the machine where n8n is running.
- *Convert to File* to take input data and output it as a file.
- *Extract from File* to get data from a binary format and convert it to JSON.

## Looping
There are some *exception of nodes and operations* that will require you to build a loop into your workflow.

To *create a loop in an n8n workflow*, you need to connect the output of one node to the input of a previous node, and add an **if node** to check when to stop the loop.

## Splitting data in batchs
If you need to process large volumes of incomid data, execute the **Code node** multiple times, or avoid API rate limits, it's best to split the data into batches (groups) and process these batches.

