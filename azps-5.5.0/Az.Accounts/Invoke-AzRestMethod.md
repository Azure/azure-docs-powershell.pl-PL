---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: f8475c7cead6159231314989d21430658128c01f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190458"
---
# <span data-ttu-id="36024-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="36024-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="36024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36024-102">SYNOPSIS</span></span>
<span data-ttu-id="36024-103">Konstruowanie i wykonywanie żądania HTTP tylko do punktu końcowego zarządzania zasobami platformy Azure</span><span class="sxs-lookup"><span data-stu-id="36024-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="36024-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="36024-104">SYNTAX</span></span>

### <span data-ttu-id="36024-105">ByPath (domyślne)</span><span class="sxs-lookup"><span data-stu-id="36024-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36024-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="36024-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36024-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="36024-107">DESCRIPTION</span></span>
<span data-ttu-id="36024-108">Konstruowanie i wykonywanie żądania HTTP tylko do punktu końcowego zarządzania zasobami platformy Azure</span><span class="sxs-lookup"><span data-stu-id="36024-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="36024-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="36024-109">EXAMPLES</span></span>

### <span data-ttu-id="36024-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="36024-110">Example 1</span></span>
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

<span data-ttu-id="36024-111">Uzyskiwanie obszaru roboczego analizy dziennika według ścieżki</span><span class="sxs-lookup"><span data-stu-id="36024-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="36024-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36024-112">PARAMETERS</span></span>

### <span data-ttu-id="36024-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="36024-113">-ApiVersion</span></span>
<span data-ttu-id="36024-114">Wersja interfejsu API</span><span class="sxs-lookup"><span data-stu-id="36024-114">Api Version</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36024-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="36024-115">-AsJob</span></span>
<span data-ttu-id="36024-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="36024-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36024-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36024-117">-DefaultProfile</span></span>
<span data-ttu-id="36024-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="36024-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36024-119">— Metoda</span><span class="sxs-lookup"><span data-stu-id="36024-119">-Method</span></span>
<span data-ttu-id="36024-120">Metoda Http</span><span class="sxs-lookup"><span data-stu-id="36024-120">Http Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: GET, POST, PUT, PATCH, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36024-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="36024-121">-Name</span></span>
<span data-ttu-id="36024-122">Lista nazwa zasobu docelowego</span><span class="sxs-lookup"><span data-stu-id="36024-122">list of Target Resource Name</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36024-123">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="36024-123">-Path</span></span>
<span data-ttu-id="36024-124">Ścieżka docelowa</span><span class="sxs-lookup"><span data-stu-id="36024-124">Target Path</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36024-125">— Ładna</span><span class="sxs-lookup"><span data-stu-id="36024-125">-Payload</span></span>
<span data-ttu-id="36024-126">JSON format payload</span><span class="sxs-lookup"><span data-stu-id="36024-126">JSON format payload</span></span>

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

### <span data-ttu-id="36024-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36024-127">-ResourceGroupName</span></span>
<span data-ttu-id="36024-128">Nazwa grupy zasobów docelowych</span><span class="sxs-lookup"><span data-stu-id="36024-128">Target Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36024-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="36024-129">-ResourceProviderName</span></span>
<span data-ttu-id="36024-130">Nazwa docelowego dostawcy zasobów</span><span class="sxs-lookup"><span data-stu-id="36024-130">Target Resource Provider Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36024-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="36024-131">-ResourceType</span></span>
<span data-ttu-id="36024-132">Lista typów zasobów docelowych</span><span class="sxs-lookup"><span data-stu-id="36024-132">List of Target Resource Type</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36024-133">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36024-133">-SubscriptionId</span></span>
<span data-ttu-id="36024-134">Identyfikator subskrypcji docelowej</span><span class="sxs-lookup"><span data-stu-id="36024-134">Target Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36024-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36024-135">-Confirm</span></span>
<span data-ttu-id="36024-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36024-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36024-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36024-137">-WhatIf</span></span>
<span data-ttu-id="36024-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36024-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36024-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="36024-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36024-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36024-140">CommonParameters</span></span>
<span data-ttu-id="36024-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36024-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36024-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36024-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36024-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36024-143">INPUTS</span></span>

### <span data-ttu-id="36024-144">System.string</span><span class="sxs-lookup"><span data-stu-id="36024-144">System.string</span></span>

## <span data-ttu-id="36024-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36024-145">OUTPUTS</span></span>

### <span data-ttu-id="36024-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="36024-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="36024-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="36024-147">NOTES</span></span>

## <span data-ttu-id="36024-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36024-148">RELATED LINKS</span></span>
