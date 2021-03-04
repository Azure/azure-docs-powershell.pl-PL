---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fc1c3a9641134c113713dab0c53b22027f2b7280
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958266"
---
# <span data-ttu-id="7ef88-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="7ef88-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="7ef88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ef88-102">SYNOPSIS</span></span>
<span data-ttu-id="7ef88-103">Tworzy prywatną grupę strefy DNS w określonym prywatnym punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="7ef88-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="7ef88-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7ef88-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ef88-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7ef88-105">DESCRIPTION</span></span>
<span data-ttu-id="7ef88-106">Polecenie **cmdlet New-AzPrivateDnsZoneGroup** umożliwia utworzenie nowej prywatnej grupy stref DNS.</span><span class="sxs-lookup"><span data-stu-id="7ef88-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="7ef88-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7ef88-107">EXAMPLES</span></span>

### <span data-ttu-id="7ef88-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7ef88-108">Example 1</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
PS C:\> New-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1" -PrivateDnsZoneConfig $config -Force
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="7ef88-109">Po `test-pr-endpoint` utworzeniu prywatnego punktu końcowego w powyższym przykładzie jest tworzona grupa strefy DNS w ramach tego prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="7ef88-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="7ef88-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ef88-110">PARAMETERS</span></span>

### <span data-ttu-id="7ef88-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7ef88-111">-AsJob</span></span>
<span data-ttu-id="7ef88-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7ef88-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ef88-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ef88-113">-DefaultProfile</span></span>
<span data-ttu-id="7ef88-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ef88-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ef88-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="7ef88-115">-Force</span></span>
<span data-ttu-id="7ef88-116">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="7ef88-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7ef88-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7ef88-117">-Name</span></span>
<span data-ttu-id="7ef88-118">Nazwa prywatnej grupy stref DNS.</span><span class="sxs-lookup"><span data-stu-id="7ef88-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef88-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="7ef88-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="7ef88-120">Zbiór prywatnych konfiguracji stref DNS prywatnej grupy stref dns.</span><span class="sxs-lookup"><span data-stu-id="7ef88-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef88-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="7ef88-121">-PrivateEndpointName</span></span>
<span data-ttu-id="7ef88-122">Nazwa prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="7ef88-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="7ef88-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ef88-123">-ResourceGroupName</span></span>
<span data-ttu-id="7ef88-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ef88-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="7ef88-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ef88-125">-Confirm</span></span>
<span data-ttu-id="7ef88-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7ef88-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ef88-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ef88-127">-WhatIf</span></span>
<span data-ttu-id="7ef88-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ef88-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ef88-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7ef88-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ef88-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ef88-130">CommonParameters</span></span>
<span data-ttu-id="7ef88-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ef88-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ef88-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ef88-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ef88-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ef88-133">INPUTS</span></span>

### <span data-ttu-id="7ef88-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7ef88-134">System.String</span></span>

### <span data-ttu-id="7ef88-135">System.Collections.generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlet.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="7ef88-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7ef88-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ef88-136">OUTPUTS</span></span>

### <span data-ttu-id="7ef88-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="7ef88-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="7ef88-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7ef88-138">NOTES</span></span>

## <span data-ttu-id="7ef88-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ef88-139">RELATED LINKS</span></span>
