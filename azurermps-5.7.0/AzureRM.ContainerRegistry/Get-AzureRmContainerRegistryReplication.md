---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: db03414e9cebe4c1593013a928b8a66d9b70bd91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542688"
---
# <span data-ttu-id="1af56-101">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="1af56-101">Get-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="1af56-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1af56-102">SYNOPSIS</span></span>
<span data-ttu-id="1af56-103">Pobiera replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="1af56-103">Gets a replication of a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1af56-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1af56-104">SYNTAX</span></span>

### <span data-ttu-id="1af56-105">ListReplicationByNameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1af56-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1af56-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="1af56-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1af56-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1af56-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1af56-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1af56-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1af56-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1af56-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1af56-110">Opis</span><span class="sxs-lookup"><span data-stu-id="1af56-110">DESCRIPTION</span></span>
<span data-ttu-id="1af56-111">Polecenie cmdlet Get-AzureRmContainerRegistryReplication pobiera określoną replikację rejestru kontenera lub wszystkich replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="1af56-111">The Get-AzureRmContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="1af56-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1af56-112">EXAMPLES</span></span>

### <span data-ttu-id="1af56-113">Przykład 1: Pobiera określoną replikację rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="1af56-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="1af56-114">Pobiera określoną replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="1af56-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="1af56-115">Przykład 2: Pobiera wszystkie replikacje rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="1af56-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="1af56-116">Pobiera wszystkie replikacje rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="1af56-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="1af56-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1af56-117">PARAMETERS</span></span>

### <span data-ttu-id="1af56-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af56-118">-DefaultProfile</span></span>
<span data-ttu-id="1af56-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1af56-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1af56-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1af56-120">-Name</span></span>
<span data-ttu-id="1af56-121">Nazwa replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="1af56-121">Container Registry Replication Name.</span></span>

```yaml
Type: String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af56-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="1af56-122">-Registry</span></span>
<span data-ttu-id="1af56-123">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="1af56-123">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1af56-124">-Registryname</span><span class="sxs-lookup"><span data-stu-id="1af56-124">-RegistryName</span></span>
<span data-ttu-id="1af56-125">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="1af56-125">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af56-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af56-126">-ResourceGroupName</span></span>
<span data-ttu-id="1af56-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1af56-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af56-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1af56-128">-ResourceId</span></span>
<span data-ttu-id="1af56-129">Identyfikator zasobu replikacji rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="1af56-129">The container registry replication resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af56-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af56-130">CommonParameters</span></span>
<span data-ttu-id="1af56-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1af56-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af56-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1af56-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af56-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1af56-133">INPUTS</span></span>

### <span data-ttu-id="1af56-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1af56-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="1af56-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1af56-135">System.String</span></span>

## <span data-ttu-id="1af56-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1af56-136">OUTPUTS</span></span>

### <span data-ttu-id="1af56-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="1af56-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="1af56-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication []</span><span class="sxs-lookup"><span data-stu-id="1af56-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication[]</span></span>

## <span data-ttu-id="1af56-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1af56-139">NOTES</span></span>

## <span data-ttu-id="1af56-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1af56-140">RELATED LINKS</span></span>

[<span data-ttu-id="1af56-141">Nowe — AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="1af56-141">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="1af56-142">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="1af56-142">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
