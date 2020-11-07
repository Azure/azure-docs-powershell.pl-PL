---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 824b3226b29ba381b9ed963bf6a21f4691c17733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717210"
---
# <span data-ttu-id="c6639-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c6639-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="c6639-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6639-102">SYNOPSIS</span></span>
<span data-ttu-id="c6639-103">Usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c6639-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6639-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6639-104">SYNTAX</span></span>

### <span data-ttu-id="c6639-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c6639-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6639-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6639-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6639-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6639-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6639-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c6639-108">DESCRIPTION</span></span>
<span data-ttu-id="c6639-109">Polecenie cmdlet Remove-AzureRmContainerRegistryReplication usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c6639-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="c6639-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6639-110">EXAMPLES</span></span>

### <span data-ttu-id="c6639-111">Przykład 1: usunięcie replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c6639-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="c6639-112">Usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c6639-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="c6639-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6639-113">PARAMETERS</span></span>

### <span data-ttu-id="c6639-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c6639-114">-Confirm</span></span>
<span data-ttu-id="c6639-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6639-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6639-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6639-116">-DefaultProfile</span></span>
<span data-ttu-id="c6639-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6639-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6639-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c6639-118">-Name</span></span>
<span data-ttu-id="c6639-119">Nazwa replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c6639-119">Container Registry Replication Name.</span></span>
<span data-ttu-id="c6639-120">Domyślnie jest to nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c6639-120">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6639-121">-Registryname</span><span class="sxs-lookup"><span data-stu-id="c6639-121">-RegistryName</span></span>
<span data-ttu-id="c6639-122">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c6639-122">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6639-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="c6639-123">-Replicatoin</span></span>
<span data-ttu-id="c6639-124">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c6639-124">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6639-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6639-125">-ResourceGroupName</span></span>
<span data-ttu-id="c6639-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c6639-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6639-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6639-127">-ResourceId</span></span>
<span data-ttu-id="c6639-128">Identyfikator zasobu replikacji rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="c6639-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="c6639-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6639-129">-WhatIf</span></span>
<span data-ttu-id="c6639-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6639-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6639-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c6639-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6639-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6639-132">-PassThru</span></span>
<span data-ttu-id="c6639-133">Wskazuje, że to polecenie cmdlet zwraca wartość PRAWDA, Jeśli usunięcie się powiodło.</span><span class="sxs-lookup"><span data-stu-id="c6639-133">Indicates that this cmdlet returns true if the removal was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6639-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6639-134">CommonParameters</span></span>
<span data-ttu-id="c6639-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6639-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6639-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6639-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6639-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6639-137">INPUTS</span></span>

### <span data-ttu-id="c6639-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c6639-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="c6639-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c6639-139">System.String</span></span>

## <span data-ttu-id="c6639-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6639-140">OUTPUTS</span></span>

### <span data-ttu-id="c6639-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="c6639-141">System.Object</span></span>

## <span data-ttu-id="c6639-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6639-142">NOTES</span></span>

## <span data-ttu-id="c6639-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6639-143">RELATED LINKS</span></span>

[<span data-ttu-id="c6639-144">Nowe — AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c6639-144">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="c6639-145">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c6639-145">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

