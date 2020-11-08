---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 649ae6233f312dab4f18263bb65c4a9cd43b2aee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223033"
---
# <span data-ttu-id="76116-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="76116-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="76116-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76116-102">SYNOPSIS</span></span>
<span data-ttu-id="76116-103">Modyfikuje połączenie z ExpressRoute krzyżową.</span><span class="sxs-lookup"><span data-stu-id="76116-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="76116-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76116-104">SYNTAX</span></span>

### <span data-ttu-id="76116-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="76116-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76116-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="76116-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76116-107">Opis</span><span class="sxs-lookup"><span data-stu-id="76116-107">DESCRIPTION</span></span>
<span data-ttu-id="76116-108">Polecenie cmdlet **Set-AzExpressRouteCrossConnection** zapisuje zmodyfikowane ExpressRoute krzyżowe połączenie z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76116-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="76116-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76116-109">EXAMPLES</span></span>

### <span data-ttu-id="76116-110">Przykład 1. Zmień stan inicjowania obsługi dostawcy usług w połączeniu krzyżowym ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="76116-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="76116-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76116-111">PARAMETERS</span></span>

### <span data-ttu-id="76116-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76116-112">-AsJob</span></span>
<span data-ttu-id="76116-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="76116-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76116-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76116-114">-DefaultProfile</span></span>
<span data-ttu-id="76116-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76116-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76116-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="76116-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="76116-117">Określa obiekt **ExpressRouteCrossConnection** , który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76116-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="76116-118">-Force</span><span class="sxs-lookup"><span data-stu-id="76116-118">-Force</span></span>
<span data-ttu-id="76116-119">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="76116-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="76116-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="76116-120">-Name</span></span>
<span data-ttu-id="76116-121">Nazwa połączenia krzyżowego Express Route.</span><span class="sxs-lookup"><span data-stu-id="76116-121">The name of express route cross connection.</span></span>

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

### <span data-ttu-id="76116-122">-Peer</span><span class="sxs-lookup"><span data-stu-id="76116-122">-Peerings</span></span>
<span data-ttu-id="76116-123">Lista połączeń z użytkownikami połączeń krzyżowych</span><span class="sxs-lookup"><span data-stu-id="76116-123">The list of peerings for the cross connection</span></span>

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

### <span data-ttu-id="76116-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76116-124">-ResourceGroupName</span></span>
<span data-ttu-id="76116-125">ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="76116-125">The ExpressRouteCrossConnection</span></span>

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

### <span data-ttu-id="76116-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="76116-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="76116-127">Uwagi dotyczące dostawcy usług</span><span class="sxs-lookup"><span data-stu-id="76116-127">The service provider notes</span></span>

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

### <span data-ttu-id="76116-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="76116-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="76116-129">Stan inicjowania obsługi dostawcy usług</span><span class="sxs-lookup"><span data-stu-id="76116-129">The service provider provisioning state to be set</span></span>

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

### <span data-ttu-id="76116-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76116-130">-Confirm</span></span>
<span data-ttu-id="76116-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76116-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76116-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76116-132">-WhatIf</span></span>
<span data-ttu-id="76116-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76116-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76116-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="76116-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76116-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76116-135">CommonParameters</span></span>
<span data-ttu-id="76116-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76116-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76116-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76116-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76116-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76116-138">INPUTS</span></span>

### <span data-ttu-id="76116-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="76116-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="76116-140">Parametr "ExpressRouteCrossConnection" akceptuje wartość typu "PSExpressRouteCrossConnection" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="76116-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="76116-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76116-141">OUTPUTS</span></span>

### <span data-ttu-id="76116-142">Microsoft. Azure. Commands. Network. models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="76116-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="76116-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76116-143">NOTES</span></span>

## <span data-ttu-id="76116-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76116-144">RELATED LINKS</span></span>

[<span data-ttu-id="76116-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="76116-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
