---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: cd9270d724e0e1523c3ee621cb58fa28a2f4bc66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184179"
---
# <span data-ttu-id="b445c-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="b445c-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="b445c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b445c-102">SYNOPSIS</span></span>
<span data-ttu-id="b445c-103">Aktualizuje grupę stref DNS</span><span class="sxs-lookup"><span data-stu-id="b445c-103">Updates DNS zone group</span></span>

## <span data-ttu-id="b445c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b445c-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b445c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b445c-105">DESCRIPTION</span></span>
<span data-ttu-id="b445c-106">Polecenie **cmdlet Set-AzPrivateDnsZoneGroup** aktualizuje grupę strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="b445c-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="b445c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b445c-107">EXAMPLES</span></span>

### <span data-ttu-id="b445c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b445c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]

PS C:\> $zone1 = Get-AzPrivateDnsZone -ResourceGroupName rg -Name "test1.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name test1-vault-azure-com -PrivateDnsZoneId $zone1.ResourceId
PS C:\> Set-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1 -PrivateDnsZoneConfig $config -Force

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test1-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test1.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="b445c-109">Powyższy przykład aktualizuje grupę strefy DNS o nazwie dnsgroup1 za pomocą nowej konfiguracji dns, która łączy się z inną strefą DNS.</span><span class="sxs-lookup"><span data-stu-id="b445c-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="b445c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b445c-110">PARAMETERS</span></span>

### <span data-ttu-id="b445c-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b445c-111">-AsJob</span></span>
<span data-ttu-id="b445c-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b445c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b445c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b445c-113">-DefaultProfile</span></span>
<span data-ttu-id="b445c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b445c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b445c-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b445c-115">-Name</span></span>
<span data-ttu-id="b445c-116">Nazwa prywatnej grupy stref DNS.</span><span class="sxs-lookup"><span data-stu-id="b445c-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="b445c-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="b445c-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="b445c-118">Zbiór prywatnych konfiguracji strefy dns prywatnej grupy strefy dns.</span><span class="sxs-lookup"><span data-stu-id="b445c-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="b445c-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="b445c-119">-PrivateEndpointName</span></span>
<span data-ttu-id="b445c-120">Nazwa prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="b445c-120">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="b445c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b445c-121">-ResourceGroupName</span></span>
<span data-ttu-id="b445c-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b445c-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="b445c-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b445c-123">-Confirm</span></span>
<span data-ttu-id="b445c-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b445c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b445c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b445c-125">-WhatIf</span></span>
<span data-ttu-id="b445c-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b445c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b445c-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b445c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b445c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b445c-128">CommonParameters</span></span>
<span data-ttu-id="b445c-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b445c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b445c-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b445c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b445c-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b445c-131">INPUTS</span></span>

### <span data-ttu-id="b445c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b445c-132">System.String</span></span>

### <span data-ttu-id="b445c-133">System.Collections.generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlet.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="b445c-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b445c-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b445c-134">OUTPUTS</span></span>

### <span data-ttu-id="b445c-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="b445c-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="b445c-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b445c-136">NOTES</span></span>

## <span data-ttu-id="b445c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b445c-137">RELATED LINKS</span></span>
