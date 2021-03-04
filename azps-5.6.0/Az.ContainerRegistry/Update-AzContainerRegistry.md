---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: aa84186be2b5dc13117397e76722a6826d5314a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956314"
---
# <span data-ttu-id="ca517-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ca517-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="ca517-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca517-102">SYNOPSIS</span></span>
<span data-ttu-id="ca517-103">Aktualizuje rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="ca517-103">Updates a container registry.</span></span>

## <span data-ttu-id="ca517-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ca517-104">SYNTAX</span></span>

### <span data-ttu-id="ca517-105">NameResourceGroupParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ca517-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca517-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca517-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca517-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca517-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca517-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca517-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca517-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca517-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca517-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca517-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca517-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="ca517-111">DESCRIPTION</span></span>
<span data-ttu-id="ca517-112">Polecenie cmdlet Update-AzContainerRegistry aktualizuje rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="ca517-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="ca517-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ca517-113">EXAMPLES</span></span>

### <span data-ttu-id="ca517-114">Przykład 1. Włączanie administratora dla określonego rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="ca517-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="ca517-115">To polecenie umożliwia użytkownikowi administratorowi korzystanie z określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="ca517-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="ca517-116">Przykład 2. Ustawianie konta magazynu używanego przez rejestr określonego kontenera</span><span class="sxs-lookup"><span data-stu-id="ca517-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="ca517-117">To polecenie ustawia określony rejestr kontenera na używanie istniejącego konta magazynu w tej \` \` samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ca517-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="ca517-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca517-118">PARAMETERS</span></span>

### <span data-ttu-id="ca517-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca517-119">-DefaultProfile</span></span>
<span data-ttu-id="ca517-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ca517-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca517-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="ca517-121">-DisableAdminUser</span></span>
<span data-ttu-id="ca517-122">Włącz dla użytkownika administratora rejestr kontenerów.</span><span class="sxs-lookup"><span data-stu-id="ca517-122">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca517-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="ca517-123">-EnableAdminUser</span></span>
<span data-ttu-id="ca517-124">Włącz dla użytkownika administratora rejestr kontenerów.</span><span class="sxs-lookup"><span data-stu-id="ca517-124">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca517-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ca517-125">-Name</span></span>
<span data-ttu-id="ca517-126">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="ca517-126">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca517-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca517-127">-NetworkRuleSet</span></span>
<span data-ttu-id="ca517-128">Zestaw reguł sieciowych dla rejestru kontenerów.</span><span class="sxs-lookup"><span data-stu-id="ca517-128">The network rule set for a container registry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca517-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca517-129">-ResourceGroupName</span></span>
<span data-ttu-id="ca517-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca517-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca517-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca517-131">-ResourceId</span></span>
<span data-ttu-id="ca517-132">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="ca517-132">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca517-133">- SKU</span><span class="sxs-lookup"><span data-stu-id="ca517-133">-Sku</span></span>
<span data-ttu-id="ca517-134">Container Registry SKU.</span><span class="sxs-lookup"><span data-stu-id="ca517-134">Container Registry SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca517-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ca517-135">-StorageAccountName</span></span>
<span data-ttu-id="ca517-136">Nazwa istniejącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ca517-136">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="ca517-137">— Tag</span><span class="sxs-lookup"><span data-stu-id="ca517-137">-Tag</span></span>
<span data-ttu-id="ca517-138">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="ca517-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="ca517-139">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ca517-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca517-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca517-140">-Confirm</span></span>
<span data-ttu-id="ca517-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ca517-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca517-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca517-142">-WhatIf</span></span>
<span data-ttu-id="ca517-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca517-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca517-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ca517-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca517-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca517-145">CommonParameters</span></span>
<span data-ttu-id="ca517-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca517-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca517-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca517-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca517-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca517-148">INPUTS</span></span>

### <span data-ttu-id="ca517-149">System.String</span><span class="sxs-lookup"><span data-stu-id="ca517-149">System.String</span></span>

## <span data-ttu-id="ca517-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca517-150">OUTPUTS</span></span>

### <span data-ttu-id="ca517-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ca517-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="ca517-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ca517-152">NOTES</span></span>

## <span data-ttu-id="ca517-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca517-153">RELATED LINKS</span></span>

[<span data-ttu-id="ca517-154">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ca517-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="ca517-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ca517-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="ca517-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ca517-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

