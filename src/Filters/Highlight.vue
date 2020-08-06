<script>
export default {
  highlight: function (word, query) {
    const highlightText = new RegExp(query, 'g')
    word.replace(highlightText, match => console.log(match))
    return word.replace(highlightText, function (matchedText) {
      let myText = ''
      myText = '<span class="hghlight-word">' + matchedText + '</span>'
      console.log(myText)
      return myText
    })
  }
}
</script>
<style>
.hghlight-word {
  background-color: yellow;
}
</style>
