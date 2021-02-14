---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: db6520ae16d114fdcad85daf3e0742589fa0fbbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195178"
---
# <span data-ttu-id="ca100-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="ca100-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="ca100-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca100-102">SYNOPSIS</span></span>
<span data-ttu-id="ca100-103">Pobiera obsługiwane typy optymalizacji profilu CDN.</span><span class="sxs-lookup"><span data-stu-id="ca100-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="ca100-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ca100-104">SYNTAX</span></span>

### <span data-ttu-id="ca100-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ca100-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca100-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca100-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca100-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ca100-107">DESCRIPTION</span></span>
<span data-ttu-id="ca100-108">Polecenie **cmdlet Get-AzCdnProfileSupportedOptimizationType** pobiera obsługiwane typy optymalizacji dla bieżącego profilu.</span><span class="sxs-lookup"><span data-stu-id="ca100-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="ca100-109">Użytkownik może utworzyć punkt końcowy z typem optymalizacji na liście wartości.</span><span class="sxs-lookup"><span data-stu-id="ca100-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="ca100-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ca100-110">EXAMPLES</span></span>

### <span data-ttu-id="ca100-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ca100-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="ca100-112">Uzyskaj obsługiwane typy optymalizacji profilu sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="ca100-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="ca100-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca100-113">PARAMETERS</span></span>

### <span data-ttu-id="ca100-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="ca100-114">-CdnProfile</span></span>
<span data-ttu-id="ca100-115">Obiekt profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="ca100-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="ca100-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca100-116">-DefaultProfile</span></span>
<span data-ttu-id="ca100-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca100-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca100-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ca100-118">-ProfileName</span></span>
<span data-ttu-id="ca100-119">Nazwa profilu.</span><span class="sxs-lookup"><span data-stu-id="ca100-119">The name of the profile.</span></span>

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

### <span data-ttu-id="ca100-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca100-120">-ResourceGroupName</span></span>
<span data-ttu-id="ca100-121">Grupa zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="ca100-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="ca100-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca100-122">CommonParameters</span></span>
<span data-ttu-id="ca100-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca100-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca100-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca100-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca100-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca100-125">INPUTS</span></span>

### <span data-ttu-id="ca100-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="ca100-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="ca100-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca100-127">OUTPUTS</span></span>

### <span data-ttu-id="ca100-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="ca100-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="ca100-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ca100-129">NOTES</span></span>

## <span data-ttu-id="ca100-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca100-130">RELATED LINKS</span></span>
