---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: 8829e81afc0549c3d4d29855e6256ab696315f0e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704726"
---
# <span data-ttu-id="44618-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="44618-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="44618-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44618-102">SYNOPSIS</span></span>
<span data-ttu-id="44618-103">Pobierz konfiguracje usługi Azure Advisor dla danej subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="44618-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="44618-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44618-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44618-105">Opis</span><span class="sxs-lookup"><span data-stu-id="44618-105">DESCRIPTION</span></span>
<span data-ttu-id="44618-106">Konfiguracje skojarzone z subskrypcją mają dwa typy:</span><span class="sxs-lookup"><span data-stu-id="44618-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="44618-107">Konfiguracja poziomu subskrypcji: dla subskrypcji może istnieć tylko jedna konfiguracja tego typu.</span><span class="sxs-lookup"><span data-stu-id="44618-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="44618-108">LowCpuThreshold i Exclude są jedyną właściwością tego typu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="44618-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="44618-109">Konfiguracja poziomu zasobów źródłowych: w subskrypcji może być tylko jedna konfiguracja dla każdej z nich.</span><span class="sxs-lookup"><span data-stu-id="44618-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="44618-110">Funkcja wykluczania jest jedyną właściwością tego typu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="44618-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="44618-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44618-111">EXAMPLES</span></span>

### <span data-ttu-id="44618-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="44618-112">Example 1</span></span>
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
<span data-ttu-id="44618-113">Pobiera listę konfiguracji usługi Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="44618-113">Retrieves a list of Azure Advisor Configration(s).</span></span>

## <span data-ttu-id="44618-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44618-114">PARAMETERS</span></span>

### <span data-ttu-id="44618-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44618-115">-DefaultProfile</span></span>
<span data-ttu-id="44618-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="44618-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44618-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44618-117">-ResourceGroupName</span></span>
<span data-ttu-id="44618-118">Nazwa grupy zasobów konfiguracji</span><span class="sxs-lookup"><span data-stu-id="44618-118">Resource Group name of the configuration</span></span>

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

### <span data-ttu-id="44618-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44618-119">CommonParameters</span></span>
<span data-ttu-id="44618-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44618-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="44618-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44618-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44618-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44618-122">INPUTS</span></span>

### <span data-ttu-id="44618-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="44618-123">None</span></span>

## <span data-ttu-id="44618-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44618-124">OUTPUTS</span></span>

### <span data-ttu-id="44618-125">Microsoft. Azure. Commands. Advisor. cmdlet. models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="44618-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="44618-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44618-126">NOTES</span></span>

## <span data-ttu-id="44618-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44618-127">RELATED LINKS</span></span>
