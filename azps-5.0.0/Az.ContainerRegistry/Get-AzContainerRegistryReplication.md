---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 57b482368834d91e36a3f557c9657c82cea24f4e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224549"
---
# <span data-ttu-id="cd17e-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cd17e-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="cd17e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd17e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd17e-103">Pobiera replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="cd17e-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="cd17e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd17e-104">SYNTAX</span></span>

### <span data-ttu-id="cd17e-105">ListReplicationByNameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd17e-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd17e-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd17e-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd17e-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd17e-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd17e-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd17e-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd17e-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd17e-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd17e-110">Opis</span><span class="sxs-lookup"><span data-stu-id="cd17e-110">DESCRIPTION</span></span>
<span data-ttu-id="cd17e-111">Polecenie cmdlet Get-AzContainerRegistryReplication pobiera określoną replikację rejestru kontenera lub wszystkich replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="cd17e-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="cd17e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd17e-112">EXAMPLES</span></span>

### <span data-ttu-id="cd17e-113">Przykład 1: Pobiera określoną replikację rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="cd17e-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="cd17e-114">Pobiera określoną replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="cd17e-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="cd17e-115">Przykład 2: Pobiera wszystkie replikacje rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="cd17e-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="cd17e-116">Pobiera wszystkie replikacje rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="cd17e-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="cd17e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd17e-117">PARAMETERS</span></span>

### <span data-ttu-id="cd17e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd17e-118">-DefaultProfile</span></span>
<span data-ttu-id="cd17e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd17e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd17e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd17e-120">-Name</span></span>
<span data-ttu-id="cd17e-121">Nazwa replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="cd17e-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="cd17e-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="cd17e-122">-Registry</span></span>
<span data-ttu-id="cd17e-123">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="cd17e-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="cd17e-124">-Registryname</span><span class="sxs-lookup"><span data-stu-id="cd17e-124">-RegistryName</span></span>
<span data-ttu-id="cd17e-125">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="cd17e-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="cd17e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd17e-126">-ResourceGroupName</span></span>
<span data-ttu-id="cd17e-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd17e-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="cd17e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd17e-128">-ResourceId</span></span>
<span data-ttu-id="cd17e-129">Identyfikator zasobu replikacji rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="cd17e-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="cd17e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd17e-130">CommonParameters</span></span>
<span data-ttu-id="cd17e-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd17e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd17e-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd17e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd17e-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd17e-133">INPUTS</span></span>

### <span data-ttu-id="cd17e-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cd17e-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="cd17e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="cd17e-135">System.String</span></span>

## <span data-ttu-id="cd17e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd17e-136">OUTPUTS</span></span>

### <span data-ttu-id="cd17e-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cd17e-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="cd17e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd17e-138">NOTES</span></span>

## <span data-ttu-id="cd17e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd17e-139">RELATED LINKS</span></span>

[<span data-ttu-id="cd17e-140">Nowe — AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cd17e-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="cd17e-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cd17e-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)