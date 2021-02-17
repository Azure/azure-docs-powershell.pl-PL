---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 951f1b6a03c621e0dd8bc5d559eaf317cfd43a2c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198875"
---
# <span data-ttu-id="1ae26-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1ae26-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="1ae26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ae26-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae26-103">Uzyskiwanie wszystkich aktywnych sesji debugowania przepływu danych za pomocą usługi Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="1ae26-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="1ae26-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1ae26-104">SYNTAX</span></span>

### <span data-ttu-id="1ae26-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="1ae26-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ae26-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ae26-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ae26-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1ae26-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ae26-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1ae26-108">DESCRIPTION</span></span>
<span data-ttu-id="1ae26-109">Lista wszystkich aktywnych sesji debugowania przepływu danych przez usługę Azure Data Factory ze szczegółami.</span><span class="sxs-lookup"><span data-stu-id="1ae26-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="1ae26-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1ae26-110">EXAMPLES</span></span>

### <span data-ttu-id="1ae26-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1ae26-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="1ae26-112">Uzyskaj wszystkie aktywne sesje debugowania przepływu danych w usłudze Azure Data Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="1ae26-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="1ae26-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ae26-113">PARAMETERS</span></span>

### <span data-ttu-id="1ae26-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ae26-114">-DataFactory</span></span>
<span data-ttu-id="1ae26-115">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="1ae26-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae26-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1ae26-116">-DataFactoryName</span></span>
<span data-ttu-id="1ae26-117">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="1ae26-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae26-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae26-118">-DefaultProfile</span></span>
<span data-ttu-id="1ae26-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ae26-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ae26-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae26-120">-ResourceGroupName</span></span>
<span data-ttu-id="1ae26-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ae26-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae26-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ae26-122">-ResourceId</span></span>
<span data-ttu-id="1ae26-123">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="1ae26-123">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae26-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae26-124">CommonParameters</span></span>
<span data-ttu-id="1ae26-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae26-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae26-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ae26-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae26-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ae26-127">INPUTS</span></span>

### <span data-ttu-id="1ae26-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1ae26-128">System.String</span></span>

### <span data-ttu-id="1ae26-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1ae26-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1ae26-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ae26-130">OUTPUTS</span></span>

### <span data-ttu-id="1ae26-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span><span class="sxs-lookup"><span data-stu-id="1ae26-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="1ae26-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1ae26-132">NOTES</span></span>
<span data-ttu-id="1ae26-133">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="1ae26-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1ae26-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ae26-134">RELATED LINKS</span></span>

[<span data-ttu-id="1ae26-135">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1ae26-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="1ae26-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="1ae26-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="1ae26-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="1ae26-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="1ae26-138">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1ae26-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)