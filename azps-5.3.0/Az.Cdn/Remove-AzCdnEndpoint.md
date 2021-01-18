---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: 780765ea56cd13ee7cbd09b64dc20db896234aec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504192"
---
# <span data-ttu-id="a13a5-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a13a5-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="a13a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a13a5-102">SYNOPSIS</span></span>
<span data-ttu-id="a13a5-103">Usuwa punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="a13a5-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="a13a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a13a5-104">SYNTAX</span></span>

### <span data-ttu-id="a13a5-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a13a5-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a13a5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a13a5-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a13a5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a13a5-107">DESCRIPTION</span></span>
<span data-ttu-id="a13a5-108">Polecenie cmdlet **Remove-AzCdnEndpoint** umożliwia usunięcie punktu końcowego sieci dostarczania zawartości platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a13a5-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="a13a5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a13a5-109">EXAMPLES</span></span>

## <span data-ttu-id="a13a5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a13a5-110">PARAMETERS</span></span>

### <span data-ttu-id="a13a5-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a13a5-111">-CdnEndpoint</span></span>
<span data-ttu-id="a13a5-112">Określa punkt końcowy, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a13a5-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a13a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a13a5-113">-DefaultProfile</span></span>
<span data-ttu-id="a13a5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a13a5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a13a5-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a13a5-115">-EndpointName</span></span>
<span data-ttu-id="a13a5-116">Określa nazwę punktu końcowego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a13a5-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a13a5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a13a5-117">-Force</span></span>
<span data-ttu-id="a13a5-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a13a5-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a13a5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a13a5-119">-PassThru</span></span>
<span data-ttu-id="a13a5-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="a13a5-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a13a5-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a13a5-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a13a5-122">-Refilename</span><span class="sxs-lookup"><span data-stu-id="a13a5-122">-ProfileName</span></span>
<span data-ttu-id="a13a5-123">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="a13a5-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="a13a5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a13a5-124">-ResourceGroupName</span></span>
<span data-ttu-id="a13a5-125">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="a13a5-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="a13a5-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a13a5-126">-Confirm</span></span>
<span data-ttu-id="a13a5-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a13a5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a13a5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a13a5-128">-WhatIf</span></span>
<span data-ttu-id="a13a5-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a13a5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a13a5-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a13a5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a13a5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a13a5-131">CommonParameters</span></span>
<span data-ttu-id="a13a5-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a13a5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a13a5-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a13a5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a13a5-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a13a5-134">INPUTS</span></span>

### <span data-ttu-id="a13a5-135">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a13a5-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="a13a5-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a13a5-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a13a5-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a13a5-137">OUTPUTS</span></span>

### <span data-ttu-id="a13a5-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a13a5-138">System.Boolean</span></span>

## <span data-ttu-id="a13a5-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a13a5-139">NOTES</span></span>

## <span data-ttu-id="a13a5-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a13a5-140">RELATED LINKS</span></span>

[<span data-ttu-id="a13a5-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a13a5-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="a13a5-142">Nowe — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a13a5-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="a13a5-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a13a5-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="a13a5-144">Start — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a13a5-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="a13a5-145">Zatrzymaj — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a13a5-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


