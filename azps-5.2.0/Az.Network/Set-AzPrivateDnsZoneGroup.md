---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: cd9270d724e0e1523c3ee621cb58fa28a2f4bc66
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364044"
---
# <span data-ttu-id="fbdd1-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="fbdd1-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="fbdd1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbdd1-102">SYNOPSIS</span></span>
<span data-ttu-id="fbdd1-103">Aktualizowanie grupy stref DNS</span><span class="sxs-lookup"><span data-stu-id="fbdd1-103">Updates DNS zone group</span></span>

## <span data-ttu-id="fbdd1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbdd1-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbdd1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fbdd1-105">DESCRIPTION</span></span>
<span data-ttu-id="fbdd1-106">W poleceniu cmdlet **Set-AzPrivateDnsZoneGroup** jest polecenie Updates Group DNS Zone.</span><span class="sxs-lookup"><span data-stu-id="fbdd1-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="fbdd1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbdd1-107">EXAMPLES</span></span>

### <span data-ttu-id="fbdd1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fbdd1-108">Example 1</span></span>
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

<span data-ttu-id="fbdd1-109">W powyższym przykładzie jest aktualizowana Grupa stref DNS o nazwie dnsgroup1 z nową opcją dnsconfig, która łączy z inną strefą DNS.</span><span class="sxs-lookup"><span data-stu-id="fbdd1-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="fbdd1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbdd1-110">PARAMETERS</span></span>

### <span data-ttu-id="fbdd1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbdd1-111">-AsJob</span></span>
<span data-ttu-id="fbdd1-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fbdd1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fbdd1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbdd1-113">-DefaultProfile</span></span>
<span data-ttu-id="fbdd1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbdd1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbdd1-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fbdd1-115">-Name</span></span>
<span data-ttu-id="fbdd1-116">Nazwa grupy prywatna strefa DNS.</span><span class="sxs-lookup"><span data-stu-id="fbdd1-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="fbdd1-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="fbdd1-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="fbdd1-118">Zbiór konfiguracji prywatnych stref DNS w grupie prywatne strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="fbdd1-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="fbdd1-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="fbdd1-119">-PrivateEndpointName</span></span>
<span data-ttu-id="fbdd1-120">Nazwa prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="fbdd1-120">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="fbdd1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbdd1-121">-ResourceGroupName</span></span>
<span data-ttu-id="fbdd1-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fbdd1-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="fbdd1-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fbdd1-123">-Confirm</span></span>
<span data-ttu-id="fbdd1-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbdd1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbdd1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbdd1-125">-WhatIf</span></span>
<span data-ttu-id="fbdd1-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbdd1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbdd1-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fbdd1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbdd1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbdd1-128">CommonParameters</span></span>
<span data-ttu-id="fbdd1-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbdd1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbdd1-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbdd1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbdd1-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbdd1-131">INPUTS</span></span>

### <span data-ttu-id="fbdd1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fbdd1-132">System.String</span></span>

### <span data-ttu-id="fbdd1-133">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. modele. PSPrivateDnsZoneConfig, Microsoft. Azure. PowerShell. cmdlets. Network, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fbdd1-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fbdd1-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbdd1-134">OUTPUTS</span></span>

### <span data-ttu-id="fbdd1-135">Microsoft. Azure. Commands. Network. models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="fbdd1-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="fbdd1-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbdd1-136">NOTES</span></span>

## <span data-ttu-id="fbdd1-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbdd1-137">RELATED LINKS</span></span>
