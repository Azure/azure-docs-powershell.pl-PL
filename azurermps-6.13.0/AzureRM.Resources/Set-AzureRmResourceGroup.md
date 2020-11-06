---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
ms.openlocfilehash: 4ba57d1f8e1abe8c506f1bcd6625a7a90551f164
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552547"
---
# <span data-ttu-id="add14-101">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="add14-101">Set-AzureRmResourceGroup</span></span>

## <span data-ttu-id="add14-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="add14-102">SYNOPSIS</span></span>
<span data-ttu-id="add14-103">Modyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="add14-103">Modifies a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="add14-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="add14-104">SYNTAX</span></span>

### <span data-ttu-id="add14-105">SetByResourceGroupName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="add14-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzureRmResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="add14-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="add14-106">SetByResourceGroupId</span></span>
```
Set-AzureRmResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="add14-107">Opis</span><span class="sxs-lookup"><span data-stu-id="add14-107">DESCRIPTION</span></span>
<span data-ttu-id="add14-108">Polecenie cmdlet **Set-AzureRmResourceGroup** modyfikuje właściwości grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="add14-108">The **Set-AzureRmResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="add14-109">Za pomocą tego polecenia cmdlet można dodawać, zmieniać i usuwać Tagi platformy Azure zastosowane do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="add14-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="add14-110">Określ parametr *name (nazwa* ), aby zidentyfikować grupę zasobów i parametr *znacznika* , aby zmodyfikować znaczniki.</span><span class="sxs-lookup"><span data-stu-id="add14-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="add14-111">Za pomocą tego polecenia cmdlet można zmienić nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="add14-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="add14-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="add14-112">EXAMPLES</span></span>

### <span data-ttu-id="add14-113">Przykład 1. Stosowanie znacznika do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="add14-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="add14-114">To polecenie powoduje zastosowanie znacznika działu z wartością do grupy zasobów bez istniejących tagów.</span><span class="sxs-lookup"><span data-stu-id="add14-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="add14-115">Przykład 2: Dodawanie znaczników do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="add14-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzureRmResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="add14-116">W tym przykładzie dodano znacznik statusu z wartością zatwierdzony i tag FY2016 do grupy zasobów zawierającej istniejące znaczniki.</span><span class="sxs-lookup"><span data-stu-id="add14-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="add14-117">Ponieważ znaczniki, które określisz, zastępują istniejące znaczniki, należy uwzględnić istniejące znaczniki w nowej kolekcji znaczników lub je utracić.</span><span class="sxs-lookup"><span data-stu-id="add14-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="add14-118">Pierwsze polecenie pobiera grupę zasobów ContosoRG i używa metody z kropką w celu uzyskania wartości właściwości znaczników.</span><span class="sxs-lookup"><span data-stu-id="add14-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="add14-119">Polecenie zapisuje znaczniki w zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="add14-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="add14-120">Drugie polecenie pobiera znaczniki ze zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="add14-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="add14-121">W trzecim poleceniu użyto operatora + =, aby dodać znaczniki statusu i FY2016 do tablicy znaczników w zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="add14-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="add14-122">W czwartym poleceniu *Tag* użyto parametru tag **Set-AzureRmResourceGroup** w celu zastosowania znaczników w zmiennej $Tags do grupy zasobów ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="add14-122">The fourth command uses the *Tag* parameter of **Set-AzureRmResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="add14-123">W piątym poleceniu są pobierane wszystkie Tagi zastosowane do grupy zasobów ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="add14-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="add14-124">Wyjście wskazuje, że grupa zasobów zawiera tag dział, a dwa nowe tagi, stan i FY2015.</span><span class="sxs-lookup"><span data-stu-id="add14-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="add14-125">Przykład 3: Usuwanie wszystkich znaczników grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="add14-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="add14-126">To polecenie określa parametr *znacznika* z pustą wartością tabeli skrótów, aby usunąć wszystkie Tagi z grupy zasobów ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="add14-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="add14-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="add14-127">PARAMETERS</span></span>

### <span data-ttu-id="add14-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="add14-128">-ApiVersion</span></span>
<span data-ttu-id="add14-129">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="add14-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="add14-130">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="add14-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="add14-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add14-131">-DefaultProfile</span></span>
<span data-ttu-id="add14-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="add14-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="add14-133">-ID</span><span class="sxs-lookup"><span data-stu-id="add14-133">-Id</span></span>
<span data-ttu-id="add14-134">Określa identyfikator grupy zasobów do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="add14-134">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add14-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="add14-135">-Name</span></span>
<span data-ttu-id="add14-136">Określa nazwę grupy zasobów do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="add14-136">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="add14-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="add14-137">-Pre</span></span>
<span data-ttu-id="add14-138">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="add14-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="add14-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="add14-139">-Tag</span></span>
<span data-ttu-id="add14-140">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="add14-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="add14-141">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"} tag to para nazwa-wartość, którą można tworzyć i stosować do zasobów i grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="add14-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="add14-142">Po przypisaniu znaczników do zasobów i grup można użyć parametru *znacznika* Get-AzureRmResource i Get-AzureRmResourceGroup do wyszukiwania zasobów i grup według nazwy lub nazwy lub wartości znacznika.</span><span class="sxs-lookup"><span data-stu-id="add14-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="add14-143">Za pomocą znaczników można klasyfikować zasoby, na przykład według działów lub MPK, a także śledzić notatki i komentarze dotyczące zasobów.</span><span class="sxs-lookup"><span data-stu-id="add14-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="add14-144">Aby dodać lub zmienić znacznik, należy zamienić kolekcję znaczników dla grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="add14-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="add14-145">Aby usunąć znacznik, wprowadź tabelę skrótów zawierającą wszystkie znaczniki, które są obecnie stosowane do grupy zasobów, z poziomu **Get-AzureRmResourceGroup** , z wyjątkiem znacznika, który chcesz usunąć.</span><span class="sxs-lookup"><span data-stu-id="add14-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzureRmResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="add14-146">Aby usunąć wszystkie znaczniki z grupy zasobów, określ pustą tabelę skrótów: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="add14-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

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

### <span data-ttu-id="add14-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add14-147">CommonParameters</span></span>
<span data-ttu-id="add14-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add14-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add14-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="add14-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add14-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="add14-150">INPUTS</span></span>

### <span data-ttu-id="add14-151">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="add14-151">None</span></span>

## <span data-ttu-id="add14-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="add14-152">OUTPUTS</span></span>

### <span data-ttu-id="add14-153">Microsoft. Azure. Commands. resources. models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="add14-153">Microsoft.Azure.Commands.Resources.Models.PSResourceGroup</span></span>

## <span data-ttu-id="add14-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="add14-154">NOTES</span></span>

## <span data-ttu-id="add14-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="add14-155">RELATED LINKS</span></span>

[<span data-ttu-id="add14-156">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="add14-156">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="add14-157">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="add14-157">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="add14-158">Nowe — AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="add14-158">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="add14-159">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="add14-159">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)
