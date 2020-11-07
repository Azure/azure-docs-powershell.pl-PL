---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/start-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
ms.openlocfilehash: cfa0eb8506230fe14b9ddf48bcd7562acf45a590
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717230"
---
# <span data-ttu-id="791a3-101">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="791a3-101">Start-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="791a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="791a3-102">SYNOPSIS</span></span>
<span data-ttu-id="791a3-103">Rozpoczynanie punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="791a3-103">Starts a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="791a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="791a3-104">SYNTAX</span></span>

### <span data-ttu-id="791a3-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="791a3-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="791a3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="791a3-106">ByObjectParameterSet</span></span>
```
Start-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="791a3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="791a3-107">DESCRIPTION</span></span>
<span data-ttu-id="791a3-108">Polecenie cmdlet **Start-AzureRmCdnEndpoint** umożliwia uruchomienie punktu końcowego sieci dostarczania zawartości Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="791a3-108">The **Start-AzureRmCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="791a3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="791a3-109">EXAMPLES</span></span>

## <span data-ttu-id="791a3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="791a3-110">PARAMETERS</span></span>

### <span data-ttu-id="791a3-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="791a3-111">-CdnEndpoint</span></span>
<span data-ttu-id="791a3-112">Określa punkt końcowy, w którym jest uruchamiane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="791a3-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="791a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="791a3-113">-DefaultProfile</span></span>
<span data-ttu-id="791a3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="791a3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="791a3-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="791a3-115">-EndpointName</span></span>
<span data-ttu-id="791a3-116">Określa nazwę punktu końcowego, który jest uruchamiany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="791a3-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="791a3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="791a3-117">-PassThru</span></span>
<span data-ttu-id="791a3-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="791a3-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="791a3-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="791a3-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="791a3-120">-Refilename</span><span class="sxs-lookup"><span data-stu-id="791a3-120">-ProfileName</span></span>
<span data-ttu-id="791a3-121">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="791a3-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="791a3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="791a3-122">-ResourceGroupName</span></span>
<span data-ttu-id="791a3-123">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="791a3-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="791a3-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="791a3-124">-Confirm</span></span>
<span data-ttu-id="791a3-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="791a3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="791a3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="791a3-126">-WhatIf</span></span>
<span data-ttu-id="791a3-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="791a3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="791a3-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="791a3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="791a3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="791a3-129">CommonParameters</span></span>
<span data-ttu-id="791a3-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="791a3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="791a3-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="791a3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="791a3-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="791a3-132">INPUTS</span></span>

### <span data-ttu-id="791a3-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="791a3-133">PSEndpoint</span></span>
<span data-ttu-id="791a3-134">Parametr "CdnEndpoint" akceptuje wartość typu "PSEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="791a3-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="791a3-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="791a3-135">OUTPUTS</span></span>

### <span data-ttu-id="791a3-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="791a3-136">System.Boolean</span></span>

## <span data-ttu-id="791a3-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="791a3-137">NOTES</span></span>

## <span data-ttu-id="791a3-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="791a3-138">RELATED LINKS</span></span>

[<span data-ttu-id="791a3-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="791a3-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="791a3-140">Nowe — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="791a3-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="791a3-141">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="791a3-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="791a3-142">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="791a3-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="791a3-143">Zatrzymaj — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="791a3-143">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


