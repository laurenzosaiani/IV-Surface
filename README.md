# IV-Surface

## Overview
    This project fetches real-time options data for any stock and constructs its implied volatility (IV) surface. The IV surface is a 3D representation of implied volatility as a          function of strike price (moneyness) and time to expiry, a key concept in options pricing.
    
## How the Surface is Constructed
    Data Collection: Pull options data using yfinance, including strikes, expiration dates, and market prices.
    Data Cleaning: Remove missing values and extreme IVs using statistical filtering (z-score).
    Compute Features:
      Moneyness: Strike / Spot Price
      Time to Maturity (TTM): Years until option expiry
    Interpolation: Use Radial Basis Functions (RBF) to create a smooth surface across moneyness and TTM.
    Visualization: Display the IV surface as a 3D plot with optional scatter points for raw data and contour projections for clarity.

## Why It’s Important
    It reflects market expectations of future volatility.
    Traders use it to price options accurately and identify mispricings.
    The shape of the surface (smile, skew) provides insights into risk perception for different strikes and expiries.

## Applications in Trading
    Pricing Models: Used in Black-Scholes, local volatility, and stochastic volatility models.
    Hedging Strategies: Helps traders construct delta/gamma/vega hedges.
    Arbitrage Opportunities: Detects inconsistencies between market prices and theoretical models.
    Volatility Trading: Traders can go long or short volatility based on surface shapes.
