const names = prompt("Bienvenido, ¿Cómo es tu nombre?").trim();
const saludo=(nombre) => { return alert("Hola "+nombre+ " muchas gracias por elegirnos") };
saludo(names);
let loan = [
    {
        id: 1,
        amount: 1000,
        interest: 15,
        share: 10,
        state: "En proceso"
    }
];
let option;
console.log(loan);
while(option !== 0) {
    option = Number(prompt("Ingrese una opción:\n1. Solicitar prestamo\n2. Ver Prestamos actuales\n3. Pagar prestamo\n0. Salir"));
    
    switch (option) {
        case 1:
            alert("¡Genial! intentaremos ofrecerte el que más te convenga");
                const amount = Number(prompt("¿Cuánto necesitas?"));
                const share = Number(prompt("¿En cuántas cuotas lo quieres saldar?"));
                const interest = Number(prompt("¿Qué tasa de interes te conviene?"));
                const creationID = getLastID() + 1; 
                const state = "En proceso"
                createLoan(creationID, amount, share, interest, state);
            break;
        case 2:
                getAllLoan();
            break;
        case 3:
                let payID =  Number(prompt("Ingrese el ID del prestamo a saldar"));
                PayLoan(payID);
                break;
        case 0: 
                alert('Gracias, vuelva prontos');
            break;
        default:
                alert("La opción ingresa no es correcta, intente nuevamente");
            break;
    }
}
function createLoan(id, amount, share, interest, state) {
    loan.push({
        id,
        amount,
        share,
        interest,
        state,
    });
}
const states = [
    "En proceso",
    "Pagado",
];
function getAllLoan() {
    loan.forEach((loan) => console.log(loan.id+ " - " + " Usted solicitó " + loan.amount + " en " + loan.share + " cuotas, y con una tasa de "+ loan.interest + " y su estado actual es "+ loan.state));
}

function PayLoan(id) {
    loan = loan.filter(loan => loan.id != id);
    alert("Gracias por pagar su prestamo")
}
function getLastID() {
    const ids = loan.map(loan => loan.id);
    return Math.max(...ids);
}
