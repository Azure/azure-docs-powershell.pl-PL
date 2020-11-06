---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 40477ad0635f1b832e7d95e459b27102dc68f8db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525141"
---
# <span data-ttu-id="e868a-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e868a-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="e868a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e868a-102">SYNOPSIS</span></span>
<span data-ttu-id="e868a-103">Usuwa plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e868a-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e868a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e868a-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Clean]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e868a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e868a-105">DESCRIPTION</span></span>
<span data-ttu-id="e868a-106">Polecenie cmdlet **Remove-AzureRmDataLakeStoreItem** usuwa plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e868a-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e868a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e868a-107">EXAMPLES</span></span>

### <span data-ttu-id="e868a-108">Przykład 1: usuwanie wielu elementów</span><span class="sxs-lookup"><span data-stu-id="e868a-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="e868a-109">To polecenie usuwa pliki File01.txt i File.csv z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e868a-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="e868a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e868a-110">PARAMETERS</span></span>

### <span data-ttu-id="e868a-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="e868a-111">-Account</span></span>
<span data-ttu-id="e868a-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e868a-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e868a-113">-Clean</span><span class="sxs-lookup"><span data-stu-id="e868a-113">-Clean</span></span>
<span data-ttu-id="e868a-114">Wskazuje, że użytkownik chce usunąć całą zawartość folderu, ale nie sam folder.</span><span class="sxs-lookup"><span data-stu-id="e868a-114">Indicates the user wants to remove all of the contents of the folder, but not the folder itself</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e868a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e868a-115">-DefaultProfile</span></span>
<span data-ttu-id="e868a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e868a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e868a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e868a-117">-Force</span></span>
<span data-ttu-id="e868a-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e868a-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e868a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e868a-119">-PassThru</span></span>
<span data-ttu-id="e868a-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e868a-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e868a-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e868a-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e868a-122">-Ścieżki</span><span class="sxs-lookup"><span data-stu-id="e868a-122">-Paths</span></span>
<span data-ttu-id="e868a-123">Określa tablicę ścieżek plików do usunięcia, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="e868a-123">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e868a-124">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="e868a-124">-Recurse</span></span>
<span data-ttu-id="e868a-125">Wskazuje, że ta operacja powoduje usunięcie wszystkich elementów w folderze docelowym, łącznie z podfolderami.</span><span class="sxs-lookup"><span data-stu-id="e868a-125">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>
<span data-ttu-id="e868a-126">Jeśli nie określono parametru *Clean* , folder docelowy również zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="e868a-126">Unless you specify the *Clean* parameter, the target folder is also deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e868a-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e868a-127">-Confirm</span></span>
<span data-ttu-id="e868a-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e868a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e868a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e868a-129">-WhatIf</span></span>
<span data-ttu-id="e868a-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e868a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e868a-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e868a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e868a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e868a-132">CommonParameters</span></span>
<span data-ttu-id="e868a-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e868a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e868a-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e868a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e868a-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e868a-135">INPUTS</span></span>

### <span data-ttu-id="e868a-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e868a-136">None</span></span>
<span data-ttu-id="e868a-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e868a-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e868a-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e868a-138">OUTPUTS</span></span>

### <span data-ttu-id="e868a-139">logiczną</span><span class="sxs-lookup"><span data-stu-id="e868a-139">bool</span></span>
<span data-ttu-id="e868a-140">Jeśli PassThru jest określony, zwraca wynik operacji.</span><span class="sxs-lookup"><span data-stu-id="e868a-140">If PassThru is specified, returns the result of the operation.</span></span>

## <span data-ttu-id="e868a-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e868a-141">NOTES</span></span>

## <span data-ttu-id="e868a-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e868a-142">RELATED LINKS</span></span>

[<span data-ttu-id="e868a-143">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e868a-143">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e868a-144">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e868a-144">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e868a-145">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e868a-145">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e868a-146">Dołącz do AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e868a-146">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e868a-147">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e868a-147">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e868a-148">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e868a-148">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


