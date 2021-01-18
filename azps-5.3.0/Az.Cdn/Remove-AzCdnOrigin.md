---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
ms.openlocfilehash: 8198d189d9619528bdc7fb80d30285ce9126dfed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502004"
---
# <span data-ttu-id="2dd10-101">Remove-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="2dd10-101">Remove-AzCdnOrigin</span></span>

## <span data-ttu-id="2dd10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2dd10-102">SYNOPSIS</span></span>
<span data-ttu-id="2dd10-103">Usuwa źródło sieci CDN</span><span class="sxs-lookup"><span data-stu-id="2dd10-103">Removes a CDN origin</span></span>

## <span data-ttu-id="2dd10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2dd10-104">SYNTAX</span></span>

### <span data-ttu-id="2dd10-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2dd10-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOrigin -OriginName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2dd10-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dd10-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOrigin -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dd10-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dd10-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOrigin [-PassThru] -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dd10-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2dd10-108">DESCRIPTION</span></span>
<span data-ttu-id="2dd10-109">Remove-AzCdnOrigin usunie początek sieci CDN z danego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="2dd10-109">Remove-AzCdnOrigin will delete a CDN origin from the given endpoint.</span></span> <span data-ttu-id="2dd10-110">Jeśli pochodzenie jest jedynym źródłem w określonym punkcie końcowym, operacja usunięcia zakończy się niepowodzeniem, ponieważ co najmniej 1 Początek jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="2dd10-110">If the origin is the only origin within the specified endpoint, then the deletion will fail since at least 1 origin is needed.</span></span> 

## <span data-ttu-id="2dd10-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2dd10-111">EXAMPLES</span></span>

### <span data-ttu-id="2dd10-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2dd10-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName 
```
<span data-ttu-id="2dd10-113">To polecenie cmdlet spowoduje usunięcie określonego pochodzenia z danego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="2dd10-113">This cmdlet will remove the specified origin from the given endpoint.</span></span> 

## <span data-ttu-id="2dd10-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2dd10-114">PARAMETERS</span></span>

### <span data-ttu-id="2dd10-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="2dd10-115">-CdnOrigin</span></span>
<span data-ttu-id="2dd10-116">Obiekt pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="2dd10-116">The CDN origin object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd10-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dd10-117">-DefaultProfile</span></span>
<span data-ttu-id="2dd10-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2dd10-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dd10-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2dd10-119">-EndpointName</span></span>
<span data-ttu-id="2dd10-120">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2dd10-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="2dd10-121">-Originname</span><span class="sxs-lookup"><span data-stu-id="2dd10-121">-OriginName</span></span>
<span data-ttu-id="2dd10-122">Nazwa pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2dd10-122">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="2dd10-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2dd10-123">-PassThru</span></span>
<span data-ttu-id="2dd10-124">Zwraca obiekt, jeśli jest określony.</span><span class="sxs-lookup"><span data-stu-id="2dd10-124">Return object if specified.</span></span>

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

### <span data-ttu-id="2dd10-125">-Refilename</span><span class="sxs-lookup"><span data-stu-id="2dd10-125">-ProfileName</span></span>
<span data-ttu-id="2dd10-126">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2dd10-126">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="2dd10-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dd10-127">-ResourceGroupName</span></span>
<span data-ttu-id="2dd10-128">Grupa zasobów profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2dd10-128">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="2dd10-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2dd10-129">-ResourceId</span></span>
<span data-ttu-id="2dd10-130">Identyfikator zasobu pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2dd10-130">The resource id of the Azure CDN origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd10-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2dd10-131">-Confirm</span></span>
<span data-ttu-id="2dd10-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dd10-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd10-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dd10-133">-WhatIf</span></span>
<span data-ttu-id="2dd10-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dd10-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dd10-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2dd10-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd10-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dd10-136">CommonParameters</span></span>
<span data-ttu-id="2dd10-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dd10-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dd10-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dd10-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dd10-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dd10-139">INPUTS</span></span>

### <span data-ttu-id="2dd10-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2dd10-140">None</span></span>

## <span data-ttu-id="2dd10-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2dd10-141">OUTPUTS</span></span>

### <span data-ttu-id="2dd10-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2dd10-142">System.Boolean</span></span>

## <span data-ttu-id="2dd10-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2dd10-143">NOTES</span></span>

## <span data-ttu-id="2dd10-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2dd10-144">RELATED LINKS</span></span>
