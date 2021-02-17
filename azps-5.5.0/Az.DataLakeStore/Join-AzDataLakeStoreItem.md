---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 1d361149109b654cf3e7fa45e133b9daff84c21c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188587"
---
# <span data-ttu-id="ec88c-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ec88c-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="ec88c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec88c-102">SYNOPSIS</span></span>
<span data-ttu-id="ec88c-103">Dołącza jeden lub więcej plików, aby utworzyć jeden plik w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec88c-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="ec88c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ec88c-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec88c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ec88c-105">DESCRIPTION</span></span>
<span data-ttu-id="ec88c-106">Polecenie cmdlet **Join-AzDataLakeStoreItem** łączy jeden lub więcej plików w celu utworzenia jednego pliku w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec88c-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="ec88c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ec88c-107">EXAMPLES</span></span>

### <span data-ttu-id="ec88c-108">Przykład 1. Sprzężenia dwóch elementów</span><span class="sxs-lookup"><span data-stu-id="ec88c-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="ec88c-109">To polecenie łączy File01.txt i File02.txt, aby utworzyć plik CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="ec88c-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="ec88c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec88c-110">PARAMETERS</span></span>

### <span data-ttu-id="ec88c-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="ec88c-111">-Account</span></span>
<span data-ttu-id="ec88c-112">Określa nazwę konta w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec88c-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ec88c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec88c-113">-DefaultProfile</span></span>
<span data-ttu-id="ec88c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec88c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec88c-115">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="ec88c-115">-Destination</span></span>
<span data-ttu-id="ec88c-116">Określa ścieżkę sklepu Data Lake Store dla połączonego elementu, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="ec88c-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ec88c-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ec88c-117">-Force</span></span>
<span data-ttu-id="ec88c-118">Oznacza, że ta operacja może zastąpić plik docelowy, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="ec88c-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="ec88c-119">— Ścieżki</span><span class="sxs-lookup"><span data-stu-id="ec88c-119">-Paths</span></span>
<span data-ttu-id="ec88c-120">Określa tablicę ścieżek do plików do połączenia w sklepie Data Lake Store, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="ec88c-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ec88c-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ec88c-121">-Confirm</span></span>
<span data-ttu-id="ec88c-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ec88c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec88c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec88c-123">-WhatIf</span></span>
<span data-ttu-id="ec88c-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec88c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec88c-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ec88c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec88c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec88c-126">CommonParameters</span></span>
<span data-ttu-id="ec88c-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec88c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec88c-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec88c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec88c-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec88c-129">INPUTS</span></span>

### <span data-ttu-id="ec88c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ec88c-130">System.String</span></span>

### <span data-ttu-id="ec88c-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span><span class="sxs-lookup"><span data-stu-id="ec88c-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="ec88c-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="ec88c-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="ec88c-133">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="ec88c-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ec88c-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ec88c-134">OUTPUTS</span></span>

### <span data-ttu-id="ec88c-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ec88c-135">System.String</span></span>

## <span data-ttu-id="ec88c-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ec88c-136">NOTES</span></span>

## <span data-ttu-id="ec88c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec88c-137">RELATED LINKS</span></span>

[<span data-ttu-id="ec88c-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ec88c-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="ec88c-139">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ec88c-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="ec88c-140">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ec88c-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="ec88c-141">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ec88c-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="ec88c-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ec88c-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="ec88c-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ec88c-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


