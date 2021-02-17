---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: 9c4bdfe189c16f3e2f6f90d3197149bdc57c78c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192730"
---
# <span data-ttu-id="567dd-101">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="567dd-101">New-AzResourceGroup</span></span>

## <span data-ttu-id="567dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="567dd-102">SYNOPSIS</span></span>
<span data-ttu-id="567dd-103">Tworzy grupę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="567dd-103">Creates an Azure resource group.</span></span>

## <span data-ttu-id="567dd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="567dd-104">SYNTAX</span></span>

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="567dd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="567dd-105">DESCRIPTION</span></span>
<span data-ttu-id="567dd-106">Polecenie **cmdlet New-AzResourceGroup** tworzy grupę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="567dd-106">The **New-AzResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="567dd-107">Grupę zasobów można utworzyć, używając tylko nazwy i lokalizacji, a następnie za pomocą polecenia cmdlet New-AzResource utworzyć zasoby w celu dodania ich do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="567dd-107">You can create a resource group by using just a name and location, and then use the New-AzResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="567dd-108">Aby dodać wdrożenie do istniejącej grupy zasobów, użyj New-AzResourceGroupDeployment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="567dd-108">To add a deployment to an existing resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="567dd-109">Aby dodać zasób do istniejącej grupy zasobów, użyj polecenia cmdlet **New-AzResource.**</span><span class="sxs-lookup"><span data-stu-id="567dd-109">To add a resource to an existing resource group, use the **New-AzResource** cmdlet.</span></span> <span data-ttu-id="567dd-110">Zasób platformy Azure to jednostka platformy Azure zarządzana przez użytkownika, taka jak serwer bazy danych, baza danych lub witryna internetowa.</span><span class="sxs-lookup"><span data-stu-id="567dd-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="567dd-111">Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostka.</span><span class="sxs-lookup"><span data-stu-id="567dd-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="567dd-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="567dd-112">EXAMPLES</span></span>

### <span data-ttu-id="567dd-113">Przykład 1. Tworzenie pustej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="567dd-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="567dd-114">To polecenie tworzy grupę zasobów, która nie ma zasobów.</span><span class="sxs-lookup"><span data-stu-id="567dd-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="567dd-115">Aby dodać zasoby i wdrożenia do tej grupy zasobów, możesz użyć polecenia cmdlet **New-AzResource** lub **New-AzResourceGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="567dd-115">You can use the **New-AzResource** or **New-AzResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="567dd-116">Przykład 2. Tworzenie pustej grupy zasobów przy użyciu parametrów pozytowych</span><span class="sxs-lookup"><span data-stu-id="567dd-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzResourceGroup RG01 "South Central US"
```

<span data-ttu-id="567dd-117">To polecenie tworzy grupę zasobów, która nie ma zasobów.</span><span class="sxs-lookup"><span data-stu-id="567dd-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="567dd-118">Przykład 3. Tworzenie grupy zasobów z tagami</span><span class="sxs-lookup"><span data-stu-id="567dd-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="567dd-119">To polecenie tworzy pustą grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="567dd-119">This command creates an empty resource group.</span></span> <span data-ttu-id="567dd-120">To polecenie jest takie samo, jak polecenie w przykładzie 1, z tym wyjątkiem, że przypisuje tagi do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="567dd-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="567dd-121">Pierwszy tag o nazwie Pusty może być używany do identyfikowania grup zasobów, które nie mają zasobów.</span><span class="sxs-lookup"><span data-stu-id="567dd-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="567dd-122">Drugi tag nosi nazwę Dział i ma wartość Marketing.</span><span class="sxs-lookup"><span data-stu-id="567dd-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="567dd-123">Do kategoryzowania grup zasobów w celu administrowania lub budżetowania można użyć tagu takiego jak ten.</span><span class="sxs-lookup"><span data-stu-id="567dd-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="567dd-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="567dd-124">PARAMETERS</span></span>

### <span data-ttu-id="567dd-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="567dd-125">-ApiVersion</span></span>
<span data-ttu-id="567dd-126">Określa wersję interfejsu API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="567dd-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="567dd-127">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="567dd-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="567dd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="567dd-128">-DefaultProfile</span></span>
<span data-ttu-id="567dd-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="567dd-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="567dd-130">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="567dd-130">-Force</span></span>
<span data-ttu-id="567dd-131">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="567dd-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="567dd-132">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="567dd-132">-Location</span></span>
<span data-ttu-id="567dd-133">Określa lokalizację grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="567dd-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="567dd-134">Określ lokalizację centrum danych platformy Azure, taką jak Stany Zjednoczone i Azja Południowo-Wschodnia.</span><span class="sxs-lookup"><span data-stu-id="567dd-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="567dd-135">Grupę zasobów można umieścić w dowolnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="567dd-135">You can place a resource group in any location.</span></span> <span data-ttu-id="567dd-136">Grupa zasobów nie musi być w tej samej lokalizacji co subskrypcja platformy Azure ani w tej samej lokalizacji co jej zasoby.</span><span class="sxs-lookup"><span data-stu-id="567dd-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="567dd-137">Aby określić, która lokalizacja obsługuje poszczególne typy zasobów, użyj Get-AzResourceProvider cmdlet z parametrem *ProviderNamespace.*</span><span class="sxs-lookup"><span data-stu-id="567dd-137">To determine which location supports each resource type, use the Get-AzResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="567dd-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="567dd-138">-Name</span></span>
<span data-ttu-id="567dd-139">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="567dd-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="567dd-140">Nazwa zasobu musi być unikatowa w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="567dd-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="567dd-141">Jeśli grupa zasobów o tej nazwie już istnieje, polecenie wyświetli monit o potwierdzenie przed zastąpieniem istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="567dd-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="567dd-142">— Przed</span><span class="sxs-lookup"><span data-stu-id="567dd-142">-Pre</span></span>
<span data-ttu-id="567dd-143">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="567dd-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="567dd-144">— Tag</span><span class="sxs-lookup"><span data-stu-id="567dd-144">-Tag</span></span>
<span data-ttu-id="567dd-145">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="567dd-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="567dd-146">Na przykład: @{key0="value0";key1=$null;key2="wartość2"} Aby dodać lub zmienić tag, musisz zastąpić kolekcję tagów dla grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="567dd-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="567dd-147">Po przypisaniu tagów do zasobów i grup możesz użyć parametru *Tag* Get-AzResource i Get-AzResourceGroup, aby wyszukiwać zasoby i grupy według nazwy tagu lub według nazwy i wartości.</span><span class="sxs-lookup"><span data-stu-id="567dd-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="567dd-148">Za pomocą tagów można kategoryzować zasoby( na przykład według działu lub centrum kosztów) albo śledzić notatki lub komentarze dotyczące zasobów.</span><span class="sxs-lookup"><span data-stu-id="567dd-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="567dd-149">Aby uzyskać wstępnie zdefiniowane tagi, użyj Get-AzTag cmdlet.</span><span class="sxs-lookup"><span data-stu-id="567dd-149">To get your predefined tags, use the Get-AzTag cmdlet.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="567dd-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="567dd-150">-Confirm</span></span>
<span data-ttu-id="567dd-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="567dd-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="567dd-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="567dd-152">-WhatIf</span></span>
<span data-ttu-id="567dd-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="567dd-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="567dd-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="567dd-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="567dd-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="567dd-155">CommonParameters</span></span>
<span data-ttu-id="567dd-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="567dd-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="567dd-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="567dd-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="567dd-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="567dd-158">INPUTS</span></span>

### <span data-ttu-id="567dd-159">System.String</span><span class="sxs-lookup"><span data-stu-id="567dd-159">System.String</span></span>

### <span data-ttu-id="567dd-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="567dd-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="567dd-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="567dd-161">OUTPUTS</span></span>

### <span data-ttu-id="567dd-162">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="567dd-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="567dd-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="567dd-163">NOTES</span></span>

## <span data-ttu-id="567dd-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="567dd-164">RELATED LINKS</span></span>

[<span data-ttu-id="567dd-165">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="567dd-165">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="567dd-166">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="567dd-166">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="567dd-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="567dd-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="567dd-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="567dd-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="567dd-169">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="567dd-169">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="567dd-170">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="567dd-170">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)
