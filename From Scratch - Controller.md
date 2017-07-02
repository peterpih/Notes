<pre>
class <b>TestsController</b> < ApplicationController
  <b>before_action</b> :set_test, only: [:show, :edit, :update, :destroy]

  # GET /tests
  # GET /tests.json
  def <b>index</b>
    @tests = Test.all
  end

  # GET /tests/1
  # GET /tests/1.json
  def <b>show</b>
  end

  # GET /tests/new
  def <b>new</b>
    @test = Test.new
  end

  # GET /tests/1/edit
  def <b>edit</b>
  end

  # POST /tests
  # POST /tests.json
  def <b>create</b>
    @test = Test.new(test_params)

    respond_to do |format|
      if @test.save
        format.html { redirect_to @test, notice: 'Test was successfully created.' }
        format.json { render :show, status: :created, location: @test }
      else
        format.html { render :new }
        format.json { render json: @test.errors, status: :unprocessable_entity }
      end
    end
  end

  # PATCH/PUT /tests/1
  # PATCH/PUT /tests/1.json
  def <b>update</b>
    respond_to do |format|
      if @test.update(test_params)
        format.html { redirect_to @test, notice: 'Test was successfully updated.' }
        format.json { render :show, status: :ok, location: @test }
      else
        format.html { render :edit }
        format.json { render json: @test.errors, status: :unprocessable_entity }
      end
    end
  end

  # DELETE /tests/1
  # DELETE /tests/1.json
  def <b>destroy</b>
    @test.destroy
    respond_to do |format|
      format.html { redirect_to tests_url, notice: 'Test was successfully destroyed.' }
      format.json { head :no_content }
    end
  end

  <b>private</b>
    # Use callbacks to share common setup or constraints between actions.
    def <b>set_test</b>
      @test = Test.find(params[:id])
    end

    # Never trust parameters from the scary internet, only allow the white list through.
    def <b>test_params</b>
      params.require(:test).permit(:first, :second)
    end
end
</pre>
