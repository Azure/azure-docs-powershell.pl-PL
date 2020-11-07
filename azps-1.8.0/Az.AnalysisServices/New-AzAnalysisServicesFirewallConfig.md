---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: f3c84b22a9ea8c913cb520ae913fff89ae9470ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704704"
---
# <span data-ttu-id="77adf-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="77adf-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="77adf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77adf-102">SYNOPSIS</span></span>
<span data-ttu-id="77adf-103">Tworzy nową konfigurację zapory usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="77adf-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="77adf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77adf-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77adf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="77adf-105">DESCRIPTION</span></span>
<span data-ttu-id="77adf-106">New-AzAnalysisServicesFirewallConfig tworzy nowy obiekt konfiguracji zapory</span><span class="sxs-lookup"><span data-stu-id="77adf-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="77adf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77adf-107">EXAMPLES</span></span>

### <span data-ttu-id="77adf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77adf-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="77adf-109">Tworzy obiekt konfiguracji zapory z dwiema regułami, a ponadto umożliwia dostęp z usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="77adf-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="77adf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77adf-110">PARAMETERS</span></span>

### <span data-ttu-id="77adf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77adf-111">-DefaultProfile</span></span>
<span data-ttu-id="77adf-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77adf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77adf-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="77adf-113">-EnablePowerBIService</span></span>
<span data-ttu-id="77adf-114">Flaga wskazująca, czy zapora zezwala na dostęp z usługi Power BI</span><span class="sxs-lookup"><span data-stu-id="77adf-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77adf-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="77adf-115">-FirewallRule</span></span>
<span data-ttu-id="77adf-116">Lista reguł zapory</span><span class="sxs-lookup"><span data-stu-id="77adf-116">A list of firewall rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77adf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77adf-117">CommonParameters</span></span>
<span data-ttu-id="77adf-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77adf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77adf-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77adf-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77adf-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77adf-120">INPUTS</span></span>

### <span data-ttu-id="77adf-121">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. AnalysisServices. MODELES. PsAzureAnalysisServicesFirewallRule, Microsoft. Azure. PowerShell. cmdlets. AnalysisServices, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="77adf-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="77adf-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77adf-122">OUTPUTS</span></span>

### <span data-ttu-id="77adf-123">Microsoft. Azure. Commands. AnalysisServices. models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="77adf-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="77adf-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77adf-124">NOTES</span></span>

## <span data-ttu-id="77adf-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77adf-125">RELATED LINKS</span></span>

[<span data-ttu-id="77adf-126">Nowe — AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="77adf-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)