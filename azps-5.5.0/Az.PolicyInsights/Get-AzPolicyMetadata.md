---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193178"
---
# <span data-ttu-id="27666-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="27666-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="27666-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27666-102">SYNOPSIS</span></span>
<span data-ttu-id="27666-103">Pobiera zasoby metadanych zasad</span><span class="sxs-lookup"><span data-stu-id="27666-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="27666-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="27666-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27666-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="27666-105">DESCRIPTION</span></span>
<span data-ttu-id="27666-106">Polecenie **cmdlet Get-AzPolicyRemediation** pobiera wszystkie zasoby metadanych zasad lub określony zasób metadanych zasad.</span><span class="sxs-lookup"><span data-stu-id="27666-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="27666-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="27666-107">EXAMPLES</span></span>

### <span data-ttu-id="27666-108">Przykład 1. Uzyskiwanie wszystkich zasobów metadanych zasad</span><span class="sxs-lookup"><span data-stu-id="27666-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="27666-109">To polecenie pobiera wszystkie zasoby metadanych zasad</span><span class="sxs-lookup"><span data-stu-id="27666-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="27666-110">Przykład 2. Uzyskiwanie kolekcji 10 zasobów metadanych zasad</span><span class="sxs-lookup"><span data-stu-id="27666-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="27666-111">To polecenie otrzymuje kolekcję 10 zasobów metadanych zasad</span><span class="sxs-lookup"><span data-stu-id="27666-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="27666-112">Przykład 3. Uzyskiwanie zasobu metadanych zasad o nazwie "ACF1348"</span><span class="sxs-lookup"><span data-stu-id="27666-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="27666-113">To polecenie otrzymuje pojedynczy zasób metadanych zasad o nazwie "ACF1348"</span><span class="sxs-lookup"><span data-stu-id="27666-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="27666-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27666-114">PARAMETERS</span></span>

### <span data-ttu-id="27666-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27666-115">-DefaultProfile</span></span>
<span data-ttu-id="27666-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="27666-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27666-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="27666-117">-Name</span></span>
<span data-ttu-id="27666-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="27666-118">Resource name.</span></span>

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

### <span data-ttu-id="27666-119">— Na górze</span><span class="sxs-lookup"><span data-stu-id="27666-119">-Top</span></span>
<span data-ttu-id="27666-120">Maksymalna liczba zwracanych zasobów metadanych zasad.</span><span class="sxs-lookup"><span data-stu-id="27666-120">Maximum number of policy metadata resources to return.</span></span>

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

### <span data-ttu-id="27666-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27666-121">CommonParameters</span></span>
<span data-ttu-id="27666-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27666-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27666-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27666-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27666-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27666-124">INPUTS</span></span>

### <span data-ttu-id="27666-125">System.String</span><span class="sxs-lookup"><span data-stu-id="27666-125">System.String</span></span>

## <span data-ttu-id="27666-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27666-126">OUTPUTS</span></span>

### <span data-ttu-id="27666-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="27666-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="27666-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="27666-128">NOTES</span></span>

## <span data-ttu-id="27666-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27666-129">RELATED LINKS</span></span>
