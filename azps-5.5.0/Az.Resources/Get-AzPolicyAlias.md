---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
ms.openlocfilehash: b2881c735caae8f644676b1ee19cb0d80725c13a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186506"
---
# <span data-ttu-id="6bead-101">Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="6bead-101">Get-AzPolicyAlias</span></span>

## <span data-ttu-id="6bead-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bead-102">SYNOPSIS</span></span>
<span data-ttu-id="6bead-103">Get-AzPolicyAlias pobiera i wyprowadza zasoby dostawców platformy Azure, które mają zdefiniowane aliasy i są zgodne z określonymi wartościami parametrów.</span><span class="sxs-lookup"><span data-stu-id="6bead-103">Get-AzPolicyAlias retrieves and outputs Azure provider resource types that have aliases defined and match the given parameter values.</span></span> <span data-ttu-id="6bead-104">Jeśli nie podano parametrów, zostaną wyprowadzne wszystkie typy zasobów dostawcy zawierające alias.</span><span class="sxs-lookup"><span data-stu-id="6bead-104">If no parameters are provided, all provider resource types that contain an alias will be output.</span></span>
<span data-ttu-id="6bead-105">Przełącznik -ListAvailable modyfikuje to zachowanie, wymieniając wszystkie pasujące typy zasobów, w tym te bez aliasów.</span><span class="sxs-lookup"><span data-stu-id="6bead-105">The -ListAvailable switch modifies this behavior by listing all matching resource types including those without aliases.</span></span>

## <span data-ttu-id="6bead-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6bead-106">SYNTAX</span></span>

```
Get-AzPolicyAlias [-NamespaceMatch <String>] [-ResourceTypeMatch <String>] [-AliasMatch <String>]
 [-PathMatch <String>] [-ApiVersionMatch <String>] [-LocationMatch <String>] [-ListAvailable]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bead-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6bead-107">DESCRIPTION</span></span>
<span data-ttu-id="6bead-108">Polecenie **cmdlet Get-AzPolicyAlias** pobiera listę aliasów zasad.</span><span class="sxs-lookup"><span data-stu-id="6bead-108">The **Get-AzPolicyAlias** cmdlet gets a listing of policy aliases.</span></span>
<span data-ttu-id="6bead-109">Aliasy zasad są używane przez zasady platformy Azure do odwoływać się do właściwości typu zasobu.</span><span class="sxs-lookup"><span data-stu-id="6bead-109">Policy aliases are used by Azure Policy to refer to resource type properties.</span></span>
<span data-ttu-id="6bead-110">Dostępne są parametry ograniczające pozycje na liście przez dopasowywanie różnych właściwości typu zasobu lub jego aliasów.</span><span class="sxs-lookup"><span data-stu-id="6bead-110">Parameters are provided that limit items in the listing by matching various properties of the resource type or its aliases.</span></span>
<span data-ttu-id="6bead-111">Podana wartość dopasowania jest dopasowana, jeśli ciąg docelowy zawiera ciąg, w przypadku porównania bez uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="6bead-111">A given match value matches if the target string contains it using case insensitive comparison.</span></span>

## <span data-ttu-id="6bead-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6bead-112">EXAMPLES</span></span>

### <span data-ttu-id="6bead-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6bead-113">Example 1</span></span>
```powershell
PS C:\> Get-AzPolicyAlias

Namespace                     ResourceType                                   Aliases
---------                     ------------                                   -------
Microsoft.AnalysisServices    servers                                        {Microsoft.AnalysisServices/servers/state, Microsoft.AnalysisServices/s...
Microsoft.Authorization       roleAssignments                                {Microsoft.Authorization/roleAssignments/roleDefinitionId, Microsoft.Au...
Microsoft.Authorization       roleDefinitions                                {Microsoft.Authorization/roleDefinitions/type, Microsoft.Authorization/...

...                           ...                                            ...

Microsoft.Web                 hostingEnvironments                            {Microsoft.Web/hostingEnvironments/clusterSettings[*].name, Microsoft.W...
Microsoft.Web                 sites/config                                   {Microsoft.Web/sites/config/httpLoggingEnabled, Microsoft.Web/sites/con...
Microsoft.GuestConfiguration  guestConfigurationAssignments                  {Microsoft.GuestConfiguration/guestConfigurationAssignments/complianceS...


PS C:\>
```

<span data-ttu-id="6bead-114">Lista wszystkich typów zasobów dostawcy, które mają alias.</span><span class="sxs-lookup"><span data-stu-id="6bead-114">Lists all provider resource types that have an alias.</span></span>

### <span data-ttu-id="6bead-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6bead-115">Example 2</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ListAvailable

Namespace                                ResourceType                                                        Aliases
---------                                ------------                                                        -------

...                                      ...                                                                 ...

Microsoft.AlertsManagement               operations                                                          {}
Microsoft.AnalysisServices               servers                                                             {Microsoft.AnalysisServices/servers/sta...
Microsoft.AnalysisServices               locations                                                           {}

...                                      ...                                                                 ...


PS C:\>
```

<span data-ttu-id="6bead-116">Lista wszystkich typów zasobów dostawcy, w tym tych bez aliasów.</span><span class="sxs-lookup"><span data-stu-id="6bead-116">Lists all provider resource types, including those without aliases.</span></span>

### <span data-ttu-id="6bead-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="6bead-117">Example 3</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -NamespaceMatch 'compute'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...
Microsoft.Compute disks                              {Microsoft.Compute/imagePublisher, Microsoft.Compute/imageOffer, Microsoft.Compute/imageSku, Mi...


PS C:\>
```

<span data-ttu-id="6bead-118">Lista wszystkich typów zasobów dostawcy, których przestrzeń nazw odpowiada "obliczaniu" i zawiera alias.</span><span class="sxs-lookup"><span data-stu-id="6bead-118">Lists all provider resource types whose namespace matches 'compute' and contain an alias.</span></span>

### <span data-ttu-id="6bead-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="6bead-119">Example 4</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ResourceTypeMatch 'virtual'

Namespace         ResourceType                           Aliases
---------         ------------                           -------
Microsoft.Compute virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Micro...
Microsoft.Compute virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualM...
Microsoft.Compute virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleS...
Microsoft.Compute virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/...
Microsoft.Network virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGateway...
Microsoft.Network virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetworks...
Microsoft.Network virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql     servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers/vi...


PS C:\>
```

<span data-ttu-id="6bead-120">Lista wszystkich typów zasobów dostawcy, których typ zasobu jest "wirtualny" i zawiera alias.</span><span class="sxs-lookup"><span data-stu-id="6bead-120">Lists all provider resource types whose resource type matches 'virtual' and contain an alias.</span></span>

### <span data-ttu-id="6bead-121">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="6bead-121">Example 5</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ResourceTypeMatch 'virtual' -ListAvailable

Namespace                    ResourceType                                               Aliases
---------                    ------------                                               -------

...                          ...                                                        ...

Microsoft.KeyVault           locations/deleteVirtualNetworkOrSubnets                    {}
Microsoft.Network            virtualNetworks                                            {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id,...
Microsoft.Network            virtualNetworkGateways                                     {Microsoft.Network/virtualNetworkGateways/sku.name, Microsof...
Microsoft.Network            locations/virtualNetworkAvailableEndpointServices          {}

...                          ...                                                        ...


PS C:\>
```

<span data-ttu-id="6bead-122">Lista wszystkich typów zasobów dostawcy, których typ zasobu jest "wirtualny", łącznie z tymi, które nie mają aliasów.</span><span class="sxs-lookup"><span data-stu-id="6bead-122">Lists all provider resource types whose resource type matches 'virtual', including those without aliases.</span></span>

### <span data-ttu-id="6bead-123">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="6bead-123">Example 6</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -NamespaceMatch 'compute' -ResourceTypeMatch 'virtual'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...


PS C:\>
```

<span data-ttu-id="6bead-124">Lista wszystkich typów zasobów dostawcy, których przestrzeń nazw jest do niej dosyć "obliczeniowa", a typ zasobu jest "wirtualny" i zawiera alias.</span><span class="sxs-lookup"><span data-stu-id="6bead-124">Lists all provider resource types whose namespace matches 'compute' and resource type matches 'virtual' and contain an alias.</span></span>
<span data-ttu-id="6bead-125">Uwaga: —NamespaceMatch i -ResourceTypeMatch oferują dopasowania wyłączności, podczas gdy pozostałe są dostępne dla wszystkich.</span><span class="sxs-lookup"><span data-stu-id="6bead-125">Note: -NamespaceMatch and -ResourceTypeMatch provide exclusive matches, whereas the others are inclusive.</span></span>

### <span data-ttu-id="6bead-126">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="6bead-126">Example 7</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -AliasMatch 'virtual'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="6bead-127">Lista wszystkich typów zasobów dostawcy, które zawierają alias odpowiadający "wirtualny".</span><span class="sxs-lookup"><span data-stu-id="6bead-127">Lists all provider resource types that contain an alias matching 'virtual'.</span></span>

### <span data-ttu-id="6bead-128">Przykład 8</span><span class="sxs-lookup"><span data-stu-id="6bead-128">Example 8</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -AliasMatch 'virtual' -PathMatch 'network'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    networkInterfaces                      {Microsoft.Network/networkInterfaces/ipconfigurations[*].subnet.id, Microsoft.Network/ne...
Microsoft.Network    networkSecurityGroups                  {Microsoft.Network/networkSecurityGroups/securityRules[*].protocol, Microsoft.Network/ne...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="6bead-129">Lista wszystkich typów zasobów dostawcy, które zawierają alias odpowiadający "wirtualny" lub alias o ścieżce zgodnej z "siecią".</span><span class="sxs-lookup"><span data-stu-id="6bead-129">Lists all provider resource types that contain an alias matching 'virtual' or an alias with a path matching 'network'.</span></span>

### <span data-ttu-id="6bead-130">Przykład 9</span><span class="sxs-lookup"><span data-stu-id="6bead-130">Example 9</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ApiVersionMatch 'alpha'

Namespace          ResourceType        Aliases
---------          ------------        -------
Microsoft.Cache    Redis               {Microsoft.Cache/Redis/sku.name, Microsoft.Cache/Redis/sku.family, Microsoft.Cache/Redis/sku.capacity, Micros...
Microsoft.Cache    Redis/firewallrules {Microsoft.Cache/Redis/firewallrules/startIP, Microsoft.Cache/Redis/firewallrules/endIP}
Microsoft.Security alerts              {Microsoft.Security/alerts/state}
Microsoft.Security pricings            {Microsoft.Security/pricings/pricingTier}
Microsoft.Security complianceResults   {Microsoft.Security/complianceResults/resourceStatus}


PS C:\>
```

<span data-ttu-id="6bead-131">Lista wszystkich typów zasobów dostawcy z wersją interfejsu api alfa lub zawierającą alias z wersją interfejsu api alfa.</span><span class="sxs-lookup"><span data-stu-id="6bead-131">Lists all provider resource types with alpha api version or containing an alias with an alpha api version.</span></span>

## <span data-ttu-id="6bead-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bead-132">PARAMETERS</span></span>

### <span data-ttu-id="6bead-133">-AliasMatch</span><span class="sxs-lookup"><span data-stu-id="6bead-133">-AliasMatch</span></span>
<span data-ttu-id="6bead-134">Uwzględnia elementy wyjściowe z aliasami, których nazwa jest taka sama jak ta wartość.</span><span class="sxs-lookup"><span data-stu-id="6bead-134">Includes in the output items with aliases whose name matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Alias

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bead-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6bead-135">-ApiVersion</span></span>
<span data-ttu-id="6bead-136">Po jego skonfigurowaniu wskazuje wersję interfejsu API dostawcy zasobów, która ma być dostępna.</span><span class="sxs-lookup"><span data-stu-id="6bead-136">When set, indicates the version of the resource provider API to use.</span></span> <span data-ttu-id="6bead-137">Jeśli nie zostanie określona, wersja interfejsu API jest automatycznie określana jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="6bead-137">If not specified, the API version is automatically determined as the latest available.</span></span>


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

### <span data-ttu-id="6bead-138">-ApiVersionMatch</span><span class="sxs-lookup"><span data-stu-id="6bead-138">-ApiVersionMatch</span></span>
<span data-ttu-id="6bead-139">Uwzględnia elementy wyjściowe, których typy lub aliasy zasobów mają pasującą wersję interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="6bead-139">Includes in the output items whose resource types or aliases have a matching api version.</span></span>


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

### <span data-ttu-id="6bead-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bead-140">-DefaultProfile</span></span>
<span data-ttu-id="6bead-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6bead-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6bead-142">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="6bead-142">-ListAvailable</span></span>
<span data-ttu-id="6bead-143">Uwzględnia pasujące elementy wyjściowe z aliasami i bez nich.</span><span class="sxs-lookup"><span data-stu-id="6bead-143">Includes in the output matching items with and without aliases.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: ShowAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bead-144">-LocationMatch</span><span class="sxs-lookup"><span data-stu-id="6bead-144">-LocationMatch</span></span>
<span data-ttu-id="6bead-145">Uwzględnia elementy wyjściowe, których typy zasobów mają pasującą lokalizację.</span><span class="sxs-lookup"><span data-stu-id="6bead-145">Includes in the output items whose resource types have a matching location.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bead-146">-NamespaceMatch</span><span class="sxs-lookup"><span data-stu-id="6bead-146">-NamespaceMatch</span></span>
<span data-ttu-id="6bead-147">Ogranicza dane wyjściowe do elementów, których przestrzeń nazw odpowiada tej wartości.</span><span class="sxs-lookup"><span data-stu-id="6bead-147">Limits the output to items whose namespace matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, Namespace

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bead-148">-PathMatch</span><span class="sxs-lookup"><span data-stu-id="6bead-148">-PathMatch</span></span>
<span data-ttu-id="6bead-149">Uwzględnia elementy wyjściowe z aliasami zawierającymi ścieżkę, która odpowiada tej wartości.</span><span class="sxs-lookup"><span data-stu-id="6bead-149">Includes in the output items with aliases containing a path that matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bead-150">— Przed</span><span class="sxs-lookup"><span data-stu-id="6bead-150">-Pre</span></span>
<span data-ttu-id="6bead-151">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="6bead-151">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>


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

### <span data-ttu-id="6bead-152">-ResourceTypeMatch</span><span class="sxs-lookup"><span data-stu-id="6bead-152">-ResourceTypeMatch</span></span>
<span data-ttu-id="6bead-153">Ogranicza dane wyjściowe do elementów, których typ zasobu odpowiada tej wartości.</span><span class="sxs-lookup"><span data-stu-id="6bead-153">Limits the output to items whose resource type matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceType, Resource

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bead-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bead-154">CommonParameters</span></span>
<span data-ttu-id="6bead-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bead-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bead-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bead-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bead-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6bead-157">INPUTS</span></span>

### <span data-ttu-id="6bead-158">Brak</span><span class="sxs-lookup"><span data-stu-id="6bead-158">None</span></span>

## <span data-ttu-id="6bead-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6bead-159">OUTPUTS</span></span>

### <span data-ttu-id="6bead-160">Microsoft.Azure.Commands.ResourceManager.Cmdlet.Implementation.PsResourceProviderAlias</span><span class="sxs-lookup"><span data-stu-id="6bead-160">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span></span>

## <span data-ttu-id="6bead-161">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6bead-161">NOTES</span></span>

* <span data-ttu-id="6bead-162">Aby rozwinąć aliasy lub dowolną inną właściwość, przekieruj dane wyjściowe `select -ExpandProperty <property>` do.</span><span class="sxs-lookup"><span data-stu-id="6bead-162">To expand the Aliases or any other property, pipe the output to `select -ExpandProperty <property>`.</span></span> <span data-ttu-id="6bead-163">Na przykład: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span><span class="sxs-lookup"><span data-stu-id="6bead-163">For example: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span></span>

* <span data-ttu-id="6bead-164">Dodatkowe właściwości są dostępne w wyniku i mogą być wyświetlane, rurując dane wyjściowe `Format-List` do.</span><span class="sxs-lookup"><span data-stu-id="6bead-164">Additional properties are available in the output and can be displayed by piping the output to `Format-List`.</span></span> <span data-ttu-id="6bead-165">Na przykład: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span><span class="sxs-lookup"><span data-stu-id="6bead-165">For example: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span></span>

## <span data-ttu-id="6bead-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6bead-166">RELATED LINKS</span></span>
