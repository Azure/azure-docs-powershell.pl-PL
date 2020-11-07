---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: f61fda6c67f0abdee1c136ec6a5fee8b31952d81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708343"
---
# <span data-ttu-id="87809-101">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="87809-101">New-AzResourceGroup</span></span>

## <span data-ttu-id="87809-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87809-102">SYNOPSIS</span></span>
<span data-ttu-id="87809-103">Tworzy grupę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="87809-103">Creates an Azure resource group.</span></span>

## <span data-ttu-id="87809-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87809-104">SYNTAX</span></span>

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87809-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87809-105">DESCRIPTION</span></span>
<span data-ttu-id="87809-106">Polecenie cmdlet **New-AzResourceGroup** tworzy grupę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="87809-106">The **New-AzResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="87809-107">Grupę zasobów można utworzyć za pomocą samej nazwy i lokalizacji, a następnie za pomocą polecenia cmdlet New-AzResource utworzyć zasoby, które mają zostać dodane do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87809-107">You can create a resource group by using just a name and location, and then use the New-AzResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="87809-108">Aby dodać wdrożenie do istniejącej grupy zasobów, użyj polecenia cmdlet New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="87809-108">To add a deployment to an existing resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="87809-109">Aby dodać zasób do istniejącej grupy zasobów, użyj polecenia cmdlet **New-AzResource** .</span><span class="sxs-lookup"><span data-stu-id="87809-109">To add a resource to an existing resource group, use the **New-AzResource** cmdlet.</span></span> <span data-ttu-id="87809-110">Zasób platformy Azure jest zarządzaną przez użytkownika jednostką Azure, taką jak serwer bazy danych, baza danych lub witryna sieci Web.</span><span class="sxs-lookup"><span data-stu-id="87809-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="87809-111">Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostka.</span><span class="sxs-lookup"><span data-stu-id="87809-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="87809-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87809-112">EXAMPLES</span></span>

### <span data-ttu-id="87809-113">Przykład 1. Tworzenie pustej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="87809-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="87809-114">To polecenie tworzy grupę zasobów bez zasobów.</span><span class="sxs-lookup"><span data-stu-id="87809-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="87809-115">Za pomocą poleceń cmdlet **New-AzResource** lub **New-AzResourceGroupDeployment** można dodawać zasoby i wdrożenia do tej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87809-115">You can use the **New-AzResource** or **New-AzResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="87809-116">Przykład 2: Tworzenie pustej grupy zasobów przy użyciu parametrów pozycyjnych</span><span class="sxs-lookup"><span data-stu-id="87809-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzResourceGroup RG01 "South Central US"
```

<span data-ttu-id="87809-117">To polecenie tworzy grupę zasobów bez zasobów.</span><span class="sxs-lookup"><span data-stu-id="87809-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="87809-118">Przykład 3: Tworzenie grupy zasobów ze znacznikami</span><span class="sxs-lookup"><span data-stu-id="87809-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="87809-119">To polecenie tworzy pustą grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="87809-119">This command creates an empty resource group.</span></span> <span data-ttu-id="87809-120">To polecenie jest takie samo jak w przypadku polecenia z przykładu 1, z wyjątkiem tego, że przypisuje znaczniki do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87809-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="87809-121">Pierwszy znacznik o nazwie Empty może być wykorzystywany do identyfikowania grup zasobów, które nie mają zasobów.</span><span class="sxs-lookup"><span data-stu-id="87809-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="87809-122">Drugi znacznik ma nazwę dział i ma wartość marketingową.</span><span class="sxs-lookup"><span data-stu-id="87809-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="87809-123">Możesz użyć znacznika, takiego jak ten, aby przydzielić grupy zasobów do administrowania lub budżetowania.</span><span class="sxs-lookup"><span data-stu-id="87809-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="87809-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87809-124">PARAMETERS</span></span>

### <span data-ttu-id="87809-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="87809-125">-ApiVersion</span></span>
<span data-ttu-id="87809-126">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="87809-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="87809-127">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="87809-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="87809-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87809-128">-DefaultProfile</span></span>
<span data-ttu-id="87809-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="87809-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87809-130">-Force</span><span class="sxs-lookup"><span data-stu-id="87809-130">-Force</span></span>
<span data-ttu-id="87809-131">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="87809-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="87809-132">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="87809-132">-Location</span></span>
<span data-ttu-id="87809-133">Określa lokalizację grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87809-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="87809-134">Określ lokalizację centrum danych platformy Azure, na przykład Azja Zachodnia lub Południowo-Wschodnia.</span><span class="sxs-lookup"><span data-stu-id="87809-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="87809-135">Grupę zasobów można umieścić w dowolnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="87809-135">You can place a resource group in any location.</span></span> <span data-ttu-id="87809-136">Grupa zasobów nie musi znajdować się w tej samej lokalizacji w ramach subskrypcji platformy Azure ani w tej samej lokalizacji co zasoby.</span><span class="sxs-lookup"><span data-stu-id="87809-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="87809-137">Aby określić, która lokalizacja obsługuje poszczególne typy zasobów, użyj polecenia cmdlet Get-AzResourceProvider z parametrem *ProviderNamespace* .</span><span class="sxs-lookup"><span data-stu-id="87809-137">To determine which location supports each resource type, use the Get-AzResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

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

### <span data-ttu-id="87809-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87809-138">-Name</span></span>
<span data-ttu-id="87809-139">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87809-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="87809-140">Nazwa zasobu musi być unikatowa w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="87809-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="87809-141">Jeśli grupa zasobów o tej nazwie już istnieje, polecenie monituje o potwierdzenie przed zastąpieniem istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87809-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

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

### <span data-ttu-id="87809-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="87809-142">-Pre</span></span>
<span data-ttu-id="87809-143">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="87809-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="87809-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="87809-144">-Tag</span></span>
<span data-ttu-id="87809-145">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="87809-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="87809-146">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"} aby dodać lub zmienić znacznik, należy zamienić kolekcję znaczników dla grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87809-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="87809-147">Po przypisaniu znaczników do zasobów i grup można użyć parametru *znacznika* Get-AzResource i Get-AzResourceGroup do wyszukiwania zasobów i grup według nazwy znacznika lub według nazwy i wartości.</span><span class="sxs-lookup"><span data-stu-id="87809-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="87809-148">Za pomocą znaczników można klasyfikować zasoby, na przykład według działów lub MPK, a także śledzić notatki i komentarze dotyczące zasobów.</span><span class="sxs-lookup"><span data-stu-id="87809-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="87809-149">Aby uzyskać wstępnie zdefiniowane Tagi, użyj polecenia cmdlet Get-AzTag.</span><span class="sxs-lookup"><span data-stu-id="87809-149">To get your predefined tags, use the Get-AzTag cmdlet.</span></span>

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

### <span data-ttu-id="87809-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87809-150">-Confirm</span></span>
<span data-ttu-id="87809-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87809-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87809-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87809-152">-WhatIf</span></span>
<span data-ttu-id="87809-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87809-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87809-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="87809-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87809-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87809-155">CommonParameters</span></span>
<span data-ttu-id="87809-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87809-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87809-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87809-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87809-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87809-158">INPUTS</span></span>

### <span data-ttu-id="87809-159">System. String</span><span class="sxs-lookup"><span data-stu-id="87809-159">System.String</span></span>

### <span data-ttu-id="87809-160">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="87809-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="87809-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87809-161">OUTPUTS</span></span>

### <span data-ttu-id="87809-162">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="87809-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="87809-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87809-163">NOTES</span></span>

## <span data-ttu-id="87809-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87809-164">RELATED LINKS</span></span>

[<span data-ttu-id="87809-165">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="87809-165">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="87809-166">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="87809-166">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="87809-167">Nowe — AzResource</span><span class="sxs-lookup"><span data-stu-id="87809-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="87809-168">Nowe — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="87809-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="87809-169">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="87809-169">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="87809-170">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="87809-170">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)
