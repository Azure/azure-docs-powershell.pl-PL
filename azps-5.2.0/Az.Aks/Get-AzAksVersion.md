---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356512"
---
# <span data-ttu-id="7f472-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="7f472-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="7f472-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f472-102">SYNOPSIS</span></span>
<span data-ttu-id="7f472-103">Lista dostępnych wersji na potrzeby tworzenia zarządzanych klastrów Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="7f472-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="7f472-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f472-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f472-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7f472-105">DESCRIPTION</span></span>
<span data-ttu-id="7f472-106">Lista dostępnych wersji na potrzeby tworzenia zarządzanych klastrów Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="7f472-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="7f472-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f472-107">EXAMPLES</span></span>

### <span data-ttu-id="7f472-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7f472-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="7f472-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f472-109">PARAMETERS</span></span>

### <span data-ttu-id="7f472-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f472-110">-DefaultProfile</span></span>
<span data-ttu-id="7f472-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f472-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f472-112">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7f472-112">-Location</span></span>
<span data-ttu-id="7f472-113">Lokalizacja platformy Azure dla klastra.</span><span class="sxs-lookup"><span data-stu-id="7f472-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="7f472-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f472-114">CommonParameters</span></span>
<span data-ttu-id="7f472-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f472-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f472-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f472-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f472-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f472-117">INPUTS</span></span>

### <span data-ttu-id="7f472-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7f472-118">None</span></span>

## <span data-ttu-id="7f472-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f472-119">OUTPUTS</span></span>

### <span data-ttu-id="7f472-120">Microsoft. Azure. Commands. AKS. models. PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="7f472-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="7f472-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f472-121">NOTES</span></span>

## <span data-ttu-id="7f472-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f472-122">RELATED LINKS</span></span>
