---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 468c4cfac836ca986d6cfbfd06f35032cca5b6a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546844"
---
# <span data-ttu-id="0f165-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0f165-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="0f165-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f165-102">SYNOPSIS</span></span>
<span data-ttu-id="0f165-103">Umożliwia zaktualizowanie rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="0f165-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f165-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f165-104">SYNTAX</span></span>

### <span data-ttu-id="0f165-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0f165-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f165-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f165-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f165-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f165-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f165-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f165-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f165-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f165-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f165-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f165-110">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f165-111">Opis</span><span class="sxs-lookup"><span data-stu-id="0f165-111">DESCRIPTION</span></span>
<span data-ttu-id="0f165-112">Polecenie cmdlet Update-AzureRmContainerRegistry aktualizuje rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="0f165-112">The Update-AzureRmContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="0f165-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f165-113">EXAMPLES</span></span>

### <span data-ttu-id="0f165-114">Przykład 1: Włączanie użytkownika administratora dla określonego rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="0f165-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="0f165-115">To polecenie umożliwia użytkownikowi administrator dla określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="0f165-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="0f165-116">Przykład 2: Ustawianie konta magazynu, które jest używane przez określony rejestr kontenerów</span><span class="sxs-lookup"><span data-stu-id="0f165-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="0f165-117">To polecenie umożliwia ustawienie określonego rejestru kontenera na używanie istniejącego konta magazynu \` mystorageaccount \` w ramach tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0f165-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="0f165-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f165-118">PARAMETERS</span></span>

### <span data-ttu-id="0f165-119">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="0f165-119">-DisableAdminUser</span></span>
<span data-ttu-id="0f165-120">Włącz użytkownika administracyjnego dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="0f165-120">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f165-121">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="0f165-121">-EnableAdminUser</span></span>
<span data-ttu-id="0f165-122">Włącz użytkownika administracyjnego dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="0f165-122">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f165-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0f165-123">-Name</span></span>
<span data-ttu-id="0f165-124">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="0f165-124">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f165-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f165-125">-ResourceGroupName</span></span>
<span data-ttu-id="0f165-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0f165-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f165-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0f165-127">-StorageAccountName</span></span>
<span data-ttu-id="0f165-128">Nazwa istniejącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="0f165-128">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="0f165-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="0f165-129">-Tag</span></span>
<span data-ttu-id="0f165-130">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="0f165-130">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="0f165-131">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="0f165-131">For example:</span></span>

<span data-ttu-id="0f165-132">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="0f165-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f165-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f165-133">-Confirm</span></span>
<span data-ttu-id="0f165-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f165-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f165-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f165-135">-WhatIf</span></span>
<span data-ttu-id="0f165-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f165-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f165-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0f165-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f165-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f165-138">-DefaultProfile</span></span>
<span data-ttu-id="0f165-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0f165-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f165-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f165-140">-ResourceId</span></span>
<span data-ttu-id="0f165-141">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="0f165-141">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f165-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="0f165-142">-Sku</span></span>
<span data-ttu-id="0f165-143">Wersja SKU rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="0f165-143">Container Registry SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f165-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f165-144">CommonParameters</span></span>
<span data-ttu-id="0f165-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f165-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f165-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f165-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f165-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f165-147">INPUTS</span></span>

### <span data-ttu-id="0f165-148">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0f165-148">None</span></span>
<span data-ttu-id="0f165-149">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="0f165-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0f165-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f165-150">OUTPUTS</span></span>

### <span data-ttu-id="0f165-151">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0f165-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="0f165-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f165-152">NOTES</span></span>

## <span data-ttu-id="0f165-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f165-153">RELATED LINKS</span></span>

[<span data-ttu-id="0f165-154">Nowe — AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0f165-154">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="0f165-155">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0f165-155">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="0f165-156">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0f165-156">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

