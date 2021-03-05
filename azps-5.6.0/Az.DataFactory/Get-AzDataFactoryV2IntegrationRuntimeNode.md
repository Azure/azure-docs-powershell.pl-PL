---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: a3b3c25ce424085597de7396be469356f3d3f1c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975169"
---
# <span data-ttu-id="375cb-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="375cb-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="375cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="375cb-102">SYNOPSIS</span></span>
<span data-ttu-id="375cb-103">Pobiera informacje o węźle środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="375cb-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="375cb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="375cb-104">SYNTAX</span></span>

### <span data-ttu-id="375cb-105">ByIntegrationRuntimeName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="375cb-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="375cb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="375cb-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="375cb-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="375cb-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="375cb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="375cb-108">DESCRIPTION</span></span>
<span data-ttu-id="375cb-109">Polecenie **cmdlet Get-AzDataFactoryV2IntegrationRuntimeNode** pobiera szczegółowe informacje węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="375cb-109">The **Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="375cb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="375cb-110">EXAMPLES</span></span>

### <span data-ttu-id="375cb-111">Przykład 1. Pobiera szczegółowe informacje o węźle środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="375cb-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              :
```

<span data-ttu-id="375cb-112">Polecenie cmdlet pobiera informacje o węźle o nazwie "Node_1" w środowisku integracji samoobsługowej "test-selfhost-ir" w data factory "test-df-eu2".</span><span class="sxs-lookup"><span data-stu-id="375cb-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="375cb-113">Przykład 2. Pobiera szczegółowe informacje węzła środowiska uruchomieniowego integracji z adresem IP.</span><span class="sxs-lookup"><span data-stu-id="375cb-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              : 167.220.1.167
```

<span data-ttu-id="375cb-114">Polecenie cmdlet pobiera informacje o węźle o nazwie "Node_1" w środowisku integracji samoobsługowej "test-selfhost-ir" w środowisku danych factory "test-df-eu2", łącznie z adresem IP.</span><span class="sxs-lookup"><span data-stu-id="375cb-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="375cb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="375cb-115">PARAMETERS</span></span>

### <span data-ttu-id="375cb-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="375cb-116">-DataFactoryName</span></span>
<span data-ttu-id="375cb-117">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="375cb-117">The data factory name.</span></span>

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

### <span data-ttu-id="375cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="375cb-118">-DefaultProfile</span></span>
<span data-ttu-id="375cb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="375cb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="375cb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="375cb-120">-InputObject</span></span>
<span data-ttu-id="375cb-121">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="375cb-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="375cb-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="375cb-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="375cb-123">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="375cb-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="375cb-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="375cb-124">-IpAddress</span></span>
<span data-ttu-id="375cb-125">Adres IP węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="375cb-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="375cb-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="375cb-126">-Name</span></span>
<span data-ttu-id="375cb-127">Nazwa węzła integracji środowiska uruchomieniowego.</span><span class="sxs-lookup"><span data-stu-id="375cb-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="375cb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="375cb-128">-ResourceGroupName</span></span>
<span data-ttu-id="375cb-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="375cb-129">The resource group name.</span></span>

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

### <span data-ttu-id="375cb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="375cb-130">-ResourceId</span></span>
<span data-ttu-id="375cb-131">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="375cb-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="375cb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="375cb-132">CommonParameters</span></span>
<span data-ttu-id="375cb-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="375cb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="375cb-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="375cb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="375cb-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="375cb-135">INPUTS</span></span>

### <span data-ttu-id="375cb-136">System.String</span><span class="sxs-lookup"><span data-stu-id="375cb-136">System.String</span></span>

### <span data-ttu-id="375cb-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="375cb-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="375cb-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="375cb-138">OUTPUTS</span></span>

### <span data-ttu-id="375cb-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="375cb-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="375cb-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="375cb-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="375cb-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="375cb-141">NOTES</span></span>
<span data-ttu-id="375cb-142">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="375cb-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="375cb-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="375cb-143">RELATED LINKS</span></span>

[<span data-ttu-id="375cb-144">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="375cb-144">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()
