---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 85fc0f0687ed3b32492f42f753f67ba1e85a4656
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177859"
---
# <span data-ttu-id="52bd4-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52bd4-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="52bd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="52bd4-103">Uruchamia punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="52bd4-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="52bd4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="52bd4-104">SYNTAX</span></span>

### <span data-ttu-id="52bd4-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="52bd4-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52bd4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52bd4-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52bd4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="52bd4-107">DESCRIPTION</span></span>
<span data-ttu-id="52bd4-108">Polecenie **cmdlet Start-AzCdnEndpoint** uruchamia punkt końcowy usługi Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="52bd4-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="52bd4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="52bd4-109">EXAMPLES</span></span>

## <span data-ttu-id="52bd4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52bd4-110">PARAMETERS</span></span>

### <span data-ttu-id="52bd4-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52bd4-111">-CdnEndpoint</span></span>
<span data-ttu-id="52bd4-112">Określa punkt końcowy, który ma się uruchamiać to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52bd4-112">Specifies the endpoint that this cmdlet starts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52bd4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52bd4-113">-DefaultProfile</span></span>
<span data-ttu-id="52bd4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="52bd4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52bd4-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="52bd4-115">-EndpointName</span></span>
<span data-ttu-id="52bd4-116">Określa nazwę punktu końcowego, na który uruchamia się to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52bd4-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bd4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52bd4-117">-PassThru</span></span>
<span data-ttu-id="52bd4-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="52bd4-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="52bd4-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="52bd4-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52bd4-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="52bd4-120">-ProfileName</span></span>
<span data-ttu-id="52bd4-121">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="52bd4-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bd4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52bd4-122">-ResourceGroupName</span></span>
<span data-ttu-id="52bd4-123">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="52bd4-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bd4-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="52bd4-124">-Confirm</span></span>
<span data-ttu-id="52bd4-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="52bd4-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bd4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52bd4-126">-WhatIf</span></span>
<span data-ttu-id="52bd4-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52bd4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52bd4-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="52bd4-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bd4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52bd4-129">CommonParameters</span></span>
<span data-ttu-id="52bd4-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52bd4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52bd4-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52bd4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52bd4-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52bd4-132">INPUTS</span></span>

### <span data-ttu-id="52bd4-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="52bd4-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="52bd4-134">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="52bd4-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="52bd4-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52bd4-135">OUTPUTS</span></span>

### <span data-ttu-id="52bd4-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52bd4-136">System.Boolean</span></span>

## <span data-ttu-id="52bd4-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="52bd4-137">NOTES</span></span>

## <span data-ttu-id="52bd4-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52bd4-138">RELATED LINKS</span></span>

[<span data-ttu-id="52bd4-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52bd4-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="52bd4-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52bd4-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="52bd4-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52bd4-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="52bd4-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52bd4-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="52bd4-143">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52bd4-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


