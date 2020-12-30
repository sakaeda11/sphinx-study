#########
Others
#########

************************************
図表の自動入力文字の変更
************************************

figureディレクティブの **図** のようにSphinxが自動的に埋め込む文字を変更したい場合


conf.py::

    numfig_format = {'figure': 'Fig. %s', 'table': '表 %s'}


***************************************************
warning,note,tipsなどの自動入力文字の変更
***************************************************

warning,note,tipsなどの自動入力文字を変更したい場合の正しい方法は不明ですが、
conf.py上でパラメータ上書きすると変更できるようです。

conf.py::

    from sphinx.locale import admonitionlabels

    admonitionlabels['note'] = u'メモ'
    admonitionlabels['warning'] = u'注意'

`参考：teratail Sphinx文書のadmonitionカスタマイズ <https://teratail.com/questions/91499>`_