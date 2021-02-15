---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: baff896564d8f3b8d70f69b190bc3429d4f465c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242163"
---
# <span data-ttu-id="d84b0-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="d84b0-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="d84b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d84b0-102">SYNOPSIS</span></span>
<span data-ttu-id="d84b0-103">Dodaj rozszerzenie maszyny wirtualnej do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="d84b0-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="d84b0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d84b0-104">SYNTAX</span></span>

### <span data-ttu-id="d84b0-105">ByObj (Domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d84b0-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d84b0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d84b0-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d84b0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d84b0-107">DESCRIPTION</span></span>
<span data-ttu-id="d84b0-108">Dodaj rozszerzenie maszyny wirtualnej do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="d84b0-108">Add vm extension to the node type.</span></span> <span data-ttu-id="d84b0-109">Spowoduje to dodanie rozszerzenia do zasobu zestawu skal maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="d84b0-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="d84b0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d84b0-110">EXAMPLES</span></span>

### <span data-ttu-id="d84b0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d84b0-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="d84b0-112">To polecenie powoduje dodanie rozszerzenia do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="d84b0-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="d84b0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d84b0-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="d84b0-114">To polecenie dodaje rozszerzenie z ustawieniami i ustawieniami chronionymi do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="d84b0-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="d84b0-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d84b0-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="d84b0-116">To polecenie dodaje rozszerzenie do typu węzła z połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="d84b0-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="d84b0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d84b0-117">PARAMETERS</span></span>

### <span data-ttu-id="d84b0-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d84b0-118">-AsJob</span></span>
<span data-ttu-id="d84b0-119">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="d84b0-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d84b0-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d84b0-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d84b0-121">Wskazuje, czy rozszerzenie powinno używać nowszej wersji pomocniczej, jeśli jest dostępne w momencie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d84b0-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="d84b0-122">Jednak po wdrożeniu rozszerzenie nie będzie uaktualniać wersji pomocniczych, o ile nie zostanie ponownie wdrożone, nawet jeśli ta właściwość jest ustawiona na prawda.</span><span class="sxs-lookup"><span data-stu-id="d84b0-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="d84b0-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d84b0-123">-ClusterName</span></span>
<span data-ttu-id="d84b0-124">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="d84b0-124">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d84b0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d84b0-125">-DefaultProfile</span></span>
<span data-ttu-id="d84b0-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d84b0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84b0-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="d84b0-127">-ForceUpdateTag</span></span>
<span data-ttu-id="d84b0-128">Jeśli podano wartość inną niż poprzednia, program obsługi rozszerzenia będzie musiał zaktualizować plik nawet wtedy, gdy konfiguracja rozszerzenia się nie zmieniła.</span><span class="sxs-lookup"><span data-stu-id="d84b0-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="d84b0-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d84b0-129">-InputObject</span></span>
<span data-ttu-id="d84b0-130">Zasób Typu węzła</span><span class="sxs-lookup"><span data-stu-id="d84b0-130">Node Type resource</span></span>

```yaml
Type: PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d84b0-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d84b0-131">-Name</span></span>
<span data-ttu-id="d84b0-132">nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d84b0-132">extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84b0-133">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="d84b0-133">-NodeTypeName</span></span>
<span data-ttu-id="d84b0-134">Określ nazwę typu węzła.</span><span class="sxs-lookup"><span data-stu-id="d84b0-134">Specify the name of the node type.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d84b0-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="d84b0-135">-ProtectedSetting</span></span>
<span data-ttu-id="d84b0-136">Rozszerzenie może zawierać ustawienia protectedSettings lub protectedSettingsFromKeyVault albo nie ma żadnych ustawień chronionych.</span><span class="sxs-lookup"><span data-stu-id="d84b0-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84b0-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="d84b0-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="d84b0-138">Zbiór nazw rozszerzeń, po których to rozszerzenie wymaga obsługi administracyjnej.</span><span class="sxs-lookup"><span data-stu-id="d84b0-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84b0-139">— Publisher</span><span class="sxs-lookup"><span data-stu-id="d84b0-139">-Publisher</span></span>
<span data-ttu-id="d84b0-140">Nazwa wydawcy programu obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d84b0-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="d84b0-141">Aby uzyskać wydawcę, Get-AzVMImagePublisher polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d84b0-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84b0-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d84b0-142">-ResourceGroupName</span></span>
<span data-ttu-id="d84b0-143">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d84b0-143">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d84b0-144">— Ustawienie</span><span class="sxs-lookup"><span data-stu-id="d84b0-144">-Setting</span></span>
<span data-ttu-id="d84b0-145">Formatowane ustawienia publiczne rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d84b0-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84b0-146">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="d84b0-146">-Type</span></span>
<span data-ttu-id="d84b0-147">Określa typ rozszerzenia. Przykładem jest "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="d84b0-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="d84b0-148">Możesz użyć polecenia cmdlet Get-AzVMExtensionImageType, aby uzyskać typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d84b0-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84b0-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d84b0-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="d84b0-150">Określa wersję programu obsługi skryptów.</span><span class="sxs-lookup"><span data-stu-id="d84b0-150">Specifies the version of the script handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84b0-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d84b0-151">-Confirm</span></span>
<span data-ttu-id="d84b0-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d84b0-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84b0-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d84b0-153">-WhatIf</span></span>
<span data-ttu-id="d84b0-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d84b0-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d84b0-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d84b0-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84b0-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d84b0-156">CommonParameters</span></span>
<span data-ttu-id="d84b0-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d84b0-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d84b0-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d84b0-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d84b0-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d84b0-159">INPUTS</span></span>

### <span data-ttu-id="d84b0-160">System.String</span><span class="sxs-lookup"><span data-stu-id="d84b0-160">System.String</span></span>

### <span data-ttu-id="d84b0-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d84b0-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="d84b0-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d84b0-162">OUTPUTS</span></span>

### <span data-ttu-id="d84b0-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d84b0-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="d84b0-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d84b0-164">NOTES</span></span>

## <span data-ttu-id="d84b0-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d84b0-165">RELATED LINKS</span></span>
