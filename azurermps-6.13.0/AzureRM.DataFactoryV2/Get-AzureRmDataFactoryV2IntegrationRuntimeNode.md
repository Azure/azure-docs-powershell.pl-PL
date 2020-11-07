---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: e8f631b485c62dba2e3871d5c2deec69881097af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717441"
---
# <span data-ttu-id="8012e-101">Get-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="8012e-101">Get-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="8012e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8012e-102">SYNOPSIS</span></span>
<span data-ttu-id="8012e-103">Pobiera informacje o węźle środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="8012e-103">Gets an integration runtime node infomation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8012e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8012e-104">SYNTAX</span></span>

### <span data-ttu-id="8012e-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8012e-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8012e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8012e-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8012e-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="8012e-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8012e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8012e-108">DESCRIPTION</span></span>
<span data-ttu-id="8012e-109">Polecenie cmdlet **Get-AzureRmDataFactoryV2IntegrationRuntimeNode umożliwia wyświetlenie** szczegółowych informacji dotyczących węzła środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="8012e-109">The **Get-AzureRmDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="8012e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8012e-110">EXAMPLES</span></span>

### <span data-ttu-id="8012e-111">Przykład 1. pobiera szczegółowe informacje dotyczące węzła środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="8012e-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'

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

<span data-ttu-id="8012e-112">Polecenie cmdlet pobiera informacje o węźle o nazwie "Node_1" w narzędziu do obsługi współhostowanej integracji "test-SelfHost-IR" w fabryce danych "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="8012e-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="8012e-113">Przykład 2: Pobiera szczegółowe informacje dotyczące węzła środowiska wykonawczego integracji wraz z adresem IP.</span><span class="sxs-lookup"><span data-stu-id="8012e-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress

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

<span data-ttu-id="8012e-114">Polecenie cmdlet pobiera informacje o węźle o nazwie "Node_1" w ramach programu "test-SelfHost-IR" w fabryce danych "test-DF-EU2", łącznie z adresem IP.</span><span class="sxs-lookup"><span data-stu-id="8012e-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="8012e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8012e-115">PARAMETERS</span></span>

### <span data-ttu-id="8012e-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8012e-116">-DataFactoryName</span></span>
<span data-ttu-id="8012e-117">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="8012e-117">The data factory name.</span></span>

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

### <span data-ttu-id="8012e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8012e-118">-DefaultProfile</span></span>
<span data-ttu-id="8012e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8012e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8012e-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8012e-120">-InputObject</span></span>
<span data-ttu-id="8012e-121">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="8012e-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="8012e-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="8012e-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="8012e-123">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="8012e-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="8012e-124">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="8012e-124">-IpAddress</span></span>
<span data-ttu-id="8012e-125">Adres IP węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="8012e-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="8012e-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8012e-126">-Name</span></span>
<span data-ttu-id="8012e-127">Nazwa węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="8012e-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="8012e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8012e-128">-ResourceGroupName</span></span>
<span data-ttu-id="8012e-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8012e-129">The resource group name.</span></span>

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

### <span data-ttu-id="8012e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8012e-130">-ResourceId</span></span>
<span data-ttu-id="8012e-131">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8012e-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8012e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8012e-132">CommonParameters</span></span>
<span data-ttu-id="8012e-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8012e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8012e-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8012e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8012e-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8012e-135">INPUTS</span></span>

### <span data-ttu-id="8012e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8012e-136">System.String</span></span>

### <span data-ttu-id="8012e-137">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8012e-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="8012e-138">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8012e-138">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="8012e-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8012e-139">OUTPUTS</span></span>

### <span data-ttu-id="8012e-140">Microsoft. Azure. Commands. DataFactoryV2. models. PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="8012e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="8012e-141">Microsoft. Azure. Commands. DataFactoryV2. models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="8012e-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="8012e-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8012e-142">NOTES</span></span>
<span data-ttu-id="8012e-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="8012e-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="8012e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8012e-144">RELATED LINKS</span></span>

[<span data-ttu-id="8012e-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8012e-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
