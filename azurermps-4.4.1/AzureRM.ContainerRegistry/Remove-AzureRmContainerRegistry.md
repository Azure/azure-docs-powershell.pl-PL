---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 5a5ea87044c18e82f4c17294356a35adb254eee4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527709"
---
# <span data-ttu-id="174bf-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="174bf-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="174bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="174bf-102">SYNOPSIS</span></span>
<span data-ttu-id="174bf-103">Usuwa rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="174bf-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="174bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="174bf-104">SYNTAX</span></span>

### <span data-ttu-id="174bf-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="174bf-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="174bf-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="174bf-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="174bf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="174bf-107">DESCRIPTION</span></span>
<span data-ttu-id="174bf-108">Polecenie cmdlet **Remove-AzureRmContainerRegistry** umożliwia usunięcie rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="174bf-108">The **Remove-AzureRmContainerRegistry** cmdlet removes a container registry.</span></span>

## <span data-ttu-id="174bf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="174bf-109">EXAMPLES</span></span>

### <span data-ttu-id="174bf-110">Przykład 1: usuwanie określonego rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="174bf-110">Example 1: Remove a specified container registry</span></span>
```
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="174bf-111">To polecenie umożliwia usunięcie określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="174bf-111">This command removes the specified container registry.</span></span>

## <span data-ttu-id="174bf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="174bf-112">PARAMETERS</span></span>

### <span data-ttu-id="174bf-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="174bf-113">-Name</span></span>
<span data-ttu-id="174bf-114">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="174bf-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="174bf-115">-Registry</span><span class="sxs-lookup"><span data-stu-id="174bf-115">-Registry</span></span>
<span data-ttu-id="174bf-116">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="174bf-116">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="174bf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="174bf-117">-ResourceGroupName</span></span>
<span data-ttu-id="174bf-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="174bf-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="174bf-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="174bf-119">-Confirm</span></span>
<span data-ttu-id="174bf-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="174bf-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="174bf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="174bf-121">-WhatIf</span></span>
<span data-ttu-id="174bf-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="174bf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="174bf-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="174bf-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="174bf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="174bf-124">-DefaultProfile</span></span>
<span data-ttu-id="174bf-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="174bf-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="174bf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="174bf-126">CommonParameters</span></span>
<span data-ttu-id="174bf-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="174bf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="174bf-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="174bf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="174bf-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="174bf-129">INPUTS</span></span>

### <span data-ttu-id="174bf-130">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="174bf-130">PSContainerRegistry</span></span>
<span data-ttu-id="174bf-131">Parametr "Registry" przyjmuje wartość typu "PSContainerRegistry" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="174bf-131">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="174bf-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="174bf-132">OUTPUTS</span></span>

### <span data-ttu-id="174bf-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="174bf-133">None</span></span>

## <span data-ttu-id="174bf-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="174bf-134">NOTES</span></span>

## <span data-ttu-id="174bf-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="174bf-135">RELATED LINKS</span></span>

[<span data-ttu-id="174bf-136">Nowe — AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="174bf-136">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="174bf-137">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="174bf-137">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="174bf-138">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="174bf-138">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

