# Shopping Cart Module — Test Plan & Results

Manual test cases run against the Buildmart shopping cart feature before merge.

| # | Test Case | Steps | Expected Result | Result |
|---|-----------|-------|------------------|--------|
| 1 | Product grid loads | Open the shop page | All 8 products display with name, price, and unit | ✅ Pass |
| 2 | Add item to cart | Click "Add to cart" on a product | Cart count badge increments, confirmation toast appears | ✅ Pass |
| 3 | Open/close cart drawer | Click the Cart button, then the close (×) button | Drawer slides open, then slides closed | ✅ Pass |
| 4 | Close cart with Escape key | Open drawer, press Escape | Drawer closes | ✅ Pass |
| 5 | Empty cart state | Open drawer with no items added | "Your cart is empty" message shown, Checkout disabled | ✅ Pass |
| 6 | Increase quantity | Click "+" on a cart item | Quantity and line total update | ✅ Pass |
| 7 | Decrease quantity to zero | Click "−" until quantity reaches 0 | Item is removed from the cart automatically | ✅ Pass |
| 8 | Remove item | Click "Remove" on a cart item | Item disappears from cart, totals recalculate | ✅ Pass |
| 9 | Subtotal / GST / Total accuracy | Add several items, compare displayed totals to manual calculation | Subtotal equals sum of line totals; GST is 10% backed out of GST-inclusive price | ✅ Pass |
| 10 | Checkout with items | Add items, click Checkout | Confirmation toast with order total shown, cart empties, drawer closes | ✅ Pass |
| 11 | Checkout disabled when empty | Open drawer with empty cart | Checkout button is disabled | ✅ Pass |
| 12 | Add same item twice, then remove once | Add an item, add it again, then click Remove once | Quantity drops by 1, item is not fully removed | ✅ Pass |
| 13 | Large cart totals | Add 5+ different items, open cart | Subtotal, GST, and Total all match manual calculation | ✅ Pass |

## Notes
- Tested in Chrome and Edge at desktop and mobile widths.
- No known open bugs at time of merge.
