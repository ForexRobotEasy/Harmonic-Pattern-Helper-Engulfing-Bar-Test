# Harmonic Pattern Helper Engulfing Bar Test

This code is a sample implementation of a trading robot that identifies and capitalizes on Engulfing Candle Patterns within a manually input price range in the Forex market. It is based on the Harmonic Pattern Helper Expert Advisor developed by the Forex Robot Easy Team.

## Introduction

The Harmonic Pattern Helper is an Expert Advisor designed to automate the identification and trading of Engulfing Candle Patterns in the Forex market. Engulfing Candle Patterns are powerful reversal patterns that occur when a candle's body engulfs the previous candle's body, indicating a potential change in market direction.

This code provides a basic implementation of the Harmonic Pattern Helper, showcasing how to identify Engulfing Candle Patterns within a manually input price range and execute trades accordingly.

## Usage

To use this code, you need to have the Trade.mqh library included in your project. This library provides the necessary functions for executing trades.

The code defines a constant `PRICE_RANGE` which represents the manually input price range for Engulfing Candle Patterns. You can adjust this value according to your trading strategy.

The trading robot is initialized in the `OnInit` function. It enables trading by setting various parameters such as the expert magic number, deviation in points, order filling type, order trade type, order time type, and slippage. You can customize these parameters to suit your trading preferences.

Incoming ticks are handled in the `OnTick` function. The code checks for Engulfing Candle Patterns within the defined price range using the `IsEngulfingPattern` function. If an Engulfing Candle Pattern is detected, a trade is executed using the `ExecuteTrade` function.

The `IsEngulfingPattern` function compares the current candle's high and low with the previous candle's high and low. It calculates the range of both candles and checks if they meet the criteria for a bullish or bearish engulfing pattern within the defined price range. If a pattern is detected, the function returns `true`; otherwise, it returns `false`.

The `ExecuteTrade` function opens a trade based on the identified Engulfing Candle Pattern. It defines the lot size, stop loss level, and take profit level for the trade. These values can be adjusted to fit your risk management strategy. The trade is executed using the `Buy` function from the Trade.mqh library.

The `OnDeinit` function is responsible for handling program shutdown. It closes all open trades using the `CloseAll` function from the Trade.mqh library.

## Additional Information

For detailed reviews and trading results of the official Harmonic Pattern Helper Expert Advisor developed by the Forex Robot Easy Team, please visit [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/harmonic-pattern-helper-review-expert-advisor-for-forex-trading/). Please note that ForexRobotEasy is not the official developer of this product, but we provide this sample code to demonstrate how it can work as described.

Please refer to the official MQL5 website to find the official developer of the Harmonic Pattern Helper Expert Advisor and obtain the complete and up-to-date version of the product.
