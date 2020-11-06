---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 2161c3c4bc81721c0d99b88ab0adfc43beac8eee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544132"
---
# <span data-ttu-id="9e53a-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e53a-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="9e53a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e53a-102">SYNOPSIS</span></span>
<span data-ttu-id="9e53a-103">Pobiera zasoby.</span><span class="sxs-lookup"><span data-stu-id="9e53a-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e53a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e53a-104">SYNTAX</span></span>

### <span data-ttu-id="9e53a-105">GetAllResources (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9e53a-105">GetAllResources (Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e53a-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e53a-106">GetByResourceId</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e53a-107">GetByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="9e53a-107">GetByTenantLevel</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e53a-108">GetBySpecifiedScopeAtTenantLevel</span><span class="sxs-lookup"><span data-stu-id="9e53a-108">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e53a-109">GetByNameAndGroup</span><span class="sxs-lookup"><span data-stu-id="9e53a-109">GetByNameAndGroup</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e53a-110">GetByResourceNameAndType</span><span class="sxs-lookup"><span data-stu-id="9e53a-110">GetByResourceNameAndType</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e53a-111">GetByNameGroupAndType</span><span class="sxs-lookup"><span data-stu-id="9e53a-111">GetByNameGroupAndType</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e53a-112">Getresourcecollection</span><span class="sxs-lookup"><span data-stu-id="9e53a-112">GetResourceCollection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e53a-113">Opis</span><span class="sxs-lookup"><span data-stu-id="9e53a-113">DESCRIPTION</span></span>
<span data-ttu-id="9e53a-114">Polecenie cmdlet **Get-AzureRmResource** umożliwia pobieranie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9e53a-114">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="9e53a-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e53a-115">EXAMPLES</span></span>

### <span data-ttu-id="9e53a-116">Przykład 1. pobieranie wszystkich zasobów określonego typu</span><span class="sxs-lookup"><span data-stu-id="9e53a-116">Example 1: Get all the resources of a particular type</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType microsoft.web/sites
```

<span data-ttu-id="9e53a-117">To polecenie uzyskuje zasób typu Microsoft. Web/Sites w obszarze ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9e53a-117">This command gets a resource of the type microsoft.web/sites under ResourceGroup11.</span></span>

### <span data-ttu-id="9e53a-118">Przykład 2: Pobieranie zasobu według nazwy</span><span class="sxs-lookup"><span data-stu-id="9e53a-118">Example 2: Get a resource by name</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceName ContosoWebsite
```

<span data-ttu-id="9e53a-119">To polecenie uzyskuje zasób o nazwie ContosoWebsite w obszarze ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9e53a-119">This command gets a resource  named ContosoWebsite under ResourceGroup11.</span></span>

### <span data-ttu-id="9e53a-120">Przykład 3: pokazywanie wszystkich stanów kont magazynu w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="9e53a-120">Example 3: Show all the status of storage accounts in a Resource Group</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType Microsoft.ClassicStorage/storageAccounts -ExpandProperties |
   Select * -Expand Properties |
   Sort Name |
   Format-Table Name,Status*
```

## <span data-ttu-id="9e53a-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e53a-121">PARAMETERS</span></span>

### <span data-ttu-id="9e53a-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9e53a-122">-ApiVersion</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e53a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e53a-123">-DefaultProfile</span></span>
<span data-ttu-id="9e53a-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9e53a-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e53a-125">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="9e53a-125">-ExpandProperties</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e53a-126">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="9e53a-126">-ExtensionResourceName</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e53a-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="9e53a-127">-ExtensionResourceType</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e53a-128">-IsCollection</span><span class="sxs-lookup"><span data-stu-id="9e53a-128">-IsCollection</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e53a-129">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="9e53a-129">-ODataQuery</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e53a-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="9e53a-130">-Pre</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e53a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e53a-131">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e53a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e53a-132">-ResourceId</span></span>
<span data-ttu-id="9e53a-133">Określa w pełni kwalifikowany identyfikator zasobu, w tym abonament, tak jak w poniższym przykładzie:</span><span class="sxs-lookup"><span data-stu-id="9e53a-133">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="9e53a-134">`/subscriptions/`Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="9e53a-134">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="9e53a-135">To polecenie cmdlet umożliwia pobieranie zasobu o tym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="9e53a-135">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e53a-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9e53a-136">-ResourceName</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e53a-137">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9e53a-137">-ResourceType</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByResourceNameAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e53a-138">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9e53a-138">-TenantLevel</span></span>
<span data-ttu-id="9e53a-139">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="9e53a-139">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e53a-140">-Początek</span><span class="sxs-lookup"><span data-stu-id="9e53a-140">-Top</span></span>
```yaml
Type: Int32
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e53a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e53a-141">CommonParameters</span></span>
<span data-ttu-id="9e53a-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e53a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e53a-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e53a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e53a-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e53a-144">INPUTS</span></span>

### <span data-ttu-id="9e53a-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9e53a-145">None</span></span>
<span data-ttu-id="9e53a-146">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9e53a-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e53a-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e53a-147">OUTPUTS</span></span>

### <span data-ttu-id="9e53a-148">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9e53a-148">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9e53a-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e53a-149">NOTES</span></span>

## <span data-ttu-id="9e53a-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e53a-150">RELATED LINKS</span></span>

[<span data-ttu-id="9e53a-151">Znajdź-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e53a-151">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="9e53a-152">Przenieś — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e53a-152">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="9e53a-153">Nowe — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e53a-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="9e53a-154">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e53a-154">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="9e53a-155">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e53a-155">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


