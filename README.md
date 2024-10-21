# PersonalExpenseTracker

exports.handler = function(event, context, callback){
  console.log("Incoming Event:",event);
  const bucket = event.Records[0].s3.bucket.name;
  const filename = decodeURIComponent(event.Records[0].s3.object.key.replace(/\+/g,' '));
  const message = `An Image is Added - ${bucket} -> ${filename}`;
  console.log(message);
  callback(null, message);
};
