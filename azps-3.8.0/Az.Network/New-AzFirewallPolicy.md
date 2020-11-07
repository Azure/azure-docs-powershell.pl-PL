---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 5c432224891de6c2fcadc42ae308e9607bc3e432
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894165"
---
# <span data-ttu-id="cede7-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="cede7-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="cede7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cede7-102">SYNOPSIS</span></span>
<span data-ttu-id="cede7-103">Tworzy nowe zasady zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cede7-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="cede7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cede7-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cede7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cede7-105">DESCRIPTION</span></span>
<span data-ttu-id="cede7-106">Polecenie cmdlet **New-AzFirewallPolicy** tworzy zasady zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cede7-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="cede7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cede7-107">EXAMPLES</span></span>

### <span data-ttu-id="cede7-108">1. tworzenie pustych zasad</span><span class="sxs-lookup"><span data-stu-id="cede7-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="cede7-109">W tym przykładzie przedstawiono tworzenie zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cede7-109">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="cede7-110">2. tworzenie pustych zasad z trybem ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="cede7-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="cede7-111">W tym przykładzie przedstawiono tworzenie zasad zapory platformy Azure z zagrożonym trybem Intel</span><span class="sxs-lookup"><span data-stu-id="cede7-111">This example creates an azure firewall policy with a threat intel mode</span></span>

## <span data-ttu-id="cede7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cede7-112">PARAMETERS</span></span>

### <span data-ttu-id="cede7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cede7-113">-AsJob</span></span>
<span data-ttu-id="cede7-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cede7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cede7-115">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="cede7-115">-BasePolicy</span></span>
<span data-ttu-id="cede7-116">Tryb pracy dla analizy zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="cede7-116">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="cede7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cede7-117">-DefaultProfile</span></span>
<span data-ttu-id="cede7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cede7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cede7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cede7-119">-Force</span></span>
<span data-ttu-id="cede7-120">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="cede7-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cede7-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cede7-121">-Location</span></span>
<span data-ttu-id="cede7-122">pozycję.</span><span class="sxs-lookup"><span data-stu-id="cede7-122">location.</span></span>

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

### <span data-ttu-id="cede7-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cede7-123">-Name</span></span>
<span data-ttu-id="cede7-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="cede7-124">The resource name.</span></span>

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

### <span data-ttu-id="cede7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cede7-125">-ResourceGroupName</span></span>
<span data-ttu-id="cede7-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cede7-126">The resource group name.</span></span>

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

### <span data-ttu-id="cede7-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="cede7-127">-Tag</span></span>
<span data-ttu-id="cede7-128">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="cede7-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="cede7-129">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="cede7-129">-ThreatIntelMode</span></span>
<span data-ttu-id="cede7-130">Tryb pracy dla analizy zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="cede7-130">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="cede7-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cede7-131">-Confirm</span></span>
<span data-ttu-id="cede7-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cede7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cede7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cede7-133">-WhatIf</span></span>
<span data-ttu-id="cede7-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cede7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cede7-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cede7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cede7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cede7-136">CommonParameters</span></span>
<span data-ttu-id="cede7-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cede7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cede7-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cede7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cede7-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cede7-139">INPUTS</span></span>

### <span data-ttu-id="cede7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cede7-140">System.String</span></span>

### <span data-ttu-id="cede7-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cede7-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cede7-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cede7-142">OUTPUTS</span></span>

### <span data-ttu-id="cede7-143">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="cede7-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="cede7-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cede7-144">NOTES</span></span>

## <span data-ttu-id="cede7-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cede7-145">RELATED LINKS</span></span>
