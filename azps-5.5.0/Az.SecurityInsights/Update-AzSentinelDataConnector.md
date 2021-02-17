---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
ms.openlocfilehash: b998d699836cf99f9d6cb9dc53bef36b6fc94ca3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191187"
---
# <span data-ttu-id="7a2df-101">Update-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="7a2df-101">Update-AzSentinelDataConnector</span></span>

## <span data-ttu-id="7a2df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a2df-102">SYNOPSIS</span></span>
<span data-ttu-id="7a2df-103">Aktualizowanie łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="7a2df-103">Update a Data Connector.</span></span>

## <span data-ttu-id="7a2df-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7a2df-104">SYNTAX</span></span>

### <span data-ttu-id="7a2df-105">DataConnectorId (domyślna)</span><span class="sxs-lookup"><span data-stu-id="7a2df-105">DataConnectorId (Default)</span></span>
```
Update-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-Alerts <String>] [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>]
 [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a2df-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7a2df-106">InputObject</span></span>
```
Update-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-Alerts <String>]
 [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>]
 [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a2df-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a2df-107">ResourceId</span></span>
```
Update-AzSentinelDataConnector -ResourceId <String> [-Alerts <String>] [-SubscriptionId <String>]
 [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>]
 [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a2df-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7a2df-108">DESCRIPTION</span></span>
<span data-ttu-id="7a2df-109">Polecenie **cmdlet Update-AzSentinelDataConnector** aktualizuje łącznik danych w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="7a2df-109">The **Update-AzSentinelDataConnector** cmdlet updates the Data Connector in the specified workspace.</span></span>
<span data-ttu-id="7a2df-110">Obiekt **DataConnector** można przekazać jako parametr lub za pomocą operatora potoku albo też określić wymagane parametry.</span><span class="sxs-lookup"><span data-stu-id="7a2df-110">You can pass an **DataConnector** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="7a2df-111">Możesz użyć *parametru Confirm* i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7a2df-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="7a2df-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7a2df-112">EXAMPLES</span></span>

### <span data-ttu-id="7a2df-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7a2df-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId" -Alerts Disabled
```

<span data-ttu-id="7a2df-114">Polecenie pobiera łącznik danych według *danychConnectorId* i ustawia stan *Alerty* na *Wyłączone.*</span><span class="sxs-lookup"><span data-stu-id="7a2df-114">The command gets the Data Connector by *DataConnectorId* and sets the *Alerts* state to *Disabled*.</span></span>  <span data-ttu-id="7a2df-115">Wszystkie pozostałe właściwości pozostają takie same.</span><span class="sxs-lookup"><span data-stu-id="7a2df-115">All other properties remain the same.</span></span>

## <span data-ttu-id="7a2df-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a2df-116">PARAMETERS</span></span>

### <span data-ttu-id="7a2df-117">— Alerty</span><span class="sxs-lookup"><span data-stu-id="7a2df-117">-Alerts</span></span>
<span data-ttu-id="7a2df-118">Alerty łącznika danych</span><span class="sxs-lookup"><span data-stu-id="7a2df-118">Data Connector Alerts</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2df-119">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="7a2df-119">-AwsRoleArn</span></span>
<span data-ttu-id="7a2df-120">Rola AWS łącznika danych</span><span class="sxs-lookup"><span data-stu-id="7a2df-120">Data Connector AWS Role Arn</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2df-121">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="7a2df-121">-DataConnectorId</span></span>
<span data-ttu-id="7a2df-122">Identyfikator łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="7a2df-122">Data Connector Id.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2df-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a2df-123">-DefaultProfile</span></span>
<span data-ttu-id="7a2df-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a2df-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2df-125">- DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="7a2df-125">-DiscoveryLogs</span></span>
<span data-ttu-id="7a2df-126">Dzienniki odnajdowania łącznika danych</span><span class="sxs-lookup"><span data-stu-id="7a2df-126">Data Connector Discovery Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2df-127">— Exchange</span><span class="sxs-lookup"><span data-stu-id="7a2df-127">-Exchange</span></span>
<span data-ttu-id="7a2df-128">Wymiana łączników danych</span><span class="sxs-lookup"><span data-stu-id="7a2df-128">Data Connector Exchange</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2df-129">— Wskaźniki</span><span class="sxs-lookup"><span data-stu-id="7a2df-129">-Indicators</span></span>
<span data-ttu-id="7a2df-130">Wskaźniki łącznika danych</span><span class="sxs-lookup"><span data-stu-id="7a2df-130">Data Connector Indicators</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2df-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a2df-131">-InputObject</span></span>
<span data-ttu-id="7a2df-132">InputObject.</span><span class="sxs-lookup"><span data-stu-id="7a2df-132">InputObject.</span></span>

```yaml
Type: PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2df-133">Dzienniki</span><span class="sxs-lookup"><span data-stu-id="7a2df-133">-Logs</span></span>
<span data-ttu-id="7a2df-134">Dzienniki łącznika danych</span><span class="sxs-lookup"><span data-stu-id="7a2df-134">Data Connector Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2df-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a2df-135">-ResourceGroupName</span></span>
<span data-ttu-id="7a2df-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a2df-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2df-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a2df-137">-ResourceId</span></span>
<span data-ttu-id="7a2df-138">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="7a2df-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2df-139">— SharePoint</span><span class="sxs-lookup"><span data-stu-id="7a2df-139">-SharePoint</span></span>
<span data-ttu-id="7a2df-140">Łącznik danych w programie SharePoint</span><span class="sxs-lookup"><span data-stu-id="7a2df-140">Data Connector SharePoint</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2df-141">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a2df-141">-SubscriptionId</span></span>
<span data-ttu-id="7a2df-142">Identyfikator subskrypcji łącznika danych</span><span class="sxs-lookup"><span data-stu-id="7a2df-142">Data connector Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2df-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7a2df-143">-WorkspaceName</span></span>
<span data-ttu-id="7a2df-144">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="7a2df-144">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2df-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a2df-145">-Confirm</span></span>
<span data-ttu-id="7a2df-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7a2df-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2df-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a2df-147">-WhatIf</span></span>
<span data-ttu-id="7a2df-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a2df-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a2df-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7a2df-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2df-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a2df-150">CommonParameters</span></span>
<span data-ttu-id="7a2df-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a2df-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a2df-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a2df-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a2df-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a2df-153">INPUTS</span></span>

### <span data-ttu-id="7a2df-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="7a2df-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

### <span data-ttu-id="7a2df-155">System.String</span><span class="sxs-lookup"><span data-stu-id="7a2df-155">System.String</span></span>

## <span data-ttu-id="7a2df-156">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a2df-156">OUTPUTS</span></span>

### <span data-ttu-id="7a2df-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="7a2df-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

## <span data-ttu-id="7a2df-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7a2df-158">NOTES</span></span>

## <span data-ttu-id="7a2df-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a2df-159">RELATED LINKS</span></span>
