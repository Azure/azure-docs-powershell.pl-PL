---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 60a61af31b5a7986779b19b893d4c02d0039ae49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007114"
---
# <span data-ttu-id="9030e-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9030e-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="9030e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9030e-102">SYNOPSIS</span></span>
<span data-ttu-id="9030e-103">Uzyskiwanie właściwości NetworkRule konta usług Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="9030e-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="9030e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9030e-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9030e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9030e-105">DESCRIPTION</span></span>
<span data-ttu-id="9030e-106">Polecenie **cmdlet Get-AzCognitiveServicesAccountNetworkRuleSet** pobiera właściwość NetworkRule konta usług Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="9030e-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="9030e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9030e-107">EXAMPLES</span></span>

### <span data-ttu-id="9030e-108">Przykład 1. Uzyskiwanie właściwości NetworkRule określonego konta usług Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="9030e-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="9030e-109">To polecenie pobiera właściwość NetworkRule określonego konta usług Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="9030e-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="9030e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9030e-110">PARAMETERS</span></span>

### <span data-ttu-id="9030e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9030e-111">-DefaultProfile</span></span>
<span data-ttu-id="9030e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9030e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9030e-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9030e-113">-Name</span></span>
<span data-ttu-id="9030e-114">Nazwa konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="9030e-114">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9030e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9030e-115">-ResourceGroupName</span></span>
<span data-ttu-id="9030e-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9030e-116">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9030e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9030e-117">CommonParameters</span></span>
<span data-ttu-id="9030e-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9030e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9030e-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9030e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9030e-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9030e-120">INPUTS</span></span>

### <span data-ttu-id="9030e-121">System.String</span><span class="sxs-lookup"><span data-stu-id="9030e-121">System.String</span></span>

## <span data-ttu-id="9030e-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9030e-122">OUTPUTS</span></span>

### <span data-ttu-id="9030e-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9030e-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="9030e-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9030e-124">NOTES</span></span>

## <span data-ttu-id="9030e-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9030e-125">RELATED LINKS</span></span>
