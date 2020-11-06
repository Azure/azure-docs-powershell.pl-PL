---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 2707100452f9b64c093b4ae52c724e09f6cfe6e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544407"
---
# <span data-ttu-id="cab65-101">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="cab65-101">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="cab65-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cab65-102">SYNOPSIS</span></span>
<span data-ttu-id="cab65-103">Usuwa źródło danych z konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cab65-103">Removes a data source from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cab65-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cab65-104">SYNTAX</span></span>

### <span data-ttu-id="cab65-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cab65-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cab65-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cab65-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cab65-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cab65-107">DESCRIPTION</span></span>
<span data-ttu-id="cab65-108">Polecenie cmdlet **Remove-AzureRmDataLakeAnalyticsDataSource** umożliwia usunięcie źródła danych z konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cab65-108">The **Remove-AzureRmDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="cab65-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cab65-109">EXAMPLES</span></span>

### <span data-ttu-id="cab65-110">Przykład 1: Usuwanie źródła danych</span><span class="sxs-lookup"><span data-stu-id="cab65-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="cab65-111">To polecenie usuwa źródło danych o nazwie AzureStorage01 z konta o nazwie ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="cab65-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="cab65-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cab65-112">PARAMETERS</span></span>

### <span data-ttu-id="cab65-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="cab65-113">-Account</span></span>
<span data-ttu-id="cab65-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cab65-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab65-115">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="cab65-115">-Blob</span></span>
<span data-ttu-id="cab65-116">Określa nazwę konta magazynu usługi AzureBlob, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="cab65-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab65-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cab65-117">-DataLakeStore</span></span>
<span data-ttu-id="cab65-118">Określa nazwę konta usługi AzureData Lake Store, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="cab65-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDataLakeStorageAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab65-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab65-119">-DefaultProfile</span></span>
<span data-ttu-id="cab65-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cab65-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cab65-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cab65-121">-Force</span></span>
<span data-ttu-id="cab65-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cab65-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab65-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cab65-123">-PassThru</span></span>
<span data-ttu-id="cab65-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="cab65-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cab65-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="cab65-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab65-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cab65-126">-ResourceGroupName</span></span>
<span data-ttu-id="cab65-127">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cab65-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab65-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cab65-128">-Confirm</span></span>
<span data-ttu-id="cab65-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cab65-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab65-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cab65-130">-WhatIf</span></span>
<span data-ttu-id="cab65-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cab65-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cab65-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cab65-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab65-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab65-133">CommonParameters</span></span>
<span data-ttu-id="cab65-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cab65-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab65-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cab65-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab65-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cab65-136">INPUTS</span></span>

### <span data-ttu-id="cab65-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cab65-137">None</span></span>
<span data-ttu-id="cab65-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="cab65-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cab65-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cab65-139">OUTPUTS</span></span>

### <span data-ttu-id="cab65-140">logiczną</span><span class="sxs-lookup"><span data-stu-id="cab65-140">bool</span></span>
<span data-ttu-id="cab65-141">Jeśli PassThru jest określony, zwraca wartość Prawda po wykonaniu operacji.</span><span class="sxs-lookup"><span data-stu-id="cab65-141">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="cab65-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cab65-142">NOTES</span></span>

## <span data-ttu-id="cab65-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cab65-143">RELATED LINKS</span></span>

[<span data-ttu-id="cab65-144">Dodaj-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="cab65-144">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="cab65-145">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="cab65-145">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


