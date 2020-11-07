---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 2a1aaef2532e8c0a00a04a42d857e2be0e2a0451
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706022"
---
# <span data-ttu-id="48dae-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="48dae-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="48dae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48dae-102">SYNOPSIS</span></span>
<span data-ttu-id="48dae-103">Pobiera klucze dla środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="48dae-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="48dae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48dae-104">SYNTAX</span></span>

### <span data-ttu-id="48dae-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="48dae-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48dae-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="48dae-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48dae-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="48dae-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48dae-108">Opis</span><span class="sxs-lookup"><span data-stu-id="48dae-108">DESCRIPTION</span></span>
<span data-ttu-id="48dae-109">Uzyskaj klucze dla środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="48dae-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="48dae-110">Klucze są używane do rejestrowania węzła środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="48dae-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="48dae-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48dae-111">EXAMPLES</span></span>

### <span data-ttu-id="48dae-112">Przykład 1: Uzyskaj klucze czasu wykonywania integracji</span><span class="sxs-lookup"><span data-stu-id="48dae-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="48dae-113">Polecenie cmdlet pobiera klucze środowiska wykonawczego integracji o nazwie test-SelfHost-IR '.</span><span class="sxs-lookup"><span data-stu-id="48dae-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="48dae-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48dae-114">PARAMETERS</span></span>

### <span data-ttu-id="48dae-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="48dae-115">-DataFactoryName</span></span>
<span data-ttu-id="48dae-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="48dae-116">The data factory name.</span></span>

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

### <span data-ttu-id="48dae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48dae-117">-DefaultProfile</span></span>
<span data-ttu-id="48dae-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="48dae-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48dae-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="48dae-119">-InputObject</span></span>
<span data-ttu-id="48dae-120">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="48dae-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="48dae-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="48dae-121">-Name</span></span>
<span data-ttu-id="48dae-122">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="48dae-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="48dae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48dae-123">-ResourceGroupName</span></span>
<span data-ttu-id="48dae-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="48dae-124">The resource group name.</span></span>

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

### <span data-ttu-id="48dae-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48dae-125">-ResourceId</span></span>
<span data-ttu-id="48dae-126">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="48dae-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="48dae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48dae-127">CommonParameters</span></span>
<span data-ttu-id="48dae-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48dae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48dae-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48dae-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48dae-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48dae-130">INPUTS</span></span>

### <span data-ttu-id="48dae-131">System. String</span><span class="sxs-lookup"><span data-stu-id="48dae-131">System.String</span></span>

### <span data-ttu-id="48dae-132">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="48dae-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="48dae-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48dae-133">OUTPUTS</span></span>

### <span data-ttu-id="48dae-134">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="48dae-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="48dae-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48dae-135">NOTES</span></span>

## <span data-ttu-id="48dae-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48dae-136">RELATED LINKS</span></span>

[<span data-ttu-id="48dae-137">Nowe — AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="48dae-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
