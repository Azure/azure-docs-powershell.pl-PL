---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: 85a5c38038116d89e7cab1e6efe2718d4c5a697b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989150"
---
# <span data-ttu-id="f7ead-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="f7ead-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="f7ead-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7ead-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ead-103">Pobiera zasoby metadanych zasad</span><span class="sxs-lookup"><span data-stu-id="f7ead-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="f7ead-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f7ead-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7ead-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f7ead-105">DESCRIPTION</span></span>
<span data-ttu-id="f7ead-106">Polecenie **cmdlet Get-AzPolicyRemediation** pobiera wszystkie zasoby metadanych zasad lub określony zasób metadanych zasad.</span><span class="sxs-lookup"><span data-stu-id="f7ead-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="f7ead-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f7ead-107">EXAMPLES</span></span>

### <span data-ttu-id="f7ead-108">Przykład 1. Uzyskiwanie wszystkich zasobów metadanych zasad</span><span class="sxs-lookup"><span data-stu-id="f7ead-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="f7ead-109">To polecenie pobiera wszystkie zasoby metadanych zasad</span><span class="sxs-lookup"><span data-stu-id="f7ead-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="f7ead-110">Przykład 2. Uzyskiwanie kolekcji 10 zasobów metadanych zasad</span><span class="sxs-lookup"><span data-stu-id="f7ead-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="f7ead-111">To polecenie otrzymuje kolekcję 10 zasobów metadanych zasad</span><span class="sxs-lookup"><span data-stu-id="f7ead-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="f7ead-112">Przykład 3. Uzyskiwanie zasobu metadanych zasad o nazwie "ACF1348"</span><span class="sxs-lookup"><span data-stu-id="f7ead-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="f7ead-113">To polecenie otrzymuje pojedynczy zasób metadanych zasad o nazwie "ACF1348"</span><span class="sxs-lookup"><span data-stu-id="f7ead-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="f7ead-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7ead-114">PARAMETERS</span></span>

### <span data-ttu-id="f7ead-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ead-115">-DefaultProfile</span></span>
<span data-ttu-id="f7ead-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ead-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7ead-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f7ead-117">-Name</span></span>
<span data-ttu-id="f7ead-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f7ead-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7ead-119">— Na górze</span><span class="sxs-lookup"><span data-stu-id="f7ead-119">-Top</span></span>
<span data-ttu-id="f7ead-120">Maksymalna liczba zwracanych zasobów metadanych zasad.</span><span class="sxs-lookup"><span data-stu-id="f7ead-120">Maximum number of policy metadata resources to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7ead-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ead-121">CommonParameters</span></span>
<span data-ttu-id="f7ead-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7ead-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ead-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7ead-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ead-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7ead-124">INPUTS</span></span>

### <span data-ttu-id="f7ead-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f7ead-125">System.String</span></span>

## <span data-ttu-id="f7ead-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7ead-126">OUTPUTS</span></span>

### <span data-ttu-id="f7ead-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="f7ead-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="f7ead-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f7ead-128">NOTES</span></span>

## <span data-ttu-id="f7ead-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7ead-129">RELATED LINKS</span></span>
