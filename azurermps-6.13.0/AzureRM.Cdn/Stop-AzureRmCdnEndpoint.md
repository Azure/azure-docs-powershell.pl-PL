---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/stop-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 20206ebf99d597a2961804bf3062cd4c049f8017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717941"
---
# <span data-ttu-id="2e80c-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e80c-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="2e80c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e80c-102">SYNOPSIS</span></span>
<span data-ttu-id="2e80c-103">Zatrzymuje punkt końcowy usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="2e80c-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e80c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e80c-104">SYNTAX</span></span>

### <span data-ttu-id="2e80c-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2e80c-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e80c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e80c-106">ByObjectParameterSet</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e80c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2e80c-107">DESCRIPTION</span></span>
<span data-ttu-id="2e80c-108">Polecenie cmdlet **stop-AzureRmCdnEndpoint** zatrzymuje punkt końcowy sieci dostarczania zawartości platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2e80c-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="2e80c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e80c-109">EXAMPLES</span></span>

## <span data-ttu-id="2e80c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e80c-110">PARAMETERS</span></span>

### <span data-ttu-id="2e80c-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e80c-111">-CdnEndpoint</span></span>
<span data-ttu-id="2e80c-112">Określa obiekt punktu końcowego, który zostanie zatrzymany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e80c-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="2e80c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e80c-113">-DefaultProfile</span></span>
<span data-ttu-id="2e80c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2e80c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e80c-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2e80c-115">-EndpointName</span></span>
<span data-ttu-id="2e80c-116">Określa nazwę punktu końcowego, który zostanie zatrzymany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e80c-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="2e80c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e80c-117">-PassThru</span></span>
<span data-ttu-id="2e80c-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="2e80c-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2e80c-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2e80c-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2e80c-120">-Refilename</span><span class="sxs-lookup"><span data-stu-id="2e80c-120">-ProfileName</span></span>
<span data-ttu-id="2e80c-121">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="2e80c-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="2e80c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e80c-122">-ResourceGroupName</span></span>
<span data-ttu-id="2e80c-123">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="2e80c-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="2e80c-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e80c-124">-Confirm</span></span>
<span data-ttu-id="2e80c-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e80c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e80c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e80c-126">-WhatIf</span></span>
<span data-ttu-id="2e80c-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e80c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e80c-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2e80c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e80c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e80c-129">CommonParameters</span></span>
<span data-ttu-id="2e80c-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e80c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e80c-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e80c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e80c-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e80c-132">INPUTS</span></span>

### <span data-ttu-id="2e80c-133">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e80c-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="2e80c-134">Parametry: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2e80c-134">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="2e80c-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2e80c-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2e80c-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e80c-136">OUTPUTS</span></span>

### <span data-ttu-id="2e80c-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2e80c-137">System.Boolean</span></span>

## <span data-ttu-id="2e80c-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e80c-138">NOTES</span></span>

## <span data-ttu-id="2e80c-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e80c-139">RELATED LINKS</span></span>

[<span data-ttu-id="2e80c-140">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e80c-140">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="2e80c-141">Nowe — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e80c-141">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="2e80c-142">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e80c-142">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="2e80c-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e80c-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="2e80c-144">Start — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e80c-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


