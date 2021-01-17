---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: afe9e1f604754c88035ed79f0eb480321ca348ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336082"
---
# <span data-ttu-id="7ed56-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="7ed56-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="7ed56-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ed56-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed56-103">Zaktualizuj listę ACL sieci usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="7ed56-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="7ed56-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ed56-104">SYNTAX</span></span>

### <span data-ttu-id="7ed56-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7ed56-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ed56-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ed56-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ed56-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ed56-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ed56-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7ed56-108">DESCRIPTION</span></span>
<span data-ttu-id="7ed56-109">Aktualizowanie listy ACL sieci usługi sygnalizującej, w tym domyślnej akcji i list ACL sieci dla połączeń publicznych i prywatnych.</span><span class="sxs-lookup"><span data-stu-id="7ed56-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="7ed56-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ed56-110">EXAMPLES</span></span>

### <span data-ttu-id="7ed56-111">Zezwalaj na RESTAPI, ClientConnection dla sieci publicznej i ustaw dla niej akcję domyślną na odmowę</span><span class="sxs-lookup"><span data-stu-id="7ed56-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
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

### <span data-ttu-id="7ed56-112">Zezwalaj na połączenie klienckie i połączenie z serwerem dla prywatnego połączenia punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="7ed56-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="7ed56-113">Odrzucanie połączenia klienta zarówno w sieci publicznej, jak i w prywatnym połączeniu punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="7ed56-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="7ed56-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ed56-114">PARAMETERS</span></span>

### <span data-ttu-id="7ed56-115">-Allow</span><span class="sxs-lookup"><span data-stu-id="7ed56-115">-Allow</span></span>
<span data-ttu-id="7ed56-116">Dozwolone listy ACL sieci</span><span class="sxs-lookup"><span data-stu-id="7ed56-116">Allowed network ACLs</span></span>

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

### <span data-ttu-id="7ed56-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ed56-117">-AsJob</span></span>
<span data-ttu-id="7ed56-118">Uruchom polecenie cmdlet w zadaniu w tle.</span><span class="sxs-lookup"><span data-stu-id="7ed56-118">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="7ed56-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="7ed56-119">-DefaultAction</span></span>
<span data-ttu-id="7ed56-120">Domyślna akcja list ACL sieci sygnalizujących — Zezwalaj lub Odmów.</span><span class="sxs-lookup"><span data-stu-id="7ed56-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="7ed56-121">Decyduje, czy odrzucać listy ACL sieci, czy zezwolić na listy ACL sieci.</span><span class="sxs-lookup"><span data-stu-id="7ed56-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="7ed56-122">Jeśli na przykład domyślną akcją jest Zezwalaj, tylko sprawy z listy Odmów dostępu.</span><span class="sxs-lookup"><span data-stu-id="7ed56-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

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

### <span data-ttu-id="7ed56-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed56-123">-DefaultProfile</span></span>
<span data-ttu-id="7ed56-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed56-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ed56-125">-Odmów</span><span class="sxs-lookup"><span data-stu-id="7ed56-125">-Deny</span></span>
<span data-ttu-id="7ed56-126">Odrzucanie list ACL sieci</span><span class="sxs-lookup"><span data-stu-id="7ed56-126">Denied network ACLs</span></span>

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

### <span data-ttu-id="7ed56-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7ed56-127">-InputObject</span></span>
<span data-ttu-id="7ed56-128">Obiekt zasobu sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="7ed56-128">The SignalR resource object.</span></span>

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

### <span data-ttu-id="7ed56-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ed56-129">-Name</span></span>
<span data-ttu-id="7ed56-130">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="7ed56-130">The SignalR service name.</span></span>

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

### <span data-ttu-id="7ed56-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="7ed56-131">-PrivateEndpointName</span></span>
<span data-ttu-id="7ed56-132">Imiona i nazwiska prywatnych punktów końcowych, które mają zostać zaktualizowane</span><span class="sxs-lookup"><span data-stu-id="7ed56-132">Name(s) of private endpoint(s) to be updated</span></span>

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

### <span data-ttu-id="7ed56-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="7ed56-133">-PublicNetwork</span></span>
<span data-ttu-id="7ed56-134">Aktualizowanie list ACL sieci publicznej</span><span class="sxs-lookup"><span data-stu-id="7ed56-134">Update public network ACLs</span></span>

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

### <span data-ttu-id="7ed56-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ed56-135">-ResourceGroupName</span></span>
<span data-ttu-id="7ed56-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ed56-136">The resource group name.</span></span>
<span data-ttu-id="7ed56-137">Jeśli nie podano, zostanie użyte ustawienie domyślne.</span><span class="sxs-lookup"><span data-stu-id="7ed56-137">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="7ed56-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ed56-138">-ResourceId</span></span>
<span data-ttu-id="7ed56-139">Identyfikator zasobu usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="7ed56-139">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="7ed56-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ed56-140">-Confirm</span></span>
<span data-ttu-id="7ed56-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ed56-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ed56-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ed56-142">-WhatIf</span></span>
<span data-ttu-id="7ed56-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ed56-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ed56-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ed56-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ed56-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed56-145">CommonParameters</span></span>
<span data-ttu-id="7ed56-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ed56-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed56-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ed56-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed56-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ed56-148">INPUTS</span></span>

### <span data-ttu-id="7ed56-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7ed56-149">System.String</span></span>

## <span data-ttu-id="7ed56-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ed56-150">OUTPUTS</span></span>

### <span data-ttu-id="7ed56-151">Microsoft. Azure. Commands. Signals. modele. PSSignalRNetworkAcls</span><span class="sxs-lookup"><span data-stu-id="7ed56-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="7ed56-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ed56-152">NOTES</span></span>

## <span data-ttu-id="7ed56-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ed56-153">RELATED LINKS</span></span>
