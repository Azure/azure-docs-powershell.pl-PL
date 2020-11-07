---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 48437526fdaf8ae226ff7693b417fcff7ffc93d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872716"
---
# <span data-ttu-id="df46d-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="df46d-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="df46d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df46d-102">SYNOPSIS</span></span>
<span data-ttu-id="df46d-103">Pobiera szczegóły serwerów vCenter zarejestrowanych do odnajdowania na serwerze konfiguracji określonym przez sieć szkieletową ASR.</span><span class="sxs-lookup"><span data-stu-id="df46d-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="df46d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df46d-104">SYNTAX</span></span>

### <span data-ttu-id="df46d-105">ByFabricObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="df46d-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df46d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="df46d-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df46d-107">ByName</span><span class="sxs-lookup"><span data-stu-id="df46d-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df46d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="df46d-108">DESCRIPTION</span></span>
<span data-ttu-id="df46d-109">Polecenie cmdlet **Get-AzRecoveryServicesAsrvCenter** pobiera szczegółowe informacje o serwerach vCenter zarejestrowanych do odnajdowania na serwerze konfiguracji określonym przez sieć szkieletową ASR.</span><span class="sxs-lookup"><span data-stu-id="df46d-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="df46d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df46d-110">EXAMPLES</span></span>

### <span data-ttu-id="df46d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="df46d-111">Example 1</span></span>
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

<span data-ttu-id="df46d-112">Pobierz witrynę Azure Site Recovery vCenter przez nazwę sieci szkieletowej i nazwę programu vCenter.</span><span class="sxs-lookup"><span data-stu-id="df46d-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="df46d-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="df46d-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="df46d-114">Pobierz listę vCenter do odzyskiwania witryny platformy Azure według nazwy sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="df46d-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="df46d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df46d-115">PARAMETERS</span></span>

### <span data-ttu-id="df46d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df46d-116">-DefaultProfile</span></span>
<span data-ttu-id="df46d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df46d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df46d-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="df46d-118">-Fabric</span></span>
<span data-ttu-id="df46d-119">Obiekt sieci szkieletowej ASR reprezentujący serwer konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="df46d-119">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="df46d-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df46d-120">-Name</span></span>
<span data-ttu-id="df46d-121">Nazwa serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="df46d-121">Name of the vCenter server.</span></span>

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

### <span data-ttu-id="df46d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df46d-122">-ResourceId</span></span>
<span data-ttu-id="df46d-123">Określa identyfikator zasobu vCenter.</span><span class="sxs-lookup"><span data-stu-id="df46d-123">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="df46d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df46d-124">CommonParameters</span></span>
<span data-ttu-id="df46d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df46d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df46d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df46d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df46d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df46d-127">INPUTS</span></span>

### <span data-ttu-id="df46d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="df46d-128">System.String</span></span>

### <span data-ttu-id="df46d-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="df46d-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="df46d-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df46d-130">OUTPUTS</span></span>

### <span data-ttu-id="df46d-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="df46d-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="df46d-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df46d-132">NOTES</span></span>

## <span data-ttu-id="df46d-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df46d-133">RELATED LINKS</span></span>
