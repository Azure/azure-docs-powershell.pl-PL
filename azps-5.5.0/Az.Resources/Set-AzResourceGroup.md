---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183642"
---
# <span data-ttu-id="88804-101">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88804-101">Set-AzResourceGroup</span></span>

## <span data-ttu-id="88804-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88804-102">SYNOPSIS</span></span>
<span data-ttu-id="88804-103">Modyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="88804-103">Modifies a resource group.</span></span>

## <span data-ttu-id="88804-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="88804-104">SYNTAX</span></span>

### <span data-ttu-id="88804-105">SetByResourceGroupName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="88804-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88804-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="88804-106">SetByResourceGroupId</span></span>
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88804-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="88804-107">DESCRIPTION</span></span>
<span data-ttu-id="88804-108">Polecenie cmdlet **Set-AzResourceGroup** modyfikuje właściwości grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="88804-108">The **Set-AzResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="88804-109">To polecenie cmdlet umożliwia dodawanie, zmienianie i usuwanie tagów platformy Azure zastosowanych do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="88804-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="88804-110">Określ parametr *Name (Nazwa),* aby zidentyfikować grupę zasobów, oraz *parametr Tag* w celu zmodyfikowania tagów.</span><span class="sxs-lookup"><span data-stu-id="88804-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="88804-111">Za pomocą tego polecenia cmdlet nie można zmienić nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="88804-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="88804-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="88804-112">EXAMPLES</span></span>

### <span data-ttu-id="88804-113">Przykład 1. Stosowanie tagu do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="88804-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="88804-114">To polecenie powoduje zastosowanie tagu Dział z wartością IT do grupy zasobów, która nie ma istniejących tagów.</span><span class="sxs-lookup"><span data-stu-id="88804-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="88804-115">Przykład 2. Dodawanie tagów do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="88804-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="88804-116">W tym przykładzie do grupy zasobów, która ma istniejące tagi, dodano tag stanu z wartością Zatwierdzony i tag roku 2016.</span><span class="sxs-lookup"><span data-stu-id="88804-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="88804-117">Ponieważ określone tagi zastępują istniejące tagi, musisz uwzględnić istniejące tagi w nowej kolekcji tagów lub je utracisz.</span><span class="sxs-lookup"><span data-stu-id="88804-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="88804-118">Pierwsze polecenie pobiera grupę zasobów ContosoRG i używa metody kropki w celu uzyskania wartości właściwości Tagi.</span><span class="sxs-lookup"><span data-stu-id="88804-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="88804-119">To polecenie przechowuje tagi w $Tags zmienną.</span><span class="sxs-lookup"><span data-stu-id="88804-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="88804-120">Drugie polecenie pobiera tagi w $Tags zmienną.</span><span class="sxs-lookup"><span data-stu-id="88804-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="88804-121">Trzecie polecenie używa operatora przydziału += w celu dodania tagów Status i FY2016 do tablicy tagów w $Tags zadania.</span><span class="sxs-lookup"><span data-stu-id="88804-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="88804-122">Czwarte polecenie używa *parametru Tag* **set-AzResourceGroup** w celu zastosowania tagów w zmiennej $Tags do grupy zasobów ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="88804-122">The fourth command uses the *Tag* parameter of **Set-AzResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="88804-123">Piąte polecenie pobiera wszystkie tagi zastosowane do grupy zasobów ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="88804-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="88804-124">Wynik pokazuje, że grupa zasobów ma tag Dział oraz dwa nowe tagi: Stan i ROK2015.</span><span class="sxs-lookup"><span data-stu-id="88804-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="88804-125">Przykład 3. Usuwanie wszystkich tagów dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="88804-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="88804-126">To polecenie określa *parametr Tag z* pustą wartością tabeli skrótu, aby usunąć wszystkie tagi z grupy zasobów ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="88804-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="88804-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88804-127">PARAMETERS</span></span>

### <span data-ttu-id="88804-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="88804-128">-ApiVersion</span></span>
<span data-ttu-id="88804-129">Określa wersję interfejsu API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="88804-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="88804-130">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="88804-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="88804-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88804-131">-DefaultProfile</span></span>
<span data-ttu-id="88804-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="88804-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88804-133">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="88804-133">-Id</span></span>
<span data-ttu-id="88804-134">Określa identyfikator grupy zasobów do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="88804-134">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88804-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="88804-135">-Name</span></span>
<span data-ttu-id="88804-136">Określa nazwę grupy zasobów do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="88804-136">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88804-137">— Przed</span><span class="sxs-lookup"><span data-stu-id="88804-137">-Pre</span></span>
<span data-ttu-id="88804-138">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="88804-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="88804-139">— Tag</span><span class="sxs-lookup"><span data-stu-id="88804-139">-Tag</span></span>
<span data-ttu-id="88804-140">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="88804-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="88804-141">Na przykład: @{key0="value0";key1=$null;key2="value2"} Tag to para wartości nazwy, która można utworzyć i zastosować do zasobów i grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="88804-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="88804-142">Po przypisaniu tagów do zasobów i grup możesz użyć parametru *Tag* Get-AzResource i Get-AzResourceGroup, aby wyszukiwać zasoby i grupy według nazwy tagu lub nazwy i wartości.</span><span class="sxs-lookup"><span data-stu-id="88804-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="88804-143">Za pomocą tagów można kategoryzować zasoby( na przykład według działu lub centrum kosztów) albo śledzić notatki lub komentarze dotyczące zasobów.</span><span class="sxs-lookup"><span data-stu-id="88804-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="88804-144">Aby dodać lub zmienić tag, musisz zastąpić kolekcję tagów grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="88804-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="88804-145">Aby usunąć tag, wprowadź tabelę skrótów ze wszystkimi tagami zastosowanymi obecnie do grupy zasobów z grupy **Get-AzResourceGroup,** z wyjątkiem tagu, który chcesz usunąć.</span><span class="sxs-lookup"><span data-stu-id="88804-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzResourceGroup**, except for the tag you want to delete.</span></span> <span data-ttu-id="88804-146">Aby usunąć wszystkie tagi z grupy zasobów, określ pustą tabelę `@{}` skrótów:</span><span class="sxs-lookup"><span data-stu-id="88804-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88804-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88804-147">CommonParameters</span></span>
<span data-ttu-id="88804-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88804-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88804-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88804-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88804-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88804-150">INPUTS</span></span>

### <span data-ttu-id="88804-151">System.String</span><span class="sxs-lookup"><span data-stu-id="88804-151">System.String</span></span>

### <span data-ttu-id="88804-152">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="88804-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="88804-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="88804-153">OUTPUTS</span></span>

### <span data-ttu-id="88804-154">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88804-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="88804-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="88804-155">NOTES</span></span>

## <span data-ttu-id="88804-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88804-156">RELATED LINKS</span></span>

[<span data-ttu-id="88804-157">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="88804-157">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="88804-158">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88804-158">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="88804-159">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88804-159">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="88804-160">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88804-160">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)
