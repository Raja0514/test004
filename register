import React, { Component } from "react";
import { Link } from "react-router-dom";
import axios from "axios";
class Register extends Component {
  constructor(props) {
    super(props);
    this.state = {
      name: "",
      email: "",
      password: "",
    };
  }
  handleChange = (e) => {
    console.log(e.target.name);
    console.log(e.target.value);
    this.setState({ [e.target.name]: e.target.value });
  };

  handleSubmit = () => {
    if (
      (this.state.name !== "" && this.state.email !== "",
      this.state.password !== "")
    ) {
      axios
        .post("http://localhost:8080/router0/register", this.state)
        .then((res) => {
          this.setState({ name: "", email: "", password: "" });
        });
    }
  };
  render() {
    return (
      <div>
        <section className="Register">
          <div className="container shadow my-5">
            <div className="row justify-content-center p-5">
              <div
                className="col-md-6 d-flex flex-column
                align-items-center text-white justify-content-center form order-2"
              >
                <h1>Hello</h1>
                <p className=" text-center">Enter your Details to Register</p>
                <h6 className="mb-4">OR</h6>
                <Link
                  to="/login"
                  className="btn btn-outline-light 
                    rounded-pill pb-2 w-50"
                >
                  Login
                </Link>
              </div>
              <div className="col-md-6 p-3">
                <h1 className="text-center">Register</h1>
                <form onSubmit={() => this.handleSubmit()}>
                  <div className="mb-3">
                    <label className="form-label">name</label>
                    <input
                      type="text"
                      className="form-control"
                      id="name"
                      name="name"
                      onChange={(e) => this.handleChange(e)}
                      value={this.state.name}
                    />
                  </div>
                  <div className="mb-3">
                    <label className="form-label">email</label>
                    <input
                      type="email"
                      className="form-control"
                      id="email"
                      name="email"
                      onChange={(e) => this.handleChange(e)}
                      value={this.state.email}
                    />
                  </div>
                  <div className="mb-3">
                    <label className="form-label">Password</label>
                    <input
                      type="text"
                      className="form-control"
                      onChange={(e) => this.handleChange(e)}
                      name="password"
                      value={this.state.password}
                    />
                  </div>

                  <button
                    type="submit"
                    className="btn btn-outline-primary w-100 mt-4"
                  >
                    Submit
                  </button>
                </form>
              </div>
            </div>
          </div>
        </section>
      </div>
    );
  }
}
export default Register;
