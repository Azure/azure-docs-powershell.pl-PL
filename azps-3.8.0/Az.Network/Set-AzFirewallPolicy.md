---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 1e5fbeba85431ab593d4daedff0f8b71af13ace4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051476"
---
# <span data-ttu-id="b4b87-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b4b87-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="b4b87-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4b87-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b87-103">Zapisuje zmodyfikowane zasady zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b4b87-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="b4b87-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4b87-104">SYNTAX</span></span>

### <span data-ttu-id="b4b87-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b4b87-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4b87-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4b87-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4b87-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4b87-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>] [-BasePolicy <String>]
 -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4b87-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b4b87-108">DESCRIPTION</span></span>
<span data-ttu-id="b4b87-109">Polecenie cmdlet **Set-AzFirewallPolicy** aktualizuje zasady zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b87-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="b4b87-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4b87-110">EXAMPLES</span></span>

### <span data-ttu-id="b4b87-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b4b87-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="b4b87-112">W tym przykładzie ustawiono zasadę zapory z nową wartością zasad zapory</span><span class="sxs-lookup"><span data-stu-id="b4b87-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="b4b87-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b4b87-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="b4b87-114">W tym przykładzie ustawiono zasady zapory przy użyciu nowego trybu zagrożenia dla procesorów firmy Intel</span><span class="sxs-lookup"><span data-stu-id="b4b87-114">This example sets the firewall policy with the new threat intel mode</span></span>

## <span data-ttu-id="b4b87-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4b87-115">PARAMETERS</span></span>

### <span data-ttu-id="b4b87-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4b87-116">-AsJob</span></span>
<span data-ttu-id="b4b87-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b4b87-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4b87-118">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="b4b87-118">-BasePolicy</span></span>
<span data-ttu-id="b4b87-119">Zasady bazowe, których dziedziczenie</span><span class="sxs-lookup"><span data-stu-id="b4b87-119">The base policy to inherit from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b87-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b87-120">-DefaultProfile</span></span>
<span data-ttu-id="b4b87-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b87-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4b87-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b4b87-122">-InputObject</span></span>
<span data-ttu-id="b4b87-123">Zasady AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b4b87-123">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b87-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b4b87-124">-Location</span></span>
<span data-ttu-id="b4b87-125">pozycję.</span><span class="sxs-lookup"><span data-stu-id="b4b87-125">location.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b87-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b4b87-126">-Name</span></span>
<span data-ttu-id="b4b87-127">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b4b87-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b87-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4b87-128">-ResourceGroupName</span></span>
<span data-ttu-id="b4b87-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4b87-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b87-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4b87-130">-ResourceId</span></span>
<span data-ttu-id="b4b87-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="b4b87-131">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b87-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4b87-132">-Tag</span></span>
<span data-ttu-id="b4b87-133">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4b87-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b4b87-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="b4b87-134">-ThreatIntelMode</span></span>
<span data-ttu-id="b4b87-135">Tryb pracy dla analizy zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="b4b87-135">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b87-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4b87-136">-Confirm</span></span>
<span data-ttu-id="b4b87-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4b87-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4b87-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4b87-138">-WhatIf</span></span>
<span data-ttu-id="b4b87-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4b87-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4b87-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b4b87-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4b87-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b87-141">CommonParameters</span></span>
<span data-ttu-id="b4b87-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4b87-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b87-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4b87-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b87-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4b87-144">INPUTS</span></span>

### <span data-ttu-id="b4b87-145">System. String</span><span class="sxs-lookup"><span data-stu-id="b4b87-145">System.String</span></span>

### <span data-ttu-id="b4b87-146">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b4b87-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="b4b87-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b4b87-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b4b87-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4b87-148">OUTPUTS</span></span>

### <span data-ttu-id="b4b87-149">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b4b87-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="b4b87-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4b87-150">NOTES</span></span>

## <span data-ttu-id="b4b87-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4b87-151">RELATED LINKS</span></span>
