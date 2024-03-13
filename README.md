
TransactionRequest request = new TransactionRequest
{
   Amount = Decimal.Parse("10.00"),
   OrderId = "order_id"
};

Result<Transaction> result = gateway.Transaction.SubmitForPartialSettlement(
    "TheParentAuthTransactionId",
    request
);

if (result.IsSuccess()) {
  Transaction settledTransaction = result.Target;
} else {
  Console.WriteLine(result.Errors);
}
531106903309ICA13087# ericajackson-gmail.paypal-prepaid.com-
ericajackson@gmail.paypal-prepaid.com
