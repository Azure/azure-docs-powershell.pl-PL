---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 83229b9251e7cbbbe4bd17d73004b9bc64800511
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547011"
---
# <span data-ttu-id="04c8b-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="04c8b-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="04c8b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="04c8b-103">Zatrzymuje punkt końcowy usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="04c8b-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04c8b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04c8b-104">SYNTAX</span></span>

### <span data-ttu-id="04c8b-105">Parametr ustawiony dla parametrów pól (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="04c8b-105">Parameter Set for fields parameters (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04c8b-106">Zestaw parametrów dla parametrów obiektu</span><span class="sxs-lookup"><span data-stu-id="04c8b-106">Parameter Set for object parameters</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04c8b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="04c8b-107">DESCRIPTION</span></span>
<span data-ttu-id="04c8b-108">Polecenie cmdlet **stop-AzureRmCdnEndpoint** zatrzymuje punkt końcowy sieci dostarczania zawartości platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="04c8b-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="04c8b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04c8b-109">EXAMPLES</span></span>

## <span data-ttu-id="04c8b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04c8b-110">PARAMETERS</span></span>

### <span data-ttu-id="04c8b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="04c8b-111">-CdnEndpoint</span></span>
<span data-ttu-id="04c8b-112">Określa obiekt punktu końcowego, który zostanie zatrzymany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04c8b-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="04c8b-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="04c8b-113">-EndpointName</span></span>
<span data-ttu-id="04c8b-114">Określa nazwę punktu końcowego, który zostanie zatrzymany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04c8b-114">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="04c8b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04c8b-115">-PassThru</span></span>
<span data-ttu-id="04c8b-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="04c8b-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="04c8b-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="04c8b-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="04c8b-118">-Refilename</span><span class="sxs-lookup"><span data-stu-id="04c8b-118">-ProfileName</span></span>
<span data-ttu-id="04c8b-119">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="04c8b-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="04c8b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04c8b-120">-ResourceGroupName</span></span>
<span data-ttu-id="04c8b-121">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="04c8b-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="04c8b-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04c8b-122">-Confirm</span></span>
<span data-ttu-id="04c8b-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04c8b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04c8b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04c8b-124">-WhatIf</span></span>
<span data-ttu-id="04c8b-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04c8b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04c8b-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="04c8b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04c8b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c8b-127">-DefaultProfile</span></span>
<span data-ttu-id="04c8b-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04c8b-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04c8b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c8b-129">CommonParameters</span></span>
<span data-ttu-id="04c8b-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04c8b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c8b-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04c8b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c8b-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04c8b-132">INPUTS</span></span>

### <span data-ttu-id="04c8b-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="04c8b-133">PSEndpoint</span></span>
<span data-ttu-id="04c8b-134">Parametr "CdnEndpoint" akceptuje wartość typu "PSEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="04c8b-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="04c8b-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04c8b-135">OUTPUTS</span></span>

### <span data-ttu-id="04c8b-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04c8b-136">System.Boolean</span></span>

## <span data-ttu-id="04c8b-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04c8b-137">NOTES</span></span>

## <span data-ttu-id="04c8b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04c8b-138">RELATED LINKS</span></span>

[<span data-ttu-id="04c8b-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="04c8b-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="04c8b-140">Nowe — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="04c8b-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="04c8b-141">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="04c8b-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="04c8b-142">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="04c8b-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="04c8b-143">Start — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="04c8b-143">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


