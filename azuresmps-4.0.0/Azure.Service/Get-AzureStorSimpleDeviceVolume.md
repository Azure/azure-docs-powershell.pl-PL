---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 79EE846E-D5BE-4808-BC6F-E3B16A308AB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9d0cd7ef0eacc7ff3e38c4619b60a0bd61f24f1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054532"
---
# <span data-ttu-id="9ddaa-101">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="9ddaa-101">Get-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="9ddaa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ddaa-102">SYNOPSIS</span></span>
<span data-ttu-id="9ddaa-103">Pobiera woluminy na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="9ddaa-103">Gets volumes on a device.</span></span>

## <span data-ttu-id="9ddaa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ddaa-104">SYNTAX</span></span>

### <span data-ttu-id="9ddaa-105">IdentifyByParentObject</span><span class="sxs-lookup"><span data-stu-id="9ddaa-105">IdentifyByParentObject</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9ddaa-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="9ddaa-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ddaa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9ddaa-107">DESCRIPTION</span></span>
<span data-ttu-id="9ddaa-108">Polecenie cmdlet **Get-AzureStorSimpleDeviceVolume** pobiera listę woluminów dla określonego kontenera woluminu lub woluminu o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="9ddaa-108">The **Get-AzureStorSimpleDeviceVolume** cmdlet gets a list of volumes for a specified volume container, or volume that has the specified name.</span></span>
<span data-ttu-id="9ddaa-109">Zwrócony obiekt zawiera następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="9ddaa-109">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="9ddaa-110">**Program accessType**</span><span class="sxs-lookup"><span data-stu-id="9ddaa-110">**AccessType**</span></span>
- <span data-ttu-id="9ddaa-111">**AcrList**</span><span class="sxs-lookup"><span data-stu-id="9ddaa-111">**AcrList**</span></span>
- <span data-ttu-id="9ddaa-112">**AppType**</span><span class="sxs-lookup"><span data-stu-id="9ddaa-112">**AppType**</span></span>
- <span data-ttu-id="9ddaa-113">**Kontenery**</span><span class="sxs-lookup"><span data-stu-id="9ddaa-113">**DataContainer**</span></span>
- <span data-ttu-id="9ddaa-114">**DataContainerId**</span><span class="sxs-lookup"><span data-stu-id="9ddaa-114">**DataContainerId**</span></span>
- <span data-ttu-id="9ddaa-115">**Obiektu**</span><span class="sxs-lookup"><span data-stu-id="9ddaa-115">**InstanceId**</span></span>
- <span data-ttu-id="9ddaa-116">**IsBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="9ddaa-116">**IsBackupEnabled**</span></span>
- <span data-ttu-id="9ddaa-117">**IsDefaultBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="9ddaa-117">**IsDefaultBackupEnabled**</span></span>
- <span data-ttu-id="9ddaa-118">**IsMonitoringEnabled**</span><span class="sxs-lookup"><span data-stu-id="9ddaa-118">**IsMonitoringEnabled**</span></span>
- <span data-ttu-id="9ddaa-119">**Nazwę**</span><span class="sxs-lookup"><span data-stu-id="9ddaa-119">**Name**</span></span>
- <span data-ttu-id="9ddaa-120">**Ekran**</span><span class="sxs-lookup"><span data-stu-id="9ddaa-120">**Online**</span></span>
- <span data-ttu-id="9ddaa-121">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="9ddaa-121">**OperationInProgress**</span></span>
- <span data-ttu-id="9ddaa-122">**SizeInBytes**</span><span class="sxs-lookup"><span data-stu-id="9ddaa-122">**SizeInBytes**</span></span>
- <span data-ttu-id="9ddaa-123">**VSN**</span><span class="sxs-lookup"><span data-stu-id="9ddaa-123">**VSN**</span></span>

## <span data-ttu-id="9ddaa-124">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ddaa-124">EXAMPLES</span></span>

### <span data-ttu-id="9ddaa-125">Przykład 1: pobieranie woluminów w określonym kontenerze</span><span class="sxs-lookup"><span data-stu-id="9ddaa-125">Example 1: Get volumes in a specified container</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container03" | Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
InstanceId             : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c
Name                   : Volume 1 Clone
Online                 : True
SizeInBytes            : 3298534883328
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c

InstanceId             : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe
Name                   : Volume 3 Clone
Online                 : True
SizeInBytes            : 1717986918400
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe

InstanceId             : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
Name                   : Volume 4
Online                 : True
SizeInBytes            : 1610612736000
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
```

<span data-ttu-id="9ddaa-126">To polecenie pobiera kontener woluminu o nazwie Container03 na urządzeniu o nazwie Contoso63-AppVm przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="9ddaa-126">This command gets the volume container named Container03 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="9ddaa-127">W poleceniu użyto operatora potoku w celu przekazania tego kontenera do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ddaa-127">The command uses the pipeline operator to pass that container to the current cmdlet.</span></span>
<span data-ttu-id="9ddaa-128">To polecenie cmdlet umożliwia pobieranie wszystkich woluminów w kontenerze dla urządzenia o nazwie Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="9ddaa-128">That cmdlet gets all the volumes in that container for the device named Contoso63-AppVm.</span></span>

### <span data-ttu-id="9ddaa-129">Przykład 2: uzyskiwanie woluminu przy użyciu jego nazwy</span><span class="sxs-lookup"><span data-stu-id="9ddaa-129">Example 2: Get a volume by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18"
InstanceId             : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
Name                   : Volume18
Online                 : True
SizeInBytes            : 2748779069440
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
```

<span data-ttu-id="9ddaa-130">To polecenie pobiera wolumin o nazwie Volume18 na urządzeniu o nazwie Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="9ddaa-130">This command gets the volume named Volume18 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="9ddaa-131">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ddaa-131">PARAMETERS</span></span>

### <span data-ttu-id="9ddaa-132">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9ddaa-132">-DeviceName</span></span>
<span data-ttu-id="9ddaa-133">Określa nazwę urządzenia StorSimple, z którego mają być uzyskiwane woluminy.</span><span class="sxs-lookup"><span data-stu-id="9ddaa-133">Specifies the name of the StorSimple device from which to get volumes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddaa-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="9ddaa-134">-Profile</span></span>
<span data-ttu-id="9ddaa-135">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9ddaa-135">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="9ddaa-136">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="9ddaa-136">-VolumeContainer</span></span>
<span data-ttu-id="9ddaa-137">Określa kontener woluminu, **który zawiera** woluminy do pobrania.</span><span class="sxs-lookup"><span data-stu-id="9ddaa-137">Specifies the volume container, as a **DataContainer** object, that includes the volumes to get.</span></span>
<span data-ttu-id="9ddaa-138">Aby uzyskać **kontener** elementu, użyj polecenia cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="9ddaa-138">To obtain a **DataContainer** , use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: IdentifyByParentObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ddaa-139">-Nazwa_woluminu</span><span class="sxs-lookup"><span data-stu-id="9ddaa-139">-VolumeName</span></span>
<span data-ttu-id="9ddaa-140">Określa nazwę woluminu, który ma być wyświetlany.</span><span class="sxs-lookup"><span data-stu-id="9ddaa-140">Specifies the name of the volume to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddaa-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ddaa-141">CommonParameters</span></span>
<span data-ttu-id="9ddaa-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ddaa-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ddaa-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ddaa-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ddaa-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ddaa-144">INPUTS</span></span>

### <span data-ttu-id="9ddaa-145">Kontenery</span><span class="sxs-lookup"><span data-stu-id="9ddaa-145">DataContainer</span></span>
<span data-ttu-id="9ddaa-146">To polecenie cmdlet umożliwia akceptowanie obiektu **kontenera** zawierającego dane, który zawiera wolumin do pobrania.</span><span class="sxs-lookup"><span data-stu-id="9ddaa-146">This cmdlet accepts a **DataContainer** object that contains the volume to get.</span></span>

## <span data-ttu-id="9ddaa-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ddaa-147">OUTPUTS</span></span>

### <span data-ttu-id="9ddaa-148">VirtualDisk, IList\<VirtualDisk\></span><span class="sxs-lookup"><span data-stu-id="9ddaa-148">VirtualDisk, IList\<VirtualDisk\></span></span>
<span data-ttu-id="9ddaa-149">To polecenie cmdlet zwraca obiekt **VirtualDisk** , jeśli określono parametr *nazwa_woluminu* .</span><span class="sxs-lookup"><span data-stu-id="9ddaa-149">This cmdlet returns a **VirtualDisk** object if you specify the *VolumeName* parameter.</span></span>
<span data-ttu-id="9ddaa-150">Jeśli określisz *VolumeContainer* , to polecenie cmdlet zwróci obiekt **IList \<VirtualDisk\>** .</span><span class="sxs-lookup"><span data-stu-id="9ddaa-150">If you specify the *VolumeContainer* , this cmdlet returns an **IList\<VirtualDisk\>** object.</span></span>

## <span data-ttu-id="9ddaa-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ddaa-151">NOTES</span></span>

## <span data-ttu-id="9ddaa-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ddaa-152">RELATED LINKS</span></span>

[<span data-ttu-id="9ddaa-153">Nowe — AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="9ddaa-153">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="9ddaa-154">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="9ddaa-154">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="9ddaa-155">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="9ddaa-155">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="9ddaa-156">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="9ddaa-156">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


