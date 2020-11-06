---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 7c35821cbaf75a616ab1b9b8bbc2db9fc2a96794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553336"
---
# <span data-ttu-id="50d29-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50d29-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="50d29-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50d29-102">SYNOPSIS</span></span>
<span data-ttu-id="50d29-103">Tworzy konto Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="50d29-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50d29-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50d29-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tags] <Hashtable>] [-MaxDegreeOfParallelism <Int32>]
 [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50d29-105">Opis</span><span class="sxs-lookup"><span data-stu-id="50d29-105">DESCRIPTION</span></span>
<span data-ttu-id="50d29-106">Polecenie cmdlet **New-AzureRmDataLakeAnalyticsAccount** tworzy konto usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="50d29-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="50d29-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50d29-107">EXAMPLES</span></span>

### <span data-ttu-id="50d29-108">Przykład 1: Tworzenie konta danych w usłudze Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="50d29-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="50d29-109">To polecenie tworzy konto usługi Data Lake Analytics o nazwie ContosoAdlAccount, w którym jest używany magazyn danych ContosoAdlStore, w grupie zasobów o nazwie ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="50d29-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="50d29-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50d29-110">PARAMETERS</span></span>

### <span data-ttu-id="50d29-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50d29-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="50d29-112">Określa nazwę konta usługi Data Lake Store, które ma zostać ustawione jako domyślne źródło danych.</span><span class="sxs-lookup"><span data-stu-id="50d29-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="50d29-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="50d29-113">-Location</span></span>
<span data-ttu-id="50d29-114">Określa lokalizację, w której ma zostać utworzone konto usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="50d29-114">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="50d29-115">Obecnie w tej chwili jest obsługiwana tylko wschód amerykańska 2.</span><span class="sxs-lookup"><span data-stu-id="50d29-115">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="50d29-116">-MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="50d29-116">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="50d29-117">Opcjonalny maksymalny obsługiwany stopień równoległości dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="50d29-117">The optional maximum supported degree of parallelism for this account.</span></span> <span data-ttu-id="50d29-118">Jeśli nie jest określona, wartość domyślna to 30</span><span class="sxs-lookup"><span data-stu-id="50d29-118">If none is specified, defaults to 30</span></span>

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

### <span data-ttu-id="50d29-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="50d29-119">-MaxJobCount</span></span>
<span data-ttu-id="50d29-120">Opcjonalna Maksymalna liczba zadań obsługiwanych w tym samym czasie na koncie.</span><span class="sxs-lookup"><span data-stu-id="50d29-120">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="50d29-121">Jeśli nie jest określona, domyślnie przyjmowana jest wartość 3.</span><span class="sxs-lookup"><span data-stu-id="50d29-121">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="50d29-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="50d29-122">-Name</span></span>
<span data-ttu-id="50d29-123">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="50d29-123">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="50d29-124">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="50d29-124">-QueryStoreRetention</span></span>
<span data-ttu-id="50d29-125">Opcjonalna liczba dni zachowywania metadanych zadania.</span><span class="sxs-lookup"><span data-stu-id="50d29-125">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="50d29-126">Jeśli nie podano, wartość domyślna to 30 dni.</span><span class="sxs-lookup"><span data-stu-id="50d29-126">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="50d29-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50d29-127">-ResourceGroupName</span></span>
<span data-ttu-id="50d29-128">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="50d29-128">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="50d29-129">Aby utworzyć grupę zasobów, użyj polecenia cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="50d29-129">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="50d29-130">-Tagi</span><span class="sxs-lookup"><span data-stu-id="50d29-130">-Tags</span></span>
<span data-ttu-id="50d29-131">Określa pary klucz-wartość, które mogą być używane do identyfikowania konta usługi Data Lake Analytics wśród innych zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="50d29-131">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

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

### <span data-ttu-id="50d29-132">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="50d29-132">-Tier</span></span>
<span data-ttu-id="50d29-133">Pożądana warstwa zobowiązań do użycia dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="50d29-133">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="50d29-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50d29-134">-DefaultProfile</span></span>
<span data-ttu-id="50d29-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50d29-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50d29-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d29-136">CommonParameters</span></span>
<span data-ttu-id="50d29-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50d29-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d29-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50d29-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d29-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50d29-139">INPUTS</span></span>

## <span data-ttu-id="50d29-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50d29-140">OUTPUTS</span></span>

### <span data-ttu-id="50d29-141">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50d29-141">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="50d29-142">Szczegóły nowo utworzonego konta.</span><span class="sxs-lookup"><span data-stu-id="50d29-142">The details of the newly created account.</span></span>

## <span data-ttu-id="50d29-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50d29-143">NOTES</span></span>

## <span data-ttu-id="50d29-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50d29-144">RELATED LINKS</span></span>

[<span data-ttu-id="50d29-145">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50d29-145">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="50d29-146">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50d29-146">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="50d29-147">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50d29-147">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="50d29-148">Test — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50d29-148">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


