<pre>
class <b>Examples</b>Controller < ApplicationController
  before_action :set_<b>example</b>, only: [:show, :edit, :update, :destroy]

  # GET /examples
  # GET /examples.json
  def index
    @<b>examples</b> = <b>Example</b>.all
  end

  # GET /examples/1
  # GET /examples/1.json
  def show
  end

  # GET /examples/new
  def new
    @<b>example</b> = <b>Example</b>.new
  end

  # GET /examples/1/edit
  def edit
  end

  # POST /examples
  # POST /examples.json
  def create
    @<b>example</b> = <b>Example</b>.new(<b>example</b>_params)

    respond_to do |format|
      if @<b>example</b>.save
        format.html { redirect_to @<b>example</b>, notice: 'Example was successfully created.' }
        format.json { render :show, status: :created, location: @<b>example</b> }
      else
        format.html { render :new }
        format.json { render json: @<b>example</b>.errors, status: :unprocessable_entity }
      end
    end
  end

  # PATCH/PUT /examples/1
  # PATCH/PUT /examples/1.json
  def update
    respond_to do |format|
      if @<b>example</b>.update(<b>example</b>_params)
        format.html { redirect_to @<b>example</b>, notice: 'Example was successfully updated.' }
        format.json { render :show, status: :ok, location: @<b>example</b> }
      else
        format.html { render :edit }
        format.json { render json: @<b>example</b>.errors, status: :unprocessable_entity }
      end
    end
  end

  &#35; DELETE /examples/1
  &#35; DELETE /examples/1.json
  def destroy
    @<b>example</b>.destroy
    respond_to do |format|
      format.html { redirect_to <b>examples</b>_url, notice: 'Example was successfully destroyed.' }
      format.json { head :no_content }
    end
  end

  private
    &#35; Use callbacks to share common setup or constraints between actions.
    def set_<b>example</b>
      @<b>example</b> = <b>Example</b>.find(params[:id])
    end

    &#35; Never trust parameters from the scary internet, only allow the white list through.
    def <b>example</b>_params
      params.require(:<b>example</b>).permit(:first, :second)
    end
end
</pre>
