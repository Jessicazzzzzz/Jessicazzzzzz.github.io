---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
一个数组 a1,a2,a3,a4
数组b  使得a 为b的前缀和
a1 = b1
a2 = b2+b1
a3 = b3 +b2+b1 
那么 b1 = a1 
     b2 = a2-a1 
     b3 = a3 - a2  ^WzJN8YIE

首先明确a 是b的前缀和
那么我们假设 a是为0的数组,那么它的差分数组也必然是为0  
构建差分数组相当于是在这个区间插入a[i]
b   b1  b2  b3 b4 b5 b6 

a   a1 a2 a3 a4 a5 a6 
                ^oXbyWJJO

先构建差分数组 根据公式 bn = an -an-1

b   a1   a2-a1   a3-a2    a4-a3   a5-a4      a6-a5 

在1-3 区间+c   
b   a1+c a2-a1   a3-a2     a4-a3-c   a5-a4    a6-a5
a   a1+c a2+c   a3+c       a4         a5       a6  // 这样就在原数组的基础上+c
   
  ^MjbV5QCs

%%
# Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.1.3",
	"elements": [
		{
			"id": "WzJN8YIE",
			"type": "text",
			"x": -327.6171875,
			"y": -203.4140625,
			"width": 243.65997314453125,
			"height": 200,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1629783031,
			"version": 227,
			"versionNonce": 1634727961,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574700393,
			"link": null,
			"locked": false,
			"text": "一个数组 a1,a2,a3,a4\n数组b  使得a 为b的前缀和\na1 = b1\na2 = b2+b1\na3 = b3 +b2+b1 \n那么 b1 = a1 \n     b2 = a2-a1 \n     b3 = a3 - a2 ",
			"rawText": "一个数组 a1,a2,a3,a4\n数组b  使得a 为b的前缀和\na1 = b1\na2 = b2+b1\na3 = b3 +b2+b1 \n那么 b1 = a1 \n     b2 = a2-a1 \n     b3 = a3 - a2 ",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "一个数组 a1,a2,a3,a4\n数组b  使得a 为b的前缀和\na1 = b1\na2 = b2+b1\na3 = b3 +b2+b1 \n那么 b1 = a1 \n     b2 = a2-a1 \n     b3 = a3 - a2 ",
			"lineHeight": 1.25
		},
		{
			"id": "TbAJ01cKkiZRUpjg7kcQS",
			"type": "line",
			"x": -347.41015625,
			"y": 142.07421875,
			"width": 296.359375,
			"height": 0.62890625,
			"angle": 0,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"seed": 1027250967,
			"version": 40,
			"versionNonce": 236710681,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574813753,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					296.359375,
					0.62890625
				]
			],
			"lastCommittedPoint": null,
			"startBinding": null,
			"endBinding": null,
			"startArrowhead": null,
			"endArrowhead": null
		},
		{
			"id": "dI6rZnItnjKILSop4v-85",
			"type": "freedraw",
			"x": -270.5390625,
			"y": 129.78515625,
			"width": 2.80078125,
			"height": 13.015625,
			"angle": 0,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1117501463,
			"version": 14,
			"versionNonce": 628382553,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574819886,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.23046875,
					0.2265625
				],
				[
					-0.4609375,
					0.453125
				],
				[
					-1.3984375,
					3.515625
				],
				[
					-1.69140625,
					4.38671875
				],
				[
					-1.984375,
					5.2578125
				],
				[
					-1.984375,
					7.63671875
				],
				[
					-2.5703125,
					10.1328125
				],
				[
					-2.80078125,
					11.4609375
				],
				[
					-2.80078125,
					12.33203125
				],
				[
					-2.80078125,
					12.7890625
				],
				[
					-2.80078125,
					13.015625
				],
				[
					-2.80078125,
					13.015625
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				-2.80078125,
				13.015625
			]
		},
		{
			"id": "jjv9Gs1lmSy21eTBTQr5d",
			"type": "freedraw",
			"x": -277.1953125,
			"y": 81.96875,
			"width": 9.84375,
			"height": 27.90625,
			"angle": 0,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1241838551,
			"version": 36,
			"versionNonce": 476889817,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574821213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.23046875,
					-0.23046875
				],
				[
					-0.4609375,
					0.2265625
				],
				[
					-1.046875,
					1.09765625
				],
				[
					-2.5859375,
					4.34765625
				],
				[
					-3.0625,
					6.7265625
				],
				[
					-4.4921875,
					11.484375
				],
				[
					-4.96875,
					13.86328125
				],
				[
					-4.96875,
					17.11328125
				],
				[
					-4.96875,
					17.5703125
				],
				[
					-5.19921875,
					18.8984375
				],
				[
					-5.19921875,
					19.35546875
				],
				[
					-5.19921875,
					20.0390625
				],
				[
					-5.78515625,
					20.91015625
				],
				[
					-5.78515625,
					21.13671875
				],
				[
					-5.78515625,
					21.36328125
				],
				[
					-5.78515625,
					22.046875
				],
				[
					-5.78515625,
					22.2734375
				],
				[
					-5.78515625,
					22.95703125
				],
				[
					-5.203125,
					24.0546875
				],
				[
					-4.51953125,
					24.5078125
				],
				[
					-3.9375,
					25.37890625
				],
				[
					-3.25390625,
					26.0625
				],
				[
					-3.02734375,
					26.2890625
				],
				[
					-2.51171875,
					27.38671875
				],
				[
					-2.28515625,
					27.38671875
				],
				[
					-1.4140625,
					27.67578125
				],
				[
					-1.1875,
					27.67578125
				],
				[
					-0.734375,
					27.67578125
				],
				[
					1.34765625,
					26.62890625
				],
				[
					2.56640625,
					25.40625
				],
				[
					2.79296875,
					25.17578125
				],
				[
					3.375,
					24.30078125
				],
				[
					4.05859375,
					23.83984375
				],
				[
					4.05859375,
					23.83984375
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				4.05859375,
				23.83984375
			]
		},
		{
			"id": "6eDzOWCuitXC07m-zggWj",
			"type": "freedraw",
			"x": -123.58984375,
			"y": 128.625,
			"width": 1.69140625,
			"height": 14.91015625,
			"angle": 0,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1929032791,
			"version": 15,
			"versionNonce": 1089132537,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574822644,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.4609375,
					0.68359375
				],
				[
					-0.4609375,
					1.5546875
				],
				[
					-0.87109375,
					3.1796875
				],
				[
					-1.69140625,
					6.4296875
				],
				[
					-1.69140625,
					9.6796875
				],
				[
					-1.69140625,
					11.3046875
				],
				[
					-1.69140625,
					11.76171875
				],
				[
					-1.69140625,
					12.859375
				],
				[
					-1.69140625,
					13.31640625
				],
				[
					-1.69140625,
					14.2265625
				],
				[
					-1.69140625,
					14.453125
				],
				[
					-1.46484375,
					14.91015625
				],
				[
					-1.46484375,
					14.91015625
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				-1.46484375,
				14.91015625
			]
		},
		{
			"id": "PvRgB2CGatmvWnVFqY1zD",
			"type": "freedraw",
			"x": -133.640625,
			"y": 81.03515625,
			"width": 13.8984375,
			"height": 20.203125,
			"angle": 0,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1055876407,
			"version": 61,
			"versionNonce": 973348185,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574824879,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.23046875,
					0.2265625
				],
				[
					-0.23046875,
					2.72265625
				],
				[
					0.8125,
					5.8515625
				],
				[
					1.85546875,
					10.60546875
				],
				[
					2.375,
					13.734375
				],
				[
					3.1875,
					16.984375
				],
				[
					3.59375,
					18.609375
				],
				[
					3.59375,
					18.8359375
				],
				[
					3.59375,
					19.0625
				],
				[
					3.59375,
					19.51953125
				],
				[
					3.36328125,
					19.9765625
				],
				[
					3.1328125,
					20.203125
				],
				[
					3.1328125,
					19.97265625
				],
				[
					2.90234375,
					19.51171875
				],
				[
					2.609375,
					18.63671875
				],
				[
					2.609375,
					17.53125
				],
				[
					2.609375,
					15.1484375
				],
				[
					2.609375,
					13.3984375
				],
				[
					2.609375,
					12.9375
				],
				[
					2.37890625,
					12.4765625
				],
				[
					2.37890625,
					12.24609375
				],
				[
					2.37890625,
					11.78515625
				],
				[
					2.37890625,
					10.91015625
				],
				[
					2.37890625,
					10.44921875
				],
				[
					2.37890625,
					9.98828125
				],
				[
					2.37890625,
					9.52734375
				],
				[
					2.37890625,
					9.06640625
				],
				[
					2.37890625,
					8.60546875
				],
				[
					2.8359375,
					7.9140625
				],
				[
					3.0625,
					7.68359375
				],
				[
					3.2890625,
					7.453125
				],
				[
					3.515625,
					6.9921875
				],
				[
					3.7421875,
					6.53125
				],
				[
					3.7421875,
					6.0703125
				],
				[
					4.42578125,
					5.37890625
				],
				[
					4.71484375,
					4.50390625
				],
				[
					4.94140625,
					3.8125
				],
				[
					5.16796875,
					3.3515625
				],
				[
					5.62109375,
					2.66015625
				],
				[
					5.84765625,
					2.19921875
				],
				[
					6.07421875,
					1.96875
				],
				[
					6.30078125,
					1.5078125
				],
				[
					6.7578125,
					1.046875
				],
				[
					6.984375,
					0.5859375
				],
				[
					7.44140625,
					0.35546875
				],
				[
					7.66796875,
					0.125
				],
				[
					8.99609375,
					0.125
				],
				[
					9.22265625,
					0.125
				],
				[
					9.44921875,
					0.125
				],
				[
					9.67578125,
					0.125
				],
				[
					10.5859375,
					0.125
				],
				[
					11.16796875,
					0.99609375
				],
				[
					11.39453125,
					0.99609375
				],
				[
					12.078125,
					1.44921875
				],
				[
					12.53515625,
					1.67578125
				],
				[
					12.98828125,
					1.90234375
				],
				[
					13.21484375,
					1.90234375
				],
				[
					13.66796875,
					2.12890625
				],
				[
					13.66796875,
					2.12890625
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				13.66796875,
				2.12890625
			]
		},
		{
			"id": "5DsY4HxIAAUCsWER_yoVh",
			"type": "freedraw",
			"x": -295.27734375,
			"y": 183.296875,
			"width": 13.65625,
			"height": 2.8828125,
			"angle": 0,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1416532439,
			"version": 14,
			"versionNonce": 1699454361,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574826015,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.23046875,
					-0.23046875
				],
				[
					2.1484375,
					-0.70703125
				],
				[
					3.3671875,
					-1.9296875
				],
				[
					6.6171875,
					-2.40625
				],
				[
					8.99609375,
					-2.40625
				],
				[
					11.83203125,
					-2.8828125
				],
				[
					12.2890625,
					-2.8828125
				],
				[
					12.74609375,
					-2.8828125
				],
				[
					12.97265625,
					-2.8828125
				],
				[
					13.19921875,
					-2.8828125
				],
				[
					13.42578125,
					-2.8828125
				],
				[
					13.42578125,
					-2.8828125
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				13.42578125,
				-2.8828125
			]
		},
		{
			"id": "9P_9rXemdr_C8BTWiVeZ3",
			"type": "freedraw",
			"x": -291.4921875,
			"y": 169.16015625,
			"width": 3.5546875,
			"height": 20.8984375,
			"angle": 0,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 258194839,
			"version": 16,
			"versionNonce": 1678822297,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574826702,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.4609375,
					0.45703125
				],
				[
					-0.4609375,
					1.328125
				],
				[
					-0.75390625,
					2.19921875
				],
				[
					-1.80078125,
					6.19921875
				],
				[
					-2.2109375,
					7.82421875
				],
				[
					-3.14453125,
					12.578125
				],
				[
					-3.5546875,
					18.20703125
				],
				[
					-3.5546875,
					18.6640625
				],
				[
					-3.5546875,
					19.76171875
				],
				[
					-3.5546875,
					20.21875
				],
				[
					-3.5546875,
					20.4453125
				],
				[
					-3.5546875,
					20.671875
				],
				[
					-3.5546875,
					20.8984375
				],
				[
					-3.5546875,
					20.8984375
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				-3.5546875,
				20.8984375
			]
		},
		{
			"id": "wUUs7_aNJoP0igMBZITdT",
			"type": "freedraw",
			"x": -251.98828125,
			"y": 172.984375,
			"width": 16.54296875,
			"height": 21.734375,
			"angle": 0,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1894395799,
			"version": 36,
			"versionNonce": 1771967257,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574827849,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.3984375,
					-1.16796875
				],
				[
					-3.02734375,
					-1.984375
				],
				[
					-4.77734375,
					-1.984375
				],
				[
					-8.03515625,
					-2.39453125
				],
				[
					-9.6640625,
					-2.8046875
				],
				[
					-9.89453125,
					-2.8046875
				],
				[
					-10.5859375,
					-2.8046875
				],
				[
					-11.046875,
					-2.3515625
				],
				[
					-11.5078125,
					-2.125
				],
				[
					-12.09375,
					-1.02734375
				],
				[
					-12.38671875,
					-0.15625
				],
				[
					-13.203125,
					1.92578125
				],
				[
					-13.203125,
					2.796875
				],
				[
					-13.61328125,
					4.421875
				],
				[
					-14.0234375,
					6.046875
				],
				[
					-14.83984375,
					8.12890625
				],
				[
					-15.25,
					9.75390625
				],
				[
					-16.3125,
					13.00390625
				],
				[
					-16.3125,
					13.875
				],
				[
					-16.54296875,
					14.33203125
				],
				[
					-16.54296875,
					15.4296875
				],
				[
					-16.54296875,
					15.8828125
				],
				[
					-16.54296875,
					16.109375
				],
				[
					-16.54296875,
					16.3359375
				],
				[
					-16.54296875,
					16.5625
				],
				[
					-16.54296875,
					17.015625
				],
				[
					-16.0859375,
					17.47265625
				],
				[
					-13.58984375,
					18.16796875
				],
				[
					-12.71875,
					18.45703125
				],
				[
					-11.09375,
					18.45703125
				],
				[
					-5.5859375,
					18.9296875
				],
				[
					-3.9609375,
					18.9296875
				],
				[
					-2.6328125,
					18.9296875
				],
				[
					-2.6328125,
					18.9296875
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				-2.6328125,
				18.9296875
			]
		},
		{
			"id": "7glWiV5T5ZtCvyaSf-mYN",
			"type": "freedraw",
			"x": -311.921875,
			"y": 183.7890625,
			"width": 17.109375,
			"height": 2.6875,
			"angle": 0,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1097142295,
			"version": 18,
			"versionNonce": 561745625,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574828933,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.45703125,
					-0.69140625
				],
				[
					1.5546875,
					-1.21484375
				],
				[
					3.93359375,
					-1.69140625
				],
				[
					5.55859375,
					-1.69140625
				],
				[
					7.30078125,
					-1.984375
				],
				[
					9.6796875,
					-1.984375
				],
				[
					11.421875,
					-2.27734375
				],
				[
					12.29296875,
					-2.27734375
				],
				[
					14.375,
					-2.6875
				],
				[
					14.83203125,
					-2.6875
				],
				[
					15.515625,
					-2.6875
				],
				[
					15.7421875,
					-2.6875
				],
				[
					16.42578125,
					-2.6875
				],
				[
					16.8828125,
					-2.6875
				],
				[
					17.109375,
					-2.6875
				],
				[
					17.109375,
					-2.6875
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				17.109375,
				-2.6875
			]
		},
		{
			"id": "SGzjBF8cOXvSpDzmwKOJJ",
			"type": "freedraw",
			"x": -109.16015625,
			"y": 131.07421875,
			"width": 1.5703125,
			"height": 14.48046875,
			"angle": 0,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1164978263,
			"version": 14,
			"versionNonce": 1498836761,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574831540,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					2.30859375
				],
				[
					-0.5234375,
					5.4375
				],
				[
					-0.5234375,
					5.89453125
				],
				[
					-1.046875,
					9.0234375
				],
				[
					-1.33984375,
					11.51953125
				],
				[
					-1.5703125,
					12.43359375
				],
				[
					-1.5703125,
					12.66015625
				],
				[
					-1.5703125,
					12.88671875
				],
				[
					-1.5703125,
					13.5703125
				],
				[
					-1.5703125,
					13.796875
				],
				[
					-1.5703125,
					14.48046875
				],
				[
					-1.5703125,
					14.48046875
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				-1.5703125,
				14.48046875
			]
		},
		{
			"id": "Ef4nCQJ62tclm2jjUaPFW",
			"type": "freedraw",
			"x": -106.60546875,
			"y": 96.25,
			"width": 11.5390625,
			"height": 19.0703125,
			"angle": 0,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1771453657,
			"version": 28,
			"versionNonce": 1358840439,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574838941,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.45703125
				],
				[
					1.10546875,
					5.7890625
				],
				[
					2.09765625,
					11.296875
				],
				[
					2.50390625,
					12.921875
				],
				[
					2.91015625,
					15.41796875
				],
				[
					3.13671875,
					15.64453125
				],
				[
					3.13671875,
					16.328125
				],
				[
					3.13671875,
					16.5546875
				],
				[
					2.66015625,
					12.54296875
				],
				[
					2.66015625,
					10.16015625
				],
				[
					2.66015625,
					8.53125
				],
				[
					3.06640625,
					6.02734375
				],
				[
					3.06640625,
					5.15234375
				],
				[
					4.69140625,
					1.89453125
				],
				[
					5.50390625,
					0.265625
				],
				[
					6.31640625,
					-1.82421875
				],
				[
					6.54296875,
					-2.0546875
				],
				[
					6.54296875,
					-2.28515625
				],
				[
					6.76953125,
					-2.515625
				],
				[
					7.6796875,
					-2.515625
				],
				[
					8.13671875,
					-2.515625
				],
				[
					8.36328125,
					-2.515625
				],
				[
					10.859375,
					-1.93359375
				],
				[
					11.0859375,
					-1.93359375
				],
				[
					11.5390625,
					-1.70703125
				],
				[
					11.5390625,
					-1.70703125
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				11.5390625,
				-1.70703125
			]
		},
		{
			"id": "dbVd9MlaC8u67jf6mf0Hy",
			"type": "freedraw",
			"x": -96.6796875,
			"y": 100.7265625,
			"width": 17.44140625,
			"height": 0,
			"angle": 0,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 107056473,
			"version": 10,
			"versionNonce": 318106039,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574839708,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.45703125,
					0
				],
				[
					2.8359375,
					0
				],
				[
					6.8359375,
					0
				],
				[
					9.96484375,
					0
				],
				[
					16.98828125,
					0
				],
				[
					17.21484375,
					0
				],
				[
					17.44140625,
					0
				],
				[
					17.44140625,
					0
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				17.44140625,
				0
			]
		},
		{
			"id": "6bWnRrDc8_luXoyyrit5h",
			"type": "freedraw",
			"x": -89.65234375,
			"y": 90.75390625,
			"width": 1.59375,
			"height": 23.07421875,
			"angle": 0,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2017419801,
			"version": 13,
			"versionNonce": 1182527575,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574840248,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.23046875,
					0.87109375
				],
				[
					-0.23046875,
					3.25
				],
				[
					-0.23046875,
					8.00390625
				],
				[
					-0.23046875,
					11.1328125
				],
				[
					-0.70703125,
					15.13671875
				],
				[
					-1.18359375,
					17.515625
				],
				[
					-1.18359375,
					19.59765625
				],
				[
					-1.59375,
					21.22265625
				],
				[
					-1.59375,
					22.84765625
				],
				[
					-1.59375,
					23.07421875
				],
				[
					-1.59375,
					23.07421875
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				-1.59375,
				23.07421875
			]
		},
		{
			"id": "1gpBvR5Y9KFDWbvC4DWpa",
			"type": "freedraw",
			"x": -69.2421875,
			"y": 88.46484375,
			"width": 1.66796875,
			"height": 25.01171875,
			"angle": 0,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 167586169,
			"version": 10,
			"versionNonce": 1208860567,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574840822,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.2265625
				],
				[
					-0.5234375,
					7.359375
				],
				[
					-1.66796875,
					15.91015625
				],
				[
					-1.66796875,
					19.8046875
				],
				[
					-1.66796875,
					23.16015625
				],
				[
					-1.66796875,
					24.78515625
				],
				[
					-1.66796875,
					25.01171875
				],
				[
					-1.66796875,
					25.01171875
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				-1.66796875,
				25.01171875
			]
		},
		{
			"id": "AwNIWN7n2P-Z_cG1jaJZB",
			"type": "freedraw",
			"x": -120.91796875,
			"y": 173.1015625,
			"width": 14.203125,
			"height": 0.23046875,
			"angle": 0,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 386684473,
			"version": 9,
			"versionNonce": 1652968887,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574842091,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					6.3828125,
					0
				],
				[
					8.76171875,
					0
				],
				[
					11.140625,
					0
				],
				[
					13.51953125,
					0
				],
				[
					13.9765625,
					0
				],
				[
					14.203125,
					-0.23046875
				],
				[
					14.203125,
					-0.23046875
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				14.203125,
				-0.23046875
			]
		},
		{
			"id": "AzLWkQjB76SoW9leJQwv3",
			"type": "freedraw",
			"x": -86.27734375,
			"y": 163.8359375,
			"width": 16.66015625,
			"height": 17.03515625,
			"angle": 0,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2080095769,
			"version": 59,
			"versionNonce": 708805655,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713574844409,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.4609375,
					-0.4609375
				],
				[
					-1.15234375,
					-0.921875
				],
				[
					-2.48828125,
					-0.921875
				],
				[
					-2.94921875,
					-0.921875
				],
				[
					-6.08203125,
					-0.921875
				],
				[
					-8.5859375,
					-0.921875
				],
				[
					-10.21484375,
					-0.921875
				],
				[
					-12.3046875,
					-0.46484375
				],
				[
					-12.765625,
					-0.0078125
				],
				[
					-13.2265625,
					0.21875
				],
				[
					-13.6875,
					0.67578125
				],
				[
					-13.91796875,
					0.90234375
				],
				[
					-14.734375,
					2.45703125
				],
				[
					-15.1953125,
					3.37109375
				],
				[
					-15.48828125,
					4.2421875
				],
				[
					-15.48828125,
					5.5703125
				],
				[
					-15.78125,
					6.44140625
				],
				[
					-16.3671875,
					8.18359375
				],
				[
					-16.3671875,
					9.0546875
				],
				[
					-16.66015625,
					10.15234375
				],
				[
					-16.66015625,
					10.609375
				],
				[
					-16.66015625,
					11.48046875
				],
				[
					-16.66015625,
					11.70703125
				],
				[
					-16.66015625,
					11.93359375
				],
				[
					-16.43359375,
					12.16015625
				],
				[
					-16.20703125,
					12.38671875
				],
				[
					-16.20703125,
					12.61328125
				],
				[
					-15.98046875,
					13.0703125
				],
				[
					-15.52734375,
					13.52734375
				],
				[
					-15.30078125,
					13.75390625
				],
				[
					-14.84765625,
					13.75390625
				],
				[
					-14.62109375,
					13.98046875
				],
				[
					-14.39453125,
					14.20703125
				],
				[
					-14.16796875,
					14.20703125
				],
				[
					-13.484375,
					14.43359375
				],
				[
					-13.2578125,
					14.43359375
				],
				[
					-12.16015625,
					15.2421875
				],
				[
					-11.578125,
					16.11328125
				],
				[
					-11.3515625,
					16.11328125
				],
				[
					-10.8984375,
					16.11328125
				],
				[
					-10.02734375,
					16.11328125
				],
				[
					-9.80078125,
					16.11328125
				],
				[
					-9.1171875,
					16.11328125
				],
				[
					-8.890625,
					16.11328125
				],
				[
					-8.6640625,
					16.11328125
				],
				[
					-7.0390625,
					16.11328125
				],
				[
					-6.58203125,
					16.11328125
				],
				[
					-5.8984375,
					16.11328125
				],
				[
					-5.671875,
					16.11328125
				],
				[
					-5.4453125,
					15.8828125
				],
				[
					-4.98828125,
					15.8828125
				],
				[
					-4.1171875,
					15.58984375
				],
				[
					-2.4921875,
					15.1796875
				],
				[
					-1.80859375,
					14.94921875
				],
				[
					-1.3515625,
					14.94921875
				],
				[
					-1.125,
					14.71875
				],
				[
					-1.125,
					14.71875
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				-1.125,
				14.71875
			]
		},
		{
			"id": "oXbyWJJO",
			"type": "text",
			"x": -378.69921875,
			"y": 250.307373046875,
			"width": 556,
			"height": 175,
			"angle": 0,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 67283385,
			"version": 342,
			"versionNonce": 1561940887,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713576696220,
			"link": null,
			"locked": false,
			"text": "首先明确a 是b的前缀和\n那么我们假设 a是为0的数组,那么它的差分数组也必然是为0  \n构建差分数组相当于是在这个区间插入a[i]\nb   b1  b2  b3 b4 b5 b6 \n\na   a1 a2 a3 a4 a5 a6 \n               ",
			"rawText": "首先明确a 是b的前缀和\n那么我们假设 a是为0的数组,那么它的差分数组也必然是为0  \n构建差分数组相当于是在这个区间插入a[i]\nb   b1  b2  b3 b4 b5 b6 \n\na   a1 a2 a3 a4 a5 a6 \n               ",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "首先明确a 是b的前缀和\n那么我们假设 a是为0的数组,那么它的差分数组也必然是为0  \n构建差分数组相当于是在这个区间插入a[i]\nb   b1  b2  b3 b4 b5 b6 \n\na   a1 a2 a3 a4 a5 a6 \n               ",
			"lineHeight": 1.25
		},
		{
			"id": "MjbV5QCs",
			"type": "text",
			"x": -383.0703125,
			"y": 430.5341796875,
			"width": 824.7798461914062,
			"height": 225,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1518946039,
			"version": 343,
			"versionNonce": 1211958903,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1713577053758,
			"link": null,
			"locked": false,
			"text": "先构建差分数组 根据公式 bn = an -an-1\n\nb   a1   a2-a1   a3-a2    a4-a3   a5-a4      a6-a5 \n\n在1-3 区间+c   \nb   a1+c a2-a1   a3-a2     a4-a3-c   a5-a4    a6-a5\na   a1+c a2+c   a3+c       a4         a5       a6  // 这样就在原数组的基础上+c\n   \n ",
			"rawText": "先构建差分数组 根据公式 bn = an -an-1\n\nb   a1   a2-a1   a3-a2    a4-a3   a5-a4      a6-a5 \n\n在1-3 区间+c   \nb   a1+c a2-a1   a3-a2     a4-a3-c   a5-a4    a6-a5\na   a1+c a2+c   a3+c       a4         a5       a6  // 这样就在原数组的基础上+c\n   \n ",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "先构建差分数组 根据公式 bn = an -an-1\n\nb   a1   a2-a1   a3-a2    a4-a3   a5-a4      a6-a5 \n\n在1-3 区间+c   \nb   a1+c a2-a1   a3-a2     a4-a3-c   a5-a4    a6-a5\na   a1+c a2+c   a3+c       a4         a5       a6  // 这样就在原数组的基础上+c\n   \n ",
			"lineHeight": 1.25
		},
		{
			"id": "S5L9VDCPcFPErqB63n2G8",
			"type": "freedraw",
			"x": -326.296875,
			"y": -212.890625,
			"width": 0.23046875,
			"height": 25.671875,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1752925399,
			"version": 16,
			"versionNonce": 226121017,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1713574519658,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.23046875
				],
				[
					0,
					0.2265625
				],
				[
					0,
					2.72265625
				],
				[
					0,
					4.34765625
				],
				[
					0,
					10.62109375
				],
				[
					0,
					20.0234375
				],
				[
					0,
					22.10546875
				],
				[
					0,
					22.5625
				],
				[
					0,
					24.1171875
				],
				[
					0,
					24.34375
				],
				[
					0,
					25.21484375
				],
				[
					-0.23046875,
					25.44140625
				],
				[
					-0.23046875,
					25.44140625
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				-0.23046875,
				25.44140625
			]
		}
	],
	"appState": {
		"theme": "light",
		"viewBackgroundColor": "#ffffff",
		"currentItemStrokeColor": "#1971c2",
		"currentItemBackgroundColor": "transparent",
		"currentItemFillStyle": "solid",
		"currentItemStrokeWidth": 0.5,
		"currentItemStrokeStyle": "solid",
		"currentItemRoughness": 1,
		"currentItemOpacity": 100,
		"currentItemFontFamily": 1,
		"currentItemFontSize": 20,
		"currentItemTextAlign": "left",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"scrollX": 407.68359375,
		"scrollY": -108.5185546875,
		"zoom": {
			"value": 1
		},
		"currentItemRoundness": "round",
		"gridSize": null,
		"gridColor": {
			"Bold": "#C9C9C9FF",
			"Regular": "#EDEDEDFF"
		},
		"currentStrokeOptions": null,
		"previousGridSize": null,
		"frameRendering": {
			"enabled": true,
			"clip": true,
			"name": true,
			"outline": true
		}
	},
	"files": {}
}
```
%%