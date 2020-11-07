---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: de91566be3c9bcd62f28dbcba80409622e86a4b5
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "93719695"
---
# <span data-ttu-id="c4592-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="c4592-101">Get-AzResource</span></span>

## <span data-ttu-id="c4592-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4592-102">SYNOPSIS</span></span>

<span data-ttu-id="c4592-103">Pobiera zasoby.</span><span class="sxs-lookup"><span data-stu-id="c4592-103">Gets resources.</span></span>

## <span data-ttu-id="c4592-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4592-104">SYNTAX</span></span>

### <span data-ttu-id="c4592-105">ByTagNameValueParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c4592-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4592-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c4592-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4592-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4592-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4592-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c4592-108">DESCRIPTION</span></span>

<span data-ttu-id="c4592-109">Polecenie cmdlet **Get-AzResource** umożliwia pobieranie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c4592-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="c4592-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4592-110">EXAMPLES</span></span>

### <span data-ttu-id="c4592-111">Przykład 1. pobieranie wszystkich zasobów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c4592-111">Example 1: Get all resources in the current subscription</span></span>

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

<span data-ttu-id="c4592-112">To polecenie umożliwia pobieranie wszystkich zasobów w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c4592-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="c4592-113">Przykład 2: pobieranie wszystkich zasobów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="c4592-113">Example 2: Get all resources in a resource group</span></span>

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

<span data-ttu-id="c4592-114">To polecenie umożliwia pobieranie wszystkich zasobów z grupy zasobów "testRG".</span><span class="sxs-lookup"><span data-stu-id="c4592-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="c4592-115">Przykład 3: pobieranie wszystkich zasobów, których Grupa zasobów odpowiada podanemu symbolowi wieloznacznemu</span><span class="sxs-lookup"><span data-stu-id="c4592-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="c4592-116">To polecenie powoduje wyświetlenie wszystkich zasobów, w których Grupa zasobów należy do "innych".</span><span class="sxs-lookup"><span data-stu-id="c4592-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="c4592-117">Przykład 4: pobieranie wszystkich zasobów o podanej nazwie</span><span class="sxs-lookup"><span data-stu-id="c4592-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

<span data-ttu-id="c4592-118">To polecenie pobiera wszystkie zasoby, których nazwa zasobu to "testVM".</span><span class="sxs-lookup"><span data-stu-id="c4592-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="c4592-119">Przykład 5: pobieranie wszystkich zasobów, których nazwa jest zgodna z podanym symbolem wieloznacznym</span><span class="sxs-lookup"><span data-stu-id="c4592-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="c4592-120">To polecenie pobiera wszystkie zasoby, których nazwa zasobu zaczyna się od ciągu "test".</span><span class="sxs-lookup"><span data-stu-id="c4592-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="c4592-121">Przykład 6: pobieranie wszystkich zasobów określonego typu zasobu</span><span class="sxs-lookup"><span data-stu-id="c4592-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="c4592-122">To polecenie umożliwia pobieranie wszystkich zasobów w bieżących abonamentach, które są maszynami wirtualnymi.</span><span class="sxs-lookup"><span data-stu-id="c4592-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="c4592-123">Przykład 7: Pobieranie zasobu według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="c4592-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

<span data-ttu-id="c4592-124">To polecenie pobiera zasób z podanym identyfikatorem zasobu, który jest maszyną wirtualną o nazwie "testVM" w grupie zasobów "testRG".</span><span class="sxs-lookup"><span data-stu-id="c4592-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="c4592-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4592-125">PARAMETERS</span></span>

### <span data-ttu-id="c4592-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c4592-126">-ApiVersion</span></span>

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

### <span data-ttu-id="c4592-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4592-127">-DefaultProfile</span></span>
<span data-ttu-id="c4592-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c4592-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4592-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="c4592-129">-ExpandProperties</span></span>
<span data-ttu-id="c4592-130">Gdy ta właściwość jest określona, rozwija właściwości zasobu.</span><span class="sxs-lookup"><span data-stu-id="c4592-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="c4592-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c4592-131">-Name</span></span>
<span data-ttu-id="c4592-132">Nazwa zasobu, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="c4592-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="c4592-133">Ten parametr obsługuje symbole wieloznaczne na początku i/lub końcu ciągu.</span><span class="sxs-lookup"><span data-stu-id="c4592-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

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

### <span data-ttu-id="c4592-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="c4592-134">-ODataQuery</span></span>

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

### <span data-ttu-id="c4592-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="c4592-135">-Pre</span></span>

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

### <span data-ttu-id="c4592-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4592-136">-ResourceGroupName</span></span>
<span data-ttu-id="c4592-137">Grupa zasobów, do których należą zasoby retireved.</span><span class="sxs-lookup"><span data-stu-id="c4592-137">The resource group the resource(s) that is retireved belongs in.</span></span> <span data-ttu-id="c4592-138">Ten parametr obsługuje symbole wieloznaczne na początku i/lub końcu ciągu.</span><span class="sxs-lookup"><span data-stu-id="c4592-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

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

### <span data-ttu-id="c4592-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4592-139">-ResourceId</span></span>
<span data-ttu-id="c4592-140">Określa w pełni kwalifikowany identyfikator zasobu, tak jak w poniższym przykładzie `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="c4592-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

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

### <span data-ttu-id="c4592-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c4592-141">-ResourceType</span></span>
<span data-ttu-id="c4592-142">Typ zasobu, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="c4592-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="c4592-143">Na przykład Microsoft. COMPUTE/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="c4592-143">For example, Microsoft.Compute/virtualMachines</span></span>

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

### <span data-ttu-id="c4592-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="c4592-144">-Tag</span></span>

<span data-ttu-id="c4592-145">Pobiera zasoby, które mają określony tag platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c4592-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="c4592-146">Wprowadź tabelę skrótów zawierającą klucz nazwy lub klucze Name oraz Value.</span><span class="sxs-lookup"><span data-stu-id="c4592-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="c4592-147">Symbole wieloznaczne nie są obsługiwane. "Tag" to para nazwa-wartość, którą można stosować do zasobów i grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4592-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="c4592-148">Za pomocą znaczników można klasyfikować zasoby, na przykład według działów lub MPK, a także śledzić notatki i komentarze dotyczące zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4592-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="c4592-149">Aby dodać znacznik do zasobu, użyj parametru tag polecenia cmdlet New-AzResource lub Set-AzResource.</span><span class="sxs-lookup"><span data-stu-id="c4592-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="c4592-150">Aby utworzyć wstępnie zdefiniowany znacznik, użyj polecenia cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="c4592-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="c4592-151">Aby uzyskać pomoc dotyczącą tabel skrótów w programie Windows PowerShell, uruchom polecenie "Get-Help about_Hashtables".</span><span class="sxs-lookup"><span data-stu-id="c4592-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

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

### <span data-ttu-id="c4592-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="c4592-152">-TagName</span></span>
<span data-ttu-id="c4592-153">Klucz znacznika zasobów, które mają zostać pobrane.</span><span class="sxs-lookup"><span data-stu-id="c4592-153">The key in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="c4592-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="c4592-154">-TagValue</span></span>
<span data-ttu-id="c4592-155">Wartość znacznika zasobów, które mają zostać pobrane.</span><span class="sxs-lookup"><span data-stu-id="c4592-155">The value in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="c4592-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4592-156">CommonParameters</span></span>
<span data-ttu-id="c4592-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4592-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4592-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4592-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4592-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4592-159">INPUTS</span></span>

### <span data-ttu-id="c4592-160">System. String</span><span class="sxs-lookup"><span data-stu-id="c4592-160">System.String</span></span>

## <span data-ttu-id="c4592-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4592-161">OUTPUTS</span></span>

### <span data-ttu-id="c4592-162">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResource</span><span class="sxs-lookup"><span data-stu-id="c4592-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="c4592-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4592-163">NOTES</span></span>

## <span data-ttu-id="c4592-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4592-164">RELATED LINKS</span></span>

[<span data-ttu-id="c4592-165">Przenieś — AzResource</span><span class="sxs-lookup"><span data-stu-id="c4592-165">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="c4592-166">Nowe — AzResource</span><span class="sxs-lookup"><span data-stu-id="c4592-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="c4592-167">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="c4592-167">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="c4592-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="c4592-168">Set-AzResource</span></span>](./Set-AzResource.md)