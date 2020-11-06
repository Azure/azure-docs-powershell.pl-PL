---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: a2515b3713f449d25963af5952e233117e078ba9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525177"
---
# <span data-ttu-id="6ca90-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6ca90-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="6ca90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ca90-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca90-103">Usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="6ca90-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ca90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ca90-104">SYNTAX</span></span>

### <span data-ttu-id="6ca90-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6ca90-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ca90-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6ca90-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca90-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="6ca90-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ca90-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6ca90-108">DESCRIPTION</span></span>
<span data-ttu-id="6ca90-109">Polecenie cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="6ca90-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="6ca90-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ca90-110">EXAMPLES</span></span>

### <span data-ttu-id="6ca90-111">Przykład 1: usuwanie środowiska wykonawczego integracji</span><span class="sxs-lookup"><span data-stu-id="6ca90-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="6ca90-112">To polecenie usuwa środowisko uruchomieniowe integracji o nazwie test-zastrzeżonym-IR ' z fabryki danych o nazwie test-DF.</span><span class="sxs-lookup"><span data-stu-id="6ca90-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="6ca90-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="6ca90-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="6ca90-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ca90-114">PARAMETERS</span></span>

### <span data-ttu-id="6ca90-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6ca90-115">-DataFactoryName</span></span>
<span data-ttu-id="6ca90-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="6ca90-116">The data factory name.</span></span>

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

### <span data-ttu-id="6ca90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca90-117">-DefaultProfile</span></span>
<span data-ttu-id="6ca90-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ca90-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ca90-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6ca90-119">-Force</span></span>
<span data-ttu-id="6ca90-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6ca90-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6ca90-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6ca90-121">-InputObject</span></span>
<span data-ttu-id="6ca90-122">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="6ca90-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="6ca90-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6ca90-123">-Name</span></span>
<span data-ttu-id="6ca90-124">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="6ca90-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="6ca90-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca90-125">-ResourceGroupName</span></span>
<span data-ttu-id="6ca90-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ca90-126">The resource group name.</span></span>

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

### <span data-ttu-id="6ca90-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ca90-127">-ResourceId</span></span>
<span data-ttu-id="6ca90-128">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6ca90-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6ca90-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ca90-129">-Confirm</span></span>
<span data-ttu-id="6ca90-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ca90-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ca90-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ca90-131">-WhatIf</span></span>
<span data-ttu-id="6ca90-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ca90-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6ca90-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca90-133">CommonParameters</span></span>
<span data-ttu-id="6ca90-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca90-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca90-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ca90-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca90-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ca90-136">INPUTS</span></span>

### <span data-ttu-id="6ca90-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6ca90-137">System.String</span></span>
<span data-ttu-id="6ca90-138">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6ca90-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6ca90-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ca90-139">OUTPUTS</span></span>

### <span data-ttu-id="6ca90-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="6ca90-140">System.Object</span></span>

## <span data-ttu-id="6ca90-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ca90-141">NOTES</span></span>
<span data-ttu-id="6ca90-142">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="6ca90-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="6ca90-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ca90-143">RELATED LINKS</span></span>

[<span data-ttu-id="6ca90-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6ca90-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="6ca90-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6ca90-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

