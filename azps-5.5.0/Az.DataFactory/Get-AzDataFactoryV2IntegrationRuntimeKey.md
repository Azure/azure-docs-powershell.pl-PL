---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 6cfda34b1718cfd73108362ee81fbe9c638310c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238300"
---
# <span data-ttu-id="92f97-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="92f97-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="92f97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92f97-102">SYNOPSIS</span></span>
<span data-ttu-id="92f97-103">Pobiera klucze środowiska integracji z własnym hostem.</span><span class="sxs-lookup"><span data-stu-id="92f97-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="92f97-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="92f97-104">SYNTAX</span></span>

### <span data-ttu-id="92f97-105">ByIntegrationRuntimeName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="92f97-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92f97-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="92f97-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92f97-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="92f97-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92f97-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="92f97-108">DESCRIPTION</span></span>
<span data-ttu-id="92f97-109">Uzyskaj klucze środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="92f97-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="92f97-110">Klucze służą do rejestrowania węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="92f97-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="92f97-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="92f97-111">EXAMPLES</span></span>

### <span data-ttu-id="92f97-112">Przykład 1. Uzyskiwanie kluczy środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="92f97-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="92f97-113">Polecenie cmdlet pobiera klucze środowiska uruchomieniowego integracji o nazwie "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="92f97-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="92f97-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92f97-114">PARAMETERS</span></span>

### <span data-ttu-id="92f97-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="92f97-115">-DataFactoryName</span></span>
<span data-ttu-id="92f97-116">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="92f97-116">The data factory name.</span></span>

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

### <span data-ttu-id="92f97-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f97-117">-DefaultProfile</span></span>
<span data-ttu-id="92f97-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="92f97-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92f97-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92f97-119">-InputObject</span></span>
<span data-ttu-id="92f97-120">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="92f97-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="92f97-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="92f97-121">-Name</span></span>
<span data-ttu-id="92f97-122">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="92f97-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="92f97-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f97-123">-ResourceGroupName</span></span>
<span data-ttu-id="92f97-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="92f97-124">The resource group name.</span></span>

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

### <span data-ttu-id="92f97-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92f97-125">-ResourceId</span></span>
<span data-ttu-id="92f97-126">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="92f97-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="92f97-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f97-127">CommonParameters</span></span>
<span data-ttu-id="92f97-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92f97-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f97-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92f97-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f97-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92f97-130">INPUTS</span></span>

### <span data-ttu-id="92f97-131">System.String</span><span class="sxs-lookup"><span data-stu-id="92f97-131">System.String</span></span>

### <span data-ttu-id="92f97-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="92f97-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="92f97-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92f97-133">OUTPUTS</span></span>

### <span data-ttu-id="92f97-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="92f97-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="92f97-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="92f97-135">NOTES</span></span>

## <span data-ttu-id="92f97-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92f97-136">RELATED LINKS</span></span>

[<span data-ttu-id="92f97-137">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="92f97-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
