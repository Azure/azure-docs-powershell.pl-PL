---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 31170e24e88f6ce25c9fd344d254189eeeae64f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717214"
---
# <span data-ttu-id="7e352-101">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7e352-101">New-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="7e352-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e352-102">SYNOPSIS</span></span>
<span data-ttu-id="7e352-103">Tworzy replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7e352-103">Creates a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e352-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e352-104">SYNTAX</span></span>

### <span data-ttu-id="7e352-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7e352-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 -Location <String> [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e352-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e352-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e352-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e352-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e352-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7e352-108">DESCRIPTION</span></span>
<span data-ttu-id="7e352-109">Polecenie cmdlet New-AzureRmContainerRegistryReplication tworzy nową replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7e352-109">The New-AzureRmContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="7e352-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e352-110">EXAMPLES</span></span>

### <span data-ttu-id="7e352-111">Przykład 1: Tworzenie nowej replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7e352-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="7e352-112">Tworzenie nowej replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7e352-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="7e352-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e352-113">PARAMETERS</span></span>

### <span data-ttu-id="7e352-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e352-114">-Confirm</span></span>
<span data-ttu-id="7e352-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e352-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e352-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e352-116">-DefaultProfile</span></span>
<span data-ttu-id="7e352-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e352-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e352-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7e352-118">-Location</span></span>
<span data-ttu-id="7e352-119">Lokalizacja rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7e352-119">Container Registry Location.</span></span>
<span data-ttu-id="7e352-120">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7e352-120">Default to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e352-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7e352-121">-Name</span></span>
<span data-ttu-id="7e352-122">Nazwa replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7e352-122">Container Registry Replication Name.</span></span>
<span data-ttu-id="7e352-123">Domyślnie jest to nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="7e352-123">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e352-124">-Registry</span><span class="sxs-lookup"><span data-stu-id="7e352-124">-Registry</span></span>
<span data-ttu-id="7e352-125">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7e352-125">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e352-126">-Registryname</span><span class="sxs-lookup"><span data-stu-id="7e352-126">-RegistryName</span></span>
<span data-ttu-id="7e352-127">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7e352-127">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e352-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e352-128">-ResourceGroupName</span></span>
<span data-ttu-id="7e352-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7e352-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e352-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e352-130">-ResourceId</span></span>
<span data-ttu-id="7e352-131">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="7e352-131">The container registry resource id</span></span>

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

### <span data-ttu-id="7e352-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e352-132">-Tag</span></span>
<span data-ttu-id="7e352-133">Znaczniki rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7e352-133">Container Registry Tags.</span></span>

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

### <span data-ttu-id="7e352-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e352-134">-WhatIf</span></span>
<span data-ttu-id="7e352-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e352-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e352-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7e352-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e352-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e352-137">CommonParameters</span></span>
<span data-ttu-id="7e352-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e352-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e352-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e352-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e352-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e352-140">INPUTS</span></span>

### <span data-ttu-id="7e352-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7e352-141">System.String</span></span>

## <span data-ttu-id="7e352-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e352-142">OUTPUTS</span></span>

### <span data-ttu-id="7e352-143">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7e352-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="7e352-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e352-144">NOTES</span></span>

## <span data-ttu-id="7e352-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e352-145">RELATED LINKS</span></span>

[<span data-ttu-id="7e352-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7e352-146">Get-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="7e352-147">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7e352-147">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
