# Plotly for Rust [![Crate](https://img.shields.io/crates/v/plotly.svg)](https://crates.io/crates/plotly) [![Documentation](https://docs.rs/plotly/badge.svg)](https://docs.rs/plotly) ![Minimum Rust version: 1.30](https://img.shields.io/badge/Minimum%20Rust%20Version-1.30-brightgreen.svg)

A plotting library for Rust powered by [Plotly JS](https://plot.ly/javascript/).


## Usage

Add this to your `Cargo.toml`:

```toml
[dependencies]
plotly = "0.3.0"
```

## Plotly in action
### Line and Scatter plot
```rust
extern crate plotly;
use plotly::charts::{Mode, Scatter};
use plotly::Plot;

fn line_and_scatter_plot() {
    let trace1 = Scatter::new(vec![1, 2, 3, 4], vec![10, 15, 13, 17])
        .name("trace1")
        .mode(Mode::Markers);
    let trace2 = Scatter::new(vec![2, 3, 4, 5], vec![16, 5, 11, 9])
        .name("trace2")
        .mode(Mode::Lines);
    let trace3 = Scatter::new(vec![1, 2, 3, 4], vec![12, 9, 15, 12]).name("trace3");

    let mut plot = Plot::new();
    plot.add_trace(trace1);
    plot.add_trace(trace2);
    plot.add_trace(trace3);

    plot.show();
}

fn main() -> std::io::Result<()> {
    line_and_scatter_plot();
    Ok(())
}
```
![Image](docs/images/line_and_scatter_plot.png)

### Bar plot


### Histogram plot


### Candlestick plot


### OHLC plot


### Surface plot



# License

Plotly for Rust is distributed under the terms of both the MIT license.

See [LICENSE-MIT](LICENSE-MIT), and [COPYRIGHT](COPYRIGHT) for details.

![Image](gbm_simple_ohlc_chart.html)