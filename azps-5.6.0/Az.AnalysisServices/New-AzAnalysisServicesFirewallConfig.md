---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: bd958c9157a5e47b1fc4a878c9ce72405490ec2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005002"
---
# <span data-ttu-id="ee66b-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="ee66b-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="ee66b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee66b-102">SYNOPSIS</span></span>
<span data-ttu-id="ee66b-103">Tworzy nową konfigurację zapory usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="ee66b-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="ee66b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ee66b-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee66b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ee66b-105">DESCRIPTION</span></span>
<span data-ttu-id="ee66b-106">Plik New-AzAnalysisServicesFirewallConfig tworzy nowy obiekt konfiguracji zapory</span><span class="sxs-lookup"><span data-stu-id="ee66b-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="ee66b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ee66b-107">EXAMPLES</span></span>

### <span data-ttu-id="ee66b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ee66b-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="ee66b-109">Tworzy obiekt konfiguracji zapory z dwiema regułami, jednocześnie włączając dostęp z usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="ee66b-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="ee66b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee66b-110">PARAMETERS</span></span>

### <span data-ttu-id="ee66b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee66b-111">-DefaultProfile</span></span>
<span data-ttu-id="ee66b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee66b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee66b-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="ee66b-113">-EnablePowerBIService</span></span>
<span data-ttu-id="ee66b-114">Flaga wskazująca, czy zapora zezwala na dostęp z usługi Power BI</span><span class="sxs-lookup"><span data-stu-id="ee66b-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="ee66b-115">- FirewallRule</span><span class="sxs-lookup"><span data-stu-id="ee66b-115">-FirewallRule</span></span>
<span data-ttu-id="ee66b-116">Lista reguł zapory</span><span class="sxs-lookup"><span data-stu-id="ee66b-116">A list of firewall rules</span></span>

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

### <span data-ttu-id="ee66b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee66b-117">CommonParameters</span></span>
<span data-ttu-id="ee66b-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee66b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee66b-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee66b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee66b-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee66b-120">INPUTS</span></span>

### <span data-ttu-id="ee66b-121">System.Collections.generic.List'1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlet.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="ee66b-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ee66b-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee66b-122">OUTPUTS</span></span>

### <span data-ttu-id="ee66b-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="ee66b-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="ee66b-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ee66b-124">NOTES</span></span>

## <span data-ttu-id="ee66b-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee66b-125">RELATED LINKS</span></span>

[<span data-ttu-id="ee66b-126">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ee66b-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)