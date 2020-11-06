---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 2fec19864e9d13e4b0e4ede1d351a08427e95357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551287"
---
# <span data-ttu-id="eabbb-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="eabbb-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="eabbb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eabbb-102">SYNOPSIS</span></span>
<span data-ttu-id="eabbb-103">Tworzy konto Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="eabbb-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eabbb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eabbb-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eabbb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eabbb-105">DESCRIPTION</span></span>
<span data-ttu-id="eabbb-106">Polecenie cmdlet **New-AzureRmDataLakeAnalyticsAccount** tworzy konto usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="eabbb-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="eabbb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eabbb-107">EXAMPLES</span></span>

### <span data-ttu-id="eabbb-108">Przykład 1: Tworzenie konta danych w usłudze Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="eabbb-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="eabbb-109">To polecenie tworzy konto usługi Data Lake Analytics o nazwie ContosoAdlAccount, w którym jest używany magazyn danych ContosoAdlStore, w grupie zasobów o nazwie ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="eabbb-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="eabbb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eabbb-110">PARAMETERS</span></span>

### <span data-ttu-id="eabbb-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eabbb-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="eabbb-112">Określa nazwę konta usługi Data Lake Store, które ma zostać ustawione jako domyślne źródło danych.</span><span class="sxs-lookup"><span data-stu-id="eabbb-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="eabbb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eabbb-113">-DefaultProfile</span></span>
<span data-ttu-id="eabbb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="eabbb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eabbb-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="eabbb-115">-Location</span></span>
<span data-ttu-id="eabbb-116">Określa lokalizację, w której ma zostać utworzone konto usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="eabbb-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="eabbb-117">Obecnie w tej chwili jest obsługiwana tylko wschód amerykańska 2.</span><span class="sxs-lookup"><span data-stu-id="eabbb-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="eabbb-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="eabbb-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="eabbb-119">Opcjonalna Maksymalna obsługiwana jednostka analityczna dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="eabbb-119">The optional maximum supported analytics units for this account.</span></span>

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

### <span data-ttu-id="eabbb-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="eabbb-120">-MaxJobCount</span></span>
<span data-ttu-id="eabbb-121">Opcjonalna Maksymalna liczba zadań obsługiwanych w tym samym czasie na koncie.</span><span class="sxs-lookup"><span data-stu-id="eabbb-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="eabbb-122">Jeśli nie jest określona, domyślnie przyjmowana jest wartość 3.</span><span class="sxs-lookup"><span data-stu-id="eabbb-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="eabbb-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eabbb-123">-Name</span></span>
<span data-ttu-id="eabbb-124">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="eabbb-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="eabbb-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="eabbb-125">-QueryStoreRetention</span></span>
<span data-ttu-id="eabbb-126">Opcjonalna liczba dni zachowywania metadanych zadania.</span><span class="sxs-lookup"><span data-stu-id="eabbb-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="eabbb-127">Jeśli nie podano, wartość domyślna to 30 dni.</span><span class="sxs-lookup"><span data-stu-id="eabbb-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="eabbb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eabbb-128">-ResourceGroupName</span></span>
<span data-ttu-id="eabbb-129">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="eabbb-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="eabbb-130">Aby utworzyć grupę zasobów, użyj polecenia cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="eabbb-130">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="eabbb-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="eabbb-131">-Tag</span></span>
<span data-ttu-id="eabbb-132">Ciąg znaczników ciągów skojarzonych z tym kontem</span><span class="sxs-lookup"><span data-stu-id="eabbb-132">A string,string dictionary of tags associated with this account</span></span>

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

### <span data-ttu-id="eabbb-133">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="eabbb-133">-Tier</span></span>
<span data-ttu-id="eabbb-134">Pożądana warstwa zobowiązań do użycia dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="eabbb-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="eabbb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eabbb-135">CommonParameters</span></span>
<span data-ttu-id="eabbb-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eabbb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eabbb-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eabbb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eabbb-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eabbb-138">INPUTS</span></span>

### <span data-ttu-id="eabbb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="eabbb-139">System.String</span></span>

### <span data-ttu-id="eabbb-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="eabbb-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="eabbb-141">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="eabbb-141">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="eabbb-142">System. Nullable "1 [[Microsoft. Azure. Management. datalake. Analytics. models., Microsoft. Azure. Management. datalake. Analytics, wersja = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="eabbb-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="eabbb-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eabbb-143">OUTPUTS</span></span>

### <span data-ttu-id="eabbb-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="eabbb-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="eabbb-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eabbb-145">NOTES</span></span>

## <span data-ttu-id="eabbb-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eabbb-146">RELATED LINKS</span></span>

[<span data-ttu-id="eabbb-147">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="eabbb-147">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="eabbb-148">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="eabbb-148">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="eabbb-149">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="eabbb-149">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="eabbb-150">Test — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="eabbb-150">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


