# 100 Days of FPGA

## Day 1

```vhdl

library ieee;
use ieee.numeric_std.all;
use ieee.std_logic_1164.all;


entity multiplexer_2to1 is
port (
  in_1 : in std_logic_vector(3 downto 0);
  in_2 : in std_logic_vector(3 downto 0);
  sel : in std_logic;
  f_out : out std_logic_vector(3 downto 0)
);
end multiplexer_2to1;


architecture Behavioral of multiplexer_2to1 is

begin
  
  
process(sel, in_1, in_2)
begin
    
    if (sel = '0') then
      f_out <= in_1;
    else
      f_out <=  in_2;
  	end if;
end process;

end Behavioral;

```
