---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/set-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: d67108e935d4f3ef14522f792a06f975d98be803
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972554"
---
# <span data-ttu-id="35f9d-101">Set-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35f9d-101">Set-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="35f9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="35f9d-103">Zaktualizuj prywatne połączenie punktu końcowego do usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="35f9d-103">Update the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="35f9d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="35f9d-104">SYNTAX</span></span>

### <span data-ttu-id="35f9d-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="35f9d-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35f9d-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35f9d-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35f9d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35f9d-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceId] <String> -Status <PSPrivateLinkServiceConnectionStatus>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35f9d-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35f9d-108">InputObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 -InputObject <PSPrivateEndpointConnection> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35f9d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="35f9d-109">DESCRIPTION</span></span>
<span data-ttu-id="35f9d-110">**Set-AzSearchPrivateEndpointConnection** aktualizuje prywatne połączenie punktu końcowego usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="35f9d-110">The **Set-AzSearchPrivateEndpointConnection** updates the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="35f9d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="35f9d-111">EXAMPLES</span></span>

### <span data-ttu-id="35f9d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="35f9d-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 -Status Rejected  -Description "Rejected" | ConvertTo-Json

{
  "Name": "arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "PrivateEndpoint": {
    "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann2/providers/Microsoft.Network/privateEndpoints/arjagann-test-cuseuap-pe"
  },
  "PrivateLinkServiceConnectionState": {
    "Status": 2,
    "Description": "Rejected",
    "ActionsRequired": "None"
  }
}
```

<span data-ttu-id="35f9d-113">W tym przykładzie jest aktualizowany stan prywatnego połączenia punktu końcowego usługi Azure Cognitive Search na "Odrzucone".</span><span class="sxs-lookup"><span data-stu-id="35f9d-113">This example updates a private endpoint connection's status of the Azure Cognitive Search service to be "Rejected".</span></span>

## <span data-ttu-id="35f9d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35f9d-114">PARAMETERS</span></span>

### <span data-ttu-id="35f9d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f9d-115">-DefaultProfile</span></span>
<span data-ttu-id="35f9d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="35f9d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35f9d-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="35f9d-117">-Description</span></span>
<span data-ttu-id="35f9d-118">Opis prywatnego połączenia punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="35f9d-118">Private endpoint connection description</span></span>

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

### <span data-ttu-id="35f9d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35f9d-119">-InputObject</span></span>
<span data-ttu-id="35f9d-120">Obiekt wejściowy połączenia prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="35f9d-120">Private endpoint connection input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35f9d-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="35f9d-121">-Name</span></span>
<span data-ttu-id="35f9d-122">Nazwa prywatnego połączenia punktu końcowego usługi Azure Cognitive Search Service</span><span class="sxs-lookup"><span data-stu-id="35f9d-122">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f9d-123">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="35f9d-123">-ParentObject</span></span>
<span data-ttu-id="35f9d-124">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="35f9d-124">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35f9d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35f9d-125">-ResourceGroupName</span></span>
<span data-ttu-id="35f9d-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="35f9d-126">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f9d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35f9d-127">-ResourceId</span></span>
<span data-ttu-id="35f9d-128">Identyfikator zasobu usługi private link</span><span class="sxs-lookup"><span data-stu-id="35f9d-128">Private link service resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f9d-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="35f9d-129">-ServiceName</span></span>
<span data-ttu-id="35f9d-130">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="35f9d-130">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f9d-131">— Status</span><span class="sxs-lookup"><span data-stu-id="35f9d-131">-Status</span></span>
<span data-ttu-id="35f9d-132">Stan połączenia z usługą private link</span><span class="sxs-lookup"><span data-stu-id="35f9d-132">Private link service connection status</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateLinkServiceConnectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Pending, Approved, Rejected, Disconnected

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f9d-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35f9d-133">-Confirm</span></span>
<span data-ttu-id="35f9d-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="35f9d-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f9d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35f9d-135">-WhatIf</span></span>
<span data-ttu-id="35f9d-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35f9d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35f9d-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="35f9d-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f9d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f9d-138">CommonParameters</span></span>
<span data-ttu-id="35f9d-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35f9d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f9d-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35f9d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f9d-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35f9d-141">INPUTS</span></span>

### <span data-ttu-id="35f9d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="35f9d-142">System.String</span></span>

## <span data-ttu-id="35f9d-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35f9d-143">OUTPUTS</span></span>

### <span data-ttu-id="35f9d-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35f9d-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="35f9d-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="35f9d-145">NOTES</span></span>

## <span data-ttu-id="35f9d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35f9d-146">RELATED LINKS</span></span>

[<span data-ttu-id="35f9d-147">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="35f9d-147">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="35f9d-148">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="35f9d-148">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)
