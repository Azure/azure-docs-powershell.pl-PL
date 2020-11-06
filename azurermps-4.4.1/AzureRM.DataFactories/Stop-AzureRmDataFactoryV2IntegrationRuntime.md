---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: f8c935dee7d5cf2dbb49d832d8c4069ddcb5612a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550019"
---
# <span data-ttu-id="5224e-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5224e-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="5224e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5224e-102">SYNOPSIS</span></span>
<span data-ttu-id="5224e-103">Zatrzymuje zarządzane dedykowane środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="5224e-103">Stops a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5224e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5224e-104">SYNTAX</span></span>

### <span data-ttu-id="5224e-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5224e-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5224e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5224e-106">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5224e-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="5224e-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5224e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5224e-108">DESCRIPTION</span></span>
<span data-ttu-id="5224e-109">Polecenie cmdlet **stop-AzureRmDataFactoryV2IntegrationRuntime** zatrzymuje zarządzane dedykowane środowisko uruchomieniowe integracji w stanie uruchomionym, który został uruchomiony przez polecenie cmdlet Start-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="5224e-109">The **Stop-AzureRmDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="5224e-110">Zasoby są zwalniane i przetransferowano stan do "Zatrzymano".</span><span class="sxs-lookup"><span data-stu-id="5224e-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="5224e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5224e-111">EXAMPLES</span></span>

### <span data-ttu-id="5224e-112">Przykład 1: zatrzymanie zarządzanego środowiska uruchomieniowego integracji, które jest w stanie uruchomionym.</span><span class="sxs-lookup"><span data-stu-id="5224e-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="5224e-113">Stan programu Managed Integration Runtime "test-reserlved-IR" jest w stanie "uruchomiony".</span><span class="sxs-lookup"><span data-stu-id="5224e-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="5224e-114">Po uruchomieniu polecenia cmdlet Stop-AzureRmDataFactoryV2IntegrationRuntime zasoby są zwalniane, a transfery stanowe są przekazywane do "zatrzymane".</span><span class="sxs-lookup"><span data-stu-id="5224e-114">After running Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="5224e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5224e-115">PARAMETERS</span></span>

### <span data-ttu-id="5224e-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5224e-116">-Confirm</span></span>
<span data-ttu-id="5224e-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5224e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5224e-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5224e-118">-DataFactoryName</span></span>
<span data-ttu-id="5224e-119">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="5224e-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5224e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5224e-120">-Force</span></span>
<span data-ttu-id="5224e-121">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5224e-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5224e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5224e-122">-InputObject</span></span>
<span data-ttu-id="5224e-123">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="5224e-123">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5224e-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5224e-124">-Name</span></span>
<span data-ttu-id="5224e-125">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="5224e-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5224e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5224e-126">-ResourceGroupName</span></span>
<span data-ttu-id="5224e-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5224e-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5224e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5224e-128">-ResourceId</span></span>
<span data-ttu-id="5224e-129">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5224e-129">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5224e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5224e-130">-WhatIf</span></span>
<span data-ttu-id="5224e-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5224e-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5224e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5224e-132">-DefaultProfile</span></span>
<span data-ttu-id="5224e-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5224e-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5224e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5224e-134">CommonParameters</span></span>
<span data-ttu-id="5224e-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5224e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5224e-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5224e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5224e-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5224e-137">INPUTS</span></span>

### <span data-ttu-id="5224e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5224e-138">System.String</span></span>
<span data-ttu-id="5224e-139">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5224e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5224e-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5224e-140">OUTPUTS</span></span>

### <span data-ttu-id="5224e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5224e-141">System.Boolean</span></span>

## <span data-ttu-id="5224e-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5224e-142">NOTES</span></span>
<span data-ttu-id="5224e-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="5224e-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="5224e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5224e-144">RELATED LINKS</span></span>

[<span data-ttu-id="5224e-145">Start — AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5224e-145">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
