---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: da26deb246fc90a1b83b63c47560dd5912616d62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551899"
---
# <span data-ttu-id="89704-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="89704-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="89704-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89704-102">SYNOPSIS</span></span>
<span data-ttu-id="89704-103">Usuwa plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="89704-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89704-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89704-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Clean]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89704-105">Opis</span><span class="sxs-lookup"><span data-stu-id="89704-105">DESCRIPTION</span></span>
<span data-ttu-id="89704-106">Polecenie cmdlet **Remove-AzureRmDataLakeStoreItem** usuwa plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="89704-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="89704-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89704-107">EXAMPLES</span></span>

### <span data-ttu-id="89704-108">Przykład 1: usuwanie wielu elementów</span><span class="sxs-lookup"><span data-stu-id="89704-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="89704-109">To polecenie usuwa pliki File01.txt i File.csv z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="89704-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="89704-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89704-110">PARAMETERS</span></span>

### <span data-ttu-id="89704-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="89704-111">-Account</span></span>
<span data-ttu-id="89704-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="89704-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="89704-113">-Clean</span><span class="sxs-lookup"><span data-stu-id="89704-113">-Clean</span></span>
<span data-ttu-id="89704-114">Wskazuje, że ta operacja powoduje usunięcie całej zawartości folderu docelowego i zachowanie folderu.</span><span class="sxs-lookup"><span data-stu-id="89704-114">Indicates that this operation removes all of the contents of the target folder and retains the folder.</span></span>
<span data-ttu-id="89704-115">Ten parametr jest używany z parametrem *rekursywowanie* .</span><span class="sxs-lookup"><span data-stu-id="89704-115">Use this parameter with the *Recurse* parameter.</span></span>

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

### <span data-ttu-id="89704-116">-Force</span><span class="sxs-lookup"><span data-stu-id="89704-116">-Force</span></span>
<span data-ttu-id="89704-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="89704-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89704-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89704-118">-PassThru</span></span>
<span data-ttu-id="89704-119">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="89704-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="89704-120">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="89704-120">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89704-121">-Ścieżki</span><span class="sxs-lookup"><span data-stu-id="89704-121">-Paths</span></span>
<span data-ttu-id="89704-122">Określa tablicę ścieżek plików do usunięcia, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="89704-122">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89704-123">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="89704-123">-Recurse</span></span>
<span data-ttu-id="89704-124">Wskazuje, że ta operacja powoduje usunięcie wszystkich elementów w folderze docelowym, łącznie z podfolderami.</span><span class="sxs-lookup"><span data-stu-id="89704-124">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>
<span data-ttu-id="89704-125">Jeśli nie określono parametru *Clean* , folder docelowy również zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="89704-125">Unless you specify the *Clean* parameter, the target folder is also deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89704-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89704-126">-Confirm</span></span>
<span data-ttu-id="89704-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89704-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89704-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89704-128">-WhatIf</span></span>
<span data-ttu-id="89704-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89704-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89704-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="89704-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89704-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89704-131">-DefaultProfile</span></span>
<span data-ttu-id="89704-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89704-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89704-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89704-133">CommonParameters</span></span>
<span data-ttu-id="89704-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89704-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89704-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89704-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89704-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89704-136">INPUTS</span></span>

## <span data-ttu-id="89704-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89704-137">OUTPUTS</span></span>

### <span data-ttu-id="89704-138">logiczną</span><span class="sxs-lookup"><span data-stu-id="89704-138">bool</span></span>
<span data-ttu-id="89704-139">Jeśli PassThru jest określony, zwraca wynik operacji.</span><span class="sxs-lookup"><span data-stu-id="89704-139">If PassThru is specified, returns the result of the operation.</span></span>

## <span data-ttu-id="89704-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89704-140">NOTES</span></span>

## <span data-ttu-id="89704-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89704-141">RELATED LINKS</span></span>

[<span data-ttu-id="89704-142">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="89704-142">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="89704-143">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="89704-143">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="89704-144">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="89704-144">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="89704-145">Dołącz do AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="89704-145">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="89704-146">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="89704-146">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="89704-147">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="89704-147">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


