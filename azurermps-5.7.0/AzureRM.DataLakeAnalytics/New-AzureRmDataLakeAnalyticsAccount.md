---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 36bf1bbfeb0c44189f5eeeaa0988d0314980e48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542660"
---
# <span data-ttu-id="62929-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="62929-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="62929-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62929-102">SYNOPSIS</span></span>
<span data-ttu-id="62929-103">Tworzy konto Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="62929-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62929-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62929-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62929-105">Opis</span><span class="sxs-lookup"><span data-stu-id="62929-105">DESCRIPTION</span></span>
<span data-ttu-id="62929-106">Polecenie cmdlet **New-AzureRmDataLakeAnalyticsAccount** tworzy konto usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="62929-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="62929-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62929-107">EXAMPLES</span></span>

### <span data-ttu-id="62929-108">Przykład 1: Tworzenie konta danych w usłudze Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="62929-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="62929-109">To polecenie tworzy konto usługi Data Lake Analytics o nazwie ContosoAdlAccount, w którym jest używany magazyn danych ContosoAdlStore, w grupie zasobów o nazwie ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="62929-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="62929-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62929-110">PARAMETERS</span></span>

### <span data-ttu-id="62929-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="62929-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="62929-112">Określa nazwę konta usługi Data Lake Store, które ma zostać ustawione jako domyślne źródło danych.</span><span class="sxs-lookup"><span data-stu-id="62929-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62929-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62929-113">-DefaultProfile</span></span>
<span data-ttu-id="62929-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="62929-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62929-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="62929-115">-Location</span></span>
<span data-ttu-id="62929-116">Określa lokalizację, w której ma zostać utworzone konto usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="62929-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="62929-117">Obecnie w tej chwili jest obsługiwana tylko wschód amerykańska 2.</span><span class="sxs-lookup"><span data-stu-id="62929-117">Only East US 2 is supported at this time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62929-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="62929-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="62929-119">Opcjonalna Maksymalna obsługiwana jednostka analityczna dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="62929-119">The optional maximum supported analytics units for this account.</span></span>

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

### <span data-ttu-id="62929-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="62929-120">-MaxJobCount</span></span>
<span data-ttu-id="62929-121">Opcjonalna Maksymalna liczba zadań obsługiwanych w tym samym czasie na koncie.</span><span class="sxs-lookup"><span data-stu-id="62929-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="62929-122">Jeśli nie jest określona, domyślnie przyjmowana jest wartość 3.</span><span class="sxs-lookup"><span data-stu-id="62929-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="62929-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="62929-123">-Name</span></span>
<span data-ttu-id="62929-124">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="62929-124">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62929-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="62929-125">-QueryStoreRetention</span></span>
<span data-ttu-id="62929-126">Opcjonalna liczba dni zachowywania metadanych zadania.</span><span class="sxs-lookup"><span data-stu-id="62929-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="62929-127">Jeśli nie podano, wartość domyślna to 30 dni.</span><span class="sxs-lookup"><span data-stu-id="62929-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="62929-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62929-128">-ResourceGroupName</span></span>
<span data-ttu-id="62929-129">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="62929-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="62929-130">Aby utworzyć grupę zasobów, użyj polecenia cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="62929-130">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="62929-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="62929-131">-Tag</span></span>
<span data-ttu-id="62929-132">Ciąg znaczników ciągów skojarzonych z tym kontem</span><span class="sxs-lookup"><span data-stu-id="62929-132">A string,string dictionary of tags associated with this account</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62929-133">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="62929-133">-Tier</span></span>
<span data-ttu-id="62929-134">Pożądana warstwa zobowiązań do użycia dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="62929-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="62929-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62929-135">CommonParameters</span></span>
<span data-ttu-id="62929-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62929-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62929-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62929-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62929-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62929-138">INPUTS</span></span>

### <span data-ttu-id="62929-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="62929-139">None</span></span>
<span data-ttu-id="62929-140">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="62929-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62929-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62929-141">OUTPUTS</span></span>

### <span data-ttu-id="62929-142">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="62929-142">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="62929-143">Szczegóły nowo utworzonego konta.</span><span class="sxs-lookup"><span data-stu-id="62929-143">The details of the newly created account.</span></span>

## <span data-ttu-id="62929-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62929-144">NOTES</span></span>

## <span data-ttu-id="62929-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62929-145">RELATED LINKS</span></span>

[<span data-ttu-id="62929-146">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="62929-146">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="62929-147">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="62929-147">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="62929-148">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="62929-148">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="62929-149">Test — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="62929-149">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


