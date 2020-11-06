---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/move-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 15c516e1d54b6e706176ceb28a1974e848945c47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541716"
---
# <span data-ttu-id="f64cd-101">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f64cd-101">Move-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="f64cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f64cd-102">SYNOPSIS</span></span>
<span data-ttu-id="f64cd-103">Przenosi plik lub folder w usłudze Data Lake Store lub zmienia jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="f64cd-103">Moves or renames a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f64cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f64cd-104">SYNTAX</span></span>

```
Move-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f64cd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f64cd-105">DESCRIPTION</span></span>
<span data-ttu-id="f64cd-106">Polecenie cmdlet **Move-AzureRmDataLakeStoreItem** przenosi lub zmienia nazwę pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f64cd-106">The **Move-AzureRmDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f64cd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f64cd-107">EXAMPLES</span></span>

### <span data-ttu-id="f64cd-108">Przykład 1: Przenoszenie elementu i zmienianie jego nazwy</span><span class="sxs-lookup"><span data-stu-id="f64cd-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="f64cd-109">To polecenie zmienia nazwę elementu File.txt na RenamedFile.txt i przenosi go do innego folderu.</span><span class="sxs-lookup"><span data-stu-id="f64cd-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="f64cd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f64cd-110">PARAMETERS</span></span>

### <span data-ttu-id="f64cd-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="f64cd-111">-Account</span></span>
<span data-ttu-id="f64cd-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f64cd-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f64cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f64cd-113">-DefaultProfile</span></span>
<span data-ttu-id="f64cd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f64cd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f64cd-115">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="f64cd-115">-Destination</span></span>
<span data-ttu-id="f64cd-116">Określa ścieżkę usługi Data Lake Store, do której ma zostać przeniesiony element, począwszy od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="f64cd-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f64cd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f64cd-117">-Force</span></span>
<span data-ttu-id="f64cd-118">Wskazuje, że ta operacja może spowodować zastąpienie pliku docelowego, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="f64cd-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="f64cd-119">-Path</span><span class="sxs-lookup"><span data-stu-id="f64cd-119">-Path</span></span>
<span data-ttu-id="f64cd-120">Określa ścieżkę elementu Data Lake Store do przeniesienia lub zmiany nazwy, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="f64cd-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f64cd-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f64cd-121">-Confirm</span></span>
<span data-ttu-id="f64cd-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f64cd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f64cd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f64cd-123">-WhatIf</span></span>
<span data-ttu-id="f64cd-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f64cd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f64cd-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f64cd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f64cd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f64cd-126">CommonParameters</span></span>
<span data-ttu-id="f64cd-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f64cd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f64cd-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f64cd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f64cd-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f64cd-129">INPUTS</span></span>

### <span data-ttu-id="f64cd-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f64cd-130">System.String</span></span>

### <span data-ttu-id="f64cd-131">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="f64cd-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f64cd-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f64cd-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f64cd-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f64cd-133">OUTPUTS</span></span>

### <span data-ttu-id="f64cd-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f64cd-134">System.String</span></span>
<span data-ttu-id="f64cd-135">Pełna ścieżka do przenoszonego pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="f64cd-135">The full path to the moved file or folder.</span></span>

## <span data-ttu-id="f64cd-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f64cd-136">NOTES</span></span>

## <span data-ttu-id="f64cd-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f64cd-137">RELATED LINKS</span></span>

[<span data-ttu-id="f64cd-138">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f64cd-138">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f64cd-139">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f64cd-139">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f64cd-140">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f64cd-140">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f64cd-141">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f64cd-141">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f64cd-142">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f64cd-142">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f64cd-143">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f64cd-143">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


