---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8ca5efc7e5cee80fdf7ce34a13ce23ac733c0154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544403"
---
# <span data-ttu-id="ea4f4-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ea4f4-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="ea4f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea4f4-102">SYNOPSIS</span></span>
<span data-ttu-id="ea4f4-103">Modyfikuje konto w usłudze Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea4f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea4f4-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea4f4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ea4f4-105">DESCRIPTION</span></span>
<span data-ttu-id="ea4f4-106">Polecenie cmdlet **Set-AzureRmDataLakeAnalyticsAccount** modyfikuje konto usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ea4f4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea4f4-107">EXAMPLES</span></span>

### <span data-ttu-id="ea4f4-108">Przykład 1. modyfikowanie źródła danych konta</span><span class="sxs-lookup"><span data-stu-id="ea4f4-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="ea4f4-109">To polecenie powoduje zmianę domyślnego źródła danych i właściwości Tagi konta.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="ea4f4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea4f4-110">PARAMETERS</span></span>

### <span data-ttu-id="ea4f4-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="ea4f4-111">-AllowAzureIpState</span></span>
<span data-ttu-id="ea4f4-112">Opcjonalnie Zezwalaj na używanie/blokowanie początkowych adresów IP platformy Azure za pośrednictwem zapory.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: FirewallAllowAzureIpsState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea4f4-113">-DefaultProfile</span></span>
<span data-ttu-id="ea4f4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ea4f4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4f4-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="ea4f4-115">-FirewallState</span></span>
<span data-ttu-id="ea4f4-116">Opcjonalnie Włącz/Wyłącz istniejące reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-116">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: FirewallState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4f4-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="ea4f4-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="ea4f4-118">Opcjonalne maksymalne obsługiwane jednostki analityczne umożliwiające aktualizowanie konta.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-118">The optional maximum supported analytics units to update the account with.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4f4-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="ea4f4-119">-MaxJobCount</span></span>
<span data-ttu-id="ea4f4-120">Opcjonalne maksymalne obsługiwane zadania w tym samym czasie skonfigurowane w ramach konta.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4f4-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ea4f4-121">-Name</span></span>
<span data-ttu-id="ea4f4-122">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-122">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4f4-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="ea4f4-123">-QueryStoreRetention</span></span>
<span data-ttu-id="ea4f4-124">Opcjonalna liczba dni, przez jaką metadane zadania są zachowywane w ramach konta.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-124">The optional number of days that job metadata is retained to set in the account.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4f4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea4f4-125">-ResourceGroupName</span></span>
<span data-ttu-id="ea4f4-126">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4f4-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="ea4f4-127">-Tag</span></span>
<span data-ttu-id="ea4f4-128">Ciąg znaków, definiujący ciąg znaczników skojarzonych z tym kontem, które powinny zastąpić bieżący zestaw tagów</span><span class="sxs-lookup"><span data-stu-id="ea4f4-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4f4-129">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="ea4f4-129">-Tier</span></span>
<span data-ttu-id="ea4f4-130">Pożądana warstwa zobowiązań do użycia dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4f4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea4f4-131">CommonParameters</span></span>
<span data-ttu-id="ea4f4-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea4f4-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea4f4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea4f4-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea4f4-134">INPUTS</span></span>

### <span data-ttu-id="ea4f4-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ea4f4-135">None</span></span>
<span data-ttu-id="ea4f4-136">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea4f4-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea4f4-137">OUTPUTS</span></span>

### <span data-ttu-id="ea4f4-138">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ea4f4-138">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="ea4f4-139">Zaktualizowane dane konta.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-139">The updated account details.</span></span>

## <span data-ttu-id="ea4f4-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea4f4-140">NOTES</span></span>

## <span data-ttu-id="ea4f4-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea4f4-141">RELATED LINKS</span></span>

[<span data-ttu-id="ea4f4-142">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ea4f4-142">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ea4f4-143">Nowe — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ea4f4-143">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ea4f4-144">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ea4f4-144">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ea4f4-145">Test — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ea4f4-145">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


