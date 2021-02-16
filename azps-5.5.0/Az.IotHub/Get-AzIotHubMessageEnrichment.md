---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 91694efaeaf1a24018269706f3ee388feb7218ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185690"
---
# <span data-ttu-id="ad2ba-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ad2ba-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="ad2ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad2ba-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2ba-103">Zawiera listę wszystkich wzbogacenia wiadomości lub wzbogacania określonej wiadomości w Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="ad2ba-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="ad2ba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ad2ba-104">SYNTAX</span></span>

### <span data-ttu-id="ad2ba-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="ad2ba-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad2ba-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ad2ba-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad2ba-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ad2ba-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad2ba-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ad2ba-108">DESCRIPTION</span></span>
<span data-ttu-id="ad2ba-109">Aby uzyskać szczegółowe objaśnienie wzbogacania wiadomości w centrum Azure IoT Hub, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="ad2ba-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="ad2ba-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ad2ba-110">EXAMPLES</span></span>

### <span data-ttu-id="ad2ba-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad2ba-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="ad2ba-112">Wzbogacenie wszystkich wiadomości w aplikacji MyIotHub</span><span class="sxs-lookup"><span data-stu-id="ad2ba-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="ad2ba-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ad2ba-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="ad2ba-114">Pokaż szczegóły wzbogacania wiadomości "newKey".</span><span class="sxs-lookup"><span data-stu-id="ad2ba-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="ad2ba-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad2ba-115">PARAMETERS</span></span>

### <span data-ttu-id="ad2ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad2ba-116">-DefaultProfile</span></span>
<span data-ttu-id="ad2ba-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad2ba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad2ba-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad2ba-118">-InputObject</span></span>
<span data-ttu-id="ad2ba-119">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="ad2ba-119">IotHub object</span></span>

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

### <span data-ttu-id="ad2ba-120">- Key</span><span class="sxs-lookup"><span data-stu-id="ad2ba-120">-Key</span></span>
<span data-ttu-id="ad2ba-121">Klucz wzbogacenia.</span><span class="sxs-lookup"><span data-stu-id="ad2ba-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="ad2ba-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ad2ba-122">-Name</span></span>
<span data-ttu-id="ad2ba-123">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="ad2ba-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ad2ba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad2ba-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad2ba-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ad2ba-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ad2ba-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad2ba-126">-ResourceId</span></span>
<span data-ttu-id="ad2ba-127">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="ad2ba-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ad2ba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2ba-128">CommonParameters</span></span>
<span data-ttu-id="ad2ba-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad2ba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad2ba-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad2ba-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2ba-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad2ba-131">INPUTS</span></span>

### <span data-ttu-id="ad2ba-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ad2ba-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ad2ba-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ad2ba-133">System.String</span></span>

## <span data-ttu-id="ad2ba-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad2ba-134">OUTPUTS</span></span>

### <span data-ttu-id="ad2ba-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="ad2ba-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="ad2ba-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span><span class="sxs-lookup"><span data-stu-id="ad2ba-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="ad2ba-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ad2ba-137">NOTES</span></span>

## <span data-ttu-id="ad2ba-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad2ba-138">RELATED LINKS</span></span>
