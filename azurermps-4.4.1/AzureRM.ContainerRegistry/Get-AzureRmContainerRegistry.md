---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: ce2cabd669f779fe94afa80089868aa04753524b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548328"
---
# <span data-ttu-id="23650-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23650-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="23650-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23650-102">SYNOPSIS</span></span>
<span data-ttu-id="23650-103">Pobiera rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="23650-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23650-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23650-104">SYNTAX</span></span>

### <span data-ttu-id="23650-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="23650-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23650-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23650-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23650-107">Opis</span><span class="sxs-lookup"><span data-stu-id="23650-107">DESCRIPTION</span></span>
<span data-ttu-id="23650-108">Polecenie cmdlet **Get-AzureRmContainerRegistry** Pobiera określony rejestr kontenera lub wszystkie rejestry kontenerów w grupie zasobów lub w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="23650-108">The **Get-AzureRmContainerRegistry** cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="23650-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23650-109">EXAMPLES</span></span>

### <span data-ttu-id="23650-110">Przykład 1: uzyskiwanie określonego rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="23650-110">Example 1: Get a specified container registry</span></span>
```
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

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
AdminUserEnabled   : False
StorageAccountName : myregistry154817
```

<span data-ttu-id="23650-111">To polecenie pobiera określony rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="23650-111">This command gets the specified container registry.</span></span>

### <span data-ttu-id="23650-112">Przykład 2: uzyskiwanie wszystkich rejestrów kontenerów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="23650-112">Example 2: Get all the container registries in a resource group</span></span>
```
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup"

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
AdminUserEnabled   : False
StorageAccountName : myregistry154817

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/AnotherRegistry
ResourceGroupName  : MyResourceGroup
Name               : AnotherRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : anotherregistry.azurecr.io
CreationDate       : 4/13/2017 3:50:49 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : anotherregistry154940
```

<span data-ttu-id="23650-113">To polecenie pobiera wszystkie rejestry kontenerów w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="23650-113">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="23650-114">Przykład 3: uzyskiwanie wszystkich rejestrów kontenerów w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="23650-114">Example 3:  Get all the container registries in the subscription</span></span>
```
PS C:\>Get-AzureRmContainerRegistry

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
AdminUserEnabled   : False
StorageAccountName : myregistry154817

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/AnotherRegistry
ResourceGroupName  : MyResourceGroup
Name               : AnotherRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : anotherregistry.azurecr.io
CreationDate       : 4/13/2017 3:50:49 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : anotherregistry154940
```

<span data-ttu-id="23650-115">To polecenie pobiera wszystkie rejestry kontenerów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="23650-115">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="23650-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23650-116">PARAMETERS</span></span>

### <span data-ttu-id="23650-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23650-117">-Name</span></span>
<span data-ttu-id="23650-118">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="23650-118">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23650-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23650-119">-ResourceGroupName</span></span>
<span data-ttu-id="23650-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23650-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23650-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23650-121">-DefaultProfile</span></span>
<span data-ttu-id="23650-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23650-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23650-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23650-123">CommonParameters</span></span>
<span data-ttu-id="23650-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23650-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23650-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23650-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23650-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23650-126">INPUTS</span></span>

## <span data-ttu-id="23650-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23650-127">OUTPUTS</span></span>

### <span data-ttu-id="23650-128">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23650-128">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="23650-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23650-129">NOTES</span></span>

## <span data-ttu-id="23650-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23650-130">RELATED LINKS</span></span>

[<span data-ttu-id="23650-131">Nowe — AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23650-131">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="23650-132">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23650-132">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="23650-133">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23650-133">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)

