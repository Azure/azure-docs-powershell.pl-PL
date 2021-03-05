---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: dd5ca513c327a1ed5d045c3b0283a8b220f6a062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967025"
---
# <span data-ttu-id="44d4f-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="44d4f-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="44d4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="44d4f-103">Uzyskaj konfiguracje doradcy platformy Azure dla danej subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="44d4f-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="44d4f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="44d4f-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44d4f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="44d4f-105">DESCRIPTION</span></span>
<span data-ttu-id="44d4f-106">Konfiguracje skojarzone z subskrypcją mają dwa typy:</span><span class="sxs-lookup"><span data-stu-id="44d4f-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="44d4f-107">Konfiguracja na poziomie subskrypcji: Dla subskrypcji może być tylko jedna konfiguracja tego typu.</span><span class="sxs-lookup"><span data-stu-id="44d4f-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="44d4f-108">Jedynymi właściwościami tego typu konfiguracji są LowCpuThreshold i Exclude.</span><span class="sxs-lookup"><span data-stu-id="44d4f-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="44d4f-109">Konfiguracja na poziomie grupy zasobów: Dla każdej grupy zasobów w subskrypcji może być tylko jedna konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="44d4f-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="44d4f-110">Jedyną właściwością tego typu konfiguracji jest Wyklucz.</span><span class="sxs-lookup"><span data-stu-id="44d4f-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="44d4f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="44d4f-111">EXAMPLES</span></span>

### <span data-ttu-id="44d4f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="44d4f-112">Example 1</span></span>
```powershell
PS C:\>$data = Get-AzAdvisorConfiguration
Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}-{resourceGroupName}
Name       : {user_subscription}-{resourceGroupName}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

PS C:\>$data[0].Properties
AdditionalProperties :
Exclude              : False
LowCpuThreshold      : 20

PS C:\>$data[1].Properties
AdditionalProperties :
Exclude              : True
LowCpuThreshold      : null

```
<span data-ttu-id="44d4f-113">Pobiera listę konfiguracji doradców platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="44d4f-113">Retrieves a list of Azure Advisor Configuration(s).</span></span>

## <span data-ttu-id="44d4f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44d4f-114">PARAMETERS</span></span>

### <span data-ttu-id="44d4f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44d4f-115">-DefaultProfile</span></span>
<span data-ttu-id="44d4f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="44d4f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44d4f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44d4f-117">-ResourceGroupName</span></span>
<span data-ttu-id="44d4f-118">Nazwa grupy zasobów konfiguracji</span><span class="sxs-lookup"><span data-stu-id="44d4f-118">Resource Group name of the configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44d4f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44d4f-119">CommonParameters</span></span>
<span data-ttu-id="44d4f-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44d4f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="44d4f-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44d4f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44d4f-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44d4f-122">INPUTS</span></span>

### <span data-ttu-id="44d4f-123">Brak</span><span class="sxs-lookup"><span data-stu-id="44d4f-123">None</span></span>

## <span data-ttu-id="44d4f-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44d4f-124">OUTPUTS</span></span>

### <span data-ttu-id="44d4f-125">Microsoft.Azure.Commands.Advisor.Cmdlet.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="44d4f-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="44d4f-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="44d4f-126">NOTES</span></span>

## <span data-ttu-id="44d4f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44d4f-127">RELATED LINKS</span></span>
