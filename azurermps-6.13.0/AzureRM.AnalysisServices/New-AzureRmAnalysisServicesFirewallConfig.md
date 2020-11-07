---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
ms.openlocfilehash: 2369720eb3a2df1e1c65df727cb02c1464ddc218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716970"
---
# <span data-ttu-id="512a5-101">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="512a5-101">New-AzureRmAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="512a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="512a5-102">SYNOPSIS</span></span>
<span data-ttu-id="512a5-103">Tworzy nową konfigurację zapory usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="512a5-103">Creates a new Analysis Services firewall config</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="512a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="512a5-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="512a5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="512a5-105">DESCRIPTION</span></span>
<span data-ttu-id="512a5-106">New-AzureRmAnalysisServicesFirewallConfig tworzy nowy obiekt konfiguracji zapory</span><span class="sxs-lookup"><span data-stu-id="512a5-106">The New-AzureRmAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="512a5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="512a5-107">EXAMPLES</span></span>

### <span data-ttu-id="512a5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="512a5-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzureRmAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="512a5-109">Tworzy obiekt konfiguracji zapory z dwiema regułami, a ponadto umożliwia dostęp z usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="512a5-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="512a5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="512a5-110">PARAMETERS</span></span>

### <span data-ttu-id="512a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="512a5-111">-DefaultProfile</span></span>
<span data-ttu-id="512a5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="512a5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="512a5-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="512a5-113">-EnablePowerBIService</span></span>
<span data-ttu-id="512a5-114">Flaga wskazująca, czy zapora zezwala na dostęp z usługi Power BI</span><span class="sxs-lookup"><span data-stu-id="512a5-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="512a5-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="512a5-115">-FirewallRule</span></span>
<span data-ttu-id="512a5-116">Lista reguł zapory</span><span class="sxs-lookup"><span data-stu-id="512a5-116">A list of firewall rules</span></span>

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

### <span data-ttu-id="512a5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="512a5-117">CommonParameters</span></span>
<span data-ttu-id="512a5-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="512a5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="512a5-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="512a5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="512a5-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="512a5-120">INPUTS</span></span>

### <span data-ttu-id="512a5-121">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. AnalysisServices. MODELES. PsAzureAnalysisServicesFirewallRule, Microsoft. Azure. Commands. AnalysisServices, Version = 0.6.11.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="512a5-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.Commands.AnalysisServices, Version=0.6.11.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="512a5-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="512a5-122">OUTPUTS</span></span>

### <span data-ttu-id="512a5-123">Microsoft. Azure. Commands. AnalysisServices. models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="512a5-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="512a5-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="512a5-124">NOTES</span></span>

## <span data-ttu-id="512a5-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="512a5-125">RELATED LINKS</span></span>

[<span data-ttu-id="512a5-126">Nowe — AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="512a5-126">New-AzureRmAnalysisServicesFirewallRule</span></span>](./New-AzureRmAnalysisServicesFirewallRule.md)
