---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 1d361149109b654cf3e7fa45e133b9daff84c21c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361165"
---
# <span data-ttu-id="c7fbf-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7fbf-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="c7fbf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7fbf-102">SYNOPSIS</span></span>
<span data-ttu-id="c7fbf-103">Umożliwia dołączenie jednego lub kilku plików w celu utworzenia jednego pliku w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c7fbf-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="c7fbf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7fbf-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7fbf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c7fbf-105">DESCRIPTION</span></span>
<span data-ttu-id="c7fbf-106">Polecenie cmdlet **Join-AzDataLakeStoreItem** łączy jeden lub więcej plików, aby utworzyć jeden plik w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c7fbf-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="c7fbf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7fbf-107">EXAMPLES</span></span>

### <span data-ttu-id="c7fbf-108">Przykład 1. Dołącz do dwóch elementów</span><span class="sxs-lookup"><span data-stu-id="c7fbf-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="c7fbf-109">To polecenie umożliwia dołączenie File01.txt i File02.txt w celu utworzenia pliku CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="c7fbf-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="c7fbf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7fbf-110">PARAMETERS</span></span>

### <span data-ttu-id="c7fbf-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="c7fbf-111">-Account</span></span>
<span data-ttu-id="c7fbf-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c7fbf-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c7fbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7fbf-113">-DefaultProfile</span></span>
<span data-ttu-id="c7fbf-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7fbf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7fbf-115">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="c7fbf-115">-Destination</span></span>
<span data-ttu-id="c7fbf-116">Określa ścieżkę usługi Data Lake Store dla połączonego elementu, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="c7fbf-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c7fbf-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c7fbf-117">-Force</span></span>
<span data-ttu-id="c7fbf-118">Wskazuje, że ta operacja może spowodować zastąpienie pliku docelowego, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="c7fbf-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="c7fbf-119">-Ścieżki</span><span class="sxs-lookup"><span data-stu-id="c7fbf-119">-Paths</span></span>
<span data-ttu-id="c7fbf-120">Określa tablicę ścieżek w usłudze Data Lake Store, które mają być połączone, począwszy od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="c7fbf-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c7fbf-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c7fbf-121">-Confirm</span></span>
<span data-ttu-id="c7fbf-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7fbf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7fbf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7fbf-123">-WhatIf</span></span>
<span data-ttu-id="c7fbf-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7fbf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7fbf-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c7fbf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7fbf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7fbf-126">CommonParameters</span></span>
<span data-ttu-id="c7fbf-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7fbf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7fbf-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7fbf-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7fbf-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7fbf-129">INPUTS</span></span>

### <span data-ttu-id="c7fbf-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c7fbf-130">System.String</span></span>

### <span data-ttu-id="c7fbf-131">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="c7fbf-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="c7fbf-132">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="c7fbf-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="c7fbf-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c7fbf-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c7fbf-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7fbf-134">OUTPUTS</span></span>

### <span data-ttu-id="c7fbf-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c7fbf-135">System.String</span></span>

## <span data-ttu-id="c7fbf-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7fbf-136">NOTES</span></span>

## <span data-ttu-id="c7fbf-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7fbf-137">RELATED LINKS</span></span>

[<span data-ttu-id="c7fbf-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7fbf-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="c7fbf-139">Eksportowanie — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7fbf-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="c7fbf-140">Import — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7fbf-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="c7fbf-141">Nowe — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7fbf-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="c7fbf-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7fbf-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="c7fbf-143">Test — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7fbf-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


