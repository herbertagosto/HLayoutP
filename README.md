# HLayoutP

Example:
```
namespace demo
{
    class Program
    {
        static void Main(string[] args)
        {
            var polarities = new List<Polarity>() {
                new Polarity("N", "P")
                , new Polarity("CLK", "DATA")
                , new Polarity("DN", "ND")
            };
            var netnames = new List<string>() {
                "CLK_100M_FPGAN_2A_N",
                "CLK_100M_CLKFPGAN_2A_N",
                "CLK_100M_DATAFPGAN_2A_N",
                "CLK_100M_DATAFPGAN_2DNA_N",
                "CLK_100M_DATAFPGAN_2NDA_N",
                "CLK_100M_FPGAN_2A_P"
            };
            var diffpairs = new DifferentialPair(polarities, netnames).Get();
        }
    }
}
```