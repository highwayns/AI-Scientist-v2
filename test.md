# 知识库文档创建
npx bmad-method flatten --input /home/tei952/sayama/03.workflow/ai-science/AI-Scientist-v2 --output /home/tei952/sayama/03.workflow/ai-science/AI-Scientist-v2/docs/flattened-codebase.xml

# 大文件分割
python xml_splitter.py ../AI_Powered_paper_manager/docs/flattened-codebase.xml -o ../AI_Powered_paper_manager/docs/ --max-mb 10 --item-tag file

# 知识库创建
python Create_Dataset AI-Scientist-v2

# 知识库文档上传
python Add_Document.py AI-Scientist-v2 /home/tei952/sayama/03.workflow/ai-science/AI-Scientist-v2/docs/flattened-codebase.xml

