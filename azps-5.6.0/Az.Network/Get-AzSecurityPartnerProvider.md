---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 99498979df259723a192bd0e2fd74ef436ae0ee1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954042"
---
# <span data-ttu-id="18cb5-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="18cb5-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="18cb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="18cb5-103">Uzyskaj subskrypcję usługi Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="18cb5-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="18cb5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="18cb5-104">SYNTAX</span></span>

### <span data-ttu-id="18cb5-105">SecurityPartnerProviderNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="18cb5-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18cb5-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18cb5-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18cb5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="18cb5-107">DESCRIPTION</span></span>
<span data-ttu-id="18cb5-108">Polecenie **cmdlet Get-AzSecurityPartnerProvider** pobiera narzędzie Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="18cb5-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="18cb5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="18cb5-109">EXAMPLES</span></span>

### <span data-ttu-id="18cb5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="18cb5-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="18cb5-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="18cb5-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="18cb5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18cb5-112">PARAMETERS</span></span>

### <span data-ttu-id="18cb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18cb5-113">-DefaultProfile</span></span>
<span data-ttu-id="18cb5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="18cb5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18cb5-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="18cb5-115">-Name</span></span>
<span data-ttu-id="18cb5-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="18cb5-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18cb5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18cb5-117">-ResourceGroupName</span></span>
<span data-ttu-id="18cb5-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="18cb5-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18cb5-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18cb5-119">-ResourceId</span></span>
<span data-ttu-id="18cb5-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="18cb5-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18cb5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18cb5-121">CommonParameters</span></span>
<span data-ttu-id="18cb5-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18cb5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18cb5-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18cb5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18cb5-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18cb5-124">INPUTS</span></span>

### <span data-ttu-id="18cb5-125">System.String</span><span class="sxs-lookup"><span data-stu-id="18cb5-125">System.String</span></span>

## <span data-ttu-id="18cb5-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18cb5-126">OUTPUTS</span></span>

### <span data-ttu-id="18cb5-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="18cb5-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="18cb5-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="18cb5-128">NOTES</span></span>

## <span data-ttu-id="18cb5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18cb5-129">RELATED LINKS</span></span>
