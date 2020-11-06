---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/stop-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 508465250489f2bcd0b031627258f11370fccfa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526997"
---
# <span data-ttu-id="aff92-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="aff92-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="aff92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aff92-102">SYNOPSIS</span></span>
<span data-ttu-id="aff92-103">Zatrzymuje punkt końcowy usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="aff92-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aff92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aff92-104">SYNTAX</span></span>

### <span data-ttu-id="aff92-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aff92-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aff92-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aff92-106">ByObjectParameterSet</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aff92-107">Opis</span><span class="sxs-lookup"><span data-stu-id="aff92-107">DESCRIPTION</span></span>
<span data-ttu-id="aff92-108">Polecenie cmdlet **stop-AzureRmCdnEndpoint** zatrzymuje punkt końcowy sieci dostarczania zawartości platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="aff92-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="aff92-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aff92-109">EXAMPLES</span></span>

## <span data-ttu-id="aff92-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aff92-110">PARAMETERS</span></span>

### <span data-ttu-id="aff92-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="aff92-111">-CdnEndpoint</span></span>
<span data-ttu-id="aff92-112">Określa obiekt punktu końcowego, który zostanie zatrzymany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aff92-112">Specifies the endpoint object that this cmdlet stops.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aff92-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff92-113">-DefaultProfile</span></span>
<span data-ttu-id="aff92-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="aff92-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff92-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="aff92-115">-EndpointName</span></span>
<span data-ttu-id="aff92-116">Określa nazwę punktu końcowego, który zostanie zatrzymany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aff92-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff92-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aff92-117">-PassThru</span></span>
<span data-ttu-id="aff92-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="aff92-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="aff92-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="aff92-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aff92-120">-Refilename</span><span class="sxs-lookup"><span data-stu-id="aff92-120">-ProfileName</span></span>
<span data-ttu-id="aff92-121">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="aff92-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff92-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aff92-122">-ResourceGroupName</span></span>
<span data-ttu-id="aff92-123">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="aff92-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff92-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aff92-124">-Confirm</span></span>
<span data-ttu-id="aff92-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aff92-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff92-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aff92-126">-WhatIf</span></span>
<span data-ttu-id="aff92-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aff92-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aff92-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aff92-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff92-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff92-129">CommonParameters</span></span>
<span data-ttu-id="aff92-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aff92-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff92-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aff92-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff92-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aff92-132">INPUTS</span></span>

### <span data-ttu-id="aff92-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="aff92-133">PSEndpoint</span></span>
<span data-ttu-id="aff92-134">Parametr "CdnEndpoint" akceptuje wartość typu "PSEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="aff92-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="aff92-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aff92-135">OUTPUTS</span></span>

### <span data-ttu-id="aff92-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aff92-136">System.Boolean</span></span>

## <span data-ttu-id="aff92-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aff92-137">NOTES</span></span>

## <span data-ttu-id="aff92-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aff92-138">RELATED LINKS</span></span>

[<span data-ttu-id="aff92-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="aff92-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="aff92-140">Nowe — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="aff92-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="aff92-141">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="aff92-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="aff92-142">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="aff92-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="aff92-143">Start — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="aff92-143">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


