---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502616"
---
# <span data-ttu-id="ed04e-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="ed04e-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="ed04e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed04e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed04e-103">Usuwa specyfikację szablonu</span><span class="sxs-lookup"><span data-stu-id="ed04e-103">Removes a Template Spec</span></span>

## <span data-ttu-id="ed04e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed04e-104">SYNTAX</span></span>

### <span data-ttu-id="ed04e-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ed04e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed04e-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed04e-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed04e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ed04e-107">DESCRIPTION</span></span>
<span data-ttu-id="ed04e-108">Usuwa określoną specyfikację szablonu. Jeśli jest podany parametr Version **-Version** , zostanie usunięta tylko określona wersja.</span><span class="sxs-lookup"><span data-stu-id="ed04e-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="ed04e-109">Jeśli nie zostanie podana określona wersja, Specyfikacja szablonu i wszystkie jej wersje zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="ed04e-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="ed04e-110">Jeśli jest dostępna flaga **-Force** , nie zostanie wyświetlony monit o potwierdzenie usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ed04e-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="ed04e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed04e-111">EXAMPLES</span></span>

### <span data-ttu-id="ed04e-112">Przykład 1: usuwanie określonej wersji według nazwy</span><span class="sxs-lookup"><span data-stu-id="ed04e-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="ed04e-113">Usuwa wersję "v 1.0" specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="ed04e-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="ed04e-114">Przykład 2: usuwanie określonej wersji według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="ed04e-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="ed04e-115">Usuwa wersję "v 1.0" specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG" subskrypcji \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="ed04e-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="ed04e-116">Przykład 3: usuwanie specyfikacji szablonu i wszystkich wersji według nazwy</span><span class="sxs-lookup"><span data-stu-id="ed04e-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="ed04e-117">Usuwa specyfikację szablonu o nazwie "MyTemplateSpec" i wszystkie jej wersje w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="ed04e-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="ed04e-118">Przykład 3: usuwanie specyfikacji szablonu i wszystkich wersji według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="ed04e-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="ed04e-119">Usuwa specyfikację szablonu o nazwie "MyTemplateSpec" i wszystkie jej wersje w grupie zasobów "myRG" subskrypcji \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="ed04e-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="ed04e-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed04e-120">PARAMETERS</span></span>

### <span data-ttu-id="ed04e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed04e-121">-DefaultProfile</span></span>
<span data-ttu-id="ed04e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed04e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed04e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ed04e-123">-Force</span></span>
<span data-ttu-id="ed04e-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ed04e-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ed04e-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ed04e-125">-Name</span></span>
<span data-ttu-id="ed04e-126">Nazwa specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="ed04e-126">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed04e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed04e-127">-ResourceGroupName</span></span>
<span data-ttu-id="ed04e-128">Nazwa grupy zasobów specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="ed04e-128">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed04e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed04e-129">-ResourceId</span></span>
<span data-ttu-id="ed04e-130">W pełni kwalifikowany identyfikator zasobu specyfikacji szablonu. przykład:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="ed04e-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed04e-131">-Version</span><span class="sxs-lookup"><span data-stu-id="ed04e-131">-Version</span></span>
<span data-ttu-id="ed04e-132">Wersja specyfikacji szablonu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ed04e-132">The version of the template spec to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed04e-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ed04e-133">-Confirm</span></span>
<span data-ttu-id="ed04e-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed04e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed04e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed04e-135">-WhatIf</span></span>
<span data-ttu-id="ed04e-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed04e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed04e-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ed04e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed04e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed04e-138">CommonParameters</span></span>
<span data-ttu-id="ed04e-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed04e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed04e-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed04e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed04e-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed04e-141">INPUTS</span></span>

### <span data-ttu-id="ed04e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ed04e-142">System.String</span></span>

## <span data-ttu-id="ed04e-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed04e-143">OUTPUTS</span></span>

### <span data-ttu-id="ed04e-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed04e-144">System.Boolean</span></span>

## <span data-ttu-id="ed04e-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed04e-145">NOTES</span></span>

## <span data-ttu-id="ed04e-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed04e-146">RELATED LINKS</span></span>
