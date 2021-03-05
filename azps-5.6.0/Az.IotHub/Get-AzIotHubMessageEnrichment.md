---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 18a6d5db9ecf7cf02604a883b49545650413ee28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987967"
---
# <span data-ttu-id="56abc-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="56abc-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="56abc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56abc-102">SYNOPSIS</span></span>
<span data-ttu-id="56abc-103">Zawiera listę wszystkich wzbogacenia wiadomości lub wzbogacania określonej wiadomości w Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="56abc-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="56abc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="56abc-104">SYNTAX</span></span>

### <span data-ttu-id="56abc-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="56abc-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56abc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="56abc-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56abc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="56abc-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56abc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="56abc-108">DESCRIPTION</span></span>
<span data-ttu-id="56abc-109">Aby uzyskać szczegółowe objaśnienie wzbogacania wiadomości w centrum Azure IoT Hub, zobacz https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="56abc-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="56abc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="56abc-110">EXAMPLES</span></span>

### <span data-ttu-id="56abc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="56abc-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="56abc-112">Wzbogacenie wszystkich wiadomości w aplikacji MyIotHub</span><span class="sxs-lookup"><span data-stu-id="56abc-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="56abc-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="56abc-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="56abc-114">Pokaż szczegóły wzbogacania wiadomości "newKey".</span><span class="sxs-lookup"><span data-stu-id="56abc-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="56abc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56abc-115">PARAMETERS</span></span>

### <span data-ttu-id="56abc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56abc-116">-DefaultProfile</span></span>
<span data-ttu-id="56abc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="56abc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56abc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56abc-118">-InputObject</span></span>
<span data-ttu-id="56abc-119">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="56abc-119">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56abc-120">- Key</span><span class="sxs-lookup"><span data-stu-id="56abc-120">-Key</span></span>
<span data-ttu-id="56abc-121">Klucz wzbogacenia.</span><span class="sxs-lookup"><span data-stu-id="56abc-121">The enrichment's key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56abc-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="56abc-122">-Name</span></span>
<span data-ttu-id="56abc-123">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="56abc-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56abc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56abc-124">-ResourceGroupName</span></span>
<span data-ttu-id="56abc-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="56abc-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56abc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56abc-126">-ResourceId</span></span>
<span data-ttu-id="56abc-127">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="56abc-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56abc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56abc-128">CommonParameters</span></span>
<span data-ttu-id="56abc-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56abc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56abc-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56abc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56abc-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56abc-131">INPUTS</span></span>

### <span data-ttu-id="56abc-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="56abc-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="56abc-133">System.String</span><span class="sxs-lookup"><span data-stu-id="56abc-133">System.String</span></span>

## <span data-ttu-id="56abc-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56abc-134">OUTPUTS</span></span>

### <span data-ttu-id="56abc-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="56abc-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="56abc-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span><span class="sxs-lookup"><span data-stu-id="56abc-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="56abc-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="56abc-137">NOTES</span></span>

## <span data-ttu-id="56abc-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56abc-138">RELATED LINKS</span></span>
