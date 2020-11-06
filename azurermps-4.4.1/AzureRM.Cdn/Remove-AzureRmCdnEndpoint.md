---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 49afefc7b80b5475735f61cb0511366b7f27a466
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554398"
---
# <span data-ttu-id="9e8c0-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e8c0-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="9e8c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e8c0-102">SYNOPSIS</span></span>
<span data-ttu-id="9e8c0-103">Usuwa punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e8c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e8c0-104">SYNTAX</span></span>

### <span data-ttu-id="9e8c0-105">Zestaw parametrów dla parametrów pól</span><span class="sxs-lookup"><span data-stu-id="9e8c0-105">Parameter Set for fields parameters</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e8c0-106">Zestaw parametrów dla parametrów obiektu</span><span class="sxs-lookup"><span data-stu-id="9e8c0-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e8c0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9e8c0-107">DESCRIPTION</span></span>
<span data-ttu-id="9e8c0-108">Polecenie cmdlet **Remove-AzureRmCdnEndpoint** umożliwia usunięcie punktu końcowego sieci dostarczania zawartości platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="9e8c0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e8c0-109">EXAMPLES</span></span>

## <span data-ttu-id="9e8c0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e8c0-110">PARAMETERS</span></span>

### <span data-ttu-id="9e8c0-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e8c0-111">-CdnEndpoint</span></span>
<span data-ttu-id="9e8c0-112">Określa punkt końcowy, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-112">Specifies the endpoint that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e8c0-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9e8c0-113">-EndpointName</span></span>
<span data-ttu-id="9e8c0-114">Określa nazwę punktu końcowego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-114">Specifies the name of the endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e8c0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9e8c0-115">-Force</span></span>
<span data-ttu-id="9e8c0-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e8c0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e8c0-117">-PassThru</span></span>
<span data-ttu-id="9e8c0-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9e8c0-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9e8c0-120">-Refilename</span><span class="sxs-lookup"><span data-stu-id="9e8c0-120">-ProfileName</span></span>
<span data-ttu-id="9e8c0-121">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e8c0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e8c0-122">-ResourceGroupName</span></span>
<span data-ttu-id="9e8c0-123">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e8c0-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9e8c0-124">-Confirm</span></span>
<span data-ttu-id="9e8c0-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e8c0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e8c0-126">-WhatIf</span></span>
<span data-ttu-id="9e8c0-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e8c0-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e8c0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e8c0-129">-DefaultProfile</span></span>
<span data-ttu-id="9e8c0-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e8c0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e8c0-131">CommonParameters</span></span>
<span data-ttu-id="9e8c0-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e8c0-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e8c0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e8c0-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e8c0-134">INPUTS</span></span>

### <span data-ttu-id="9e8c0-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e8c0-135">PSEndpoint</span></span>
<span data-ttu-id="9e8c0-136">Parametr "CdnEndpoint" akceptuje wartość typu "PSEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="9e8c0-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="9e8c0-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e8c0-137">OUTPUTS</span></span>

### <span data-ttu-id="9e8c0-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e8c0-138">System.Boolean</span></span>

## <span data-ttu-id="9e8c0-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e8c0-139">NOTES</span></span>

## <span data-ttu-id="9e8c0-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e8c0-140">RELATED LINKS</span></span>

[<span data-ttu-id="9e8c0-141">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e8c0-141">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9e8c0-142">Nowe — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e8c0-142">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9e8c0-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e8c0-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9e8c0-144">Start — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e8c0-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9e8c0-145">Zatrzymaj — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e8c0-145">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


