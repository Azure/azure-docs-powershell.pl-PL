---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: e8e90b6cca2808bbf2caee69ebef5582ed0f8c5b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194643"
---
# <span data-ttu-id="95b37-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95b37-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="95b37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95b37-102">SYNOPSIS</span></span>
<span data-ttu-id="95b37-103">Przenosi lub zmienia nazwę pliku lub folderu w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95b37-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="95b37-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="95b37-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95b37-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="95b37-105">DESCRIPTION</span></span>
<span data-ttu-id="95b37-106">Polecenie **cmdlet Move-AzDataLakeStoreItem** przenosi lub zmienia nazwę pliku lub folderu w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95b37-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="95b37-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="95b37-107">EXAMPLES</span></span>

### <span data-ttu-id="95b37-108">Przykład 1. Przenoszenie elementu i zmienianie jego nazwy</span><span class="sxs-lookup"><span data-stu-id="95b37-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="95b37-109">To polecenie zmieni nazwę elementu na File.txt RenamedFile.txt i przeniesie go do innego folderu.</span><span class="sxs-lookup"><span data-stu-id="95b37-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="95b37-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95b37-110">PARAMETERS</span></span>

### <span data-ttu-id="95b37-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="95b37-111">-Account</span></span>
<span data-ttu-id="95b37-112">Określa nazwę konta sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95b37-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="95b37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95b37-113">-DefaultProfile</span></span>
<span data-ttu-id="95b37-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="95b37-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95b37-115">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="95b37-115">-Destination</span></span>
<span data-ttu-id="95b37-116">Określa ścieżkę do usługi Data Lake Store, do której chcesz przenieść element, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="95b37-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="95b37-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="95b37-117">-Force</span></span>
<span data-ttu-id="95b37-118">Oznacza, że ta operacja może zastąpić plik docelowy, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="95b37-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="95b37-119">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="95b37-119">-Path</span></span>
<span data-ttu-id="95b37-120">Określa ścieżkę folderu Data Lake Store do przeniesienia lub zmiany nazwy, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="95b37-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="95b37-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95b37-121">-Confirm</span></span>
<span data-ttu-id="95b37-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="95b37-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95b37-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95b37-123">-WhatIf</span></span>
<span data-ttu-id="95b37-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95b37-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95b37-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="95b37-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95b37-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95b37-126">CommonParameters</span></span>
<span data-ttu-id="95b37-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95b37-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95b37-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95b37-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95b37-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95b37-129">INPUTS</span></span>

### <span data-ttu-id="95b37-130">System.String</span><span class="sxs-lookup"><span data-stu-id="95b37-130">System.String</span></span>

### <span data-ttu-id="95b37-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="95b37-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="95b37-132">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="95b37-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="95b37-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95b37-133">OUTPUTS</span></span>

### <span data-ttu-id="95b37-134">System.String</span><span class="sxs-lookup"><span data-stu-id="95b37-134">System.String</span></span>

## <span data-ttu-id="95b37-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="95b37-135">NOTES</span></span>

## <span data-ttu-id="95b37-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95b37-136">RELATED LINKS</span></span>

[<span data-ttu-id="95b37-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95b37-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="95b37-138">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95b37-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="95b37-139">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95b37-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="95b37-140">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95b37-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="95b37-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95b37-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="95b37-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95b37-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


