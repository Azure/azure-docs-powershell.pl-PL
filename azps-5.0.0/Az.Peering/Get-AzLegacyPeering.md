---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: e7b5ef8ef41c66cc3c19fd5ebdcfd53ddcc6f3a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309060"
---
# <span data-ttu-id="b463c-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="b463c-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="b463c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b463c-102">SYNOPSIS</span></span>
<span data-ttu-id="b463c-103">Służy do konwertowania starszych zasobów równorzędnych na zasoby usługi Azure Resource Management (ARM).</span><span class="sxs-lookup"><span data-stu-id="b463c-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="b463c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b463c-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b463c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b463c-105">DESCRIPTION</span></span>
<span data-ttu-id="b463c-106">To polecenie służy do wyświetlania starszych zasobów komunikacji równorzędnej, które zostaną przekonwertowane na zasoby ARM (Azure Resource Management).</span><span class="sxs-lookup"><span data-stu-id="b463c-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="b463c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b463c-107">EXAMPLES</span></span>

### <span data-ttu-id="b463c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b463c-108">Example 1</span></span>
```powershell
PS C:> Get-AzLegacyPeering -PeeringLocation "Seattle" -Kind Direct

Name                       :
Sku                        : Basic_Direct_Free
Kind                       : Direct
PeeringLocation            : Seattle
UseForPeeringService       : False
PeerAsn.Id                 :
Connection                 : ------------------------
PeeringDBFacilityId        : 71
SessionPrefixIPv4          : 173.205.50.236/30
PeerSessionIPv4Address     : 173.205.50.237
MicrosoftIPv4Address       : 173.205.50.238
SessionStateV4             : Established
MaxPrefixesAdvertisedV4    : 20000
SessionPrefixIPv6          : 2001:668:0:3:ffff:0:adcd:32ec/126
PeerSessionIPv6Address     : 2001:668:0:3:ffff:0:adcd:32ed
MicrosoftIPv6Address       : 2001:668:0:3:ffff:0:adcd:32ee
SessionStateV6             : Established
MaxPrefixesAdvertisedV6    : 2000
ConnectionState            : Active
BandwidthInMbps            : 0
ProvisionedBandwidthInMbps : 20000
ProvisioningState          : Succeeded
```

<span data-ttu-id="b463c-109">Pobiera starszy sposób komunikacji równorzędnej w Seattle</span><span class="sxs-lookup"><span data-stu-id="b463c-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="b463c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b463c-110">PARAMETERS</span></span>

### <span data-ttu-id="b463c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b463c-111">-DefaultProfile</span></span>
<span data-ttu-id="b463c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b463c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b463c-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="b463c-113">-Kind</span></span>
<span data-ttu-id="b463c-114">Wyświetla wszystkie zasoby komunikacji równorzędnej według rodzaju.</span><span class="sxs-lookup"><span data-stu-id="b463c-114">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b463c-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="b463c-115">-PeeringLocation</span></span>
<span data-ttu-id="b463c-116">Wyświetla wszystkie zasoby komunikacji równorzędnej według rodzaju.</span><span class="sxs-lookup"><span data-stu-id="b463c-116">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b463c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b463c-117">CommonParameters</span></span>
<span data-ttu-id="b463c-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b463c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b463c-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b463c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b463c-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b463c-120">INPUTS</span></span>

### <span data-ttu-id="b463c-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b463c-121">None</span></span>

## <span data-ttu-id="b463c-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b463c-122">OUTPUTS</span></span>

### <span data-ttu-id="b463c-123">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeering</span><span class="sxs-lookup"><span data-stu-id="b463c-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="b463c-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b463c-124">NOTES</span></span>

## <span data-ttu-id="b463c-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b463c-125">RELATED LINKS</span></span>
