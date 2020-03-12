var AWS = require('aws-sdk');
    AWS.config.update({
        "accessKeyId": "<<IAM users's access key id>>",
        "secretAccessKey": "<<IAM users's secret access key>>",
        "region": "<<region>>"
    })
var s3 = new AWS.S3();
var params = {
        Bucket: '<<Bucker name>>',
        Key: '<<files's url>>',
        Expires: <<60>> // 60 sec
};
module.exports = async (req, res) => {
        const imagesrc = await s3.getSignedUrlPromise('getObject', params);
        res.status(200).json({imagesrc: imagesrc}) // you can get a signed url from s3
}
