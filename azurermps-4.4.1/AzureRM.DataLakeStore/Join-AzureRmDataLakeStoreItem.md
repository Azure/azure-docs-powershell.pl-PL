---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 1f09d1da5ab4ad88ff16be56affaa582ad1e24d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550015"
---
# <span data-ttu-id="31ade-101">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="31ade-101">Join-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="31ade-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31ade-102">SYNOPSIS</span></span>
<span data-ttu-id="31ade-103">Umożliwia dołączenie jednego lub kilku plików w celu utworzenia jednego pliku w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="31ade-103">Joins one or more files to create one file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31ade-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31ade-104">SYNTAX</span></span>

```
Join-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31ade-105">Opis</span><span class="sxs-lookup"><span data-stu-id="31ade-105">DESCRIPTION</span></span>
<span data-ttu-id="31ade-106">Polecenie cmdlet **Join-AzureRmDataLakeStoreItem** łączy jeden lub więcej plików, aby utworzyć jeden plik w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="31ade-106">The **Join-AzureRmDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="31ade-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31ade-107">EXAMPLES</span></span>

### <span data-ttu-id="31ade-108">Przykład 1. Dołącz do dwóch elementów</span><span class="sxs-lookup"><span data-stu-id="31ade-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="31ade-109">To polecenie umożliwia dołączenie File01.txt i File02.txt w celu utworzenia pliku CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="31ade-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="31ade-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31ade-110">PARAMETERS</span></span>

### <span data-ttu-id="31ade-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="31ade-111">-Account</span></span>
<span data-ttu-id="31ade-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="31ade-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="31ade-113">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="31ade-113">-Destination</span></span>
<span data-ttu-id="31ade-114">Określa ścieżkę usługi Data Lake Store dla połączonego elementu, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="31ade-114">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="31ade-115">-Force</span><span class="sxs-lookup"><span data-stu-id="31ade-115">-Force</span></span>
<span data-ttu-id="31ade-116">Wskazuje, że ta operacja może spowodować zastąpienie pliku docelowego, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="31ade-116">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="31ade-117">-Ścieżki</span><span class="sxs-lookup"><span data-stu-id="31ade-117">-Paths</span></span>
<span data-ttu-id="31ade-118">Określa tablicę ścieżek w usłudze Data Lake Store, które mają być połączone, począwszy od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="31ade-118">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31ade-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="31ade-119">-Confirm</span></span>
<span data-ttu-id="31ade-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31ade-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31ade-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31ade-121">-WhatIf</span></span>
<span data-ttu-id="31ade-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31ade-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31ade-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="31ade-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31ade-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ade-124">-DefaultProfile</span></span>
<span data-ttu-id="31ade-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31ade-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31ade-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ade-126">CommonParameters</span></span>
<span data-ttu-id="31ade-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31ade-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ade-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31ade-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ade-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31ade-129">INPUTS</span></span>

## <span data-ttu-id="31ade-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31ade-130">OUTPUTS</span></span>

### <span data-ttu-id="31ade-131">ciąg</span><span class="sxs-lookup"><span data-stu-id="31ade-131">string</span></span>
<span data-ttu-id="31ade-132">Pełna ścieżka do pliku wynikowego z dołączonych plików.</span><span class="sxs-lookup"><span data-stu-id="31ade-132">The full path to the resulting file from the joined files.</span></span>

## <span data-ttu-id="31ade-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31ade-133">NOTES</span></span>

## <span data-ttu-id="31ade-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31ade-134">RELATED LINKS</span></span>

[<span data-ttu-id="31ade-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="31ade-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="31ade-136">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="31ade-136">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="31ade-137">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="31ade-137">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="31ade-138">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="31ade-138">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="31ade-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="31ade-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="31ade-140">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="31ade-140">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


