---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: eda4cb403381bd41f7be471b91b2cbba3a6d2ad3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239987"
---
# <span data-ttu-id="ac913-101">Set-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ac913-101">Set-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="ac913-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac913-102">SYNOPSIS</span></span>
<span data-ttu-id="ac913-103">Zaktualizuj prywatne połączenie punktu końcowego do usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="ac913-103">Update the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="ac913-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ac913-104">SYNTAX</span></span>

### <span data-ttu-id="ac913-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ac913-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac913-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac913-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac913-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac913-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceId] <String> -Status <PSPrivateLinkServiceConnectionStatus>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac913-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac913-108">InputObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 -InputObject <PSPrivateEndpointConnection> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac913-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="ac913-109">DESCRIPTION</span></span>
<span data-ttu-id="ac913-110">**Set-AzSearchPrivateEndpointConnection** aktualizuje prywatne połączenie punktu końcowego z usługą Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="ac913-110">The **Set-AzSearchPrivateEndpointConnection** updates the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="ac913-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ac913-111">EXAMPLES</span></span>

### <span data-ttu-id="ac913-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ac913-112">Example 1</span></span>
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

<span data-ttu-id="ac913-113">W tym przykładzie jest aktualizowany stan prywatnego połączenia punktu końcowego usługi Azure Cognitive Search na "Odrzucone".</span><span class="sxs-lookup"><span data-stu-id="ac913-113">This example updates a private endpoint connection's status of the Azure Cognitive Search service to be "Rejected".</span></span>

## <span data-ttu-id="ac913-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac913-114">PARAMETERS</span></span>

### <span data-ttu-id="ac913-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac913-115">-DefaultProfile</span></span>
<span data-ttu-id="ac913-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac913-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac913-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="ac913-117">-Description</span></span>
<span data-ttu-id="ac913-118">Opis prywatnego połączenia punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="ac913-118">Private endpoint connection description</span></span>

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

### <span data-ttu-id="ac913-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac913-119">-InputObject</span></span>
<span data-ttu-id="ac913-120">Obiekt wejściowy połączenia prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="ac913-120">Private endpoint connection input object</span></span>

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

### <span data-ttu-id="ac913-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ac913-121">-Name</span></span>
<span data-ttu-id="ac913-122">Nazwa prywatnego połączenia punktu końcowego usługi Azure Cognitive Search Service</span><span class="sxs-lookup"><span data-stu-id="ac913-122">Azure Cognitive Search Service private endpoint connection name</span></span>

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

### <span data-ttu-id="ac913-123">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="ac913-123">-ParentObject</span></span>
<span data-ttu-id="ac913-124">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="ac913-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="ac913-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac913-125">-ResourceGroupName</span></span>
<span data-ttu-id="ac913-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ac913-126">Resource Group name.</span></span>

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

### <span data-ttu-id="ac913-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac913-127">-ResourceId</span></span>
<span data-ttu-id="ac913-128">Identyfikator zasobu usługi private link</span><span class="sxs-lookup"><span data-stu-id="ac913-128">Private link service resource id</span></span>

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

### <span data-ttu-id="ac913-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ac913-129">-ServiceName</span></span>
<span data-ttu-id="ac913-130">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="ac913-130">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="ac913-131">— Status</span><span class="sxs-lookup"><span data-stu-id="ac913-131">-Status</span></span>
<span data-ttu-id="ac913-132">Stan połączenia z usługą private link</span><span class="sxs-lookup"><span data-stu-id="ac913-132">Private link service connection status</span></span>

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

### <span data-ttu-id="ac913-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ac913-133">-Confirm</span></span>
<span data-ttu-id="ac913-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ac913-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac913-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac913-135">-WhatIf</span></span>
<span data-ttu-id="ac913-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac913-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac913-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ac913-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac913-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac913-138">CommonParameters</span></span>
<span data-ttu-id="ac913-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac913-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac913-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac913-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac913-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac913-141">INPUTS</span></span>

### <span data-ttu-id="ac913-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ac913-142">System.String</span></span>

## <span data-ttu-id="ac913-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ac913-143">OUTPUTS</span></span>

### <span data-ttu-id="ac913-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ac913-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="ac913-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ac913-145">NOTES</span></span>

## <span data-ttu-id="ac913-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac913-146">RELATED LINKS</span></span>

[<span data-ttu-id="ac913-147">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="ac913-147">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="ac913-148">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="ac913-148">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)
