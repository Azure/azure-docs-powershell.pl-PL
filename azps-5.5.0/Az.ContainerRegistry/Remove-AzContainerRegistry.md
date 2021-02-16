---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: d36e362f1782e3566bc0d2febd65aebd4c68220d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199123"
---
# <span data-ttu-id="a8959-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a8959-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="a8959-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8959-102">SYNOPSIS</span></span>
<span data-ttu-id="a8959-103">Usuwa rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="a8959-103">Removes a container registry.</span></span>

## <span data-ttu-id="a8959-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a8959-104">SYNTAX</span></span>

### <span data-ttu-id="a8959-105">NameResourceGroupParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a8959-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8959-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8959-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8959-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8959-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8959-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a8959-108">DESCRIPTION</span></span>
<span data-ttu-id="a8959-109">Polecenie Remove-AzContainerRegistry cmdlet usuwa rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="a8959-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="a8959-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a8959-110">EXAMPLES</span></span>

### <span data-ttu-id="a8959-111">Przykład 1. Usuwanie określonego rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="a8959-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="a8959-112">To polecenie usuwa określony rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="a8959-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="a8959-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8959-113">PARAMETERS</span></span>

### <span data-ttu-id="a8959-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8959-114">-DefaultProfile</span></span>
<span data-ttu-id="a8959-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a8959-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8959-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a8959-116">-Name</span></span>
<span data-ttu-id="a8959-117">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="a8959-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8959-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8959-118">-PassThru</span></span>
<span data-ttu-id="a8959-119">Wskazuje, że to polecenie cmdlet zwraca wartość prawda, jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="a8959-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="a8959-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="a8959-120">-Registry</span></span>
<span data-ttu-id="a8959-121">Obiekt Container Registry.</span><span class="sxs-lookup"><span data-stu-id="a8959-121">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8959-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8959-122">-ResourceGroupName</span></span>
<span data-ttu-id="a8959-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a8959-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8959-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8959-124">-ResourceId</span></span>
<span data-ttu-id="a8959-125">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="a8959-125">The container registry resource id</span></span>

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

### <span data-ttu-id="a8959-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a8959-126">-Confirm</span></span>
<span data-ttu-id="a8959-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a8959-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8959-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8959-128">-WhatIf</span></span>
<span data-ttu-id="a8959-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8959-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8959-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a8959-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8959-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8959-131">CommonParameters</span></span>
<span data-ttu-id="a8959-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8959-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8959-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8959-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8959-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8959-134">INPUTS</span></span>

### <span data-ttu-id="a8959-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a8959-135">System.String</span></span>

## <span data-ttu-id="a8959-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8959-136">OUTPUTS</span></span>

### <span data-ttu-id="a8959-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a8959-137">System.Boolean</span></span>

## <span data-ttu-id="a8959-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a8959-138">NOTES</span></span>

## <span data-ttu-id="a8959-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8959-139">RELATED LINKS</span></span>

[<span data-ttu-id="a8959-140">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a8959-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="a8959-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a8959-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="a8959-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a8959-142">Update-AzContainerRegistry</span></span>]()

