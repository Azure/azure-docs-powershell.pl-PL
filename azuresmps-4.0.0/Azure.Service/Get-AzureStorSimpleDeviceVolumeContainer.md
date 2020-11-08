---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7EF20FC0-3E2A-4AFC-AC02-9B11C8952DB8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22263501f2a79a36c1ace1915ee6898c4833b52b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054529"
---
# <span data-ttu-id="317bd-101">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="317bd-101">Get-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="317bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="317bd-102">SYNOPSIS</span></span>
<span data-ttu-id="317bd-103">Pobiera kontenery wolumenu na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="317bd-103">Gets volume containers on a device.</span></span>

## <span data-ttu-id="317bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="317bd-104">SYNTAX</span></span>

```
Get-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> [-VolumeContainerName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="317bd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="317bd-105">DESCRIPTION</span></span>
<span data-ttu-id="317bd-106">Polecenie cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** pobiera listę kontenerów woluminów na urządzeniu lub kontenera woluminów o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="317bd-106">The **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet gets a list of volume containers on a device, or volume container that has the specified name.</span></span>
<span data-ttu-id="317bd-107">Zwrócony obiekt zawiera następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="317bd-107">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="317bd-108">**BandwidthRate**</span><span class="sxs-lookup"><span data-stu-id="317bd-108">**BandwidthRate**</span></span>
- <span data-ttu-id="317bd-109">**EncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="317bd-109">**EncryptionKey**</span></span>
- <span data-ttu-id="317bd-110">**Obiektu**</span><span class="sxs-lookup"><span data-stu-id="317bd-110">**InstanceId**</span></span>
- <span data-ttu-id="317bd-111">**Wartość domyślna**</span><span class="sxs-lookup"><span data-stu-id="317bd-111">**IsDefault**</span></span>
- <span data-ttu-id="317bd-112">**IsEncryptionEnabled**</span><span class="sxs-lookup"><span data-stu-id="317bd-112">**IsEncryptionEnabled**</span></span>
- <span data-ttu-id="317bd-113">**Nazwę**</span><span class="sxs-lookup"><span data-stu-id="317bd-113">**Name**</span></span>
- <span data-ttu-id="317bd-114">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="317bd-114">**OperationInProgress**</span></span>
- <span data-ttu-id="317bd-115">**Należą**</span><span class="sxs-lookup"><span data-stu-id="317bd-115">**Owned**</span></span>
- <span data-ttu-id="317bd-116">**PrimaryStorageAccountCredential**</span><span class="sxs-lookup"><span data-stu-id="317bd-116">**PrimaryStorageAccountCredential**</span></span>
- <span data-ttu-id="317bd-117">**SecretsEncryptionThumbprint**</span><span class="sxs-lookup"><span data-stu-id="317bd-117">**SecretsEncryptionThumbprint**</span></span>
- <span data-ttu-id="317bd-118">**VolumeCount**</span><span class="sxs-lookup"><span data-stu-id="317bd-118">**VolumeCount**</span></span>

## <span data-ttu-id="317bd-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="317bd-119">EXAMPLES</span></span>

### <span data-ttu-id="317bd-120">Przykład 1: uzyskiwanie wszystkich kontenerów na urządzeniu</span><span class="sxs-lookup"><span data-stu-id="317bd-120">Example 1: Get all the containers on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "8600-Bravo 001"
InstanceId                           Name                                             IsEncryptionEnabled  Owned BandwidthRate                                    PrimaryStorageAccountCredential                 VolumeCount                                    
----------                           ----                                             -------------------  ----- -------------                                    -------------------------------                 -----------                                    
127135b6-92de-4f53-850d-70e1f9a38cbe Test_Container                                   False                True  0                                                Test_Account                                    6
```

<span data-ttu-id="317bd-121">To polecenie otrzymuje listę kontenerów woluminów na urządzeniu o nazwie 8600-Bravo 001.</span><span class="sxs-lookup"><span data-stu-id="317bd-121">This command gets a list of the volume containers on the device named 8600-Bravo 001.</span></span>

### <span data-ttu-id="317bd-122">Przykład 2: uzyskiwanie kontenera przy użyciu jego nazwy</span><span class="sxs-lookup"><span data-stu-id="317bd-122">Example 2: Get a container by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08"
VERBOSE: ClientRequestId: 8027c66a-869b-4ea3-97a2-e17d98ec751c_PS
VERBOSE: ClientRequestId: 344f9be5-0887-4d37-98ef-e45c557774f1_PS
VERBOSE: ClientRequestId: 14919be5-d6f5-4f81-b7f1-d7fafff2238c_PS


BandwidthRate                   : 256
EncryptionKey                   : 
InstanceId                      : 04ea9aad-7a56-4a50-b195-86061b0a810a
IsDefault                       : False
IsEncryptionEnabled             : False
Name                            : Container03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 5

VERBOSE: Volume container with name: Container03 is found.
```

<span data-ttu-id="317bd-123">To polecenie pobiera kontener woluminu o nazwie Container08 na urządzeniu o nazwie Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="317bd-123">This command gets the volume container named Container08 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="317bd-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="317bd-124">PARAMETERS</span></span>

### <span data-ttu-id="317bd-125">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="317bd-125">-DeviceName</span></span>
<span data-ttu-id="317bd-126">Określa nazwę urządzenia StorSimple.</span><span class="sxs-lookup"><span data-stu-id="317bd-126">Specifies the name of a StorSimple device.</span></span>
<span data-ttu-id="317bd-127">To polecenie cmdlet umożliwia pobieranie kontenerów woluminów z urządzenia, które ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="317bd-127">This cmdlet gets volume containers from the device that this parameter specifies.</span></span>

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

### <span data-ttu-id="317bd-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="317bd-128">-Profile</span></span>
<span data-ttu-id="317bd-129">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="317bd-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="317bd-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="317bd-130">-VolumeContainerName</span></span>
<span data-ttu-id="317bd-131">Określa nazwę kontenera woluminu, który ma zostać przyjdzie.</span><span class="sxs-lookup"><span data-stu-id="317bd-131">Specifies the name of the volume container to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317bd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="317bd-132">CommonParameters</span></span>
<span data-ttu-id="317bd-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="317bd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="317bd-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="317bd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="317bd-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="317bd-135">INPUTS</span></span>

### <span data-ttu-id="317bd-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="317bd-136">None</span></span>

## <span data-ttu-id="317bd-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="317bd-137">OUTPUTS</span></span>

### <span data-ttu-id="317bd-138">Kontenery Data, IList\<DataContainer\></span><span class="sxs-lookup"><span data-stu-id="317bd-138">DataContainer, IList\<DataContainer\></span></span>
<span data-ttu-id="317bd-139">To polecenie cmdlet zwraca obiekt **kontenera typu datakontener** , jeśli określisz parametr *VolumeContainerName* .</span><span class="sxs-lookup"><span data-stu-id="317bd-139">This cmdlet returns a **DataContainer** object, if you specify the *VolumeContainerName* parameter.</span></span>
<span data-ttu-id="317bd-140">Jeśli nie określisz tego parametru, to polecenie cmdlet zwróci obiekt **IList \<DataContainer\>** .</span><span class="sxs-lookup"><span data-stu-id="317bd-140">If you do not specify that parameter, this cmdlet returns an **IList\<DataContainer\>** object.</span></span>

## <span data-ttu-id="317bd-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="317bd-141">NOTES</span></span>

## <span data-ttu-id="317bd-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="317bd-142">RELATED LINKS</span></span>

[<span data-ttu-id="317bd-143">Nowe — AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="317bd-143">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="317bd-144">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="317bd-144">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)


