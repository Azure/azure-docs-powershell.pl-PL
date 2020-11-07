---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 9b0e4b5da6ecd2877bab5860179cbaed80f43911
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718242"
---
# <span data-ttu-id="208a1-101">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="208a1-101">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="208a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="208a1-102">SYNOPSIS</span></span>
<span data-ttu-id="208a1-103">Usuwa źródło danych z konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="208a1-103">Removes a data source from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="208a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="208a1-104">SYNTAX</span></span>

### <span data-ttu-id="208a1-105">Usuwanie konta programu Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="208a1-105">Remove a Data Lake storage account</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="208a1-106">Usuwanie konta magazynu obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="208a1-106">Remove a Blob storage account</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="208a1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="208a1-107">DESCRIPTION</span></span>
<span data-ttu-id="208a1-108">Polecenie cmdlet **Remove-AzureRmDataLakeAnalyticsDataSource** umożliwia usunięcie źródła danych z konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="208a1-108">The **Remove-AzureRmDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="208a1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="208a1-109">EXAMPLES</span></span>

### <span data-ttu-id="208a1-110">Przykład 1: Usuwanie źródła danych</span><span class="sxs-lookup"><span data-stu-id="208a1-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="208a1-111">To polecenie usuwa źródło danych o nazwie AzureStorage01 z konta o nazwie ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="208a1-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="208a1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="208a1-112">PARAMETERS</span></span>

### <span data-ttu-id="208a1-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="208a1-113">-Account</span></span>
<span data-ttu-id="208a1-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="208a1-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-115">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="208a1-115">-Blob</span></span>
<span data-ttu-id="208a1-116">Określa nazwę konta magazynu usługi AzureBlob, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="208a1-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="208a1-117">-DataLakeStore</span></span>
<span data-ttu-id="208a1-118">Określa nazwę konta usługi AzureData Lake Store, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="208a1-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Data Lake storage account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="208a1-119">-Force</span></span>
<span data-ttu-id="208a1-120">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="208a1-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="208a1-121">-PassThru</span></span>
<span data-ttu-id="208a1-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="208a1-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="208a1-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="208a1-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="208a1-124">-ResourceGroupName</span></span>
<span data-ttu-id="208a1-125">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="208a1-125">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="208a1-126">-Confirm</span></span>
<span data-ttu-id="208a1-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="208a1-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="208a1-128">-WhatIf</span></span>
<span data-ttu-id="208a1-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="208a1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="208a1-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="208a1-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="208a1-131">-DefaultProfile</span></span>
<span data-ttu-id="208a1-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="208a1-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="208a1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="208a1-133">CommonParameters</span></span>
<span data-ttu-id="208a1-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="208a1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="208a1-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="208a1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="208a1-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="208a1-136">INPUTS</span></span>

## <span data-ttu-id="208a1-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="208a1-137">OUTPUTS</span></span>

### <span data-ttu-id="208a1-138">logiczną</span><span class="sxs-lookup"><span data-stu-id="208a1-138">bool</span></span>
<span data-ttu-id="208a1-139">Jeśli PassThru jest określony, zwraca wartość Prawda po wykonaniu operacji.</span><span class="sxs-lookup"><span data-stu-id="208a1-139">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="208a1-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="208a1-140">NOTES</span></span>

## <span data-ttu-id="208a1-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="208a1-141">RELATED LINKS</span></span>

[<span data-ttu-id="208a1-142">Dodaj-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="208a1-142">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="208a1-143">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="208a1-143">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


