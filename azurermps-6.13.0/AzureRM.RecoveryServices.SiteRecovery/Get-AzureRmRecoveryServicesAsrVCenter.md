---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 8db3dd9579e528110ec41f59b1c29da5d132d18d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552079"
---
# <span data-ttu-id="565e9-101">Get-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="565e9-101">Get-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="565e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="565e9-102">SYNOPSIS</span></span>
<span data-ttu-id="565e9-103">Pobiera szczegóły serwerów vCenter zarejestrowanych do odnajdowania na serwerze konfiguracji określonym przez sieć szkieletową ASR.</span><span class="sxs-lookup"><span data-stu-id="565e9-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="565e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="565e9-104">SYNTAX</span></span>

### <span data-ttu-id="565e9-105">ByFabricObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="565e9-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="565e9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="565e9-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="565e9-107">ByName</span><span class="sxs-lookup"><span data-stu-id="565e9-107">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="565e9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="565e9-108">DESCRIPTION</span></span>
<span data-ttu-id="565e9-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrvCenter** pobiera szczegółowe informacje o serwerach vCenter zarejestrowanych do odnajdowania na serwerze konfiguracji określonym przez sieć szkieletową ASR.</span><span class="sxs-lookup"><span data-stu-id="565e9-109">The **Get-AzureRmRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="565e9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="565e9-110">EXAMPLES</span></span>

### <span data-ttu-id="565e9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="565e9-111">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

FriendlyName          : inmtest81
Server                : 10.150.209.27
Port                  : 443
Name                  : inmtest81
ID                    : /Subscriptions/xxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxx/replicationvCenters/inmtest81
FabricArmResourceName : d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9
ProcessServerId       : 526C9B6C-4039-D841-97A92FB0BD153B53
AccountId             : 2
DiscoveryStatus       : Pending
LastHeartbeat         :
```

<span data-ttu-id="565e9-112">Pobierz witrynę Azure Site Recovery vCenter przez nazwę sieci szkieletowej i nazwę programu vCenter.</span><span class="sxs-lookup"><span data-stu-id="565e9-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="565e9-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="565e9-113">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="565e9-114">Pobierz listę vCenter do odzyskiwania witryny platformy Azure według nazwy sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="565e9-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="565e9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="565e9-115">PARAMETERS</span></span>

### <span data-ttu-id="565e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="565e9-116">-DefaultProfile</span></span>
<span data-ttu-id="565e9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="565e9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="565e9-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="565e9-118">-Fabric</span></span>
<span data-ttu-id="565e9-119">Obiekt sieci szkieletowej ASR reprezentujący serwer konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="565e9-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="565e9-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="565e9-120">-Name</span></span>
<span data-ttu-id="565e9-121">Nazwa serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="565e9-121">Name of the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="565e9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="565e9-122">-ResourceId</span></span>
<span data-ttu-id="565e9-123">Określa identyfikator zasobu vCenter.</span><span class="sxs-lookup"><span data-stu-id="565e9-123">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="565e9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="565e9-124">CommonParameters</span></span>
<span data-ttu-id="565e9-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="565e9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="565e9-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="565e9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="565e9-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="565e9-127">INPUTS</span></span>

### <span data-ttu-id="565e9-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="565e9-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="565e9-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="565e9-129">OUTPUTS</span></span>

### <span data-ttu-id="565e9-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="565e9-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="565e9-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="565e9-131">NOTES</span></span>

## <span data-ttu-id="565e9-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="565e9-132">RELATED LINKS</span></span>
