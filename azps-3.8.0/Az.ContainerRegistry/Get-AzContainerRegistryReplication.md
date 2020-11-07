---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 57b482368834d91e36a3f557c9657c82cea24f4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894853"
---
# <span data-ttu-id="06db2-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="06db2-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="06db2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06db2-102">SYNOPSIS</span></span>
<span data-ttu-id="06db2-103">Pobiera replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="06db2-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="06db2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06db2-104">SYNTAX</span></span>

### <span data-ttu-id="06db2-105">ListReplicationByNameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="06db2-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06db2-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="06db2-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06db2-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06db2-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06db2-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06db2-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06db2-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06db2-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06db2-110">Opis</span><span class="sxs-lookup"><span data-stu-id="06db2-110">DESCRIPTION</span></span>
<span data-ttu-id="06db2-111">Polecenie cmdlet Get-AzContainerRegistryReplication pobiera określoną replikację rejestru kontenera lub wszystkich replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="06db2-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="06db2-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06db2-112">EXAMPLES</span></span>

### <span data-ttu-id="06db2-113">Przykład 1: Pobiera określoną replikację rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="06db2-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="06db2-114">Pobiera określoną replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="06db2-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="06db2-115">Przykład 2: Pobiera wszystkie replikacje rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="06db2-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="06db2-116">Pobiera wszystkie replikacje rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="06db2-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="06db2-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06db2-117">PARAMETERS</span></span>

### <span data-ttu-id="06db2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06db2-118">-DefaultProfile</span></span>
<span data-ttu-id="06db2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="06db2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06db2-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="06db2-120">-Name</span></span>
<span data-ttu-id="06db2-121">Nazwa replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="06db2-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="06db2-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="06db2-122">-Registry</span></span>
<span data-ttu-id="06db2-123">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="06db2-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="06db2-124">-Registryname</span><span class="sxs-lookup"><span data-stu-id="06db2-124">-RegistryName</span></span>
<span data-ttu-id="06db2-125">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="06db2-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="06db2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06db2-126">-ResourceGroupName</span></span>
<span data-ttu-id="06db2-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="06db2-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="06db2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06db2-128">-ResourceId</span></span>
<span data-ttu-id="06db2-129">Identyfikator zasobu replikacji rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="06db2-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="06db2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06db2-130">CommonParameters</span></span>
<span data-ttu-id="06db2-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06db2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06db2-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06db2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06db2-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06db2-133">INPUTS</span></span>

### <span data-ttu-id="06db2-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="06db2-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="06db2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="06db2-135">System.String</span></span>

## <span data-ttu-id="06db2-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06db2-136">OUTPUTS</span></span>

### <span data-ttu-id="06db2-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="06db2-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="06db2-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06db2-138">NOTES</span></span>

## <span data-ttu-id="06db2-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06db2-139">RELATED LINKS</span></span>

[<span data-ttu-id="06db2-140">Nowe — AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="06db2-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="06db2-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="06db2-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)