---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
ms.openlocfilehash: b998d699836cf99f9d6cb9dc53bef36b6fc94ca3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502946"
---
# <span data-ttu-id="8f112-101">Update-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="8f112-101">Update-AzSentinelDataConnector</span></span>

## <span data-ttu-id="8f112-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f112-102">SYNOPSIS</span></span>
<span data-ttu-id="8f112-103">Aktualizowanie łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="8f112-103">Update a Data Connector.</span></span>

## <span data-ttu-id="8f112-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f112-104">SYNTAX</span></span>

### <span data-ttu-id="8f112-105">DataConnectorId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8f112-105">DataConnectorId (Default)</span></span>
```
Update-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-Alerts <String>] [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>]
 [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f112-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="8f112-106">InputObject</span></span>
```
Update-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-Alerts <String>]
 [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>]
 [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f112-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="8f112-107">ResourceId</span></span>
```
Update-AzSentinelDataConnector -ResourceId <String> [-Alerts <String>] [-SubscriptionId <String>]
 [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>]
 [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f112-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8f112-108">DESCRIPTION</span></span>
<span data-ttu-id="8f112-109">Polecenie cmdlet **Update-AzSentinelDataConnector** umożliwia zaktualizowanie łącznika danych w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="8f112-109">The **Update-AzSentinelDataConnector** cmdlet updates the Data Connector in the specified workspace.</span></span>
<span data-ttu-id="8f112-110">Obiekt programu **Dataconnecter** można przekazać jako parametr lub za pomocą operatora potoku albo też określić parametry wymagane.</span><span class="sxs-lookup"><span data-stu-id="8f112-110">You can pass an **DataConnector** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="8f112-111">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8f112-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="8f112-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f112-112">EXAMPLES</span></span>

### <span data-ttu-id="8f112-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8f112-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId" -Alerts Disabled
```

<span data-ttu-id="8f112-114">Polecenie pobiera Łącznik danych przez *DataConnectorId* i ustawia stan *alertów* na *wyłączony*.</span><span class="sxs-lookup"><span data-stu-id="8f112-114">The command gets the Data Connector by *DataConnectorId* and sets the *Alerts* state to *Disabled*.</span></span>  <span data-ttu-id="8f112-115">Pozostałe właściwości pozostają bez zmian.</span><span class="sxs-lookup"><span data-stu-id="8f112-115">All other properties remain the same.</span></span>

## <span data-ttu-id="8f112-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f112-116">PARAMETERS</span></span>

### <span data-ttu-id="8f112-117">-Alerty</span><span class="sxs-lookup"><span data-stu-id="8f112-117">-Alerts</span></span>
<span data-ttu-id="8f112-118">Alerty łącznika danych</span><span class="sxs-lookup"><span data-stu-id="8f112-118">Data Connector Alerts</span></span>

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

### <span data-ttu-id="8f112-119">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="8f112-119">-AwsRoleArn</span></span>
<span data-ttu-id="8f112-120">Łącznik danych AWS rola ARN</span><span class="sxs-lookup"><span data-stu-id="8f112-120">Data Connector AWS Role Arn</span></span>

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

### <span data-ttu-id="8f112-121">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="8f112-121">-DataConnectorId</span></span>
<span data-ttu-id="8f112-122">Identyfikator łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="8f112-122">Data Connector Id.</span></span>

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

### <span data-ttu-id="8f112-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f112-123">-DefaultProfile</span></span>
<span data-ttu-id="8f112-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f112-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f112-125">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="8f112-125">-DiscoveryLogs</span></span>
<span data-ttu-id="8f112-126">Dzienniki odnajdowania łączników danych</span><span class="sxs-lookup"><span data-stu-id="8f112-126">Data Connector Discovery Logs</span></span>

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

### <span data-ttu-id="8f112-127">-Exchange</span><span class="sxs-lookup"><span data-stu-id="8f112-127">-Exchange</span></span>
<span data-ttu-id="8f112-128">Wymiana łącznika danych</span><span class="sxs-lookup"><span data-stu-id="8f112-128">Data Connector Exchange</span></span>

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

### <span data-ttu-id="8f112-129">-Wskaźniki</span><span class="sxs-lookup"><span data-stu-id="8f112-129">-Indicators</span></span>
<span data-ttu-id="8f112-130">Wskaźniki łącznika danych</span><span class="sxs-lookup"><span data-stu-id="8f112-130">Data Connector Indicators</span></span>

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

### <span data-ttu-id="8f112-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8f112-131">-InputObject</span></span>
<span data-ttu-id="8f112-132">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="8f112-132">InputObject.</span></span>

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

### <span data-ttu-id="8f112-133">— Dzienniki</span><span class="sxs-lookup"><span data-stu-id="8f112-133">-Logs</span></span>
<span data-ttu-id="8f112-134">Dzienniki łącznika danych</span><span class="sxs-lookup"><span data-stu-id="8f112-134">Data Connector Logs</span></span>

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

### <span data-ttu-id="8f112-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f112-135">-ResourceGroupName</span></span>
<span data-ttu-id="8f112-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8f112-136">Resource group name.</span></span>

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

### <span data-ttu-id="8f112-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f112-137">-ResourceId</span></span>
<span data-ttu-id="8f112-138">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="8f112-138">Resource Id.</span></span>

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

### <span data-ttu-id="8f112-139">-Program SharePoint</span><span class="sxs-lookup"><span data-stu-id="8f112-139">-SharePoint</span></span>
<span data-ttu-id="8f112-140">Łącznik danych programu SharePoint</span><span class="sxs-lookup"><span data-stu-id="8f112-140">Data Connector SharePoint</span></span>

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

### <span data-ttu-id="8f112-141">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8f112-141">-SubscriptionId</span></span>
<span data-ttu-id="8f112-142">Identyfikator subskrypcji łącznika danych</span><span class="sxs-lookup"><span data-stu-id="8f112-142">Data connector Subscription Id</span></span>

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

### <span data-ttu-id="8f112-143">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="8f112-143">-WorkspaceName</span></span>
<span data-ttu-id="8f112-144">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8f112-144">Workspace Name.</span></span>

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

### <span data-ttu-id="8f112-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f112-145">-Confirm</span></span>
<span data-ttu-id="8f112-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f112-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f112-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f112-147">-WhatIf</span></span>
<span data-ttu-id="8f112-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f112-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f112-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8f112-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f112-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f112-150">CommonParameters</span></span>
<span data-ttu-id="8f112-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f112-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f112-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f112-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f112-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f112-153">INPUTS</span></span>

### <span data-ttu-id="8f112-154">Microsoft. Azure. Commands. SecurityInsights. models. dataconnects. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="8f112-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

### <span data-ttu-id="8f112-155">System. String</span><span class="sxs-lookup"><span data-stu-id="8f112-155">System.String</span></span>

## <span data-ttu-id="8f112-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f112-156">OUTPUTS</span></span>

### <span data-ttu-id="8f112-157">Microsoft. Azure. Commands. SecurityInsights. models. dataconnects. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="8f112-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

## <span data-ttu-id="8f112-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f112-158">NOTES</span></span>

## <span data-ttu-id="8f112-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f112-159">RELATED LINKS</span></span>
