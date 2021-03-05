---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: 969e37173c487b2ed3ee4ab6dad5374208f5ff27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004449"
---
# <span data-ttu-id="13de0-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="13de0-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="13de0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13de0-102">SYNOPSIS</span></span>
<span data-ttu-id="13de0-103">Pobiera rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="13de0-103">Gets a container registry.</span></span>

## <span data-ttu-id="13de0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="13de0-104">SYNTAX</span></span>

### <span data-ttu-id="13de0-105">ListRegistriesParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="13de0-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13de0-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="13de0-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13de0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13de0-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13de0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="13de0-108">DESCRIPTION</span></span>
<span data-ttu-id="13de0-109">Polecenie Get-AzContainerRegistry pobiera określony rejestr kontenera lub wszystkie rejestry kontenerów w grupie zasobów lub w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="13de0-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="13de0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="13de0-110">EXAMPLES</span></span>

### <span data-ttu-id="13de0-111">Przykład 1. Uzyskiwanie określonego rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="13de0-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="13de0-112">To polecenie pobiera określony rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="13de0-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="13de0-113">Przykład 2. Uzyskiwanie wszystkich rejestrów kontenerów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="13de0-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="13de0-114">To polecenie pobiera wszystkie rejestry kontenerów w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="13de0-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="13de0-115">Przykład 3. Uzyskiwanie wszystkich rejestrów kontenerów w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="13de0-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzContainerRegistry

  Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="13de0-116">To polecenie pobiera wszystkie rejestry kontenerów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="13de0-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="13de0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13de0-117">PARAMETERS</span></span>

### <span data-ttu-id="13de0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13de0-118">-DefaultProfile</span></span>
<span data-ttu-id="13de0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="13de0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13de0-120">- IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="13de0-120">-IncludeDetail</span></span>
<span data-ttu-id="13de0-121">Pokaż więcej szczegółów na temat rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="13de0-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="13de0-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="13de0-122">-Name</span></span>
<span data-ttu-id="13de0-123">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="13de0-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="13de0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13de0-124">-ResourceGroupName</span></span>
<span data-ttu-id="13de0-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="13de0-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListRegistriesParameterSet
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

### <span data-ttu-id="13de0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13de0-126">-ResourceId</span></span>
<span data-ttu-id="13de0-127">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="13de0-127">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13de0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13de0-128">CommonParameters</span></span>
<span data-ttu-id="13de0-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13de0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13de0-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13de0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13de0-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13de0-131">INPUTS</span></span>

### <span data-ttu-id="13de0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="13de0-132">System.String</span></span>

## <span data-ttu-id="13de0-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13de0-133">OUTPUTS</span></span>

### <span data-ttu-id="13de0-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="13de0-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="13de0-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="13de0-135">NOTES</span></span>

## <span data-ttu-id="13de0-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13de0-136">RELATED LINKS</span></span>

[<span data-ttu-id="13de0-137">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="13de0-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="13de0-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="13de0-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="13de0-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="13de0-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

