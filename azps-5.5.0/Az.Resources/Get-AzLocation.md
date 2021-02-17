---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: f14da4760f70c8e4ba95136b81a884f830f4f44a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178827"
---
# <span data-ttu-id="e1bba-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="e1bba-101">Get-AzLocation</span></span>

## <span data-ttu-id="e1bba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1bba-102">SYNOPSIS</span></span>
<span data-ttu-id="e1bba-103">Pobiera wszystkie lokalizacje i obsługiwanych dostawców zasobów dla każdej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="e1bba-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="e1bba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e1bba-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1bba-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e1bba-105">DESCRIPTION</span></span>
<span data-ttu-id="e1bba-106">Polecenie **cmdlet Get-AzLocation** pobiera wszystkie lokalizacje i obsługiwanych dostawców zasobów dla każdej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="e1bba-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="e1bba-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e1bba-107">EXAMPLES</span></span>

### <span data-ttu-id="e1bba-108">Przykład 1. Uzyskiwanie wszystkich lokalizacji i obsługiwanych dostawców zasobów</span><span class="sxs-lookup"><span data-stu-id="e1bba-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="e1bba-109">To polecenie pobiera wszystkie lokalizacje i obsługiwanych dostawców zasobów dla każdej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="e1bba-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="e1bba-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1bba-110">PARAMETERS</span></span>

### <span data-ttu-id="e1bba-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e1bba-111">-ApiVersion</span></span>
<span data-ttu-id="e1bba-112">Określa wersję interfejsu API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="e1bba-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e1bba-113">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="e1bba-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e1bba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1bba-114">-DefaultProfile</span></span>
<span data-ttu-id="e1bba-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e1bba-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1bba-116">— Przed</span><span class="sxs-lookup"><span data-stu-id="e1bba-116">-Pre</span></span>
<span data-ttu-id="e1bba-117">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="e1bba-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e1bba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bba-118">CommonParameters</span></span>
<span data-ttu-id="e1bba-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1bba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bba-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1bba-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bba-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1bba-121">INPUTS</span></span>

### <span data-ttu-id="e1bba-122">Brak</span><span class="sxs-lookup"><span data-stu-id="e1bba-122">None</span></span>

## <span data-ttu-id="e1bba-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e1bba-123">OUTPUTS</span></span>

### <span data-ttu-id="e1bba-124">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="e1bba-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="e1bba-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e1bba-125">NOTES</span></span>

## <span data-ttu-id="e1bba-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1bba-126">RELATED LINKS</span></span>
