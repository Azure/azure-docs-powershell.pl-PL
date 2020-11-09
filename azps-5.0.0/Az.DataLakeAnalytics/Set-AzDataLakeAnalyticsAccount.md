---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 2a762bb115132f97dd31cf14f9f13d7c6cf5ef70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305761"
---
# <span data-ttu-id="28969-101">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="28969-101">Set-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="28969-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28969-102">SYNOPSIS</span></span>
<span data-ttu-id="28969-103">Modyfikuje konto w usłudze Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="28969-103">Modifies a Data Lake Analytics account.</span></span>

## <span data-ttu-id="28969-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28969-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28969-105">Opis</span><span class="sxs-lookup"><span data-stu-id="28969-105">DESCRIPTION</span></span>
<span data-ttu-id="28969-106">Polecenie cmdlet **Set-AzDataLakeAnalyticsAccount** modyfikuje konto usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="28969-106">The **Set-AzDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="28969-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28969-107">EXAMPLES</span></span>

### <span data-ttu-id="28969-108">Przykład 1. modyfikowanie źródła danych konta</span><span class="sxs-lookup"><span data-stu-id="28969-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="28969-109">To polecenie powoduje zmianę domyślnego źródła danych i właściwości Tagi konta.</span><span class="sxs-lookup"><span data-stu-id="28969-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="28969-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28969-110">PARAMETERS</span></span>

### <span data-ttu-id="28969-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="28969-111">-AllowAzureIpState</span></span>
<span data-ttu-id="28969-112">Opcjonalnie Zezwalaj na używanie/blokowanie początkowych adresów IP platformy Azure za pośrednictwem zapory.</span><span class="sxs-lookup"><span data-stu-id="28969-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28969-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28969-113">-DefaultProfile</span></span>
<span data-ttu-id="28969-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="28969-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28969-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="28969-115">-FirewallState</span></span>
<span data-ttu-id="28969-116">Opcjonalnie Włącz/Wyłącz istniejące reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="28969-116">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28969-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="28969-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="28969-118">Opcjonalne maksymalne obsługiwane jednostki analityczne umożliwiające aktualizowanie konta.</span><span class="sxs-lookup"><span data-stu-id="28969-118">The optional maximum supported analytics units to update the account with.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28969-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="28969-119">-MaxJobCount</span></span>
<span data-ttu-id="28969-120">Opcjonalne maksymalne obsługiwane zadania w tym samym czasie skonfigurowane w ramach konta.</span><span class="sxs-lookup"><span data-stu-id="28969-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28969-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="28969-121">-Name</span></span>
<span data-ttu-id="28969-122">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="28969-122">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28969-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="28969-123">-QueryStoreRetention</span></span>
<span data-ttu-id="28969-124">Opcjonalna liczba dni, przez jaką metadane zadania są zachowywane w ramach konta.</span><span class="sxs-lookup"><span data-stu-id="28969-124">The optional number of days that job metadata is retained to set in the account.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28969-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28969-125">-ResourceGroupName</span></span>
<span data-ttu-id="28969-126">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="28969-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28969-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="28969-127">-Tag</span></span>
<span data-ttu-id="28969-128">Ciąg znaków, definiujący ciąg znaczników skojarzonych z tym kontem, które powinny zastąpić bieżący zestaw tagów</span><span class="sxs-lookup"><span data-stu-id="28969-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28969-129">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="28969-129">-Tier</span></span>
<span data-ttu-id="28969-130">Pożądana warstwa zobowiązań do użycia dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="28969-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28969-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28969-131">CommonParameters</span></span>
<span data-ttu-id="28969-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28969-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28969-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28969-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28969-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28969-134">INPUTS</span></span>

### <span data-ttu-id="28969-135">System. String</span><span class="sxs-lookup"><span data-stu-id="28969-135">System.String</span></span>

### <span data-ttu-id="28969-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="28969-136">System.Collections.Hashtable</span></span>

### <span data-ttu-id="28969-137">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="28969-137">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="28969-138">System. Nullable "1 [[Microsoft. Azure. Management. datalake. Analytics. models., Microsoft. Azure. Management. datalake. Analytics, wersja = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="28969-138">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="28969-139">System. Nullable "1 [[Microsoft. Azure. Management. datalake. Analytics. modele. FirewallState, Microsoft. Azure. Management. datalake. Analytics, wersja = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="28969-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="28969-140">System. Nullable "1 [[Microsoft. Azure. Management. datalake. Analytics. modele. FirewallAllowAzureIpsState, Microsoft. Azure. Management. datalake. Analytics, wersja = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="28969-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="28969-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28969-141">OUTPUTS</span></span>

### <span data-ttu-id="28969-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="28969-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="28969-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28969-143">NOTES</span></span>

## <span data-ttu-id="28969-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28969-144">RELATED LINKS</span></span>

[<span data-ttu-id="28969-145">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="28969-145">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="28969-146">Nowe — AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="28969-146">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="28969-147">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="28969-147">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="28969-148">Test — AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="28969-148">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


