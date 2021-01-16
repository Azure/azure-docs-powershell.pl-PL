---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: f8475c7cead6159231314989d21430658128c01f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363904"
---
# <span data-ttu-id="4d115-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="4d115-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="4d115-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d115-102">SYNOPSIS</span></span>
<span data-ttu-id="4d115-103">Konstruowanie i wykonywanie żądania HTTP do punktu końcowego zarządzania zasobami platformy Azure</span><span class="sxs-lookup"><span data-stu-id="4d115-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="4d115-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d115-104">SYNTAX</span></span>

### <span data-ttu-id="4d115-105">ByPath (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4d115-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d115-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="4d115-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d115-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4d115-107">DESCRIPTION</span></span>
<span data-ttu-id="4d115-108">Konstruowanie i wykonywanie żądania HTTP do punktu końcowego zarządzania zasobami platformy Azure</span><span class="sxs-lookup"><span data-stu-id="4d115-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="4d115-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d115-109">EXAMPLES</span></span>

### <span data-ttu-id="4d115-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4d115-110">Example 1</span></span>
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

<span data-ttu-id="4d115-111">Pobieranie obszaru roboczego Analiza dzienników według ścieżki</span><span class="sxs-lookup"><span data-stu-id="4d115-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="4d115-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d115-112">PARAMETERS</span></span>

### <span data-ttu-id="4d115-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4d115-113">-ApiVersion</span></span>
<span data-ttu-id="4d115-114">Wersja interfejsu API</span><span class="sxs-lookup"><span data-stu-id="4d115-114">Api Version</span></span>

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

### <span data-ttu-id="4d115-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d115-115">-AsJob</span></span>
<span data-ttu-id="4d115-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4d115-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d115-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d115-117">-DefaultProfile</span></span>
<span data-ttu-id="4d115-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d115-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d115-119">-Method</span><span class="sxs-lookup"><span data-stu-id="4d115-119">-Method</span></span>
<span data-ttu-id="4d115-120">Metoda http</span><span class="sxs-lookup"><span data-stu-id="4d115-120">Http Method</span></span>

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

### <span data-ttu-id="4d115-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4d115-121">-Name</span></span>
<span data-ttu-id="4d115-122">Lista nazw zasobów docelowych</span><span class="sxs-lookup"><span data-stu-id="4d115-122">list of Target Resource Name</span></span>

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

### <span data-ttu-id="4d115-123">-Path</span><span class="sxs-lookup"><span data-stu-id="4d115-123">-Path</span></span>
<span data-ttu-id="4d115-124">Ścieżka docelowa</span><span class="sxs-lookup"><span data-stu-id="4d115-124">Target Path</span></span>

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

### <span data-ttu-id="4d115-125">-Ładunek</span><span class="sxs-lookup"><span data-stu-id="4d115-125">-Payload</span></span>
<span data-ttu-id="4d115-126">Ładunek formatu JSON</span><span class="sxs-lookup"><span data-stu-id="4d115-126">JSON format payload</span></span>

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

### <span data-ttu-id="4d115-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d115-127">-ResourceGroupName</span></span>
<span data-ttu-id="4d115-128">Nazwa grupy zasobów docelowych</span><span class="sxs-lookup"><span data-stu-id="4d115-128">Target Resource Group Name</span></span>

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

### <span data-ttu-id="4d115-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="4d115-129">-ResourceProviderName</span></span>
<span data-ttu-id="4d115-130">Nazwa dostawcy zasobów docelowych</span><span class="sxs-lookup"><span data-stu-id="4d115-130">Target Resource Provider Name</span></span>

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

### <span data-ttu-id="4d115-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4d115-131">-ResourceType</span></span>
<span data-ttu-id="4d115-132">Lista typów zasobów docelowych</span><span class="sxs-lookup"><span data-stu-id="4d115-132">List of Target Resource Type</span></span>

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

### <span data-ttu-id="4d115-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4d115-133">-SubscriptionId</span></span>
<span data-ttu-id="4d115-134">Identyfikator subskrypcji docelowej</span><span class="sxs-lookup"><span data-stu-id="4d115-134">Target Subscription Id</span></span>

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

### <span data-ttu-id="4d115-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d115-135">-Confirm</span></span>
<span data-ttu-id="4d115-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d115-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d115-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d115-137">-WhatIf</span></span>
<span data-ttu-id="4d115-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d115-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d115-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d115-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d115-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d115-140">CommonParameters</span></span>
<span data-ttu-id="4d115-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d115-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d115-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d115-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d115-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d115-143">INPUTS</span></span>

### <span data-ttu-id="4d115-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4d115-144">System.string</span></span>

## <span data-ttu-id="4d115-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d115-145">OUTPUTS</span></span>

### <span data-ttu-id="4d115-146">Microsoft. Azure. Commands. profile. PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="4d115-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="4d115-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d115-147">NOTES</span></span>

## <span data-ttu-id="4d115-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d115-148">RELATED LINKS</span></span>
