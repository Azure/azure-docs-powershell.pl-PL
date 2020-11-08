---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
ms.openlocfilehash: b2881c735caae8f644676b1ee19cb0d80725c13a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223191"
---
# <span data-ttu-id="13600-101">Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="13600-101">Get-AzPolicyAlias</span></span>

## <span data-ttu-id="13600-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13600-102">SYNOPSIS</span></span>
<span data-ttu-id="13600-103">Get-AzPolicyAlias pobiera i wyprowadza typy zasobów usług Azure Provider, dla których zdefiniowano aliasy i pasują do podanych wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="13600-103">Get-AzPolicyAlias retrieves and outputs Azure provider resource types that have aliases defined and match the given parameter values.</span></span> <span data-ttu-id="13600-104">Jeśli nie zostaną podane żadne parametry, wszystkie typy zasobów dostawców zawierające alias będą wyprowadzane.</span><span class="sxs-lookup"><span data-stu-id="13600-104">If no parameters are provided, all provider resource types that contain an alias will be output.</span></span>
<span data-ttu-id="13600-105">Przełącznik-ListAvailable modyfikuje to zachowanie, wyświetlając wszystkie pasujące typy zasobów, w tym te, które nie mają aliasów.</span><span class="sxs-lookup"><span data-stu-id="13600-105">The -ListAvailable switch modifies this behavior by listing all matching resource types including those without aliases.</span></span>

## <span data-ttu-id="13600-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13600-106">SYNTAX</span></span>

```
Get-AzPolicyAlias [-NamespaceMatch <String>] [-ResourceTypeMatch <String>] [-AliasMatch <String>]
 [-PathMatch <String>] [-ApiVersionMatch <String>] [-LocationMatch <String>] [-ListAvailable]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13600-107">Opis</span><span class="sxs-lookup"><span data-stu-id="13600-107">DESCRIPTION</span></span>
<span data-ttu-id="13600-108">Polecenie cmdlet **Get-AzPolicyAlias** pobiera listę aliasów zasad.</span><span class="sxs-lookup"><span data-stu-id="13600-108">The **Get-AzPolicyAlias** cmdlet gets a listing of policy aliases.</span></span>
<span data-ttu-id="13600-109">Aliasy zasad są używane przez zasady platformy Azure do odwoływania się do właściwości typu zasobu.</span><span class="sxs-lookup"><span data-stu-id="13600-109">Policy aliases are used by Azure Policy to refer to resource type properties.</span></span>
<span data-ttu-id="13600-110">Podane są parametry, które ograniczają liczbę elementów na liście, dopasowując różne właściwości typu zasobu lub aliasy.</span><span class="sxs-lookup"><span data-stu-id="13600-110">Parameters are provided that limit items in the listing by matching various properties of the resource type or its aliases.</span></span>
<span data-ttu-id="13600-111">Podana wartość dopasowania jest zgodna, jeśli ciąg docelowy zawiera wyrażenie uwzględniające wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="13600-111">A given match value matches if the target string contains it using case insensitive comparison.</span></span>

## <span data-ttu-id="13600-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13600-112">EXAMPLES</span></span>

### <span data-ttu-id="13600-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13600-113">Example 1</span></span>
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

<span data-ttu-id="13600-114">Zawiera listę wszystkich typów zasobów dostawców, które mają alias.</span><span class="sxs-lookup"><span data-stu-id="13600-114">Lists all provider resource types that have an alias.</span></span>

### <span data-ttu-id="13600-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="13600-115">Example 2</span></span>
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

<span data-ttu-id="13600-116">Wyświetla wszystkie typy zasobów dostawców, w tym te bez aliasów.</span><span class="sxs-lookup"><span data-stu-id="13600-116">Lists all provider resource types, including those without aliases.</span></span>

### <span data-ttu-id="13600-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="13600-117">Example 3</span></span>
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

<span data-ttu-id="13600-118">Wyświetla listę wszystkich typów zasobów dostawców, których przestrzeń nazw pasuje do "obliczenia" i zawiera alias.</span><span class="sxs-lookup"><span data-stu-id="13600-118">Lists all provider resource types whose namespace matches 'compute' and contain an alias.</span></span>

### <span data-ttu-id="13600-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="13600-119">Example 4</span></span>
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

<span data-ttu-id="13600-120">Wyświetla listę wszystkich typów zasobów dostawców, których typ zasobu odpowiada "wirtualny" i zawiera alias.</span><span class="sxs-lookup"><span data-stu-id="13600-120">Lists all provider resource types whose resource type matches 'virtual' and contain an alias.</span></span>

### <span data-ttu-id="13600-121">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="13600-121">Example 5</span></span>
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

<span data-ttu-id="13600-122">Wyświetla listę wszystkich typów zasobów dostawców, których typ zasobu jest zgodny z typem "wirtualny", łącznie z tymi, które nie są aliasami.</span><span class="sxs-lookup"><span data-stu-id="13600-122">Lists all provider resource types whose resource type matches 'virtual', including those without aliases.</span></span>

### <span data-ttu-id="13600-123">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="13600-123">Example 6</span></span>
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

<span data-ttu-id="13600-124">Wyświetla listę wszystkich typów zasobów dostawców, których przestrzeń nazw pasuje do "obliczeniowa", oraz typ zasobu pasuje do elementu "Virtual" i zawierają alias.</span><span class="sxs-lookup"><span data-stu-id="13600-124">Lists all provider resource types whose namespace matches 'compute' and resource type matches 'virtual' and contain an alias.</span></span>
<span data-ttu-id="13600-125">Uwaga:-NamespaceMatch i-ResourceTypeMatch zapewniają wykluczające się dopasowania, podczas gdy inne są dostępne.</span><span class="sxs-lookup"><span data-stu-id="13600-125">Note: -NamespaceMatch and -ResourceTypeMatch provide exclusive matches, whereas the others are inclusive.</span></span>

### <span data-ttu-id="13600-126">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="13600-126">Example 7</span></span>
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

<span data-ttu-id="13600-127">Wyświetla listę wszystkich typów zasobów dostawców, które zawierają alias pasujący do "Virtual".</span><span class="sxs-lookup"><span data-stu-id="13600-127">Lists all provider resource types that contain an alias matching 'virtual'.</span></span>

### <span data-ttu-id="13600-128">Przykład 8</span><span class="sxs-lookup"><span data-stu-id="13600-128">Example 8</span></span>
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

<span data-ttu-id="13600-129">Zawiera listę wszystkich typów zasobów dostawców, które zawierają alias zgodny z instrukcją "Virtual" lub alias z ścieżką odpowiadającą "Network".</span><span class="sxs-lookup"><span data-stu-id="13600-129">Lists all provider resource types that contain an alias matching 'virtual' or an alias with a path matching 'network'.</span></span>

### <span data-ttu-id="13600-130">Przykład 9</span><span class="sxs-lookup"><span data-stu-id="13600-130">Example 9</span></span>
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

<span data-ttu-id="13600-131">Zawiera listę wszystkich typów zasobów dostawcy z wersją API Alpha lub zawierającą alias z wersją interfejsu API Alpha.</span><span class="sxs-lookup"><span data-stu-id="13600-131">Lists all provider resource types with alpha api version or containing an alias with an alpha api version.</span></span>

## <span data-ttu-id="13600-132">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13600-132">PARAMETERS</span></span>

### <span data-ttu-id="13600-133">-AliasMatch</span><span class="sxs-lookup"><span data-stu-id="13600-133">-AliasMatch</span></span>
<span data-ttu-id="13600-134">Umożliwia uwzględnienie w elementach wyjściowych aliasów, których nazwa jest zgodna z tą wartością.</span><span class="sxs-lookup"><span data-stu-id="13600-134">Includes in the output items with aliases whose name matches this value.</span></span>


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

### <span data-ttu-id="13600-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="13600-135">-ApiVersion</span></span>
<span data-ttu-id="13600-136">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="13600-136">When set, indicates the version of the resource provider API to use.</span></span> <span data-ttu-id="13600-137">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="13600-137">If not specified, the API version is automatically determined as the latest available.</span></span>


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

### <span data-ttu-id="13600-138">-ApiVersionMatch</span><span class="sxs-lookup"><span data-stu-id="13600-138">-ApiVersionMatch</span></span>
<span data-ttu-id="13600-139">Obejmuje elementy wyjściowe, których typy zasobów lub aliasy mają zgodne wersje API.</span><span class="sxs-lookup"><span data-stu-id="13600-139">Includes in the output items whose resource types or aliases have a matching api version.</span></span>


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

### <span data-ttu-id="13600-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13600-140">-DefaultProfile</span></span>
<span data-ttu-id="13600-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13600-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="13600-142">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="13600-142">-ListAvailable</span></span>
<span data-ttu-id="13600-143">Uwzględnia elementy, które są zgodne z aliasami lub bez.</span><span class="sxs-lookup"><span data-stu-id="13600-143">Includes in the output matching items with and without aliases.</span></span>


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

### <span data-ttu-id="13600-144">-LocationMatch</span><span class="sxs-lookup"><span data-stu-id="13600-144">-LocationMatch</span></span>
<span data-ttu-id="13600-145">Obejmuje elementy wyjściowe, dla których typy zasobów mają pasującą lokalizację.</span><span class="sxs-lookup"><span data-stu-id="13600-145">Includes in the output items whose resource types have a matching location.</span></span>


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

### <span data-ttu-id="13600-146">-NamespaceMatch</span><span class="sxs-lookup"><span data-stu-id="13600-146">-NamespaceMatch</span></span>
<span data-ttu-id="13600-147">Ograniczanie wyników do elementów, których przestrzeń nazw pasuje do tej wartości.</span><span class="sxs-lookup"><span data-stu-id="13600-147">Limits the output to items whose namespace matches this value.</span></span>


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

### <span data-ttu-id="13600-148">-PathMatch</span><span class="sxs-lookup"><span data-stu-id="13600-148">-PathMatch</span></span>
<span data-ttu-id="13600-149">Umożliwia uwzględnienie w elementach wyjściowych aliasów zawierających ścieżkę pasującą do tej wartości.</span><span class="sxs-lookup"><span data-stu-id="13600-149">Includes in the output items with aliases containing a path that matches this value.</span></span>


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

### <span data-ttu-id="13600-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="13600-150">-Pre</span></span>
<span data-ttu-id="13600-151">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="13600-151">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>


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

### <span data-ttu-id="13600-152">-ResourceTypeMatch</span><span class="sxs-lookup"><span data-stu-id="13600-152">-ResourceTypeMatch</span></span>
<span data-ttu-id="13600-153">Ogranicza liczbę danych wyjściowych do elementów, których typ zasobu pasuje do tej wartości.</span><span class="sxs-lookup"><span data-stu-id="13600-153">Limits the output to items whose resource type matches this value.</span></span>


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

### <span data-ttu-id="13600-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13600-154">CommonParameters</span></span>
<span data-ttu-id="13600-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13600-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13600-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13600-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13600-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13600-157">INPUTS</span></span>

### <span data-ttu-id="13600-158">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="13600-158">None</span></span>

## <span data-ttu-id="13600-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13600-159">OUTPUTS</span></span>

### <span data-ttu-id="13600-160">Microsoft. Azure. Commands. ResourceManager. cmdlet. implementacja. PsResourceProviderAlias</span><span class="sxs-lookup"><span data-stu-id="13600-160">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span></span>

## <span data-ttu-id="13600-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13600-161">NOTES</span></span>

* <span data-ttu-id="13600-162">Aby rozwinąć aliasy lub dowolną inną właściwość, przeprowadź połączenie z danymi wyjściowymi `select -ExpandProperty <property>` .</span><span class="sxs-lookup"><span data-stu-id="13600-162">To expand the Aliases or any other property, pipe the output to `select -ExpandProperty <property>`.</span></span> <span data-ttu-id="13600-163">Na przykład: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span><span class="sxs-lookup"><span data-stu-id="13600-163">For example: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span></span>

* <span data-ttu-id="13600-164">Dodatkowe właściwości są dostępne w wynikach i można je wyświetlić, przechodząc do tego wyjścia `Format-List` .</span><span class="sxs-lookup"><span data-stu-id="13600-164">Additional properties are available in the output and can be displayed by piping the output to `Format-List`.</span></span> <span data-ttu-id="13600-165">Na przykład: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span><span class="sxs-lookup"><span data-stu-id="13600-165">For example: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span></span>

## <span data-ttu-id="13600-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13600-166">RELATED LINKS</span></span>
