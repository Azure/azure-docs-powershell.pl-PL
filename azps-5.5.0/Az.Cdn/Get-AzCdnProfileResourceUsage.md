---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 8395fc4d90eb4e6d38eda18753761a1bf2598479
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239129"
---
# <span data-ttu-id="c361a-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="c361a-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="c361a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c361a-102">SYNOPSIS</span></span>
<span data-ttu-id="c361a-103">Pobiera użycie zasobu profilu sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="c361a-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="c361a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c361a-104">SYNTAX</span></span>

### <span data-ttu-id="c361a-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c361a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c361a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c361a-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c361a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c361a-107">DESCRIPTION</span></span>
<span data-ttu-id="c361a-108">{{Wypełnij opis}}</span><span class="sxs-lookup"><span data-stu-id="c361a-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="c361a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c361a-109">EXAMPLES</span></span>

### <span data-ttu-id="c361a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c361a-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c361a-111">{{ Dodaj przykładowy opis tutaj }}</span><span class="sxs-lookup"><span data-stu-id="c361a-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="c361a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c361a-112">PARAMETERS</span></span>

### <span data-ttu-id="c361a-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="c361a-113">-CdnProfile</span></span>
<span data-ttu-id="c361a-114">Obiekt profilu sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c361a-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="c361a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c361a-115">-DefaultProfile</span></span>
<span data-ttu-id="c361a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c361a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c361a-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c361a-117">-ProfileName</span></span>
<span data-ttu-id="c361a-118">Nazwa profilu.</span><span class="sxs-lookup"><span data-stu-id="c361a-118">The name of the profile.</span></span>

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

### <span data-ttu-id="c361a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c361a-119">-ResourceGroupName</span></span>
<span data-ttu-id="c361a-120">Grupa zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="c361a-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="c361a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c361a-121">CommonParameters</span></span>
<span data-ttu-id="c361a-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c361a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c361a-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c361a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c361a-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c361a-124">INPUTS</span></span>

### <span data-ttu-id="c361a-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="c361a-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="c361a-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c361a-126">OUTPUTS</span></span>

### <span data-ttu-id="c361a-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="c361a-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="c361a-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c361a-128">NOTES</span></span>

## <span data-ttu-id="c361a-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c361a-129">RELATED LINKS</span></span>
