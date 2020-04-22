// Returns a random DNA base
const returnRandBase = () => {
  const dnaBases = ['A', 'T', 'C', 'G']
  return dnaBases[Math.floor(Math.random() * 4)] 
}

// Returns a random single stand of DNA containing 15 bases
const mockUpStrand = () => {
  const newStrand = []
  for (let i = 0; i < 15; i++) {
    newStrand.push(returnRandBase())
  }
  return newStrand
}

const pAequorFactor = (number, dnaArray) => {
  return {
    specimenNum: number,
    dna: dnaArray,
    mutate() {
      index = Math.floor(Math.random()*dnaArray.length);
      x = this.dna[index];
      y = '';
      do {
        y = returnRandBase();
      } while (x === y);
      if (x !== y) {
        this.dna.splice(index, 1, y);
      }
        return this.dna;    
    },
    compareDNA(pAequorCompare) {     
      let match = 0;
      let total = dnaArray.length;
      for (i = 0; i<dnaArray.length; i++) {
        if (this.dna[i] === pAequorCompare.dna[i]) {
          console.log(`${this.dna[i]}  ${pAequorCompare.dna[i]} match`);
          match++;
        } else {
          console.log(`${this.dna[i]}  ${pAequorCompare.dna[i]} no match`);
        }        
        }
      console.log(`Specimen ${this.specimenNum} and ${pAequorCompare.specimenNum} share ${(match/total)*100}% of DNA pairs`);
      },
    willLikelySurvive() {
      let counter = 0;
      let total = dnaArray.length;
      for (i = 0; i<dnaArray.length; i++) {
        if (this.dna[i] === 'C' || this.dna[i] === 'G') {
          counter++;
        }
      }
      if (counter >= (total*.6)){
        // console.log('true');
        return true;
      } else {
        return false;        
      }
    }
    }
  }
  
let survivors = [];
let counterSur = 0
let counterInd = 1;
do {
  let individual = pAequorFactor(counterInd, mockUpStrand());
  counterInd++;
  if (individual.willLikelySurvive() === true) {
    counterSur++;   
    survivors.push(individual.specimenNum);
  }
  } while (counterSur < 30);

console.log(survivors);
