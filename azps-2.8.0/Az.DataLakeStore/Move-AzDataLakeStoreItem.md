---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: 8a8cc4d60bfba73b9cbcc9d323b063bff87f8a2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705794"
---
# <span data-ttu-id="da170-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da170-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="da170-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da170-102">SYNOPSIS</span></span>
<span data-ttu-id="da170-103">Przenosi plik lub folder w usłudze Data Lake Store lub zmienia jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="da170-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="da170-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da170-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da170-105">Opis</span><span class="sxs-lookup"><span data-stu-id="da170-105">DESCRIPTION</span></span>
<span data-ttu-id="da170-106">Polecenie cmdlet **Move-AzDataLakeStoreItem** przenosi lub zmienia nazwę pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="da170-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="da170-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da170-107">EXAMPLES</span></span>

### <span data-ttu-id="da170-108">Przykład 1: Przenoszenie elementu i zmienianie jego nazwy</span><span class="sxs-lookup"><span data-stu-id="da170-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="da170-109">To polecenie zmienia nazwę elementu File.txt na RenamedFile.txt i przenosi go do innego folderu.</span><span class="sxs-lookup"><span data-stu-id="da170-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="da170-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da170-110">PARAMETERS</span></span>

### <span data-ttu-id="da170-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="da170-111">-Account</span></span>
<span data-ttu-id="da170-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="da170-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="da170-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da170-113">-DefaultProfile</span></span>
<span data-ttu-id="da170-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da170-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da170-115">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="da170-115">-Destination</span></span>
<span data-ttu-id="da170-116">Określa ścieżkę usługi Data Lake Store, do której ma zostać przeniesiony element, począwszy od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="da170-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da170-117">-Force</span><span class="sxs-lookup"><span data-stu-id="da170-117">-Force</span></span>
<span data-ttu-id="da170-118">Wskazuje, że ta operacja może spowodować zastąpienie pliku docelowego, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="da170-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da170-119">-Path</span><span class="sxs-lookup"><span data-stu-id="da170-119">-Path</span></span>
<span data-ttu-id="da170-120">Określa ścieżkę elementu Data Lake Store do przeniesienia lub zmiany nazwy, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="da170-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da170-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da170-121">-Confirm</span></span>
<span data-ttu-id="da170-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da170-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da170-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da170-123">-WhatIf</span></span>
<span data-ttu-id="da170-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da170-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da170-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da170-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da170-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da170-126">CommonParameters</span></span>
<span data-ttu-id="da170-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da170-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da170-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da170-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da170-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da170-129">INPUTS</span></span>

### <span data-ttu-id="da170-130">System. String</span><span class="sxs-lookup"><span data-stu-id="da170-130">System.String</span></span>

### <span data-ttu-id="da170-131">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="da170-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="da170-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="da170-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="da170-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da170-133">OUTPUTS</span></span>

### <span data-ttu-id="da170-134">System. String</span><span class="sxs-lookup"><span data-stu-id="da170-134">System.String</span></span>

## <span data-ttu-id="da170-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da170-135">NOTES</span></span>

## <span data-ttu-id="da170-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da170-136">RELATED LINKS</span></span>

[<span data-ttu-id="da170-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da170-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="da170-138">Eksportowanie — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da170-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="da170-139">Import — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da170-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="da170-140">Nowe — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da170-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="da170-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da170-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="da170-142">Test — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da170-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


