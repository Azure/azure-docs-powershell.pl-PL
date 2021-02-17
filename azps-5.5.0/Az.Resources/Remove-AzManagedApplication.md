---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 17a28da26aa26860b7fd4a28ec922932bb089da3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186370"
---
# <span data-ttu-id="3a217-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="3a217-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="3a217-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a217-102">SYNOPSIS</span></span>
<span data-ttu-id="3a217-103">Usuwa aplikację zarządzaną</span><span class="sxs-lookup"><span data-stu-id="3a217-103">Removes a managed application</span></span>

## <span data-ttu-id="3a217-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3a217-104">SYNTAX</span></span>

### <span data-ttu-id="3a217-105">RemoveByNameAndResourceGroup (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="3a217-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a217-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="3a217-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a217-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3a217-107">DESCRIPTION</span></span>
<span data-ttu-id="3a217-108">Polecenie **cmdlet Remove-AzManagedApplication** usuwa aplikację zarządzaną</span><span class="sxs-lookup"><span data-stu-id="3a217-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="3a217-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3a217-109">EXAMPLES</span></span>

### <span data-ttu-id="3a217-110">Przykład 1. Usuwanie aplikacji zarządzanej według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="3a217-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="3a217-111">Pierwsze polecenie otrzymuje aplikację zarządzaną o nazwie myApp przy użyciu Get-AzManagedApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a217-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="3a217-112">Polecenie przechowuje je w $Application zmienną.</span><span class="sxs-lookup"><span data-stu-id="3a217-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="3a217-113">Drugie polecenie usuwa aplikację zarządzaną identyfikowaną przez właściwość **ResourceId** $Application.</span><span class="sxs-lookup"><span data-stu-id="3a217-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="3a217-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a217-114">PARAMETERS</span></span>

### <span data-ttu-id="3a217-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3a217-115">-ApiVersion</span></span>
<span data-ttu-id="3a217-116">Po jego skonfigurowaniu wskazuje wersję interfejsu API dostawcy zasobów, która ma być dostępna.</span><span class="sxs-lookup"><span data-stu-id="3a217-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3a217-117">Jeśli nie zostanie określona, wersja interfejsu API jest automatycznie określana jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="3a217-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3a217-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a217-118">-DefaultProfile</span></span>
<span data-ttu-id="3a217-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a217-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a217-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3a217-120">-Force</span></span>
<span data-ttu-id="3a217-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3a217-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3a217-122">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="3a217-122">-Id</span></span>
<span data-ttu-id="3a217-123">W pełni kwalifikowany identyfikator aplikacji zarządzanej, łącznie z subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="3a217-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="3a217-124">np. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="3a217-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a217-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3a217-125">-Name</span></span>
<span data-ttu-id="3a217-126">Nazwa aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="3a217-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a217-127">— Przed</span><span class="sxs-lookup"><span data-stu-id="3a217-127">-Pre</span></span>
<span data-ttu-id="3a217-128">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="3a217-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3a217-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a217-129">-ResourceGroupName</span></span>
<span data-ttu-id="3a217-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a217-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a217-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a217-131">-Confirm</span></span>
<span data-ttu-id="3a217-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3a217-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a217-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a217-133">-WhatIf</span></span>
<span data-ttu-id="3a217-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a217-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a217-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3a217-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a217-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a217-136">CommonParameters</span></span>
<span data-ttu-id="3a217-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a217-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a217-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a217-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a217-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a217-139">INPUTS</span></span>

### <span data-ttu-id="3a217-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3a217-140">System.String</span></span>

## <span data-ttu-id="3a217-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a217-141">OUTPUTS</span></span>

### <span data-ttu-id="3a217-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a217-142">System.Boolean</span></span>

## <span data-ttu-id="3a217-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3a217-143">NOTES</span></span>

## <span data-ttu-id="3a217-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a217-144">RELATED LINKS</span></span>
