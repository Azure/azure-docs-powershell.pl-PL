---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
ms.openlocfilehash: ea1a656222383428f7e951ce858ec94c3fdc979e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717762"
---
# <span data-ttu-id="e35c0-101">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="e35c0-101">New-AzureRmAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="e35c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e35c0-102">SYNOPSIS</span></span>
<span data-ttu-id="e35c0-103">Tworzy nową konfigurację zapory usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="e35c0-103">Creates a new Analysis Services firewall config</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e35c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e35c0-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallConfig [-EnablePowerBIService] [-FirewallRules] List<Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule> 
```

## <span data-ttu-id="e35c0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e35c0-105">DESCRIPTION</span></span>
<span data-ttu-id="e35c0-106">New-AzureRmAnalysisServicesFirewallConfig tworzy nowy obiekt konfiguracji zapory</span><span class="sxs-lookup"><span data-stu-id="e35c0-106">The New-AzureRmAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="e35c0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e35c0-107">EXAMPLES</span></span>

### <span data-ttu-id="e35c0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e35c0-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> New-AzureRmAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRules $rule1,$rule2
```

<span data-ttu-id="e35c0-109">Tworzy konfigurację reguły zapory bez włączania usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="e35c0-109">Creates a firewall rule config without enabling power bi service.</span></span>

## <span data-ttu-id="e35c0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e35c0-110">PARAMETERS</span></span>

### <span data-ttu-id="e35c0-111">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="e35c0-111">-EnablePowerBIService</span></span>
<span data-ttu-id="e35c0-112">Flaga wskazująca, czy włączyć usługę PowerBI</span><span class="sxs-lookup"><span data-stu-id="e35c0-112">A flag to indicate if enable PowerBI service</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35c0-113">-FirewallRules</span><span class="sxs-lookup"><span data-stu-id="e35c0-113">-FirewallRules</span></span>
<span data-ttu-id="e35c0-114">Lista reguł zapory</span><span class="sxs-lookup"><span data-stu-id="e35c0-114">A list of firewall rules</span></span>

```yaml
Type: List<Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule>
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="e35c0-115">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e35c0-115">INPUTS</span></span>

## <span data-ttu-id="e35c0-116">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e35c0-116">OUTPUTS</span></span>

### <span data-ttu-id="e35c0-117">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="e35c0-117">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="e35c0-118">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e35c0-118">RELATED LINKS</span></span>

[<span data-ttu-id="e35c0-119">Nowe — AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="e35c0-119">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
