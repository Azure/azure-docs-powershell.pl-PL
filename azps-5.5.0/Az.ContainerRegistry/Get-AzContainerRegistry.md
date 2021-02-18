---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: 759bc79a7ab36f99e01ce1e96b0bb6c3c6a9483b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181483"
---
# <span data-ttu-id="a1e8d-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a1e8d-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="a1e8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1e8d-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e8d-103">Pobiera rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="a1e8d-103">Gets a container registry.</span></span>

## <span data-ttu-id="a1e8d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a1e8d-104">SYNTAX</span></span>

### <span data-ttu-id="a1e8d-105">ListRegistriesParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a1e8d-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1e8d-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1e8d-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1e8d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1e8d-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1e8d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a1e8d-108">DESCRIPTION</span></span>
<span data-ttu-id="a1e8d-109">Polecenie Get-AzContainerRegistry pobiera określony rejestr kontenera lub wszystkie rejestry kontenerów w grupie zasobów lub w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a1e8d-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="a1e8d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a1e8d-110">EXAMPLES</span></span>

### <span data-ttu-id="a1e8d-111">Przykład 1. Uzyskiwanie określonego rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="a1e8d-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="a1e8d-112">To polecenie pobiera określony rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="a1e8d-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="a1e8d-113">Przykład 2. Uzyskiwanie wszystkich rejestrów kontenerów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="a1e8d-113">Example 2: Get all the container registries in a resource group</span></span>
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

<span data-ttu-id="a1e8d-114">To polecenie pobiera wszystkie rejestry kontenerów w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1e8d-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="a1e8d-115">Przykład 3. Uzyskiwanie wszystkich rejestrów kontenerów w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a1e8d-115">Example 3:  Get all the container registries in the subscription</span></span>
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

<span data-ttu-id="a1e8d-116">To polecenie pobiera wszystkie rejestry kontenerów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a1e8d-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="a1e8d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1e8d-117">PARAMETERS</span></span>

### <span data-ttu-id="a1e8d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e8d-118">-DefaultProfile</span></span>
<span data-ttu-id="a1e8d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a1e8d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1e8d-120">- IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="a1e8d-120">-IncludeDetail</span></span>
<span data-ttu-id="a1e8d-121">Pokaż więcej szczegółów na temat rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="a1e8d-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="a1e8d-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a1e8d-122">-Name</span></span>
<span data-ttu-id="a1e8d-123">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="a1e8d-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="a1e8d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e8d-124">-ResourceGroupName</span></span>
<span data-ttu-id="a1e8d-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1e8d-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a1e8d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1e8d-126">-ResourceId</span></span>
<span data-ttu-id="a1e8d-127">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="a1e8d-127">The container registry resource id</span></span>

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

### <span data-ttu-id="a1e8d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e8d-128">CommonParameters</span></span>
<span data-ttu-id="a1e8d-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1e8d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e8d-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1e8d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e8d-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1e8d-131">INPUTS</span></span>

### <span data-ttu-id="a1e8d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a1e8d-132">System.String</span></span>

## <span data-ttu-id="a1e8d-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1e8d-133">OUTPUTS</span></span>

### <span data-ttu-id="a1e8d-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a1e8d-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="a1e8d-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a1e8d-135">NOTES</span></span>

## <span data-ttu-id="a1e8d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1e8d-136">RELATED LINKS</span></span>

[<span data-ttu-id="a1e8d-137">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a1e8d-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="a1e8d-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a1e8d-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="a1e8d-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a1e8d-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

