---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 88d89e819d97a42a797be81e5cb0b4b401401108
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186354"
---
# <span data-ttu-id="60215-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="60215-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="60215-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60215-102">SYNOPSIS</span></span>
<span data-ttu-id="60215-103">Usuwa zarządzaną definicję aplikacji</span><span class="sxs-lookup"><span data-stu-id="60215-103">Removes a managed application definition</span></span>

## <span data-ttu-id="60215-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="60215-104">SYNTAX</span></span>

### <span data-ttu-id="60215-105">RemoveByNameAndResourceGroup (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="60215-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60215-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="60215-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60215-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="60215-107">DESCRIPTION</span></span>
<span data-ttu-id="60215-108">Polecenie **cmdlet Remove-AzManagedApplicationDefinition** usuwa definicję aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="60215-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="60215-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="60215-109">EXAMPLES</span></span>

### <span data-ttu-id="60215-110">Przykład 1. Usuwanie definicji aplikacji zarządzanej według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="60215-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="60215-111">Pierwsze polecenie otrzymuje zarządzaną definicję aplikacji o nazwie myAppDef przy użyciu Get-AzManagedApplicationDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60215-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="60215-112">Polecenie przechowuje je w $ApplicationDefinition zmienną.</span><span class="sxs-lookup"><span data-stu-id="60215-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="60215-113">Drugie polecenie usuwa definicję aplikacji zarządzanej zidentyfikowanych przez właściwość **ResourceId** $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="60215-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="60215-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60215-114">PARAMETERS</span></span>

### <span data-ttu-id="60215-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="60215-115">-ApiVersion</span></span>
<span data-ttu-id="60215-116">Po jego skonfigurowaniu wskazuje wersję interfejsu API dostawcy zasobów, która ma być dostępna.</span><span class="sxs-lookup"><span data-stu-id="60215-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="60215-117">Jeśli nie zostanie określona, wersja interfejsu API jest automatycznie określana jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="60215-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="60215-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60215-118">-DefaultProfile</span></span>
<span data-ttu-id="60215-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="60215-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60215-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="60215-120">-Force</span></span>
<span data-ttu-id="60215-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="60215-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="60215-122">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="60215-122">-Id</span></span>
<span data-ttu-id="60215-123">W pełni kwalifikowany identyfikator definicji aplikacji zarządzanej, łącznie z subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="60215-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="60215-124">np. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="60215-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="60215-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="60215-125">-Name</span></span>
<span data-ttu-id="60215-126">Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="60215-126">The managed application definition name.</span></span>

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

### <span data-ttu-id="60215-127">— Przed</span><span class="sxs-lookup"><span data-stu-id="60215-127">-Pre</span></span>
<span data-ttu-id="60215-128">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="60215-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="60215-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60215-129">-ResourceGroupName</span></span>
<span data-ttu-id="60215-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="60215-130">The resource group name.</span></span>

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

### <span data-ttu-id="60215-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="60215-131">-Confirm</span></span>
<span data-ttu-id="60215-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="60215-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60215-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60215-133">-WhatIf</span></span>
<span data-ttu-id="60215-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60215-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60215-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="60215-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60215-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60215-136">CommonParameters</span></span>
<span data-ttu-id="60215-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60215-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60215-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60215-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60215-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60215-139">INPUTS</span></span>

### <span data-ttu-id="60215-140">System.String</span><span class="sxs-lookup"><span data-stu-id="60215-140">System.String</span></span>

## <span data-ttu-id="60215-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60215-141">OUTPUTS</span></span>

### <span data-ttu-id="60215-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="60215-142">System.Boolean</span></span>

## <span data-ttu-id="60215-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="60215-143">NOTES</span></span>

## <span data-ttu-id="60215-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60215-144">RELATED LINKS</span></span>
