---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/stop-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
ms.openlocfilehash: e1afa87d1ab21222987a4eeecf68a3786934ef57
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064290"
---
# <span data-ttu-id="98b92-101">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="98b92-101">Stop-AzCdnEndpoint</span></span>

## <span data-ttu-id="98b92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98b92-102">SYNOPSIS</span></span>
<span data-ttu-id="98b92-103">Zatrzymuje punkt końcowy usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="98b92-103">Stops the CDN endpoint.</span></span>

## <span data-ttu-id="98b92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98b92-104">SYNTAX</span></span>

### <span data-ttu-id="98b92-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="98b92-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98b92-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98b92-106">ByObjectParameterSet</span></span>
```
Stop-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98b92-107">Opis</span><span class="sxs-lookup"><span data-stu-id="98b92-107">DESCRIPTION</span></span>
<span data-ttu-id="98b92-108">Polecenie cmdlet **stop-AzCdnEndpoint** zatrzymuje punkt końcowy sieci dostarczania zawartości platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="98b92-108">The **Stop-AzCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="98b92-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98b92-109">EXAMPLES</span></span>

## <span data-ttu-id="98b92-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98b92-110">PARAMETERS</span></span>

### <span data-ttu-id="98b92-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="98b92-111">-CdnEndpoint</span></span>
<span data-ttu-id="98b92-112">Określa obiekt punktu końcowego, który zostanie zatrzymany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98b92-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="98b92-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98b92-113">-DefaultProfile</span></span>
<span data-ttu-id="98b92-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="98b92-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98b92-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="98b92-115">-EndpointName</span></span>
<span data-ttu-id="98b92-116">Określa nazwę punktu końcowego, który zostanie zatrzymany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98b92-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="98b92-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98b92-117">-PassThru</span></span>
<span data-ttu-id="98b92-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="98b92-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="98b92-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="98b92-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="98b92-120">-Refilename</span><span class="sxs-lookup"><span data-stu-id="98b92-120">-ProfileName</span></span>
<span data-ttu-id="98b92-121">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="98b92-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="98b92-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98b92-122">-ResourceGroupName</span></span>
<span data-ttu-id="98b92-123">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="98b92-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="98b92-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98b92-124">-Confirm</span></span>
<span data-ttu-id="98b92-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98b92-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98b92-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98b92-126">-WhatIf</span></span>
<span data-ttu-id="98b92-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98b92-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98b92-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="98b92-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98b92-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b92-129">CommonParameters</span></span>
<span data-ttu-id="98b92-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98b92-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b92-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98b92-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b92-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98b92-132">INPUTS</span></span>

### <span data-ttu-id="98b92-133">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="98b92-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="98b92-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="98b92-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="98b92-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98b92-135">OUTPUTS</span></span>

### <span data-ttu-id="98b92-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98b92-136">System.Boolean</span></span>

## <span data-ttu-id="98b92-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98b92-137">NOTES</span></span>

## <span data-ttu-id="98b92-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98b92-138">RELATED LINKS</span></span>

[<span data-ttu-id="98b92-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="98b92-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="98b92-140">Nowe — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="98b92-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="98b92-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="98b92-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="98b92-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="98b92-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="98b92-143">Start — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="98b92-143">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)


