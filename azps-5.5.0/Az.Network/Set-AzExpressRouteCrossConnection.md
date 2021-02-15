---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 649ae6233f312dab4f18263bb65c4a9cd43b2aee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189523"
---
# <span data-ttu-id="2cab6-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2cab6-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="2cab6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cab6-102">SYNOPSIS</span></span>
<span data-ttu-id="2cab6-103">Zmodyfikuje połączenie krzyżowe z usługą ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2cab6-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="2cab6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2cab6-104">SYNTAX</span></span>

### <span data-ttu-id="2cab6-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="2cab6-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cab6-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="2cab6-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cab6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="2cab6-107">DESCRIPTION</span></span>
<span data-ttu-id="2cab6-108">Polecenie **cmdlet Set-AzExpressRouteCrossConnection** zapisuje zmodyfikowane połączenie krzyżowe usługi ExpressRoute na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2cab6-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="2cab6-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2cab6-109">EXAMPLES</span></span>

### <span data-ttu-id="2cab6-110">Przykład 1. Zmienianie stanu inicjowania obsługi przez dostawcę usług w połączeniu krzyżowym usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="2cab6-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="2cab6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cab6-111">PARAMETERS</span></span>

### <span data-ttu-id="2cab6-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2cab6-112">-AsJob</span></span>
<span data-ttu-id="2cab6-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2cab6-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2cab6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cab6-114">-DefaultProfile</span></span>
<span data-ttu-id="2cab6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2cab6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cab6-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2cab6-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="2cab6-117">Określa obiekt **ExpressRouteCrossConnection,** który zostanie zmodyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cab6-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: ModifyByCircuitReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cab6-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2cab6-118">-Force</span></span>
<span data-ttu-id="2cab6-119">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="2cab6-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2cab6-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2cab6-120">-Name</span></span>
<span data-ttu-id="2cab6-121">Nazwa połączenia krzyżowego trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="2cab6-121">The name of express route cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cab6-122">— Komunikacja równorzędna</span><span class="sxs-lookup"><span data-stu-id="2cab6-122">-Peerings</span></span>
<span data-ttu-id="2cab6-123">Lista komunikacji równorzędnej dla połączenia krzyżowego</span><span class="sxs-lookup"><span data-stu-id="2cab6-123">The list of peerings for the cross connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionPeering[]
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cab6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cab6-124">-ResourceGroupName</span></span>
<span data-ttu-id="2cab6-125">The ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2cab6-125">The ExpressRouteCrossConnection</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cab6-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="2cab6-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="2cab6-127">Notatki usługodawca notatki</span><span class="sxs-lookup"><span data-stu-id="2cab6-127">The service provider notes</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cab6-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="2cab6-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="2cab6-129">Stan usługodawca obsługi administracyjnej do ustawienia</span><span class="sxs-lookup"><span data-stu-id="2cab6-129">The service provider provisioning state to be set</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cab6-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2cab6-130">-Confirm</span></span>
<span data-ttu-id="2cab6-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2cab6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cab6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cab6-132">-WhatIf</span></span>
<span data-ttu-id="2cab6-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cab6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2cab6-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2cab6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cab6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cab6-135">CommonParameters</span></span>
<span data-ttu-id="2cab6-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cab6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cab6-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cab6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cab6-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2cab6-138">INPUTS</span></span>

### <span data-ttu-id="2cab6-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2cab6-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="2cab6-140">Parametr "ExpressRouteCrossConnection" akceptuje wartość typu "PSExpressRouteCrossConnection" z potoku</span><span class="sxs-lookup"><span data-stu-id="2cab6-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="2cab6-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2cab6-141">OUTPUTS</span></span>

### <span data-ttu-id="2cab6-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2cab6-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="2cab6-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2cab6-143">NOTES</span></span>

## <span data-ttu-id="2cab6-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2cab6-144">RELATED LINKS</span></span>

[<span data-ttu-id="2cab6-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2cab6-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
