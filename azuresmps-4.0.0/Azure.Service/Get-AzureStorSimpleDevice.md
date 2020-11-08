---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C5A2A8D2-A840-4712-A8BD-F49C6063D193
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1156b4887e7b97d4e783ec738a939d320fe397a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055258"
---
# <span data-ttu-id="e849c-101">Get-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="e849c-101">Get-AzureStorSimpleDevice</span></span>

## <span data-ttu-id="e849c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e849c-102">SYNOPSIS</span></span>
<span data-ttu-id="e849c-103">Pobiera urządzenia dołączone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="e849c-103">Gets devices attached to the resource.</span></span>

## <span data-ttu-id="e849c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e849c-104">SYNTAX</span></span>

### <span data-ttu-id="e849c-105">Empty (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e849c-105">Empty (Default)</span></span>
```
Get-AzureStorSimpleDevice [-Type <String>] [-ModelID <String>] [-Detailed] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e849c-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="e849c-106">IdentifyById</span></span>
```
Get-AzureStorSimpleDevice [-DeviceId <String>] [-Type <String>] [-ModelID <String>] [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e849c-107">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="e849c-107">IdentifyByName</span></span>
```
Get-AzureStorSimpleDevice [-DeviceName <String>] [-Type <String>] [-ModelID <String>] [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e849c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e849c-108">DESCRIPTION</span></span>
<span data-ttu-id="e849c-109">Polecenie cmdlet **Get-AzureStorSimpleDevice** pobiera listę urządzeń StorSimple dołączonych do zasobu.</span><span class="sxs-lookup"><span data-stu-id="e849c-109">The **Get-AzureStorSimpleDevice** cmdlet gets a list of StorSimple devices attached to the resource.</span></span>
<span data-ttu-id="e849c-110">Możesz określić identyfikator urządzenia, nazwę, Identyfikator modelu i typ.</span><span class="sxs-lookup"><span data-stu-id="e849c-110">You can specify device ID, name, model ID, and type.</span></span>
<span data-ttu-id="e849c-111">Użyj właściwości **DeviceID** otrzymanej za pomocą tego polecenia cmdlet, aby określić urządzenia dla innych poleceń cmdlet StorSimple.</span><span class="sxs-lookup"><span data-stu-id="e849c-111">Use the **DeviceID** property obtained by using this cmdlet to specify devices for other StorSimple cmdlets.</span></span>

## <span data-ttu-id="e849c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e849c-112">EXAMPLES</span></span>

### <span data-ttu-id="e849c-113">Przykład 1: uzyskiwanie dostępnych urządzeń w zasobie</span><span class="sxs-lookup"><span data-stu-id="e849c-113">Example 1: Get available devices on a resource</span></span>
```
PS C:\>Get-AzureStorSimpleDevice
DeviceId                  : 6f9ab151-39c7-4ded-b7d0-f5b0968f2766
DeviceName                : 8600-: SHX0881018G88
SerialNumber              : SHX0881018G88
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Offline
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx0991018g00e4-target
TimeZone                  : Pacific Standard Time
ActivationTime            : 2015-04-07T16:32:30.2960842Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 12693995520

DeviceId                  : eb30ea31-c856-4cf2-9a02-aee611d6a3b9
DeviceName                : 8100-Delta 001
SerialNumber              : SHX90391XXXXXXX
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8100
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8100-shx90193xxxxxxx-target
TimeZone                  : Eastern Standard Time
ActivationTime            : 2015-03-26T14:53:14.4219391Z
AvailableStorageInBytes   : 205509890146304
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 219902325555200
UsingStorageInBytes       : 23904321536

DeviceId                  : edcb0b9b-1ed5-4102-9c5d-c589f7632994
DeviceName                : 8600-Bravo 001
SerialNumber              : SHX0900915G44SY
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx0900915g44sy-target
TimeZone                  : Eastern Standard Time
ActivationTime            : 2015-03-26T15:36:26.0870525Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 978893799424
```

<span data-ttu-id="e849c-114">To polecenie pobiera wszystkie dostępne urządzenia w zasobie.</span><span class="sxs-lookup"><span data-stu-id="e849c-114">This command gets all available devices on a resource.</span></span>
<span data-ttu-id="e849c-115">W tym przykładzie jest dostępne tylko jedno urządzenie.</span><span class="sxs-lookup"><span data-stu-id="e849c-115">In this example, only one device is available.</span></span>

### <span data-ttu-id="e849c-116">Przykład 2: uzyskiwanie określonych dostępnych urządzeń w zasobie</span><span class="sxs-lookup"><span data-stu-id="e849c-116">Example 2: Get specific available devices on a resource</span></span>
```
PS C:\>Get-AzureStorSimpleDevice -DeviceName "8600-SHX90193XXXXXXX" -Type Appliance -ModelId "8600"
DeviceId                  : f9db31da-8a6c-4718-8f5b-5ce89e600f28
DeviceName                : 8600-SHX90193XXXXXXX
SerialNumber              : SHX90193XXXXXXX
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx90193xxxxxxx-target
TimeZone                  : Pacific Standard Time
ActivationTime            : 2015-04-07T18:10:46.4524766Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 14445182976
```

<span data-ttu-id="e849c-117">To polecenie pobiera wszystkie dostępne urządzenia z zasobu o określonej nazwie, typie i IDENTYFIKATORze modelu.</span><span class="sxs-lookup"><span data-stu-id="e849c-117">This command gets all available devices on a resource that have the specified name, type, and model ID.</span></span>

### <span data-ttu-id="e849c-118">Przykład 3: uzyskiwanie szczegółowych informacji dotyczących urządzenia</span><span class="sxs-lookup"><span data-stu-id="e849c-118">Example 3: Get details for a device</span></span>
```
PS C:\>Get-AzureStorSimpleDevice -Name "8600-SHX90193XXXXXXX" -Type Appliance -Detailed
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : f9db31da-8a6c-4718-8f5b-5ce89e600f28
Name                           : 
NetInterfaceList               : {Data0, Data1, Data2, Data3...} 
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings

RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : Appliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings
```

<span data-ttu-id="e849c-119">To polecenie pobiera wszystkie dostępne urządzenia w zasobie o określonej nazwie i typie.</span><span class="sxs-lookup"><span data-stu-id="e849c-119">This command gets all available devices on a resource that have the specified name and type.</span></span>
<span data-ttu-id="e849c-120">To polecenie określa parametr *szczegółowy* .</span><span class="sxs-lookup"><span data-stu-id="e849c-120">This command specifies the *Detailed* parameter.</span></span>
<span data-ttu-id="e849c-121">Polecenie udostępnia dodatkowe informacje o urządzeniach, które zwraca.</span><span class="sxs-lookup"><span data-stu-id="e849c-121">The command provides additional details about the devices it returns.</span></span>

## <span data-ttu-id="e849c-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e849c-122">PARAMETERS</span></span>

### <span data-ttu-id="e849c-123">— Szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="e849c-123">-Detailed</span></span>
<span data-ttu-id="e849c-124">Wskazuje, że to polecenie cmdlet zwraca dane urządzenia dotyczące urządzeń, które otrzymuje.</span><span class="sxs-lookup"><span data-stu-id="e849c-124">Indicates that this cmdlet returns device details for the devices that it gets.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e849c-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e849c-125">-DeviceId</span></span>
<span data-ttu-id="e849c-126">Określa identyfikator wystąpienia urządzenia do pobrania.</span><span class="sxs-lookup"><span data-stu-id="e849c-126">Specifies the instance ID of the device to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e849c-127">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e849c-127">-DeviceName</span></span>
<span data-ttu-id="e849c-128">Określa nazwę urządzenia StorSimple do pobrania.</span><span class="sxs-lookup"><span data-stu-id="e849c-128">Specifies the name of the StorSimple device to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e849c-129">-ModelID</span><span class="sxs-lookup"><span data-stu-id="e849c-129">-ModelID</span></span>
<span data-ttu-id="e849c-130">Określa identyfikator modelu urządzeń StorSimple.</span><span class="sxs-lookup"><span data-stu-id="e849c-130">Specifies the ID of the model of StorSimple devices to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e849c-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="e849c-131">-Profile</span></span>
<span data-ttu-id="e849c-132">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e849c-132">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e849c-133">-Type</span><span class="sxs-lookup"><span data-stu-id="e849c-133">-Type</span></span>
<span data-ttu-id="e849c-134">Umożliwia określenie typu urządzenia StorSimple.</span><span class="sxs-lookup"><span data-stu-id="e849c-134">Specifies the type of a StorSimple device.</span></span>
<span data-ttu-id="e849c-135">Prawidłowe wartości to: urządzenie i VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="e849c-135">Valid values are: Appliance and VirtualAppliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e849c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e849c-136">CommonParameters</span></span>
<span data-ttu-id="e849c-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e849c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e849c-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e849c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e849c-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e849c-139">INPUTS</span></span>

### <span data-ttu-id="e849c-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e849c-140">None</span></span>

## <span data-ttu-id="e849c-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e849c-141">OUTPUTS</span></span>

### <span data-ttu-id="e849c-142">Lista \<DeviceDetails\> , IEnumerable\<DeviceInfo\></span><span class="sxs-lookup"><span data-stu-id="e849c-142">List\<DeviceDetails\>, IEnumerable\<DeviceInfo\></span></span>
<span data-ttu-id="e849c-143">To polecenie cmdlet zwraca **obiekt \<DeviceDetails\> listy** , jeśli określono parametr *szczegółowy* .</span><span class="sxs-lookup"><span data-stu-id="e849c-143">This cmdlet returns a **List\<DeviceDetails\>** object, if you specify the *Detailed* parameter.</span></span>
<span data-ttu-id="e849c-144">Jeśli nie określisz tego parametru, zwraca obiekt **IEnumerable \<DeviceInfo\>** .</span><span class="sxs-lookup"><span data-stu-id="e849c-144">If you do not specify that parameter, it returns an **IEnumerable\<DeviceInfo\>** object.</span></span>

## <span data-ttu-id="e849c-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e849c-145">NOTES</span></span>

## <span data-ttu-id="e849c-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e849c-146">RELATED LINKS</span></span>

[<span data-ttu-id="e849c-147">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="e849c-147">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)

[<span data-ttu-id="e849c-148">Wybierz — AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="e849c-148">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


