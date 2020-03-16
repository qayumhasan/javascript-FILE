# javascript-FILE
## Add & Delete Extra Field.
  <script>
    $(document).ready(function () {
        var photo_div = '<div class="gallery_photo mt-2">';
        photo_div += '<div class="row">';
        photo_div += '<div class="col-sm-5">';
        photo_div += '<label for="inputEmail3" class=" col-form-label text-right">Gallery Photo</label>';
        photo_div += '<input type="file" class="form-control" name="gallery_photo[]" required>';
        photo_div += '</div>';
        photo_div += '<div class="col-sm-6">';
        photo_div += '<label for="inputEmail3" class=" col-form-label text-right">Photo Caption</label>';
        photo_div += '<input type="text" class="form-control" placeholder="Photo Caption" name="photo_caption[]" required>';
        photo_div += '</div>';
        photo_div += '<div class="col-sm-1">';
        photo_div += '<div class="cross_button_area">';
        photo_div += '<button onclick="delete_row(this);" type="button" class="btn btn-sm  btn-danger"><i class="fa fa-times"></i></button>';
        photo_div += '</div>';
        photo_div += '</div>';
        photo_div += '</div>';
        photo_div += '</div>';
        $('.add_more_button').on('click', function () {
            $('.gallery_photos_area').append(photo_div);
        })
    })

    function delete_row(row) {
        $(row).closest('.gallery_photo').remove();
    }
</script>
