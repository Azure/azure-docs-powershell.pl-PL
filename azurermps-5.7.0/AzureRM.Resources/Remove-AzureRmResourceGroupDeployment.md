---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: ce1d614050f9b70bfe4ed2ff4d242f1a6f38c55f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547995"
---
# <span data-ttu-id="c3e1f-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c3e1f-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="c3e1f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e1f-103">Usuwa wdrożenie grupy zasobów i wszystkie skojarzone z nią operacje.</span><span class="sxs-lookup"><span data-stu-id="c3e1f-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3e1f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3e1f-104">SYNTAX</span></span>

### <span data-ttu-id="c3e1f-105">RemoveByResourceGroupName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c3e1f-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3e1f-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c3e1f-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3e1f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c3e1f-107">DESCRIPTION</span></span>
<span data-ttu-id="c3e1f-108">Polecenie cmdlet **Remove-AzureRmResourceGroupDeployment** umożliwia usunięcie wdrożenia grupy zasobów platformy Azure oraz wszystkich skojarzonych operacji.</span><span class="sxs-lookup"><span data-stu-id="c3e1f-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="c3e1f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3e1f-109">EXAMPLES</span></span>

## <span data-ttu-id="c3e1f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3e1f-110">PARAMETERS</span></span>

### <span data-ttu-id="c3e1f-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c3e1f-111">-ApiVersion</span></span>
<span data-ttu-id="c3e1f-112">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="c3e1f-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="c3e1f-113">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="c3e1f-113">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e1f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e1f-114">-DefaultProfile</span></span>
<span data-ttu-id="c3e1f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c3e1f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3e1f-116">-ID</span><span class="sxs-lookup"><span data-stu-id="c3e1f-116">-Id</span></span>
<span data-ttu-id="c3e1f-117">Określa identyfikator wdrożenia grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c3e1f-117">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e1f-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c3e1f-118">-Name</span></span>
<span data-ttu-id="c3e1f-119">Określa nazwę wdrożenia grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c3e1f-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e1f-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="c3e1f-120">-Pre</span></span>
<span data-ttu-id="c3e1f-121">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="c3e1f-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c3e1f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e1f-122">-ResourceGroupName</span></span>
<span data-ttu-id="c3e1f-123">Określa nazwę grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c3e1f-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e1f-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c3e1f-124">-Confirm</span></span>
<span data-ttu-id="c3e1f-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3e1f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3e1f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3e1f-126">-WhatIf</span></span>
<span data-ttu-id="c3e1f-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3e1f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3e1f-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c3e1f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3e1f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e1f-129">CommonParameters</span></span>
<span data-ttu-id="c3e1f-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e1f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e1f-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e1f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e1f-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3e1f-132">INPUTS</span></span>

### <span data-ttu-id="c3e1f-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c3e1f-133">None</span></span>
<span data-ttu-id="c3e1f-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c3e1f-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c3e1f-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3e1f-135">OUTPUTS</span></span>

### <span data-ttu-id="c3e1f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e1f-136">System.Boolean</span></span>

## <span data-ttu-id="c3e1f-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3e1f-137">NOTES</span></span>

## <span data-ttu-id="c3e1f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3e1f-138">RELATED LINKS</span></span>

[<span data-ttu-id="c3e1f-139">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c3e1f-139">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="c3e1f-140">Nowe — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c3e1f-140">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="c3e1f-141">Zatrzymaj — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c3e1f-141">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="c3e1f-142">Test — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c3e1f-142">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


