As an air traffic controller 
So I can get passengers to a destination 
I want to instruct a plane to land at an airport

irb >
require './lib/plane.rb'
require './lib/airport.rb'
airbus = Plane.new
heathrow = Airport.new
airbus.land(heathrow)

As an air traffic controller 
So I can get passengers on the way to their destination 
I want to instruct a plane to take off from an airport and confirm that it is no longer in the airport

require './lib/plane.rb'
require './lib/airport.rb'
airbus = Plane.new
heathrow = Airport.new
airbus.land(heathrow)
heathrow.take_off

As an air traffic controller 
To ensure safety 
I want to prevent takeoff when weather is stormy 

As an air traffic controller 
To ensure safety 
I want to prevent landing when weather is stormy 

require './lib/plane.rb'
require './lib/airport.rb'
airbus = Plane.new
heathrow = Airport.new
airbus.land(heathrow)

As an air traffic controller 
To ensure safety 
I want to prevent landing when the airport is full 

require './lib/plane.rb'
require './lib/airport.rb'
require './lib/weather.rb'
airbus = Plane.new
heathrow = Airport.new
airbus.land(heathrow)

As the system designer
So that the software can be used for many different airports
I would like a default airport capacity that can be overridden as appropriate

require './lib/plane.rb'
require './lib/airport.rb'
heathrow = Airport.new(10)
10.times { Plane.new.land(heathrow) }
