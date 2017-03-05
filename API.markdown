##API
###网络
	发起请求 wx.request
	上传 wx.uploadFile
	下载 wx.downloadFile
	WebSocket
		wx.connectSocket 创建一个WebSocket连接
		wx.sendSocketMessage 通过WebSocket连接发送数据
		wx.closeSocket 关闭WebSocket连接
###媒体
	图片 wx.chooseImage
###数据缓存
	1.wx.setStorage:将数据存储在本地缓存中指定的 key 中，会覆盖掉原来该 key 对应的内容，这是一个异步接口
		wx.setStorage({
  			key:"key",
  			data:"value"
		})
	2.wx.setStorageSync:将 data 存储在本地缓存中指定的 key 中，会覆盖掉原来该 key 对应的内容，这是一个同步接口
		try {
    			wx.setStorageSync('key', 'value')
		} catch (e) {    
			}
	3.wx.getStorageSync:从本地缓存中同步获取制定Key的内容
		try {
  			var value = wx.getStorageSync('key')
 			if (value) {
      			// Do something with return value
  			}
		} catch (e) {
 		 // Do something when catch error
		}
	4.wx.getStorageInfo
	5.wx.getStorageInfoSync
	6.wx.removeStorage:从本地缓存中异步移除指定 key
		wx.removeStorage({
  			key: 'key',
  			success: function(res) {
    			console.log(res.data)
  			} 
		})
	7.wx.removeStorageSync:从本地缓存中同步移除指定 key
		try {
  			wx.removeStorageSync('key')
		} catch (e) {
  			// Do something when catch error
		}
	8.wx.clearStorage
	9.wx.clearStorageSync
###位置
	获取位置	
		wx.getLocation