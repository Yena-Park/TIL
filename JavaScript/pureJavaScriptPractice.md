The goal is to output an object showing which important amenities are available in a given list of schools.
We want to look for facilities that are existing keys in a given object (refer to facilityExistsInList below).
The values corresponding to each key are boolean values that indicate whether the facility exists in the list.
We also only want to check for schools in the given country.
IMPORTANT: If no country is provided, look though all schools

Create a function, getExistingAmenities, that will output an object of the same structure as amenityExistsInList but with
existing amenities set to true

Create another function, getExistingfacilities, that will return a de-duped(no duplicates) array of all facilities in a given school list

Create another function, calcSchoolfacilities, that returns an array with the number of facilities each schools has in a given school list

NOTE: Bonus points for making the getExistingfacilities a pure function.
```javascript

 const schools = [
  {
    name: 'mexicoCity college', 
    country: 'Mexico',
    facilities: ['Pool', 'Cafeteria', 'Sauna', 'Gym', 'Wifi'],
  },
  {
    name: 'oaville college', 
    country: 'Canada',
    facilities: ['Cafeteria', 'Sauna', 'library'],
  },
  {
    name: 'waterloo college', 
    country: 'Canada',
    facilities: ['BookStore'],
  },
  {
    name: 'kitchener college', 
    country: 'Canada',
    facilities: ['Cafeteria', 'Gym'],
  },
]

const facilityExistsInList = {
  pool: false,
  Cafeteria: false,
  wifi: false,
  car: false,
  gym: false,
}

const country = 'Canada';

const calcSchoolfacilities =(schools) => {
  return schools.map(school => school.facilities.length);
}

const getAllfacilities = (schools) => {
  const facilities = schools.reduce((array, school) => [...array, ...school.facilities], []);
  const set = new Set(facilities);
  const result = Array.from(set);
  return result;
}


const getExistingfacilities = (schools, facilityExistsInList, country) => {
  const copiedFacilityExistsInList = Object.assign({}, facilityExistsInList);
  const filteredschools = schools.filter(school => school.country === country);

  const result = Array.from(new Set(filteredschools.reduce((arr, school) => [...arr, ...school.facilities], [])))
    .map(facility => facility.toLowerCase())
    .reduce((list, facility) => {
      if(list[facility] != null) {
        list[facility] = true;
      }
      return list;
    }, copiedFacilityExistsInList)

  return result;
}

console.log(getExistingfacilities(schools, facilityExistsInList, country));
console.log(facilityExistsInList);
console.log(calcSchoolfacilities(schools));
console.log(getAllfacilities(schools));
```
