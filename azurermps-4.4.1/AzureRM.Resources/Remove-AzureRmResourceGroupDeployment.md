---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 84aa6f50d02f4c85de674c163565a205f2b83750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549867"
---
# <span data-ttu-id="d4c0d-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d4c0d-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="d4c0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4c0d-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c0d-103">Usuwa wdrożenie grupy zasobów i wszystkie skojarzone z nią operacje.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4c0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4c0d-104">SYNTAX</span></span>

### <span data-ttu-id="d4c0d-105">Zestaw parametrów nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-105">The deployment name parameter set.</span></span> <span data-ttu-id="d4c0d-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="d4c0d-106">(Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4c0d-107">Zestaw parametrów identyfikator wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-107">The deployment Id parameter set.</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4c0d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d4c0d-108">DESCRIPTION</span></span>
<span data-ttu-id="d4c0d-109">Polecenie cmdlet **Remove-AzureRmResourceGroupDeployment** umożliwia usunięcie wdrożenia grupy zasobów platformy Azure oraz wszystkich skojarzonych operacji.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-109">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="d4c0d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4c0d-110">EXAMPLES</span></span>

## <span data-ttu-id="d4c0d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4c0d-111">PARAMETERS</span></span>

### <span data-ttu-id="d4c0d-112">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d4c0d-112">-ApiVersion</span></span>
<span data-ttu-id="d4c0d-113">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-113">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d4c0d-114">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-114">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="d4c0d-115">-ID</span><span class="sxs-lookup"><span data-stu-id="d4c0d-115">-Id</span></span>
<span data-ttu-id="d4c0d-116">Określa identyfikator wdrożenia grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-116">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c0d-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d4c0d-117">-Name</span></span>
<span data-ttu-id="d4c0d-118">Określa nazwę wdrożenia grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-118">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4c0d-119">-Pre</span><span class="sxs-lookup"><span data-stu-id="d4c0d-119">-Pre</span></span>
<span data-ttu-id="d4c0d-120">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-120">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d4c0d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4c0d-121">-ResourceGroupName</span></span>
<span data-ttu-id="d4c0d-122">Określa nazwę grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-122">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4c0d-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4c0d-123">-Confirm</span></span>
<span data-ttu-id="d4c0d-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4c0d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4c0d-125">-WhatIf</span></span>
<span data-ttu-id="d4c0d-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4c0d-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4c0d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c0d-128">-DefaultProfile</span></span>
<span data-ttu-id="d4c0d-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4c0d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c0d-130">CommonParameters</span></span>
<span data-ttu-id="d4c0d-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4c0d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c0d-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4c0d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c0d-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4c0d-133">INPUTS</span></span>

## <span data-ttu-id="d4c0d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4c0d-134">OUTPUTS</span></span>

### <span data-ttu-id="d4c0d-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4c0d-135">System.Boolean</span></span>

## <span data-ttu-id="d4c0d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4c0d-136">NOTES</span></span>

## <span data-ttu-id="d4c0d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4c0d-137">RELATED LINKS</span></span>

[<span data-ttu-id="d4c0d-138">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d4c0d-138">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d4c0d-139">Nowe — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d4c0d-139">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d4c0d-140">Zatrzymaj — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d4c0d-140">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d4c0d-141">Test — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d4c0d-141">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


