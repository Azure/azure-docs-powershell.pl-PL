---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 5f59ae54d472d1d831b41f58789625c195961de5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552399"
---
# <span data-ttu-id="49f08-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="49f08-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="49f08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49f08-102">SYNOPSIS</span></span>
<span data-ttu-id="49f08-103">Umożliwia zaktualizowanie rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="49f08-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49f08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49f08-104">SYNTAX</span></span>

### <span data-ttu-id="49f08-105">Empty (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="49f08-105">Empty (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49f08-106">EnableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="49f08-106">EnableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49f08-107">DisableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="49f08-107">DisableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49f08-108">Opis</span><span class="sxs-lookup"><span data-stu-id="49f08-108">DESCRIPTION</span></span>
<span data-ttu-id="49f08-109">Polecenie cmdlet **Update-AzureRmContainerRegistry** umożliwia zaktualizowanie rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="49f08-109">The **Update-AzureRmContainerRegistry** cmdlet updates a container registry.</span></span>

## <span data-ttu-id="49f08-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49f08-110">EXAMPLES</span></span>

### <span data-ttu-id="49f08-111">Przykład 1: Włączanie użytkownika administratora dla określonego rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="49f08-111">Example 1: Enable admin user for a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : myregistry154817
```

<span data-ttu-id="49f08-112">To polecenie umożliwia użytkownikowi administrator dla określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="49f08-112">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="49f08-113">Przykład 2: Ustawianie konta magazynu, które jest używane przez określony rejestr kontenerów</span><span class="sxs-lookup"><span data-stu-id="49f08-113">Example 2: Set the storage account used by a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : mystorageaccount
```

<span data-ttu-id="49f08-114">To polecenie umożliwia ustawienie określonego rejestru kontenera na używanie istniejącego konta magazynu `mystorageaccount` w tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="49f08-114">This command sets the specified container registry to use an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="49f08-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49f08-115">PARAMETERS</span></span>

### <span data-ttu-id="49f08-116">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="49f08-116">-DisableAdminUser</span></span>
<span data-ttu-id="49f08-117">Włącz użytkownika administracyjnego dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="49f08-117">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: DisableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f08-118">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="49f08-118">-EnableAdminUser</span></span>
<span data-ttu-id="49f08-119">Włącz użytkownika administracyjnego dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="49f08-119">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f08-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="49f08-120">-Name</span></span>
<span data-ttu-id="49f08-121">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="49f08-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f08-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49f08-122">-ResourceGroupName</span></span>
<span data-ttu-id="49f08-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="49f08-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f08-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="49f08-124">-StorageAccountName</span></span>
<span data-ttu-id="49f08-125">Nazwa istniejącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="49f08-125">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="49f08-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="49f08-126">-Tag</span></span>
<span data-ttu-id="49f08-127">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="49f08-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="49f08-128">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="49f08-128">For example:</span></span>

<span data-ttu-id="49f08-129">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="49f08-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="49f08-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49f08-130">-Confirm</span></span>
<span data-ttu-id="49f08-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49f08-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f08-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49f08-132">-WhatIf</span></span>
<span data-ttu-id="49f08-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49f08-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49f08-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="49f08-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f08-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f08-135">-DefaultProfile</span></span>
<span data-ttu-id="49f08-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="49f08-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49f08-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f08-137">CommonParameters</span></span>
<span data-ttu-id="49f08-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49f08-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f08-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49f08-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f08-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49f08-140">INPUTS</span></span>

## <span data-ttu-id="49f08-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49f08-141">OUTPUTS</span></span>

### <span data-ttu-id="49f08-142">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="49f08-142">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="49f08-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49f08-143">NOTES</span></span>

## <span data-ttu-id="49f08-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49f08-144">RELATED LINKS</span></span>

[<span data-ttu-id="49f08-145">Nowe — AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="49f08-145">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="49f08-146">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="49f08-146">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="49f08-147">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="49f08-147">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)
