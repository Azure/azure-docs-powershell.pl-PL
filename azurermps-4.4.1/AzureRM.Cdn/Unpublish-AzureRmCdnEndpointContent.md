---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: a774aec8114883d3ba2a5edf189f115f99d3eb4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546991"
---
# <span data-ttu-id="3b103-101">Unpublish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="3b103-101">Unpublish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="3b103-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b103-102">SYNOPSIS</span></span>
<span data-ttu-id="3b103-103">Przeczyszcza punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="3b103-103">Purges a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b103-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b103-104">SYNTAX</span></span>

### <span data-ttu-id="3b103-105">Parametr ustawiony dla parametrów pól (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3b103-105">Parameter Set for fields parameters (Default)</span></span>
```
Unpublish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b103-106">Zestaw parametrów dla parametrów obiektu</span><span class="sxs-lookup"><span data-stu-id="3b103-106">Parameter Set for object parameters</span></span>
```
Unpublish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b103-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3b103-107">DESCRIPTION</span></span>
<span data-ttu-id="3b103-108">Polecenie cmdlet **cofnięcia publikowania — AzureRmCdnEndpointContent** Przeczyszcza zawartość z punktu końcowego sieci dostarczania zawartości Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="3b103-108">The **Unpublish-AzureRmCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="3b103-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b103-109">EXAMPLES</span></span>

## <span data-ttu-id="3b103-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b103-110">PARAMETERS</span></span>

### <span data-ttu-id="3b103-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b103-111">-CdnEndpoint</span></span>
<span data-ttu-id="3b103-112">Określa punkt końcowy, który to polecenie cmdlet Przeczyszcza.</span><span class="sxs-lookup"><span data-stu-id="3b103-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="3b103-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3b103-113">-EndpointName</span></span>
<span data-ttu-id="3b103-114">Określa nazwę punktu końcowego, który jest czyszczony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b103-114">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="3b103-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b103-115">-PassThru</span></span>
<span data-ttu-id="3b103-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="3b103-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3b103-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3b103-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3b103-118">-Refilename</span><span class="sxs-lookup"><span data-stu-id="3b103-118">-ProfileName</span></span>
<span data-ttu-id="3b103-119">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="3b103-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="3b103-120">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="3b103-120">-PurgeContent</span></span>
<span data-ttu-id="3b103-121">Określa tablicę względnych ścieżek dla zawartości na serwerze pochodzenia, którą to polecenie cmdlet Przeczyszcza.</span><span class="sxs-lookup"><span data-stu-id="3b103-121">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b103-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b103-122">-ResourceGroupName</span></span>
<span data-ttu-id="3b103-123">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="3b103-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="3b103-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b103-124">-Confirm</span></span>
<span data-ttu-id="3b103-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b103-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b103-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b103-126">-WhatIf</span></span>
<span data-ttu-id="3b103-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b103-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b103-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3b103-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b103-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b103-129">-DefaultProfile</span></span>
<span data-ttu-id="3b103-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b103-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b103-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b103-131">CommonParameters</span></span>
<span data-ttu-id="3b103-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b103-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b103-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b103-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b103-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b103-134">INPUTS</span></span>

### <span data-ttu-id="3b103-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b103-135">PSEndpoint</span></span>
<span data-ttu-id="3b103-136">Parametr "CdnEndpoint" akceptuje wartość typu "PSEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="3b103-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="3b103-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b103-137">OUTPUTS</span></span>

### <span data-ttu-id="3b103-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b103-138">System.Boolean</span></span>

## <span data-ttu-id="3b103-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b103-139">NOTES</span></span>

## <span data-ttu-id="3b103-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b103-140">RELATED LINKS</span></span>

[<span data-ttu-id="3b103-141">Publikowanie — AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="3b103-141">Publish-AzureRmCdnEndpointContent</span></span>](./Publish-AzureRmCdnEndpointContent.md)


