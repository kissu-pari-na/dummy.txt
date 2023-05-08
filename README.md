# dummy.txt

<section class="vh-200" style="background-color: #0d6efd;">
    <div class="container py-5 h-100">
      <div class="row d-flex justify-content-center align-items-center h-100">
        <div class="col col-md-12 col-lg-10 col-xl-10">
            <div class="card row g-0">
              <div class="align-items-center">
                <div class="card-body p-4 p-lg-5 text-black" style="width: 100%">
                  <form [formGroup]="signupForm" (submit)="onSubmit()" ngbForm>
  
                    <div class="d-flex align-items-center mb-3 pb-1">
                      <span class="h1 fw-bold mb-0" style="color: #0D6EFD;">EBirth Registration</span>
                    </div>
  
                    <h4 class="fw-normal mb-3 pb-3" style="letter-spacing: 1px;">Sign up</h4>
                    
                    <div class="form-group">
                      <label for="role" class="form-label">Role</label>
                      <select id="role" name="role" formControlName="role" class="form-control form-control-md" (change)="onRoleChange()">
                        <option value="User">User</option>
                        <option value="Hospital">Hospital</option>
                        <option value="Admin">Admin</option>
                      </select>
                      <app-reactive-form-builder-common-errors-display
                          [formGroup] = "signupForm"
                          [field] = "'role'"
                      >
                      </app-reactive-form-builder-common-errors-display>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="user-name">User Name</label>
                        <input type="text" id="user-name" name="user-name" formControlName="userName" class="form-control form-control-md" />
                        <app-reactive-form-builder-common-errors-display
                            [formGroup] = "signupForm"
                            [field] = "'userName'"
                        >
                        </app-reactive-form-builder-common-errors-display>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="first-name">First Name</label>
                        <input type="text" id="first-name" name="first-name" formControlName="firstName" class="form-control form-control-md" />
                        <app-reactive-form-builder-common-errors-display
                            [formGroup] = "signupForm"
                            [field] = "'firstName'"
                        >
                        </app-reactive-form-builder-common-errors-display>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="last-name">Last Name</label>
                        <input type="text" id="last-name" name="last-name" formControlName="lastName" class="form-control form-control-md" />
                        <app-reactive-form-builder-common-errors-display
                            [formGroup] = "signupForm"
                            [field] = "'lastName'"
                        >
                        </app-reactive-form-builder-common-errors-display>
                    </div>
                    <div *ngIf="selectedRole.value === 'Hospital'" class="form-group">
                      <label class="form-label" for="hospital-name">Hospital Name</label>
                      <input type="text" id="hospital-name" name="hospital-name" formControlName="hospitalName" class="form-control form-control-md" />
                      <app-reactive-form-builder-common-errors-display
                          [formGroup] = "signupForm"
                          [field] = "'hospitalName'"
                      >
                      </app-reactive-form-builder-common-errors-display>
                  </div>
                    <div class="form-group">
                        <label class="form-label" for="email">Email address</label>
                        <input type="email" id="email" name="email" formControlName="email" class="form-control form-control-md" />
                        <app-reactive-form-builder-common-errors-display
                            [formGroup] = "signupForm"
                            [field] = "'email'"
                        >
                        </app-reactive-form-builder-common-errors-display>
                    </div>

                    <div class="form-group">
                      <label class="form-label" for="phone">Phone Number</label>
                      <input type="tel" id="phone" name="phone" formControlName="phone" class="form-control form-control-md" placeholder="+8801701665545">
                      <app-reactive-form-builder-common-errors-display
                          [formGroup] = "signupForm"
                          [field] = "'phone'"
                      >
                      </app-reactive-form-builder-common-errors-display>
                  </div>
                  <div class="mb-3" formGroupName="address">
                    <ngb-accordion>
                      <ngb-panel id="address" [title]="'Address'">
                        <ng-template ngbPanelContent>
                          <div class="form-group">
                            <label class="form-label" for="country">Country</label>
                            <input type="text" class="form-control" id="country" name="country" formControlName="country" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'address.country'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                          <div class="form-group">
                            <label class="form-label" for="division">Division</label>
                            <input type="text" class="form-control" id="division" name="division" formControlName="division" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'address.division'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                          <div class="form-group">
                            <label class="form-label" for="district">District</label>
                            <input type="text" class="form-control" id="district" name="district" formControlName="district" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'address.district'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                          <div class="form-group">
                            <label class="form-label" for="thana">Thana</label>
                            <input type="text" class="form-control" id="thana" name="thana" formControlName="thana" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'address.thana'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                          <div class="form-group">
                            <label class="form-label" for="ward-number">Ward Number</label>
                            <input type="text" class="form-control" id="ward-number" name="ward-number" formControlName="wardNumber" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'address.wardNumber'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                          <div class="form-group">
                            <label class="form-label" for="area">Area</label>
                            <input type="text" class="form-control" id="area" name="area" formControlName="area" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'address.area'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                          <div class="form-group">
                            <label class="form-label" for="post-office-number">Post Office Number</label>
                            <input type="text" class="form-control" id="post-office-number" name="post-office-number" formControlName="postOfficeNumber" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'address.postOfficeNumber'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                          <div class="form-group">
                            <label class="form-label" for="road-number">Road Number</label>
                            <input type="text" class="form-control" id="road-number" name="road-number" formControlName="roadNumber" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'address.roadNumber'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                          <div class="form-group">
                            <label class="form-label" for="house-number">House Number</label>
                            <input type="text" class="form-control" id="house-number" name="house-number" formControlName="houseNumber" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'address.houseNumber'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                        </ng-template>
                      </ngb-panel>
                    </ngb-accordion>
                  </div>

                  <div *ngIf="selectedRole.value === 'Admin'" class="mb-3" formGroupName="workingAddress">
                    <ngb-accordion>
                      <ngb-panel id="address" [title]="'Working Address'">
                        <ng-template ngbPanelContent>
                          <div class="form-group">
                            <label class="form-label" for="working-address-country">Country</label>
                            <input type="text" class="form-control" id="working-address-country" name="working-address-country" formControlName="country" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'workingAddress.country'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                          <div class="form-group">
                            <label class="form-label" for="working-address-division">Division</label>
                            <input type="text" class="form-control" id="working-address-division" name="working-address-division" formControlName="division" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'workingAddress.division'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                          <div class="form-group">
                            <label class="form-label" for="working-address-district">District</label>
                            <input type="text" class="form-control" id="working-address-district" name="working-address-district" formControlName="district" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'workingAddress.district'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                          <div class="form-group">
                            <label class="form-label" for="working-address-thana">Thana</label>
                            <input type="text" class="form-control" id="working-address-thana" name="working-address-thana" formControlName="thana" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'workingAddress.thana'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                          <div class="form-group">
                            <label class="form-label" for="working-address-ward-number">Ward Number</label>
                            <input type="text" class="form-control" id="working-address-ward-number" name="working-address-ward-number" formControlName="wardNumber" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'workingAddress.wardNumber'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                          <div class="form-group">
                            <label class="form-label" for="working-address-area">Area</label>
                            <input type="text" class="form-control" id="working-address-area" name="working-address-area" formControlName="area" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'workingAddress.area'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                          <div class="form-group">
                            <label class="form-label" for="working-address-post-office-number">Post Office Number</label>
                            <input type="text" class="form-control" id="working-address-post-office-number" name="working-address-post-office-number" formControlName="postOfficeNumber" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'workingAddress.postOfficeNumber'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                          <div class="form-group">
                            <label class="form-label" for="working-address-road-number">Road Number</label>
                            <input type="text" class="form-control" id="working-address-road-number" name="working-address-road-number" formControlName="roadNumber" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'workingAddress.roadNumber'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                          <div class="form-group">
                            <label class="form-label" for="working-address-house-number">House Number</label>
                            <input type="text" class="form-control" id="working-address-house-number" name="working-address-house-number" formControlName="houseNumber" class="form-control form-control-md">
                            <app-reactive-form-builder-common-errors-display
                                [formGroup] = "signupForm"
                                [field] = "'workingAddress.houseNumber'"
                            >
                            </app-reactive-form-builder-common-errors-display>
                          </div>
                        </ng-template>
                      </ngb-panel>
                    </ngb-accordion>
                  </div>


                    <div *ngIf="selectedRole.value === 'User' || selectedRole.value === 'Admin'" class="form-group">
                        <label class="form-label" for="nid">National Id Card Number</label>
                        <input type="text" id="nid" name="nid" formControlName="nid" class="form-control form-control-md">
                        <app-reactive-form-builder-common-errors-display
                            [formGroup] = "signupForm"
                            [field] = "'nid'"
                        >
                        </app-reactive-form-builder-common-errors-display>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="password">Password</label>
                        <input type="password" id="password" name="password" formControlName="password" class="form-control form-control-md" />
                        <app-reactive-form-builder-common-errors-display
                            [formGroup] = "signupForm"
                            [field] = "'password'"
                        >
                        </app-reactive-form-builder-common-errors-display>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="confirmPassword">Confirm Password</label>
                        <input type="password" id="confirmPassword" name="confirmPassword" formControlName="confirmPassword" class="form-control form-control-md" />
                        <app-reactive-form-builder-common-errors-display
                            [formGroup] = "signupForm"
                            [field] = "'confirmPassword'"
                        >
                        </app-reactive-form-builder-common-errors-display>
                    </div>
  
                    <div class="pt-1 mb-4">
                      <button class="btn btn-primary btn-lg btn-block" type="submit" [disabled]="signupForm.invalid">Sign Up</button>
                      <div *ngIf="error" class="alert alert-danger alert-dismissible fade show mt-3">
                        <strong>Error!</strong> {{errorMessage()}}
                        <button type="button" class="btn-close" data-bs-dismiss="alert"></button>
                      </div>
                    </div>

                    <p class="mb-5 pb-lg-2">Already have an account? <a (click)="goToLoginPage()"
                        style="color: #0d6efd; cursor: pointer; font-weight: bold;">Login here</a></p>
                    <div *ngIf="confirmEmailMessage" [innerHTML]="confirmEmailMessage"></div>
                  </form>
                </div>
              </div>
            </div>
        </div>
      </div>
    </div>
  </section>
