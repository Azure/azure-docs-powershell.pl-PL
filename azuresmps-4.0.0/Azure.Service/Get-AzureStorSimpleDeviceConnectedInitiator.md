---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 9436E1AB-870F-4717-ABE0-55A90C07F7E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 555ce014bbbf7174b3f7142cf7e2f217317eadc6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055257"
---
# <span data-ttu-id="bd069-101">Get-AzureStorSimpleDeviceConnectedInitiator</span><span class="sxs-lookup"><span data-stu-id="bd069-101">Get-AzureStorSimpleDeviceConnectedInitiator</span></span>

## <span data-ttu-id="bd069-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd069-102">SYNOPSIS</span></span>
<span data-ttu-id="bd069-103">Pobiera połączenia iSCSI dostępne dla urządzenia StorSimple.</span><span class="sxs-lookup"><span data-stu-id="bd069-103">Gets the iSCSI connections available for a StorSimple device.</span></span>

## <span data-ttu-id="bd069-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd069-104">SYNTAX</span></span>

### <span data-ttu-id="bd069-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="bd069-105">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bd069-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="bd069-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd069-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bd069-107">DESCRIPTION</span></span>
<span data-ttu-id="bd069-108">Polecenie cmdlet **Get-AzureStorSimpleDeviceConnectedInitiator** pobiera listę połączeń iSCSI dostępnych dla urządzenia StorSimple.</span><span class="sxs-lookup"><span data-stu-id="bd069-108">The **Get-AzureStorSimpleDeviceConnectedInitiator** cmdlet gets a list of the iSCSI connections available for a StorSimple device.</span></span>
<span data-ttu-id="bd069-109">Obiekty połączeń iSCSI, które ten aplet cmdlet zwróci, zawierają następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="bd069-109">The iSCSI connection objects that this cmdlet returns contain the following properties:</span></span>

- <span data-ttu-id="bd069-110">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="bd069-110">**AcrInstanceId**</span></span>
- <span data-ttu-id="bd069-111">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="bd069-111">**AcrName**</span></span>
- <span data-ttu-id="bd069-112">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="bd069-112">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="bd069-113">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="bd069-113">**InitiatorAddress**</span></span>
- <span data-ttu-id="bd069-114">**Połączeń**</span><span class="sxs-lookup"><span data-stu-id="bd069-114">**Interfaces**</span></span>
- <span data-ttu-id="bd069-115">**IQN**</span><span class="sxs-lookup"><span data-stu-id="bd069-115">**Iqn**</span></span>
- <span data-ttu-id="bd069-116">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="bd069-116">**IscsiConnectionId**</span></span>

<span data-ttu-id="bd069-117">Ten aplet polecenia pobiera obiekt Connection tylko wtedy, gdy na urządzeniu są włączone połączenia iSCSI.</span><span class="sxs-lookup"><span data-stu-id="bd069-117">This cmdlet gets connection object only if iSCSI connections are turned on for the device.</span></span>
<span data-ttu-id="bd069-118">Połączenia są domyślnie wyłączone.</span><span class="sxs-lookup"><span data-stu-id="bd069-118">By default, connections are turned off.</span></span>

## <span data-ttu-id="bd069-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd069-119">EXAMPLES</span></span>

### <span data-ttu-id="bd069-120">Przykład 1: uzyskiwanie wszystkich połączeń dla urządzenia</span><span class="sxs-lookup"><span data-stu-id="bd069-120">Example 1: Get all connections for a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: bec615b9-79ab-4671-88b0-287adeb6bf68_PS
VERBOSE: ClientRequestId: ef976c58-2660-41c8-aa15-c84e70c9d01c_PS
VERBOSE: ClientRequestId: 9b306b96-8e76-47ed-beda-d3bd2fb2bb82_PS
VERBOSE: ClientRequestId: 0f4fc743-0b60-45da-a45a-27f4b0f32bd2_PS

AcrInstanceId      : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
AcrName            : Contoso63-AppVm
AllowedVolumeNames : {Policyvolume1_Default}
InitiatorAddress   : 
Interfaces         : {Data0}
Iqn                : iqn10
IscsiConnectionId  : cfc144cb-00f1-44b1-9655-80b431f2161b

VERBOSE: 1 Iscsi Connection found!
```

<span data-ttu-id="bd069-121">To polecenie pobiera wszystkie połączenia iSCSI dotyczące urządzenia o nazwie Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="bd069-121">This command gets all iSCSI connections for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="bd069-122">To polecenie zwraca połączenia tylko wtedy, gdy dla urządzenia są włączone połączenia.</span><span class="sxs-lookup"><span data-stu-id="bd069-122">This command returns connections only if connections are turned on for the device.</span></span>

## <span data-ttu-id="bd069-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd069-123">PARAMETERS</span></span>

### <span data-ttu-id="bd069-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="bd069-124">-DeviceId</span></span>
<span data-ttu-id="bd069-125">Określa identyfikator wystąpienia urządzenia StorSimple, z którego mają być odbierane inicjatory iSCSI.</span><span class="sxs-lookup"><span data-stu-id="bd069-125">Specifies the instance ID of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd069-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="bd069-126">-DeviceName</span></span>
<span data-ttu-id="bd069-127">Określa nazwę urządzenia StorSimple, z którego mają być odbierane inicjatory iSCSI.</span><span class="sxs-lookup"><span data-stu-id="bd069-127">Specifies the name of the StorSimple device from which to get iSCSI initiators.</span></span>

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

### <span data-ttu-id="bd069-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="bd069-128">-Profile</span></span>
<span data-ttu-id="bd069-129">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bd069-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="bd069-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd069-130">CommonParameters</span></span>
<span data-ttu-id="bd069-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd069-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd069-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd069-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd069-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd069-133">INPUTS</span></span>

### <span data-ttu-id="bd069-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bd069-134">None</span></span>

## <span data-ttu-id="bd069-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd069-135">OUTPUTS</span></span>

### <span data-ttu-id="bd069-136">Lista\<IscsiConnection\></span><span class="sxs-lookup"><span data-stu-id="bd069-136">List\<IscsiConnection\></span></span>
<span data-ttu-id="bd069-137">To polecenie cmdlet zwraca obiekt połączenia iSCSI zawierający następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="bd069-137">This cmdlet returns an iSCSI connection object that contains the following properties:</span></span> 

- <span data-ttu-id="bd069-138">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="bd069-138">**AcrInstanceId**</span></span>
- <span data-ttu-id="bd069-139">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="bd069-139">**AcrName**</span></span>
- <span data-ttu-id="bd069-140">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="bd069-140">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="bd069-141">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="bd069-141">**InitiatorAddress**</span></span>
- <span data-ttu-id="bd069-142">**Połączeń**</span><span class="sxs-lookup"><span data-stu-id="bd069-142">**Interfaces**</span></span>
- <span data-ttu-id="bd069-143">**IQN**</span><span class="sxs-lookup"><span data-stu-id="bd069-143">**Iqn**</span></span>
- <span data-ttu-id="bd069-144">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="bd069-144">**IscsiConnectionId**</span></span>

## <span data-ttu-id="bd069-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd069-145">NOTES</span></span>

## <span data-ttu-id="bd069-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd069-146">RELATED LINKS</span></span>

[<span data-ttu-id="bd069-147">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="bd069-147">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


