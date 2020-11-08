---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 49adcdefac7fe3f06cfd9678137dd58cff021f52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049861"
---
# <span data-ttu-id="b5e7c-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="b5e7c-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="b5e7c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e7c-103">Pobiera szczegóły serwerów vCenter zarejestrowanych do odnajdowania na serwerze konfiguracji określonym przez sieć szkieletową ASR.</span><span class="sxs-lookup"><span data-stu-id="b5e7c-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="b5e7c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5e7c-104">SYNTAX</span></span>

### <span data-ttu-id="b5e7c-105">ByFabricObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b5e7c-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5e7c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b5e7c-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5e7c-107">ByName</span><span class="sxs-lookup"><span data-stu-id="b5e7c-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5e7c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b5e7c-108">DESCRIPTION</span></span>
<span data-ttu-id="b5e7c-109">Polecenie cmdlet **Get-AzRecoveryServicesAsrvCenter** pobiera szczegółowe informacje o serwerach vCenter zarejestrowanych do odnajdowania na serwerze konfiguracji określonym przez sieć szkieletową ASR.</span><span class="sxs-lookup"><span data-stu-id="b5e7c-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="b5e7c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5e7c-110">EXAMPLES</span></span>

### <span data-ttu-id="b5e7c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b5e7c-111">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

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

<span data-ttu-id="b5e7c-112">Pobierz witrynę Azure Site Recovery vCenter przez nazwę sieci szkieletowej i nazwę programu vCenter.</span><span class="sxs-lookup"><span data-stu-id="b5e7c-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="b5e7c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b5e7c-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="b5e7c-114">Pobierz listę vCenter do odzyskiwania witryny platformy Azure według nazwy sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="b5e7c-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="b5e7c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5e7c-115">PARAMETERS</span></span>

### <span data-ttu-id="b5e7c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5e7c-116">-DefaultProfile</span></span>
<span data-ttu-id="b5e7c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5e7c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e7c-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="b5e7c-118">-Fabric</span></span>
<span data-ttu-id="b5e7c-119">Obiekt sieci szkieletowej ASR reprezentujący serwer konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="b5e7c-119">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="b5e7c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b5e7c-120">-Name</span></span>
<span data-ttu-id="b5e7c-121">Nazwa serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="b5e7c-121">Name of the vCenter server.</span></span>

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

### <span data-ttu-id="b5e7c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5e7c-122">-ResourceId</span></span>
<span data-ttu-id="b5e7c-123">Określa identyfikator zasobu vCenter.</span><span class="sxs-lookup"><span data-stu-id="b5e7c-123">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="b5e7c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e7c-124">CommonParameters</span></span>
<span data-ttu-id="b5e7c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5e7c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e7c-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5e7c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e7c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5e7c-127">INPUTS</span></span>

### <span data-ttu-id="b5e7c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b5e7c-128">System.String</span></span>

### <span data-ttu-id="b5e7c-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="b5e7c-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="b5e7c-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5e7c-130">OUTPUTS</span></span>

### <span data-ttu-id="b5e7c-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="b5e7c-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="b5e7c-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5e7c-132">NOTES</span></span>

## <span data-ttu-id="b5e7c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5e7c-133">RELATED LINKS</span></span>
