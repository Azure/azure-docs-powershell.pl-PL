---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 32d7767ac5bd43be8fb9a3129966a0a88d761953
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179722"
---
# <span data-ttu-id="da6bc-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="da6bc-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="da6bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da6bc-102">SYNOPSIS</span></span>
<span data-ttu-id="da6bc-103">Tworzy grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="da6bc-103">Creates an application security group.</span></span>

## <span data-ttu-id="da6bc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="da6bc-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da6bc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="da6bc-105">DESCRIPTION</span></span>
<span data-ttu-id="da6bc-106">Polecenie **cmdlet New-AzApplicationSecurityGroup** tworzy grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="da6bc-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="da6bc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="da6bc-107">EXAMPLES</span></span>

### <span data-ttu-id="da6bc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da6bc-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="da6bc-109">W tym przykładzie jest grupę zabezpieczeń aplikacji bez skojarzeń.</span><span class="sxs-lookup"><span data-stu-id="da6bc-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="da6bc-110">Po utworzeniu konfiguracji adresów IP w interfejsie sieciowym można dodać je do grupy.</span><span class="sxs-lookup"><span data-stu-id="da6bc-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="da6bc-111">Reguły zabezpieczeń mogą również odwoływać się do grupy jako do jej źródeł lub miejsc docelowych.</span><span class="sxs-lookup"><span data-stu-id="da6bc-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="da6bc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da6bc-112">PARAMETERS</span></span>

### <span data-ttu-id="da6bc-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="da6bc-113">-AsJob</span></span>
<span data-ttu-id="da6bc-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="da6bc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da6bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da6bc-115">-DefaultProfile</span></span>
<span data-ttu-id="da6bc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="da6bc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da6bc-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="da6bc-117">-Force</span></span>
<span data-ttu-id="da6bc-118">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób.</span><span class="sxs-lookup"><span data-stu-id="da6bc-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="da6bc-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="da6bc-119">-Location</span></span>
<span data-ttu-id="da6bc-120">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="da6bc-120">The location.</span></span>

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

### <span data-ttu-id="da6bc-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="da6bc-121">-Name</span></span>
<span data-ttu-id="da6bc-122">Nazwa grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="da6bc-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="da6bc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da6bc-123">-ResourceGroupName</span></span>
<span data-ttu-id="da6bc-124">Nazwa grupy zasobów grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="da6bc-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="da6bc-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="da6bc-125">-Tag</span></span>
<span data-ttu-id="da6bc-126">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="da6bc-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="da6bc-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da6bc-127">-Confirm</span></span>
<span data-ttu-id="da6bc-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="da6bc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da6bc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da6bc-129">-WhatIf</span></span>
<span data-ttu-id="da6bc-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da6bc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da6bc-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="da6bc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da6bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da6bc-132">CommonParameters</span></span>
<span data-ttu-id="da6bc-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da6bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da6bc-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da6bc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da6bc-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da6bc-135">INPUTS</span></span>

### <span data-ttu-id="da6bc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="da6bc-136">System.String</span></span>

### <span data-ttu-id="da6bc-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="da6bc-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="da6bc-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da6bc-138">OUTPUTS</span></span>

### <span data-ttu-id="da6bc-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="da6bc-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="da6bc-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="da6bc-140">NOTES</span></span>

## <span data-ttu-id="da6bc-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da6bc-141">RELATED LINKS</span></span>

[<span data-ttu-id="da6bc-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="da6bc-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="da6bc-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="da6bc-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="da6bc-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="da6bc-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="da6bc-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="da6bc-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="da6bc-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="da6bc-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="da6bc-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="da6bc-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="da6bc-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="da6bc-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="da6bc-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="da6bc-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
