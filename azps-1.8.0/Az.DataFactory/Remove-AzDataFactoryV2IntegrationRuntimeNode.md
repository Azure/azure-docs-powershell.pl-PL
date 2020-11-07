---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: dbf5b4eba8c6fe2dc55e55a58df79ed9b7d08afb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710093"
---
# <span data-ttu-id="98f5d-101">Remove-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="98f5d-101">Remove-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="98f5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="98f5d-103">Usuwanie węzła o podanej nazwie w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="98f5d-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="98f5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98f5d-104">SYNTAX</span></span>

### <span data-ttu-id="98f5d-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="98f5d-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98f5d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="98f5d-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98f5d-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="98f5d-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98f5d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="98f5d-108">DESCRIPTION</span></span>
<span data-ttu-id="98f5d-109">Polecenie cmdlet Remove-AzDataFactoryV2IntegrationRuntimeNode powoduje usunięcie węzła w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="98f5d-109">The Remove-AzDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="98f5d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98f5d-110">EXAMPLES</span></span>

### <span data-ttu-id="98f5d-111">Przykład 1: Usuwanie węzła z środowiska wykonawczego integracji</span><span class="sxs-lookup"><span data-stu-id="98f5d-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="98f5d-112">To polecenie usuwa węzeł o nazwie "Node_1" w środowisku wykonawczym integracji o nazwie "test-SelfHost-IR" w subskrypcji grupy zasobów o nazwie "RG-test-dfv2" i fabryki danych o nazwie "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="98f5d-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="98f5d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98f5d-113">PARAMETERS</span></span>

### <span data-ttu-id="98f5d-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="98f5d-114">-DataFactoryName</span></span>
<span data-ttu-id="98f5d-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="98f5d-115">The data factory name.</span></span>

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

### <span data-ttu-id="98f5d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f5d-116">-DefaultProfile</span></span>
<span data-ttu-id="98f5d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98f5d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98f5d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="98f5d-118">-Force</span></span>
<span data-ttu-id="98f5d-119">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="98f5d-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="98f5d-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="98f5d-120">-InputObject</span></span>
<span data-ttu-id="98f5d-121">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="98f5d-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="98f5d-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="98f5d-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="98f5d-123">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="98f5d-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98f5d-124">-Nodename</span><span class="sxs-lookup"><span data-stu-id="98f5d-124">-NodeName</span></span>
<span data-ttu-id="98f5d-125">Nazwa węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="98f5d-125">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f5d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f5d-126">-ResourceGroupName</span></span>
<span data-ttu-id="98f5d-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="98f5d-127">The resource group name.</span></span>

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

### <span data-ttu-id="98f5d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98f5d-128">-ResourceId</span></span>
<span data-ttu-id="98f5d-129">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="98f5d-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="98f5d-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98f5d-130">-Confirm</span></span>
<span data-ttu-id="98f5d-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98f5d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98f5d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98f5d-132">-WhatIf</span></span>
<span data-ttu-id="98f5d-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98f5d-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="98f5d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f5d-134">CommonParameters</span></span>
<span data-ttu-id="98f5d-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98f5d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f5d-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98f5d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f5d-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98f5d-137">INPUTS</span></span>

### <span data-ttu-id="98f5d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="98f5d-138">System.String</span></span>

### <span data-ttu-id="98f5d-139">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="98f5d-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="98f5d-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98f5d-140">OUTPUTS</span></span>

### <span data-ttu-id="98f5d-141">System. void</span><span class="sxs-lookup"><span data-stu-id="98f5d-141">System.Void</span></span>

## <span data-ttu-id="98f5d-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98f5d-142">NOTES</span></span>

## <span data-ttu-id="98f5d-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98f5d-143">RELATED LINKS</span></span>
