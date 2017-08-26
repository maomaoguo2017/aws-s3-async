# aws-s3-async

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](https://github.com/DevStarSJ/aws-s3-async/blob/master/LICENSE)

AWS S3 helper package for async. (callback-style functions to async functions)

I will add them one by one if necessary.
Not all features are implemented.
I will also provide additional convenience features.

## install

```
npm install aws-s3-async --save
```

## Implemented Features

- `getObjectAsync(params: GetObjectRequest, fileName: string): Promise<string>`

```TypeScript
const FILE_NAME = "/tmp/temp.jpg";
await getObjectAsync({Bucket: "BUCKET_NAME", Key: "KEY"}, FILE_NAME)
const image = fs.readfilesync(FILE_NAME);
```

- `putObjectAsync(params: PutObjectRequest, fileName: string)`

```TypeScript
const FILE_NAME = "/tmp/temp.jpg";
await putObjectAsync({Bucket: "BUCKET_NAME", Key: "KEY"}, FILE_NAME)
```

- `listObjectsAsync(params: ListObjectsRequest)`

```TypeScript
const params: ListObjectsRequest  = {Bucket: "BUCKET_NAME", Prefix: "PREFIX", Marker: "START_OBJECT"};
const result = await listObjectsAsync(params);
console.info(JSON.stringify(result, null, 2));
```

- `listAllKeysAsync(Bucket: string, Prefix: string): Promise<any>` : additional convenience features

```TypeScript
const result = await listAllKeysAsync("BUCKET_NAME", "PREFIX");
console.info(JSON.stringify(result, null, 2));
```


## Author
[Yun.Seok-Joon](http://DevStarSJ.github.io)

## License
Toggler is available under the MIT license. See the LICENSE file for more info.