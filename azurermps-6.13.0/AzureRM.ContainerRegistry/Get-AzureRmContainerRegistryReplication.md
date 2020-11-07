---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: d2cac696382f807a1fc4afe94f9d2d61ea65cece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716447"
---
# <span data-ttu-id="812e9-101">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="812e9-101">Get-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="812e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="812e9-102">SYNOPSIS</span></span>
<span data-ttu-id="812e9-103">Pobiera replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="812e9-103">Gets a replication of a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="812e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="812e9-104">SYNTAX</span></span>

### <span data-ttu-id="812e9-105">ListReplicationByNameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="812e9-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="812e9-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="812e9-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="812e9-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="812e9-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="812e9-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="812e9-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="812e9-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="812e9-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="812e9-110">Opis</span><span class="sxs-lookup"><span data-stu-id="812e9-110">DESCRIPTION</span></span>
<span data-ttu-id="812e9-111">Polecenie cmdlet Get-AzureRmContainerRegistryReplication pobiera określoną replikację rejestru kontenera lub wszystkich replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="812e9-111">The Get-AzureRmContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="812e9-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="812e9-112">EXAMPLES</span></span>

### <span data-ttu-id="812e9-113">Przykład 1: Pobiera określoną replikację rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="812e9-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="812e9-114">Pobiera określoną replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="812e9-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="812e9-115">Przykład 2: Pobiera wszystkie replikacje rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="812e9-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="812e9-116">Pobiera wszystkie replikacje rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="812e9-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="812e9-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="812e9-117">PARAMETERS</span></span>

### <span data-ttu-id="812e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="812e9-118">-DefaultProfile</span></span>
<span data-ttu-id="812e9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="812e9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="812e9-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="812e9-120">-Name</span></span>
<span data-ttu-id="812e9-121">Nazwa replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="812e9-121">Container Registry Replication Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="812e9-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="812e9-122">-Registry</span></span>
<span data-ttu-id="812e9-123">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="812e9-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="812e9-124">-Registryname</span><span class="sxs-lookup"><span data-stu-id="812e9-124">-RegistryName</span></span>
<span data-ttu-id="812e9-125">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="812e9-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="812e9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="812e9-126">-ResourceGroupName</span></span>
<span data-ttu-id="812e9-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="812e9-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="812e9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="812e9-128">-ResourceId</span></span>
<span data-ttu-id="812e9-129">Identyfikator zasobu replikacji rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="812e9-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="812e9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="812e9-130">CommonParameters</span></span>
<span data-ttu-id="812e9-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="812e9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="812e9-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="812e9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="812e9-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="812e9-133">INPUTS</span></span>

### <span data-ttu-id="812e9-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="812e9-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="812e9-135">Parametry: Registry (ByValue)</span><span class="sxs-lookup"><span data-stu-id="812e9-135">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="812e9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="812e9-136">System.String</span></span>

## <span data-ttu-id="812e9-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="812e9-137">OUTPUTS</span></span>

### <span data-ttu-id="812e9-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="812e9-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="812e9-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="812e9-139">NOTES</span></span>

## <span data-ttu-id="812e9-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="812e9-140">RELATED LINKS</span></span>

[<span data-ttu-id="812e9-141">Nowe — AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="812e9-141">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="812e9-142">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="812e9-142">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
