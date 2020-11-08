---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: d36e362f1782e3566bc0d2febd65aebd4c68220d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224545"
---
# <span data-ttu-id="9556c-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9556c-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="9556c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9556c-102">SYNOPSIS</span></span>
<span data-ttu-id="9556c-103">Usuwa rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="9556c-103">Removes a container registry.</span></span>

## <span data-ttu-id="9556c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9556c-104">SYNTAX</span></span>

### <span data-ttu-id="9556c-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9556c-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9556c-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9556c-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9556c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9556c-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9556c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9556c-108">DESCRIPTION</span></span>
<span data-ttu-id="9556c-109">Polecenie cmdlet Remove-AzContainerRegistry powoduje usunięcie rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="9556c-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="9556c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9556c-110">EXAMPLES</span></span>

### <span data-ttu-id="9556c-111">Przykład 1: usuwanie określonego rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="9556c-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="9556c-112">To polecenie umożliwia usunięcie określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="9556c-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="9556c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9556c-113">PARAMETERS</span></span>

### <span data-ttu-id="9556c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9556c-114">-DefaultProfile</span></span>
<span data-ttu-id="9556c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9556c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9556c-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9556c-116">-Name</span></span>
<span data-ttu-id="9556c-117">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="9556c-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="9556c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9556c-118">-PassThru</span></span>
<span data-ttu-id="9556c-119">Wskazuje, że to polecenie cmdlet zwraca wartość PRAWDA, Jeśli usunięcie się powiodło.</span><span class="sxs-lookup"><span data-stu-id="9556c-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="9556c-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="9556c-120">-Registry</span></span>
<span data-ttu-id="9556c-121">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="9556c-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="9556c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9556c-122">-ResourceGroupName</span></span>
<span data-ttu-id="9556c-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9556c-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="9556c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9556c-124">-ResourceId</span></span>
<span data-ttu-id="9556c-125">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="9556c-125">The container registry resource id</span></span>

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

### <span data-ttu-id="9556c-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9556c-126">-Confirm</span></span>
<span data-ttu-id="9556c-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9556c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9556c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9556c-128">-WhatIf</span></span>
<span data-ttu-id="9556c-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9556c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9556c-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9556c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9556c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9556c-131">CommonParameters</span></span>
<span data-ttu-id="9556c-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9556c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9556c-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9556c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9556c-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9556c-134">INPUTS</span></span>

### <span data-ttu-id="9556c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9556c-135">System.String</span></span>

## <span data-ttu-id="9556c-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9556c-136">OUTPUTS</span></span>

### <span data-ttu-id="9556c-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9556c-137">System.Boolean</span></span>

## <span data-ttu-id="9556c-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9556c-138">NOTES</span></span>

## <span data-ttu-id="9556c-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9556c-139">RELATED LINKS</span></span>

[<span data-ttu-id="9556c-140">Nowe — AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9556c-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="9556c-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9556c-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="9556c-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9556c-142">Update-AzContainerRegistry</span></span>]()

