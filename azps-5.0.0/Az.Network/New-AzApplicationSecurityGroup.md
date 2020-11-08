---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 32d7767ac5bd43be8fb9a3129966a0a88d761953
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233029"
---
# <span data-ttu-id="76311-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="76311-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="76311-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76311-102">SYNOPSIS</span></span>
<span data-ttu-id="76311-103">Tworzy grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="76311-103">Creates an application security group.</span></span>

## <span data-ttu-id="76311-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76311-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76311-105">Opis</span><span class="sxs-lookup"><span data-stu-id="76311-105">DESCRIPTION</span></span>
<span data-ttu-id="76311-106">Polecenie cmdlet **New-AzApplicationSecurityGroup** tworzy grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="76311-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="76311-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76311-107">EXAMPLES</span></span>

### <span data-ttu-id="76311-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76311-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="76311-109">W tym przykładzie jest tworzona Grupa zabezpieczeń aplikacji bez żadnych skojarzeń.</span><span class="sxs-lookup"><span data-stu-id="76311-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="76311-110">Po jego utworzeniu w grupie mogą wchodzić konfiguracje IP w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="76311-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="76311-111">Reguły bezpieczeństwa mogą również odwoływać się do grupy jako jej źródeł lub lokalizacji docelowych.</span><span class="sxs-lookup"><span data-stu-id="76311-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="76311-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76311-112">PARAMETERS</span></span>

### <span data-ttu-id="76311-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76311-113">-AsJob</span></span>
<span data-ttu-id="76311-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="76311-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76311-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76311-115">-DefaultProfile</span></span>
<span data-ttu-id="76311-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76311-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76311-117">-Force</span><span class="sxs-lookup"><span data-stu-id="76311-117">-Force</span></span>
<span data-ttu-id="76311-118">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób.</span><span class="sxs-lookup"><span data-stu-id="76311-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="76311-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="76311-119">-Location</span></span>
<span data-ttu-id="76311-120">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="76311-120">The location.</span></span>

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

### <span data-ttu-id="76311-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="76311-121">-Name</span></span>
<span data-ttu-id="76311-122">Nazwa grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="76311-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="76311-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76311-123">-ResourceGroupName</span></span>
<span data-ttu-id="76311-124">Nazwa grupy zasobów grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="76311-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="76311-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="76311-125">-Tag</span></span>
<span data-ttu-id="76311-126">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="76311-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="76311-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76311-127">-Confirm</span></span>
<span data-ttu-id="76311-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76311-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76311-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76311-129">-WhatIf</span></span>
<span data-ttu-id="76311-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76311-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76311-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="76311-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76311-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76311-132">CommonParameters</span></span>
<span data-ttu-id="76311-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76311-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76311-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76311-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76311-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76311-135">INPUTS</span></span>

### <span data-ttu-id="76311-136">System. String</span><span class="sxs-lookup"><span data-stu-id="76311-136">System.String</span></span>

### <span data-ttu-id="76311-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="76311-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="76311-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76311-138">OUTPUTS</span></span>

### <span data-ttu-id="76311-139">Microsoft. Azure. Commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="76311-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="76311-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76311-140">NOTES</span></span>

## <span data-ttu-id="76311-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76311-141">RELATED LINKS</span></span>

[<span data-ttu-id="76311-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="76311-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="76311-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="76311-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="76311-144">Nowe — AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76311-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="76311-145">Dodaj-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76311-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="76311-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76311-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="76311-147">Nowe — AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="76311-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="76311-148">Dodaj-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="76311-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="76311-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="76311-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
