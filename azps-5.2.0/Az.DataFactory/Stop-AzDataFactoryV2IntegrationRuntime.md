---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: aa838b24cc2410d9d699bac4dc8d4c00e3153174
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355042"
---
# <span data-ttu-id="72be9-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="72be9-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="72be9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72be9-102">SYNOPSIS</span></span>
<span data-ttu-id="72be9-103">Zatrzymuje zarządzane dedykowane środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="72be9-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="72be9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72be9-104">SYNTAX</span></span>

### <span data-ttu-id="72be9-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="72be9-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72be9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="72be9-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72be9-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="72be9-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72be9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="72be9-108">DESCRIPTION</span></span>
<span data-ttu-id="72be9-109">Polecenie cmdlet **stop-AzDataFactoryV2IntegrationRuntime** zatrzymuje zarządzane dedykowane środowisko uruchomieniowe integracji w stanie uruchomionym, który został uruchomiony przez polecenie cmdlet Start-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="72be9-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="72be9-110">Zasoby są zwalniane i przetransferowano stan do "Zatrzymano".</span><span class="sxs-lookup"><span data-stu-id="72be9-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="72be9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72be9-111">EXAMPLES</span></span>

### <span data-ttu-id="72be9-112">Przykład 1: zatrzymanie zarządzanego środowiska uruchomieniowego integracji, które jest w stanie uruchomionym.</span><span class="sxs-lookup"><span data-stu-id="72be9-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="72be9-113">Stan programu Managed Integration Runtime "test-reserlved-IR" jest w stanie "uruchomiony".</span><span class="sxs-lookup"><span data-stu-id="72be9-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="72be9-114">Po uruchomieniu polecenia cmdlet Stop-AzDataFactoryV2IntegrationRuntime zasoby są zwalniane, a transfery stanowe są przekazywane do "zatrzymane".</span><span class="sxs-lookup"><span data-stu-id="72be9-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="72be9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72be9-115">PARAMETERS</span></span>

### <span data-ttu-id="72be9-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="72be9-116">-DataFactoryName</span></span>
<span data-ttu-id="72be9-117">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="72be9-117">The data factory name.</span></span>

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

### <span data-ttu-id="72be9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72be9-118">-DefaultProfile</span></span>
<span data-ttu-id="72be9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="72be9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72be9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="72be9-120">-Force</span></span>
<span data-ttu-id="72be9-121">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="72be9-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="72be9-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="72be9-122">-InputObject</span></span>
<span data-ttu-id="72be9-123">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="72be9-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="72be9-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="72be9-124">-Name</span></span>
<span data-ttu-id="72be9-125">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="72be9-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="72be9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72be9-126">-ResourceGroupName</span></span>
<span data-ttu-id="72be9-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="72be9-127">The resource group name.</span></span>

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

### <span data-ttu-id="72be9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72be9-128">-ResourceId</span></span>
<span data-ttu-id="72be9-129">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="72be9-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="72be9-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72be9-130">-Confirm</span></span>
<span data-ttu-id="72be9-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72be9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72be9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72be9-132">-WhatIf</span></span>
<span data-ttu-id="72be9-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72be9-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="72be9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72be9-134">CommonParameters</span></span>
<span data-ttu-id="72be9-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72be9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72be9-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72be9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72be9-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72be9-137">INPUTS</span></span>

### <span data-ttu-id="72be9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="72be9-138">System.String</span></span>

### <span data-ttu-id="72be9-139">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="72be9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="72be9-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72be9-140">OUTPUTS</span></span>

### <span data-ttu-id="72be9-141">System. void</span><span class="sxs-lookup"><span data-stu-id="72be9-141">System.Void</span></span>

## <span data-ttu-id="72be9-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72be9-142">NOTES</span></span>
<span data-ttu-id="72be9-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="72be9-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="72be9-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72be9-144">RELATED LINKS</span></span>

[<span data-ttu-id="72be9-145">Start — AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="72be9-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
