---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 341edce877666d56a78064f1e13dc7b7af9b26a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240011"
---
# <span data-ttu-id="37698-101">Remove-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37698-101">Remove-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="37698-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37698-102">SYNOPSIS</span></span>
<span data-ttu-id="37698-103">Usuń prywatne połączenie punktu końcowego z usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="37698-103">Remove the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="37698-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="37698-104">SYNTAX</span></span>

### <span data-ttu-id="37698-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="37698-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37698-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37698-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37698-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37698-107">InputObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -InputObject <PSPrivateEndpointConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37698-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37698-108">ResourceIdParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37698-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="37698-109">DESCRIPTION</span></span>
<span data-ttu-id="37698-110">Funkcja **Remove-AzSearchPrivateEndpointConnection** usuwa prywatne połączenie punktu końcowego z usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="37698-110">The **Remove-AzSearchPrivateEndpointConnection** removes the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="37698-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="37698-111">EXAMPLES</span></span>

### <span data-ttu-id="37698-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="37698-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="37698-113">W tym przykładzie jest usuwane prywatne połączenie punktu końcowego z usługi wyszukiwania według nazwy.</span><span class="sxs-lookup"><span data-stu-id="37698-113">This example removes a private endpoint connection from the search service by name.</span></span>

## <span data-ttu-id="37698-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37698-114">PARAMETERS</span></span>

### <span data-ttu-id="37698-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37698-115">-DefaultProfile</span></span>
<span data-ttu-id="37698-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="37698-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37698-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="37698-117">-Force</span></span>
<span data-ttu-id="37698-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="37698-118">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37698-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37698-119">-InputObject</span></span>
<span data-ttu-id="37698-120">Obiekt wejściowy połączenia prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="37698-120">Private endpoint connection input object</span></span>

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

### <span data-ttu-id="37698-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="37698-121">-Name</span></span>
<span data-ttu-id="37698-122">Nazwa prywatnego połączenia punktu końcowego usługi Azure Cognitive Search Service</span><span class="sxs-lookup"><span data-stu-id="37698-122">Azure Cognitive Search Service private endpoint connection name</span></span>

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

### <span data-ttu-id="37698-123">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="37698-123">-ParentObject</span></span>
<span data-ttu-id="37698-124">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="37698-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="37698-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37698-125">-PassThru</span></span>
<span data-ttu-id="37698-126">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="37698-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="37698-127">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="37698-127">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37698-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37698-128">-ResourceGroupName</span></span>
<span data-ttu-id="37698-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="37698-129">Resource Group name.</span></span>

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

### <span data-ttu-id="37698-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37698-130">-ResourceId</span></span>
<span data-ttu-id="37698-131">Identyfikator zasobu usługi private link</span><span class="sxs-lookup"><span data-stu-id="37698-131">Private link service resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37698-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="37698-132">-ServiceName</span></span>
<span data-ttu-id="37698-133">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="37698-133">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="37698-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37698-134">-Confirm</span></span>
<span data-ttu-id="37698-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="37698-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37698-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37698-136">-WhatIf</span></span>
<span data-ttu-id="37698-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37698-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37698-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="37698-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37698-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37698-139">CommonParameters</span></span>
<span data-ttu-id="37698-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37698-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37698-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37698-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37698-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37698-142">INPUTS</span></span>

### <span data-ttu-id="37698-143">Brak</span><span class="sxs-lookup"><span data-stu-id="37698-143">None</span></span>

## <span data-ttu-id="37698-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="37698-144">OUTPUTS</span></span>

### <span data-ttu-id="37698-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37698-145">System.Boolean</span></span>

## <span data-ttu-id="37698-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="37698-146">NOTES</span></span>

## <span data-ttu-id="37698-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37698-147">RELATED LINKS</span></span>

[<span data-ttu-id="37698-148">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="37698-148">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="37698-149">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="37698-149">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)