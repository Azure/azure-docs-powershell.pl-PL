---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: 355de1e4eb4518b8ec3d7291b20f76bda5fb1a89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955018"
---
# <span data-ttu-id="78b76-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="78b76-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="78b76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78b76-102">SYNOPSIS</span></span>
<span data-ttu-id="78b76-103">Konstruowanie i wykonywanie żądania HTTP tylko do punktu końcowego zarządzania zasobami platformy Azure</span><span class="sxs-lookup"><span data-stu-id="78b76-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="78b76-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="78b76-104">SYNTAX</span></span>

### <span data-ttu-id="78b76-105">ByPath (domyślne)</span><span class="sxs-lookup"><span data-stu-id="78b76-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78b76-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="78b76-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78b76-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="78b76-107">DESCRIPTION</span></span>
<span data-ttu-id="78b76-108">Konstruowanie i wykonywanie żądania HTTP tylko do punktu końcowego zarządzania zasobami platformy Azure</span><span class="sxs-lookup"><span data-stu-id="78b76-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="78b76-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="78b76-109">EXAMPLES</span></span>

### <span data-ttu-id="78b76-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="78b76-110">Example 1</span></span>
```powershell
Invoke-AzRestMethod -Path "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}?api-version={API}" -Method GET

Headers    : {[Cache-Control, System.String[]], [Pragma, System.String[]], [x-ms-request-id, System.String[]], [Strict-Transport-Security, System.String[]]…}
Version    : 1.1
StatusCode : 200
Method     : GET
Content    : {
               "properties": {
                 "source": "Azure",
                 "customerId": "{customerId}",
                 "provisioningState": "Succeeded",
                 "sku": {
                   "name": "pergb2018",
                   "maxCapacityReservationLevel": 3000,
                   "lastSkuUpdate": "Mon, 25 May 2020 11:10:01 GMT"
                 },
                 "retentionInDays": 30,
                 "features": {
                   "legacy": 0,
                   "searchVersion": 1,
                   "enableLogAccessUsingOnlyResourcePermissions": true
                 },
                 "workspaceCapping": {
                   "dailyQuotaGb": -1.0,
                   "quotaNextResetTime": "Thu, 18 Jun 2020 05:00:00 GMT",
                   "dataIngestionStatus": "RespectQuota"
                 },
                 "enableFailover": false,
                 "publicNetworkAccessForIngestion": "Enabled",
                 "publicNetworkAccessForQuery": "Enabled",
                 "createdDate": "Mon, 25 May 2020 11:10:01 GMT",
                 "modifiedDate": "Mon, 25 May 2020 11:10:02 GMT"
               },
               "id": "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}",
               "name": "{workspace}",
               "type": "Microsoft.OperationalInsights/workspaces",
               "location": "eastasia",
               "tags": {}
             }
```

<span data-ttu-id="78b76-111">Uzyskiwanie obszaru roboczego analizy dziennika według ścieżki</span><span class="sxs-lookup"><span data-stu-id="78b76-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="78b76-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78b76-112">PARAMETERS</span></span>

### <span data-ttu-id="78b76-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="78b76-113">-ApiVersion</span></span>
<span data-ttu-id="78b76-114">Wersja interfejsu API</span><span class="sxs-lookup"><span data-stu-id="78b76-114">Api Version</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b76-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="78b76-115">-AsJob</span></span>
<span data-ttu-id="78b76-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="78b76-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78b76-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78b76-117">-DefaultProfile</span></span>
<span data-ttu-id="78b76-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="78b76-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78b76-119">— Metoda</span><span class="sxs-lookup"><span data-stu-id="78b76-119">-Method</span></span>
<span data-ttu-id="78b76-120">Metoda HTTP</span><span class="sxs-lookup"><span data-stu-id="78b76-120">Http Method</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GET, POST, PUT, PATCH, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b76-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="78b76-121">-Name</span></span>
<span data-ttu-id="78b76-122">Lista nazwa zasobu docelowego</span><span class="sxs-lookup"><span data-stu-id="78b76-122">list of Target Resource Name</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b76-123">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="78b76-123">-Path</span></span>
<span data-ttu-id="78b76-124">Ścieżka docelowa</span><span class="sxs-lookup"><span data-stu-id="78b76-124">Target Path</span></span>

```yaml
Type: System.String
Parameter Sets: ByPath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b76-125">— Ładna</span><span class="sxs-lookup"><span data-stu-id="78b76-125">-Payload</span></span>
<span data-ttu-id="78b76-126">JSON format payload</span><span class="sxs-lookup"><span data-stu-id="78b76-126">JSON format payload</span></span>

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

### <span data-ttu-id="78b76-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78b76-127">-ResourceGroupName</span></span>
<span data-ttu-id="78b76-128">Nazwa grupy zasobów docelowych</span><span class="sxs-lookup"><span data-stu-id="78b76-128">Target Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b76-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="78b76-129">-ResourceProviderName</span></span>
<span data-ttu-id="78b76-130">Nazwa dostawcy zasobów docelowych</span><span class="sxs-lookup"><span data-stu-id="78b76-130">Target Resource Provider Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b76-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="78b76-131">-ResourceType</span></span>
<span data-ttu-id="78b76-132">Lista typów zasobów docelowych</span><span class="sxs-lookup"><span data-stu-id="78b76-132">List of Target Resource Type</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b76-133">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78b76-133">-SubscriptionId</span></span>
<span data-ttu-id="78b76-134">Identyfikator subskrypcji docelowej</span><span class="sxs-lookup"><span data-stu-id="78b76-134">Target Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b76-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78b76-135">-Confirm</span></span>
<span data-ttu-id="78b76-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="78b76-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78b76-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78b76-137">-WhatIf</span></span>
<span data-ttu-id="78b76-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78b76-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78b76-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="78b76-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78b76-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b76-140">CommonParameters</span></span>
<span data-ttu-id="78b76-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78b76-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b76-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78b76-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b76-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78b76-143">INPUTS</span></span>

### <span data-ttu-id="78b76-144">System.string</span><span class="sxs-lookup"><span data-stu-id="78b76-144">System.string</span></span>

## <span data-ttu-id="78b76-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78b76-145">OUTPUTS</span></span>

### <span data-ttu-id="78b76-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="78b76-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="78b76-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="78b76-147">NOTES</span></span>

## <span data-ttu-id="78b76-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78b76-148">RELATED LINKS</span></span>
