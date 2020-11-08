---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 606f92a3cc75deb40b3781b3578e38794ae65b2b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063549"
---
# <span data-ttu-id="d76ac-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d76ac-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="d76ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d76ac-102">SYNOPSIS</span></span>
<span data-ttu-id="d76ac-103">Umożliwia zaktualizowanie rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="d76ac-103">Updates a container registry.</span></span>

## <span data-ttu-id="d76ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d76ac-104">SYNTAX</span></span>

### <span data-ttu-id="d76ac-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d76ac-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d76ac-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d76ac-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d76ac-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d76ac-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d76ac-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d76ac-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d76ac-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d76ac-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d76ac-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d76ac-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d76ac-111">Opis</span><span class="sxs-lookup"><span data-stu-id="d76ac-111">DESCRIPTION</span></span>
<span data-ttu-id="d76ac-112">Polecenie cmdlet Update-AzContainerRegistry aktualizuje rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="d76ac-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="d76ac-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d76ac-113">EXAMPLES</span></span>

### <span data-ttu-id="d76ac-114">Przykład 1: Włączanie użytkownika administratora dla określonego rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="d76ac-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="d76ac-115">To polecenie umożliwia użytkownikowi administrator dla określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="d76ac-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="d76ac-116">Przykład 2: Ustawianie konta magazynu, które jest używane przez określony rejestr kontenerów</span><span class="sxs-lookup"><span data-stu-id="d76ac-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="d76ac-117">To polecenie umożliwia ustawienie określonego rejestru kontenera na używanie istniejącego konta magazynu \` mystorageaccount \` w ramach tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d76ac-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="d76ac-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d76ac-118">PARAMETERS</span></span>

### <span data-ttu-id="d76ac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d76ac-119">-DefaultProfile</span></span>
<span data-ttu-id="d76ac-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d76ac-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d76ac-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="d76ac-121">-DisableAdminUser</span></span>
<span data-ttu-id="d76ac-122">Włącz użytkownika administracyjnego dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="d76ac-122">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="d76ac-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="d76ac-123">-EnableAdminUser</span></span>
<span data-ttu-id="d76ac-124">Włącz użytkownika administracyjnego dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="d76ac-124">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="d76ac-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d76ac-125">-Name</span></span>
<span data-ttu-id="d76ac-126">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="d76ac-126">Container Registry Name.</span></span>

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

### <span data-ttu-id="d76ac-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d76ac-127">-ResourceGroupName</span></span>
<span data-ttu-id="d76ac-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d76ac-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="d76ac-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d76ac-129">-ResourceId</span></span>
<span data-ttu-id="d76ac-130">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="d76ac-130">The container registry resource id</span></span>

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

### <span data-ttu-id="d76ac-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="d76ac-131">-Sku</span></span>
<span data-ttu-id="d76ac-132">Wersja SKU rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="d76ac-132">Container Registry SKU.</span></span>

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

### <span data-ttu-id="d76ac-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d76ac-133">-StorageAccountName</span></span>
<span data-ttu-id="d76ac-134">Nazwa istniejącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d76ac-134">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="d76ac-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="d76ac-135">-Tag</span></span>
<span data-ttu-id="d76ac-136">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d76ac-136">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="d76ac-137">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="d76ac-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d76ac-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d76ac-138">-Confirm</span></span>
<span data-ttu-id="d76ac-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d76ac-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d76ac-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d76ac-140">-WhatIf</span></span>
<span data-ttu-id="d76ac-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d76ac-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d76ac-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d76ac-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d76ac-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d76ac-143">CommonParameters</span></span>
<span data-ttu-id="d76ac-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d76ac-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d76ac-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d76ac-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d76ac-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d76ac-146">INPUTS</span></span>

### <span data-ttu-id="d76ac-147">System. String</span><span class="sxs-lookup"><span data-stu-id="d76ac-147">System.String</span></span>

## <span data-ttu-id="d76ac-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d76ac-148">OUTPUTS</span></span>

### <span data-ttu-id="d76ac-149">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d76ac-149">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="d76ac-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d76ac-150">NOTES</span></span>

## <span data-ttu-id="d76ac-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d76ac-151">RELATED LINKS</span></span>

[<span data-ttu-id="d76ac-152">Nowe — AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d76ac-152">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="d76ac-153">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d76ac-153">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="d76ac-154">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d76ac-154">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

