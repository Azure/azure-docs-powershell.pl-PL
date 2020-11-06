---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: 3d9580549308c17c92037b3e31a337f11bbe6938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524517"
---
# <span data-ttu-id="ce13d-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ce13d-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="ce13d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce13d-102">SYNOPSIS</span></span>
<span data-ttu-id="ce13d-103">Pobiera rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="ce13d-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce13d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce13d-104">SYNTAX</span></span>

### <span data-ttu-id="ce13d-105">ListRegistriesParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ce13d-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce13d-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce13d-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce13d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce13d-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce13d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ce13d-108">DESCRIPTION</span></span>
<span data-ttu-id="ce13d-109">Polecenie cmdlet Get-AzureRmContainerRegistry umożliwia pobieranie określonego rejestru kontenera lub wszystkich rejestrów kontenerów w grupie zasobów lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ce13d-109">The Get-AzureRmContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="ce13d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce13d-110">EXAMPLES</span></span>

### <span data-ttu-id="ce13d-111">Przykład 1: uzyskiwanie określonego rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="ce13d-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="ce13d-112">To polecenie pobiera określony rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="ce13d-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="ce13d-113">Przykład 2: uzyskiwanie wszystkich rejestrów kontenerów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="ce13d-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup"

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

<span data-ttu-id="ce13d-114">To polecenie pobiera wszystkie rejestry kontenerów w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="ce13d-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="ce13d-115">Przykład 3: uzyskiwanie wszystkich rejestrów kontenerów w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="ce13d-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry

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

<span data-ttu-id="ce13d-116">To polecenie pobiera wszystkie rejestry kontenerów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ce13d-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="ce13d-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce13d-117">PARAMETERS</span></span>

### <span data-ttu-id="ce13d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce13d-118">-DefaultProfile</span></span>
<span data-ttu-id="ce13d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ce13d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce13d-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="ce13d-120">-IncludeDetail</span></span>
<span data-ttu-id="ce13d-121">Pokaż więcej szczegółów dotyczących rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="ce13d-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="ce13d-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ce13d-122">-Name</span></span>
<span data-ttu-id="ce13d-123">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="ce13d-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="ce13d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce13d-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce13d-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ce13d-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ce13d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce13d-126">-ResourceId</span></span>
<span data-ttu-id="ce13d-127">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="ce13d-127">The container registry resource id</span></span>

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

### <span data-ttu-id="ce13d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce13d-128">CommonParameters</span></span>
<span data-ttu-id="ce13d-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce13d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce13d-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce13d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce13d-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce13d-131">INPUTS</span></span>

### <span data-ttu-id="ce13d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ce13d-132">System.String</span></span>

## <span data-ttu-id="ce13d-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce13d-133">OUTPUTS</span></span>

### <span data-ttu-id="ce13d-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ce13d-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="ce13d-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce13d-135">NOTES</span></span>

## <span data-ttu-id="ce13d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce13d-136">RELATED LINKS</span></span>

[<span data-ttu-id="ce13d-137">Nowe — AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ce13d-137">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="ce13d-138">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ce13d-138">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="ce13d-139">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ce13d-139">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

