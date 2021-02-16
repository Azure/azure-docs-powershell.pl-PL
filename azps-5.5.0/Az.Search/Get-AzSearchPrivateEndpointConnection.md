---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 3500cf71bb09bec4b204acc0bbf56f185f6ff647
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242434"
---
# <span data-ttu-id="33f11-101">Get-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="33f11-101">Get-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="33f11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33f11-102">SYNOPSIS</span></span>
<span data-ttu-id="33f11-103">Pobiera prywatne połączenia punktów końcowych z usługą Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="33f11-103">Gets private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="33f11-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="33f11-104">SYNTAX</span></span>

### <span data-ttu-id="33f11-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="33f11-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33f11-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33f11-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33f11-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33f11-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33f11-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="33f11-108">DESCRIPTION</span></span>
<span data-ttu-id="33f11-109">Polecenie **cmdlet Get-AzSearchPrivateEndpointConnection** pobiera prywatne połączenia punktów końcowych do usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="33f11-109">The **Get-AzSearchPrivateEndpointConnection** cmdlet gets the private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="33f11-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="33f11-110">EXAMPLES</span></span>

### <span data-ttu-id="33f11-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="33f11-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Name                                                          Id
----                                                          --
arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="33f11-112">W tym przykładzie wszystkie prywatne połączenia punktu końcowego z usługą Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="33f11-112">The example gets all the private endpoint connections to the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="33f11-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="33f11-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266  | ConvertTo-Json

{
  "Name": "arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "PrivateEndpoint": {
    "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann2/providers/Microsoft.Network/privateEndpoints/arjagann-test-cuseuap-pe"
  },
  "PrivateLinkServiceConnectionState": {
    "Status": 1,
    "Description": "Auto-approved",
    "ActionsRequired": "None"
  }
}
```

<span data-ttu-id="33f11-114">Przykład uzyskuje określone prywatne połączenie punktu końcowego według nazwy (przekonwertowane na JSON w celu ułatwienia czytania) do usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="33f11-114">The example gets a specific private endpoint connection by name (converted to JSON for ease of reading) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="33f11-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33f11-115">PARAMETERS</span></span>

### <span data-ttu-id="33f11-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33f11-116">-DefaultProfile</span></span>
<span data-ttu-id="33f11-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="33f11-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33f11-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="33f11-118">-Name</span></span>
<span data-ttu-id="33f11-119">Nazwa prywatnego połączenia punktu końcowego usługi Azure Cognitive Search Service</span><span class="sxs-lookup"><span data-stu-id="33f11-119">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f11-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="33f11-120">-ParentObject</span></span>
<span data-ttu-id="33f11-121">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="33f11-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33f11-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33f11-122">-ResourceGroupName</span></span>
<span data-ttu-id="33f11-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="33f11-123">Resource Group name.</span></span>

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

### <span data-ttu-id="33f11-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33f11-124">-ResourceId</span></span>
<span data-ttu-id="33f11-125">Identyfikator zasobu usługi private link</span><span class="sxs-lookup"><span data-stu-id="33f11-125">Private link service resource id</span></span>

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

### <span data-ttu-id="33f11-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="33f11-126">-ServiceName</span></span>
<span data-ttu-id="33f11-127">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="33f11-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="33f11-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="33f11-128">-Confirm</span></span>
<span data-ttu-id="33f11-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="33f11-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33f11-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33f11-130">-WhatIf</span></span>
<span data-ttu-id="33f11-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33f11-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33f11-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="33f11-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33f11-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33f11-133">CommonParameters</span></span>
<span data-ttu-id="33f11-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33f11-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33f11-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33f11-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33f11-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33f11-136">INPUTS</span></span>

### <span data-ttu-id="33f11-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="33f11-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="33f11-138">System.String</span><span class="sxs-lookup"><span data-stu-id="33f11-138">System.String</span></span>

## <span data-ttu-id="33f11-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33f11-139">OUTPUTS</span></span>

### <span data-ttu-id="33f11-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="33f11-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="33f11-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="33f11-141">NOTES</span></span>

## <span data-ttu-id="33f11-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33f11-142">RELATED LINKS</span></span>

[<span data-ttu-id="33f11-143">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="33f11-143">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="33f11-144">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="33f11-144">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)
