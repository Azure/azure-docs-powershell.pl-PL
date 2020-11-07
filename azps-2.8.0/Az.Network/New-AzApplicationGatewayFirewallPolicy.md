---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: dc6005c77a72b3965f2fca670c1d729fc7c7bd07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870540"
---
# <span data-ttu-id="2e929-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="2e929-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="2e929-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e929-102">SYNOPSIS</span></span>
<span data-ttu-id="2e929-103">Tworzy zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2e929-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="2e929-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e929-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e929-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e929-105">DESCRIPTION</span></span>
<span data-ttu-id="2e929-106">Polecenie cmdlet **New-AzApplicationGatewayFirewallPolicy** tworzy zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2e929-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="2e929-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e929-107">EXAMPLES</span></span>

### <span data-ttu-id="2e929-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2e929-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRules $customRule
```

<span data-ttu-id="2e929-109">To polecenie tworzy nową zasadę zapory dla bramy aplikacji platformy Azure o nazwie "wafResource1" w grupie zasobów "RG1" w lokalizacji "zachód" z regułami niestandardowymi zdefiniowanymi w zmiennej $customRule</span><span class="sxs-lookup"><span data-stu-id="2e929-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="2e929-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e929-110">PARAMETERS</span></span>

### <span data-ttu-id="2e929-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e929-111">-AsJob</span></span>
<span data-ttu-id="2e929-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2e929-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e929-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="2e929-113">-CustomRule</span></span>
<span data-ttu-id="2e929-114">Lista CustomRules</span><span class="sxs-lookup"><span data-stu-id="2e929-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e929-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e929-115">-DefaultProfile</span></span>
<span data-ttu-id="2e929-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e929-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e929-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2e929-117">-Force</span></span>
<span data-ttu-id="2e929-118">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="2e929-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2e929-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2e929-119">-Location</span></span>
<span data-ttu-id="2e929-120">pozycję.</span><span class="sxs-lookup"><span data-stu-id="2e929-120">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e929-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e929-121">-Name</span></span>
<span data-ttu-id="2e929-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="2e929-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e929-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e929-123">-ResourceGroupName</span></span>
<span data-ttu-id="2e929-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e929-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e929-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e929-125">-Tag</span></span>
<span data-ttu-id="2e929-126">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e929-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e929-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e929-127">-Confirm</span></span>
<span data-ttu-id="2e929-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e929-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e929-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e929-129">-WhatIf</span></span>
<span data-ttu-id="2e929-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e929-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e929-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2e929-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e929-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e929-132">CommonParameters</span></span>
<span data-ttu-id="2e929-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e929-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e929-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e929-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e929-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e929-135">INPUTS</span></span>

### <span data-ttu-id="2e929-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2e929-136">System.String</span></span>

### <span data-ttu-id="2e929-137">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="2e929-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="2e929-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2e929-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2e929-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e929-139">OUTPUTS</span></span>

### <span data-ttu-id="2e929-140">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="2e929-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="2e929-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e929-141">NOTES</span></span>

## <span data-ttu-id="2e929-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e929-142">RELATED LINKS</span></span>
