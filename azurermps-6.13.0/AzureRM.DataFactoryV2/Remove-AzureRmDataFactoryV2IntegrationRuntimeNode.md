---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 413125f6bcc9935ffae66551ba5bd178eb4a3c53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716444"
---
# <span data-ttu-id="48597-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="48597-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="48597-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48597-102">SYNOPSIS</span></span>
<span data-ttu-id="48597-103">Usuwanie węzła o podanej nazwie w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="48597-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48597-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48597-104">SYNTAX</span></span>

### <span data-ttu-id="48597-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="48597-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48597-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="48597-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48597-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="48597-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48597-108">Opis</span><span class="sxs-lookup"><span data-stu-id="48597-108">DESCRIPTION</span></span>
<span data-ttu-id="48597-109">Polecenie cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntimeNode powoduje usunięcie węzła w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="48597-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="48597-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48597-110">EXAMPLES</span></span>

### <span data-ttu-id="48597-111">Przykład 1: Usuwanie węzła z środowiska wykonawczego integracji</span><span class="sxs-lookup"><span data-stu-id="48597-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="48597-112">To polecenie usuwa węzeł o nazwie "Node_1" w środowisku wykonawczym integracji o nazwie "test-SelfHost-IR" w subskrypcji grupy zasobów o nazwie "RG-test-dfv2" i fabryki danych o nazwie "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="48597-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="48597-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48597-113">PARAMETERS</span></span>

### <span data-ttu-id="48597-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="48597-114">-DataFactoryName</span></span>
<span data-ttu-id="48597-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="48597-115">The data factory name.</span></span>

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

### <span data-ttu-id="48597-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48597-116">-DefaultProfile</span></span>
<span data-ttu-id="48597-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="48597-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48597-118">-Force</span><span class="sxs-lookup"><span data-stu-id="48597-118">-Force</span></span>
<span data-ttu-id="48597-119">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="48597-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="48597-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="48597-120">-InputObject</span></span>
<span data-ttu-id="48597-121">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="48597-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="48597-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="48597-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="48597-123">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="48597-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="48597-124">-Nodename</span><span class="sxs-lookup"><span data-stu-id="48597-124">-NodeName</span></span>
<span data-ttu-id="48597-125">Nazwa węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="48597-125">The integration runtime node name.</span></span>

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

### <span data-ttu-id="48597-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48597-126">-ResourceGroupName</span></span>
<span data-ttu-id="48597-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="48597-127">The resource group name.</span></span>

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

### <span data-ttu-id="48597-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48597-128">-ResourceId</span></span>
<span data-ttu-id="48597-129">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="48597-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="48597-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48597-130">-Confirm</span></span>
<span data-ttu-id="48597-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48597-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48597-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48597-132">-WhatIf</span></span>
<span data-ttu-id="48597-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48597-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="48597-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48597-134">CommonParameters</span></span>
<span data-ttu-id="48597-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48597-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48597-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48597-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48597-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48597-137">INPUTS</span></span>

### <span data-ttu-id="48597-138">System. String</span><span class="sxs-lookup"><span data-stu-id="48597-138">System.String</span></span>

### <span data-ttu-id="48597-139">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="48597-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="48597-140">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="48597-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="48597-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48597-141">OUTPUTS</span></span>

### <span data-ttu-id="48597-142">System. void</span><span class="sxs-lookup"><span data-stu-id="48597-142">System.Void</span></span>

## <span data-ttu-id="48597-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48597-143">NOTES</span></span>

## <span data-ttu-id="48597-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48597-144">RELATED LINKS</span></span>
