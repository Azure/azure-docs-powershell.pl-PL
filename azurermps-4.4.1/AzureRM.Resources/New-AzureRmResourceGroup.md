---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
ms.openlocfilehash: ccb0b4afdf39510461dd0f6627748492ba22818f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546087"
---
# <span data-ttu-id="cc227-101">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cc227-101">New-AzureRmResourceGroup</span></span>

## <span data-ttu-id="cc227-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc227-102">SYNOPSIS</span></span>
<span data-ttu-id="cc227-103">Tworzy grupę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cc227-103">Creates an Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc227-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc227-104">SYNTAX</span></span>

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc227-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cc227-105">DESCRIPTION</span></span>
<span data-ttu-id="cc227-106">Polecenie cmdlet **New-AzureRmResourceGroup** tworzy grupę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cc227-106">The **New-AzureRmResourceGroup** cmdlet creates an Azure resource group.</span></span>

<span data-ttu-id="cc227-107">Grupę zasobów można utworzyć za pomocą samej nazwy i lokalizacji, a następnie za pomocą polecenia cmdlet New-AzureRmResource utworzyć zasoby, które mają zostać dodane do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc227-107">You can create a resource group by using just a name and location, and then use the New-AzureRmResource cmdlet to create resources to add to the resource group.</span></span>

<span data-ttu-id="cc227-108">Aby dodać wdrożenie do istniejącej grupy zasobów, użyj polecenia cmdlet New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="cc227-108">To add a deployment to an existing resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="cc227-109">Aby dodać zasób do istniejącej grupy zasobów, użyj polecenia cmdlet **New-AzureRmResource** .</span><span class="sxs-lookup"><span data-stu-id="cc227-109">To add a resource to an existing resource group, use the **New-AzureRmResource** cmdlet.</span></span> <span data-ttu-id="cc227-110">Zasób platformy Azure jest zarządzaną przez użytkownika jednostką Azure, taką jak serwer bazy danych, baza danych lub witryna sieci Web.</span><span class="sxs-lookup"><span data-stu-id="cc227-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="cc227-111">Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostka.</span><span class="sxs-lookup"><span data-stu-id="cc227-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="cc227-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc227-112">EXAMPLES</span></span>

### <span data-ttu-id="cc227-113">Przykład 1. Tworzenie pustej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cc227-113">Example 1: Create an empty resource group</span></span>
```
PS C:\>New-AzureRmResourceGroup -Name "RG01" -Location "South Central US"
```

<span data-ttu-id="cc227-114">To polecenie tworzy grupę zasobów bez zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc227-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="cc227-115">Za pomocą poleceń cmdlet **New-AzureRmResource** lub **New-AzureRmResourceGroupDeployment** można dodawać zasoby i wdrożenia do tej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc227-115">You can use the **New-AzureRmResource** or **New-AzureRmResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="cc227-116">Przykład 2: Tworzenie grupy zasobów ze znacznikami</span><span class="sxs-lookup"><span data-stu-id="cc227-116">Example 2: Create a resource group with tags</span></span>
```
PS C:\>New-AzureRmResourceGroup -Name "RG01" -Location "South Central US" -Tag @{"Empty"=$null; "Department"="Marketing"}
```

<span data-ttu-id="cc227-117">To polecenie tworzy pustą grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc227-117">This command creates an empty resource group.</span></span> <span data-ttu-id="cc227-118">To polecenie jest takie samo jak w przypadku polecenia z przykładu 1, z wyjątkiem tego, że przypisuje znaczniki do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc227-118">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="cc227-119">Pierwszy znacznik o nazwie Empty może być wykorzystywany do identyfikowania grup zasobów, które nie mają zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc227-119">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="cc227-120">Drugi znacznik ma nazwę dział i ma wartość marketingową.</span><span class="sxs-lookup"><span data-stu-id="cc227-120">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="cc227-121">Możesz użyć znacznika, takiego jak ten, aby przydzielić grupy zasobów do administrowania lub budżetowania.</span><span class="sxs-lookup"><span data-stu-id="cc227-121">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="cc227-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc227-122">PARAMETERS</span></span>

### <span data-ttu-id="cc227-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cc227-123">-ApiVersion</span></span>
<span data-ttu-id="cc227-124">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc227-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="cc227-125">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="cc227-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="cc227-126">-Force</span><span class="sxs-lookup"><span data-stu-id="cc227-126">-Force</span></span>
<span data-ttu-id="cc227-127">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cc227-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc227-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cc227-128">-Location</span></span>
<span data-ttu-id="cc227-129">Określa lokalizację grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc227-129">Specifies the location of the resource group.</span></span> <span data-ttu-id="cc227-130">Określ lokalizację centrum danych platformy Azure, na przykład Azja Zachodnia lub Południowo-Wschodnia.</span><span class="sxs-lookup"><span data-stu-id="cc227-130">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="cc227-131">Grupę zasobów można umieścić w dowolnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="cc227-131">You can place a resource group in any location.</span></span> <span data-ttu-id="cc227-132">Grupa zasobów nie musi znajdować się w tej samej lokalizacji w ramach subskrypcji platformy Azure ani w tej samej lokalizacji co zasoby.</span><span class="sxs-lookup"><span data-stu-id="cc227-132">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>

<span data-ttu-id="cc227-133">Aby określić, która lokalizacja obsługuje poszczególne typy zasobów, użyj polecenia cmdlet Get-AzureRmResourceProvider z parametrem *ProviderNamespace* .</span><span class="sxs-lookup"><span data-stu-id="cc227-133">To determine which location supports each resource type, use the Get-AzureRmResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc227-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cc227-134">-Name</span></span>
<span data-ttu-id="cc227-135">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc227-135">Specifies a name for the resource group.</span></span> <span data-ttu-id="cc227-136">Nazwa zasobu musi być unikatowa w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cc227-136">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="cc227-137">Jeśli grupa zasobów o tej nazwie już istnieje, polecenie monituje o potwierdzenie przed zastąpieniem istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc227-137">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc227-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="cc227-138">-Pre</span></span>
<span data-ttu-id="cc227-139">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="cc227-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cc227-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="cc227-140">-Tag</span></span>
<span data-ttu-id="cc227-141">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="cc227-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cc227-142">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="cc227-142">For example:</span></span>

<span data-ttu-id="cc227-143">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="cc227-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="cc227-144">Aby dodać lub zmienić znacznik, należy zamienić kolekcję znaczników dla grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc227-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span>

<span data-ttu-id="cc227-145">Po przypisaniu znaczników do zasobów i grup można użyć parametru *znacznika* Get-AzureRmResource i Get-AzureRmResourceGroup do wyszukiwania zasobów i grup według nazwy znacznika lub według nazwy i wartości.</span><span class="sxs-lookup"><span data-stu-id="cc227-145">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="cc227-146">Za pomocą znaczników można klasyfikować zasoby, na przykład według działów lub MPK, a także śledzić notatki i komentarze dotyczące zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc227-146">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>

<span data-ttu-id="cc227-147">Aby uzyskać wstępnie zdefiniowane Tagi, użyj polecenia cmdlet Get-AzureRMTag.</span><span class="sxs-lookup"><span data-stu-id="cc227-147">To get your predefined tags, use the Get-AzureRMTag cmdlet.</span></span>

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

### <span data-ttu-id="cc227-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc227-148">-Confirm</span></span>
<span data-ttu-id="cc227-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc227-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc227-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc227-150">-WhatIf</span></span>
<span data-ttu-id="cc227-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc227-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc227-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cc227-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc227-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc227-153">-DefaultProfile</span></span>
<span data-ttu-id="cc227-154">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc227-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc227-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc227-155">CommonParameters</span></span>
<span data-ttu-id="cc227-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc227-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc227-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc227-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc227-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc227-158">INPUTS</span></span>

### <span data-ttu-id="cc227-159">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cc227-159">None</span></span>

## <span data-ttu-id="cc227-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc227-160">OUTPUTS</span></span>

### <span data-ttu-id="cc227-161">Microsoft. Azure. Commands. ResourceManagement. models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cc227-161">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroup</span></span>

## <span data-ttu-id="cc227-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc227-162">NOTES</span></span>

## <span data-ttu-id="cc227-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc227-163">RELATED LINKS</span></span>

[<span data-ttu-id="cc227-164">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="cc227-164">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="cc227-165">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cc227-165">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="cc227-166">Nowe — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="cc227-166">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="cc227-167">Nowe — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="cc227-167">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="cc227-168">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cc227-168">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="cc227-169">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cc227-169">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)
