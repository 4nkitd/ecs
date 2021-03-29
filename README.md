# ecs | Easy Code Snippets

## language : javascript

fun / function : will generate a function with try catch

```javascript

const fun_name = async (req, res) => {
    try {

        var name = req.body.name;

    } catch (error) {

        var log = " file:index.js @  line:1  | fun_name |-> ${JSON.stringify(error)} "
       // logger.log('Error', log);

        return res.json({
                status: false,
                error: 'Unknown Error Ocurred',
        });

    }
};

```

## language : php
fun / function : will generate a const assigned function with try catch, async, await, public, private

eg.

```php


public function fun_name(Request $request){

try {

    $input = $request->all();

    $validator = Validator::make($input,[
        'name'=>'required',
    ]);

    if($validator->fails()){
        $resp = [ 
            'status'=> false, 
            'error'=> $validator->errors()
            ];
        return response()->json($resp);
    }

    $resp = [];

    return response()->json($resp, 200);

} catch (Throwable $e) {

    // remember to add logs

    $resp = [ 'status'=> false, 'error'=> $e->getMessage()];
    return response()->json($resp);

}

```