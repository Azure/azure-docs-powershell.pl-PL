---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 01e4e6b990a35b8573a9ea1d2f2803f6d6fabc1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549924"
---
# <span data-ttu-id="feb45-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="feb45-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="feb45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="feb45-102">SYNOPSIS</span></span>
<span data-ttu-id="feb45-103">Pobiera zasoby.</span><span class="sxs-lookup"><span data-stu-id="feb45-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="feb45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="feb45-104">SYNTAX</span></span>

### <span data-ttu-id="feb45-105">Zestaw parametrów lista wszystkich zasobów.</span><span class="sxs-lookup"><span data-stu-id="feb45-105">The list all resources parameter set.</span></span> <span data-ttu-id="feb45-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="feb45-106">(Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feb45-107">Uzyskaj jeden zasób według jego identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="feb45-107">Get a single resource by its Id.</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feb45-108">Pobierz jeden zasób na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="feb45-108">Get a single resource at the tenant level.</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feb45-109">Wyświetla listę zasobów na podstawie określonego zakresu na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="feb45-109">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feb45-110">Pobierz zasób według nazwy i grupy</span><span class="sxs-lookup"><span data-stu-id="feb45-110">Get resource by name and group</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="feb45-111">Pobierz zasób według nazwy i typu.</span><span class="sxs-lookup"><span data-stu-id="feb45-111">Get a resource by name and type.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feb45-112">Pobierz zasób według nazwy, grupy i typu</span><span class="sxs-lookup"><span data-stu-id="feb45-112">Get resource by name, group and type</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feb45-113">Pobieranie kolekcji zasobów</span><span class="sxs-lookup"><span data-stu-id="feb45-113">Get resource collection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="feb45-114">Opis</span><span class="sxs-lookup"><span data-stu-id="feb45-114">DESCRIPTION</span></span>
<span data-ttu-id="feb45-115">Polecenie cmdlet **Get-AzureRmResource** umożliwia pobieranie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="feb45-115">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="feb45-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="feb45-116">EXAMPLES</span></span>

### <span data-ttu-id="feb45-117">Przykład 1. Pobieranie zasobu</span><span class="sxs-lookup"><span data-stu-id="feb45-117">Example 1: Get a resource</span></span>
```
PS C:\>Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoWebsite"
```

<span data-ttu-id="feb45-118">To polecenie uzyskuje zasób typu Microsoft. Web/Sites o nazwie ContosoWebsite w obszarze ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="feb45-118">This command gets a resource of the type microsoft.web/sites, named ContosoWebsite under ResourceGroup11.</span></span>

## <span data-ttu-id="feb45-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="feb45-119">PARAMETERS</span></span>

### <span data-ttu-id="feb45-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="feb45-120">-ApiVersion</span></span>
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

### <span data-ttu-id="feb45-121">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="feb45-121">-ExpandProperties</span></span>
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

### <span data-ttu-id="feb45-122">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="feb45-122">-ExtensionResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feb45-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="feb45-123">-ExtensionResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feb45-124">-IsCollection</span><span class="sxs-lookup"><span data-stu-id="feb45-124">-IsCollection</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feb45-125">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="feb45-125">-ODataQuery</span></span>
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

### <span data-ttu-id="feb45-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="feb45-126">-Pre</span></span>
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

### <span data-ttu-id="feb45-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feb45-127">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: Get resource by name and group
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feb45-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="feb45-128">-ResourceId</span></span>
<span data-ttu-id="feb45-129">Określa w pełni kwalifikowany identyfikator zasobu, w tym abonament, tak jak w poniższym przykładzie:</span><span class="sxs-lookup"><span data-stu-id="feb45-129">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="feb45-130">`/subscriptions/`Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="feb45-130">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="feb45-131">To polecenie cmdlet umożliwia pobieranie zasobu o tym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="feb45-131">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a single resource by its Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feb45-132">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="feb45-132">-ResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feb45-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="feb45-133">-ResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resource by name and type.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feb45-134">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="feb45-134">-TenantLevel</span></span>
<span data-ttu-id="feb45-135">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="feb45-135">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feb45-136">-Początek</span><span class="sxs-lookup"><span data-stu-id="feb45-136">-Top</span></span>
```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feb45-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb45-137">-DefaultProfile</span></span>
<span data-ttu-id="feb45-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="feb45-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="feb45-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb45-139">CommonParameters</span></span>
<span data-ttu-id="feb45-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feb45-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb45-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feb45-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb45-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="feb45-142">INPUTS</span></span>

## <span data-ttu-id="feb45-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="feb45-143">OUTPUTS</span></span>

### <span data-ttu-id="feb45-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="feb45-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="feb45-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="feb45-145">NOTES</span></span>

## <span data-ttu-id="feb45-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="feb45-146">RELATED LINKS</span></span>

[<span data-ttu-id="feb45-147">Znajdź-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="feb45-147">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="feb45-148">Przenieś — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="feb45-148">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="feb45-149">Nowe — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="feb45-149">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="feb45-150">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="feb45-150">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="feb45-151">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="feb45-151">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


