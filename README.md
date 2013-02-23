Bootstrap-AcknowledgeInputs
===========================

A small bootstrap plugin that provide form input controls that feedback to the user as to whether their input was valid.

Using Bootstrap-AcknowledgeInput.js
===================================

1. Make sure you include all the required files:
    
    ```html
    <html lang="en">
        <head>
            <link rel="stylesheet" href="css/bootstrap.min.css">
            <link rel="stylesheet" href="css/font-awesome.min.css"> <!-- optional but recommended -->
        </head>
        <body>
            <!-- PAGE CONTENT -->
            <script type="text/javascript" src="js/jquery-1.9.1.min.js"></script>
            <script type="text/javascript" src="js/bootstrap.min.js" ></script>
            <script type="text/javascript" src="js/bootstrap-acknowledgeinput.min.js" ></script>
        </body>
    </html> 
    ```

2. Define your form with new acknowledge inputs

    ```html
    <form>
        <label>Username</label>
        <div class="input-append" data-role="acknowledge-input">
            <input type="text" required="required" placeholder="Any Text Required" data-type="text" />
            <div data-role="acknowledgement"><i></i></div>
        </div>
    </form>
    ```

    The key things to note here is the use of `data-role` and `data-type` (optional). <br/>
    The `data-type` attribute tells the plugin what format the input text should be to warrant a success.<br/>
    The current `data-type` options are `text` (default), `email` and `tel`.

3. Call the plugin on document ready

    ```html
    <script type="text/javascript">
        $().ready(function() {
            $().acknowledgeinput();
        });
    </script>
    ```
