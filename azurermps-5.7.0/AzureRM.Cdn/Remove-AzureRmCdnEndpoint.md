---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 8748806346baa4f84550d15749e7792ae928ad34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544540"
---
# <span data-ttu-id="34f19-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="34f19-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="34f19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34f19-102">SYNOPSIS</span></span>
<span data-ttu-id="34f19-103">Usuwa punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="34f19-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34f19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34f19-104">SYNTAX</span></span>

### <span data-ttu-id="34f19-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="34f19-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34f19-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34f19-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34f19-107">Opis</span><span class="sxs-lookup"><span data-stu-id="34f19-107">DESCRIPTION</span></span>
<span data-ttu-id="34f19-108">Polecenie cmdlet **Remove-AzureRmCdnEndpoint** umożliwia usunięcie punktu końcowego sieci dostarczania zawartości platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="34f19-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="34f19-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34f19-109">EXAMPLES</span></span>

## <span data-ttu-id="34f19-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34f19-110">PARAMETERS</span></span>

### <span data-ttu-id="34f19-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="34f19-111">-CdnEndpoint</span></span>
<span data-ttu-id="34f19-112">Określa punkt końcowy, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34f19-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="34f19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f19-113">-DefaultProfile</span></span>
<span data-ttu-id="34f19-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="34f19-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34f19-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="34f19-115">-EndpointName</span></span>
<span data-ttu-id="34f19-116">Określa nazwę punktu końcowego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34f19-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="34f19-117">-Force</span><span class="sxs-lookup"><span data-stu-id="34f19-117">-Force</span></span>
<span data-ttu-id="34f19-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="34f19-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f19-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34f19-119">-PassThru</span></span>
<span data-ttu-id="34f19-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="34f19-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="34f19-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="34f19-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="34f19-122">-Refilename</span><span class="sxs-lookup"><span data-stu-id="34f19-122">-ProfileName</span></span>
<span data-ttu-id="34f19-123">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="34f19-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="34f19-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34f19-124">-ResourceGroupName</span></span>
<span data-ttu-id="34f19-125">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="34f19-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="34f19-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34f19-126">-Confirm</span></span>
<span data-ttu-id="34f19-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34f19-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34f19-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34f19-128">-WhatIf</span></span>
<span data-ttu-id="34f19-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34f19-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34f19-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="34f19-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34f19-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f19-131">CommonParameters</span></span>
<span data-ttu-id="34f19-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34f19-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f19-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34f19-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f19-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34f19-134">INPUTS</span></span>

### <span data-ttu-id="34f19-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="34f19-135">PSEndpoint</span></span>
<span data-ttu-id="34f19-136">Parametr "CdnEndpoint" akceptuje wartość typu "PSEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="34f19-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="34f19-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34f19-137">OUTPUTS</span></span>

### <span data-ttu-id="34f19-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34f19-138">System.Boolean</span></span>

## <span data-ttu-id="34f19-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34f19-139">NOTES</span></span>

## <span data-ttu-id="34f19-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34f19-140">RELATED LINKS</span></span>

[<span data-ttu-id="34f19-141">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="34f19-141">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="34f19-142">Nowe — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="34f19-142">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="34f19-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="34f19-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="34f19-144">Start — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="34f19-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="34f19-145">Zatrzymaj — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="34f19-145">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


