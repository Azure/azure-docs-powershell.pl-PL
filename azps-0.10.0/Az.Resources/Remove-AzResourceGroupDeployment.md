---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: da66d0cacbddbeb53972308faa681bde42c813d2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892385"
---
# <span data-ttu-id="add23-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="add23-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="add23-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="add23-102">SYNOPSIS</span></span>
<span data-ttu-id="add23-103">Usuwa wdrożenie grupy zasobów i wszystkie skojarzone z nią operacje.</span><span class="sxs-lookup"><span data-stu-id="add23-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="add23-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="add23-104">SYNTAX</span></span>

### <span data-ttu-id="add23-105">RemoveByResourceGroupName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="add23-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="add23-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="add23-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="add23-107">Opis</span><span class="sxs-lookup"><span data-stu-id="add23-107">DESCRIPTION</span></span>
<span data-ttu-id="add23-108">Polecenie cmdlet **Remove-AzResourceGroupDeployment** umożliwia usunięcie wdrożenia grupy zasobów platformy Azure oraz wszystkich skojarzonych operacji.</span><span class="sxs-lookup"><span data-stu-id="add23-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="add23-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="add23-109">EXAMPLES</span></span>

## <span data-ttu-id="add23-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="add23-110">PARAMETERS</span></span>

### <span data-ttu-id="add23-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="add23-111">-ApiVersion</span></span>
<span data-ttu-id="add23-112">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="add23-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="add23-113">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="add23-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="add23-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add23-114">-DefaultProfile</span></span>
<span data-ttu-id="add23-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="add23-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add23-116">-ID</span><span class="sxs-lookup"><span data-stu-id="add23-116">-Id</span></span>
<span data-ttu-id="add23-117">Określa identyfikator wdrożenia grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="add23-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="add23-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="add23-118">-Name</span></span>
<span data-ttu-id="add23-119">Określa nazwę wdrożenia grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="add23-119">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="add23-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="add23-120">-Pre</span></span>
<span data-ttu-id="add23-121">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="add23-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="add23-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add23-122">-ResourceGroupName</span></span>
<span data-ttu-id="add23-123">Określa nazwę grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="add23-123">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="add23-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="add23-124">-Confirm</span></span>
<span data-ttu-id="add23-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="add23-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="add23-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="add23-126">-WhatIf</span></span>
<span data-ttu-id="add23-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="add23-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="add23-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="add23-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="add23-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add23-129">CommonParameters</span></span>
<span data-ttu-id="add23-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add23-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add23-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="add23-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add23-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="add23-132">INPUTS</span></span>

### <span data-ttu-id="add23-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="add23-133">None</span></span>

## <span data-ttu-id="add23-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="add23-134">OUTPUTS</span></span>

## <span data-ttu-id="add23-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="add23-135">NOTES</span></span>

## <span data-ttu-id="add23-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="add23-136">RELATED LINKS</span></span>

[<span data-ttu-id="add23-137">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="add23-137">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="add23-138">Nowe — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="add23-138">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="add23-139">Zatrzymaj — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="add23-139">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="add23-140">Test — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="add23-140">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


