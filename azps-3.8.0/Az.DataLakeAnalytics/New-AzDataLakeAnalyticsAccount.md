---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: c79665a6ed21309a7a702d9fd5bc5e876aa2ff21
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049808"
---
# <span data-ttu-id="53384-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="53384-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="53384-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53384-102">SYNOPSIS</span></span>
<span data-ttu-id="53384-103">Tworzy konto Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="53384-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="53384-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53384-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53384-105">Opis</span><span class="sxs-lookup"><span data-stu-id="53384-105">DESCRIPTION</span></span>
<span data-ttu-id="53384-106">Polecenie cmdlet **New-AzDataLakeAnalyticsAccount** tworzy konto usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="53384-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="53384-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53384-107">EXAMPLES</span></span>

### <span data-ttu-id="53384-108">Przykład 1: Tworzenie konta danych w usłudze Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="53384-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="53384-109">To polecenie tworzy konto usługi Data Lake Analytics o nazwie ContosoAdlAccount, w którym jest używany magazyn danych ContosoAdlStore, w grupie zasobów o nazwie ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="53384-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="53384-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53384-110">PARAMETERS</span></span>

### <span data-ttu-id="53384-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53384-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="53384-112">Określa nazwę konta usługi Data Lake Store, które ma zostać ustawione jako domyślne źródło danych.</span><span class="sxs-lookup"><span data-stu-id="53384-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53384-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53384-113">-DefaultProfile</span></span>
<span data-ttu-id="53384-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="53384-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53384-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="53384-115">-Location</span></span>
<span data-ttu-id="53384-116">Określa lokalizację, w której ma zostać utworzone konto usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="53384-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="53384-117">Obecnie w tej chwili jest obsługiwana tylko wschód amerykańska 2.</span><span class="sxs-lookup"><span data-stu-id="53384-117">Only East US 2 is supported at this time.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53384-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="53384-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="53384-119">Opcjonalna Maksymalna obsługiwana jednostka analityczna dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="53384-119">The optional maximum supported analytics units for this account.</span></span>

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

### <span data-ttu-id="53384-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="53384-120">-MaxJobCount</span></span>
<span data-ttu-id="53384-121">Opcjonalna Maksymalna liczba zadań obsługiwanych w tym samym czasie na koncie.</span><span class="sxs-lookup"><span data-stu-id="53384-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="53384-122">Jeśli nie jest określona, domyślnie przyjmowana jest wartość 3.</span><span class="sxs-lookup"><span data-stu-id="53384-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="53384-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="53384-123">-Name</span></span>
<span data-ttu-id="53384-124">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="53384-124">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53384-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="53384-125">-QueryStoreRetention</span></span>
<span data-ttu-id="53384-126">Opcjonalna liczba dni zachowywania metadanych zadania.</span><span class="sxs-lookup"><span data-stu-id="53384-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="53384-127">Jeśli nie podano, wartość domyślna to 30 dni.</span><span class="sxs-lookup"><span data-stu-id="53384-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="53384-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53384-128">-ResourceGroupName</span></span>
<span data-ttu-id="53384-129">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="53384-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="53384-130">Aby utworzyć grupę zasobów, użyj polecenia cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="53384-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="53384-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="53384-131">-Tag</span></span>
<span data-ttu-id="53384-132">Ciąg znaczników ciągów skojarzonych z tym kontem</span><span class="sxs-lookup"><span data-stu-id="53384-132">A string,string dictionary of tags associated with this account</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53384-133">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="53384-133">-Tier</span></span>
<span data-ttu-id="53384-134">Pożądana warstwa zobowiązań do użycia dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="53384-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="53384-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53384-135">CommonParameters</span></span>
<span data-ttu-id="53384-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53384-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53384-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53384-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53384-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53384-138">INPUTS</span></span>

### <span data-ttu-id="53384-139">System. String</span><span class="sxs-lookup"><span data-stu-id="53384-139">System.String</span></span>

### <span data-ttu-id="53384-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="53384-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="53384-141">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="53384-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="53384-142">System. Nullable "1 [[Microsoft. Azure. Management. datalake. Analytics. models., Microsoft. Azure. Management. datalake. Analytics, wersja = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="53384-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="53384-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53384-143">OUTPUTS</span></span>

### <span data-ttu-id="53384-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="53384-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="53384-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53384-145">NOTES</span></span>

## <span data-ttu-id="53384-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53384-146">RELATED LINKS</span></span>

[<span data-ttu-id="53384-147">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="53384-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="53384-148">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="53384-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="53384-149">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="53384-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="53384-150">Test — AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="53384-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


