---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 1521f0f4f3b90010e24185a036dca047860e27c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706029"
---
# <span data-ttu-id="99d6f-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="99d6f-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="99d6f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="99d6f-103">Uzyskiwanie wszystkich aktywnych sesji debugowania przepływu danych za pomocą usługi Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="99d6f-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="99d6f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99d6f-104">SYNTAX</span></span>

### <span data-ttu-id="99d6f-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="99d6f-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99d6f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="99d6f-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99d6f-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="99d6f-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99d6f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="99d6f-108">DESCRIPTION</span></span>
<span data-ttu-id="99d6f-109">Wyświetlanie wszystkich aktywnych sesji debugowania przepływu danych przez usługę Azure Data Factory ze szczegółami.</span><span class="sxs-lookup"><span data-stu-id="99d6f-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="99d6f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99d6f-110">EXAMPLES</span></span>

### <span data-ttu-id="99d6f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99d6f-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="99d6f-112">Pobierz wszystkie aktywne sesje debugowania przepływu danych w fabryce danych platformy Azure "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="99d6f-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="99d6f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99d6f-113">PARAMETERS</span></span>

### <span data-ttu-id="99d6f-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="99d6f-114">-DataFactory</span></span>
<span data-ttu-id="99d6f-115">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="99d6f-115">The data factory object.</span></span>

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

### <span data-ttu-id="99d6f-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="99d6f-116">-DataFactoryName</span></span>
<span data-ttu-id="99d6f-117">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="99d6f-117">The data factory name.</span></span>

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

### <span data-ttu-id="99d6f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d6f-118">-DefaultProfile</span></span>
<span data-ttu-id="99d6f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="99d6f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99d6f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99d6f-120">-ResourceGroupName</span></span>
<span data-ttu-id="99d6f-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="99d6f-121">The resource group name.</span></span>

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

### <span data-ttu-id="99d6f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99d6f-122">-ResourceId</span></span>
<span data-ttu-id="99d6f-123">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="99d6f-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="99d6f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d6f-124">CommonParameters</span></span>
<span data-ttu-id="99d6f-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d6f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d6f-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99d6f-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d6f-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99d6f-127">INPUTS</span></span>

### <span data-ttu-id="99d6f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="99d6f-128">System.String</span></span>

### <span data-ttu-id="99d6f-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="99d6f-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="99d6f-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99d6f-130">OUTPUTS</span></span>

### <span data-ttu-id="99d6f-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span><span class="sxs-lookup"><span data-stu-id="99d6f-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="99d6f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99d6f-132">NOTES</span></span>
<span data-ttu-id="99d6f-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="99d6f-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="99d6f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99d6f-134">RELATED LINKS</span></span>

[<span data-ttu-id="99d6f-135">Start — AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="99d6f-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="99d6f-136">Dodaj-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="99d6f-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="99d6f-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="99d6f-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="99d6f-138">Zatrzymaj — AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="99d6f-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)