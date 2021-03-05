---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: 22b9d3322baa146bcd916024b15eea96b824f2eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003130"
---
# <span data-ttu-id="28a26-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="28a26-101">Get-AzLocation</span></span>

## <span data-ttu-id="28a26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28a26-102">SYNOPSIS</span></span>
<span data-ttu-id="28a26-103">Pobiera wszystkie lokalizacje i obsługiwanych dostawców zasobów dla każdej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="28a26-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="28a26-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="28a26-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28a26-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="28a26-105">DESCRIPTION</span></span>
<span data-ttu-id="28a26-106">Polecenie **cmdlet Get-AzLocation** pobiera wszystkie lokalizacje i obsługiwanych dostawców zasobów dla każdej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="28a26-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="28a26-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="28a26-107">EXAMPLES</span></span>

### <span data-ttu-id="28a26-108">Przykład 1. Uzyskiwanie wszystkich lokalizacji i obsługiwanych dostawców zasobów</span><span class="sxs-lookup"><span data-stu-id="28a26-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="28a26-109">To polecenie pobiera wszystkie lokalizacje i obsługiwanych dostawców zasobów dla każdej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="28a26-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="28a26-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28a26-110">PARAMETERS</span></span>

### <span data-ttu-id="28a26-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="28a26-111">-ApiVersion</span></span>
<span data-ttu-id="28a26-112">Określa wersję interfejsu API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="28a26-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="28a26-113">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="28a26-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a26-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a26-114">-DefaultProfile</span></span>
<span data-ttu-id="28a26-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="28a26-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28a26-116">— Przed</span><span class="sxs-lookup"><span data-stu-id="28a26-116">-Pre</span></span>
<span data-ttu-id="28a26-117">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="28a26-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a26-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a26-118">CommonParameters</span></span>
<span data-ttu-id="28a26-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28a26-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a26-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28a26-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a26-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28a26-121">INPUTS</span></span>

### <span data-ttu-id="28a26-122">Brak</span><span class="sxs-lookup"><span data-stu-id="28a26-122">None</span></span>

## <span data-ttu-id="28a26-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28a26-123">OUTPUTS</span></span>

### <span data-ttu-id="28a26-124">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="28a26-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="28a26-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="28a26-125">NOTES</span></span>

## <span data-ttu-id="28a26-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28a26-126">RELATED LINKS</span></span>
