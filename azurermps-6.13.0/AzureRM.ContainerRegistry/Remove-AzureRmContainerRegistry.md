---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 2235e533e999fedbb06b79548bf4e2ce8de3586a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718346"
---
# <span data-ttu-id="02836-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="02836-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="02836-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02836-102">SYNOPSIS</span></span>
<span data-ttu-id="02836-103">Usuwa rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="02836-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02836-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02836-104">SYNTAX</span></span>

### <span data-ttu-id="02836-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="02836-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02836-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02836-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02836-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02836-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02836-108">Opis</span><span class="sxs-lookup"><span data-stu-id="02836-108">DESCRIPTION</span></span>
<span data-ttu-id="02836-109">Polecenie cmdlet Remove-AzureRmContainerRegistry powoduje usunięcie rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="02836-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="02836-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02836-110">EXAMPLES</span></span>

### <span data-ttu-id="02836-111">Przykład 1: usuwanie określonego rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="02836-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="02836-112">To polecenie umożliwia usunięcie określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="02836-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="02836-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02836-113">PARAMETERS</span></span>

### <span data-ttu-id="02836-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02836-114">-DefaultProfile</span></span>
<span data-ttu-id="02836-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="02836-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02836-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02836-116">-Name</span></span>
<span data-ttu-id="02836-117">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="02836-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="02836-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02836-118">-PassThru</span></span>
<span data-ttu-id="02836-119">Wskazuje, że to polecenie cmdlet zwraca wartość PRAWDA, Jeśli usunięcie się powiodło.</span><span class="sxs-lookup"><span data-stu-id="02836-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="02836-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="02836-120">-Registry</span></span>
<span data-ttu-id="02836-121">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="02836-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="02836-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02836-122">-ResourceGroupName</span></span>
<span data-ttu-id="02836-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="02836-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="02836-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02836-124">-ResourceId</span></span>
<span data-ttu-id="02836-125">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="02836-125">The container registry resource id</span></span>

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

### <span data-ttu-id="02836-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02836-126">-Confirm</span></span>
<span data-ttu-id="02836-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02836-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02836-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02836-128">-WhatIf</span></span>
<span data-ttu-id="02836-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02836-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02836-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02836-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02836-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02836-131">CommonParameters</span></span>
<span data-ttu-id="02836-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02836-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02836-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02836-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02836-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02836-134">INPUTS</span></span>

### <span data-ttu-id="02836-135">System. String</span><span class="sxs-lookup"><span data-stu-id="02836-135">System.String</span></span>

## <span data-ttu-id="02836-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02836-136">OUTPUTS</span></span>

### <span data-ttu-id="02836-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02836-137">System.Boolean</span></span>

## <span data-ttu-id="02836-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02836-138">NOTES</span></span>

## <span data-ttu-id="02836-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02836-139">RELATED LINKS</span></span>

[<span data-ttu-id="02836-140">Nowe — AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="02836-140">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="02836-141">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="02836-141">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="02836-142">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="02836-142">Update-AzureRmContainerRegistry</span></span>]()

