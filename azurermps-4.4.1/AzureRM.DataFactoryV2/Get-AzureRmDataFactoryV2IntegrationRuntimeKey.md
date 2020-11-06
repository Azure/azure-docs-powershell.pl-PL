---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 42ccd34e299439d3288a8a587ce9d62abe198847
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553943"
---
# <span data-ttu-id="284be-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="284be-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="284be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="284be-102">SYNOPSIS</span></span>
<span data-ttu-id="284be-103">Pobiera klucze dla środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="284be-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="284be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="284be-104">SYNTAX</span></span>

### <span data-ttu-id="284be-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="284be-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="284be-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="284be-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String>
```

### <span data-ttu-id="284be-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="284be-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="284be-108">Opis</span><span class="sxs-lookup"><span data-stu-id="284be-108">DESCRIPTION</span></span>
<span data-ttu-id="284be-109">Uzyskaj klucze dla środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="284be-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="284be-110">Klucze są używane do rejestrowania węzła środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="284be-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="284be-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="284be-111">EXAMPLES</span></span>

### <span data-ttu-id="284be-112">Przykład 1: Uzyskaj klucze czasu wykonywania integracji</span><span class="sxs-lookup"><span data-stu-id="284be-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="284be-113">Polecenie cmdlet pobiera klucze środowiska wykonawczego integracji o nazwie test-SelfHost-IR '.</span><span class="sxs-lookup"><span data-stu-id="284be-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="284be-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="284be-114">PARAMETERS</span></span>

### <span data-ttu-id="284be-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="284be-115">-DataFactoryName</span></span>
<span data-ttu-id="284be-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="284be-116">The data factory name.</span></span>

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

### <span data-ttu-id="284be-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="284be-117">-InputObject</span></span>
<span data-ttu-id="284be-118">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="284be-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="284be-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="284be-119">-Name</span></span>
<span data-ttu-id="284be-120">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="284be-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="284be-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="284be-121">-ResourceGroupName</span></span>
<span data-ttu-id="284be-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="284be-122">The resource group name.</span></span>

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

### <span data-ttu-id="284be-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="284be-123">-ResourceId</span></span>
<span data-ttu-id="284be-124">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="284be-124">The Azure resource ID.</span></span>

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

## <span data-ttu-id="284be-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="284be-125">INPUTS</span></span>

### <span data-ttu-id="284be-126">System. String</span><span class="sxs-lookup"><span data-stu-id="284be-126">System.String</span></span>
<span data-ttu-id="284be-127">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="284be-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 


## <span data-ttu-id="284be-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="284be-128">OUTPUTS</span></span>

### <span data-ttu-id="284be-129">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="284be-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>


## <span data-ttu-id="284be-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="284be-130">NOTES</span></span>

## <span data-ttu-id="284be-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="284be-131">RELATED LINKS</span></span>
[<span data-ttu-id="284be-132">Nowe — AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="284be-132">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
