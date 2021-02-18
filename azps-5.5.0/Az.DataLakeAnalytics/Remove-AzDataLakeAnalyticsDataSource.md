---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: dfdd338fd5b49813d17e089755b419605761af3a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180923"
---
# <span data-ttu-id="51e02-101">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="51e02-101">Remove-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="51e02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51e02-102">SYNOPSIS</span></span>
<span data-ttu-id="51e02-103">Usuwa źródło danych z konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="51e02-103">Removes a data source from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="51e02-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="51e02-104">SYNTAX</span></span>

### <span data-ttu-id="51e02-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="51e02-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51e02-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="51e02-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51e02-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="51e02-107">DESCRIPTION</span></span>
<span data-ttu-id="51e02-108">Polecenie **cmdlet Remove-AzDataLakeAnalyticsDataSource** usuwa źródło danych z konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="51e02-108">The **Remove-AzDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="51e02-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="51e02-109">EXAMPLES</span></span>

### <span data-ttu-id="51e02-110">Przykład 1. Usuwanie źródła danych</span><span class="sxs-lookup"><span data-stu-id="51e02-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="51e02-111">To polecenie usuwa źródło danych o nazwie AzureStorage01 z konta o nazwie ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="51e02-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="51e02-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51e02-112">PARAMETERS</span></span>

### <span data-ttu-id="51e02-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="51e02-113">-Account</span></span>
<span data-ttu-id="51e02-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="51e02-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="51e02-115">— obiekt blob</span><span class="sxs-lookup"><span data-stu-id="51e02-115">-Blob</span></span>
<span data-ttu-id="51e02-116">Określa nazwę konta magazynu usługi AzureBlob do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="51e02-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

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

### <span data-ttu-id="51e02-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="51e02-117">-DataLakeStore</span></span>
<span data-ttu-id="51e02-118">Określa nazwę konta azureData Lake Store do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="51e02-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

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

### <span data-ttu-id="51e02-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e02-119">-DefaultProfile</span></span>
<span data-ttu-id="51e02-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="51e02-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51e02-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="51e02-121">-Force</span></span>
<span data-ttu-id="51e02-122">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="51e02-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="51e02-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51e02-123">-PassThru</span></span>
<span data-ttu-id="51e02-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="51e02-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="51e02-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="51e02-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="51e02-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51e02-126">-ResourceGroupName</span></span>
<span data-ttu-id="51e02-127">Określa nazwę grupy zasobów dla konta Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="51e02-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="51e02-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51e02-128">-Confirm</span></span>
<span data-ttu-id="51e02-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="51e02-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51e02-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51e02-130">-WhatIf</span></span>
<span data-ttu-id="51e02-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51e02-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51e02-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="51e02-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51e02-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e02-133">CommonParameters</span></span>
<span data-ttu-id="51e02-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51e02-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e02-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51e02-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e02-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51e02-136">INPUTS</span></span>

### <span data-ttu-id="51e02-137">System.String</span><span class="sxs-lookup"><span data-stu-id="51e02-137">System.String</span></span>

## <span data-ttu-id="51e02-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51e02-138">OUTPUTS</span></span>

### <span data-ttu-id="51e02-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="51e02-139">System.Boolean</span></span>

## <span data-ttu-id="51e02-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="51e02-140">NOTES</span></span>

## <span data-ttu-id="51e02-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51e02-141">RELATED LINKS</span></span>

[<span data-ttu-id="51e02-142">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="51e02-142">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="51e02-143">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="51e02-143">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


