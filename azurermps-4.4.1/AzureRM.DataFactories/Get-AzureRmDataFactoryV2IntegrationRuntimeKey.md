---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 7bab6fb42e5d50cc0ede06a42540cf628a5ee4a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552396"
---
# <span data-ttu-id="777d2-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="777d2-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="777d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="777d2-102">SYNOPSIS</span></span>
<span data-ttu-id="777d2-103">Pobiera klucze dla środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="777d2-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="777d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="777d2-104">SYNTAX</span></span>

### <span data-ttu-id="777d2-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="777d2-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="777d2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="777d2-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="777d2-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="777d2-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="777d2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="777d2-108">DESCRIPTION</span></span>
<span data-ttu-id="777d2-109">Uzyskaj klucze dla środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="777d2-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="777d2-110">Klucze są używane do rejestrowania węzła środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="777d2-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="777d2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="777d2-111">EXAMPLES</span></span>

### <span data-ttu-id="777d2-112">Przykład 1: Uzyskaj klucze czasu wykonywania integracji</span><span class="sxs-lookup"><span data-stu-id="777d2-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="777d2-113">Polecenie cmdlet pobiera klucze środowiska wykonawczego integracji o nazwie test-SelfHost-IR '.</span><span class="sxs-lookup"><span data-stu-id="777d2-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="777d2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="777d2-114">PARAMETERS</span></span>

### <span data-ttu-id="777d2-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="777d2-115">-DataFactoryName</span></span>
<span data-ttu-id="777d2-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="777d2-116">The data factory name.</span></span>

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

### <span data-ttu-id="777d2-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="777d2-117">-InputObject</span></span>
<span data-ttu-id="777d2-118">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="777d2-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="777d2-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="777d2-119">-Name</span></span>
<span data-ttu-id="777d2-120">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="777d2-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="777d2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="777d2-121">-ResourceGroupName</span></span>
<span data-ttu-id="777d2-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="777d2-122">The resource group name.</span></span>

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

### <span data-ttu-id="777d2-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="777d2-123">-ResourceId</span></span>
<span data-ttu-id="777d2-124">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="777d2-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="777d2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="777d2-125">-DefaultProfile</span></span>
<span data-ttu-id="777d2-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="777d2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="777d2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="777d2-127">CommonParameters</span></span>
<span data-ttu-id="777d2-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="777d2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="777d2-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="777d2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="777d2-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="777d2-130">INPUTS</span></span>

### <span data-ttu-id="777d2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="777d2-131">System.String</span></span>
<span data-ttu-id="777d2-132">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="777d2-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 

## <span data-ttu-id="777d2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="777d2-133">OUTPUTS</span></span>

### <span data-ttu-id="777d2-134">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="777d2-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="777d2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="777d2-135">NOTES</span></span>

## <span data-ttu-id="777d2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="777d2-136">RELATED LINKS</span></span>

[<span data-ttu-id="777d2-137">Nowe — AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="777d2-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
