---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 81b05b8229530a8975be023a3b4a5e8c93d93c80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553936"
---
# <span data-ttu-id="dbab4-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dbab4-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="dbab4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dbab4-102">SYNOPSIS</span></span>
<span data-ttu-id="dbab4-103">Usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="dbab4-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbab4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dbab4-104">SYNTAX</span></span>

### <span data-ttu-id="dbab4-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dbab4-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="dbab4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dbab4-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="dbab4-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="dbab4-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="dbab4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dbab4-108">DESCRIPTION</span></span>
<span data-ttu-id="dbab4-109">Polecenie cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="dbab4-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="dbab4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dbab4-110">EXAMPLES</span></span>

### <span data-ttu-id="dbab4-111">Przykład 1: usuwanie środowiska wykonawczego integracji</span><span class="sxs-lookup"><span data-stu-id="dbab4-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="dbab4-112">To polecenie usuwa środowisko uruchomieniowe integracji o nazwie test-zastrzeżonym-IR ' z fabryki danych o nazwie test-DF.</span><span class="sxs-lookup"><span data-stu-id="dbab4-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="dbab4-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="dbab4-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="dbab4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dbab4-114">PARAMETERS</span></span>

### <span data-ttu-id="dbab4-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="dbab4-115">-DataFactoryName</span></span>
<span data-ttu-id="dbab4-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="dbab4-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbab4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dbab4-117">-Force</span></span>
<span data-ttu-id="dbab4-118">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dbab4-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="dbab4-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dbab4-119">-InputObject</span></span>
<span data-ttu-id="dbab4-120">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="dbab4-120">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbab4-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dbab4-121">-Name</span></span>
<span data-ttu-id="dbab4-122">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dbab4-122">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbab4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbab4-123">-ResourceGroupName</span></span>
<span data-ttu-id="dbab4-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dbab4-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbab4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbab4-125">-ResourceId</span></span>
<span data-ttu-id="dbab4-126">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dbab4-126">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbab4-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dbab4-127">-Confirm</span></span>
<span data-ttu-id="dbab4-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbab4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbab4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbab4-129">-WhatIf</span></span>
<span data-ttu-id="dbab4-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbab4-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="dbab4-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbab4-131">INPUTS</span></span>

### <span data-ttu-id="dbab4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dbab4-132">System.String</span></span>
<span data-ttu-id="dbab4-133">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dbab4-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="dbab4-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dbab4-134">OUTPUTS</span></span>

### <span data-ttu-id="dbab4-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="dbab4-135">System.Object</span></span>

## <span data-ttu-id="dbab4-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dbab4-136">NOTES</span></span>
<span data-ttu-id="dbab4-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="dbab4-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="dbab4-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dbab4-138">RELATED LINKS</span></span>
[<span data-ttu-id="dbab4-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dbab4-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="dbab4-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dbab4-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

