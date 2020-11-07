---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
ms.openlocfilehash: a6fa8a27bacf5504564703d8669616f748aa95d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718703"
---
# <span data-ttu-id="85990-101">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="85990-101">Set-AzureRmResourceGroup</span></span>

## <span data-ttu-id="85990-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85990-102">SYNOPSIS</span></span>
<span data-ttu-id="85990-103">Modyfikuje grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="85990-103">Modifies a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85990-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85990-104">SYNTAX</span></span>

### <span data-ttu-id="85990-105">Umożliwia wyświetlenie listy grup zasobów na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="85990-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="85990-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="85990-106">(Default)</span></span>
```
Set-AzureRmResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85990-107">Umożliwia wyświetlenie listy grup zasobów na podstawie identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="85990-107">Lists the resource group based in the Id.</span></span>
```
Set-AzureRmResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85990-108">Opis</span><span class="sxs-lookup"><span data-stu-id="85990-108">DESCRIPTION</span></span>
<span data-ttu-id="85990-109">Polecenie cmdlet **Set-AzureRmResourceGroup** modyfikuje właściwości grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85990-109">The **Set-AzureRmResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="85990-110">Za pomocą tego polecenia cmdlet można dodawać, zmieniać i usuwać Tagi platformy Azure zastosowane do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85990-110">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="85990-111">Określ parametr *name (nazwa* ), aby zidentyfikować grupę zasobów i parametr *znacznika* , aby zmodyfikować znaczniki.</span><span class="sxs-lookup"><span data-stu-id="85990-111">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>

<span data-ttu-id="85990-112">Za pomocą tego polecenia cmdlet można zmienić nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85990-112">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="85990-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85990-113">EXAMPLES</span></span>

### <span data-ttu-id="85990-114">Przykład 1. Stosowanie znacznika do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="85990-114">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="85990-115">To polecenie powoduje zastosowanie znacznika działu z wartością do grupy zasobów bez istniejących tagów.</span><span class="sxs-lookup"><span data-stu-id="85990-115">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="85990-116">Przykład 2: Dodawanie znaczników do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="85990-116">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzureRmResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="85990-117">W tym przykładzie dodano znacznik statusu z wartością zatwierdzony i tag FY2016 do grupy zasobów zawierającej istniejące znaczniki.</span><span class="sxs-lookup"><span data-stu-id="85990-117">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="85990-118">Ponieważ znaczniki, które określisz, zastępują istniejące znaczniki, należy uwzględnić istniejące znaczniki w nowej kolekcji znaczników lub je utracić.</span><span class="sxs-lookup"><span data-stu-id="85990-118">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>

<span data-ttu-id="85990-119">Pierwsze polecenie pobiera grupę zasobów ContosoRG i używa metody z kropką w celu uzyskania wartości właściwości znaczników.</span><span class="sxs-lookup"><span data-stu-id="85990-119">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="85990-120">Polecenie zapisuje znaczniki w zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="85990-120">The command stores the tags in the $Tags variable.</span></span>

<span data-ttu-id="85990-121">Drugie polecenie pobiera znaczniki ze zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="85990-121">The second command gets the tags in the $Tags variable.</span></span>

<span data-ttu-id="85990-122">W trzecim poleceniu użyto operatora + =, aby dodać znaczniki statusu i FY2016 do tablicy znaczników w zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="85990-122">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>

<span data-ttu-id="85990-123">W czwartym poleceniu *Tag* użyto parametru tag **Set-AzureRmResourceGroup** w celu zastosowania znaczników w zmiennej $Tags do grupy zasobów ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="85990-123">The fourth command uses the *Tag* parameter of **Set-AzureRmResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>

<span data-ttu-id="85990-124">W piątym poleceniu są pobierane wszystkie Tagi zastosowane do grupy zasobów ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="85990-124">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="85990-125">Wyjście wskazuje, że grupa zasobów zawiera tag dział, a dwa nowe tagi, stan i FY2015.</span><span class="sxs-lookup"><span data-stu-id="85990-125">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="85990-126">Przykład 3: Usuwanie wszystkich znaczników grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="85990-126">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="85990-127">To polecenie określa parametr *znacznika* z pustą wartością tabeli skrótów, aby usunąć wszystkie Tagi z grupy zasobów ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="85990-127">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="85990-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85990-128">PARAMETERS</span></span>

### <span data-ttu-id="85990-129">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="85990-129">-ApiVersion</span></span>
<span data-ttu-id="85990-130">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="85990-130">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="85990-131">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="85990-131">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="85990-132">-ID</span><span class="sxs-lookup"><span data-stu-id="85990-132">-Id</span></span>
<span data-ttu-id="85990-133">Określa identyfikator grupy zasobów do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="85990-133">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85990-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85990-134">-Name</span></span>
<span data-ttu-id="85990-135">Określa nazwę grupy zasobów do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="85990-135">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85990-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="85990-136">-Pre</span></span>
<span data-ttu-id="85990-137">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="85990-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="85990-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="85990-138">-Tag</span></span>
<span data-ttu-id="85990-139">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="85990-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="85990-140">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="85990-140">For example:</span></span>

<span data-ttu-id="85990-141">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="85990-141">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="85990-142">Tag to para nazwa-wartość, którą można tworzyć i stosować do zasobów i grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="85990-142">A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="85990-143">Po przypisaniu znaczników do zasobów i grup można użyć parametru *znacznika* Get-AzureRmResource i Get-AzureRmResourceGroup do wyszukiwania zasobów i grup według nazwy lub nazwy lub wartości znacznika.</span><span class="sxs-lookup"><span data-stu-id="85990-143">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="85990-144">Za pomocą znaczników można klasyfikować zasoby, na przykład według działów lub MPK, a także śledzić notatki i komentarze dotyczące zasobów.</span><span class="sxs-lookup"><span data-stu-id="85990-144">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>

<span data-ttu-id="85990-145">Aby dodać lub zmienić znacznik, należy zamienić kolekcję znaczników dla grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85990-145">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="85990-146">Aby usunąć znacznik, wprowadź tabelę skrótów zawierającą wszystkie znaczniki, które są obecnie stosowane do grupy zasobów, z poziomu **Get-AzureRmResourceGroup** , z wyjątkiem znacznika, który chcesz usunąć.</span><span class="sxs-lookup"><span data-stu-id="85990-146">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzureRmResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="85990-147">Aby usunąć wszystkie znaczniki z grupy zasobów, określ pustą tabelę skrótów: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="85990-147">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

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

### <span data-ttu-id="85990-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85990-148">-DefaultProfile</span></span>
<span data-ttu-id="85990-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85990-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85990-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85990-150">CommonParameters</span></span>
<span data-ttu-id="85990-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85990-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85990-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85990-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85990-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85990-153">INPUTS</span></span>

### <span data-ttu-id="85990-154">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="85990-154">None</span></span>

## <span data-ttu-id="85990-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85990-155">OUTPUTS</span></span>

### <span data-ttu-id="85990-156">Microsoft. Azure. Commands. resources. models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="85990-156">Microsoft.Azure.Commands.Resources.Models.PSResourceGroup</span></span>

## <span data-ttu-id="85990-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85990-157">NOTES</span></span>

## <span data-ttu-id="85990-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85990-158">RELATED LINKS</span></span>

[<span data-ttu-id="85990-159">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="85990-159">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="85990-160">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="85990-160">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="85990-161">Nowe — AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="85990-161">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="85990-162">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="85990-162">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)
