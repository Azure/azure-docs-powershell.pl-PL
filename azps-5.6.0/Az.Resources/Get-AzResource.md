---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: 92a9e1820af2e850af6c3abaca71a7be1f15ed5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950993"
---
# <span data-ttu-id="6652b-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="6652b-101">Get-AzResource</span></span>

## <span data-ttu-id="6652b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6652b-102">SYNOPSIS</span></span>

<span data-ttu-id="6652b-103">Pobiera zasoby.</span><span class="sxs-lookup"><span data-stu-id="6652b-103">Gets resources.</span></span>

## <span data-ttu-id="6652b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6652b-104">SYNTAX</span></span>

### <span data-ttu-id="6652b-105">ByTagNameValueParameterSet (Domyślny)</span><span class="sxs-lookup"><span data-stu-id="6652b-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6652b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6652b-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6652b-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6652b-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6652b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6652b-108">DESCRIPTION</span></span>

<span data-ttu-id="6652b-109">Polecenie **cmdlet Get-AzResource** pobiera zasoby platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6652b-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="6652b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6652b-110">EXAMPLES</span></span>

### <span data-ttu-id="6652b-111">Przykład 1. Uzyskiwanie wszystkich zasobów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6652b-111">Example 1: Get all resources in the current subscription</span></span>

```
PS C:\> Get-AzResource | ft

Name    ResourceGroupName  ResourceType                            Location
----    -----------------  ------------                            --------
testVM  testRG             Microsoft.Compute/virtualMachines       westus
disk    testRG             Microsoft.Compute/disks                 westus
nic     testRG             Microsoft.Network/networkInterfaces     westus
nsg     testRG             Microsoft.Network/networkSecurityGroups westus
ip      testRG             Microsoft.Network/publicIPAddresses     westus
vnet    testRG             Microsoft.Network/virtualNetworks       westus
testKV  otherRG            Microsoft.KeyVault/vaults               eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts       eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines       eastus
```

<span data-ttu-id="6652b-112">To polecenie pobiera wszystkie zasoby w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6652b-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="6652b-113">Przykład 2. Uzyskiwanie wszystkich zasobów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="6652b-113">Example 2: Get all resources in a resource group</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName testRG | ft

Name   ResourceGroupName ResourceType                            Location
----   ----------------- ------------                            --------
testVM testRG            Microsoft.Compute/virtualMachines       westus
disk   testRG            Microsoft.Compute/disks                 westus
nic    testRG            Microsoft.Network/networkInterfaces     westus
nsg    testRG            Microsoft.Network/networkSecurityGroups westus
ip     testRG            Microsoft.Network/publicIPAddresses     westus
vnet   testRG            Microsoft.Network/virtualNetworks       westus
```

<span data-ttu-id="6652b-114">To polecenie pobiera wszystkie zasoby w grupie zasobów "testRG".</span><span class="sxs-lookup"><span data-stu-id="6652b-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="6652b-115">Przykład 3. Uzyskiwanie wszystkich zasobów, których grupa zasobów jest odpowiada podanej symbolowi wieloznaczne</span><span class="sxs-lookup"><span data-stu-id="6652b-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="6652b-116">To polecenie pobiera wszystkie zasoby, których grupa zasobów należy jako istoty, z "innymi".</span><span class="sxs-lookup"><span data-stu-id="6652b-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="6652b-117">Przykład 4. Uzyskiwanie wszystkich zasobów o danej nazwie</span><span class="sxs-lookup"><span data-stu-id="6652b-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="6652b-118">To polecenie pobiera wszystkie zasoby, których nazwa zasobu to "testVM".</span><span class="sxs-lookup"><span data-stu-id="6652b-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="6652b-119">Przykład 5. Uzyskiwanie wszystkich zasobów o nazwie takiej jak podany symbol wieloznaczny</span><span class="sxs-lookup"><span data-stu-id="6652b-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="6652b-120">To polecenie pobiera wszystkie zasoby, których nazwa zasobu rozpoczyna się od "testu".</span><span class="sxs-lookup"><span data-stu-id="6652b-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="6652b-121">Przykład 6. Uzyskiwanie wszystkich zasobów danego typu zasobu</span><span class="sxs-lookup"><span data-stu-id="6652b-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="6652b-122">To polecenie pobiera wszystkie zasoby z bieżących subskrypcji, które są maszynami wirtualnymi.</span><span class="sxs-lookup"><span data-stu-id="6652b-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="6652b-123">Przykład 7. Uzyskiwanie zasobu według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="6652b-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="6652b-124">To polecenie pobiera zasób z dostarczonym identyfikatorem zasobu, czyli maszyną wirtualną o nazwie "testVM" w grupie zasobów "testRG".</span><span class="sxs-lookup"><span data-stu-id="6652b-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="6652b-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6652b-125">PARAMETERS</span></span>

### <span data-ttu-id="6652b-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6652b-126">-ApiVersion</span></span>

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

### <span data-ttu-id="6652b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6652b-127">-DefaultProfile</span></span>
<span data-ttu-id="6652b-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6652b-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6652b-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="6652b-129">-ExpandProperties</span></span>
<span data-ttu-id="6652b-130">Jeśli jest to określone, rozszerza właściwości zasobu.</span><span class="sxs-lookup"><span data-stu-id="6652b-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="6652b-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6652b-131">-Name</span></span>
<span data-ttu-id="6652b-132">Nazwy zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="6652b-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="6652b-133">Ten parametr obsługuje symbole wieloznaczne na początku i/lub na końcu ciągu.</span><span class="sxs-lookup"><span data-stu-id="6652b-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="6652b-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="6652b-134">-ODataQuery</span></span>

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

### <span data-ttu-id="6652b-135">— Przed</span><span class="sxs-lookup"><span data-stu-id="6652b-135">-Pre</span></span>

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

### <span data-ttu-id="6652b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6652b-136">-ResourceGroupName</span></span>
<span data-ttu-id="6652b-137">Grupa zasobów, do której są pobierane zasoby.</span><span class="sxs-lookup"><span data-stu-id="6652b-137">The resource group the resource(s) that is retrieved belongs in.</span></span> <span data-ttu-id="6652b-138">Ten parametr obsługuje symbole wieloznaczne na początku i/lub na końcu ciągu.</span><span class="sxs-lookup"><span data-stu-id="6652b-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="6652b-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6652b-139">-ResourceId</span></span>
<span data-ttu-id="6652b-140">Określa w pełni kwalifikowany identyfikator zasobu, jak w poniższym przykładzie. `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="6652b-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6652b-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6652b-141">-ResourceType</span></span>
<span data-ttu-id="6652b-142">Typ zasobu, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="6652b-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="6652b-143">Na przykład Microsoft.Compute/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="6652b-143">For example, Microsoft.Compute/virtualMachines</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6652b-144">— Tag</span><span class="sxs-lookup"><span data-stu-id="6652b-144">-Tag</span></span>

<span data-ttu-id="6652b-145">Pobiera zasoby, które mają określony tag platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6652b-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="6652b-146">Wprowadź tabelę skrótów z klawiszem Name lub klawiszami Nazwa i Wartość.</span><span class="sxs-lookup"><span data-stu-id="6652b-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="6652b-147">Symbole wieloznaczne nie są obsługiwane. "Tag" to para wartości nazwy, która można zastosować do zasobów i grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="6652b-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="6652b-148">Przy użyciu tagów można kategoryzować zasoby( na przykład według działu lub centrum kosztów) albo śledzić notatki lub komentarze dotyczące zasobów.</span><span class="sxs-lookup"><span data-stu-id="6652b-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="6652b-149">Aby dodać tag do zasobu, użyj parametru Tag New-AzResource lub Set-AzResource cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6652b-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="6652b-150">Aby utworzyć wstępnie zdefiniowany tag, użyj New-AzTag cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6652b-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="6652b-151">Aby uzyskać pomoc na dotyczące skrótów tabel w programie Windows PowerShell, uruchom polecenia "Uzyskaj pomoc about_Hashtables".</span><span class="sxs-lookup"><span data-stu-id="6652b-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6652b-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="6652b-152">-TagName</span></span>
<span data-ttu-id="6652b-153">Klucz w tagach zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="6652b-153">The key in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6652b-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="6652b-154">-TagValue</span></span>
<span data-ttu-id="6652b-155">Wartość w tagach zasobów, które mają zostać pobrane.</span><span class="sxs-lookup"><span data-stu-id="6652b-155">The value in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6652b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6652b-156">CommonParameters</span></span>
<span data-ttu-id="6652b-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6652b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6652b-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6652b-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6652b-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6652b-159">INPUTS</span></span>

### <span data-ttu-id="6652b-160">System.String</span><span class="sxs-lookup"><span data-stu-id="6652b-160">System.String</span></span>

## <span data-ttu-id="6652b-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6652b-161">OUTPUTS</span></span>

### <span data-ttu-id="6652b-162">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResource</span><span class="sxs-lookup"><span data-stu-id="6652b-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="6652b-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6652b-163">NOTES</span></span>

## <span data-ttu-id="6652b-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6652b-164">RELATED LINKS</span></span>

[<span data-ttu-id="6652b-165">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="6652b-165">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="6652b-166">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="6652b-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="6652b-167">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="6652b-167">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="6652b-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="6652b-168">Set-AzResource</span></span>](./Set-AzResource.md)