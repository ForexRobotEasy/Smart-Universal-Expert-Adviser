# Smart Universal EA

This is a sample code for the Smart Universal Expert Advisor (EA) developed by the Forex Robot Easy Team. Please note that ForexRobotEasy is not the official developer of this product. This code serves as a demonstration of how the Smart Universal EA can work as described in the product.

For detailed reviews and trading results of the Smart Universal EA, please visit [Forex Robot Easy - Smart Universal Expert Adviser Review](https://forexroboteasy.com/forex-robot-review/smart-universal-expert-adviser-review-enhance-forex-trading/).

## Description

The Smart Universal EA is an automated trading system designed for the MetaTrader 5 platform. It uses custom indicator signals to determine when to enter buy or sell positions in the market.

## Input Parameters

- `StopLoss`: The desired Stop Loss level in pips.
- `TakeProfit`: The desired Take Profit level in pips.

## How It Works

1. On each tick, the EA retrieves the buy and sell buffers from the custom indicator.
2. If the buy buffer value at the current index is greater than 0, a buy order is placed.
   - The current market ask price is obtained.
   - The stop loss level is calculated by subtracting the specified Stop Loss value multiplied by the point size from the ask price.
   - The take profit level is calculated by adding the specified Take Profit value multiplied by the point size to the ask price.
   - The order is sent to the market with the calculated stop loss and take profit levels.
3. If the sell buffer value at the current index is greater than 0, a sell order is placed.
   - The current market bid price is obtained.
   - The stop loss level is calculated by adding the specified Stop Loss value multiplied by the point size to the bid price.
   - The take profit level is calculated by subtracting the specified Take Profit value multiplied by the point size from the bid price.
   - The order is sent to the market with the calculated stop loss and take profit levels.

## Notes

- Make sure to properly set the input parameters `StopLoss` and `TakeProfit` according to your trading strategy and risk tolerance.
- This code assumes that the custom indicator being used has two buffers: one for buy signals and one for sell signals. Adjust the `CopyBuffer` function parameters accordingly if your indicator has different buffer indices or sizes.
- It is recommended to test this EA on a demo account before using it on a live account.
- For the official developer of the Smart Universal EA, please refer to the MQL5 website.

## Cleanup Resources

The `OnDeinit` function is called when the EA is removed from the chart or the terminal is closed. This function can be used to clean up any resources used by the EA.

## Initialization Code

The `OnStart` function is called when the EA is attached to a chart. This function can be used for any initialization code required by the EA.

For more information and support on the Smart Universal EA, please visit [forexroboteasy.com](https://forexroboteasy.com).
