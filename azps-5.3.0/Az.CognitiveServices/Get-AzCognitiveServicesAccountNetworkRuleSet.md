---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 24b2cb6efca1213365c99a2c095f90e675c317c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501983"
---
# <span data-ttu-id="f7666-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7666-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="f7666-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7666-102">SYNOPSIS</span></span>
<span data-ttu-id="f7666-103">Uzyskiwanie właściwości NetworkRule konta usług poznawczych</span><span class="sxs-lookup"><span data-stu-id="f7666-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="f7666-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7666-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7666-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7666-105">DESCRIPTION</span></span>
<span data-ttu-id="f7666-106">Polecenie cmdlet **Get-AzCognitiveServicesAccountNetworkRuleSet** Pobiera właściwość NetworkRule konta usług poznawczych</span><span class="sxs-lookup"><span data-stu-id="f7666-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="f7666-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7666-107">EXAMPLES</span></span>

### <span data-ttu-id="f7666-108">Przykład 1: pobieranie właściwości NetworkRule dla określonego konta usług poznawczych</span><span class="sxs-lookup"><span data-stu-id="f7666-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="f7666-109">To polecenie pobiera właściwość NetworkRule określonego konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="f7666-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="f7666-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7666-110">PARAMETERS</span></span>

### <span data-ttu-id="f7666-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7666-111">-DefaultProfile</span></span>
<span data-ttu-id="f7666-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7666-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7666-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f7666-113">-Name</span></span>
<span data-ttu-id="f7666-114">Nazwa konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="f7666-114">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="f7666-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7666-115">-ResourceGroupName</span></span>
<span data-ttu-id="f7666-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7666-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="f7666-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7666-117">CommonParameters</span></span>
<span data-ttu-id="f7666-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7666-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7666-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7666-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7666-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7666-120">INPUTS</span></span>

### <span data-ttu-id="f7666-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f7666-121">System.String</span></span>

## <span data-ttu-id="f7666-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7666-122">OUTPUTS</span></span>

### <span data-ttu-id="f7666-123">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7666-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="f7666-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7666-124">NOTES</span></span>

## <span data-ttu-id="f7666-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7666-125">RELATED LINKS</span></span>
