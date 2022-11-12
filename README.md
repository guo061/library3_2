# library3_2
一.效果截图：
![3S1)KLVPIJZUF%J3I_7_599](https://user-images.githubusercontent.com/114241292/201458815-bf7af615-b325-4514-a054-effd6c846c1d.png)
![ISTPKWF9 _ORXD W2I4TYIS](https://user-images.githubusercontent.com/114241292/201458817-97580e4c-8f85-41cb-b7c0-6093f2323375.png)
![L8GKTV 1K{HZVLZ 1DMYA0U](https://user-images.githubusercontent.com/114241292/201458822-34226800-98d7-4bef-89f1-07bf0bcfc7b3.png)


二.代码：
    第二个实验：https://github.com/guo061/library3_2/blob/master/exam3_2/app/src/main/java/com/example/exam3_2/MainActivity_2.java

   第三个实验：https://github.com/guo061/library3_2/blob/master/exam3_2/app/src/main/java/com/example/exam3_2/MainActivity_3.java

   第四个实验：https://github.com/guo061/library3_2/blob/master/exam3_2/app/src/main/java/com/example/exam3_2/MainActivity_4.java

三.思路
实验二：首先设置好框架，为constraintlayout框架；接着写java代码，其中登录和取消登录的代码如下：
                .setPositiveButton("登录", new DialogInterface.OnClickListener() {
                    @Override
                    public void onClick(DialogInterface dialogInterface, int i) {
                        //登录
                    }
                })
                .setNegativeButton("取消", new DialogInterface.OnClickListener() {
                    @Override
                    public void onClick(DialogInterface dialogInterface, int i) {
                        //取消登录
                    }
                })
实验三：框架为线性框架，字体大小，字体颜色，普通菜单的实现代码如下：
        fontMenu.setHeaderTitle("请选择字体大小");
        fontMenu.add(0,font_10,0,"10号");
        fontMenu.add(0,font_12,0,"12号");
        fontMenu.add(0,font_14,0,"14号");
        fontMenu.add(0,font_16,0,"16号");
        fontMenu.add(0,font_18,0,"18号");

        menu.add(0,PLAIN_ITEM,0,"普通菜单");
        SubMenu colorMenu=menu.addSubMenu("字体颜色");
        colorMenu.setIcon(R.drawable.color);
        colorMenu.setHeaderIcon(R.drawable.color);

        colorMenu.setHeaderTitle("选择字体颜色");
        colorMenu.add(0,font_red,0,"红色");
        colorMenu.add(0,font_blue,0,"蓝色");
        colorMenu.add(0,font_green,0,"绿色");
实验四：框架为线性框架，框架内容代码如下：
        public List<Map<String,Object>>getData(){
        List<Map<String,Object>>list=new ArrayList<Map<String,Object>>();
        Map<String ,Object> map;
        map=new HashMap<String,Object>();
        map.put("title","One");
        map.put("image",R.drawable.jq);
        list.add(map);

        map=new HashMap<String,Object>();
        map.put("title","Two");
        map.put("image",R.drawable.jq);
        list.add(map);

        map=new HashMap<String,Object>();
        map.put("title","Three");
        map.put("image",R.drawable.jq);
        list.add(map);

        map=new HashMap<String,Object>();
        map.put("title","Four");
        map.put("image",R.drawable.jq);
        list.add(map);

        map=new HashMap<String,Object>();
        map.put("title","Five");
        map.put("image",R.drawable.jq);
        list.add(map);
        return list;
    }
    删除操作实现代码如下：
        @Override
        public boolean onActionItemClicked(ActionMode mode, MenuItem item) {
            boolean ret = false;
            if (item.getItemId() == R.id.menu_delete) {
                mode.finish();
                ret = true;
            }
            return ret;
        }
