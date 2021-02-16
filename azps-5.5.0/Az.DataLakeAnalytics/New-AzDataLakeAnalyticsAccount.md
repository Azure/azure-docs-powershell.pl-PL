---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: c79665a6ed21309a7a702d9fd5bc5e876aa2ff21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238240"
---
# <span data-ttu-id="44a72-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="44a72-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="44a72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44a72-102">SYNOPSIS</span></span>
<span data-ttu-id="44a72-103">Tworzy konto usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="44a72-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="44a72-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="44a72-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44a72-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="44a72-105">DESCRIPTION</span></span>
<span data-ttu-id="44a72-106">Polecenie **cmdlet New-AzDataLakeAnalyticsAccount** tworzy konto usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="44a72-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="44a72-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="44a72-107">EXAMPLES</span></span>

### <span data-ttu-id="44a72-108">Przykład 1. Tworzenie konta usługi Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="44a72-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="44a72-109">To polecenie tworzy konto usługi Data Lake Analytics o nazwie ContosoAdlAccount, które korzysta ze sklepu danych ContosoAdlStore, w grupie zasobów o nazwie ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="44a72-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="44a72-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44a72-110">PARAMETERS</span></span>

### <span data-ttu-id="44a72-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="44a72-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="44a72-112">Określa nazwę konta magazynu Data Lake Store, które ma być ustawiane jako domyślne źródło danych.</span><span class="sxs-lookup"><span data-stu-id="44a72-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="44a72-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44a72-113">-DefaultProfile</span></span>
<span data-ttu-id="44a72-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="44a72-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44a72-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="44a72-115">-Location</span></span>
<span data-ttu-id="44a72-116">Określa lokalizację, w której ma być tworzyć konto Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="44a72-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="44a72-117">Obecnie obsługiwany jest tylko region Wschód STANÓW Zjednoczonych 2.</span><span class="sxs-lookup"><span data-stu-id="44a72-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="44a72-118">- MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="44a72-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="44a72-119">Opcjonalne maksymalna liczba obsługiwanych jednostek analizy dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="44a72-119">The optional maximum supported analytics units for this account.</span></span>

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

### <span data-ttu-id="44a72-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="44a72-120">-MaxJobCount</span></span>
<span data-ttu-id="44a72-121">Opcjonalne maksymalna liczba obsługiwanych zadań uruchomionych w tym samym czasie w ramach konta.</span><span class="sxs-lookup"><span data-stu-id="44a72-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="44a72-122">Jeśli nie zostanie określony, wartość domyślna to 3.</span><span class="sxs-lookup"><span data-stu-id="44a72-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="44a72-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="44a72-123">-Name</span></span>
<span data-ttu-id="44a72-124">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="44a72-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="44a72-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="44a72-125">-QueryStoreRetention</span></span>
<span data-ttu-id="44a72-126">Opcjonalna liczba dni zachowywania metadanych zadania.</span><span class="sxs-lookup"><span data-stu-id="44a72-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="44a72-127">Jeśli nie zostanie określona, wartością domyślną jest 30 dni.</span><span class="sxs-lookup"><span data-stu-id="44a72-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="44a72-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44a72-128">-ResourceGroupName</span></span>
<span data-ttu-id="44a72-129">Określa nazwę grupy zasobów dla konta Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="44a72-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="44a72-130">Aby utworzyć grupę zasobów, użyj New-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44a72-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="44a72-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="44a72-131">-Tag</span></span>
<span data-ttu-id="44a72-132">A string,string dictionary of tags associated with this account</span><span class="sxs-lookup"><span data-stu-id="44a72-132">A string,string dictionary of tags associated with this account</span></span>

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

### <span data-ttu-id="44a72-133">- Warstwa</span><span class="sxs-lookup"><span data-stu-id="44a72-133">-Tier</span></span>
<span data-ttu-id="44a72-134">Żądana warstwa zobowiązania dla tego konta do użycia.</span><span class="sxs-lookup"><span data-stu-id="44a72-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="44a72-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44a72-135">CommonParameters</span></span>
<span data-ttu-id="44a72-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44a72-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44a72-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44a72-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44a72-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44a72-138">INPUTS</span></span>

### <span data-ttu-id="44a72-139">System.String</span><span class="sxs-lookup"><span data-stu-id="44a72-139">System.String</span></span>

### <span data-ttu-id="44a72-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="44a72-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="44a72-141">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="44a72-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="44a72-142">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="44a72-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="44a72-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44a72-143">OUTPUTS</span></span>

### <span data-ttu-id="44a72-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="44a72-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="44a72-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="44a72-145">NOTES</span></span>

## <span data-ttu-id="44a72-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44a72-146">RELATED LINKS</span></span>

[<span data-ttu-id="44a72-147">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="44a72-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="44a72-148">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="44a72-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="44a72-149">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="44a72-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="44a72-150">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="44a72-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


