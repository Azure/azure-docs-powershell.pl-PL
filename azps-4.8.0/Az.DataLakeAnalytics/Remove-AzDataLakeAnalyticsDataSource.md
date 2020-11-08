---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: dfdd338fd5b49813d17e089755b419605761af3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064165"
---
# <span data-ttu-id="9f47c-101">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="9f47c-101">Remove-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="9f47c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9f47c-102">SYNOPSIS</span></span>
<span data-ttu-id="9f47c-103">Usuwa źródło danych z konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9f47c-103">Removes a data source from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="9f47c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9f47c-104">SYNTAX</span></span>

### <span data-ttu-id="9f47c-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9f47c-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f47c-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9f47c-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f47c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9f47c-107">DESCRIPTION</span></span>
<span data-ttu-id="9f47c-108">Polecenie cmdlet **Remove-AzDataLakeAnalyticsDataSource** umożliwia usunięcie źródła danych z konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9f47c-108">The **Remove-AzDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="9f47c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9f47c-109">EXAMPLES</span></span>

### <span data-ttu-id="9f47c-110">Przykład 1: Usuwanie źródła danych</span><span class="sxs-lookup"><span data-stu-id="9f47c-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="9f47c-111">To polecenie usuwa źródło danych o nazwie AzureStorage01 z konta o nazwie ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="9f47c-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="9f47c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f47c-112">PARAMETERS</span></span>

### <span data-ttu-id="9f47c-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="9f47c-113">-Account</span></span>
<span data-ttu-id="9f47c-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9f47c-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="9f47c-115">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="9f47c-115">-Blob</span></span>
<span data-ttu-id="9f47c-116">Określa nazwę konta magazynu usługi AzureBlob, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="9f47c-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f47c-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9f47c-117">-DataLakeStore</span></span>
<span data-ttu-id="9f47c-118">Określa nazwę konta usługi AzureData Lake Store, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="9f47c-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f47c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f47c-119">-DefaultProfile</span></span>
<span data-ttu-id="9f47c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9f47c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f47c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9f47c-121">-Force</span></span>
<span data-ttu-id="9f47c-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9f47c-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9f47c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f47c-123">-PassThru</span></span>
<span data-ttu-id="9f47c-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="9f47c-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9f47c-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="9f47c-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9f47c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f47c-126">-ResourceGroupName</span></span>
<span data-ttu-id="9f47c-127">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9f47c-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="9f47c-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9f47c-128">-Confirm</span></span>
<span data-ttu-id="9f47c-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f47c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f47c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f47c-130">-WhatIf</span></span>
<span data-ttu-id="9f47c-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f47c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f47c-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9f47c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f47c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f47c-133">CommonParameters</span></span>
<span data-ttu-id="9f47c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f47c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f47c-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f47c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f47c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f47c-136">INPUTS</span></span>

### <span data-ttu-id="9f47c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9f47c-137">System.String</span></span>

## <span data-ttu-id="9f47c-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9f47c-138">OUTPUTS</span></span>

### <span data-ttu-id="9f47c-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f47c-139">System.Boolean</span></span>

## <span data-ttu-id="9f47c-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9f47c-140">NOTES</span></span>

## <span data-ttu-id="9f47c-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f47c-141">RELATED LINKS</span></span>

[<span data-ttu-id="9f47c-142">Dodaj-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="9f47c-142">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="9f47c-143">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="9f47c-143">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


