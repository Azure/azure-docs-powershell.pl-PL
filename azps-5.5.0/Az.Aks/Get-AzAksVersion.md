---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199866"
---
# <span data-ttu-id="cbb2a-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="cbb2a-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="cbb2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbb2a-102">SYNOPSIS</span></span>
<span data-ttu-id="cbb2a-103">Lista dostępnych wersji do tworzenia zarządzanego klastra Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="cbb2a-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="cbb2a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cbb2a-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbb2a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cbb2a-105">DESCRIPTION</span></span>
<span data-ttu-id="cbb2a-106">Lista dostępnych wersji do tworzenia zarządzanego klastra Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="cbb2a-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="cbb2a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cbb2a-107">EXAMPLES</span></span>

### <span data-ttu-id="cbb2a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cbb2a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="cbb2a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbb2a-109">PARAMETERS</span></span>

### <span data-ttu-id="cbb2a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbb2a-110">-DefaultProfile</span></span>
<span data-ttu-id="cbb2a-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cbb2a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbb2a-112">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cbb2a-112">-Location</span></span>
<span data-ttu-id="cbb2a-113">Lokalizacja na platformie Azure dla klastrów.</span><span class="sxs-lookup"><span data-stu-id="cbb2a-113">Azure location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbb2a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbb2a-114">CommonParameters</span></span>
<span data-ttu-id="cbb2a-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbb2a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbb2a-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbb2a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbb2a-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbb2a-117">INPUTS</span></span>

### <span data-ttu-id="cbb2a-118">Brak</span><span class="sxs-lookup"><span data-stu-id="cbb2a-118">None</span></span>

## <span data-ttu-id="cbb2a-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cbb2a-119">OUTPUTS</span></span>

### <span data-ttu-id="cbb2a-120">Microsoft.Azure.Commands.Aks.Models.PSO przewrotnietratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="cbb2a-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="cbb2a-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cbb2a-121">NOTES</span></span>

## <span data-ttu-id="cbb2a-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbb2a-122">RELATED LINKS</span></span>
