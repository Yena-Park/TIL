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
