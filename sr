// Клас "Розумний будинок"
class SmartHouse {
    constructor(name) {
        this.name = name
        this.devices = []
    }

    addDevice(device) {
        this.devices.push(device)
    }

    getDevices() {
        return this.devices
    }

    getDeviceByName(deviceName) {
        return this.devices.find(device => device.name === deviceName)
    }

    offAllDevice() {
        this.devices.forEach(device => {
            device.off()
        })
    }
}

// Базовий клас пристрою
class Device {
    constructor(name) {
        this.name = name
        this.isOn = false
    }

    on() {
        this.isOn = true
        console.log(`${this.name} turned on.`)
    }

    off() {
        this.isOn = false
        console.log(`${this.name} turned off.`)
    }
}

// Клас для лампи
class Lamp extends Device {
    constructor(name) {
        super(name)
    }

    changeBrightness(level) {
        console.log(`${this.name} brightness changed to ${level}.`)
    }
}

// Клас для жалюзів, який успадковує властивості від базового класу пристрою
class Blinds extends Device {
    constructor(name) {
        super(name)
    }

    raise() {
        console.log(`${this.name} raised.`)
    }

    lower() {
        console.log(`${this.name} lowered.`)
    }
}

// Клас для сигналізації
class Alarm extends Device {
    constructor(name) {
        super(name)
    }

    activate() {
        console.log(`${this.name} activated.`)
    }

    deactivate() {
        console.log(`${this.name} deactivated.`)
    }
}

// Створення розумного будинку та додавання пристроїв
const sh = new SmartHouse("MySmartHouse")
sh.addDevice(new Lamp("LivingRoomLamp"))
sh.addDevice(new Blinds("BedroomBlinds"))
sh.addDevice(new Alarm("HomeAlarm"))

// Взаємодія з пристроями
sh.getDevices().forEach(device => {
    device.on()
})

sh.getDeviceByName("BedroomBlinds").raise()
sh.getDeviceByName("LivingRoomLamp").changeBrightness(50)
sh.offAllDevice()
