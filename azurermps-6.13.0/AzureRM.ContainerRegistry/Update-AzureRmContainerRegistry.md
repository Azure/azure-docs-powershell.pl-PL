---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 10321e780532cd522e7cc1d4532baa360350c324
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716581"
---
# <span data-ttu-id="42551-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="42551-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="42551-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42551-102">SYNOPSIS</span></span>
<span data-ttu-id="42551-103">Umożliwia zaktualizowanie rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="42551-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42551-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42551-104">SYNTAX</span></span>

### <span data-ttu-id="42551-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="42551-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42551-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="42551-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42551-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="42551-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42551-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42551-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42551-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42551-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42551-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42551-110">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42551-111">Opis</span><span class="sxs-lookup"><span data-stu-id="42551-111">DESCRIPTION</span></span>
<span data-ttu-id="42551-112">Polecenie cmdlet Update-AzureRmContainerRegistry aktualizuje rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="42551-112">The Update-AzureRmContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="42551-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42551-113">EXAMPLES</span></span>

### <span data-ttu-id="42551-114">Przykład 1: Włączanie użytkownika administratora dla określonego rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="42551-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="42551-115">To polecenie umożliwia użytkownikowi administrator dla określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="42551-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="42551-116">Przykład 2: Ustawianie konta magazynu, które jest używane przez określony rejestr kontenerów</span><span class="sxs-lookup"><span data-stu-id="42551-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="42551-117">To polecenie umożliwia ustawienie określonego rejestru kontenera na używanie istniejącego konta magazynu \` mystorageaccount \` w ramach tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="42551-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="42551-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42551-118">PARAMETERS</span></span>

### <span data-ttu-id="42551-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42551-119">-DefaultProfile</span></span>
<span data-ttu-id="42551-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="42551-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42551-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="42551-121">-DisableAdminUser</span></span>
<span data-ttu-id="42551-122">Włącz użytkownika administracyjnego dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="42551-122">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="42551-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="42551-123">-EnableAdminUser</span></span>
<span data-ttu-id="42551-124">Włącz użytkownika administracyjnego dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="42551-124">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="42551-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42551-125">-Name</span></span>
<span data-ttu-id="42551-126">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="42551-126">Container Registry Name.</span></span>

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

### <span data-ttu-id="42551-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42551-127">-ResourceGroupName</span></span>
<span data-ttu-id="42551-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="42551-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="42551-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42551-129">-ResourceId</span></span>
<span data-ttu-id="42551-130">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="42551-130">The container registry resource id</span></span>

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

### <span data-ttu-id="42551-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="42551-131">-Sku</span></span>
<span data-ttu-id="42551-132">Wersja SKU rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="42551-132">Container Registry SKU.</span></span>

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

### <span data-ttu-id="42551-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="42551-133">-StorageAccountName</span></span>
<span data-ttu-id="42551-134">Nazwa istniejącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="42551-134">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="42551-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="42551-135">-Tag</span></span>
<span data-ttu-id="42551-136">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="42551-136">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="42551-137">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="42551-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="42551-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42551-138">-Confirm</span></span>
<span data-ttu-id="42551-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42551-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42551-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42551-140">-WhatIf</span></span>
<span data-ttu-id="42551-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42551-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42551-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="42551-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42551-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42551-143">CommonParameters</span></span>
<span data-ttu-id="42551-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42551-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42551-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42551-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42551-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42551-146">INPUTS</span></span>

### <span data-ttu-id="42551-147">System. String</span><span class="sxs-lookup"><span data-stu-id="42551-147">System.String</span></span>

## <span data-ttu-id="42551-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42551-148">OUTPUTS</span></span>

### <span data-ttu-id="42551-149">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="42551-149">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="42551-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42551-150">NOTES</span></span>

## <span data-ttu-id="42551-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42551-151">RELATED LINKS</span></span>

[<span data-ttu-id="42551-152">Nowe — AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="42551-152">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="42551-153">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="42551-153">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="42551-154">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="42551-154">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

