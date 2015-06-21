# API

Converters:

	rgb: {
		fromHex(hex) -> RGB,
		toHex(RGB) -> hex
	}
	xyz(rgbSpace?=workspace.sRGB, whitePoint?=illuminant.D65) -> {
		fromRgb(RGB) -> XYZ,
		toRgb(XYZ) -> RGB,
	},
	cam(viewingConditions?) -> {
		fromXyz(XYZ) -> CAM,
		toXyz(CAM) -> XYZ
	},
	ucs(name?="UCS") -> {
		fromCam(CAM) -> UCS,
		toCam(UCS) -> CAM,
		distance(UCS1, UCS2) -> number
	}

Default viewing conditions:

	{
		whitePoint: illuminant.D65,
		adaptingLuminance: 40,
		backgroundLuminance: 20,
		surroundType: "average",
		discounting: false
	}
