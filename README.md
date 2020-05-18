# Reactimport React from "react";
import ReactDOM from 'react-dom';



class App extends React.Component{
    constructor(){
        super();
        this.state = {
            firstName :"Dhirendra",
            lastName : "Kumar",
            profession: 'Programmer'
        }   
        }
        render(){
            return(
            <React.Fragment>
            <Detail firstName = {this.state.firstName} lastName = {this.state.lastName}
             profession=  {this.state.profession}/>
            </React.Fragment>);
        }
    }


class Person extends React.Component {
    render(){
        return(
            <React.Fragment>
            <h2>This is Person's Detail....</h2>
            <h2> My first name is:<u>{this.props.firstName}</u></h2>
            <h4>My last name is :<b> {this.props.lastName}</b></h4>
            <p>My full name is : <b>{this.props.firstName} {this.props.lastName}</b></p>
            <p>My profession is : <b>{this.props.profession}</b></p>
            </React.Fragment>
        );
    }
}

function Detail(props){
    
    return (
        <div>
        <h2>This is detail....</h2>
    <Person firstName={props.firstName} lastName = {props.lastName} profession={props.profession}/>
    </div>)
        }
        


export default App;
