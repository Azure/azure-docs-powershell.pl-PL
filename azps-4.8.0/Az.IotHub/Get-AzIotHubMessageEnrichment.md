---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 91694efaeaf1a24018269706f3ee388feb7218ea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222326"
---
# <span data-ttu-id="e33ee-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e33ee-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="e33ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e33ee-102">SYNOPSIS</span></span>
<span data-ttu-id="e33ee-103">Wyświetla wszystkie wzbogacenia wiadomości lub inne wzbogacanie wiadomości dla Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="e33ee-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="e33ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e33ee-104">SYNTAX</span></span>

### <span data-ttu-id="e33ee-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e33ee-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e33ee-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e33ee-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e33ee-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e33ee-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e33ee-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e33ee-108">DESCRIPTION</span></span>
<span data-ttu-id="e33ee-109">Aby uzyskać szczegółowe wyjaśnienie dotyczące wzbogacenia wiadomości w centrum usługi Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="e33ee-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="e33ee-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e33ee-110">EXAMPLES</span></span>

### <span data-ttu-id="e33ee-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e33ee-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="e33ee-112">Lista wszystkich ulepszonych wiadomości w programie MyIotHub</span><span class="sxs-lookup"><span data-stu-id="e33ee-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="e33ee-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e33ee-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="e33ee-114">Pokaż szczegóły dotyczące wzbogacania wiadomości "newKey".</span><span class="sxs-lookup"><span data-stu-id="e33ee-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="e33ee-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e33ee-115">PARAMETERS</span></span>

### <span data-ttu-id="e33ee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e33ee-116">-DefaultProfile</span></span>
<span data-ttu-id="e33ee-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e33ee-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e33ee-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e33ee-118">-InputObject</span></span>
<span data-ttu-id="e33ee-119">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="e33ee-119">IotHub object</span></span>

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

### <span data-ttu-id="e33ee-120">-Key</span><span class="sxs-lookup"><span data-stu-id="e33ee-120">-Key</span></span>
<span data-ttu-id="e33ee-121">Klucz wzbogacenia.</span><span class="sxs-lookup"><span data-stu-id="e33ee-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="e33ee-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e33ee-122">-Name</span></span>
<span data-ttu-id="e33ee-123">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="e33ee-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e33ee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e33ee-124">-ResourceGroupName</span></span>
<span data-ttu-id="e33ee-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e33ee-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e33ee-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e33ee-126">-ResourceId</span></span>
<span data-ttu-id="e33ee-127">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="e33ee-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e33ee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e33ee-128">CommonParameters</span></span>
<span data-ttu-id="e33ee-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e33ee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e33ee-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e33ee-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e33ee-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e33ee-131">INPUTS</span></span>

### <span data-ttu-id="e33ee-132">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e33ee-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e33ee-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e33ee-133">System.String</span></span>

## <span data-ttu-id="e33ee-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e33ee-134">OUTPUTS</span></span>

### <span data-ttu-id="e33ee-135">Microsoft. Azure. Commands. Management. IotHub. models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="e33ee-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="e33ee-136">Microsoft. Azure. Commands. Management. IotHub. models. PSEnrichmentProperties []</span><span class="sxs-lookup"><span data-stu-id="e33ee-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="e33ee-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e33ee-137">NOTES</span></span>

## <span data-ttu-id="e33ee-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e33ee-138">RELATED LINKS</span></span>
