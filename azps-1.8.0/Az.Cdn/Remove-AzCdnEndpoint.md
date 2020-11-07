---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: 4dca00cf4b1746590591301657eb3ac0cbc7c17e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710367"
---
# <span data-ttu-id="6e965-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e965-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="6e965-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e965-102">SYNOPSIS</span></span>
<span data-ttu-id="6e965-103">Usuwa punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="6e965-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="6e965-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e965-104">SYNTAX</span></span>

### <span data-ttu-id="6e965-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e965-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e965-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e965-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e965-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6e965-107">DESCRIPTION</span></span>
<span data-ttu-id="6e965-108">Polecenie cmdlet **Remove-AzCdnEndpoint** umożliwia usunięcie punktu końcowego sieci dostarczania zawartości platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6e965-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="6e965-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e965-109">EXAMPLES</span></span>

## <span data-ttu-id="6e965-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e965-110">PARAMETERS</span></span>

### <span data-ttu-id="6e965-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e965-111">-CdnEndpoint</span></span>
<span data-ttu-id="6e965-112">Określa punkt końcowy, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e965-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6e965-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e965-113">-DefaultProfile</span></span>
<span data-ttu-id="6e965-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6e965-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e965-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6e965-115">-EndpointName</span></span>
<span data-ttu-id="6e965-116">Określa nazwę punktu końcowego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e965-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6e965-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6e965-117">-Force</span></span>
<span data-ttu-id="6e965-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6e965-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6e965-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e965-119">-PassThru</span></span>
<span data-ttu-id="6e965-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="6e965-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6e965-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="6e965-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6e965-122">-Refilename</span><span class="sxs-lookup"><span data-stu-id="6e965-122">-ProfileName</span></span>
<span data-ttu-id="6e965-123">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="6e965-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="6e965-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e965-124">-ResourceGroupName</span></span>
<span data-ttu-id="6e965-125">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="6e965-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="6e965-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6e965-126">-Confirm</span></span>
<span data-ttu-id="6e965-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e965-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e965-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e965-128">-WhatIf</span></span>
<span data-ttu-id="6e965-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e965-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e965-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6e965-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e965-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e965-131">CommonParameters</span></span>
<span data-ttu-id="6e965-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e965-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e965-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e965-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e965-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e965-134">INPUTS</span></span>

### <span data-ttu-id="6e965-135">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e965-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="6e965-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6e965-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6e965-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e965-137">OUTPUTS</span></span>

### <span data-ttu-id="6e965-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e965-138">System.Boolean</span></span>

## <span data-ttu-id="6e965-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e965-139">NOTES</span></span>

## <span data-ttu-id="6e965-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e965-140">RELATED LINKS</span></span>

[<span data-ttu-id="6e965-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e965-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="6e965-142">Nowe — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e965-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="6e965-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e965-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="6e965-144">Start — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e965-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="6e965-145">Zatrzymaj — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e965-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)

