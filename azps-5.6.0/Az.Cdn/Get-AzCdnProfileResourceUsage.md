---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 1a4e3f08653f6c7bda799b55618caff4e77fe7bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004586"
---
# <span data-ttu-id="fc7d2-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="fc7d2-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="fc7d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc7d2-102">SYNOPSIS</span></span>
<span data-ttu-id="fc7d2-103">Pobiera użycie zasobu profilu sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="fc7d2-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="fc7d2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fc7d2-104">SYNTAX</span></span>

### <span data-ttu-id="fc7d2-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="fc7d2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc7d2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc7d2-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc7d2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fc7d2-107">DESCRIPTION</span></span>
<span data-ttu-id="fc7d2-108">{{Wypełnij opis}}</span><span class="sxs-lookup"><span data-stu-id="fc7d2-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="fc7d2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fc7d2-109">EXAMPLES</span></span>

### <span data-ttu-id="fc7d2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fc7d2-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="fc7d2-111">{{ Dodaj przykładowy opis tutaj }}</span><span class="sxs-lookup"><span data-stu-id="fc7d2-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="fc7d2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc7d2-112">PARAMETERS</span></span>

### <span data-ttu-id="fc7d2-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="fc7d2-113">-CdnProfile</span></span>
<span data-ttu-id="fc7d2-114">Obiekt profilu sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fc7d2-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="fc7d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc7d2-115">-DefaultProfile</span></span>
<span data-ttu-id="fc7d2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="fc7d2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc7d2-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fc7d2-117">-ProfileName</span></span>
<span data-ttu-id="fc7d2-118">Nazwa profilu.</span><span class="sxs-lookup"><span data-stu-id="fc7d2-118">The name of the profile.</span></span>

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

### <span data-ttu-id="fc7d2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc7d2-119">-ResourceGroupName</span></span>
<span data-ttu-id="fc7d2-120">Grupa zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="fc7d2-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="fc7d2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc7d2-121">CommonParameters</span></span>
<span data-ttu-id="fc7d2-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc7d2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc7d2-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc7d2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc7d2-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc7d2-124">INPUTS</span></span>

### <span data-ttu-id="fc7d2-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="fc7d2-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="fc7d2-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc7d2-126">OUTPUTS</span></span>

### <span data-ttu-id="fc7d2-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="fc7d2-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="fc7d2-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fc7d2-128">NOTES</span></span>

## <span data-ttu-id="fc7d2-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc7d2-129">RELATED LINKS</span></span>
