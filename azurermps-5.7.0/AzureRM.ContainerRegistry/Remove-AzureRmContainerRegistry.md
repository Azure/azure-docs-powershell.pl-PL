---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: df0c938db8f44ebffedc9760e4a3d33ee175ae01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546819"
---
# <span data-ttu-id="8c26b-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8c26b-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="8c26b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c26b-102">SYNOPSIS</span></span>
<span data-ttu-id="8c26b-103">Usuwa rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="8c26b-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c26b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c26b-104">SYNTAX</span></span>

### <span data-ttu-id="8c26b-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8c26b-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c26b-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c26b-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c26b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c26b-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c26b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8c26b-108">DESCRIPTION</span></span>
<span data-ttu-id="8c26b-109">Polecenie cmdlet Remove-AzureRmContainerRegistry powoduje usunięcie rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="8c26b-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="8c26b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c26b-110">EXAMPLES</span></span>

### <span data-ttu-id="8c26b-111">Przykład 1: usuwanie określonego rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="8c26b-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="8c26b-112">To polecenie umożliwia usunięcie określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="8c26b-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="8c26b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c26b-113">PARAMETERS</span></span>

### <span data-ttu-id="8c26b-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8c26b-114">-Name</span></span>
<span data-ttu-id="8c26b-115">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="8c26b-115">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c26b-116">-Registry</span><span class="sxs-lookup"><span data-stu-id="8c26b-116">-Registry</span></span>
<span data-ttu-id="8c26b-117">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="8c26b-117">Container Registry Object.</span></span>

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

### <span data-ttu-id="8c26b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c26b-118">-ResourceGroupName</span></span>
<span data-ttu-id="8c26b-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c26b-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="8c26b-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c26b-120">-Confirm</span></span>
<span data-ttu-id="8c26b-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c26b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c26b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c26b-122">-WhatIf</span></span>
<span data-ttu-id="8c26b-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c26b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c26b-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8c26b-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c26b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c26b-125">-DefaultProfile</span></span>
<span data-ttu-id="8c26b-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8c26b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c26b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c26b-127">-ResourceId</span></span>
<span data-ttu-id="8c26b-128">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="8c26b-128">The container registry resource id</span></span>

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

### <span data-ttu-id="8c26b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c26b-129">-PassThru</span></span>
<span data-ttu-id="8c26b-130">Wskazuje, że to polecenie cmdlet zwraca wartość PRAWDA, Jeśli usunięcie się powiodło.</span><span class="sxs-lookup"><span data-stu-id="8c26b-130">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="8c26b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c26b-131">CommonParameters</span></span>
<span data-ttu-id="8c26b-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c26b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c26b-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c26b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c26b-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c26b-134">INPUTS</span></span>

### <span data-ttu-id="8c26b-135">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8c26b-135">PSContainerRegistry</span></span>
<span data-ttu-id="8c26b-136">Parametr "Registry" przyjmuje wartość typu "PSContainerRegistry" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="8c26b-136">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="8c26b-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c26b-137">OUTPUTS</span></span>

### <span data-ttu-id="8c26b-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8c26b-138">None</span></span>

## <span data-ttu-id="8c26b-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c26b-139">NOTES</span></span>

## <span data-ttu-id="8c26b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c26b-140">RELATED LINKS</span></span>

[<span data-ttu-id="8c26b-141">Nowe — AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8c26b-141">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="8c26b-142">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8c26b-142">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="8c26b-143">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8c26b-143">Update-AzureRmContainerRegistry</span></span>]()

