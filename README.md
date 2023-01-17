# html2pdfimg
HTML下载成pdf或者img格式，并支持水印，pdf支持配置分页元素自动分页，不会截断元素。

基于jspdf.js和watermark.js二次封装，并且优化了pdf的分割判断方式，不会出现截断元素的问题。
使用方法：

import JsPdfImg from "@/utils/jspdf.js";

new YkJsPdf("#printPage", "导出的图片名称", {
        pageBreak: ['.title', '#area'],
        watermarkOption: {
          watermark_txt: "水印配置",
          z_index: 97,
          watermark_x: 0,
          watermark_y: 0,
          watermark_x_space: 160,
          watermark_y_space: 160,
          watermark_width: 180,
        },
      }).outImage(() => {
        console.log('结束')
      });
      
      new YkJsPdf("#printPage", "导出的pdf名称", {
        pageBreak: ['.title', '#area'],
        watermarkOption: {
          watermark_txt: "水印配置",
          z_index: 97,
          watermark_x: 0,
          watermark_y: 0,
          watermark_x_space: 160,
          watermark_y_space: 160,
          watermark_width: 180,
        },
      }).outPdf(() => {
        console.log('结束')
      });