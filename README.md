# AW Close By Total Profit

This code is a MetaTrader 5 (MT5) expert advisor that is designed to close orders based on the total profit of the current symbol. It provides three main functions: closing orders, trailing profit, and one-click stop.

## Global Variables

- `TakeProfit`: The default take profit level for orders.
- `StopLoss`: The default stop loss level for orders.

## Closing Orders Function

The `CloseOrders` function is responsible for closing orders. It takes a boolean parameter `closeAll` which, when set to `true`, closes all orders for the current symbol. If `closeAll` is set to `false`, it closes only the first order found for the current symbol.

## Trailing Profit Function

The `TrailingProfit` function is responsible for trailing the profit of orders. It continuously checks for open orders and modifies the stop loss level based on the trailing stop value. If the current profit of an order exceeds the trailing level and the stop loss price is less than the current stop loss, the function modifies the order to update the stop loss level.

## One-Click Stop Function

The `OneClickStop` function is triggered when a button is clicked. It calls the `ExpertRemove` function to stop the expert advisor from running.

## Initialization

The `OnInit` function is called during the initialization of the expert advisor. It registers a chart click event using the `ChartEventAdd` function.

## Deinitialization

The `OnDeinit` function is called during the deinitialization of the expert advisor. It unregisters the chart click event using the `ChartEventRemove` function.

## OnChartEvent

The `OnChartEvent` function is called when a chart event occurs. In this code, it checks if the chart event is a click event and calls the `OneClickStop` function.

## Start Function

The `OnStart` function is the entry point of the expert advisor. It first calls the `CloseOrders` function to close any existing orders for the current symbol. Then, it starts the trailing profit function with a trailing stop of 10 pips.

---

This code is a sample provided by Forex Robot Easy Team and is not the official developer of the product. To find the official developer and obtain detailed reviews and trading results of this product, please visit the [Forex Robot Easy website](https://forexroboteasy.com/forex-robot-review/aw-close-by-total-profit-review-and-download-forex-software-for-professional-forex-traders/). This code demonstrates how the product works and can be used as a reference. For the official developer and further information, please refer to MQL5.
