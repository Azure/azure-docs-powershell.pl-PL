---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8de6b2a0d86c9eb83a067f4982a5ef62d3a9adbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527642"
---
# <span data-ttu-id="806b7-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="806b7-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="806b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="806b7-102">SYNOPSIS</span></span>
<span data-ttu-id="806b7-103">Modyfikuje konto w usłudze Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="806b7-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="806b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="806b7-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tags] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxDegreeOfParallelism <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="806b7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="806b7-105">DESCRIPTION</span></span>
<span data-ttu-id="806b7-106">Polecenie cmdlet **Set-AzureRmDataLakeAnalyticsAccount** modyfikuje konto usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="806b7-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="806b7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="806b7-107">EXAMPLES</span></span>

### <span data-ttu-id="806b7-108">Przykład 1. modyfikowanie źródła danych konta</span><span class="sxs-lookup"><span data-stu-id="806b7-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="806b7-109">To polecenie powoduje zmianę domyślnego źródła danych i właściwości Tagi konta.</span><span class="sxs-lookup"><span data-stu-id="806b7-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="806b7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="806b7-110">PARAMETERS</span></span>

### <span data-ttu-id="806b7-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="806b7-111">-AllowAzureIpState</span></span>
<span data-ttu-id="806b7-112">Opcjonalnie Zezwalaj na używanie/blokowanie początkowych adresów IP platformy Azure za pośrednictwem zapory.</span><span class="sxs-lookup"><span data-stu-id="806b7-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="806b7-113">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="806b7-113">-FirewallState</span></span>
<span data-ttu-id="806b7-114">Opcjonalnie Włącz/Wyłącz istniejące reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="806b7-114">Optionally enable/disable existing firewall rules.</span></span>

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

### <span data-ttu-id="806b7-115">-MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="806b7-115">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="806b7-116">Opcjonalny maksymalny obsługiwany stopień równoległości w celu zaktualizowania konta.</span><span class="sxs-lookup"><span data-stu-id="806b7-116">The optional maximum supported degree of parallelism to update the account with.</span></span>

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

### <span data-ttu-id="806b7-117">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="806b7-117">-MaxJobCount</span></span>
<span data-ttu-id="806b7-118">Opcjonalne maksymalne obsługiwane zadania w tym samym czasie skonfigurowane w ramach konta.</span><span class="sxs-lookup"><span data-stu-id="806b7-118">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="806b7-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="806b7-119">-Name</span></span>
<span data-ttu-id="806b7-120">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="806b7-120">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="806b7-121">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="806b7-121">-QueryStoreRetention</span></span>
<span data-ttu-id="806b7-122">Opcjonalna liczba dni, przez jaką metadane zadania są zachowywane w ramach konta.</span><span class="sxs-lookup"><span data-stu-id="806b7-122">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="806b7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="806b7-123">-ResourceGroupName</span></span>
<span data-ttu-id="806b7-124">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="806b7-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="806b7-125">-Tagi</span><span class="sxs-lookup"><span data-stu-id="806b7-125">-Tags</span></span>
<span data-ttu-id="806b7-126">Określa pary klucz-wartość, które mogą być używane do identyfikowania konta usługi Data Lake Analytics wśród innych zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="806b7-126">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

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

### <span data-ttu-id="806b7-127">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="806b7-127">-Tier</span></span>
<span data-ttu-id="806b7-128">Pożądana warstwa zobowiązań do użycia dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="806b7-128">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="806b7-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="806b7-129">-DefaultProfile</span></span>
<span data-ttu-id="806b7-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="806b7-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806b7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="806b7-131">CommonParameters</span></span>
<span data-ttu-id="806b7-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="806b7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="806b7-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="806b7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="806b7-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="806b7-134">INPUTS</span></span>

## <span data-ttu-id="806b7-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="806b7-135">OUTPUTS</span></span>

### <span data-ttu-id="806b7-136">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="806b7-136">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="806b7-137">Zaktualizowane dane konta.</span><span class="sxs-lookup"><span data-stu-id="806b7-137">The updated account details.</span></span>

## <span data-ttu-id="806b7-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="806b7-138">NOTES</span></span>

## <span data-ttu-id="806b7-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="806b7-139">RELATED LINKS</span></span>

[<span data-ttu-id="806b7-140">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="806b7-140">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="806b7-141">Nowe — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="806b7-141">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="806b7-142">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="806b7-142">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="806b7-143">Test — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="806b7-143">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


