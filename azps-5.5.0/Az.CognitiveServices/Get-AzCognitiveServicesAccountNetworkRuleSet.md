---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 24b2cb6efca1213365c99a2c095f90e675c317c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239070"
---
# <span data-ttu-id="43655-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="43655-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="43655-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43655-102">SYNOPSIS</span></span>
<span data-ttu-id="43655-103">Uzyskiwanie właściwości NetworkRule konta usług Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="43655-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="43655-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="43655-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43655-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="43655-105">DESCRIPTION</span></span>
<span data-ttu-id="43655-106">Polecenie **cmdlet Get-AzCognitiveServicesAccountNetworkRuleSet** pobiera właściwość NetworkRule konta usług Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="43655-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="43655-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="43655-107">EXAMPLES</span></span>

### <span data-ttu-id="43655-108">Przykład 1. Uzyskiwanie właściwości NetworkRule określonego konta usług Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="43655-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="43655-109">To polecenie pobiera właściwość NetworkRule określonego konta usług Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="43655-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="43655-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43655-110">PARAMETERS</span></span>

### <span data-ttu-id="43655-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43655-111">-DefaultProfile</span></span>
<span data-ttu-id="43655-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="43655-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43655-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="43655-113">-Name</span></span>
<span data-ttu-id="43655-114">Nazwa konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="43655-114">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="43655-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43655-115">-ResourceGroupName</span></span>
<span data-ttu-id="43655-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="43655-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="43655-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43655-117">CommonParameters</span></span>
<span data-ttu-id="43655-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43655-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43655-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43655-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43655-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43655-120">INPUTS</span></span>

### <span data-ttu-id="43655-121">System.String</span><span class="sxs-lookup"><span data-stu-id="43655-121">System.String</span></span>

## <span data-ttu-id="43655-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43655-122">OUTPUTS</span></span>

### <span data-ttu-id="43655-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="43655-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="43655-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="43655-124">NOTES</span></span>

## <span data-ttu-id="43655-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43655-125">RELATED LINKS</span></span>
