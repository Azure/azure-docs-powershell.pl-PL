---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184403"
---
# <span data-ttu-id="9417e-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="9417e-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="9417e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9417e-102">SYNOPSIS</span></span>
<span data-ttu-id="9417e-103">Tworzy prywatną grupę strefy DNS w określonym prywatnym punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="9417e-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="9417e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9417e-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9417e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9417e-105">DESCRIPTION</span></span>
<span data-ttu-id="9417e-106">Polecenie **cmdlet New-AzPrivateDnsZoneGroup** umożliwia utworzenie nowej prywatnej grupy stref DNS.</span><span class="sxs-lookup"><span data-stu-id="9417e-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="9417e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9417e-107">EXAMPLES</span></span>

### <span data-ttu-id="9417e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9417e-108">Example 1</span></span>
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

<span data-ttu-id="9417e-109">Po `test-pr-endpoint` utworzeniu prywatnego punktu końcowego w powyższym przykładzie jest tworzona grupa strefy DNS w ramach tego prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9417e-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="9417e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9417e-110">PARAMETERS</span></span>

### <span data-ttu-id="9417e-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9417e-111">-AsJob</span></span>
<span data-ttu-id="9417e-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9417e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9417e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9417e-113">-DefaultProfile</span></span>
<span data-ttu-id="9417e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9417e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9417e-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9417e-115">-Force</span></span>
<span data-ttu-id="9417e-116">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="9417e-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9417e-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9417e-117">-Name</span></span>
<span data-ttu-id="9417e-118">Nazwa prywatnej grupy stref DNS.</span><span class="sxs-lookup"><span data-stu-id="9417e-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="9417e-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="9417e-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="9417e-120">Zbiór prywatnych konfiguracji stref DNS prywatnej grupy stref dns.</span><span class="sxs-lookup"><span data-stu-id="9417e-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="9417e-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="9417e-121">-PrivateEndpointName</span></span>
<span data-ttu-id="9417e-122">Nazwa prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9417e-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="9417e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9417e-123">-ResourceGroupName</span></span>
<span data-ttu-id="9417e-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9417e-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="9417e-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9417e-125">-Confirm</span></span>
<span data-ttu-id="9417e-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9417e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9417e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9417e-127">-WhatIf</span></span>
<span data-ttu-id="9417e-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9417e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9417e-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9417e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9417e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9417e-130">CommonParameters</span></span>
<span data-ttu-id="9417e-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9417e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9417e-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9417e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9417e-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9417e-133">INPUTS</span></span>

### <span data-ttu-id="9417e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9417e-134">System.String</span></span>

### <span data-ttu-id="9417e-135">System.Collections.generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlet.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="9417e-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9417e-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9417e-136">OUTPUTS</span></span>

### <span data-ttu-id="9417e-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="9417e-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="9417e-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9417e-138">NOTES</span></span>

## <span data-ttu-id="9417e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9417e-139">RELATED LINKS</span></span>
