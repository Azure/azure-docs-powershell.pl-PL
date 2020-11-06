---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 6feb7eb3f20e06c8dfffaa3dd9a1fb2bf3cc4c68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547527"
---
# <span data-ttu-id="89bff-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="89bff-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="89bff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89bff-102">SYNOPSIS</span></span>
<span data-ttu-id="89bff-103">Usuwa punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="89bff-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89bff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89bff-104">SYNTAX</span></span>

### <span data-ttu-id="89bff-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="89bff-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89bff-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89bff-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89bff-107">Opis</span><span class="sxs-lookup"><span data-stu-id="89bff-107">DESCRIPTION</span></span>
<span data-ttu-id="89bff-108">Polecenie cmdlet **Remove-AzureRmCdnEndpoint** umożliwia usunięcie punktu końcowego sieci dostarczania zawartości platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="89bff-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="89bff-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89bff-109">EXAMPLES</span></span>

## <span data-ttu-id="89bff-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89bff-110">PARAMETERS</span></span>

### <span data-ttu-id="89bff-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="89bff-111">-CdnEndpoint</span></span>
<span data-ttu-id="89bff-112">Określa punkt końcowy, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89bff-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="89bff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89bff-113">-DefaultProfile</span></span>
<span data-ttu-id="89bff-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="89bff-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89bff-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="89bff-115">-EndpointName</span></span>
<span data-ttu-id="89bff-116">Określa nazwę punktu końcowego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89bff-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="89bff-117">-Force</span><span class="sxs-lookup"><span data-stu-id="89bff-117">-Force</span></span>
<span data-ttu-id="89bff-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="89bff-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89bff-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89bff-119">-PassThru</span></span>
<span data-ttu-id="89bff-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="89bff-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="89bff-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="89bff-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="89bff-122">-Refilename</span><span class="sxs-lookup"><span data-stu-id="89bff-122">-ProfileName</span></span>
<span data-ttu-id="89bff-123">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="89bff-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="89bff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89bff-124">-ResourceGroupName</span></span>
<span data-ttu-id="89bff-125">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="89bff-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="89bff-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89bff-126">-Confirm</span></span>
<span data-ttu-id="89bff-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89bff-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89bff-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89bff-128">-WhatIf</span></span>
<span data-ttu-id="89bff-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89bff-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89bff-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="89bff-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89bff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89bff-131">CommonParameters</span></span>
<span data-ttu-id="89bff-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89bff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89bff-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89bff-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89bff-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89bff-134">INPUTS</span></span>

### <span data-ttu-id="89bff-135">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="89bff-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="89bff-136">Parametry: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="89bff-136">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="89bff-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="89bff-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="89bff-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89bff-138">OUTPUTS</span></span>

### <span data-ttu-id="89bff-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89bff-139">System.Boolean</span></span>

## <span data-ttu-id="89bff-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89bff-140">NOTES</span></span>

## <span data-ttu-id="89bff-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89bff-141">RELATED LINKS</span></span>

[<span data-ttu-id="89bff-142">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="89bff-142">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="89bff-143">Nowe — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="89bff-143">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="89bff-144">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="89bff-144">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="89bff-145">Start — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="89bff-145">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="89bff-146">Zatrzymaj — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="89bff-146">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


