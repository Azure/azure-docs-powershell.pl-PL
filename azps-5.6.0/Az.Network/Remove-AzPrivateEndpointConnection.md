---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: be060c320c05b44a4b0d8f79b519f63e4dd47bcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996150"
---
# <span data-ttu-id="c69ae-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c69ae-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="c69ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c69ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c69ae-103">Usuwa prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="c69ae-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="c69ae-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c69ae-104">SYNTAX</span></span>

### <span data-ttu-id="c69ae-105">ByResourceId (Default)</span><span class="sxs-lookup"><span data-stu-id="c69ae-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c69ae-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="c69ae-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c69ae-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c69ae-107">DESCRIPTION</span></span>
<span data-ttu-id="c69ae-108">Polecenie **cmdlet Remove-AzPrivateEndpointConnection** usuwa prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="c69ae-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="c69ae-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c69ae-109">EXAMPLES</span></span>

### <span data-ttu-id="c69ae-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c69ae-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="c69ae-111">W tym przykładzie usuniesz prywatne połączenie punktu końcowego o nazwie MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="c69ae-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="c69ae-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c69ae-112">PARAMETERS</span></span>

### <span data-ttu-id="c69ae-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c69ae-113">-AsJob</span></span>
<span data-ttu-id="c69ae-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c69ae-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c69ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c69ae-115">-DefaultProfile</span></span>
<span data-ttu-id="c69ae-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c69ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c69ae-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c69ae-117">-Force</span></span>
<span data-ttu-id="c69ae-118">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="c69ae-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="c69ae-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c69ae-119">-Name</span></span>
<span data-ttu-id="c69ae-120">Nazwa prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="c69ae-120">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69ae-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c69ae-121">-PassThru</span></span>
<span data-ttu-id="c69ae-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="c69ae-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c69ae-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c69ae-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c69ae-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="c69ae-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="c69ae-125">Typ zasobu linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="c69ae-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69ae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c69ae-126">-ResourceGroupName</span></span>
<span data-ttu-id="c69ae-127">Nazwa grupy zasobów dla prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="c69ae-127">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69ae-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c69ae-128">-ResourceId</span></span>
<span data-ttu-id="c69ae-129">Identyfikator menedżera zasobów platformy Azure prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="c69ae-129">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69ae-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c69ae-130">-ServiceName</span></span>
<span data-ttu-id="c69ae-131">Nazwa usługi, do której należy prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="c69ae-131">The name of service that the private endpoint connection belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69ae-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c69ae-132">-Confirm</span></span>
<span data-ttu-id="c69ae-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c69ae-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c69ae-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c69ae-134">-WhatIf</span></span>
<span data-ttu-id="c69ae-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c69ae-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c69ae-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c69ae-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c69ae-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c69ae-137">CommonParameters</span></span>
<span data-ttu-id="c69ae-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c69ae-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c69ae-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c69ae-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c69ae-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c69ae-140">INPUTS</span></span>

### <span data-ttu-id="c69ae-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c69ae-141">System.String</span></span>

## <span data-ttu-id="c69ae-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c69ae-142">OUTPUTS</span></span>

### <span data-ttu-id="c69ae-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c69ae-143">System.Boolean</span></span>

## <span data-ttu-id="c69ae-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c69ae-144">NOTES</span></span>

## <span data-ttu-id="c69ae-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c69ae-145">RELATED LINKS</span></span>

[<span data-ttu-id="c69ae-146">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c69ae-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="c69ae-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c69ae-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="c69ae-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c69ae-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="c69ae-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c69ae-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
