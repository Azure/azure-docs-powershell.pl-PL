---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: eb248e1059da6dcab581e4fba8b3eac7f970bb30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546779"
---
# <span data-ttu-id="e35d0-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="e35d0-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="e35d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e35d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e35d0-103">Pobiera klucze dla środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="e35d0-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e35d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e35d0-104">SYNTAX</span></span>

### <span data-ttu-id="e35d0-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e35d0-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e35d0-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e35d0-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e35d0-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e35d0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e35d0-108">DESCRIPTION</span></span>
<span data-ttu-id="e35d0-109">Uzyskaj klucze dla środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="e35d0-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="e35d0-110">Klucze są używane do rejestrowania węzła środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="e35d0-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="e35d0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e35d0-111">EXAMPLES</span></span>

### <span data-ttu-id="e35d0-112">Przykład 1: Uzyskaj klucze czasu wykonywania integracji</span><span class="sxs-lookup"><span data-stu-id="e35d0-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="e35d0-113">Polecenie cmdlet pobiera klucze środowiska wykonawczego integracji o nazwie test-SelfHost-IR '.</span><span class="sxs-lookup"><span data-stu-id="e35d0-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="e35d0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e35d0-114">PARAMETERS</span></span>

### <span data-ttu-id="e35d0-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e35d0-115">-DataFactoryName</span></span>
<span data-ttu-id="e35d0-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e35d0-116">The data factory name.</span></span>

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

### <span data-ttu-id="e35d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35d0-117">-DefaultProfile</span></span>
<span data-ttu-id="e35d0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e35d0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e35d0-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e35d0-119">-InputObject</span></span>
<span data-ttu-id="e35d0-120">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="e35d0-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="e35d0-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e35d0-121">-Name</span></span>
<span data-ttu-id="e35d0-122">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="e35d0-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="e35d0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e35d0-123">-ResourceGroupName</span></span>
<span data-ttu-id="e35d0-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e35d0-124">The resource group name.</span></span>

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

### <span data-ttu-id="e35d0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e35d0-125">-ResourceId</span></span>
<span data-ttu-id="e35d0-126">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e35d0-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e35d0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35d0-127">CommonParameters</span></span>
<span data-ttu-id="e35d0-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e35d0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35d0-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e35d0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35d0-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e35d0-130">INPUTS</span></span>

### <span data-ttu-id="e35d0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e35d0-131">System.String</span></span>
<span data-ttu-id="e35d0-132">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e35d0-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 

## <span data-ttu-id="e35d0-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e35d0-133">OUTPUTS</span></span>

### <span data-ttu-id="e35d0-134">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="e35d0-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="e35d0-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e35d0-135">NOTES</span></span>

## <span data-ttu-id="e35d0-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e35d0-136">RELATED LINKS</span></span>

[<span data-ttu-id="e35d0-137">Nowe — AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="e35d0-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
