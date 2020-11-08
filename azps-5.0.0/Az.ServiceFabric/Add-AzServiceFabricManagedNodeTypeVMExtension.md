---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: baff896564d8f3b8d70f69b190bc3429d4f465c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234269"
---
# <span data-ttu-id="d7b31-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="d7b31-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="d7b31-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7b31-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b31-103">Dodaj rozszerzenie maszyny wirtualnej do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="d7b31-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="d7b31-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7b31-104">SYNTAX</span></span>

### <span data-ttu-id="d7b31-105">ByObj (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d7b31-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7b31-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d7b31-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7b31-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d7b31-107">DESCRIPTION</span></span>
<span data-ttu-id="d7b31-108">Dodaj rozszerzenie maszyny wirtualnej do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="d7b31-108">Add vm extension to the node type.</span></span> <span data-ttu-id="d7b31-109">Spowoduje to dodanie rozszerzenia do zasobu zestawu skalowanie maszyny wirtualnej underliying.</span><span class="sxs-lookup"><span data-stu-id="d7b31-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="d7b31-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7b31-110">EXAMPLES</span></span>

### <span data-ttu-id="d7b31-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d7b31-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="d7b31-112">To polecenie dodaje rozszerzenie do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="d7b31-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="d7b31-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d7b31-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="d7b31-114">To polecenie powoduje dodanie rozszerzenia z ustawieniami i ustawieniami chronionymi do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="d7b31-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="d7b31-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d7b31-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="d7b31-116">To polecenie dodaje rozszerzenie do typu węzła za pomocą połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="d7b31-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="d7b31-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7b31-117">PARAMETERS</span></span>

### <span data-ttu-id="d7b31-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7b31-118">-AsJob</span></span>
<span data-ttu-id="d7b31-119">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="d7b31-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d7b31-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d7b31-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d7b31-121">Wskazuje, czy rozszerzenie ma używać nowszej wersji pomocniczej, jeśli jest dostępna w czasie wdrażania.</span><span class="sxs-lookup"><span data-stu-id="d7b31-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="d7b31-122">Po wdrożeniu rozszerzenie nie będzie jednak uaktualnić wersji pomocniczych, o ile nie zostanie ponownie wdrożone, nawet jeśli ta właściwość ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="d7b31-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="d7b31-123">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="d7b31-123">-ClusterName</span></span>
<span data-ttu-id="d7b31-124">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="d7b31-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d7b31-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b31-125">-DefaultProfile</span></span>
<span data-ttu-id="d7b31-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7b31-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7b31-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="d7b31-127">-ForceUpdateTag</span></span>
<span data-ttu-id="d7b31-128">Jeśli wartość jest podana i jest różna od poprzedniej wartości, program obsługi rozszerzeń zostanie zmuszony do zaktualizowania, nawet jeśli konfiguracja rozszerzenia nie została zmieniona.</span><span class="sxs-lookup"><span data-stu-id="d7b31-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="d7b31-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d7b31-129">-InputObject</span></span>
<span data-ttu-id="d7b31-130">Zasób typu węzła</span><span class="sxs-lookup"><span data-stu-id="d7b31-130">Node Type resource</span></span>

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

### <span data-ttu-id="d7b31-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d7b31-131">-Name</span></span>
<span data-ttu-id="d7b31-132">Nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d7b31-132">extension name.</span></span>

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

### <span data-ttu-id="d7b31-133">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="d7b31-133">-NodeTypeName</span></span>
<span data-ttu-id="d7b31-134">Określ nazwę typu węzła.</span><span class="sxs-lookup"><span data-stu-id="d7b31-134">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="d7b31-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="d7b31-135">-ProtectedSetting</span></span>
<span data-ttu-id="d7b31-136">Rozszerzenie może zawierać protectedSettings lub protectedSettingsFromKeyVault lub nie ma żadnych ustawień chronionych.</span><span class="sxs-lookup"><span data-stu-id="d7b31-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="d7b31-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="d7b31-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="d7b31-138">Kolekcja nazw rozszerzeń, po których to rozszerzenie musi zostać zainicjowane.</span><span class="sxs-lookup"><span data-stu-id="d7b31-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="d7b31-139">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="d7b31-139">-Publisher</span></span>
<span data-ttu-id="d7b31-140">Nazwa wydawcy obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d7b31-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="d7b31-141">Może to zrobić za pomocą polecenia cmdlet Get-AzVMImagePublisher w celu uzyskania wydawcy.</span><span class="sxs-lookup"><span data-stu-id="d7b31-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="d7b31-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b31-142">-ResourceGroupName</span></span>
<span data-ttu-id="d7b31-143">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d7b31-143">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d7b31-144">-Setting</span><span class="sxs-lookup"><span data-stu-id="d7b31-144">-Setting</span></span>
<span data-ttu-id="d7b31-145">Ustawienia publiczne w formacie JSON dla rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d7b31-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="d7b31-146">-Type</span><span class="sxs-lookup"><span data-stu-id="d7b31-146">-Type</span></span>
<span data-ttu-id="d7b31-147">Określa typ rozszerzenia; Przykładem jest "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="d7b31-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="d7b31-148">Możesz użyć polecenia cmdlet Get-AzVMExtensionImageType, aby uzyskać typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d7b31-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="d7b31-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d7b31-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="d7b31-150">Określa wersję obsługi skryptów.</span><span class="sxs-lookup"><span data-stu-id="d7b31-150">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="d7b31-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7b31-151">-Confirm</span></span>
<span data-ttu-id="d7b31-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7b31-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7b31-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7b31-153">-WhatIf</span></span>
<span data-ttu-id="d7b31-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7b31-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7b31-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7b31-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7b31-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b31-156">CommonParameters</span></span>
<span data-ttu-id="d7b31-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7b31-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b31-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7b31-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b31-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7b31-159">INPUTS</span></span>

### <span data-ttu-id="d7b31-160">System. String</span><span class="sxs-lookup"><span data-stu-id="d7b31-160">System.String</span></span>

### <span data-ttu-id="d7b31-161">Microsoft. Azure. Commands. servicefabric. MODELES. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d7b31-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="d7b31-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7b31-162">OUTPUTS</span></span>

### <span data-ttu-id="d7b31-163">Microsoft. Azure. Commands. servicefabric. MODELES. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d7b31-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="d7b31-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7b31-164">NOTES</span></span>

## <span data-ttu-id="d7b31-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7b31-165">RELATED LINKS</span></span>
