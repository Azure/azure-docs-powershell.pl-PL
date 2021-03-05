---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: f26e1bd19b9856df7bf68de6c8afddefb3ee64a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988485"
---
# <span data-ttu-id="cbf0e-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="cbf0e-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="cbf0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbf0e-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf0e-103">Pobiera obsługiwane typy optymalizacji profilu SIECI CDN.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="cbf0e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cbf0e-104">SYNTAX</span></span>

### <span data-ttu-id="cbf0e-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="cbf0e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbf0e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbf0e-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbf0e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cbf0e-107">DESCRIPTION</span></span>
<span data-ttu-id="cbf0e-108">Polecenie **cmdlet Get-AzCdnProfileSupportedOptimizationType** pobiera obsługiwane typy optymalizacji dla bieżącego profilu.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="cbf0e-109">Użytkownik może utworzyć punkt końcowy o typie optymalizacji na liście wartości.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="cbf0e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cbf0e-110">EXAMPLES</span></span>

### <span data-ttu-id="cbf0e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cbf0e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="cbf0e-112">Uzyskaj obsługiwane typy optymalizacji profilu sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="cbf0e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbf0e-113">PARAMETERS</span></span>

### <span data-ttu-id="cbf0e-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="cbf0e-114">-CdnProfile</span></span>
<span data-ttu-id="cbf0e-115">Obiekt profilu sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-115">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf0e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf0e-116">-DefaultProfile</span></span>
<span data-ttu-id="cbf0e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbf0e-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="cbf0e-118">-ProfileName</span></span>
<span data-ttu-id="cbf0e-119">Nazwa profilu.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-119">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf0e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbf0e-120">-ResourceGroupName</span></span>
<span data-ttu-id="cbf0e-121">Grupa zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-121">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf0e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf0e-122">CommonParameters</span></span>
<span data-ttu-id="cbf0e-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf0e-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbf0e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf0e-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbf0e-125">INPUTS</span></span>

### <span data-ttu-id="cbf0e-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="cbf0e-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="cbf0e-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbf0e-127">OUTPUTS</span></span>

### <span data-ttu-id="cbf0e-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="cbf0e-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="cbf0e-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cbf0e-129">NOTES</span></span>

## <span data-ttu-id="cbf0e-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbf0e-130">RELATED LINKS</span></span>
