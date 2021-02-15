---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: afe9e1f604754c88035ed79f0eb480321ca348ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242059"
---
# <span data-ttu-id="1b19c-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="1b19c-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="1b19c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b19c-102">SYNOPSIS</span></span>
<span data-ttu-id="1b19c-103">Aktualizowanie listy ACL sieci usługi signalr.</span><span class="sxs-lookup"><span data-stu-id="1b19c-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="1b19c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1b19c-104">SYNTAX</span></span>

### <span data-ttu-id="1b19c-105">ResourceGroupParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="1b19c-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b19c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b19c-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b19c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b19c-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b19c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1b19c-108">DESCRIPTION</span></span>
<span data-ttu-id="1b19c-109">Zaktualizuj wartość ACL sieci usługi signalr, w tym domyślną akcję i wartość Acls sieci dla połączenia publicznego i prywatnego.</span><span class="sxs-lookup"><span data-stu-id="1b19c-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="1b19c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1b19c-110">EXAMPLES</span></span>

### <span data-ttu-id="1b19c-111">Zezwalaj na usługę RESTAPI, clientConnection dla sieci publicznej i ustaw domyślną akcję Deny (Odmów)</span><span class="sxs-lookup"><span data-stu-id="1b19c-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -DefaultAction Deny -PublicNetwork -Allow RESTAPI,ClientConnection

PS C:\>  $networkAcl

DefaultAction PublicNetwork                                        PrivateEndpoints
------------- -------------                                        ----------------
Deny          Microsoft.Azure.Commands.SignalR.Models.PSNetworkAcl {pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1}

PS C:\> $networkAcl.PublicNetwork
Allow                       Deny
-----                       ----
{ClientConnection, RESTAPI} {}
```

### <span data-ttu-id="1b19c-112">Zezwalaj na połączenie klienta i połączenie z serwerem dla prywatnego połączenia punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="1b19c-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="1b19c-113">Odrzucanie połączenia klienta zarówno dla sieci publicznej, jak i prywatnego połączenia punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="1b19c-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="1b19c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b19c-114">PARAMETERS</span></span>

### <span data-ttu-id="1b19c-115">— Zezwalaj</span><span class="sxs-lookup"><span data-stu-id="1b19c-115">-Allow</span></span>
<span data-ttu-id="1b19c-116">Dozwolone adresy ACL sieci</span><span class="sxs-lookup"><span data-stu-id="1b19c-116">Allowed network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b19c-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1b19c-117">-AsJob</span></span>
<span data-ttu-id="1b19c-118">Uruchom polecenie cmdlet w zadaniu w tle.</span><span class="sxs-lookup"><span data-stu-id="1b19c-118">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="1b19c-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="1b19c-119">-DefaultAction</span></span>
<span data-ttu-id="1b19c-120">Domyślna akcja acl sieci signalr ( zezwalaj lub odmów).</span><span class="sxs-lookup"><span data-stu-id="1b19c-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="1b19c-121">Decyduje ona, czy ACL sieci są odrzucane, czy zezwalać na ich działanie.</span><span class="sxs-lookup"><span data-stu-id="1b19c-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="1b19c-122">Jeśli na przykład akcja domyślna jest zezwalana, ważne są tylko acla odmów.</span><span class="sxs-lookup"><span data-stu-id="1b19c-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b19c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b19c-123">-DefaultProfile</span></span>
<span data-ttu-id="1b19c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b19c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b19c-125">— Odmów</span><span class="sxs-lookup"><span data-stu-id="1b19c-125">-Deny</span></span>
<span data-ttu-id="1b19c-126">Odmówiono ACL sieci</span><span class="sxs-lookup"><span data-stu-id="1b19c-126">Denied network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b19c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b19c-127">-InputObject</span></span>
<span data-ttu-id="1b19c-128">Obiekt zasobu SignalR.</span><span class="sxs-lookup"><span data-stu-id="1b19c-128">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b19c-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1b19c-129">-Name</span></span>
<span data-ttu-id="1b19c-130">Nazwa usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="1b19c-130">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b19c-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="1b19c-131">-PrivateEndpointName</span></span>
<span data-ttu-id="1b19c-132">Nazwy prywatnych punktów końcowych do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="1b19c-132">Name(s) of private endpoint(s) to be updated</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b19c-133">- PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="1b19c-133">-PublicNetwork</span></span>
<span data-ttu-id="1b19c-134">Aktualizowanie ACL sieci publicznej</span><span class="sxs-lookup"><span data-stu-id="1b19c-134">Update public network ACLs</span></span>

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

### <span data-ttu-id="1b19c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b19c-135">-ResourceGroupName</span></span>
<span data-ttu-id="1b19c-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1b19c-136">The resource group name.</span></span>
<span data-ttu-id="1b19c-137">Ustawienie domyślne będzie używane, jeśli nie zostanie określone.</span><span class="sxs-lookup"><span data-stu-id="1b19c-137">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b19c-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b19c-138">-ResourceId</span></span>
<span data-ttu-id="1b19c-139">Identyfikator zasobu usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="1b19c-139">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b19c-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b19c-140">-Confirm</span></span>
<span data-ttu-id="1b19c-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1b19c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b19c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b19c-142">-WhatIf</span></span>
<span data-ttu-id="1b19c-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b19c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b19c-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1b19c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b19c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b19c-145">CommonParameters</span></span>
<span data-ttu-id="1b19c-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b19c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b19c-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b19c-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b19c-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b19c-148">INPUTS</span></span>

### <span data-ttu-id="1b19c-149">System.String</span><span class="sxs-lookup"><span data-stu-id="1b19c-149">System.String</span></span>

## <span data-ttu-id="1b19c-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1b19c-150">OUTPUTS</span></span>

### <span data-ttu-id="1b19c-151">Microsoft.Azure.Commands.Signalr.Models.PSSignalRNetworkAcls</span><span class="sxs-lookup"><span data-stu-id="1b19c-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="1b19c-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1b19c-152">NOTES</span></span>

## <span data-ttu-id="1b19c-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b19c-153">RELATED LINKS</span></span>
