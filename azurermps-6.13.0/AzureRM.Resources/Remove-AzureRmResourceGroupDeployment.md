---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 19662972e115acb0e3a194e14abf3f956d39035e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543483"
---
# <span data-ttu-id="26eed-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26eed-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="26eed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26eed-102">SYNOPSIS</span></span>
<span data-ttu-id="26eed-103">Usuwa wdrożenie grupy zasobów i wszystkie skojarzone z nią operacje.</span><span class="sxs-lookup"><span data-stu-id="26eed-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26eed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26eed-104">SYNTAX</span></span>

### <span data-ttu-id="26eed-105">RemoveByResourceGroupName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="26eed-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26eed-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="26eed-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26eed-107">Opis</span><span class="sxs-lookup"><span data-stu-id="26eed-107">DESCRIPTION</span></span>
<span data-ttu-id="26eed-108">Polecenie cmdlet **Remove-AzureRmResourceGroupDeployment** umożliwia usunięcie wdrożenia grupy zasobów platformy Azure oraz wszystkich skojarzonych operacji.</span><span class="sxs-lookup"><span data-stu-id="26eed-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="26eed-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26eed-109">EXAMPLES</span></span>

## <span data-ttu-id="26eed-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26eed-110">PARAMETERS</span></span>

### <span data-ttu-id="26eed-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="26eed-111">-ApiVersion</span></span>
<span data-ttu-id="26eed-112">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="26eed-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="26eed-113">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="26eed-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26eed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26eed-114">-DefaultProfile</span></span>
<span data-ttu-id="26eed-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="26eed-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26eed-116">-ID</span><span class="sxs-lookup"><span data-stu-id="26eed-116">-Id</span></span>
<span data-ttu-id="26eed-117">Określa identyfikator wdrożenia grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="26eed-117">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26eed-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26eed-118">-Name</span></span>
<span data-ttu-id="26eed-119">Określa nazwę wdrożenia grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="26eed-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26eed-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="26eed-120">-Pre</span></span>
<span data-ttu-id="26eed-121">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="26eed-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="26eed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26eed-122">-ResourceGroupName</span></span>
<span data-ttu-id="26eed-123">Określa nazwę grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="26eed-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26eed-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26eed-124">-Confirm</span></span>
<span data-ttu-id="26eed-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26eed-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26eed-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26eed-126">-WhatIf</span></span>
<span data-ttu-id="26eed-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26eed-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26eed-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26eed-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26eed-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26eed-129">CommonParameters</span></span>
<span data-ttu-id="26eed-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26eed-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26eed-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26eed-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26eed-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26eed-132">INPUTS</span></span>

### <span data-ttu-id="26eed-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="26eed-133">None</span></span>

## <span data-ttu-id="26eed-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26eed-134">OUTPUTS</span></span>

## <span data-ttu-id="26eed-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26eed-135">NOTES</span></span>

## <span data-ttu-id="26eed-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26eed-136">RELATED LINKS</span></span>

[<span data-ttu-id="26eed-137">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26eed-137">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="26eed-138">Nowe — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26eed-138">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="26eed-139">Zatrzymaj — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26eed-139">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="26eed-140">Test — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26eed-140">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


